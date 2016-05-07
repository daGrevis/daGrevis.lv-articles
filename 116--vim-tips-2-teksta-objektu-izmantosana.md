# Vim tips #2: Teksta-objektu izmantošana

Vim ir tāds jēdziens kā teksta-objekts. Šis jēdziens, vienkāršiem vārdiem, ir teksta apgabals. Apgabali var būt, piemēram, vārds, teikums, rindkopa utt.. Šajā rakstā es pastāstīšu, kā ar tiem var selektēt un, pēcāk, modificēt tekstu.

Pieņemsim, ka mums ir šāds kods:

    :::javascript
    var days = [
        "Monday",
        "Tuesday",
        "Wednesday",
        "Thursday",
        "Friday",
        "Saturday",
        "Sunday"
    ]

Ja kursors atrodas starp `[` un `]`, varam izdzēst lista saturu ar komandu `di[`.

    :::javascript
    var days = []

Ja mums ir šāds kods, un gribam stringa vietā (`"Cheese"`) ielikt `None`:

    :::python
    foo = {
        "bar": True,
        "baz": "Cheese"
    }

Dodamies uz jebkuru pozīciju, zem kuras strings ir definēts, un `ca"`.

Tagad strings būs izdzēsts un mēs būsim nonākuši «insert mode», lai varētu ierakstīt jauno saturu — rakstam `None`!

    :::python
    foo = {
        "bar": True,
        "baz": None
    }

Pašas komandas izskatās briesmīgas, bet tās, īstenībā, ir loģiskas; pat lasāmas! Piemēram, `di[` lasītos kā «delete inner `[`», bet `ca"` kā «change a `"`».

Vairāk informācijas Vim manuālī: `:help text-objects`.

**Labojums:** Lai visiem būtu skaidrs: komanda `i` (kā `cit`) izdzēsīs saturu iekš objekta, bet `a` (kā `cat`) izdzēsīs visu — ieskaitot objektu.