# TempoConductor — prototipo web v2

## Corrección de detección
La versión anterior contaba los dos cambios de dirección verticales de cada ciclo, lo que podía estimar aproximadamente el doble del tempo real. Esta versión cuenta solo un tipo de extremo vertical por ciclo.

## Incluye
- Acceso a cámara frontal y seguimiento corporal mediante MediaPipe Pose Landmarker.
- Estimación experimental de BPM.
- Pantalla de tempo a pantalla completa con fondos de color y número gigante.
- Gráfico de evolución y referencia de tempo.
- PWA básica.

## Limitaciones importantes
Sigue siendo un prototipo de viabilidad, no una herramienta validada. El seguimiento de muñeca no reconoce de forma robusta el ictus musical, la anacrusa ni todos los patrones de dirección. La estimación debe contrastarse con un metrónomo y probarse con movimientos reales. El vídeo se procesa localmente; la primera carga descarga el modelo desde internet.

## Prueba
La cámara requiere HTTPS o localhost. Puedes usar `python -m http.server 8000` en un ordenador para probar localmente. Para usarlo desde el móvil, publícalo en un alojamiento HTTPS estático.
