# Farmie 

### Prezentare generală
Farmie este o aplicație web dezvoltată în React ce integrează Firebase pentru
autentificare și pentru stocarea datelor și platforma Google Maps pentru afișarea hărților și
gestionarea locațiilor și terenurilor agricole.

Lucrarea îmbină concepte din domeniile economic, financiar și tehnologic, aducând
mai aproape de utilizator uneltele necesare gestionării proprietăților agricole și capitalului
economic.

Aplicația permite înregistrarea utilizatorilor noi și autentificarea celor existenți.
Utilizatorii care nu sunt conectați nu pot accesa paginile aplicației, iar cei autentificați nu se
pot autentifica din nou fără a se deconecta.

Prima pagina este cea de statistici. Aici utilizatorul poate vedea sumele investite,
încasate și profitul realizat. Fiecare sumă aparține unei tranzacții și conține toate detaliile
aferente operațiunii. Utilizatorul poate adăuga sau șterge tranzacțiile și poate vizualiza grafic,
în ordine cronologică, toate operațiunile realizate.

Următoarea pagină privește amplasamentul culturilor și prezintă o hartă. Dacă
utilizatorul oferă permisiunea, harta localizează poziția curentă a acestuia și o afișează, altfel
este afișat întreg teritoriul României, iar utilizatorul poate naviga singur către locația dorită.
De asemenea, se poate folosi bara de căutare pentru a naviga rapid la o anumită locație.

Pe hartă se pot marca terenuri, sub forma unor poligoane pe care utilizatorul le poate
modela sub orice formă pentru a acoperi locația dorită. După ce este realizată modelarea, se
pot introduce informațiile aferente terenului: numele, tipul culturii care se dorește a fi sădită,
precum și detalii auxiliare. Suprafața și locația terenului sunt calculate automat de către
aplicație, folosind geolocația, și sunt actualizate după fiecare modificare a acestuia. Locația
este calculată folosind coordonatele centrului poligonului.

### Obiective
Pe scurt, obiectivele acestei lucrări sunt:
- să ofere o unealtă de măsurare a încasărilor și cheltuielilor agricole, precum și grafice
ale evoluției acestor valori în timp cu scopul realizării unor decizii financiare
informate, care să ajute fermierii să se dezvolte mai rapid și în mod durabil
- să ofere o modalitate intuitivă și vizuală de gestionare a terenurilor agricole
- să ofere posibilitatea de stocare a tuturor informațiilor necesare în cloud
- să utilizeze un număr cât mai mic de resurse din partea utilizatorilor

### Tehnologii
- ***React*** - bibliotecă JavaScript open source ce permite dezvoltarea de pagini web rapide și dinamice
- ***CSS*** - pentru proiectarea stilului în care elementele urmează să fie afișate pe ecran
- ***Bootstrap 4, React Bootstrap și Reactstrap*** - framework-uri și biblioteci utilizate pentru stilizarea componentelor (îmbinărrea acestora oferă flexibilitate, dar și rapiditatea implementării codului. În cazul ultimelor 2, codul este
organizat sub formă de componente, deci este mai apropiat de structura folosită în React, pe când primul este format din marcatori cărora le sunt aplicate diverse clase)
MongoDB Atlas - for the global cloud database service used on Heroku
Heroku - for the hosting and deployment of the website
- ***Firebase*** - este un BaaS (Backend-as-a-Service) și oferă două servii importante utlizate în cadrul aplicației: Cloud Firestore și Firebase Authentication
- ***Cloud Firestore*** - bază de date NoSQL care permite stocarea (în colecții și documente), interogarea și sincronizarea datelor în cadrul dispozitivelor care le utilizează
- ***Firebase Authentication*** - serviciu care facilitează utilizarea unor sisteme de autentificare sigure, îmbunătățind în același timp experiența de conectare a utilizatorilor finali. El oferă posibilitatea creării de conturi folosind e-mailul și parola, autentificarea cu
Google, Twitter, Facebook, și GitHub.

Motivația îmbinării tuturor acestor funcționalități sub forma unei aplicații web a fost
dorința de a oferi o unealtă independentă de sistemele principale de operare ale computerelor
(Windows, Linux, macOS) și ale telefoanelor mobile (iOS, Android). Avantajul rulării
aplicației în browser este acela de a se adresa unui număr cât mai mare de fermieri, întrucât
aceștia nu vor fi restricționați din punct de vedere tehnologic: orice fermier din orice zonă
geografică a țării care dispune de un dispozitiv și de o conexiune la Internet poate accesa
aplicația.
