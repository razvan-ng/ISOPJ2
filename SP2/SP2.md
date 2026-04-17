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

---
