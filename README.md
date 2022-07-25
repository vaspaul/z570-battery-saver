# z570-battery-saver

> Lenovo Ideapad z570 Battery Manager for Linux

**z570-battery-saver** allows managing Lenovo Ideapad's firmware on the battery
and shifts between the usual charging thresholds from 100% to 50%.
In some cases, not charging the battery to 100% constantly may improve
the overall lifespan of the battery. This setting is suggested for a system
that is always plugged into the AC adapter.


## Installation

The standard `make install` routine is used.

The following additional variables are supported:
- `DESTDIR` -- determines environment for staged installs,
- `PREFIX`  -- determines where the script will be installed (default: `/usr/local`).

### Installation script:

```shell
wget https://github.com/vaspaul/z570-battery-saver/releases/download/v1.0/z570-battery-saver-v1_0.zip
unzip z570-battery-saver-v1_0.zip
cd z570-battery-saver-main
sudo make install
```

## Requirements

The script requires the following to run:
- `bash`
- `linux >= 4.14`
- `acpi-call-dkms`


## Usage

Run: `z570-battery-saver [operation]`

| Operation        | Description                                              |
| :--------------- | :------------------------------------------------------- |
| `-h`, `--help`     |  Show help message.                                      |
| `-v`, `--version`  |  Show script version.                                    |
| `-s`, `--status`   |  Show battery protection status.                         |
| `-e`, `--enable`   |  Enable battery protection (charge level 50%).           |
| `-d`, `--disable`  |  Disable battery protection (charge level 100%).         |
| `--clbr_start`     |  Start battery calibration.                              |
| `--clbr_stop`      |  Stop battery calibration.                               |

## License

See the [LICENSE](LICENSE) file for details.
