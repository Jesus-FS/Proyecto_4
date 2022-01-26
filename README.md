4° Proyecto Acamica DataWarehouse

Cuarto Proyecto de la carrera Desarrollo Web Full Stack en Acamica.

Procedimiento :

## 1 - Instalación de dependencias 

⌨️ npm install

## 2 - Crear base de datos 


Importar el Archivo data_warehouse.sql desde el panel de Administracion
Recuerde Editar el archivo configuracion/configuracion.js con los datos de su entorno.

## 3 - Iniciar el servidor 

Abrir el archivo servidor.js desde VisualStudio y ejecutar en terminal :

⌨️ nodemon servidor.js

## 4 - Ya podes Utitlizar el Sistema ! 


## 5 Ingreso al Sitio

Para Ingresar Con Usuario Normal:

Usuario: Acamica , Contraseña : 123

Administrador :

Usuario: Leandrouno , Contraseña :123

## 6 ENDPOINT

localhost:3001/v1

| Metodo |       Enpoint      |           Body	        	|           Header	        	|                  Descripcion                           |
|--------|--------------------|-----------------------------|-------------------------------|--------------------------------------------------------|
|  POST  | /login             |{usuario,contraseña}		    |                   		    | Devuelve el Token del Usuario                          |
|   GET  | /usuarios          |                   		    |           {token }    		| Devuelve Informacion de todos los usuarios             |
|  POST  | /usuariosFiltro    |{id || email || usuario ||   |           {token }    		| Devuelve informacion de un Usuario 					 |
|        |                    | nombre || apellido}         |                               |                                                        |
|  POST  | /usuarios          |{ usuario, nombre, apellido, |                   		    | Crea un Usuario                                        |
|		 |					  |	email, contrasena, telefono,|                   		    |                                                        |
|		 |					  | domicilio  }          		|                   		    |					                                     |
|   PUT  | /usuarios          |{ usuario, nombre, apellido, |           {token }    		| Modifica un Usuario                   (Solo Admin)     |
|        | 				      |	email, contrasena, telefono,|                   		    |                                                        |
|		 |					  | domicilio}          		|                   		    |                                                        |
| DELETE | /usuarios          |{usuario}    				|           {token }    		| Elimina un usuario                    (Solo Admin)     |
|--------|--------------------|-----------------------------|-------------------------------|--------------------------------------------------------|
|   GET  | /contactos         |                      	    |           {token }       	    | Devuelve todos los contactos                           |
|  POST  | /contactosFiltro   | {id || email || nombre ||   |           {token }            | Devuelve el Contacto con la Busqueda Filtrada          |
|        |                    |apellido || pais || compania}|     	                        |                                                        |
|  POST  | /contactos         |{ nombre, apellido, email,   |           {token }            |                                                        |
|        |                    | telefono, pais, compania,   |                               |                                                        |
|        |                    | cargo, canal_preferido }    |                        		| Crea un Contacto                                       |
|		 |					  |                             |                   		    |                                                        |
|  PUT   | /contactos         |{ id, nombre, apellido, email|           {token }            |  Modifica un Contacto                                  |
|        |                    | telefono, pais, compania,   |                               |                                                        |
|        |                    | cargo, canal_preferido }    |                        		|                                                        |
|		 |					  |                             |                   		    |                                                        |
| DELETE | /contactos         |{ id}                        |           {token }    		| Elimina un Contacto                                    |
|--------|--------------------|-----------------------------|-------------------------------|--------------------------------------------------------|
|   GET  | /paises            |                      	    |           {token }       	    | Devuelve todos los paises                              |
|   POST | /paisesFiltro      | {nombre}              	    |           {token }       	    | Devuelve el resultado de paises Filtrado               |
|--------|--------------------|-----------------------------|-------------------------------|--------------------------------------------------------|
