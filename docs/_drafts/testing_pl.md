**Testowanie**

***Wstęp***

Zastanawiałem się od czego zacząć opisywanie kanonu zasad, którymi mógłby kierować się każdy programista. 
Wzorce projektowe? Algorytymy? A może struktury danych?... Tematów jest tak wiele, że w zasadzie można by 
spokojnie napisać kilka książek o każdym z osobna - przekonując jednocześnie, że "Tak! To jest najważniejsze!".

W mojej głowie jednak na pierwszy plan wychodzi - TESTOWANIE. 

Temat trochę kontrowersyjny, czasami niewygodny, a nade wszystko unikany i zaniedbywany.

Tak, pierwszą żelazną zasadą jest TESTOWANIE. I w tym miejscu postaram się opisać czym ono jest w teorii i praktyce.

Zapraszam:-)

***Filozofia***

Wielokrotnie w swojej praktyce spotykałem ludzi, którzy byli za testowanie oraz takich, którzy najchętniej  
nie testowaliby kodu w ogóle. Zawsze traktowali to jako nudny obowiązek po zakończeniu zadania.
Każda ze stron była w stanie podać dość przekonywające argumenty za i przeciw testowaniu. Co sprawiało, że 
omawiane pojęcie urastało do rangi filozoficznych rozważań. Trochę tak jakby znany wszystkim Makbet 
miałby nagle wielce zastanawiać się: "Testować, czy nie testować?".

Skąd taka rozbieżność i rozważania?

***Perspektywa***

Jako pierwszą podejrzaną wzywam - Perspektywę. W moim przypadku wskazanie jej jako winną całego zamieszania 
jest dość naturalne i oczywiste. Wynika to z mojego wcześniejszego doświadczenia jako tester.
Swoją przygodę w IT zacząłem od skrupulatnego sprawdzania aplikacji tworzonych przez kolegów programistów. 
Dlatego, gdy zmieniłem perspektywę i zacząłem pisać kod, który następnie był weryfikowany, pewne wyobrażenia 
o tym, jak powinno się tworzyć oprogramowanie zaczęły ulegać zmianie.
Okazało się, że pisanie testów bliżej kodu (testy jednostkowe) nie zawsze ma miejsce. I tu najczęściej padały 
slogany typu: "Brakło czasu na testy.", "Testy nie zostały wzięte pod uwagę podczas estymacji." i moje ulubione 
"Skończyłem implementację, więc teraz może dopiszę kilka testów."
Na początku kompletnie tego nie rozumiałem... w końcu, po co było rozmawiać o piramidzie testów i o tym jak ważne
jest wczesne testowanie kodu... W rzeczywistości wszystko było odwrócone do góry nogami.
Co w zasadzie potwierdzało to, dlaczego w zespole QA zawsze było dużo pracy i panowała nieufność wobec kolegów
tworzących kod.

Więc co z tą perspektywą jest nie tak? 

Obie strony QA i DEV chcą osiągnąć ten sam efekt, tj. dostarczyć oprogramowania, które spełnia oczekiwane biznesu.

Ale...

****QA nastawiony jest na psucie kodu****

Różnica w podejściu jest taka, że tester głębiej analizuje wymagania. Następnie na ich podstawie tworzy scenariusze 
testowe. Buduje wiedzę, albo inaczej bazę testów (test suite), która (często zautomatywana) jest podstawą do
udowadniania, że oprogramowanie działa. Dlatego QA'eje często stają się ekspertami w danej dziedzinie biznesowej.
Ilość narzędzi, jakich potrzebują do wykonywania pracy jest zdecydowanie mniejsza. A to z kolei pozwala im lepiej 
skupić się na swojej pracy.
Z drugiej strony ilość wiedzy biznesowej potrafi być przytłaczająca i tu w zależności od domeny, jedni będą lepiej
poruszać się w zawiłych zagadnieniach, a inni będą się w danej domenie gubić.

****DEV nastawiony jest na dostarczanie kodu****

Programista z drugiej strony jest bardzo nastawiony na dostarczanie implementacji. W jego głowie pojawiają się 
techniczne pytania typu: "Skąd pobrać dane?", "Czy powiadomić inny serwis?" lub "Czy użycie warstwy pośredniej to dobry pomysł?".
Oczywiście wszystko zależy od zadania, dlatego pytania będą mniej lub bardziej zawiłe. 
Do tego obrazu należałoby jeszcze dodać złożoność narzędzi, framework'ów oraz samego biznesu.
Na pewno nie jest to łatwe zadanie i w wielu przypadkach trudno się dziwić, że pracownicy są tak zafiksowani 
na dostarczaniu kodu, że na koniec dnia nie mają już czasu ani ochoty pisać testów jednostkowych.
Należy też dodać, że takie pisanie testów to kolejne linijki kodu + złożoność kolejnych narzędzi.

Inną sprawą jest też to, że u ludzi pojawia się lenistwo oraz bagatelizowanie tematu. Dlatego nie dziwi mnie 
już dzisiaj stwierdzenie w stylu: "Takiego testu nie ma sensu pisać, bo to sprawdzi QA"... na co kolega tester 
w danym dniu może zareagować podobnym lenistwem, co może prowadzić do wprowadzenia problemu w aplikacji. 

***Czy problem w ogóle istnieje?***

Można się zastanowić czy problem w ogóle istnieje? W końcu ostatecznie produkt powstaje, jest przetestowany 
przez zespół testerów. Na pozostałe problemy (często zgłaszane już przez samych użytkowników) zakłada się bug'a, 
którego w końcu się naprawi. Każdy ma pracę i wszystko jest okay. 
Prawda?









