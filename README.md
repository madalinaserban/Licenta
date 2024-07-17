# Licenta
 
 Comunicarea între dispozitive și accesul instantaneu la informații în timp real reprezintă o 
cerință în creștere continuă, cu un impact semnificativ în domeniul medical. 
Prin proiectul “Take Care” propunem îmbinarea mai multor tehnologii în vederea 
automatizării gestionării datelor din spitale.  

În prima parte a proiectului avem în vedere implementarea unei aplicații pentru sistemul 
de operare Android cu ajutorul căreia utilizatorii își pot vedea locația curentă, cel mai 
apropiat spital, numărul de locuri disponibile din spitale în funcție de secție și rute către 
acestea. Aplicația mobilă este însoțita de un Raspberry 3B+ împreuna cu un modul RFID 
RC522 ce actualizează în timp real atât numărul de locuri libere din spitale cât și istoricul 
pacientului. 

Pentru partea administrativă, a fost dezvoltată o aplicație web care are la bază 
gestionarea și actualizarea datelor pacienților. Prin intermediul acestei aplicații urmărim 
stocarea centralizată a datelor pacienților și eficientizarea timpului acordat de personalul 
medical privind diagnosticarea și tratarea pacienților. 

Distribuția cardului național de sănătate, care a început pe data de 19 septembrie 20141 
pentru persoanele asigurate cu vârsta de peste 18 ani, marchează un pas semnificativ în 
modernizarea sistemului de asigurări de sănătate, o ițiativă ce a avut ca scop înființarea 
unui sistem mai eficient de gestionare a informațiilor și îmbunătățirea accesului la 
serviciile medicale. 
Prin proiectul "Take Care", am propus accesul și monitorizarea pacienților în diferite secții 
ale spitalelor pe baza cardului de sănătate activat. Cardul de sănătate aflat în uz curent 
stochează date precum: numele și prenumele asiguratului, data nașterii și termenul 
de valabilitate al cardului, dar pentru utilizarea aplicațiilor propuse singurele date 
necesare sunt numărul de identificare al cardului, restul informaților fiind stocate în baza 
de date din cloud. 
Prin folosirea aplicațiilor implementate se propune simplificarea procesul de înregistrare,  
autentificare și identificare a pacienților, astfel reducându-se nevoia de documente fizice 
și timpul de așteptare. 

În acest proiect, arhitectura joacă un rol crucial în asigurarea unei interacțiuni eficiente 
între aplicații. Fiecare componentă are propriul rol specific și schimbă informații cu 
celelalte prin conectarea la platforma Firebase pentru a facilita stocarea și sincronizarea 
datelor în timp real. 
Aplicația web este destinată personalului calificat din spitale și are ca scop administrarea 
și actualizarea datelor pacienților. Personalul medical și administratorii spitalelor pot 
accesa platforma web pentru a gestiona informațiile pacienților, inclusiv înregistrarea și 
actualizarea datelor sau activarea/dezactivarea cradurilor din baza de date. 
Aplicația Android oferă utilizatorilor acces la informații despre spitalele din baza de date 
printre care: numărul de locuri disponibile în funcție de secția selectată, o rută de la 
locația curentă și ratingul conform Google Maps. Utilizatorii pot utiliza cardul de sănătate 
pentru autentificare și vizualizare a datelor personale. 
Scopul dispozitivului Raspberry Pi, împreună cu modulul RFID RC522 este de a actualiza 
în timp real numărul de locuri libere din spitale și de a păstra istoricul vizitelor fiecărui 
pacient. Dispozitivul actualizează aplicația mobilă prin intermediul platformei Firebase, 
astfel asigurând sincronizarea și actualizarea în timp real a informațiilor. 
Platforma Firebase este utilizată pentru a trimite datele către toate componentele 
sistemului. Aceasta oferă o modalitate rapidă si eficientă de colectare, stocare si trimitere 
de date între toate dispozitivele monționate.

![image](https://github.com/user-attachments/assets/44417ce9-f26e-4189-b978-0d02d6ff2e37)

Arhitectura discutată mai sus asigură o interacțiune eficientă între utilizatori și instituțiile 
medicale, facilitând astfel accesul la informații actualizate. 
În capitolele ce urmează vom detalia în profunzime fiecare componentă a arhitecturii și 
vom evidenția interacțiunile și fluxurile de date dintre acestea.
