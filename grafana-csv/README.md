# Servicio de Grafana con soporte para CSV

Este directorio contiene un ejemplo de configuración para ejecutar Grafana en un contenedor Docker y cargar datos desde un archivo CSV.

## Contenido

- `docker-compose.yml`: define el servicio de Grafana y monta la carpeta `csv` con los datos.
- `provisioning/datasources/datasource.yaml`: configura automáticamente una fuente de datos basada en el plugin CSV.
- `csv/sample.csv`: archivo de ejemplo con datos que se usarán en la visualización.

## Uso

1. Instalar Docker y Docker Compose.
2. Desde este directorio ejecutar:

```bash
docker-compose up -d
```

3. Abrir [http://localhost:3000](http://localhost:3000) en el navegador. Usuario y contraseña por defecto: `admin` / `admin`.
4. Grafana cargará el plugin `marcusolsson-csv-datasource` e incluirá una fuente de datos llamada **CSV Data** que apunta al archivo `csv/sample.csv`.
5. Crear un dashboard y seleccionar la fuente de datos **CSV Data** para visualizar la información del archivo.

Este ejemplo se basa en los pasos discutidos en el chat compartido.
