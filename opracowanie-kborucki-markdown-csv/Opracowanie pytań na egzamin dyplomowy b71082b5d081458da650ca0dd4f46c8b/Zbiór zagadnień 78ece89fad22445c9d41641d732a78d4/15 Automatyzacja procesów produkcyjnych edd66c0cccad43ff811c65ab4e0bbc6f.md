# 15. Automatyzacja procesów produkcyjnych

Status: Zrobione

### a) struktury przemysłowych systemów sterowania

Wśród struktur przemysłowych systemów sterowania można wymienić:

- **sterowanie lokalne** - jest to indywidualne sterowanie procesem, w którym wykorzystuje się sterownik PLC na miejscu wykonywania procesu. Do wizualizacji można wykorzystać lokalne panele HMI.
- **sterowanie zintegrowane (rozproszone)** - sterowanie z jednego miejsca wielu urządzeń procesu przemysłowego, czyli jeden system obsługuje całą linię produkcyjną
- **sterowanie zdalne** - sterowanie stosowane w przypadku istnienia większych odległości między urządzeniem sterującym i sterowanym

![Untitled](15%20Automatyzacja%20proceso%CC%81w%20produkcyjnych%20edd66c0cccad43ff811c65ab4e0bbc6f/Untitled.png)

Systemy sterowania lokalnego realizuje się w oparciu o pojedyncze sterowniki PLC.

Sterowanie rozproszone opiera się już na systemach typu SCADA i DCS:

- **SCADA** - *Supervisory Control And Data Acquisition **-*** system sterowania nadrzędnego i zbierania danych, który dopełnia i rozszerza możliwości sterowników, realizując w warstwie sterowania nadrzędnego takie funkcje jak komunikacja z urządzeniami obiektowymi (sterowniki, regulatory), zbieranie i przetwarzanie zmiennych procesowych i ich archiwizacji, tworzenie interfejsu operatora wraz z wizualizacją wartości mierzonych czy generowanie raportów, sygnałów alarmowych czy diagnostyki zasobów, komunikacji i redundancji
- **DCS** - *Distributed Control System* - system tego typu odpowiada za sterowanie i wizualizację procesu przemysłowego w oparciu o wspólną bazę danych (tagów) do sterowania i wizualizacji (w PLC i SCADA bazy te są rozdzielone); DCS jest przy tym bardzo skalowalny

Systemy typu DCS są dedykowane dla określonych obiektów sterowania (obiektów przemysłowych), opiera się o zaawansowane algorytmy takie jak sieci neuronowe, a przy tym ma wspólną bazę danych wizualizacji i sterowania, komponenty jednego producenta, dużą niezawodność i wymaganie co do nadzoru procesu.

SCADA dla odmiany to system elastyczny, uniwersalny i optymalizowany przede wszystkim dla algorytmów sterowania dyskretnego. Dopuszcza stosowanie urządzeń różnych producentów, przy czym PLC i SCADA mogą działać niezależnie od siebie. 

### Źródła

[1] Materiały z wykładu *Automatyka procesów produkcyjnych*

[2] Materiały z wykładu *Automatyka procesów produkcyjnych - zagadnienia wybrane*

### b) sterowniki PLC - budowa, zasada działania i języki programowania

### **Budowa sterowników PLC**

Generalnie, wyróżnia się sterowniki **kompaktowe** oraz **modułowe**. Kompaktowe mają wszystkie elementy wymagane do pracy w jednej obudowie. Modułowe mają funkcjonalność taką, jaką moduły do nich dobrane.

Ogólnie, w podstawowej wersji sterownik PLC składa się z: 

- **zasilacza** na ogół 24 V lub 110VAC / 230 VAC o dużej sprawności
- **jednostki centralnej CPU:** mikroprocesor z systemem operacyjnym, pamięcią, programem, etc., co łącznie służy do wykonywania rozkazów. Mikroprocesory na ogół 8-, 16- i 32-bitowe. Pamięci RAM i EEPROM lub FLASH EPROM.
- **modułu wejść cyfrowych** - przetworniki C/C do obsługi sygnałów dyskretnych
- **modułu wyjść cyfrowych** - przetworniki C/C do zadawania sygnałów dyskretnych
- **modułu wejść analogowych** - przetworniki A/C do obsługi sygnałów ciągłych
- **modułu wyjść analogowych** - przetworniki C/A do zadawania sygnałów ciągłych
- **modułów komunikacyjnych**: interfejsy służące do komunikacji z innymi urządzeniami systemu sterowania w sieci przemysłowej, np. czujniki, urządzenia HMI, inne sterowniki, komputery, etc.
- **modułów specjalnych** do rozszerzenia możliwości urządzenia - np. moduły do pomiaru temperatury, szybkich liczników (np. 1MHz), generatorów PWM, pozycjonowania osi, precyzyjnych wejść analogowych, etc.

![Untitled](15%20Automatyzacja%20proceso%CC%81w%20produkcyjnych%20edd66c0cccad43ff811c65ab4e0bbc6f/Untitled%201.png)

### Zasada działania

Sterownik PLC działa zgodnie z programem zapisanym w pamięci. Taki program to ciąg rozkazów logicznych wykonywanych sekwencyjnie, jeden po drugim. Pojedynczy rozkaz to najmniejsza część programu sterującego i składa się z operacji określającej rodzaj wykonywanej funkcji oraz argumentów określających sygnały wejściowe i wyjściowe sterownika. Można tu wykonywać operacje logiczne i arytmetyczne, odczyt i zapis danych do i z pamięci.

Sterownik pracuje w cyklach, przy czym każdy z nich wygląda tak jak poprzedni:

- **inicjalizacja**: sprawdzenie poprawności obwodów i konfiguracji sprzętowej
- **odczyt sygnałów wejściowych**: sprawdzenie specjalnego obszaru pamięci pod kątem nowych danych
- **wykonanie programu użytkownika**: przetwarzanie instrukcji programu sterującego i zapisanie nowych stanów wyjść do specjalnej części pamięci
- **zapis sygnałów wyjściowych sterownika:** pobranie z pamięci stanów wyjść i ich aktualizacja
- **obsługa komunikacji:** jeżeli sterownik komunikuje się sieciowo z czymś z zewnątrz, to właśnie w tym etapie pracy
- **autodiagnostyka**: sprawdzenie poprawności działania sterownika, np. poprzez sprawdzenie wartości napięcia zasilania, stanu baterii pamięci itp.

![Untitled](15%20Automatyzacja%20proceso%CC%81w%20produkcyjnych%20edd66c0cccad43ff811c65ab4e0bbc6f/Untitled%202.png)

### Języki programowania

Języki programowania sterowników PLC dzieli się na graficzne i tekstowe. 

Wśród języków tekstowych można wymienić: 

- **IL:** *Instruction List* - język niskopoziomowy składający się z zestawu instrukcji takich jak operacje logiczne i arytmetyczne, funkcje czasowe i licznikowe, operacje porównania i transferu danych. Jest to język podobny do asemblera, bardzo wydajny.
- **ST:** *Structured Text -* język wysokopoziomowy, podobny do Basica czy Pascala. Pozwala na używanie wyrażeń i instrukcji takich jak IF ELSE, zamiast operatorów zorientowanych maszynowo jak OR XOR.

Wśród języków graficznych można wymienić:

- **FBD**: *Functional Block Diagram* - język graficzny wzorowany na schematach ideowych stosowanych w elektronice, gdzie pokazany jest przepływ sygnałów i topologia połączeń układów scalonych. Charakterystyczne elementy języka to bloki i elementy sterujące (łączniki), oparte o przepływ sygnałów.
- **LD:** *Ladder Diagram* - język graficzny, który opiera się na symbolach elektrycznych układów sterowania w technice stykowo-przekaźnikowej. Podstawowymi elementami są styki, przedstawiające wartości logiczne sygnałów wejściowych i zmiennych boolowskich oraz dwustanowe wyjścia, odzwierciedlające cewki przekaźnika. Wykorzystuje się tu też bloki funkcyjne takie jak liczniki, komparatory, etc.

### Źródła

[1] M. Pawlak - *Sterowniki Programowalne*

### c) systemy komunikacyjne w automatyce przemysłowej

### Ogólny podział

**Sieci komunikacyjne** można podzielić **ze względu na rozmiar** na:

- **sieci lokalne (LAN)**, o zasięgu kilku kilometrów
- **sieci metropolitalne (MAN)**, obejmujące obszar od kilkunastu do kilkudziesięciu kilometrów, na ogół zespół miejski
- **sieci rozległe (WAN)**, obejmujące swym zasięgiem region, kraj lub cały świat.

Wśród **topologii sieci** można wyróżnić:

- magistralowe
- pierścieniowe
- osiowe
- gwiaździste
- nieregularne

![Untitled](15%20Automatyzacja%20proceso%CC%81w%20produkcyjnych%20edd66c0cccad43ff811c65ab4e0bbc6f/Untitled%203.png)

**Sieci przemysłowe** to specyficzna grupa sieci lokalnych, w których postawiony jest nacisk na wysoką **niezawodność** i **przewidywalność** przebiegu komunikacji. W takich sieciach nacisk nie jest stawiany na przepustowość łącz, lecz na terminowość przekazu informacji - ze względu na konieczność szybkiego reagowania układów sterowania na zmiany odczytów czujników itp. 

Połączenie ze sobą kilku standardowych sieci przemysłowych może doprowadzić do powstania sieci rozległej o nieregularnej strukturze. 

### Warstwy sieci

Sieci komunikacyjne można dzielić na warstwy zgodnie z modelem warstwowym Fieldbus. W przypadku sieci przemysłowych, wygodnym podziałem jest podział analogiczny do sieci TCP/IP lub ISO/OSI, w którym wyróżnia się trzy warstwy:

- **poziom czujników i elementów wykonawczych [Sensor / Actuator Level]** - należą do niego wszelkiego rodzaju czujniki (przyciski, przełączniki, czujniki indukcyjne, pojemnościowe, enkodery, etc.) oraz elementy wykonawcze (zawory, lampki, generatory akustyczne, proste napędy). Komunikację optymalizuje się pod kątem bitowego przesyłu informacji (zera i jedynki).
- **poziom sterowania [Device Level]** - należą do niego bardziej skomplikowane czujniki i elementy wykonawcze oraz moduły o 8 lub więcej modułach I/O, np. skanery i czytniki kodów, przetworniki ciśnienia, temperatury, przepływu, napędy z reg. prędkości stacje operatorskie. Przepływ informacji zachodzi tu domyślnie w bajtach (1 bajt = 8 bitów).
- **poziom zarządzania [Field Level]** - urządzenia na tym poziomie to wyspy urządzeń automatyki, na tym poziomie też łączy się je między sobą i podłącza do większych jednostek. Wymiana danych idzie w sposób blokowych, czyli całych pakietach (32- lub 64- bajty); na tym poziomie często zachodzi przesył danych między poziomem sterowania a poziomami nadrzędnymi, jak np. ERP, MIS czy sieciami biurowymi.

![Model warstwowy sieci typu Fieldbus](15%20Automatyzacja%20proceso%CC%81w%20produkcyjnych%20edd66c0cccad43ff811c65ab4e0bbc6f/Untitled%204.png)

Model warstwowy sieci typu Fieldbus

### Protokoły

Każdy poziom sieci charakteryzuje się swoimi własnymi protokołami, podobnie jak w sieciach internetowych. Jako przykłady można wymienić tu kolejno:

- **poziom czujników i elementów wykonawczych:** Seriplex, AS-Interface
- **poziom sterowania:** CANOpen, DeviceNet, Device WorldFIP, InterBus, PRofiBus, SDS, Modbus
- **poziom zarządzania:** ControlNet, FF (Fieldbus), P-Net, ProfiNet Profibus FMS, WorldFIP.

Protokoły komunikacyjne są określone normą IEC61158 i przypisane dla konkretnych warstw sieci w modelu OSI. 

### Źródła

[1] Materiały z wykładu *Automatyka procesów produkcyjnych*

[2] Materiały z wykładu *Automatyka procesów produkcyjnych - zagadnienia wybrane*

### d) analogowe i cyfrowe interfejsy w przemysłowych systemach pomiarowo-sterujących

### Podstawowe definicje

**Interfejs** - urządzenie pozwalające na połączenie ze sobą dwóch lub więcej urządzeń, które bez niego nie mogłyby ze sobą współpracować. Interfejsem może być gniazdo lub kabel, może być też inne urządzenie. 

Gniazdo na płycie głównej komputera jest interfejsem, w który wkłada się np. kartę graficzną, ale i sama karta jest również interfejsem umożliwiającym współpracę monitora z resztą systemu komputerowego. Idąc dalej, monitor jako całe urządzenie to także interfejs, bo posiada swój własny interfejs w postaci ekranu, który połączony jest bezprzewodowo z patrzącym na niego użytkownikiem posiadającym interfejs w postaci narządu wzroku. Potencjometry sterujące monitorem, a obecnie coraz częściej panel sterujący z przyciskami, to drugi, obok ekranu, interfejs monitora.

**System pomiarowo-sterujący -** zestaw współpracujących urządzeń pomiarowych i sterujących współpracujących ze sobą w celu zbierania, porównywania, rejestracji i przetwarzania sygnałów o mierzonych wielkościach fizycznych w celu określenia stanu obiektu i zmiany sterowanych wielkości. 

W celu standaryzacji parametrów wejściowych i wyjściowych aparatury, stosuje się standardowe sygnały pomiarowe i kontrolne - analogowe lub cyfrowe. Wśród sygnałów analogowych można wymienić **sygnały napięciowe** (0-10 V, +- 15V, +- 5V) oraz **sygnały prądowe** (0-20 mA, 4-20 mA). Na ogół sygnały prądowe stosowane są chętniej, ze względu na mniejsze zakłócenia. 

**Interfejsy szeregowe**

Wśród interfejsów szeregowych można wymienić takie interfejsy jak RS-232C, RS-449, RS-422A, RS-423A, RS-530, RS-485, HART, IEC 1158-2, PROFIBUS, MicroLAN, CAN. 

**Interfejsy równoległe**

Interfejsy równoległe oferują większą prędkość transmisji niż interfejsy szeregowe. Dane są przesyłane w wielobitowych słowach, bez konieczności stosowania podziału strumienia bitów na słowa z dodatkowymi funkcjami kontrolnymi i korekcyjnymi. 

Wśród interfejsów równoległych można wymienić: Centronics (IEEE 1284), IEC-625.

### Interfejsy analogowe

Wśród interfejsów analogowych trudno wymienić jakieś rozsądne opcje. Na ogół analogowe sygnały są przetwarzane przez odpowiednie przetworniki na sygnały cyfrowe i poddawane obróbce w takiej formie, stąd interfejsy analogowe są często raczej czujnikami i fizycznymi elementami układu.

Do interfejsów analogowych systemów przemysłowych można zaliczyć również te elementy, które odpowiadają za interakcje na linii użytkownik-urządzenie, czyli klawiatury, ekrany, przyciski, pokrętła itp. 

### Interfejsy cyfrowe

Interfejsy cyfrowe służą najczęściej do komunikacji i przesyłania danych między urządzeniami. 

Interfejsy te można dzielić na **synchroniczne** oraz **asynchroniczne**. W przypadku **synchronicznej komunikacji**, poszczególne bity czy słowa wysyłane są w **równych przedziałach czasu**, co może sprawić że informacje zostaną utracone przy desynchronizacji. W **transmisji asynchronicznej**, dane są wysyłane w **nierównych odstępach czasu**, przy czym pojawiają się **bloki początku i końca transmisji**. Jest to częściej stosowana metoda transmisji.

Interfejsy cyfrowe można też dzielić na **szeregowe** i **równoległe**. Transmisja szeregowa to przesyłanie danych bit po bicie zgodnie z taktami zegara synchronizującego. Transmisja równoległa to przesyłanie ciągu słów (długość słowa zależnie od standardu) kolejno słowo po słowie synchronicznie - bity są wysyłane równolegle. 

Interfejsy cyfrowe w systemach przemysłowych wykorzystuje się głównie do przesyłu informacji między urządzeniami w ramach różnych sieci przemysłowych. 

### Transmisja bezprzewodowa

Do transmisji na małe odległości można stosować również inne interfejsy, takie jak Bluetooth, IRDA czy ZigBee. Na większe odległości dane przesyła się z zastosowaniem interfejsów takich jak WLAN (systemy radiowe), GSM/GPRS czy inne sieci komórkowe takie jak EDGE, HSDPA, LTE i 5G. 

### Wybrane interfejsy i protokoły

**RS-232C**

Interfejs szeregowy RS-232C to zdefiniowany sposób połączenia dwóch urządzeń końcowych. Urządzenia są połączone z linią telefoniczną poprzez modem. 

**MicroLAN**

W tym systemie możliwa jest komunikacja między jednym układem master (komputer, mikrokontroler) i wieloma elementami slave (czujniki itp.). System MicroLAN składa się z układu nadrzędnego, oprogramowania, połączeń i zespołu elementów typu slave (w tym przetworniki, czujniki, układy pamięci). Linia MicroLAN jest sterowana przez interfejs RS-232C. 

**PROFIBUS**

PROFIBUS (Process Field Bus) to rodzina lokalnych sieci przemysłowych w trzech wersjach, zależnie od warstwy sterowania. W standardzie PROFIBUS DP lub FMS jako warstwę fizyczną stosuje się sieć RS-485. Długość kabla (100-1200m) zależy od szybkości transmisji (9,6 - 1500 kbit/s). 

**HART**

Hart to protokół komunikacyjny oparty o standard 4-20 mA. Służy głównie do zmiany nastaw i diagnostyki. W protokole tym jeden cykl 1200 Hz oznacza binarne 1, dwa cykle 2200 Hz - binarne 0. Na sygnał analogowy prądu nakładany jest sygnał cyfrowy komunikacyjny i tak złożona informacja jest przesyłana dalej. Sygnały są tu analogowe. 

![Untitled](15%20Automatyzacja%20proceso%CC%81w%20produkcyjnych%20edd66c0cccad43ff811c65ab4e0bbc6f/Untitled%205.png)

**AS-Interface**

Actuator Sensor Interface to otwarty standard łączący punkty binarne. Służy głównie do kontroli czujników, elementów wykonawczych i urządzeń wejściowo-wyjściowych. Dystans działania takiej sieci ASI to ok. 300 m. Jednym kablem 2-żyłowym dostarczane jest zasilanie oraz transmisja danych. 

**CAN**

*Controlled Area Network* to sieć o różnych zastosowaniach, zależnie od standardu. Sieci CAN występują w różnych strukturach (linearna, gwiaździsta, pierścieniowa) i służą do transmisji sygnałów między urządzeniami. Sterowniki muszą posiadać blok przetwarzający przesyłane informacje (kontroler CAN) oraz układ nadawczo-odbiorczy. Odpowiadają one za nadawanie danym konkretnej postaci i komunikacji z magistralą. Magistrala to dwa przewody (high i low) złączone w skrętkę. Bity są przesyłane tak, by były symetryczne względem siebie. 

Elementy podłączone do magistrali CAN nazywa się modułami lub węzłami. Cechą CAN są duża szybkość transmisji danych uzależniona od długości magistrali, duża odporność na zakłócenia oraz elastyczność systemu co do liczby podłączonych elementów. CAN wymaga użycia czujników wyposażonych w wyjścia cyfrowe. 

**EtherCAT**

W tym interfejsie sieci komunikacyjnej węzeł master wysyła ramkę ethernetową do wszystkich slave’ów. Ramka jest interpretowana przez każdy odbiornik pod kątem tego, czy jakieś dane zostały wysłane do niego. Jeżeli tak, fragment ramki jest odczytywany i przesyłana jest informacja zwrotna potwierdzająca odbiór. 

Sieci EtherCAT pracują w logicznej topologii pierścienia

**Centronics (IEEE-1284)**

Interfejs Centronics służy na ogół do połączenia drukarek z komputerami i przesyłania danych w obydwu kierunkach. Jest on jednak używany też w urządzeniach pomiarowych (oscyloskopy, analizatory widma) i pozwala na wysyłanie danych do drukarki bez komputera. 

**DeviceNet**

Ten protokół jest oparty o technologię CAN. Komunikuje on ze sobą urządzenia przemysłowe takie jak wyłączniki krańcowe, czujniki fotoelektryczne, zawory wielodrożne, rozruszniki silników, przyciski sterujące, czytniki kodów kreskowych, przemienniki częstotliwości, panele operatorskie itp. 

DeviceNET wymaga niskiej szerokości pasma, bo ma mały format ramki, co jest zaletą. Wymaga dzięki temu mniejszego procesora.

**Ethernet/IP** 

Protokół ten opiera się o dwa rodzaje wiadomości: diagnostyczne i konfiguracyjne przesyłane protokołem TCP, oraz dane przesyłane w czasie rzeczywistym, UDP. Ethernet/IP pozwala na priorytetyzację przesyłanych pakietów i synchronizację zegarów czasu rzeczywistego w rozproszonych systemach. Do synchronizacji wykorzystywany jest protokół PTP, precyzyjnie synchronizujący czas do najważniejszego zegara w sieci. 

### Źródła

[1] Materiały z wykładu *Automatyka procesów produkcyjnych*

[2] Materiały z wykładu *Automatyka procesów produkcyjnych - zagadnienia wybrane*

[3] Robert Czabanowski - *Sensory i systemy pomiarowe*

[4] [https://pl.wikipedia.org/wiki/Interfejs_(urządzenie)](https://pl.wikipedia.org/wiki/Interfejs_(urz%C4%85dzenie))

[5] M. Pawlak - *Sterowniki Programowalne*