# 🐳 Ejercicio Práctico de Docker CLI 

En este ejercicio pondrás en práctica los comandos esenciales de Docker para gestionar **imágenes**, **contenedores** y crear tu **primera imagen personalizada**.  

Tu misión es completar los comandos faltantes en cada paso. 🚀  

---

## 🔹 Parte 1: Gestión de Imágenes y Contenedores

### 1. Ver imágenes existentes
Muestra las imágenes que tienes en tu máquina local:  
```bash
docker ______
```

### 2. Descargar Ubuntu
Descarga la última imagen oficial de Ubuntu desde Docker Hub:  
```bash
docker ____ ubuntu
```

### 3. Ejecutar un contenedor Ubuntu
Ejecuta un contenedor basado en Ubuntu:  
```bash
docker ___ ubuntu
```
👉 Observa qué ocurre con el contenedor.

### 4. Ejecutar NGINX en segundo plano
Inicia un contenedor llamado **web_server** en modo *detached* (en segundo plano), mapeando el puerto **80** del host al **80** del contenedor:  
```bash
docker run __ --name web_server -p 80:80 nginx
```

### 5. Ver contenedores activos y detenidos
- Solo contenedores activos:  
```bash
docker __
```

- Todos los contenedores (activos + detenidos):  
```bash
docker __ -a
```

### 6. Manejo de contenedores
- Iniciar un contenedor detenido:  
```bash
docker start <________>
```

- Detener un contenedor en ejecución:  
```bash
docker ____ <________>
```

- Eliminar un contenedor que ya no necesitas:  
```bash
docker __ <________>
```

### 7. Filtrar y limpiar
- Buscar un contenedor específico por nombre (**web_server**):  
```bash
docker ps --filter "name=________"
```

- Detener todos los contenedores en ejecución:  
```bash
docker stop $(docker ps -__)
```

- Eliminar todos los contenedores detenidos:  
```bash
docker rm $(docker ps -a -__)
```

---

## 🔹 Parte 2: Interacción y Creación de Imágenes

### 8. Ver registros del contenedor NGINX
- Mostrar logs del contenedor **web_server**:  
```bash
docker logs _________
```

- Seguir logs en tiempo real:  
```bash
docker logs __ _________
```

### 9. Ejecutar comandos dentro del contenedor
Abre una shell dentro del contenedor **web_server**:  
```bash
docker exec -__ web_server __
```

### 10. Crear tu primera imagen personalizada
1. Crea un archivo llamado **Dockerfile** con este contenido:
   ```dockerfile
   FROM ubuntu:latest
   CMD ["echo", "¡Hola desde mi primera imagen Docker!"]
   ```

2. Construye la imagen con el nombre `mi_primer_imagen`:  
```bash
docker build -t _____________ .
```

3. Ejecuta tu nueva imagen:  
```bash
docker run ______________
```

---

## 🎯 Conclusión
Has practicado cómo:  
✅ Gestionar imágenes y contenedores con la CLI.  
✅ Iniciar, detener y eliminar contenedores.  
✅ Ver logs y ejecutar comandos dentro de un contenedor.  
✅ Crear tu primera imagen Docker personalizada.  

Ahora ya tienes la base para seguir profundizando en Docker. ¡Éxitos! 🐳🚀
