# Smartphone (teléfono para Minecraft 1.21.1)

Un teléfono estilo FiveM que aparece abajo a la derecha. Son **dos piezas**:

| Pieza | Dónde va | Qué hace |
|-------|----------|----------|
| **Plugin de Paper** (`SmartphonePlugin-1.0.0.jar`) | Carpeta `plugins` del servidor | Guarda números, mensajes, contactos, llamadas |
| **Mod de Fabric** (`smartphone-1.0.0.jar`) | Carpeta `mods` de **cada jugador** | La pantalla del teléfono, cámara y galería |

Tu servidor sigue siendo Paper y conserva todos sus plugins.

## Qué incluye
- **Mensajes**: burbujas de chat, historial completo guardado en el servidor, estados Enviado / Entregado / Leído. Si el otro está desconectado, el mensaje le espera y lo ve al entrar.
- **Número único** por jugador (formato `555-1234`). Para agregar a alguien necesitas su número.
- **Contactos (agenda)**.
- **Llamadas** con voz usando **Plasmo Voice**, con timbre, contestar, rechazar, colgar y recientes.
- **Cámara**: saca fotos (sin HUD) y se guardan en la **Galería** del teléfono (carpeta `phone_gallery`, solo en el PC del jugador).
- **Ajustes**: volumen del tono, No molestar, fondo de pantalla.

## Instalación
**Servidor (Paper 1.21.1):**
1. Pon `SmartphonePlugin-1.0.0.jar` en `plugins`.
2. Tiene que estar instalado el plugin **Plasmo Voice** (versión Paper) para que haya audio en las llamadas. Sin él, todo funciona menos el sonido de la llamada.
3. Reinicia el servidor.

**Cada jugador (cliente Fabric 1.21.1):**
1. Fabric Loader + **Fabric API**.
2. **Plasmo Voice** (versión Fabric).
3. `smartphone-1.0.0.jar` en la carpeta `mods`.

## Teclas (se pueden cambiar en Controles → Teléfono)
| Tecla | Acción |
|-------|--------|
| `M` | Abrir / cerrar el teléfono (y salir del modo cámara) |
| `Y` | Contestar llamada |
| `N` | Rechazar / colgar |
| `Enter` | Tomar foto (solo en modo cámara) |

Comando: `/phone number` te dice tu número.

## Cómo hablar en una llamada
Plasmo Voice añade una activación llamada **Teléfono**. Entra en los ajustes de Plasmo Voice
(tecla `V` por defecto) → *Activaciones* → *Teléfono* y elige cómo activarla (pulsar para hablar con una tecla,
o por voz). Lo que hables con esa activación solo lo oye la persona con quien estás en llamada.

## Compilar (GitHub Actions)
Sube el contenido de esta carpeta a un repositorio. En **Actions** se compilan solos las dos piezas
y se descargan desde **Artifacts**: `mod-fabric-para-jugadores` y `plugin-paper-para-el-servidor`.

## Datos
El servidor guarda todo en `plugins/Smartphone/smartphone.json`. Haz copia de seguridad de ese archivo.
