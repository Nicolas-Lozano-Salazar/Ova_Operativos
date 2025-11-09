Este proyecto implementa un servicio REST en Spring Boot que integra una librería nativa (JNI)
para simular el algoritmo de planificación **Round Robin** utilizado en sistemas operativos.


##  Requisitos previos

Antes de ejecutar el proyecto asegúrate de tener instalado:

- **Java 22 o superior**
- **Maven**
- **Docker**

# Proyecto Spring Boot JNI - Round Robin

Para ejecutar el proyecto en local, simplemente usa Docker Compose.

##  Ejecución

1. Abre una terminal en la carpeta del proyecto.
2. Ejecuta el siguiente comando:

   docker compose up

3. Una vez iniciado, el servicio estará disponible en:
   http://localhost:8083

##  Ejemplo de prueba con CURL

```bash
curl -X POST "http://localhost:8083/api/sistemas-operativos/roundrobin/3" \
-H "Content-Type: application/json" \
-d '[
  { "id": 1, "llegada": 0, "rafaga": 5, "prioridad": 2 },
  { "id": 2, "llegada": 1, "rafaga": 3, "prioridad": 1 },
  { "id": 3, "llegada": 2, "rafaga": 8, "prioridad": 3 }
]'
```
Esto devolverá un JSON con los resultados del algoritmo Round Robin.