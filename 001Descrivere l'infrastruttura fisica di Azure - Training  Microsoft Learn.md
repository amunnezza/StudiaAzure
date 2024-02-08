---
created: 2024-02-08T09:05:04 (UTC +01:00)
tags: []
source: https://learn.microsoft.com/it-it/training/modules/describe-core-architectural-components-of-azure/5-describe-azure-physical-infrastructure
author: wwlpublish
---

# Descrivere l'infrastruttura fisica di Azure - Training | Microsoft Learn

> ## Excerpt
> Descrivere l'infrastruttura fisica di Azure

---
-   6 minuti

Durante il percorso con Microsoft Azure, si sentiranno e si useranno termini come aree, zone di disponibilità, risorse, sottoscrizioni e altro ancora. Questo modulo è incentrato sui componenti principali dell'architettura di Azure. I componenti principali dell'architettura di Azure possono essere suddivisi in due raggruppamenti principali: l'infrastruttura fisica e l'infrastruttura di gestione.

## Infrastruttura fisica

L'infrastruttura fisica per Azure inizia con i data center. Concettualmente, i data center sono come data center aziendali di grandi dimensioni. Sono strutture con risorse disposte in rack, con alimentazione, raffreddamento e infrastruttura di rete dedicati.

In qualità di provider di servizi cloud globale, Azure ha data center in tutto il mondo. Tuttavia, i singoli data center non sono direttamente accessibili. I data center sono raggruppati in aree di Azure o in zone di disponibilità di Azure progettate per offrire agli utenti resilienza e affidabilità per i carichi di lavoro aziendali critici.

Il sito [Infrastruttura globale](https://infrastructuremap.microsoft.com/) offre la possibilità di esplorare in modo interattivo l'infrastruttura di Azure sottostante.

### Regioni

Un'area è un'area geografica del mondo che contiene almeno uno, ma potenzialmente più data center in stretta vicinanza collegati tra loro tramite una rete a bassa latenza. Azure assegna e controlla in modo intelligente le risorse contenute in ogni area per garantire che i carichi di lavoro siano correttamente bilanciati.

Quando si distribuisce una risorsa in Azure, è spesso necessario scegliere l'area in cui si vuole distribuirla.

Nota

Alcuni servizi o funzionalità delle macchine virtuali (VM) sono disponibili solo in determinate aree geografiche, ad esempio alcuni tipi di archiviazione o dimensioni delle VM. Per alcuni servizi globali di Azure non è necessario selezionare un'area specifica, come nel caso di Microsoft Entra ID, Gestione traffico di Azure e DNS di Azure.

### Zone di disponibilità

Le zone di disponibilità sono data center separati fisicamente all'interno di un'area di Azure. Ogni zona di disponibilità è costituita da uno o più data center dotati di impianti indipendenti per l'energia, il raffreddamento e la rete. Una zona di disponibilità è configurata per essere un limite di isolamento. Se una zona diventa inattiva, l'altra continua a funzionare. Le zone di disponibilità sono connesse tramite reti in fibra ottica private ad alta velocità.![[availability-zones.png]]



Importante

Per assicurare la resilienza, sono presenti almeno tre zone di disponibilità separate in tutte le aree abilitate per le zone di disponibilità. Tuttavia, non tutte le aree di Azure attualmente supportano le zone di disponibilità.

#### Usare le zone di disponibilità nelle app

È necessario assicurare che servizi e dati siano ridondanti in modo da proteggere le informazioni in caso di errore. Quando si ospita l'infrastruttura, per configurare la ridondanza è necessario creare ambienti hardware duplicati. Azure contribuisce a rendere l'app a disponibilità elevata tramite le zone di disponibilità.

È possibile usare le zone di disponibilità per eseguire applicazioni di importanza strategica e configurare la disponibilità elevata nell'architettura delle applicazioni condividendo le risorse di calcolo, archiviazione, rete e dati in una zona di disponibilità e replicandole in altre zone di disponibilità. Tenere presente che la duplicazione dei servizi e il trasferimento dei dati tra le zone di disponibilità potrebbero essere soggetti a costi.

Le zone di disponibilità sono principalmente destinate a macchine virtuali, dischi gestiti, servizi di bilanciamento del carico e database SQL. I servizi di Azure che supportano le zone di disponibilità rientrano in tre categorie:

-   Servizi di zona: le risorse, ad esempio macchine virtuali, dischi gestiti o indirizzi IP, vengono associate a una zona specifica.
-   Servizi con ridondanza della zona: la piattaforma replica automaticamente le applicazioni e i dati tra le zone, usando ad esempio l'archiviazione con ridondanza della zona o il database SQL.
-   Servizi non a livello di area: i servizi sono sempre disponibili nelle aree geografiche di Azure e sono resilienti alle interruzioni a livello di zona, oltre che alle interruzioni a livello di area.

Anche con la resilienza aggiuntiva offerta dalle zone di disponibilità, è possibile che un evento sia così grande da influire su più zone di disponibilità in una singola area. Per offrire una maggiore resilienza, Azure include le coppie di aree.

### Coppie di aree

La maggior parte delle aree di Azure è associata a un'altra area con la stessa collocazione geografica (ad esempio Stati Uniti, Europa o Asia) ad almeno 480 km di distanza. Questo approccio consente la replica delle risorse in due diverse aree geografiche in modo da ridurre la probabilità di interruzioni dovute a eventi come calamità naturali, agitazioni, interruzioni di corrente o interruzioni della rete fisica che interessano un'intera area. Ad esempio, se un'area dovesse essere interessata da una calamità naturale, verrebbe eseguito automaticamente il failover dei servizi nell'altra area della coppia.

Importante

Non tutti i servizi di Azure replicano automaticamente i dati o eseguono automaticamente il fallback da un'area problematica per eseguire la replica incrociata in un'altra area abilitata. In questi scenari il ripristino e la replica devono essere configurati dal cliente.

Esempi di coppie di aree in Azure sono Stati Uniti occidentali e Stati Uniti orientali o Asia sud-orientale e Asia orientale. Poiché la coppia di aree è direttamente connessa e le aree sono sufficientemente distanti da essere isolate dalle situazioni di emergenza a livello di area, queste possono essere usate per garantire la ridondanza dei servizi e dei dati.![[region-pairs.png]]



#### Altri vantaggi delle coppie di aree includono:

-   Nel caso di un'interruzione di Azure di vaste proporzioni, viene assegnata la priorità a un'area di ogni coppia per assicurarsi che almeno una venga ripristinata il più rapidamente possibile per le applicazioni ospitate nella coppia di aree.
-   Gli aggiornamenti pianificati di Azure vengono implementati nelle coppie di aree un'area alla volta per ridurre al minimo il tempo di inattività e il rischio di interruzione delle applicazioni.
-   I dati continuano a risiedere all'interno della stessa area geografica, ad eccezione del Brasile meridionale, per finalità fiscali e adempimenti legali.

Importante

La maggior parte delle aree è abbinata bi-direzionalmente, ovvero ciascuna costituisce il backup per l'area che rappresenta la rispettiva area di backup (gli Stati Uniti occidentali e gli Stati Uniti orientali costituiscono ciascuna l'area di backup dell'altra). Alcune aree, tuttavia, come l'India occidentale e il Brasile meridionale, sono abbinate solo unidirezionalmente. In questo tipo di abbinamento, l'area primaria non costituisce l'area di backup per l'altra. Pertanto, anche se la regione secondaria dell'India occidentale è l'India meridionale, quest'ultima non potrà fare affidamento sull'India occidentale. L'area secondaria dell'area India occidentale è India meridionale, mentre l'area secondaria dell'India meridionale è India centrale. L'area Brasile meridionale è unica perché è abbinata a un'area esterna alla sua area geografica. L'area secondaria del Brasile meridionale è Stati Uniti centro-meridionali. L'area secondaria degli Stati Uniti centro-meridionali non è il Brasile meridionale.

### Aree sovrane

Oltre alle aree normali, Azure include anche aree sovrane. Le aree sovrane sono istanze di Azure isolate dall'istanza principale di Azure. Può essere necessario usare un'area sovrana per scopi legali o di conformità.

Le aree sovrane di Azure includono:

-   US DoD (area centrale), US Gov Virginia, US Gov Iowa e altre: queste aree sono istanze logiche e fisiche di Azure isolate dalla rete per i partner e gli enti pubblici statunitensi. Questi data center sono gestiti da cittadini statunitensi selezionati e includono certificazioni di conformità aggiuntive.
-   Cina orientale, Cina settentrionale e altre: queste aree sono disponibili nel contesto di una partnership esclusiva tra Microsoft e 21Vianet, in virtù della quale i datacenter non sono gestiti direttamente da Microsoft.

___

## Unità successiva: Descrivere l'infrastruttura di gestione di Azure

[Continua](https://learn.microsoft.com/it-it/training/modules/describe-core-architectural-components-of-azure/6-describe-azure-management-infrastructure/)
