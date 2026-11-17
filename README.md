# LaboratorioAzureActiveDirectory
Questo è un laboratorio active directory creato su Azure. Le varie versioni sono funzionanti. Lo scopo finale è simulare un collegamento da un datacenter on prem a un datacenter on cloud, avendo tutti i tools di governance funzionanti e sicuri.
# V0.01
In questa versione ho configurato due windows server 2022 (Gen 2) su due reti differenti: ho creato due Vnet distinte e le ho collegate tramite Vpeering. Una delle due macchine l'ho impostata come domain controller. Ho configurato le impostazioni Azure per il DNS. Ho creato due OU (una per le macchine, l'altra per gli utenti). Ho creato una Group Policy e l'ho collegata alle due OU. Ho configurato l'altro windows server mettendolo sotto dominio. Ho configurato i permessi di un utente in modo da poter entrare tramite la Virtual Machine Client usando credenziali AD in Azure Bastion. Tutto il sistema è isolato da internet e simula un ambiente AD on premise. Attualmente è tutto funzionante. dentro AD attualmente sono registrati 2 OU, 2 PC, 1 GPO e 2 Utenti con permessi elevati.
Nelle foto:
Foto 1: Topologia Azure
Foto 2: Schermata Active directory nel domain controller con le OU
Foto 3: Schermata Group Policies
Foto 4: Schermata VM client con dimostrazione partecipazione dominio
Foto 5: Errore presentato se si prova ad accedere al pannello di controllo tramite utente secondario (Dimostrazione GPO funzionante)

In allegato l'ARM template del laboratorio senza parametri.
