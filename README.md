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




## 🔹 Blocco 2 – Azure Networking (Reti in Azure)
### 1. 🧱 Virtual Network (VNet) & Subnet
VNet: è come una rete locale (LAN) ma nel cloud. Tutte le risorse (come VM, database, ecc.) possono stare dentro questa rete e comunicare tra loro.

Subnet: sono sottosezioni della VNet. Dividono la rete in più parti per organizzare meglio le risorse e controllare il traffico tra loro.

💡 Esempio: una subnet per i server web, una per i database.




### 2. 🔒 NSG (Network Security Group) & ASG (Application Security Group)
NSG: imposta regole su cosa è permesso o bloccato nella rete. Puoi dire, ad esempio: “Blocca tutte le connessioni tranne quelle sulla porta 80 (HTTP)”.

ASG: invece di assegnare regole a singole macchine, puoi creare gruppi di macchine e assegnare le regole al gruppo.

💡 Esempio: raggruppi tutte le VM web in un ASG chiamato “web” e tutte le regole vengono applicate a tutte insieme.




### 3. 🛣️ Routing & UDR (User Defined Routes)
Azure gestisce automaticamente il traffico tra subnet e VNet.

Ma se vuoi più controllo, puoi creare delle UDR (tabelle di routing personalizzate).

Servono per dirigere il traffico in modi specifici, ad esempio farlo passare da un firewall o un’appliance di rete.

💡 Pensa a UDR come dei cartelli stradali che dicono ai dati dove andare.




### 4. 🔁 VNet Peering
VNet Peering collega due VNet diverse (anche in regioni diverse) come se fossero una sola.

I dati passano in modo privato e veloce (non passano da internet).

💡 Molto utile per grandi infrastrutture distribuite.




### 5. 🌐 VPN Gateway (P2S e S2S)
Point-to-Site (P2S): un singolo PC si collega alla rete aziendale Azure (es. da casa o in trasferta).

Site-to-Site (S2S): intera rete locale collegata a una VNet in Azure (via router VPN).

💡 Serve per lavorare in sicurezza anche da remoto.

### 6. 🔄 NAT (Network Address Translation)
Se una risorsa è in una rete privata, può uscire su Internet tramite NAT Gateway

Non devi configurare NSG complicati, e tutto il traffico esce con un unico IP pubblico.

💡 Utile per VM che devono accedere a Internet ma non vogliono essere esposte.




### 7. ⚖️ Load Balancer (Bilanciatore di Carico)
Distribuisce le richieste tra più macchine (es. VM) per evitare sovraccarichi.

Public Load Balancer: accessibile da Internet.

Internal Load Balancer: usato solo dentro la rete Azure.

💡 Immagina tanti clienti che visitano un sito: il load balancer manda ciascuno alla VM meno occupata.




### 8. 🛑 Endpoint di Servizio & Filtraggio
Gli Endpoint di Servizio collegano una VNet direttamente a un servizio Azure (es. Storage), senza passare da Internet.

Filtraggio: con NSG e ASG puoi bloccare traffico indesiderato o consentire solo quello da subnet specifiche.

💡 Sicurezza aumentata senza perdere la connessione ai servizi.




### 9. 🧠 Azure Network Manager
Strumento centrale per gestire reti su più regioni Azure.

Ti permette di:

Applicare regole NSG a più reti.

Creare policy comuni per tutta l’infrastruttura.

Visualizzare topologie e connessioni.

💡 Ideale per grandi aziende con molte sedi o ambienti diversi.

✅ Ripasso in breve






