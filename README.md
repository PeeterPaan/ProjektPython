# ProjektPython

##Opis ogólny 

  >Program ma za zadanie przekonwertowanie zeskanowanego tekstu na OCR, a następnie odczytanie z niego określonych argumentów.
  Argumenty następnie powinny być zapisywane do pliku txt, lub csv, a później z tego pliku wprowadzane do interfejsu programu   księgowego. 

##Wymagania sprzętowe
  
 >Komputer, skaner, połączenie między 1, a 2. 
  
##Założenia
  
  >Zakładam, że biblioteka Ocropus poradzi sobie ze zczytywaniem danych z faktur pisanych różną czcionką, w różnych językach. 
  
##Funkcje 
  
  >Osoba korzystająca z programu będzie mogła sobie wybrać jakiego rodzaju danych szuka. Będzie możliwość wybrania np kwoty     neto, kwoty brutto, stawki podatku określonych pozycji na fakturze, nazwa Sprzedawcy, nazwa Kontrahenta, numery NIP. W       przypadku niektórych faktur potrzebne jest więcej, lub mniej danych, dlatego możliwość wyboru jest istotna.  

##Ograniczenia 

   >Program nie będzie w stanie sam poradzić sobie z niuansami księgowymi - jest wiele zawiłości, które trzeba zweryfikować w   trakcie wprowadzania. Księgowi zazwyczaj i tak najpierw księgują wszystkie dokumenty, a później sprawdzają jeszcze raz w programie księgowym, czy wszystko się zgadza. 
 
##Czego jeszcze nie wiem

  >Programy księgowe zazwyczaj mają opcję importowania zaksięgowanych faktur całych firm, lub na całe lata ( np wszystkie dokumenty na 2015r ). Muszę dowiedzieć się w jakiej postaci muszą być przygotowane pliki importowane, wtedy będzie można w łatwy sposób stworzyć "współpracę" pomiędzy dwoma programami i zautomatyzować cały proces. 
  
##Co jeśli nie zostaną spełnione założenia : 

  >Jeśli okaże się, że biblioteka Ocropus nie będzie wystarczająco efektywna w odczytywaniu tego, czego potrzebuję, chcę stworzyć program, który pozwoli na kodowanie wszystkich potrzebnych dannych w kodzie QR ( lub innym tego typu rozwiązaniu ), który będzie można odczytać dzięki narzędziu zainstalowanym na komputerze osoby księgującej. 

##Interfejs użytkownika

  >Użytkownik musi mieć możliwość weryfikacji zczytywanych danych w momencie pojawienia się błędu - w zależności od poziomu skuteczności odczytywania. Jeśli skuteczność będzie na poziomie 99 %, wystarczy, że użytkownik na koniec działania programu zobaczy okno z problematycznymi dokumentami i ręcznie je zredaguje. Jeśli skuteczność okaże się być na poziomie 50%, użtkownik będzie musiał siedzieć przy komputerze i sprawdzać dane pod kątem poprawności. Program będzie działał na platformie Windows i jest interfejs powinien się ograniczać do powiadomienia pojawiającego się w momencie zatrzymania działania programu ( dokument problematyczny w odczycie ), może w tym momencie również być odgrywany jakiś dźwięk. W momencie pojawienia się błędu wyskakuje np w prawym górnym rogu informacja o błędzie, oraz przycisk, którym można wznowić działanie programu po zredagowaniu wprowadzonych przez niego danych. 
  
##Interakcja ( jak powinien działać krok po kroku ) 
>
  1. Użytkownik włącza program, który wskakuje do traya i działa w tle. 
  2. Program powinien mieć opcję umożliwiającą użytkownikowi wybór, czy chce, żeby program działał od razu po włączenu, czy dopiero w momencie wciśnięcia np. start. 
  3. Kiedy program działa, sprawdza on wprowadzony wcześniej folder ( folder, do którego skaner zapisuje zdjęcia dokumentów ), a kiedy znajdzie nowy plik, wykonuje na nim operacje zczytywania. 
  4. Zczytane dane sa zapisywane do pliku csv, lub wprowadzane automatycznie do programu ( nie jestem jeszcze pewien, czy jest możliwość, stąd dwa różne pomysły ) 
  5. Program powinien mieć możliwość ustawienia, czy użytkownik chce zreadgować błędnie zczytane dokumenty na samym końcu skanowania, czy w momencie pojawienia się błędu. 
  6. W momencie, w którym nie będą pojawiały się nowe obrazy w folderze skanowania, program powinien odliczać ok minuty, po czym pownno wyskoczyć okno z zapytaniem, czy użytkownik chce zakończyć jego działanie. 
