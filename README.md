projecte-3/
└── tasca01/
    ├── README.md
    ├── informe.md
    ├── guia.md
    └── img/
        ├── bitwarden-instal·lacio.png
        ├── bitwarden-generador.png
        ├── bitwarden-guardar-credencial.png
        ├── bitwarden-autofill.png
        └── bitwarden-backup.png



        
# T01: Gestor de contrasenyes

## Descripció
Aquesta tasca sorgeix arran d’un incident de seguretat sofert per EverPia, en què una contrasenya feble o reutilitzada va permetre a atacants accedir a informació confidencial.  
Com a resposta, la Direcció Tècnica ha ordenat l’ús obligatori d’un **gestor de contrasenyes** per al personal tècnic.  

L’objectiu d’aquesta activitat és:
1. Analitzar i justificar tècnicament l’ús d’un gestor de contrasenyes.
2. Elaborar una guia pràctica d’ús per a l’eina seleccionada.

---

## Fitxers

- [`informe.md`](./informe.md): Anàlisi i justificació tècnica (Fase 1)
- [`guia.md`](./guia.md): Guia tècnica d’ús (Fase 2)
- Carpeta [`img/`](./img): Conté les captures de pantalla de la guia.

---

## Eina escollida
Després d’una comparativa entre **Bitwarden** i **KeePassXC**, s’ha escollit **Bitwarden** com a solució recomanada per al personal tècnic d’EverPia, per la seva seguretat E2E, sincronització multi-dispositiu i facilitat de gestió centralitzada.






# Informe Tècnic: Gestor de Contrasenyes

## 1. Introducció i Justificació

Les contrasenyes febles o reutilitzades constitueixen una de les principals causes de **compromís de comptes corporatius**.  
Aquests atacs aprofiten vulnerabilitats com:
- **Atacs de diccionari**: proves automatitzades amb contrasenyes comunes (p. ex. “123456”, “password”).
- **Credential stuffing**: reutilització de contrasenyes filtrades en altres webs.
- **Phishing**: enginyeria social per obtenir credencials reutilitzades.

### Riscos associats
- Accés no autoritzat a dades internes.
- Escalada de privilegis dins la xarxa.
- Interrupció d’operacions i dany reputacional.

### Solució
L’ús d’un **gestor de contrasenyes** permet:
- Generar contrasenyes úniques i complexes.
- Emmagatzemar-les de manera segura amb **xifratge fort**.
- Reduir la dependència de la memòria humana i les repeticions.

---

## 2. Comparativa Tècnica

| Característica | **Bitwarden (Online)** | **KeePassXC (Offline)** |
|----------------|------------------------|--------------------------|
| **Model de funcionament** | Núvol / multi-dispositiu | Escriptori / arxiu local |
| **Xifratge** | AES-256 + E2E encryption | AES-256 local |
| **Accés multiplataforma** | Sí (web, app, navegador, mòbil) | Sí (Windows, Linux, macOS) |
| **Còpia de seguretat** | Automàtica al núvol | Manual (fitxer .kdbx) |
| **Codi obert** | Sí (open source) | Sí (open source) |
| **Autenticació 2FA** | Sí | Limitada |
| **Model freemium** | Gratuït amb opcions Premium | Totalment gratuït |
| **Dependència del núvol** | Sí | No |
| **Sincronització** | Automàtica entre dispositius | Manual |
| **Administració d’equip** | Sí (Bitwarden Organizations) | No nativa |

---

## 3. Avantatges i Inconvenients

| Model | Avantatges | Inconvenients |
|--------|-------------|----------------|
| **Bitwarden (Online)** | - Sincronització automàtica<br>- Xifratge E2E<br>- Fàcil d’administrar equips<br>- Compatible amb tots els dispositius | - Requereix connexió a Internet<br>- Dependència del servidor del proveïdor |
| **KeePassXC (Offline)** | - Control total de les dades<br>- No depèn d’un núvol extern<br>- Portable (fitxer .kdbx) | - Sense sincronització automàtica<br>- Gestió manual de còpies de seguretat<br>- Pot ser menys intuïtiu per a usuaris no tècnics |

---

## 4. Recomanació

Després de l’anàlisi, **es recomana l’ús de Bitwarden** per al personal tècnic d’EverPia.  
Els motius principals són:
- **Model de seguretat robust** (xifratge E2E).
- **Facilitat d’ús i adopció** per part de l’equip.
- **Sincronització automàtica** entre dispositius corporatius.
- Possibilitat de **gestió centralitzada d’equips**.

Per a entorns crítics sense connexió a Internet (p. ex. laboratoris aïllats), KeePassXC podria considerar-se com a complement offline.

---





# Guia d’Ús: Bitwarden per a l’Equip Tècnic

## 1. Instal·lació i Configuració Inicial

1. Accediu a [https://bitwarden.com/download/](https://bitwarden.com/download/).
2. Descarregueu la versió per al vostre sistema operatiu.
3. Instal·leu l’aplicació i creeu un compte amb un **correu corporatiu**.
4. Definiu una **contrasenya mestra robusta**:
   - Mínim 14 caràcters.
   - Combinació de majúscules, minúscules, números i símbols.
5. Activeu la **verificació en dos passos (2FA)**.

📸 *Vegeu la imatge `img/bitwarden-instal·lacio.png`.*

---

## 2. Generació de Contrasenyes Segures

1. A l’aplicació, feu clic a **Generador de contrasenyes**.
2. Configureu els paràmetres:
   - Longitud: recomanat 16–20 caràcters.
   - Incloure símbols i números.
3. Copieu i deseu la contrasenya al vostre element de Bitwarden.

📸 *`img/bitwarden-generador.png`.*

---

## 3. Desar Credencials i Emplenament Automàtic

### a. Desar un compte de correu
1. Feu clic a “Afegir element”.
2. Introduïu:
   - Nom: “Compte corporatiu”.
   - Usuari: `usuari@everpia.com`
   - Contrasenya: generada prèviament.
3. Deseu l’element.

📸 *`img/bitwarden-guardar-credencial.png`.*

### b. Desar un servei web
- Bitwarden detecta automàticament els formularis de login.
- Quan accediu a un lloc nou, el navegador oferirà **“Guardar al Bitwarden”**.

### c. Emplenament automàtic
1. Instal·leu l’extensió de Bitwarden al navegador.
2. Inicieu sessió.
3. Quan entreu a un web conegut, premeu `Ctrl + Shift + L` per emplenar automàticament les dades.

📸 *`img/bitwarden-autofill.png`.*

---

## 4. Gestió de Còpies de Seguretat (Backup)

### a. Exportar dades
1. A l’aplicació d’escriptori, aneu a **Configuració → Eines → Exportar vault**.
2. Seleccioneu format `.json` o `.csv` (xifrat).
3. Deseu-lo temporalment.

### b. Emmagatzematge segur
- **Opció recomanada:** guardar la còpia en una **clau USB xifrada**.
- Alternativament, pujar-la a un **núvol xifrat** (p. ex. Tresorit o OneDrive amb BitLocker).

📸 *`img/bitwarden-backup.png`.*

---

## 5. Bones pràctiques

✅ No reutilitzeu mai contrasenyes.  
✅ No compartiu la contrasenya mestra.  
✅ Activeu sempre l’autenticació 2FA.  
✅ Manteniu el programari actualitzat.

---



