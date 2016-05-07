# Git auto-complete

Ļoti bieži izmantoju CLI. Iespējams vairāk laiku pavadu termināli, nekā GUI! Lai tiktu ieekonomēts laiks, izmantoju «auto-complete», lai nebūtu tik daudz jāraksta un būtu mazāks kļūdīšanās procents. Un ar «auto-complete» es domāju «Tab» taustiņu.

Tā kā esmu programmētājs — es lietoju versiju kontroli. Manā gadījumā, Git. Nebūs pārsteigums, ka Git'u lietoju arī «caur CLI»! Problēma un sāpe tāda, ka Git nepiedāvā «auto-complete» fīču. Jūs pat nevarat iedomāties, cik bieži kļūdos rakstot vārdu «checokut»!

Tad nu lūk risinājums, lai arī Git'am būtu «auto-complete» fīča.

Iekš `~/.bashrc`:

`source /usr/share/git/completion/git-completion.bash`

Ļoti patikāmi, ka tiks piedāvātas ne tikai, piemēram, komandas, bet arī, teiksim, pēc `git checkout`, brenči. Un tamlīdzīgi. :)