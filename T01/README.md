# T01: Gestor de contrasenyes

## Breu descripció

**Alerta!!** EverPia ha estat atacada per ciberdelinqüents. La consultora on esteu de becaris ha patit una fuita d’informació (*data breach*) i informació confidencial sobre un projecte que està en fase de desenvolupament està ara en mans de delinqüents que amenacen amb publicar-la si no es paga un rescat.

Òbviament, això ha causat una gran alarma dins la companyia i s’ha creat un comitè de crisi per gestionar la situació.  
La investigació interna ha revelat que un dels comptes tècnics va ser compromès a causa de l'ús d'una contrasenya feble o reutilitzada.

Com a resposta a aquesta crisi, la Direcció Tècnica ha emès una directriu: tot el personal tècnic ha de començar a utilitzar un gestor de contrasenyes validat per garantir l'ús de credencials úniques i robustes.  
Se us encarrega la tasca d'avaluar les opcions i crear la documentació necessària per a la formació del personal.

---

## Fase 1: Anàlisi i Justificació (Document d'Informe)

Heu de redactar un informe que justifiqui tècnicament la decisió de la Direcció i compari les opcions. Aquest informe ha d'incloure:

### Introducció i Justificació
- Explicació de per què les contrasenyes febles o reutilitzades són un risc crític per a l'empresa (atac de diccionari, credential stuffing, etc.).
- La funció crucial d'un gestor de contrasenyes per mitigar aquests riscos.

### Comparativa Tècnica

| Eina                  | Tipus               | Sincronització / Accés | Model de seguretat        | Cost / Freemium | Observacions |
|-----------------------|-------------------|----------------------|-------------------------|----------------|-------------|
| **Bitwarden**         | Online / Núvol    | Multi-dispositiu     | Xifratge end-to-end      | Sí / Freemium   | Accés des de qualsevol dispositiu, còpies al núvol |
| **KeePassX / KeePassXC** | Offline / Escriptori | Local (arxiu KDBX) | Open Source, emmagatzematge local | Gratuït | Independència del núvol, portable, dependència de la gestió manual de còpies |

### Avantatges i Inconvenients

- **Bitwarden (Online)**  
  - **Avantatges:** Accés fàcil des de múltiples dispositius, còpies automàtiques al núvol, suport per compartir contrasenyes.  
  - **Inconvenients:** Dependència del núvol, possible atac remot si el servidor és vulnerat.

- **KeePassX / KeePassXC (Offline)**  
  - **Avantatges:** Control complet sobre les dades, independent del núvol, codi obert.  
  - **Inconvenients:** Menys còmode per a múltiples dispositius, gestió manual de còpies de seguretat, aprenentatge inicial més alt.

### Recomanació
Concloure escollint l'eina més adequada per al personal tècnic i justificar l'elecció.

---

## Fase 2: Guia d'Ús Tècnica (Manual Operatiu)

Utilitzant l'eina seleccionada a la Fase 1, crear una **Guia d'Ús** per a l'Equip Tècnic amb instruccions clares i captures de pantalla.

### Contingut obligatori

1. **Instal·lació i Configuració Inicial**  
   - Descàrrega i instal·lació.  
   - Creació de la BBDD principal o compte mestre.

2. **Generació de Contrasenyes Segures**  
   - Com utilitzar el generador de contrasenyes.  
   - Paràmetres, longitud i caràcters especials.

3. **Exemples d'Ús i Emplenament Automàtic**  
   - Desar una credencial d'un compte de correu electrònic.  
   - Desar una credencial d'una aplicació o servei web.  
   - Ús de l’extensió del navegador per emplenar automàticament les dades.

4. **Gestió de Còpies de Seguretat (Backup)**  
   - Com fer còpia de seguretat de l'arxiu de contrasenyes (KDBX o exportació Bitwarden).  
   - Recomanacions de millor pràctica (clau USB xifrada o emmagatzematge xifrat al núvol).

---

## Entregables

Dins el repositori del **projecte-3**:

