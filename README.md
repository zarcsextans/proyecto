## Descripción del Proyecto

Este proyecto implementa un encriptador y desencriptador utilizando el Cifrado Hill con una matriz clave de tamaño 2×2.
El sistema permite:

Encriptar un mensaje.

Generar la matriz correspondiente al mensaje.

Validar si la clave ingresada es válida.

Desencriptar el mensaje utilizando la matriz inversa módulo 26.

Visualizar todo de manera interactiva mediante una interfaz gráfica en HTML, CSS y JavaScript.

Este cifrado se basa en álgebra lineal y operaciones módulo 26, asignando un valor numérico a cada letra.

 ## Instrucciones de Uso
### 1. Abrir el proyecto

Abre el archivo:

index.html


Este cargará la aplicación completa en tu navegador.

### 2. Encriptar

Escribe un mensaje (máx. 30 caracteres).

Ingresa la matriz clave 2×2:

| a  b |
| c  d |



### 3. Haz clic en **Encriptar**.

El sistema mostrará:

- La matriz generada del mensaje.
- El texto encriptado.

---

### 4. 🔓 Desencriptar

1. Usa la misma clave.
2. Haz clic en **Desencriptar**.

El sistema:

- Calcula la matriz inversa módulo 26.
- Recupera el mensaje original si la clave es válida.
- Muestra un error si la matriz **NO es invertible**.

---

## 🧮 Matemáticas del Cifrado Hill

### 1. Representación del alfabeto  
Cada letra se convierte en un número:



A = 0
B = 1
C = 2
...
Z = 25


Se eliminan espacios, acentos y símbolos.

---

### 2. Matriz del mensaje  
El texto se agrupa en pares:

Ejemplo:

CASA → CA | SA


Luego se convierte a números:

CA → [2, 0]
SA → [18, 0]


Se forma una matriz de 2 filas.

3. Matriz clave 2×2

El usuario ingresa:

| a  b |
| c  d |


Esta matriz debe ser invertible en módulo 26.

Condición necesaria:
gcd(det(K), 26) = 1


Si no se cumple → **NO se puede desencriptar**.

---

### 4. 🔐 Encriptación

Fórmula:
C = K × M  mod 26

Donde:

- **K** = matriz clave  
- **M** = pares del mensaje  
- **C** = texto cifrado  

---

### 5. 🔍 Matriz inversa para desencriptar

Para recuperar el mensaje:


Pasos:

Determinante:

det = ad − bc


Inverso modular del determinante:

det⁻¹ mod 26


Inversa de la matriz:

K⁻¹ = det⁻¹ × |  d  -b |
                | -c   a |   mod 26


Multiplicar K⁻¹ con C.


---

## 🎨 Personalización Realizada (Frontend)

El proyecto incluye una interfaz con:

- Fondo animado multicolor estilo **neón**.
- Contenedor translúcido **glassmorphism**.
- Botones con efectos luminosos.
- Inputs y textareas con glow dinámico.
- Animaciones suaves y aspecto futurista.

Todos los estilos se encuentran en **style.css**.

---

## 📁 Archivos del Proyecto

| Archivo      | Descripción |
|--------------|-------------|
| `index.html` | Interfaz principal del sistema |
| `style.css`  | Estilos visuales con efectos neon y animaciones |
| `script.js`  | Lógica del cifrado Hill y desencriptación |
| `README.md`  | Documentación del proyecto |

---

## 🧪 Ejemplo de Funcionamiento

### Clave:

Clave:

| 3  3 |
| 2  5 |


Mensaje:

HOLA


Resultado encriptado:

LZZR


Resultado desencriptado:

HOLA

 Autor

Proyecto realizado por:
Scarlet Angelina Ruelas Cardeña