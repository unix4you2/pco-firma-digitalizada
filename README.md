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

## 🚀 Uso

1. Sube los archivos del proyecto a tu servidor web (o usa GitHub Pages).
2. Accede a la página con los parámetros `documento` y `servidor` en la URL:  https://unix4you2.github.io/pco-firma-digitalizada/?documento=XXXXXXX&servidor=https%3A%2F%2Fnombrehost.tudominio.com%2Ferp%2Fsig%2Fendpoint.php

2.a. Reemplace XXXXXXX por el documento o llave unica que necesita su sistema para guardar finalmente la captura

2.b. Asegurese de codificar su URL de endpoint antes de enviarla como parametro, Ejemplo de encodeURIComponent("https://servidor.tudominio.com/erp/sig/endpoint.php") Sería: servidor=https%3A%2F%2Fnombrehost.tudominio.com%2Ferp%2Fsig%2Fendpoint.php


## IMPORTANTE

Puede requerir que en tu endpoint encargado de almacenar la firma final agregues un  
`header("Access-Control-Allow-Origin: https://unix4you2.github.io");`

ó 

`header("Access-Control-Allow-Origin: *"); //Más inseguro`
