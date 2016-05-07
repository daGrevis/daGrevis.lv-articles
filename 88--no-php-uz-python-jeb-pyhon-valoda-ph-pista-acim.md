# No PHP uz Python jeb Pyhon valoda PH-Pista acīm

Ir pagājuši jau gandrīz divi mēneši kopš mainīju savu darba vietu. Tagad esmu Python programmētājs un ļoti ceru, ka PHP valodai vairs nebūs «jāpieskaras». Kas tas tāds ir — Python? Kādas ir galvenās atšķirības starp šīm divām valodām? Kas tad vainas PHP? Par to šajā rakstā. :)

### Par čūsku (Python)

Python ir vēl viena skriptu valoda. Jauns tūlis manā tūlboksā! Sen jau bija doma mācīties jaunu programmēšanas valodu un, cik atceros, izvēle bija starp Python un Ruby. Abas valodas ir relatīvi skaistas un no abām arī zinu cilvēkus, kuri attiecīgās valodas arī lieto. Beigu beigās izlēmu par labu Python, jo ar to arī bieži vien raksta CLI utilītas (biežāk nekā web lapas, starp citu), veido _ne-tik-ļoti-blingy-bling_ 2D spēles un pat ļoti primitīvas GUI aplikācijas! Ir iespējams palaist Python uz Android un Python ļoti bieži izmanto kā pluginu-valodu ([kaut vai pašam ST2](http://dagrevis.lv/article/76/sublime_text_2_koda_editors "Sublime Text 2 (koda editors)")). Protams ar Ruby un, Dievs pasarg (!), PHP arī to var darīt, bet... katrai lietai ir savs tūlis un Python, beigu beigās, tomēr būs piemērotāks CLI utilītām nekā Ruby. Bet Ruby arī ir ļoti jauks! ;D

Pats Python ir interpretējams, strauji attīstās (diezgan nesen iznāca trešā versija un cilvēki čīkst par portēšanas problēmām :) ), relatīvi populārs (ne tik ļoti kā PHP vai JavaScript, bet...)  un pēdējā laikā pieprasījums pēc Python programmētājiem darba tirgū ir tikai cēlies (šis fakts sāk ieņemt lomu valodas izvēlē, kad tu ar to «pelni maizi»). Priecē fakts, ka Python nosaukums ir cēlies no humora šova Monty Python (iesaku ieguglēt (iebingot?) par šo jebkuram, kuram patīk labi pasmieties).

### «Kas tas par pseido-kodu?»

Pirmais, kas, domāju, jebkuram (pareizāk jebkuram, kurš nāk no C-like valodas: C, C++, C#, Java, JavaScript, PHP, Go utt. utjp.) liks teikt WTF, ieraugot Python, ir sintakse. Nav semikoli, nav braketi un viss izskatās, vienkārši, kā jau es minēju, pēc pseido-koda.

Koda gabali iz Python (tik pat labi tas varētu būt arī pseido-kods):

Gabals #1:

    :::python
    # Simulates «ls /spam/eggs/».
    directory = sys.argv[1] if len(sys.argv) > 1 else "."
    for item in os.listdir(directory):
        print item,

Gabals #2:

    :::python
    def fib(n):
        """Genarates sequence of Fibonacci numbers."""
        if n == 0: return 0
        elif n == 1: return 1
        else: return fib(n - 1) + fib(n - 2)

    print fib(42)  # 42th number in Fibonacci sequence.

Gabals #3:

    :::python
    # Searches for string in web-page and prints-out the result.

    needle = "— You're flying! How? — Python!"
    haystack = urlopen("http://dagrevis.lv/")

    if needle in haystack.read(): print "Found!"
    else: print "Not found!"

Gabals #4:

    :::python
    @app.route("/hello/<username>")
    def hello(username):
        """Says hello."""
        if username is None:
            return "Hello, anonymous!"
        return "Hello, {}!".format(username)

Galīgi nepierasti, vai ne? Sākumā es arī biju pārsteigts. Pat ļoti! Tomēr, jau sen esmu pieradis un, es droši varu teikt, ka šāda sintakse ir ērtāka un vieglāk lasāma. Neredzu jēgu, tā teikt, «liekajiem semikoliem» katras jaunas rindiņas beigās. Neredzu jēgu «liekajiem braketiem», jo, beigu beigās, tāpat ir pieņemts kodu indentot un tas jau ir pietiekami, lai pats parseris varētu saprast kur sākas un beidzas bloks ar kodu.

Gadījums iz dzīves bija, ka jaunajā darbā pēc krietna Pythonisma nācās uzrakstīt dazās rindiņas ar JavaScriptu. Tā kā manam ST2 ir SublimeLinter plagins, uzreiz pirmajā rindiņā parādījās iespējamā kļūda. Es ilgi nevarēju saprast kur ir problēma, jo rindiņa izskatījās pareiza. Beigu beigās tomēr sapratu, ka nav noslēdzošā semikola. Lūk tas ir pieradums! :)

### Python valoda PHP programmētājam

Jau minēju, ka kādreiz biju PHP programmētājs. Tagad, cik nu objektīvi spēšu, salīdzināšu šīs divas valodas.

Pirmais, kas likās nedaudz jocīgi, ir tas, ka viss ir kā modulis. Pašam Pythonam ir astoņdesmit funkcijas. Pārējais — smuki sakārtots pa moduļiem. Tā teikt, _OOP approach_. Tiem, kas nezin — iekš PHP ir varbūt pat daži tūkstoši **iebūvētās funkcijas**, kas ir prefiksotas ar, gluži vai, random nosaukumiem. Tas nenozīmē, ka PHP ir vairāk funkcionalitātes. Tas nozīmē, ka iekš Python viss ir skaisti sakārtots un pieejams tikai, kad pieprasīts.

Ja jau sākam runāt par kārtību valodā, Python valoda pati seko _development guidlines_. Attiecīgi, nav redzēti tādi brīnumi, ka visas funkcijas iekš modeļa ir, teiksim, ar under_score nosaukiem, bet viena, ļoti īpaša, ir camelCase'ā. Tas pats arī attiecas uz parametru kārtību — ja funkcija ar nosaukumu «foo» pieņem argumentus secībā «x» un «y», tad funkcija ar nosaukumu «reversed_foo», kas dara to pašu, tikai otrādi, pieņems argumentus tādā pašā, visnotaļ loģiskā, secībā.

Ja jau sākam par argumentiem... kas man pašam ļoti, ļoti patīk — «named arguments». Iedomāsimies funckiju, kurai ir desmit argumenti (no kuriem deviņiem ir defaultā vērtība).

**Labojums:** Parasti funkcijai nevajadzētu būt vairāk par trīs argumentiem. Tomēr, ir gadījumi, kad tas nav ievērots un «ir kaudze» ar defaultajiem argumentiem.

Situācija, ka nepieciešams izsaukt šo funkciju ar desmito argumentu kā True.

Iekš PHP: `foo(42, null, null, "", 0, 0, array(), 0, null, true)`

Iekš Python: `foo(42, bar=True)`

Attiecīgi, varam norādīt argumenta nosaukumu un nenorādīt visus astoņu pa vidu esošo argumentu defaultās vērtības. Patīkami, ne?

KKur lasīju, ka PHP 5.5 ir doma ieviest «default» kījvordu, kas, attiecīgi, būs pieejams kā arguments un nosetotosies uz defaulto vērtību.

Tātad: `foo(42, default, default, default, default, default, default, default, default, true)`

Iekš Python, tā pat kā JavaScript, viss ir objekts. Mēs varam mantot klasi no stringa vai jebkura cita datu tipa. Mēs varam klases instancei modificēt atribūtus. Tā kā funkcija arī ir objekts, mēs varam pieprasīt jebkuru funkcijas atribūtu (objektiem taču ir atribūti, vai ne? :) ). Mēs varam jebko mētāt apkārt, jo viss, viss ir objekts!

Ir vēl daudz, daudz mazi un arī ne tik ļoti mazi sīkumi, kas padara Python savā ziņā labāku par PHP valodu. Bet tas viss ir sīkums, jo atcerējos, ko nesen runāju ar [@laadinjsh](http://twitter.com/laadinjsh "Lādiņš (laadinjsh) on Twitter") (Ruby programmētāju). Sekojoši: galvenais valodā ir prieks, bauda (kaifs?) to lietot un, man rakstīt Python valodā ir nesalīdzināmi patīkamām nekā PHP. :)

**Labojums:** Šis raksts ir izpelnījies lielu kritiku no PHP programmētajiem. Nesaprotu kāpēc ir jāaizstāv kāda no valodām... tie visi ir tikai tūļi, kas palīdz nonākt pie labāka rezultāta. Es nesaku, ka PHP ir slikta valoda, bet saku, ka Python **manā uztverē**, **maniem uzdevumiem** der labāk. Man pieredze ar PHP ir ~3 gadi un nav gluži tā, ka neko par to pats nesaprotu — tā kā man ir viedoklis par to. Ar Python esmu profesionāli strādājis apmēram divus mēnešus — šie ir tikai pirmie iespaidi. Esmu drošs, ka laika gaitā atradīsies simts un viena lieta, kas Python padarīs ne tik ļoti pievilcīgu kā tagad. ...un es vēlreiz uzsveru, ka tie ir tikai tūļi darba paveikšanai. Izskatās tā, ka daži no jums «ir iemīlējušies savā valodā» un aizstāv to «ar putām uz lūpām». :)

> There is no silver bullet. /Fred Brooks/

### TL;DR

Tagad esmu Python programmētājs. Python, cik redzu un jūtu, ir labāks par PHP.