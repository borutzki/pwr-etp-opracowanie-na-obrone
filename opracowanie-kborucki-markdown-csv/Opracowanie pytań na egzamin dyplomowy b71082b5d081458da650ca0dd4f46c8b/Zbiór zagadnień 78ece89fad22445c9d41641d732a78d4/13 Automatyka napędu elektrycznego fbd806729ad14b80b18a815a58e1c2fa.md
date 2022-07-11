# 13. Automatyka napędu elektrycznego

Status: Zrobione

### a) rodzaje regulatorów w układach napędowych na przykładzie napędu prądu stałego, zjawisko windup w regulatorach PI/PID

W układach napędowych można wyróżnić regulatory:

- liniowe P, PI, PID, etc.
- stanu
- ślizgowe
- predykcyjne
- rozmyte
- neuronowe

**Regulatory liniowe PID** opierają się na przetwarzaniu sygnału wejściowego w sposób liniowy, wykonując na nim podstawowe operacje różniczkowe: całkowanie, różniczkowanie, wzmacnianie. Tego typu regulatory mogą składać się ze wszystkich trzech członów lub tylko z wybranych.

![Untitled](13%20Automatyka%20nape%CC%A8du%20elektrycznego%20fbd806729ad14b80b18a815a58e1c2fa/Untitled.png)

**Regulatory stanu** opierają się o sterowanie silnikiem w oparciu o znane lub estymowane zmienne stanu. Struktura regulatora stanu pozwala na jednoczesną kontrolę dużej liczby sygnałów - regulator składa się z zestawu wzmocnień w pętlach sprzężeń zwrotnych zmiennych sterowanych. Sygnały sprzężeń zwrotnych są sumowane i wszystkie naraz tworzą uchyb sygnału sterującego. 

![Untitled](13%20Automatyka%20nape%CC%A8du%20elektrycznego%20fbd806729ad14b80b18a815a58e1c2fa/Untitled%201.png)

**Regulatory ślizgowe** są regulatorami dwustanowymi, których sposobem przełączania np. napięcia steruje funkcja sterowania. W układach tego typu występuje regulacja oparta o naprzemienne załączanie dwóch stanów wartości sterowanej, np. napięcia, zależnie od trajektorii **funkcji przełączeń** na płaszczyźnie fazowej.

![Untitled](13%20Automatyka%20nape%CC%A8du%20elektrycznego%20fbd806729ad14b80b18a815a58e1c2fa/Untitled%202.png)

**Regulatory predykcyjne** wykorzystują przewidywane przyszłe stany obiektu sterowanego, obliczone na podstawie modelu matematycznego. Definiuje się **funkcję celu** jako **wskaźnik jakości sterowania** oparty o model matematyczny. Operując na obliczeniach możliwych przyszłych stanów obiektu wybiera się takie sterowanie, by zapewnić minimalizację wybranego wskaźnika jakości sterowania. 

W **regulatorach rozmytych** stosowana jest **logika rozmyta**, oparta o przesłanki i konkluzje. Regulatory rozmyte często są regulatorami nieliniowymi. Definiuje się w nich pewne reguły, w oparciu o które na podstawie sygnałów wejść dobierane są sygnały wyjść. Bazuje się tu na przedziałach wielkości i to na ich podstawie wykonywana jest cała logika.

![Untitled](13%20Automatyka%20nape%CC%A8du%20elektrycznego%20fbd806729ad14b80b18a815a58e1c2fa/Untitled%203.png)

![Untitled](13%20Automatyka%20nape%CC%A8du%20elektrycznego%20fbd806729ad14b80b18a815a58e1c2fa/Untitled%204.png)

**Regulatory neuronowe** natomiast są oparte o sieci neuronowe, których na studiach nie było. Wyższa informatyka.

**Zjawisko windup**

W typowych układach regulacji napędów, stosuje się ograniczenia wartości wyjściowej sygnału regulatora - wynika to z ograniczeń silników, np. przeciążalności prądowej. Ograniczenie można zrealizować np. przez wprowadzenie nasycenia sygnału wyjściowego.

W stanach dynamicznych, np. przy rozruchu, regulator PI początkowo działa w obszarze nasycenia. Im bliżej zadanej wartości, np. odpowiedniej prędkości obrotowej, tym sygnał regulatora jest niższy i regulator zaczyna wychodzić ze stanu nasycenia. 

Regulator PI ma tę wadę, że człon całkujący, po wyjściu przez regulator ze stanu nasycenia, nadal generuje duży sygnał wyjściowy. Dzieje się tak, ponieważ przez cały czas sumował on sygnał uchybu. Takie zjawisko nazywa się zjawiskiem windup.

Aby zapobiec zjawisku windup, stosuje się kilka strategii, których ideą główną jest ograniczenie maksymalnego sygnału członu całkującego. Sprowadzają się one do mniejszych lub większych modyfikacji struktury regulatora PI. Modyfikacje te nazywa się układami anti-windup

Przykładowymi realizacjami układu anti-windup są:

- ustawienie takiego samego ograniczenia dla członu całkującego i sygnału wyjściowego całego regulatora
- zastosowanie dodatkowego sprzężenia zwrotnego od różnicy sygnałów sprzed i zza ograniczenia regulatora; otrzymany w ten sposób uchyb osłabia sygnał członu całkującego
- Zastosowanie regulatora przyrostowego PI z ograniczeniem całki na wyjściu. Budowa tego regulatora wynika z prostych przekształceń różniczkowych przesuwających całkę na koniec układu
- zastosowanie regulatora przyrostowego IP z ograniczeniem całki na wyjściu. Zasadniczą cechą tego układu jest przesunięcie członu proporcjonalnego do pętli sprzężenia zwrotnego, co eliminuje konieczność stosowania filtru wejściowego.

**Źródła:**

[1] Materiały i notatki z wykładu *Automatyka napędu elektrycznego - zagadnienia wybrane*

[2] Materiały i notatki z wykładu *Komputerowo sterowane modelowanie i projektowanie układów regulacji*

### b) podobieństwo metod sterowania wektorowego dla układu z falownikiem napięcia i silnikiem indukcyjnym oraz dla przekształtnika sieciowego AC/DC

W układach z **silnikiem indukcyjnym i falownikiem** napięcia sterowanych wektorowo, korzystamy z **transformaty Clarke** w celu przekształcenia układu trzech prądów fazowych do jednego zapisu wektorowego, a następnie z **transformaty Parka**, żeby **zmienić układ współrzędnych ze stacjonarnego na wirujący**.

Podobnie, w metodach sterowania **przekształtnikami sieciowymi AC/DC** stosuje się te same transformaty, żeby **trójfazową sieć elektroenergetyczną** z punktu widzenia przekształtnika zamienić na pojedynczy wektor **wirujący**. 

Kolejne podobieństwo polega na tym, że sterowanie odbywa się poprzez **regulację składowych wirującego wektora prądu**. W przypadku silników indukcyjnych, składowe prądu odpowiadają za strumień elektromagnetyczny oraz moment elektromagnetyczny silnika. Gdy mowa o przekształtnikach, to zależnie od metody sterowania, poszczególne składowe wirującego wektora odpowiadają za wartość napięcia oraz pobieraną przez przekształtnik moc bierną. 

Zarówno w przypadku wektorowych metod sterowania przekształtnikiem, jak i silnikiem, **jedną ze składowych staramy się minimalizować i stabilizować, natomiast zasadnicze sterowanie polega na kontrolowaniu drugiej z nich**.

Idąc dalej, można wykazać **podobieństwa metod zorientowanych napięciowo dla przekształtnika AC/DC do metod zorientowanych polowo dla silnika** AC. Za poszczególne wartości odpowiadają poszczególne składowe.

Natomiast **metody DPC dla przekształtników AC/DC są analogiczne do metod DTC dla silników** prądu przemiennego. W obu przypadkach operuje się poprzez odpowiednie kluczowanie tak, by osiągnąć bezpośrednią kontrolę nad wielkością sterowaną. Dla silników jest to moment elektromagnetyczny; dla przekształtników - moce czynna i bierna. 

**Źródła:**

[1] Materiały i notatki z wykładu *Automatyka napędu elektrycznego - zagadnienia wybrane*

### c) metody odtwarzania zmiennych stanu i parametrów dla silników prądu przemiennego

W silnikach prądu przemiennego, w celu odtwarzania trudno mierzalnych zmiennych stanu i parametrów, stosuje się kilka różnorodnych podejść do estymacji. Wyróżnia się tu metody fizykalne, algorytmiczne oraz neuronowe.

### **Metody fizykalne**

Metody fizykalne bazują na **asymetrii magnetycznej maszyny** i na podstawie pomiaru pewnych wartości i znajomości pewnych zjawisk fizycznych pozwalają na określenie innych wartości fizycznych. Metody te wymagają rzeczywistych układów pomiarowych - dawniej do pomiaru strumienia poosiowego, współcześnie - do pomiaru prądów silnika. 

Fizykalne metody estymacji opierają się o **analizę spektralną harmonicznych prądu lub strumienia**. Przy estymacji wielkości, zakłada się w nich stacjonarność sygnału, wskutek czego **stany dynamiczne wprowadzają pewien błąd estymacji**.

Zaletą metod fizykalnych jest **dokładne obliczanie wielkości estymowanych** oraz **niezależność od parametrów silnika**. Wadą tych metod jest to, że nie radzą sobie ze stanami dynamicznymi układów napędowych, a oprócz tego tracą dokładność przy niewielkich prędkościach obrotowych silnika. 

### **Metody algorytmiczne**

Metody algorytmiczne opierają się o model matematyczny silnika indukcyjnego (lub innego, zależnie od układu napędowego). Wśród nich można wyróżnić symulatory zmiennych stanu, obserwatory zmiennych stanu oraz filtry Kalmana. 

**Symulatory zmiennych stanu** w oparciu o część modelu matematycznego silnika i pewne mierzone wielkości pozwalają na obliczenie innych potrzebnych wielkości, np. na podstawie równań obwodu wirnika i pomiaru prądu można określić strumień wirnika. W układach tych nie uwzględnia się zmian parametrów silnika, więc każda taka zmiana wprowadza błąd estymacji. Oprócz tego, sama niedokładność określenia parametrów silnika uwzględnionych w symulatorze wprowadza błąd estymacji. 

![Untitled](13%20Automatyka%20nape%CC%A8du%20elektrycznego%20fbd806729ad14b80b18a815a58e1c2fa/Untitled%205.png)

**Obserwatory zmiennych stanu** działają podobnie do symulatorów zmiennych stanu, ale z uwzględnieniem sprzężenia zwrotnego od rzeczywistych wartości silnika - np. estymowaną na podstawie zastosowanego modelu wartość prądu porównuje się z jego rzeczywistą, mierzoną wartością. Dzięki wykorzystaniu informacji o błędzie estymacji, uzyskuje się mniejszą wrażliwość estymatora na niedokładność określenia lub zmienność parametrów silnika. Istnieje kilka typów obserwatorów zmiennych stanu, różniących się stopniem złożoności - obserwatory nieliniowe, liniowe niestacjonarne, rozszerzone i tzw. “sliding-mode”. 

![Untitled](13%20Automatyka%20nape%CC%A8du%20elektrycznego%20fbd806729ad14b80b18a815a58e1c2fa/Untitled%206.png)

**Filtry Kalmana** nazywa się optymalnymi estymatorami. W estymacji zmiennych stanu silnika uwzględniają fakt, że sygnały są zakłócone - zarówno sygnały pomiarowe, jak i parametry obiektów. Filtry Kalmana działają w oparciu o algorytmy rekurencyjne, nie analityczne. W przypadku zakłóceń sygnałów pomiarowych o rozkładzie gaussowskim, można mówić o optymalnej estymacji - filtr Kalmana minimalizuje błąd średniokwadratowy estymowanych zmiennych stanu. Wadą filtrów Kalmana jest duża złożoność obliczeniowa - mikroprocesor musi wykonywać dużą liczbę operacji macierzowych w krótkim czasie.

![Untitled](13%20Automatyka%20nape%CC%A8du%20elektrycznego%20fbd806729ad14b80b18a815a58e1c2fa/Untitled%207.png)

![Untitled](13%20Automatyka%20nape%CC%A8du%20elektrycznego%20fbd806729ad14b80b18a815a58e1c2fa/Untitled%208.png)

### **Metody neuronowe**

Metody neuronowe estymacji zmiennych stanu opierają się o sieci neuronowe. Rozróżnia się metody neuronowe off-line oraz on-line, zależnie od sposobu trenowania sieci neuronowych.

**Metoda off-line (bazująca na neuronowej identyfikacji)**, w której trenuje się sieć neuronową przed umieszczeniem estymatora w rzeczywistym obiekcie. Estymator przygotowany w ten sposób powinien odzwierciedlać prędkość na podstawie mierzalnych wejść. Lepsze parametry estymacji można osiągnąć stosując także wejścia od próbek spóźnionych, np. dwóch do tyłu - czyli de facto “wartości historycznych”.

**Metoda on-line (bazująca na neuronowym modelowaniu)** jest uczona na bieżąco, podczas stosowania na obiekcie sterowanym, gdzie algorytm uczący wykorzystuje jako sprzężenie zwrotne wartość błędu między wielkością estymowaną i mierzoną określonego sygnału. Jest to metoda działająca w oparciu o ideę podobną do estymatorów typu MRAS.

**Źródła:**

[1] Materiały i notatki z wykładu *Automatyka napędu elektrycznego - zagadnienia wybrane*

### d) podstawowe struktury sterowania napędem z połączeniem sprężystym

W układach napędowych z połączeniem sprężystym można wykorzystać kilka różnych struktur sterowania. Można tu wymienić struktury kaskadowe z dodatkowymi sprzężeniami zwrotnymi, regulatory stanu oraz regulatory rozmyte, ślizgowe czy adaptacyjne.

W **strukturze kaskadowej**, stosuje się **dodatkowe sprzężenia zwrotne** od pewnych zmiennych stanu. Wyróżnia się trzy grupy dodatkowych sprzężeń zwrotnych i zastosowanie każdej z nich pozwalają na osiągnięcie różnych parametrów sterowania. Można zastosować **dwa dodatkowe sprzężenia zwrotne**, co pozwala na **pełne sterowanie dynamiką układu** - zarówno rozłożeniem biegunów, jak i współczynnikiem tłumienia.

![Untitled](13%20Automatyka%20nape%CC%A8du%20elektrycznego%20fbd806729ad14b80b18a815a58e1c2fa/Untitled%209.png)

![Untitled](13%20Automatyka%20nape%CC%A8du%20elektrycznego%20fbd806729ad14b80b18a815a58e1c2fa/Untitled%2010.png)

![Untitled](13%20Automatyka%20nape%CC%A8du%20elektrycznego%20fbd806729ad14b80b18a815a58e1c2fa/Untitled%2011.png)

Do sterowania układami dwumasowymi można wykorzystywać również **regulatory stanu**, które uwzględniają zmienne stanu połączenia sprężystego, takie jak moment skrętny i prędkość obrotowa po stronie maszyny roboczej. Należy jednak mieć na uwadze, że **stosowanie regulatorów stanu wymaga wykorzystania estymatora tych zmiennych** - np. obserwatora Luenbergera. 

![Untitled](13%20Automatyka%20nape%CC%A8du%20elektrycznego%20fbd806729ad14b80b18a815a58e1c2fa/Untitled%2012.png)

![Untitled](13%20Automatyka%20nape%CC%A8du%20elektrycznego%20fbd806729ad14b80b18a815a58e1c2fa/Untitled%2013.png)

Układy dwumasowe można sterować również korzystając z rozmytych i ślizgowych układów regulacji automatycznej, a także przy wykorzystaniu różnego rodzaju układów adaptacyjnych. Każda z tych metod ma pewne unikalne właściwości - np. sterowanie adaptacyjne typu MRAS pozwala na uodpornienie układu na zmiany parametrów napędu.

**Źródła:**

[1] Materiały i notatki z wykładu *Automatyka napędu elektrycznego - zagadnienia wybrane*

[2] Materiały i notatki z wykładu *Komputerowo wspomagane projektowanie układów regulacji*