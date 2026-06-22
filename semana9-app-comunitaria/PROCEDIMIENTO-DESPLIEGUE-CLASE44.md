# Procedimiento de despliegue y operación básica

## 1. Objetivo
Explicar los pasos para instalar, configurar, ejecutar y verificar la aplicación Node.js de la Semana 9.

## 2. Entorno de trabajo
- GitHub Codespaces
- Node.js
- npm
- Git
- PM2 (para ejecutar la app en segundo plano)

## 3. Requisitos previos
Antes de comenzar, asegúrate de tener:
- Acceso al repositorio.
- El proyecto abierto en Codespaces.
- La carpeta `semana9-app-comunitaria` seleccionada.
- Node.js instalado y disponible.
- Un archivo `.env` local creado.
- El archivo `.env` excluido del repositorio.

## 4. Archivo de variables de entorno
Crea un archivo local llamado `.env` con este formato:

PORT=3000
APP_NAME=App Comunitaria Semana 9
APP_ENV=development
REQUIRE_TELEGRAM=true
TELEGRAM_BOT_TOKEN=MI_TOKEN_DE_PRACTICA

Importante: no uses tokens reales en ejemplos públicos y no subas `.env` a GitHub.

## 5. Instalar dependencias
Ejecuta este comando dentro de `semana9-app-comunitaria`:

npm install

Si necesitas instalar paquetes adicionales:

npm install express dotenv
npm install pm2 --save-dev

## 6. Ejecutar la app con Node.js
Inicia la aplicación con:

npm start

Luego verifica que funcione con:

curl http://localhost:3000/estado

## 7. Ejecutar la app con PM2
Usa PM2 para mantener la app en ejecución en segundo plano.

Iniciar la app:

npx pm2 start server.js --name app-semana9

Ver procesos activos:

npx pm2 list

Reiniciar la app:

npx pm2 restart app-semana9

Detener la app:

npx pm2 stop app-semana9

Ver los últimos 20 registros:

npx pm2 logs app-semana9 --lines 20

Eliminar el proceso de PM2:

npx pm2 delete app-semana9

## 8. Rutas para verificar la aplicación
Prueba estas direcciones en el navegador o con `curl`:

- `http://localhost:3000/`
- `http://localhost:3000/saludo`
- `http://localhost:3000/estado`
- `http://localhost:3000/api/info`
- `http://localhost:3000/diagnostico`

## 9. Archivos y carpetas que no deben subirse
Asegúrate de que estos elementos estén excluidos:

- `.env`
- `*.env`
- `node_modules/`
- `uploads/`
- `logs/`
- `tmp/`

Si necesitas conservar carpetas vacías, usa archivos `.gitkeep`.

## 10. Revisar antes de hacer commit
Comprueba el estado y los archivos ignorados:

git status
git check-ignore -v .env
git check-ignore -v uploads/documento-prueba.txt
git check-ignore -v logs/app.log
git check-ignore -v tmp/temporal.txt

## 11. Guardar cambios en Git
Cuando todo esté listo, usa:

git add .
git commit -m "Documenta despliegue y protege archivos locales"
git push -u origin clase-44-documentacion-ia-gitignore

## 12. Buenas prácticas
- No publiques tokens ni credenciales.
- No subas `.env` al repositorio.
- No subas logs ni archivos de usuarios.
- No pegues credenciales en asistentes de IA.
- Revisa cada comando antes de ejecutarlo.