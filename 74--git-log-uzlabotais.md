# Git Log (uzlabotais)

Tātad nedaudz uzlaboju [jau uzlabotu](http://www.jukie.net/bart/blog/pimping-out-git-log) [git log](http://www.kernel.org/pub/software/scm/git/docs/git-log.html) komandu. :)

![git log](http://i.imgur.com/ViaMy.png "git log")

P.S. Attēlā ir redzama [python-markdown2 repo](https://github.com/trentm/python-markdown2).

Lai iegūtu šo formatējumu:

~~~
git config --global alias.lg "log --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr)%Creset %Cblue<%an>%Creset' --abbrev-commit --date=relative"
~~~

...un izsaucam to ar `git lg` (ne `git log`).

Ja vēlaties, varat arī izdarīt tā — komanda `lg` izsauks attiecīgo, jau formatēto `git log`. Tikai uzmanieties, lai nebūtu alias konflikti!

Atveram `~/.bashrc` un pievienojam šo:

~~~
alias lg="git log --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr)%Creset %Cblue<%an>%Creset' --abbrev-commit --date=relative"
~~~

Tad izpildam šo komandu (lai izmaiņas sāktu darboties):

~~~
source ~/.bashrc
~~~