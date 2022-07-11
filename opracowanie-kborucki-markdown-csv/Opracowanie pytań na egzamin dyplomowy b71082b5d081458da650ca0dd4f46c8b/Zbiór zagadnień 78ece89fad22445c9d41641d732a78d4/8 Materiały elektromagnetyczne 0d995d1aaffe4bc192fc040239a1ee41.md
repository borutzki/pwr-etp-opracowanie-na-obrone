# 8. Materiały elektromagnetyczne

Status: Zrobione

### a) parametry materiałowe opisujące oddziaływanie materii z polem elektrycznym i magnetycznym

**Przenikalność elektryczna i magnetyczna**

Podstawowe dwa parametry, charakteryzujące materiały pod względem użyteczności w procesach z silnymi polami, to przenikalność elektryczna $\varepsilon$ oraz przenikalność magnetyczna $\mu$. Obydwie te wielkości mówią, jak dużo energii z pól elektromagnetycznych są w stanie zgromadzić w sobie materiały. 

Wynika to z zależności:

$$
W_{VH}=\frac{1}{2}BH
$$

$$
W_{VE}=\frac{1}{2}DE
$$

Przy czym wielkości w obydwu równaniach wiążą się ze sobą poprzez przenikalność odpowiednio magnetyczną i elektryczną, co opisują poniższe zależności:

$$
D=\varepsilon \varepsilon_0E
$$

$$
B=\mu \mu_0H
$$

**Parametry elektryczne**

Istnieje kilka parametrów materiałów, które opisują ich oddziaływanie z polem elektrycznym. Na początek można wyróżnić **rezystywność** i jej odwrotność, **konduktywność** - które dla danego materiału opisują, jak duża ilość nośników ładunku jest w stanie przepływać przez materiał, po przyłożeniu do niego pola elektrycznego. 

Jedną z istotnych wielkości opisujących parametry materiału w obecności pola elektrycznego jest **wytrzymałość elektryczna**. Jest to maksymalna wartość natężenia pola elektrycznego, przy której nie dochodzi do wyładowań w materiale. Wytrzymałość elektryczna wraz z przenikalnością elektryczną mówią, jak dużo energii jest w stanie zgromadzić materiał.

Najważniejszym parametrem materiałowym, który opisuje oddziaływanie pola elektrycznego na materię, jest jednak **przenikalność elektryczna,** która opisuje zdolność dielektryków do gromadzenia energii w polu elektrycznym. Przenikalność elektryczną określa się jako stosunek pojemności kondensatora wypełnianego wybranym dielektrykiem do pojemności tego samego kondensatora *wypełnionego* próżnią. **Przenikalność zależy od stanu skupienia dielektryka, rodzajów polaryzacji, temperatury i częstotliwości**.

W przypadku materiałów przewodzących, czyli metali, istnieje multum wolnych nośników ładunku, które przemieszczają się w zależności od działającego pola. W dielektrykach sprawa ma się inaczej. Wszystkie ładunki są złączone z określonymi atomami co sprawia, że mogą się poruszać jedynie na małe odległości, w obrębie atomu lub cząsteczki. Stąd biorą się różne zjawiska polaryzacji. 

Na **polaryzację** składa się kilka różnych mechanizmów. Pole elektryczne, oddziałując na ładunki związane w atomach i cząstkach powoduje ich przesuwanie. W najmniejszej skali, czyli atomowej, pojawia się **polaryzacja elektronowa**, czyli przesuwanie ładunków dodatnich i ujemnych w atomie. Kolejna jest **polaryzacja jonowa,** która polega na przesuwaniu ujemnych i dodatnich ładunków w polu elektrycznym w obrębie cząstki, co powoduje powstawanie dipoli. Poza tym, działa również **polaryzacja dipolowa,** czyli obracanie się w polu elektrycznym cząstek, które na stałe są dipolami. Ostatnia jest **polaryzacja makroskopowa,** czyli przemieszczanie się wolnych nośników ładunku w dielektryku zgodnie z kierunkiem działania sił pola.

Dodatkowo, można wyróżnić **podatność elektryczną.** Jest to niemianowana wielkość, która opisuje, jak materiał jest w stanie gromadzić energię poprzez polaryzację. Jest to wielkość bezpośrednio związana z przenikalnością elektryczną materiału ($\varepsilon=1+\chi$).

**Parametry magnetyczne**

Materiały magnetyczne klasyfikuje się na podstawie **podatności magnetycznej**, czyli proporcji magnetyzacji (momentu magnetycznego przypadającego na jednostkę objętości materiału) do przyłożonego pola zewnętrznego. Materiały podatności niższej od zera klasyfikowane są jako diamagnetyki. Materiały, których podatność jest w zakresie od 0 do 1 są nazywane paramagnetykami, natomiast materiały o większej podatności magnetycznej nazywa się ferromagnetykami.

Podatność paramagnetyków i ferromagnetyków zależy od temperatury. Właściwości magnetyczne wraz z temperaturą są osłabiane, a przy temperaturze zwanej **temperaturą Curie**, ferromagnetyki stają się paramagnetykami. Paramagnetyki natomiast wykazują coraz mniejszą podatność magnetyczną wraz ze wzrostem temperatury.

W przypadku pól magnetycznych, podstawowym parametrem opisującym materiał jest **przenikalność magnetyczna**. Opisuje ona, ile energii pola magnetycznego jest w stanie zgromadzić materiał. W przypadku materiałów ferromagnetycznych, przenikalność magnetyczna materiału zmienia się wraz ze wzrostem natężenia pola magnetycznego. Z tej właściwości wynika pętla histerezy materiału.

**Źródła**

[1] Opracowanie do przedmiotu *Silne pola elektromagnetyczne w procesach przemysłowych*

[2] David J. Griffiths - *Introduction to electrodynamics*

[3] Materiały z wykładu *Materiały elektromagnetyczne*

### b) przewodnictwo elektryczne metali czystych i stopów, reguła Matthiessena, prawo Wiedemanna-Franza

Materiałoznawstwo elektrotechniczne: strona 78 - 91

**Przewodnictwo elektryczne metali czystych**

Zgodnie z **elektronową teorią przewodnictwa**, w metalach znajdują się wolne elektrony, niezwiązane z jonami siatki krystalicznej, które domyślnie poruszają się zgodnie w sposób chaotyczny, z energiami kinetycznymi zależnymi od temperatury - jest to tzw. ruch cieplny. Jony siatki krystalicznej natomiast drgają wokół położeń równowagi. 

W momencie przyłożenia pola elektrycznego, swobodne elektrony - nośniki ładunku - zaczynają oprócz ruchów losowych, przemieszczać się powoli, w sposób uporządkowany, w kierunku przeciwnym do linii sił pola elektrycznego. Ten powolny ruch elektronów w określonym kierunku nazywa się **dryfem**. Prędkość dryfu nazywa się **prędkością unoszenia,** natomiast proporcja prędkości unoszenia a natężeniem pola elektrycznego jest nazywana **ruchliwością elektronów**. 

Rezystancja (lub konduktywność) materiału jest w tej teorii rozumiana jako ilość zderzeń elektronów z jonami siatki krystalicznej. Im wyższa temperatura, tym wyższe ruchy cieplne i większe drgania siatki, stąd większe prawdopodobieństwo zderzenia - ruchliwość elektronów maleje, prędkość unoszenia się zmniejsza. Stąd definiuje się **temperaturowy współczynnik rezystancji.**

Innymi teoriami, którymi można wyjaśnić przewodnictwo metali są **teoria kwantowa** oraz **teoria pasmowa**. 

**Teoria kwantowa** opiera się na założeniu jamy potencjału - cząstki na zewnątrz metalu mają najwyższy poziom energii, wewnątrz - najniższy. Jako, że cząstki dążą do minimum energii, najniższe poziomy energetyczne są wypełnione, natomiast poziom najwyższy - jako pusty - pozwala na przewodnictwo. Poziom ten nazywa się poziomem Fermiego.

W **teorii pasmowej**, metale traktuje się jako duże atomy. Bliskość wielu atomów sprawia, że ich poziomy energetyczne (patrz: model atomu Bohra) są zbliżone, ale nie nakładają się na siebie - co można interpretować jako pasma energetyczne. Pasma energetyczne mogą być od siebie oddzielone lub nie. Jeżeli nie są oddzielone (jak w metalach), to materiały są w stanie przewodzić prąd przy minimalnym polu elektrycznym, tj. minimalnej dostarczonej energii - więc są traktowane jako przewodniki.

**Przewodnictwo elektryczne stopów metali**

Wszelkiego rodzaju defekty sieci krystalicznej, domieszki i zanieczyszczenia powodują zmniejszenie drogi swobodnej elektronów w przewodniku. Oznacza to, że stopy metali oraz wszelkiego rodzaju domieszki zawsze będą posiadać mniejszą przewodność niż metale czyste. Wynika to z faktu, że wszelkie domieszki powodują zakłócenia regularnej budowy siatki krystalicznej, co zwiększa opory ruchu elektronów swobodnych. 

Spadki konduktywności  mogą być znaczne, przy czym w stopach aluminium są większe niż w stopach miedzi. Ponadto, w stopach jednorodnych (tworzących roztwory stałe) rezystywność jest znacznie większa niż rezystywności metali składowych. Natomiast w stopach niejednorodnych, rezystywność zależy od procentowego udziału dwóch metali. Najwyższej wartości rezystywności można spodziewać się przy stosunku metali w stopie równym 1:1.

**Reguła Matthiessena**

Reguła Matthiessena opisuje rezystywność materiału jako sumę dwóch składowych: składowej termicznej oraz składowej strukturalnej. 

**Składowa termiczna** jest związana z drganiami siatki krystalicznej wywołanymi temperaturą. Składowa ta zanika wraz z dążeniem temperatury do 0 Kelvina. **Składowa strukturalna** dotyczy natomiast rezystywności wynikającej z wszelkich defektów siatki krystalicznej i nawet przy zerze kelwina, jej wartość jest niezerowa.

W praktyce oznacza to, że przy zerze kelwina, rezystywności materiałów nie opadają do 0.  

**Prawo Wiedemanna-Franza**

Prawo Wiedemanna-Franza to prawo fizyczne, zgodnie z którym stosunek przewodności cieplnej do przewodności elektrycznej metali jest proporcjonalny do temperatury. Wielkości te wiąże stała Lorenza, zgodnie ze wzorem:

$$
\frac{\kappa}{\sigma}=LT
$$

Prawo to zostało wyprowadzone empirycznie jeszcze w XIX wieku. W 2011 i 2016 roku znaleziono materiały, które dowodzą, że prawo Wiedemanna-Franza nie w każdym przypadku obowiązuje - czyli że jego pierwotna forma przestała być aktualna.

**Źródła:**

[1] Zdzisław Celiński - *Materiałoznawstwo elektrotechniczne*

[2] Materiały z wykładu *Materiały elektromagnetyczne*

[3] [http://www.ifmpan.poznan.pl/~urbaniak/cwiczenie1b.pdf](http://www.ifmpan.poznan.pl/~urbaniak/cwiczenie1b.pdf)

[4] [https://en.wikipedia.org/wiki/Wiedemann–Franz_law](https://en.wikipedia.org/wiki/Wiedemann%E2%80%93Franz_law)

### c) przewodnictwo elektryczne półprzewodników krystalicznych, półprzewodniki samoistne i domieszkowe

**Przewodnictwo elektryczne półprzewodników krystalicznych**

Półprzewodniki to materiały, których przewodność elektryczna jest mniejsza niż przewodność metali, natomiast większa niż przewodność dielektryków. Przy tym, konduktywność półprzewodników silnie zależy od warunków zewnętrznych, takich jak pole elektryczne, temperatura czy promieniowanie. 

Przewodnictwo elektryczne półprzewodników najlepiej wyjaśnia **teoria pasmowa**. Półprzewodnikami są materiały, w których siatce krystalicznej elektrony są silnie związane z atomami, a ich oderwanie wymaga dostarczenia z zewnątrz relatywnie dużej porcji energii, zwanej **energią aktywacji**. Ilość wymaganej energii do aktywacji półprzewodnika jest zależna od **pasma wzbronionego**, czyli pasma energetycznego pomiędzy pasmami przewodnictwa i walencyjnym w pasmowym modelu półprzewodnika. 

**Pasmo walencyjne** jest zakresem energii, jaką mają elektrony walencyjne związane z jądrem atomu. **Pasmo przewodnictwa** to zakres energii, którą mają elektrony uwolnione z atomu, będące (po uwolnieniu) nośnikami swobodnymi. 

![Untitled](8%20Materia%C5%82y%20elektromagnetyczne%200d995d1aaffe4bc192fc040239a1ee41/Untitled.png)

**Półprzewodniki samoistne**

Półprzewodniki samoistne to materiały, w których same **drgania cieplne elektronów walencyjnych mogą powodować ich wzbudzenie**, czyli przejście do pasma przewodnictwa. Przejście elektronu do pasma przewodnictwa powoduje powstanie **pary elektron-dziura**: elektron przeskakuje do innego pasma energetycznego, natomiast dziura jest de facto ubytkiem w paśmie walencyjnym - czyli, można powiedzieć, ładunkiem dodatnim (brakiem ładunku ujemnego) w tym paśmie. 

Proces powstawania par elektron-dziura nazywa się procesem **jonizacji**. Procesem odwrotnym do jonizacji jest proces **rekombinacji**, w którym pary dziura-elektron zostają zneutralizowane wskutek przeskoczenia elektronu do pasma walencyjnego. 

Elektrony w pasmie przewodnictwa stanowią niewielką liczbę wszystkich elektronów, co sprawia, że przewodność takiego półprzewodnika jest niewielka, np. w porównaniu do przewodności metali. 

Dziury zachowują się podobnie do swobodnych ładunków - tu też może odbywać się ruch nośników, tylko w kierunku odwrotnym do kierunku elektronów. Oznacza to, że **prąd płynący przez półprzewodnik jest wypadkowo sumą ruchu ładunków dodatnich i ujemnych**.

**Półprzewodniki domieszkowe**

Półprzewodniki domieszkowe to przewodniki, w których do materiałów bazowych (german, krzem) dodawane są odpowiednio dobrane domieszki. **Zależnie od dobranej domieszki, można uzyskać półprzewodnik typu n lub typu p.** Wprowadzenie atomów domieszkowych sprawia, że w półprzewodniku powstają dodatkowe poziomy energetyczne.

![Untitled](8%20Materia%C5%82y%20elektromagnetyczne%200d995d1aaffe4bc192fc040239a1ee41/Untitled%201.png)

**Półprzewodnik typu n (negative)** to taki, w którym domieszka sprawia, że w sieci krystalicznej pojawia się dodatkowy, słabo związany elektron. Taki elektron łatwo przechodzi do pasma przewodnictwa. Ta właściwość sprawia, że w półprzewodnikach typu n, większość nośników ładunku to elektrony, czyli mamy do czynienia z **elektronowym charakterem przewodnictwa elektrycznego** - stąd nazwa. 

W **półprzewodniku typu p (positive)**, domieszka sprawia, że nad pasmem walencyjnym pojawia się dodatkowe pasmo energetyczne. Przez to, większościowym nośnikiem ładunku stają się dziury elektronowe, więc mamy do czynienia z **przewodnictwem dziurowym.**

**Źródła**

[1] Zdzisław Celiński - *Materiałoznawstwo elektrotechniczne*

### d) mieszaniny dielektryczne

Mieszaniny dielektryczne to po prostu **połączenie różnych rodzajów dielektryków**. Stosuje się je **w celu uzyskania pożądanej przenikalności elektrycznej**. Wśród mieszanin dielektrycznych można wyróżnić mieszaniny regularne oraz mieszaniny nieregularne.

**Mieszaniny regularne** to takie, w których występuje regularność geometryczna. W tego typu mieszaninach, wypadkową przenikalność elektryczną można wyznaczyć analitycznie, w funkcji przenikalności i objętości materiałów składowych. Zależnie od ilości składników i ich proporcji, stosuje się różne równania - np. Clausuis’a-Mossottiego, Boetchera czy Rayleigha. 

**Mieszaniny nieregularne** to natomiast takie, w których nie ma regularności geometrycznej. Oznacza to, że mogą składać się ze zmieszanych ziaren o różnej wielkości (częściowo uporządkowane), mogą być zawiesinami (jeden składnik jest ośrodkiem dla drugiego) albo zbudowane tak, że ziarna jednego otaczają ziarna drugiego - i odwrotnie (mieszaniny równouprawnione). 

W **mieszaninach nieregularnych dwuskładnikowych**, przenikalność elektryczną przedstawia się jako charakterystyki, tzw. **krzywe Wienera**, które są krzywymi granicznymi. Rzeczywista przenikalność mieszaniny zawiera się między tymi krzywymi granicznymi. Dlaczego? Bo pierwsza krzywa graniczna daje przenikalność elektryczną jak w przypadku szeregowego ustawienia materiałów, druga - jak w przypadku równoległego. W mieszaninach nieregularnych, układ materiałów jest gdzieś po środku. **Krzywe Wienera są zależne od kształtu ziaren**. 

Jeżeli **kształt ziaren nie gra roli**, przenikalność mieszanin nieregularnych oblicza się za pomocą zależności podanych przez **Lichtenkera**, które są bardziej uogólnionym przypadkiem zależności Wienera. 

W przypadku mieszanin dielektrycznych w układach kompozytowych dielektryk-przewodnik, można mówić też o **zjawisku tunelowania**. W tym zjawisku chodzi o to, że ładunki z rozłożonych w dielektryku cząstek przewodzących mają pewne prawdopodobieństwo przeskoku przez barierę dielektryczną. Gdyby nie to, materiał tego typu byłby nieprzewodzący.

**Źródła:**

[1] Materiały z wykładu *Materiały elektromagnetyczne*