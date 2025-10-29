
 **Aquí podràs trobar la tasca 04 i la seva correcció.** ✅

# 🧩 **T04: Serveis de Directori - LDAP**

📂 En aquesta tasca treballarem amb **serveis de directori LDAP**, aprenent a **instal·lar, configurar i validar** un servidor OpenLDAP i la seva integració amb un client Ubuntu.

🚀 Objectiu: comprendre com funciona LDAP com a **directori centralitzat d’usuaris i grups**, i posar-lo en pràctica en un entorn virtual de proves.

🧠 Temes clau:
- Instal·lació i configuració bàsica d’OpenLDAP  
- Creació d’Unitats Organitzatives (OUs), usuaris i grups  
- Gestió amb **LDAP Account Manager (LAM)**  
- Integració d’un client Ubuntu amb autenticació LDAP  

![captura2](img/capt2.png)

---

# 📝 Sobre aquesta guia

En aquesta guia veurem el **procés complet** per instal·lar, configurar i provar un servei de directori basat en **OpenLDAP** en un entorn **GNU/Linux**.



En primer lloc, he creat una màquina nova i li he posat el nom de:  
**T04: Serveis de directori - LDAP** 🖥️  

He utilitzat la **ISO de Ubuntu**, i acte seguit he iniciat la màquina i he establert la contrasenya:  


Un cop fet això, he reiniciat la màquina i he començat a seguir els passos per dur a terme l’activitat **T04**.

Per canviar el nom del servidor de `server` a `server.innovatech25.test`, he fet:  

```bash
sudo nano /etc/hosts
````
![captura3](img/capt3.png)  ![captura4](img/capt4.png)

---

Després de canviar el nom del servidor, he **aturat la màquina** per entrar a l’apartat de **Paràmetres** i he configurat els adaptadors de xarxa 🌐.

- **Primer adaptador:** NAT (per accés a Internet i descàrrega de paquets)  
- **Segon adaptador:** Host-Only / Amfitrió (per a comunicació privada amb la màquina física)

![captura5](img/capt5.png)

---

# 🛠️ Instal·lació OpenLDAP

Per instal·lar el servei **slapd** i les utilitats **ldap-utils**, he executat la següent comanda:

```bash
sudo apt install slapd ldap-utils -y

```
![captura6](img/capt6.png)
