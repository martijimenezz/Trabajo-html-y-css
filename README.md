# Planeta Juguete

## Estructura

### Tecnologías:
- HTML5
- CSS
- Visual Studio Code con extensiones:
  - Live Preview
  - Plottier
- ChatGPT para la generación de imágenes y aclaraciones
- Google para la multimedia, fuentes y visualización de la página

### Características:
- **Colores principales**: #67ee72 y green.
- **Enlaces** que dirigen a las otras páginas de la web con hovers y actives.
- **Imagen parallax** en la página index.

### División de tareas
- **Juan**: index y formularios
- **Martí**: artículos e info

### Fotos
![Index](imagenesREADME/ImagenREADME1png.png)
![Index iphoneSE](imagenesREADME/ImagenREADME2.png)
![Articulos](imagenesREADME/ImagenREADME3.png)
![Articulos iphoneSE](imagenesREADME/ImagenREADME4.png)
![Info](imagenesREADME/ImagenREADME5.png)
![Info iphoneSE](imagenesREADME/ImagenREADME6.png)

#### Formularios

![Formulario de registro para el club de la web.](imagenesREADME/ImagenREADME7.png)
![Formulario para contactar con el personal de la web para informar problemas, hacer propuestas, etc.](imagenesREADME/ImagenREADME8.png)

### Expresiones regulares para la validación
# Expresiones Regulares para la Validación

## 1. Validar un campo que solo contiene letras
**Regex**: `^[a-zA-ZáéíóúÁÉÍÓÚñÑ\s]{3,}$`

Valida un campo que solo puede contener:
- Letras (mayúsculas y minúsculas).
- Acentos (`áéíóúÁÉÍÓÚ`).
- La letra `ñ` (tanto en mayúscula como minúscula).
- Espacios.
- Al menos 3 caracteres.

### Desglose:
- `^`: Inicia la validación desde el inicio de la cadena.
- `[a-zA-ZáéíóúÁÉÍÓÚñÑ\s]`: Define los caracteres permitidos:
  - `a-zA-Z`: Letras minúsculas y mayúsculas.
  - `áéíóúÁÉÍÓÚ`: Letras con acentos.
  - `ñÑ`: La letra "ñ" (minúscula y mayúscula).
  - `\s`: Espacios en blanco.
- `{3,}`: Especifica que debe tener al menos 3 caracteres.
- `$`: Indica el final de la cadena, asegurando que toda la entrada sea válida.

---

## 2. Validar un correo electrónico
**Regex**: `^[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,}$`

Valida un correo electrónico con el formato estándar.

### Desglose:
- `^`: Inicia la validación desde el inicio de la cadena.
- `[a-zA-Z0-9._%+-]+`: Define lo que puede aparecer antes del símbolo `@`:
  - `a-zA-Z0-9`: Letras y números.
  - `._%+-`: Caracteres adicionales permitidos (puntos, guiones, etc.).
  - `+`: Indica al menos un carácter permitido.
- `@`: El símbolo obligatorio `@` separa la parte local del dominio.
- `[a-zA-Z0-9.-]+`: Define la parte del dominio:
  - `a-zA-Z0-9`: Letras y números.
  - `.-`: Puntos y guiones.
- `\.`: El punto que separa el dominio del TLD.
- `[a-zA-Z]{2,}`: Define que el TLD debe tener al menos 2 letras.
- `$`: Termina la validación al final de la cadena.

---

## 3. Validar una contraseña
**Regex**: `^(?=.*[A-Za-z])(?=.*\d)(?=.*[@$!%*?&])[A-Za-z\d@$!%*?&]{8,}$`

Valida una contraseña que debe cumplir con:
- Al menos una letra (mayúscula o minúscula).
- Al menos un número.
- Al menos un carácter especial de los siguientes: `@$!%*?&`.
- Al menos 8 caracteres en total.

### Desglose:
- `^`: Inicia la validación desde el inicio de la cadena.
- `(?=.*[A-Za-z])`: Asegura que contenga al menos una letra.
- `(?=.*\d)`: Asegura que contenga al menos un número (`\d` es equivalente a `[0-9]`).
- `(?=.*[@$!%*?&])`: Asegura que contenga al menos un carácter especial.
- `[A-Za-z\d@$!%*?&]{8,}`: Permite letras, números y caracteres especiales, con un mínimo de 8 caracteres.
- `$`: Termina la validación al final de la cadena.
