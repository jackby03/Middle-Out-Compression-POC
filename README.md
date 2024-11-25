# Middle-Out Compression Algorithm (PoC)

## Descripción
Este proyecto es un **Proof of Concept (PoC)** para implementar un algoritmo de compresión inspirado en el concepto ficticio de "*middle-out compression*" (popularizado por la serie *Silicon Valley*). El objetivo es diseñar un algoritmo funcional capaz de comprimir y descomprimir archivos de forma eficiente, similar a herramientas existentes como gzip o zstd, utilizando el lenguaje **Zig**, conocido por su alto rendimiento.

## Características
- Implementación de un nuevo enfoque de compresión.
- Inspirado en la idea de procesar datos desde el centro hacia los extremos.
- Optimización basada en técnicas modernas de compresión.
- Comparación con herramientas estándar como gzip, zstd y otros.
- Desempeño sobresaliente gracias a Zig, un lenguaje de próxima generación.

## Estructura del Proyecto
```plaintext
middle-out-compression/
│
├── src/                     # Código fuente principal
│   ├── main.zig             # Punto de entrada de la aplicación
│   ├── compress.zig         # Lógica del algoritmo de compresión
│   ├── decompress.zig       # Lógica del algoritmo de descompresión
│   ├── utils.zig            # Funciones auxiliares (manejo de archivos, validaciones)
│   └── constants.zig        # Definiciones de constantes y configuraciones
│
├── tests/                   # Pruebas unitarias y de integración
│   ├── compress_tests.zig   # Pruebas para la compresión
│   ├── decompress_tests.zig # Pruebas para la descompresión
│   └── test_runner.zig      # Archivo principal para ejecutar todas las pruebas
│
├── benchmarks/              # Herramientas y scripts para medir el rendimiento
│   ├── benchmarks.zig       # Comparación con gzip, zstd, etc.
│   └── test_files/          # Archivos de prueba de diferentes tamaños y formatos
│
├── docs/                    # Documentación del proyecto
│   ├── architecture.md      # Diseño técnico del algoritmo
│   └── benchmarks.md        # Resultados y análisis de rendimiento
│
├── examples/                # Ejemplos de uso del algoritmo
│   └── simple_example.zig   # Demostración de compresión y descompresión
│
├── README.md                # Descripción general del proyecto
├── LICENSE                  # Licencia del proyecto
├── Makefile                 # Tareas de automatización (build, tests, benchmarks)
└── .gitignore               # Archivos y carpetas ignoradas por Git
```

## Requisitos
- **Zig** (versión >= 0.11)
- **CMake** (para benchmarks externos)
- Herramientas opcionales:
  - gzip
  - zstd

## Instalación
1. Clona este repositorio:
   ```bash
   git clone https://github.com/tu-usuario/middle-out-compression.git
   cd middle-out-compression
   ```
2. Asegúrate de tener Zig instalado. Si no, descárgalo de [ziglang.org](https://ziglang.org/).
3. Construye el proyecto:
   ```bash
   zig build
   ```

## Uso
### Comprimir un archivo
```bash
zig-out/bin/middle-out-compress input.txt compressed.moc
```

### Descomprimir un archivo
```bash
zig-out/bin/middle-out-decompress compressed.moc output.txt
```

## Benchmarks
Para ejecutar los benchmarks:
```bash
zig run benchmarks/benchmarks.zig
```

## Roadmap
1. **MVP (Producto Viable Mínimo):**
   - Implementar compresión y descompresión básica.
2. **Optimización:**
   - Mejorar la eficiencia del algoritmo con técnicas avanzadas.
3. **Comparación:**
   - Comparar rendimiento frente a gzip y zstd.
4. **Extensiones:**
   - Soporte para múltiples formatos de entrada (texto, binario, imágenes).

## Contribuciones
¡Contribuciones son bienvenidas! Por favor, abre un *issue* o envía un *pull request*.

## Licencia
Este proyecto está bajo la Licencia MIT. Consulta el archivo `LICENSE` para más detalles.