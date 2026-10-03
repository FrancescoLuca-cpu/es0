# Osservazioni — Esercitazione 0

Gruppo:

Componenti (Francesco Luca, Rachele Giordano  e FrancescoLuca-cpu, Rachele):

URL del repository condiviso: https://github.com/FrancescoLuca-cpu/es0.git

Chi ha usato la tastiera nello step 1 e nello step 2: Ci siamo divisi i comandi

Compilate insieme le osservazioni e discutete le risposte: entrambi dovete
saper spiegare le prove svolte.

## Step 1 — Hello World: compilazione ed esecuzione

Comando di compilazione:gcc -std=c17 -Wall -Wextra -Wpedantic hello.c -o hello

Comando di esecuzione e risultato osservato:./hello stampa di "Hello, computational physics!"
 
Che cosa ho capito su sorgente ed eseguibile: hello.c corrisponde alla sorgente e hello all'eseguibile. Se la sorgente viene modificata e non ricompilata, l'output non riporta le modifiche perche senza compilazione l'eseguibile non viene modificato

Output richiesto e comportamento del programma prima della modifica: Prima dell'aggiunta del comando printf, il file compilava ma non stampava il messaggio richiesto.

Esito dopo la modifica e spiegazione della correzione: Dopo aver aggiunto l'istruzione di stampa, aver compilato la sorgente hello.c ed eseguito hello, il terminale mostrava il messaggio richiesto "Hello, computational physics!". Inoltre, modificando il messaggio nel comando printf senza ricompilare, l'output non riportava le modifiche.

## Step 1 — Git

Quali file ho incluso nel commit e perché: Nel commit abbiamo incluso hello.c e osserazioni.md, per riportare le modifiche ai file

Come ho verificato che la versione provata sia presente su GitHub: Con il comando git status.

Che cosa ho osservato prima e dopo `git pull`, e perché non serve un nuovo clone: Dopo git pull le modifiche vengono scaricate e integrate automaticamente aggiornando i file nella cartella di lavoro all'ultima versione disponibile sul server. Non serve eseguire un nuovo git clone perche questo comando scarica l'intero repository solo la prima volta. Git pull permette invece di scaricare solo le differenze e i nuovi commit in modo rapido 

## Step 2 — Eco: prima prova

Argomenti passati, comando e risultato: ciao 12 3.5, ./eco ciao 12 3.5, ciao 12 3.50000

Che cosa posso concludere: Il programma acquisisce correttamente i 3 argomenti da riga di comando, converte la stringa del secondo valore in intero e quella del terzo in double, stampando i valori separati da spazio nell'ordine richiesto e terminando con una nuova riga.

## Step 2 — Eco: seconda prova

Argomenti passati, comando e risultato: ciao 12 3.5, ./eco ciao 12 3.5, ciao 0 3.500000

Che cosa ho capito su testo, conversioni e stampa: La prima stringa viene usata così com'è tramite il puntatore char *. Le funzioni atoi e atof convertono i caratteri numerici in valori di tipo int e double. Nella printf, la specifica %.6f impone la stampa di esattamente sei cifre decimali dopo il punto. 

## Step 2 — Risultato ed errori

Previsioni per l'esecuzione con argomenti validi e per quella con `dodici`:Con argomenti validi (es. 12 3.5), le conversioni hanno successo e il programma stampa i tre valori come richiesto. Passando la stringa "dodici" al posto di 12, la funzione atoi non trova cifre valide e stampa 0 al posto dell'intero.   

Contenuto di `eco.txt`, messaggi nel terminale e codici di uscita osservati:ciao 12 3.500000 ciao 0 3.50000, /eco ciao 12 3.5 > eco.txt  ./eco ciao 0 3.5 > eco.txt, il codice d'uscita risulta pari a 0 poiché il codice è stato eseguito con successo

Come un controllo automatico può riconoscere un errore: Un controllo automatico riconosce un errore verificando che il codice di uscita del programma sia diverso da zero, controllando la presenza di messaggi di errore sullo standard error oppure riscontrando un output/file generato diverso da quello atteso.

## Step 2 — Parametri e calcolo fisico

Quando serve ricompilare e quando basta cambiare gli argomenti: Serve ricompilare ogni volta che si modifica il codice sorgente ovvero eco.c

## Step 2 — Git

Come riconosco nella cronologia i commit dei due step:Eseguendo il comando git log --oneline da terminale e identificando i commit distinti tramite i relativi messaggi descrittivi.

Come ho verificato che la versione finale sia presente su GitHub: Verificando tramite git status che il ramo locale sia completamente allineato a quello remoto (Your branch is up to date with 'origin/main') e controllando direttamente sulla repository su GitHub che l'ultimo commit sia presente.
