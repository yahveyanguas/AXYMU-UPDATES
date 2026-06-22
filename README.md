# AXYMU-UPDATES
AXYMU version tracker (VERSION PARA USUARIO)
AXYMU — Guía de actualizaciones

Cómo funciona el sistema

Cuando un cliente abre AXYMU, el archivo hace una consulta silenciosa a GitHub.
Si la versión en GitHub es mayor que la del archivo del cliente, aparece una barra verde:
"Nueva versión X.X disponible — Descargar ahora"

El cliente hace clic y descarga la nueva versión.


Tu repositorio de control

URL: https://github.com/yahveyanguas/AXYMU-UPDATES
Archivo clave: version.json


Pasos para lanzar una actualización


Prepara el nuevo archivo AXYMU (ej: AXYMU_v9.html)
Súbelo a donde quieras que lo descarguen los clientes
(el repositorio GitHub, Gumroad, tu web, etc.)
Ve a github.com/yahveyanguas/AXYMU-UPDATES
Abre version.json → clic en el lápiz ✏️
Cambia el número de versión:
"version": "8.0"  →  "version": "9.0"
Cambia la URL de descarga:
"url": "https://..."  →  enlace directo al nuevo archivo
Commit changes
Listo — todos los clientes verán el aviso la próxima vez que abran AXYMU



Estructura del version.json

json{
  "version": "8.0",
  "url": "https://github.com/yahveyanguas/AXYMU-UPDATES",
  "notes": "Descripción breve de la versión"
}


version → número de la versión nueva (debe ser mayor que la del cliente)
url → enlace directo de descarga del nuevo archivo
notes → descripción interna, el cliente no la ve



Versiones y su número interno en AXYMU

Cada archivo AXYMU tiene esta línea en el JS:

var AXYMU_CURRENT_VERSION = '8.0';

Cuando prepares una nueva versión del archivo, recuerda cambiar ese número
para que coincida con el version.json.


Prueba rápida

Para verificar que el aviso funciona:


Cambia version.json a un número mayor (ej: 9.0)
Abre AXYMU y espera 2-3 segundos
Debe aparecer la barra verde
Vuelve a poner el número real cuando termines de probar
