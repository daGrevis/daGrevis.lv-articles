# Git repo uz sava servera

Gluži par to, kas ir Git, es nestāstīšu, bet pastāstīšu, kā izmantot Git repo privātām vajadzībām.

Vismaz mana problēma ar GitHub ir, ka viss, kas tur tiek hostēts, ir vai nu publisks visiem, vai nu privāts, bet par to ir jāmaksā. Nepārprotiet mani, es mīlu _open source_! Tomēr, ir gadījumi, kad repo vienkārši nedrīkst būt publiski pieejams (kaut vai frīlanc darbiņi). Ir Bitbucket, bet nu tas ir jauns serviss, līdzīgs GitHub, kas jāmācās... un, manām vajadzībām, efektu var panākt ar vienkāršāku ceļu, ja, protams, ir sava «Linux kaste»! :)

Uzstādīt pašam savu Git repo, kura ir privāta, ir daudz vienkāršāk, nekā domāju. Ar SSH piekonektējamies savam serverim, izpidlam `git init --bare private_repo` un... tas arī ir viss! Atslēgvārds šajā visā pasācienā ir «[--bare](http://www.bitflop.com/document/111)». Tagad no jebkura datora varam pieslēgties un sākt strādāt ar tikko izveidotu privāto repo: `git clone dagrevis@my_server:~/private_repo` (konekcijas dati un parole — tādi paši kā SSH).

**Labojums:** Izskatās, ka dažiem te kkas nesanāk. :)

    $ git init --bare cheese
    Initialized empty Git repository in /home/dagrevis/cheese/
    $
    Connection to 123.123.123.123 closed.
    ~  » git clone dagrevis@123.123.123.123:~/cheese
    Cloning into 'cheese'...
    Password:
    warning: You appear to have cloned an empty repository.
    ~  » cd cheese
    ~/cheese - [master] » touch foo
    ~/cheese - [master●] » git add .
    ~/cheese - [master●] » git commit -m "test commit"
    [master (root-commit) d9f89b2] test commit
    0 files changed
    create mode 100644 foo
    ~/cheese - [master] » git push -u origin master
    Password:
    Counting objects: 3, done.
    Writing objects: 100% (3/3), 217 bytes, done.
    Total 3 (delta 0), reused 0 (delta 0)
    To dagrevis@123.123.123.123:~/cheese
    * [new branch]      master -> master
    Branch master set up to track remote branch master from origin.
    ~/cheese - [master] » ssh dagrevis@123.123.123.123
    Password:
    Welcome to Ubuntu [..]
    $ cd cheese
    $ git log
    WARNING: terminal is not fully functional
    commit d9f89b2829af5954a45f2231dbaa8a03b33e9c24
    Author: Raitis Stengrevics <[..]>
    Date:   Thu Dec 6 13:07:08 2012 +0200

        test commit