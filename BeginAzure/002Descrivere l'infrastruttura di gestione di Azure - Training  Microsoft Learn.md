---
created: 2024-02-08T09:38:21 (UTC +01:00)
tags: []
source: https://learn.microsoft.com/it-it/training/modules/describe-core-architectural-components-of-azure/6-describe-azure-management-infrastructure
author: wwlpublish
---

# Descrivere l'infrastruttura di gestione di Azure - Training | Microsoft Learn

> ## Excerpt
> Descrivere l'infrastruttura di gestione di Azure

---
-   7 minuti

L'infrastruttura di gestione include risorse e gruppi di risorse, sottoscrizioni e account di Azure. Se si comprende l'organizzazione gerarchica diventa più facile pianificare i progetti e i prodotti in Azure.

## Risorse e gruppi di risorse di Azure

Una risorsa è il blocco predefinito di base di Azure. Tutto ciò che si crea, di cui si effettua il provisioning, che si distribuisce e così via è una risorsa. Macchine virtuali (VM), reti virtuali, database, servizi cognitivi e così via sono tutti considerati risorse all'interno di Azure.![[003resource-group-eb2d7177.png]]

![Diagram showing a resource group box with a function]

I gruppi di risorse sono semplicemente raggruppamenti di risorse. Quando si crea una risorsa, è necessario inserirla in un gruppo di risorse. Anche se un gruppo di risorse può contenere molte risorse, una risorsa può appartenere a un solo gruppo di risorse alla volta. È possibile spostare le risorse tra gruppi di risorse, ma la risorsa che viene spostata in un nuovo gruppo non sarà più associata al gruppo precedente. Inoltre i gruppi di risorse non possono essere annidati. Questo significa che non è possibile inserire il gruppo di risorse B all'interno del gruppo di risorse A.

I gruppi di risorse offrono un modo pratico per raggruppare le risorse. Quando si applica un'azione a un gruppo di risorse, tale azione verrà applicata a tutte le risorse all'interno del gruppo. Se si elimina un gruppo di risorse, verranno eliminate anche tutte le risorse al suo interno. Se si concede o si nega l'accesso a un gruppo di risorse, si concede o si nega l'accesso a tutte le risorse all'interno del gruppo.

Quando si effettua il provisioning delle risorse, è consigliabile considerare la struttura del gruppo di risorse più adatta alle proprie esigenze.

Se ad esempio si configura un ambiente di sviluppo temporaneo, raggruppando tutte le risorse è possibile eseguire il deprovisioning contemporaneamente di tutte le risorse associate eliminando il gruppo di risorse. Se si effettua il provisioning di risorse di calcolo che richiederanno tre schemi di accesso diversi, potrebbe essere più utile raggruppare le risorse in base allo schema di accesso e quindi assegnare l'accesso a livello di gruppo di risorse.

Non esistono regole rigide su come usare i gruppi di risorse, quindi è bene valutare come configurare i gruppi di risorse per massimizzarne l'utilità per le proprie esigenze.

## Sottoscrizioni Azure

Le sottoscrizioni sono un'unità di gestione, fatturazione e scalabilità in Azure. Così come i gruppi di risorse sono un modo per organizzare in modo logico le risorse, le sottoscrizioni consentono di organizzare logicamente i gruppi di risorse e di facilitare la fatturazione.![[004subscriptions-d415577b.png]]


![Diagram showing Azure subscriptions using authentication and authorization to access Azure accounts.]
L'uso di Azure richiede una sottoscrizione di Azure. Con una sottoscrizione si ottiene l'accesso autenticato e autorizzato ai servizi e ai prodotti di Azure, oltre alla possibilità di effettuare il provisioning delle risorse. Una sottoscrizione di Azure è collegata a un account Azure, ovvero un'identità in Microsoft Entra ID o in una directory considerata attendibile da Microsoft Entra ID.

Un account può avere più sottoscrizioni, ma deve necessariamente averne almeno una. In un account con più sottoscrizioni è possibile usare le sottoscrizioni per configurare modelli di fatturazione diversi e applicare criteri di gestione degli accessi diversi. È possibile usare le sottoscrizioni di Azure per definire i limiti relativi a prodotti, servizi e risorse di Azure. È possibile usare due tipi di limiti delle sottoscrizioni:

-   **Limite di fatturazione**: Questo tipo di sottoscrizione determina la modalità di fatturazione di un account Azure per l'uso di Azure. È possibile creare più sottoscrizioni per diversi tipi di requisiti di fatturazione. Azure genera report di fatturazione e fatture distinti per ogni sottoscrizione, in modo da poter organizzare e gestire i costi.
-   **Limite di controllo di accesso**: Azure applica i criteri di gestione degli accessi a livello di sottoscrizione ed è possibile creare sottoscrizioni separate in base alle diverse strutture organizzative. Ad esempio, all'interno di un'azienda è possibile applicare criteri di sottoscrizione di Azure distinti ai diversi reparti. Questo modello di fatturazione consente di gestire e controllare l'accesso alle risorse di cui gli utenti effettuano il provisioning con sottoscrizioni specifiche.

### Creare sottoscrizioni di Azure aggiuntive

Così come si usano i gruppi di risorse per separare le risorse in base alla funzione o all'accesso, è possibile creare sottoscrizioni aggiuntive per agevolare la gestione delle risorse o della fatturazione. Ad esempio, è possibile scegliere di creare altre sottoscrizioni per separare:

-   **Ambienti**: è possibile scegliere di creare sottoscrizioni per configurare ambienti distinti per lo sviluppo e i test, per la sicurezza o per isolare i dati per motivi di conformità. Questa progettazione è particolarmente utile perché il controllo di accesso alle risorse si verifica a livello di sottoscrizione.
-   **Strutture organizzative**: è possibile creare sottoscrizioni che rispecchino diverse strutture organizzative. Si potrebbe ad esempio limitare un team alle risorse a basso costo e consentire invece al reparto IT l'accesso alla gamma di risorse completa. Questa progettazione consente di gestire e controllare l'accesso alle risorse di cui gli utenti effettuano il provisioning all'interno di ogni sottoscrizione.
-   **Fatturazione**: è possibile anche creare sottoscrizioni aggiuntive per finalità di fatturazione. Poiché i costi vengono prima aggregati a livello di sottoscrizione, potrebbe essere utile creare sottoscrizioni per gestire e tenere traccia dei costi in base alle esigenze. Ad esempio, potrebbe essere necessario creare una sottoscrizione per i carichi di lavoro di produzione e un'altra sottoscrizione per i carichi di lavoro di sviluppo e test.

## Gruppi di gestione di Azure

La parte finale è il gruppo di gestione. Le risorse vengono raccolte in gruppi di risorse e questi ultimi vengono raccolti nelle sottoscrizioni. Se si è appena iniziato a usare Azure, potrebbe sembrare che la gerarchia sia sufficiente per mantenere organizzate le cose. Si supponga tuttavia di dover gestire più applicazioni, più team di sviluppo, in più aree geografiche.

Se si dispone di molte sottoscrizioni, potrebbe essere necessario trovare una modalità di gestione efficiente degli accessi, dei criteri e della conformità per tali sottoscrizioni. I gruppi di gestione di Azure offrono un livello di ambito superiore alle sottoscrizioni. Si organizzano le sottoscrizioni in contenitori denominati gruppi di gestione e si applicano le condizioni di governance ai gruppi di gestione. Tutte le sottoscrizioni all'interno di un gruppo di gestione ereditano automaticamente le condizioni applicate al gruppo di gestione, allo stesso modo in cui i gruppi di risorse ereditano le impostazioni dalle sottoscrizioni e le risorse le ereditano dai gruppi di risorse. I gruppi di gestione offrono gestione di livello aziendale su larga scala, indipendentemente dal tipo di sottoscrizioni che si possiede. I gruppi di gestione possono essere annidati.

## Gerarchia di gruppi di gestione, sottoscrizioni e gruppi di risorse

È possibile creare una struttura flessibile di gruppi di gestione e sottoscrizioni, in modo da organizzare le risorse in una gerarchia per la gestione unificata di accesso e criteri. Il diagramma seguente mostra un esempio di creazione di una gerarchia per la governance tramite gruppi di gestione.
![[005management-groups-subscriptions-dfd5a108.png]]


![Diagram showing an example of a management group hierarchy tree.]
Alcuni esempi di come usare i gruppi di gestione possono essere:

-   **Creare una gerarchia che applica un criterio**. È ad esempio possibile limitare le posizioni delle macchine virtuali all'area Stati Uniti occidentali in un gruppo chiamato Produzione. Questo criterio erediterà da tutte le sottoscrizioni discendenti del gruppo di gestione e verrà applicato a tutte le macchine virtuali all'interno delle sottoscrizioni. Questi criteri di sicurezza, inoltre, non possono essere modificati dal proprietario della risorsa o della sottoscrizione e ciò consente una governance migliore.
-   **Fornire l'accesso utente a più sottoscrizioni**. Spostando più sottoscrizioni all'interno di un gruppo di gestione, è possibile creare un'assegnazione di controllo degli accessi in base al ruolo di Azure nel gruppo di gestione. L'assegnazione del controllo degli accessi in base al ruolo di Azure a livello di gruppo di gestione significa che anche tutti i gruppi di sottogestione, le sottoscrizioni, i gruppi di risorse e le risorse sottostanti erediteranno tali autorizzazioni. Una sola assegnazione nel gruppo di gestione può consentire agli utenti di accedere a tutte le risorse necessarie invece di eseguire script di controllo degli accessi in base al ruolo di Azure per diverse sottoscrizioni.

Informazioni importanti sui gruppi di gestione:

-   Una singola directory può supportare 10.000 gruppi di gestione.
-   L'albero di un gruppo di gestione può supportare fino a sei livelli di profondità. Questo limite non include il livello radice o il livello di sottoscrizione.
-   Ogni gruppo di gestione e sottoscrizione può supportare un solo elemento padre.

___

## Unità successiva: Esercizio: Creare una risorsa di Azure

[Continua](https://learn.microsoft.com/it-it/training/modules/describe-core-architectural-components-of-azure/7-exercise-create-azure-resource/)


# Summary

Completed100 XP

- 2 minutes

In this module, you learned about the physical and management structure of Microsoft Azure. You were introduced to the relationship between datacenters, availability zones, and regions. You explored how the infrastructure supports the benefits of the cloud, such as high availability and reliability. You also learned about the management infrastructure of Azure. You explored how resources and resource groups are related, and how subscriptions and management groups can help manage resources.

## Learning objectives

You should now be able to:

- Describe Azure regions, region pairs, and sovereign regions.
- Describe Availability Zones.
- Describe Azure datacenters.
- Describe Azure resources and Resource Groups.
- Describe subscriptions.
- Describe management groups.
- Describe the hierarchy of resource groups, subscriptions, and management groups.
