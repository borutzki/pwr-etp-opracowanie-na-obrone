# 12. Komputerowe wspomaganie projektowania w energetyce

Status: Zrobione

### a) ogólna charakterystyka programów typu CAD do projektowania instalacji elektrycznych

**CAD** - *Computer Aided Design -* komputerowo wspomagane projektowanie; 

**CAE** - *Computer Aided Engineering* - komputerowo wspomagana inżynieria.

Obydwie powyższe definicje dotyczą pakietów oprogramowania, przeznaczonych do **komputerowego wspomagania prac inżynierskich, rysowania i projektowania**. Wśród programów CAD można wyróżnić **programy uniwersalne**, opracowywane przez niezależnych producentów, oraz **programy dedykowane**, opracowywane przez poszczególne firmy z branży - w tym wypadku elektroenergetycznej. 

Programy **uniwersalne** posiadają **otwarte bazy różnego rodzaju rozwiązań**, natomiast **oprogramowanie dedykowane** na ogół zawiera **bazy rozwiązań** (elementów instalacji, etc.) **konkretnego producenta**. 

Wśród programów CAD do projektowania instalacji elektrycznych, można wymienić:

- **programy obliczeniowe** - służą do **wykonywania obliczeń** instalacji elektrycznych, znacząco przyspieszając **proces doboru przekroju przewodów oraz aparatów elektrycznych** i zabezpieczeń w różnych typach instalacji, w tym instalacji oświetleniowych; przykłądy: *Relux, Dialux, Pająk, Simaris;*
- **programy do tworzenia planów instalacji** - programy te służą do planowania położenia instalacji elektrycznych w rzeczywistych obiektach - czyli de facto do przygotowywania projektów wykonawczych instalacji; przykłady: *Revit, AutoCAD Electrical, WSCAD;*
- **konfiguratory -** ich głównym zadaniem jest konfiguracja szaf elektrycznych, porównywanie charakterystyk czasowo-prądowych urządzeń, dobór układów rozruchowych, wyłączników, etc. Konfiguratory występują na ogół w postaci funkcji w programach innego typu.
- **programy do projektowania rozdzielnic -** służą do doboru aparatów elektrycznych oraz ich umiejscowienia, a często także wymiarowania oraz kosztorysowania rozdzielnic; przykłady: *XL PRO2, ETI-pro, XPD;*

Podstawowymi typami programów do projektowania instalacji są zatem programy obliczeniowe oraz programy do tworzenia planów instalacji. 

**Programy obliczeniowe** pozwalają na projektowanie rozbudowanych sieci elektrycznych. **Na podstawie zadanych parametrów** układu, takich jak napięcie górne i dolne transformatora, układ, częstotliwość czy rezerwy - **wprowadzonych przy użyciu środowiska graficznego** - **programy obliczeniowe obliczają wymagane parametry komponentów elektrycznych**, w tym przekrój przewodów, prądy i napięcia aparatury, etc. 

Na ogół, **programy tego typu (**przykład: Simaris, Pająk) **umożliwiają** także **prostą edycję ręczną** poszczególnych **komponentów instalacji**, a także szybkie **wykonywanie dokumentacji graficznej** (schematy jednokreskowe) **i tekstowej** (spis aparatury i wyników obliczeń) rozpatrywanej instalacji.

**Programy do tworzenia planów instalacji** pozwalają natomiast na **wykonywanie przestrzennych projektów instalacji**, obejmujących **umiejscowienie poszczególnych elementów układu** takich jak rozdzielnice, gniazdka, położenie przewodów i rodzaj ich poprowadzenia. W takich przypadkach stosuje się programy typu Revit czy AutoCAD, coraz częściej także Solidworks. Programy te służą również często do wykonywania **wizualizacji projektów**. 

**Źródła**

[1] Robert Leśniak - *Opracowanie do wykładu Komputerowe systemy CAD projektowania w elektroenergetyce*

[2] Materiały z wykładu *Komputerowe systemy CAD projektowania w elektroenergetyce*

### b) zasady projektowania oświetlenia wnętrz i oświetlenia terenów zewnętrznych. Wykorzystanie oprogramowania typu CAD do projektowania oświetlenia

### **Zasady projektowania oświetlenia wnętrz**

Projektując oświetlenie wnętrz, należy zadbać o to, by spełnione zostały określone normami parametry oświetlenia. Wartości tych parametrów zależą głównie od typu budynku i charakteru oświetlenia. Ponadto, źródła światła powinny spełniać wymogi otoczenia, czyli mieć odpowiednią klasę IK oraz IP. 

Projektowanie sprowadza się do doboru rodzajów źródeł światła oraz umiejscowienia ich na terenie budynku lub pomieszczenia w taki sposób, by spełnione zostały warunki co do następujących parametrów:

- **natężenie oświetlenia** - *gęstość powierzchniowa strumienia świetlnego*, padającego na daną powierzchnię, wyrażona w [lx] - przynajmniej 200 lx w płaszczyźnie roboczej;
- **równomierność oświetlenia** - *iloraz z najmniejszej zmierzonej wartości natężenia oświetlenia na danej płaszczyźnie do średniego oświetlenia na tej płaszczyźnie;* na ogół wartość ta powinna być większa niż 0,7;
- **rozkład luminancji** - ****luminancja to miara natężenia oświetlenia padającego w danym kierunku, wyrażona jako [cd/m2]; rozkład luminancji podaje się w formie współczynników odbicia ścian, sufitu i podłogi i im jest większy, tym lepiej światło odbija się od tych miejsc
- **współczynnik olśnienia przykrego** - $UGR$ - współczynnik ten wyznacza się na etapie projektowania instalacji i powinien mieć odpowiednio niską wartość, by zjawisko olśnienia nie występowało; zjawisko to jest dyskomfortem wywołanym dużymi kontrastami oświetlenia w otoczeniu lub poprzez bezpośrednie spojrzenie na źródło światła lub odbitego światła
- **barwa światła -** de facto temperatura barwowa; jej wartość na ogół powinna rosnąć wraz ze wzrostem średniej wartości wymaganego natężenia oświetlenia
- **wskaźnik oddawania barw -** parametr ten wskazuje na właściwości oddawania barw przez źródła światła i powinien być możliwie wysoki, minimum 80; w pobliżu 100 jeżeli praca jest wrażliwa na kolory.
- **migotanie i efekt stroboskopowy** - powinno się unikać układów zasilania 50 Hz dla opraw oświetleniowych pracujących w otoczeniu maszyn wirujących - mogą one prowadzić do zjawiska stroboskopowego.

### **Zasady projektowania oświetlenia terenów zewnętrznych**

Projektowanie oświetlenia terenów zewnętrznych również wymaga spełnienia pewnych parametrów oświetleniowych, z tym że określają to inne normy. 

Projektowanie oświetlenia terenów zewnętrznych można podzielić na 3 etapy:

1. **Określenie założeń projektowych** takich, jak rodzaj oświetlenia drogi, jej wymiary, przeznaczenie, rodzaj nawierzchni, otoczenie, użytkownicy drogi i prędkość ruchu, etc.
2. **Wybór określonej sytuacji oświetleniowej oraz klasy oświetlenia i określenie wymagań oświetleniowych**, zgodnie z normami.
3. **Wybór źródeł światła i opraw oświetleniowych** w taki sposób, by cały czas były zachowane wszystkie wymagane parametry oświetleniowe.
4. **Dobór sposobu rozmieszczenia punktów świetlnych i geometrii systemu świetlnego.**
5. **Wykonanie obliczeń parametrów oświetleniowych i sprawdzenie pod kątem spełnienia norm.**

Wśród parametrów wybieranych na potrzeby oświetlenia zewnętrznego, zwłaszcza drogowego, znajdują się:

- **luminancja**: jaskrawość powierzchni, widziana przez obserwatora poruszającego się w określonym kierunku - zależy od poziomu natężenia oświetlenia, rodzaju opraw, jasności drogi, odbić od powierzchni
- **poziom luminancji drogi** - utrzymanie odpowiedniego poziomu luminancji na drodze gwarantuje dobrą widoczność
- **równomierność luminancji drogi** - im większa, tym lepsze warunki jazdy - brak stref jasnych i ciemnych; minimum to 0,4
- **ograniczanie olśnienia** - wskaźnik progu kontrastu TI powinien być mniejszy niż 10; oprawy powinny dobrze rozprowadzać światło, nie kierować go w oczy kierowców;
- **prowadzenie wzrokowe** - odpowiednie instalacje dają dodatkowe informacje - np. przy zjazdach, zakrętach itp. powinien być stosowany inny rodzaj oświetlenia niż na drogach prostych (inna wysokość, inna barwa światła, etc.)

### Wykorzystanie oprogramowania typu CAD do projektowania oświetlenia

Do projektowania oświetlenia można wykorzystać oprogramowanie typu DIALUX lub RELUX, które pozwala na wygodny dobór opraw ulicznych, planowanie ich rozmieszczenia w rzutach trójwymiarowych lub dwuwymiarowych. 

Dobrane w ten sposób oprawy i ich rozmieszczenie można wprowadzić do modułu obliczeniowego, by przeliczyć parametry świetlne w różnych punktach i ich zgodność z normami. 

Nowoczesne programy pozwalają na obliczenia wartości światła dziennego, mają zawarte modele 3D do planowania otoczenia, umożliwiają współpracę z innym oprogramowaniem CAD oraz zawierają pakiety norm dla różnych obszarów.

Programy CAD projektowania oświetlenia pozwalają również na wykonanie dokumentacji rysunkowej i tekstowej.

### Źródła

[1] Robert Leśniak - *Opracowanie do wykładu Komputerowe systemy CAD projektowania w elektroenergetyce*

[2] Materiały z wykładu *Komputerowe systemy CAD projektowania w elektroenergetyce*

[3] Opracowanie do wykładu Komputerowe systemy CAD projektowania w elektroenergetyce z poprzedniego rocznika studiów **

[4] [https://www.ciop.pl/CIOPPortalWAR/appmanager/ciop/pl?_nfpb=true&_pageLabel=P30001831335539182278&html_tresc_root_id=23200&html_tresc_id=23217&html_klucz=19558&html_klucz_spis=#3](https://www.ciop.pl/CIOPPortalWAR/appmanager/ciop/pl?_nfpb=true&_pageLabel=P30001831335539182278&html_tresc_root_id=23200&html_tresc_id=23217&html_klucz=19558&html_klucz_spis=#3)

[5] [http://nop.ciop.pl/m6-7/m6-7_3.htm](http://nop.ciop.pl/m6-7/m6-7_3.htm)

[6] [https://ledline.pl/strony/olsnienie-przykre-oraz-ocena-ugr](https://ledline.pl/strony/olsnienie-przykre-oraz-ocena-ugr)

### c) zasady projektowania rozdzielnic elektrycznych niskiego napięcia. Charakterystyka programów CAD do projektowania rozdzielnic

### Zasady projektowania rozdzielnic elektrycznych niskiego napięcia

Projektując rozdzielnice elektryczne niskiego napięcia, należy mieć na uwadze takie czynniki jak bezpieczeństwo obsługi, wygodę eksploatacji (łatwe wykonywanie wszelkiego rodzaju łączeń), łatwy montaż i eksploatację, dużą niezawodność, możliwość rozbudowy oraz niewielki koszt i małe gabaryty.

Projektując rozdzielnice trzeba mieć już gotowy zestaw danych aparatów potrzebnych do rozdziału energii w miejscu jej zastosowania. Stąd, projektowanie rozdzielnic niskiego napięcia nie zawsze może być wykonywane w oderwaniu od projektowania instalacji elektrycznych.

### Charakterystyka programów CAD do projektowania rozdzielnic

Programami do projektowania rozdzielnic są m.in. XL PRO 2 lub SBC. 

Korzystanie z programu XL PRO 2 sprowadza się do trzech etapów:

1. **Konfiguracja rozdzielnicy**. 
    
    Służą do tego moduły Zestawienie, Układ i Schemat. Zestawienie pozwala na dobór aparatów bez rozmieszczenia ich w rozdzielnicy. Moduł Układ pozwala na umiejscowienie aparatów. Moduł Schemat pozwala natomiast na wizualizację schematu elektrycznego rozdzielnicy. 
    
    W skrócie, wybiera się aparaty, ich rozmieszczenie oraz układy połączeń.
    
2. **Dobór rozdzielnicy**
    
    Na podstawie dobranych aparatów, wybiera się obudowę rozdzielnicy spośród opcji proponowanych przez oprogramowanie. Można także wybierać niektóre akcesoria, takie jak drzwiczki, osłony itp. Moduł ten dobiera także akcesoria montażowe i uzupełnia o nie listę materiałów.
    
3. **Wizualizacja**
    
    Moduł Widok umożliwia sprawdzenie końcowego wyglądu rozdzielnicy w formie wizualizacji. Na tym etapie można także dodać różnego rodzaju akcesoria takie jak zamek do drzwi, etc. Można tu również modyfikować rozmieszczenie i sposób montażu aparatów. 
    
4. **Kosztorysowanie**
    
    Na tym etapie, korzystając z listy urządzeń i cennika Legrand, można wykonać kosztorys zaprojektowanej rozdzielnicy.
    
5. **Wydruki**
    
    Na ostatnim etapie projektowania rozdzielnicy można wykonać listę dokumentów takich jak widoki, schemat elektryczny, kosztorys czy lista materiałów - i łatwo te dokumenty wyeksportować. 
    

### Źródła

[1] Robert Leśniak - *Opracowanie do wykładu Komputerowe systemy CAD projektowania w elektroenergetyce*

[2] Opracowanie do wykładu Komputerowe systemy CAD projektowania w elektroenergetyce z poprzedniego rocznika studiów **

### d) zasady tworzenia dokumentacji projektowej. Charakterystyka programów typu CAD do tworzenia dokumentacji projektowej

### **Zasady tworzenia dokumentacji projektowej**

Podstawową koncepcją tworzenia dokumentacji projektowej jest wieloetapowe podejście, przy czym poszczególne etapy różnią się od siebie celem i poziomem szczegółowości. Etapami opracowywania dokumentacji projektowej są:

1. **Koncepcja projektowa**
    
    Etap ten nie zawsze jest konieczny. Rozpoznaje się tu stan sieci i urządzeń elektroenergetycznych na terenie projektowanej inwestycji, przygotowuje wstępne zestawienie odbiorników energii i bilansu mocy i energii zapotrzebowanej, a przy tym opracowuje koncepcję rozwiązania podstawowych instalacji wewnątrz i na zewnątrz obiektu, sposobu zasilania budynku oraz plany zewnętrznych linii i ich powiązania z istniejącymi. Określa się też lokalizację stacji elektroenergetycznych.
    
2. **Program funkcjonalno-użytkowy**
    
    Na tym etapie ustala się koszty prac projektowych i robót budowlanych i przygotowuje oferty. Przyjmuje się tu zakładane funkcjonalności w obiekcie. Etap ten to wstęp do opracowania projektu budowlanego, nie jest więc etapem wiążącym i może zajść potrzeba korekcji ustaleń. 
    
3. **Projekt budowlany**
    
    Projekt budowlany to opracowanie planów inwestycji budowlanej, wymagane aby uzyskać pozwolenie na budowę. Układ i zawartość projektów budowlanych są regulowane przez prawo budowlane. 
    
    Projekt budowlany musi uwzględniać wytyczne miejscowego planu zagospodarowania przestrzennego, obowiązujących warunków zabudowy oraz wymogi urzędowe. Dokumentacja na tym etapie powinna dzielić się na projekt zagospodarowania terenu oraz projekt architektoniczno-budowlany. 
    
    **Projekt architektoniczno-budowlany** powinien zawierać rozwiązania instalacji elektrycznych, teletechnicznych oraz odgromowych, a także sposób ich powiązania z istniejącymi sieciami. Powinny się także znaleźć przyjęte założenia wstępne oraz wyniki obliczeń i uzasadnienie doboru urządzeń.
    
    Oprócz tego, w projekcie architektoniczno-budowlanym powinna znaleźć się charakterystyka energetyczna obiektu (bilans mocy, etc.), charakterystyka ekologiczna instalacji i urządzeń (wszelkiego rodzaju emisje) oraz warunki ochrony przeciwpożarowej.
    
4. **Projekt wykonawczy**
    
    Projekt wykonawczy zawiera szczegółowe rozwiązania projektowe z podziałem na branże. musi zawierać wszystkie opisowa i rysunkowe elementy niezbędne do realizacji inwestycji, takie jak schematy instalacji elektrycznych, rzuty i przekroje obiektu, schematy i rysunki montażowe, dane techniczne urządzeń, wykaz materiałów, aparatów i urządzeń, wskazówki dot. eksploatacji, koniecznych zabiegów konserwacyjnych i ich terminów oraz kryteria badań tych elementów.
    
    Projekt wykonawczy jest niezbędny dla oceny prawidłowości wykonania robót w zakresie zgodności z projektem wykonawczym oraz osiągniętych parametrów i wyników pomiarów na etapie rozruchu. Jest on również częścią dokumentacji która powinna zawierać wielkość zużycia materiałów i ogólnie kosztorysy.
    
5. **Rysunki warsztatowe**
    
    Rysunki warsztatowe obejmują wszelkiego rodzaju rysunki, wykazy i zestawienia, wraz ze szczegółami połączeń między elementami. Są niezbędne do prefabrykacji elementów wykorzystywanych na inwestycji. Rysunki warsztatowe zawierają nie tylko wymiary i listę materiałów, lecz również technologię wykonania poszczególnych elementów konstrukcji.
    
    Rysunki warsztatowe są wykonywane przez Wykonawcę, Podwykonawcę, Producenta lub Dystrybutora. 
    

### Charakterystyka programów typu CAD do tworzenia dokumentacji projektowej

De facto każdy branżowy program CAD typu Simaris, Dialux, Relux, etc. jest również programem do tworzenia dokumentacji projektowej. Na podstawie zadanych parametrów i dobranych aparatów, urządzeń itp. sporządzane są projekty poszczególnych instalacji wraz z kosztorysami. Mogą to być dokumenty tworzone zasadniczo na każdym etapie projektu. 

Wspomniane programy projektowania instalacji elektrycznych, oświetleniowych i rozdzielnic mają możliwości eksportowania dokumentacji tekstowej i rysunkowej oraz listy materiałów. 

### Źródła

[1] Robert Leśniak - *Opracowanie do wykładu Komputerowe systemy CAD projektowania w elektroenergetyce*

[2] Materiały z wykładu *Komputerowe systemy CAD projektowania w elektroenergetyce*

[3] Opracowanie do wykładu Komputerowe systemy CAD projektowania w elektroenergetyce z poprzedniego rocznika studiów **