**Lekcja: Konfiguracja adresu IP w Ubuntu za pomocą mc**

---

**Cel lekcji:**

Nauczysz się, jak skonfigurować adres IP w systemie Ubuntu, używając menadżera plików **mc** (Midnight Commander) w terminalu. Pokażemy Ci również, jak skopiować przykładowy plik konfiguracyjny i dostosować go do swoich potrzeb.

---

### **Krok 1: Uruchomienie terminala**

- Znajdź na swoim pulpicie ikonę **Terminal**.
- Kliknij na nią, aby otworzyć okno terminala.
- **Lub** naciśnij jednocześnie klawisze **Ctrl + Alt + T**.

### **Krok 2: Instalacja mc (jeśli nie jest zainstalowany)**

- Wpisz w terminalu komendę:

  ```
  sudo apt-get install mc
  ```

- Naciśnij **Enter**.
- Jeśli pojawi się prośba o hasło, wpisz swoje hasło i naciśnij **Enter**.
- Poczekaj, aż instalacja się zakończy.

### **Krok 3: Uruchomienie mc**

- W terminalu wpisz:

  ```
  mc
  ```

- Naciśnij **Enter**.
- Otworzy się program **mc** z dwoma panelami.

### **Krok 4: Przejście do katalogu konfiguracyjnego**

- Używając strzałek na klawiaturze, przejdź do katalogu **/etc/netplan**.
- Jeśli nie widzisz tego katalogu, najpierw przejdź do głównego katalogu **/**.
  - Wybierz katalog **".."** (dwie kropki) i naciśnij **Enter** aż dojdziesz do **/**.
  - Znajdź i wybierz katalog **etc**.
  - Następnie wybierz **netplan**.

### **Krok 5: Skopiowanie przykładowego pliku konfiguracyjnego**

- W drugim panelu przejdź do katalogu z przykładami:
  - Naciśnij klawisz **Tab**, aby przełączyć się do drugiego panelu.
  - Przejdź do **/usr/share/doc/netplan/examples**.
- Znajdź plik o nazwie **static.yaml**.
- Zaznacz go i naciśnij klawisz **F5** (kopiuj).
- Upewnij się, że kopia trafi do katalogu **/etc/netplan** (pierwszy panel).
- Naciśnij **Enter**, aby potwierdzić kopiowanie.

### **Krok 6: Edycja pliku konfiguracyjnego**

- W pierwszym panelu (powinien być w **/etc/netplan**) znajdź plik **static.yaml**.
- Zaznacz go i naciśnij klawisz **F4** (edytuj).

### **Krok 7: Dostosowanie pliku do swoich potrzeb**

- W edytorze zobaczysz zawartość pliku.
- Znajdź linijkę z **addresses**.
- Zmień adres IP na swój własny.

  Przykład:

  ```yaml
  addresses: [192.168.1.100/24]
  ```

- Upewnij się, że podajesz poprawny adres bramy (**gateway4**) i serwery DNS.

### **Krok 8: Zapisanie zmian**

- Po wprowadzeniu zmian naciśnij klawisz **F2** (zapisz).
- Naciśnij klawisz **F10** (wyjdź z edytora).

### **Krok 9: Zastosowanie nowej konfiguracji**

- Wyjdź z programu **mc**, naciskając **F10**.
- W terminalu wpisz:

  ```
  sudo netplan apply
  ```

- Naciśnij **Enter**.

### **Krok 10: Sprawdzenie ustawień sieci**

- W terminalu wpisz:

  ```
  ip addr show
  ```

- Naciśnij **Enter**.
- Sprawdź, czy adres IP został zmieniony na ten, który ustawiłeś.

---

**Gratulacje!** Właśnie skonfigurowałeś adres IP w swoim systemie Ubuntu.

---

**Porady:**

- **Czytaj powoli** i upewnij się, że rozumiesz każdy krok.
- Jeśli masz problem, **poproś o pomoc** nauczyciela lub kolegę.
- **Nie spiesz się**. Ważne jest, aby zrozumieć, co robisz.
- **Zapisz sobie** ważne komendy, aby łatwiej było je zapamiętać.

---

**Pamiętaj:** Ćwiczenie czyni mistrza! Im więcej będziesz praktykować, tym łatwiej będzie Ci wykonywać te czynności w przyszłości.
