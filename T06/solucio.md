# 🧩 T06: Fonaments del servei DNS

```{"variant":"standard","id":"73152","title":"Fase Pràctica: Diagnosi de Noms (Auditoria amb CLI)"}
# 🧰 Fase Pràctica: Diagnosi de Noms (Auditoria amb CLI)

## ℹ️ Sobre aquesta guia
Aquesta guia descriu com dur a terme una **auditoria DNS** emprant les eines més habituals de la línia d’ordres.  

El **DNS (Domain Name System)** actua com una mena d’“agenda de contactes” d’Internet, traduint els **noms de domini** (com ara `google.com`) en **adreces IP** comprensibles pels ordinadors. 🌐💻
```

## 🧪 Comanda 1: Consulta Bàsica de Registre A

### 💻 Codi utilitzat

```bash
dig xtec.cat A
```

### 🔍 Anàlisi

La **IP de resposta** és `83.247.151.214`, amb un **valor TTL** de `3270` segons.
El **servidor que va respondre** és `127.0.0.53`, que correspon al **servidor DNS local** del sistema.

El **temps de consulta** va ser de `5 ms`, un resultat molt ràpid.
El **TTL** indica quant de temps es mantindrà aquesta resposta a la **memòria cau** abans de realitzar una nova consulta. ⚡🧠

![cptura3](img/capt3.png)

## 🧪 Comanda 2: Consulta de Servidors de Noms (NS)

### 💻 Codi utilitzat

```bash
dig tecnocampus.cat NS
```

### 🔍 Anàlisi

El domini **tecnocampus.cat** disposa de **quatre servidors de noms autoritatius**:

* `ns-1689.awsdns-19.co.uk`
* `ns-535.awsdns-02.net`
* `ns-1071.awsdns-05.org`
* `ns-130.awsdns-16.com`

Aquests servidors pertanyen a **AWS (Amazon Web Services)** i són els **responsables finals de proporcionar informació autoritativa** sobre aquest domini. 🌐🛠️

![captura4](img/capt4.png)
