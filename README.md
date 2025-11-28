# Kółko i krzyżyk (klient - serwer)

### Struktura plików
```
tic-tac-toe/
│
├── server/
|   ├── Main.java
|   ├── controller/
│   │   ├── GameServer.java      
│   │   ├── GameController.java  
│   │
│   ├── model/
│   │   ├── GameEngine.java      
│   │   ├── GameRoom.java         
│   │   ├── PlayerStats.java      
│   │
│   ├── view/
│       ├── ServerLogger.java    
│
├── client/
│   ├── Main.java
│   ├── controller/
│   │   ├── ClientController.java  
│   │
│   ├── model/
│   │   ├── Client.java           
│   │
│   ├── view/
│   │   ├── UI.java               
│
├── shared/
│   ├── GameServerInterface.java 
│   ├── ClientInterface.java  
│   ├── enumy
```



## Treść programowa:
1. Rozpraszanie obliczeń poprzez wykorzystanie gniazd TCP/IP.
2. Rozpraszanie obliczeń poprzez zdalne wywoływanie procedur. (RMI)
## Funkcjonalności
1. **Hybrydowa komunikacja sieciowa** - użycie zarówno komunikacji poprzez RMI jak i gniazd TCP/IP.
2. **Mechanika gry** - implementacja silnika zarządzającego mechaniką gry w kółko i krzyżyk
- Wykorzystany mechanizm RMI w celu nawiązania połączenia między dwoma graczami oraz obsługę mechaniki gry.
- Mechanika gry zaimplementowana w aplikacji serwera.
- Serwer obsługuje więcej niż jednego gracza w tym samym momencie poprzez realizację gier w dedykowanych pokojach.
- Serwer oblicza statystyki graczy w danej sesji - ilość wygranych, remisów oraz porażek.
- Aplikacja serwera loguje w konsoli kluczowe dane.
- chat pomiędzy użytkownikami z TCP/IP.
- Gniazda otworzone pomiędzy grającymi użytkownikami.
- Serwer udostępnia informację o adresach IP użytkowników.

![image](https://github.com/user-attachments/assets/e624110e-2d44-481f-a49f-e2ecf4c448df)

## Wymagania
1. Minimum dwie aplikacje (serwer, klient, obserwator*)
2. Zaimplementowane zasady gry, statystyki
3. Komunikacja z wykorzystaniem protokołu RMI
4. Obsługa N klientów (skalowalność)
5. Obsługa mechaniki pokojów (gracze nie są parowami losowego)
6. Implementacja funkcjonalności chatu pomiędzy dwoma graczami z wykorzystaniem mechanizmu gniazd TCP/IP.


### Uruchamianie
#### Serwer
```bash
java -jar server.jar <port>
```
![Logowanie historii działań klientów](https://github.com/user-attachments/assets/350f3bf6-bddc-4fff-a8db-49d1fa5a6a86)

#### Klient
```bash
java -jar client.jar <server_port> <username>
```
### Dostępne polecenia
![Polecenia](https://github.com/user-attachments/assets/5a196179-ec54-43df-a8d8-631cd9c1cebe)

### Widok z rozgrywki z czatem
![Widok z rozgrywki z czatem](https://github.com/user-attachments/assets/71351515-fcaf-4429-998d-41d9d6904d2c)










