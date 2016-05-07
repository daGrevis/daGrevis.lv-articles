# Versiju kontrole un Git 101

Šajā rakstā es pastāstīšu kāpēc ir jāizmanto versiju kontrole un kā, visā visumā, tas izskatās ar Git. Šis raksts tevi neiemācīs lietot Git vai versiju kontroli, bet izskaidros _what and why_.

# Sāpīgā nepieciešamība versiju kontrolei

Es vairs nespēju iedomāties savu dzīvi bez versiju kontroles.

Kas notiek, kad 2+ cilvēki strādā pie projekta? Katrs strādā ar savu failu un vēlāk faili, kuri tika izmainīti, tiek kopēti pareizajās vietās no programmētāju datoriem? Vai, vēl trakāk, viss, pa taisno, tiek augšupielādēts uz servera? Kas notiek, ka divi cilvēki ir strādājuši pie vienu un tā paša faila? Tikai izmaiņas no viena cilvēka tiek ņemtas vērā? Kā var saprast, kas un kad ir mainīts? Kurš pirms četriem mēnešiem izmainījā tā faila 421 rindiņu? Kas notiek, ja tavs uzdevums ir izmēģināt pavisam jaunu laibariju uz esošā koda, neieteiksmējot kodu, ar kuru strādā citi cilvēki? Kas notiek, ja ir karsta fīča vai traks bags, kuru jāsalabo ASAP, nevis tad, kad patreizējā fīča tiks izlabota? Kad notiek, ja kods, kas tika rakstīts visu nedēļu, ir pilnīgī un galīgi nepareizs — kā visu var atgriezt iepriekšējā stadijā?

Tiks daudz sāpīgu jautājumu, bet viena, pareiza atbilde — versiju kontrole!

# Vispopulārākie versiju kontroles tūļi

Cik zinu, vispopulārākie versiju kontroles tūļi ir [Git](http://en.wikipedia.org/wiki/Git_%28software%29) un [Mercurial](http://en.wikipedia.org/wiki/Mercurial). Teorētiski man vajadzētu lietot Mercurial, nevis Git, jo tas ir rakstīts Python, bet prakstiski gan tā nav. Lietoju Git jau divus gadu un lietoju laimīgs! Centīšos par to pastāstīt, lai iesācējiem to sākšana lietot nebūtu raķešu zinātne.

Nevaru atturēties un nepieminēt, ka eksistē [SVN](http://en.wikipedia.org/wiki/Apache_Subversion). Tā gan ir pagātne un, ja tu to vēl nezini, es neredzu jēgu to apgūt.

# Kā viss kopumā strādā

Viss ir vienkāršāk, nekā varētu likties.

- Ir nepieciešams centrālais serveris (piemēram, [GitHub](https://github.com/) vai [BitBucket](https://bitbucket.org/)) ar repozitoriju (piemēram, [daGrevis.lv](https://github.com/daGrevis/daGrevis.lv) (šis blogs) vai [Dotfiles](https://github.com/daGrevis/Dotfiles)),

- Tiek glabātas koda izmaiņas, nevis fails ar visu saturu,

- Koda izmaiņas ir jādabū lokāli, lai ar tām sāktu strādāt,

- Pēc tam koda izmaiņas ir jāsūta atpakaļ uz repo,

- Kods tiek dalīts brenčos un komitos;

Ja tas neliekas skaidri, tas nekas! Vieglāk to ir parādīt.

P.S. Mums būs nepieciešams Git un termināls.

# Pirmais projekts

Iedomāsimes, ka mums ir jauna, forša ideja un mēs gribam sākt projektu. Tikai šoreiz izmantosim Git! :)

Pirmais, kas ir jāizdara, ir jāuztaisa repozitorija. Domāju, ka GitHub būs gana labs!

P.S. Esmu rakstījis par [Git repo uz sava servera](http://dagrevis.lv/blog/107/git-repo-uz-sava-servera/).

Tātad, piereģistrējamies GitHub un izveidojam repo.

Lai mēs varētu strādāt ar izveidoto repo, tā jādabū uz lokālā datora:

    git clone git@github.com:{{ username }}/{{ repo_name }}.git

Šī komanda izveidos direktoriju ar visiem failiem no mūsu repo. Esam gatavi sākt projektu!

Pirmais uzdevums, ko varētu izdarīt, ir izveidot `README.md` un ierakstīt kko par mūsu projektu. Daram to!

Tagad, izpildot `git status`, mēs ieraugam, kad ir izveidots jauns fails, bet tas nav pievienots repo (_untracked_). Izpildot `git add README.md` šis fails «kļūst pievienots».

Tālāk mums ir jāizveido komits — `git commit`. Tiks prasīts ierakstīt mesedžu un tur varam ierakstīt apmēram «Added README.md with project description.». 

Apsveicu, pirmais komits ir izveidots! Komiti ir atskaites punkti izdarītajām lietām, kas veido visa projekta vēsturi.

Piemēram, varu uzzināt pēdējos komitus darot šādi:

    git log --oneline | head -n 10

    a5c2c8d Minor changes to colors.
    c037cc5 Bug #57: Tag size doesn't work correctly
    410a7e7 Improvement #55: Add space between tags
    9810129 Bug #53: Link in footer is incorrect
    9d95abd Improvement #50: Superuser comments are too highlighted
    fb0803c Fixed links to RSS and ATOM feeds in `base.html` template.
    f6ff396 Bug #49: URLs to feeds are incorrect
    2e20a8e Added Gunicorn.
    35a9a3a Added server-specific things to `.gitignore`.
    c24b433 Added content to About and Contacts pages.

Tas man skaidri parāda kas nesen ir darīts.

Tagad, kad komits ir izveidots, tas pie mums ir lokāli. Lai to dabūtu serverī, izpildam `git push`.

# Projekts komandai

Iztēlosimies, ka mūsu projekts kļūst populārs un citi cilvēki vēlas strādāt pie tā. Nav problēmu! Viss, kas cilvēkam ir jāizdara ir jānoklonē projekts, jāveic izmaiņas, jāuztaisa komits un pušs. Ja 2+ cilvēki ir labojuši vienu un to pašu failu, Git parūpēsies par abām izmaiņām. Ja Git tomēr nespēs izdarīt to automātiski, tiks prasīts viņam pateikt kas tieši tika izmainīts.

Kad tu atsāc darbu, tev ir jāizpilda `git pull`. Tas atjaunos lokālo repo, lai tajā būtu visajunākās izmaiņas. Ja, kamēr strādāji, kāds būs jau nopušojis jaunas izmaiņas uz repo, un bet tu centīsies pušot, kamēr tev nav jaunākās izmaiņas, Git atkal par visu parūpēsies un pateikts, ka sākumā tev vajag nopūloties.

# Par brenčiem

Jau minēju, ka izmaiņas tiek dalītas brenčos. Sākot projektu, tiek izveidots «master» brenčs. Parasti masterā ir izmaiņas, kas ir stabilas un produkcijai gatavas. Jaunu brenču var izveidot ar komandu `git branch {{ branch_name }}`.

Izveidojot brenču, tu patreizējās izmaiņas patreizējajā brenčā iekopē jaunajā brenčā. Tas nozīmē, ka brenči ir izolēti no citiem brenčiem.

Tas noder, kad veido kādu lielāku tasku vai, esot kāda taska brenčā, pārslēdzies uz citu (`git checkout`) un sāc strādāt ASAP uzdevumam.

Vēlāk brenčus var apvienot ar `git merge` vai atjaunot brenču ar `git rebase`. Tātad sanāk, ka tu vari izolēti strādāt savā brenčā, teiksim, nedēļu un tad, kad viss ir ejošs, šīs izmaiņas ielikt masterā.

P.S. Pats personīgi veidoju brenču jaunam taskam, ja vien tasks ir ļoti, ļoti mazs. Kad tasks ir pabeigts, iemerdžoju brenču master brenčā ar `squash` flegu, kas visus brenčā komitus saspiež vienā komitā, kur komita mesedžš ir taska ID un apraksts.

# Es vēlos apgūt Git!

Ceru, ka kaut nedaudz ievērsu skaidrību par Git un versiju kontroli kā tādu.

[Šeit](http://rogerdudler.github.com/git-guide/) un [arī šeit](http://nfarina.com/post/9868516270/git-is-simpler) ir tehniskāks apraksts par Git iesācējiem!

Git ir de-fakto standarts, un to ir vērts apgūt! Pat ja tagad liekas, ka tas ir ļoti sarežģīti — ir vērts pacenties — tas atmaksāsies!

Ja esmu pieļāvis kļūdiņas, vai tev ir kādi jautājumi — droši komentē! :)

**Labojums:** Šeit ir [vesela grāmata par Git](http://git-scm.com/book)!