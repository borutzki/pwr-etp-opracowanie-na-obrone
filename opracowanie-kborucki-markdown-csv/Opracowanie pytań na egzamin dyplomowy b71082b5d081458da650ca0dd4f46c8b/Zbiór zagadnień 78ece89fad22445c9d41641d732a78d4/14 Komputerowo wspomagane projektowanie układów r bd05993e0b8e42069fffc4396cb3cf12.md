# 14. Komputerowo wspomagane projektowanie układów regulacji

Status: Zrobione

### a) kaskadowa struktura regulacji a struktura sterowania z regulatorem stanu - schemat blokowy, zasada działania, dobór parametrów, właściwości

**Struktura kaskadowa**

W strukturze kaskadowej pojawiają się **dwie pętle sterowania**: nadrzędna oraz podrzędna. Każda z pętli ma swój regulator, który kompensuje określoną stałą czasową układu. W przypadku silnika prądu stałego, **regulator prądu niweluje stałą czasową elektromagnetyczną silnika**, natomiast **regulator prędkości - stałą czasową mechaniczną**.

![Untitled](14%20Komputerowo%20wspomagane%20projektowanie%20uk%C5%82ado%CC%81w%20r%20bd05993e0b8e42069fffc4396cb3cf12/Untitled.png)

Działanie układu polega na tym, że nadrzędny regulator prędkości, na podstawie uchybu prędkości, zadaje wartość prądu. Podrzędny regulator na podstawie uchybu prądu zadaje wartość napięcia przekształtnika. Pętla wewnętrzna jest zależna od sygnału pętli zewnętrznej.

W strukturze kaskadowej stosuje się **regulatory liniowe**, najczęściej PI. Ich parametry można dobierać za pomocą uproszczonych **kryteriów modułu i symetrii** lub przy wykorzystaniu **metody rozłożenia biegunów** na podstawie równania charakterystycznego. 

Układ kaskadowy cechuje się tym, że **dynamika pętli nadrzędnej jest zależna od dynamiki pętli podrzędnej**. Jeżeli różnica czasów reakcji obu pętli jest niewielka, w układzie mogą pojawiać się oscylacje. Zasadniczą cechą jest natomiast to, że **dwie pętle - prędkościowa i prądowa - sterowane są osobno** przez dwa regulatory.

**Struktura sterowania z regulatorem stanu**

W przypadku struktury z regulatorem stanu, wszystkie sterowane zmienne są uwzględnione w pętli sprzężenia zwrotnego przy wejściu układu. Regulator stanu można stosować dla obiektów każdego rzędu. **Struktura regulatora stanu bazuje na równaniach stanu obiektu**. 

![Untitled](14%20Komputerowo%20wspomagane%20projektowanie%20uk%C5%82ado%CC%81w%20r%20bd05993e0b8e42069fffc4396cb3cf12/Untitled%201.png)

Działanie regulatora stanu opiera się o **jednoczesne sterowanie wszystkimi zmiennymi**. Regulator uwzględnia każdą z nich w sprzężeniu zwrotnym na wejściu układu. Zmiana sygnałów wyjściowych powoduje zmianę uchybu. Uchyb jest tu sygnałem sterującym. 

**Projektowanie układu z regulatorem stanu polega na wyznaczeniu wzmocnień w pętlach sprzężeń zwrotnych** poszczególnych zmiennych. Wzmocnienia dobiera się **metodą rozłożenia biegunów**. Ponadto, na wejście układu można wprowadzić człon całkujący, który niweluje uchyb ustalony mogący pojawić się przy wystąpieniu zakłócenia. Oprócz tego, nie wszystkie zmienne można zawsze mierzyć, więc w przypadku sterowania przy użyciu regulatora stanu **na ogół stosuje się estymatory** zmiennych stanu. 

![Untitled](14%20Komputerowo%20wspomagane%20projektowanie%20uk%C5%82ado%CC%81w%20r%20bd05993e0b8e42069fffc4396cb3cf12/Untitled%202.png)

Jak już wspomniano, regulator stanu **steruje wszystkimi zmiennymi jednocześnie.** Jest to najprostsza możliwa struktura regulacji. Regulator ten sprawdza się bardzo dobrze w systemach, w których zachodzi potrzeba **kontrolowania dużej liczby zmiennych** (stąd jego stosowanie w układach dwumasowych). Do wad regulatora stanu należy jego **podatność na zmiany w układzie**, **trudność w nakładaniu ograniczeń** na zmienne stanu (trzeba stosować zaawansowane techniki) oraz częsta **konieczność stosowania estymatorów** zmiennych stanu.

**Podsumowując...**

Podsumowując, struktura kaskadowa dobrze sprawdza się tam, gdzie chcemy wprowadzać ograniczenia zmiennych sterowanych, najlepiej w prostych, nieskomplikowanych układach. 

Układ z regulatorem stanu natomiast najlepiej sprawdza się tam, gdzie potrzebna jest kontrola wielu sygnałów jednocześnie. Ze względu na prostotę (po prostu system wzmocnień), regulator stanu dobrze sprawdza się jako regulator w układach rozmytych lub adaptacyjnych.  

**Źródła**

[1] Notatki z wykładu *Komputerowo wspomagane projektowanie układów regulacji*

[2] Materiały z wykładu *Automatyka napędu elektrycznego - zagadnienia wybrane*

[3] Roland Buchi, Markus Kottmann - *State regulator with observer -* [https://www.researchgate.net/profile/Mohamed_Mourad_Lafifi/post/initial_condition_for_observer/attachment/5dd92817cfe4a777d4f3b1fa/AS%3A828380303851520%401574512663125/download/State+Regulator+with+Observer.pdf](https://www.researchgate.net/profile/Mohamed_Mourad_Lafifi/post/initial_condition_for_observer/attachment/5dd92817cfe4a777d4f3b1fa/AS%3A828380303851520%401574512663125/download/State+Regulator+with+Observer.pdf)

[4] [https://digitalcollection.zhaw.ch/bitstream/11475/3792/2/2010_Buechi_State-Space-Control-LQR-and-Observer.pdf](https://digitalcollection.zhaw.ch/bitstream/11475/3792/2/2010_Buechi_State-Space-Control-LQR-and-Observer.pdf)

[5] [http://yadda.icm.edu.pl/baztech/element/bwmeta1.element.baztech-6c0892fc-8aa0-48eb-929f-1c3a42c5a357](http://yadda.icm.edu.pl/baztech/element/bwmeta1.element.baztech-6c0892fc-8aa0-48eb-929f-1c3a42c5a357)

### b) układ regulacji z regulatorami rozmytymi - struktury, metody projektowania

Układy regulacji z regulatorami rozmytymi bazują na regulatorach rozmytych. Regulatory rozmyte to regulatory, których prawo sterowania jest opisane regułami lingwistycznymi. Prawo sterowania to relacja między wejściem a wyjściem regulatora - np. w regulatorze PI jest to suma transmitancji członów P oraz I. 

Prawo sterowania regulatorów rozmytych operuje na zmiennych lingwistycznych, które można opisać za pomocą przesłanek i konkluzji. Przesłanki są to sygnały wejściowe, natomiast konkluzje - sygnały wejściowe. Bazowy “wzór” na funkcję sterowania to:

<aside>
💡 JEŻELI <przesłanka> TO <konkluzja>

</aside>

W regulatorach rozmytych, wartości wejść są określane za pomocą funkcji przynależności. Funkcja przynależności przyjmuje wartości od 0 do 1. Sygnały wejściowe regulatora mają więc przypisane wartości funkcji przynależności. Im bardziej sygnał mieści się w zakresie opisanym funkcją przynależności, tym większą wartość przyjmuje ona dla tego sygnału. Na podstawie funkcji przynależności budowane są konkluzje.

![Untitled](14%20Komputerowo%20wspomagane%20projektowanie%20uk%C5%82ado%CC%81w%20r%20bd05993e0b8e42069fffc4396cb3cf12/Untitled%203.png)

Działanie regulatora rozmytego polega na tym, że rozmywa on sygnały wejściowe, przypisując im określone wartości różnych funkcji przynależności - czyli tworzy przesłanki. 

![Untitled](14%20Komputerowo%20wspomagane%20projektowanie%20uk%C5%82ado%CC%81w%20r%20bd05993e0b8e42069fffc4396cb3cf12/Untitled%204.png)

W następnym kroku, na podstawie przynależności sygnałów, dokonywane jest wnioskowanie.  Wnioskowanie przypisuje przesłanki do konkluzji, czyli na podstawie wartości funkcji przynależności sygnałów wejściowych, określa funkcję przynależności sygnału wyjściowego.

Po wnioskowaniu następuje wyostrzanie, czyli przypisanie konkretnej wartości wyjścia regulatora.

![Untitled](14%20Komputerowo%20wspomagane%20projektowanie%20uk%C5%82ado%CC%81w%20r%20bd05993e0b8e42069fffc4396cb3cf12/Untitled%205.png)

**Rodzaje regulatorów rozmytych**

Wyróżnia się dwa rodzaje regulatorów rozmytych: regulatory Mamdaniego oraz regulatory TSK. 

**Regulatory Mamdaniego** mają funkcje przynależności dla wejść oraz funkcję przynależności dla wyjść (wyjścia). Wskutek defuzyfikacji (wyostrzania) uzyskuje się tu jednoznaczną wartość. Regulatory Mamdaniego są przystosowane do stosowania reguł lingwistycznych.

![Untitled](14%20Komputerowo%20wspomagane%20projektowanie%20uk%C5%82ado%CC%81w%20r%20bd05993e0b8e42069fffc4396cb3cf12/Untitled%206.png)

**Regulatory TSK** (Takagi-Sugeno-Kanga) zawierają natomiast konkluzję funkcyjną, czyli konkluzja nie ma określonej wartości, lecz wartość określoną poprzez funkcję wartości zmiennych wejściowych. Wyjście nie jest defuzyfikowane. Regulatory TSK są przystosowane do analizy matematycznej.

![Untitled](14%20Komputerowo%20wspomagane%20projektowanie%20uk%C5%82ado%CC%81w%20r%20bd05993e0b8e42069fffc4396cb3cf12/Untitled%207.png)

Regulatory Mamdaniego wykorzystuje się na ogół przy niewielkiej liczbie wejść. Regulatory TSK wykorzystuje się tam, gdzie liczba wejść jest znacząca - regulatory te są bardziej skomplikowane. 

**Struktury układów sterowania z regulatorami rozmytymi**

Regulatory rozmyte w układach sterowania napędami stosuje się jako zastępstwo regulatorów PI. Sygnałami wejściowymi są tu uchyb oraz zmiana (pochodna) uchybu. 

![Untitled](14%20Komputerowo%20wspomagane%20projektowanie%20uk%C5%82ado%CC%81w%20r%20bd05993e0b8e42069fffc4396cb3cf12/Untitled%208.png)

**Metody projektowania układów sterowania z regulatorami rozmytymi**

Projektowanie regulatorów rozmytych typu Mamdaniego polega na zdefiniowaniu funkcji przynależności wejść i wyjść. Oznacza to zdefiniowanie bazy reguł. Funkcje te mogą być oparte na doświadczeniu operatorów i nie muszą być liniowe. Należy pamiętać, że reguły nie powinny być ze sobą sprzeczne, ale powinny przy tym zapewniać pokrycie całego zbioru wartości sygnałów.

W regulatorach typu TSK należy natomiast zdefiniować funkcje przynależności sygnałów wejściowych oraz na ich podstawie bazę reguł, która określa wzmocnienia dla funkcji wyjścia regulatora. 

Powyższe regulatory można projektować m.in. w środowisku Matlab przy wykorzystaniu odpowiednich wtyczek, ułatwiających opisywanie reguł (funkcji przynależności). 

**Źródła**

[1] [http://www.cs.put.poznan.pl/pzakrzewski/iss/iss_wykład_3.pdf](http://www.cs.put.poznan.pl/pzakrzewski/iss/iss_wyk%C5%82ad_3.pdf)

[2] [https://www.researchgate.net/post/What_is_the_difference_between_Mamdani_Method_and_Takagi-Sugeno-kang_Method_TSK](https://www.researchgate.net/post/What_is_the_difference_between_Mamdani_Method_and_Takagi-Sugeno-kang_Method_TSK)

[3] [https://yadda.icm.edu.pl/yadda/element/bwmeta1.element.baztech-d8413fca-a7a6-4e26-92bb-d22d9636876c/c/Drozdz.pdf](https://yadda.icm.edu.pl/yadda/element/bwmeta1.element.baztech-d8413fca-a7a6-4e26-92bb-d22d9636876c/c/Drozdz.pdf)

[4] [https://eti.pg.edu.pl/documents/176593/26523587/ProsteRegRozmyte.pdf](https://eti.pg.edu.pl/documents/176593/26523587/ProsteRegRozmyte.pdf)

[5] [https://we.pb.edu.pl/kair/wp-content/uploads/sites/4/2020/10/rozmyte.pdf](https://we.pb.edu.pl/kair/wp-content/uploads/sites/4/2020/10/rozmyte.pdf)

[6] Notatki z wykładu *Komputerowo wspomagane projektowanie układów regulacji*

### c) sterowanie predykcyjne układów dynamicznych - idea sterowania, metoda projektowania, właściwości

Sterowanie predykcyjne polega na przewidywaniu przyszłych stanów obiektu sterowanego na podstawie jego modelu matematycznego. W sterowaniu tym porównuje się obecny stan obiektu z jego przewidywanym przyszłym stanem i stara się zminimalizować uchyb sterowanej wielkości. 

Liczba przewidywanych przedziałów czasowych (kroków) w przypadku sterowań nazywana jest **horyzontem sterowań**, natomiast w przypadku wyjść - czyli zachowań obiektu - **horyzontem predykcji**. Horyzont predykcji jest zawsze większy niż horyzont sterowań. 

Obliczenia stanów obiektów w horyzoncie sterowań i horyzoncie predykcji opiera się o model matematyczny, który musi zostać sformułowany. Po każdej zmianie sterowania, obliczenia są wykonywane ponownie dla nowego stanu początkowego.  

<aside>
💡 Idea sterowania predykcyjnego polega na tym, że minimalizuje się błąd, który jeszcze nie powstał.

</aside>

**Idea algorytmu sterowania i sformułowanie funkcji celu**

Przy stosowaniu sterowania predykcyjnego, należy zdefiniować funkcję celu, czyli wskaźnik jakości sterowania, oparty o model matematyczny obiektu. Przy predykcji dąży się do takiego doboru sterowań, aby wartość zdefiniowanego wskaźnika jakości minimalizować - wykonuje się zatem obliczenia różnych wariantów sterowań układem, a następnie wybiera to, przy którym wskaźnik jakości przyjmuje najmniejszą wartość.

Oprócz wskaźników jakości sterowania, w algorytmie sterowania predykcyjnego należy uwzględnić również ograniczenia wielkości sterowanych - i dopiero po ich uwzględnieniu, dokonywać procesu minimalizacji funkcji celu.

Idea algorytmu sterowania polega na tym, że w pierwszej chwili wyznacza się wartość wektora stanu (poprzez pomiar lub estymację). Jest to określenie warunków początkowych.

Następnie rozwiązuje się problem optymalizacyjny, minimalizując określony wskaźnik jakości sterowania w celu wyznaczenia sekwencji sterowań. Następnie wprowadza się określone sterowanie na obiekt. Proces ten jest iteracyjny - powtarza się z każdym krokiem. 

![Untitled](14%20Komputerowo%20wspomagane%20projektowanie%20uk%C5%82ado%CC%81w%20r%20bd05993e0b8e42069fffc4396cb3cf12/Untitled%209.png)

Sterowanie predykcyjne można dzielić na sterowanie online i offline. To pierwsze polega na przeprowadzaniu predykcji w czasie działania układu - co wymaga bardzo szybkich obliczeń, skraca więc horyzont predykcji i sterowania. Natomiast sterowanie offline pozwala na przeprowadzanie predykcji poza obiektem, a następnie wprowadzeniu wartości optymalnych sterowania na obiekt, w postaci np. lookup-tables, 

**Metoda projektowania**

1. **Zdefiniowanie modelu obiektu**. To na modelu opierają się wszystkie predykcje i obliczenia w układzie predykcyjnym, więc im lepsze odwzorowanie rzeczywistego obiektu, tym lepsze działanie układu.
2. **Określenie kryterium jakości regulacji**. Kryteria jakości regulacji są pewnymi działaniami na uchybach wielkości sterowanych i generalnie dąży się do ich minimalizacji. Na potrzeby układów predykcyjnych, kryteria jakości regulacji są tym, wobec czego optymalizowane jest sterowanie - np. efektywność energetyczna. 
3. **Zdefiniowanie horyzontów predykcji i sterowania.** Horyzont predykcji mówi, na ile próbek do przodu obliczane są wartości sygnału wyjściowego przy określonym sterowaniu. Horyzont sterowania definiuje natomiast liczbę próbek, po których sygnał sterujący powinien dojść do zera, czyli układ powinien osiągnąć wartość zadaną. 
4. **Zdefiniowanie trajektorii odniesienia. Opcjonalnie.** Trajektorię odniesienia definiuje się jako pożądaną zmianę wielkości sterowanej. Dąży się do takiego sterowania, by rzeczywista trajektoria była jak najbliżej trajektorii odniesienia. 

**Właściwości układu**

Sterowanie predykcyjne pozwala na uwzględnianie ograniczeń nałożonych na wielkości regulowane i sterujące już na etapie projektowania regulatora. Sterowanie to sprawdza się dobrze w układach nieliniowych.

Ponadto, możliwość predykcji stanów obiektów złożonych pozwala na sterowanie układami trudnymi (oscylacyjnymi, niestabilnymi, nieliniowymi, niestacjonarnymi). Sterowanie to jest również mało wrażliwe na zmiany parametrów obiektu.

Do wad należy duża wrażliwość na zmiany struktury obiektu, złożoność obliczeniowa oraz trudność w modelowaniu sterowanego obiektu. Ponadto, sterowanie online wymaga bardzo szybkiego procesora obliczeniowego co sprawia, że częściej stosuje się rozwiązania offline.

**Źródła**

[1] Notatki i materiały z wykładu *Automatyka napędu elektrycznego - zagadnienia wybrane*

[2] Wikipedia [https://pl.wikipedia.org/wiki/Sterowanie_predykcyjne#Zalety_i_wady_regulacji_predykcyjnej](https://pl.wikipedia.org/wiki/Sterowanie_predykcyjne#Zalety_i_wady_regulacji_predykcyjnej) 

### d) sterowanie ślizgowe układów dynamicznych - idea sterowania, metoda projektowania, właściwości

**Idea sterowania**

W sterowaniu ślizgowym mamy do czynienia z regulacją określonych wielkości poprzez **załączanie naprzemiennie dwóch stanów przekształtnika**, **zależnie od aktualnego położenia trajektorii fazowej układu względem funkcji (prostej) przełączeń na płaszczyźnie fazowej**. 

Nazwa sterowania pochodzi od ruchu ślizgowego, w którym przełączanie dwustanowe powoduje zmianę kierunku trajektorii wielkości sterowanej. Pod**ążanie po za prostą przełączeń polega na jej wielokrotnym przecinaniu, przy możliwie jak najbliższym położeniu względem niej**.

![Untitled](14%20Komputerowo%20wspomagane%20projektowanie%20uk%C5%82ado%CC%81w%20r%20bd05993e0b8e42069fffc4396cb3cf12/Untitled%2010.png)

**Projektowanie**

Idea sterowania ślizgowego opiera się właśnie o **zdefiniowanie prostej przełączeń na płaszczyźnie fazowej**, na której **osią x jest uchyb wielkości**, natomiast **osią y jest dynamika (pochodna) tego uchybu**, czyli de facto dynamika sterowanej wielkości. Chcemy, żeby trajektoria uchybu dążyła do 0 - czyli do punktu zadanego - po linii prostej, ponieważ to oznacza możliwie najlepszą dynamikę, czyli dynamikę członu inercyjnego. 

Podstawowy układ ślizgowy działa w oparciu o funkcję signum. Stan załączeń zależy od aktualnego znaku funkcji przełączającej definiowanej dla danego obiektu. Stąd właśnie idea cecha sterowania ślizgowego, czyli przełączanie dwustanowe. Istnieją jednak również inne możliwości wykonania sterowania ślizgowego, niż funkcja signum. 

Zaprojektowanie układu ze sterowaniem ślizgowym polega zatem na **określeniu funkcji przełączeń** oraz **wybraniu funkcji przełączającej**. 

![Untitled](14%20Komputerowo%20wspomagane%20projektowanie%20uk%C5%82ado%CC%81w%20r%20bd05993e0b8e42069fffc4396cb3cf12/Untitled%2011.png)

Na przykładzie sterowania silnikiem prądu stałego, sterowanie ślizgowe polega na wymuszeniu zadanej prędkości obrotowej poprzez naprzemienne załączanie napięcia $+U_{dc}$ i $-U_{dc}$, przy czym napięcie twornika staje się napięciem uśrednionym, zależnie od czasu ząłączeń poszczególnych poziomów napięć.

**Zalety sterowania ślizgowego:**

- **Prostota sterowania**: dwustanowe przełączanie jest sterowaniem naturalnym dla każdego przekształtnika. Takie przełączanie sprowadza się do przełączania par tranzystorów naprzemiennie, ze stałą czasową $T_c$.
- Gdy funkcja przełączająca osiąga 0, układ znajduje się w stanie ustalonym. Następuje to po czasie $3T_c$, czyli po trzykrotności stałej czasowej regulatora. Jest to **sterowanie łatwe do “ustawienia”,** bo jego dynamika sprowadza się tylko do tego parametru (przy zdefiniowanej funkcji przełączającej).
- **Algorytm sterowania jest bardzo prosty**: nie trzeba dobierać nastaw, ustalamy **tylko czas do ustalenia wartości zadanej**. Nie ma tu również regulatorów liniowych, w strukturze sterowania ślizgowego pojawiają się tylko proste operacje arytmetyczne i algebraiczne
- **Redukcja rzędu układu**: silnik to układ 2 rzędu. Przez zaprojektowanie regulatora ślizgowego z założoną dynamiką 1 rzędu, otrzymujemy wypadkowo dynamikę 1 rzędu - układ staje się układem inercyjnym.
- Sterowanie ślizgowe jest **sterowaniem odpornym**. **Niewrażliwość na zakłócenia i zmiany parametrów**: w przypadku regulatorów PI, mamy do czynienia ze stałymi czasowymi, w oparciu o które nastraja się regulatory. Przy zmianie parametrów układów, stałe czasowe ulegają zmianie, co musi być kompensowane, żeby zachować pożądaną dynamikę układu. **W regulatorach ślizgowych nie ma nastaw** - są to regulatory sztywne - więc **dynamika nie zależy od parametrów obiektu sterowanego**.

**Wady sterowania ślizgowego:**

- Algorytm sterowania wymaga **różniczkowania sygnału wielkości sterowanej**, co powoduje wzmacnianie wszelkich szumów w układzie
- Sterowanie ślizgowe to **bezpośrednie sterowanie prędkością obrotową**. W najprostszym przypadku oznacza to, że **nie mamy kontroli nad prądem i momentem** silnika.
- **Chattering**: w związku z dwustanowym przełączaniem, w układzie występują **tętnienia prądu i momentu silnika**.
- **Brak członu całkującego** w układzie stwarza **ryzyko powstania uchybu ustalonego** odpowiedzi układu
- Przebieg trajektorii sterowania względem funkcji przełączającej powoduje, że w układach ze sterowaniem ślizgowym **częstotliwość przełączeń przekształtnika jest zmienna**.

**Źródła**

[1] Materiały i notatki z wykładu *Automatyka napędu elektrycznego - zagadnienia wybrane*