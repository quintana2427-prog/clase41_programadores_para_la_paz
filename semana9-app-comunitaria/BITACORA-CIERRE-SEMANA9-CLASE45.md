# Bitácora de cierre - Semana 9 - Clase 45

## Datos generales

Nombre: Luis Quintana Avila 
Fecha: 27/06/2026
Entorno: GitHub Codespaces
Rama de trabajo: clase-45-cierre-git-integrador

## 1. Verificación de aplicación

Comando usado para levantar la aplicación: npm start

Respuesta de /estado: La aplicación respondió indicando que el estado era activo.

Respuesta de /diagnostico: Mostró el entorno de ejecución y confirmó si el token de Telegram estaba configurado, sin revelar información sensible.

Respuesta de /api/info: Mostró la información del proyecto: Programa "Capacitación en Democracia y Tecnología", alias "Programadores para la Paz", Semana 9, Clase 42 y el tema correspondiente.

## 2. Variables de entorno

¿Qué variables se usaron? 
TELEGRAM_BOT_TOKEN
REQUIRE_TELEGRAM

¿Por qué .env no debe subirse? Porque contiene información sensible como claves, tokens y configuraciones privadas que no deben publicarse en el repositorio.

## 3. Seguridad operativa

¿Qué medidas de seguridad se aplicaron durante la semana? 
Uso de variables de entorno.
Protección del archivo .env mediante .gitignore.
Exclusión de archivos temporales, logs y archivos de pruebas.
Verificación de que no se expusieran credenciales.

## 4. Diagnóstico

¿Qué error simulado se trabajó durante la semana? Se simuló la falta de configuración del token de Telegram y la revisión del estado de la aplicación.

¿Cómo se corrigió? Configurando correctamente las variables de entorno y verificando el funcionamiento mediante las rutas de diagnóstico.

## 5. Documentación

¿Qué documento explica el procedimiento de despliegue? PROCEDIMIENTO-DESPLIEGUE-CLASE44.md

## 6. Git

¿Qué aprendí sobre ramas? Que permiten desarrollar nuevas funcionalidades sin afectar la rama principal.

¿Qué aprendí sobre stash? Que permite guardar cambios temporalmente para recuperarlos después.

¿Qué aprendí sobre merge fast-forward? Que une ramas cuando no existen cambios paralelos, manteniendo un historial lineal.

¿Qué aprendí sobre merge no-fast-forward? Que crea un commit de fusión cuando ambas ramas tienen cambios independientes.

¿Qué aprendí sobre conflictos? Que deben resolverse manualmente cuando Git no puede combinar automáticamente los cambios de dos ramas.

## 7. Reflexión final

¿Qué fue lo más importante de la Semana 9? Aprendí a preparar una aplicación para un entorno de trabajo más seguro utilizando variables de entorno, documentación técnica, buenas prácticas con Git y organización del proyecto mediante ramas, diagnósticos y control de archivos sensible