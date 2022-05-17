# Upgrade python-3.9.12-on-wsl2

Below are the steps for installing python on wsl2 from source code.

Update package lists

```
sudo apt update
sudo apt upgrade
sudo apt install build-essential zlib1g-dev libncurses5-dev libgdbm-dev libnss3-dev libssl-dev libreadline-dev libffi-dev wget
```

Create a temp directory and download the python source code

```
mkdir ~/tmp
cd ~/tmp
wget https://www.python.org/ftp/python/3.9.12/Python-3.9.12.tgz
```

Unzip

```
tar -xvzf Python-3.9.12.tgz
```

Configure

```
cd Python-3.9.12
./configure
```

Install
```
sudo make altinstall
```

Check the install
```
python3.9 --version
```

You should see => Python 3.9.12

Make Python 3.9 default
- Change ~/.bashrc file to add `alias python='/usr/local/bin/python3.9'` 
- Run `source ~/.bashrc`

Verify the installation `python --version`




