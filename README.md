To obtain the hosted site on your local computer,

`mkdir [folder name]`
`git init`
`git remote add live ssh://utk@apphost.ocf.berkeley.edu/home/u/ut/utk/public_html`
`git pull live +master:refs/head/master`


Then to update the site from your local computer,

`git push live +master:refs/head/master`


If you want to log in without a password,

`if [ ! -d ~/.ssh ]; then mkdir ~/.ssh; fi`
ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
ssh utk@apphost.ocf.berkeley.edu 'cat >> ~/.ssh/authorized_keys' < ~/.ssh/id_rsa.pub
