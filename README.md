## Cel zadania
Rozwinięcie wiedzy z zakresu korzystania z .htaccess

## Przed rozpoczęciem
* Stwórz sobie na serwerze testowym katalog (twoje_imie_data) do którego przegraj zawartość tego repozytorium
* Podepnij testową domenę (np `twoje_imie_data.domena_testowa.pl`, dalej nazywana po prostu `twoja_domena`)
* Podepnij SSL dla testowej domeny, tak aby równolegle działały obie wersje (z i bez certyfikatu)

## Pomocne linki
* Syntax .htaccess
* Rodzaje flag w .htaccess

## Kroki
### Testowanie odpowiedzi serwera ###
* Na stronie [httpstatus.io](https://httpstatus.io/) można testować odpowiedzi serwera
* Poniższe adresy powinny zwracać status 200
** `http://twoja_domena`
** `https://twoja_domena`
### Stwórz przekierowanie na HTTPS ###
* w pliku `.htaccess` stwórz regułę która przekieruje ruch na stronę z aktywnym certyfikatem SSL
* [httpstatus.io](https://httpstatus.io/) adres HTTP powinien zwracać status 301 i kierować na adres HTTPS, adres HTTPS powinien zwracać nadal 200

### Stwóz przekierowanie na HTTPS typu 'catch-all' ###
* Czyli nie używając nazwy domeny przy tworzeniu przekierowania
* W celu przetestowania możesz podpiąć drugą domenę pod katalog na serwerze i sprawdzić czy również dla niej [httpstatus.io](https://httpstatus.io/) zwróci status 301 z adresu HTTP na HTTPS
