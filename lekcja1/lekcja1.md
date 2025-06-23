**Wprowadzenie**

**Czym jest prawo Ohma?**  
Prawo Ohma opisuje fundamentalną zależność między prądem elektrycznym, napięciem i rezystancją w obwodzie elektrycznym. Mówi ono, że napięcie przyłożone do elementu obwodu jest równe iloczynowi prądu płynącego przez ten element i jego rezystancji. Na szczęście nie trzeba uczyć się żadnej długiej regułki, ponieważ w najprostszej formie wyraża się ono trzema prostymi wzorami, które dla ułatwienia zazwyczaj zapisuje się w formie poniższej piramidki.

![Prawo Ohma - wzór, schemat i przykładowe obliczenia](prawo_ohma.jpg)

Jedne z najważniejszych wzorów dla elektronika

Jak korzystać z tej piramidki? Zasłaniamy wielkość, którą chcemy uzyskać, a ułożenie pozostałych wielkości podpowiada nam wzór.

**Interpretacja prawa Ohma**

Prawo Ohma pozwala zrozumieć, jak zmieniają się parametry obwodu. Przykładowo, przy stałej rezystancji, wzrost napięcia powoduje proporcjonalny wzrost prądu. Można to zobrazować analogią do przepływu wody: zwiększenie ciśnienia wody (napięcia) przy stałym otwarciu zaworu (rezystancji) skutkuje większym przepływem wody (prądu).

![Prawo Ohma przedstawione jako analogia wodna (animacja)](analogia_wodna_1)

Analogia wodna: przy stałym oporze zwiększenie napięcia prowadzi do wzrostu prądu

Z kolei, przy stałym napięciu, zmniejszenie rezystancji prowadzi do wzrostu prądu. W analogii wodnej odpowiada to sytuacji, gdy przy stałym ciśnieniu wody, szerzej otwieramy zawór, co zwiększa przepływ.

![Prawo Ohma - wpływ rezystancji na prąd płynący w obwodzie](analogia_wodna_2)
Analogia wodna: przy stałym napięciu zmniejszenie oporu prowadzi do wzrostu prądu

**Prawo Ohma w praktyce**

Załóżmy, że mamy obwód z baterią o napięciu 9 V i rezystorem o oporze 10 kΩ. Chcemy obliczyć prąd płynący w obwodzie.

![Pomiar prądu w układzie demonstrującym prawo Ohma](uklad_testowy.jpg)

Układ testowy do pomiaru prądu

Na początku sprawdzenie teoretyczne. Korzystamy z poznanych wcześniej wzorów:

U = 9 V, R = 10 kΩ, I = ?

I = U / R = 9 V / 10000 Ω = 0,0009 A = 0,9 mA

W praktycznych pomiarach mogą wystąpić niewielkie różnice między obliczeniami a wynikami pomiarów. Jest to spowodowane niedokładnościami elementów (np. tolerancja rezystorów), oporem przewodów pomiarowych oraz dokładnością samego miernika.

**LED – diody świecące w praktyce**

Dioda LED (ang. Light Emitting Diode), to element elektroniczny, który przewodzi prąd w jednym kierunku i emituje światło.

![Dioda świecąca (LED) oraz symbol ze schematu ideowego](schemat_diody.jpg)

Przykładowa dioda i symbol stosowany na schematach

Dioda LED zawiera specjalny kryształ, który pod wpływem przepływającego prądu emituje światło. Dioda LED ma dwa wyprowadzenia: anodę (plus) i katodę (minus). Prąd musi płynąć od anody do katody, aby dioda świeciła. Podłączenie diody w odwrotnym kierunku (zaporowo) blokuje przepływ prądu i dioda nie świeci.

![Dioda świecąca w środku - przekrój LED](przekroj_diody.jpg)

![Dioda odpowiednio podłączona – świeci](dioda_dobrze_podl.jpg)

Dioda odpowiednio podłączona – świeci

![Dioda podłączona błędnie (zaporowo) – nie świeci](dioda_zle_podl.jpg)

Dioda podłączona błędnie (zaporowo) – nie świeci

![Dioda świecąca bez rezystora szybko ulegnie uszkodzeniu](dioda_uszkodzona.jpg)

Brak rezystora i zbyt duży prąd uszkadzają diodę

**Jak rozpoznać wyprowadzenia diody świecącej?**

Katodę diody LED można rozpoznać na kilka sposobów:

- Jest krótsza od anody.
- Obudowa diody ma ścięcie przy katodzie.
- Wewnątrz diody katoda łączy się z większym elementem.

![Dioda świecąca anoda i katoda - rozpoznawanie wyprowadzeń](el_char_diody.jpg)

Elementy charakterystyczne diody

**Parametry diod świecących**

Diody świecące charakteryzują się podobnymi parametrami jak diody prostownicze, tyle że większą uwagę zwraca się na inne z tych cech (np. barwę, jasność, kąt świecenia). Najistotniejszy jest jednak prąd przewodzenia. Dla diod takich jak te dołączone do zestawu maksymalny prąd przewodzenia wynosi około 20 mA. Nowoczesne diody świecą jednak bardzo jasno nawet już przy 1–2 mA. Dlatego zwykle ogranicza się ten prąd do bardzo małych wartości.

**Dobieranie rezystora do diody świecącej (LED)**

Diodom trzeba ograniczać prąd. Najprostszym rozwiązaniem jest wstawienie rezystora szeregowo z diodą LED. Zgodnie z prawem Kirchhoffa część napięcia odłoży się na diodzie, a pozostała – na rezystorze. Ponadto, znając (mniej więcej) napięcie, jakie „weźmie na siebie” rezystor, można – zgodnie z prawem Ohma – obliczyć prąd, jaki przez niego płynie. Elementy te są połączone szeregowo, więc ten sam prąd popłynie przez diodę, a to nas głównie interesuje.

Wzór pozwalający obliczyć rezystancję rezystora do zasilania diody LED wygląda następująco:

![Obliczanie rezystora dla diody świecącej](rezyst_diody.jpg)
- U<sub>zas</sub> – napięcie zasilania obwodu z diodą
- U<sub>diody</sub> – napięcie przewodzenia diody (z tabelki wyżej)
- I<sub>diody</sub> – prąd, który ma płynąć przez diodę

![Schemat testujący diodę świecącą podłączoną do baterii przez rezystor](schemat_diody.jpg)

Podstawowy schemat podłączenia diody świecącej do źródła zasilania

Obliczmy wartość rezystora w układzie zasilanym z 9 V. Załóżmy, że napięcie przewodzenia diody to 2 V, a ma przez nią popłynąć 7 mA. Wypisujemy wartości:

- U<sub>zas</sub> = 9 V
- U<sub>diody</sub> = 2 V
- I<sub>diody</sub> = 7 mA = 0,007 A

Obliczamy wartość potrzebnego rezystora:

R = (9 V − 2 V) / 0,007 A = 7 V / 0,007 A = 1000 Ω = 1 kΩ

Jaki prąd powinien płynąć przez diodę? Na pewno mniejszy od maksymalnego, czyli podanych już 20 mA. Produkowane dzisiaj diody świecą wystarczająco jasno, jeśli płynie przez nie prąd <10 mA. W układach zasilanych z baterii, w których zależy nam na niskim zużyciu energii, można przyjąć 1–5 mA.

![Wpływ rezystora na jasność diody - animacja działania układu](swiecenie_a_rezyst.jpg)

Świecenie diody w zależności od dobranego rezystora

**Czy rezystor musi być „przed” diodą?**

Kolejność podłączenia rezystora i diody w obwodzie szeregowym nie ma wpływu na działanie obwodu.. Przez elementy połączone szeregowo płynie ten sam prąd – wynika to z praw Kirchhoffa.

![Rezystor umieszczony „przed diodą”](rezyst_przed.jpg)

Rezystor umieszczony „przed diodą”

![Rezystor umieszczony „za diodą”](rezyst_za.jpg)

Rezystor umieszczony „za diodą”

**Czym są kondensatory?**

Kondensator to element elektroniczny, który magazynuje energię elektryczną. Kondensatory dzielą się na biegunowe i bezbiegunowe. Kondensatory biegunowe (np. elektrolityczne) mają oznaczoną biegunowość i muszą być podłączone do obwodu zgodnie z polaryzacją. Kondensatory bezbiegunowe (np. ceramiczne, foliowe) można podłączać w obwodzie w dowolnym kierunku.

![Kondensatory elektrolityczne, ceramiczne i tantalowe](typy_kondensatorow.jpg)

Różne typy kondensatorów. Najczęściej używane są kondensatory elektrolityczne (dwa pierwsze z lewej) i ceramiczne (trzeci od lewej)

Kondensatory włączamy równolegle do zasilanego urządzenia, dzięki czemu zachowują się podobnie do akumulatorów: ładują się podczas normalnej pracy i rozładowują, kiedy nasze źródło zasilania jest chwilowo niewystarczające (np. gdy urządzenie przez krótką chwilę próbuje pobrać duży prąd).

Zastosowanie kondensatorów i wykorzystanie powyższych właściwości powoduje, że wahania napięcia zasilającego układ zmniejszają się, o czym przekonasz się wykonując odpowiednie ćwiczenia. Często mówi się więc, że kondensatory filtrują zasilanie.

**Kondensatory biegunowe**

Do kondensatorów biegunowych zaliczają się m.in. bardzo popularne kondensatory elektrolityczne. Elementy te mają odpowiednio opisane wyprowadzenia – najczęściej na obudowie opisana jest nóżka, którą należy podłączyć do masy układu (czyli „minusa” z baterii).

Z kolei na schematach znakiem plusa oznacza się wyprowadzenie, które powinno być podłączone do dodatniej szyny zasilania („plusa” z baterii).

![Kondensator elektrolityczny 470 uF wraz z przykładowym symbolem ze schematu ideowego](kondensator_elektrolityczny.jpg)

Przykładowy kondensator elektrolityczny wraz z opisanym symbolem

**Kondensatory bezbiegunowe**

Kondensatorów bezbiegunowych, czyli niespolaryzowanych, jest dość dużo, a ich zróżnicowanie wynika z materiałów, jakie są stosowane na dielektryki między okładkami. Używa się m.in.:

- ceramiki (kondensatory ceramiczne),
- folii (kondensatory poliestrowe i polipropylenowe).

Każda grupa ma różne zastosowania. Kondensatory ceramiczne wykorzystuje się np. w układach, gdzie napięcia mogą zmieniać się bardzo, bardzo często, a foliowe – w układach pracujących przy napięciu sieciowym, z uwagi na ich dużą wytrzymałość napięciową (rzędu setek woltów) i małe straty.

Niezależnie od typu kondensatora niespolaryzowanego na schemacie przedstawia się je w taki sam sposób. Kondensatory bezbiegunowe, w zależności od metody ich wykonania, występują również w różnych obudowach.

**Pojemność kondensatorów**

Kondensatory cechują się głównie dwoma parametrami: pojemnością i napięciem pracy. Pierwszy określa zdolność do gromadzenia ładunku i wyraża się go w faradach (symbol F). Jest to jednak bardzo duża jednostka, dlatego w praktyce spotkasz się głównie z:

- pikofaradami \[pF\] (1 pF = 0,000 000 000 001 F),
- nanofaradami \[nF\] (1 nF = 0,000 000 001 F),
- mikrofaradami \[μF\] (1 μF = 0,000 001 F).

**Napięcie pracy kondensatorów**

Ten parametr wyrażany jest w woltach \[V\] i określa, jakie napięcie może panować między okładkami kondensatora bez ryzyka jego uszkodzenia. Jest to wartość graniczna, dlatego należy stosować elementy na napięcia wyższe niż te, jakie są przewidywane w układzie. Najpopularniejsze wartości napięć pracy kondensatorów to: 10 V, 16 V, 25 V, 35 V, 50 V, 63 V i 100 V.

Maksymalne napięcie pracy wpływa znacząco na rozmiar kondensatorów. Przykładowo, największy (fizycznie) kondensator na poniższym zdjęciu charakteryzuje się najmniejszą pojemnością, ale za to jest w stanie wytrzymać bardzo duże napięcie (330 V).

![Kondensatory elektrolityczne różniące się pojemnością, napięciem oraz rozmiarem](elektrolityczne_rozne.jpg)

Jak widać, rozmiar kondensatora nie zależy tylko od jego pojemności

**Wykorzystanie kondensatorów w praktyce**

Kondensatory znajdują szerokie zastosowanie w elektronice. W układach cyfrowych są często używane do filtrowania zasilania (np. przy ceramicznych wielkość wynosi 100nF) , stabilizacji napięcia i eliminacji zakłóceń. Kondensatory wykorzystuje się również w układach audio, zasilaczach i wielu innych aplikacjach. Im większa pojemność tym kondensator może przechowywać więcej energii. Kondensator o pojemności 1F naładowany do napięcia 1 V przechowuje energię 0,5 J natomiast kondensator o pojemności 1000uF (0,001F) naładowany do napięcia 1,5 V przechowuje energię 0,001125 J. Ilość energii można obliczyć ze wzoru E = 0,5 \* C \* V^2, gdzie E to energia, C to pojemność a V to napięcie.

**Pomiar oporu rezystora miernikiem**

Rezystancję rezystora można zmierzyć za pomocą miernika uniwersalnego (multimetru). Podczas pomiaru rezystancji nie ma znaczenia, jak podłączymy sondy miernika do wyprowadzeń rezystora.

Poniżej pomiar rezystora 10 k, więc opór mierzymy na zakresie 20 k. Przy pomiarze oporu nie ma czegoś takiego jak biegunowość, nie ma zatem różnicy, do których wyprowadzeń przyłożymy sondy:

![Pomiar oporu](pomiar_oporu.jpg)

Pomiar oporu

Odczytana wartość to 9,56 kΩ, więc rezystor, jak widać, mieści się w zakresie tolerancji producenta.

**Połączenie szeregowe w praktyce**

Połączmy teraz szeregowo dwa rezystory (330 Ω oraz 1 kΩ). Poniżej widoczny jest przykład takiego układu w praktyce. Nie musisz wkładać elementów dokładnie w te same dziurki, wystarczy, że mając w głowie powyższy schemat płytki stykowej, połączysz szeregowo dwa rezystory.

Poniżej specjalnie pokazane są inne połączenia rezystorów (korzystające z różnych otworów):

![Połączenie szeregowe w praktyce](polaczenie_szeregowe.jpg)

Połączenie szeregowe w praktyce

**Połączenie równoległe w praktyce**

Teraz pora na połączenie równoległe tych samych rezystorów, co jest właściwie jeszcze łatwiejsze. Przykład połączenia widoczny jest poniżej.

![Połączenie równoległe w praktyce](polaczenie_rownolegle.jpg)

Połączenie równoległe w praktyce

**Układ NE555**

Układ scalony NE555 to popularny element, który został wprowadzony na rynek w 1970 roku. Jest on używany do generowania sygnałów czasowych i znajduje zastosowanie w wielu różnych urządzeniach.

![Jedna z wersji układu NE555 w obudowie przewlekanej](ne555.jpg)

Jedna z wersji układu NE555 w obudowie przewlekanej

Pomimo swojej prostoty, NE555 jest bardzo uniwersalny. W jego strukturze można wyróżnić kilka podstawowych bloków, które, odpowiednio połączone, pozwalają na realizację różnych funkcji. Układ ten jest wykorzystywany na przykład w układach migających diod, sterownikach serwomechanizmów, generatorach dźwięku i regulatorach mocy silników.

NE555 jest dostępny w obudowie z 8 wyprowadzeniami. Istnieje również wersja NE556, która zawiera dwa układy NE555 w jednej obudowie z 14 wyprowadzeniami, ale jest mniej popularna.

Przy pracy z układami scalonymi, ważne jest korzystanie z dokumentacji technicznej, zwanej notą katalogową, która zawiera szczegółowe informacje o układzie. W podstawowym zakresie, do zrozumienia działania układu wystarcza znajomość opisu wyprowadzeń, czyli pinout.

![Opis wyprowadzeń układu NE555](ne555_wyprowadzenia.jpg)

Opis wyprowadzeń układu NE555

**Budowa wewnętrzna NE555**

Układy scalone są zbudowane z tranzystorów, rezystorów i innych elementów. Wewnętrzną strukturę NE555 można przedstawić w postaci bloków funkcjonalnych, co ułatwia zrozumienie jego działania. Schemat blokowy NE555 pokazuje, jak połączone są ze sobą poszczególne bloki. Na schemacie tym nie zaznacza się zazwyczaj połączeń zasilania i masy, aby był bardziej czytelny.

![Schemat blokowy układu NE555](ne555_schemat.jpg)

Schemat blokowy układu NE555

**Blok 1: Dzielnik napięcia**

![NE555, blok 1: dzielnik napięcia](ne555_blok1.jpg)

NE555, blok 1: dzielnik napięcia

**Blok 2: Komparatory napięcia**

![NE555, blok 2: komparatory napięcia](ne555_blok2.jpg)

NE555, blok 2: komparatory napięcia

**Blok 3: Przerzutnik RS**

Prostokąt z pięcioma wyprowadzeniami to tzw. przerzutnik RS. Jest to podzespół cyfrowy, który zapamiętuje stany logiczne z wyjść komparatorów. Przerzutnik ma wejścia S (set), R (reset) i RES (reset z negacją) oraz wyjścia Q i Q z negacją.

![NE555, blok 3: przerzutnik RS](ne555_blok3.jpg)

NE555, blok 3: przerzutnik RS

Funkcje jego wyprowadzeń są następujące:

- S (set) – podanie stanu wysokiego powoduje ustawienie wyjścia Q w stan wysoki,
- R (reset) – podanie stanu wysokiego powoduje ustawienie wyjścia Q w stan niski,
- RES z kółkiem oznaczającym negację – podanie stanu niskiego na to wejście resetuje układ, czyli ustawia 0 na wyjściu Q niezależnie od stanu pozostałych dwóch wejść,
- Q – wyjście przerzutnika,
- Q z kreską oznaczającą negację – zanegowane wyjście przerzutnika (stan przeciwny do Q).

**Blok 4: Bufor wyjściowy**

Między wyjściem Q przerzutnika a wyprowadzeniem OUT układu znajduje się tzw. bufor wyjściowy, którego zadaniem jest zwiększenie wydajności prądowej tego wyjścia. Dzięki niemu bezpośrednio do wyjścia NE555 można dołączać np. diody lub przekaźniki.

Wyjście przerzutnika nie podołałoby temu zadaniu, ponieważ struktura logiczna nie jest przystosowana do przewodzenia dużych prądów. Bufor „sam z siebie” nie wpływa na stan logiczny na wyjściu – podąża on tylko za tym, co otrzyma na swoim wejściu, czyli za wyjściem przerzutnika.

![NE555, blok 4: bufor wyjściowy](ne555_blok4.jpg)

NE555, blok 4: bufor wyjściowy

**Blok 5: Tranzystor**

W układzie znajduje się tranzystor, który służy do rozładowywania zewnętrznego kondensatora, podłączanego do NE555. Tranzystor ten jest sterowany z zanegowanego wyjścia przerzutnika, czyli otwiera się wtedy, kiedy wyjście Q jest w stanie niskim, bo wówczas na zanegowanym Q mamy stan wysoki. Jest to oczywiście tranzystor o odpowiednio dużej wydajności prądowej, aby nie uległ uszkodzeniu po otwarciu – jego rolą jest szybkie rozładowanie kondensatora.

![NE555, blok 5: tranzystor](ne555_blok5.jpg)

NE555, blok 5: tranzystor

**Część wykonawcza**

**1\. Moduł Prawa Ohma – pomiar R9 i prądu**

- Włącz moduł **Prawa Ohma**.
- Za pomocą multimetru **zmierz rezystancję rezystora R9**.
- Zmierz **prąd płynący przez rezystor R9**, wykorzystując punkty **TP5 i TP6**. Pamiętaj, że amperomierz należy włączyć szeregowo z obciążeniem.
- Na podstawie uzyskanych wyników oblicz spadek napięcia na rezystorze:
- (Opcjonalnie) zmierz również napięcie między TP5 i TP6 i porównaj je z wartością obliczoną.
- Oceń zgodność wyników – uwzględnij możliwe błędy pomiarowe i tolerancję elementów.

**2\. Teoretyczne obliczenia dla dzielnika napięciowego**

- Oblicz spadki napięć:
- Zanotuj wartości i przygotuj je do porównania z pomiarami z punktu 3.

**3\. Pomiar napięć w dzielniku napięciowym**

- Włącz **moduł dzielnika napięciowego**.
- Wykonaj pomiary napięć między następującymi punktami:
  - **TP1 – TP2**
  - **TP2 – TP4**
  - **TP1 – TP4**
- Porównaj wartości zmierzone z wartościami teoretycznymi z punktu 2.
- Oceń poprawność działania dzielnika – czy napięcia rozkładają się proporcjonalnie do rezystancji?

**4\. Moduł ładowania kondensatora – porównanie szybkości ładowania**

- Włącz **moduł ładowania kondensatora**.
- Obserwuj, który z dostępnych kondensatorów ładuje się szybciej.
- Zastanów się, dlaczego tak się dzieje, biorąc pod uwagę wzór:
- Porównaj wartości pojemności i/lub rezystancji w obu obwodach.
- Wyciągnij wniosek: większa wartość C lub R oznacza dłuższy czas ładowania.

**5\. Moduł NE555 – obserwacja działania generatora**

- Włącz **moduł z układem NE555**.
- Zaobserwuj działanie układu – dioda LED powinna migać z określoną częstotliwością.
- Zastanów się, co wpływa na częstotliwość generowanego sygnału – zauważ, że zależy ona od wartości elementów R i C.
- Zanotuj częstotliwość migania oraz ogólną charakterystykę działania.
- Generator NE555 zostanie dokładniej omówiony w następnej lekcji.