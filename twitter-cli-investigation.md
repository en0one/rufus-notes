# Investigación: Twitter/X desde CLI (Actualizada 2026)

## Resumen Ejecutivo

Sí es posible usar Twitter/X desde la línea de comandos, pero hay cambios importantes respecto a antes:
- El **Free Tier** de la API ahora es muy limitado (50 credits/mes)
- Se requiere **Twitter Developer Account** para casi todas las opciones
- Existen alternativas gratuitas con limitaciones

---

## Opciones Disponibles

### 1. **xcli** ⭐ (Recomendado para posting básico)
- **Lenguaje:** Go
- **Autenticación:** OAuth2 con PKCE
- **Repo:** https://github.com/haydenkz/xcli
- **Instalación:**
  ```bash
  git clone https://github.com/haydenkz/xcli.git
  cd xcli
  chmod +x install.sh
  sudo ./install.sh
  ```
- **Pros:**
  - Instalación simple
  - Usa OAuth2 PKCE (más seguro)
  - Interactive REPL para tweets
- **Contras:**
  - Solo posting, no timeline ni streaming
  - Requiere Client ID de Twitter Developer

### 2. **Rainbow Stream** (Cliente completo)
- **Lenguaje:** Python
- **Repo:** https://github.com/orakaro/rainbowstream
- **Instalación:**
  ```bash
  pip install rainbowstream
  rainbowstream -iot
  ```
- **Pros:**
  - Timeline real-time
  - Compose, search, favorite, retweet
  - Interfaz visual con colores
- **Contras:**
  - Requiere API keys de Twitter
  - Configuración más compleja

### 3. **Twython** (Biblioteca Python)
- **Lenguaje:** Python (biblioteca)
- **Repo:** https://github.com/ryanmcgrath/twython
- **Uso:** Para desarrollo personalizado
- **Pros:**
  - Flexible, para construir tus propias tools
  - Bien documentado
- **Contras:**
  - Requiere programación

### 4. **Nitter** (Solo lectura - Alternativa sin API)
- **Qué es:** Frontend web alternativo para Twitter
- **Repo:** https://github.com/zedeus/nitter
- **Alternativas públicas:** https://nitter.net
- **Uso:**
  ```bash
  curl "https://nitter.net/[usuario]/rss"
  ```
- **Pros:**
  - No requiere API
  - RSS disponible
- **Contras:**
  - Solo lectura
  - Depende de instancias públicas

---

## API de Twitter/X - Estado Actual (2026)

### Niveles de Acceso

| Tier | Precio | Credits/mes | Funcionalidad |
|------|--------|-------------|---------------|
| Free | $0 | 50 (~500 datos) | Solo lectura, posting básico |
| Basic | $200/mes | 10,000 | Posting, métricas básicas |
| Pro | $5,000/mes | 1,000,000 | Analytics, ads API |
| Enterprise | Custom | Ilimitado | Full API access |

### Cómo obtener acceso

1. Ir a https://developer.twitter.com/
2. Crear cuenta de desarrollador (gratis)
3. Crear proyecto y app
4. Generar credenciales:
   - API Key
   - API Secret
   - Bearer Token
   - Access Token (para posting)

### Limitaciones del Free Tier (2025-2026)
- Solo 50 credits/mes (~500 requests)
- No streaming
- No acceso a Ads API
- Rate limits muy estrictos

---

## Alternativas a la API de Twitter

### Para leer tweets sin API
1. **Nitter** - Instancia web
2. **FixupX** - Alternativa web
3. **Fxtwitter** - API de proxy:
   ```
   https://api.fxtwitter.com/status/ID
   ```

### Para posting sin pagar
- **Facebook/Instagram** (más generosos)
- **Mastodon** (opensource, gratis)
- **Bluesky** (API más abierta)

---

## Comparativa Final

| Herramienta | Dificultad | Requiere Dev | Funcionalidad | Costo |
|-------------|------------|--------------|---------------|-------|
| xcli | Media | Sí | Post only | Gratis* |
| Rainbow Stream | Alta | Sí | Full client | Gratis* |
| Twython | Alta | Sí | Custom | Gratis* |
| Nitter | Baja | No | Solo lectura | Gratis |
| Fxtwitter API | Baja | No | Read + embed | Gratis |

*Gratis si ya tenés Developer Account

---

## Recomendación

Para uso personal desde CLI:
1. **Si solo necesitás postear:** xcli + Developer Account (free tier)
2. **Si necesitás timeline completo:** Rainbow Stream
3. **Si no querés pagar ni registrarte:** Nitter o Fxtwitter

---

## Links Útiles

- [Twitter Developer Portal](https://developer.twitter.com/)
- [xcli GitHub](https://github.com/haydenkz/xcli)
- [Rainbow Stream](https://github.com/orakaro/rainbowstream)
- [Nitter](https://github.com/zedeus/nitter)
- [Fxtwitter](https://github.com/axcore/taxy)

---

*Investigación actualizada: 2026-02-15*
*Usando content-writer skill*
