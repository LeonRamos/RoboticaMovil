# Cinemática en Robótica Móvil

## 1. Introducción a la Cinemática
La **cinemática** estudia el movimiento de los cuerpos sin considerar las fuerzas que lo generan. En robótica móvil, la cinemática se encarga de describir cómo un robot se desplaza en el espacio a partir de los movimientos de sus partes.

## 2. Tipos de Cinemática
- **Cinemática Directa (Forward Kinematics):** Dada una configuración de las articulaciones o ruedas del robot, se calcula su posición y orientación en el espacio.
- **Cinemática Inversa (Inverse Kinematics):** Dada una posición y orientación deseadas del robot, se calculan las configuraciones de sus articulaciones o ruedas necesarias para alcanzar dicha posición.

## 3. Modelos Cinemáticos
- **Robot de Diferencia de Velocidad (Differential Drive):** Un tipo común de robot móvil con dos ruedas impulsadas por motores independientes. La cinemática de este modelo se describe mediante la velocidad de cada rueda.
  - Ecuaciones de movimiento:
    \[
    v = \frac{r}{2}(\omega_R + \omega_L)
    \]
    \[
    \omega = \frac{r}{L}(\omega_R - \omega_L)
    \]
    Donde \( v \) es la velocidad lineal, \( \omega \) es la velocidad angular, \( r \) es el radio de la rueda, \( L \) es la distancia entre las ruedas, y \( \omega_R, \omega_L \) son las velocidades angulares de las ruedas derecha e izquierda, respectivamente.
- **Robot Holonómico (Omnidireccional):** Un robot con ruedas que pueden moverse en cualquier dirección sin necesidad de cambiar su orientación.

## 4. Transformaciones de Coordenadas
Para describir el movimiento de los robots en el espacio, utilizamos **matrices de transformación** para cambiar de un sistema de coordenadas a otro.
- **Transformación homogénea (2D):**
  \[
  T = \begin{bmatrix}
  \cos(\theta) & -\sin(\theta) & x \\
  \sin(\theta) & \cos(\theta) & y \\
  0 & 0 & 1
  \end{bmatrix}
  \]
  Donde \( \theta \) es el ángulo de rotación y \( x, y \) son las coordenadas de traslación.

## 5. Práctica
- **Ejercicio 1:** Implementar un simulador de un robot diferencial utilizando Python. Los estudiantes deben programar las ecuaciones de movimiento y observar cómo el robot cambia de posición y orientación en función de las velocidades de las ruedas.
- **Ejercicio 2:** Resolver la cinemática inversa de un robot móvil para alcanzar una posición específica en un entorno 2D.

## 6. Aplicaciones
- **Robots Aspiradores (e.g., Roomba):** Utilizan cinemática diferencial para moverse por el hogar y cubrir el área completa mediante trayectorias predefinidas.
- **Drones:** Aunque su cinemática incluye una tercera dimensión (altitud), las bases de la cinemática móvil 2D son cruciales para el control de sus desplazamientos horizontales.

## 7. Recursos Adicionales
- [Documento de referencia sobre cinemática móvil](https://link-to-reference.com)
- [Simulador en línea de robots móviles](https://link-to-simulator.com)
