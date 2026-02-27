# OptiMicroTools Hub - Guía Técnica de Configuración

Este repositorio contiene la Landing Page principal para `optimicrotools.com`, un directorio de herramientas de alto rendimiento procesadas localmente.

## Configuración de Subdominios (Namecheap + Vercel)

Para que la jerarquía de subdominios funcione correctamente, sigue estos pasos:

### 1. En Namecheap (DNS Config)
Accede a tu panel de control de Namecheap y para el dominio `optimicrotools.com`, añade los siguientes registros CNAME en la pestaña **Advanced DNS**:

| Host | Type | Value (Target) |
|------|------|----------------|
| `text` | CNAME Record | `cname.vercel-dns.com` |
| `qr` | CNAME Record | `cname.vercel-dns.com` |
| `prompt` | CNAME Record | `cname.vercel-dns.com` |

> [!NOTE]
> El valor `cname.vercel-dns.com` es el estándar para despliegues en Vercel. Si usas otro proveedor, ajusta el valor según sus instrucciones.

### 2. En Vercel (Project Settings)
Si tienes cada herramienta en un proyecto de Vercel diferente:
1. Ve a cada proyecto específico (e.g., el proyecto de PureText).
2. Entra en **Settings** > **Domains**.
3. Añade el dominio correspondiente (e.g., `text.optimicrotools.com`).
4. Vercel detectará automáticamente los registros DNS una vez que se propaguen.

### 3. Registro A (Opcional - Para el Hub Principal)
Para que `optimicrotools.com` (el hub) apunte a este código:
- **Host**: `@`
- **Type**: `A Record`
- **Value**: `76.76.21.21` (IP de Vercel)

---

## Especificaciones Técnicas
- **Stack**: HTML5, Tailwind CSS, Vanilla JS.
- **Visual**: Dark Luxury Tech (#000000 + #06B6D4).
- **i18n**: Detección automática de idioma + Toggle manual con persistencia.
- **Performance**: 0 dependencias pesadas, carga instantánea.
# optimicrotools
