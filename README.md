# MedborgarAI – Din guide genom kommunal byråkrati
Building AI course project

🇸🇪 Svenska nedan | 🇬🇧 English below

## Summary
MedborgarAI är ett AI-drivet verktyg som hjälper svenska medborgare att förstå, skriva och skicka in kommunala ärenden, klagomål och ansökningar på korrekt svenska. Verktyget riktar sig särskilt till personer med begränsade kunskaper i svenska byråkratiskt språk – till exempel nyanlända, äldre eller personer med lässvårigheter.

## Background
Vilket problem löser MedborgarAI?

Kommunal byråkrati är svår att navigera för många. Formulär är komplicerade, juridiskt språk är svårtolkat och konsekvenserna av att fylla i något fel kan vara stora – man kan förlora rätten till bidrag, missa en ansökningsfrist eller inte få sin röst hörd i ett planärende.

Problem 1: Kommunala formulär och beslut är skrivna på formell svenska som är svår att förstå för många medborgare.
Problem 2: Det finns idag inga öppna AI-verktyg som är anpassade för nordisk/svensk kommunal kontext.
Problem 3: Rådgivningstjänster (t.ex. kommunens kontaktcenter) har långa väntetider och begränsade öppettider.
Personlig motivation: Sverige har 40 000+ invånare som tagit kursen Elements of AI, men AI-verktyg anpassade för det svenska samhällets unika struktur saknas nästan helt. Kommuner digitaliserar allt mer – men utan AI-stöd för medborgarna riskerar vi att öka klyftorna snarare än minska dem.

Varför är detta viktigt? Rättvis tillgång till samhällsinformation är en demokratifråga. AI kan vara en utjämnande kraft – men bara om det finns tillgängliga verktyg på rätt språk och i rätt kontext.

## How is it used?
Flödet ser ut så här:

Medborgaren besöker MedborgarAI via webben (mobil eller dator)
Hen beskriver sitt ärende i klartext: "Jag vill klaga på att min granne byggt ett plank som skymmer min utsikt"
AI:n identifierar ärendetyp (bygglov, grannelagsrätt, etc.) och ber om kompletterande information
Verktyget genererar ett korrekt formulerat brev/ärende på formell svenska, redo att skickas till kommunen
Medborgaren granskar, justerar och laddar ned dokumentet

## Vem använder det?
Nyanlända med begränsade kunskaper i formell svenska
Äldre medborgare ovana vid digitala formulär
Allmänheten i kontakt med kommunen kring bygglov, socialtjänst, skola, miljö m.m.
Viktiga perspektiv att beakta:

Tillgänglighet: gränssnittet måste fungera på enkel svenska och vara skärmläsarvänligt
Integritet: känsliga uppgifter (personnummer, adress) ska hanteras varsamt
Kommunernas perspektiv: verktyget bör minska, inte öka, felaktiga ärenden
Illustration av en medborgare som interagerar med en AI-assistent

## Data sources and AI methods
Komponent	Beskrivning
Språkmodell	GPT-SW3 (AI Sweden) eller Llama 3 Scandinavian (AI Sweden/HuggingFace)
Träningsdata	Offentliga kommunala dokument, SKR:s mallar och riktlinjer
Formulärdata	Öppna data från Digg (myndigheten för digital förvaltning)
Klassificering	Naiv Bayesiansk klassificering för att identifiera ärendetyp utifrån fri text
Textgenerering	Fine-tunad LLM på svenska kommunala ärenden

## Tillgång till data:
SKR – Sveriges Kommuner och Regioner publicerar mallar och riktlinjer öppet
Digg – öppna data tillhandahåller offentlig förvaltningsdata
Kommuners offentliga handlingar är tillgängliga via offentlighetsprincipen
AI-tekniker:

## Klassificering av ärendetyp (nearest neighbor eller naiv Bayes)
Textgenerering med instruktionsfinjusterad LLM
RAG (Retrieval-Augmented Generation) för att hämta aktuella regler och mallar
Challenges
Vad löser MedborgarAI INTE?

Verktyget ger inte juridisk rådgivning – det hjälper att formulera ärenden, inte att avgöra om man har rätt i sak
AI:n kan göra fel – medborgaren måste alltid granska det genererade dokumentet
Systemet täcker inte alla kommuners specifika rutiner – Sverige har 290 kommuner med delvis olika processer
Verktyget hjälper inte vid muntliga möten eller telefonkontakt med kommunen

## Etiska överväganden:
Risk för att medborgare litar för mycket på AI-genererade ärenden utan att förstå innehållet
Algoritmbias: om träningsdata speglar historiska ojämlikheter kan verktyget missgynna vissa grupper
Tillgänglighet för dem utan internet eller dator är fortfarande en utmaning

## What next?
Pilotkommun: Samarbeta med en svensk kommun för att testa verktyget i verkligheten
Fler ärendetyper: Börja med bygglov och grannelagsärenden, expandera till socialtjänst, skola och miljö
Flerspråkigt stöd: Lägga till stöd för de vanligaste invandrarspråken i Sverige (arabiska, somaliska, dari)
Integration med e-tjänster: Koppla mot kommunernas egna e-tjänsteplattformar
Kompetenser som behövs: Juridisk expertis inom förvaltningsrätt, UX-design för tillgänglighet, samarbete med SKR

## Acknowledgments
Inspiration från Elements of AI
Språkmodell: GPT-SW3 av AI Sweden / Apache 2.0-licens
Scandinavian Llama 3: AI Sweden på HuggingFace / Meta Llama 3 Community License
Öppna data: Digg och SKR
Illustrationsbild: A woman using a computer / CC BY-SA 3.0
Tack till NNAI för inspiration kring nordisk AI-infrastruktur
<a name="english"></a>

# MedborgarAI – Your Guide Through Municipal Bureaucracy
Building AI course project

🇬🇧 English | 🇸🇪 Svenska ovan

## Summary
MedborgarAI is an AI-powered tool that helps Swedish citizens understand, draft, and submit municipal cases, complaints, and applications in correct formal Swedish. It is especially aimed at people with limited knowledge of formal bureaucratic Swedish — such as newly arrived immigrants, elderly people, or those with reading difficulties.

## Background
What problem does MedborgarAI solve?

Municipal bureaucracy is difficult to navigate for many people. Forms are complex, legal language is hard to interpret, and the consequences of making a mistake can be significant — you may lose access to benefits, miss an application deadline, or fail to have your voice heard in a planning matter.

Problem 1: Municipal forms and decisions are written in formal Swedish that many citizens find hard to understand.
Problem 2: There are currently no open AI tools adapted to the Nordic/Swedish municipal context.
Problem 3: Advisory services (e.g. municipal contact centers) have long waiting times and limited opening hours.
Personal motivation: Sweden has 40,000+ residents who have completed the Elements of AI course, yet AI tools adapted to the unique structure of Swedish society are almost entirely absent. Municipalities are increasingly going digital — but without AI support for citizens, we risk widening rather than closing the gap.

Why does this matter? Fair access to civic information is a democratic issue. AI can be a leveling force — but only if tools exist in the right language and the right context.

## How is it used?
The flow looks like this:
The citizen visits MedborgarAI via web (mobile or desktop)
They describe their case in plain language: "I want to complain that my neighbour has built a fence that blocks my view"
The AI identifies the case type (building permit, neighbour law, etc.) and asks for additional information
The tool generates a correctly worded letter/case in formal Swedish, ready to be submitted to the municipality
The citizen reviews, adjusts, and downloads the document

## Who uses it?
Newly arrived immigrants with limited knowledge of formal Swedish
Elderly citizens unfamiliar with digital forms
The general public dealing with the municipality on topics like building permits, social services, schools, and the environment
Important perspectives to consider:

Accessibility: the interface must work in plain Swedish and be screen-reader friendly
Privacy: sensitive data (personal ID numbers, addresses) must be handled carefully
The municipality's perspective: the tool should reduce, not increase, incorrectly filed cases
Illustration of a citizen interacting with an AI assistant

## Data sources and AI methods
Component	Description
Language model	GPT-SW3 (AI Sweden) or Llama 3 Scandinavian (AI Sweden/HuggingFace)
Training data	Public municipal documents, SKR templates and guidelines
Form data	Open data from Digg (Swedish Agency for Digital Government)
Classification	Naive Bayes classifier to identify case type from free text
Text generation	Fine-tuned LLM on Swedish municipal cases

## Data access:
SKR – Swedish Association of Local Authorities and Regions publishes templates and guidelines openly
Digg – open data provides public administration data
Municipal public records are accessible under Sweden's principle of public access (offentlighetsprincipen)
AI techniques:

Case type classification (nearest neighbor or naive Bayes)
Text generation with an instruction-tuned LLM
RAG (Retrieval-Augmented Generation) to fetch current rules and templates

## Challenges
What does MedborgarAI NOT solve?
The tool does not provide legal advice — it helps formulate cases, not determine whether you are legally in the right
The AI can make mistakes — the citizen must always review the generated document
The system does not cover all municipalities' specific procedures — Sweden has 290 municipalities with partly different processes
The tool does not help with verbal meetings or phone contact with the municipality

## Ethical considerations:
Risk that citizens place too much trust in AI-generated documents without understanding the content
Algorithmic bias: if training data reflects historical inequalities, the tool may disadvantage certain groups
Accessibility for those without internet access or a computer remains a challenge

## What next?
Pilot municipality: Partner with a Swedish municipality to test the tool in a real-world setting
More case types: Start with building permits and neighbour disputes, expand to social services, schools, and environment
Multilingual support: Add support for the most common immigrant languages in Sweden (Arabic, Somali, Dari)
E-service integration: Connect to municipalities' own digital service platforms
Skills needed: Legal expertise in administrative law, accessibility-focused UX design, collaboration with SKR

## Acknowledgments
Inspired by Elements of AI
Language model: GPT-SW3 by AI Sweden / Apache 2.0 license
Scandinavian Llama 3: AI Sweden on HuggingFace / Meta Llama 3 Community License
Open data: Digg and SKR
Image: A woman using a computer / CC BY-SA 3.0
Thanks to NNAI for inspiration on Nordic AI infrastructure
