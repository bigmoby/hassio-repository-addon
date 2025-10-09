# Home Assistant Bigmoby Add-ons

![Project Stage][project-stage-shield]
![Maintenance][maintenance-shield]
[![License][license-shield]](LICENSE.md)

## About

Home Assistant allows anyone to create add-on repositories to share their
add-ons for Home Assistant easily. This repository is one of those repositories,
providing extra Home Assistant add-ons for your installation.

The primary goal of this project is to provide you (as a Home Assistant user)
with additional, high quality, add-ons that allow you to take your automated
home to the next level.

## Installation

Adding this add-ons repository to your Home Assistant instance is pretty easy. In the
Home Assistant add-on store, a possibility to add a repository is provided.

Use the following URL to add this repository:

```txt
https://github.com/bigmoby/hassio-repository-addon
```

## Add-ons provided by this repository

### &#10003; [WireGuard Client][addon-wireguard-client]

![Latest Version][wireguard-client-version-shield]
![Supports aarch64 Architecture][wireguard-client-aarch64-shield]
![Supports amd64 Architecture][wireguard-client-amd64-shield]

Fast, modern, secure VPN tunnel

[:books: WireGuard add-on documentation][addon-doc-wireguard-client]


### &#10003; [Surf embedded browser][addon-embedded-browser]

![Latest Version][embedded-browser-version-shield]
![Supports aarch64 Architecture][embedded-browser-aarch64-shield]
![Supports amd64 Architecture][embedded-browser-amd64-shield]
![Supports armv7 Architecture][embedded-browser-armv7-shield]

[WARNING] Please DO NOT use this add-on unless you really KNOW what you are doing! It is in a very early stage of development. [WARNING]

[:books: Surf embedded browser add-on documentation][addon-doc-embedded-browser]

## Releases

Releases are based on [Semantic Versioning][semver], and use the format
of ``MAJOR.MINOR.PATCH``. In a nutshell, the version will be incremented
based on the following:

- ``MAJOR``: Incompatible or major changes.
- ``MINOR``: Backwards-compatible new features and enhancements.
- ``PATCH``: Backwards-compatible bugfixes and package updates.

## Support

You could also open an issue here on GitHub. Note, we use a separate
GitHub repository for each add-on. Please ensure you are creating the issue
on the correct GitHub repository matching the add-on.

- [Open an issue for the add-on: WireGuard][wireguard-client-issue]
- [Open an issue for the add-on: Firefox embedded browser][embedded-browser-issue]

For a general repository issue or add-on ideas [open an issue here][issue]

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

## Adding a new add-on

We are currently not accepting third party add-ons to this repository.

For questions, please contact [Fabio Mauro][bigmoby]:

- Message him via the LinkedIn: [fabiomauro][https://www.linkedin.com/in/fabiomauro/]

## License

MIT License

Copyright (c) 2020-2025 Fabio Mauro

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


[addon-wireguard-client]: https://github.com/bigmoby/addon-wireguard-client
[addon-doc-wireguard-client]: https://github.com/bigmoby/addon-wireguard-client/blob/main/README.md
[wireguard-client-issue]: https://github.com/bigmoby/addon-wireguard-client/issues
[wireguard-client-version-shield]: https://img.shields.io/github/v/release/bigmoby/addon-wireguard-client.svg
[wireguard-client-aarch64-shield]: https://img.shields.io/badge/aarch64-yes-green.svg
[wireguard-client-amd64-shield]: https://img.shields.io/badge/amd64-yes-green.svg

[addon-embedded-browser]: https://github.com/bigmoby/addon-embedded-browser
[addon-doc-embedded-browser]: https://github.com/bigmoby/addon-embedded-browser/blob/main/README.md
[embedded-browser-issue]: https://github.com/bigmoby/addon-embedded-browser/issues
[embedded-browser-version-shield]: https://img.shields.io/github/v/release/bigmoby/addon-embedded-browser.svg
[embedded-browser-aarch64-shield]: https://img.shields.io/badge/aarch64-yes-green.svg
[embedded-browser-amd64-shield]: https://img.shields.io/badge/amd64-yes-green.svg
[embedded-browser-armhf-shield]: https://img.shields.io/badge/armhf-yes-green.svg
[embedded-browser-i386-shield]: https://img.shields.io/badge/i386-yes-green.svg
[embedded-browser-armv7-shield]: https://img.shields.io/badge/armv7-yes-green.svg

[awesome-shield]: https://img.shields.io/badge/awesome%3F-yes-brightgreen.svg
[awesome]: https://awesome-ha.com

[bigmoby]: https://github.com/bigmoby

[issue]: https://github.com/hassio-addons/repository/issues
[license-shield]: https://img.shields.io/github/license/bigmoby/hassio-repository-addon.svg
[maintenance-shield]: https://img.shields.io/maintenance/yes/2025.svg
[project-stage-shield]: https://img.shields.io/badge/project%20stage-production%20ready-brightgreen.svg

[semver]: http://semver.org/spec/v2.0.0.html
