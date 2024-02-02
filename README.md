# Návrh a ověření prototypu elektronického herbáře

[Online verze](<https://vse-my.sharepoint.com/:w:/g/personal/olim02_vse_cz/EXrRd2VRxYxDpbQ76hZnw-UB2PpayTA-KKMjYzs7VwuYWw?e=1uGk4o>)  
[Offline verze](.attachments/82a0bb8fbb84d20f391beade34af05bf5c3da56c.docx) 

**Vedoucí DP: Ing. et Ing. Michal Doležel, Ph.D.**
**Letní semestr 2023/2024**

## Abstrakt
Cílem této práce je navrhnout a ověřit prototyp elektronického . Návrh prototypu bude utvářen pomocí user-centered metodiky Design Thinking.  Následné kapitoly rozeberou témata související s koncovým produktem jako praktiky zaznamenávání souřadnic nálezů rostlin v přírodě, archivace rostlin do herbářů a jiné elektronické databázové systémy rostlin. Metodika práce bude pojednávat o jednotlivých fázích projektu, rozhovorech s vědeckými pracovníky, jakým způsobem se prototyp aplikace vyvíjel a bude popisovat průchod jednotlivými aktivitami design thinkingu a testování uživatelů. Výsledkem práce bude celkové zhodnocení designu prototypu, výsledky testování uživatelů a zhodnocení metodiky design thinking.

## Abstract
The aim of this thesis is to design and validate a prototype application in Figma tool, which will meet the functional requirements of the molecular biology laboratory staff at the Faculty of Science of the University of South Bohemia. The design of the prototype will be shaped using user-centered Design Thinking methodology. In the first chapter, the thesis will discuss the history of the methodology, its transformation from innovation management to its current form, its principles and practices. In the second chapter, the thesis will focus on UX and UI design practices and their testing. Subsequent chapters will discuss end-product related topics such as the practices of recording coordinates of plant finds in nature, archiving plants in herbariums, and other electronic plant database systems. The methodology of the thesis will discuss the different phases of the project, interviews with researchers, how the prototype application was developed, and will describe the flow through the various design thinking and user testing activities. The thesis will result in an overall evaluation of the prototype design, the results of user testing and an evaluation of the design thinking methodology.

## Úvod

Nedílnou součástí botanického výzkumu je mj. floristika – mapování jednotlivých druhů rostlin v přírodě a sledování změn jejich rozšíření. Zásadní fází je pak určování rostlin, které se často neobejde bez následné analýzy optickým mikroskopem. Právě takovéto analýzy zaměřené na reprodukční vlastnosti rostlin mohou významně přispět k odhalení genetického kontextu zkoumaných rostlin. Díky této kombinaci lze porozumět nejen šíření rostlin, ale i jeho evolučním příčinám.

Herbář je možné popsat jako způsob archivace nálezů rostlin v přírodě. Nálezy jsou vysušeny, většinou připevněny k listu papíru a opatřeny štítkem informujícím o jejich nálezcích, lokaci a stručných informací o podmínkách, ve kterých byla rostlina nalezena. Botanické laboratoře po celém světě si vytvářejí vlastní systémy sběru a uchovávání těchto vzorků podle problematiky, na kterou se zaměřují. Podle Brownovy univerzity jsou tyto herbářové sbírky využívány mimo jiné k pochopení populačních trendů vzácných rostlin, studium šíření a preferencí invazních druhů nebo provádění etnobotanických studií (Magdalena, 2018).

Sledování výskytu rostlin a jejich genetické informaci se mimo jiné věnují i pracovníci Laboratoře molekulární biologie rostlin Přírodovědecké fakulty Jihočeské univerzity. Katedra botaniky PřF JU uvádí dva hlavní účely budování vlastního herbáře. Prvniím je výuka, kdy herbář slouží jako srovnávací materiál pro studenty, při vlastním rozpoznávání obtížnějších skupin a druhým je místo uložení dokladových herbářových položek k odborným pracím zaměstnanců a studentů katedry (Katedra botaniky PřF JU, 2023).

Laboratoř se mimo jiné zaměřuje na výzkum kapraďorostů, kde součástí výzkumných aktivit je detekce abortovaných (mrtvých) a fertilních (živých) spor (výtrusů) při jejich pozorování pod optickým mikroskopem.

Do rozšiřování vědeckého poznání tak ve floristice spadají tyto aktivity: hledání a mapování výskytu a šíření rostlin v přírodě, analýza buněk a tkání optickým mikroskopem, archivace nálezů do herbáře a zanesení dat a nových poznatků do databází a informačních systémů.

## Vymezení problému

Při mapování výskytu rostlin v terénu je zapotřebí mít informace o přesné lokalitě nálezu, popsat či vyfotit prostředí, ve kterém se nález vyskytoval a následně tyto informace zadat do databáze. Aktuálně taková aktivita probíhá tak, že pracovník má v terénu po ruce GPS lokátor, sáčky pro sběr vzorků a zápisník na poznámky. Při nalezení požadované rostliny uloží do lokátoru aktuální polohu, vloží vzorek do sáčku a ten popíše pořadovým číslem z lokátoru. Díky tomu může poté v laboratoři zpětně určit, ke kterým vzorkům patří dané souřadnice. Následně si, pokud to je potřeba, zapíše do zápisníku bližší informace o místě nálezu. Tyto informace pak musí opět zadávat do databáze zpětně.

Druhá část problému se týká mikroskopického výzkumu laboratoře. Jednou z aktivit, které pracovníci vykonávají, je pozorování výtrusů kapradin a plavuní či pylových zrn krytosemenných rostlin. Během tohoto pozorování pracovníci počítají množství živých a mrtvých buněk zkoumaného vzorku. V řádu jednotek spočtených buněk se jedná o relativně rychlou činnost. Pokud se však nachází pod mikroskopem počet buněk v řádu vyšších desítek až nízkých stovek kusů, jedná se o časově velmi náročnou činnost. Mezi ukazatele mortality buněk může patřit jejich tvar, barva, průsvitnost, nebo také jejich reakce (zbarvení) na různé chemické směsi a látky.

Pro efektivní spolupráci laboratoří nejen na území České republiky, ale i v zahraničí, je v zájmu pracovníků uchovávat informace o svém výzkumu a data o rostlinách v digitální podobě. Většina laboratoří využívá svůj vlastní databázový systém uzpůsobený jejich konkrétním potřebám.

Laboratoř molekulární biologie PřF JČU ke dni psaní projektu DP využívá webovou PHP aplikaci Vratička. Tato aplikace při svém vzniku nebyla zamýšlena jako floristická databáze, ale byla v ni postupně modifikována. S ohledem na způsob vzniku a následný vývoj, aplikace nikdy neodpovídala skutečným potřebám vědeckých pracovníků a stala se více administrativní zátěží nežli pomocníkem. Přestože většina připomínek na funkčnost aplikace byla řešena záplatováním stávajícího řešení, vyskytuje se v aplikaci doposud mnoho funkčních i technických nedostatků. Jedním z takových problémů, o kterém se jedna pracovnice zmínila, je například smazání vyplněného formuláře při jeho chybném vyplnění. Dalším je nutnost přecházet na jiné stránky aplikace pro získání informací potřebných pro vyplnění daného formuláře, či nutnost instalace dalších softwarů pro import dat.

Vědečtí pracovníci se tak při výzkumu potýkají se třemi hlavními problémy:
1. nemožnost zadávat informace o nálezech přímo v terénu v místě nálezu,
2. ruční počítání buněk pod mikroskopem a
3. nevhodné aktuální softwarové řešení, ať již z hlediska funkčnosti, UX či UI.

## Rešeršní strategie rešerše provedené v projektu DP

Část rešerše byla provedena pozorováním a rozhovory s vědeckými pracovníky laboratoře. Díky tomu, bylo možné rychle pochopit, jak v obecné rovině funguje laboratoř pro floristický výzkum, jaký software aktuálně používá a jaké jsou jeho nedostatky a potřeby. Součástí tohoto průzkumu bylo i několik cest do terénu, kde jsem měl možnost pozorovat, jakým způsobem sběr vzorků v přírodě probíhá, a také se na něm účastnit.

Rešerše na internetu byla realizována pomocí nástrojů Google advanced search, ProQuest a elektronických zdrojů VŠE. Vyhledávání bylo omezeno ve větší části na práce zveřejněné v posledních pěti letech zejména s klíčovými slovy v těchto kombinacích:

- Electronic herbarium
- Electronic management system herbarium
- Digital herbarium
- Design thinking

V rámci výzkumu metodiky Design thinking se autor zaměřil hlavně na články Tima Browna (iniciátora této metodiky) či články, které jej citovaly. Vzhledem k popularizaci metodiky teprve od roku 2008, vyhledával autor články staré do pěti let, aby vyfiltroval spíše již zralejší přístupy. Mnoho článků i odborných prací se odkazovalo na uzamčené články Harvard Business Review a zakladatele společnosti IDEO.

## Cíle diplomové práce

Pracovníci laboratoře potřebují v zefektivnit sběr dat a vzorků v terénu (zadávání lokace nálezu a potřebných údajů do aplikace v mobilu), jejich laboratorní analýzu (rozpoznávání a počítání mikroskopických buněk pomocí Machine Learningu) a následnou administrativu s těmito procesy spojenou (zadávání dat o nálezcích, projektech, výzkumech a taxonomie rostlin) do jednotné aplikace – herbáře.

Cílem práce je za pomocí evolučního prototypováním navrhnout a uživatelskými testy ověřit horizontální prototyp multiplatformního systému pro podporu archivace a molekulárního rozboru rostlin.

Hlavním cílem práce je tedy navrhnout a ověřit prototyp takové aplikace.

Jednotlivé cíle jsou rozděleny následovně:
1. Získat informace o aktuálním stavu a potřebách pracovníků laboratoře
2. Navrhnout architekturu systému elektronického herbáře
3. Vytvořit prototyp UI aplikace ve Figmě pokrývající potřeby pracovníků
4. Ověřit prototyp u vědeckých pracovníků laboratoře

## Metody použité k dosažení cílů
Způsob sběru požadavků a návrhu aplikace bude odpovídat metodice Design thinking. Metodika používá user-centric přístup (zaměření na uživatele). Jejím cílem je co nejužším zapojením uživatelů rozšiřovat znalosti o problému a hledání jeho řešení ještě před samotnou implementací produktu (Brown, 2008).

Metodika cyklicky prochází fázemi inspirace (pozorování problematiky), ideace (proces hledání nápadů k řešení problému) a implementace (design prototypu). Tyto fáze jsou pak podle preferencí rozdělovány nejčastěji do čtyř až sedmi kroků. Tato práce využije systém pěti kroků: Empatizace, Definice, Ideace, Implementace a Ověření (Benedikt, 2022).

Empatizace je o porozumění uživatelům a problémům, kterým čelí. V rámci této práce již byl proveden úvodní průzkum aktivit pracovníků nejen participací při jejich výkonu, ale i rozhovory s pracovníky a bude nadále tímto způsobem vykonáván.

Dalším krokem je definice problému, ve které autor na základě sběru dat z kroku empatizace, sestaví kombinaci souboru aktérů a user stories. Diagramy pro popis use cases a procesů budou používat notaci UML a BPMN.

Krok ideace bude zahrnovat komunikaci s uživateli a po první iteraci návrhu řešení bude nejčastějším návratovým bodem pro další iterace. V tomto kroku budou navrhovány řešení zpětné vazby získané z testování prototypu.

Implementace prototypu bude probíhat v online nástroji Figma. Autor se rozhodl rozdělit implementaci na dva dílčí návrhy řešení: wireframe a high-fidelity prototyp. Nejdříve bude design navrhován jako low fidelity wireframe (design s nízkou úrovní detailu, užívaný nejčastěji pro grafické znázornění implementace user stories), aby bylo možné co nejefektivněji zajistit naplnění všech user stories v prototypu. Po sestavení wireframu pokrývajícího všechny use cases, bude probíhat iterace high fidelity designu. Aplikace bude využívána na mobilních a desktop zařízeních. Design tedy bude navržen přístupem mobile first a následně upraven i pro desktop zařízení. Prototyp bude reflektovat budoucí využití technologie Flutter pro vývoj aplikace. Součástí návrhu prototypu bude pak následně i návrh architektury aplikace.

Testování prototypu bude ve většině případů probíhat online a bude sloužit pro sběr zpětné vazby a nápadů pro další iterace prototypu pomocí metodiky user testing. Pro účely testování budou připraveny scénáře, kterými budou uživatelé procházet. Cílem testů bude nejen sledovat, nakolik intuitivní je vytvořený design aplikace, ale zároveň se průběžně ujistit, že v daných scénářích nechybí žádný use case. Závěrečný test proběhne osobně s následným dotazníkovým šetřením pro získání závěrečné zpětné vazby.

## Omezení diplomové práce

Požadavky laboratoře v době přípravy projektu DP stále nejsou kompletní a budou se blíže specifikovat v průběhu implementace prototypu. Komunikace s laboratoří byla kvůli zahlcení pracovníků administrativou ke konci roku slabší. Riziko neefektivní komunikace při sběru zpětné vazby by se mělo co nejvíce omezit nastavením efektivních komunikačních kanálů a schůzek.

Materiály pro rozpoznávání buněk ze snímků mikroskopu jsou omezené, a přestože existují modely, které lze pro tyto účely využít, nelze dopředu říci, nakolik budou úspěšné při rozpoznávání reprodukčních buněk kapradin a plavuní. Přestože prototyp může být úspěšný, nelze zaručit, že jeho následná implementace bude úspěšná, či mu bude plně odpovídat.

## Význam a přínos diplomové práce

Výsledkem práce je prototyp aplikace, která nejen usnadní zaznamenávání výskytu rostlin na území České republiky, ale zároveň se může díky rozpoznávání reprodukčních buněk rostlin stát základem pro automatizaci mikrobiologického výzkumu jako takového.

Prototyp umožní identifikovat slabá místa a přijít na nové funkční požadavky ještě před samotným vývojem a dá pracovníkům představu o budoucím směřování vývoje aplikace.

Jedním z výsledků práce je podchycení a zefektivnění procesů vědeckých pracovníků laboratoře molekulární biologie rostlin na Přírodovědecké fakultě Jihočeské univerzity. Součástí práce tedy bude i závěrečný průzkum nakolik má budoucí aplikace potenciál usnadnit pracovníkům zpracovávání úkolů a běh laboratoře.

V případě úspěchu bude mít aplikace potenciál být implementována i dalšími mikrobiologickými laboratořemi a rozšířena o další funkce, včetně rozpoznávání nových typů buněk, ať již rostlinných či jiných.

## Zdroje

NEW YORK BOTANICAL GARDEN. Index Herbariorum - The William & Lynda Steere Herbarium, 2023. [online] Dostupné z: https://sweetgum.nybg.org/science/ih/.

KATEDRA BOTANIKY PŘF JU. Systematika cévnatých rostlin na Katedře botaniky BF JU, 2023. [online] Dostupné z: https://botanika.prf.jcu.cz/systematics/herbar.html/.

KATEDRA BOTANIKY PŘF JU. Systematika vyšších rostlin – Výzkum, 2023. [online] Dostupné z: https://botanika.prf.jcu.cz/systematics/vyzkum/.

MAGDALENA, Ulises Rodrigo et al. A new methodology for the retrieval and evaluation of geographic coordinates within databases of scientific plant collections. Applied Geography (Sevenoaks). 2018, vol. 96, p. 11-15. ISSN 0143-6228.

KISLOV, Dmitry E. et al. An electronic management system for a digital herbarium: Development and future prospects. Botanica Pacifica: Journal of Plant Science and Conservation. 2017, vol. 6, no. 2, p. 59-68. ISSN 2226-4701.

Design Thinking, 2008. Harvard Business Review [online]. 2008 [cited 2020-11-08]. Dostupné z: https://hbr.org/2008/06/design-thinking.

BROWN, Tim, Clayton M. CHRISTENSEN, Indra NOOYI, and Vijay GOVINDARAJAN. HBR’s 10 Must Reads on Design Thinking. B.m.: Harvard Business Review Press, 2020.

ESTHER, Han. What Is Design Thinking & Why Is It Important? | HBS Online. Business Insights Blog [online]. 18. leden 2022 [vid. 2024-01-10]. Dostupné z: https://online.hbs.edu/blog/post/what-is-design-thinking.

BENEDIKT, Jiří. Design thinking proces – Rychlé shrnutí [online]. [vid. 2024-01-10]. Dostupné z: https://www.jiribenedikt.com/materialy/design-thinking/proces/.

TEAMAZING, Design Thinking: How it works [Theory, Practice & Examples] [online]. [vid. 2024-01-10]. Dostupné z: https://www.teamazing.com/design-thinking/.

BROWN, Tim. Change by Design, Revised and Updated: How Design Thinking Transforms Organizations and Inspires Innovation. Revised, Updated ed. edition. B.m.: Harper Business, 2019.

TONHAUSER, Pauline. Design Thinking Workshop: The 12 Indispensable Elements for a Design Thinking Workshop [online] 2016 [vid. 2024-01-10]. Dostupné z: https://www.amazon.com/dp/B01BHKI148?ref=yb_qv_ov_kndl_dp_rw
