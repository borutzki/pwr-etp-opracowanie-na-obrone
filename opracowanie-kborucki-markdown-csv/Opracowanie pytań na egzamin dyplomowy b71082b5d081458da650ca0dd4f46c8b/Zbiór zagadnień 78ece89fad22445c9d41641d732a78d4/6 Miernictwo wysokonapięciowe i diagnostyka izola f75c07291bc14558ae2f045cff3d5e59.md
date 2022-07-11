# 6. Miernictwo wysokonapięciowe i diagnostyka izolacji

Status: Zrobione

### a) dzielniki wysokiego napięcia przemiennego - budowa, dobór elementów, niepewność pomiarowa

**Budowa dzielnika**

W najprostszej wersji, dzielnik wysokiego napięcia przemiennego składa się z dwóch kondensatorów - jest to dzielnik pojemnościowy. Pojemności kondensatorów określają przekładnię dzielników. 

![Untitled](6%20Miernictwo%20wysokonapie%CC%A8ciowe%20i%20diagnostyka%20izola%20f75c07291bc14558ae2f045cff3d5e59/Untitled.png)

Przekładnię dzielnika jak na powyższym obrazku można przedstawić zależnością $\vartheta=\frac{C_1+C_2}{C_1}=\frac{U}{U_2}$. 

Po uwzględnieniu pojemności doziemnej, schemat zastępczy dzielnika przedstawia się następująco:

![Untitled](6%20Miernictwo%20wysokonapie%CC%A8ciowe%20i%20diagnostyka%20izola%20f75c07291bc14558ae2f045cff3d5e59/Untitled%201.png)

**Dobór elementów dzielnika**

Kondensator C2 jest kondensatorem wzorcowym. Jego pojemność musi być możliwie mała, żeby reaktancja była duża - co pozwala na uzyskanie dużej wartości przekładni. W celu uzyskania małej pojemności, stosuje się duże odstępy izolacyjne między elektrodami - co zwiększa jednocześnie wytrzymałość układu.

Zgodnie ze schematem zastępczym, wypadkowa przekładnia zależy od stosunku pojemności doziemnej do pojemności kondensatora strony wysokonapięciowej. Stąd, duża pojemność tego kondensatora ogranicza wpływ pojemności doziemnej, powoduje jednak zmniejszenie przekładni.

**Niepewność pomiarowa**

Główną przyczyną niepewności pomiarowej przy korzystaniu z dzielnika napięcia przemiennego jest pojemność doziemna układu. Powoduje ona wprowadzenie niedokładności przekładni takiego dzielnika. Z tego powodu, przekładnię dzielnika pojemnościowego wyznacza się drogą pomiarową, nie obliczeniową.

![Untitled](6%20Miernictwo%20wysokonapie%CC%A8ciowe%20i%20diagnostyka%20izola%20f75c07291bc14558ae2f045cff3d5e59/Untitled%202.png)

Niepewność pomiaru wartości skutecznej przy wykorzystaniu dzielnika napięcia określa zależność $\delta \approx\frac{1}{2\omega^2 C^2_2 R^2}$. Oznacza to, że dokładniejsze wartości pomiarów możemy uzyskać  przy pomiarach napięć o wyższych częstotliwościach, wykorzystując kondensatory wzorcowe o większych pojemnościach oraz zwiększając rezystancję odbiornika - czyli np. impedancję układu pomiarowego. 

### Najważniejsze punkty

- dzielnik napięcia przemiennego to dwa kondensatory: wysokonapięciowy oraz wzorcowy
- kondensator wysokonapięciowy: mała pojemność to mała przekładnia, ale jednocześnie mniejszy wpływ pojemności doziemnej
- kondensator wzorcowy: wymagana mała pojemność w celu uzyskania dużej przekładni
- błąd pomiarowy bierze się z częstotliwości, pojemności C2 i oporu wewnętrznego strony niskiego napięcia - im wielkości te większe, tym niepewność mniejsza

### **Źródło**

[1] Materiały z wykładu prof. Wieczorka

### b) dzielniki napięć udarowych - budowa, dobór elementów, współpraca z aparaturą pomiarowo-rejestrującą

**Budowa dzielnika**

Dzielniki napięć udarowych buduje się jako rezystancyjne, pojemnościowe lub pojemnościowo-rezystancyjne. Najważniejsze jest, by charaktery impedancji strony wysokiej i strony niskiej były identyczne. 

![Untitled](6%20Miernictwo%20wysokonapie%CC%A8ciowe%20i%20diagnostyka%20izola%20f75c07291bc14558ae2f045cff3d5e59/Untitled%203.png)

W przypadku dzielników napięć szczytowych, istotnymi parametrami są czas odpowiedzi na impuls prostokątny oraz częstotliwość rezonansowa dzielnika dla odpowiedzi periodycznej. 

**Dobór elementów dzielnika**

W przypadku dzielników napięć udarowych, należy zadbać przede wszystkim o to, żeby przekładnia pozostawała stała dla szerokiego zakresu częstotliwości napięć oraz dla szerokiego zakresu warunków pomiaru. 

Sprowadza się to do doboru takich elementów, które charakteryzują się bardzo małymi parametrami pasożytniczymi - czyli pojemność i indukcyjność w przypadku dzielnika rezystancyjnego. Układ z minimalną indukcyjnością charakteryzuje się najlepszą odpowiedzią - stała czasowa jest pomijalna. 

Indukcyjności można kompensować specjalnie wykonanymi rezystorami. Pojemności - stosując ekranowanie dzielnika. 

**Niepewność pomiarowa**

Jak już wspomniano wyżej, źródłem błędów pomiarowych w dzielnikach napięć udarowych są parametry pasożytnicze elementów dzielnika - pojemność i indukcyjność przy dzielnikach rezystancyjnych, indukcyjność przy dzielnikach pojemnościowych i pojemnościowo-rezystancyjnych. 

### **Najważniejsze punkty**

- dzielniki udarowe: R, C, lub RC
- niepewności pomiarowe biorą się z pasożytniczych parametrów R, L, C
- dobór elementów: odpowiednia konstrukcja, jak najniższe parametry pasożytnicze
- praca z aparaturą: przebieg udarowy trzeba zarejestrować żeby mieć o nim jakieś informacje, więc aparatura musi być odpowiednio szybka

### **Źródła:**

[1] Fleszyński - Miernictwo wysokonapięciowe i laboratorium wysokich napięć

[2] Materiały z wykładu prof. Wieczorka

### c) pomiary wyładowań niezupełnych w badaniach diagnostycznych izolacji wysokonapięciowej, model dielektryka z wtrąciną gazową, parametry wyładowań niezupełnych, metody elektryczne pomiaru, metody akustyczne pomiaru, lokalizacja wyładowań niezupełnych

**Pomiary wyładowań niezupełnych w badaniach diagnostycznych izolacji wysokonapięciowej**

Pomiary wyładowań niezupełnych są konieczne w badaniach diagnostycznych izolacji wysokonapięciowej, ponieważ dostarczają informacji o stanie badanej izolacji. Wyładowania niezupełne mogą znacząco skrócić żywotność izolacji, powodując degradację materiału izolacyjnego.  

O ile pomiary kąta stratności pozwalają na wyznaczenie progu jonizacji (napięcia początkowego wyładowań niezupełnych), o tyle pomiary wyładowań niezupełnych skupiają się na określeniu intensywności tych wyładowań.

Warto pamiętać, że wśród wyładowań niezupełnych można wyróżnić wyładowania ulotowe, powierzchniowe i wewnętrzne.

Celem diagnostycznym badań wyładowań niezupełnych jest ich detekcja, określenie intensywności, lokalizacji, rodzaju defektu izolacji oraz przybliżonego czasu życia izolacji. 

**Model dielektryka z wtrąciną gazową**

Do analizy zjawiska wyładowań niezupełnych w objętości izolacji wykorzystuje się model dielektryka z wnęką gazową. Można przyjąć, że pojemność C3 to pojemność otoczenia wtrąciny powietrznej, pojemność C2 - pojemność elementów izolacji pod i nad wtrąciną, natomiast pojemność C1 - pojemność samej wtrąciny.

![Untitled](6%20Miernictwo%20wysokonapie%CC%A8ciowe%20i%20diagnostyka%20izola%20f75c07291bc14558ae2f045cff3d5e59/Untitled%204.png)

Wyładowania niezupełne występują wtedy, gdy napięcie zasilające przekracza wartość napięcia krytycznego (wytrzymałości elektrycznej) wtrąciny. W tej sytuacji, można przyjąć, że następuje zwarcie wtrąciny - napięcie na niej spada do 0 i łuk gaśnie. Dalszy wzrost napięcia zasilającego - wzrost sinusoidy - powoduje ponowne zwiększenie napięcia na tej wtrącinie i ponowne pojawienie się wyładowania.  

**Parametry wyładowań niezupełnych**

Podstawowym parametrem wyładowań niezupełnych jest ładunek odpowiadający rzeczywistemu ładunkowi przepływającemu we wtrącinie podczas wyładowania. Jednak jego bezpośredni pomiar jest niemożliwy. Dlatego stosuje się układy pomiarowe, w których zamiast tego mierzona jest wartość ładunku przepływającego przez impedancję pomiarową przy wyładowaniu - czyli wartość ładunku, który dopływa do miejsca wyładowania. Ładunek przepływający przez impedancję układu pomiarowego powoduje wygenerowanie fali napięciowej.

Ładunek płynący do miejsca wyładowania nazywa się **ładunkiem pozornym**. Jest to podstawowa miara intensywności wyładowań niezupełnych. Ładunek pozorny nie jest równy co do wartości rzeczywistemu ładunkowi wyładowania - jest do niego proporcjonalny. 

Drugim podstawowym parametrem wyładowań niezupełnych jest **częstotliwość powtarzania impulsów wyładowań**. 

Na podstawie tych dwóch parametrów można wyznaczyć pozostałe parametry tzw. sumarycznej intensywności wyładowań, czyli średni prąd wyładowań niezupełnych, średni kwadrat ładunków wyładowań oraz moc wyładowań. 

Innymi parametrami są :

- **napięcie początkowe wyładowań** - najniższa wartość napięcia, przy której obserwuje się wyładowania za pomocą układu probierczego na którym napięcie przyłożone jest zwiększane
- **napięcie gaśnięcia** - najniższa wartość napięcia, przy której obserwuje się wyładowania za pomocą układu probierczego na którym napięcie przyłożone jest zmniejszane
- kąt fazowy pojedynczego impulsu
- ładunek maksymalny wyładowań

**Metody elektryczne pomiaru**

W pomiarach wyładowań niezupełnych, stosuje się układy w których mierzona jest wartość ładunku pozornego. Opisuje je schemat jak na rysunku poniżej: 

![Untitled](6%20Miernictwo%20wysokonapie%CC%A8ciowe%20i%20diagnostyka%20izola%20f75c07291bc14558ae2f045cff3d5e59/Untitled%205.png)

Oprócz powyższych, stosuje się także układy mostkowe. Układy do pomiarów wyładowań niezupełnych metodami elektrycznymi wymagają kalibracji, są przy tym podatne na różne źródła zakłóceń od aparatury, sieci itd. 

Oprócz układów do określenia ładunku pozornego, stosuje się również układy takie jak mostek Scheringa do określenia kąta stratności materiału izolacyjnego. Do pewnego poziomu napięcia tangens delta jest stały, powyżej pewnej wartości rośnie. Ta wartość to właśnie napięcie zapoczątkowania wyładowań niezupełnych. 

**Metody akustyczne pomiaru**

Wyładowania niezupełne są źródłem impulsów napięciowych i prądowych w obwodzie, można je więc badać metodami elektrycznymi. Jednak oprócz tego, są one źródłem impulsów mechanicznych: lokalnych zmian ciśnienia. Zmiana ciśnienia to de facto fala akustyczna. Dlatego do pomiaru wyładowań niezupełnych można wykorzystać bardzo czułe mikrofony. 

Energia fali akustycznej jest proporcjonalna do prądu wyładowania niezupełnego, co pozwala na określenie intensywności wyładowań. Zaletą tego typu pomiarów jest też odporność na zakłócenia wskutek działania promieniowania elektromagnetycznego. 

Do pomiarów akustycznych wykorzystuje się:

- hydrofony, przeznaczone do pomiarów ciśnienia w ośrodku ciekłym
- przetworniki stykowe, mikrofonowe, przeznaczone do pomiarów ciśnienia w ośrodku stałym
- przetworniki stykowe rezonansowe, służące do pomiaru przyspieszenia - akcelerometry.

Czyli de facto można tu stosować mikrofony lub czujniki ciśnienia. 

**Lokalizacja wyładowań niezupełnych**

Wyróżnia się dwie metody lokalizacji wyładowań niezupełnych:

- metoda triangulacyjna: polega na pomiarach czasów opóźnienia, z jakimi sygnały docierają do przetworników pomiarowych, rozmieszczonych w różnych punktach badanego urządzenia
- metoda największej głośności: polega na znalezieniu miejsca na obudowie urządzenia, w którym amplitudy sygnałów akustycznych są największe.

**Źródła**

[1] Materiały z wykładu prof. Wieczorka

[2] J. Fleszyński - *Miernictwo wysokonapięciowe i laboratorium wysokich napięć*

[3] J. Fleszyński - *Laboratorium wysokonapięciowe w dydaktyce i elektroenergetyce*

### d) badania diagnostyczne transformatorów elektroenergetycznych

Istnieje kilka badań diagnostycznych wykonywanych na transformatorach, które sumarycznie dają wiele informacji na temat stanu jego izolacji. Dla transformatorów na ogół prowadzi się dzienniki, w których zapisane są ich najważniejsze parametry w różnych punktach czasu - od badania do badania. Porównanie wartości tych wskaźników pozwala na ocenę aktualnego stanu izolacji względem stanu wyjściowego. 

**Indeks rezystancyjny**

Do układu izolacyjnego doprowadza się napięcie stałe, z narastającą stopniami wartością, na określony czas każdy stopień. Sprawdzana jest wartość prądu pojemnościowego w izolacji transformatora. Zmiany prądu w zależności od napięcia probierczego pokazują, w jakim stanie jest izolacja transformatora. Uzyskane wyniki porównuje się do wyników uzyskanych dla tego transformatora przy odbiorze.

Układ pomiarowy wygląda jak poniżej:

![Untitled](6%20Miernictwo%20wysokonapie%CC%A8ciowe%20i%20diagnostyka%20izola%20f75c07291bc14558ae2f045cff3d5e59/Untitled%206.png)

Przy czym wyniki pomiarów wyglądają jak poniżej:

![Untitled](6%20Miernictwo%20wysokonapie%CC%A8ciowe%20i%20diagnostyka%20izola%20f75c07291bc14558ae2f045cff3d5e59/Untitled%207.png)

**Pomiar napięcia powrotnego**

Jednym z badań stanu izolacji transformatora jest badanie napięcia powrotu, czyli przebiegu krzywej napięcia pojawiającego się na zaciskach uzwojenia po naładowaniu transformatora, a następnie rozładowaniu go. 

Wykorzystuje się tu układ jak poniżej:

![Untitled](6%20Miernictwo%20wysokonapie%CC%A8ciowe%20i%20diagnostyka%20izola%20f75c07291bc14558ae2f045cff3d5e59/Untitled%208.png)

Natomiast otrzymywane przebiegi mają kształt jak poniżej: 

![Untitled](6%20Miernictwo%20wysokonapie%CC%A8ciowe%20i%20diagnostyka%20izola%20f75c07291bc14558ae2f045cff3d5e59/Untitled%209.png)

Przy czym t_c to czas ładowania, natomiast t_d to czas rozładowania transformatora. Ponownie, uzyskane charakterystyki porównuje się z charakterystykami uzyskanymi dla nowo odebranego transformatora. 

**Diagnostyka wibroakustyczna**

Wśród metod diagnostyki transformatorów można wymienić również metodę wibroakustyczną, czyli analizę zmian poziomu drgań w czasie. Bada się tu stan rozruchu transformatora nieobciążonego. 

**Badania oleju**

Jednym z kluczowych badań diagnostycznych transformatora elektroenergetycznego jest analiza próbki oleju. Badania oleju są znormalizowane i mają na celu określenie wartości napięcia przebicia, współczynnika strat dielektrycznych oraz przebiegu jego zmian w funkcji temperatury, a także zbadanie rezystywności oleju i jej zmian w funkcji temperatury.

Oprócz parametrów elektrycznych, bada się także parametry fizykochemiczne oleju, takie jak napięcie powierzchniowe, liczba kwasowa, zawartość wody, PCB, furanów czy gazów rozpuszczonych w oleju. 

Wszystkie te wskaźniki oczywiście odnotowuje się w dzienniku maszyny i porównuje z wartościami uzyskanymi w ramach badań nowego transformatora. Każdy z tych parametrów pozwala ocenić, w jakim stanie jest olej transformatora, czyli realnie w jakim stanie jest transformator i czy może być dalej eksploatowany. 

**Pozostałe próby napięciowe**

Oprócz powyższych, podczas badań diagnostycznych prowadzi się także inne badania, takie jak współczynnik stratności izolacji transformatora i przepustu, pomiar pojemności transformatora i przepustu, pomiar wyładowań niezupełnych. 

**Źródła**

[1] Materiały z wykładu prof. Wieczorka

[2] [http://elektroonline.pl/a/6054,Badania-diagnostyczne-w-eksploatacji-transformatorow,,Energetyka](http://elektroonline.pl/a/6054,Badania-diagnostyczne-w-eksploatacji-transformatorow,,Energetyka) 

### e) próby napięciowe izolacji, układy probiercze

Wśród prób napięciowych izolacji urządzeń elektroenergetycznych można wymienić następujące:

### **Indeks rezystancyjny**

Indeks rezystancyjny to badania oporności izolacji urządzeń elektroenergetycznych, współczynnika absorpcji tej izolacji oraz prądu przewodnościowego.

Wykonuje się tu pomiary rezystancji po różnych czasach przyłożenia napięcia, często po 60 sekundach i 300 sekundach. Pomiary wykonuje się między fazami oraz do ziemi. Wskaźniki rezystancji izolacji zależą od wymiarów geometrycznych.

**Współczynnik absorpcji** jest de facto stosunkiem różnych wskaźników rezystancji, najczęściej R60/R15, czyli opisuje jak zmienia się rezystancja w czasie przyłożenia napięcia. Pomiary te wykonuje się przy napięciu 2,5 kV, przy wykorzystaniu megaomomierzy.

**Prąd przewodnościowy** jest mierzony przy wyższych napięciach - ostatni pomiar jest wykonywany przy dwukrotnej wartości napięcia znamionowego. Szybki wzrost wartości prądu przewodzenia podczas próby wskazuje na osłabienie stanu izolacji. 

Pomiary indeksów rezystancyjnych wykonuje się metodą schodkową: przykłada się na 10 minut coraz większe wartości napięcia. 

![Untitled](6%20Miernictwo%20wysokonapie%CC%A8ciowe%20i%20diagnostyka%20izola%20f75c07291bc14558ae2f045cff3d5e59/Untitled%2010.png)

### **Indeks pojemnościowy**

Wskaźnikami typu pojemnościowego są współczynnik stratności (tangens delta), wartość pojemności badanego obiektu i napięcie powrotne.

**Współczynnik stratności** zależy od poziomu zawilgocenia i zestarzenia izolacji oraz od poziomu wyładowań niezupełnych, a także od temperatury i poziomu napięcia. Współczynnik ten mierzy się korzystając z układu opartego o mostek Scheringa.

![Untitled](6%20Miernictwo%20wysokonapie%CC%A8ciowe%20i%20diagnostyka%20izola%20f75c07291bc14558ae2f045cff3d5e59/Untitled%2011.png)

Pomiary **pojemności izolacji** mogą wskazywać na zmianę stanu jej zawilgocenia - wnikanie wody wgłąb izolacji zwiększa jej przenikalność elektryczną, co pozwala dielektrykowi kumulować więcej ładunku. Powoduje to większe straty dielektryczne. 

Pomiary pojemności układu izolacyjnego wykonuje się przy częstotliwości napięcia 2 Hz i 50 Hz, a następnie oblicza się wskaźnik C2/C50. Wskaźnik ten maleje przy wzroście zawilgocenia.

Drugim wskaźnikiem jest pojemność wyznaczona przy różnych temperaturach: $80\degree C, 20\degree C$. Oblicza się wtedy wskaźnik będący stosunkiem C80/C20, który rośnie przy wzroście zawilgocenia izolacji. 

Pojemność układu izolacyjnego można zmierzyć korzystając z mostka Scheringa, jak w poprzednim podpunkcie.

Im większa zdolność do polaryzacji dielektryka, tym mocniejsze jest zjawisko **napięcia powrotnego**, czyli zjawiska utrzymywania się napięcia na zaciskach transformatora pewnego poziomu napięcia. Pomiar napięcia powrotnego stosowany jest właśnie w diagnostycznych pomiarach izolacji transformatorów.

Napięcie powrotne mierzy się poprzez pomiar napięcia na zaciskach uzwojenia transformatora po jego uprzednim naładowaniu i rozładowaniu. Transformator ładuje się napięciem 2 kV, a następnie bada stromość narastania napięcia powrotnego. 

Wykorzystuje się tu układ jak poniżej:

![Untitled](6%20Miernictwo%20wysokonapie%CC%A8ciowe%20i%20diagnostyka%20izola%20f75c07291bc14558ae2f045cff3d5e59/Untitled%208.png)

Natomiast otrzymywane przebiegi mają kształt jak poniżej: 

![Untitled](6%20Miernictwo%20wysokonapie%CC%A8ciowe%20i%20diagnostyka%20izola%20f75c07291bc14558ae2f045cff3d5e59/Untitled%209.png)

Przy czym t_c to czas ładowania, natomiast t_d to czas rozładowania transformatora. Ponownie, uzyskane charakterystyki porównuje się z charakterystykami uzyskanymi dla nowo odebranego transformatora. 

### **Widmo polaryzacji dielektryka**

Dla dielektryków, można także zbadać widmo polaryzacji, czyli zależność przenikalności elektrycznej od częstotliwości napięcia. Badania te wykonuje się korzystając z mostków Scheringa przy częstotliwościach od 50 Hz do częstotliwości akustycznych, lub układami do pomiaru napięcia powrotnego w zakresie bardzo małych częstotliwości. 

### **Pomiar wyładowań niezupełnych**

Inną miarą stanu izolacji jest pomiar wyładowań niezupełnych. Pomiary tych wyładowań polegają na badaniu wielkości ładunku przepływającego przez impedancję pomiarową do miejsca wyładowania niezupełnego w izolacji. Wielkość i częstotliwość wyładowań niezupełnych są większe w zestarzałych izolacjach, przy czym jednocześnie powodują one zwiększenie tempa dalszego starzenia izolacji.

![Untitled](6%20Miernictwo%20wysokonapie%CC%A8ciowe%20i%20diagnostyka%20izola%20f75c07291bc14558ae2f045cff3d5e59/Untitled%205.png)

### **Badania stromym udarem**

W przypadku badań izolatorów kompozytowych, stosuje się metodę opartą o strome udary. Poddanie izolatora oddziaływaniu wysokiego udaru powinno spowodować przeskok w powietrzu, nie na samej próbce. Pomiary wykonuje się zgodnie z wymaganiami opisanymi w normie PN-IEC, co gwarantuje odpowiednie parametry udaru, takie jak czas narastania czy wartość szczytowa. 

![Untitled](6%20Miernictwo%20wysokonapie%CC%A8ciowe%20i%20diagnostyka%20izola%20f75c07291bc14558ae2f045cff3d5e59/Untitled%2012.png)

**Źródła**

[1] Materiały z wykładu prof. Wieczorka

### f) współczynnik strat dielektrycznych tgδ – zależność od częstotliwości, temperatury, napięcia; pomiar mostkiem Scheringa

Współczynnik strat dielektrycznych tgδ to kąt pomiędzy idealnym prądem pojemnościowym a rzeczywistym prądem mierzonym na izolacji (w zapisie wektorowym). Kąt ten mówi nam, jaka jest stratność dielektryczna badanego materiału, sam tangens delta jest proporcjonalny do strat cieplnych na izolacji. Większy kąt delta oznacza, że spadła rezystancja badanej izolacji. 

Pomiary współczynnika strat dielektrycznych pozwalają na określenie stanu izolacji: procesy starzeniowe, zawilgocenie izolacji czy oddziaływanie wyładowań niezupełnych powodują zwiększenie tego współczynnika.

Wartość współczynnika strat dielektrycznych rośnie wraz ze wzrostem przyłożonego napięcia, od pewnego etapu - progu wyładowań niezupełnych.  

![Untitled](6%20Miernictwo%20wysokonapie%CC%A8ciowe%20i%20diagnostyka%20izola%20f75c07291bc14558ae2f045cff3d5e59/Untitled%2013.png)

Natomiast wpływ częstotliwości i temperatury zależy od tego, który z mechanizmów strat dielektrycznych bierze górę: straty typu relaksacyjnego (związanych z ruchem nośników, których zdolność do przemieszczania się w dielektryku jest ograniczona), czy straty przewodnościowe (związane z ruchem nośników swobodnych, w całym zakresie częstotliwości. 

Charakterystyki strat można przedstawiono na poniższym obrazku:

![Untitled](6%20Miernictwo%20wysokonapie%CC%A8ciowe%20i%20diagnostyka%20izola%20f75c07291bc14558ae2f045cff3d5e59/Untitled%2014.png)

**Pomiar mostkiem Scheringa**

Mostek Scheringa przedstawiono na poniższym obrazku: 

![Untitled](6%20Miernictwo%20wysokonapie%CC%A8ciowe%20i%20diagnostyka%20izola%20f75c07291bc14558ae2f045cff3d5e59/Untitled%2015.png)

Pomiary mostkiem Scheringa wykonuje się przy wysokim napięciu, bo mechanizmy stratności zależą od natężenia pola elektrycznego. Pomiar polega na zrównoważeniu potencjałów 3 i 4 poprzez spełnienie warunków równowagi (iloczyny przeciwległych impedancji powinny być sobie równe). Konstrukcja mostka i dobór kondensatora wzorcowego musi umożliwiać wyzerowanie mostka. 

Równowagę potencjałów uzyskuje się poprzez dobór odpowiednich składowych impedancji poszczególnych gałęzi. W mostku Scheringa, elementem wzorcowym jest kondensator Cn, elementem mierzonym - pojemność Cx. Zrównanie iloczynów uzyskuje się przez sterowanie rezystorami R3 i R4 oraz pojemnością C4. 

W celu uniknięcia wpływu zakłóceń elektromagnetycznych, część mostka można ekranować klatką Faradaya. Pomiar mostkiem Scheringa można wykonać zdalnie. 

Pomiar mostkiem Scheringa pozwala na wyznaczenie kąta strat dielektrycznych oraz pojemności badanej próbki.

**Źródła:**

[1] [https://www.dbc.wroc.pl/Content/1148/podstawy_inzynierii_materialowej.pdf](https://www.dbc.wroc.pl/Content/1148/podstawy_inzynierii_materialowej.pdf)

[2] J. Fleszyński - *Miernictwo wysokonapięciowe i laboratorium wysokich napięć*

[3] Materiały z wykładu prof. Wieczorka

[4] Materiały z wykładu *Miernictwo Elektryczne 2*