# 10. Termokinetyka urządzeń elektrycznych i elektronicznych

Status: Zrobione

### a) mechanizmy przewodzenia ciepła w ciałach stałych, ciekłych i gazowych. Przewodzenie ciepła w układach jedno- i wielowarstwowych o różnej geometrii - prawo Fouriera

### Przewodzenie ciepła w płynach

Przewodzenie ciepła może występować w ciałach stałych, ciekłych i gazowych. **W płynach** (czyli gazach i cieczach), **przewodzenie ciepła polega na zderzaniu się ze sobą cząstek poruszających się z różną prędkością**. Mówimy, że cząstki o większej prędkości mają większą temperaturę i w trakcie zderzeń, przekazują ją (w postaci energii kinetycznej) do innych cząstek. Na ogół przewodzenie ciepła w płynach jest połączone z konwekcją. Jeżeli chodzi o ciecze, przewodzenie ciepła jest bardziej złożone ze względu na oddziaływania międzycząsteczkowe płynu o większej gęstości. 

### Przewodzenie ciepła w ciałach stałych

**W ciałach stałych, przewodzenie ciepła polega na przekazywaniu energii drgań siatki krystalicznej**, ruchu swobodnych elektronów, wzbudzeniu magnetycznym lub promieniowaniu elektromagnetycznym. Drgania siatki dotyczą w zasadzie wszystkich ciał stałych. 

Siatka krystaliczna materiału ma większe drgania przy wyższej temperaturze i są one przekazywane do przylegających cząstek o niższej temperaturze. 

Ruch swobodnych elektronów (gazu elektronowego) powoduje ich zderzanie się z siatką krystaliczną i wzbudzanie jej drgań - logiczne jest zatem, że zjawisko to występuje tylko w materiałach dobrze przewodzących. 

Wzbudzenie magnetyczne wynika z występowania dipoli magnetycznych i ich momentów, których oddziaływanie ma wpływ na przepływ ciepła w materiale. Natomiast oddziaływanie elektromagnetyczne dotyczy materiałów przezroczystych, w które może wnikać.

### Prawo Fouriera

Prawo Fouriera to sformułowanie fizycznego spostrzeżenia, zgodnie z którym przewodzenie ciepła zachodzi zawsze w kierunku od wyższej do niższej temperatury, tym szybciej im wyższa powierzchnia styku dwóch materiałów i tym lepiej, im wyższa przewodność cieplna rozpatrywanego materiału. Można to zapisać wzorem:

$$
\frac{q_x}{A}=-k \frac{dT}{dx}\rarr\frac{q_x}{A}L=-k\frac{T_1-T_2}{L}
$$

Gdzie $q_x$ jest strumieniem ciepła w kierunku x wyrażonym w W, A to powierzchnia styku materiałów, k - przewodność cieplna materiału [$\frac{W}{m\cdot K}$], natomiast $dT/dx$ to gradient temperatury w kierunku x, $L$ - miejsce w grubości materiału.

### Przewodzenie ciepła w układach jedno- i wielowarstwowych o różnej geometrii

Przewodzenie ciepła w **układach płaskich** jest zagadnieniem dosyć prostym. Strumień cieplny można tu potraktować tak, jak prąd w obwodach elektrycznych. Różnica temperatur to napięcie. Przewodność cieplna, powierzchnia styku i długość w materiale (długość jako określone miejsce w grubości ściany z materiału) tworzą opór cieplny. 

Układy tego typu można rozpatrywać podobnie do obwodów elektrycznych. Jeżeli ściany ułożone są w szeregu, to można policzyć wypadkowy strumień cieplny (jak prąd) z różnicy temperatur na dwóch końcach układu i ich oporu cieplnego. Potem temperatury w poszczególnych miejscach (jak napięcie) wylicza się po prostu mnożąc strumień przez opór cieplny. W obwodach równoległych sprawa ma się analogicznie. 

![Untitled](10%20Termokinetyka%20urza%CC%A8dzen%CC%81%20elektrycznych%20i%20elektr%2002ecaa01a0d24d34810b38ff4b757e48/Untitled.png)

![Untitled](10%20Termokinetyka%20urza%CC%A8dzen%CC%81%20elektrycznych%20i%20elektr%2002ecaa01a0d24d34810b38ff4b757e48/Untitled%201.png)

**Układy cylindryczne** są bardziej złożone, bo ciepło rozchodzi się jednocześnie w wielu kierunkach (od środka do zewnątrz układu), przy czym powierzchnie wewnętrzna i zewnętrzna materiału są różne. Uwzględnienie tych cech układów cylindrycznych sprowadza się w uproszczeniu do zastosowania logarytmów wiążących promienie wewnętrzne i zewnętrzne cylindrów. Wyprowadzenie tych zależności zaczyna się od współrzędnych biegunowych.

Ułożenie koncentrycznie cylindrów termoprzewodzących znowu sprowadza się do analizy układu podobnego do obwodu elektrycznego, przy czym sposób liczenia oporu cieplnego wynika tu z wspomnianych wyżej zależności logarytmicznych. 

Ogólnie, opór cieplny w układzie cylindrycznym zależy od logarytmu naturalnego stosunku większego promienia do mniejszego i maleje wraz z długością materiału, bo to od długości cylindra zależy powierzchnia styku. 

![Untitled](10%20Termokinetyka%20urza%CC%A8dzen%CC%81%20elektrycznych%20i%20elektr%2002ecaa01a0d24d34810b38ff4b757e48/Untitled%202.png)

**Układy sferyczne,** podobnie jak cylindryczne, w celu wyprowadzenia uproszczonych zależności, należy rozpatrywać we współrzędnych biegunowych. Ostateczna zależność na opór cieplny wynika z proporcji promieni sfer do iloczynu tych promieni. 

![Untitled](10%20Termokinetyka%20urza%CC%A8dzen%CC%81%20elektrycznych%20i%20elektr%2002ecaa01a0d24d34810b38ff4b757e48/Untitled%203.png)

**Źródła:**

[1] Wiśniewski, Wiśniewski - *Wymiana Ciepła*

[2] William S. Janna - *Engineering Heat Transfer, Third Edition*

### b) konwekcja swobodna i wymuszona - istota zjawiska, ogólne zasady doboru kryteriów do obliczeń cieplnych w układach elektrycznych

**Konwekcja** to sposób przewodzenia ciepła związany z **ruchem płynów**. Jeżeli ruch płynów jest spowodowany **zewnętrznym czynnikiem**, takim jak działanie pompy lub wentylatora, mówimy o **konwekcji wymuszonej**. Jeżeli ciesz porusza się głównie ze względu na wynikającą z różnicy temperatur **różnicę gęstości** - czyli płyn gęstszy opada, rzadszy - unosi się - mówimy o **konwekcji naturalnej**.

**Przejmowanie ciepła** to wymiana ciepła między powierzchnią ciała stałego a opływającym ją płynem. Gęstość strumienia przejmowanego ciepła określana jest prawem Newtona (prawo stygnięcia), które wiąże różnice temperatur ciała stałego i płynu przy wykorzystaniu współczynnika przejmowania ciepła ($\frac{W}{m^2K}$).

Jeżeli mówimy o obliczeniach cieplnych w układach elektrycznych, chodzi nam tu głównie o sposób w jaki konwekcja wymuszona - czyli np. działanie wentylatora - przejmuje ciepło z obwodów urządzenia. Czyli interesuje nas strumień przejmowanego ciepła lub jego gęstość.

Liczenie strumienia cieplnego z **prawa Newtona** wymaga obliczenia **współczynnika przejmowania ciepła**. Współczynnik przejmowania ciepła zależy od prędkości cieczy i rodzaju przepływu warstwy przyściennej (laminarny - cząstki płyną równolegle do siebie; turbulentny - tory ruchu cząstek przecinają się), a także od lepkości, gęstości i przewodności cieplnej płynu.

Kryterium do obliczeń cieplnych dobiera się na podstawie kilku czynników, ale podstawowymi są rodzaj przepływu (turbulentny / laminarny), kształtu kanału (opływanie płaskiej ściany to co innego niż ruch w kanale cylindrycznym) i rodzaju płynu, przy czym rodzaj płynu zawiera w sobie wspomniane wyżej właściwości fizyczne - lepkość, gęstość, przewodność cieplną. Wszystkie te wielkości są ze sobą wiązane przez różne współczynniki takie, jak liczba Nusselta, liczba Reynoldsa, liczba Prandtla czy liczba Eckerta. 

**Źródła:**

[1] Wiśniewski, Wiśniewski - *Wymiana Ciepła*

[2] William S. Janna - *Engineering Heat Transfer, Third Edition*

[3] Materiały z wykładu *Termokinetyka urządzeń elektrycznych i elektronicznych*

### c) rury cieplne - budowa i zasada działania, zalety, typy. Zastosowanie rur cieplnych w układach chłodzących

### Budowa i zasada działania

Rurka ciepła to szczelnie zamknięta rurka lub pojemnik o innym kształcie, której przestrzeń jest częściowo wypełniona cieczą. Ciecz do rurki dobiera się zależnie od temperatury pracy rurki i oczekiwanej gęstości strumienia ciepła. 

Rurka jest zbudowana z trzech stref: parownika, strefy adiabatycznej oraz skraplacza. Do parownika doprowadzane jest ciepło powodujące odparowanie cieczy. Strefa adiabatyczna służy do transportu ciepła bez wymiany z otoczeniem. Skraplacz natomiast służy do oddawania ciepła na zewnątrz, a swoją nazwę zawdzięcza temu, że to w nim para w rurce ulega skropleniu. Skropliny w takiej rurce przemieszczają się pod wpływem sił kapilarnych (sił między parą a cieczą) przeciwnie do kierunku pary. Proces parowania, transportu i skraplania zachodzi w sposób ciągły.

![Untitled](10%20Termokinetyka%20urza%CC%A8dzen%CC%81%20elektrycznych%20i%20elektr%2002ecaa01a0d24d34810b38ff4b757e48/Untitled%204.png)

Wewnętrzna powierzchnia rurki jest pokryta na ogół strukturami kapilarnymi, natomiast jej zewnętrzna powierzchnia j pokryta jest izolacją termiczną. Struktury kapilarne to po prostu odpowiednie ukształtowanie powierzchni wewnętrznej rurki tak, by wytworzyć różnicę ciśnienia kapilarnego między skraplaczem a parownikiem. Są to na ogół tzw. knoty wykonane z metalowych siatek umieszczonych na obwodzie lub w środku rurki. 

Struktury kapilarne mogę być po prostu podłużnymi rowkami, ale są też pewne konstrukcje, które tworzą tzw. diodę cieplną, czyli rurkę umożliwiającą przepływ ciepła w tylko jedną stronę. 

![Untitled](10%20Termokinetyka%20urza%CC%A8dzen%CC%81%20elektrycznych%20i%20elektr%2002ecaa01a0d24d34810b38ff4b757e48/Untitled%205.png)

### Typy rur cieplnych

Rurki cieplne można rozróżniać ze względu na sposób działania. Wśród nich można wymienić:

- **grawitacyjne rury cieplne (termosyfony)** - kondensat przemieszcza się w nich pod wpływem siły ciężkości
- **klasyczne rury cieplne** - kondensat przemieszcza się w nich ze względu na różnicę ciśnień kapilarnych
- **wirujące rury cieplne** - transport kondensatu następuje dzięki działaniu siły odśrodkowej
- **termosyfony antygrawitacyjne** - skraplacz jest tu poniżej parownika, a kondensat przemieszcza się w postaci dwufazowej mieszaniny w osobnym (wewnętrznym) przewodzie posiadającym dodatkowy grzejnik
- **mikrorurki** - są to płaskie płytki lub zestawy cienkich rurek, stosowane głównie w laptopach i elektronice;
- **rurki ciepła o zmiennym przewodnictwie** - rurki w których jest możliwość regulacji wielkości powierzchni wymiany ciepła dzięki obecności “korka” z nieskraplającego się gazu.

### Zalety

Podstawową zaletą rurek cieplnych jest to, że wskutek procesów parowania i skraplania czynnika roboczego (czyli z wykorzystaniem ciepła utajonego), uzyskuje się **bardzo duże gęstości przekazywanego strumienia ciepła** przy niewielkich różnicach temperatur. Dzięki temu, współczynniki przewodzenia ciepła takich rurek są znacznie większe nawet niż w przypadku najlepiej przewodzących ciepło metali. 

Kolejną zaletą są **szerokie możliwości zastosowania** ze względu na fakt, że to od czynnika cieplnego zależą docelowe temperatury pracy. Jasne, poszczególne czynniki mogą mieć relatywnie małą rozpiętość temperaturową, ale wypadkowo można spreparować rury cieplne do pracy tak w pobliżu zera kelwina, jak i w temperaturze rzędu 2000 stopni celsjusza.

Ze względu na różne rozmiary konstrukcyjne, rurki cieplne można stosować zarówno w niewielkiej elektronice pokroju laptopów, jak i do chłodzenia większych maszyn i urządzeń.

### Zastosowanie

Rurki ciepła sprawdzają się w wielu dziedzinach, wśród których można wymienić:

- technika kosmiczna - wyrównywanie temperatur, transport ciepła
- elektronika - chłodzenie części czynnych, zasilaczy, procesorów, wzmacniaczy, konsol, etc.
- budownictwo - stabilizacja temperatury gruntu wokół fundamentów i podpór w obszarach arktycznych, rozmrażanie oblodzonych dróg, etc.
- przemysłowe wymienniki ciepła - w tym zastosowanie wymienników z rurkami ciepła w systemach klimatyzacyjnych
- lotnictwo - termiczna regulacja w samolotach cywilnych i wojskowych;

Ciekawym zastosowaniem są wymienniki cieplne z rurkami ciepła w systemach klimatyzacyjnych. Pobierają one ciepło z nagrzanego powietrza w pomieszczeniu i oddają je do otoczenia, przy czym nie mają ruchomych części, oferują wysoką sprawność, niskie spadki ciśnienia przepływającego powietrza, brak zapotrzebowania na energię z zewnątrz, bezobsługowość i długi okres użytkowania. 

Poniżej fotka - rurki ciepła zamontowane do chłodnicy procesora:

![Untitled](10%20Termokinetyka%20urza%CC%A8dzen%CC%81%20elektrycznych%20i%20elektr%2002ecaa01a0d24d34810b38ff4b757e48/Untitled%206.png)

**Źródła**

[1] Wiśniewski, Wiśniewski - *Wymiana Ciepła*

[2] Pabiś, Koszut - *Rurki ciepła - zasada działania, budowa, zastosowania -* [https://repozytorium.biblos.pk.edu.pl/redo/resources/31775/file/suwFiles/PabisA_RurkiCiepla.pdf](https://repozytorium.biblos.pk.edu.pl/redo/resources/31775/file/suwFiles/PabisA_RurkiCiepla.pdf)

### d) zjawiska termoelektryczne - rodzaje i sposób wykorzystania do chłodzenia urządzeń elektrycznych i elektronicznych

### Zjawiska termoelektryczne

Zjawiska termoelektryczne polegają na bezpośredniej transformacji różnicy temperatury na napięcie elektryczne lub napięcia elektrycznego na różnicę temperatur. Wśród zjawisk termoelektrycznych wyróżnia się trzy podstawowe: zjawisko Seebecka, zjawisko Peltiera oraz zjawisko Thomsona. 

**Zjawisko Peltiera** polega na tym, że podczas przepływu prądu stałego przez styk dwóch różnych materiałów powoduje, że jeden z tych materiałów się nagrzewa, drugi chłodzi. Zjawisko to jest niezależne od ciepła Joule’a-Lenza (nagrzewaniu się rezystancji). Wynika to z przechodzenia elektronów między półprzewodnikiem a przewodnikiem. Przeskok elektronu z przewodnika na półprzewodnik mogą wykonać tylko elektrony o dużej energii, co powoduje wychładzanie się metalu. W drugą stronę, elektrony przeskakujące z półprzewodnika na metal oddają dużą porcję energii przeskakując z pasma przewodnictwa, nagrzewając tym samym metal. 

**Zjawisko Seebecka** polega na tym, że na styku dwóch różnych materiałów przewodzących, w przypadku ich różnych temperatur, powstaje siła elektromotoryczna. W półprzewodnikach wynika to z faktu, że w materiale o różnej temperaturze na obu końcach zmienia się gęstość koncentracji nośników ładunku - wskutek czego zależnie od rodzaju przewodnictwa, nośniki ładunku przemieszczają się w określonym kierunku (elektrony w półprzewodniku typu “n” uciekają do zimniejszego końca próbki i nadają mu potencjał ujemny). W przewodnikach, wolne elektrony nabierają energii kinetycznej i przemieszczają się w kierunku zimnego końca próbki. Zjawisko to opisuje się współczynnikiem Seebecka. 

**Zjawisko Thomsona** polega na tym, że przy przepływie prądu przez próbkę półprzewodnika na której występuje różnica temperatur, próbka wydziela (lub pobiera z otoczenia) pewną ilość ciepła, niezależną od ciepła Joule’a-Lenza. Wynika to z faktu różnorodnej koncentracji nośników ładunku w takiej próbce (co wynika znowu z różnicy temperatur) i występowania prądu dyfuzji. Zewnętrzne pole elektryczne może być zgodne lub przeciwne do prądu dyfuzji. Jeżeli zewnętrzne pole jest zgodne z polem wynikającym z prądu dyfuzji materiału, dochodzi do chłodzenia próbki. W przeciwnym razie, dodatkowa praca pola zewnętrznego wykonana na nośnikach ładunku powoduje dodatkowe nagrzewanie próbki. 

### Wykorzystanie zjawisk termoelektrycznych

Zjawiska termoelektryczne wykorzystywane są w technice do systemów ogrzewania, chłodzenia i pomiarów temperatury. 

**Zjawisko Peltiera** wykorzystuje się do budowania pomp ciepła, służących do chłodzenia i nagrzewania różnych obiektów. Gradient temperatury na półprzewodniku powoduje powstanie siły elektromotorycznej i odpowiedni obwód jest w stanie ją wyprowadzić na zewnątrz w postaci prądu elektrycznego.

**Zjawisko Seebecka** wykorzystuje się natomiast do produkcji termopar. Termopary reagują na różnicę temperatur w których umieszczono ich spoiny. To znaczy, że termopara działa z temperaturą odniesienia (termostatyzacją) - jedno złącze jest umieszczone w temperaturze badanej, drugie - w temperaturze odniesienia. Powstające napięcie pozwala na określenie różnicy temperatur. Efekt Seebecka stosuje się też do budowy termostosów, które konwertują energię cieplną na elektryczną. 

**Źródła**

[1] [https://pl.wikipedia.org/wiki/Zjawisko_termoelektryczne](https://pl.wikipedia.org/wiki/Zjawisko_termoelektryczne)

[2] [https://pl.wikipedia.org/wiki/Termopara](https://pl.wikipedia.org/wiki/Termopara)

[3] Materiały z wykładu *Materiały elektromagnetyczne*

### e) promieniowanie cieplne - opis zjawiska, podstawowych praw i parametrów. Ekrany cieplne

### Opis zjawiska i podstawowych praw

**Promieniowanie cieplne** to przekazywanie ciepła poprzez fale elektromagnetyczne. Konwencjonalnie, jako radiację cieplną określa się przede wszystkim tę część fal elektromagnetycznych, która klasyfikowana jest jako promieniowanie podczerwone. 

Przewodzenie cieplne i konwekcja to mechanizmy przekazywania ciepła opierające się o fizyczne medium. **Promieniowanie cieplne** wyróżnia się na ich tle tym, że **może odbywać się również w próżni** i odbywa się poprzez fale elektromagnetyczne. Na dodatek, do przekazywanie ciepła przez promieniowanie **nie wymaga różnicy temperatur**. Promieniowanie elektromagnetyczne jest emitowane.

To, jaki strumień ciepła (albo gęstość strumienia ciepła) emituje ciało, zależy od czwartej potęgi jego temperatury. W idealnym przypadku, nazywanym **ciałem doskonale czarnym**, strumień ciepła zależy tylko od temperatury ciała, jego powierzchni oraz stałej Boltzmanna, zgodnie ze wzorem, nazywanym **prawem Stefana-Boltzmanna**:

$$
q_r=\sigma AT^4
$$

**Widmo promieniowania** ciała doskonale czarnego - czyli wykres pokazujący, ile energii ciało wypromieniowuje w postaci fal elektromagnetycznych o określonej częstotliwości - wygląda jak poniżej. Różnymi kolorami oznaczono widma promieniowania ciał o różnych temperaturach (5000K, 4000K itd.) Strumień ciepła ciała doskonale czarnego to po prostu pole pod takim wykresem. Obydwie te rzeczy są opisane **prawem Plancka.**

![Untitled](10%20Termokinetyka%20urza%CC%A8dzen%CC%81%20elektrycznych%20i%20elektr%2002ecaa01a0d24d34810b38ff4b757e48/Untitled%207.png)

Na widmie promieniowania widać, że natężenie promieniowania jest różne dla różnych długości fal, a jego maksimum przypada gdzieś w zakresie światła widzialnego albo podczerwieni. Widać też, że im niższa temperatura, tym bardziej maksymalne natężenie - i całe widmo - przesuwa się w stronę dłuższych fal, czyli w stronę fal podczerwonych. To zjawisko opisywane jest **prawem Wiena.** 

W naturze rzadko zdarza się jednak, żeby ciała miały widmo promieniowania takie, jak na rysunku powyżej. Często poszczególne długości fal są “powycinane” - np. dwutlenek węgla emituje bardzo mało energii w zakresie podczerwieni (m.in. dlatego nazywa się go gazem cieplarnianym - bo ogranicza ilość ciepła oddawanego przez Ziemię w przestrzeń kosmiczną). Ciało o takim ograniczonym spektrum promieniowania w różnych zakresach nazywa się **ciałem szarym**. 

### Podstawowe parametry

Emitowane przez ciało szare ciepło jest mniejsze niż emitowane przez ciało doskonale czarne i stosunek tej emisji do emisji ciała doskonale czarnego nazywa się **emisyjnością.** Emisyjność przyjmuje wartości od 0 do 1. 

Wyróżnia się przy tym różne rodzaje emisyjności. Podstawowa to **emisyjność kierunkowa**, czyli opisany wyżej ułamek, ale w stosunku do promieniowania emitowanego w jednym kierunku. Inna to **półsferyczna**, czyli opisująca rzeczywistą powierzchnię ciała. W każdym przypadku mówi się też o emisyjności **panchromatycznej** (czyli obejmującej całe spektrum) lub **monochromatycznej** (opisującej określoną długość fali). Ot, nomenklatura.

Inne podstawowe parametry opisujące promieniowanie cieplne to *absorpcyjność*, *refleksyjność* oraz *przepuszczalność*. Każdy z nich to współczynnik o wartości od 0 do 1. Wszystkie z nich (włączając w to emisyjność) zależą od powierzchni opisywanego ciała.

**Absorpcyjność** opisuje ilość energii pochłanianej przez ciało jako ułamek energii docierającej do niego. Przy tej samej temperaturze, absorpcyjność powierzchni może być równa jej emisyjności w określonym kierunku. Czarne auto jednocześnie dobrze pochłania ciepło i je emituje, nagrzewając wszystko dookoła - inaczej nagrzewałoby się w nieskończoność.

**Refleksyjność** to ułamek energii odbitej przez ciało. Energia odbita to po prostu odbite fale elektromagnetyczne, niepochłaniane przez ciało. Śnieg o białej powierzchni odbija sporą część promieniowania, czyli ma wysoką refleksyjność. 

**Przepuszczalność** to ułamek promieniowania elektromagnetycznego, które przechodzi przez ciało, ale nie jest pochłaniane ani odbijane - po prostu przelatuje. W naturze w zasadzie każdy materiał ma bardzo niską przepuszczalność, bliską zera. Nawet szkło całkiem nieźle pochłania ciepło i nie ma aż tak dobrej przepuszczalności. Dla uzyskania wysokiej przepuszczalności robi się specjalne materiały, ale nawet w nich dotyczy to przede wszystkim określonej części widma.

Oprócz tego istnieją jeszcze **współczynniki konfiguracji**, które opisują właściwości promieniowania docierającego do różnych układów geometrycznych. Opisują np. jaka część energii dociera do pokoju, gdy promieniowanie wpada przez okno - bo przecież inna ilość dociera do ściany naprzeciw okna, a inna do ściany z oknem. Ale raczej nikt o to nie będzie męczyć buły na egzaminie.

Z wielkości dotyczących samego promieniowania, można natomiast wymienić dwie. Są nimi:

- **natężenie promieniowania** - jest to strumień promieniowania wysyłany w jednostkowy kąt bryłowy, wyrażony jako wat na steradian [W/sr];
- **strumień promieniowania** - energia niesiona przez promieniowanie przechodzące przez określoną płaszczyznę w jednostce czasu, wyrażona w watach [W];
- **irradiancja** - moc jaką przenosi promieniowanie przez płaszczyznę jednostkową, wyrażona w watach na metr kwadratowy [W/m2];

### Podstawowe prawa

W promieniowaniu cieplnym można wyróżnić cztery podstawowe prawa, z czego wszystkie z nich zostały już wyżej opisane. Są to:

- **Prawo Kirchhoffa** - zgodnie z nim, dana powierzchnia przy stałej temperaturze ma taką samą emisyjność co absorpcyjność.
- **Prawo Stefana-Boltzmanna** - zgodnie z nim, ilość energii wypromieniowywanej przez ciało jest proporcjonalna do czwartej potęgi temperatury tego ciała.
- **Prawo Plancka** - prawo to opisuje emisję promieniowania ciała doskonale czarnego - to z niego bierze się widmo promieniowania na obrazku opisanym wcześniej i to z niego wynika, że ilość wypromieniowanej energii jest polem pod tym wykresem.
- **Prawo Wiena** - mówi, że wraz ze wzrostem temperatury ciała, jego widmo promieniowania przenosi się w stronę fal krótkich. Dlatego gorące słoneczko wali w nas  dużą dawką ultrafioletu.

### Ekrany cieplne

Mając na uwadze wszystko co zostało wyżej opisane, łatwo jest wywnioskować, że **ekran cieplny** to prosty “izolator” ciepła, który nie tyle izoluje ciepło (bo nie ma tu termoprzewodnictwa), co po prostu **odbija promieniowanie elektromagnetyczne**, zwłaszcza w zakresie fal podczerwonych. Oznacza to, że ekran cieplny to po prostu **materiał o wysokim współczynniku refleksyjności**. 

Ekrany cieplne stosuje się w szeroko pojętym budownictwie i chłodnictwie. Pozwalają one na dobre zachowanie temperatury ze względu na odbijanie z powrotem promieniowania podczerwonego. Przy zastosowaniu konstrukcji dwuwarstwowej, wypełnionej np. powietrzem, taki ekran cieplny może jednocześnie blokować przepływ ciepła przez przewodzenie.

**Źródła:**

[1] Wiśniewski, Wiśniewski - *Wymiana Ciepła*

[2] William S. Janna - *Engineering Heat Transfer, Third Edition*

[3] [https://pl.wikipedia.org/wiki/Ciało_doskonale_czarne](https://pl.wikipedia.org/wiki/Cia%C5%82o_doskonale_czarne) 

[4] [https://pl.wikipedia.org/wiki/Prawo_Wiena](https://pl.wikipedia.org/wiki/Prawo_Wiena) 

[5] [https://pl.wikipedia.org/wiki/Prawo_Plancka](https://pl.wikipedia.org/wiki/Prawo_Plancka) 

[6] Popkiewicz, Kardaś, Malinowski - *Nauka o klimacie* 

[7] [https://pl.wikipedia.org/wiki/Refleksyjna_izolacja_termiczna](https://pl.wikipedia.org/wiki/Refleksyjna_izolacja_termiczna)

[8] [https://pl.wikipedia.org/wiki/Strumień_promieniowania](https://pl.wikipedia.org/wiki/Strumie%C5%84_promieniowania) 

[9] [https://pl.wikipedia.org/wiki/Irradiancja](https://pl.wikipedia.org/wiki/Irradiancja) 

[10] [https://pl.wikipedia.org/wiki/Natężenie_promieniowania](https://pl.wikipedia.org/wiki/Nat%C4%99%C5%BCenie_promieniowania)