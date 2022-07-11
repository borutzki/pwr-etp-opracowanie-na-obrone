# 5. Zakłócenia w układach elektroenergetycznych

Status: Zrobione

### a) identyfikacja zwarć w systemie el. en. – algorytmy detekcji, klasyfikacji oraz określania kierunku zwarcia

### **Detekcja zwarć (*fault detection)***

Detekcja zwarć jest potrzebna w celu umożliwienia zadziałania urządzeń zabezpieczających. Zasadniczym **celem detekcji zwarcia jest wyodrębnienie przebiegu na interwały przed-zwarciowy i zwarciowy** (tzw. fault interval). 

W celu detekcji zwarć mierzy się różne wartości elektryczne, zależnie od użytej automatyki. Przykładami są amplitudy prądów fazowych, napięcia fazowe, impedancje fazowe czy prądy kolejności zerowej. Często operuje się też na pochodnych tych sygnałów. 

Można wyróżnić dwa główne algorytmy detekcji zwarć:

- **algorytm próbka-po-próbce**: porównuje się dwie kolejne próbki ze sobą. Jeżeli różnica między nimi jest zbyt duża (powyżej ustalonego progu), aktywowany jest licznik. Jeżeli różnice kolejnych próbek wciąż są duże, licznik się przepełnia i aktywowane jest urządzenie zabezpieczające.
- **algorytm okres-po-okresie:** porównuje się ze sobą aktualną próbkę i jej odpowiednik w poprzednim okresie (próbkę przesuniętą w czasie o 20 ms w przypadku sieci 50 Hz). Jeżeli różnica między tymi próbkami jest większa niż zakładane maksimum, to - podobnie jak wcześniej - aktywowany jest licznik i jeżeli kolejne różnice są również zbyt duże, licznik się przepełnia i aktywowane jest urządzenie zabezpieczające.

![Untitled](5%20Zak%C5%82o%CC%81cenia%20w%20uk%C5%82adach%20elektroenergetycznych%204553a7810b6d420398095081ed0771d3/Untitled.png)

Wartości progowe można określić np. na podstawie typowego przebiegu, gdzie największe różnice między próbkami zachodzą w pobliżu zera prądu czy napięcia, a najmniejsze - w szczytowych momentach sinusoidy. 

![Untitled](5%20Zak%C5%82o%CC%81cenia%20w%20uk%C5%82adach%20elektroenergetycznych%204553a7810b6d420398095081ed0771d3/Untitled%201.png)

W każdym razie, ustawia się pewien próg, nazywany wartością progową, którego przekroczenie powoduje aktywację automatyki zabezpieczającej. Próg ten jest jakąś krotnością wybranej wartości, np. 1,2 spodziewanego prądu - ale wartość jest różna zależnie od sytuacji stosowania zabezpieczenia. Dotyczy to obydwu algorytmów.

![Untitled](5%20Zak%C5%82o%CC%81cenia%20w%20uk%C5%82adach%20elektroenergetycznych%204553a7810b6d420398095081ed0771d3/Untitled%202.png)

![Untitled](5%20Zak%C5%82o%CC%81cenia%20w%20uk%C5%82adach%20elektroenergetycznych%204553a7810b6d420398095081ed0771d3/Untitled%203.png)

### **Określenie kierunków zwarć (*fault direction discrimination)***

**Określenie kierunku zwarcia to obliczenie mające odpowiedzieć na pytanie, w którą stronę przebiega zwarcie**. Informacja ta jest potrzebna, ponieważ urzą**dzenia zabezpieczające zabezpieczają przed różnymi typami zwarć, mianowicie zwarciami do przodu lub do tyłu względem rozpatrywanego punktu** (przykład: urządzenia przeciwzwarciowe odległościowe mogą zabezpieczać np. 85% długości linii przed zwarciami w określonym kierunku, ale jednocześnie nie reagują w ogóle na zwarcia przebiegające w drugą stronę). 

W celu określenia kierunku zwarcia, **wyznacza się impedancję przyrostową dla składowej zgodnej napięcia i prądu**. Impedancja przyrostowa to po prostu zmiana impedancji po wystąpieniu zwarcia. Liczy się ją z poniższego wzoru:

![Untitled](5%20Zak%C5%82o%CC%81cenia%20w%20uk%C5%82adach%20elektroenergetycznych%204553a7810b6d420398095081ed0771d3/Untitled%204.png)

A mówiąc bardziej po ludzku, impedancja przyrostowa dla składowej zgodnej to impedancja, w której zamiast tradycyjnego U/I, na górze daje się różnicę między składową zgodną napięcia w trakcie zwarcia i przed zwarciem, a na dole - różnicę między składową zgodną prądu w trakcie zwarcia i przed zwarciem.

Jak już mamy przyrost impedancji, to **określenie kierunku zwarcia zależy tylko od położenia impedancji przyrostowej na płaszczyźnie zespolonej**. Jeżeli **impedancja jest w trzeciej ćwiartce, zwarcie jest zwarciem do przodu**. Jeżeli **impedancja jest w pierwszej ćwiartce, zwarcie jest zwarciem do tyłu**. Tak po prawdzie, wystarczy znać znak reaktancji, żeby określić kierunek zwarcia.

![Untitled](5%20Zak%C5%82o%CC%81cenia%20w%20uk%C5%82adach%20elektroenergetycznych%204553a7810b6d420398095081ed0771d3/Untitled%205.png)

### **Klasyfikacja zwarć (*phase selection)***

**Klasyfikacja zwarć to określenie rodzaju zwarcia - które fazy biorą w nim udział** (zwarcie jednofazowe, dwufazowe, trójfazowe) oraz **czy jest to zwarcie z udziałem ziemi,** czy bez. Informacja ta jest potrzebna w celu określenia odpowiedniej pętli zwarciowej.

**Według informacji z wykładu, w celu klasyfikacji zwarć wykorzystuje się informacje o amplitudach składowej zgodnej, przeciwnej i zerowej prądu. Na podstawie informacji o tych składowych oblicza się kąty alfa, alfa przyrostowy oraz beta.** Kąt alfa to kąt stosunku składowej przeciwnej do zgodnej (liczby zespolone!), kąt przyrostowy alfa to kąt stosunku składowej zgodnej do przyrostu składowej zgodnej, natomiast kąt beta to kąt stosunku składowej przeciwnej do składowej zerowej). 

**Ogólnie, bierze się tu pod uwagę stosunek składowej przeciwnej do zgodnej, składowej przeciwnej do składowej zerowej oraz duże zmiany składowej zgodnej przy braku pozostałych składowych.**

Z powyższego, klasyfikację zwarć można opisać poniższym algorytmem. Wielkości oznaczone w nawiasach {x} to wielkości opcjonalne w klasyfikacji. Kąty alfa są uwzględniane zawsze, kąt beta tylko przy niesymetrycznych zwarciach z udziałem ziemi

![Untitled](5%20Zak%C5%82o%CC%81cenia%20w%20uk%C5%82adach%20elektroenergetycznych%204553a7810b6d420398095081ed0771d3/Untitled%206.png)

Opisując to słowami:

1. **Zwarcie trójfazowe symetryczne** to zwarcie w którym następuje **przyrost składowej zgodnej**, natomiast **nie pojawiają się w ogóle składowa zgodna i przeciwna**. 
2. **Zwarcia z udziałem ziemi:** w tych zwarciach pojawia się składowa zerowa, więc pojawia się kąt beta. Są tu zwarcia jednofazowe (doziemne) oraz dwufazowe niesymetryczne. 
3. **Zwarcia izolowane:** zwarcia te nie mają składowej zerowej, są bez udziału ziemi. Liczy się tylko kąt alfa, kąt beta nie jest uwzględniany bo składowa zerowa jest równa 0. 

![Untitled](5%20Zak%C5%82o%CC%81cenia%20w%20uk%C5%82adach%20elektroenergetycznych%204553a7810b6d420398095081ed0771d3/Untitled%207.png)

### Najważniejsze punkty

- detekcja zwarć: algorytm próbka-po-próbce lub okres-po-okresie; chodzi o wykrycie czy w ciągu próbki lub okresu jakaś wartość wyskoczyła ponad wartość graniczną zadziałania zabezpieczenia
- określanie kierunku zwarcia: obliczenie impedancji przyrostowej (zmiany impedancji) dla składowej zgodnej; na podstawie jej położenia na płaszczyźnie zespolonej określa się kierunek zwarcia
- klasyfikacja zwarć: oblicza się składowe symetryczne i kąty między nimi, a na tej podstawie można określić typ zwarcia (symetryczne, niesymetryczne jednofazowe/dwufazowe, doziemne, etc.)

### **Źródła**

[1] Materiały z wykładu *Zakłócenia w układach elektroenergetycznych*

[2] Jan Iżykowski - *Power System Faults*

### b) obliczanie prądów i napięć podczas zwarć symetrycznych i niesymetrycznych w sieciach wysokiego napięcia z punktem neutralnym uziemionym bezpośrednio

**Zwarcia symetryczne** to zwarcia w których wektory prądów przewodowych i napięć fazowych są symetryczne - czyli są to zwarcia 3-fazowe. **Zwarcia niesymetryczne** to zwarcia w których fazy obciążone są nierównomiernie - czyli zwarcia 1-fazowe (**doziemne**), 2-fazowe oraz 2-fazowe z ziemią. 

Do obliczania prądów i napięć podczas zwarć w sieciach wysokiego napięcia stosuje się **metodę składowych symetrycznych**. Ponadto, praca z bezpośrednio uziemionym punktem neutralnym oznacza, że punkt neutralny N oraz ziemia E są ze sobą elektrycznie połączone. Przekształcenia napięć i prądów fazowych na składowe symetryczne przedstawiono poniżej:

![Untitled](5%20Zak%C5%82o%CC%81cenia%20w%20uk%C5%82adach%20elektroenergetycznych%204553a7810b6d420398095081ed0771d3/Untitled%208.png)

W obliczeniach przyjmuje się, że zwarcie dotyczy jednego węzła sieci, a w stanie przed zwarciem panują warunki symetrii fazowej napięć i prądów - czyli składowe zgodne są różne od zera, składowe zerowe i przeciwne - równe zeru. 

**Zwarcia symetryczne**

W przypadku zwarć trójfazowych, zakłada się że zwarcie trzech faz nastąpiło przez symetryczną impedancję. Prądy i napięcia składowej zgodnej są niezerowe, pozostałych składowych - równe zeru. 

![Untitled](5%20Zak%C5%82o%CC%81cenia%20w%20uk%C5%82adach%20elektroenergetycznych%204553a7810b6d420398095081ed0771d3/Untitled%209.png)

W przypadku zwarcia trójfazowego, można przyjąć że prądy i napięcia w poszczególnych fazach są takie same, co upraszcza obliczenia. Do samych obliczeń stosuje się metodę Thevenina. Rozpatrywany układ przedstawia się jako uproszczony schemat zastępczy, a na to stosuje się zasadę superpozycji - sieć zastępuje się dwiema sieciami zastępczymi, w których jedna jest siecią w normalnym stanie pracy, druga - stanem uzupełniającym. Stan uzupełniający to sieć w której doprowadza się w punkcie zwarcia napięcie o kierunku zgodnym z napięciem przed zwarciem. 

![Untitled](5%20Zak%C5%82o%CC%81cenia%20w%20uk%C5%82adach%20elektroenergetycznych%204553a7810b6d420398095081ed0771d3/Untitled%2010.png)

Po wykonaniu superpozycji, sieć upraszcza się do jednego elementu zastępczego Thevenina, z którego można policzyć składową zgodną prądu i napięcia  - która jako jedyna występuje podczas tego typu zwarcia. 

**Zwarcie jednofazowe**

W przypadku zwarć jednofazowych rozpatruje się jako graficzną interpretację składowych symetrycznych. W takim zwarciu sieci dla składowych zgodnej, przeciwnej i zerowej są ze sobą połączone szeregowo. Suma napięć poszczególnych składowych jest równa zeru, natomiast składowe prądu są sobie równe dla wszystkich składowych. 

![Untitled](5%20Zak%C5%82o%CC%81cenia%20w%20uk%C5%82adach%20elektroenergetycznych%204553a7810b6d420398095081ed0771d3/Untitled%2011.png)

Ponownie, zwarcie oblicza się stosując metodę Thevenina z zastępczym źródłem i obciążeniem. Analizę prądów i napięć prowadzi się w oparciu o składowe symetryczne. 

W przypadku zwarć jednofazowych, pojawienie się zakłócenia w jednej z faz wpływa na inne fazy. 

**Zwarcia dwufazowe**

W przypadku zwarcia między dwiema fazami bez udziału ziemi, układ rozpatrujemy jako taki, w którym pojawiają się składowa zgodna i przeciwna, ale nie pojawia się składowa zerowa. W rozpatrywanym układzie sieci składowej zgodnej i przeciwnej przedstawia się jako połączone równolegle do siebie poprzez impedancję zwarcia.  

![Untitled](5%20Zak%C5%82o%CC%81cenia%20w%20uk%C5%82adach%20elektroenergetycznych%204553a7810b6d420398095081ed0771d3/Untitled%2012.png)

Ponownie, do obliczeń stosuje się metodę Thevenina i upraszcza obwód. Prądy i napięcia oblicza się kolejno z praw Ohma i Kirchhoffa dla przyjętych impedancji poszczególnych składowych symetrycznych oraz impedancji zwarcia.

![Untitled](5%20Zak%C5%82o%CC%81cenia%20w%20uk%C5%82adach%20elektroenergetycznych%204553a7810b6d420398095081ed0771d3/Untitled%2013.png)

**Zwarcia dwufazowe z ziemią**

W przypadku zwarcia dwóch faz z ziemią, suma ich prądów płynie do ziemi.  Odpowiada to trzykrotnej wartości składowej zerowej prądu zwarcia. Stąd, w schemacie składowych symetrycznych, łączy się je ze sobą w jednym węźle. W obwodzie składowej zerowej pojawia się natomiast trzykrotność impedancji zwarcia.

![Untitled](5%20Zak%C5%82o%CC%81cenia%20w%20uk%C5%82adach%20elektroenergetycznych%204553a7810b6d420398095081ed0771d3/Untitled%2014.png)

W każdym razie, ponownie do obliczenia prądów i napięć zwarciowych stosuje się metodę Thevenina, a potem kolejne wartości prądów, napięć i impedancji oblicza na podstawie praw Kirchhoffa i Ohma. 

**Podsumowanie**

Ogólnie rzecz ujmując, w przypadku obliczania prądów i napięć podczas zwarć w sieciach wysokiego napięcia z punktem neutralnym bezpośrednio uziemionym, stosuje się w każdym przypadku metodę składowych symetrycznych. 

Prądy, napięcia i impedancje dla poszczególnych składowych symetrycznych przedstawia się w postaci schematów zastępczych. Schematy te są ze sobą połączone w różne sposoby, zależnie od rodzaju zwarcia. 

Przyjęte schematy zastępcze oblicza się następnie, korzystając z twierdzenia Thevenina oraz praw Kirchhoffa i Ohma. Otrzymane wartości poszczególnych składowych symetrycznych przekształca się z powrotem do układu trójfazowego. 

A poniżej garść wzorów dla sportu.

![Untitled](5%20Zak%C5%82o%CC%81cenia%20w%20uk%C5%82adach%20elektroenergetycznych%204553a7810b6d420398095081ed0771d3/Untitled%2015.png)

### Najważniejsze punkty

- obliczanie prądów i napięć zwarć w sieciach WN uziemionych bezpośrednio sprowadza się do analizy składowych symetrycznych i metody Thevenina
- w pierwszym kroku oblicza się wartości poszczególnych składowych symetrycznych
- zależnie od rodzaju zwarcia, rysuje się odpowiedni schemat zastępczy dla składowych symetrycznych i upraszcza obwód
- schemat zastępczy - prądy i napięcia miejsca zwarcia - liczy się za pomocą metody Thevenina

### **Źródła**

[1] Kacejko, Machowski - *Zwarcia w systemach elektroenergetycznych*

### c) zjawiska prądowe i napięciowe towarzyszące zwarciom doziemnym w sieciach rozdzielczych średniego napięcia

Sieci rozdzielcze średniego napięcia, w przeciwieństwie do sieci WN, są często sieciami z **izolowanym punktem neutralnym** lub z **punktem neutralnym uziemionym przez dławik, rezystor lub obydwa**. Ta sytuacja sprawia, że w przypadku zwarć doziemnych, **składowa zerowa prądu zwarciowego ma małą wartość**. Wskutek tego, w analizie zachodzących zjawisk należy uwzględniać pojemności sieci równoległą do impedancji składowej zerowej.

  

![Untitled](5%20Zak%C5%82o%CC%81cenia%20w%20uk%C5%82adach%20elektroenergetycznych%204553a7810b6d420398095081ed0771d3/Untitled%2016.png)

![Untitled](5%20Zak%C5%82o%CC%81cenia%20w%20uk%C5%82adach%20elektroenergetycznych%204553a7810b6d420398095081ed0771d3/Untitled%2017.png)

Zjawiska prądowe i napięciowe w przypadku zwarć doziemnych zależą od tego, w jaki sposób uziemiony (lub izolowany) jest punkt zerowy układu. Izolowany punkt neutralny i uziemienie przez dławik (kompensację sieci) stosuje się w relatywnie niewielkich sieciach SN. Rezystory stosowane są natomiast w sieciach rozległych 

W każdym przypadku można jednak zakładać, że wskutek wyładowania pojemności fazy zwieranej i doładowania pojemności faz zdrowych, nastąpią duże przepięcia, szybkie oscylacje i zapalenie łuku elektrycznego. 

Stąd, można wyróżnić trzy przypadki:

1. **Izolowany punkt zerowy**
    
    W przypadku izolowanego punktu zerowego, impedancja dla składowej zerowej jest bardzo duża. Prąd zwarcia ma zatem charakter pojemnościowy. Prąd zwarciowy największą wartość ma w miejscu zwarcia, a im bliżej do źródła zasilania, tym jest ona niższa - co wynika z rozłożonej pojemności linii. 
    
    Jeżeli chodzi o napięcia, to napięcie fazy ze zwarciem spada do 0, natomiast napięcia pozostałych faz wzrastają do wartości międzyfazowej. Pojawia się jednak przy tym niebezpieczne zjawisko polegające na wyładowaniu pojemności linii dla faz zdrowych, mających dużą wartość napięcia w czasie zwarcia. Rozładowanie tych pojemności może spowodować duże oscylacje i bardzo silne przepięcia w układzie. Może pojawić się tu też przerywany łuk elektryczny.
    
2. **Punkt zerowy uziemiony przez dławik**
    
    W celu kompensacji prądu pojemnościowego, sieć może być uziemiona przez dławik - jest nim np. cewka Petersena lub transformator Baucha albo Reithoffera. W celu takiego uziemienia, muszą być stosowane specjalne transformatory uziemiające. 
    
    W idealnym przypadku, kompensacja pojemności przez cewkę prowadzi do osiągnięcia prądu zwarcia równego 0. Składowe symetryczne napięcia w tej sytuacji stają się identyczne jak w przypadku sieci z izolowanym punktem neutralnym. Napięcie uszkodzonej fazy spada do zera, natomiast napięcia faz zdrowych wzrastają do wartości międzyprzewodowej. Prąd zwarciowy jest najmniejszy w miejscu zwarcia, a największy w punkcie gwiazdowym transformatora. 
    
    W przypadku uziemienia cewką powstają warunki do szybszego gaszenia łuku, co sprawia, że napięcia faz wracają do poziomu sprzed wystąpienia zwarcia w relatywnie krótkim czasie. Co ciekawe, sieć uziemiona przez cewkę Petersena może działać przez dłuższy czas w stanie zwarcia.
    
    W praktyce jednak nie istnieje idealna kompensacja (cewka jest dobrana tylko na podstawową harmoniczną), a co więcej - powodowałaby ona największe przepięcia w układzie przy rozładowywaniu pojemności. Cewki Petersena stosuje się wraz ze sterowaniem ich reaktancją. 
    
3. **Punkt zerowy uziemiony przez rezystor lub rezystor równoległy z dławikiem**
    
    Stosowanie rezystora to metoda mieszcząca się między siecią z izolowanym punktem pracy a siecią skutecznie uziemioną. Tego typu uziemienia stosuje się po to, żeby w kontrolowany sposób zwiększyć prąd zwarciowy w celu przyspieszenia zadziałania zabezpieczeń - ustala się poziom prądu zwarciowego na od kilkudziesięciu amperów do kilkuset amperów. 
    
    Zapewnienie odpowiedniej rezystancji podnóży stacji elektroenergetycznych jest trudne do zapewnienia, więc stosuje się też układ R-L równoległy. Rezystor działa w czasie zwarcia, natomiast cewka w normalnym stanie pracy (kompensuje ona sieć). 
    
    Przełączenie na rezystor można opóźnić - kompensacja zwarcia przez cewkę w początkowej fazie może ułatwić zgaszenie łuku elektrycznego. 
    
4. **Punkt zerowy uziemiony bezpośrednio**
    
    Ten wariant raczej nie będzie potrzebny do zaliczenia egzaminu, ale można o nim wspomnieć. W przypadku, gdy dojdzie do zwarcia doziemnego w sieci z uziemionym bezpośrednio punktem neutralnym, przepływ prądu zwarciowego przez ziemię i jego transformacja przez transformator na stronę sieci sprawiają, że generator zasilający sieć obciążony jest prądem zwarciowym w dwóch fazach. 
    
    Jeżeli punkt zerowy jest uziemiony, to ma on dużą wartość. Ma ona znacznie większe znaczenie niż składowa pojemnościowa prądu. Oczywiście znowu pojawia się zjawisko rozładowania pojemności fazy ze zwarciem i doładowania faz zdrowych, ale fazy zdrowe tym razem nie mają zwiększonej wartości napięcia, więc przebiegi i oscylacje są odpowiednio mniejsze. 
    

### Najważniejsze punkty

- zwarcia doziemne w sieciach SN ze względu na izolowanie punktu neutralnego lub uziemienie przez rezystor lub dławik, uwidaczniają zjawiska związane z pojemnościami linii
- podczas zwarć doziemnych, można spodziewać się rozładowania pojemności fazy ze zwarciem i doładowania pojemności faz zdrowych i wzrostu napięcia w nich
- rozładowania i doładowania pojemności prowadzą do dużych przepięć, szybkich oscylacji oraz powstawania łuku elektrycznego
- uziemienie przez dławik może kompensować sieć, czyli sprowadzać prąd zwarciowy do 0
- uziemienie przez rezystor służy do odpowiedniego zwiększenia prądu zwarciowego tak, by zadziałały zabezpieczenia

**Źródła**

[1] Iżykowski - *Power system faults*

[2] Kacejko, Machowski - *Zwarcia w systemach elektroenergetycznych*

### d) zapady napięcia i przerwy w zasilaniu - przyczyny, skutki i sposoby ochrony

Z definicji, **zapad napięcia** to **nagłe zmniejszenie się napięcia zasilającego do wartości zawartej w przedziale od 90% do 1% napięcia znamionowego Un, po którym następuje wzrost napięcia do poprzedniej wartości**. Umownie, czas trwania zapadu napięcia wynosi od 10 ms do 1 minuty.

**Przerwa w zasilaniu** jest natomiast **całkowitym odizolowaniem odbiorcy od źródła zasilania**. Z definicji wyróżnia się krótkie przerwy w zasilaniu (do 1 minuty) oraz długie przerwy w zasilaniu (powyżej 1 minuty). 

![Untitled](5%20Zak%C5%82o%CC%81cenia%20w%20uk%C5%82adach%20elektroenergetycznych%204553a7810b6d420398095081ed0771d3/Untitled%2018.png)

**Parametry**

Zapady napięcia oraz przerwy w zasilaniu charakteryzuje się następującymi wielkościami:

- wartością zapadu napięcia
- czasem trwania
- głębokością zapadu napięcia
- wielkością zapadu napięcia

![Untitled](5%20Zak%C5%82o%CC%81cenia%20w%20uk%C5%82adach%20elektroenergetycznych%204553a7810b6d420398095081ed0771d3/Untitled%2019.png)

**Przyczyny**

Wśród przyczyn zapadów napięcia, można wyróżnić przyczyny wewnętrzne i zewnętrzne. 

**Przyczyny zewnętrzne** to przyczyny pojawiające się w systemie elektroenergetycznym i można do nich zaliczyć:

- zmiany konfiguracji sieci, prowadzące do wzrostu impedancji źródła (czyli np. zbyt duża impedancja nowej linii, transformatora i spadek napięcia na niej)
- zwarcia w sieci
- nieprawidłowa praca regulatora napięcia transformatora

**Przyczyny wewnętrzne** to natomiast przyczyny występujące w instalacji odbiorcy. Można wśród nich wymienić:

- Załączanie dużych odbiorników statycznych, np. pieców oporowych
- Rozruch bezpośredni dużych silników asynchronicznych
- Zwarcia w instalacji odbiorcy

Na podstawie powyższych, można wymienić trzy podstawowe, zasadnicze przyczyny zapadów:

- **duże prądy**: powodują one znacznie większy spadek napięcia na impedancjach sieci lub instalacji, więc w miejscu odbiornika napięcie jest niższe
- **impedancje sieci**: jeżeli impedancje między źródłem zasilania a odbiornikiem są duże, napięcie na zaciskach odbiornika jest znacznie obniżone
- **regulacja**: jeżeli np. przy regulatorze napięcia transformatora coś działa nieprawidłowo, napięcie może zostać obniżone do poziomu poniżej wartości progowej.

**Skutki**

Podstawowym skutkiem zapadów napięcia jest fakt, że urządzenia odbiorcze nie otrzymują wymaganej ilości energii elektrycznej, więc przestają działać prawidłowo. Dotyczy to zarówno bezpośrednio odbiorników, jak i układów regulacji. 

Stąd, wśród skutków zapadów napięcia można wymienić:

- nieprawidłowe działanie wrażliwych odbiorników energii elektrycznej takich jak napędy elektryczne z regulacją prędkości, sprzęt informatyczny, urządzenia elektroniczne itd.
- zbędne wyłączenia odbiorników przez styczniki lub układ sterowania
- zbędne wyłączenia odbiorników przez zabezpieczenie podnapięciowe
- zbędne wyłączenia silników przez zabezpieczenia od asymetrii zasilania

**Sposoby ochrony**

Istnieje kilka różnych podejść mających na celu ochronę przed skutkami zapadów napięcia lub zapobiegających takim zjawiskom w systemie elektroenergetycznym. Celami nadrzędnymi są redukcja czasu trwania zapadu, redukcja częstotliwości występowania zapadów oraz uodparnianie urządzeń na zapady napięcia. Wszystkie te zjawiska sprowadzają się natomiast do ograniczania skutków zwarć.

Stąd, można wymienić następujące metody ochrony przed negatywnymi skutkami zapadów napięcia:

1. **Redukcja liczby zwarć**
    
    Redukcję liczby zwarć można osiągnąć metodami bardzo konwencjonalnymi. Zastępuje się linie napowietrzne liniami kablowymi lub stosuje się w nich izolowane przewody. Przycina się drzewa w strefie tych linii i instaluje osłony przed zwierzętami. Ekranuje się przewody napowietrzne, zwiększa poziom izolacji i instaluje liniowe odgromniki. Można też po prostu zwiększyć częstotliwość remontów, przeglądów, mycia izolatorów itp.
    
2. **Redukcja czasu eliminacji zwarć**
    
    Redukcja czasu zwarć łagodzi ich skutki, nie ogranicza ich rzadszego występowania. Najprościej, stosuje się bezpieczniki z ograniczeniem prądu. Redukcja czasu eliminacji zwarć nie oznacza natomiast skrócenia czasu przerwy w zasilaniu. 
    
3. **Zmiana konfiguracji systemu zasilającego**
    
    Rozwiązania tego typu są kosztowne, zwłaszcza w sieciach wysokich napięć, bo sprowadzają się do redundancji. Można zainstalować generator w pobliżu czułych odbiorów. Można zwiększyć liczbę szyn i rozdzielni w celu ograniczenia ilości odbiorców odczuwających zakłócenia lub instalować dławiki zwarciowe w celu zwiększenia elektrycznej odległości od miejsca zwarcia. Można też zasilać czułych odbiorców równolegle z kilku rozdzielni - wtedy zapad napięcia na jednej jest redukowany zasilaniem z innej. 
    
4. **Włączenie specjalnych urządzeń pomiędzy sieć zasilającą i zaciski czułego sprzętu (stabilizatory napięcia)**
    
    Stabilizatory napięcia to najpowszechniej stosowane zabezpieczenie przed negatywnymi skutkami zapadów. Mogą być stosowane tak po stronie sieci jak i odbiorcy, ale raczej stosuje się je właśnie po stronie odbiorcy. Urządzenia tego typu mają na celu w razie zaburzenia szybko przełączyć urządzenie na zasilanie z alternatywnego źródła energii, zapewniając przy tym odpowiednie parametry zasilania. De facto są to wszelkiego rodzaju zasilacze UPS.
    
5. **Poprawa odporności urządzeń**
    
    Dobrą metodą ograniczania skutków zapadów napięcia, zwłaszcza u odbiorców przemysłowych, jest dobór urządzeń o odpowiedniej odporności na zakłócenia. W idealnym świecie można by na podstawie informacji o pracy systemu w danym miejscu dobrać urządzenia o odpowiedniej czułości lub w oparciu o tę informację zdecydować się na UPS (bo tańszy). Niestety, aktualnie nie ma żadnych standardów tego typu i ciężko jest te informacje otrzymać. Stąd, poprawa odporności urządzeń sprowadza się do ich odpowiedniego zaprojektowania już na etapie produkcji. 
    

### Najważniejsze punkty

- zapad napięcia to spadek napięcia w sieci do wartości 1-90% wartości znamionowej na czas do 1 minuty; powyżej tego czasu mówimy o przerwie w zasilaniu
- zapady napięcia mają przyczyny zewnętrzne (poza instalacją odbiorczą) oraz wewnętrzne (wynikające z działania instalacji); wszystkie te przyczyny sprowadzają się do dużych prądów i spadków napięć na impedancjach linii lub do nieprawidłowej pracy układów regulacji
- przyczyny zewnętrzne: zwarcia i awarie w systemie, zmiany konfiguracji sieci, nieprawidłowa praca regulacji transformatora
- przyczyny wewnętrzne: załączanie dużych odbiorników, rozruch silników, zwarcia
- skutki: nieprawidłowa praca odbiorników, nieplanowane wyłączenia odbiorników przez zabezpieczenia i wiążące się z tym straty finansowe
- zapobieganie: odpowiednie projektowanie urządzeń, redukcja liczby i czasu eliminacji zwarć, stosowanie zasilaczy UPS, zmiana konfiguracji zasilania (dodatkowy generator, druga linia zasilająca itp.)

**Źródła**

[1] Materiały z wykładu *Zakłócenia w układach elektroenergetycznych*

[2] [https://www.cire.pl/pliki/2/hanzelka-zapady1.pdf](https://www.cire.pl/pliki/2/hanzelka-zapady1.pdf)

[3] [https://pl.wikipedia.org/wiki/Zapad_napięcia](https://pl.wikipedia.org/wiki/Zapad_napi%C4%99cia)