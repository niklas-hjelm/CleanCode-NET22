# Labb 2 - Micro services och Test

Ett sätt att bygga upp funktionalitet åt en större organisation eller företag är att tillämpa
arkitekturmönstret mikrotjänster, vilket både löser en hel del problem men samtidigt introducerar
nya svårigheter.

Denna labben går ut på att utveckla två stycken ``microservices`` och en ``API-Gateway`` som tillsammans utgör en webbtjänst. **Varje** medlem i gruppen ansvarar för var sin ``microservice``.

Vi vill kunna lägga till samt läsa information
från tjänsterna vilket gör att dessa behöver supporta minst **GET** och **POST**. Men vill man kan man
även implementera **PUT** och **DELETE**.

### [Implement API Gateways with Ocelot](https://learn.microsoft.com/en-us/dotnet/architecture/microservices/multi-container-microservice-net-applications/implement-api-gateways-with-ocelot)
## Genomförs i grupp er om 3 personer

## Labben består av 3 delar 

## Del 1:

Ni ska tillsammans i gruppen enas om en webbtjänst som ska byggas. 
Ni ska också tillsammans skriva API-specifikationer för samtliga ``microservices`` och ``gateway``. Bestämma vilken typ av databas som ska användas och vem som ansvarar för vilken del. Sätt sedan upp repo och projekten med alla relevanta ``Interface`` och ``databasmodeller``.

### Förslag på projekt:

En tjänst lagrar pizzor med deras namn, ingredienser
och pris medans en annan fristående tjänst lagrar beställningar på pizzor.

En tjänst som lagrar information om användare så som namn, adress,
länk till profilbild m.m. och en annan tjänst som lagrar meddelanden med en rubrik, text, datum samt id för vilken användare som postat meddelandet.

## Del 2: Microservices och API-Gateway

Implementera microservices och API Gateway. Varje medlem i gruppen ska ansvara för en microservice.
Upprepa 2.0 Tills ni är klara.

## Del 3: Reflektioner och Analys

När man är färdig med sin ``microservice`` ska alla skriva en kortfattad analys av arbetet. Här ska man analysera sitt eget arbete. Svara på dessa frågor men utöka gärna om det behövs.
* Vad har du lärt dig om ``microservices``?
* Vad hade du gjort annorlunda om du fick uppgiften igen?

## VG-Uppgifter

### Alternativ 1: Authentisering

För att använda alla endpoints utom GET frågor så vill vi veta identiteten på den som anropar våra
tjänster. Lägg till funktionalitet för att hantera JWT i api gateway och även skicka vidare den
informationen till bakomliggande tjänster.

#### [Make secure .NET Microservices and Web Applications](https://learn.microsoft.com/en-us/dotnet/architecture/microservices/secure-net-microservices-web-applications/)

### Alternativ 2: Message Queue

Implementera en message queue för att hantera kommunikation mellan tjänsterna. Detta kan göras med hjälp av RabbitMQ eller liknande.

#### [RabbitMQ](https://www.rabbitmq.com/tutorials/tutorial-one-dotnet.html)

## Redovisning

Ni ska lämna in det som behövs för att köra projektet med eventuella anvisningar. Ett tips kan vara att jobba i ett github-projekt och bjuda in mig i det.

## Bedömning

### Krav för G

* Ni har en(eller flera) API-spec för alla delar
* Frågorna i steg 3 är besvarade tydligt och med självreflektion
* Det ska gå att utföra minst **Get** och **Post** requests på alla microservices.
* Ni har utvecklat projektet på ett sätt som är löst kopplat
  
### Krav för VG

* En eller flera extra uppgifter för VG är genomförd
* Man har tillämpat SOLID i utvecklingen

## Deadline är 30/12-2023 kl 23:59
Sen inlämning innebär komplettrering i Februari.
