# RIPASSO_GENERALE_ACCADEMY_AVANADE


## 📦 Blocco 1 – Concetti base del Cloud e Azure

### 🔹 Cos’è il Cloud Computing?
Il Cloud Computing è un modo di usare la potenza di computer e software tramite Internet, senza doverli avere fisicamente sul proprio PC. È come affittare spazio e potenza da un grande centro dati (data center).



 ### 🔹Tipi di Cloud:
Cloud Pubblico: i servizi sono offerti da provider come Microsoft (Azure), Amazon (AWS), Google (GCP). È come usare un hotel: paghi solo quando lo usi.

Cloud Privato: è gestito internamente da un’azienda. È come avere una villa privata: gestisci tutto da solo.

Cloud Ibrido: unisce pubblico e privato. Usi servizi esterni, ma tieni alcuni dati/servizi sensibili internamente.

### 🔹 Tipi di Servizi Cloud:
IaaS (Infrastructure as a Service): ti affittano hardware (es: macchine virtuali). Esempio: Azure Virtual Machines.

PaaS (Platform as a Service): ti forniscono un ambiente completo per sviluppare e pubblicare app. Esempio: Azure App Service.

SaaS (Software as a Service): usi software già pronto. Esempio: Office 365, Gmail.

DaaS (Desktop as a Service): desktop virtuali accessibili da remoto. Esempio: Azure Virtual Desktop.



### 🔹 Cosa offre Microsoft Azure?
Azure è la piattaforma cloud di Microsoft. Offre servizi per calcolo, rete, archiviazione, sicurezza, database, intelligenza artificiale e tanto altro.


### 🔹 Architettura di Azure:
Azure ha un’organizzazione geografica:

Region: aree geografiche (es. Europa Occidentale).

Coppie di regioni: due regioni accoppiate per garantire backup e continuità.

Availability Set: gruppo di VM distribuite per minimizzare problemi (se una macchina ha problemi, l’altra continua a funzionare).

UD (Update Domain): garantisce che non tutte le VM vengano aggiornate insieme.

FD (Fault Domain): separa fisicamente le macchine per evitare guasti simultanei.



### 🔹 Risorse in Azure:
Una risorsa è qualsiasi servizio creato: una VM, un database, un file system.

Le resource group (gruppi di risorse) servono per organizzare le risorse in base a progetto, cliente o ambiente (test, produzione...).

È importante strutturarle bene fin dall’inizio!


### 🔹 Strumenti di gestione Azure:
Puoi gestire Azure in diversi modi:

Portale Azure: interfaccia grafica via browser.

Azure PowerShell: comandi da terminale Windows.

Azure CLI: comandi da qualsiasi terminale (anche Linux/macOS).

API REST: per automatizzare attività via codice.


### 🔹 Azure Resource Manager (ARM):
È il sistema che gestisce tutte le risorse in Azure. Ti permette di:

Organizzare e raggruppare risorse.

Automatizzare distribuzioni (deploy).

Controllare accessi (chi può fare cosa).

Applicare policy aziendali.



### 🔹 Contratti di servizio (SLA):
SLA (Service Level Agreement): indica la disponibilità garantita (es. 99,9%).

Contratti compositi: più servizi usati insieme devono rispettare tutti il loro SLA per mantenere l’affidabilità dell’intero sistema.
