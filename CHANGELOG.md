# Registro de Cambios

Todos los cambios notables en este proyecto serán documentados en este archivo.

El formato se basa en [Keep a Changelog](https://keepachangelog.com/es-ES/1.0.0/),
y este proyecto adhiere a [Semantic Versioning](https://semver.org/lang/es/).

## [1.1.0] - 2025-12-04
### Añadido
- **Calculadora EUI-64**: Herramienta para calcular direcciones IPv6 SLAAC a partir de una dirección MAC y un prefijo.
- **Generador de PTR**: Botón para copiar al portapapeles el registro DNS inverso (`.ip6.arpa`) de una subred.
- **Clasificación de Direcciones**: Etiquetas visuales para identificar tipos de direcciones (Global, Link-Local, ULA, Multicast).
- **Visualización Expandida**: Opción para alternar entre formato comprimido (`::`) y expandido (todos los ceros) de las direcciones IPv6.

## [1.0.0] - 2025-12-04
### Añadido
- Lanzamiento inicial de la Calculadora Visual IPv6.
- Implementación de lógica matemática con `BigInt` para soporte de 128 bits.
- Interfaz de usuario basada en Tailwind CSS con soporte para modo oscuro.
- Funcionalidad de división (Split) y unión (Join) de subredes.
- Generación de enlaces permanentes (Permalinks) con estado en URL.
- Exportación de tabla a formato CSV.
- Validación de direcciones IPv6 y corrección automática de direcciones de red.
