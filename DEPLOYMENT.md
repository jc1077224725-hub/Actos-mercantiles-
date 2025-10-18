# Guía de Despliegue en Netlify

## Folleto Digital Interactivo: Actos de Comercio

Esta guía te ayudará a desplegar permanentemente el folleto digital en Netlify.

---

## Opción 1: Despliegue Manual (Más Rápido - 2 minutos)

### Paso 1: Preparar los archivos
1. Descarga o copia la carpeta `folleto-actos-comercio` en tu computadora
2. Asegúrate de que contenga:
   - `index.html`
   - `css/styles.css`
   - `js/script.js`
   - `netlify.toml`
   - `package.json`

### Paso 2: Ir a Netlify
1. Abre [netlify.com](https://netlify.com) en tu navegador
2. Haz clic en **"Sign up"** (si no tienes cuenta) o **"Log in"** (si ya la tienes)
3. Puedes registrarte con GitHub, GitLab, Bitbucket o correo electrónico

### Paso 3: Crear nuevo sitio
1. En el dashboard de Netlify, haz clic en **"Add new site"**
2. Selecciona **"Deploy manually"**

### Paso 4: Subir archivos
1. Arrastra la carpeta `folleto-actos-comercio` al área de drop
2. O haz clic en el área para seleccionar los archivos
3. Netlify comenzará a procesar los archivos

### Paso 5: Obtener tu URL
1. Espera a que termine el despliegue (generalmente 30 segundos)
2. Verás un mensaje de éxito con tu URL permanente
3. La URL será algo como: `https://[nombre-aleatorio].netlify.app`

### Paso 6: Personalizar el dominio (Opcional)
1. En la página del sitio, haz clic en **"Site settings"**
2. Ve a **"Domain management"**
3. Haz clic en **"Edit site name"** para cambiar el nombre
4. O conecta tu propio dominio personalizado

---

## Opción 2: Despliegue con Git (Más Profesional)

### Requisitos
- Cuenta en GitHub, GitLab o Bitbucket
- Git instalado en tu computadora

### Paso 1: Crear repositorio
1. Ve a [github.com](https://github.com)
2. Haz clic en **"New repository"**
3. Nombra el repositorio: `folleto-actos-comercio`
4. Haz clic en **"Create repository"**

### Paso 2: Subir archivos a Git
```bash
# En tu terminal, ve a la carpeta del proyecto
cd folleto-actos-comercio

# Inicializar Git
git init

# Agregar todos los archivos
git add .

# Hacer commit
git commit -m "Initial commit: Folleto Digital Actos de Comercio"

# Agregar el repositorio remoto (reemplaza TU_USUARIO)
git remote add origin https://github.com/TU_USUARIO/folleto-actos-comercio.git

# Subir a GitHub
git branch -M main
git push -u origin main
```

### Paso 3: Conectar con Netlify
1. Ve a [netlify.com](https://netlify.com) y haz login
2. Haz clic en **"Add new site"**
3. Selecciona **"Import an existing project"**
4. Elige **"GitHub"** (o tu plataforma)
5. Autoriza a Netlify a acceder a tu cuenta
6. Selecciona el repositorio `folleto-actos-comercio`
7. Haz clic en **"Deploy site"**

### Paso 4: Configuración automática
Netlify leerá automáticamente `netlify.toml` y configurará:
- Build command
- Publish directory
- Headers de seguridad
- Cache policies

### Paso 5: Obtener URL
Tu sitio estará disponible en una URL como:
`https://[nombre-aleatorio].netlify.app`

---

## Después del Despliegue

### Cambiar el nombre del sitio
1. Ve a **"Site settings"**
2. Haz clic en **"Change site name"**
3. Ingresa un nuevo nombre (ej: `folleto-actos-comercio`)
4. Tu URL será: `https://folleto-actos-comercio.netlify.app`

### Conectar dominio personalizado
1. Ve a **"Domain management"**
2. Haz clic en **"Add custom domain"**
3. Ingresa tu dominio (ej: `midominio.com`)
4. Sigue las instrucciones para actualizar los DNS

### Habilitar HTTPS
- Netlify proporciona HTTPS gratuito automáticamente
- Tu sitio será accesible en `https://`

### Configurar redirecciones
- Edita `netlify.toml` si necesitas redirecciones personalizadas
- Haz push a Git y Netlify se actualizará automáticamente

---

## Verificación Post-Despliegue

Después de desplegar, verifica que todo funcione correctamente:

### ✅ Checklist
- [ ] El sitio carga correctamente
- [ ] La navegación funciona (menú y enlaces)
- [ ] Los tabs del Numeral 13 son interactivos
- [ ] Las animaciones se ven suave
- [ ] El diseño es responsivo en móvil
- [ ] Los iconos se cargan correctamente
- [ ] Las fuentes se ven bien
- [ ] No hay errores en la consola del navegador

### Verificar errores
1. Abre el sitio en tu navegador
2. Presiona `F12` para abrir Developer Tools
3. Ve a la pestaña **"Console"**
4. No debería haber errores en rojo

---

## Solución de Problemas

### El sitio no carga
- Verifica que todos los archivos estén en la carpeta raíz
- Asegúrate de que `index.html` esté en el nivel superior
- Recarga la página (Ctrl+Shift+R o Cmd+Shift+R)

### Los estilos no se ven
- Verifica que la carpeta `css/` esté presente
- Comprueba que `styles.css` esté dentro de `css/`
- Limpia el cache del navegador

### Los scripts no funcionan
- Verifica que la carpeta `js/` esté presente
- Comprueba que `script.js` esté dentro de `js/`
- Abre la consola del navegador (F12) para ver errores

### Las fuentes no cargan
- Verifica tu conexión a Internet
- Comprueba que Google Fonts esté accesible
- Intenta desde otro navegador

---

## Actualizaciones Futuras

### Con Git (Recomendado)
```bash
# Hacer cambios locales
# Editar archivos según sea necesario

# Subir cambios
git add .
git commit -m "Descripción de cambios"
git push origin main

# Netlify se actualizará automáticamente
```

### Manual
1. Ve a Netlify dashboard
2. Haz clic en **"Deploys"**
3. Arrastra la carpeta actualizada
4. Netlify desplegará la nueva versión

---

## Estadísticas y Monitoreo

### En Netlify Dashboard
- **Deploys**: Historial de despliegues
- **Analytics**: Visitantes y estadísticas
- **Logs**: Información de compilación y errores
- **Performance**: Velocidad y rendimiento

---

## Soporte

Si encuentras problemas:

1. **Documentación de Netlify**: [docs.netlify.com](https://docs.netlify.com)
2. **Comunidad Netlify**: [community.netlify.com](https://community.netlify.com)
3. **GitHub Issues**: Abre un issue en tu repositorio

---

## Resumen Rápido

| Tarea | Tiempo | Dificultad |
|-------|--------|-----------|
| Despliegue manual | 2 min | Muy fácil |
| Despliegue con Git | 10 min | Fácil |
| Cambiar nombre | 1 min | Muy fácil |
| Conectar dominio | 5 min | Fácil |

---

**¡Tu folleto digital estará disponible permanentemente en Internet!**

Para más información, visita [netlify.com](https://netlify.com)

---

*Última actualización: Octubre 2025*

