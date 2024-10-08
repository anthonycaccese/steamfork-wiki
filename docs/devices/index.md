# :material-television: Device Support

## Tested devices

SteamFork has been tested (i.e. booted at least once) on the list of devices below marked sponsored and verified.  Devices with a sponsor are actively tested and used with SteamFork frequently.  Devices without a sponsor are not actively maintained and may have unknown issues. While untested, modern laptops, desktops, and mini PCs with Intel or AMD should not have any issues.

| Manufacturer | Product | Sponsor <sup>1</sup> |
| -- | -- | -- |
| Anbernic | Win600 | [uejji](https://github.com/uejji) |
| ANTEC | Core HS <sup>2</sup> | [Fewtarius](https://github.com/fewtarius) |
| ASUS | ROG Ally / Ally X | [flukejones](https://github.com/flukejones) |
| Atari | VCS | [Fewtarius](https://github.com/fewtarius) |
| AYANEO | 1S <sup>2</sup> | Community Verified |
| AYANEO | 2 | Community Verified |
| AYANEO | 2021 / Pro / Retro Power | Unsponsored |
| AYANEO | 2S <sup>2</sup> | [Fewtarius](https://github.com/fewtarius) |
| AYANEO | Air / Air Pro | [Fewtarius](https://github.com/fewtarius) |
| AYANEO | Air Plus | [Fewtarius](https://github.com/fewtarius) |
| AYANEO | Flip DS <sup>2</sup> | Unsponsored |
| AYANEO | Flip KB <sup>2</sup> | [Fewtarius](https://github.com/fewtarius) |
| AYANEO | Founder Edition | Unsponsored |
| AYANEO | Geek | Unsponsored |
| AYANEO | Next, Next Pro | Community Verified |
| AYANEO | Slide <sup>2</sup> | [Fewtarius](https://github.com/fewtarius) |
| Ayn | Loki Max | [Fewtarius](https://github.com/fewtarius) |
| Ayn | Loki Zero | Community Verified |
| GPD | Win 4 | [anthonycaccese](https://github.com/anthonycaccese) |
| GPD | Win Mini | Community Verified |

!!! info
    - 1. Sponsored devices are fully supported by its maintainer.  Support for unsponsored and community verified devices may vary.<br>
    - 2. New AMD 7000 series devices do not support S3 sleep and must be configured for Modern Standby + s0i3.  This setting is locked down on many Ayaneo devices and must be enabled using a third party helper.  Follow the [process on the Wiki](https://wiki.steamfork.org/troubleshooting/#enabling-modern-sleep-on-7000-series-amd-based-devices) to configure your device.

## Sponsoring a device

### Sponsorship
Sponsoring a device is a commitment to maintaining support for your device by validating, testing, and bugfixing any issues that may arise.  Adding support for a device's basic features is straight forward, however, it can become far more technical to add support for features such as fan control.  If you are interested in sponsoring your device, follow the process below.

1. Create a GitHub account if you do not already have one.
2. Boot the SteamFork installation image.
3. Create a device quirk using the [quirk creation tool](https://wiki.steamfork.org/contribute/quirks/) included with the distribution.  Minimum requirements are gamescope resolution, and rotation if needed.
4. Create a pull request to the [SteamFork Device Support](https://github.com/SteamFork/distribution/tree/main/PKGBUILD/steamfork-device-support) package with your new addition.
5. Open and take ownership of any issues specific to your device on the [SteamFork Bug Tracker](https://github.com/SteamFork/bugtracker).
6. When ready to begin sunsetting support for your device, generate and PR new quirk with the `--supported false` property.
