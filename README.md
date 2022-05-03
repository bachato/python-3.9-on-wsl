# Upgrade python-3.9-on-wsl

Update package lists

```
sudo apt update
```

Download python binary

```
wget https://www.python.org/ftp/python/3.9.1/Python-3.9.1.tgz
```

Unzip

```
tar -xzf Python-3.9.1.tgz
```

Configure

```
cd Python-3.9.1

./configure --enable-optimizations
```

Build

```
make -j 2
```

Install
```
sudo make install
```

Make Python 3.9 default
- Change ~/.bashrc file to add `alias python='/usr/local/bin/python3.9'` 
- Run `source ~/.bashrc`

Verify the installation `python --version`




