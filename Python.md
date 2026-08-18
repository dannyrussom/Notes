## Python with pyenv

- first build the dependencies:

sudo apt update

sudo apt install -y \
    build-essential \
    curl \
    git \
    libssl-dev \
    zlib1g-dev \
    libbz2-dev \
    libreadline-dev \
    libsqlite3-dev \
    libncursesw5-dev \
    xz-utils \
    tk-dev \
    libxml2-dev \
    libxmlsec1-dev \
    libffi-dev \
    liblzma-dev

- then install pyenv:

curl https://pyenv.run | bash


- then add it to the shell:

echo 'export PYENV_ROOT="$HOME/.pyenv"' >> ~/.bashrc
echo '[[ -d $PYENV_ROOT/bin ]] && export PATH="$PYENV_ROOT/bin:$PATH"' >> ~/.bashrc
echo 'eval "$(pyenv init - bash)"' >> ~/.bashrc


- then reload shell:

source ~/.bashrc


- see available Python versions:

pyenv install --list


- For example, install Python 3.11 and 3.12:

pyenv install 3.11.9
pyenv install 3.12.3


- Check what you have:

pyenv versions

- make one version the default:

pyenv global 3.12.3


- choose a version only for a particular project:

cd ~/Documents/2_Projects/Pose_Estimation
pyenv local 3.11.9


- check version:

python --version


- create a virtual environment:

python -m venv venv
source venv/bin/activate
