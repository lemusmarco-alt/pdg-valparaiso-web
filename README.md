# PDG Regional Valparaiso - Sitio Web

Sitio web oficial del Partido de la Gente Regional Valparaiso.

## Stack Tecnologico

- React 19 + TypeScript
- Vite
- Tailwind CSS
- shadcn/ui
- React Router (HashRouter)

## Despliegue en Vercel (Paso a paso)

### Opcion A: Deploy automatico con Git (Recomendado)

1. **Sube el codigo a GitHub**
   - Ve a https://github.com/new y crea un repositorio nuevo (ej: `pdg-valparaiso-web`)
   - En tu terminal local, ejecuta:
   ```bash
   cd /ruta/del/proyecto
   git remote add origin https://github.com/TU_USUARIO/pdg-valparaiso-web.git
   git branch -M main
   git push -u origin main
   ```

2. **Conecta a Vercel**
   - Ve a https://vercel.com/new
   - Selecciona tu repositorio de GitHub
   - Framework Preset: `Vite`
   - Build Command: `npm run build`
   - Output Directory: `dist`
   - Click en **Deploy**

3. **Conecta tu dominio propio**
   - En el dashboard de tu proyecto en Vercel, ve a **Settings > Domains**
   - Escribe tu dominio y click en **Add**
   - Configura los DNS en tu proveedor de dominio:
     - Tipo `A` → `@` → `76.76.21.21`
     - O usa los nameservers de Vercel (recomendado)

### Opcion B: Deploy manual (CLI)

```bash
# Instala Vercel CLI
npm i -g vercel

# Login
vercel login

# Deploy
vercel --prod
```

### Opcion C: Usando los archivos dist/

1. Ejecuta `npm run build`
2. Sube el contenido de la carpeta `dist/` via drag & drop en https://vercel.com/new

## Dominio personalizado en Vercel

Una vez deployado:

1. Ve al proyecto → **Settings → Domains**
2. Agrega tu dominio (ej: `pdgvalparaiso.cl`)
3. Vercel te dara instrucciones especificas para tu proveedor de dominio

### Configuracion DNS tipica

| Tipo | Nombre | Valor |
|------|--------|-------|
| A | @ | 76.76.21.21 |
| CNAME | www | cname.vercel-dns.com |

## Estructura del sitio

| Ruta | Pagina |
|------|--------|
| `/` | Inicio |
| `/#/olivares` | Diputado Olivares |
| `/#/valenzuela` | Diputado Valenzuela |
| `/#/transparencia` | Panel de Transparencia |
| `/#/formacion` | Escuela de Formacion |
| `/#/voluntarios` | Registro de Voluntarios |
| `/#/comunidad` | Comunidad PDG |

## Personalizacion

Para modificar contenido, edita los archivos en `src/pages/` y corre `npm run build`.

---

Desarrollado para PDG Regional Valparaiso 2026
