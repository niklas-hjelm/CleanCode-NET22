# Docker Övningar för .NET-utvecklare

Dessa övningar är utformade för att ge .NET-utvecklare praktisk erfarenhet av att använda Docker och Docker Compose, med ett fokus på applikationer som interagerar med databaser.

## Övning 1: Skapa en Dockerfile för en enkel .NET applikation

### Mål

Förstå grunderna i en Dockerfile och hur man containeriserar en .NET applikation.

### Uppgift

Skapa en Dockerfile för en enkel "Hello World" .NET konsolapplikation.

### Steg

1. Skapa en ny .NET konsolapplikation med `dotnet new console`.
2. Skriv en Dockerfile som använder Microsofts officiella .NET image som bas.
3. Definiera arbetsmappen i containern.
4. Kopiera projektets filer till containern.
5. Använd `dotnet restore` och `dotnet build` för att bygga applikationen.
6. Ange kommandot som ska köras när containern startar.

### Förväntat Resultat

- Dockerfilen ska vara korrekt formulerad utan syntaxfel.
- Containern ska kunna byggas och köras utan fel.
- När containern körs ska den visa "Hello World" i terminalen.

## Övning 2: Skapa en multi-stage build Dockerfile

### Mål

Lär dig att optimera en Docker image med multi-stage builds för att minska storleken och förbättra säkerheten.

### Uppgift

Modifiera Dockerfile från Övning 1 för att använda multi-stage builds.

### Steg

1. Definiera en bygg-stage som använder `sdk`-bilden för att bygga applikationen.
2. Definiera en runtime-stage som använder `aspnet`-bilden för att köra applikationen.
3. Kopiera det byggda programmet från bygg-stagen till runtime-stagen.

### Förväntat Resultat

- Den slutliga image storleken bör vara minskad jämfört med en icke multi-stage build.
- Containern ska kunna köras och fungera som avsett.

## Övning 3: Hantera persistent data med Docker Volumes

### Mål

Förstå hur man hanterar data som ska bevaras mellan container omstarter.

### Uppgift

Modifiera en .NET applikation så att den skriver ut loggar till en fil och konfigurera Docker för att använda en volume för att bevara loggfilerna.

### Steg

1. Uppdatera .NET-applikationen för att logga till en fil.
2. Skapa en Dockerfile som bygger applikationen och konfigurerar en volume.
3. Kör containern med volymen monterad för att bevara loggdata.

### Förväntat Resultat

- Loggfilerna ska finnas kvar även efter att containern har stoppats och startats om.
- Eleverna ska kunna visa var och hur datan bevaras på värdsystemet.

## Övning 4: Networking och kommunikation mellan containers

### Mål

Förstå hur containers kommunicerar med varandra via Docker nätverk.

### Uppgift

Skapa två containers som kan kommunicera med varandra, den ena kör en .NET Web API och den andra en frontend-applikation.

### Steg

1. Skapa en enkel .NET Web API som svarar på HTTP-förfrågningar.
2. Skapa en Dockerfile för Web API-projektet.
3. Kör API-containern i ett Docker-nätverk.
4. Skapa och kör en annan container i samma nätverk som kan nå API:t.

### Förväntat Resultat

- API-containern ska kunna ta emot förfrågningar från frontend-containern.
- Kommunikationen mellan containers ska ske via ett Docker-nätverk.

## Övning 5: Använda Docker Compose för att orkestrera containers

### Mål

Förstå hur Docker Compose används för att definiera och köra multi-container Docker applikationer.

### Uppgift

Skapa en `docker-compose.yml` fil för att orkestrera en .NET applikation och en databas.

### Steg

1. Definiera en tjänst för .NET-applikationen med en beroende Dockerfile.
2. Lägg till en tjänst för en SQL-databas i samma `docker-compose.yml`.
3. Konfigurera nätverksinställningar så att .NET-applikationen kan kommunicera med databasen.
4. Använd Docker Compose för att starta hela stacken.

### Förväntat Resultat

- `docker-compose up` kommandot ska starta både applikationen och databasen utan fel.
- Applikationen ska kunna ansluta till och interagera med databasen.

## Övning 6: Hantering av persistenta databaser med Docker Compose

### Mål

Förstå hur man använder Docker Volumes med Docker Compose för att hantera persistent data för databaser.

### Uppgift

Utöka `docker-compose.yml` från Övning 5 för att inkludera persistent volymer för databasen.

### Steg

1. Lägg till en volym-konfiguration i `docker-compose.yml` för databas-tjänsten.
2. Konfigurera databas-tjänsten att använda volymen för att lagra databasfiler.
3. Starta tjänsterna med Docker Compose och verifiera att data bevaras över omstarter.

### Förväntat Resultat

- Databasdata ska vara persistent över container omstarter.
- Volymen med databasdata ska vara tillgänglig och korrekt kopplad till databas-tjänsten.
