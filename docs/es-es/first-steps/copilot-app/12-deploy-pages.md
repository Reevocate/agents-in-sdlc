---
title: "Lección 12 - Publica el sitio con GitHub Pages"
description: "Usa la aplicación GitHub Copilot para configurar un flujo de trabajo de Pages, revisar su solicitud de cambios y comprobar el Space Quiz publicado."
authors:
  - jamesmontemagno
lastUpdated: 2026-10-12
---

Publica Space Quiz en GitHub Pages para que todo el mundo pueda acceder. Copilot puede preparar el flujo de trabajo y guiarte durante la publicación, pero debes revisar los cambios y confirmar que el sitio está disponible.

En esta lección:

- Pide a Copilot que configure una implementación con GitHub Pages.
- Revisa el flujo de trabajo y la solicitud de cambios antes de fusionarla.
- Sigue la implementación y comprueba el sitio publicado.

## Escenario

Space Quiz ya está en un repositorio de GitHub, pero aún hace falta una forma sencilla de probarlo. Publicar el sitio de un solo archivo con GitHub Pages permite acceder a él desde una URL pública sin añadir un servidor ni una dependencia del entorno de ejecución.

## Pide a Copilot que publique el sitio

En la sesión de la aplicación Copilot para `space-quiz`, envía este mensaje:

```plaintext
Habilita GitHub Pages para este repositorio. Crea un flujo de trabajo de GitHub Actions que compile el sitio web si es necesario y lo publique en GitHub Pages. Añade un README que describa la aplicación y cómo ejecutarla localmente si aún no existe. Crea una solicitud de cambios con estos cambios y fusiónala cuando se superen las comprobaciones obligatorias. Supervisa la implementación hasta que se complete correctamente y, después, indica la URL final del sitio web publicado. Si no tienes permiso para habilitar Pages o fusionar la solicitud, dime exactamente qué debo aprobar o hacer; no indiques que se ha completado correctamente hasta que el sitio esté publicado.
```

![Diagrama de tres etapas: una solicitud de cambios de space-quiz fusionada; una ejecución correcta de GitHub Actions Deploy website con los pasos Build website, Upload artifact y Deploy to Pages; y Space Quiz publicado en yourname.github.io/space-quiz/.](../../../_images/first-steps-app-pages-deploy.svg)

> [!WARNING]
> Este mensaje pide al agente que cree y fusione una solicitud de cambios y modifique la configuración de Pages del repositorio. Revisa las diferencias, los permisos de implementación y cualquier solicitud de aprobación de GitHub antes de continuar.

## Revisa el flujo de trabajo y comprueba la implementación

1. Confirma que el README solo se ha añadido si el repositorio aún no tenía uno.
2. Revisa los cambios de la solicitud, incluidos los pasos de compilación e implementación del flujo de trabajo.
3. Fusiona la solicitud únicamente cuando se superen las comprobaciones obligatorias.
4. Sigue la ejecución de implementación de GitHub Actions hasta que se complete correctamente.
5. Abre la URL indicada y confirma que se carga Space Quiz.

Si el agente no puede habilitar Pages o fusionar la solicitud de cambios, sigue las instrucciones concretas que te proporcione. No des la tarea por terminada hasta que la implementación se complete correctamente y el sitio esté disponible.

## Resumen y siguientes pasos

Space Quiz ya está disponible como sitio web y has comprobado la implementación en lugar de confiar únicamente en el informe del agente. Continúa con [Lección 13: Repaso y siguientes pasos][next-lesson].

[next-lesson]: ../13-review/
