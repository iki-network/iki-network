# IKI Network — Whitepaper

**Versión 1.0 — Junio 2026**
**Tuxtla Gutiérrez, Chiapas, México**

---

## Resumen

La infraestructura digital de Latinoamérica depende, casi en su
totalidad, de servidores y plataformas controladas por un puñado
de empresas extranjeras. Esta dependencia introduce puntos únicos
de falla en servicios críticos, impone fricciones de facturación
internacional sobre economías que operan en monedas locales, y
deja a desarrolladores y negocios de la región sin control real
sobre dónde y cómo viven sus datos.

IKI Network es un protocolo de infraestructura de cómputo
distribuido diseñado para resolver este problema desde su origen
geográfico: Latinoamérica. En lugar de depender de un único
centro de datos, IKI fragmenta y distribuye sitios web y
aplicaciones entre una red de nodos independientes, eliminando
puntos únicos de falla y permitiendo que la infraestructura crezca
de forma orgánica, impulsada por quienes participan en la red, no
por una corporación centralizada.

El protocolo está diseñado para dos tipos de participantes:
quienes proveen capacidad de cómputo ociosa a la red (Nodos),
recibiendo compensación a medida que la red genera ingresos, y
quienes utilizan esa infraestructura para alojar sus proyectos
(Clientes), pagando en la moneda de su país o en dólares, según lo
que mejor les convenga, sin las fricciones de la facturación
internacional tradicional.

IKI Network nace en Chiapas, México, y se construye con la
convicción de que la próxima generación de infraestructura de
internet en Latinoamérica debe ser construida por y para la
región, no importada desde fuera de ella.

---

## 1. El Problema

**La infraestructura digital de Latinoamérica no es
latinoamericana.**

Cada vez que un negocio en México, Colombia, Argentina o
cualquier país de la región contrata hosting, dominio o servicios
en la nube, depende por completo de las decisiones de un
proveedor centralizado, casi siempre fuera del continente: su
forma de pago, sus políticas de servicio, y la ubicación física
de los datos quedan fuera del control de quien realmente los usa.

### Dos fallas estructurales

**1. Puntos únicos de falla**

El modelo dominante de hosting centraliza cada sitio o aplicación
en un único servidor o, en el mejor de los casos, en la
infraestructura de un único proveedor. Cuando ese servidor falla,
o cuando el proveedor decide suspender una cuenta por cualquier
motivo administrativo, el servicio se detiene por completo. No
existe redundancia real distribuida entre partes independientes.

**2. Ausencia de soberanía regional de datos**

Los datos de negocios, gobiernos y ciudadanos latinoamericanos se
almacenan, en su gran mayoría, en centros de datos fuera de la
región. Esto plantea preguntas no resueltas sobre jurisdicción
legal, latencia para usuarios locales, y control real sobre la
información que circula dentro de la economía digital de cada
país.

### El resultado

Latinoamérica construye sobre cimientos que no controla. Cada
nueva aplicación, cada nuevo negocio digital, cada nueva startup
de la región, se levanta sobre infraestructura ajena, sujeta a
decisiones, precios y políticas que se definen fuera de ella.

---

## 2. La Solución: IKI Network

**IKI Network es un protocolo de infraestructura de cómputo
distribuido que permite alojar sitios web y aplicaciones en una
red de nodos independientes, en lugar de un único servidor
centralizado.**

### Cómo resuelve cada falla estructural

**Frente a los puntos únicos de falla**

Cuando un sitio o aplicación se despliega en IKI Network, su
contenido se fragmenta y se distribuye entre múltiples nodos
independientes. Si uno de esos nodos deja de estar disponible,
los demás continúan sirviendo el contenido sin interrupción. La
red, en su conjunto, es más resiliente que cualquiera de sus
partes individuales.

**Frente a la soberanía regional de datos**

Al estar compuesta por nodos físicamente ubicados en
Latinoamérica, la red mantiene los datos dentro de la región,
reduce la latencia para usuarios, y devuelve a la región
el control sobre la infraestructura que sostiene su propia
economía digital.

### Un beneficio adicional: flexibilidad de pago

Más allá de resolver las fallas estructurales anteriores, IKI
permite a clientes y nodos operar en la moneda de su país o en
dólares, según lo que mejor les convenga. A medida que la red
crece por Latinoamérica, el modelo de pago se adapta a las
condiciones de cada mercado, ofreciendo una opción real en lugar
de un único esquema impuesto.

### Los dos lados del protocolo

| Proveedores de Nodo | Clientes |
|---|---|
| Aportan capacidad de cómputo y almacenamiento a la red | Despliegan sitios web y aplicaciones sobre la infraestructura distribuida |
| Reciben compensación proporcional a su contribución a medida que la red opera | Pagan en la moneda de su país o en dólares, según les convenga |

Cualquier persona u organización con una computadora conectada a
internet puede convertirse en un nodo. Cualquier desarrollador,
agencia o negocio que necesite alojar un proyecto puede
convertirse en cliente. IKI Network no posee la infraestructura:
la orquesta.

---

## 3. Arquitectura Técnica

> Esta sección describe el funcionamiento del protocolo a nivel
> conceptual. IKI Network se encuentra en desarrollo activo; los
> detalles de implementación evolucionan junto con la red.

### El ciclo de vida de un despliegue

**Paso 1 — Empaquetado**

Cuando un cliente despliega un proyecto en IKI, su aplicación se
empaqueta como un contenedor estándar (compatible con Docker),
preservando el stack tecnológico original sin requerir
modificaciones al código.

**Paso 2 — Fragmentación**

El contenido del proyecto se divide en fragmentos cifrados.
Ningún nodo individual almacena el proyecto completo, lo que
significa que ningún nodo aislado puede reconstruir o exponer el
contenido por sí solo.

**Paso 3 — Distribución**

Los fragmentos se distribuyen entre múltiples nodos independientes
de la red, seleccionados según disponibilidad, capacidad y
ubicación geográfica. El número de copias distribuidas
(redundancia) determina cuántos nodos pueden fallar
simultáneamente sin afectar la disponibilidad del proyecto.

**Paso 4 — Orquestación**

Una capa de orquestación mantiene el registro de qué nodos
almacenan qué fragmentos, y dirige las solicitudes entrantes hacia
los nodos disponibles más cercanos o con mejor rendimiento en ese
momento.

**Paso 5 — Recuperación ante fallos**

Si un nodo deja de responder, la capa de orquestación redirige
automáticamente las solicitudes a los nodos restantes que
conservan los fragmentos necesarios, y puede iniciar la
redistribución de esos fragmentos hacia nuevos nodos para
restaurar el nivel de redundancia original.

### Tipos de nodo

| Micro Nodo | Nodo Compartido | Nodo Dedicado |
|---|---|---|
| Ideal para proyectos de prueba y bajo tráfico | Ideal para proyectos de tráfico moderado, compartiendo recursos con otros despliegues | Ideal para aplicaciones con requisitos de rendimiento constantes |

### Estado actual del desarrollo

El protocolo de fragmentación y distribución se encuentra en fase
de implementación. La red opera actualmente con un conjunto
inicial de nodos propios mientras se valida el mecanismo de
orquestación, antes de abrir el ingreso de nodos externos a la
red.

---

## 4. Modelo de Incentivos

IKI Network funciona como un mercado de dos lados: quienes
aportan capacidad de cómputo, y quienes la utilizan. El protocolo
está diseñado para que ambos lados se beneficien directamente del
crecimiento de la red.

### Para los Proveedores de Nodo

Quien aporta capacidad de cómputo a la red recibe
compensación proporcional a su contribución, calculada según el
espacio, el ancho de banda y el tiempo de disponibilidad que
aporta.

A diferencia de otros protocolos de la industria que dependen de
tokens y mecanismos cripto, IKI opera con un modelo de
compensación directa: pago en la moneda que mejor se adapte a
cada mercado de Latinoamérica, sin especulación ni volatilidad de
criptomonedas.

**Programa Founding Nodes**

Durante la Fase Alfa, IKI Network invita a un número limitado de
participantes a unirse como Founding Nodes. Quienes se incorporen
en esta etapa reciben:

- Prioridad de compensación sobre nodos que se incorporen en
  etapas posteriores, una vez que la red comience a generar
  ingresos por clientes activos.
- Una tarifa de comisión congelada de por vida, preferencial
  frente a la comisión estándar que aplicará a nodos futuros.
- Reconocimiento permanente como parte fundadora de la red,
  visible públicamente dentro de la plataforma y la comunidad.
- Acceso preferente a futuras herramientas y beneficios que se
  habiliten conforme el protocolo madure.

### Para los Clientes

Quien despliega un proyecto en IKI Network paga por el uso de
recursos de cómputo y almacenamiento, según lo que mejor convenga a su operación, sin las
fricciones de facturación internacional propias de los
proveedores tradicionales.

**Clientes Fundadores**

Los clientes que se incorporen durante la Fase Alfa aseguran una
tarifa congelada, que no incrementará a medida que la red escale,
como reconocimiento por la confianza depositada en una etapa
temprana del proyecto.

### Sostenibilidad del protocolo

IKI Network retiene una porción de cada transacción para
financiar el desarrollo continuo del protocolo, el mantenimiento
de la capa de orquestación, y el soporte directo a proveedores de
nodo y clientes. Esta porción se define con el objetivo de
mantenerse muy por debajo de los márgenes que aplican los
proveedores de infraestructura centralizados tradicionales.

---

## 5. Roadmap

El desarrollo de IKI Network avanza en fases, cada una construida
sobre la validación de la anterior.

### Fase Alfa — En curso

- Validación de la arquitectura de fragmentación y distribución
  con un conjunto inicial de nodos propios.
- Apertura del programa de Founding Nodes a un grupo limitado de
  participantes externos.
- Publicación del Whitepaper y construcción de la comunidad
  inicial alrededor del protocolo.
- Operación de IKI Hosting como primer servicio real sobre la
  infraestructura, validando demanda.

### Fase Beta

- Integración de los primeros nodos externos a la red,
  incluyendo posibles nodos institucionales (universidades y
  laboratorios de cómputo).
- Implementación del mecanismo de orquestación y recuperación
  ante fallos a escala real, más allá del conjunto inicial de
  nodos propios.
- Apertura gradual a clientes adicionales fuera del grupo de
  Clientes Fundadores.

### Lanzamiento

- Red operando con nodos distribuidos en múltiples ubicaciones
  dentro de México, con miras a expansión hacia otros países de
  Latinoamérica.
- Mecanismo de pago multi-divisa activo, permitiendo a clientes y
  nodos operar en la moneda de su país o en dólares.
- Apertura completa del programa de Nodos más allá del grupo
  Founding, bajo las condiciones estándar del protocolo.

> Las fechas específicas de cada fase se publican y actualizan
conforme avanza el desarrollo.

---

## 6. Equipo y Origen

IKI Network nace en Tuxtla Gutiérrez, Chiapas, México, de la
convicción de que la infraestructura digital de Latinoamérica
debe construirse desde la región, no importarse desde fuera de
ella.

El proyecto es liderado por su fundador, quien combina formación
técnica con la decisión de construir y validar el protocolo de
forma independiente, y en la colaboración temprana con instituciones 
académicas locales para explorar la integración 
de laboratorios de cómputo universitarios como parte de la red de nodos.

IKI Network no se construye en aislamiento. Se construye en
público: documentando avances reales, compartiendo el progreso
técnico tal como ocurre, y abriendo la puerta a quienes quieran
ser parte de la red desde su etapa más temprana.

---

## 7. Cómo Participar

**Si tienes una computadora o servidor disponible**, únete al
programa de Founding Nodes a través de nuestro
[Discord](https://discord.com/invite/DnC5kw6cZ). Cuéntanos qué equipo tienes disponible (CPU, RAM,
almacenamiento) y cuántas horas al día podría estar conectado.

**Si eres desarrollador, agencia o negocio** y necesitas alojar
un proyecto, regístrate en la lista de espera en
[iki.network](https://iki.network).

**Si quieres seguir el desarrollo de cerca**, sigue el progreso
técnico real del proyecto en nuestro
[repositorio de GitHub](https://github.com/iki-network/iki-network).

---

*IKI Network © 2026 · Tuxtla Gutiérrez, Chiapas, México*
*Este documento es la Versión 1.0 y se actualizará conforme el
protocolo evolucione.*
