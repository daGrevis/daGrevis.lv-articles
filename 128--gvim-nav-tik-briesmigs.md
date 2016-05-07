# GVim nav tik briesmīgs

Tie, kas nezina, — Vim'am ir vairākas versijas, kur, divas populārākās, ir Vim un GVim. Atškirība ir tāda, ka «parastais Vim» ir konsoles appa, bet GVim — grafiskā. Visu laiku lietoju Vim, jo nespēju izturēt grafiskās appas un tā jūtos tuvāk Unix'am. Tomēr, Vim ir maza problēma — krāsu daudzums un fonti ir tik labi, cik nu tavs terminālis atļauj.

Nedaudz paspēlējos un atradu veidu, kā GVim padarīt tik pat vienkāršu kā «parasto Vim» — bez nekādiem tūlbāriem, meņučiem un citām Vim-lietotājam necienīgām, nevajadzīgām lietām!

Iekš `.bashenv`, `.zshenv` vai kāds jums tur šellis ir:

    :::sh
    function vim {
        gvim -p $@ & disown && exit
    }

Iekš `.vimrc` vai `.gvimrc`:

    :::viml
    if has("gui_running")

        " Removes all GUI stuff.
        set guioptions=

        " Tells to always use block-style cursor.
        set guicursor=a:block

        " Allows copying/pasting in GVim using <C-c> and <C-p>.
        nmap <C-v> "+gP
        imap <C-v> <Esc><C-v>i
        vmap <C-c> "+y
        cmap <C-v> <C-r>*
        " To copy from cmode, type `q:` and copy command from there.

    endif

Tas arī ir viss. Visi konfi un plagini strādās, un Vim varēs atvērt ar to pašu `vim` komandu. Lietas, kas mainās ir kopēšana un peistošana. Attiecīgi, lai kopētu — _<C-c>_, bet peistotu — _<C-v>_.

Tas, ko iegūstam, ir krāsas un foršākus fontus! Varbūt zemāk redzamajā piemērā tas nav tik izteikti, bet _the devil is in the details_!

Vim:

[![Vim](http://i.imgur.com/tuEQNJ9.png)](http://i.imgur.com/tuEQNJ9.png)

GVim:

[![GVim](http://i.imgur.com/kfMaVeU.png)](http://i.imgur.com/kfMaVeU.png)