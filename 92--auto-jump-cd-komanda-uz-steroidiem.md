# Auto-jump — «cd» komanda uz steroīdiem!

Jau kādu labu laiku izmantoju auto-jump. Tā ir ļoti vienkārša, bet tajā pašā laikā arī ģeniāla CLI utilīta. Pašā kodolā tā ir «cd» komanda («change directory»), kas atceras tās vietas, kur tu esi bijis, kā arī apmeklētības biežumu. Rezultātā, pēc neilgas datora palietošanas, ar auto-jump var pārvietoties pa direktorijām daudz ātrāk; var lekt! :)

~~~
[dagrevis@localhost ~]$ j dag
/home/dagrevis/Python/daGrevis.lv/dagrevis_lv
[dagrevis@localhost dagrevis_lv]$ j Scre
/home/dagrevis/Screenshots
[dagrevis@localhost Screenshots]$ j Dow
/home/dagrevis/Downloads
[dagrevis@localhost Downloads]$
~~~

P.S. Komanda «j» ir šorthends.

Šeit ir [GitHub lapa](https://github.com/joelthelion/autojump "joelthelion/autojump") instalācijas instrukcijām un koda apskatei. Uz Arch Linux instalācija ir tik vienkārša kā `pacman -S autojump`! :)