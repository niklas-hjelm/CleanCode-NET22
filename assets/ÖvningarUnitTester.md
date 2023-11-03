## Övningar utan ramverk

### 1. Enkel strängmanipulation

- **Uppgift:** Implementera en metod `InvertString` som tar en sträng som input och returnerar dess inverterade version.
- **Tester:** Testa denna metod i `Main`-metod där du manuellt testar metoden med minst tre olika strängar och skriver ut resultatet samt förväntat resultat.

### 2. Calculator-funktioner

- **Uppgift:** Skapa en `Calculator`-klass med metoder för att utföra addition, subtraktion, multiplikation och division.
- **Tester:** Testa denna metod i `Main`-metod som testar varje räkneoperation med olika talpar och validerar resultatet mot förväntade värden.

### 3. Sorteringsalgoritm

- **Uppgift:** Implementera en metod `SortArray` som sorterar en array av heltal i stigande ordning.
- **Tester:** Testa denna metod i `Main`-metod där du testar sorteringsmetoden med olika datamängder och jämför den sorterade arrayen med en förväntad resultatarray.

### 4. Palindrom-checker

- **Uppgift:** Skriv en metod `IsPalindrome` som avgör om en given sträng är ett palindrom.
- **Tester:** Testa denna metod i `Main` med en uppsättning strängar som inkluderar kända palindromer och icke-palindromer för att validera metoden.

### 5. Temperaturomvandling

- **Uppgift:** Utveckla en `TemperatureConverter`-klass med metoder för att konvertera temperatur mellan Celsius och Fahrenheit.
- **Tester:** Testa denna metod i `Main` för att testa dina konverteringsmetoder med flera temperaturvärden och kontrollera att de matchar de förväntade värdena.

## Övningar med xUnit

### 6. String Joiner

- **Uppgift:** Skriv en metod `JoinStrings` som sammanfogar en array av strängar med ett specifikt avskiljtecken.
- **Tester:** Använd xUnit för att skapa tester som verifierar att metoden korrekt hanterar olika scenarier, inklusive tomma arrays och null-värden.

### 7. Användarvalidering

- **Uppgift:** Implementera en `UserValidator`-klass med metoder för att validera e-postadresser och lösenord.
- **Tester:** Använd xUnit för att skriva tester som täcker olika felaktiga och korrekta format på e-postadresser och lösenord.

### 8. Dagbokfunktionalitet

- **Uppgift:** Skapa en `Diary`-klass som låter användare lägga till och ta bort anteckningar.
- **Tester:** Använd xUnit för att testa att anteckningar kan läggas till, visas och tas bort korrekt.

### 9. API-responsparser

- **Uppgift:** Implementera en parser som konverterar JSON-svar från ett API till objekt.
- **Tester:** Skriv xUnit-tester som simulerar API-svar i olika format för att se till att parsningen hanterar dessa korrekt.

### 10. Lagerhanteringssystem

- **Uppgift:** Skapa en grundläggande `InventoryManager`-klass för att hantera lager av produkter.
- **Tester:** Använd xUnit för att testa att produkter kan läggas till, uppdateras och tas bort från lagret.

## Övningar med FakeItEasy

### 11. E-posttjänst Mocking

- **Uppgift:** Anta att du har en `EmailService` som skickar e-postmeddelanden. Använd FakeItEasy för att skapa en mock av denna tjänst.
- **Tester:** Skriv tester som verifierar att ett e-postmeddelande "skickas" (dvs. metoden `SendEmail` anropas) när det är tänkt att skickas.

### 12. Databas-repository Faking

- **Uppgift:** Skapa en `UserRepository`-klass. Använd FakeItEasy för att fejka databas-interaktioner.
- **Tester:** Testa `UserRepository` för att säkerställa att CRUD-operationer utförs som förväntat genom att använda en fake databas.

### 13. Autentiseringstjänst Mocking

- **Uppgift:** Mocka en `AuthenticationService` som har en metod `Authenticate` som tar emot användarnamn och lösenord och returnerar en autentiseringsstatus.
- **Tester:** Använd FakeItEasy för att verifiera att rätt metoder anropas när en användare försöker logga in.

### 14. Integrationstest med Fake Services

- **Uppgift:** Anta att du har en applikation som använder externa tjänster för betalningar. Skapa integrationstester som mockar dessa tjänster.
- **Tester:** Använd FakeItEasy för att imitera dessa tjänster och verifiera att applikationen hanterar interaktionen korrekt.

### 15. Konfigurationshanterare Mocking

- **Uppgift:** Mocka en `ConfigurationManager`-klass som läser konfigurationsinställningar. Metoderna kan inkludera `GetSetting(string key)` och `SetSetting(string key, string value)`.
- **Tester:** Använd FakeItEasy för att säkerställa att applikationen hämtar och använder rätt konfigurationsvärden.

## Övningar med FakeItEasy och Dummy Data

### 16. Testning med Dummy-användare

- **Uppgift:** Skapa dummy-användare för att testa `UserService`-klassen. Metoderna kan inkludera `CreateUser`, `DeleteUser`, och `FindUserById`.
- **Tester:** Använd FakeItEasy för att generera testanvändardata och verifiera att `UserService` behandlar användarna korrekt.

### 17. Produktkatalog med Dummy-produkter

- **Uppgift:** Generera en lista med dummy-produkter för att testa funktioner i en `ProductService`-klass.
- **Tester:** Använd FakeItEasy för att skapa testprodukter och verifiera att `ProductService` utför korrekta operationer med produkterna.

### 18. Orderbehandling med Dummy-orders

- **Uppgift:** Skapa dummy-orderdata för att testa en `OrderProcessingService`. Metoderna kan inkludera `PlaceOrder`, `CancelOrder`, och `GetOrderDetails`.
- **Tester:** Använd FakeItEasy för att generera ordertestdata och verifiera att ordern bearbetas som förväntat.

### 19. Event-logger med Dummy-events

- **Uppgift:** Implementera en `EventLogger`-klass som har metoder såsom `LogEvent` som loggar information om händelser.
- **Tester:** Använd FakeItEasy för att generera dummy-event och verifiera att `EventLogger` loggar dessa händelser korrekt.

### 20. Kundtjänstscenario med Dummy-interaktioner

- **Uppgift:** Simulera en kundtjänstapplikation där kundinteraktioner hanteras. Metoderna kan innefatta `ReceiveCustomerInquiry` och `RespondToInquiry`.
- **Tester:** Använd FakeItEasy för att skapa dummy-kundinteraktioner och testa att applikationen svarar och hanterar dessa på ett korrekt sätt.

## Interface för övningsuppgifterna 11-20

```csharp
// Uppgift 11
public interface IEmailService
{
    void SendEmail(string toAddress, string subject, string body);
}

// Uppgift 12
public interface IUserRepository
{
    void AddUser(User user);
    void UpdateUser(User user);
    User GetUserById(int id);
    void DeleteUser(int id);
}

// Uppgift 13
public interface IAuthenticationService
{
    bool Authenticate(string username, string password);
}

// Uppgift 14 (inget nytt interface behövs om det redan finns t.ex. IEmailService som ovan)

// Uppgift 15
public interface IConfigurationManager
{
    string GetSetting(string key);
    void SetSetting(string key, string value);
}

// Uppgift 16
public interface IUserService
{
    void CreateUser(User user);
    User FindUserById(int id);
    void DeleteUser(int id);
}

// Uppgift 17
public interface IProductService
{
    IEnumerable<Product> GetAllProducts();
    Product GetProductById(int id);
    void AddProduct(Product product);
    void UpdateProduct(Product product);
    void DeleteProduct(int id);
}

// Uppgift 18
public interface IOrderProcessingService
{
    Order PlaceOrder(OrderDetails orderDetails);
    bool CancelOrder(int orderId);
    Order GetOrderDetails(int orderId);
}

// Uppgift 19
public interface IEventLogger
{
    void LogEvent(string message);
}

// Uppgift 20
public interface ICustomerService
{
    InquiryResponse ReceiveCustomerInquiry(CustomerInquiry inquiry);
    void RespondToInquiry(InquiryResponse response);
}

```
