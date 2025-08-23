Con looker lavorare con più tabelle è moolto pesante, ho preferito lavorare sulle singole.

Ho effettuato una prima pulizia dati con power query (es: rimosso duplicati, sostituzione sede "sanremo" con "palafiori", separazione dei nomi cantanti nelle collaborazioni, etc.)

Ogni risultato ottenuto attraverso l'utilizzo di python è stato poi incollato in un nuovo foglio excel che viene poi esaminato da Looker. 

ARTISTI PIÙ PRESENTI NELLA STORIA DI SANREMO 
Scoprire quali cantanti hanno partecipato più volte (anche in duo o gruppo).
ho usato la tabella "classifica"
Nota: Un artista può apparire come solista o come parte di una collaborazione con altri artisti (es. Al Bano, Al Bano & Romina Power, etc.). 

Per conteggiare le partecipazioni dell'artista, solo o in gruppo, ho lavorato con python (pandas) per automatizzare (con un ciclo for) il conteggio, facendo attenzione a contare una sola partecipazione per artista per anno e usando un separatore per distinguere i solisti dalle collaborazioni. Il risultato è stato inserito in un nuovo file excel che ho importato su Looker. 

I CANTANTI PIU VINCENTI
Su excel ho diviso le coppie e trii di cantanti vincenti con un testo in 3 diverse colonne (cantante 1, cantante 2, cantante 3). Questo mi consente di contaggiare con python (pandas) i vincitori in un modo più comodo.


LE PAROLE PIU FREQUENTI NELLE CANZONI E LE PIU FREQUENTI NELLE CANZONI VINCENTI.  
Usando i filtri su excel ho estratto i soli nomi dei vincitori e delle loro canzoni. Ho diviso il testo in colonne per distinguere i singoli cantanti. Ho poi incollato quei valori in un nuovo file chiamato "vincitori sanremo". 
Con python (pandas) ho unito e normalizzato i dati, rimosso i caratteri non alfabetici, imposto delle stopwords che ho poi rimosso all'interno di un ciclo for, e alla fine ho usato un counter per conteggiare le parole filtrate. Alla fine ho fatto una classifica con la funzione .head(). 
Ho poi copiato il risultato su un nuovo file excel "frequenza parole in tutte le canzoni sanremo".

Ho fatto lo stesso lavoro anche per ricavare la classifica delle parole più frequenti, che ho salvato in un file excel "frequenza parole vincenti sanremo" 


AUTORI PIU VINCENTI 
in excel ho sostituito "e" e "," con "-" per poi dividere il testo in colonne usando "-" come separatore. 
Ho poi proceduto ad analizzare con Python (Pandas) i risultati per ottenere la classifica. 


