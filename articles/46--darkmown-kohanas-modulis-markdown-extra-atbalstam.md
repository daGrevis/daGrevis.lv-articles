# Darkmown — Kohanas modulis Markdown Extra atbalstam

### Kas tas ir; ko tas dara?

Nesen šodien gan sāku, gan arī pabeidzu mazu projektiņu ar nosaukumu «Darkmown». Tiem, kas zina, kas ir Markdown — vārdu salikums «Markdown parser» uzreiz izteiks gandrīz visu! Tie kas nezina «kas tas par zvēru»... īsumā: tā ir markapa sintakse, kas ļauj bez programmēšanas zināšanām formatēt saturu, visbiežāk, internetā («resns, slīps, attēls, tabula»).

Še-ku labs citāts no Vikipēdijas:

> Markdown is a markup language allowing people to write using an easy-to-read, easy-to-write plain text format, then convert it to structurally valid XHTML (or HTML).

Pašu parseri kā tādu pats gan nerakstīju. Ņēmu gatavu, atrodamu [šeit][1]! Tas, ko es pats darīju — uzrakstīju Kohanas moduli, kas ir kā vraperis esošajai, ne manai, Markdown implementācijai. Vēl «jāpiezīmē», ka esošā Markdown implementācija ir galīgi nelaba, nejauka un, atļaušos teikt, pat pretīga (galvenais iemesls ir PHP4 atbalsts). Bet strādā! ;D

Tāks... kas vēl... īstenībā Kohanai jau ir viens modulis, kas cenšas darīt to pašu. Še links [uz to][2]! Galvenā atšķirība no mana moduļa ir tāda, ka manam ir iespēja ieslēgt «Markdown Extra» atbalstu. Atkal īsumā: tas ir Markdown «uz steroīdiem»! Re cik smuki un īsi sanāca, bet vairāk info var atrast [te][3].

### Kā izmantot?

Oficiālajā [GitHub lapā][4] viss ir smuki un angliski paskaidrots. Instalācija aizņem pusminūti un viss strādā bez jebkādas konfigurācijas. Ja tomēr tev patīk konfigurēt, to arī var izdarīt. Ja rodas kādi jautājumi — turpat, Github'ā, arī prasiet. Šeit komentāros labāk nejautājiet (es jau runāju nākotnes formā, jo šeit ir iecerēta komentēšanas iespēja ;D). Likums «par turieni» attiecas arī uz visiem bag reportiem (cerēsim, ka vispār nebūs bagu) un fīčer rekvestiem. Starp citu, [vienu bagu][5] jau noķēru un salaboju! :)

P.S. Mans blogs jau sen izmanto Markdown atbalstu, par to [jau rakstīju][6] (implementācija gan bija cita, primitīvāka). Tagad tā vietā tiek izmantots šis modulis!


[1]: https://github.com/michelf/php-markdown
[2]: https://github.com/aptgraph/kohana-markdown
[3]: http://michelf.com/projects/php-markdown/extra/
[4]: https://github.com/daGrevis/Darkmown
[5]: https://github.com/daGrevis/Darkmown/issues/1
[6]: http://dagrevis.lv/article/10/markdown_atbalsts