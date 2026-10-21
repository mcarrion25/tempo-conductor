# TempoConductor — prototipo web

## Qué incluye
- Interfaz móvil y pantalla de tempo a pantalla completa.
- Acceso a cámara frontal.
- Seguimiento corporal mediante MediaPipe Pose Landmarker.
- Estimación experimental del tempo a partir de inversiones del movimiento vertical de la muñeca.
- Código de colores, referencia activa, gráfico y configuración básica.
- PWA básica para poder añadirla a la pantalla de inicio.

## Importante
Este es un prototipo de viabilidad, no una versión validada para evaluar estudiantes. La detección basada en la muñeca no reconoce todavía de forma robusta la anacrusa, el ictus musical ni todos los patrones de dirección. Los filtros de doble/mitad y la confirmación de 9 pulsos son aproximaciones iniciales que deben calibrarse con vídeos reales y compararse con un metrónomo.

La primera carga necesita conexión para descargar MediaPipe y el modelo corporal. El vídeo se procesa localmente; esta página no lo graba ni lo envía a un servidor.

## Cómo probarlo
La cámara del navegador requiere HTTPS o localhost; abrir index.html con doble clic puede impedir el acceso a cámara.

Opción local:
1. Instala Python 3.
2. Abre una terminal en esta carpeta.
3. Ejecuta `python -m http.server 8000`
4. En el propio ordenador abre `http://localhost:8000`.
5. Para probar desde el móvil, publica la carpeta en un alojamiento HTTPS estático (por ejemplo, GitHub Pages o un hosting propio) o configura HTTPS local.

## Próximas mejoras recomendadas
1. Detectar la mano/batuta con un seguimiento específico, no solo la muñeca.
2. Separar detección del ictus y cambios de dirección intermedios.
3. Afinar la lógica de intervalos: el tempo debe derivarse de intervalos entre pulsos equivalentes, no de cualquier inversión de movimiento.
4. Implementar confirmación de nuevo tempo basada en nueve beats musicales válidos y estabilidad robusta.
5. Medir latencia y precisión en diferentes modelos de teléfono.
