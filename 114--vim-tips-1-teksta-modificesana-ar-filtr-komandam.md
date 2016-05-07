# Vim tips #1: Teksta modificēšana ar filtr-komandām

`:help !`

    4. Complex changes                                      complex-change

    4.1 Filter commands                                     filter

    A filter is a program that accepts text at standard input, changes it in some
    way, and sends it to standard output.  You can use the commands below to send
    some text through a filter, so that it is replaced by the filter output.
    Examples of filters are "sort", which sorts lines alphabetically, and
    "indent", which formats C program files (you need a version of indent that
    works like a filter; not all versions do).  The 'shell' option specifies the
    shell Vim uses to execute the filter command (See also the 'shelltype'
    option).  You can repeat filter commands with ".".  Vim does not recognize a
    comment (starting with '"') after the :! command.

                                                            !
    !{motion}{filter}       Filter {motion} text lines through the external
                            program {filter}.

Pieņemsim, ka mums ir C kods, kurš ir nesmuki formatēts, jo indentācija šajā valodā nav uzspiesta.

    :::c
    #include <stdio.h>

    void
    foo(void) {
            printf("Hello");
    }

    int         main(  void) {
    return 0;}

Kā jau manuālī minēts (skatīt augstāk), varam izmantot `indent` komandu.

`:%!indent`

    :::c
    #include <stdio.h>

    void
    foo (void)
    {
        printf ("Hello");
    }

    int
    main (void)
    {
        return 0;
    }

Esmu liels Markdown fans. Lūk piemērs, kā varu izmantot Vim un `markdown` komandu savā labā!

    # Header1

    ## Header2

    **bold**

    _italic_

`:%!markdown`

    :::html
    <h1>Header1</h1>

    <h2>Header2</h2>

    <p><strong>bold</strong></p>

    <p><em>italic</em></p>

Ļoti atbalstu šo filozofiju:

> This is the Unix philosophy: Write programs that do one thing and do it well. Write programs to work together. Write programs to handle text streams, because that is a universal interface.

`:%!cowsay`

    _____________________________________
    < Šis raksts neliekas pabeigts... :) >
    -------------------------------------
            \   ^__^
            \  (oo)\_______
                (__)\       )\/\
                    ||----w |
                    ||     ||