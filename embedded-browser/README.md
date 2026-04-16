# Home Assistant Bigmoby Add-on: Epiphany embedded browser

[![GitHub Release][releases-shield]][releases]
![Project Stage][project-stage-shield]
[![License][license-shield]](LICENSE.md)

![Maintenance][maintenance-shield]
[![GitHub Activity][commits-shield]][commits]

Epiphany embedded browser.

## About

> **Note:** Direct VNC access (port 5900) is not password-protected by default. Set a `vnc_password` in the add-on configuration to enable VNC authentication.


## Local development — known issues

### Add-on installation blocked — `docker_gateway_unprotected`

The Supervisor blocks job execution because the Docker gateway is not secured. This is the expected behavior in a devcontainer environment (Docker-in-Docker). Run this command once after the container starts to unblock the add-on installation:

```bash
ha jobs options --ignore-conditions healthy
```

> **Note:** this setting is not persistent and must be re-applied every time the devcontainer is restarted.

## Contributing

This is an active open-source project. We are always open to people who want to
use the code or contribute to it.

We have set up a separate document containing our
[contribution guidelines](CONTRIBUTING.md).

Thank you for being involved! :heart_eyes:

## Sponsor

Please, if You want support this kind of projects:

<a href="https://www.buymeacoffee.com/bigmoby" target="_blank"><img src="https://www.buymeacoffee.com/assets/img/custom_images/orange_img.png" alt="Buy Me A Coffee" style="height: 41px !important;width: 174px !important;box-shadow: 0px 3px 2px 0px rgba(190, 190, 190, 0.5) !important;-webkit-box-shadow: 0px 3px 2px 0px rgba(190, 190, 190, 0.5) !important;" ></a>

Many Thanks,

Fabio Mauro

## Authors & contributors

Fabio Mauro

For a full list of all authors and contributors,
check [the contributor's page][contributors].

## License

MIT License

Copyright (c) 2023-2026 Fabio Mauro

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


[contributors]: https://github.com/bigmoby/addon-embedded-browser/graphs/contributors
[aarch64-shield]: https://img.shields.io/badge/aarch64-yes-green.svg
[amd64-shield]: https://img.shields.io/badge/amd64-yes-green.svg
[commits-shield]: https://img.shields.io/github/commit-activity/y/hassio-addons/addon-embedded-browser.svg
[commits]: https://github.com/bigmoby/addon-embedded-browser/commits/main
[docs]: https://github.com/bigmoby/addon-embedded-browser/blob/master/embedded-browser/DOCS.md
[issue]: https://img.shields.io/github/issues/bigmoby/addon-embedded-browser.svg
[license-shield]: https://img.shields.io/github/license/bigmoby/addon-embedded-browser.svg
[maintenance-shield]: https://img.shields.io/maintenance/yes/2026.svg
[project-stage-shield]: https://img.shields.io/badge/project%20stage-under%20development-brightgreen.svg
[reddit]: https://reddit.com/r/homeassistant
[releases-shield]: https://img.shields.io/github/release/bigmoby/addon-embedded-browser.svg
[releases]: https://github.com/bigmoby/addon-embedded-browser/releases
[repository]: https://github.com/bigmoby/hassio-repository-addon

