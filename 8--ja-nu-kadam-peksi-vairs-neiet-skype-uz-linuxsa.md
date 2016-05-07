# Ja nu kādam pēkši vairs neiet Skype uz Linux'ša...

Tik tikko saskāros ar problēmu, ka Skype pēc `yum upgrade` komandas izpildes un datora restarta vairs nestrādā. Nestrādāšanas izpaužas kā nevarēšana ielogoties — ilgs lādēšanās process kas beidzas ar kļūdas paziņojumu: «P2P connect failed».

Lai jums nebūtu ilgi un dikti «jāčakarējas»...

    su
    rm -rf /home/dagrevis/.Skype

(kur `dagrevis` ir jūsu lietotājvārds)

...un visam atkal vajadzētu iet! :)

**Labojums:**

Attiecīgā komanda izdzēsīs saglabātos Skype'a iestatījumus uz jūsu datora (arī vēsture!).

Tas tā, informācijai.