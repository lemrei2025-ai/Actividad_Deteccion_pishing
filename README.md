# Actividad 2 — Detecta al Impostor: Ingeniería Social y Phishing sin Riesgos

Taller introductorio de ciberseguridad — **Especialización en Seguridad Informática**, módulo *Ciberespacio y Seguridad Digital* (basado en la Sesión 1, Fundación Universitaria Los Libertadores).

> Nivel: **introductorio**. No requiere conocimientos previos de hacking ni programación.
> En ningún momento se crea, envía o reenvía un mensaje engañoso a otra persona, ni se hace clic en un enlace real de phishing. Ver [Reglas de la actividad](#reglas-de-esta-actividad).

## Índice

- [Objetivo de aprendizaje](#objetivo-de-aprendizaje)
- [Recordatorio conceptual](#recordatorio-conceptual)
- [Resultados de aprendizaje](#resultados-de-aprendizaje)
- [Materiales y herramientas](#materiales-y-herramientas)
- [Reglas de esta actividad](#reglas-de-esta-actividad)
- [Desarrollo paso a paso](#desarrollo-paso-a-paso)
  - [Fase 1 — Análisis guiado de mensajes](#fase-1--análisis-guiado-de-mensajes)
  - [Fase 2 — Verificación segura de enlaces](#fase-2--verificación-segura-de-enlaces)
  - [Fase 3 — Verificación de dominio en Kali Linux](#fase-3--verificación-de-dominio-en-kali-linux)
  - [Fase 4 — Puesta en común y concientización](#fase-4--puesta-en-común-y-concientización)
- [Entregable](#entregable)
- [Rúbrica de evaluación](#rúbrica-de-evaluación-100-puntos)
- [Licencia](#licencia)

## Objetivo de aprendizaje

Reconocer, mediante el análisis de mensajes reales y herramientas simples de verificación, las técnicas de ingeniería social y phishing vistas en la sesión, sin necesidad de crear ni enviar ningún mensaje engañoso a otra persona.

## Recordatorio conceptual

La ingeniería social no ataca la tecnología, sino la confianza, la prisa y el miedo de las personas; el phishing es su forma más común. Esta actividad convierte la checklist **"Detecta al Impostor"** en un método de trabajo, basado en cuatro señales: el **remitente**, el **saludo genérico**, el **tono de urgencia** y el **enlace sospechoso**.

## Resultados de aprendizaje

- Clasificar mensajes (correo, SMS, WhatsApp) como legítimos o como intentos de phishing, aplicando una checklist estructurada.
- Verificar de forma segura un enlace sospechoso sin necesidad de abrirlo, usando un analizador en línea.
- Usar, de forma guiada, `whois` y `nslookup` en Kali Linux para revisar la antigüedad y el registro de un dominio sospechoso.
- Diseñar una pieza breve de concientización dirigida a un público cercano.

## Materiales y herramientas

| Herramienta | Uso |
|---|---|
| Banco de mensajes de ejemplo | 4 a 6 capturas de correos, SMS o WhatsApp (legítimos y de phishing), entregadas por el docente |
| [VirusTotal](https://www.virustotal.com) | Analiza una URL o archivo sospechoso sin necesidad de abrirlo |
| Máquina Kali Linux (de la Actividad 1) | Solo para los comandos `whois` y `nslookup`, ambos de consulta pública |
| Checklist "Detecta al Impostor" | Remitente, saludo genérico, urgencia, enlace sospechoso |

## Reglas de esta actividad

> En ningún momento se crea, se envía ni se reenvía un mensaje engañoso a otra persona, ni se hace clic en un enlace real de phishing. El trabajo es de **analista**: observar mensajes ya existentes (proporcionados por el docente) y verificar enlaces o dominios copiando el texto, nunca haciendo clic directamente sobre ellos.

## Desarrollo paso a paso

### Fase 1 — Análisis guiado de mensajes

1. En grupos pequeños, recibir del docente entre 4 y 6 mensajes de ejemplo.
2. Construir una tabla con las columnas: `N.°`, `Remitente`, `Tipo de saludo`, `¿Urgencia/amenaza?`, `Aspecto del enlace/contacto`, `Clasificación`.
3. Para cada mensaje:
   - Revisar y anotar el **remitente** (correo, número o cuenta).
   - Clasificar el **saludo** como genérico ("Estimado cliente") o personalizado (tu nombre completo).
   - Marcar sí/no si hay **urgencia o amenaza** ("actúe ahora", "su cuenta será bloqueada").
   - Describir el **enlace o contacto** sin hacer clic: dominio oficial conocido, acortador (bit.ly, tinyurl) o número desconocido.
   - Clasificar como **legítimo** o **phishing/sospechoso**, con al menos dos señales que sustenten la decisión.
4. Repetir para todos los mensajes entregados.

### Fase 2 — Verificación segura de enlaces

1. De los mensajes sospechosos, copiar el texto del enlace **sin hacer clic** (clic derecho → Copiar, o `Ctrl+C`).
2. Ir a [https://www.virustotal.com](https://www.virustotal.com)
3. Clic en la pestaña **URL**.
4. Pegar el enlace (`Ctrl+V`) y presionar Enter o clic en el ícono de lupa.
5. Esperar el análisis y leer el resultado (por ejemplo, `3/90` = motores que lo marcaron malicioso).
6. Registrar el resultado y una captura de pantalla en la tabla de análisis.
7. Repetir para cada enlace sospechoso.

### Fase 3 — Verificación de dominio en Kali Linux

Se usa la misma máquina Kali configurada en la **Actividad 1**. Abrir una terminal (`Ctrl + Alt + T`).

```bash
# Identificar solo el dominio, por ejemplo de
# http://banco-colombia.seguridad.co/clientes -> banco-colombia.seguridad.co

whois <dominio_del_enlace_sospechoso>
```

Ubicar el campo `Creation Date`: un dominio registrado hace pocos días o semanas es una señal de alerta adicional.

```bash
nslookup <dominio_del_enlace_sospechoso>
```

Anotar la IP obtenida y comparar el dominio con el oficial conocido de la entidad (escrito directamente en el navegador, nunca a través del enlace sospechoso).

### Fase 4 — Puesta en común y concientización

1. Cada grupo presenta uno de sus casos: qué señales encontró y cómo lo verificó.
2. Diseñar una pieza breve de concientización (infografía de una página, carrusel de 3–4 imágenes, o guion de video corto) dirigida a un público cercano, con:
   - Al menos **tres señales de alerta**.
   - Al menos **tres recomendaciones de defensa** (verificar por otro canal, activar 2FA, no dejarse presionar por la urgencia).

## Entregable

- Tabla de análisis de los mensajes con clasificación y señales identificadas (ver [plantilla](./plantillas/tabla-analisis-mensajes.md)).
- Capturas de VirusTotal y de los comandos `whois`/`nslookup` ejecutados.
- Pieza de concientización final, lista para compartir con un público real fuera del curso (ver [plantilla](./plantillas/plan-concientizacion.md)).

## Rúbrica de evaluación (100 puntos)

| Criterio | Descripción | Ponderación |
|---|---|---|
| Análisis de mensajes | Aplicación correcta y justificada de la checklist | 30% |
| Verificación de enlaces | Uso correcto de VirusTotal e interpretación adecuada | 25% |
| Verificación de dominio | Ejecución correcta de whois/nslookup y lectura de la fecha de registro | 20% |
| Pieza de concientización | Claridad, precisión y utilidad para un público no técnico | 25% |

## Licencia

Este material educativo se distribuye bajo licencia [Creative Commons Atribución-CompartirIgual 4.0 Internacional (CC BY-SA 4.0)](https://creativecommons.org/licenses/by-sa/4.0/deed.es). Puedes usarlo, adaptarlo y compartirlo dando el crédito correspondiente.
