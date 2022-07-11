# 3. Pomiary wielkości nieelektrycznych

Status: Zrobione

### a) metody stykowe pomiaru temperatury - błędy metod

**Termopary**

Podstawową metodą stykowego badania temperatury jest wykorzystanie termopary. Termopary są oparte na zjawisku Seebecka, w którym różnica temperatur na materiale powoduje powstanie napięcia między punktami o różnych temperaturach. Zależność Seebecka jest liniowa. 

Błędy metod pomiarowych w termoparach wynikają z tego, że czułości termopar nie mają przebiegu liniowego - powstające napięcie nie jest wprost proporcjonalne do mierzonej temperatury. Dlatego pomiar termoparą jest możliwy tylko na pewnym zakresie temperatur, zależnie od typu termopary. Typy są unormowane.

W celu linearyzacji termopar, stosuje się współczynniki (poprawki) na przetwornikach.

**Rezystancyjne czujniki temperatury**

- **Czujniki metalowe**: wykorzystuje się tu zmiany rezystancji przy zmianach temperatury materiału. Podobnie jak w przypadku termopar, funkcja rezystywności nie jest wprost proporcjonalna do temperatury. Dlatego czujniki np. platynowe wykorzystuje się tylko dla określonego zakresu temperatur, zależnie od zastosowanego materiału. Platyna ma najszerszy zakres liniowy.
- **Termistory półprzewodnikowe PTC i NTC**: są to czujniki zbudowane z materiałów półprzewodnikowych, których rezystancja silnie zmienia się wraz ze zmianami temperatury. Wyróżnia się czujniki PTC i NTC, o dodatnim lub ujemnym współczynniku temperaturowym rezystancji. Ich błędy pomiarowe biorą się głównie z tego, że współczynniki temperaturowe rezystancji silnie zmieniają się wraz z temperaturą. Ich charakterystyki rezystancji w funkcji temperatury przedstawiane są w skalach logarytmicznych, co powoduje że wymagane są układy do linearyzacji.
- **Czujniki półprzewodnikowe:** mówi się tu o diodach i tranzystorach, jako scalonych czujnikach temperatury. Ich zaletami są duża czułość i liniowość charakterystyki, natomiast wadą jest mały zakres pomiarowy. Charakterystyki nie są idealnie liniowe, ale lepsze niż w pozostałych czujnikach.

**Ogólne źródła błędów przy stykowych pomiarach temperatury:**

Po pierwsze, przyłożenie termometru czy innego czujnika powoduje pobranie pewnej ilości ciepła z mierzonego punktu. Wprowadza to zakłócenie termiczne badanego obiektu. Jest to podstawowym źródłem błędu pomiarowego.

Powyższy błąd można zmniejszyć przez zastosowanie płytki pośredniczącej z pastą przewodzącą na obiekcie, do której można przyłączyć stykowy czujnik. 

Druga rzecz: w przypadku pomiaru temperatur cieczy i gazów, błąd pomiaru może być generowany dlatego, że element na którym zamocowany jest czujnik w rurze, może odprowadzać ciepło. Dlatego pomiar wykazuje niższą temperaturę, niż ma ciecz czy gaz przepływające przez rurę. 

Eliminacja powyższego błędu sprowadza się do zmniejszania wypromieniowywania ciepła z czujnika. Osiąga się to przez stosowanie przesłon ograniczających promieniowanie, polerowanie osłon czujnika (zmniejszenie współczynnika emisyjności powierzchni) oraz zwiększenie współczynnika wnikania ciepła - czyli zwiększenie prędkości przepływu gazu czy cieczy w rurze. 

### Najważniejsze punkty

- do pomiaru stykowego wykorzystuje się termopary (zjawisko Seebecka) lub czujniki rezystancyjne (oparte o zmiany rezystancji materiału przy zmianie temperatury)
- czujniki rezystancyjne to metale (np. platyna), termistory PTC i NTC (półprzewodniki) oraz czujniki półprzewodnikowe (oparte o diody i tranzystory)
- wszystkie czujniki i termopary mają nieliniowe charakterystyki i trzeba wprowadzać odpowiednie poprawki
- wszystkie metody pomiaru stykowego mogą pobierać pewną ilość ciepła z miejsca styku z próbką, co zmienia temperaturę w miejscu pomiaru
- powyższe dwa punkty to podstawowe błędy metod stykowych

### **Źródła:**

[1] Materiały z wykładu *Pomiary elektryczne wielkości nieelektrycznych*

### b) pomiary tensometryczne - pomiar momentu skręcającego na wale

**Typy tensometrów**

Wyróżnia się dwa podstawowe rodzaje tensometrów: tensometry oporowe oraz tensometry półprzewodnikowe.

**Tensometry oporowe** opierają się o najprostszy wzór na rezystancję, $R=\rho \frac{l}{S}$, oraz o fakt, że przy rozciąganiu metalowego elementu, zwęża się on. Spadek przekroju i wzrost długości powodują wzrost rezystancji materiału. Zmianę grubości materiału przy zmianie jego długości wiąże współczynnik Poissona. 

Względna zmiana rezystancji tensometru wiąże się ze zmianą jego długości tzw. **współczynnikiem czułości tensometru** (dla tensometrii oporowej: 2 - 4). Współczynnik ten zależy od wspołczynnika Poissona.

Tensometry oporowe stosuje się w zakresie rozciągania sprężystego. Zbyt mocne rozciągnięcie może je uszkodzić.

Pomiary w tensometrii oporowej wykonuje się na ogół w układach mostkowych. Ze względu na relatywnie niewielką czułość, duże naprężenia nie powodują dużej zmiany rezystancji tensometru.

**Tensometry półprzewodnikowe** opierają się o efekt piezorezystancyjny, zgodnie z którym rezystancja tensometru zmienia się wraz ze zwiększaniem naprężenia. Efekt ten jest związany z deformacją sieci krystalicznej materiału półprzewodnikowego. W praktyce, tensometry półprzewodnikowe dzięki innej naturze zjawisk zachodzących w nich, oferują dużo większą czułość na naprężenia, niż tensometry oporowe (współczynnik czułości tensometru przyjmuje wartości rzędu 40 - 400)

![Untitled](3%20Pomiary%20wielkos%CC%81ci%20nieelektrycznych%201908256a1a8042669ec2c20c7cad29e5/Untitled.png)

Ogólnie, tensometry najczęściej wykonuje się jako foliowe. Dawniej stosowano tensometry drutowe. Tensometry foliowe można budować w postaci membran, co służy np. do pomiaru ciśnienia.

**Zastosowania tensometrów**

Tensometry stosuje się wszędzie tam, gdzie potrzebna jest znajomość sił działających na obiekt. Dlatego są one stosowane w czujnikach siły, momentu, wagach kuchennych, przy ciśnieniomierzach, przepływomierzach czy nawet czujnikach przesunięcia. 

**Pomiar momentu skręcającego na wale**

Tensometry można wykorzystywać do czujników momentu skręcającego na wale. 

Można wyróżnić dwa rodzaje czujników momentu:

- **Czujniki momentu do pomiaru wałów statycznych (reakcyjne):** stosowane tam, gdzie wał się nie obraca, a jest poddawany tylko skręceniu. Tego typu czujniki nie muszą się obracać. Można je wykonać w postaci dwóch elementów - jednego przymocowanego nieruchomo, drugiego na wale silnika. Między tymi elementami (kołnierzami) umieszcza się tensometr. Ściskanie tensometru umożliwia pomiar siły, czyli de facto momentu, działającego na czujnik
- **Czujniki momentu do pomiaru na wałach ruchomych: a**by zmierzyć moment, tensometr montuje się na tzw. elemencie torsyjnym, którego skręcenie jest proporcjonalne do momentu przenoszonego z wału silnika na wał maszyny roboczej. Skręcenie mierzone jest właśnie tensometrem w układzie mostkowym. Jeżeli parametry materiału, z którego wykonany jest element torsyjny, są znane - można na podstawie wyniku pomiaru obliczyć moment elektromagnetyczny.
    
    W związku z tym, że czujniki tego typu muszą się obracać na wale, komunikacja i dostarczanie zasilania coraz częściej zapewniane są w sposób bezprzewodowy (komunikacja radiowa oraz zasilanie indukcyjne). 
    

### Najważniejsze punkty

- tensometry dzieli się na oporowe (zmiana rezystancji wskutek zmiany geometrii czujnika) oraz półprzewodnikowe (efekt piezorezystancyjny - nacisk powoduje powstanie napięcia)
- tensometry stosuje się tam, gdzie trzeba wykonać pomiar sił, naprężeń i ciśnień - np. wagi, czujniki siły i momentu, przepływomierze, etc.
- czujniki momentu statyczne: do wału silnika doczepiony element obracający się z nim, element ten naciska na nieruchomy element hamujący - duży nacisk to słaby moment (silnik jest cały czas zahamowany)
- czujniki momentu na wałach ruchomych: tensometr umieszcza się na elemencie torsyjnym, który skręca się przy oddziaływaniu na niego momentu silnika; skręcenie elementu torsyjnego odkształca tensometr i pozwala na pomiar działającego odkształcenia - stąd oblicza się moment

### **Źródła:**

[1] Materiały z wykładu *Pomiary elektryczne wielkości nieelektrycznych*

[2] [https://www.futek.com/torque-meter](https://www.futek.com/torque-meter)

[3] [https://tilkom.pl/catalog/czujnik-momentu-obrotowego/](https://tilkom.pl/catalog/czujnik-momentu-obrotowego/)

### c) pomiary natężenia przepływu

Wszelkie pomiary natężenia przepływu opierają się o dwa równania, opisujące prawa dla dynamiki gazów i płynów. Pierwsze z nich to tzw. równanie stanu gazu doskonałego:

$$
p=\frac{nRT}{V} \to \frac{pV}{T}=nR=const
$$

Drugie to równanie Bernoulliego: 

$$
p+\frac{1}{2}\rho v^2+\rho g h=const
$$

W których p - ciśnienie; n - liczba cząstek (masa); T - temperatura bezwzględna gazu; R - uniwersalna stała gazowa; h - wysokość (położenie), g - przyspieszenie ziemskie; $\rho$ - gęstość cieczy lub gazu.

Z pierwszego równania wynika, że dla stałej masy gazu, temperatura, objętość i ciśnienie dopasowują swoje proporcje do siebie. Z drugiego równania wynika natomiast, że suma ciśnienia, energii kinetycznej i energii potencjalnej cieczy są w przybliżeniu stałe. Oznacza to tyle, że jak prędkość cieczy rośnie na tej samej wysokości, to ciśnienie spada. Jak ciśnienie i wysokość rosną, to spada prędkość - i tak dalej. 

Pierwsze równanie pozwala na wyprowadzenie metod pomiaru przepływu gazu. Drugie równanie pozwala na wyprowadzenie metod pomiaru przepływu cieczy. 

**Typy pomiarów przepływu płynów:**

Zasadniczo, można wyróżnić cztery różne zasady działania przepływomierzy:

- **Pomiar różnicy ciśnienia**: przepływ oblicza się z różnicy mierzonych ciśnień. Do tego typu metod należą zwężki, kryzy, dysze, rotametry i rurki Pitota
- **Liczniki płynów**: są to np. liczniki bębnowe, z owalnymi wirnikami czy z mimośrodową komorą wirnikową.
- **Pomiar prędkości**: ****pomiar przepływu opiera się tu o wielkości stricte mechaniczne, gdzie prędkość przepływu jest przekształcana bezpośrednio na inną wielkość, np. przepływomierze turbinkowe, elektromagnetyczne, ultradźwiękowe
- **Pomiar przepływu masy**: pomiary zależne od tego, jaka masa płynu została przepuszczona przez przepływomierz, chodzi tu np. o przepływomierze Coriolisa czy kalorymetryczne.

**Metody pomiary przepływu płynów:**

- **Metoda zwężkowa:** w rurze wprowadza się przegrodę zwężającą. Jeżeli mamy stałą wysokość, to z równania Bernoulliego wynika, że suma energii kinetycznej i ciśnienia musi pozostawać stała. Przez zwężkę ciecz płynie z większą prędkością (bo płynie ta sama masa i objętość cieczy, ale przekrój przepływu się zmniejsza - przepływ rośnie). Ciśnienie za zwężką jest mniejsze, niż ciśnienie przed nią. Na podstawie znanych przekrojów rury i zwężki, a także gęstości płynu, można z różnicy ciśnień obliczyć przepływ cieczy.
    
    ![Untitled](3%20Pomiary%20wielkos%CC%81ci%20nieelektrycznych%201908256a1a8042669ec2c20c7cad29e5/Untitled%201.png)
    
- **Rurka spiętrzająca Pitota:** w tej metodzie, do rury z cieczą doprowadza się dwie rurki. Jedna jedynie styka się z rurą i mierzy ciśnienie statyczne cieczy - jakaś ilość cieczy jest w nią wciskana. Druga rurka jest doprowadzona w środek przepływu i płynąca ciecz jest w nią wciskana mocniej. Różnica między wskazaniem drugiej rurki i pierwszej rurki to ciśnienie dynamiczne przepływu.
    
    ![Untitled](3%20Pomiary%20wielkos%CC%81ci%20nieelektrycznych%201908256a1a8042669ec2c20c7cad29e5/Untitled%202.png)
    
- **Przepływomierz pływakowy (rotametr):** w tej konstrukcji, w rurociągu pionowym umieszczony jest pływak o gęstości większej niż gęstość cieczy. Pływak opada, zamykając rurociąg. Im większy jest przepływ, tym wyżej pływak unosi się nad wlotem rurociągu. Siła cieczy napierającej na pływak jest równoważona przez oddziaływanie grawitacyjne, więc pływak w pewnym punkcie się zatrzymuje. Wysokość pływaka wyznacza nam przepływ, przy czym jest to zależność nieliniowa.
    
    ![Untitled](3%20Pomiary%20wielkos%CC%81ci%20nieelektrycznych%201908256a1a8042669ec2c20c7cad29e5/Untitled%203.png)
    
- **Przepływomierz wirnikowy (turbinkowy):** w tym przypadku w rurze montuje się wiatraczek o określonym kącie nachylenia łopatek. Przepływająca ciecz (lub gaz) powoduje obrót wiatraczka. Prędkość obrotowa jest proporcjonalna do przepływu, więc jej pomiar pozwala na określenie przepływu w rurze.
    
    ![Untitled](3%20Pomiary%20wielkos%CC%81ci%20nieelektrycznych%201908256a1a8042669ec2c20c7cad29e5/Untitled%204.png)
    
- **Przepływomierz wirowy:** w rurze wprowadza się prostopadłą przegrodę, która powoduje miejscowe zawirowania w przepływającej cieczy. Wskutek wiru, w badanym medium następuje zakłócenie komunikacji np. falami ultradźwiękowymi. Pomiar zakłóceń jest proporcjonalny do szybkości przepływu.
    
    ![Untitled](3%20Pomiary%20wielkos%CC%81ci%20nieelektrycznych%201908256a1a8042669ec2c20c7cad29e5/Untitled%205.png)
    
- **Przepływomierz elektromagnetyczny:** przepływomierz tego typu stosuje się tam, gdzie ciecz ma właściwości przewodzące. Na rurze naprzeciw siebie umieszcza się wie elektrody, a prostopadle do nich umieszcza się cewki AC lub DC. Cewka zasilona napięciem powoduje wzbudzenie prądów wirowych w cieczy. Te indukują napięcie na elektrodach pomiarowych, wskutek względnego przemieszczenia ładunków względem elektrod. Im wyższy przepływ, tym wyższe indukowane napięcie.
    
    ![Untitled](3%20Pomiary%20wielkos%CC%81ci%20nieelektrycznych%201908256a1a8042669ec2c20c7cad29e5/Untitled%206.png)
    
- **Przepływomierz kalorymetryczny:** istnieje kilka konstrukcji przepływomierzy kalorymetrycznych. Ich działanie polega na tym, że w rurze umieszcza się element grzejny. Ciecz przepływając przez niego ogrzewa się. Przepływomierz mierzy temperatury przed grzejnikiem i za grzejnikiem. Im szybciej ciecz się porusza, tym cieplejsza dopływa do drugiego punktu pomiarowego. Czyli im większa różnica temperatur między termometrami, tym wyższy przepływ.
    
    ![Untitled](3%20Pomiary%20wielkos%CC%81ci%20nieelektrycznych%201908256a1a8042669ec2c20c7cad29e5/Untitled%207.png)
    
- **Przepływomierz Coriolisa (żyroskopowy):** opiera się o działanie siły Coriolisa oddziałującej na obracające się rurki, w których płynie ciecz. Przy stałej prędkości obrotowej, większy przepływ cieczy (większa prędkość cieczy) powoduje większe odchylenie się rurek od płaszczyzny obrotu.
- **Przepływomierz ultradźwiękowy:** w tej konstrukcji, ciecz przepuszczana jest przez rurkę, w której od nadajnika do odbiornika rozchodzą się fale akustyczne. Szybszy przepływ sprawia, że fale docierają do odbiornika szybciej, więc tempo rozchodzenia się ich jest proporcjonalne do przepływu.
    
    ![Untitled](3%20Pomiary%20wielkos%CC%81ci%20nieelektrycznych%201908256a1a8042669ec2c20c7cad29e5/Untitled%208.png)
    

### Najważniejsze punkty

- pomiary przepływu opierają się o znane zależności gazu doskonałego oraz równania Bernoulliego
- zasady działania przepływomierzy: pomiar różnicy ciśnienia, liczniki cieczy, pomiar prędkości cieczy, pomiar przepływu masy
- przykładowe przepływomierze: zwężkowy, z rurką Pitota, elektromagnetyczny, turbinkowy, pływakowy, ultradźwiękowy, Coriolisa, kalorymetryczny
- przepływomierz zwężkowy: w rurze wprowadza się zwężkę i mierzy ciśnienie za nią i przed nią; z różnicy ciśnień i parametrów cieczy oblicza się przepływ
- przepływomierz z rurką Pitota: do kanału z cieczą wkłada się rurkę - im większe ciśnienie dynamiczne, tym wyższy stan cieczy w tej rurce (więcej cieczy jest w nią wpychane)
- kalorymetryczny: w jednym punkcie podgrzewa się gaz lub ciecz, w drugim mierzy temperaturę; duża różnica temperatur oznacza, że ciecz płynie powoli i ma czas stygnąć

### **Źródła:**

[1] Materiały z wykładu *Pomiary elektryczne wielkości nieelektrycznych*

[2] [https://www.princeton.edu/~asmits/Bicycle_web/Bernoulli.html](https://www.princeton.edu/~asmits/Bicycle_web/Bernoulli.html)

### d) pomiary ciśnienia

**Podstawowe wielkości**

W przypadku ciśnienia, zawsze mówimy o sile oddziałującej na pewną powierzchnię, wyrażonej w paskalach, czyli N/m^2. Jednak można tu wyróżnić trzy różne typy pomiarów:

- **Ciśnienie absolutne**, czyli ciśnienie mierzone w odniesieniu do próżni absolutnej. Pomiar ciśnienia atmosferycznego przy powierzchni ziemi jest pomiarem ciśnienia absolutnego.
- **Ciśnienie różnicowe**, czyli różnicę ciśnień między dwoma punktami poboru ciśnienia.
- **Ciśnienie względne**, czyli nadciśnienie lub podciśnienie mierzone w odniesieniu do ciśnienia atmosferycznego.

![Untitled](3%20Pomiary%20wielkos%CC%81ci%20nieelektrycznych%201908256a1a8042669ec2c20c7cad29e5/Untitled%209.png)

**Urządzenia do pomiaru ciśnienia**

Wśród urządzeń do pomiaru ciśnienia można wyróżnić zarówno urządzenia analogowe, jak i elektroniczne. Wśród analogowych można znaleźć manometry i barometry różnej konstrukcji. Wśród urządzeń elektronicznych, wyróżnia się przetworniki rezystancyjne czy pojemnościowe. Mówiąc dokładniej:

- **Manometr z rurką Bourdona:** proste urządzenie do pomiaru ciśnienia. Ma w konstrukcji rurkę podłączoną do mierzonego procesu. Wzrost ciśnienia w rurce powoduje jej odkształcenie się, natomiast odkształcenie rurki powoduje ruch wskazówki. Odkształcenie to na ogół po prostu rozszerzenie rurki i nacisk na wskazówkę.
    
    ![Untitled](3%20Pomiary%20wielkos%CC%81ci%20nieelektrycznych%201908256a1a8042669ec2c20c7cad29e5/Untitled%2010.png)
    
- **Manometr z puszką membranową:** w tym urządzeniu nie ma rurki, jest za to membrana. Większe ciśnienie oznacza większy nacisk na membranę. Membrana się rozszerza. Membrana jest sprzężona ze wskazówką manometru, więc jej rozszerzenie powoduje ruch wskazówki.
    
    ![Untitled](3%20Pomiary%20wielkos%CC%81ci%20nieelektrycznych%201908256a1a8042669ec2c20c7cad29e5/Untitled%2011.png)
    
- **Tensometryczne pomiary ciśnienia:** w specjalnych typach mierników ciśnienia, można zastosować tensometry w układzie mostkowym, zamontowane na tej samej belce. Na belkę działają ciśnienie procesu i ciśnienie odniesienia. Różnica ciśnień powoduje odkształcenie belki w jedną ze stron - zależnie od tego, które jest większe. Odkształcenie belki zmienia rezystancje tensometrów - jeden się ściska, drugi rozszerza. Zmiany rezystancji można zmierzyć i w ten sposób uzyskać różnicę między ciśnieniem mierzonym a ciśnieniem odniesienia.
    
    ![Untitled](3%20Pomiary%20wielkos%CC%81ci%20nieelektrycznych%201908256a1a8042669ec2c20c7cad29e5/Untitled%2012.png)
    
- **Pojemnościowe przetworniki ciśnienia:** ciśnienie odniesienia i ciśnienie procesu oddziałują na membranę między okładkami kondensatora. Stąd, membrana stanowi kondensator zarówno z górną jak i z dolną okładką. Przesunięcie okładki w jedną ze stron powoduje zmiany pojemności kondensatorów. Zmiany pojemności przelicza się na ciśnienie. Układ zasila się napięciem przemiennym.
    
    ![Untitled](3%20Pomiary%20wielkos%CC%81ci%20nieelektrycznych%201908256a1a8042669ec2c20c7cad29e5/Untitled%2013.png)
    
- **Rezystancyjne przetworniki ciśnienia:** ciśnienie procesu powoduje przesuwanie się regulatora rezystora w układzie mostka Wheatstone’a. Zmiana ta powoduje zmianę rezystancji mierzonej w układzie. To również można przeliczyć na ciśnienie.
    
    ![Untitled](3%20Pomiary%20wielkos%CC%81ci%20nieelektrycznych%201908256a1a8042669ec2c20c7cad29e5/Untitled%2014.png)
    
- **Przetworniki ciśnienia z transformatorem różnicowym:** w tym przypadku ciśnienie powoduje przesuwanie rdzenia w transformatorze różnicowym z dwoma uzwojeniami wtórnymi. Zależnie od kierunku przesunięcia rdzenia, na jednym z uzwojeń powstaje napięcie wyższe, na drugim - niższe. Różnice napięć można przeliczać na ciśnienie.
    
    ![Untitled](3%20Pomiary%20wielkos%CC%81ci%20nieelektrycznych%201908256a1a8042669ec2c20c7cad29e5/Untitled%2015.png)
    
- **Barometry cieczowe:** w tego typu urządzeniach ciecz wprowadzona jest do u-rurki, na której dwóch końcach działają różne ciśnienia. Mogą to być ciśnienie odniesienia i ciśnienie procesu, mogą być ciśnienie atmosferyczne lub próżnia. W podstawowym układzie, przemieszczenie cieczy powoduje zmianę wskazania ciśnienia, bo następuje wskutek różnicy ciśnień. Z jednej strony u-rurki ciecz się podnosi, z drugiej opada. W bardziej zaawansowanej konstrukcji, ruch cieczy może powodować przesuwanie się położenia rdzenia transformatora różnicowego.
    
    ![Untitled](3%20Pomiary%20wielkos%CC%81ci%20nieelektrycznych%201908256a1a8042669ec2c20c7cad29e5/Untitled%2016.png)
    

### Najważniejsze punkty

- **manometr z rurką Bourdona**: większe ciśnienie odkształca rurkę, odkształcona rurka przesuwa wskazówkę
- **manometr z puszką membranową**: nacisk na membranę ją odkształca, odkształcona membrana porusza wskazówką
- **pomiar tensometryczny**: na membranie jest tensometr, ciśnienie odkształca membranę i jednocześnie tensometr - efekt piezoelektryczny podaje sygnał proporcjonalny do ciśnienia
- **czujnik pojemnościowy**: na okładkę kondensatora działa ciśnienie, im większe tym okładki bliżej, im okładki bliżej tym pojemność układu mniejsza, pomiar pojemności pozwala na pomiar ciśnienia
- **czujnik rezystancyjny**: ciśnienie działa na element zmieniający rezystancję regulowanego rezystora, zmiana rezystancji zmienia sygnał pomiarowy
- **układ z transformatorem różnicowym**: działanie ciśnienia przesuwa rdzeń transformatora różnicowego, na dwóch uzwojeniach przez to pojawiają się różne napięcia
- **barometr cieczowy**: w u-rurce jest ciecz; na ciecz działa ciśnienie - im większe, tym wyżej jest ona na drugim końcu rurki

### **Źródła**

[1] Materiały z wykładu *Pomiary elektryczne wielkości nieelektrycznych*

[2] Instrukcja do laboratorium *Pomiary elektryczne wielkości nieelektrycznych: Badanie czujników i przetworników ciśnienia*

### e) pomiar wilgotności

Pomiary wilgotności to de facto pomiary ciśnienia cząstkowego pary wodnej zawartej w powietrzu, czyli - mówiąc prościej - pomiar tego, jak dużo pary wodnej znajduje się w powietrzu. 

**Podstawowe wielkości**

W przypadku wilgotności, można wyróżnić dwie podstawowe wielkości:

- wilgotność bezwzględną, czyli dosłownie masę wody w jednostce objętości powietrza, co wyraża się na ogół w [g/m^3]
- wilgotność względną, wyrażoną w [%], która mówi, ile wody jest w powietrzu w odniesieniu do maksymalnej ilości wody, która może być w powietrzu o tej temperaturze. Im wyższa temperatura, tym więcej wody może *pomieścić* powietrze, tj. ciśnienie pary nasyconej rośnie.

**Fizyczne podstawy pomiarów wilgotności**

Wśród metod pomiaru wilgotności powietrza można wymienić:

- pomiar masy pary pochłoniętej przez absorbent (higrometry grawimetryczne)
- analizę zmiany parametrów powietrza (tłumienie określonych częstotliwości promieniowania podczerwonego, zmiana prędkości rozchodzenia się fal elektromagnetycznych)
- badanie zmian parametrów materiałów (np. wydłużanie się wilgotnych włosów czy nici nylonowych)
- pomiary charakterystycznych temperatur (np. temperatura punktu rosy)

**Urządzenia do pomiaru wilgotności**

Wśród urządzeń do pomiaru wilgotności można wymienić:

- **Psychrometr Augusta:** urządzenie składające się z dwóch termometrów, z czego jeden jest w zwilżanej koszulce. Woda ze zwilżonego termometru odparowuje, pobierając ciepło (tzw. ciepło utajone), więc wskazanie tego termometru spada. W przypadku 100% wilgotności powietrza, woda nie odparowuje, natomiast przy 0% - odparowuje bardzo szybko. Oznacza to tyle, że im większa różnica temperatur na termometrach, tym mniejsza wilgotność względna powietrza. W celu eliminacji wpływu ruchu powietrza na wynik pomiaru, stosuje się też **psychrometr Assmanna,** w którym przepływ powietrza jest po prostu wymuszany na zadanym poziomie.
    
    ![Untitled](3%20Pomiary%20wielkos%CC%81ci%20nieelektrycznych%201908256a1a8042669ec2c20c7cad29e5/Untitled%2017.png)
    
- **Higrometry punktu rosy**: urządzenia, w których miejscowo ochładza się powietrze i sprawdza, przy jakiej temperaturze para wodna skrapla się np. na lusterku. Temperatura ta jest temperaturą punktu rosy i pozwala na odczyt z krzywych psychrometrycznych wilgotności względnej powietrza w aktualnej temperaturze.
    
    ![Untitled](3%20Pomiary%20wielkos%CC%81ci%20nieelektrycznych%201908256a1a8042669ec2c20c7cad29e5/Untitled%2018.png)
    
- **Higrometr włosowy**: urządzenie to opiera pomiar o zmianę geometrycznych wymiarów materiałów. Badaną wielkością jest długość włosa, aktualnie nylonowego. Większa wilgotność powoduje wydłużenie włosa, a odczyt tej długości pozwala na zbadanie zmiany wilgotności
    
    ![Untitled](3%20Pomiary%20wielkos%CC%81ci%20nieelektrycznych%201908256a1a8042669ec2c20c7cad29e5/Untitled%2019.png)
    
- **Higrometr absorpcyjny:** urządzenie działa na podobnej zasadzie, co higrometr włosowy. Większa wilgoć powoduje większe odkształcenie membrany, która naciska na tensometry. Odkształcenie jej zmniejsza nacisk na tensometry, co powoduje zmianę sygnału pomiarowego.
    
    ![Untitled](3%20Pomiary%20wielkos%CC%81ci%20nieelektrycznych%201908256a1a8042669ec2c20c7cad29e5/Untitled%2020.png)
    
- **Higrometr z czujnikami impedancyjnymi:** zasada działania tego higrometru opiera się o pomiar parametrów elektrycznych materiałów. Wraz ze zmianą wilgotności, zmieniają się rezystancja czy pojemność materiałów elektrycznych. Zmiana tych wielkości powoduje zmianę sygnału pomiarowego, co pozwala na odczyt wilgotności.
    
    ![Untitled](3%20Pomiary%20wielkos%CC%81ci%20nieelektrycznych%201908256a1a8042669ec2c20c7cad29e5/Untitled%2021.png)
    

### Najważniejsze punkty

- mierzy się wilgotność względną lub bezwzględną
- urządzenia pomiarowe: psychrometr Augusta, higrometr włosowy, higrometr punktu rosy, higrometr absorpcyjny, higrometr z czujnikiem impedancyjnym
- psychrometr Augusta: dwa termometry, jeden zwilżony - jeżeli wilgotność jest mała, ze zwilżonego odparowuje woda i pobierze ciepło utajone; termometr pokaże niższą temperaturą - im wyższa różnica temperatur, tym niższa wilgotność
- higrometr punktu rosy: schładza się powierzchnię lusterka w którym odbite jest światło; przy temperaturze punktu rosy, para wodna skrapla się na lusterku i odbicie światła jest osłabione - to jest punkt rosy

### **Źródła:**

[1] Materiały z wykładu *Pomiary elektryczne wielkości nieelektrycznych*

[2] Instrukcja do laboratorium *Pomiary elektryczne wielkości nieelektrycznych: Pomiary wilgotności*