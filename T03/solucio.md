# 🐧 Part Linux: LVM amb Zorin OS

Un cop superada la fase de formació, ja esteu preparats per afrontar el repte dels nostres clients.  

Com ja es va explicar, tenim un nou i important client: el bufet d’advocats **Garriga i Associats**, un dels més prestigiosos de la ciutat. Aquest client gestiona una gran quantitat d'informació legal sensible, per la qual cosa la **integritat**, la **disponibilitat** (alta redundància) i la **facilitat de gestió** del seu emmagatzematge són d'importància crítica. ⚖️💾  

![captura1](img/capt1.png)

La direcció de *Garriga i Associats* ha expressat la necessitat urgent de **renovar els seus sistemes de servidors** per garantir que la informació estigui protegida contra fallades de disc i que l'espai pugui ser ampliat sense interrupcions.

Com a tècnics d’**Everpia**, teniu l'encàrrec de **dissenyar i documentar** les solucions d'emmagatzematge que compliran aquests requisits tant en entorns **Linux** com **Windows**.  
Aquest disseny permetrà presentar al client una proposta de solució sòlida i escalable.

---

## 🎯 Objectiu Principal

Dissenyar i documentar **dues solucions d'emmagatzematge** (una per servidors **Linux** i una per **Windows**) que compleixin amb els principis següents:

- 🔁 Alta disponibilitat  
- 🧩 Redundància  
- 📈 Escalabilitat  

> 🧠 Com que és una prova de concepte, no es treballarà amb servidors físics, sinó amb **màquines virtuals** de sistemes operatius clients per documentar els procediments.

---

## 🐧 1. Part Linux: LVM amb Zorin OS

S'ha d'utilitzar la distribució **Zorin OS** (o una alternativa Linux compatible) per demostrar la utilitat del **Logical Volume Manager (LVM)**.

### ⚙️ Requisits de la Implementació i Demostració

#### 🧱 Configuració Inicial
- Crear un **grup de volums (VG)** i un **volum lògic (LV)** utilitzant **dos discs durs simulats** de **10 GB** cadascun.  
- El volum ha d’estar **formatat i muntat automàticament** al sistema mitjançant l’edició de l’arxiu `/etc/fstab`.

#### 🔒 Alta Disponibilitat
- Implementar una configuració amb **mirall (lvm_mirror)** per protegir la informació davant la fallada d’un disc.

#### 🪞 Instantànies (Snapshots)
- Afegir **dos discos de 10 GB** addicionals al grup de volums.  
- Crear un volum `lvm_dades` amb el **primer disc afegit**, formatar-lo i muntar-lo.  
- Afegir-hi **arxius (per exemple, imatges d’Internet)**.  
- Utilitzar el **segon disc** per crear un **snapshot (`lv_snapshot`)** i documentar com **restaurar-lo** en cas que la informació original es danyi.

#### 📈 Escalabilitat
- Demostrar el procés d’**ampliació del volum `lv_dades`** utilitzant l’espai lliure restant dins el grup de volums.

---

## 🧰 Configuració Inicial

Com a **configuració inicial**, i amb la màquina **aturada**, s’han creat **dos discs virtuals de 10 GB cadascun**.  
Això permet disposar d’un **emmagatzematge més elevat** per realitzar totes les proves i configuracions necessàries. 💽💡

![captura2](img/capt2.png)

---

## 💽 Verificació dels Discs Virtuals

Acte seguit, hem obert la **màquina virtual** i hem comprovat, amb la següent comanda, que el sistema hagi detectat els dos discos creats anteriorment:

```bash
fdisk -l

```

Vols que continuï amb el següent pas (per exemple, la creació de particions amb `pvcreate`, `vgcreate`, etc.) en el mateix estil Markdown? Puc seguir el fil i fer-te tota la documentació pas a pas.

![captura3](img/capt3.png)

---

## ⚙️ 1. Configuració inicial d’un grup de volums (VG) i un volum lògic (LV)

Per començar, hem creat els **volums físics** amb la comanda següent:

```bash
sudo pvcreate

sudo apt install lvm2


Vols que continuï amb el següent pas — la creació del **Volume Group (VG)** i el **Logical Volume (LV)** amb les seves comandes (`vgcreate`, `lvcreate`, etc.) en el mateix estil Markdown?

```
![captura4](img/capt4.png)
