# Changelog

Todos los cambios notables en este proyecto serán documentados en este archivo.

El formato se basa en [Keep a Changelog](https://keepachangelog.com/es-ES/1.0.0/),
y este proyecto se adhiere al [Versionado Semántico](https://semver.org/lang/es/).

## [1.2.0] - 2025-09-18

### ✨ Añadido
- **Información de llave** Se presenta la información de la llave o documento recibido como parámetro en la parte superior
- **Cambio de pincel** Se aumenta el grosor del pincel para hacer más consistente la firma al redimensionar

## [1.2.0] - 2025-09-18

### ✨ Añadido
- **Canvas maximizado** que ocupa 85-90% de la altura de pantalla y 95% del ancho
- **Cálculo dinámico del tamaño** del canvas basado en dimensiones de viewport
- **Redimensionado automático** del canvas al cambiar el tamaño de ventana
- **Layout optimizado** con header ultra compacto de solo 40px de altura
- **Área de controles comprimida** a máximo 100px en la parte inferior

### 🔄 Cambiado  
- **Estructura del layout** reorganizada para priorizar el área de dibujo
- **Vista previa reducida** a 150x50px para ahorrar espacio vertical
- **Posicionamiento de controles** agrupados horizontalmente en la parte inferior
- **Título y documento** mostrados en la misma línea para minimizar espacio

### 🛠️ Mejorado
- **Experiencia de firma** especialmente en tablets y pantallas grandes
- **Aprovechamiento del espacio** disponible en pantalla al máximo
- **Responsive design** mejorado para diferentes tamaños de dispositivos
- **Usabilidad general** con más área disponible para dibujo

---

## [1.1.0] - 2025-09-18

### ✨ Añadido
- **Modo claro moderno** con esquema de colores profesional
- **Interfaz compacta** optimizada para eficiencia de espacio
- **Tipografía system-ui** para apariencia nativa en cada sistema operativo
- **Vista previa integrada** de 200x66px al lado de los controles
- **Transiciones suaves** en botones y efectos hover

### 🔄 Cambiado
- **Tamaño del canvas** reducido al 70% para mejor balance visual
- **Header minimalista** con altura máxima de 60px
- **Botones más compactos** con padding reducido pero manteniendo usabilidad
- **Colores actualizados** a paleta moderna (azul #007bff, verde #28a745, rojo #dc3545)

### 🛠️ Mejorado
- **Diseño visual general** con esquinas redondeadas y sombras sutiles
- **Organización de controles** en una sola fila horizontal
- **Espaciado consistente** usando sistema de 8px/16px
- **Legibilidad** con mejores contrastes y jerarquía tipográfica

### 🎨 Estilo
- **Fondo principal** cambiado a blanco puro (#ffffff)
- **Superficie secundaria** en gris muy claro (#f8f9fa)  
- **Bordes sutiles** en gris claro (#e9ecef)
- **Elementos con profundidad** mediante sombras discretas

---

## [1.0.0] - 2025-09-18

### ✨ Añadido - Versión inicial
- **Canvas de firma digital** con soporte completo para mouse y touch
- **Parámetros de URL** configurables (`documento` y `servidor`)
- **Procesamiento inteligente** de imagen con detección de bounding box
- **Redimensionado automático** a 250×83 píxeles manteniendo proporciones
- **Tres botones principales**:
  - `Finalizar Firma`: Procesa y muestra vista previa
  - `Guardar Firma`: Envía al servidor especificado  
  - `Limpiar`: Reinicia el canvas para nueva firma
- **Envío automático** via POST con FormData (userfile + documento)
- **Validación de parámetros** con mensajes de error informativos
- **Conversión a JPG** con calidad optimizada
- **Vista previa** de 250×83px para verificación visual
- **Soporte responsive** para desktop, tablets y móviles
- **Manejo de errores** con mensajes de estado al usuario

### 🏗️ Arquitectura
- **Clase JavaScript** modular (`SignatureApp`) para mejor organización
- **Canvas HTML5** como base del sistema de dibujo  
- **CSS moderno** con custom properties y diseño responsive
- **API FormData** para envío eficiente de archivos
- **Event listeners** optimizados para mouse y touch events

### 🎨 Diseño
- **Interfaz limpia** con elementos bien organizados
- **Canvas con bordes** y fondo blanco para mejor visibilidad
- **Botones con estados** (normal, hover, disabled)
- **Tipografía legible** con jerarquía clara
- **Layout responsive** que se adapta a diferentes pantallas

### 🔧 Funcionalidades técnicas
- **Detección automática** de límites reales de la firma
- **Eliminación de espacios** en blanco innecesarios  
- **Líneas suaves** con requestAnimationFrame para mejor rendimiento
- **Grosor de línea** optimizado (3-4px) para firmas naturales
- **Algoritmo de redimensionado** que preserva exactamente las proporciones
- **Validación de entrada** antes de permitir acciones
- **Manejo de estados** de la aplicación (limpio, firmado, procesado)

---

## Tipos de cambios

- **✨ Añadido** para nuevas funcionalidades
- **🔄 Cambiado** para cambios en funcionalidades existentes  
- **🗑️ Deprecado** para funcionalidades que serán eliminadas pronto
- **🚫 Eliminado** para funcionalidades eliminadas ahora
- **🛠️ Mejorado** para corrección de errores
- **🔒 Seguridad** en caso de vulnerabilidades
