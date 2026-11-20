# Insulin Intake Forecasting SaaS — Secure Cloud Computing

Progetto universitario per il corso di **Secure Cloud Computing**, dedicato all'esplorazione, addestramento, containerizzazione e serving in modalità SaaS di un modello di Machine Learning per la **previsione dell'assunzione/fabbisogno di insulina in pazienti con diabete di tipo 1**. L'avanzamento e la suddivisione delle attività sono gestiti tramite **GitHub Issues**.

## Team
* **Ascolese Lara**
* **Beatrice Rebecca**
* **Cuccaro Giacomo**

---

## Panoramica e Obiettivi
Il sistema espone tramite web application un modello di previsione su serie temporali (*time-series forecasting*) applicato a dati relativi al diabete di tipo 1. L'obiettivo è realizzare una soluzione End-to-End containerizzata su infrastruttura cloud sicura, capace di sostenere il carico previsto e rispettare i vincoli di servizio definiti.

### Requisiti di Capacità e Service Level Agreement (SLA)
* **Utenti totali stimati**: ~50.000 clienti.
* **Picco di carico nel serving**: fino a 5.000 richieste simultanee al minuto.
* **Finestra di uptime (Opzione 1)**: dalle 06:00 alle 22:00, tutti i giorni (7 giorni su 7).
* **Availability & Reliability**: $\ge 99{,}5\%$ durante la finestra di uptime.
* **Tolleranza ai guasti (Outage)**: durata massima 30 minuti, media 3 minuti.
* **Tempo di risposta**: $\le 1$ secondo.

---

## Sicurezza e Controlli (Focus Dominio Sanitario)
Trattando previsioni legate alla gestione dell'insulina nel diabete di tipo 1, disponibilità, integrità e protezione del servizio sono aspetti centrali:
* **Supply chain & immagini container**: analisi delle vulnerabilità tramite **Docker Scout** e applicazione delle patch rimovibili prima del rilascio.
* **Sicurezza del cluster e traffic management con NGINX**: configurazione di **NGINX** motivata in base al caso d'uso specifico per proteggere l'accesso e gestire il traffico verso il cluster Kubernetes.
* **Architettura del cluster**: esecuzione su cluster Kubernetes con un control node e uno o più worker node.

---

## Struttura del Repository
Il repository è organizzato separando documentazione e codice per mantenere chiara la struttura del progetto.

```
