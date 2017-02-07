Q:Server aborted the SSL handshake on Mac

A1:upgrade curl
    brew install curl

A2:change to ssh way.
    1､You can see how to connecting to github with ssh by the following website:https://help.github.com/articles/connecting-to-github-with-ssh/

        1)ssh-keygen -t rsa -b 4096 -C "your_git_account_email@example.com"
        2)eval "$(ssh-agent -s)"
        3)ssh-add ~/.ssh/${id_rsa}
            id_rsa is the default name, if u change the ssh-keygen file name use that name
        4)add the new ssh key to github account-----setting----ssh and gpg keys-----new ssh key----add ssh key
        5)ssh -T git@github.com
        ###////test
    2､If the repository is switching from https to ssh,change it.
        1)git remote -v
        2)git remote set-url ssh git address
            for example:
                git remote set-url origin git@github.com:USERNAME/OTHERREPOSITORY.git
