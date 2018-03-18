 # backend
brew install pyenv
pyenv install 3.6.4
cd /Users/yalla/personal/sahityam/backend
/Users/yalla/.pyenv/versions/3.6.4/bin/python3 -m venv virtual_environment
source virtual_environment/bin/activate
pip install django (at this point pip version is 9.0.2)
python -m django --version  (2.0.3)


Add a new ssh key
ssh-add <id_rsa> file of the new identity
change the .ssh/config to 

Host github-personal
        HostName github.com
        PreferredAuthentications publickey
        IdentityFile ~/.ssh/yagnasri/id_rsa

Host github.com
        HostName github.com
        PreferredAuthentications publickey
        IdentityFile ~/.ssh/id_rsa


//Change the git config should look like this
[core]
        repositoryformatversion = 0
        filemode = true
        bare = false
        logallrefupdates = true
        ignorecase = true
        precomposeunicode = true
[branch "master"]
[remote "origin"]
        url = git@github-personal:sahityam-telugu/backend.git
        fetch = +refs/heads/*:refs/remotes/origin/*
