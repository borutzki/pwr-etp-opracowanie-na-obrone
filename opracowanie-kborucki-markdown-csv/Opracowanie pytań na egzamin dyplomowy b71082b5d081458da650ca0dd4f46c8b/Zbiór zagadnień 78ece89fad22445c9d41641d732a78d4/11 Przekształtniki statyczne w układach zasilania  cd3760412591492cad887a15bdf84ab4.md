# 11. Przekształtniki statyczne w układach zasilania i sterowania

Status: Zrobione

### a) przekształtniki AC – DC, prostowniki niesterowane i sterowane, praca w zakresie prądów ciągłych i impulsowych, korektory współczynnika mocy – PFC

**Przekształtniki AC-DC**

Przekształtniki AC-DC to po prostu układy prostownicze, przekształcające przemienne napięcia na napięcia stałe o różnych parametrach (mniejsza lub większa wartość, mniej lub bardziej wygładzone). Przekształtniki AC-DC dzieli się na sterowane i niesterowane oraz zależnie od liczby pulsów (liczby elementów elektronicznych). Wyróżnia się też dwa stany pracy - w zakresie prądów ciągłych i impulsowych.

**Prostowniki niesterowane i sterowane**

**Prostowniki niesterowane** to najprostsze możliwe układy, w których komutacja napięć i prądów zachodzi w sposób naturalny, bez żadnego sterowania z zewnątrz. Przekształtniki tego typu **oparte są o różne układy diod**. 

**Prostowniki sterowane** w przeciwieństwie do prostowników niesterowanych, umożliwiają kontrolę nad wyjściowymi wartościami napięć oraz prądów. W tego typu przekształtnikach, **zamiast diod stosuje się tyrystory lub tranzystory z odpowiednimi układami sterowania**, najczęściej poprzez modulację szerokości impulsów. 

Prostowniki sterowane i niesterowane występują w analogicznych topologiach, różnią się natomiast typem urządzeń prostujących (diody albo tranzystory / tyrystory). Ogólnie, można wśród nich wyróżnić:

- **prostowniki jednofazowe jednopulsowe**: stosuje się w nich jedną diodę, przepuszczającą tylko jedną połówkę sinusoidy
    
    ![Untitled](11%20Przekszta%C5%82tniki%20statyczne%20w%20uk%C5%82adach%20zasilania%20%20cd3760412591492cad887a15bdf84ab4/Untitled.png)
    
- **prostowniki jednofazowe dwupulsowe**: układy te składają się z dwóch lub czterech diod, które umożliwiają przekształcanie obydwu połówek sinusoidy napięcia na jedną stronę, co zapewnia brak przerw w przebiegach
    
    ![Untitled](11%20Przekszta%C5%82tniki%20statyczne%20w%20uk%C5%82adach%20zasilania%20%20cd3760412591492cad887a15bdf84ab4/Untitled%201.png)
    
- **prostowniki trójfazowe jednopołówkowe:** układy tego typu posiadają jeden element prostujący w każdej fazie, co powoduje że na wyjściu pojawiają się nałożone napięcia tylko “górnych” połówek sinusoid wejściowych napięć
    
    ![Untitled](11%20Przekszta%C5%82tniki%20statyczne%20w%20uk%C5%82adach%20zasilania%20%20cd3760412591492cad887a15bdf84ab4/Untitled%202.png)
    
- **prostowniki trójfazowe dwupołówkowe:** układy te są najczęściej stosowane w przypadku sterowania silnikami, ponieważ charakteryzują się przetwarzaniem górnych i dolnych połówek sinusoid, co zapewnia najmniejsze pulsacje napięcia na wyjściu takiego układu.
    
    ![Untitled](11%20Przekszta%C5%82tniki%20statyczne%20w%20uk%C5%82adach%20zasilania%20%20cd3760412591492cad887a15bdf84ab4/Untitled%203.png)
    

Generalnie przyjmuje się, że im więcej pulsów ma napięcie wyjściowe, tym lepsza jest jakość zasilania odbiornika DC oraz tym lepszy jest współczynnik mocy prostownika - czyli wypadkowo jego wydajność. 

Układy powyższych prostowników można budować również jako prostowniki sterowane. Wtedy układ sterowania powinien załączać w odpowiednich chwilach element sterowany (tyrystor lub tranzystor) tak, by na wyjściu pojawiało się napięcie o pożądanej wartości średniej. Poniżej przedstawiono animację pokazującą, jak działa tyrystor (niebieski sygnał to sygnał załączający przewodzenie tyrystora).

Zasadniczą zaletą prostowników sterowanych jest fakt, że umożliwiają dwukierunkowy przepływ energii - mogą więc działać również w stanie pracy falownikowej.

![https://upload.wikimedia.org/wikipedia/commons/0/07/Regulated_rectifier.gif](https://upload.wikimedia.org/wikipedia/commons/0/07/Regulated_rectifier.gif)

**Praca w zakresie prądów ciągłych i impulsowych**

Pracujący w zakresie prądów ciągłych prostownik ma składową stałą prądu większą, niż składowa zmienna. Jeżeli składowa zmienna staje się większa niż składowa stała, to pulsujący prąd w pewnych odcinkach czasu jest równy (lub mniejszy) 0. Mówi się wtedy o zakresie pracy prądów impulsowych. 

Pracę prądów nieciągłych można osiągnąć przy dużym wysterowaniu prostownika, przy niewielkiej indukcyjności odbiornika lub w przypadku, gdy odbiornik jest odbiorem RE lub RLE, gdzie prąd płynie tylko w chwilach, gdy napięcie na wyjściu prostownika jest wyższe niż napięcie na odbiorniku. 

![Untitled](11%20Przekszta%C5%82tniki%20statyczne%20w%20uk%C5%82adach%20zasilania%20%20cd3760412591492cad887a15bdf84ab4/Untitled%204.png)

Podczas pracy w zakresie prądów nieciągłych, napięcie przestaje zmieniać się proporcjonalnie do współczynnika wypełnienia tyrystora. Charakterystyka sterowania staje się nieliniowa i *miękka*. Żeby utrzymać stały poziom napięcia, trzeba zmieniać kąt wysterowania.

Innymi wadami pracy nieciągłej jest pozorny wzrost impedancji wyjścia przekształtnika, napięcie staje się silnie zależne od odbioru przekształtnika, można też stracić nad nim kontrolę w przypadku szybkich zmian odbioru. 

**Korektory współczynnika mocy**

Prąd pobierany z sieci przez prostowniki (oraz ogólnie, zasilacze), jest na ogół silnie odkształcony, zwłaszcza w przypadku prostowników jednopulsowych. Prąd w takich układach jest często impulsowy (np. do ładowania kondensatora), w związku z czym współczynnik mocy utrzymuje się na niskim poziomie - co jest niejako wyznacznikiem jakości zasilania. 

Korekcję współczynnika mocy PFC można wykonywać w sposób pasywny i aktywny. 

**Pasywna korekcja** polega na stosowaniu **filtrów pasywnych**, czyli **elementów LC wpiętych do obwodu prostownika**. Stosuje się tu filtry LC na wyjściu lub wejściu prostownika. Mogą to też być po prostu cewki lub kondensatory. Innym podejściem jest wstawienie układów filtrów pasmowo-przepustowych ograniczających wysokie harmoniczne prądu. 

![Untitled](11%20Przekszta%C5%82tniki%20statyczne%20w%20uk%C5%82adach%20zasilania%20%20cd3760412591492cad887a15bdf84ab4/Untitled%205.png)

Korekcja tego typu pozwala na poprawę współczynnika mocy tylko do pewnego stopnia. Układy te są proste w konstrukcji, nie generują zakłóceń elektromagnetycznych i nie generują strat mocy na przełączenia. Są jednak często duże gabarytowo.

**Aktywna korekcja** współczynnika mocy polega na stosowaniu dodatkowego przekształtnika za obwodem prostownika, najczęściej przkeształtnika typu Boost. Jest to przekształtnik sterowany ze sprzężeniem zwrotnym od docelowej wartości napięcia wyjściowego.

![Untitled](11%20Przekszta%C5%82tniki%20statyczne%20w%20uk%C5%82adach%20zasilania%20%20cd3760412591492cad887a15bdf84ab4/Untitled%206.png)

Istnieje kilka różnych podejść do korekcji aktywnej współczynnika mocy. Można rozróżnić układy z ciągłym, nieciągłym lub granicznym prądem dławika (CICM vs. DCM vs. BCM). Korektory projektuje się na ogół do pracy z ciągłym lub granicznym prądem dławika (niespadającym do zera). Prąd cewki przekształtnika jest sterowany w określony sposób za pomocą PWM - kluczowanie następuje w przypadku wykrycia przejścia prądu przez zero.

Dopasowanie napięcia wyjściowego za prostownikiem diodowym pozwala na ograniczanie prądów wyższych harmonicznych, zwiększenie współczynnika mocy oraz zmniejszenie kondensatora filtrującego, przy zapewnieniu lepszego sterowania napięciem na wyjściu. 

**Źródła**

[1] [https://pl.wikipedia.org/wiki/Prostownik](https://pl.wikipedia.org/wiki/Prostownik)

[2] [https://eia.pg.edu.pl/documents/184045/282792/prostownik_DML.pdf](https://eia.pg.edu.pl/documents/184045/282792/prostownik_DML.pdf)

[3] Ned Mohan - *Power Electronics*

[4] [https://elektronikab2b.pl/technika/15244-pasywne-i-aktywne-uklady-korekcji-wspolczynnika-mocy/strona/1](https://elektronikab2b.pl/technika/15244-pasywne-i-aktywne-uklady-korekcji-wspolczynnika-mocy/strona/1)

### b) prostowniki aktywne

**Prostowniki aktywne** to układy prostowników, w których **zamiast diod** prostowniczych **zastosowane są tranzystory** (najczęściej MOSFET lub JBT). Prostowniki aktywne w porównaniu do pozostałych typów prostowników, są **sterowane w układzie bardziej złożonym**, przy czym podstawową metodą sterowania jest tu PWM. 

![Untitled](11%20Przekszta%C5%82tniki%20statyczne%20w%20uk%C5%82adach%20zasilania%20%20cd3760412591492cad887a15bdf84ab4/Untitled%207.png)

Jedną z cech prostowników aktywnych jest **możliwość ich łatwego przystosowania do pracy czterokwadrantowej**, tj. z możliwością nie tylko pobierania energii z sieci, lecz również zwrotu energii do sieci. W klasycznych strukturach, możliwość zwrotu energii do sieci wymagała zastosowania dodatkowego przekształtnika. Zastosowanie sterowanych przez PWM prostowników aktywnych pozwala więc ograniczyć liczbę elementów elektronicznych - i przy tym także awaryjność układu. 

![Untitled](11%20Przekszta%C5%82tniki%20statyczne%20w%20uk%C5%82adach%20zasilania%20%20cd3760412591492cad887a15bdf84ab4/Untitled%208.png)

Innymi zaletami prostowników aktywnych są możliwość pracy przy **większej efektywności** niż w przypadku innych prostowników oraz **możliwość aktywnej kompensacji mocy biernej** (sterowanie prądem wejścia tak, by był kształtem dopasowany do sinusoidy napięcia na wejściu). 

Metody sterowania prostownikami aktywnymi są często rozbudowane, ale istnieje tu **możliwość zastosowania metod opartych na sterowaniu PWM**, które umożliwiają wykorzystanie takich cech prostowników aktywnych, jak kompensacja współczynnika mocy.

Do powyższych metod należą **metody wektorowe**. Można wśród nich wymienić:

- **VOC**: napięciowo-zorientowana, polegająca na kontrolowaniu położenia i amplitudy wektora prądu sieci względem wektora napięcia sieci
- **VFOC**: strumieniowo-zorientowana, polegająca na kontrolowaniu położenia i amplitudy wektora prądu sieci względem wektora wirtualnego strumienia sieci
- **DPC**: *direct power control -* metoda bezpośredniego sterowania mocą, w której sterowane są wartości chwilowe mocy czynnej i biernej przenoszonej przez prostownik; istnieją dwa warianty tej metody:
    - **V-DPC**: zorientowane napięciowo DPC, gdzie kontrola przepływu mocy czynnej i biernej realizowana jest na podstawie wiedzy o module i położeniu wektora napięcia sieci
    - **VF-DPC**: zorientowane strumieniowo DPC, gdzie kontrola przepływu mocy czynnej i biernej realizowana jest na podstawie wiedzy o module i położeniu wektora wirtualnego strumienia sieci.
    
    ![Untitled](11%20Przekszta%C5%82tniki%20statyczne%20w%20uk%C5%82adach%20zasilania%20%20cd3760412591492cad887a15bdf84ab4/Untitled%209.png)
    

**Źródła**

[1] [https://en.wikipedia.org/wiki/Active_rectification](https://en.wikipedia.org/wiki/Active_rectification)

[2] [http://kmnipe.pwr.edu.pl/files/prv/id35/zn-lab/ane/ANEZW/Cwiczenie6.pdf](http://kmnipe.pwr.edu.pl/files/prv/id35/zn-lab/ane/ANEZW/Cwiczenie6.pdf)

### c) impulsowe przekształtniki DC – DC prądu stałego z nieizolowanym wejściem i wyjściem, przetwornice z izolowanym wejściem i wyjściem

Przekształtniki DC-DC prądu stałego służą do przekształcania napięć i prądów stałych z jednego poziomu na drugie. Można wyróżnić kilka głównych topologii tego typu przekształtników, zależnie od funkcji i zastosowanej izolacji wejścia lub wyjścia. 

![Untitled](11%20Przekszta%C5%82tniki%20statyczne%20w%20uk%C5%82adach%20zasilania%20%20cd3760412591492cad887a15bdf84ab4/Untitled%2010.png)

Nazwa *impulsowe* pochodzi od zasady ich działania - są to przekształtniki z łącznikiem w formie sterowanego tranzystora (lub kilku), przewodzącego tylko w odpowiednich chwilach w okresie sterowania. Poniżej omówiono podstawowe topologie przekształtników impulsowych DC-DC.

**Przekształtnik Buck (obniżający napięcie)**

Przekształtnik typu Buck służy do obniżania napięcia. Jego zasada działania polega na tym, że łącznik na wejściu jest załączany i wyłączany. Wyłączenie tranzystora sprawia, że ze źródła do odbiornika nie płynie prąd, natomiast prąd istniejący już w odbiorniku (nie znika, bo w obwodzie jest cewka lub filtr LC) zamyka się przez diodę zerową. Im dłużej jest zamknięty tranzystor, tym wyższe jest napięcie na odbiorniku - przy czym nie będzie ono wyższe niż na wejściu przekształtnika. Na odbiorniku naprzemiennie pojawia się więc napięcie zasilania i napięcie cewki przekształtnika.

Na przekształtniku typu Buck, na wyjściu odbiornika prąd jest ciągły.

![Untitled](11%20Przekszta%C5%82tniki%20statyczne%20w%20uk%C5%82adach%20zasilania%20%20cd3760412591492cad887a15bdf84ab4/Untitled%2011.png)

**Przekształtnik Boost (podwyższający napięcie)**

W przekształtniku typu Boost, gdy tranzystor jest załączony, prąd płynie przez niego (zwarcie), ładując cewkę L. Gdy tranzystor jest wyłączony, zsumowane napięcie źródła oraz rozładowującej się cewki (energia pola magnetycznego cewki) podawane są na odbiornik. Wyłączenie tranzystora na stałe oznacza napięcie na wyjściu takie, jak na wejściu. Im wyższy współczynnik wypełnienia, tym wyższe napięcie na wyjściu przekształtnika.

Na przekształtniku typu boost, prąd wejściowy jest ciągły.

![Untitled](11%20Przekszta%C5%82tniki%20statyczne%20w%20uk%C5%82adach%20zasilania%20%20cd3760412591492cad887a15bdf84ab4/Untitled%2012.png)

**Przekształtnik Buck-Boost (obniżająco-podwyższający napięcie)**

Przekształtnik Buck-Boost łączy w sobie topologie Buck i Boost. Pozwala on zarówno na podwyższanie jak i obniżanie napięcia, przy czym na jego wyjściu napięcie ma polaryzację odwrotną niż na wejściu. 

Gdy tranzystor jest załączony, cewka L jest ładowana i prąd płynie tylko przez nią (w kierunku odbiornika - blokuje go dioda). Wyłączenie tranzystora sprawia, że na rozładowującej się cewce pojawia się napięcie, a prąd cewki rozładowuje się przez odbiornik. Stąd można zauważyć, że napięcie na odbiorniku można obniżyć praktycznie do 0 jak w przekształtniku Buck, można je też odpowiednią modulacją podwyższyć, modulując jak w przekształtniku Boost.

![Untitled](11%20Przekszta%C5%82tniki%20statyczne%20w%20uk%C5%82adach%20zasilania%20%20cd3760412591492cad887a15bdf84ab4/Untitled%2013.png)

**Przekształtnik Čuka**

Przekształtnik Čuka to alternatywna topologia złożonego przekształtnika podwyższająco-obniżającego napięcie. W tym przekształtniku, podobnie jak w buck-boost, napięcie na wyjściu ma polaryzację odwrotną od wejścia. 

Gdy tranzystor jest wyłączony, prąd obydwu cewek zamyka się przez diodę. Kondensator C1 jest ładowany zarówno ze źródła, jak i z cewki L1. Energia magazynowana w L2 zasila natomiast odbiornik. 

Gdy tranzystor jest załączony, napięcie naładowanego kondensatora C1 blokuje diodę D2, natomiast prądy cewek L1 i L2 płyną przez tranzystor. Kondensator oddaje przy tym energię do odbiornika i cewki L2. Cewka L1 jest ładowana. 

Zaletą przekształtnika Čuka jest możliwość zredukowania praktycznie do 0 pulsacji prądu. Wadą - to, że do tego wygładzenia prądu potrzebuje relatywnie dużego kondensatora. 

![Untitled](11%20Przekszta%C5%82tniki%20statyczne%20w%20uk%C5%82adach%20zasilania%20%20cd3760412591492cad887a15bdf84ab4/Untitled%2014.png)

**Przekształtnik wielokwadrantowy (mostkowy lub półmostkowy)**

Przekształtnik mostkowy ma tę zaletę, że może działać czterokwadrantowo, czyli umożliwia przepływ energii w dwie strony. Jego zasada działania jest podobna do falownika. 

Sterowanie tego przekształtnika można realizować na dwa sposoby: PWM unipolarny lub bipolarny. W unipolarnym gałęzie mostka traktowane są jako dwie pary i sterowane jako pary. Napięcie na wyjściu przyjmuje tylko jedną biegunowość W bipolarnym - każdy tranzystor sterowany jest osobno, a napięcie przyjmuje trzy stany: 0, +1, -1 Ud. 

![Untitled](11%20Przekszta%C5%82tniki%20statyczne%20w%20uk%C5%82adach%20zasilania%20%20cd3760412591492cad887a15bdf84ab4/Untitled%2015.png)

W przypadku układu mostkowego, można zmieniać zarówno kierunek prądu, jak i napięcia. Podobną topologią jest układ półmostkowy, w którym można zmienić tylko kierunek prądu. 

![Untitled](11%20Przekszta%C5%82tniki%20statyczne%20w%20uk%C5%82adach%20zasilania%20%20cd3760412591492cad887a15bdf84ab4/Untitled%2016.png)

**Przekształtnik Flyback (dwutaktowy)**

Przekształtnik Flyback oparty jest na topologii Buck-Boost. Ogólna koncepcja polega na tym, że do przekształtnika Buck-Boost, na jedną cewkę nawija się drugą, co wypadkowo tworzy transformator. 

Gdy tranzystor S1 jest załączony, energia jest magazynowana w transformatorze L1, natomiast dioda D1 jest spolaryzowana zaporowo. Odbiornik pobiera energię z kondensatora C1. 

Gdy tranzystor jest wyłączony, napięcie indukuje się w uzwojeniu wtórnym, dioda staje się spolaryzowana w kierunku przewodzenia, i wypadkowo energia z transformatora jest przekazywana do kondensatora i odbiornika. 

Układy Flyback służą do obniżania oraz podwyższania napięcia.

![Untitled](11%20Przekszta%C5%82tniki%20statyczne%20w%20uk%C5%82adach%20zasilania%20%20cd3760412591492cad887a15bdf84ab4/Untitled%2017.png)

**Przekształtnik Forward (jednotaktowy)**

Układ typu forward oparty jest o topologię Buck i posiada transformator zapewniający izolację galwaniczną, którego przekładnia może jednocześnie określać wypadkowe wzmocnienie całego układu. Układy tego typu pracują na wysokich częstotliwościach.  

Gdy tranzystor T1 jest załączony, dioda D1 przewodzi - napięcie ze strony pierwotnej jest transformowane na stronę wtórną, zasilając odbiornik. Gdy tranzystor T1 jest wyłączony, przewodzą diody D2 i D3. Dioda D2 zamyka prąd odbiornika (płynący wciąż, bo cewka L utrzymuje napięcie). Dioda D3 przepuszcza prąd rozmagnesowujący.

Przetwornica tego typu służy do obniżania napięcia, przy czym współczynnik wypełnienia współgra tu z przekładnią transformatora. Transformator nie służy tu do magazynowania energii, służy jedynie do jej przekazywania. Należy jednak brać pod uwagę energię magazynowaną w transformatorze, bo niepilnowana może popsuć przekształtnik. 

![Untitled](11%20Przekszta%C5%82tniki%20statyczne%20w%20uk%C5%82adach%20zasilania%20%20cd3760412591492cad887a15bdf84ab4/Untitled%2018.png)

**Push-pull**

Przekształtnik Push-Pull bazuje na układzie falownika push-pull. Na wejście transformatora wysokiej częstotliwości podawany jest prostokątny sygnał AC. Układy tego typu steruje się metodą PWM.

Gdy tranzystor T1 lub T2 jest załączony, energia jest podawana przez transformator na stronę wtórną. Prąd przez diody D1 lub D2 płynie do obciążenia poprzez cewkę. Gdy tranzystor jest wyłączony, energia do odbiornika płynie z cewki przez dwie połówki uzwojenia transformatora.

Napięcie na wyjściu zależy od przekładni transformatora oraz współczynnika wypełnienia. Działanie jest tu podobne do przekształtnika typu Buck, więc napięcie na stronie wtórnej, podwyższone przez transformator, jest obniżane przez współczynnik wypełnienia. 

![Untitled](11%20Przekszta%C5%82tniki%20statyczne%20w%20uk%C5%82adach%20zasilania%20%20cd3760412591492cad887a15bdf84ab4/Untitled%2019.png)

**Przekształtnik półmostkowy**

Przekształtnik półmostkowy bazuje na topologii buck. Transformator ma końcówkę uzwojenia wpiętą między dwa kondensatory, co pozwala na magazynowanie większej ilości energii. 

W układzie tego typu, tranzystory T1 i T2 załączane są naprzemiennie, jest też okres gdy obydwa są wyłączone. Załączenie tranzystorów przekazuje energię na stronę wtórną. Gdy tranzystory są wyłączone, prąd odbioru zamyka się przez diody D5 i D6, cewkę oraz obciążenie. Czyli napięcie jest znowu podwyższane przez transformator, obniżane przez układ sterowania. 

![Untitled](11%20Przekszta%C5%82tniki%20statyczne%20w%20uk%C5%82adach%20zasilania%20%20cd3760412591492cad887a15bdf84ab4/Untitled%2020.png)

**Przekształtnik mostkowy**

Przekształtnik mostkowy jest podobny do półmostkowego, ale zawiera dwukrotnie większą liczbę łączników. Oznacza to, że tranzystory są mniej obciążone, nie stosuje się tu też kondensatorów dzielących napięcie wejściowe transformatora na pół (można natomiast wrzucić kondensator przed układ mostkowy).

Układ sterowania jest tu nieco bardziej złożony, bo wymaga kluczowania czterech tranzystorów. Tranzystory kluczowane są parami. 

![Untitled](11%20Przekszta%C5%82tniki%20statyczne%20w%20uk%C5%82adach%20zasilania%20%20cd3760412591492cad887a15bdf84ab4/Untitled%2021.png)

**Stosowanie izolacji**

Izolację w przekształtnikach stosuje się między innymi po to, by:

- zapewnić bezpieczeństwo w razie awarii - części o różnych poziomach napięcia są od siebie odizolowane;
- zapewnić większą odporność na zakłócenia sieciowe - obwody doziemne strony pierwotnej i wtórnej są od siebie oddzielone
- znaczne obniżenie napięć bez podawania ich bezpośrednio na układ przekształtnika

Izolacja jednak podwyższa koszty przekształtników, komplikuje ich układy i zwiększa gabaryty.

**Źródła**

[1] Materiały oraz notatki z wykładu *Przekształtniki energoelektroniczne w układach zasilania i sterowania 1* (w tym skany książek od prowadzącego)

[2] Materiały z wykładu *Energoelektronika 1*

[3] Ned Mohan - *Power Electronics*

[4] [https://www.quora.com/Why-do-we-use-an-isolation-transformer-in-a-DC-DC-converter](https://www.quora.com/Why-do-we-use-an-isolation-transformer-in-a-DC-DC-converter)

[5] [https://www.digikey.com/en/articles/use-isolated-dc-dc-converters-with-embedded-transformers-to-ease-assembly](https://www.digikey.com/en/articles/use-isolated-dc-dc-converters-with-embedded-transformers-to-ease-assembly)

### d) oddziaływanie przekształtników na sieć zasilającą, podstawowe sposoby ograniczenia tego oddziaływania

**Oddziaływanie przekształtników na sieć zasilającą**

- **pobieranie z sieci odkształconych prądów:** podstawowy problem, z którego powstają inne; prądy pobierane przez odbiorniki zasilane z przekształtników są niesinusoidalne i jako takie mają zawartość wyższych harmonicznych, które reagują z innymi elementami sieci (reaktancje i pojemności linii, etc.)
- **harmoniczne**: działające układy prostowników diodowych (mostek Graetza) lub tyrystorowych pobierają z sieci prąd odkształcony, który płynąć przez przewody zasilające powoduje wygenerowanie wyższych harmonicznych w napięciu zasilającym; podobnie układy zasilania napędów elektrycznych mogą wprowadzać do sieci wyższe harmoniczne ze względu na rodzaj sterowania PWM
- **trzecia harmoniczna**: bardzo duża liczba odbiorników zasilanych z przekształtników generuje bardzo duże prądy trzeciej harmonicznej, które zamykają się przez przewody neutralne instalacji trójfazowych - co w przypadku instalacji w starych budynkach grozi nawet pożarami
- **składowa przeciwna:** pojawienie się w sieci zasilającej składowej przeciwnej powoduje, że moment obrotowy silników może zostać obniżony - jest to spowodowane przepływem prądów harmonicznych wyższych rzędów
- **obniżenie współczynnika mocy**: pobieranie z sieci odkształconych prądów sprawia, że odbiorniki mają z punktu widzenia sieci niski współczynnik mocy - zatem wypadkowo sprawność urządzeń jest niższa ze względu na moc bierną deformacji; oprócz tego może dochodzić do przesunięcia fazowego prądów względem napięć
- **spadki napięć:** przekształtniki impulsowe działają praktycznie w stanach zwarć, co może powodować ucinanie przebiegu sinusoidy w sieci podczas działania takich urządzeń - zwłaszcza w stanach komutacji
- **zakłócenia wysokoczęstotliwościowe:** szybkie przełączenia napięć dużej wartości oznaczają bardzo duże stromości narostu fal napięciowych, co w efekcie oddziałując z pojemnościami sieci może generować znaczne przepięcia i uszkadzać izolację
- **zakłócenia elektromagnetyczne:** wyżej opisane przepięcia mogą też generować duże chwilowe prądy harmonicznych o wysokich częstotliwościach - przepływ tych prądów o dużych wartościach generuje fale elektromagnetyczne wysokich częstotliwości, które mogą oddziaływać z urządzeniami bezprzewodowymi, komputerami, etc. w pobliżu
- **indukowanie prądów w łożyskach silników:** przepływy wyższych harmonicznych przez uzwojenia silników mogą sprawiać, że strumienie magnetyczne indukowane dla tych harmonicznych zaczną indukować prądy w łożyskach silników
- **zjawiska rezonansowe:** pojawienie się wyższych harmonicznych może też powodować zjawiska rezonansowe, jak np. znaczne przepięcia na zaciskach silników prądu przemiennego, wiele razy w ciągu kilku sekund.

**Sposoby ograniczania przekształtników na sieć zasilającą**

- **ograniczanie stosowania niesterowanych lub tyrystorowych prostowników tylko do układów małej mocy**
- **stosowanie dławików:** dławiki wygładzają prąd, ograniczając tempo ładowania kondensatorów po stronie DC układów, co w efekcie zmniejsza zawartość prądów wyższych harmonicznych - co jest skuteczne zwłaszcza w układach PWM
- **izolacja harmonicznych**: poprzez zastosowanie transformatorów o połączeniach określonego typu, wyższe harmoniczne przestają być przenoszone do sieci (D/Y albo Y/Z układy połączeń)
- **metody wielopulsowe:** działające przekształtniki można synchronizować w taki sposób, by wzajemnie eliminowały generowane przez siebie harmoniczne - przydatne są tu transformatory o uzwojeniach generujących określone przesunięcia fazowe
- **filtry pasywne:** redukcję wyższych harmonicznych można osiągać przez stosowanie filtrów pasywnych szeregowych lub równoległych do odbiorników; filtry szeregowe w oparciu o rezonanse blokują określone harmoniczne, natomiast filtry równoległe je analogicznie zwierają ze sobą, przez co nie płyną one do odbiorników.
    
    ![Untitled](11%20Przekszta%C5%82tniki%20statyczne%20w%20uk%C5%82adach%20zasilania%20%20cd3760412591492cad887a15bdf84ab4/Untitled%2022.png)
    
- **filtry aktywne**
    - **układy korekcji współczynnika mocy:** specjalne przekształtniki dc-dc lub układy prostowników sterowanych w określony sposób pozwalają na sterowanie poborem mocy biernej oraz zawartością harmonicznych w pobieranych prądach; takie układy stosuje się przede wszystkim w prostownikach diodowych
        
        ![Untitled](11%20Przekszta%C5%82tniki%20statyczne%20w%20uk%C5%82adach%20zasilania%20%20cd3760412591492cad887a15bdf84ab4/Untitled%2023.png)
        
    - **prostowniki aktywne:** specjalnie sterowane układy prostowników, które pozwalają na kontrolę współczynnika mocy - stosowane przede wszystkim tam gdzie potrzebna jest możliwość dwukierunkowego przepływu energii
- **kompensacja mocy biernej:** stosuje się tu specjalne kompensatory nadążne lub przełączalne baterie kondensatorów ze sterownikiem prądu indukcyjnego; bardziej optymalnym rozwiązaniem jest tu jednak stosowanie filtrów aktywnych

**Źródła**

[1] Angelo Baggini - *Handbook of power quality*

[2] Ned Mohan - *Power Electronics*

[3] [https://bezel.com.pl/2018/08/01/oddzialywanie-na-siec-zasilajaca/](https://bezel.com.pl/2018/08/01/oddzialywanie-na-siec-zasilajaca/)