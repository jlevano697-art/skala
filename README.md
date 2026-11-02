# Skala — publicación en Buffer

Videos de Skala ya editados y **aprobados** en el Estudio Skala, listos para que Buffer los publique como Reel.

- `cola.json`: videos aprobados con su texto, fecha y hora (hora de Lima) y estado (`pendiente`, `en_buffer`, `error`, `cancelado`).
- `publicar/`: los videos aprobados (Buffer los descarga desde aquí a la hora de publicar).
- `.github/workflows/buffer.yml`: cada hora (y al aprobar) envía a Buffer lo que toca en las próximas 72 h.

Configuración del repositorio (Settings → Secrets and variables → Actions):
- Secreto `BUFFER_API_KEY`: clave de la API de la cuenta de Buffer de Skala.
- Variable `CANALES`: IDs de canal de Buffer (separados por coma).
- Variable `MODO`: `prueba` (no publica) o `real`.

Nada se envía si no se aprobó en el estudio. Los crudos nunca se suben aquí.
