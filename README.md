<img src="icons/logo.png" alt="Nexus Tablet Charge Card" width="360">

# Nexus Tablet Charge Card

Card per l'integrazione [Nexus Tablet Charge](https://github.com/Pacco24626/nexus_tablet_charge).

Per ogni tablet mostra il livello di batteria su una barra che disegna anche la
**banda di carica scelta**, così si vede a colpo d'occhio dove sta il dispositivo
rispetto alle sue soglie. Accanto: stato del ciclo, pulsante di carica immediata e
interruttore per sospendere la gestione. Le due soglie si regolano dagli slider,
senza aprire la configurazione dell'integrazione.

## Installazione via HACS

1. HACS → menu ⋮ → **Repository personalizzate**
2. URL `https://github.com/Pacco24626/nexus_tablet_charge_card`, categoria **Dashboard**
3. Installa, poi ricarica il browser con **Ctrl+F5**

## Uso

Aggiungi la card dalla dashboard e scegli **Nexus Tablet Charge**. L'unica cosa da
impostare è il sensore di stato del gruppo:

```yaml
type: custom:nexus-tablet-charge-card
entity: sensor.tablet_stato
```

Opzionale:

```yaml
title: Tablet di casa
```

## Perché serve solo un'entità

Il sensore di stato del gruppo porta negli attributi la mappa completa: tablet,
livelli, soglie, entità dei comandi. La card legge quella. Se aggiungi un tablet
dall'integrazione compare da solo: la configurazione della dashboard non va toccata.

## Requisiti

Integrazione `nexus_tablet_charge` 1.0.0 o superiore. Senza di essa la card non ha
nulla da mostrare.
