---
layout: custom
title: "Sprint 2: Instal·lació, Configuració de Programari de Base i Gestió de Fitxers"
---

# Fase 1 – Preparació del sistema

## Pas 1 – Afegir un nou disc virtual a la màquina virtual

<img width="1315" height="535" alt="image" src="https://github.com/user-attachments/assets/8196bcd1-3ed0-4d45-ab72-c38d803a3187" />

Sel·lecionem la màquina virtual > _Settings_ > afegir disc virtual.

<img width="790" height="557" alt="image" src="https://github.com/user-attachments/assets/a49f4b14-c800-4a43-b5f3-614c2414a03c" />

Creem un disc d'unes 40GB per poder fer dues particions de 20GB. Un cop acabem fem click sobre _Finish_.

<img width="955" height="298" alt="image" src="https://github.com/user-attachments/assets/e130c42e-dbd9-4b34-b0ab-5f59986e5f3b" />

Després sel·lecionem el disc virtual i fem click sobre _Choose_.

## Pas 2 - Iniciar Windows i obrir Gestió de discs

<img width="430" height="674" alt="image" src="https://github.com/user-attachments/assets/bbcdc182-618c-42ec-8d7c-6afd5f12ff5a" />

Fem click dret sobre l'icona de Windows i entrem a _Disk Management_.

## Pas 3. Inicialitzar el disc, crear dues particions: una anomenada Dades i una en FAT32 anomenada Portable

<img width="406" height="307" alt="image" src="https://github.com/user-attachments/assets/6b78babf-5677-4ed2-8478-12175127ef69" />

Sel·lecionem el disc i fem click sobre _OK_.

<img width="703" height="550" alt="image" src="https://github.com/user-attachments/assets/b9323cf2-2bd4-43e0-84e7-dc0664faa6b8" />

Després, fem click dret sobre el disc i clickem _New Simple Volume_.

<img width="495" height="391" alt="image" src="https://github.com/user-attachments/assets/cc17624d-4478-477f-af47-6bfabbac2da8" />

Fem _Next_ fins arribar a aquesta pantalla. Aqui farem dues particions de 20GB cadauna. Fem _Next_.

<img width="497" height="389" alt="image" src="https://github.com/user-attachments/assets/db34974b-a254-45c9-a20f-cae540ac5c11" />

Assignem la lletra E a la partició i fem click sobre _Next_.

<img width="494" height="387" alt="image" src="https://github.com/user-attachments/assets/ba9bada0-714b-4c9e-a227-571fbbebf269" />

Asignem el nom "Dades" al nou volum i fem click sobre _Next_. Finalment, fem finish.

<img width="746" height="228" alt="image" src="https://github.com/user-attachments/assets/1470fa0b-8631-43bd-975b-e80dbefbc50b" />

Ara podem veure que tenim dues particions, una creada i l'altra en espai per alocar. Anem a fer una altra partició en format FAT32 i nom "Portable". 

<img width="501" height="393" alt="image" src="https://github.com/user-attachments/assets/6358f44e-c907-4675-a29c-33c4fe3a50f5" />

Haurem de seguir els mateixos passos fins arribar a la pantalla de formatar. Triem FAT32 i l'anomenem "Portable".

<img width="695" height="116" alt="image" src="https://github.com/user-attachments/assets/07b43496-b394-4870-a6f8-1cbf9f3a0681" />

Ara podem comprovar que tenim dues particions.

<img width="786" height="312" alt="image" src="https://github.com/user-attachments/assets/162b173d-b1b5-4a8d-b338-927d2e6e7224" />

Si anem al Explorador d'Arxius podem veure les dos paricions amb lletres E i F.

## Pas 4. Assignar lletres i comprovar amb diskpart la configuració

<img width="671" height="252" alt="image" src="https://github.com/user-attachments/assets/a70e5bf0-a925-4468-8bb2-58835e8132cb" />

Obrim una consola amb administrador.

<img width="508" height="430" alt="image" src="https://github.com/user-attachments/assets/8fb499e0-0df9-48ae-8a74-697029a4b082" />

Amb les comandes "list disk" llistem els discos del sistema. Amb "sel disk X" sel·lecionem un disc segons la llista de discos anterior. Amb "list part" llistem les particions del disc sel·leccionat.

<img width="755" height="502" alt="image" src="https://github.com/user-attachments/assets/bafeca38-c428-44ef-bf63-253a04491c23" />

Per assignar una lletra a un volum primer hem d'executar _list vol_ per extreure un llistat dels volums disponibles. Després el sel·leccionem amb _sel vol x_ i finalment executem _assign letter=X_ canviant X per la lletra que volem assignar. 

---

# Fase 2 – Quotes i usuaris

## Pas 5. Activar quotes de disc a la partició Dades (NTFS).

<img width="839" height="710" alt="image" src="https://github.com/user-attachments/assets/b7c19ef5-faed-4742-af95-0ecc23b345ee" />

Entrem al explorador d'arxius > _This PC_ per veure els dispositius i discos. Després fem click dret sobre el disk Dades i anem a _Properties_.

<img width="360" height="501" alt="image" src="https://github.com/user-attachments/assets/2971b0cd-9ee0-4336-a883-24a79434faec" />

Després se'ns obrirà la pantalla de propietats. Haurem d'anar a la pestanya _Quota_ i després _Show Quota Settings_.

<img width="359" height="448" alt="image" src="https://github.com/user-attachments/assets/f11453ef-4d68-4c64-bbc5-0d70206c7699" />

Després marquem la casella _Enable quota management_.

## Pas 6. Establir límit de 300 MB per usuari, amb notificació d’advertència.

<img width="364" height="452" alt="image" src="https://github.com/user-attachments/assets/6ced7b96-44e5-4d67-aabd-d438f095bff0" />

En aquesta pestanya he configurat que el límit per usuari sigui 300MB i que l'advertència salti quan s'arriba als 200MB. D'altra banda he activat els logs per quan un usuari excedeix el límit i quan rep una advertència. A la part superior he activar l'opció _Deny disk space to users exceeding quota limit_. Aquesta funció m'ajuda a denegar més espai de disc als usuaris que ja han excedit el límit.

<img width="403" height="190" alt="image" src="https://github.com/user-attachments/assets/724c1339-3ab7-4ebd-a0b2-2d4ae161b5d1" />

Ens saltarà aquesta pantalla, haurem de fer click sobre _OK_.

<img width="360" height="449" alt="image" src="https://github.com/user-attachments/assets/6d4f151c-90b7-4105-b42c-f0eaf13b019f" />

Ara si tornem a la pantalla d'abans veurem que les quotes estan activades.

## Pas 7. Crear dos usuaris locals: alumne1 i alumne2.

<img width="370" height="106" alt="image" src="https://github.com/user-attachments/assets/d0e84ecd-69d7-48e8-88b9-eb55e5351271" />

Obrim el cmd com administrador i executem les següents comandes net user indicant l'usuari a crear. Si no especifiquem cap paràmetre després del nom d'usuari, els usuaris que crearem no tindran contrasenya assignada.

## Pas 8. Afegir-los a un grup nou anomenat Limitats.

<img width="416" height="94" alt="image" src="https://github.com/user-attachments/assets/4ddd4f69-5040-4a59-be15-d854ee081fd6" />

Creem el grup Limitats amb net localgroup des del CMD amb privilegis d'administrador.

<img width="526" height="84" alt="image" src="https://github.com/user-attachments/assets/e48bc9d2-7779-4503-a3b2-4433795fd3ad" />

Després, amb net localgroup _nomgrup_ _nomusuari_ /add, afegim els usuaris que vulguem al grup dessitjat. 

<img width="398" height="175" alt="image" src="https://github.com/user-attachments/assets/2a22d30b-3cc7-4825-ba2f-34130bf6b5cd" />

Comprovem que s'han afegit correctament mitjançant net localgroup i el nom del grup.

## Pas 9. Provar la còpia de fitxers dins Dades per veure com actuen les quotes (superar límit).

<img width="708" height="307" alt="image" src="https://github.com/user-attachments/assets/a1cc42bb-faaa-46bd-8ade-908b7c00edd3" />

He iniciat sessió amb l'usuari alumne1. Si entrem a l'explorador d'arxius veurem que el disc Dades té un espai disponible de 300MB. Tot i això, provare a guardar un fitxer més gran de 300MB.

<img width="752" height="562" alt="image" src="https://github.com/user-attachments/assets/302dbe5e-9dea-4682-bd1f-6daf8fc61c2c" />

Dins del disc, fem click dret > _Open in Terminal_.

<img width="526" height="264" alt="image" src="https://github.com/user-attachments/assets/3c0dbb6f-6e76-4059-8e5c-0fc636252e4a" />

Després se'ns obrirà un Powershell. Per entrar a cmd haurem d'executar cmd.

<img width="452" height="87" alt="image" src="https://github.com/user-attachments/assets/f444c2b8-a3a1-4e15-8f57-e541aaf2b3c2" />

L'eina fsutil ens permet generar fitxers per fer aquest tipus de proves. Si intentem generar un fitxer major a 300MB podem veure que ens salta Error 112 indicant-nos que no tenim espai suficient.

<img width="430" height="96" alt="image" src="https://github.com/user-attachments/assets/a5174439-84c3-41d4-ab9a-61dd28d40ea8" />

Però si creem un fitxer menor a 300MB, podrem fer-ho perfectament.

<img width="363" height="449" alt="image" src="https://github.com/user-attachments/assets/ed4e2ea1-0794-45d4-97e9-3ea21aea96a0" />

Ara si tornem a l'usuari administrador, a la pantalla dels ajustaments de la quota, podrem anar a veure els logs fent click a _Quota Entries_.

<img width="841" height="170" alt="image" src="https://github.com/user-attachments/assets/bfa2a935-7f6c-49c5-b168-113552bb4ea9" />

I veurem un missatge d'alerta dient-nos que l'usuari alumne1 està a punt d'esgotar la seva quota. 

<img width="428" height="141" alt="image" src="https://github.com/user-attachments/assets/84a9a827-ca8e-4b51-9d05-490f0b3b8305" />

Ara generarem fitxers per gastar tota la quota de l'usuari alumne1.

<img width="777" height="338" alt="image" src="https://github.com/user-attachments/assets/234452b5-6a2f-4c25-a4ea-1bb441e4922c" />

Si anem a l'explorador d'arxius veurem que ens queda 0 bytes disponibles.

<img width="839" height="182" alt="image" src="https://github.com/user-attachments/assets/31fffc9f-9562-4169-923e-8c30966df5e4" />

I si anem als logs de quota veurem que l'usuari alumne1 està per sobre del límit, és a dir, ha fet servir tota la seva quota.

---

# Fase 3 – Scripts de còpia i automatizació.

