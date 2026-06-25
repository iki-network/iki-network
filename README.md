# IKI Network

![Status](https://img.shields.io/badge/status-Fase%20Alfa-orange)
![License](https://img.shields.io/badge/license-MIT-blue)
![Made in](https://img.shields.io/badge/hecho%20en-México%20🇲🇽-green)

**Infraestructura de cómputo distribuido para Latinoamérica.**

IKI Network es un protocolo construido para que ningún sitio web
o aplicación en la región dependa de un solo servidor, ni de una
sola empresa extranjera.

📄 Whitepaper completo: [WHITEPAPER.md](./WHITEPAPER.md)
🌐 Sitio web: [iki.network](https://iki.network)
💬 Comunidad: [Discord](https://discord.gg/DnC5kw6cZ)

---

## El problema

La infraestructura digital de Latinoamérica no es latinoamericana.

Cada negocio, desarrollador o startup de la región que contrata
hosting o cómputo en la nube termina dependiendo de un único
proveedor centralizado, casi siempre fuera del continente. Esto
significa puntos únicos de falla, fricciones de facturación
internacional, y cero control real sobre dónde vive la
infraestructura que sostiene su propio negocio.

## La solución

IKI distribuye sitios web y aplicaciones entre una red de nodos
independientes en lugar de un único servidor centralizado. Si un
nodo falla, los demás mantienen el servicio funcionando, sin
interrupciones.

El protocolo conecta dos tipos de participantes:

- **Clientes** — despliegan sus proyectos sobre la infraestructura
  distribuida, pagando en la moneda de su país o en dólares, según
  les convenga.
- **Nodos** — aportan capacidad de cómputo a la red y reciben
  compensación directa por su contribución, sin tokens ni
  mecanismos especulativos.

Lee el [Whitepaper completo](./WHITEPAPER.md) para el detalle
técnico completo y el modelo de incentivos.

## Arquitectura

```
Cliente → Protocolo IKI → fragmenta y distribuye
              │
    ┌─────────┼─────────┐
    ▼         ▼         ▼
 Nodo 1     Nodo 2     Nodo 3
(Fragmento A)(Fragmento B)(Fragmento C)
```

Si un nodo cae, los demás conservan los fragmentos necesarios
para mantener el servicio activo. La resiliencia no depende de
una sola máquina, depende de la red completa.

## Estado actual del proyecto

**Fase Alfa.** Estamos construyendo y validando el protocolo con
un conjunto inicial de nodos propios, antes de abrir el ingreso
de nodos externos a la red.

Este repositorio documenta el progreso real del proyecto:
decisiones de arquitectura, avances de desarrollo, y la evolución
del Whitepaper. Nada de lo que ves aquí es una promesa vacía —
es exactamente lo que existe hoy, etiquetado como lo que es.

## Cómo participar

**¿Tienes una computadora o servidor disponible?**
Únete al programa de Founding Nodes a través de nuestro
[Discord](https://discord.gg/DnC5kw6cZ). Los primeros en integrarse aseguran prioridad de
compensación y una tarifa de comisión congelada de por vida.

**¿Eres developer o agencia que necesita hosting?**
Regístrate en la lista de espera en [iki.network](https://iki.network).

**¿Quieres seguir el desarrollo de cerca?**
Activa las notificaciones de este repositorio (Watch arriba a la
derecha) y revisa la pestaña de [Issues](../../issues) para ver
en qué estamos trabajando ahora mismo.


## Contribuir

Este proyecto está en etapa temprana de desarrollo. Lee
[CONTRIBUTING.md](./CONTRIBUTING.md) para conocer las formas
actuales de involucrarte, incluso antes de que el código sea
público.

## Licencia

Este proyecto se distribuye bajo la licencia MIT. Ver
[LICENSE](./LICENSE) para más detalle.

---

*Construido desde Tuxtla Gutiérrez, Chiapas, México.
Esto recién empieza.*
