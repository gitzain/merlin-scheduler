# merlin-scheduler
Simplify scheduling scripts on your Asuswrt-Merlin based router. Just drop your bash script in the designated folder for your desired interval (minute, half-hour, hour, or day) and merlin-merlin-scheduler takes care of the rest.

The project includes bash scripts to capture and send vital information from the Asuswrt-Merlin router to InfluxDB to be displayed in Grafana.

## Table of content
- [Motivation](#motivation)
- [Installation \& Usage](#installation--usage)
    - [Installation](#installation)
    - [Usage](#usage)
- [Contributing](#contributing)
- [History](#history)
- [Credits](#credits)
- [License](#license)

## Motivation
I was tired of manually running scripts to monitor my Asuswrt-Merlin router. I wanted a simpler way to track things like ping times, internet speeds, and connected devices. This project automates scheduling those scripts and the default scripts integrate with InfluxDB and Grafana, giving me a clean and easy-to-read dashboard of network's health.

## Installation & Usage

### Installation
1. Download the files in this project
2. scp the entire contents of the src folder to /jffs (scp -rp src/* <router username>@<IP to router>:/jffs/scripts)
3. Make all files executable (chmod -R a+rx /jffs/scripts/*)
4. Reboot your router

### Usage
Write your bash script and simply drop it into the appropriate folder. For example if i wanted the scrip to run every minute i would need to drop it into /jffs/scripts/merlin-scheduler/minute

## Contributing
1. Fork it!
2. Create your feature branch: `git checkout -b my-new-feature`
3. Commit your changes: `git commit -am 'Add some feature'`
4. Push to the branch: `git push origin my-new-feature`
5. Submit a pull request :D

## History
v0.1: Beta

## Credits
- Inspired by <a href="https://github.com/gitzain/merlin-scheduler">merlin-scheduler</a>.
- Template for this README is <a href="https://github.com/gitzain/template-README">Template-README</a> created by <a href="https://iamzain.com">Zain Khan</a>

## License
See the LICENSE file in this project's directory.
