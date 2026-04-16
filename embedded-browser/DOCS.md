# Home Assistant Bigmoby Application: Epiphany embedded browser

> **Note:** Direct VNC access (port 5900) is not password-protected by default. Set a `vnc_password` in the add-on configuration to enable VNC authentication.

## Technical Architecture

Under the hood, this add-on runs a complete lightweight desktop environment inside a container, translating the visual output to your web browser. Here is the step-by-step process of how it works:

1. **Process Manager (s6-overlay)**: Docker containers are typically designed for single processes. Since this add-on requires multiple services, it uses `s6-overlay` as an init system to launch and supervise the display server, window manager, browser, and network bridge simultaneously.
2. **Virtual Display Server (Xtigervnc)**: Without a physical monitor, the add-on runs `tigervncserver` to create an X11 virtual display (`:0`). All applications draw their graphical interfaces onto this virtual screen, which is exposed internally via the VNC protocol on port `5900` (secured with `VncAuth` if a password is set).
3. **Window Manager (Openbox)**: A lightweight window manager (`openbox`) is started to handle application framing. Scripts using `xdotool` and `wmctrl` automatically intercept the browser window and force it to be fullscreen and maximized without any borders.
4. **Browser Engine (Epiphany & D-Bus)**: Before the browser starts, a system `dbus-daemon` is launched to support modern Linux IPC communications. Then, **Epiphany** (the official GNOME WebKit-based browser) is executed, drawing its content to the `:0` virtual display and connecting to your target `start_url`.
5. **WebSocket Bridge (Websockify)**: A standard web browser cannot understand raw VNC TCP traffic. **Websockify** is used as a bridge to wrap the raw VNC data from port `5900` into a WebSocket stream exposed on local port `5901`.
6. **Frontend Interface (noVNC & Ingress)**: Finally, a lightweight web server (**NGINX**) handles the Home Assistant Ingress connection on port `8099`. When you open the add-on UI, it serves `ingress.html` which loads the **noVNC** JavaScript library. noVNC connects to the WebSocket stream and renders the remote desktop directly onto an HTML5 `<canvas>` in your browser, seamlessly capturing your local mouse and keyboard inputs and sending them back to the isolated Epiphany browser.

## Authors & contributors

The original setup of this repository is by [Fabio Mauro][bigmoby].

## License

MIT License

Copyright (c) 2026 Fabio Mauro

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

[bigmoby]: https://github.com/bigmoby
[original_project]: https://github.com/hassio-addons/addon-embedded-browser
[contributors]: https://github.com/bigmoby/addon-embedded-browser/graphs/contributors
