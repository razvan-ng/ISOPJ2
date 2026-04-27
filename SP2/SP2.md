---
layout: default
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

## Pas 10. Afegir tercer disc virtual, formatar-lo en NTFS com a Backups.

<img width="859" height="525" alt="image" src="https://github.com/user-attachments/assets/775b9065-566f-4eba-b14d-d279d99b9fca" />

Amb la màquina apagada, anem les configuracions de la màquina virtual > _Storage_ i afegim un nou disc virtual.

<img width="964" height="584" alt="image" src="https://github.com/user-attachments/assets/c2a17f52-a4fc-42da-8bcf-d26d41156107" />

Crearem un disc de 20GB.

<img width="948" height="284" alt="image" src="https://github.com/user-attachments/assets/1dcbb297-0202-41cd-833c-2a7ac6623cb0" />

I després el triem.

<img width="758" height="596" alt="image" src="https://github.com/user-attachments/assets/2d1692c8-35ab-4d6b-b95c-06d43c1d515c" />

Anem al administrador de discos i inicialitzem el disc.

<img width="663" height="352" alt="image" src="https://github.com/user-attachments/assets/48218d6c-18bc-4d65-8eb2-0d0e4dea98a3" />

Després fem click dret > _New Simple Volume_. Crearem la partició igual que com hem fet en passos anteriors.

<img width="490" height="390" alt="image" src="https://github.com/user-attachments/assets/c9956fd5-5314-4704-b1c4-833bbd1395ae" />

Ens assegurem de donar els paràmetres correctes.

## Pas 11. Crear carpeta CòpiesUsuaris dins Backups.

<img width="777" height="372" alt="image" src="https://github.com/user-attachments/assets/76538f52-14a3-46bb-80c4-3d09cbcc5d55" />

<img width="637" height="115" alt="image" src="https://github.com/user-attachments/assets/e3fe12fa-6037-4ea0-88d6-5d3c788a52d9" />

Anem a l'explorador d'arxius i creem la carpeta.

## Pas 12. Crear un script .bat que copiï C:\Users\%USERNAME% a E:\CòpiesUsuaris\%USERNAME%.

<img width="480" height="399" alt="image" src="https://github.com/user-attachments/assets/527ff7d5-a510-409d-8ae5-63e40dc9b54b" />

Fem click dret i creem un nou document de text.

<img width="146" height="140" alt="image" src="https://github.com/user-attachments/assets/26d383ec-fa36-4382-9570-1568c3c1e421" />

Li posem el nom que vulguem i canviem l'extensió txt per bat.

<img width="345" height="402" alt="image" src="https://github.com/user-attachments/assets/7f7e397c-df62-473a-9d4d-c1e3fad16efa" />

Després de crear el fitxer fem click dret a sobre seu i l'editem amb Bloc de Notes.

<img width="677" height="187" alt="image" src="https://github.com/user-attachments/assets/64b90cd6-abea-4b44-bd2f-843de6c1feda" />

Per fer el que se'ns demana podem fer-ho amb el codi següent. Aquest .bat crea (si no existeix) la carpeta de destí a E:\CòpiesUsuaris\%USERNAME% i copia tota la carpeta de l’usuari (C:\Users\%USERNAME%) cap allí. Inclou subcarpetes i fitxers ocults, no demana confirmacions i continua encara que hi hagi errors. Al final es queda obert per veure el resultat.

## Pas 13. Obre gpedit.msc → Configuració d’usuari → Scripts → Inici de sessió

<img width="764" height="252" alt="image" src="https://github.com/user-attachments/assets/822d5c4f-1b5c-4152-90c5-3e8f59f735e1" />

Busquem al calaix d'aplicacions _gedit.msc_ i l'obrim.

<img width="758" height="529" alt="image" src="https://github.com/user-attachments/assets/2b0bd55c-6174-4f65-840f-7148dc48dd47" />

Després entrem a l'apartat on configurarem els scripts al moment del logon.

<img width="808" height="628" alt="image" src="https://github.com/user-attachments/assets/abcab3d3-f254-48fa-83d6-a98df1796068" />

Després configurem el script perque s'iniciï al moment de l'inici de sessió.

<img width="399" height="458" alt="image" src="https://github.com/user-attachments/assets/8fb8ef2a-8819-4820-8ee5-f5fd6812286f" />

Apliquem els canvis i surtim.

# Fase 4 – Verificació i documentació

## Pas 15. Inicia sessió amb alumne1, comprova que l’script fa la còpia a Backups i que la quota de Dades bloqueja si supera el límit, així com comprovacions que tot el que has configurat funciona correctament

<img width="779" height="202" alt="image" src="https://github.com/user-attachments/assets/c36f25fb-746b-40e2-8d9c-c89901517df7" />

Entrem amb l'usuari i podem veure que tenim la carpeta creada.

<img width="766" height="567" alt="image" src="https://github.com/user-attachments/assets/c50f05c3-45b2-40d2-a7b3-6cd2ba43c5cb" />

I si entrem a la carpeta veurem el contingut de la carpeta del nostre usuari.

# Fase 5 – Gestió de processos i serveis

## Pas 19. Llistar processos actius

<img width="848" height="820" alt="image" src="https://github.com/user-attachments/assets/43b2f58a-6b85-4d58-9af5-73c6800a4a31" />

Si entrem amb l'usuari _alumne1_ i executem la comanda _tasklist_ veurem una llista amb tots els processos en segon plà.

<img width="652" height="189" alt="image" src="https://github.com/user-attachments/assets/b039b0a2-5d2c-4ba4-a5fb-1e116e327142" />

També podem fer un dump de la informació de tasklist a un fitxer txt.

<img width="642" height="893" alt="image" src="https://github.com/user-attachments/assets/a09a31eb-58a0-415f-aa02-96b557c25da4" />

Un cop ha acabat podem entrar a l'arxiu i buscar processos, per exemple, el explorer.exe.

## Pas 20. Identificar processos prescindibles

<img width="692" height="822" alt="image" src="https://github.com/user-attachments/assets/cdb7e193-ce65-4082-90cb-a9f1e175ab08" />

Amb el mateix document generat anteriorment, podem buscar processos com _OneDrive_.

| Nom del procés | Memòria usada | Justificació per eliminar-lo |
|---|---:|---|
| OneDrive.exe | 133,984 K | No és un procés essencial per al funcionament bàsic de l’usuari. Si no s’estan sincronitzant fitxers amb OneDrive, es pot tancar per alliberar memòria. |

## Pas 21. Eliminar processos manualment

<img width="676" height="97" alt="image" src="https://github.com/user-attachments/assets/b0de79a9-d193-439d-9b13-7fde3514e89e" />

Amb la consola, podem matar el procés de OneDrive amb taskkill /IM (nom procés) /F.

<img width="823" height="902" alt="image" src="https://github.com/user-attachments/assets/a7503616-a240-4d9e-92dc-bf819d74198c" />

Ara podrem veure que el procés ja no està actiu.

## Pas 22. Automatitzar-ho a l’inici de sessió

<img width="603" height="427" alt="image" src="https://github.com/user-attachments/assets/8bc643eb-995a-4921-b4a6-659d4a12a8e2" />

Modifiquem el script principal per automatitzar l'eliminació de processos al iniciar el sistema.

<img width="651" height="243" alt="image" src="https://github.com/user-attachments/assets/cdbdfed5-75f8-471f-94e9-60fc0efdac5d" />

Afegim aquestes dues linies al final per matar els processos de Teams i OneDrive al iniciar sessió.

<img width="815" height="907" alt="image" src="https://github.com/user-attachments/assets/b17f5ea1-78aa-4618-9aae-d63e9d4e68d2" />

Si executem tasklist amb l'usuari alumne2 veurem que no tenim ni OneDrive executant-se ni Teams.

## Pas 23. Documentació

## Què passa si mates `explorer.exe`

Si es tanca `explorer.exe`, desapareixen l’escriptori i la barra de tasques. El sistema continua encès, però la interfície queda incompleta. Es pot recuperar tornant a executar `explorer.exe` des del Gestor de tasques.

<img width="895" height="881" alt="image" src="https://github.com/user-attachments/assets/6361a65d-49f3-4f6d-b429-26b66b234fe4" />

## Millora del rendiment

Tancar processos no essencials ajuda a alliberar memòria i pot fer que una màquina virtual o un equip amb pocs recursos vagi més fluid. Això millora la resposta general del sistema i redueix la càrrega innecessària.

# Fase 6 – Gestió de permisos (ACLs)

## Pas 24. Crear la carpeta

<img width="443" height="168" alt="image" src="https://github.com/user-attachments/assets/6eea0834-def1-4801-a7de-0df9d52e9583" />

## Pas 25. Assignar permisos normals al grup

<img width="788" height="395" alt="image" src="https://github.com/user-attachments/assets/3b302a2f-1398-4ea9-ba0c-53e57ca70f7f" />

Entrarem a les propietats de la carpeta.

<img width="360" height="489" alt="image" src="https://github.com/user-attachments/assets/f49dc33a-990c-434e-aba8-fec362995830" />

Després entrem a la pestanya de _Security_.

<img width="866" height="901" alt="image" src="https://github.com/user-attachments/assets/fd198bb0-9d7d-4847-af62-25df0f4caa66" />

A _Advanced_ > _Change permissions_ podrem desactivar l'herència i conservar els permissos existents.

<img width="755" height="440" alt="image" src="https://github.com/user-attachments/assets/903fb82d-c7e5-4836-a3ed-727fac5f5330" />

Haurem de borrar el grup Users.

<img width="873" height="927" alt="image" src="https://github.com/user-attachments/assets/42fe479e-aaad-495e-8996-29880fa53994" />

Afegirem el grup Limitats. Escriurem "Limitats" i després farem click a _Check Names_. Un cop estigui tot correcte farem click sobre Ok.

<img width="890" height="594" alt="image" src="https://github.com/user-attachments/assets/a07507d3-53c1-4e6d-b762-550e05be81b5" />

Finalment donarem control total i aplicarem els canvis.

## Pas 26. Comprovar accés amb alumne1.

<img width="784" height="359" alt="image" src="https://github.com/user-attachments/assets/a8e440f1-102d-4331-b474-edc0f7b45489" />

<img width="783" height="372" alt="image" src="https://github.com/user-attachments/assets/81521896-cf1f-4fb8-8bdc-00d9e9b08a48" />

Un cop iniciem sessió podem crear un fitxer de text amb contingut dins. Veurem que el podem crear i eliminar.

## Pas 27. Aplicar excepció per alumne2

<img width="508" height="99" alt="image" src="https://github.com/user-attachments/assets/84dba28c-3e21-4985-a55f-fc72116e4652" />

Això substitueix qualsevol permís anterior d’alumne2 i li dona només lectura.

## Pas 28. Comprovar l'excepció amb alumne2

<img width="779" height="444" alt="image" src="https://github.com/user-attachments/assets/7afaeedb-94b1-428c-8edf-65b6cf2b907d" />

Si iniciem sessió amb alumne2 veurem que podrem llegir l'arxiu.

<img width="786" height="473" alt="image" src="https://github.com/user-attachments/assets/f5770e67-6194-47bd-b6ff-19246df4880c" />

Si per exemple intentem eliminar l'arxiu veurem que no podrem fer-ho i ens demanarà permissos d'administrador.

## Pas 29. Consultar els permisos aplicats

<img width="512" height="181" alt="image" src="https://github.com/user-attachments/assets/684a267b-abf6-4f0d-bdcc-8c89dfe78d68" />

Ara podrem comprovar que el grup té control total però l'usuari només pot llegir.
