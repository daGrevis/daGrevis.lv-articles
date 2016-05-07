# Vim konfigurācija

Izdomāju pastāstīt par Vim konfigurāciju un plaginiem, kurus izmantoju.

[![Vim](http://i.imgur.com/vdrXZkH.png "Vim")](http://i.imgur.com/GK3mjai.jpg)

# .vimrc dotfails

Dotfails `.vimrc` ir fails, kurš satur konfigurāciju Vim editoram. Šis fails ir VimL (Vim valoda) un, bieži vien, satur ne tikai būleān-tipa konfigurāciju, bet arī kīj-baindingus un pat funkcijas!

Lūk arī daži «izvilkumi» no tā...

    :::viml
    " Sets fave color scheme.
    colorscheme solarized

Vim, iespējams, ir visplašākā izvēle krāsu shēmās visā pasaulē! Pēdējās nedēļās lietoju [Solarized](http://ethanschoonover.com/solarized), bet esmu arī fans [Monokai](http://studiostyl.es/schemes/monokai)!

    :::viml
    " Shows relative line numbers.
    set relativenumber

Vai ziniet tos cipariņus, kas rādās sānā visiem editoriem? Man arī tādi ir, tikai relatīvi (skatīt attēlu no Vim) — tas ir priekš pārvietošanās uz augšu/leju, izmantojot multiplajeri (piemēram, `10j`).

    :::viml
    " Fix broken Vim regexes.
    nnoremap / /\v
    vnoremap / /\v
    nnoremap ? ?\v
    vnoremap ? ?\v

Vima regeksi strādā jocīgi. Šis te ieslēdz regeksus, kas strādā līdzīgi kā Perl.

    :::viml
    " I don"t like to hold <S> key.
    nore ; :

Lai Vimā ievadītu komandu, ir jāspiež `:`. Lai dabūtu to taustiņu, ir jātur `Shift` (jeb `<S>`). Es to daru ļoti, ļoti bieži. Man patiešām rūp kījstroukes!

    :::viml
    " Emacs ways to change cursor in cmode (<C-a> to get to the start, but <C-e>
    " -- to the end).
    cmap <C-a> <Home>
    cmap <C-e> <End>

Ok, tiek ievadīta gara komanda... bet vai (!), pats sākums ir nepareizs! Te nu nāk talkā Emacs bindingi, kas, starp citu, ir pieejami arī pašā terminālī.

    :::viml
    " Maps <Right> to indenting text to the right, but <Left> to the left. Works
    " in mode and vmode.
    nmap <Left> <<
    nmap <Right> >>
    vmap <Left> <gv
    vmap <Right> >gv

    " Maps <Up> to spawning blank line above, but <Down> -- below.
    nmap <Up> O<Esc>j
    nmap <Down> o<Esc>k

Mēs taču **ne**izmantojam bultiņas, vai ne? Ļoti labi!, — tagad padarīsim bultiņas noderīgas kkam citam, kas, tomēr, nav tik bieža operācija kā `hjkl`!

    :::viml
    " Maps <Leader>p in imode to go in pmode.
    inoremap <Leader>p <C-o>:set paste<CR>
    " Unsets pmode when leaving imode.
    au InsertLeave * :set nopaste
    " Fixes that InsertLeave event doesn"t catch <C-c> mapping.
    inoremap <C-c> <Esc>

Kas notiek, kad esam ieslēguši maģisko indentāciju un peistojam no, teiksim, browsera Vimā? Notiek haoss! Lūk, mana ideja, kā to atrisināt. Attiecīgi, imoudē, spiežot `<Leader>p`, Vim mūs iemētīs pmoudā, kas, pēc tam, ejot atpakaļ uz nmoudi, unsetosies.

Visu to un vēl var atrast [daGrevis/Dotfiles](https://github.com/daGrevis/Dotfiles) repo! Viss ir radoši sakomentēts un, ik pa laikam, tiek uzlabots.

# Plagini

Esmu mēģinājis tonnas plaginu. Tagad aprakstīšu tos izredzētos, ilgdzīvotājus — tos, bez kuriem nevaru!

## Pathogen

Šis plagins ir kā helperis, lai uzinstalētu citus. Pēc šī plagina instalācijas citus plaginus var uzinstalēt sekundēs.

## Sensible

Šis plagins satur Vim konfigu, kādu izmanto 90% no Vim lietotājiem. Tieši tāpēc manā `.vimrc` nav lietas, kas parasti ir citur — tās man garantē plagins.

## Powerline

Vim status-bars ir noderīga lieta. Diemžēl, tā nav vissmukākā lieta.

Arī, šis plagins ir jau nokonfigurēts, lai strādātu ar citiem plaginiem (piemēram, Fugitive).

## Syntastic

Koda lintošana. Tiek izmantoti ārējie linteri, lai čekotu sintaksi, atbilstību standartiem utt. utjp..

## Commentary

Helperis komentēšanai. Aizkomentējam, atkomentējam utt..

## MatchTag

Kāds uzspiež atvērt XML vai HTML dokumentu? Šis plagins iekrāso atverošo un aizverošo tagu, lai tu nejustos pilnīgi zudis.

## Surround

Šis plagins ir par lietām, kas ir apkārt lietām. Piemēram, ar dažiem kījstrokiem varam aplikt ap teikumu `<p>` tegu (`yss<p>`) vai, teiksim, izdzēst iekavas ap vārdu (`ds(`).

## Fugitive

Git editorā! Atzīšos, ka šo te izmantoju tikai fiksajam bleimam (`git blame` jeb, iekš Vim, `:Gblame`).

_Yet!_

## NERDTree

Failu struktūra trī formātā. Šo es izmantoju tikai, lai saprastu kur ir kas.

## Tagbar

Koda struktūra trī formātā. Šis te parādīs klases, metodes utt. attiecīgajā failā un ļaus pie tām nokļūt.

## Repeat

Komanda `.` ir spēks (tiem, kas nezina -- šī komanda atkārto pēdējo izpildīto komandu vēlreiz)! Šis plagins uztaisa tādu kā huku citiem plaginiem, kā rezultātā — citi plagini var sadraudzēties ar `.` komandu.

## CtrlP

Fuzī vai regeksu meklēšana pēc faila nosaukuma. Atveram vajadzīgo failu nekavējoties!

## Ack

Meklēšana failos izmantojot [Ack](http://betterthangrep.com/). Pēcāk, varam atrasto failu arī atvērt.