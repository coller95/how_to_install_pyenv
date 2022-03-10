# how_to_install_pyenv



//////////////////
// pyenv installation
//////////////////
---install curl,git---
```console
sudo apt -y install -y curl git
```
---install pyenv---
```console
curl https://pyenv.run | bash
```
--append to ~/.bashrc--
```console
echo 'export PATH="/home/ubuntu/.pyenv/bin:$PATH"' >> ~/.bashrc 
echo 'eval "$(pyenv init --path)"' >> ~/.bashrc 
echo 'eval "$(pyenv init -)"' >> ~/.bashrc 
echo 'eval "$(pyenv virtualenv-init -)"' >> ~/.bashrc 
echo 'export PYENV_VIRTUALENV_DISABLE_PROMPT=1' >> ~/.bashrc 
```

```console
source ~/.bashrc
```

--install dependency--
```console
sudo apt-get install -y make build-essential libssl-dev zlib1g-dev libbz2-dev \
libreadline-dev libsqlite3-dev wget curl llvm libncurses5-dev libncursesw5-dev \
xz-utils tk-dev libffi-dev liblzma-dev python-openssl git
```

```console
env PYTHON_CONFIGURE_OPTS="--enable-shared" pyenv install --force 3.6.9 -v
pyenv global 3.6.9
```
