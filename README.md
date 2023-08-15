# Pybase

## Install Python

### MACOS

```sh
brew install pyenv
pyenv versions
pyenv install --list | grep 11
brew install xz # fixed missing lib when install python using pyenv
pyenv install 3.11.4
pyenv global 3.11.4
```

- Add **"eval "$(pyenv init --path)"** to **"/.zprofile"**

```cnf
# Setting PATH for Python 3.11
# The original version is saved in .zprofile.pysave
# PATH="/Library/Frameworks/Python.framework/Versions/3.11/bin:${PATH}"

# Setting PATH for pyenv
eval "$(pyenv init --path)"
```

```sh
which python
which python3
which pip
```

#### Install pipenv

```sh
pip3 install --user pipenv
```

.zprofile

```cfg
# Setting pip packages
export PYTHONUSERBASE="$HOME/.local"
PATH="$PYTHONUSERBASE/bin:${PATH}"
```

```sh
source ~/.zprofile
which pipenv
```

#### Use pipenv

```sh
# activate
pipenv shell
# install dependencies
pipenv install
```
