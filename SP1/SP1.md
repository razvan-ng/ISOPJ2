---
layout: custom
title: "Sprint 1: Instal·lació i Configuració Inicial – Windows"
---

# Fase 1 – Instal·lació del sistema operatiu

## Pas 1 – Crear la màquina virtual amb VirtualBox

En aquest pas creo una nova màquina virtual a VirtualBox. Li poso un nom identificatiu, selecciono el tipus **Microsoft Windows** i la versió corresponent de **Windows 11 (64-bit)**. En aquest punt encara no he iniciat la instal·lació, només deixo preparada la màquina virtual.

<img width="905" height="614" alt="image" src="https://github.com/user-attachments/assets/47d322e4-1f4f-44f3-8c30-613219ee442d" />

---

## Pas 2 – Assignar recursos (RAM mínima 4 GB, disc mínim 40 GB)

A continuació configuro els recursos mínims de la màquina virtual:
    1. **Memòria RAM: 4096 MB (4 GB)** com a mínim.
    2. **Disc dur virtual: 80 GB**.
    3. Si cal, també ajusto el nombre de processadors per millorar el rendiment.

Amb aquesta configuració, la màquina virtual queda preparada per poder instal·lar Windows correctament.

<img width="905" height="614" alt="image" src="https://github.com/user-attachments/assets/dcbc2e82-a884-4912-b2e9-ea7fc600b0aa" />
<img width="905" height="614" alt="image" src="https://github.com/user-attachments/assets/27d47452-cb7a-454f-9cd8-0c653357086a" />

---

## Pas 3 – Carregar la ISO de Windows

En aquest pas carrego la imatge ISO de Windows a la màquina virtual. Ho faig des de l’apartat d’emmagatzematge de VirtualBox, seleccionant la ISO com a unitat òptica. D’aquesta manera, quan la màquina arrenca, ho fa directament des de la imatge d’instal·lació.

<img width="1385" height="771" alt="image" src="https://github.com/user-attachments/assets/21cfb584-5d84-4134-a75b-5407ed85b691" />
<img width="1393" height="375" alt="image" src="https://github.com/user-attachments/assets/e380cb86-c623-4540-8265-ceb5e8194408" />

---

## Pas 4 – Instal·lar el sistema

Una vegada iniciada la màquina virtual, comença l’assistent d’instal·lació de Windows. Selecciono l’idioma, el format regional i la distribució del teclat. Després segueixo els passos per instal·lar el sistema al disc virtual creat anteriorment.

<img width="943" height="730" alt="image" src="https://github.com/user-attachments/assets/8928a363-b5f4-4b3e-ae54-d3bede7c57d5" />
<img width="710" height="556" alt="image" src="https://github.com/user-attachments/assets/255b87f1-c010-44ba-bda0-b8b151cf8bd6" />

En aquest pas ens demana una clau de producte, com ara no disposo de cap, faré click sobre _I don't have a product key_ per continuar amb la instal·lació.

<img width="713" height="568" alt="image" src="https://github.com/user-attachments/assets/58c648cd-5dd1-49cd-9135-68b9b50f4478" />

Sel·lecciono la versió de Windows 11 a instal·lar, en aquest cas la Pro.

<img width="709" height="549" alt="image" src="https://github.com/user-attachments/assets/d52f75b6-6441-4780-9f66-bbc797d14cf9" />

Accepto la politica d'ús de Windows,

<img width="710" height="562" alt="image" src="https://github.com/user-attachments/assets/079e5716-f10f-4cdf-bd71-c463f1116b45" />

Trio el disc virtual de 80GB que he creat abans. Aquest serà on s'instal·larà Windows. Si fem click sobre _Next_, l'instal·lador farà les particions necessàries per completar la instal·lació.

<img width="715" height="564" alt="image" src="https://github.com/user-attachments/assets/06ef9c0b-008f-427e-a86a-652455a19988" />

Quan veiguem _Ready to install_ significa que ja podem procedir a la instal·lació. Només hem de fer click sobre _Install_.

<img width="708" height="556" alt="image" src="https://github.com/user-attachments/assets/2d70d344-63b2-41d2-a42d-5b86058a51a0" />

Ara haurem d'esperar a que es completi. 

<img width="527" height="258" alt="image" src="https://github.com/user-attachments/assets/fa14ebc9-8cb5-4899-b8ad-1b22c4cd48bb" />

És possible que l'ordinador es reiniciï. Haurem d'esperar fins que veiguem l'OOBE (_Out Of Box Experience_), que és l'assistent d'instal·lació.

<img width="824" height="629" alt="image" src="https://github.com/user-attachments/assets/fb6bd310-b8bd-4af6-a268-4e1654690a2a" />

Quan hagi arrancat l'assistent primer haurem de triar la regió del sistema.

<img width="922" height="698" alt="image" src="https://github.com/user-attachments/assets/94e4c178-e123-4010-84f9-194d56b70a16" />

Després la distribució del teclat, i li diem que no volem afegir un _layout_ secundari. Si fos el cas, aqui ho podriem configurar.

<img width="952" height="685" alt="image" src="https://github.com/user-attachments/assets/8e5f4866-4df7-47d4-96a2-912811679ebe" />
<img width="962" height="704" alt="image" src="https://github.com/user-attachments/assets/d02b7989-411a-4d10-888c-fdb710a2c7c1" />

Ara ens demanarà que li posem un nom al dispositiu. És útil fer-ho quan tenim una xarxa amb més d'ún ordinador, però per ara ho ometrem.

<img width="944" height="691" alt="image" src="https://github.com/user-attachments/assets/3c549859-7610-478e-8d9d-f82cc8391cd6" />

Configurem el sistema per ús casolà.

<img width="949" height="683" alt="image" src="https://github.com/user-attachments/assets/f947c822-f434-4514-a944-5b74d9b8fb3e" />

Podria ser el cas que ho hagin actualitzacions pendents. En aquest cas hauriem d'esperar a que es completi.

<img width="857" height="630" alt="image" src="https://github.com/user-attachments/assets/ab160250-5fd8-467b-a11d-dcfc0fbbb9f8" />

Ara un cop ha acabat d'actualitzar, ens demanarà d'iniciar sessió amb el nostre compte de Microsoft. Però per fer un compte local hi ha un truc que ens permet saltar-nos aquest pas.

<img width="961" height="697" alt="image" src="https://github.com/user-attachments/assets/7dd3fab0-1ee4-46bf-9b1b-c792a48ca793" />

Fem Shift+F10 i ens surtirà el CMD. Haurem d'escriure la comanda oobe\bypassnro. Un cop fem enter se'ns reiniciarà la màquina.

<img width="1006" height="647" alt="image" src="https://github.com/user-attachments/assets/9da95ea4-82ba-4b5a-b282-237ecf2b80f9" />

Se'ns haurà reiniciat l'assistent. Haurem de seguir els mateixos passos que abans.

<img width="968" height="706" alt="image" src="https://github.com/user-attachments/assets/9abfa248-29f9-4eed-bee6-6e5c82a082b8" />

I ara ja ens deixarà crear un usuari local. Fem click sobre next.

<img width="969" height="699" alt="image" src="https://github.com/user-attachments/assets/366c55af-cabf-4919-a494-881df6f44f36" />

Després ens demanarà configurar una contrasenya.

<img width="983" height="704" alt="image" src="https://github.com/user-attachments/assets/a34da496-cd51-4fa0-bea5-0364e5fab123" />
<img width="987" height="698" alt="image" src="https://github.com/user-attachments/assets/68564e23-e1c0-424c-9d60-c600c4098577" />

I configurar una sèrie de preguntes de seguretat. Escolliim les que més ens agradin.

<img width="975" height="706" alt="image" src="https://github.com/user-attachments/assets/7f8424c4-0c2e-419a-8a4f-6bc9ec41a950" />

Ara configurem la nostra experiència d'ús. Podem configurar-ho segons les nostres preferències, però com això és una màquina de prova no és tant important.

<img width="980" height="699" alt="image" src="https://github.com/user-attachments/assets/af8b45f6-78d5-4e9f-9ef6-5c69624970d3" />
<img width="969" height="700" alt="image" src="https://github.com/user-attachments/assets/e41719a0-27ce-4335-9a8a-24ab48a821c5" />
<img width="964" height="696" alt="image" src="https://github.com/user-attachments/assets/5c3783dd-4b8d-4de3-8e75-f2d88fc4e408" />
<img width="963" height="698" alt="image" src="https://github.com/user-attachments/assets/74f63eef-a11f-46c6-89c1-55fcd94fcf68" />
<img width="990" height="688" alt="image" src="https://github.com/user-attachments/assets/542eace5-4c3d-449b-9477-ee3f06ae028a" />


---

## Pas 5 – Comprovar que arrenca correctament

* Quan la instal·lació finalitza, reinicio la màquina virtual i comprovo que Windows arrenca correctament. El sistema entra a l’escriptori sense errors i queda llest per començar la configuració posterior.

![Pas 5 – Windows arrencat correctament](imatges-windows/7.png)

---

# Fase 2 – Punts de restauració

## Pas 6 – Cercar "Crear un punt de restauració"

* Des del cercador de Windows busco l’opció **“Crear un punt de restauració”** per accedir a la configuració de protecció del sistema.

![Pas 6 – Cerca de “Crear un punt de restauració”](imatges-windows/8.png)

---

## Pas 7 – Activar la protecció del sistema al disc C:

* A la finestra de **Protecció del sistema**, selecciono el disc **C:** i activo la protecció del sistema. Aquesta opció és necessària per poder crear punts de restauració i tornar a un estat anterior del sistema si hi ha algun problema.

![Pas 7a – Protecció del sistema desactivada](imatges-windows/9.png)

![Pas 7b – Activació de la protecció del sistema al disc C:](imatges-windows/10.png)

---

## Pas 8 – Crear un punt de restauració manual

* Una vegada activada la protecció, creo manualment un punt de restauració amb una descripció identificativa. Aquest punt servirà per recuperar el sistema més endavant si es fa algun canvi no desitjat.

![Pas 8 – Creació del punt de restauració manual](imatges-windows/11.png)

---

## Pas 9 – Fer un canvi (instal·lar una app o modificar una configuració)

* Per comprovar que la restauració funciona, faig un canvi al sistema. Aquest canvi pot ser instal·lar un programa, crear un fitxer o modificar alguna configuració del sistema.

![Pas 9 – Canvi realitzat al sistema](imatges-windows/12.png)

---

## Pas 10 – Restaurar i comprovar

* Després utilitzo l’opció **Restaurar sistema** per tornar al punt de restauració que havia creat abans. Una vegada finalitzat el procés, comprovo que el sistema ha tornat a l’estat anterior i que el canvi fet ja no hi és.

![Pas 10a – Inici de la restauració del sistema](imatges-windows/13.png)

![Pas 10b – Selecció del punt de restauració](imatges-windows/14.png)

![Pas 10c – Comprovació final després de restaurar](imatges-windows/15.png)

---

# Fase 3 – Llicències de Windows

## Pas 11 – Obrir Configuració → Sistema → Activació

* En aquest pas obro **Configuració** i vaig a l’apartat **Sistema > Activació** per veure l’estat de la llicència de Windows.

![Pas 11 – Pantalla d’activació de Windows](imatges-windows/16.png)

---

## Pas 12 – Veure si Windows està activat

* En la pantalla d’activació comprovo si el sistema està activat o no. Això em permet saber si Windows té una llicència vàlida o si encara està pendent d’activació.

![Pas 12 – Estat de l’activació de Windows](imatges-windows/17.png)

---

## Pas 13 – Executar al CMD: `slmgr /xpr`

* Obro el símbol del sistema i executo la comanda `slmgr /xpr`. Aquesta comanda mostra informació sobre l’estat de l’activació i permet saber si la llicència és permanent o si el sistema es troba en mode de notificació.

![Pas 13 – Resultat de la comanda slmgr /xpr](imatges-windows/18.png)

---

## Pas 14 – Tipus de llicenciament de Windows

> **Tipus de llicències de Windows més habituals:**
>
> | Tipus | Descripció |
> |---|---|
> | **OEM** | Ve preinstal·lada amb un ordinador i normalment queda vinculada a aquell maquinari. |
> | **Retail** | És la llicència comprada per separat per l’usuari i es pot transferir a un altre equip. |
> | **Volume** | S’utilitza sobretot en empreses o centres educatius per activar molts equips. |
> | **Digital License** | Queda associada al compte de Microsoft i es reactiva automàticament. |
>
> En una màquina virtual de pràctiques és habitual que Windows no estiga activat o que aparega en mode de notificació.

---

## Pas 15 – Consultar el preu aproximat d’una llicència Windows

> **Preu aproximat d’una llicència de Windows:**
>
> | Edició | Preu aproximat |
> |---|---|
> | Windows 11 Home | al voltant de 145 € |
> | Windows 11 Pro | al voltant de 259 € |
>
> El preu pot variar segons la botiga o el tipus de llicència.

![Pas 15 – Consulta del preu de la llicència](imatges-windows/19.png)

---

# Fase 4 – Gestor d’arrencada

## Pas 16 – Obrir Command Prompt com a administrador

* Busco **cmd** al cercador de Windows i l’obro amb l’opció **Executar com a administrador** per poder consultar la configuració d’arrencada del sistema.

![Pas 16 – CMD obert com a administrador](imatges-windows/20.png)

---

## Pas 17 – Executar `bcdedit`

* Executo la comanda `bcdedit`, que mostra la informació del gestor d’arrencada de Windows i les entrades configurades al sistema.

![Pas 17 – Resultat de la comanda bcdedit](imatges-windows/21.png)

---

## Pas 18 – Identificar els blocs Boot Manager i Boot Loader

* En la sortida de `bcdedit` identifico dos blocs principals:
    - **Windows Boot Manager**
    - **Windows Boot Loader**

* Al bloc **Boot Manager** m’interessa sobretot veure el valor `default` i el valor `timeout`.

* Al bloc **Boot Loader** m’interessa identificar els camps `device`, `path` i `description`.

![Pas 18 – Línies importants de Boot Manager i Boot Loader](imatges-windows/22.png)

---

## Pas 19 – Interpretar dades concretes

> **Del bloc Boot Manager:**
>
> | Camp | Valor | Significat |
> |---|---|---|
> | `default` | `{current}` | És el sistema que arrenca per defecte |
> | `timeout` | `30` | Temps d’espera abans d’arrencar automàticament |
>
> **Del bloc Boot Loader:**
>
> | Camp | Valor | Significat |
> |---|---|---|
> | `device` | `partition=C:` | Partició on està instal·lat Windows |
> | `path` | `\Windows\system32\winload.efi` | Fitxer que carrega el sistema |
> | `description` | `Windows 11` o `Windows 10` | Nom del sistema operatiu |

---

## Pas 20 – Respostes a les preguntes curtes

> **Quin sistema s’està arrencant?**  
> → El sistema que apareix com a actual a la configuració d’arrencada.
>
> **A quina partició està instal·lat?**  
> → A la partició indicada al camp `device`.
>
> **Quant temps espera abans d’arrencar?**  
> → El temps que indica el camp `timeout`.
>
> **Quin fitxer inicia Windows?**  
> → El fitxer indicat al camp `path`, normalment `winload.efi`.

---

## Pas 21 – Interpretació final

> **Qui decideix l’arrencada (Boot Manager):**  
> El **Windows Boot Manager** és qui decideix quina entrada s’executa i quant de temps espera abans d’iniciar el sistema.
>
> **Qui carrega el sistema (Boot Loader):**  
> El **Windows Boot Loader** és el fitxer responsable de carregar realment el sistema operatiu.

---

# Fase 5 – Xarxa bàsica

## Pas 22 – Obrir la configuració de xarxa

* Obro **Configuració > Xarxa i Internet** per veure la configuració de la connexió de xarxa de la màquina virtual.

![Pas 22 – Configuració de xarxa de Windows](imatges-windows/23.png)

---

## Pas 23 – Consultar la IP amb `ipconfig`

* Obro el CMD i executo la comanda `ipconfig`. Aquesta comanda mostra la configuració IP actual, com l’adreça IPv4, la màscara de subxarxa i la porta d’enllaç.

![Pas 23 – Resultat de la comanda ipconfig](imatges-windows/24.png)

---

## Pas 24 – Configurar IP dinàmica (DHCP automàtic)

* Comprovo que la configuració de xarxa està en mode automàtic, és a dir, que la IP s’obté mitjançant **DHCP**. Això vol dir que la configuració la rep automàticament des de la xarxa.

![Pas 24 – Configuració IP automàtica amb DHCP](imatges-windows/25.png)

---

## Pas 25 – Configurar IP fixa (manual)

* Després practico la configuració manual d’una IP fixa, introduint l’adreça IP, la màscara, la porta d’enllaç i el servidor DNS de manera manual.

![Pas 25 – Configuració manual d’IP fixa](imatges-windows/26.png)

---

## Pas 26 – Comprovar la connexió amb `ping google.com`

* Finalment executo `ping google.com` per comprovar que la connexió a la xarxa funciona correctament i que hi ha connectivitat amb Internet.

![Pas 26 – Resultat del ping a google.com](imatges-windows/27.png)

---

# Fase 6 – Comandes generals

## Pas 27 – Obrir PowerShell

* Busco **Windows PowerShell** al cercador i l’obro per començar a treballar també amb aquest terminal.

![Pas 27 – PowerShell obert](imatges-windows/28.png)

---

## Pas 28 – Diferenciar CMD i PowerShell

> | Característica | CMD | PowerShell |
> |---|---|---|
> | Ús principal | Comandes bàsiques i clàssiques | Automatització i administració avançada |
> | Funcionament | Basat en text | Treballa també amb objectes |
> | Scripts | `.bat` | `.ps1` |
>
> El **CMD** és més simple i clàssic, mentre que **PowerShell** és més potent i està orientat a l’administració del sistema.

---

## Pas 29 – Comandes bàsiques

* En aquest pas provo diverses comandes bàsiques:
    - `dir` per veure fitxers i carpetes
    - `cd` per moure’m per directoris
    - `mkdir prova` per crear una carpeta
    - `echo hola > fitxer.txt` per crear un fitxer
    - `del fitxer.txt` per eliminar-lo

![Pas 29a – Comandes bàsiques executades](imatges-windows/29.png)

![Pas 29b – Comprovació del fitxer i la carpeta creats](imatges-windows/30.png)

---

## Pas 30 – Comandes útils del sistema

* També executo altres comandes útils:
    - `tasklist` per veure els processos actius
    - `taskkill /IM notepad.exe /F` per tancar un procés
    - `systeminfo` per veure informació completa del sistema
    - `hostname` per veure el nom de l’equip
    - `whoami` per veure l’usuari actual

![Pas 30a – Resultat de tasklist](imatges-windows/31.png)

![Pas 30b – Resultat de systeminfo](imatges-windows/32.png)

![Pas 30c – Resultat de hostname i whoami](imatges-windows/33.png)

---

## Pas 31 – Comandes de xarxa

* A més, provo aquestes comandes de xarxa:
    - `ipconfig`
    - `ping google.com`
    - `netstat -an`

* Aquestes ordres serveixen per veure la configuració de xarxa, comprovar la connexió i visualitzar connexions i ports oberts.

![Pas 31 – Resultat de les comandes de xarxa](imatges-windows/34.png)

---

## Pas 32 – Comandes interessants (una mica més avançades)

* Finalment provo algunes ordres addicionals:
    - `tree` per veure l’estructura de carpetes
    - `cls` per netejar la pantalla
    - `help` per veure l’ajuda de comandes
    - `shutdown /s /t 0` per apagar l’equip

* La comanda `shutdown /s /t 0` apaga immediatament la màquina, així que normalment es deixa per al final.

![Pas 32a – Resultat de tree](imatges-windows/35.png)

![Pas 32b – Resultat de help o cls](imatges-windows/36.png)

---

## Pas 33 – Mini interpretació

> **Què mostra `tasklist`?**  
> → Mostra els processos que estan actius en aquell moment.
>
> **Què mostra `ipconfig`?**  
> → Mostra la configuració de xarxa de l’equip.
>
> **Què mostra `systeminfo`?**  
> → Mostra informació general i detallada del sistema operatiu i del maquinari.

---

# Fase 7 – Instal·lació d’aplicacions

## Pas 34 – Descarregar un programa des del navegador

* Obro el navegador i descarrego un programa, com per exemple **Google Chrome** o **Visual Studio Code**, des de la seua pàgina oficial.

![Pas 34 – Descàrrega d’un programa des del navegador](imatges-windows/37.png)

---

## Pas 35 – Instal·lar-lo seguint l’assistent

* Execute l’instal·lador i segueixo els passos de l’assistent fins que la instal·lació finalitza correctament.

![Pas 35 – Procés d’instal·lació del programa](imatges-windows/38.png)

---

## Pas 36 – Obrir-lo i comprovar que funciona

* Una vegada instal·lat, obro el programa i comprovo que funciona correctament.

![Pas 36 – Programa instal·lat i obert correctament](imatges-windows/39.png)

---

## Pas 37 – Instal·lar una aplicació des de Microsoft Store

* També obro la **Microsoft Store**, busco una aplicació i la instal·lo des d’allí.

![Pas 37 – Aplicació seleccionada a Microsoft Store](imatges-windows/40.png)

---

## Pas 38 – Obrir-la i comprovar el funcionament

* Quan acaba la instal·lació, obro l’aplicació i verifico que funciona bé.

![Pas 38 – Aplicació de Microsoft Store oberta](imatges-windows/41.png)

---

## Pas 39 – Desinstal·lar una aplicació

* Des de **Configuració > Aplicacions**, busco una aplicació instal·lada i la desinstal·lo.

![Pas 39 – Desinstal·lació de l’aplicació](imatges-windows/42.png)

---

## Pas 40 – Verificació: comprovar que ja no apareix al sistema

* Finalment, comprovo que l’aplicació desinstal·lada ja no apareix al sistema i que l’eliminació s’ha fet correctament.

![Pas 40 – Verificació final de la desinstal·lació](imatges-windows/43.png)

---

# Conclusió

* Amb aquest sprint he après a instal·lar i configurar un sistema Windows dins d’una màquina virtual. També he practicat la creació de punts de restauració, la comprovació de l’activació de Windows, la interpretació del gestor d’arrencada, la configuració bàsica de la xarxa, l’ús de comandes útils i la instal·lació i desinstal·lació d’aplicacions. En general, aquesta pràctica m’ha ajudat a entendre millor l’administració inicial d’un sistema operatiu Windows.
