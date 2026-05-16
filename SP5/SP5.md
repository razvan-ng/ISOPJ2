---
layout: default
title: "Sprint 5: Monitoratge, Auditories i Programari Client/Servidor"
---

# Autorització i auditories en Windows

<img width="785" height="565" alt="image" src="https://github.com/user-attachments/assets/1d127ab0-39e1-4c00-b7e3-ae05a0042afc" />

<img width="844" height="511" alt="image" src="https://github.com/user-attachments/assets/fe94de3e-9838-4c9d-a767-c60e61532ee7" />

Obrim Directives de seguretat local i accedim a Directives locals > Directiva d’auditoria. Activem “Auditar eventos de inicio de sesión” i “Auditar el acceso a objetos” per registrar inicis de sessió i accessos a recursos del sistema.

<img width="1006" height="557" alt="image" src="https://github.com/user-attachments/assets/fcf4ef1b-e4ba-43a8-a9a4-dd83e755bd4c" />

Un cop activades les auditories, iniciem sessió amb un usuari. Si és correcte, al Visor d’esdeveniments es registrarà l’Event ID 4624, corresponent a un inici de sessió satisfactori.

<img width="779" height="624" alt="image" src="https://github.com/user-attachments/assets/7e668c2b-e24a-4870-9cee-67b98481285d" />

<img width="1023" height="828" alt="image" src="https://github.com/user-attachments/assets/266136ca-1af5-4529-b9c6-c711c75e2caa" />

<img width="1066" height="614" alt="image" src="https://github.com/user-attachments/assets/2483f779-35a6-4059-9ce3-6e322399a2b4" />

Creem una carpeta nova i configurem l’auditoria des de les seves propietats. Afegim l’usuari Razvan amb permisos de lectura perquè el sistema registri els accessos realitzats.

<img width="915" height="591" alt="image" src="https://github.com/user-attachments/assets/f48ac535-d22b-45ea-a3ab-4ce34e5347e1" />

<img width="766" height="383" alt="image" src="https://github.com/user-attachments/assets/64df3eff-77db-4e89-941f-31a42c4ca297" />

També afegim l’usuari Administrador amb control total sobre la carpeta per fer proves d’accés i modificació.

<img width="770" height="236" alt="image" src="https://github.com/user-attachments/assets/ae0aff5c-46da-4876-b8ac-d75461c2de23" />

<img width="1031" height="669" alt="image" src="https://github.com/user-attachments/assets/bb064206-2507-4724-b4cb-1ef9f357b57e" />

En crear, modificar o consultar fitxers dins la carpeta auditada, Windows registra l’Event ID 4663, que indica un accés a un objecte del sistema.

<img width="781" height="370" alt="image" src="https://github.com/user-attachments/assets/1b23bf93-c002-43e9-91ef-de732d2594ea" />

<img width="416" height="512" alt="image" src="https://github.com/user-attachments/assets/2e8bf1f6-5191-4dc8-a834-f8f0c8bd3651" />

<img width="860" height="600" alt="image" src="https://github.com/user-attachments/assets/8d273cd8-f962-4a60-ac3b-f7e2c5cec1f7" />

Activem “Auditar el seguimiento de procesos” i obrim un programa, com Paint. Aquesta acció registra l’Event ID 4688, associat a la creació d’un procés.

<img width="941" height="645" alt="image" src="https://github.com/user-attachments/assets/165f8473-1cad-4e92-8b22-a0b092d1c775" />

Si tanquem el programa des de l’Administrador de tasques, es registra l’Event ID 4689, corresponent a la finalització del procés.

<img width="1202" height="547" alt="image" src="https://github.com/user-attachments/assets/c9172498-8a2d-467f-8059-e2c0b424b4d9" />

<img width="606" height="461" alt="image" src="https://github.com/user-attachments/assets/e781b889-f108-4df9-909e-d812f6a6d759" />

<img width="325" height="322" alt="image" src="https://github.com/user-attachments/assets/fb0a94b7-304d-4c1d-89b7-107278eb9ee8" />

Habilitem l’auditoria d’Administración de cuentas i creem un usuari nou. Aquesta acció registra els esdeveniments 4720 (creació del compte) i 4722 (activació del compte).

<img width="660" height="239" alt="image" src="https://github.com/user-attachments/assets/298df60c-8a27-4e69-ae3f-22dc4b0fcc2e" />

Si desactivem l’usuari, Windows registra l’Event ID 4725, corresponent a la desactivació del compte.

<img width="484" height="200" alt="image" src="https://github.com/user-attachments/assets/81bd881b-db6f-4e6e-bd13-d5fb07df9fcd" />

<img width="876" height="522" alt="image" src="https://github.com/user-attachments/assets/ea6295be-e0a5-4f6f-b47f-780fea2e09c6" />

Finalment, eliminem l’usuari creat. Aquesta acció registra l’Event ID 4726, corresponent a l’eliminació d’un compte d’usuari.
