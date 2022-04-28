**Testowanie**

***Wstęp***

Zastanawiałem się od czego zacząć opisywanie kanonu zasad, którymi mógłby kierować się każdy programista. 
Wzorce projektowe? Algorytymy? A może struktury danych?... Tematów jest tak wiele, że w zasadzie można by spokojnie napisać kilka książek o każdym z osobna - przekonując jednocześnie, że "Tak! To jest najważniejsze!".

Jednak, w mojej głowie na pierwszy plan wychodzi - TESTOWANIE. 

Temat trochę kontrowersyjny, czasami niewygodny, a nade wszystko unikany i zaniedbywany.

Tak, pierwszą żelazną zasadą jest TESTOWANIE. I w tym miejscu postaram się opisać czym ono jest w teorii i praktyce.

Zapraszam:-)

***Filozofia***

W swojej praktyce spotkałem ludzi, którzy byli za testowanie oraz takich, którzy najchętniej nie testowaliby kodu w ogóle. Zawsze traktowali to jako nudny obowiązek po zakończeniu zadania.
Każda ze stron była w stanie podać dość przekonywające argumenty za i przeciw testowaniu. Co sprawiało, że omawiane pojęcie urastało do rangi filozoficznych rozważań. Trochę tak jakby znany wszystkim Makbet miałby nagle wielce zastanawiać się: "Testować, czy nie testować?".

Skąd taka rozbieżność i rozważania?

***Perspektywa***

Jako pierwszą podejrzaną wzywam - Perspektywę. W moim przypadku wskazanie jej jako winną całego zamieszania jest dość naturalne i oczywiste. Wynika to z mojego wcześniejszego doświadczenia jako tester.
Swoją przygodę w IT zacząłem od skrupulatnego sprawdzania aplikacji tworzonych przez kolegów programistów. 
Dlatego, gdy zmieniłem perspektywę i zacząłem pisać kod, który następnie był weryfikowany, pewne wyobrażenia o tym, jak powinno się tworzyć oprogramowanie, zaczęły ulegać zmianie.
Okazało się, że pisanie testów bliżej kodu (testy jednostkowe) nie zawsze ma miejsce. I tu najczęściej padały slogany typu: "Brakło czasu na testy.", "Testy nie zostały wzięte pod uwagę podczas estymacji." i moje ulubione "Skończyłem implementację, więc teraz może dopiszę kilka testów."
Na początku kompletnie tego nie rozumiałem... w końcu, po co było rozmawiać o piramidzie testów i o tym jak ważne jest wczesne testowanie kodu... W rzeczywistości wszystko było odwrócone do góry nogami.
Co w zasadzie to wszystko potwierdzało to, dlaczego w zespole QA zawsze było dużo pracy i panowała nieufność wobec kolegów tworzących kod.

Więc co z tą perspektywą jest nie tak? W końcu obie strony QA i DEV chcą osiągnąć ten sam efekt, tj. dostarczyć oprogramowania, które spełnia oczekiwania biznesu.

Ale...

****QA nastawiony jest na psucie kodu****

Różnica w podejściu jest taka, że tester głębiej analizuje wymagania. Następnie na ich podstawie tworzy scenariusze testowe. Buduje wiedzę, albo inaczej bazę testów (test suite), która (często zautomatywana) jest podstawą do udowadniania, że oprogramowanie działa. 
QA'eje starają się w pewnym sensie zepsuć aplikację, często stają się przy tym ekspertami w danej dziedzinie biznesowej.
Ilość narzędzi, jakich potrzebują do wykonywania pracy jest zdecydowanie mniejsza, co pozwala im bardziej skupić się na swojej pracy.
Z drugiej strony ilość wiedzy biznesowej potrafi być przytłaczająca i tu w zależności od domeny, jedni będą lepiej poruszać się w jej zawiłych zagadnieniach, a inni będą się w danej domenie gubić.

****DEV nastawiony jest na dostarczanie kodu****

Programista jest bardzo nastawiony na dostarczanie implementacji. W jego głowie pojawiają się techniczne pytania typu: "Skąd pobrać dane?", "Czy powiadomić inny serwis?" lub "Czy użycie warstwy pośredniej to dobry pomysł?".
Oczywiście wszystko zależy od zadania, dlatego pytania będą mniej lub bardziej zawiłe. 
Do tego obrazu należałoby jeszcze dodać złożoność narzędzi, framework'ów oraz samego biznesu.
Na pewno nie jest to łatwe zadanie i w wielu przypadkach trudno się dziwić, że pracownicy są tak zafiksowani na dostarczaniu kodu, że na koniec dnia nie mają już czasu ani ochoty pisać testów jednostkowych.
Należy też dodać, że takie pisanie testów to kolejne linijki kodu + złożoność kolejnych narzędzi.

****Czynnik ludzki****

Inną sprawą jest też to, że u ludzi pojawia się lenistwo oraz bagatelizowanie tematu. Dlatego nie dziwi mnie już dzisiaj stwierdzenie w stylu: "Takiego testu nie ma sensu pisać, bo to sprawdzi QA"... na co kolega tester w danym dniu może zareagować podobną postawą, co może prowadzić do wprowadzenia problemu w aplikacji. 

***Czy problem w ogóle istnieje?***

Można się zastanowić czy mamy tu do czynienia z problemem, czy może temat jest niepotrzebnie wyolbrzymiony? W końcu ostatecznie produkt powstaje, jest przetestowany 
przez zespół testerów. Na pozostałe problemy (często zgłaszane już przez samych użytkowników) zakłada się bug'a, którego w końcu się naprawi. 
Każdy ma pracę i wszystko się kręci. 
Prawda?

Można na tym poprzestać i uznać, że tak pracuje się w IT. W końcu jest to branża, która sama tworzy problemy, aby później było co naprawiać;-)

***Ukryte konsekwencje***

Osoby, które pracują już kilka lat w branży, dostrzegają z czasem, że coś tu jednak nie gra. Najlpiej to widać w momencie, gdy trzeba tworzyć kolejne workaround'y (czyli łatanie dziur).
Nagle okazuje się, że stworzona aplikacja jest kosztowna w utrzymaniu, a jej dalszy rozwój jest bardzo utrudniony. Co w zasadzie jest cechą starego kodu (legacy code).
Zniechęceni pracownicy odchodzą, a w ich miejsce pojawiają się nowi, którzy stwierdzają, że ten kod jest do przepisania;-)

Uważam, że zdecydowana większość omawianych tu problemów wynika z powierzchownego podejścia do testowania. Zajęcia, które wykonuje się na końcu implementacji, po to żeby tylko "coś tam" było.


***Sięgając po coś więcej***

Jeżeli czytasz ten wpis, to zakładam, że tak jak ja pragniesz jednak pracować inaczej! Pracować jak prawdziwy profesjonalista! Dlatego chcesz ulepszyć swoje rzemiosło. Szukasz pomysłów i sposobu na usprawnienie swojego warsztatu.

W tym i w kolejnych postach postaram się przekonać Cię, jak można pisać kod z którego będziesz dumny!:-)











