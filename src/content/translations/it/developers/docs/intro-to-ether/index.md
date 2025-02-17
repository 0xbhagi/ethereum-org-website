---
title: Intro agli ether
description: Introduzione di uno sviluppatore alla criptovaluta ether.
lang: it
---

## Prerequisiti {#prerequisites}

Per comprendere meglio questa pagina, consigliamo innanzi tutto di leggere l'[Introduzione a Ethereum](/developers/docs/intro-to-ethereum/).

## Cos'è una criptovaluta? {#what-is-a-cryptocurrency}

Una criptovaluta è un mezzo di scambio protetto da un registro basato su blockchain.

Con mezzo di scambio si intende qualsiasi forma di pagamento ampiamente accettata per beni e servizi, mentre con registro si intende un archivio di dati che tiene traccia delle transazioni. La tecnologia Blockchain consente agli utenti di effettuare transazioni sul registro senza fare affidamento su una terza parte fidata per mantenere il registro.

La prima criptovaluta è stata Bitcoin, creata da Satoshi Nakamoto. Dal rilascio di Bitcoin nel 2009, sono state create migliaia di criptovalute su molte blockchain diverse.

## Cos'è un ether? {#what-is-ether}

**Ether (ETH)** è la criptovaluta impiegata per molti scopi sulla rete Ethereum. Fondamentalmente è l'unica forma di pagamento accettabile per le commissioni sulle transazioni, e dopo [la fusione](/upgrades/merge) servianno degli ether per convalidare e proporre blocchi sulla rete principale. Ether viene anche utilizzato come forma primaria di garanzia nei mercati dei prestiti [DeFi](/defi), come unità di conto nei mercati NFT, come pagamento guadagnato per l'esecuzione di servizi o la vendita di beni fisici e altro ancora.

Ethereum consente agli sviluppatori di creare [**applicazioni decentralizzate (dapp)**](/developers/docs/dapps), che condividono tutte un pool di potenza di elaborazione. Questo pool condiviso è limitato, quindi Ethereum necessita di un meccanismo per determinare chi lo usa. In caso contrario, una dApp potrebbe consumare accidentalmente o malevolmente tutte le risorse della rete, impedendo ad altri di accedervi.

La criptovaluta ether supporta un meccanismo di determinazione dei prezzi per la potenza di calcolo di Ethereum. Quando vogliono effettuare una transazione, gli utenti devono pagare ether per far riconoscere la propria transazione sulla blockchain. Questi costi d'uso sono noti come [commissioni del carburante](/developers/docs/gas/) e dipendono dalla quantità di potenza di calcolo necessaria per eseguire la transazione e dalla domanda di potenza di calcolo a livello della rete in quel momento.

Pertanto, anche se una dApp malevola inviasse un ciclo infinito, a un certo punto la transazione terminerebbe gli ether e si arresterebbe, consentendo alla rete di tornare alla normalità.

Capita [spesso](https://www.reuters.com/article/us-crypto-currencies-lending-insight-idUSKBN25M0GP#:~:text=price%20of%20ethereum) [di](https://abcnews.go.com/Business/bitcoin-slumps-week-low-amid-renewed-worries-chinese/story?id=78399845#:~:text=cryptocurrencies%20including%20ethereum) [confondere](https://www.cnn.com/2021/03/14/tech/nft-art-buying/index.html#:~:text=price%20of%20ethereum) Ethereum con ether; quando qualcuno si riferisce al "prezzo di Ethereum", è facile che stia parlando del prezzo dell'ether.

## Coniare ether {#minting-ether}

La coniazione è il processo con vengono creati nuovi ether sul registro di Ethereum. Il protocollo sottostante di Ethereum crea i nuovi ether, cosa impossibile da fare per un utente.

L'ether è coniato quando è creato un nuovo blocco sulla blockchain di Ethereum. Come incentivo a creare i blocchi, il protocollo concede una ricompensa in ogni blocco, incrementando il saldo di un indirizzo impostato dal produttore del blocco. Nel tempo la ricompensa per i blocchi è cambiata e oggi ammonta a 2 ETH per blocco. Dopo la fusione, l'emissione di ogni validatore dipende dalla quantità di ether che hanno messo in staking e dalle loro prestazioni.

## Bruciare ether {#burning-ether}

Oltre a essere creato tramite le ricompense per il blocco, l'ether può essere anche distrutto o "bruciato", come si dice in gergo. L'ether bruciato viene rimosso dalla circolazione in via permanente.

La bruciatura di ether ha luogo in ogni transazione su Ethereum. Quando gli utenti pagano per le proprie transazioni, viene distrutta una commissione di base sul gas, impostata dalla rete a seconda della domanda di transazioni. Questo, insieme a dimensioni variabili dei blocchi e una commissione del gas massima, semplifica la stima della commissione di transazione su Ethereum. Quando la domanda della rete è elevata, i [blocchi](https://etherscan.io/block/12965263) possono bruciare più ether di quanto ne sia coniato, compensando efficacemente l'emissione di ether.

Bruciare la commissione di base impedisce vari metodi in cui i produttori del blocco potrebbero altrimenti manipolarla. Ad esempio, se i produttori del blocco hanno ricevuto la commissione di base, potrebbero includere le proprie transazioni gratuitamente e aumentare la commissione di base per tutti gli altri. In caso contrario, potrebbero rimborsare la commissione di base ad alcuni utenti al di fuori della catena, creando così un mercato delle commissioni sulle transazioni più opaco e complesso.

## Denominazioni dell'ether {#denominations}

Poiché molte transazioni su Ethereum sono di dimensioni ridotte, l'ether ha diverse denominazioni che possono essere utilizzate per importi di piccola entità. Tra queste denominazioni, Wei e gwei sono particolarmente importanti.

Wei è la quantità più piccola possibile di ether. Di conseguenza, molte implementazioni tecniche, come l'[Ethereum Yellowpaper](https://ethereum.github.io/yellowpaper/paper.pdf), effettuano tutti i loro calcoli in Wei.

Gwei, abbreviazione di giga-wei, è spesso usato per descrivere i costi del gas su Ethereum.

| Denominazione | Valore in ether  | Uso comune                                     |
| ------------- | ---------------- | ---------------------------------------------- |
| Wei           | 10<sup>-18</sup> | Implementazioni tecniche                       |
| Gwei          | 10<sup>-9</sup>  | Commissioni sul carburante leggibili dall'uomo |

## Trasferire ether {#transferring-ether}

Ogni transazione su Ethereum contiene un campo di `valore`, che specifica l'importo di ether da trasferire, denominato in wei, e da inviare dall'indirizzo del mittente all'indirizzo del destinatario.

Quando l'indirizzo del destinatario è uno [smart contract](/developers/docs/smart-contracts/), questo ether trasferito potrebbe essere usato per pagare il carburante quando lo smart contract esegue il proprio codice.

[Maggiori informazioni sulle transazioni](/developers/docs/transactions/)

## Interrogare l'ether {#querying-ether}

Gli utenti possono interrogare il saldo di ether di qualsiasi [accout](/developers/docs/accounts/) consultando il rispettivo campo del `saldo`, che mostra le posizioni in ether denominate in wei.

[Etherscan](https://etherscan.io) è uno strumento popolare per consultare i saldi dell'indirizzo attraverso un'applicazione basata sul web. Per esempio, [questa pagina di Etherscan](https://etherscan.io/address/0xde0b295669a9fd93d5f28d9ec85e40f4cb697bae) mostra il saldo per la Ethereum Foundation. I saldi del conto sono anche interrogabili usando i portafogli o direttamente effettuando richieste ai nodi.

## Letture consigliate {#further-reading}

- [Definire Ether ed Ethereum](https://www.cmegroup.com/education/courses/introduction-to-ether/defining-ether-and-ethereum.html) – _CME Group_
- [Ethereum Whitepaper](/whitepaper/): La proposta originale per Ethereum. Questo documento include una descrizione dell'ether e le motivazioni dietro alla sua creazione.
- [Gwei Calculator](https://www.alchemy.com/gwei-calculator): Usa questa calcolatrice di gwei per convertire facilmente wei, gwei ed ether. Basta inserire qualsiasi importo di wei, gwei o ETH e calcolare automaticamente la conversione.

_Conosci una risorsa pubblica che ti è stata utile? Modifica questa pagina e aggiungila!_
