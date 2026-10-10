# 👥 Moyolo - CRM de Gestión de Recursos Humanos (RRHH)

Sistema integral de gestión de talento humano, control de personal, seguimiento de contratos, asistencia y cumplimiento laboral (SST/EMO) diseñado para optimizar los procesos de Recursos Humanos.

---

## 🚀 Tecnologías Principales

- **[Astro](https://astro.build/)** (v7.x): Framework web de alto rendimiento optimizado para velocidad y arquitectura de componentes.
- **[Tailwind CSS v4](https://tailwindcss.com/)**: Motor de estilos de última generación integrado mediante `@tailwindcss/vite`.
- **[Remix Icon](https://remixicon.com/)**: Librería moderna de iconografía vectorial.
- **[Plus Jakarta Sans](https://fonts.google.com/specimen/Plus+Jakarta+Sans)**: Tipografía moderna y profesional para interfaces empresariales.

---

## 📦 Módulos del Sistema

El sistema cuenta con una arquitectura modular orientada a las distintas áreas de la gestión de RRHH:

### 1. 📊 General & Métricas
- **Dashboard (`/Dachboard`)**: Panel central de control con KPIs clave (empleados activos, métricas globales, alertas tempranas).

### 2. 👤 Gestión de Personal
- **Colaboradores (`/colaboradores`)**: Directorio y fichas de personal con información laboral y de contacto.
- **Contratos & Vencimientos (`/contratos`, `/Iniciocontrato`)**: Monitoreo de vigencia de contratos, renovaciones y alertas preventivas.
- **Documentos / Legajos (`/expedientes`)**: Archivo y custodia digital de documentos del trabajador.

### 3. ⏱️ Operaciones Diarias
- **Asistencia & Tardanzas (`/asistencia`)**: Control de registro, marcaciones, puntualidad e incidencias.
- **Vacaciones & Permisos (`/permisos`)**: Solicitud, aprobación y balance de días de descanso y permisos especiales.
- **Boletas de Pago (`/boletas`)**: Emisión, consulta y distribución de recibos y boletas de remuneraciones.

### 4. 🛡️ Seguridad & Cumplimiento
- **SST / EMO (`/sst`)**: Gestión de Seguridad y Salud en el Trabajo y seguimiento a Exámenes Médicos Ocupacionales periódicos.
- **Configuración (`/configuracion`)**: Ajustes de parámetros generales, roles y permisos de usuario.

---

## 📂 Estructura del Proyecto

```text
crm_rrhh/
├── public/                     # Archivos estáticos públicos (favicons, etc.)
├── src/
│   ├── assets/                 # Recursos gráficos (logos, vectores, imágenes)
│   ├── components/
│   │   ├── Dashboard/          # Componentes específicos del tablero de control
│   │   └── Global/             # Componentes transversales
│   │       ├── Cardkpi.astro   # Tarjetas de indicadores y métricas
│   │       ├── header.astro    # Barra superior del panel
│   │       └── siderbar.astro  # Barra lateral con navegación y badges de alerta
│   ├── layouts/
│   │   └── Layout.astro        # Plantilla base con tema Dark y navegación integrada
│   ├── pages/                  # Enrutamiento basado en archivos de Astro
│   │   ├── Dachboard.astro     # Vista del Dashboard
│   │   ├── Iniciocontrato.astro# Creación / gestión de contratos
│   │   └── index.astro         # Página de entrada
│   └── styles/
│       └── global.css          # Estilos globales y configuración Tailwind v4
├── astro.config.mjs            # Configuración de Astro y plugins Vite
├── package.json                # Dependencias y scripts del proyecto
└── tsconfig.json               # Configuración de TypeScript
```

---

## 🛠️ Requisitos Previos

- **Node.js**: `>= 22.12.0` (recomendado v22 LTS o superior)
- **Gestor de paquetes**: `npm` (incluido con Node.js)

---

## ⚡ Instalación y Puesta en Marcha

1. **Clonar o abrir el repositorio**:
   ```bash
   cd crm_rrhh
   ```

2. **Instalar las dependencias**:
   ```bash
   npm install
   ```

3. **Iniciar el servidor de desarrollo**:
   ```bash
   npm run dev
   ```
   > Abre tu navegador en [http://localhost:4321](http://localhost:4321) para visualizar la aplicación.

4. **Modo Background (según directivas de desarrollo)**:
   ```bash
   astro dev --background
   ```
   - Ver estado: `astro dev status`
   - Ver logs: `astro dev logs`
   - Detener servidor: `astro dev stop`

---

## 📜 Scripts Disponibles

| Comando | Descripción |
| :--- | :--- |
| `npm run dev` | Inicia el entorno local de desarrollo con recarga en vivo. |
| `npm run build` | Compila la aplicación optimizada para producción en la carpeta `./dist/`. |
| `npm run preview` | Previsualiza localmente el build de producción antes de desplegar. |
| `npm run astro ...` | Ejecuta comandos de la CLI de Astro (por ej. `astro check`). |

---

## 🎨 Diseño e Identidad Visual

- **Tema Oscuro Premium**: Paleta basada en tonos `slate-900`/`slate-950` con contrastes en `indigo` y `sky`.
- **Microinteracciones**: Estados activos con efecto `backdrop-blur`, badges pulsantes de alerta para vencimientos y transiciones fluidas.
- **Diseño Responsivo**: Adaptado para resoluciones de escritorio y pantallas compactas.
