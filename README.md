# Calculadora Visual de Redes IPv6

## Descripción
Esta es una herramienta web moderna para visualizar y manipular divisiones de una red IPv6. A diferencia de las calculadoras IPv4 tradicionales, esta herramienta utiliza `BigInt` de JavaScript para manejar la inmensa escala de direcciones de 128 bits con precisión matemática exacta.

Permite calcular subredes, dividir una red en dos mitades (split) y unir subredes adyacentes (join), mostrando para cada subred la dirección de red en notación CIDR y el rango de direcciones.

## Características Principales
- **Soporte IPv6 Nativo**: Utiliza `BigInt` para cálculos de 128 bits, superando el límite de enteros seguros de JavaScript ($2^{53}$).
- **Interfaz Moderna**: Construida con Tailwind CSS (CDN) para un diseño limpio, responsive y adaptable a modo oscuro.
- **Visualización de Árbol**: Representación jerárquica de las divisiones de red.
- **Operaciones Interactivas**:
  - **Dividir**: Separa una red en dos subredes (/n+1).
  - **Unir**: Combina dos subredes adyacentes en su red padre.
- **Persistencia**: Genera enlaces permanentes que guardan el estado exacto de las divisiones en la URL.
- **Exportación**: Permite copiar la tabla de resultados al portapapeles en formato CSV compatible con Excel/Sheets.

## Uso
1. Abrir `index.html` en un navegador moderno.
2. Introducir una dirección IPv6 (ej. `2001:db8::`) y el prefijo (ej. `32`).
3. Pulsar **Calcular**.
4. Usar los botones de **Dividir** en la tabla para segmentar la red.
5. Usar las barras laterales verdes de **Unir** para recombinar subredes.
6. Utilizar el **Link Persistente** para guardar o compartir el diseño de red actual.

## Detalles Técnicos
- **Motor Matemático**: Implementación personalizada de aritmética de 128 bits usando `BigInt`.
  - `ipv6ToBigInt()`: Convierte cadenas hexadecimales comprimidas a enteros.
  - `bigIntToIPv6()`: Convierte enteros a notación hexadecimal estándar con compresión de ceros (`::`).
- **Estructura de Datos**: Árbol binario recursivo para gestionar el estado de las divisiones (`rootSubnet`).
- **Sin Dependencias de Build**: Funciona directamente en el navegador sin necesidad de Node.js, Webpack o compiladores.

## Créditos
Desarrollado por **Ernesto Pineda B.** (2025).
Basado en el concepto de la calculadora visual IPv4 original.
