## Sesión 1 - 8 septiembre 2026
- Aprendí navegación en terminal: pwd, ls, cd, mkdir, touch
- Aprendí el ciclo básico de Git: git init, git add, git commit
- Entendí qué es un README.md y para qué sirve
- Hice mi primer commit en el proyecto git-basico
- Próximo paso: conectar el repo local a GitHub con git push
## Sesion 2 - 9 septiembre 2026
- Aprendí a conectar Github y Git
- Aprendí a utilizar el comando git push
- Instalé y comencé con Python básico 3.14.7
## Sesión 3 - 11 de septiembre
- Aprendí: print(), variables, tipos de datos (str, int, float, bool)
- Aprendí: concatenación de strings (+, str()) y con comas
- Aprendí: operadores matemáticos (incluyendo % y //)
- Aprendí: input() y conversión de tipos (int(), float())
- Aprendí: condicionales if/elif/else
- Aprendí: bucles for (con range()) y while (con condición)
- Entendí el error TypeError y cómo leer un traceback
- Próximo paso: listas
## Sesión 4 - 12 de septiembre
- Aprendí: listas (crear, acceder por índice, len(), append(), recorrer con for)
- Aprendí: diccionarios (crear, acceder por clave, añadir claves, recorrer con for)
- Próximo paso: funciones (def)
## Sesión 5 - 13 de septiembre
- Aprendí: funciones (def, parámetros, return vs print)
- Aprendí: manejo de errores (try/except, ValueError)
- Próximo paso: archivos (leer/escribir), luego Módulo 1 (APIs/HTTP) y JSON
## Sesión 6 - 14 de septiembre
- Aprendí: archivos (open, write, read, modos "w"/"a"/"r", with)
- Completados los fundamentos "puros" de Python
- Próximo paso: Módulo 1 (APIs/HTTP) y JSON
## Sesión 7 - 16 de septiembre
- Aprendi APIs/HTTP/JSON
- Completé: requests (.get(), .status_code, .json())
- Próximo paso: POST, query params con params, autenticación con API keys en headers
## Sesión 8 — 17 de septiembre
- Completado: Módulo 1 (APIs/HTTP/JSON) — API, HTTP (verbos y códigos de estado), 
  JSON, peticiones reales con `requests` (.get(), .status_code, .json()), 
  extracción de datos anidados, query params, POST, API keys/headers
- Próximo paso: retomar Python puro (Fase 1)
## Sesión 9 — 18 de septiembre
- Empecé Módulo 2: n8n
- Instalé Docker Desktop para poder usar n8n
## Sesión 10 — 19 de septiembre
- Instalé n8n
- Aprendí triggers y actions
- Cree mi primer trigger en n8n
## Sesión 11 — 20 de septiembre
- Retomé triggers y actions (repaso desde cero)
- Aprendí a crear un workflow con Manual Trigger + Edit Fields (Set)
- Aprendí que los datos en n8n viajan como listas de JSON (items)
- Aprendí a referenciar datos de un nodo anterior con expresiones ({{ $json.campo }})
- Aprendí el nodo HTTP Request para conectar con una API real
- Aprendí a acceder a JSON anidado (address.city, company.name)
- Aprendí el nodo IF (condición, dos salidas true/false)
- Mini-proyecto: "Verificador de empresa por usuario" (Manual Trigger → HTTP Request → IF → Edit Fields), subido a Proyectos/n8n-verificador-empresa
- Completado Módulo 2 (n8n)
- Próximo paso: IA/prompting con salidas estructuradas
## Sesión 12 — 21 de septiembre
- Retomé el concepto de salidas estructuradas (por qué una IA debe responder en JSON, no en texto libre)
- Configuré Google Gemini API como alternativa gratuita a Anthropic (de pago)
- Setup: .env, .gitignore, python-dotenv, google-genai
- Depuré varios errores reales: módulo no encontrado (pip de versión incorrecta), modelo deprecado, 503 por saturación del servicio
- Hice mi primera llamada real a la API con salida en texto libre
- Aprendí a forzar salida JSON estructurada con Pydantic (BaseModel, response_schema, response_mime_type)
- Proyecto: Proyectos/ia-prompting
- Próximo paso: seguir profundizando en salidas estructuradas (esquemas más complejos, validación de datos)
## Sesión 13 — 22 de septiembre
- Amplié salidas estructuradas: listas dentro del schema (List[str]) y valores limitados (Literal)
- Aprendí la diferencia entre response.text (string crudo) y response.parsed (objeto validado contra el schema)
- Empecé mini-proyecto "Analizador de sentimiento de reseñas" (pendiente de terminar)
- Próximo paso: terminar el mini-proyecto de análisis de sentimiento
## Sesión 14 — 23 de septiembre
- Terminé el mini-proyecto "Analizador de sentimiento de reseñas" (schema Reseñas: sentimiento, resumen, requiere_atencion + bucle for)
- Fase 2 (n8n + IA/prompting con salidas estructuradas) oficialmente completa
- Repasé el criterio de fases: seguir avanzando por fases propias, no por el orden 0-16 del documento, y solo lo esencial dentro de cada fase
- Decidido: antes de Fase 3, construir un proyecto de consolidación que junte n8n + Python + IA de forma más realista (ej. reseñas → clasificación IA → alerta), para afianzar Fases 1-2 y dejar que sea el propio proyecto quien pida SQL/FastAPI/RAG cuando haga falta, no al revés
- Próximo paso: definir y empezar el proyecto de consolidación
## Sesión 15 — 24 de septiembre
- Comienzo de mini proyecto en n8n + IA prompting
- Faltan consolidar partes del proyecto en el workflow
## Sesión 16 — 24 de septiembre
- Definí y construí el proyecto de consolidación: "Gestor de reseñas con alertas automáticas"
- Workflow completo en n8n: Manual Trigger → Edit Fields (reseñas) → AI Agent + Google Gemini Chat Model → Structured Output Parser (JSON forzado) → IF → acción simulada según la rama
- Aprendí a forzar JSON en el nodo AI Agent de n8n (Has Output Parser + Structured Output Parser), sin necesidad de Python/FastAPI
- Decisión consciente de no adelantar Fase 3 (nada de conexiones reales tipo Gmail/Slack, solo simulación de la alerta)
- Proyecto subido a Proyectos/gestor-resenas-n8n
- Próximo paso: sin definir — Fase 3 (SQL, FastAPI, RAG, agentes) queda en espera hasta que un proyecto real la requiera
## Sesión 17 — 26 de septiembre
- Empecé FastAPI como excepción consciente (adelantado de Fase 3, sin esperar proyecto real, por conectar directo con la necesidad real de unir Python + n8n)
- Aprendí el concepto de decorador (@app.get, @app.post) como trigger→action, igual que en n8n
- Monté un servidor básico con uvicorn (ruta GET funcionando en localhost:8000)
- Aprendí a recibir y validar datos con POST usando Pydantic (endpoint /analizar)
- Probé el endpoint desde /docs (documentación automática de FastAPI)
- Próximo paso: conectar /analizar con la lógica real de Gemini, y después con n8n vía HTTP Request
## Sesión 18 — 27 de septiembre
- Conecté el endpoint /analizar de FastAPI con la lógica real de Gemini
- Reforcé conceptos clave: return termina la función (código después nunca se ejecuta), no reutilizar el mismo nombre de variable para cosas distintas, dos schemas separados (uno para lo que entra, otro para lo que la IA genera)
- Endpoint funcionando de punta a punta: texto → análisis con sentimiento/resumen/requiere_atencion
- Próximo paso: conectar /analizar desde n8n con un nodo HTTP Request (cerrar el círculo Python↔n8n)
## Sesión 19 — 28 de septiembre
- Conecté n8n con mi propio servidor FastAPI: nodo HTTP Request (POST) a http://host.docker.internal:8000/analizar
- Aprendí que desde Docker, localhost no apunta a mi PC — hay que usar host.docker.internal
- Depuré un IF que siempre se iba a true: el operador estaba en "exists" en vez de "is true"
- Círculo completo funcionando: n8n → mi servidor Python → Gemini → IF reaccionando bien a true/false
- Próximo paso: sin definir
## Sesión 20 — 29 de septiembre
- Arrancado nuevo proyecto de consolidación: "Sistema de triage automático de tickets de soporte" (FastAPI + Gemini + n8n + histórico de tickets)
- Creado dentro del repo existente ia-prompting, en archivo separado del de reseñas
- Diseñé el schema Ticket (categoria, sentimiento, urgencia, resumen) y TicketEntrada (solo texto)
- Endpoint /tickets funcionando de punta a punta contra Gemini, probado desde /docs con un caso real
- Próximo paso: guardar cada ticket procesado en un histórico (archivo CSV o JSON)
## Sesión 21 — 30 de septiembre
- Aprendí a escribir/añadir archivos con open() (modos "r"/"w"/"a") y with como context manager
- Aprendí el formato JSON Lines (JSONL) para históricos: una línea = un JSON completo
- Usé model_dump_json() de Pydantic para convertir un objeto Ticket a JSON
- Endpoint /tickets ahora guarda cada ticket analizado en tickets_historial.jsonl antes del return
- Cacé y arreglé un bug real de encoding (tildes/ñ corrompidas) añadiendo encoding="utf-8" a open()
- Próximo paso: conectar /tickets con n8n (HTTP Request + IF de urgencia) para cerrar el proyecto
## Sesión 22 — 1 de octubre
- Conecté el endpoint /tickets con n8n mediante un nodo HTTP Request
- Configuré n8n para enviar los tickets al endpoint y recibir la respuesta estructurada de Gemini
- Añadí un nodo IF para comprobar automáticamente la urgencia del ticket
- Configuré la condición para detectar cuándo urgencia == "alta" y separar el flujo según el resultado
- Exporté el workflow de n8n en formato JSON para guardarlo dentro del proyecto y versionarlo con Git
## Sesión 23 — 2 de octubre
- Conecté el Webhook de n8n con mi endpoint /tickets, sustituyendo el Manual Trigger por un disparador real que acepta datos dinámicos
- Usé curl desde Git Bash para simular peticiones externas, con -d @archivo.json en vez de texto directo en el comando (evita un bug de encoding de curl en Windows)
- Entendí que $json.body.texto es necesario (no $json.texto) porque los datos de un Webhook llegan anidados dentro de "body"
- Aprendí que una terminal se queda "ocupada" mientras un servidor corre (uvicorn), y hace falta una segunda terminal para ejecutar otros comandos en paralelo
- Entendí el concepto de Retry on Fail en n8n para manejar fallos temporales de APIs externas (ej: 503 de Gemini), y la importancia de dejar tiempo de espera real entre reintentos
- Entendí (sin implementarlo aún) el patrón "Continue On Fail" + rama de error para no perder tickets si Gemini falla definitivamente, aplazado como siguiente paso
- Entendí el hueco que llena el Webhook en una automatización real: formularios, chatbots o emails reenviando datos automáticamente, aplazado a Fase 4