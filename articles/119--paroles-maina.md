# Paroles maiņa

Vakar Tviteris paziņoja par datu leaku ap 1/4 miljonu lietotāju datu.

> However, our investigation has thus far indicated that the attackers may have had access to limited user information – usernames, email addresses, session tokens and encrypted/salted versions of passwords – for approximately 250,000 users. /[Twitter Blog](http://blog.twitter.com/2013/02/keeping-our-users-secure.html)/

Uzskatu, ka tas ir labs iemesls, lai nomainītu paroles visiem saitiem, kurus izmantoju. Parolēm ir jābūt neuzmināmām, unikālam _per-resource_ un tās ir jāmaina _on the daily basis_.

Nedaudz papētiju un nonācu pie secinājuma, ka izmantošu «pwsafe». Šī appa ir uzstādāma gan uz Linux, OS X, gan Windows un iOS.

Uzstādīšana uz Arch Linux:

    sudo pacman -S pwsafe

Pirmkārt, «piepildīsim» `~/.rnd` ar datiem no `/dev/urandom`.

    dd if=/dev/urandom of=~/.rnd bs=1M count=2

Tad palaidīsim šo appu pirmo reizi ar `--createdb` argumentu.

    pwsafe --createdb

Tiks prasīta «master parole», ievadam to!

Šī parole tiks izmantota kā atslēga, lai redzētu, labotu un dzēstu pārējās paroles. Šī ir vienīgā parole, kura ir jāceras pašam; _yet_ tai ir jābūt drošai!

Tālāk varam apskatīt paroli — `pwsafe -Ep example.com`, pievienot — `pwsafe -a`, labot — `pwsafe -e example.com`, arī dzēst `pwsafe --delete example.com` utt.. Sīkāk — `man pwsafe`.

Patīkami, ka appa piedāvā uzģenerēt paroles. Ja paši tomēr domājam paroles, iesaku to drošību pārbaudīt [How Secure Is My Password?](http://howsecureismypassword.net/).

Paroles tiek glabātas `~/.pwsafe.dat`, kas ir droši sakriptēts. Pieņemu, ka šis datubāzes fails strādās uz jebkuras sistēmas, ja, iepriekš ģenerētais `~/.rnd` key-fails, sakrīt.

Ir arī arguments `--exportdb`, kas ļauj paroļu ierakstus no datubāzes #1 «samerdžot» ar datubāzi #2.

Šāda sistēma ir daudz drošāka un ērtāka, nekā visiem saitiem izmantot vienu paroli, vai paroles rakstīt uz lapiņas / TXT failā, kas ir totāli stulbi.