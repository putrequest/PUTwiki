**Biały wywiad** (ang. *open-source intelligence*, OSINT, rozpoznanie otwartoźródłowe) - kategoria rozpoznania oraz forma wywiadu gospodarczego, polegająca na gromadzeniu informacji pochodzących z ogólnodostępnych źródeł. Wywiadowcy posługują się wyłącznie jawnymi i etycznymi metodami pozyskiwania informacji.

Ważne fakty:

* Choć OSINT wywodzi się z tradycyjnej kryminalistyki tak codzienna praktyka pokazuje, ze przenika się z wieloma innymi dziedzinami, przede wszystkim z informatyką śledzczą (forensics).
* Swoje wymagania pod kątem wiedzy narzuci kazde śledztwo, a rozpoznawanie branż o których nie mamy pojęcia wymusi na nas zapoznanie się z prawami jakie nią kierują np. badając anomalie cenowe na rynku nawozów rolniczych będziesz musiał nauczyć się odrózniać fosforany od azotanów.
* OSINT to ruletka. W niektórych przypadkach poznamy całą historię czyjegoś życia, w innych dana osoba może w ogóle nie istnieć.
* OSINT nie jest zjawiskiem nowym. Techniki otwartego wywiadu stosowano już w czasie I wojny światowej kiedy to nikt nie myślał o kodowaniu kanałowym łączności radiowej i ryzyku jej podsłuchiwania. Obecnie wraz z rozwojem społeczeństwa informacji zaczęto zwracać na niego uwagę, a prawdziwy rozgłos zyskał w momencie wybuchu wojny na Ukrainie. O historycznych przypadkach OSINTu przeczytasz [tutaj](https://www.intelmsl.com/osint-history/).

## Aspekt prawny

> Art. 267. KK [Bezprawne uzyskanie informacji]
>
> §  1.  Kto bez uprawnienia uzyskuje dostęp do informacji dla niego nieprzeznaczonej, otwierając zamknięte pismo, podłączając się do sieci telekomunikacyjnej lub przełamując albo omijając elektroniczne, magnetyczne, informatyczne lub inne szczególne jej zabezpieczenie,
podlega grzywnie, karze ograniczenia wolności albo pozbawienia wolności do lat 2.
>
> §  2.  Tej samej karze podlega, kto bez uprawnienia uzyskuje dostęp do całości lub części systemu informatycznego.
>
> §  3.  Tej samej karze podlega, kto w celu uzyskania informacji, do której nie jest uprawniony, zakłada lub posługuje się urządzeniem podsłuchowym, wizualnym albo innym urządzeniem lub oprogramowaniem.
>
> §  4.  Tej samej karze podlega, kto informację uzyskaną w sposób określony w § 1-3 ujawnia innej osobie.
>
> §  5.  Ściganie przestępstwa określonego w § 1-4 następuje na wniosek pokrzywdzonego.

Zgodnie z definicją OSINT opiera się o legalne i powszechnie dostępne źródła informacji wobec, których przepis ten nie znajduje zastosowania. Dotyczy on jednak szeroko rozumianego włamywania się do systemów i urządzeń. Jezeli np. udałoby nam się pozyskać login i hasło przechowywane w indeksowanym przez Google pliku, skorzystanie z takich poświadczeń stanowi przestępstwo. Podobnie z sytuacją gdy uda się wstrzelić poprzez admin/admin.

> Art.  190a. KK [Uporczywe nękanie. Kradzież tożsamości]
>
> §  1.  Kto przez uporczywe nękanie innej osoby lub osoby dla niej najbliższej wzbudza u niej uzasadnione okolicznościami poczucie zagrożenia, poniżenia lub udręczenia lub istotnie narusza jej prywatność,
podlega karze pozbawienia wolności od 6 miesięcy do lat 8.
>
> §  2.  Tej samej karze podlega, kto, podszywając się pod inną osobę, wykorzystuje jej wizerunek, inne jej dane osobowe lub inne dane, za pomocą których jest ona publicznie identyfikowana, przez co wyrządza jej szkodę majątkową lub osobistą.
>
> §  3.  Jeżeli następstwem czynu określonego w § 1 lub 2 jest targnięcie się pokrzywdzonego na własne życie, sprawca podlega karze pozbawienia wolności od lat 2 do 15.
>
> §  4.  Ściganie przestępstwa określonego w § 1 lub 2 następuje na wniosek pokrzywdzonego.

Zastosowanie tego przepisu dotyczy głównie tworzenia kont operacyjnych. O ile mają one wyglądać jak najbardziej prawdziwie, tak korzystanie z danych istniejących osób nosi znamiona kradzieży tozsamosci. Mozemy stworzyc konto na zmyślone personalia ze zdjęciem wygenerowanym przez AI. Nie możemy natomiast nazwać profilu Teofil Jesionowski i wrzucić na profilowe zdjęcia JM Rektora.

> Art. 6 pkt. 1 RODO
>
> Przetwarzanie jest zgodne z prawem wyłącznie w przypadkach, gdy – i w takim zakresie, w jakim – spełniony jest co najmniej jeden z poniższych warunków:
>
> a)     osoba, której dane dotyczą wyraziła zgodę na przetwarzanie swoich danych osobowych w jednym lub większej liczbie określonych celów;
>
> b)     przetwarzanie jest niezbędne do wykonania umowy, której stroną jest osoba, której dane dotyczą, lub do podjęcia działań na żądanie osoby, której dane dotyczą, przed zawarciem umowy;
>
> c)     **przetwarzanie jest niezbędne do wypełnienia obowiązku prawnego ciążącego na administratorze;**
>
> d)     przetwarzanie jest niezbędne do ochrony żywotnych interesów osoby, której dane dotyczą, lub innej osoby fizycznej;
>
> e)     **przetwarzanie jest niezbędne do wykonania zadania realizowanego w interesie publicznym lub w ramach sprawowania władzy publicznej powierzonej administratorowi;**
> 
>f)      **przetwarzanie jest niezbędne do celów wynikających z prawnie uzasadnionych interesów realizowanych przez administratora lub przez stronę trzecią**, z wyjątkiem sytuacji, w których nadrzędny charakter wobec tych interesów mają interesy lub podstawowe prawa i wolności osoby, której dane dotyczą, wymagające ochrony danych osobowych, w szczególności gdy osoba, której dane dotyczą, jest dzieckiem.

RODO określa podstawy przetwarzania danych osobowych osób fizocznych na terenie UE. Dla OSINTowców najważniejszy jest kontekst wypełnienia przez administratora obowiązków prawnych. Może to obejmować np. konieczność publikowania oświadczeń majątkowych przez osoby publiczne. Z drugiej strony art. 6 wspomina o zgodzie wyrażonej przez osobę, której dane dotyczą. Jeżeli jest to np. zgoda wydana Facebookowi (Meta) osoba taka sama poświadczyła, że zdaje sobie sprawę z faktu, że jej tresci będą dostępne w tym serwisie i mogą być dostępne publicznie. Tym samym RODO nie określa zakresu działań OSINTowców, a jedynie definiuje dlaczego pewne informacje mogą znaleźć się w domenie publicznej.

**Jeżeli zasób jest dostępny publicznie nie potrzebujemy zgody na skorzystanie z niego.** Zastosowanie mogą mieć tu jednak odrębne przepisy np. ustawa o prawie autorskim i prawach pokrewnych.

## Terminologia

* Figurant - cel rozpoznania czyli dana osoba, firma lub instytucja 
* Selektor - informacja powiązana z figurantem np. e-mail, NIP, adres zamieszkania czy imię psa
* Transformacja - przekształcenie selektora w inny selektor
* Śledztwo - zbiór działań mających uzyskać określone dane dot. figuranta
* False-positive (błąd pierwszego rodzaju) - informacja fałszywie dodatnia

* HUMINT, *human intelligence* - osobowe źródła informacji (OZI)
* SOCMINT, SMINT, *social media intelligence* - wywiad mediów społecznościowych
* SIGINT, *signal intelligence* - rozpoznanie elektromagnetyczne
* TECHINT, *technical intelligence* - rozpoznanie techniczne
* GEOINT, *geographical intelligence* - rozpoznanie w oparciu o geolokalizację i kartografię
* FININT, *finance intelligence* - rozpoznanie finansowe
* OPSEC, *operations security* - bezpieczeństwo operacyjne

### Cykl wywiadowczy 

Polski proces wywiadowczy definiuje doktryna *rozpoznanie wojskowe D/2*, zawiera czteroetapowy model cyklu rozpoznawczego realizowanego przez Wojsko Polskie i polskie służby wywiadowcze. Nie jest to jednak jedyny model. Bardzo często stosuje się też model amerykański oraz australisjki. W ogólności można przyjąć następujący cykl zgodny ze standardami NATO, który jest klasycznym modelem wojskowym.

1. **Ukierunkowanie** to faza inicjująca proces rozpoznania lub nadająca mu nowy kierunek, cel bądź zakres. Dzieli się ona na dwa etapy – określenie wymagań informacyjnych i przygotowanie działań rozpoznawczych;
2. **Gromadzenie** polega na wykorzystaniu potencjału informacyjnego (wszystkich dostępnych źródeł) i wykonawczego systemu rozpoznania (operacyjnego pozyskiwania danych) w celu zdobycia danych oraz dostarczenia ich do przetworzenia w wiadomości rozpoznawcze. Gromadzenie danych również dzieli się na dwa etapy – pozyskiwanie (użycie wszelkich źródeł i sposobów zdobywania danych oraz ich koordynacja) i zbieranie (terminowe skupienie pochodzących z różnych źródeł, rozproszonych zbiorów informacji, a następnie przekazanie ich do komórek analitycznych);
3. **Przetwarzanie** to przekształcanie zgromadzonych danych w wiadomości rozpoznawcze. Głównymi etapami tej fazy są: zestawianie (ewidencja), ocena (pewności źródła i wiarygodności), analiza i integracja oraz interpretacja;
4. **Rozpowszechnianie** jest terminowym i celowym przekazywaniem wiadomości rozpoznawczych z pomocą odpowiednich środków w określonej formie uprawnionym podmiotom. Owe formy dzielą się na: rozpowszechnianie elektroniczne, pisemne i graficzne, a także ustne.

![cyklwywiadowczy](Australijski_model_cyklu_wywiadowczego.jpg)

W swoich załozeniach śledztwo ma doprowadzić do ustalenia konkretnej informacji np. czy osoba X jest udziałowcem spółki Y. Przeprowadzenie śledztwa, które zbierze "wszystko" poskutkuje jedynie ślepą nieskończoną pętlą, w której będziemy oddalać się od celu śledztwa. Innymi słowy nie ma sensu badać rodziny figuranta 9 pokoleń wstecz.

## [Źródła informacji](sources/sources_wiki.md)

### Google Hacking

Google hacking – termin opisujący stosowanie specjalnie dobranych zapytań dla popularnej wyszukiwarki internetowej Google, które pozwalają na odszukanie informacji przydatnych z punktu widzenia analizy bezpieczeństwa innych witryn WWW. Wbrew nazwie działania takie można prowadzić również dla innych popularnych wyszukiwarek jak Bing, Yandex itp.

* [Operatory Google](https://www.google.pl/intl/pl/help/operators.html)
* [Operatory Bing](https://support.microsoft.com/en-gb/topic/advanced-search-options-b92e25f1-0085-4271-bdf9-14aaea720930)
* [Operatory Yandex](https://yandex.com/support/direct/keywords/symbols-and-operators.html)

Przykłady dorków:

* inurl:microsoft filetype:iso – pliki obrazów płyt ze stron zawierających w URL słowo Microsoft
* filetype:bak inurl:"htaccess|passwd|shadow|htusers" – pliki konfiguracyjne serwisów WWW
v intitle:"Index of" .mysql_history – historia zapytań SQL z serwisów WWW
* 90010100000..99123199999 +pesel filetype:xls – pliki Excela zawierające numery PESEL z danego przedziału
* site:cat.put.poznan.pl filetype:pdf intitle:plan semestr 7 – plany zajęć w formie PDF dla semestru siódmego ze strony WIiT.

Należy pamiętać, że Google nie musi indeksować każdego zasobu, ale z drugiej strony indeksuje często to co niekoniecznie powinno być publicznie dostępne. W przypadku wysyłania wielu złożonych zapytań Google może wymagać wypełniania Captchy.

## Software
* [Maltego](https://www.maltego.com) - oprogramowanie pełni dwie role. Z jednej strony pozwala na obrazowanie selektorów w postaci grafów i umozliwia stworzenie całej "tablicy dowodów". Z drugiej pozwala ono na automatyzację transformacji np. poprzez integrację z róznymi API. Jest jedną z popularniejszych aplikacji, ale pomimo popularnego przeświadczenia nie zrobi śledztwa za nas. Więcej o Maltego [TUTAJ](maltego/maltego_wiki.md).
* [Recon-ng](https://github.com/paralax/Recon-ng) - alternatywne dla Maltego narzędzie słuzące do prowadzenia transformacji automatycznych w oparciu o dołączone wtyczki.
* [Project Sherlock](https://github.com/sherlock-project/sherlock) - oprogramowanie do wyszukiwania kont w oparciu o pseudonim.
* [Spiderfoot](https://github.com/smicallef/spiderfoot) - program przeznaczony do threat intelligence.
* [Exiftool](https://exiftool.org) - oprogramowanie do przeglądania metadanych. Podstawowa wersja jest tekstowa.
* [Shodan](https://www.shodan.io) - taki Google, ale wyszukujący urządzenia sieciowe zamiast stron WWW.
* [Hunchly](https://www.hunch.ly) - oprogramowanie integrowane z przeglądarką internetową. Pozwala oznaczać i archiwizować konkretne zasoby przeglądane w internecie w oparciu o słowa kluczowe.
* [Youtube-DL](https://github.com/ytdl-org/youtube-dl) - oprogramowanie słuzące do pobierania filmów m.in. z Youtuba. Z powodzeniem działa tez na innych platformach.
* [Data Miner](https://chromewebstore.google.com/detail/data-scraper-easy-web-scr/nndknepjnldbdbepjfgmncbggmopgden?pli=1) - wtyczka do Chroma umozliwiająca automatyczne pobieranie treści ze stron internetowych i ich zapisywania w ustrukturalizowanym pliku.
* [VideoDownloadHelper](https://www.downloadhelper.net) - wtyczka służąca do pobierania wideo ze stron WWW.
* [DownThemAll](https://www.downthemall.net) - wtyczka do masowego pobierania plików ze stron WWW.
* [dnsenum](https://www.kali.org/tools/dnsenum/) - narzędzie do enumeracji przestrzeni DNS. Pozwala na znajdowanie subdomen, które nie są przechowywane w bazach WHOIS.

## OPSEC
**Bezpieczeństwo operacyjne** (ang. *operations security*, OPSEC) - proces, który identyfikuje krytyczne informacje w celu ustalenia, czy przyjazne działania mogą być obserwowane przez wywiad wroga. Określa, czy uzyskane informacje mogą być użyteczne. W naszych przypadku to wdrożenie środków mających na celu zniwelowanie ryzyka ujawnienia krytycznych informacji. Nie chcemy w końcu by ktoś dowiedział się, ze się nim interesujemy oraz zeby odwiedzili nas smutni panowie w garniturach. Początki tego terminu sięgają wojny w Wietnamie.

OPSEC moze dotyczyć wielu obszarów; od kwesti połączenia z internetem po niepodawanie swojego prawdziwego nazwiska w formularzu kontaktowym na stronie WWW. **Zachowanie anonimowości jest mozliwe, ale wymaga wielu wyrzeczeń, a błędy mogą być kosztowne.** Nic nie da łączenie się ze stroną przez Tor-over-VPN i rejestrowanie się na jednorazowy mail jezeli w formie płatności podamy naszą kartę debetową. Pamiętaj, że niekażde śledztwo wymagać będzie stosowania wszystkich środków bezpieczeństwa operacyjnego.

### Konta operacyjne
Konta operacyjne słuzyć mają przeglądaniu m.in. mediów społecznościowych. W przeciwieństwie do pospolitego "fejka" mają one wyglądać jak najbardziej prawdziwie i posiadać mozliwie długą historię. W tym przypadku przydatne okazą się być generatory [personaliów](https://www.fakenamegenerator.com) czy [twarzy](https://thispersondoesnotexist.com). Warto jest jednak zaznaczyć, ze niektóre platformy (np. Facebook) są wyczulone na treści z generatorów, dlatego warto poddać je mniejszej lub większej obróbce.

O czym warto pamiętać:

* Wiele serwisów (np. FB) jest wyczulonych na zdjęcia generowane przez AI. Da się jednak oszukać algorytmy modyfikując zdjęcie często w prosty sposób np. kadrowanie. Działa to np. w przypadku stosowania zdjęć z *thispersondoesnotexist.com*, w których pozycja oczu osoby jest prawie zawsze w tym samym miejscu.
* Niektóre serwisy mogą wymusić dodatkowe uwierzytelnianie np. numerem telefonu (jak Google), i sięgać nawet po skrajne metody takie jak żądanie przesłania skanu dowodu tożsamości (czasem Facebook).
* Warto jest spisać historię/biografię postaci, która ma stać za wybranym kontem operacyjnym: kim jest, skąd pochodzi, gdzie pracuje, ile ma dzieci i jaki sos do kebaba lubi najbardziej.
* Zalecane jest stosowanie kont operacyjnych razem z innymi narzędziami OPSECowymi np. sieciami VPN oraz logowanie sie na nie na maszynach wirtualnych.

### Łączenie z siecią

Do ukrywania IP mozna wykorzystać między innymi:

* VPNy i Proxy - w załozeniu mają ukryć nasz faktyczny adres IP. Nie da się jednak jednoznacznie stwierdzić czy dostawca VPNa nie trzyma logów i nie sprzeda ich słuzbom.
* Publiczne punkty dostępowe - wbrew ich "wątpliwemu bezpieczeństwu" korzystanie z publicznego Wi-Fi może utrudnić namierzenie danej osoby z uwagi na dużą rotację podłączonych urządzeń. Należy zwrócić jednak uwagę na aspekt bezpieczeństwa przy korzystaniu z takiego publicznego AP i unikania nieszyfrowanej komunikacji. Ponadto właściciel AP może w dalszym ciągu obserwować z jakimi adresami IP nawiązujemy połączenie nawet jeżeli sama treść komunikacji jest szyfrowana.
* [Tor](https://www.torproject.org/download/) - łączenie z siecią wykorzystujące [trasowanie cebulowe](https://pl.wikipedia.org/wiki/Trasowanie_cebulowe). Tor łączy się z serwerem docelowym poprzez szyfrowaną komunikację przechodzącą przez kilka (zwykle 4-5) węzłów pośredniczących. W teorii powoduje to, że żaden węzeł nie ma pełnej wiedzy o źródle i celu ruchu, jednak kosztem niskiej przepływności i opóźnień. Należy pamiętac, ze węzły Tora są publicznie znane a np. nasz ISP moze łatwo ustalic, że się z nim łączymy. Tor może zostać połączony z siecią VPN w konfiguracji VPN-over-Tor lub Tor-over-VPN, w którym wchodzimy do tunelu VPN po przejściu przez Tora lub odwrotnie.

### Komunikacja

* Anonimowe maile np. [Proton](https://proton.me), [Tutanota](https://tuta.com)
* Maile jednorazowe np. [Tempmail](https://temp-mail.org/pl/)
* Numery tymczasowe np. [ReceiveSMS](https://receive-smss.com)
* Karty SIM bez rejestracji. Obecnie najtaniej wychodzi czeski T-Mobile (kilkanaście PLN na allegro).

### Maszyny wirtualne

Przyjmuje się, ze działania operacyjne powinny być prowadzone w przygotowanych do tego izolowanych środowiskach a kazde powinno odpowiadać danemu śledztwu. Warto jest zapewnić pełną izolację środowiska operacyjnego oraz jego bezpieczeństwo np. poprzez szyfrowanie.

Pod kątem komputerów sprawdzają się takie hipervisory takie jak VMware czy Hyper-V. Dla urządzeń mobilnych wartym rozwazenia jest emulator Android Studio lub [Genymotion](https://www.genymotion.com). Im więcej funkcji posiada oprogramowanie tym lepiej.

Warto pamiętać, ze identyfikację umozliwić moze wiele innych aspektów np. wersja oprogramowania, używany język czy wtyczki w przeglądarce - tzw. [fingerprint przeglądarki](https://amiunique.org). Jeżeli chcesz zobaczyc co może zdradzic o Tobie samo zachowanie w przeglądarce zajrzyj [tutaj](http://clickclickclick.click/).

Używany system operacyjny należy dostosować do potrzeb i przeznaczenia. Warto rozdzielić maszynę do operacyjnego pozyskiwania danych z maszyną do logowań na konta operacyjne. Z uwagi na możliwość niektórych serwisów do wykrywania systemu operacyjnego klienta warto jest skupić się na popularnych wersjach Windowsa. Do przetwarzania danych warto jest spojrzeć na dedykowane ku temu dystrybucje Linuxa np. Kali lub Tsurugi.

## Ciekawe case study
* [Otrucie Skripala](https://www.bellingcat.com/news/uk-and-europe/2018/10/09/full-report-skripal-poisoning-suspect-dr-alexander-mishkin-hero-russia/)
* [Rosyjska dezinformacja w USA](https://medium.com/@brichett13/social-media-intelligence-case-study-an-osint-data-engineers-investigation-into-american-813ecf2463d6)
* [Sprawa Natalii Janoszek](https://youtu.be/oKYBBVQa8NY)
* [Kampania scamowa](https://keyfindings.blog/2019/08/28/unravelling-the-norton-scam/)
* [Anatomy of a killing](https://twitter.com/BBCAfrica/status/1044186344153583616)

## Metryka zmian
| Wersja       | Data       | Osoba             | Opis zmian                         |
| ------------ | ---------- | ----------------- | ---------------------------------- |
| v1.0.0       | 08.03.2024 | Grzegorz Jaskuła  | Wersja bazowa                      |
