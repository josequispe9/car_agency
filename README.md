my_project/
│
├── app/                           # Código de la aplicación web
│   ├── _init_.py                # Inicializa la app
│   ├── routes.py                  # Rutas (Flask/Django)
│   ├── views.py                   # Lógica para renderizar las páginas
│   ├── templates/                 # Plantillas HTML (si usas Flask o Django)
│   ├── static/                     # Archivos estáticos (CSS, JS, imágenes)
│   ├── database/                   # Gestión de la base de datos
│   │   ├── _init_.py             # Inicialización
│   │   ├── db_connector.py         # Conexión con MySQL Workbench
│   │   ├── models.py               # Modelos de base de datos con SQLAlchemy
│   │   ├── queries.py              # Funciones para interactuar con la BD
│
├── scraper/                        # Módulo de scraping
│   ├── _init_.py                 # Inicialización del módulo
│   ├── main_scraper.py             # Script principal para orquestar todo
│   ├── sites/                       # Carpeta con los scrapers de cada página
│   │   ├── _init_.py             # Inicializa el paquete
│   │   ├── site1_scraper.py         # Scraper específico de un sitio web
│   │   ├── site2_scraper.py         # Scraper de otro sitio
│   │   ├── site3_scraper.py         # Y así para cada página
│   ├── utils.py                     # Funciones auxiliares para el scraping
│   ├── config.py                    # Configuración general del scraping (User Agents, proxies, etc.)
│   ├── requirements.txt              # Dependencias del scraper (BeautifulSoup, Selenium, Scrapy, etc.)
│
├── ml/                             # Módulo de Machine Learning
│   ├── _init_.py                 # Inicialización
│   ├── train_model.py              # Entrenamiento del modelo ML
│   ├── predict.py                  # Lógica de predicción
│   ├── model.pkl                   # Modelo entrenado
│   ├── utils.py                     # Funciones auxiliares (preprocesamiento, normalización)
│
├── config/                         # Configuración global
│   ├── config.py                   # Parámetros de configuración (BD, API keys, scraping)
│   ├── .env                        # Variables de entorno (credenciales)
│
├── tests/                          # Pruebas unitarias
│   ├── test_scraper.py             # Test para scraper
│   ├── test_ml.py                  # Test para ML
│   ├── test_database.py            # Test para base de datos
│
├── requirements.txt                # Dependencias generales del proyecto
├── .gitignore                      # Archivos a ignorar en Git
├── README.md                       # Documentación del proyecto
└── Dockerfile                      # Archivo para contenedorización (opcional)


# Para crear una nueva rama
git checkout -b feature/scraper develop
git push origin feature/scraper

# Para cambiar de rama 
git checkout feature/scraper

# Cuando termine de trabajar en una rama, fusionar los cambios en develop
git checkout develop
git merge feature/scraper
git push origin develop

# Eliminar ramas obsoletas (rama local - rama remota)
git branch -d feature/scraper
git push origin --delete feature/scraper

# develop: Rama base para nuevas funcionalidades.
# feature/scraper: Desarrollo del scraper.
# feature/ml-model: Desarrollo del modelo de ML.
# feature/web-ui: Desarrollo de la interfaz web.
# docs/update-readme: Actualización de la documentación.
# test/docker-integration: Pruebas de integración con Docker.
# refactor/clean-database-code: Refactorización del código de la base de datos.
# experiment/new-scraping-approach: Experimentación con nuevos enfoques de scraping.
# release/v1.0.0: Preparación para la liberación de la versión 1.0.0.
# hotfix/fix-db-connection: Corrección de errores críticos.