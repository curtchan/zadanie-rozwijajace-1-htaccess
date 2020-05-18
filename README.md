## Cel zadania
Rozwinięcie wiedzy z zakresu korzystania z `.htaccess`
Każdy podpunkt rozwiąż osobno, komentarzem opisz co poszczególne linie twojego kodu robią.

## Przed rozpoczęciem
* Stwórz sobie na serwerze testowym katalog (twoje_imie_data) do którego przegraj zawartość tego repozytorium
* Podepnij testową domenę (np `twoje_imie_data.domena_testowa.pl`, dalej nazywana po prostu `twoja_domena`)
* Podepnij SSL dla testowej domeny, tak aby równolegle działały obie wersje (z i bez certyfikatu)

## Pomocne linki
* [Rodzaje flag w .htaccess](https://httpd.apache.org/docs/2.4/rewrite/flags.html)
* [Complete 2020 guide](https://www.whoishostingthis.com/resources/htaccess/)
* [Suchy tester przekierowań .htaccess](https://htaccess.madewithlove.be/) - _nie ogarnia niektórych opcji przy przekierowaniach_
* [Batch RewriteRule Generator](https://donatstudios.com/RewriteRule_Generator) - Generator przekierowań z jednego adresu na drugi, _nie ogarnia przekierowań między-domenami, oraz między protokołami_
* [httpstatus.io](https://httpstatus.io) - Narzędzie do testowania przekierowań
* [generator haseł htpasswd](https://www.htaccesstools.com/htpasswd-%20generator/)

## Zadania
### 1. Testowanie odpowiedzi serwera ###
* Na stronie [httpstatus.io](https://httpstatus.io/) można testować odpowiedzi serwera
* Poniższe adresy powinny zwracać status 200
** `http://twoja_domena`
** `https://twoja_domena`
### Przekierowania ###
#### 2. Stwórz przekierowanie na HTTPS ####
* w pliku `.htaccess` stwórz regułę która przekieruje ruch na stronę z aktywnym certyfikatem SSL
* [httpstatus.io](https://httpstatus.io/) adres HTTP powinien zwracać status 301 i kierować na adres HTTPS, adres HTTPS powinien zwracać nadal 200

#### 3. Stwóz przekierowanie na HTTPS typu 'catch-all' ####
* Czyli nie używając nazwy domeny przy tworzeniu przekierowania
* W celu przetestowania możesz podpiąć drugą domenę pod katalog na serwerze i sprawdzić czy również dla niej [httpstatus.io](https://httpstatus.io/) zwróci status 301 z adresu HTTP na HTTPS

#### 4. Przekieruj podstronę ####
* Przekieruj z podstrony `podstrona-2.php` na `podstrona-3.php`

### Inne zadania z htaccess ###
#### 5. Zabezpieczanie dostępu ####
* Skonfiguruj htaccess tak aby dostęp do `zabezpieczona.php` był dodatkowo zabezpieczony loginem i hasłem

#### 6. Modyfikowanie adresu ####
* Skonfiguruj htaccess tak aby rozszerzenie było ukryte przy wejściu na podstronę `bez-rozszerzenia.php`

#### 7. Dokument błędu ####
* W przypadku wejścia na podstronę która nie istnieje, wyświetl plik `404.php`