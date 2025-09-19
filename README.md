# pco-firma-digitalizada

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
2. Accede a la página con los parámetros `documento` y `servidor` en la URL:


## IMPORTANTE

Puede requerir que en tu endpoint encargado de almacenar la firma final agregues un  
`header("Access-Control-Allow-Origin: https://unix4you2.github.io");`

ó 

`header("Access-Control-Allow-Origin: *"); //Más inseguro`
