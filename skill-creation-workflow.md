# Workflow para Crear Skills

Este documento describe el proceso para crear nuevas skills para Rufus.

## Opciones para Crear Skills

### 1. ctx7 CLI (Automatizado)

**Recomendado para:** Librerías/frameworks con documentación

```bash
# Install ctx7
npm install -g ctx7

# Login (requiere OAuth)
npx ctx7 login

# Buscar skills existentes
npx ctx7 skills search <termino>

# Generar nueva skill desde docs
npx ctx7 skills generate
# Respon preguntas interactde lasivas
# El CLI genera un SKILL.md desde la documentación
```

**Pros:**
- Genera draft desde docs reales
- Rápido
- Mantiene skills actualizadas

**Contras:**
- Requiere login OAuth
- Solo para libs con docs indexadas

### 2. Creación Manual

**Recomendado para:** Skills genéricas, procesos, metodologías

Pasos:
1. Investigar el tema
2. Crear estructura del SKILL.md
3. Documentar comandos, casos de uso, ejemplos
4. Instalar en `/root/.openclaw/workspace/skills/`
5. Actualizar README.md y sincronizar a GitHub

### 3. Adaptar de Ejemplos

**Recomendado para:** Skills similares a existentes

- Revisar skills existentes en el workspace
- Copiar estructura y adaptar contenido

## Estructura de una Skill

```markdown
---
name: nombre-skill
description: Descripción corta de cuándo usar esta skill
---

# Título

## Cuándo Usar Esta Skill
- Caso 1
- Caso 2

## Contenido principal
...
```

## Dónde Instalar

- **Skills del workspace:** `/root/.openclaw/workspace/skills/`
- **Skills del sistema:** `/usr/lib/node_modules/openclaw/skills/`

## Sincronizar a GitHub

```bash
cd /root/.openclaw/workspace/skills
git add .
git commit -m "Nueva skill: nombre"
git push origin main
```

## Mejores Prácticas

1. **Usa TDD**: Define casos de prueba primero
2. **Sé específico**: Cada skill tiene un propósito claro
3. **Incluye ejemplos**: Comandos reales, código funcional
4. **Documenta prerequisitos**: Qué se necesita antes de usar
5. **Actualiza regularmente**: Revisa y mejora skills existentes

## Referencias

- Superpowers: `writing-skills`
- Superpowers: `test-driven-development`
- ctx7: https://context7.com
