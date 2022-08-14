


  
w docker compose environmet vars są wrzucane w kontener do użytku przez aplikację wew. kontenera  
  
volumes: nie używać jeśli nie potrzebujemy; kontner to tak na prawdę komputer w komputerze który jest odizolowany jeden od drugiego; bo usunięciu kontenera wszystkie dane ze środka są bezpowrotnie usuwane  
  
  
version: "3.9"  
  
services:  
 db:  
 image: postgres  
 volumes:  
 - ./data/db:/var/lib/postgresql/data  
  
powyższy kod łączy folder z komputera z folderem wewnątrz kontenera  
  
NIE UŻYWAC VOLUMES BEZ POTRZEBY  
  
kontener działa wiecznie jako root; jeśli folder nie jest utworzony zostanie zrobiony przez dockera z własicielem root czyli nie ma do nich potem dostępu z poziomu uzytkownika  
  
w przypadku WEB używac volumes;   
  
 web:  
 build: .*volumes**:  
 - .:/code*  
  
Django nie będzie na90% tworzyć żadnych plików; ścieżka .:/code jest już utworzona więc nie dostanie uprawnień root  
Pomaga to w updacie kodu i nie wymaga przebudowania kontenera przy każdej zmianie  
  
ports:  
 - "8000:8000"  
   
 umożliwia łącznenie z lokalnego komputera z portem z kontenera, lewa strona port komputera prawa port kontenera. Lewa strona jest automatycznie przydzielana na localhost. Działa zarówno przy web i db.  
  
  
web:  
 build: .  
   
 oznacza że plik Dockerfile jest obecny w bieżacym folderze  
  
  
  
db:  
 image: postgres  
  
pobiera obraz z dockerhuba  
  
  

```python
docker compose up --force-recreate   
```
  
  
robi update po zmianie w configu ale może usunąc dane do tej pory stworzone w kontenerze  
  
jeżeli zmiany są w dockerfile, to musi być obraz zrobiony na nowo i dopiero zaciąga się go do docker compose  
  

```python
docker compose up --build
```
  
  
wymusza wtedy zbudowanie nowego obraz w oparciu o zmieniony dockerfile   
  
  
  
Docker jest wrażliwy na kolejnośc parametrów w komendzie  
  
id kontenera na samym końcu (z małym wyjątkiem)  
  
WEJŚCIE DO CHODZĄCEGO KONTENERA  
  

```python
docker exec <nazwa\_kontenera> bash # exec uruchamia komendę w kontenerze o podanej nazwie ; bash to komenda do uruchomienia  
```
  
  
  
pomocne przy robieniu migracji (up)  
  
komenda run otwiera nowy kontener  
  
komenda exec uruchamia zmiany w istniejącym kontenerze  
  
  

```python
docker compose rm -v 
```
  
  
usuwa wszystkie kontenery ZALECANE PRZED PR i uruchomienie na nowo  
