# ![](https://github.com/unix4you2/practico/raw/master/img/logo.png) Firma digitalizada

Este es un proyecto derivado de [Práctico Framework](https://www.practico.org) articulable como plugin o complemento

Pruébalo en línea directamente en [Este enlace](https://unix4you2.github.io/pco-firma-digitalizada/). Si se requiere implementación directa desde otro sistema revise la sección de "Uso" más adelante.

Una herramienta web simple, ligera y moderna que permite a los usuarios o sistemas capturar su firma manuscrita (mediante ratón, touchpad o tableta digitalizadora) en un lienzo HTML5 Canvas, redimensionarla automáticamente a las dimensiones estándar de 250x83 píxeles conservando proporciones, y enviarla como archivo JPG a un endpoint de servidor especificado.

Ideal para integrarse en flujos de trabajo de documentos digitales, formularios web o sistemas ERP que requieran captura de firmas.

---

## ✨ Características

- ✍️ **Lienzo de firma intuitivo**: ocupa casi toda la pantalla para máxima comodidad.
- 📏 **Redimensionado automático**: ajusta la firma a 250x83 px manteniendo la proporción original.
- 🖼️ **Formato JPG**: la firma se envía comprimida en formato estándar.
- 🔄 **Botones de control**: Finalizar, Guardar y Limpiar para una experiencia fluida.
- 🌐 **Totalmente responsive**: funciona en escritorio, tablet y móvil.
- 🔒 **Seguridad CORS**: el endpoint PHP puede configurarse para aceptar solo peticiones desde tu dominio.
- ⚡ **Sin dependencias**: puro HTML, CSS y JavaScript vanilla.

---

## Requisitos

- Navegador con soporte HTML5, JavaScript y canvas.
- No requiere servidor — aplicación 100% client-side.
- Conexión a internet (a menos que se haga un despliegue en red local)

---

## 🚀 Uso

1. Sube los archivos del proyecto a tu servidor web (o usa GitHub Pages).
2. Accede a la página con los parámetros `documento` y `servidor` en la URL:  https://unix4you2.github.io/pco-firma-digitalizada/?documento=XXXXXXX&servidor=https%3A%2F%2Fnombrehost.tudominio.com%2Ferp%2Fsig%2Fendpoint.php

2.a. Reemplace XXXXXXX por el documento o llave unica que necesita su sistema para guardar finalmente la captura

2.b. Asegurese de codificar su URL de endpoint antes de enviarla como parametro, Ejemplo de encodeURIComponent("https://servidor.tudominio.com/erp/sig/endpoint.php") Sería: servidor=https%3A%2F%2Fnombrehost.tudominio.com%2Ferp%2Fsig%2Fendpoint.php


## IMPORTANTE

Puede requerir que en tu endpoint encargado de almacenar la firma final agregues un  
`header("Access-Control-Allow-Origin: https://unix4you2.github.io");`  ó  `header("Access-Control-Allow-Origin: *"); //Más inseguro`

Así pues, a manera de ejemplu su endpoint podría ser algo como:

``
header("Access-Control-Allow-Origin: https://unix4you2.github.io"); //Posible * en lugar del dominio, aunque mas inseguro
if (move_uploaded_file($_FILES['userfile']['tmp_name'], "archivo.jpg"))
  echo "[OK] Archivo almacenado en el servidor";
else
  echo "[ERROR] En archivo (origen/destino)";
``

## Contribuciones

Las contribuciones son bienvenidas. Para contribuir:

- Hacer fork del proyecto.
- Crear una rama nueva para tus cambios.
- Enviar pull requests con descripciones claras.
- Reportar issues y bugs en el repositorio.

## Licencia

Ver archivo LICENSE para detalles.

---

#### Soporte y donaciones al proyecto

Si encuentra útil este proyecto y deseas contribuir al desarrollo del mismo puede apoyarnos con un valor voluntario.

💵 Usando GitHub Sponsors para tus [Donaciones](https://github.com/sponsors/unix4you2/)
