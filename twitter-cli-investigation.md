# Investigación: Twitter/X desde CLI

## Resumen
Sí es posible usar Twitter/X desde la línea de comandos, pero requiere configuración y en algunos casos una cuenta de desarrollador.

## Opciones Disponibles

### 1. **xcli** (Recomendado)
- Herramienta escrita en Go
- Usa OAuth2 con PKCE
- Requiere **Twitter Developer Account** (Client ID)
- Repo: https://github.com/haydenkz/xcli
- Instalación:克隆 + `sudo ./install.sh`
- Limitación: Solo posting, no streaming

### 2. **Rainbow Stream**
- Cliente Twitter avanzado para Linux
- Escrito en Python
- Requiere API keys de Twitter
- Más features que xcli (timeline, mentions, etc)

### 3. **t-ruby** (Obsoleto)
- Cliente Ruby clásico
- Ya no funciona bien con la API actual de Twitter

## Requisitos para usar X desde CLI

1. **Cuenta de Twitter/X** (cuenta normal)
2. **Twitter Developer Portal** - Necesitás crear una app para obtener:
   - `API Key`
   - `API Secret`  
   - `Bearer Token`
3. **OAuth2** - La mayoría de herramientas usan autenticación OAuth

## Cómo obtener Developer Access

1. Ir a https://developer.twitter.com/
2. Apply for access (gratis para uso personal)
3. Crear un proyecto y una app
4. Generar las credenciales

## Alternativa: Nitter (Solo lectura)

- Nitter es un frontend web para Twitter
- Puedes usarlo con `curl` para ver timelines
- No requiere API
- Repo: https://github.com/zedeus/nitter

## Conclusión

| Opción | Dificultad | Requiere Dev Account | Funcionalidad |
|--------|------------|---------------------|---------------|
| xcli | Media | Sí | Post only |
| Rainbow Stream | Media-Alta | Sí | Full client |
| Nitter | Baja | No | Solo lectura |

**Recomendación**: Si solo necesitás postear, xcli es lo más simple. Si necesitás más features, hay que configurar Developer API.

---
*Investigación realizada: 2026-02-15*
