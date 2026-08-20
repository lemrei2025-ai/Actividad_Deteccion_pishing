# Banco de mensajes de ejemplo — Actividad 2

> **Advertencia de uso:** todos los mensajes de este banco son **ficticios**, creados únicamente con fines educativos para esta actividad. "Banco Andino", "ColEnvíos" y "MegaTienda" no son entidades reales; cualquier parecido es intencional solo como recurso pedagógico para representar patrones típicos (bancos, transportadoras, comercios). Ningún enlace de este documento es funcional ni debe considerarse seguro para hacer clic fuera del ejercicio: en la actividad **solo se copia el texto**, nunca se abre directamente.
>
> Este archivo es para uso del **estudiante**. La clasificación correcta de cada mensaje (legítimo o phishing) y las señales que la sustentan están en la guía del docente: [`docente/guia-respuestas-banco-mensajes.md`](../docente/guia-respuestas-banco-mensajes.md). No la revises antes de completar tu análisis.

## Cómo usar este banco

1. Trabaja los 6 mensajes en el orden en que aparecen.
2. Por cada mensaje, regístralo en la fila correspondiente de la [tabla de análisis](./tabla-analisis-mensajes.md) (N.° 1 a 6).
3. Para los mensajes que contengan un enlace o dominio, **no hagas clic**: cópialo y utilízalo en las fases 2 (VirusTotal) y 3 (`whois`/`nslookup`) de la guía principal.
4. Al final, contrasta tu clasificación con la puesta en común del docente.

---

## Mensaje N.° 1 — Correo electrónico

| Campo | Valor |
|---|---|
| Canal | Correo electrónico |
| De | `Banco Andino <soporte@banco-andino-verificacion.com>` |
| Fecha | 18/08/2026, 7:03 a. m. |
| Asunto | ⚠️ Su cuenta será BLOQUEADA en 24 horas |

> Estimado cliente,
>
> Hemos detectado actividad inusual en su cuenta. Por su seguridad, **su cuenta será suspendida en las próximas 24 horas** si no verifica su información de inmediato.
>
> Haga clic en el siguiente enlace para confirmar sus datos y evitar el bloqueo:
>
> 👉 `http://bit.ly/verificaBA-2026`
>
> Actúe ahora. Su tranquilidad es nuestra prioridad.
>
> Atentamente,
> Departamento de Seguridad
> Banco Andino

---

## Mensaje N.° 2 — SMS

| Campo | Valor |
|---|---|
| Canal | SMS |
| De | `ColEnvios` (remitente alfanumérico) |
| Fecha | 19/08/2026, 11:47 a. m. |

> ColEnvios: Su paquete #CE-88213 esta retenido en aduana por datos incompletos. Actualice su direccion y pague $4.900 de arancel aqui: colenvios-tracking.info/pago para evitar devolucion. Vence hoy.

---

## Mensaje N.° 3 — WhatsApp

| Campo | Valor |
|---|---|
| Canal | WhatsApp |
| De | Contacto guardado como "MegaTienda Ofertas", número +57 320 XXX XX21 |
| Fecha | 19/08/2026, 3:15 p. m. |

> ¡Felicidades! 🎉 Tu número fue seleccionado entre miles de participantes y ganaste un bono de **$500.000** en MegaTienda. Para reclamar tu premio antes de que expire (quedan 2 horas), completa tus datos aquí: `megatienda-premios.net/reclamo`
>
> Comparte este mensaje con 5 contactos para validar tu premio. ¡No dejes pasar esta oportunidad única! 🛍️

---

## Mensaje N.° 4 — Correo electrónico

| Campo | Valor |
|---|---|
| Canal | Correo electrónico |
| De | `Coordinación Académica <coordinacion.especializaciones@unilibertadores.edu.co>` |
| Fecha | 17/08/2026, 4:30 p. m. |
| Asunto | Cambio de aula — Sesión del sábado 23 de agosto |

> Estimado(a) [Nombre del estudiante],
>
> Le informamos que la sesión presencial del sábado 23 de agosto del módulo *Ciberespacio y Seguridad Digital* se realizará en el **aula 305, Bloque B**, y no en el aula habitual, debido a mantenimiento programado.
>
> Si tiene alguna inquietud, puede responder a este mismo correo o comunicarse con la Coordinación de Especializaciones en el horario de atención habitual.
>
> Cordialmente,
> Coordinación de Especializaciones
> Fundación Universitaria Los Libertadores

---

## Mensaje N.° 5 — SMS

| Campo | Valor |
|---|---|
| Canal | SMS |
| De | `BancoAndino` (remitente alfanumérico) |
| Fecha | 19/08/2026, 6:42 p. m. |

> BancoAndino: Compra aprobada por $85.000 en ALMACEN EXITO con tarjeta terminada en 4821, el 19/08/2026 a las 18:42. Si no reconoce esta transaccion, comuniquese al 01-8000-XXX-XXX o desde la app oficial.

---

## Mensaje N.° 6 — WhatsApp

| Campo | Valor |
|---|---|
| Canal | WhatsApp |
| De | Número desconocido, +57 300 XXX XX07 (no está en la lista de contactos) |
| Fecha | 20/08/2026, 9:10 a. m. |

> Hola papá/mamá, este es mi nuevo número, perdí mi celular 📱. Estoy en una emergencia y necesito que me ayudes a hacer una transferencia urgente de $350.000 para resolver algo importante, te explico luego, ahorita no puedo hablar por llamada. ¿Me puedes hacer el favor ya? Te paso el número de cuenta apenas confirmes.

---

**Recuerda:** ningún mensaje de este banco debe reenviarse, copiarse a un chat real ni utilizarse fuera de este ejercicio. El objetivo es analizar, no reproducir.
