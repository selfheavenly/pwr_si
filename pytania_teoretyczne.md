# Pytania ze slajdów z wykładu z kursu Sztuczna Inteligencja

## Pytania ogólne

### Scharakteryzuj oraz porównaj AI Silną oraz Słabą

- **Słaba AI (Narrow AI)** – systemy zaprojektowane do wykonywania konkretnych zadań. Nie posiadają świadomości ani rozumienia. Przykładami są asystenci głosowi, systemy rekomendacyjne, chatboty. Ich działanie opiera się na algorytmach przetwarzania danych i modelowaniu wiedzy w ograniczonym zakresie.
- **Silna AI (General AI)** – hipotetyczne systemy, które dorównują lub przewyższają ludzką inteligencję we wszystkich aspektach. Potrafią uczyć się, rozumować, planować, rozumieć język naturalny, posiadają świadomość i samoświadomość.

**Porównanie:**
| Cecha | Słaba AI | Silna AI |
|---------------------------|------------------------------|------------------------------------|
| Zakres działania | Wąski, zadaniowy | Ogólny, uniwersalny|
| Świadomość| Brak | Potencjalnie obecna|
| Przykłady | Siri, Google Translate | (Nie istnieje obecnie) |
| Zdolność adaptacji| Ograniczona | Bardzo wysoka |
| Obszar badań | Praktyczne zastosowania | Teoretyczne, filozoficzne |

### Przedstaw na czym polega Paradoks Moraveca

Paradoks Moraveca mówi, że:

> "Stosunkowo łatwo sprawić, żeby komputery przejawiały umiejętności dorosłego człowieka w testach na inteligencję albo w grze w warcaby, ale jest trudne albo wręcz niemożliwe zaprogramowanie im umiejętności rocznego dziecka w percepcji i mobilności."

Innymi słowy, łatwiej jest zautomatyzować logiczne rozumowanie niż percepcję i motorykę – czyli odwrotnie niż u ludzi.

### Omów kryteria Testu Turinga

Test Turinga polega na sprawdzeniu, czy maszyna potrafi prowadzić rozmowę w języku naturalnym w taki sposób, by człowiek nie był w stanie rozpoznać, że rozmawia z maszyną.

**Wymagania do zdania testu:**

- Przetwarzanie języka naturalnego
- Reprezentowanie wiedzy
- Automatyczne wnioskowanie
- Uczenie maszynowe

**Dla totalnego testu Turinga dodatkowo:**

- Widzenie komputerowe i rozpoznawanie mowy
- Manipulowanie obiektami i przemieszczanie się

Zaliczenie testu nie jest równoznaczne z posiadaniem inteligencji – np. ELIZA z 1964 r. potrafiła udawać psychoanalityka bez rozumienia treści.

### Na czym polega przetwarzanie brzegowe (edge computing)?

**Brak informacji w źródłach.**
(_Warto dodać samodzielnie: przetwarzanie brzegowe polega na analizowaniu danych możliwie blisko źródła ich powstawania – np. w urządzeniach IoT – zamiast przesyłania ich do scentralizowanej chmury. Zmniejsza to opóźnienia, zwiększa prywatność i odciąża sieć._)

---

## Algorytmy przeszukiwania przestrzeni stanów

### Jakie problemy można rozwiązać metodą przeszukiwania? Opisz krótko wymienione problemy.

Problemy:

- Przesuwanki (np. kostka Rubika)
- Labirynty – szukanie drogi
- Zagadki logiczne (np. misjonarze i kanibale)
- Gry planszowe
- Topografia układów scalonych
- Nawigacja robotów
- Sekwencjonowanie montażu
- Planowanie białek

Rozwiązanie polega na znalezieniu ścieżki w grafie przestrzeni stanów od stanu początkowego do końcowego.

### Definicje których elementów problemu są wymagane w celu zastosowania metody przeszukiwania?

- Zbiór możliwych stanów (przestrzeń stanów)
- Stan początkowy i końcowy
- Zestaw operacji (akcji)
- Model przejścia (skutek akcji)
- Funkcja kosztu akcji (np. koszt = 1)

### Przedstaw czym jest uporządkowana czwórka.

**[N, A, S, G]**, gdzie:

- **N** – zbiór wierzchołków (stanów)
- **A** – zbiór krawędzi (operacji)
- **S** – zbiór stanów początkowych
- **G** – zbiór stanów końcowych

### Czym jest Strategia Przeszukiwania?

To metoda wyboru operatora spośród dostępnych na danym etapie wyszukiwania. Strategia wpływa na efektywność, czas, koszt oraz zakończenie działania algorytmu.

### Jakie kroki są wymagane w celu uzyskania rozwiązania danego problemu metodą przeszukiwania?

1. Określić reprezentację stanów
2. Określić operatory
3. Zdefiniować stan początkowy i końcowy
4. Wybrać strategię przeszukiwania

### Wymień najważniejsze kryteria oceny jakościowej i ilościowej algorytmu wyszukiwania

- Zupełność
- Optymalność kosztowa
- Złożoność czasowa
- Złożoność pamięciowa

### Które struktury danych są związane z wyszukiwaniem?

- **OPEN** – stany do rozwinięcia (kolejki: FIFO, LIFO, priorytetowa)
- **CLOSED** – stany już rozwinięte
- Struktura węzła (NODE): stan, koszt, rodzic, operator

### Przedstaw sposób klasyfikacji strategii przeszukiwania oraz następnie opisz każdą z wymienionych grup wraz z wypisaniem przykładowych metod do nich zaliczanych.

**1. Metody „na ślepo” (niedoinformowane):**

- Nie wykorzystują informacji heurystycznych.
- Przykłady:
  - Przeszukiwanie wszerz (BFS)
  - Przeszukiwanie w głąb (DFS)
  - Przeszukiwanie z nawrotami (Backtracking)
  - Iteracyjne pogłębianie

**2. Metody heurystyczne (doinformowane):**

- Wykorzystują funkcję oceny (heurystykę).
- Przykłady:
  - Algorytm A\*
  - Algorytm zachłanny (Greedy Best-First Search)
  - Przeszukiwanie lokalne (np. wspinaczka górska, symulowane wyżarzanie)

### Czym są metody szukania "na ślepo"? Wymień przykłady.

- Metody bez znajomości celu
- Nie używają heurystyki
- Przykłady:
  - BFS (Breadth-First Search)
  - DFS (Depth-First Search)
  - Iteracyjne pogłębianie

### Czym są metody heurystyczne? Wymień przykłady.

- Wykorzystują funkcję oceniającą stan
- Pozwalają szybciej znaleźć dobre rozwiązania
- Przykłady:
  - A\*
  - Algorytm zachłanny
  - Wspinaczka górska
  - Symulowane wyżarzanie

## Wyznaczanie strategii w grach

### Przedstaw oraz wyjaśnij terminy wykorzystywane do charakteryzowania gier oraz omów popularne sposoby ich klasyfikacji.

**Gra** to rozgrywka między graczami, prowadzona według ustalonych zasad, w celu osiągnięcia określonego celu. Składa się z zestawu reguł, stanu początkowego oraz stanu końcowego (wygranego, przegranego lub remisowego). Ze stanami końcowymi można powiązać funkcję wypłaty.

Źródła skupiają się na grach dwuosobowych, wielochodowych, o sumie zerowej, o pełnej informacji i deterministycznych.

### Wyjaśnij pojęcie punktu siodłowego oraz jego rolę z strategiach min/max.

Dla gier o pełnej informacji rozwiązanie jest trywialne, ponieważ każdy gracz stosuje tylko jedną strategię, zwaną **strategią czystą**. Teoria gier określa takie gry jako "mało ciekawe". W praktyce wiele gier dwuosobowych nie posiada punktu siodłowego, co oznacza, że reprezentacja macierzowa do wyznaczenia optymalnych strategii jest często nieprzydatna.

**Strategia minimaksu** polega na utworzeniu drzewa gry i przypisaniu wartości wierzchołkom końcowym. Następnie, wierzchołkom na kolejnych poziomach przypisuje się wartości zgodnie z zasadą: **maksymalna wartość potomka dla gracza** (MAX) oraz **minimalna wartość potomka dla przeciwnika** (MIN). Po osiągnięciu korzenia, wybiera się strategię zapewniającą największe zyski.

### Omów twierdzenie minimaksowe von Neumanna. Wyjaśnij każdy z branżowych terminów użytych w definicji.

**Twierdzenie minimaksowe** von Neumanna (1928) mówi, że **każda skończona gra dwuosobowa o sumie zerowej ma co najmniej jedno rozwiązanie, które określa wartość gry i optymalne strategie graczy**.

**Skończona gra dwuosobowa o sumie zerowej**: Gra z ustaloną, skończoną liczbą ruchów i dwóch graczy, gdzie suma zysków jednego gracza i strat drugiego wynosi zero (lub stałą wartość) dla każdego możliwego wyniku.
**Wartość gry**: Wartość liczbowa związana z rozwiązaniem gry, która określa oczekiwany wynik dla gracza przy założeniu, że obu graczy stosuje optymalne strategie.
**Optymalne strategie graczy**: Strategie, które maksymalizują zyski gracza przy założeniu, że przeciwnik również stosuje optymalną strategię.

### Omów algorytm cięć $\alpha - \beta$.

**Algorytm cięć α-β** to **modyfikacja algorytmu minimaksowego**, która **eliminuje z dalszej analizy węzły nie wpływające na wartość przypisywaną ich przodkom**. Pozwala to na znaczne ograniczenie drzewa gry. W algorytmie występują dwa rodzaje cięć: **cięcie α** (dla wierzchołków gracza, ocena potomnych może zakończyć się, gdy wartość jest niższa niż dotychczasowe maksimum α) oraz **cięcie β**.

## Reprezentacja wiedzy i wnioskowanie

### Czym różnią się reprezentacje wiedzy deklaratywne od proceduralnych?

W podejściu **deklaratywnym** wiedza jest **zbiorem specyficznych faktów**, a korzystanie z niej polega na stosowaniu ogólnych procedur manipulacji do tego zbioru. Następuje **wyraźne oddzielenie wiedzy od sposobu jej wykorzystania w procesie wnioskowania**. Metody deklaratywne są przydatne do reprezentowania **wiedzy o charakterze statycznym**, np. cech obiektów czy relacji logicznych. Przykładem jest reprezentacja logiczna.

W podejściu **proceduralnym** zakłada się, że główną część wiedzy stanowią **informacje o procesach i działaniach**. **"Wiedzieć" jest równoważne z "wiedzieć jak"**. Wiedza zawarta jest w **procedurach**, które określają, jak zachować się w danej sytuacji. Metody proceduralne służą do reprezentowania **wiedzy o charakterze dynamicznym**, np. ciągów akcji czy algorytmów postępowania.

### Wymień i opisz trzy aspekty wykorzystania wiedzy.

Trzy aspekty wykorzystania wiedzy to:

1.  **Gromadzenie nowej wiedzy**: Dodawanie nowych faktów do bazy wiedzy, uwzględniając ich związki z już istniejącą wiedzą i eliminując powtórzenia (klasyfikacja i integracja wiedzy).
2.  **Wydobycie z bazy wiedzy faktów dotyczących danego problemu**: Odzyskiwanie odpowiednich informacji z bazy wiedzy w celu rozwiązania problemu.
3.  **Rozumowanie (wnioskowanie) przy użyciu faktów w poszukiwaniu rozwiązania**: Proces wyprowadzania nowych twierdzeń (wniosków) z faktów uznanych za prawdziwe (przesłanek), zgodnie z prawami logiki. Celem jest udowodnienie określonej hipotezy.

### Zestaw ze sobą CNF oraz DNF.

Dostarczone źródła nie zawierają informacji na temat Koniunkcyjnej Formy Normalnej (CNF) ani Dysjunkcyjnej Formy Normalnej (DNF). Wspominają o formułach logicznych w rachunku zdań i predykatów, a także o klauzulach, ale nie opisują tych konkretnych form normalnych.

### Na czym polega rachunek predykatów? Omów czym jest predykat.

**Rachunek predykatów** (logika pierwszego rzędu) jest **językiem zbudowanym na bazie obiektów i relacji** zachodzących między nimi. Umożliwia wyrażanie faktów dotyczących wybranych lub wszystkich obiektów, co pozwala na formułowanie ogólnych praw i reguł. Jest bardzo ważnym narzędziem do reprezentacji wiedzy i podstawą programowania w logice (np. Prolog).

**Predykat** to wyrażenie, w którym występuje zmienna (lub zmienne) i które staje się zdaniem prawdziwym lub fałszywym po podstawieniu wartości za zmienne. W zagadnieniach reprezentacji wiedzy definiuje się go jako **własność obiektu lub relację między obiektami**. Składa się z nazwy i dowolnej liczby argumentów (termów), którymi mogą być stałe, zmienne lub inne predykaty. Strukturę predykatu można przedstawić jako `nazwa_predykatu(arg1, arg2, .. , argn)`.

### Wyjaśnij czym są Sieci Semantyczne. Z czego się składają?

**Sieci semantyczne** to **etykietowane grafy skierowane**, w których **wierzchołki reprezentują ogólne stany rzeczy** (obiekty, zdarzenia, pojęcia abstrakcyjne itp.), a **krawędzie określają relacje między wierzchołkami**. Relacje mogą wyrażać dowolne treści semantyczne. Zalicza się je do deklaratywnych metod reprezentacji wiedzy. Przykładowe relacje to AKO (bycie podklasą), ISA (bycie instancją), POSS (posiadanie składowych), OWN (posiadanie obiektów), CAN (umiejętność), FEATURE (posiadanie cech).

### Porównaj ze sobą następujące metody wnioskowania: Modus Ponens, Regresywne, Progresywne, Rezolucyjne.

Wnioskowanie to proces wyprowadzania nowych twierdzeń z przesłanek.
**Modus Ponens**: Jest to jedna z często stosowanych reguł wnioskowania. Klasyczny schemat zakłada przesłankę A i implikację A -> B, co prowadzi do wniosku B. W logice rozmytej można go rozszerzyć na częściową prawdziwość zdań.
**Wnioskowanie regresywne (wstecz)**: Polega na **startowaniu od hipotezy głównej (celu)** i próbie wykazania jej prawdziwości na podstawie przesłanek. Jeśli przesłanka nie jest faktem w bazie, staje się nową hipotezą. Proces idzie "wstecz" od celu do faktów.
**Wnioskowanie progresywne (w przód)**: Polega na **startowaniu od prawdziwych faktów** i generowaniu nowych prawdziwych stwierdzeń na podstawie dostępnych reguł. Proces idzie "w przód" od faktów do nowych konkluzji, aż do momentu wygenerowania hipotezy lub braku możliwości generowania nowych faktów. Nazywane też wnioskowaniem sterowanym danymi.
**Metoda rezolucji**: Metoda **dowodzenia przez zaprzeczenie**, stosowana m.in. w Prologu. Polega na wykazaniu, że **negacja zdania (hipotezy) prowadzi do sprzeczności** z faktami i regułami zawartymi w bazie wiedzy (KB). Dowód polega na wykazaniu, że formuła `KB ^ ¬ h` jest niespełnialna, co realizuje się przez iteracyjne generowanie klauzul aż do uzyskania klauzuli pustej (sprzeczność).

## Wiedza niepewna i wnioskowanie

### Omów fundamenty teorii zbiorów rozmytych w kontekście sztucznej inteligencji.

Teoria zbiorów rozmytych, zapoczątkowana przez L. Zadeha w 1965 r., jest stosowana w AI do **przetwarzania wiedzy niepewnej lub niepełnej**. Pozwala na **formalne określenie pojęć nieprecyzyjnych i wieloznacznych** (np. "średni wzrost", "wysoka temperatura"), których nie da się opisać logiką dwuwartościową. Podstawowym pojęciem jest **zbiór rozmyty**, definiowany przez **funkcję przynależności (µA(x))**, która każdemu elementowi przypisuje **stopień przynależności** do zbioru w przedziale.

### Jakie rozróżniamy rodzaje "niedoskonałości" wiedzy?

Wyróżnia się następujące rodzaje "niedoskonałości" wiedzy:
**Niepewność**: Nie można jednoznacznie stwierdzić, czy dane fakty są prawdziwe, czy fałszywe.
**Niepełność**: Brak wystarczającej wiedzy, aby stwierdzić prawdziwość pewnych faktów, co nie oznacza, że są one fałszywe.
**Niedokładność**: Nie można precyzyjnie odróżnić obiektów należących do pewnej relacji od obiektów do niej nienależących.

## Wiedza niepewna i wnioskowanie

### Przedstaw oraz omów podstawowe klasy funkcji przynależności

Funkcja przynależności (µA(x)) przypisuje każdemu elementowi stopień przynależności do zbioru rozmytego w przedziale. W źródłach przedstawiono przykładowe klasy funkcji przynależności, często składające się z fragmentów funkcji liniowych lub kwadratowych. Zestaw ten jest otwarty i obejmuje m.in. funkcje typu s, π, Γ (gamma), L (lambda) oraz V. Definicje tych funkcji wykorzystują różne parametry do określenia ich kształtu.

### Opisz własności zbiorów rozmytych oraz ich możliwe operacje

Podstawowe własności zbiorów rozmytych:

- **Nośnik zbioru rozmytego (supp A)**: Zbiór elementów przestrzeni X, dla których funkcja przynależności jest większa od 0.
- **Wysokość zbioru rozmytego (h(A))**: Kres górny wartości funkcji przynależności zbioru.
- **Zbiór normalny**: Zbiór rozmyty, którego wysokość wynosi 1.

Możliwe operacje na zbiorach rozmytych A i B:

- **Iloczyn zbiorów rozmytych (A∩B)**: Określany przez minimum stopni przynależności µA∩B(x) = min(µA(x), µB(x)) [61 - przykład].
- **Suma zbiorów rozmytych (A∪B)**: Określana przez maksimum stopni przynależności µA∪B(x) = max(µA(x), µB(x)) [61 - przykład].
- **Dopełnienie zbioru rozmytego (¬A)**: Patrz niżej.

### Wyjaśnij pojęcie dopełnienia zbioru rozmytego

**Dopełnienie (negacja)** zbioru rozmytego A (¬A) w przestrzeni X to zbiór rozmyty, którego funkcja przynależności dla każdego elementu x wynosi **µ¬A(x) = 1 - µA(x)** [61 - przykład].

### Czym są S-normy oraz T-normy? W jaki sposób się je definiuje?

**S-normy (dla sumy) i T-normy (dla iloczynu)** to funkcje wprowadzone w literaturze do określenia "lepszych" operacji sumy i iloczynu zbiorów rozmytych. Powinny one spełniać warunki takie jak: łączność, przemienność, monotoniczność oraz odpowiednie warunki brzegowe. T-normy i S-normy można zdefiniować za pomocą operatorów algebraicznych, np. iloczyn jako µA∩B(x) = µA(x)\*µB(x), a suma jako µA∪B(x) = µA(x)+µB(x) - µA(x)\*µB(x).

### Omów pojęcia: koncentracji i rozcieńczenia zbiorów rozmytych

- **Koncentracją** zbioru rozmytego A (CON(A)) nazywamy zbiór rozmyty, którego funkcja przynależności µCON(A)(x) jest **kwadratem funkcji przynależności zbioru A**: µCON(A)(x) = [µA(x)]².
- **Rozcieńczeniem (rozrzedzeniem)** zbioru rozmytego A (DIL(A)) nazywamy zbiór rozmyty, którego funkcja przynależności µDIL(A)(x) jest **pierwiastkiem kwadratowym funkcji przynależności zbioru A**: µDIL(A)(x) = [µA(x)]⁰,⁵.

### Wyjaśnij pojęcie zmiennej lingwistycznej

**Zmienna lingwistyczna** to jedno z najważniejszych pojęć logiki rozmytej. Przyjmuje ona jako swoje wartości **wyrażenia języka naturalnego**, które są nieprecyzyjne lub wieloznaczne, np. "mała prędkość", "wysoka cena", "młody", "stary". Dla każdej wartości zmiennej lingwistycznej przyporządkowany jest odpowiedni zbiór rozmyty.

### Omów model Mamdaniego.

Model Mamdaniego to jedna z najczęściej stosowanych metod wyznaczenia funkcji przynależności dla **implikacji rozmytej A → B** na podstawie znanych funkcji przynależności µA(x) i µB(y). Zakłada on, że **stopień prawdziwości konkluzji (wniosku) nie może być wyższy niż stopień prawdziwości przesłanki**. W sterowaniu rozmytym często przyjmuje się operację minimum lub produktu (iloczynu algebraicznego) do wyliczania zbioru wynikowego.

### Omów pojęcie sterowania rozmytego oraz zestaw ze sobą sterowniki klasyczne z rozmytymi (FLC)

**Sterowanie rozmyte** to ważne zastosowanie logiki rozmytej w systemach sterowania. Jego celem jest przetwarzanie danych wejściowych na wyjściowe w celu **osiągnięcia i utrzymania pożądanego stanu systemu**. **Sterowniki rozmyte (FLC)** stanowią alternatywę dla sterowników klasycznych, szczególnie tam, gdzie **nie jest wymagana bezwzględna precyzja**, a liczy się **prostota rozwiązania i szybkość działania**.

### Przedstaw i omów schemat sterowania rozmytego. Opisz każdy z modułów.

Schemat sterownika rozmytego składa się z:

- **Moduł rozmywania (Fuzzification)**: Zamienia **ostre (liczbowe) wartości wejściowe** na odpowiadające im **zbiory rozmyte** (wartości zmiennych lingwistycznych, np. "mały", "średni"). Jest to konieczne, ponieważ moduł wnioskujący działa na zbiorach rozmytych. Często stosuje się zastąpienie wartości ostrej singletonem rozmytym.
- **Baza reguł (Rule Base)**: Zawiera **reguły rozmyte**, często w postaci IF (warunek) THEN (konkluzja), które tworzą model lingwistyczny procesu sterowania. Reguły te operują na zmiennych lingwistycznych.
- **Moduł wnioskowania (Inference Module)**: Jest głównym elementem sterownika. Działa w oparciu o schemat wnioskowania przybliżonego (np. modus ponens). Określa **stopień prawdziwości konkluzji dla każdej reguły** na podstawie stopnia prawdziwości części przesłankowej. Sposób wyliczenia zbioru wynikowego zależy od wybranej T-normy (np. minimum lub iloczyn algebraiczny).
- **Moduł wyostrzania (Defuzzification)**: Zamienia **zbiory rozmyte** uzyskane na wyjściu modułu wnioskowania na **ostre (rzeczywiste, liczbowe) wartości sterujące**. Wybór wartości ostrej nie zawsze jest prosty, stosuje się różne metody (np. metoda środka ciężkości).

## Uczenie się maszyn

### Wyjaśnij termin Brzytwy Ockhama

**Brzytwa Ockhama** to zasada, zgodnie z którą w wyjaśnianiu zjawisk **należy dążyć do prostoty**, wybierając takie wyjaśnienia, które opierają się na jak najmniejszej liczbie pojęć i założeń. W kontekście uczenia się maszyn (Ockham Learning), oznacza to, że **krótsze wyjaśnienie** obserwowanych danych powinno być preferowane nad dłuższym, przy założeniu, że wszystkie inne rzeczy są równe. Arystoteles stwierdził: „Im bardziej ograniczone – jeśli słusznie – tym lepsze”.

### Wymień warunki konieczne oraz motywacje tworzenia dla systemów uczących się

Warunki konieczne lub, precyzyjniej, **motywacje tworzenia systemów uczących się** obejmują:

- **Złożoność problemu**: gdy uzyskanie modelu teoretycznego jest bardzo kosztowne lub mało wiarygodne.
- **Rozmiary problemu**: gdy system analizuje dużą ilość danych, które mogą być przetwarzane tylko automatycznie, np. w analizie ekonomicznych lub medycznych baz danych.

Systemy uczące się są ważnym elementem sztucznej inteligencji. Uczenie się systemu to autonomiczna zmiana na podstawie doświadczeń prowadząca do poprawy jakości działania.

### Wymień metody (strategie) nabywania wiedzy oraz je scharakteryzuj

### Na czym polega kryterium stopu oraz czym jest metoda wyboru atrybutu w algorytmie?

W kontekście **budowy drzew decyzyjnych**, **kryterium stopu** określa warunki, po spełnieniu których węzeł w drzewie staje się liściem i nie jest dalej rozgałęziany. Kryteria stopu mogą być spełnione, gdy:

- W zestawie przykładów do danego węzła znajdują się już tylko przykłady opisujące jedną kategorię (węzeł staje się liściem z etykietą tej kategorii).
- Zbiór dostępnych atrybutów jest pusty, co może oznaczać błąd (brak możliwości jednoznacznego ustalenia kategorii) lub konieczność potraktowania węzła jako liścia z najliczniejszą kategorią w zestawie przykładów.

**Metoda wyboru atrybutu** (kryterium wyboru atrybutów) jest kluczową częścią algorytmu konstrukcji drzewa decyzyjnego, wpływającą znacząco na jego wygląd (np. złożoność). Polega na wyborze najlepszego atrybutu ze zbioru dostępnych, który pozwoli podzielić zbiór przykładów na mniejsze podzbiory. System ocen atrybutów opiera się na założeniu, że **najkorzystniejszym atrybutem jest ten, dzięki któremu kategorie przykładów w uzyskanych podzbiorach są mało zróżnicowane**.

### Wymień wady i zalety drzew decyzyjnych

### Omów pojęcie lasu losowego

**Las losowy** (losowy las decyzyjny) to **metoda zespołowa uczenia maszynowego**. Jest stosowana do klasyfikacji, regresji i innych zadań. Polega na **konstruowaniu wielu drzew decyzyjnych** w czasie uczenia. Wynik (klasa w przypadku klasyfikacji lub przewidywana średnia w przypadku regresji) jest **generowany na podstawie dominanty klas** (klasyfikacja) **lub przewidywanej średniej** (regresja) z poszczególnych drzew. Główną zaletą lasów losowych jest **zapobieganie tendencji drzew decyzyjnych do nadmiernego dopasowywania się do zestawu treningowego**. Na ogół znacząco poprawiają skuteczność algorytmu uczenia.

## Algorytmy genetyczne

### Wymień i opisz trzy główne klasy algorytmów ewolucyjnych

W źródłach wyróżnia się **cztery główne klasy algorytmów ewolucyjnych**:

1.  **Algorytmy genetyczne** (genetics algorithms – GA).
2.  **Programowanie genetyczne** (genetic programming – GP).
3.  **Strategie ewolucyjne** (evolutionary strategies – ES).
4.  **Programowanie ewolucyjne** (evolutionary programming – EP).

Opis skupia się głównie na algorytmach genetycznych i programowaniu genetycznym. **Algorytmy genetyczne** to algorytmy przeszukiwania oparte na mechanizmach doboru naturalnego i dziedziczności, przetwarzające populację osobników reprezentujących rozwiązania problemu. **Programowanie genetyczne** rozpoczyna się od losowej populacji programów (reprezentowanych jako drzewa) i stosuje operatory ewolucyjne w celu wyewoluowania programów lepiej rozwiązujących dane zadanie.

### Czym sa algorytmy genetyczne?

**Algorytmy genetyczne** (GA) są to **algorytmy przeszukiwania przestrzeni alternatywnych rozwiązań** oparte na mechanizmach **doboru naturalnego oraz dziedziczności**. Przetwarzają one **populację osobników**, z których każdy jest propozycją rozwiązania danego problemu. Każdemu osobnikowi przyporządkowana jest **wartość liczbowa zwana przystosowaniem osobnika**, określająca jakość reprezentowanego rozwiązania. Działanie algorytmu polega na iteracyjnym wykonywaniu operacji elementarnych w celu tworzenia kolejnych populacji złożonych z osobników powstałych z najlepiej przystosowanych przedstawicieli poprzedniego pokolenia. Algorytmy genetyczne są historycznie najstarszym i najlepiej poznanym kierunkiem obliczeń ewolucyjnych.

### Wyjaśnij własności algorytmów genetycznych. Jakie są ich zastosowania?

Własności algorytmów genetycznych (wg D. Goldberga) to:

- Nie przetwarzają bezpośrednio parametrów zadania, lecz **ich zakodowaną postać**.
- Prowadzą poszukiwania **wychodząc z wielu punktów** (populacji).
- Korzystają **wyłącznie z funkcji celu** (nie wymagają dodatkowych informacji o danym problemie).
- Stosują **probabilistyczne (losowe) reguły wyboru**.

**Zastosowania algorytmów genetycznych** obejmują:

- Zadania **optymalizacji**.
- Zadania **przeszukiwania**.
- **Uczenie robotów i urządzeń**.
- Modelowanie procesów biologicznych, ekonomicznych, ekologicznych, społecznych.
- Automatyczne programowanie.
- Projektowanie układów elektronicznych (np. układów logicznych, filtrów).
- Wspomaganie projektowania sieci neuronowych.
- Modelowanie naturalnych systemów odpornościowych.
- Badanie systemów społecznych.
  Są stosowane do poszukiwania rozwiązań problemów trudno definiowalnych matematycznie, gdy znany jest sposób oceny jakości rozwiązania.

### Wymień i wyjaśnij pojęcia używane w algorytmach genetycznych.

Podstawowe pojęcia w algorytmach genetycznych:

- **Gen** (cecha, znak lub detektor) – pojedynczy element chromosomu.
- **Chromosom** (ciąg kodowy lub łańcuch) – uporządkowany ciąg genów.
- **Genotyp** (struktura) – zespół chromosomów właściwych dla danego osobnika.
- **Fenotyp** – zestaw wartości odpowiadających danemu genotypowi.
- **Osobnik** – zbiór parametrów zadania stanowiących rozwiązanie problemu, zakodowany w postaci chromosomów.
- **Populacja** – zbiór osobników o określonej liczebności.
- **Allel** – wartość danego genu (lub wartość cechy).
- **Locus** – miejsce położenia danego genu w genotypie (lub chromosomie).
- **Funkcja przystosowania** (dopasowania, oceny) – pozwala ocenić stopień przystosowania poszczególnych osobników w populacji.

### Opisz mechanizm działania klasycznego algorytmu genetycznego

Mechanizm działania klasycznego algorytmu genetycznego składa się z następujących etapów:

1.  **Losowanie populacji początkowej**.
2.  **Ocena populacji (selekcja)**. Najlepiej przystosowane osobniki biorą udział w reprodukcji.
3.  Genotypy wybranych osobników poddawane są **operatorom ewolucyjnym**:
    - **Krzyżowania** (łączenie fragmentów genotypów rodziców).
    - **Mutacji** (wprowadzenie drobnych, losowych zmian do genotypów).
4.  **Utworzenie kolejnego pokolenia** (nowej populacji).
    Proces jest **iterowany** (powrót do punktu 2), jeśli nie znaleziono dostatecznie dobrego rozwiązania. W przeciwnym wypadku, uzyskuje się wynik.

### Na czym polega kodowanie parametrów zadania w algorytmie genetycznym?

**Kodowanie parametrów zadania** jest pierwszym krokiem konstrukcji algorytmu genetycznego. Polega na **zakodowaniu poszukiwanych parametrów zadania w postaci chromosomów**. Dobór odpowiedniej metody kodowania jest ważny i nie powinien faworyzować żadnego z możliwych rozwiązań. W klasycznym algorytmie genetycznym stosuje się **kodowanie binarne**, gdzie geny stanowią ciąg zer i jedynek. Dla kodowania liczb rzeczywistych stosuje się odwzorowanie przedziału liczbowego na przedział wartości dziesiętnych ciągu binarnego.

### Czym są metody selekcji stosowane w algorytmach genetycznych? Jaka jest ich relacja z funkcją przystosowania?

**Metody selekcji osobników** służą do wyboru "najlepszych" osobników z danej populacji (rodziców) w celu tworzenia nowej populacji (potomków). Każdy osobnik jest **oceniany za pomocą funkcji przystosowania**. Celem selekcji jest, aby kolejne populacje charakteryzowały się wyższą średnią wartością funkcji przystosowania.

Relacja z funkcją przystosowania jest kluczowa: **większa wartość funkcji przystosowania osobnika powinna oznaczać większe prawdopodobieństwo jego wyboru** do nowo tworzonej populacji.

Przykładowe metody selekcji to:

- Metoda koła ruletki (wielkość wycinka koła proporcjonalna do wartości funkcji przystosowania).
- Selekcja rankingowa (osobniki sortowane wg funkcji przystosowania, ranga jest argumentem funkcji wyznaczającej współczynnik selekcji).
- Selekcja turniejowa (osobniki rywalizują w turniejach, zwycięzcy przechodzą dalej).
- Selekcja (μ + λ).

### Opisz czym są operatory genetyczne?

**Operatory genetyczne** są stosowane do populacji osobników otrzymanej w wyniku selekcji. Ich celem jest **wygenerowanie nowego pokolenia**, które powinno być lepiej dopasowane do założonego środowiska (dążenie do uzyskania lepszego rozwiązania). W klasycznym algorytmie genetycznym stosowane są dwa główne operatory:

- **Krzyżowanie**: Ma za zadanie **łączyć cechy pochodzące z różnych osobników**. Jest to operator dominujący, stosowany częściej niż mutacja. Zazwyczaj z pary rodzicielskiej tworzy parę potomków poprzez losowanie punktu(ów) krzyżowania i wymianę segmentów chromosomów.
- **Mutacja**: Polega na **zmianie wartości wybranego elementu ciągu kodowego** (np. zanegowaniu bitu przy kodowaniu binarnym lub zamianie genów). Jej funkcją jest wprowadzanie różnorodności w populacji, zapobieganie przedwczesnej zbieżności algorytmu i zapewnienie, że reprodukcja i krzyżowanie nie wyeliminują potencjalnie korzystnego materiału genetycznego. Wykonywana jest bardzo rzadko.

### Wyjaśnij na czym polega Teoria Schematów. Omów jej kluczowe założenia oraz pojęcia

**Teoria schematów** stanowi **formalną analizę działania algorytmów genetycznych**. Jej twórcą jest J. H. Holland.

Kluczowe pojęcia i założenia:

- **Schemat**: Jest to **wzorzec opisujący podzbiór ciągów (chromosomów)**, które są podobne ze względu na **ustalone pozycje**. Do definiowania schematów używa się alfabetu {0, 1, _}, gdzie '_' oznacza wartość 0 lub 1 (obojętną).
- **Rozpiętość schematu** (d(Sj)): Nazywana jest odległością między dwiema skrajnymi pozycjami ustalonymi w schemacie.
- **Rząd schematu**: Określany przez liczbę ustalonych pozycji (bez symboli '\*') w schemacie (choć definicja rzędu nie jest wprost podana w źródle, wynika z kontekstu Twierdzenia o schematach).

**Twierdzenie o schematach**: Jest kluczowym założeniem teorii. Mówi, że **krótkie (o małej rozpiętości), niskiego rzędu i oceniane powyżej średniej schematy uzyskują wykładniczo rosnącą liczbę łańcuchów (reprezentantów) w kolejnych pokoleniach algorytmu genetycznego**.

- **Hipoteza o blokach budujących**: Algorytm genetyczny dąży do znalezienia rozwiązania zbliżonego do optymalnego poprzez **zestawienie krótkich (o małej rozpiętości), niskiego rzędu schematów o dużej wydajności działania**, zwanych **blokami budującymi**.

## Programowanie Genetyczne

### Czym różni się programowanie genetyczne od klasycznego algorytmu genetycznego?

### Jakie typy węzłów są powszechnie używane w programowaniu genetycznym?

###
