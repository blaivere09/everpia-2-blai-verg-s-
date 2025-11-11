# T03: Gestió flexible de discos (LVM i Espais d’emmagatzematge)

## 🧾 Breu descripció

Un cop superada la fase de formació, ja esteu preparats per afrontar el repte dels nostres clients.  

Com ja es va explicar, tenim un nou i important client: **el bufet d’advocats Garriga i Associats**, un dels més prestigiosos de la ciutat, que ha requerit els serveis de la nostra consultora.  

Gestiona una gran quantitat d'informació legal sensible, per la qual cosa **la integritat, la disponibilitat (alta redundància)** i **la facilitat de gestió** del seu emmagatzematge són d'importància crítica.

![captura1](img/capt1.png)

La direcció de *Garriga i Associats* ha expressat la necessitat urgent de **renovar els seus sistemes de servidors** per garantir que la informació estigui protegida contra fallades de disc i que l'espai pugui ser **ampliat sense interrupcions**.

Com a tècnics d’**Everpia**, teniu l'encàrrec de **dissenyar i documentar les solucions d'emmagatzematge** que compliran aquests requisits tant en entorns **Linux** com **Windows**. Aquest disseny permetrà presentar al client una proposta de solució.

L'objectiu principal és **dissenyar i documentar dues solucions d'emmagatzematge** (una per servidors Linux i una per servidors Windows) que compleixin amb els principis d’**alta disponibilitat**, **redundància** i **escalabilitat** per al client.  

Com que ha de ser una **prova de concepte**, no treballareu amb servidors, sinó amb **màquines virtuals de sistemes operatius clients** per documentar els procediments.

---

## 🐧 Part Linux: LVM amb Zorin OS

S'ha d'utilitzar la distribució **Zorin OS** (o una alternativa Linux compatible) per demostrar la utilitat del **Logical Volume Manager (LVM)**.

### 🔧 Requisits de la Implementació i Demostració

#### 1. Configuració inicial
- Crear un **grup de volums (VG)** i un **volum lògic (LV)** utilitzant inicialment **dos discs durs simulats de 10 GB**.
- El volum ha d’estar **formatat i muntat automàticament** al sistema mitjançant l’edició de l’arxiu `/etc/fstab`.

#### 2. Alta disponibilitat
- Implementar la configuració d’un **mirall (`lvm_mirror`)** per protegir la informació davant la fallada d'un disc.

#### 3. Instantànies (snapshots)
1. Afegir **dos discos de 10 GB** al grup de volums.
2. Crear un volum (`lvm_dades`) amb el **primer disc afegit**, formatar-lo i muntar-lo.
3. Afegir arxius al volum (poden ser imatges d’Internet).
4. Usar el **segon disc** per crear un **snapshot (`lv_snapshot`)**.
5. Documentar com **restaurar el snapshot** si la informació del volum original es danya.

#### 4. Escalabilitat
- Demostrar el **procés d'ampliació**.
- Usar l’espai lliure dins el grup de volums per **ampliar el volum `lv_dades`**.

---

## 🪟 Part Windows: Espais d'Emmagatzematge (Storage Spaces)

S'ha d'utilitzar **Windows 11** per demostrar les configuracions possibles mitjançant els **Espais d'Emmagatzematge (Storage Spaces)**.

### 🔧 Requisits de la Implementació i Demostració

#### 1. Configuració inicial
- Crear un **Storage Pool** amb **tres discos simulats de 10 GB**.

#### 2. Estudi de configuracions
- **Resiliència de Mirall (Mirroring):**
  - Usar **dos discos**.
  - Comprovar que ofereix **alta disponibilitat**.

- **Resiliència de Paritat (Parity):**
  - Explicar la seva **eficiència d'espai** en comparació amb el mirall.
  - Cal usar **tres discos**.

- **Resiliència de Mirall Triple:**
  - Afegir tants discos de 10 GB com siguin necessaris.

#### 3. Demostració de la gestió
- Mostrar com es visualitza **l'estat dels discos i del pool** des de la **consola de gestió de Windows**.
- Simular la **facilitat de manteniment**.

---

## 👩‍💻 Com treballareu i què lliurareu?

- El treball serà **en grup**.
- En primer lloc, us dividireu en **dos equips**:
  - Un per **Linux (LVM)**.
  - Un per **Windows (Storage Spaces)**.

- **Individualment**, preparareu el **guió de la tasca**, cercant les comandes i la documentació necessària.
- **En parelles**, realitzareu la demostració corresponent.
- Finalment, **tots els membres del grup** revisareu la documentació i **pujareu els resultats al vostre repositori.**

### 📁 Estructura de lliurament
- Crear una carpeta anomenada `tasca03` dins del projecte.
- Incloure-hi tota la documentació en **format Markdown** amb imatges i explicacions.
- L’arxiu principal ha de ser `README.md`, que contindrà:
  - La **descripció de la tasca**.
  - Els **enllaços** als dos documents (Linux i Windows).

### 🧩 Avaluació
- La nota serà **conjunta per al grup**.
- És essencial mantenir una **bona comunicació interna** i **organització.**

### 🗣️ Presentació
Posteriorment, haureu de **presentar al client les conclusions** del vostre treball en una **presentació conjunta**.

---

## 📚 Material de classe (disponible al Moodle)

- **LVM Linux**
- **Espais d’emmagatzematge (Windows)**

