<div align="center">

# 🎓 Aula IA · Aula virtual con recomendaciones

**Aula virtual tipo Coursera/Udemy** construida alrededor de un recomendador al estilo Netflix, accesible para personas ciegas y con baja visión.

[![Demo](https://img.shields.io/badge/Ver%20demo-aula--virtual--con--ia.vercel.app-000000?style=for-the-badge&logo=vercel&logoColor=white)](https://aula-virtual-con-ia.vercel.app)
[![Portafolio](https://img.shields.io/badge/Detalle%20en%20el%20portafolio-E34F26?style=for-the-badge&logo=astro&logoColor=white)](https://luis-mercado-portfolio.vercel.app/proyectos/aula-virtual-ia)
![Estado](https://img.shields.io/badge/Estado-En%20producci%C3%B3n-2EA44F?style=for-the-badge)

<img src="docs/portada.jpg" alt="Portada de Aula IA" width="100%" />

</div>

> 🔒 **Repositorio de presentación.** El código fuente es privado. Aquí encontrarás la descripción, la arquitectura y capturas del sistema. Si quieres conocer el código para un proceso de selección, [escríbeme](mailto:luisda3329@hotmail.com).

---

## 📌 Qué es

Plataforma de cursos con estudiantes, docentes, foros, reseñas y evaluaciones, construida alrededor de un **motor de recomendaciones propio**. La primera vez pregunta los intereses (o los aprende de lo que la persona empieza a ver) y desde ahí arma filas personalizadas que **explican por qué aparece cada curso**.

Todo el sitio está pensado para que lo usen personas que no ven: navegación por lector de pantalla, lectura en voz alta y ajustes de alto contraste, tamaño de texto y fuente de alta legibilidad.

## ✨ Funcionalidades

- 🧠 **Recomendador híbrido:** similitud de contenido + filtrado colaborativo ítem a ítem, popularidad bayesiana, decaimiento temporal y diversidad MMR, cubierto con 16 pruebas.
- ❄️ **Arranque en frío:** bienvenida opcional de intereses o aprendizaje a partir de lo que la persona consume; cada fila explica su razón.
- 📚 **Cursos** con módulos, lecturas, videos con transcripción, evaluaciones calificadas, progreso y constancia al completar.
- 💬 **Foros** por curso, **reseñas** con calificación y **panel de docencia** para crear y publicar cursos.
- ♿ **Accesibilidad WCAG 2.2 AA** verificada con axe: lector de pantalla, lectura en voz alta, alto contraste, texto al 200 % y fuente Atkinson Hyperlegible.
- 🎬 Diseño editorial con GSAP y Lenis que respeta el movimiento reducido.

## 🖼️ Capturas

| | |
|---|---|
| <img src="docs/02-inicio-personalizado.jpg" alt="Inicio personalizado" /> <br/> **Inicio personalizado** con filas de recomendaciones | <img src="docs/03-curso.jpg" alt="Curso" /> <br/> **Página de curso** con temario, reseñas y profesor |
| <img src="docs/04-leccion.jpg" alt="Lección" /> <br/> **Lección** con lectura en voz alta y temario lateral | <img src="docs/06-bienvenida.jpg" alt="Bienvenida" /> <br/> **Bienvenida** opcional para elegir intereses |
| <img src="docs/05-docencia.jpg" alt="Docencia" /> <br/> **Panel de docencia** | <img src="docs/01-portada.jpg" alt="Portada pública" /> <br/> **Portada pública** |

## 🏗️ Arquitectura

```mermaid
flowchart LR
    U[Estudiante] --> UI
    D[Docente] --> UI
    subgraph App["Next.js 16 · App Router"]
        UI[Interfaz accesible<br/>lector de pantalla · voz · alto contraste]
        SA[Server Actions]
        REC[Motor de recomendaciones<br/>contenido · colaborativo · bayesiano · MMR]
    end
    DB[(PostgreSQL · Neon<br/>Drizzle ORM)]

    UI --> SA
    SA --> REC
    SA --> DB
    REC -- historial y señales --> DB
```

## 🛠️ Stack

![Next.js](https://img.shields.io/badge/Next.js-000000?style=for-the-badge&logo=nextdotjs&logoColor=white)
![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white)
![Tailwind CSS](https://img.shields.io/badge/Tailwind%20CSS-06B6D4?style=for-the-badge&logo=tailwindcss&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white)
![Drizzle](https://img.shields.io/badge/Drizzle-C5F74F?style=for-the-badge&logo=drizzle&logoColor=black)
![Neon](https://img.shields.io/badge/Neon-00E599?style=for-the-badge&logo=neon&logoColor=black)
![GSAP](https://img.shields.io/badge/GSAP-0AE448?style=for-the-badge&logo=gsap&logoColor=black)
![Vercel](https://img.shields.io/badge/Vercel-000000?style=for-the-badge&logo=vercel&logoColor=white)

---

<div align="center">

Hecho por **[Luis Mercado](https://github.com/luismercado29)** · Diseño y desarrollo full-stack · 2026

© 2026 Luis Mercado. Todos los derechos reservados.

</div>
