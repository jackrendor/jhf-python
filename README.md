# Jack Hash Finder
Quick lookup for the original value of an hash

# Purpose
I was tired of looking up for common hashes values by hand. During CTFs you will eventually encounter some hashes. Instead of cracking them on your local machine or fire up a browser and look it up, the script does it for you. It tryies some services to see if it's a common and known hash.

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

Then you're ready to go. Simply execute the `jhf` file:

```bash
./jhf 21232f297a57a5a743894a0e4a801fc3
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
