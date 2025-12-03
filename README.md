# Cifrado Hill 2x2 (Web)

## Información del Alumno
- **Nombre Completo:** Leonardo Torres Tellez
- **Grupo:** 1-B
- **Materia:** Fundamentos de algebra
- **Maestro:** Pedrozo

---

## Descripción
Aplicación web que implementa el **Cifrado Hill** de tamaño 2x2:
- Encripta mensajes en pares de letras usando una matriz clave.
- Desencripta mensajes aplicando la **inversa modular** de la clave.
- Muestra la **matriz del mensaje** y permite copiar el resultado.

---

## Instrucciones de uso
1. Descarga o clona el repositorio.
2. Abre `index.html` en tu navegador.
3. Escribe un mensaje (solo se consideran A–Z; otros caracteres se filtran).
4. Ingresa la matriz clave (2x2). Debe ser invertible módulo 26.
5. Presiona **Encriptar** para obtener el cifrado.
6. Presiona **Desencriptar** para recuperar el texto.
7. Usa **Copiar resultado** para copiar al portapapeles.

---

## Matemáticas del algoritmo
- Mapeo alfabético: `A=0, B=1, ..., Z=25`.
- Agrupación en pares: si hay longitud impar, se agrega padding con `X` (23).
- Encriptación:
  

\[
  C = K \cdot P \pmod{26}
  \]


- Desencriptación:
  

\[
  P = K^{-1} \cdot C \pmod{26}
  \]


- Inversa de \(K\) (2x2) se calcula como:
  

\[
  K^{-1} = (det(K))^{-1} \cdot \begin{bmatrix} d & -b \\ -c & a \end{bmatrix} \pmod{26}
  \]


  con \(det(K) = ad - bc\) y \((det(K))^{-1}\) el inverso modular en \(\mathbb{Z}_{26}\).

Requisitos para que la clave sea válida:
- \(det(K)\) debe ser coprimo con 26 (tiene inverso). Valores típicos: 1, 3, 5, 7, 9, 11, 15, 17, 19, 21, 23, 25.

---

## Personalización y diseño
- Paleta con **azul marino** y **negro** dominantes.
- Tarjeta estilo **glass** oscuro, animaciones `fadeIn` y `fadeInUp`.
- Botones con **ripple** en el clic y sombra dinámica.
- Diseño responsive para móviles.

---

## Estructura del proyecto

