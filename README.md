<h1>Actividad Evaluativa: Contenedores con Docker</h1>

<h4>Realizado por: Juan David Bedoya - Amerika Esmeralda Giraldo</h4>
<h2>Objetivo General</h2>
Implementar contenedores Docker para servicios web y de base de datos, utilizando volúmenes persistentes para asegurar la conservación de la información tras la eliminación de contenedores. Se realizará lo siguiente:

1. Crear una imagen personalizada de Apache con una página web propia.

2. Usar un volumen para /usr/local/apache2/htdocs.

3. Verificar la persistencia del volumen al eliminar el contenedor.

4. Configurar MariaDB con persistencia de datos utilizando docker-compose.

5. Conectar phpMyAdmin al contenedor de MariaDB.

6. Verificar la persistencia de datos.

<h2>1. Configuración de Apache con Página Personalizada</h2>
<h3>1.1. Estructura de directorios</h3>
Creamos una carpeta para el proyecto:
<h4><img width="393" height="80" alt="image" src="https://github.com/user-attachments/assets/94cc7421-4e9e-407c-bda5-77872ed9eab9" /></h4>
Dentro de ella, creamos:
<h4><img width="452" height="110" alt="image" src="https://github.com/user-attachments/assets/2be8ba74-3ec7-4bfb-a0c5-ac7bde9bd534" /></h4>
Creamos un archivo index.html dentro de htdocs:
<h4><img width="1088" height="84" alt="image" src="https://github.com/user-attachments/assets/b9909016-7105-4331-8c90-79baca676e03" /></h4>
<h3>1.2. Creación del Dockerfile</h3>
Creamos el archivo Dockerfile:
<h4><img width="889" height="117" alt="image" src="https://github.com/user-attachments/assets/2b1f587d-c66d-4d0f-97be-ac4f1664c849" /></h4>
<h3>1.4. Construcción de la imagen</h3>
<h4><img width="1251" height="391" alt="image" src="https://github.com/user-attachments/assets/ba64ceda-6960-4a9f-904d-5142d16f23bc" /></h4>
<h3>1.5. Creación del contenedor con volumen persistente</h3>
<h4><img width="1214" height="58" alt="image" src="https://github.com/user-attachments/assets/ad0b50aa-4a24-4668-868e-9e3b711adaaf" /></h4>
<h3>1.6. Verificación del funcionamiento</h3>
<h4><img width="1272" height="728" alt="image" src="https://github.com/user-attachments/assets/dc3a0d1d-fe5a-40b9-ba4b-710eb8f5c728" /></h4>
<h3>1.7. Verificación de persistencia</h3>
Eliminamos el contenedor:
<h4><img width="497" height="98" alt="image" src="https://github.com/user-attachments/assets/13f744b4-ecc2-48c7-afc0-9429c8ff4728" /></h4>
<h4><img width="1272" height="780" alt="image" src="https://github.com/user-attachments/assets/d51ae7a7-4a7a-444e-bfa4-ba8ae7157719" /></h4>
Creamos otro contenedor:
<h4><img width="1141" height="128" alt="image" src="https://github.com/user-attachments/assets/4fc7c427-35f3-4ada-a93f-31160ea72372" /></h4>
<h4><img width="1278" height="629" alt="image" src="https://github.com/user-attachments/assets/468af742-7467-4671-b232-4e432c11605a" /></h4>

<h2>Reto Adicional: MariaDB + phpMyAdmin con Persistencia</h2>

<h3>2.1. Crear archivo docker-compose.yml</h3>
<h4><img width="504" height="85" alt="image" src="https://github.com/user-attachments/assets/66f84bdf-045b-4fb1-8cd6-786e0529e66c" /></h4>
<h4><img width="328" height="639" alt="image" src="https://github.com/user-attachments/assets/533e18f1-4de4-4744-919d-eabc194b142a" /></h4>
<h3>2.2. Levantar los contenedores</h3>
<h4><img width="1254" height="564" alt="image" src="https://github.com/user-attachments/assets/41b07b4e-108f-42b9-832c-2aeff5ca1f20" /></h4>
<h3>2.3. Acceder a phpMyAdmin</h3>
<h4><img width="1277" height="1047" alt="image" src="https://github.com/user-attachments/assets/e91b0f61-e458-47d1-bf24-46159e212de7" /></h4>
<h3>2.4. Crear una tabla y agregar datos</h3>
<h4><img width="1279" height="1084" alt="image" src="https://github.com/user-attachments/assets/64597ae5-ecc3-4f5a-a5bd-2cc323b5be97" /></h4>
<h4><img width="636" height="263" alt="image" src="https://github.com/user-attachments/assets/61db2d39-be20-4939-87d2-5083a9b10411" /></h4>
<h3>2.5. Verificar persistencia</h3>
<h4><img width="1260" height="151" alt="image" src="https://github.com/user-attachments/assets/913ec0f2-e27d-494a-9c67-6ead8a72804b" /></h4>
<h4><img width="1256" height="146" alt="image" src="https://github.com/user-attachments/assets/9cd73211-a93f-4fbe-8785-847fa9976d1a" /></h4>
<h4><img width="629" height="265" alt="image" src="https://github.com/user-attachments/assets/0d21269a-4f81-4d48-98e4-803c46fa2f57" /></h4>
Observamos que, efectivamente, los datos persisten.
