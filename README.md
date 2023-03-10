Verificarea unui input de face verificand liniile -> coloanele -> regiunile

1. Verificarea validitatii pe linii
Stim ca, in input, o linie este cuprinsa intre doua "*". Astfel, masina trece de
prima "*" si cauta, pe rand, numerele de la 1 la 4 pana la ultima "*".
De exemplu, pentru prima linie, se trece de prima "*" si se cauta nr 1. Daca
este gasit, Masina Turing se intoarce la inceputul liniei si porneste cautarea
nr-lui 2, asemanatoare cu cea a lui 1. Se repeta procedura pana la nr 4.Daca 
atunci cand este cautat un nr se ajunge la urmatoarea "*", cea care ne spune ca
prima linie s-a terminat, atunci Masina Turing ajunge in starea N, unde isi
termina executia. Logica este urmatoarea: daca exista un duplicat al vreunui
numar, atunci stiu sigur ca unul dintre numere lipseste de pe linie.

2. Verificarea validitatii pe coloane
2.1. Prima coloana
Logica este aceeasi, caut numerele de la 1 la 4, iar daca unul dintre ele nu
exista inseamna ca avem unul sau mai multe duplicate din celelalte numere. Ceea
ce se schimba este parcurgerea. Prima coloana este reprezentata de primul
element de dupa fiecare "*". Astfel, cand caut, de exemplu, cifra 1, pornesc de 
la prima "*", verific primul element, daca nu il gasesc, merg la urmatoarea "*" 
si tot asa pana la ultima steluta, la care, daca se ajunge, elementul de dupa 
ea va fi "_" ceea ce inseana ca am ajuns la finalul primei coloane, deci
numarul 1 lipseste din acea coloana => Masina Turing ajunge in starea N, unde
isi termina executia. Daca nr 1 este gasit, Masina Turing se duce la inceputul
inputului si se cauta in mod asemanator urmatoarele numere.
2.2. A doua coloana
A doua coloana este reprezentata de toate numerele care se afla inaintea 
simbolului ":". Prima oara vom cauta nr 1. Parcurgem inputul pana la ":"
si ne intoarcem cu o pozitie inapoi si verificam numarul. Daca nu este egal cu 1
atunci parcurgem inputul pana la urmatoarea "*", apoi pana la primul simbol
":" pe care il gasim, ne intoarcem cu o pozitie inapoi si verificam numarul.
Se repeta procedura pana ajungem la finalul inputului, "_", unde Masina intra in
srarea N si isi termina executia, sau, daca numarul este gasit, ne intoarcem
la inceputul inputului si cautam urmatorul numar in acelasi mod.
2.3.-2.4. A treia si a patra coloana
Dupa ce a doua coloana a fost verificata si a fost validata, se merge la finalul
inputului si se verifica, pe rand, a patra coloana, apoi a treia coloana, 
dupa cum urmeaza:
-pentru coloana 4, verificarea este aceeeasi ca la prima coloana, cu exceptia
parcurgerii. Atunci cand parcurgem elementele de pe coloana acestea vor fi
verificate de la final la inceput(de la dreapta la stanga inputului). Astfel,
ultimul element de pe coloana 4 se afla dupa ultima steluta(daca citim 
de la dreapta la stanga). Atunci cand numarul este gasit, ne intoarcem la
sfarsitul inputului, altfel, daca ajungem la inceputul inputului, la "_"
Masina Turing ajunge in starea N.
-pentru coloana 3, verificarea este asemanatoare cu verificarea celei de-a doua
coloane, exceptie facand parcurgerea, care se face de la finalul inputului la
inceputul lui(de la dreapta la stanga). Astfel, daca citim de la drepta la
stanga, ultima cifra din coloana 3 se afla dupa primul simbol ":" pe care
il gasim. Daca numarul cautat nu este gasit, de ducem la urmatorul element
de pe coloana 3, parcurgand inputul catre inceput. Daca nr este gasit, ne 
intoarcem la finalul inputului, altfel Msina intra in starea N.

3. Verificarea validitatii pe regiuni
regiuni:
1 2
4 3

3.1. Regiunile 1 si 3
-pentru regiunea 1 trebuie verificate, de la stanga la dreapta, cele 2 cifre
aflate dupa primele 2 stelute("*").
-pentru regiunea 3 trebuie verificate, de la dreapta la stanga, cele 2 cifre
aflate dupa(la stanga) ultimele 2 stelute.
3.2. Regiunile 2 si 4
-pentru regiunea 2 trebuie verificate, de la stanga la dreapta, cele 2 cifre
aflate dupa primele doua caractere ":".
-pentru regiunea 4 trebuie verificate, de la dreapta la stanga, cele 2 cifre
aflate dupa ultimele 2 caractere ":"(adica la stanga lor).
Verificarile merg dupa aceeasi logica, exact ca si pana acum, se verifica
fiecare numar in parte daca exista in regiune.
