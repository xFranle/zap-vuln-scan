# Automatización de Análisis de Vulnerabilidades Web con OWASP ZAP y Python

## Descripción
Este proyecto automatiza el análisis de vulnerabilidades en aplicaciones web utilizando OWASP ZAP y Python. El objetivo es identificar y reportar vulnerabilidades comunes de manera eficiente, mejorando la seguridad de las aplicaciones web mediante la integración de un escaneo de seguridad automatizado.

## Tecnologias utilizadas
- OWASP ZAP
- Python
- Biblioteca `requests`

## Instalación
1. Instalar OWASP ZAP desde [aquí](https://www.zaproxy.org/download/).
2. Clonar este repositorio:
    ```sh
    git clone https://github.com/xFranle/zap-vuln-scan.git
    ```
3. Instalar las dependencias en Python:
    ```sh
    pip install requests
    ```

## Uso
1. Configurar la API Key de OWASP ZAP en el script `zap_scan.py` si es necesario.
2. Ejecutar OWASP ZAP en modo daemon:
    ```sh
    zap.sh -daemon -port 8080 -config api.disablekey=true
    ```
    O si usas una API Key:
    ```sh
    zap.sh -daemon -port 8080 -config api.key=tu_api_key
    ```
3. Ejecutar el script:
    ```sh
    python zap_scan.py
    ```
4. El reporte de vulnerabilidades se generará en `reporte_vulnerabilidades.json`.
