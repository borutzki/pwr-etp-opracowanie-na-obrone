# 1. Wybrane zagadnienia teorii obwodów

Status: Zrobione

### a) zastosowanie grafów przepływowych i schematów blokowych do analizy obwodów

**Grafy przepływowe**

Grafy przepływowe to sposób opisu przesyłu sygnałów w obwodach elektrycznych i układach automatyki. Opisując układ grafem przepływowym, zmienne układu rysuje się jako **węzły** połączone **strzałkami** wskazującymi **kierunek przepływu sygnału**. Założeniami tej metody jest fakt, że **sygnały mogą płynąć w tylko jednym kierunku**, określonym końcem strzałki. Powiązania są zatem przyczynowo-skutkowe. 

![Podstawowy zapis grafu przepływowego. x1 i y1 to zmienne, a11 to transmitancja której poddawany jest sygnał.](1%20Wybrane%20zagadnienia%20teorii%20obwodo%CC%81w%203dbd4542e315461ebb4f5d3bdda661d5/Untitled.png)

Podstawowy zapis grafu przepływowego. x1 i y1 to zmienne, a11 to transmitancja której poddawany jest sygnał.

**Każda strzałka ma natomiast przypisaną transmitancję**, przez którą mnożony jest sygnał przekształcany z jednej zmiennej w drugą. Wykorzystanie grafów przepływowych i ich dostępnych przekształceń pozwala na obliczenie wypadkowej transmitancji całego rozpatrywanego układu. Do takich obliczeń wykorzystuję się **teorię grafów zorientowanych**.

Przykład zapisu czwórnika prądowego w postaci grafu przepływowego przedstawiono poniżej. 

![Przykładowy zapis czwórnika elektrycznego w postaci grafu przepływowego. y11, y21, y22 i y12 są tutaj transmitancjami pomiędzy zmiennymi. Należy tu zauważyć, że wejście i wyjście stanowią napięcia, natomiast pomiędzy nimi zmiennymi układu są prądy. Transmitancje opisują zatem, jak układ przekształca napięcia na prądy, a także jak prądy oddziałując z rezystancjami na wejściu i wyjściu pozwalają na uzyskanie napięć. ](1%20Wybrane%20zagadnienia%20teorii%20obwodo%CC%81w%203dbd4542e315461ebb4f5d3bdda661d5/Untitled%201.png)

Przykładowy zapis czwórnika elektrycznego w postaci grafu przepływowego. y11, y21, y22 i y12 są tutaj transmitancjami pomiędzy zmiennymi. Należy tu zauważyć, że wejście i wyjście stanowią napięcia, natomiast pomiędzy nimi zmiennymi układu są prądy. Transmitancje opisują zatem, jak układ przekształca napięcia na prądy, a także jak prądy oddziałując z rezystancjami na wejściu i wyjściu pozwalają na uzyskanie napięć. 

**Schematy blokowe**

Schematy blokowe to powszechniejsza, przynajmniej na W5, metoda przedstawiania układów automatyki czy obwodów elektrycznych. W schematach blokowych, **bloki są transmitancjami**, natomiast **połączenia między nimi są zmiennymi** - czyli zmienna jest jednocześnie wyjściem bloku i wejściem kolejnego. 

![Przykładowy układ regulacji automatyki ze sprzężeniem zwrotnym, zapisany w postaci schematu blokowego.](1%20Wybrane%20zagadnienia%20teorii%20obwodo%CC%81w%203dbd4542e315461ebb4f5d3bdda661d5/Untitled%202.png)

Przykładowy układ regulacji automatyki ze sprzężeniem zwrotnym, zapisany w postaci schematu blokowego.

Schematy blokowe można analizować przy wykorzystaniu tzw. **algebry schematów blokowych**, pozwalającej na upraszczanie układów wieloelementowych i sprowadzanie ich do pojedynczej transmitancji. 

**Podsumowanie**

Schematy blokowe oraz grafy przepływowe to metody matematyczne pozwalające opisywać rzeczywiste układy, złożone ze zbioru prostych elementów. Układy takie zapisuje się wybraną metodą, aby następnie analizować ich wypadkowy wpływ na przetwarzanie sygnału (zmiennej) wejściowego na wyjściowy.

Choć obie te metody mogą być stosowane dla różnego rodzaju układów fizycznych, to jednak ich główną domeną są układy regulacji automatycznej, a rzadziej obwody elektryczne.

### **Najważniejsze punkty**

- grafy przepływowe: węzły to zmienne, strzałki to transmitancje
- schematy blokowe: bloki to transmitancje, strzałki to sygnały
- obie metody pozwalają na uproszczenie analizy układów - redukcja schematów blokowych i grafów węzłowych

### **Źródła**

[1] [https://en.wikipedia.org/wiki/Signal-flow_graph](https://en.wikipedia.org/wiki/Signal-flow_graph)

[2] [https://pl.wikipedia.org/wiki/Graf_przepływu_sygnałów](https://pl.wikipedia.org/wiki/Graf_przep%C5%82ywu_sygna%C5%82%C3%B3w)

[3] [https://pl.wikipedia.org/wiki/Schemat_blokowy_(automatyka)](https://pl.wikipedia.org/wiki/Schemat_blokowy_(automatyka))

### b) obwody nieliniowe na przykładzie obwodu z łukiem elektrycznym i obwodów z rdzeniem ferromagnetycznym - zagadnienia stabilności i rezonansu

**Obwody elektryczne nieliniowe** to takie obwody, w których występuje **co najmniej jeden element o nieliniowej charakterystyce** lub kilka elementów nieliniowych, nierównoważących się nawzajem. **Element nieliniowy** to taki, którego **charakterystyka prądowo-napięciowa nie może być opisana równaniem prostej** **y=ax+b**. 

Zależnie od kształtu krzywej charakterystyki elementu, wyróżnia się elementy nieliniowe **symetryczne, niesymetryczne, jednoznaczne i wieloznaczne**. Symetryczne i niesymetryczne nazywa się zależnie od przebiegu charakterystyki w zakresie dodatnim i ujemnym. Jednoznaczne i wieloznaczne - zależnie od tego, czy pojawiają się w nich punkty na osi x z dwiema wartościami na osi y - czyli, w praktyce, wieloznaczne obwody to obwody z histerezą.

![Untitled](1%20Wybrane%20zagadnienia%20teorii%20obwodo%CC%81w%203dbd4542e315461ebb4f5d3bdda661d5/Untitled%203.png)

W obwodach nieliniowych obowiązują prawa Kirchhoffa, zasada kompensacji, twierdzenie Thevenina i twierdzenie Nortona. Nie obowiązują natomiast prawo Ohma, zasada superpozycji i zasada wzajemności. 

**Stabilność**

**Stabilność układu** definiuje się jako **zdolność tego układu do powrotu do punktu równowagi po zmianie wymuszenia lub wystąpieniu zakłócenia**. Znaczy to tyle, że w nowych warunkach pracy układ powinien przyjąć nowy punkt pracy zamiast np. w nieskończoność zwiększać obroty silnika czy prąd płynący przez obwód. 

Stabilność układów nieliniowych analizuje się przede wszystkim dwiema metodami Lapunowa. Pierwsza metoda Lapunowa to metoda pośrednia pozwalająca na badanie stabilności lokalnej, w obrębie pewnego punktu pracy. Druga metoda Lapunowa, nazywana bezpośrednią - służy do badania stabilności w ograniczonym lub nieograniczonym obszarze przestrzeni stanów układów nieliniowych.

**Rezonans**

Rezonans jest zjawiskiem fizycznym, w którym **przy określonej częstotliwości sił wymuszających następuje znaczne zwiększenie amplitudy drgań układu**. 

W obwodach elektrycznych, **rezonans jest zjawiskiem pojawiającym się, gdy częstotliwość wymuszenia** (np. napięcia) **odpowiada częstotliwości rezonansowej obwodu** (zależnej od impedancji elementów LC). **Moc bierna pobierana przez obwód spada do zera**.

W przypadku elementów LC **szeregowych**, występuje **rezonans napięciowy** i **prąd znacznie wzrasta**. W przypadku elementów LC **równoległych**, **prąd maleje praktycznie do zera**, ale jednocześnie **wzrastają znacznie napięcia na elementach obwodu**.  

Rezonans elektryczny można wykorzystać do kompensacji mocy biernej (przez wyzerowanie prądu składowej biernej, czyli rezonans prądów), a także jako filtry lub wzmacniacze określonych częstotliwości w radiotechnice.

Szczególnym typem rezonansu jest **ferrorezonans**. Ferrorezonans pojawia się w obwodach, w których **nieliniowa indukcyjność jest zasilona ze źródła z szeregowo wpiętą pojemnością i dojdzie do zakłócenia** np. w postaci załączenia nowego odbiornika. W takim przypadku mogą wystąpić **znaczne przetężenia i przepięcia** w obwodzie. 

**Praktyczną sytuacją** z ferrorezonansem jest np. wystąpienie w 3-fazowym układzie elektroenergetycznym **zakłócenia w jednej z faz**. Transformatory są elementami tylu L, linie kablowe - elementami typu C. Zakłócenie w jednej faz powoduje znaczne zmiany napięcia w pozostałych fazach. Ta gwałtowna zmiana może wywołać ferrorezonans, co z kolei może prowadzić do uszkodzenia izolacji w systemie.

**Obwód z łukiem elektrycznym**

Obwód prądu stałego z łukiem elektrycznym jest przykładem obwodu nieliniowego. W takim obwodzie, elementem nieliniowym jest sam łuk elektryczny. Jego charakterystyka przecina się z liniową charakterystyką obwodu w dwóch miejscach. Te dwa punkty nazywa się kolejno punktem równowagi chwiejnej (A) i punktem równowagi stabilnej (B). Punkty te wydzielają dwa obszary napięcia obwodu: zakres dodatni, przy którym $L\frac{di}{dt}>0$ oraz ujemny, przy którym $L\frac{di}{dt}<0$. W zakresie dodatnim, prąd łuku wzrasta. W zakresie ujemnym - maleje.

![Untitled](1%20Wybrane%20zagadnienia%20teorii%20obwodo%CC%81w%203dbd4542e315461ebb4f5d3bdda661d5/Untitled%204.png)

Wytrącenie łuku z punktu równowagi A poprzez zmniejszenie prądu, powoduje jego zgaszenie - wejście w zakres ujemny napięć i w związku z tym dalsze osłabienie prądu. Jeżeli prąd w tym punkcie równowagi się zwiększy, prąd zacznie rosnąć i łuk znajdzie się ostatecznie w nowym punkcie pracy, czyli B. Zgaszenie łuku oznacza zatem wytrącenie obwodu z punktu równowagi, czyli de facto jego destabilizację. 

![Untitled](1%20Wybrane%20zagadnienia%20teorii%20obwodo%CC%81w%203dbd4542e315461ebb4f5d3bdda661d5/Untitled%205.png)

**Obwód z rdzeniem ferromagnetycznym**

Obwód z rdzeniem ferromagnetycznym jest **obwodem nieliniowym** ze względu na **histerezę rdzenia** dławika, transformatora czy innej maszyny elektrycznej. Histereza opisuje zmianę indukcji magnetycznej materiału przy zmianie natężenia pola magnetycznego, któremu materiał jest poddawany. 

W obwodzie elektrycznym, histereza sprawia że **charakterystyka prądowo-napięciowa jest nieliniowa** i od pewnego punktu, zwanego nasyceniem, **zwiększenie płynącego w obwodzie prądu wymaga znacznego zwiększenia napięcia zasilającego**. Ta właściwość obwodów magnetycznych sprawia, że są one podatne na zjawisko **ferrorezonansu**. 

**Ferrorezonans** w przypadku nieliniowej cewki wynika z faktu **nieliniowego przebiegu reaktancji**. Pojawienie się nagłego skoku napięcia w systemie trójfazowym wskutek zakłócenia w jednej faz może sprawić, że zmiana indukcyjności cewki w połączeniu z pojemnością lini kablowych spowoduje pojawienie się rezonansu. Ferrorezonans, w przeciwieństwie do rezonansu liniowego, objawia się skokową zmianą prądu lub napięcia. To może prowadzić do uszkodzenia linii czy izolacji transformatorów. 

### Najważniejsze punkty

- obwody liniowe to takie, w których występuje element nieliniowy
- element nieliniowy to taki, którego charakterystyka prądowo-napięciowa nie jest linią prostą
- łuk elektryczny gasi się poprzez wytrącenie go poza stabilny punkt pracy na nieliniowej charakterystyce prądowo-napięciowej
- w obwodzie z rdzeniem magnetycznym występuje histereza - wzrost prądu powoduje duży wzrost napięcia lub wymaga dużego wzrostu napięcia
- histereza może powodować rezonans (ferrorezonans) gdy w układzie z elementem ferromagnetycznym dojdzie do zakłócenia - zmienia się jego reaktancja.

### **Źródła**

[1] [https://zoise.wel.wat.edu.pl/dydaktyka/WEL niestacjonarne/Wyklady/05_Obwody_nieliniowe_pradu_stalego.pdf](https://zoise.wel.wat.edu.pl/dydaktyka/WEL%20niestacjonarne/Wyklady/05_Obwody_nieliniowe_pradu_stalego.pdf)

[2] [https://pl.wikipedia.org/wiki/Stabilność_układu_automatycznej_regulacji#Stabilność_układów_nieliniowych_i_niestacjonarnych](https://pl.wikipedia.org/wiki/Stabilno%C5%9B%C4%87_uk%C5%82adu_automatycznej_regulacji#Stabilno%C5%9B%C4%87_uk%C5%82ad%C3%B3w_nieliniowych_i_niestacjonarnych)

[3] [https://docplayer.pl/3362988-3-luk-elektryczny-pradu-stalego-i-przemiennego.html](https://docplayer.pl/3362988-3-luk-elektryczny-pradu-stalego-i-przemiennego.html)

[4] [https://en.wikipedia.org/wiki/Resonance#RLC_series_circuits](https://en.wikipedia.org/wiki/Resonance#RLC_series_circuits)

[5] [https://en.wikipedia.org/wiki/Ferroresonance_in_electricity_networks](https://en.wikipedia.org/wiki/Ferroresonance_in_electricity_networks)

[6] [https://zoise.wel.wat.edu.pl/dydaktyka/ENERGETYKA/CW_6_Badanie_obwodow_magnetycznych.pdf](https://zoise.wel.wat.edu.pl/dydaktyka/ENERGETYKA/CW_6_Badanie_obwodow_magnetycznych.pdf)

### c) opis układu cyfrowego za pomocą równania różnicowego - transmitancja układu cyfrowego

**Układ cyfrowy** to układ **dyskretny**. Oznacza to, że przynajmniej jeden jego sygnał ma charakter dyskretny, czyli przyjmuje tylko określone wartości tylko dla określonych chwil czasu - tzw. próbki. Próbki sygnału są przesunięte od siebie w czasie o okres próbkowania. 

**Równania różnicowe**

Różnica pierwszego rzędu to po prostu zmiana wartości sygnału między następną a aktualną próbką, czyli: $\Delta f(n)=f(n+1)-f(n)$. Różnicę uzyskuję się poprzez zastąpienie czasu ciągłego (dt) operatorem dyskretnym różniczki czasu. Różnica jest analogią do różniczki w równaniu różniczkowym. Można też obliczać różnice wyższych rzędów, czyli niejako “pochodne” wyższych rzędów w równaniach dyskretnych.

Równanie różnicowe to sposób opisu układów dyskretnych analogiczny do zapisu układów ciągłych przez równania różniczkowe. Równanie różnicowe to suma różnic pierwszego i wyższych rzędów sygnału wejścia i wyjścia układu, zapisane w jednolitej postaci. Równanie różnicowe opisuje przebieg próbki w dziedzinie czasu i przyjmuje postać:

$$
\sum^n_{i=0}\frac{a_i}{T^i}\Delta^i y(k)=\sum^m_{l=0}\frac{n_l}{T^l}\Delta^l u(k)
$$

Powyższe równanie ustosunkowuje wejście do wyjścia układu. Parametr k jest numerem rozpatrywanej próbki.

**Transmitancja układu cyfrowego**

**Transmitancja dyskretna** układu cyfrowego to **stosunek dyskretnej transformaty Laplace’a sygnału wyjściowego Y(z) do transformaty sygnału wejściowego U(z)**, przy założeniu **zerowych warunków początkowych**. Stąd równanie $G(z)=\frac{Y(z)}{U(z)}$.

W celu uzyskania transformat równań różnicowych stosuje się tzw. **transformatę Z, czyli dyskretną wersję transformaty Laplace’a**. Transformata Laplace’a ciągi (bo próbki dyskretne opisuje się ciągami) przekształca do zespolonej zmiennej ciągłej *z*. Transformata stosowana w analizie układów dyskretnych jest **transformatą dwustronną**, czyli obejmuje obszar od minus do plus nieskończoności.  

Dzięki transmitancji dyskretnej, układy dyskretne można analizować w sposób podobny do układów ciągłych pomimo dyskretyzacji. Można przy tym stosować kryteria podobne do tych układów oraz korzystać z podobnej algebry schematów blokowych.

### Najważniejsze punkty

- równanie różnicowe to odpowiednik równania różniczkowego dla układów dyskretnych; różnica polega na zastosowaniu operatora dyskretnego $\Delta t$ zamiast ciągłego $dt$
- transmitancja układu dyskretnego to stosunek transformaty $***z***$ sygnału wyjścia takiego układu do transformaty $z$ sygnału wejścia
- transformata $z$ to dyskretna forma transformaty Laplace’a, która ciągi (sygnał dyskretny to ciąg) przekształca na ciągłe zmienne zespolone $z$

**Źródła**

[1] [https://home.agh.edu.pl/~sypka/dydaktyka/materialy/2E_CPS_2020-2021_08_B.pdf](https://home.agh.edu.pl/~sypka/dydaktyka/materialy/2E_CPS_2020-2021_08_B.pdf) 

[2] [http://wikizmsi.zut.edu.pl/uploads/6/63/Lab2_WDAC.pdf](http://wikizmsi.zut.edu.pl/uploads/6/63/Lab2_WDAC.pdf)

[3] [https://ioisp.el.pcz.pl/images/instrukcje/air/Komputery w sterowaniu/Cw.4 Dyskretne uklady liniowe.pdf](https://ioisp.el.pcz.pl/images/instrukcje/air/Komputery%20w%20sterowaniu/Cw.4%20Dyskretne%20uklady%20liniowe.pdf)

### d) splot dyskretny oraz odpowiedź układu cyfrowego na dowolne wymuszenie

**Odpowiedź impulsowa** h[n] układu cyfrowego to wyjście tego układu y[n], gdy wymuszenie x[n] jest deltą Koneckera $\delta[n]$ - pojedynczym impulsem o wartości 1. Typowa odpowiedź impulsowa układu cyfrowego wygląda tak:

![Untitled](1%20Wybrane%20zagadnienia%20teorii%20obwodo%CC%81w%203dbd4542e315461ebb4f5d3bdda661d5/Untitled%206.png)

Każda kolejna widoczna na niej “szpila” to wartość początkowa przemnożona kolejny raz przez 0,7 (niejako stała czasowa układu). Można to przedstawić w postaci następującego bloku:

![Untitled](1%20Wybrane%20zagadnienia%20teorii%20obwodo%CC%81w%203dbd4542e315461ebb4f5d3bdda661d5/Untitled%207.png)

Stąd, jeżeli na wejściu damy wymuszenie $x[n]=6\delta [n-2]$, wyglądające tak:

![Untitled](1%20Wybrane%20zagadnienia%20teorii%20obwodo%CC%81w%203dbd4542e315461ebb4f5d3bdda661d5/Untitled%208.png)

To **odpowiedź układu będzie przemnożeniem wymuszenia przez odpowiedź impulsową** - czyli jak poniżej:

![Untitled](1%20Wybrane%20zagadnienia%20teorii%20obwodo%CC%81w%203dbd4542e315461ebb4f5d3bdda661d5/Untitled%209.png)

**Odpowiedź y[n] na dowolne wymuszenie x[n] jest** tak naprawdę **superpozycją odpowiedzi impulsowych na poszczególne składowe wymuszenia**. To znaczy, że jeżeli sygnał wymuszający to $x[n]=5\delta[n]+6\delta[n-2]+4\delta[n-5]$, narysowany poniżej:

![Untitled](1%20Wybrane%20zagadnienia%20teorii%20obwodo%CC%81w%203dbd4542e315461ebb4f5d3bdda661d5/Untitled%2010.png)

To odpowiedzią tego wymuszenia jest odpowiedź impulsowa na każdą “szpilę” z osobna, co wygląda jak poniżej.

![Untitled](1%20Wybrane%20zagadnienia%20teorii%20obwodo%CC%81w%203dbd4542e315461ebb4f5d3bdda661d5/Untitled%2011.png)

Odpowiedź układu na dowolne wymuszenie można więc przedstawić tak, jak powyżej. **Dowolne wymuszenie dyskretne można przedstawić jako nieskończoną sumę delt Koneckera**, co z zasady superpozycji pozwala określić odpowiedź układu na to wymuszenie. 

Patrząc na obrazek powyżej można więc zauważyć zależność:

$$
y[0] = x[0]h[0]
$$

$$
y[1] = x[0]h[1] + x[1]h[0]
$$

$$
y[2] = x[0]h[2] + x[1]h[1] + x[2]h[0]
$$

I tak dalej, co można przedstawić ogólnie za pomocą sumy, w której x[k] to wymuszenie w próbce k, natomiast h[k] to odpowiedź impulsowa na wymuszenie w próbce k:

$y[n]=\sum^{n}_{k=0}x[k]h[n-k]=\sum^{n}_{k=0}x[n-k]h[k]$ 

Powyższe równanie z prawej strony definiuje dwuargumentową operację pomiędzy ciągami x[n] i h[n]. Operacja ta to właśnie **splot dyskretny.**

Cały powyższy wywód mówi jedno: **odpowiedź wymuszona y[n] układu liniowego jest równa splotowi dyskretnemu sygnału wejściowego x[n] z odpowiedzią impulsową h[n] tego układu**. Stąd, **żeby wyznaczyć sygnał wyjściowy y[n], wystarczy znaleźć odpowiedź impulsową h[n] układu i spleść ją z sygnałem wejściowym x[n]. Dotyczy to każdego wymuszenia.**

**Własności splotu dyskretnego**

Właściwością splotu dyskretnego jest to, że transformata Z splotu dwóch ciągów jest równa iloczynowi transformat tych ciągów, czyli $f_1[n]*f_2[n]\lrarr F_1(z)F_2(z)$.

Poza tym, splot jest:

- operacją przemienną, czyli $f_1[n]*f_2[n]=f_2[n]*f_1[n]$
- operacją łączną, czyli $\{f_1[n]*f_2[n]\}*f_3[n]=f_1[n]*\{f_2[n]*f_3[n]\}$

### Najważniejsze punkty

- odpowiedź impulsowa układu to jego odpowiedź na deltę Koneckera - sygnał typu *szpila*; przebieg odpowiedzi impulsowej to spróbkowane zanikanie wykładnicze (każda kolejna próbka to ok. 0,7 poprzedniej)
- każde wymuszenie dyskretne można zapisać matematycznie jako sumę delt Koneckera
- odpowiedź układu dyskretnego na dowolne wymuszenie zapisane jako suma delt Koneckera, to po prostu superpozycja odpowiedzi impulsowych tego układu na każde z tych wymuszeń
- splot dyskretny to operacja matematyczna, opisująca odpowiedź układu dyskretnego jako superpozycję odpowiedzi impulsowych na wymuszenia zapisane w postaci sumy delt Koneckera
- splot dyskretny opisuje odpowiedź układu dyskretnego na dowolne wymuszenie

### **Źródła**

[1] Athanasios Papoulis - *Obwody i układy*