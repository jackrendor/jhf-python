<p align="center">
    <img src="logo.png">
</p>

# Jack Hash Finder
Quick lookup for the original value of an hash

# DEPRECATED
This repository is deprecated, go for the new version of jhf: [https://github.com/jackrendor/jhf](https://github.com/jackrendor/jhf)

# Purpose
I was tired of looking up for common hashes values by hand. During CTFs you will eventually encounter some hashes. Instead of cracking them on your local machine or fire up a browser and look it up, the script does it for you. It tries some services to see if it's a common and known hash.

# Supported hashes
| Type   | Support |
|:------:|:-------:|
| MySQL  | weak    |
| NTLM   | weak    |
| md5    | strong  |
| sha1   | strong  |
| sha256 | strong  |
| sha384 | strong  |
| sha512 | strong  |

# Video Demonstration

[![asciicast](https://asciinema.org/a/K6GPiBw9iNU0lq2P2Da2yEF0j.svg)](https://asciinema.org/a/K6GPiBw9iNU0lq2P2Da2yEF0j)

# Configure
Based on your distro, you should install first some dependencies.

### Debian / Ubuntu
`sudo apt install python3 python3-virtualenv`
### Fedora / RedHat
`sudo dnf install python3 python3-virtualenv`

Then simply execute the `configure.sh` file

```bash
bash configure.sh
```

or

```bash
./configure
```

Then you're ready to go. Simply execute the `jhf` file. You can pass the hash as argument:

```bash
./jhf 21232f297a57a5a743894a0e4a801fc3
```
You can specify more than one hash
```bash
./jhf b3ddbc502e307665f346cbd6e52cc10d 0bc11f2f3279555c317be9cf9e52645a
```
Or you can read from file by using `-f` or `--file`
```bash
./jhf -f report/hashes.txt
./jhf --file report/hashes.txt
```

### No virtualenv
In case you don't want to use a virtual environment **(which I discourage)**, install the python dependencies as user:
```bash
pip3 install --user -r ./requirements.txt
```
and DO NOT USE the `jhf` script. Just use the Python one:
```bash
python3 jhf.py
```
