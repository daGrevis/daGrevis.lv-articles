# Skype uz Fedora 17 (64 biti)

Šo programmu kā tādu uzinstalēt Linux vidē ir nedaudz āķīgi... tāpēc šeit ir īsa pamācība. :)

Izveidojam failu `/etc/yum/repos.d/skype.repo` ar sekojošu saturu:

~~~
[skype]
name=Skype Repository
baseurl=http://download.skype.com/linux/repos/fedora/updates/i586/
enabled=1
gpgchek=0
~~~

Tad, kā super-jūzers, palaižam šīs komandas:

~~~
# yum install alsa-lib.i686 libXv.i686 libXScrnSaver.i686 qt.i686 qt-x11.i686
# yum install skype
~~~

P.S. Jā, tagad darbā esmu apgreidojies uz Fedora 17! :]