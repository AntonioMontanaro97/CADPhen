# CADPhen
## APPROCCI DI APPRENDIMENTO NON SUPERVISIONATOPER L'ANALISI E IL CONFRONTO DI FENOTIPI EDENDOTIPI NELLA MALATTIA CORONARICA
### Abstract
Il presente progetto di tesi si è svolto nell’ambito del progetto “Intestrat-cad” (Integrated Stratification Tools in Coronary Artery Disease) coordinato dal centro cardiologico Monzino IRCCS. Il progetto Intestrat-cad coinvolge 829 pazienti in uno studio prospettico osservazionale, con lo scopo di stratificare una popolazione affetta da malattia coronarica, la cui incidenza, negli ultimi anni è in notevole aumento. 
Lo scopo principale del progetto è una comprensione più dettagliata e approfondita del motivo per cui alcuni pazienti classificati come a basso rischio tramite gli attuali approcci ed indicatori di rischio cardiovascolare, in realtà incorressero in manifestazioni acute come infarti, angina instabile o morte istantanea. A tal proposito si è voluto migliorare la capacità di individuare questi soggetti in modo da poterli riconoscere preventivamente e curare tempestivamente. Nell’ambito del progetto “Intestrat-cad” il profilo di rischio si baserà su tre diversi componenti: entità della placca coronarica, profilo clinico-fisiopatologico e dati omici. 
In questo progetto di tesi ci si è focalizzati sull’aspetto clinico. In particolare, dal registro per la raccolta di dati clinici RedCap sono stati acquisiti i dati dei pazienti raccolti durante la prima visita di follow-up, che includono dati demografici, risultati di test di laboratorio e comorbidità. Il dataset è stato pre-processato al fine di valutare la qualità dei dati raccolti e risolvere il problema della  mancanza di dati per ottenere un sub-dataset completo e coerente con il tipo di analisi svolta in questa tesi. Quindi, sono stati utilizzati metodi di apprendimento automatico non supervisionati per distinguere sotto-fenotipi che permettessero di ottenere una stratificazione del rischio più accurata. 
A questo scopo, è stato utilizzato un metodo basato sulla rappresentazione dei dati in spazi topologici, chiamato TDA Mapper. L’algoritmo TDA mapper ha richiesto diversi step per l’impostazione di parametri per una rappresentazione stabile e congruente della popolazione in esame, guidata da informazioni cliniche inerenti all’entità della placca osservata. 
La rappresentazione topologica dei dati così ottenuta ha permesso l’identificazione di sottogruppi di pazienti eterogeni da un punto di vista degli score del rischio tradizionali. Si sono quindi analizzati in modo approfondito questi gruppi, per determinare nuovi fenotipi del rischio, che saranno validati durante lo sviluppo del progetto “Intestrat-cad” con lo scopo di ottenere una migliore stratificazione del rischio di eventi acuti e quindi la sensibilità dei modelli predittivi. 

### Descrizione script presenti in cartella:
  1.Lo script  <b>ChoosingLens</b>  rappresenta una prima applicazione dell'analisi topologica dei dati tramite il pacchetto Kmapper. Sono state implementate altre tre funzioni ad hoc  che permettono di visualizzare e confrontare i risultati ma anche di effettuare una prima valutazione delle capacità delle funzioni da cui si ottengono le proeizioni.

 2.Lo script  <b>db_patologie</b> permette di andare a ordinare l'informazione della patologie per ogni paziente. In questo modo ogni paziente avrà una riga con colonne più o meno vuote in relazione alle patologie che sono state diagnosticate. Tale script potrebbe essere molto utile soprattutto in futuro quando verrà presa in considerazione anche tale informazione.

 3.Lo script  <b>ValutazioneImputing</b>  rappresenta un primo approccio per la valutazione a posteriori dell'imputazione svolto dall'algoritmo prescelto. L'idea è quella di svolgere dei test statistici che valutano la proporzione rispetto alla classe dei dati imputati contro quelli non imputati. 

 4.Lo script  <b>PredictionModel_RiskScore</b>  permette di andare a valutare diversi modelli di predizione partendo dai dati raccolti nello studio. Sono stati anche confrontati i diversi modelli con dataset a cui di volta in volta è stata aggiunta diverso tipo di informazione.

 5.Lo script  <b>OriginalDataProject</b>  contiene la parte di preprocessing dei dati: eliminazione delle colonne superflue, ridefinizione di alcune variabili, divisione del dataset rispetto alla visita 1-2-3. Inoltre viene analizzato in modo visivo la missingness dei dati totali e continui nel dataset costituito solo da Visita = "Visita 1" oltre alla correlazione tra le variabile. Infine vi è una sezione in cui vengono paragonati tramite RMSE i diversi algoritmi di imputing per poter scegliere il migliore con cui andare ad imputare l'intero dataset.

 6.Lo script  <b>OriginalDataProject2</b> è lo script principale in cui viene contenuta la Topological Data analysis con anche la parte di integrazione con il pacchetto NetworkX per le analisi delle reti.
 
 ### Installazioni
 Avendo utilizzato Python in Jupyter, segue l'elenco di tutti i packages richiesti per eseguire l'algoritmo:
communities; community; docx; giotto-tda; gower; kmapper; matplotlib; missingno; missingpy; netgraph; networkx;
pandas; pytest; python-igraph; scikit-learn;scipy;seaborn; sklearn; statsmodels; tableone; tables; tabulate; umap-learn;

 ### Autori
 Antonio Montanaro 
 
 ### Stato del progetto
 Progetto di ricerca condotto dal Centro Cardiologico Monzino di Milano non ancora concluso. Progetto di tesi concluso
 
 ### Licenze
 Progetto scritto interamente in Python3 su Jupiter
