# Opis
Projekt składa się z jednej aplikacji która służy do zarządzania magazynem odpadów radioaktywnych. Obsługuje takie czynności jak dodawanie nowych odpadów, pomiarów i pomiarów tła. Przy dodawaniu odpadu użytkownik musi podać takie informacje jak izotopy zawarte w odpadzie, rodzaj odpadu, jego pochodzenie, gdzie został złożony (pokój, regał i półka) itd. Pomiar musi mieć określoną intensywność promieniowania, odległość z jakiej go wykonano, jakim sprzętem itd. Pomiar tła podobnie tylko że wystarczy podać budynek w jakim go wykonano.
Przechowywane są także informacje o tym jakie osoby wykonują pomiary, oddają odpady do magazynu, odbierają odpady itp. 
Na podstawie parametrów takich jak czas przechowywania odpadu (przyjęte jest 10 okresów połowicznego rozpadu od daty powstania) i\lub jego radioaktywność (względem tła) staje się on dostępny do wyrzucenia.  
W produkcji serwerem aplikacji jest gunicorn, proxy nginx a baza danych to mySQL/mariaDB. Całość uruchamiana jest w containerze dockerowym we wspólnej sieci. Do stawiania containerów wykorzystywany jest docker-compose.  

# Struktura

aplikacja `waste`  
projekt `waste_storage`

# Użytkowanie  
Do działania aplikacja wymaga bazy danych mySQL/mariaDB oraz wygenerowania własnego pliku `settings.py`.  
Developerski serwer można postawić za pomocą polecenia `python manage.py runserver`.  

