# Drive Shortcuts Manager

Este repositorio incluye un cuaderno de Google Colab (`docs_proyectos_activación_accesos_directos.ipynb`) que automatiza la activación y gestión de accesos a documentación de proyectos en Google Drive:

- **Lectura de CSV** con columnas `ticket_id`, `ticket_title`, `ticket_user`, `url`
- **Creación de carpetas** por proyecto en la unidad indicada
- **Generación de shortcuts** a cada URL (docs o folders)
- **Compartición de permisos**: asigna rol _reader_ a usuarios sobre recursos destino y shortcuts
- **Manejo de errores**: registra URLs sin acceso en `urls-sin-acceso.txt`
- **Orden y control**: procesa subcarpetas alfabéticamente y evita duplicados

## Requisitos

- Python 3.8+ (solo para dependencias, si se ejecuta local)
- Google Colab y cuenta Workspace con permisos de Drive API
- Librerías (si es local):
  ```bash
  pip install google-auth-oauthlib google-api-python-client pandas
  ```

## Uso en Colab

1. Abre el cuaderno en Colab.
2. Monta Drive y fija `ROOT_FOLDER_ID` (ID de la carpeta raíz donde crearás proyectos).
3. Ajusta la lista de proyectos y su documentación en la celda de configuración.
4. Ejecuta todas las celdas.

## Licencia

MIT © 2025
