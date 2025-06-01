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
