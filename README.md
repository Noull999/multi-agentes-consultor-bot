# 🤖 Multi-Agentes

**3 sistemas multi-agente con CrewAI + OpenCode Go**

Repositorio unificado con 3 herramientas de IA orquestadas, API REST, Docker Compose y menú interactivo.

## 📦 Proyectos

| Proyecto | Agentes | Input → Output |
|---|---|---|
| 🔍 **Code Review Bot** | 4 | Ruta de proyecto → Reporte de bugs + estilo + docs |
| 🛠️ **IT Support Bot** | 4 | Problema técnico → Diagnóstico + plan de solución |
| 🎯 **Consultor Full-Stack** | 5 | Descripción de cliente → Propuesta + código base |

## 🚀 Cómo usar

### Desde terminal
```bash
git clone https://github.com/Noull999/multi-agentes.git
cd multi-agentes
./agente.sh
```

### Con Docker (proyecto individual)
```bash
cd code-review-bot
cp .env.docker .env  # editar con tu API key
docker compose up -d
# Usar: docker exec code-review python src/main.py /ruta/proyecto --opencode
```

### Con Docker (todo junto - API REST)
```bash
cp .env.docker .env
docker compose up -d
# API en http://localhost:8000
```

### API REST (con Docker)
```
POST /api/code-review  → body: {"path": "/proyecto", "model": "kimi-k2.7-code"}
POST /api/it-support   → body: {"issue": "PC no enciende"}
POST /api/consultor    → body: {"description": "App para restaurant..."}
```

## 🧠 Modelos recomendados

| Proyecto | Modelo |
|---|---|
| Code Review Bot | `kimi-k2.7-code` |
| IT Support Bot | `deepseek-v4-flash` |
| Consultor Full-Stack | `kimi-k2.7-code` |

## 🛠 Stack

- **Python 3.12** + CrewAI 1.14
- **OpenCode Go** (endpoint OpenAI-compatible)
- **FastAPI** (REST API)
- **Docker Compose**
- Alternativas: Gemini (gratis), OpenAI

## 📄 Licencia

MIT
