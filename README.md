# ⚽ El DT
> **El Orquestador Definitivo & Project Manager**
Bienvenido a **El DT** (El Director Técnico). Este proyecto sirve como un centro de comando central para orquestar flujos de trabajo, gestionar tareas y asegurar que tu equipo juegue como verdaderos campeones.
---
## 🚀 Visión General
**El DT** está diseñado para poner orden en el caos. Tal como un director técnico desde la línea de banda, esta herramienta te ayuda a:
- **Orquestar** flujos de trabajo complejos.
- **Gestionar** las tareas del proyecto y los tiempos.
- **Dirigir** tu estrategia de desarrollo con precisión.
## 🤖 Task Master y Configuración MCP
Para maximizar la capacidad de "El DT", integramos **Task Master** a través del Model Context Protocol (MCP). Esto permite una gestión inteligente de tareas y contexto.
### Instalación de Task Master
Sigue estos pasos para instalar y configurar correctamente el servidor MCP de Task Master:
1.  **Clonar el Repositorio**
    Necesitas clonar el repositorio de Task Master en tu máquina local (preferiblemente en una carpeta hermana a este proyecto).
    ```bash
    git clone https://github.com/eyaltoledano/claude-task-master.git
    cd claude-task-master
    npm install
    npm run build
    ```
    > **Nota:** Verifica que este sea el repositorio correcto de Task Master que utiliza tu equipo.
2.  **Configuración de API Keys**
    El servidor requiere credenciales para interactuar con los modelos. Crea un archivo `.env` en la raíz del directorio de `claude-task-master` copiando el ejemplo:
    ```bash
    cp .env.example .env
    ```
    Asegúrate de definir tus claves, especialmente si usas proveedores externos:
    ```env
    OPENAI_API_KEY=sk-...
    # O cualquier otra clave requerida por tu configuración de Task Master
    ```
3.  **Configurar el Cliente MCP**
    Para usarlo en Claude Desktop o tu IDE compatible (como Cursor), edita tu archivo de configuración (ej. `claude_desktop_config.json`):
    ```json
    {
      "mcpServers": {
        "task-master-ai": {
          "command": "node",
          "args": ["/ruta/absoluta/a/claude-task-master/build/index.js"],
          "env": {
             "NODE_ENV": "production"
          }
        }
      }
    }
    ```
    *Asegúrate de reemplazar `/ruta/absoluta/a/` con la ruta real en tu sistema.*
## 📂 Documentación y Seguridad
Nos tomamos la seguridad muy en serio. Toda la documentación sensible se mantiene fuera del control de versiones.
### Manejo de Datos Sensibles
Si necesitas agregar configuración o documentación confidencial:
1.  Navega a la carpeta `docs/`.
2.  **NO HAGAS COMMIT** de archivos con secretos reales.
3.  Usa `docs/SENSITIVE_DATA_TEMPLATE.md` como guía.
4.  Cualquier archivo en `docs/` es ignorado por `.gitignore` por defecto, *excepto* las plantillas.
## 🛠️ Comenzando (Getting Started)
1.  **Clonar este repositorio**
    ```bash
    git clone https://github.com/Mazalucas/El-DT.git
    ```
2.  **Configurar Entorno**
    Revisa el archivo `.env.example` y crea tu propio archivo `.env` en la raíz de "El DT".
3.  **Ejecutar el Orquestador**
    *(Instrucciones de ejecución pendientes)*
## 🤝 Contribuyendo
¡Damos la bienvenida a nuevos jugadores a la plantilla! Por favor, revisa la pestaña de *issues* y envía un Pull Request.
---
*Construido con ❤️ por @LucasMazalan & el Equipo de El DT*
