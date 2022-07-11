# 4. Analiza procesów w elektromechanicznym systemie napędowym

Status: Zrobione

### a) przy pominięciu procesów elektromagnetycznych silnika - równanie ruchu dla układu napędowego o ruchu obrotowym, schemat strukturalny układu

**Połączenie sztywne**

W przypadku połączenia sztywnego, układ napędowy o ruchu obrotowym można przedstawić w postaci jednomasowego wału o momencie bezwładności równym sumie momentów bezwładności silnika i maszyny roboczej. 

Moment pochodzący od silnika traktuje się jako zmienną zależną od układu sterowania, natomiast moment obciążenia jest traktowany jako zakłócenie zewnętrzne. Można również zdefiniować moment dynamiczny, czyli różnicę momentu obciążenia i momentu elektromagnetycznego w stanach dynamicznych układu. 

![Untitled](4%20Analiza%20proceso%CC%81w%20w%20elektromechanicznym%20systemie%20c409d31dd1a34dffb13f506dcd4e9107/Untitled.png)

Połączenie sztywne można przedstawić w postaci schematu blokowego jako całkę z momentu dynamicznego o stałej równej momentowi bezwładności układu, jak poniżej:

 

![Untitled](4%20Analiza%20proceso%CC%81w%20w%20elektromechanicznym%20systemie%20c409d31dd1a34dffb13f506dcd4e9107/Untitled%201.png)

Równanie ruchu dla układu napędowego z połączeniem sztywnym wyprowadza się z zasady zachowania energii. Energia elektryczna dostarczana do układu jest transformowana na energię użyteczną oraz energię kinetyczną. Energię kinetyczną stanowią energie obrotu mas bezwładności. Energia użyteczna to energia przenoszona na układ napędowy.

Ogólnie rzecz ujmując, równanie ruchu układu z połączeniem sztywnym przyjmuje postać:

$$
m_e-m_o=m_d=J\frac{d\omega}{dt}
$$

Czyli moment dynamiczny jest równy pochodnej prędkości pomnożonej przez moment bezwładności układu. Moment dynamiczny można przedstawić przy tym jako różnicę między momentem elektromagnetycznym silnika a momentem oporowym maszyny roboczej.

**Połączenie elastyczne**

W przypadku połączenia elastycznego, w stanach dynamicznych prędkości obrotowe pędnika i maszyny roboczej są różne, zależnie od elastyczności połączenia. W tym przypadku, analizę układu sprowadza się do połączenia dwumasowego, w którym moment bezwładności wału dzieli się po połowie między pędnik a maszynę roboczą.

![Untitled](4%20Analiza%20proceso%CC%81w%20w%20elektromechanicznym%20systemie%20c409d31dd1a34dffb13f506dcd4e9107/Untitled%202.png)

Schemat blokowy takiego układu jest bardziej złożony, ponieważ moment oprócz momentów obciążenia i elektromagnetycznego, pojawia się moment skrętny związany z elastycznością wału. W układzie pojawiają się zatem stałe czasowe silnika, wału oraz maszyny roboczej, co ilustruje poniższy schemat blokowy:

![Untitled](4%20Analiza%20proceso%CC%81w%20w%20elektromechanicznym%20systemie%20c409d31dd1a34dffb13f506dcd4e9107/Untitled%203.png)

Schemat blokowy układu jest jednoznacznie związany z równaniem ruchu. W układzie dwumasowym można wyróżnić równania ruchu dla poszczególnych jego elementów, kolejno połączenia silnik-wał, połączenia wał-obciążenie oraz samego wału:

$$
m_e-m_s=J_1\frac{d\omega_1}{dt}
$$

$$
m_s-m_o=J_2\frac{d\omega_1}{dt}
$$

$$
m_s=K_w\int_0^t(\omega-\omega_2)d\tau+D_w(\omega-\omega_2)
$$

Przy czym Kw i Dw to kolejno współczynniki sprężystości i tłumienia wału.

### Najważniejsze punkty

- równanie ruchu mówi, że prędkość obrotowa zmienia się zależnie od bezwładności masy wirującej oraz różnicy momentu elektromagnetycznego i obciążenia
- schemat strukturalny układu napędowego to wał łączący silnik z maszyną roboczą
- układy dwumasowe: różnica momentu silnika i momentu skrętnego daje prędkość wału silnika; różnica prędkości wału silnika i maszyny roboczej daje moment skrętny; różnica momentu skrętnego i momentu obciążenia daje prędkość maszyny roboczej

### **Źródła**

[1] Materiały i notatki z wykładu *Elektromechaniczne systemy napędowe*

[2] Zawirski, Deskur, Kaczmarek - *Automatyka napędu elektrycznego*

### b) z silnikiem obcowzbudnym prądu stałego - model i równania stanu układu, elektromechaniczna i elektromagnetyczna stała czasowa układu i ich wpływ na charakter procesów elektromagnetycznych

**Model układu**

Układ napędowy z silnikiem obcowzbudnym prądu stałego można przedstawić schematycznie w poniższej postaci: 

![Untitled](4%20Analiza%20proceso%CC%81w%20w%20elektromechanicznym%20systemie%20c409d31dd1a34dffb13f506dcd4e9107/Untitled%204.png)

Widać więc, że w takim układzie można wyróżnić takie elementy jak obwód twornika, obwód wzbudzenia, generację siły elektromotorycznej oraz część mechaniczną. 

**Obwód twornika** jest traktowany jako **element inercyjny** o stałej czasowej równej **elektromagnetycznej stałej czasowej twornika**. To oznacza, że przy skokowej zmianie napięcia zasilania lub siły elektromotorycznej, zmiana wartości prądu twornika wystąpi z opóźnieniem określonym przez tę stałą czasową. 

Elektromagnetyczną stałą czasową układu z silnikiem prądu stałego wyznacza się z parametrów obwodu twornika zgodnie z równaniem: $T_e=\frac{L_t}{R_t}$. Im wyższa indukcyjność, tym większa stała czasowa.

Podobnie, struktura **obwodu wzbudzenia** jest członem inercyjnym, przy czym najczęściej w przypadku silników obcowzbudnych pomijamy ten element. 

**Generację siły elektromotorycznej** **można traktować jako człon proporcjonalny o wzmocnieniu zależnym od wartości strumienia wzbudzenia oraz stałej konstrukcyjnej silnika.

**Układ mechaniczny** traktuje się jako element całkujący opisywany przez równanie ruchu $m_e(t)-m_m(t)=m_d(t)=J_z\frac{d\omega(t)}{dt}$. Jego stała całkowania jest równa momentowi bezwładności układu mechanicznego. Stąd, **mechaniczna stała czasowa** układu jest **zależna od momentów bezwładności** silnika i maszyny roboczej oraz od prędkości biegu jałowego oraz znamionowego momentu silnika, zgodnie z równaniem $T_M=\frac{J\Omega_0}{M_N}$. Od mechanicznej stałej czasowej zależy to, jak szybko silnik przyspiesza, więc również to, jak szybko siła elektromotoryczna silnika zrówna się z napięciem znamionowym.  

Połączenie powyższych członów daje następujący układ napędowy z silnikiem prądu stałego:

![Untitled](4%20Analiza%20proceso%CC%81w%20w%20elektromechanicznym%20systemie%20c409d31dd1a34dffb13f506dcd4e9107/Untitled%205.png)

Mając na uwadze powyższe, silnik prądu stałego można opisać następującymi równaniami stanu:

- obwód twornika: $u(t)=R_t\cdot i_t(t)+L_t\cdot d/dt i_t(t) + e(t)$
- siła elektromotoryczna twornika: $e(t)=k_e\cdot\Phi_w\cdot\omega(t)$
- moment elektromagnetyczny silnika: $m_e(t)=k_e\cdot\Phi_w\cdot i_t(t)$
- równanie równowagi mechanicznej: $m_e(t)-m_m(t)=J_z\cdot\frac{d}{dt}\omega(t)$

Silnik można opisać również poniższymi równaniami różniczkowymi:

$$
T_e\frac{d_i}{dt}=-i_t+K_t(u_t-\psi_f\omega_m)
$$

$$
T_M\frac{d\omega_m}{dt}=\psi_fi_f-m_o
$$

Gdzie $K_t=\frac{U_{tN}}{I_{tN}R_{tN}}$ to współczynnik wzmocnienia obwodu twornika silnika prądu stałego

### Najważniejsze punkty

- równania stanu SPS opisują zmienne pojawiające się w silniku takie jak prądy, napięcia, moment, prędkość czy siła elektromotoryczna
- równania stanu SPS to równania obwodów twornika, wzbudzenia, połączenia mechanicznego oraz członu generacji SEM
- mechaniczna stała czasowa układu mówi, jak szybko zmienia się prędkość silnika przy pojawieniu się momentu dynamicznego i jest zależna od bezwładności wirnika
- elektromagnetyczna stała czasowa układu mówi, jak szybko zmienia się prąd przy pojawieniu się napięcia i jest zależna od parametrów R i L obwodu twornika

### **Źródła**

[1] Materiały i notatki z wykładu *Elektromechaniczne systemy napędowe*

### c) z silnikiem indukcyjnym - model i wektorowe równania stanu układu, współczynniki tłumienia i stałe czasowe układu elektromechanicznego

Silnik indukcyjny modeluje się jako maszynę z trzema uzwojeniami stojana oraz trzema uzwojeniami wirnika, a także z połączeniem mechanicznym.

![Untitled](4%20Analiza%20proceso%CC%81w%20w%20elektromechanicznym%20systemie%20c409d31dd1a34dffb13f506dcd4e9107/Untitled%206.png)

Model trójfazowy można opisać układami równań dla każdej z faz osobno, jednak jest to rozwiązanie niewygodne, ponieważ składa się z wielu równań i zmiennych. W celu uproszczenia układu pod kątem sterowania, stosuje się transformaty Clarke i Parka, przekształcające układy równań trójfazowych do zapisu wektorowego, stacjonarnego kolejno względem stojana lub wirnika. 

Wektorowe równania stanu są dużo wygodniejsze, ponieważ zmienne pojawiające się w trzech fazach opisywane są jednym wektorem, który może być sterowany przez układ regulacji. 

Wśród równań stanu silnika indukcyjnego można wyróżnić:

- Równanie wektorowe stojana: $\underline{u}_s=R_s\cdot \underline{i}_s+\frac{d}{dt}\underline{\psi}_s+j\omega_k\underline{\psi}_s$
- Równanie wektorowe wirnika: $0=R_r\cdot \underline{i}_r+\frac{d}{dt}\underline{\psi}_r+j(\omega_k-\omega_e)\underline{\psi}_r$
- Równanie wektorowe strumienia stojana: $\underline{\psi}_s=L_s\cdot \underline{i}_s+L_m\cdot\underline{i}_r$
- Równanie wektorowe strumienia wirnika: $\underline{\psi}_r=L_m\cdot \underline{i}_s+L_r\cdot\underline{i}_r$
- Równanie równowagi mechanicznej: $m_e-m_m=\frac{J_Z}{p}\cdot \frac{d}{dt}\omega_e$
- Równanie momentu elektromagnetycznego silnika: $m_e=\frac{3}{2}p(\underline{\psi}_s\times \underline{i}_s)=-\frac{3}{2}p(\underline{\psi}_r\times \underline{i}_r)$

Najważniejsze spośród tych równań to równanie momentu elektromagnetycznego silnika, ponieważ to z niego wynika, że sterowanie wektorowe silnikiem indukcyjnym wymaga kontroli nad jego zmiennymi elektromagnetycznymi - prądami lub strumieniami. 

W układach sterowania silnikami indukcyjnymi można wyróżnić następujące stałe czasowe:

![Untitled](4%20Analiza%20proceso%CC%81w%20w%20elektromechanicznym%20systemie%20c409d31dd1a34dffb13f506dcd4e9107/Untitled%207.png)

- **stałą czasową obwodu stojana Ts** - człon stojana jest inercyjny i czas narostu prądu jest skończony
- **stałą czasową obwodu wirnika Tr** - człon wirnika jest inercyjny i w nim czas narostu prądu i procesów elektromagnetycznych jest znacznie dłuższy niż w obwodzie stojana
- **stałą czasową mechaniczną TM** - połączenie mechaniczne przedstawia się jako człon całkujący moment dynamiczny na prędkość i jego stała czasowa wynika z niezerowej bezwładności wirnika i wału
- **stałą czasową przekształtnika TV** - tranzystory mają skończony czas przełączania i wprowadzają do układu sterowania kolejną stałą czasową

**Współczynniki tłumienia**

W przypadku silnika indukcyjnego, można wyróżnić drgania elektromagnetyczne w uzwojeniach (stany nieustalone), drgania wynikające z regulacji i objawiające się oscylacjami prędkości oraz drgania skrętne, potencjalnie wynikające z elastycznych połączeń. 

Można zatem wyróżnić współczynniki:

- **tłumienia drgań elektromagnetycznych** - czyli rezystancję poszczególnych uzwojeń;
- **tłumienia oscylacji układu regulacji** - czyli współczynnik ustalany przy doborze docelowej transmitancji, osiągany dzięki odpowiednim nastawom regulatorów
- **tłumienia drgań skrętnych** - ponownie, wynikający z doboru nastaw regulatorów w układzie regulacji

### Najważniejsze punkty

- silnik indukcyjny modeluje się jako układ trójfazowy, ale dla wygody przekształca go do postaci wektorowej, w której każdy wektor opisuje wszystkie trzy fazy jednocześnie
- model wektorowy silnika indukcyjnego składa się z równań obwodu stojana, wirnika, połączenia mechanicznego oraz równań strumieni stojana i wirnika oraz równania momentu elektromagnetycznego
- wektorowe równania stanu opisują wszystkie zmienne w układzie silnika indukcyjnego; najważniejsze z nich to równanie stanu na moment elektromagnetyczny - mówi ono, że sterowanie momentem wymaga kontroli nad zmiennymi elektromagnetycznymi takimi jak prądy lub strumienie
- współczynniki tłumienia: tłumienie drgań elektromagnetycznych, tłumienie drgań układu regulacji, tłumienia drgań skrętnych w układzie dwumasowym; najważniejsze - tłumienie drgań układu regulacji, zgodnie z metodą rozłożenia biegunów
- stałe czasowe: stojana (opóźnienie w generowaniu prądu z napięcia), wirnika (to samo ale dla wirnika), mechaniczna (opóźnienie w generowaniu prędkości z różnic momentów)

### **Źródła**

[1] Materiały i notatki z wykładu *Elektromechaniczne układy napędowe*

[2] Materiały i notatki z wykładu *Automatyka napędu elektrycznego - podstawy*

[3] Notatki z wykładu *Komputerowo wspomagane projektowanie układów regulacji*

### d) wyznaczanie współczynników elektromagnetycznych i stałych czasowych dla elektromechanicznego systemu napędowego z silnikiem obcowzbudnym prądu stałego i z silnikiem indukcyjnym

**Silnik obcowzbudny**

Silniki obcowzbudne prądu stałego można na podstawie ich obwodów twornika i wzbudzenia opisać za pomocą prostego układu równań Kirchhoffa. W przypadku takiego silnika, można wyróżnić następujące stałe czasowe:

- **elektromagnetyczną stałą czasową** obwodu twornika, opisaną równaniem $T_e=\frac{L_t}{R_t}$, w którym Lt i Rt to odpowiednio indukcyjność i rezystancja obwodu twornika
- **elektromechaniczną stałą czasową**, opisaną równaniem $T_M=\frac{J\Omega_0}{M_N}$ czyli zgodnie z momentem znamionowym, prędkością biegu jałowego i bezwładnością masy wirnika
- **stałą czasową układu przekształtnika,** czyli czas przełączania zaworów;

Oraz następujące współczynniki:

- **współczynnik wzmocnienia obwodu twornika**, opisany równaniem $K_t=\frac{U_{tN}}{I_{tN}R_{tN}}$, czyli wiążący wielkości obwodu twornika odpowiedzialne za prąd

Powyższe wielkości definiują kolejno: czas odpowiedzi obwodu twornika na napięcie, czas narastania prędkości przy pojawieniu się momentu dynamicznego, czas przełączania przekształtnika, wzmocnienie członu twornika.

**Silnik indukcyjny**

W przypadku silnika obcowzbudnego, można wyróżnić następujące stałe czasowe:

- **stałą czasową obwodu stojana $T_s=\frac{L_s}{R_s}$**
- **stałą czasową obwodu wirnika $T_r=\frac{L_r}{R_r}$**
- **stałą czasową mechaniczną $T_M=\frac{J\Omega_0}{M_N}$**
- **stałą czasową przekształtnika $T_0$**

Oraz następujące współczynniki elektromagnetyczne:

- **poślizg** czyli stosunek różnicy prędkości wirowania pola stojana i wirnika do prędkości wirowania pola stojana (prędkości synchronicznej)
- **liczbę par biegunów**, czyli wielkość konstrukcyjną wiążącą prędkość elektryczną pola magnetycznego z prędkością mechaniczną wirnika

Z czego powyższe wielkości można w większości wyznaczyć z parametrów znamionowych silnika, z wyjątkiem poślizgu który wynika z obciążenia silnika oraz inercji J która wynika z masy wirnika. 

### Najważniejsze punkty

- stałe czasowe silników można wyznaczać z ich parametrów znamionowych
- stałe czasowe SPS: zależne od bezwładności wirnika (mechaniczna) oraz R i L uzwojenia twornika (elektromagnetyczna)
- stałe czasowe SI: zależne bezwładności wirnika (mechaniczna), R i L uzwojenia stojana (stała stojana), R i L obwodu wirnika (stała wirnika)
- współczynniki elektromagnetyczne ustala się na podstawie pomiarów maszyn lub z ich kart katalogowych

### **Źródła**

[1] Materiały i notatki z wykładu *Elektromechaniczne układy napędowe*