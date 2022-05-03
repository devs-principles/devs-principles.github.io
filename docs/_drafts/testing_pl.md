**Filar 1 - Testowanie**

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
To wszystko tylko wyjaśniało to, dlaczego w zespole QA zawsze było dużo pracy i panowała nieufność wobec kolegów tworzących kod.

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

Inną sprawą jest też to, że u ludzi pojawia się lenistwo oraz bagatelizowanie tematu. Dlatego nie zaskakują mnie już dzisiaj hasła w stylu: "Takiego testu nie ma sensu pisać, bo to sprawdzi QA"... na co kolega tester w danym dniu może zareagować podobną postawą, co może prowadzić do wprowadzenia problemu w aplikacji. 

***Czy problem w ogóle istnieje?***

Można się zastanowić czy mamy tu do czynienia z problemem, czy może temat jest niepotrzebnie wyolbrzymiony? W końcu ostatecznie produkt powstaje, jest przetestowany 
przez zespół testerów. Na pozostałe problemy (często zgłaszane już przez samych użytkowników) zakłada się bug'a, którego w końcu zostanie naprawiony. 
Każdy ma pracę i wszystko się kręci. 
Prawda?

Można na tym poprzestać i uznać, że tak pracuje się w IT. W końcu jest to branża, która sama tworzy problemy, aby później było co naprawiać;-)

***Ukryte konsekwencje***

Osoby, które pracują już kilka lat w branży, dostrzegają z czasem, że coś tu jednak nie gra. Najlpiej to widać w momencie, gdy trzeba tworzyć kolejne workaround'y (czyli łatanie dziur).
Nagle okazuje się, że stworzona aplikacja jest kosztowna w utrzymaniu, a jej dalszy rozwój jest bardzo utrudniony. Co w zasadzie jest cechą starego kodu (legacy code).
Zniechęceni pracownicy odchodzą, a w ich miejsce pojawiają się nowi, którzy stwierdzają, że ten kod jest do przepisania;-)

Uważam, że zdecydowana większość omawianych tu problemów wynika z powierzchownego podejścia do testowania tj. zajęcia, które wykonuje się na końcu implementacji, po to żeby tylko "coś tam" było.


***Sięgając po coś więcej***

Jeżeli czytasz ten wpis, to zakładam, że tak jak ja pragniesz jednak pracować inaczej! Pracować jak prawdziwy profesjonalista! Dlatego chcesz ulepszyć swoje rzemiosło. Szukasz pomysłów i sposobu na usprawnienie swojego warsztatu.

W tym i w kolejnych postach postaram się przekonać Cię, jak można pisać kod z którego będziesz dumny!:-)

Kod oparty na pierwszym filarze - TESTOWANIE!


----


Mapa? Albo trasa?

***Testy jednostkowe jako solidne fundamenty***

Kiedy znajomi czy rodzina pytają mnie o to, co ja właściwie robię jako programista, najczęściej odpowiadam im, że buduję programy - co często prowadzi do nieporozumienia. Ludzie dzwonią do mnie i pytają co mają zrobić w tej czy innej aplikacji, lub dlaczego nie mogą dodać czegoś do koszyka w jakimś serwisie... pomijam tu pytania o problemy z drukarką czy wirusami.
Zastanawiam się wtedy czy od inżynierów budowy też oczekuje się, że będą wiedzieli wszystko o budownictwie włączając w to budynki, których nie wybudowali i nie widzieli na oczy. W końcu budownictwo to jedna z kilku dziedziń, w których też coś się tworzy. Dodatkowo, budownictwo ma swój odcisk na branży IT - pierwsze projekty były realizowane wg metodologii 'waterfall' - tj. podejścia zarządzania projektami, znanego z budowanictwa, gdzie dostajemy wymagania biznesowe/techniczne, budujemy, sprawdzamy i oddajemy budowlę. W trakcie takiej budowy są audyty i drobne korekcje w planach, ale dostarczany obiekt w zasadzie w 90% pokrywa się z wymaganiami.

Dzisiaj, po blisko 50 latach tworzenia oprogramowania w podobny sposób, branża IT zmieniła kierunek na metodologie zwinne - najbardziej znana obecnie to Scrum. Stało się tak dlatego, że ponad 80% projektów nie spełniała wymagań klientów. Należałoby tu zaznaczyć, że pierwszymi klientami były urzędy, korporacje i duże firmy. Wymagania były spisywane w postaci dużych, często kilkuset stronicowych, dokumentów, które następnie były przekazywane do realizacji. Pomimo audytów, końcowy produkt, przekazany do użytku pracownikom, był bezużyteczny. Okazywało się, że procesy biznesowe były skomplikowane, interfajs był nieczytelny, a szybkość działania też pozostawiała wiele do rzyczenia. Pracownicy woleli wykonywać swoją pracę "po staremu", ponieważ wykonywanie czynności w znany im sposób był bardziej efektywny niż ten w nowej aplikacji. 

Wiele lat musiało upłynąć, zanim branża dostrzegła:
* niedociągnięcia w tworzeniu wymagań,
* brak konsultacji projektu z użytkownikiem końcowym czy
* zaakceptowanie ogólnej natury zmienności tworzonych produktów.

Stąd, dzisiaj już wiemy, że interacyjne podejście do tworzenia oprogramowania zmniejsza znacząco ryzyko niepowodzenia projektów. 

**Co to ma wspólnego z testowaniem?**

W IT tak samo jak w budownictwie ważne są fundamenty. Budynek może wznosić się w góre dzięki solidnej podstawie. Jeżeli ta okaże się zbyt słaba to może dojśc do tragedii i zawalenia konstrukcji. Z drugiej strony, jeżeli mamy twardą i wytrzymałą podstawę, to możemy wznieść na niej drapacz chmur.
Dlatego, dodając kolejną cegłę lub całe piętro kierownik budowy musi mieć pewność, że fundament wytrzyma dodatkowe obciążenie. Podstawa w pewnym sensie rośnie wraz z budynkiem, w końcu gdy dodajemy kolejne piętro budynku, to dla dodawanej konstrukcji, podstawą staje się wszystko co jest pod nią.

W IT jest bardzo podobnie. 

Dodajemy kod, który jest następnie wykorzystywany do budowania kolejnych warstw programu. 
No dobrze, ale czym jest fundament w IT? Zanim zaczniemy budować jakiegokolwiek oprogramowanie bierzemy pod uwagę m.in. takie elementy jak:
* środowisko uruchomieniowe (system lub chmura)
* jezyk programowania
* dostępność bibliotek (SDK)
* frameworki

Przykład wyboru to:
* środowisko uruchomieniowe - chmura
* język programowania - Java
* bibliteki - Java 11 SDK, apache, spark, itp
* frameworki - Spring Boot

Taki przykład jest dobrym wyborem do budowania wielu serwisów w internecie np. usług bankowych.

No dobrze, mamy fundamenty i co dalej?

Czytamy wymagania biznesowe i dodajemy nasze pierwsze cegły na wybranej platformie. Mamy tu do czynienia z szczęśliwym dostarczaniem nowej funkcjonalności (tzw. happy development). Programiści są zadowoleni z tego, że mogą pisać nowy kod zamiast poprawiać bug'i w istniejącym produkcie.
W przypadku start up'ów taki development często jest bez inwestowania czasu w testy jednostkowe, ponieważ najważniejsze jest to, żeby pokazać działające koncepcje w najprostrzej wersji.
Kiedy już powstał jakiś kod najczęściej na końcu dodawane są testy jednostkowe, żeby w pewnym sensie "wzmocnić konstrukcję" upewniając się, że implementacja faktycznie działa i dostacza tego, czego oczekuje biznes. 

       /OOOOO
      / -----\
     /  XXXXX \ 
    /   XXXXX  \

Fig 1: Wygląda to mniej więcej tak, jakbyśmy do zbudowanej konstrukcji przykładali rusztowania albo jakieś bale które miałyby tą konstrukcję trzymać w ryzach.

I tu często pojawia się pierwsza ze słabości takiego rozwiązania. Gdy mamy już napisany kod, programista skupia się przede wszystkim na napisaniu testów sprawdzających, że podstawowe przypadki działają. W końcu implementacja spełnia podstawowe wymagania biznesu, mamy kod, więc nie ma potrzeby tracić więcej czasu na skrajne przypadki.

Najważniesza myśl jest taka, że testy jednostkowe traktowane są jako "wzmocnienie konstrukcji" lub upewnie się, żę konstrukcja się nie zawali. Przez co testy stają się czymś obok. Jak są - to mówimy, że "dobrze, że są", a gdy ich nie ma to mówimy "możnaby jakieś testy napisać, jeżeli jest na to czas". 
Testy nie mają też bezpośredniego wpływu na konstrukcję, ponieważ są dopisywane na końcu implementacji danej funkcjonalności. Możnaby się tu zastanawiać czy w zasadzie są częścią konstrukcji czy nie. Myślę, że wiele osób jednak powie, że tak dopisywane testy nie są częścią budowanej konstrukcji ponieważ nie miały bezpośredniego wpływu na nią podczas jej tworzenia.

To podejście/mentalność ma dalsze konsekwencje. Powiedzmy, że został napisany kawałek kodu lub mówiąc bardziej ogólnie postawiony kawałek konstrukcji, który jest jakiś taki dziwny, trochę odstający, i w pewnym sensie niewygodny, ale spełnia podstwowe wymaganie. I teraz wiemy, że robi to co ma robić w tworzonej budowli i teraz potrzebujemy tylko go wzmocnić, czy podeprzeć, po to żeby mieć pewność, że postawiony w tym miejscu spełnia swoją funkcję, i że możemy na jego podstawie stawiać kolejne piętra budowli.
Nagle okazuje się, że ten kawałek nie jest łatwo podeprzeć... jest on na tyle nieforemny, że wzmacnianie go nie ma sensu na tym etapie, więc dochodzimy do wniosku, że dodamy kolejne piętra i wzmocnimy całość, gdy będzie więcej pięter i będzie wygodniej zaczepić się wyżej (testy integracyjne).

Takie podejście może doprowadzić do tego, że mamy bardzo mało podstawowych wsporników (testów jednostkowych), a dużo ogromnych przęseł wzmacniających całą konstrukcję (testy integracyjne).

Fig 2. Tu można pokazać obrazek, na którym jest budowla z wieloma mniejszymi podporami i obok taka co ma kilka podpór małych i wiele dużych podpór.

Koszty dodawania takich wielkich wsporników okaże się być większy, ponieważ będzie potrzeba ich więcej niż dodawanie na bieżąco mniejszych podpór. Jest to przykład odwórconej piramidy testów.

Ale koszt samych testów to jeszcze nic w porównaniu do kosztu zmiany wymagań czy nawet refaktoringu kodu. Okazuje się bowiem, że nie mając mniejszych podpór i bazując tylko na testach integracyjnych, jesteśmy narażeni na wprowadzanie większej ilości błedów do zaimplementowanego rozwiązania. To trochę tak, jakbyśmy w środku budowli zaczeli coś zmieniać i nagle zrobiłaby się wielka dziura w konstrukcji ponieważ nie było w tym obszarze mniejszych wzmocnień (testów jednostkowych). Niby cała konstrukcja stoi i testy integracyjne to potwierdzają, jednak właśnie doprowadziliśmy do nieoczekiwanego ubytky w funkcjonalności. 

Fig 3. Tu można pokazać jak kruszy się jakaś ściana budowli, żeby pokazać jak powstają ubytki funkcjonalności.

Oczywiście, można w ten sposób dalej budować produkt, jednak narażamy się w ten sposób na kolejne ubytki przy zmianie wymagań czy dodawaniu nowej funkcjonalności - pamiętajmy o tym, że cały czas coś tam się kruszy w samej konstrukcji.

Najprawdopodobniej zbudujemy coś zbliżonego do tego co wymaga klient. Jednak powstała konstrukcja będzie się chwiać i niechętnie będziemy chcieli wprowadzać w niej zmiany.

Fig 4. Tu można by pokazać jakąś budowlę, która nie jest pewna "wieża w Pizie" albo coś co w ten deseń....coś takiego w czym nikt nie chciałby wprowadzać zmnian bo grozi zawaleniem.

Należy pamiętać, że "zmiana" a raczej "ryzyko zmian" w IT to chleb powszedni i należy się z nim zawsze liczyć - dlatego projekty dostarcza się wykorzystując metodologie zwinne (patrz wyżej).

Czy możemy zrobić coś innego, żeby poprawić sytuację? 

Czy jesteśmy w stanie stawiać budowle wyżej i wyżej zawsze będąc pewnym, że podstawy i wzmocnienia mamy solidne?

Uważam, że TAK! Należy jednak zmienić myślęnie o testach jednotkowych. Zamiast dodawać podpory do zbudowanej konstrukcji, trzeba wykorzystać podpory jako podstawę do stawiania kolejnych warstw - traktując je jako podstawę kolejnych pięter.

Co to w ogóle znaczy?

Przed przystąpieniem do stawiania kolejnej konstrukcji, rozstawiamy rusztowanie (konstrukcję wspięrającą) zgodnie z wymaganiami jakie stawia biznes. Jeżeli mowa jest o tym, że w lewym rogu ma być antresola to stawiamy w tym miejscu odpowiednie rusztowanie aby tą antresole można było postawić. Dlatego piszemy test jednostkowy, który sprawdza to wymaganie. Nasz test nie przechodzi, ponieważ nie mamy jeszcze implementacji.
W podobny sposób rusztowanie pod antresolę pokazuje, że w tym miejscu powinna być antresola, ale jej jeszcze nie ma.
W kolejnym kroku budujemy anresolę w żądanym miejscu. Po wykonaniu pracy mamy antresolę i konstrukcję ją wspierającą. Dodatkowo, kształt i wymiar konstrukcji wspierającej w bezpośredni sposób wpłynął na to, jak wygląda antresola.

Dla porównania, gdyby najpierw zbudować antresolę i później dodać kilka elementów wspierających powstałą konstrukcję, mielibyśmy testy, które w bardzo niewielkim stopniu odzwierciedlają to jak antresola faktycznie wygląda.

Dlatego pisząc najpierw test lub stawiając najpierw konstrukcję wspierającą wg wymagań biznesu sprawiamy, że te elementy pomocnicze stają się częścią konstrukcji, ponieważ konstrukcja z niej wychodzi.  
Wyobraźmy sobie tak zbudowaną całą budowlę względem, której klient ma kolejne oczekiwania i wprowadza zmiany. Jakie jest ryzyko, że w takiej konstrukcji pojawią się ubydki w budowli? O wiele mniejsze, lub rzadne, ponieważ konstrukcje wspierające są częścią budynku.
Co sprawia, że te wcześniej omawiane ubytki są najprawdopodobniej zabezpieczone. Elementy, które w wyniku zmian powinny zostać usunięte, zostaną zburzone wraz z rusztowaniem, które je wspiera.
Przy czym rozbierając takie rusztowanie w danym miejscu będziemy je tak robić, żeby nie zepsuć innych elementów budowli.
Jest to pewne i świadome wprowadzanie zmian w kodzie, względem wcześniejszego liczenia na to, że dokonane zmiany nic nie zepsuły ponieważ mamy mnóstwo konstrukcji wspierających cała budowle (testy intergracyjne).

Opisywane podejście w budownictwie jest naturalnym sposobem na stawianie budowli. Mają na to wpływ prawa fizyki i siły, którym budynek musi się przeciwstawiać. Dlatego rusztowania, wsporniki lub inne konstrukcje pomocnicze są niezbędne do budowania budowli.

W IT jest inaczej. Programista jest w stanie stworzyć działający program bez wznoszenia nawet jednego "rusztowania" (testu jednostkowego). Wynika to zbraku ogólnie zrozumiałych dla wszystkich praw fizyki, jakie znamy z życia codziennego. 
Dzięki powszechnemu prawu ciążenia jesteśmy sobie w prosty sposób wyjaśnić czy zobrazować proces budowania budynków.
W IT nie ma tak prostego modelu. Cała branża, pomimo dokonania ogromnego postępu w tej dziedzinie, nadal poszukuje lepszego i pewniejszego (obarczonego mniejszym ryzkiem niepowodzenia) tworzenia programów.

Dlatego pokazana wyżej analogia z budownictwem dość dobrze przedstawia omawiany tu problem braku testowania, oraz dlaczego warto testować jak najwcześniej.

Implementacja tworzona na fundamentach testów jednostkowych to nic innego jak wprowadzone w branży pojęcie TDD - Test-Driven Development - implementacja sterowana testami.



















