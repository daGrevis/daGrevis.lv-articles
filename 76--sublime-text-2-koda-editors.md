# Sublime Text 2 (koda editors)

Tik tikko ir iznācis, kā jau virsrakstā minēts, [Sublime Text 2 (v2.0)](http://www.sublimetext.com/blog/articles/sublime-text-2-0-released), kas ir netikai _yet another code editor_, bet arī ir ātrs, stabils, funkcionāls un izskatīgs! Tagad arī pastāstīšu par to, kāpēc esmu tik apmāts ar šo editoru (jā, tam ir labs pamatojums).

### Ieskats

Editora pirmsākumi (ST, bez divnieka) meklējami [2005. gadā](http://www.sublimetext.com/blog/articles/introduction), bet ST2 — [2011. gada pašā sākumā](http://www.sublimetext.com/blog/articles/sublime-text-2-public-alpha). Tas nozīmē, ka kopš alfa līdz fainal versijai ir pagājuši apmēram četrdesmit-divi mēneši. Ar to es gribu teikt, ka editors vairs nav nemaz tik zaļš... Pietam, man lietojot beta versijas arī nav nācies saskarties ar nepatīkamiem pārsteigumiem.

Editora kodols, pārmaiņas pēc, ir rakstīts [C++](http://en.wikipedia.org/wiki/C%2B%2B), nevis [Java](http://en.wikipedia.org/wiki/Java_(programming_language)). Tas daudziem liksies kā liels plus, jo Java-beist editori ([Eclipse](http://www.eclipse.org/), [NetBeans](http://netbeans.org/)) mēdz būt ļoti lēni. Konfigurācijas faili ir [JSON formātā](http://en.wikipedia.org/wiki/JSON), kas pat ne-programmētajam liksies ērti. Ir iespējams pievienot jaunu un mainīt esošo funkcionalitāti ar plaginiem, kas rakstīti [Python valodā](http://en.wikipedia.org/wiki/Python_(programming_language)). Editors ir [«multi-platformizēts»](http://en.wikipedia.org/wiki/Cross-platform), kas nozīmē — ies gan uz tava [Windows](http://en.wikipedia.org/wiki/Microsoft_Windows), gan uz tava hipster-drauga [OS X](http://en.wikipedia.org/wiki/OS_X) (_that would be Mac_)... un uz manas [Fedoras](http://en.wikipedia.org/wiki/Fedora_(operating_system)) un [Arch Linux](http://en.wikipedia.org/wiki/Arch_Linux) «jau griežas»! :)

### Kāpēc man vajadzētu to pamēģināt?

Īsumā: _Why not..._

Ja tevi neapmierina tavs pašreizējais editors (lēns, bieži karās, maz funkcijas, izskatās kā no deviņdesmitajiem?)... pēdējais laiks meklēt ko jaunu. ST2 ir viena no labākajām alternatīvām! Ja tomēr pašreizējais editors darbu veic, tā teikt, godam — iespējams attiecīgos uzdevumus var paveikt vēl produktīvāk un, vienkārši, labāk. Varam ilgi un dikti strīdēties, bet vienīgā pareizā atbilde — tev nevar būt viedoklis par to, ko nekad neesi izmēģinājis!

Es no sirds rekomendēju vismaz dažas nedēļas paspēlēties ar šo editoru. :)

### Instalācija

Pietiks gari un daiļi runāt... ķersimies pie ST2 instalācijas! Tas aizņems piecas minūtes un, ja tomēr kkas galīgi, galīgi neapmierina, to ir iespējams tik pat ātri atinstalēt. Nekautrējamies, patiešām!

#### Windows

Nelietoju Windows. Visticamāk lejupielādējam [vajadzīgo EXE (32 vai 64 biti)](http://sublimetext.com/2) un «palaižam to».

#### OS X

Šo arī neesmu lietojis (šoreiz diemžēl), bet visticamāk «ir jāpalaiž» iegūtais [DMG fails](http://sublimetext.com/2).

#### Linux

##### Arch Linux

Atrodam [AUR'ā](http://aur.archlinux.org/) vajadzīgo pakedžu un sekojam izcilajai [AUR dokumentācijai](http://wiki.archlinux.org/index.php/AUR_User_Guidelines).

##### Fedora

Fedorai būs nedaudz sarežģītāk... tātad ir divi varianti:

1. [Darīt kā šajā pamācībā](http://makewhatis.com/2011/11/sublime-text-2-fedora-1516-unofficial-repo) un pievienot ST2 repo (neoficiālo) pie pārējām (rakstīšanas brīdi v2.0 vēl tur nebija, bet bija iepriekšējā versija),

2. [Lejupielādēt ST2](http://sublimetext.com/2) no oficiālās mājaslapas un [pašam sakompilēt RPM pakedžu](http://fedoraproject.org/wiki/How_to_create_an_RPM_package)... vai iztikt bez RPM pakedža un [darīt šādi](http://microlizard.wordpress.com/2012/03/19/installing-sublime-text-2-on-linux-fedora-16/);

P.S. Es izvēlētos soli #1. Iepriekšējā versija arī ir diezgan stabila.

### Veram vaļā!

Dubult-klikšķis uz editora ikonas un... tas jau ir atvēries (atceros kā bija ar NetBeans)!

[![Atvērts ST2](http://i.imgur.com/pN6V1.jpg "Atvērts ST2")](http://i.imgur.com/ET4EG.jpg)

#### Pamatlietas

Lietas, kas ir gandrīz jebkura koda editorā šeit arī ir un darbojas kā jau esi pieradis:

* Faila izveidošana (_File -> New File_, _Ctrl + N_),
* Faila atvēršana (_File -> Open File_, _Ctrl + O_),
* Faila saglabāšana (_File -> Save_, _Ctrl + S_),
* Direktorijas un faili trī vjūvā (_View -> Side Bar_ un _Project -> Add Folder to Project_),
* Meklēšana un aizstāšana ar redžeksu atbalstu (_Ctrl + F_, _Ctrl + H_),
* Sintakses Hailaits (_View -> Syntax_),
* Tabi (līdzīgi kā ir pārlūkos);

### Savādāka pieeja vecajām problēmām

Lūk ir dažas lietas, ar ko ST2 izceļas.

#### «Goto Anything»

Uzklikojam _Ctrl + P_. Atveras tā sauktais «Goto anything» logs. Teiksim, ja es esmu atvēris savu kkādu kodu kā projektu un tur ierakstu «template.php», man parādās visi faili attiecīgajā projektā, kuru nosaukums satur manis ievadīto tekstu. Viens «Enter» un fails tiek atvērts. Ja es sākam tekstu ar «@» un es esmu PHP failā, tiek parādīts lists ar visām funkcijām, klasēm un metodēm. Ja es būtu HTML failā, tiktu parādīti visi ID atribūti. Ja es būtu Python vai Ruby failā, ST2 pielāgotos! Ar «#» es meklēju pašreizējajā failā, bet ar «:» nonāku izvēlētajā rindiņā. Pats labākais ir tas, ka visu to var kombinēt. Piemēram, _Ctrl + P_ un `template#foo` meklē visos projekta failos, kuru nosaukumā ir «template», pēc frāzes «foo».

![Goto Anything](http://i.imgur.com/CdxrM.jpg "Goto Anything")

P.S. Lai redzētu, kā tas viss strādā — projektam ar saturu tajā ir jābūt atvērtam.

#### «Command Palette»

Līdzīgi fīčai «Goto anything», spiežot _Ctrl + Shift + P_ atveras logs. Atšķirība, ka šeit parādās visas ST2 komandas.

![Command Palette](http://i.imgur.com/6kSdf.jpg "Command Palette")

Komandu piemēri:

* «File: Save All»,
* «File: Search Files»,
* «Project: Add Folder»,
* «Set Syntax: *»,
* Utt. utjp.;

Vislabākais, ka plagini arī var pievienot komandas. Tā, piemēram, dara «Package Control» plagins.

#### «Multiple Selections»

Iezīmējiet kko, turiet «Ctrl» un iezējiet vēl kko. Abas lietas tika iezīmētas!

![Multiple Selections](http://i.imgur.com/xocL8.jpg "Multiple Selections")

Piemēram, jums ir atvērti divi faili ar divām klasēm. Klasē «Foo» ir metodes: «do_a()», «do_b()» un «do_c()». Secība šajā gadījumā ir svarīga. Otra klase ir tukša. Tagad jums vajag metodes «do_a()» un «do_c()» ielikt tukšajā klasē. Parastais process būtu apmēram, ka jūs izgriežat pirmo metodi, atverat failu, ielīmejat to tajā failā (izgriežat, ielīmējat... nopietni?), atveram atkal pirmo failu, atkal izgriežam nu jau trešo metodi, tad atveram otru failu, izgriežam. Tagad varam darīt tā: iezīmējam pirmo **un** trešo metodi, tad atveram otru klasi un izgriežam abas iezīmētās metodes ārā.

    :::php
    class Foo {

        function do_a() {}

        function do_b() {}

        function do_c() {}

    }

    class Bar {
	
        // do_a() & do_c()

    }

Vēl viens labs jūz-keiss varētu būt, piemēram, ja jums ir lists ar elementiem bez vajadzīgā komata. Paņemam un iezīmējam visus elementus. Tad _Ctrl + Shift + L_, lai novietu kursoru katras iezīmētās rindiņas sākumā. Tad visus kursorus novietojam rindiņu pašās beigās (ar bultiņ-taistiņiem) un ieliekam komatu.

    :::javascript
    a = [
        'x',
        'y',
        'z',
    ]

#### «Auto-complete»

Kad tu raksti aplikāciju, tev ik pēc laika ir jāatkārto sevi. Vai nu tas ir mainīgaiā, vai funkcijas nosaukums... bet tā nu tas ir. «Auto-complete» palīdz izvairīties no vēlreizējas pārrakstīšanas un pārrakstīšanās. Vienkārši sakot, tev tiek piedāvāti varianti vārdam, ko vēlies uzrakstīt, tiklīdz sāc to rakstīt. ST2 vārdus ņem no pašreizējā faila, ne no pašreizējā projekta. To gan var izmainīt ar attiecīgu plaginu, par kuru var izlasīt zemāk.

![Auto-complete](http://i.imgur.com/P56rv.jpg "Auto-complete")

Patīkama lieta arī ir tāda, ka ja tu labo, piemēram, PHP failu — visas PHP iebūvētās funkcijas / metodes ir pieejamas. Ja tu labo Python failu, visas Python funkcijas / moduļu funkcijas un metodes ir pieejamas. Ja tu labo HTML, tad... bla, bla, bla. «Auto-complete» arī no valodas references.

#### «Minimap»

Labajā sānā ir «Minimap». Idejiski, tas ir pašreizējais fails — tikai kādas 10x atzūmots. Doma tam visam ir parādīt vizuāli visu koda failu un uzlabot pārvietošanos. Dažreiz pārvietoties izmantojot to ir vieglāk nekā izmantojot «Goto anything». Piemēram, ja tev vajag tikt vietā, kur sākās daudzie komentāri... sintakse taču komentārus iekrāso zaļus! Tad tu apskaties «Minimap» un redzi to zaļo vietu — viens klikšķis un tu jau esi tur! Kā arī, tas izskatās **tik episki**!

![Minimap](http://i.imgur.com/qVjLa.jpg "Minimap")

#### «Split Editing»

Jums ir liels monitors! Jocīgi, man arī... Tagad jautājums: vai nav, es nezinu, nedaudz izšķērdīgi, ja visas, teiksim, 27 collas aizņem viens fails? Kur nu vēl tad, ja faila platums nepārsniedz 80 simbolus! Nu lūk... tagad tu vari labot reizē, teiksim, četrus failus. Viņi var būt horizontāli blakus, vai, piemēram, _izmanto fantāziju_... un es pēc pieredzes varu teikt, ka tā ir daudz ērtāk!

[![Split Editing](http://i.imgur.com/pOC1D.jpg "Split Editing")](http://i.imgur.com/e728S.jpg)

#### «Distraction Free»

Spiežot _Shift + F11_, viss izņemot kodu tiek aizvākts; kods tiek novietots pa vidu. Noderīgi, kad gribas vienkārši pakodēt... bez nekādas uzmanības novēršanas. Efekts ir vēl labāks, ja tev ir liels monitors. Kaut gan, uz maziem monitoriem šī fīča arī būs ļoti noderīga — bez skrollbars viss kods saies ekrānā! ;D

[![Distraction Free](http://i.imgur.com/b5RNz.jpg "Distraction Free")](http://i.imgur.com/Yw3AD.jpg)

#### «ST2 Console»

Spiežot _Ctrl + `_ atveras tā sauktā «ST2 console». Tas ir Python interpretators, kas arī ziņo par visiem ST2 un plaginu procesiem! Šo var izmantot par kalkulatoru, vai, teiksim, lai konvertētu skaitļus ar 10 bāzi uz skatiļiem ar 16 bāzi. Idejiski tu tur vari pat uzkodēt spēlīti...

![ST2 Console](http://i.imgur.com/17VKV.jpg "ST2 Console")

### Konfigurācija un papildus funkcionalitāte

Kā jau tu redzi, ST2 ir ōōsom pat ar defalto konfigurāciju un bez nekādiem ekstra plaginiem. Tomēr, ir iespējams «iet vēl daudz tālāk».

#### JSON konfigurācija

Ir divi galvenie konfigurācijas faili, ar kuriem var izmainīt ST2 darbības un izskatu.

1. _Preferences -> Settings — User_,
2. _Preferences -> Key Bindings — User_,

Abi šie faili satur informāciju JSON formātā. Ja informācija nav norādīta, tiek lietoti dafaltie iestatījumi no _Preferences -> Settings — Default_ un _Preferences -> Key Bindings — Default_. Defaltie iestatījumi kalpo kā labs piemērs, lai izmainītu personālos iestatījumus. Lieki teikt, ka defaltie iestatījumi nav maināmi.

Ja ir kāds brīvāks brīdis, varat «izstaigāt cauri» visiem iestatījumiem. Varbūt fīču X jūs gribat atslēgt, bet fīču Y atkal ieslēgt. :)

Šeit ir mani iestatījumi:

    :::json
    {
        "highlight_line": true,
        "trim_trailing_white_space_on_save": true,
        "ensure_newline_at_eof_on_save": true,
        "hot_exit": false,
        // "theme": "Soda Dark.sublime-theme",
        // "color_scheme": "Packages/User/Monokai Soda.tmTheme",
        // "font_face": "Meslo LG L DZ",
        "font_size": 8
    }

    [
        // { "keys": ["ctrl+m"], "command": "markdown_preview", "args": {"target": "browser"} },
        // { "keys": ["ctrl+1"], "command": "phpcs_sniff_this_file" },
        // { "keys": ["ctrl+2"], "command": "phpcs_clear_sniffer_marks" }
    ]

P.S. Atkomentējiet komentārus, ja jums ir attiecīgie komponenti.

#### Plagini

Lūk ir lists ar plaginiem, kurus es pats lietoju. Tie, protams, **nav** visi pieejamie plagini!

#### «Package Control»

Plaginu plagins! Izmantojot šo, tiek instalēti citi plagini.

Pamācība [instalācijai](http://wbond.net/sublime_packages/package_control/installation) un [izmantošanai](http://wbond.net/sublime_packages/package_control/usage). Pēc veiksmīgas instalācija un ST2 restarta, «Command palette» būs jaunas iespējas. Izvēlamies _Package Control: Install Package_ un parādīsies lists ar oficiālās repo pieejamajiem pluginiem. Ja vēlamies, uzinstalējam kādu!

![Package Control](http://i.imgur.com/hwgZ3.jpg "Package Control")

#### «HTML5» un «jQuery»

Snippetu pakas [HTML5](http://en.wikipedia.org/wiki/HTML5) un [jQuery](http://jquery.com/). Domātas «Auto-complete».

#### «Bracket Highlighter»

Izceļ taga sākumu un beigas. Atbalstītās valodas: HTML, CSS, JavaScript, PHP, Python uc..

![Bracket Highlighter](http://i.imgur.com/6WUok.jpg "Bracket Highlighter")

Plaginam mēdz būt ar pašam savi JSON iestatījumi. Attiecīgi man defaltie nedaudz nepatika, tāpēc...

    :::json
    {
        "search_threshold": 5000,
        "tag_search_threshold": 5000
    }

#### «SideBar Enhancements»

Pievieno jaunas opcijas said-bārā, kas atļauj vispār atteikties no OS iebūvētā failu menedžera.

#### «ColorPicker»

Man ik pa laikam savajagas uzināt krāsu kodu kādai krāsai... un vērt vaļā GIMP vai kko citu — par ilgu.

#### «Markdown Preview»

Šis plagins atver pašreizējo failu pārlūkā un parsē tā saturu ar Markdown. Lieti noder, piemēram, tagad, kad rakstu šo rakstu.

#### «DocBlockr»

Šis plagins palīdz izveidot [PHPDoc](http://www.phpdoc.org/) un [JSDoc](http://code.google.com/p/jsdoc-toolkit/) komentārus.

#### «Github Gist»

Šis plagins «pa tiešo» ļauj pievienot jaunus, izmantot esošos un veikt citas perversijas ar GitHub Gistiem. Es, personīgi, to izmantoju kā peistie-laik servisu un, nezinu, kā «tiltu» starp datoru un Gist serveri, lai saglabātu savus personīgus snippetus.

#### «PHP CodeSniffer»

Koda snifferis PHP valodai.

#### «Linter»

Linteris, kas atbalsta: CoffeeScript, CSS, Java, Javascript, Objective-J, Perl, PHP, Python, Ruby. Uzmanīgi ar šo plaginu, jo diezgan liela konfigurācija ir nepieciešama!

#### «CodeIntel»

Plagins apvieno divas lietas, kas man pietrūka no NetBeans.

1. Auto-komplīt, kas meklē arī projektā (meklē gudri),
2. Klikšķis uz, teiksim, funkcijas izsaukumu — atver failu, kur funkcija ir definēta;

Arī būs normāli jākonfigurē.

#### «Soda Theme»

Izskats ST2. Izmantoju arī [Meslo fontu un color skīmu](https://github.com/buymeasoda/soda-theme).

[![Soda Theme](http://i.imgur.com/gD9wp.jpg "Soda Theme")](http://i.imgur.com/7Upxi.jpg)

### Kopumā

Nolādēts, cik ST2 ir labs editors! Es nebūtu rakstījis šo rakstu, ja es tā nedomātu.

P.S. Lūdzu iepazīstieties [ar licenci](http://www.sublimetext.com/buy), lai nesanāk nepatīkami pārsteigumi.