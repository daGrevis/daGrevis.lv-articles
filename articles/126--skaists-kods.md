# Skaists kods

Esmu lasījis tūkstošiem rindiņu sveša koda. Un lielāka daļa no tā ir tik ļoti neglīta, ka uznāk vēlma to visu pārrakstīt vai, vēl šausmīgāk, -- atrast attiecīgā koda autoru un to iepļaukāt!

Ar dūri.

# Kāpēc kodam ir jābūt skaistam?

Tāpēc, ka mēs kodu lasam daudz, daudz vairāk nekā to rakstam. Es teiktu, ka aptuveni 80% no laika, kad atrodamies editorā, mēs nevis rakstam jaunas rindas, bet cenšamies saprast kā strādā vecās.

Tāpēc kodam ir jābūt skaistam. Un ar skaistu es domāju _lasāmu_.

Citēšu _The Zen of Python_:

> Beautiful is better than ugly.

> Readability counts.

Tas neattiecas tikai uz to kodu, ko redz citi. Visticamāk, ka savu kodu beigās lasīsi tu pats. Tāpēc atvieglo dzīvi sev un raksti skaisti, tīri un saprotami. Pat tad, kad tas ir skripcelējums vai ātrs haks.

It īpaši, ja tas ir haks.

P.S. Nerunāju tikai par Python valodu.

# Kas ir skaists kods?

Pirmkārt ir jāapzinās, ka viss, ko tu esi kādreiz uzrakstījis, un viss, ko es esmu kādreiz uzrakstījis, ir briesmīgs. Viss ir relatīvs -- kas vienam ir smuks un foršs, otram ir ASCII sprādziens.

Tomēr ir dažas lietas, kas liekas īpaši kaitinošas gandrīz visiem:

* Indentācijas neesamība vai, ak šausmas(!), koda indentācijas nepareiza izmantošana,

* Faili ar 2000+ rindiņām, objekti ar 20+ metodēm, metodes ar 200+ rindiņām, funckijas ar 5+ parametriem utml.,

* Stulbi nosaukumi: `do`, `rework`, `t`, `ccnt`, `data`, `data2` utml.,

* Valodu mikslis: HTML ir kopā ar CSS un JavaScript, PHP ir kopā ar SQL utml.,

* Loģikas mikslis: templeits, kurš izpilda SQL, modelis, kurš strāda ar rekvestu utml.,

* Riteņa izgatavošana no jauna -- savi freimvorki, parseri, templei-endžini, user-sistēmas utml..,

* Optimizācija nevietā -- lūk, mēs varam ietaupīt 3ms pārrakstot 10 rindiņu ejošu kodu un 120 rindiņu baismīgu monstru (Doh!),

* Vairāk komentāri nekā paša koda un komentāri, kas atbild uz jautājumu «kas» (nevis «kāpēc),

* Standartu neievērošana un «special cases» (`'` vai `"`, tabi vai speisi, kamel-keis vai underskoure-keis, `XmlParser1` vai `XmlParser2`, nevis abi, utt. utjp.);

# Kā iemācīties rakstīt skaisti?

Kāds teiktu, lai lasi jau gatavu kodu, vēlāms, kādu freimvorku, laibariju. Tas ir galīgi garām. Kaut vai paskatamies uz WordPress vai Django kodu -- diezgan briesmīgi! Arī, šis kods jau ir optimizēts un, tāpēc, var saturēt daudz hakus un citus brīnumus, lai uzlabotu performanci, kas, diemžēl, arī pasliktina lasāmību.

Te vissvarīgākais, manuprāt, ir spēja spriest kas ir skaisti un lasāmi -- kas nē. Tev pašam ir jāsaprot kā ir labāk un tā arī ir jāraksta. Šo saprašanu var iegūt mēģinot un eksperimentējot. Izdari tā, tad izdari savādak un skaties -- kas ir lasāmāk, loģiskāk.

# «Galvenais, ka strādā!»

Šis citāts man liek degt elles dusmās. Protams, ka tas ir galvenais; tas ir primārais uzdevums.

Bet kas notiks vēlāk, kad tiks atrasts simts un viens bags un bizness prasīs jaunu funckionalitāti? Vaimanas par koda refaktorēšanu vai vispārīgu pārrakstīšanu viņus neinteresēs.