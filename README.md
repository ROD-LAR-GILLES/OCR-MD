# 📄➡️📝 OCR-MD

**OCR-MD** es una aplicación web moderna que convierte documentos PDF (digitales o escaneados) en archivos Markdown de forma automática y eficiente. Combina tecnologías de OCR avanzadas con una interfaz web intuitiva para ofrecer una experiencia completa de conversión de documentos.

##  Características Principales

- **OCR Inteligente**: Extrae texto y tablas de PDFs usando Tesseract y pdfplumber
- **Detección de Tablas**: Reconoce y convierte tablas automáticamente a formato Markdown
- **API REST**: Backend robusto con FastAPI para procesamiento eficiente
- **Interfaz Moderna**: Frontend responsive desarrollado con React + Vite
- **Completamente Dockerizado**: Fácil despliegue con Docker Compose
- **Gestión de Archivos**: Sistema de carpetas compartidas para resultados
- **Procesamiento Rápido**: Optimizado para documentos de diferentes tamaños

## 🛠️ Stack Tecnológico

| Capa | Tecnologías |
|------|-------------|
| **Frontend** | React 19, Vite, ESLint |
| **Backend** | Python, FastAPI, Tesseract OCR, pdfplumber |
| **Containerización** | Docker, Docker Compose |
| **Desarrollo** | Node.js 20, npm |

## 📁 Estructura del Proyecto

```
OCR-MD/
├── backend/
│   ├── Dockerfile
│   ├── requirements.txt
│   └── app/
│       ├── main.py
│       ├── ocr.py
│       ├── markdown_converter.py
│       └── routes.py
├── frontend/
│   ├── Dockerfile
│   ├── package.json
│   ├── index.html
│   ├── vite.config.js
│   └── src/
│       ├── App.jsx
│       ├── App.css
│       ├── main.jsx
│       └── assets/
├── shared/
├── docker-compose.yml
└── README.md
```

## Inicio Rápido

### Prerequisitos

- Docker y Docker Compose instalados
- Git

### Instalación y Ejecución

1. **Clona el repositorio**
   ```bash
   git clone https://github.com/tu-usuario/OCR-MD.git
   cd OCR-MD
   ```

2. **Ejecuta con Docker Compose**
   ```bash
   docker compose up --build
   ```

3. **Accede a la aplicación**
   - Frontend: http://localhost:5173
   - API Backend: http://localhost:8000 (cuando esté configurado)

### Uso Local (Desarrollo)

**Frontend:**
```bash
cd frontend
npm install
npm run dev
```

**Backend:**
```bash
cd backend
pip install -r requirements.txt
python app/main.py
```

## Cómo Usar

1. **Sube tu PDF**: Arrastra y suelta o selecciona tu archivo PDF
2. **Procesa**: La aplicación extraerá automáticamente el texto y las tablas
3. **Descarga**: Obtén tu archivo Markdown convertido desde la carpeta `shared/`

## 🔧 Configuración

Los archivos de configuración principales incluyen:

- [`docker-compose.yml`](docker-compose.yml): Orquestación de servicios
- [`frontend/vite.config.js`](frontend/vite.config.js): Configuración de Vite
- [`frontend/package.json`](frontend/package.json): Dependencias del frontend
- [`backend/requirements.txt`](backend/requirements.txt): Dependencias de Python

## Licencia

Este proyecto está bajo la Licencia MIT. Ver el archivo `LICENSE` para más detalles.

