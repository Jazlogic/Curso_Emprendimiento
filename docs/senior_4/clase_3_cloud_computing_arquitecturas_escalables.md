# Clase 3: Cloud Computing y Arquitecturas Escalables

## Objetivos de la Clase

- Dominar los fundamentos del cloud computing y sus modelos de servicio
- Diseñar arquitecturas escalables y resilientes
- Implementar soluciones de containerización con Docker y Kubernetes
- Optimizar costos y rendimiento en la nube

## Navegación del Módulo

| Clase | Tema | Duración | Tipo |
|-------|------|----------|------|
| 1 | Fundamentos de Transformación Digital | 2 horas | Teórica |
| 2 | Estrategias de Adopción Tecnológica | 2 horas | Teórica |
| 3 | **Cloud Computing y Arquitecturas Escalables** | 3 horas | Práctica |
| 4 | Desarrollo de APIs y Microservicios | 3 horas | Práctica |
| 5 | Inteligencia Artificial y Machine Learning | 3 horas | Práctica |
| 6 | Blockchain y Tecnologías Descentralizadas | 2 horas | Teórica |
| 7 | IoT y Conectividad Empresarial | 2 horas | Teórica |
| 8 | Ciberseguridad y Protección de Datos | 2 horas | Teórica |
| 9 | Gestión de Proyectos Tecnológicos | 2 horas | Teórica |
| 10 | Proyecto Integrador: Plataforma Digital | 4 horas | Práctica |

## Contenido Teórico

### 1. Fundamentos de Cloud Computing

#### 1.1 Modelos de Servicio
- **IaaS (Infrastructure as a Service)**: Infraestructura virtualizada
  - Ejemplos: AWS EC2, Azure VMs, Google Compute Engine
  - Control: Sistema operativo, aplicaciones, datos
  - Responsabilidad: Cliente gestiona todo excepto hardware

- **PaaS (Platform as a Service)**: Plataforma de desarrollo
  - Ejemplos: AWS Elastic Beanstalk, Azure App Service, Google App Engine
  - Control: Aplicaciones y datos
  - Responsabilidad: Proveedor gestiona infraestructura y plataforma

- **SaaS (Software as a Service)**: Software como servicio
  - Ejemplos: Salesforce, Office 365, Google Workspace
  - Control: Solo configuración y datos
  - Responsabilidad: Proveedor gestiona todo

#### 1.2 Modelos de Despliegue
- **Pública**: Recursos compartidos, multi-tenant
- **Privada**: Recursos dedicados, single-tenant
- **Híbrida**: Combinación de nube pública y privada
- **Multi-nube**: Uso de múltiples proveedores

### 2. Principales Proveedores Cloud

#### 2.1 Amazon Web Services (AWS)
- **Servicios Principales**:
  - EC2: Servidores virtuales
  - S3: Almacenamiento de objetos
  - RDS: Bases de datos gestionadas
  - Lambda: Funciones sin servidor
  - VPC: Red privada virtual

#### 2.2 Microsoft Azure
- **Servicios Principales**:
  - Virtual Machines: Servidores virtuales
  - Blob Storage: Almacenamiento de objetos
  - SQL Database: Base de datos SQL
  - Functions: Funciones sin servidor
  - Virtual Network: Red virtual

#### 2.3 Google Cloud Platform (GCP)
- **Servicios Principales**:
  - Compute Engine: Servidores virtuales
  - Cloud Storage: Almacenamiento de objetos
  - Cloud SQL: Base de datos SQL
  - Cloud Functions: Funciones sin servidor
  - VPC: Red privada virtual

### 3. Arquitecturas Escalables

#### 3.1 Principios de Escalabilidad
- **Escalabilidad Horizontal**: Agregar más servidores
- **Escalabilidad Vertical**: Aumentar recursos del servidor
- **Auto-scaling**: Escalado automático basado en demanda
- **Load Balancing**: Distribución de carga entre servidores

#### 3.2 Patrones de Arquitectura
- **Monolítica**: Aplicación única y cohesiva
- **Microservicios**: Aplicación como conjunto de servicios
- **Serverless**: Ejecución de código sin gestión de servidores
- **Event-driven**: Arquitectura basada en eventos

#### 3.3 Arquitectura de Microservicios
```
┌─────────────┐    ┌─────────────┐    ┌─────────────┐
│   Frontend  │    │   API       │    │  Database   │
│   (React)   │◄──►│   Gateway   │◄──►│  (PostgreSQL)│
└─────────────┘    └─────────────┘    └─────────────┘
                           │
                    ┌──────┴──────┐
                    │             │
            ┌───────▼──────┐ ┌────▼──────┐
            │   Service A  │ │  Service B │
            │   (Node.js)  │ │  (Python)  │
            └──────────────┘ └───────────┘
```

### 4. Containerización con Docker

#### 4.1 Conceptos de Docker
- **Container**: Entorno aislado para ejecutar aplicaciones
- **Image**: Plantilla para crear containers
- **Dockerfile**: Archivo de configuración para crear imágenes
- **Registry**: Repositorio de imágenes Docker

#### 4.2 Dockerfile Básico
```dockerfile
# Usar imagen base de Node.js
FROM node:18-alpine

# Establecer directorio de trabajo
WORKDIR /app

# Copiar archivos de dependencias
COPY package*.json ./

# Instalar dependencias
RUN npm install

# Copiar código fuente
COPY . .

# Exponer puerto
EXPOSE 3000

# Comando para ejecutar la aplicación
CMD ["npm", "start"]
```

#### 4.3 Docker Compose
```yaml
version: '3.8'
services:
  web:
    build: .
    ports:
      - "3000:3000"
    environment:
      - NODE_ENV=production
    depends_on:
      - db
  
  db:
    image: postgres:13
    environment:
      - POSTGRES_DB=myapp
      - POSTGRES_USER=user
      - POSTGRES_PASSWORD=password
    volumes:
      - postgres_data:/var/lib/postgresql/data

volumes:
  postgres_data:
```

### 5. Orquestación con Kubernetes

#### 5.1 Conceptos de Kubernetes
- **Pod**: Unidad más pequeña de despliegue
- **Service**: Punto de acceso estable a un conjunto de pods
- **Deployment**: Gestión de réplicas de pods
- **Namespace**: Agrupación lógica de recursos

#### 5.2 YAML de Deployment
```yaml
apiVersion: apps/v1
kind: Deployment
metadata:
  name: my-app
spec:
  replicas: 3
  selector:
    matchLabels:
      app: my-app
  template:
    metadata:
      labels:
        app: my-app
    spec:
      containers:
      - name: my-app
        image: my-app:latest
        ports:
        - containerPort: 3000
        env:
        - name: NODE_ENV
          value: "production"
```

#### 5.3 YAML de Service
```yaml
apiVersion: v1
kind: Service
metadata:
  name: my-app-service
spec:
  selector:
    app: my-app
  ports:
  - protocol: TCP
    port: 80
    targetPort: 3000
  type: LoadBalancer
```

### 6. Optimización de Costos en la Nube

#### 6.1 Estrategias de Optimización
- **Right-sizing**: Dimensionar recursos según necesidades reales
- **Reserved Instances**: Compromiso a largo plazo por descuentos
- **Spot Instances**: Uso de capacidad no utilizada
- **Auto-scaling**: Ajustar recursos según demanda

#### 6.2 Monitoreo y Métricas
- **CloudWatch (AWS)**: Monitoreo y logging
- **Azure Monitor**: Monitoreo y análisis
- **Google Cloud Monitoring**: Observabilidad y alertas
- **Cost Management**: Herramientas de gestión de costos

## Ejercicios Prácticos

### Ejercicio 1: Configuración de Infraestructura Cloud
**Objetivo**: Crear una infraestructura básica en la nube

**Instrucciones**:
1. Crea una cuenta en AWS/Azure/GCP (nivel gratuito)
2. Configura una instancia virtual básica
3. Instala y configura un servidor web
4. Despliega una aplicación simple

**Entregables**:
- Captura de pantalla de la instancia creada
- URL de la aplicación desplegada
- Documentación del proceso

### Ejercicio 2: Containerización con Docker
**Objetivo**: Containerizar una aplicación web

**Instrucciones**:
1. Crea un Dockerfile para tu aplicación
2. Construye la imagen Docker
3. Ejecuta el container
4. Configura Docker Compose para múltiples servicios

**Código de Ejemplo**:
```dockerfile
FROM node:18-alpine
WORKDIR /app
COPY package*.json ./
RUN npm install
COPY . .
EXPOSE 3000
CMD ["npm", "start"]
```

### Ejercicio 3: Despliegue en Kubernetes
**Objetivo**: Desplegar una aplicación en Kubernetes

**Instrucciones**:
1. Configura un cluster de Kubernetes local (minikube)
2. Crea los archivos YAML de deployment y service
3. Despliega la aplicación
4. Verifica el funcionamiento

**Comandos Básicos**:
```bash
# Iniciar minikube
minikube start

# Desplegar aplicación
kubectl apply -f deployment.yaml
kubectl apply -f service.yaml

# Verificar estado
kubectl get pods
kubectl get services
```

## Conceptos Clave

- **Cloud Computing**: Computación como servicio
- **IaaS/PaaS/SaaS**: Modelos de servicio cloud
- **Microservicios**: Arquitectura de servicios independientes
- **Docker**: Containerización de aplicaciones
- **Kubernetes**: Orquestación de containers
- **Auto-scaling**: Escalado automático de recursos

## Preguntas de Repaso

1. ¿Cuáles son las ventajas del cloud computing sobre infraestructura tradicional?
2. ¿Cómo se diferencia la escalabilidad horizontal de la vertical?
3. ¿Qué beneficios ofrece la containerización con Docker?
4. ¿Cuál es el papel de Kubernetes en la orquestación de containers?
5. ¿Cómo se puede optimizar los costos en la nube?

## Próximos Pasos

1. **Practicar** con los ejercicios de Docker y Kubernetes
2. **Explorar** los servicios de tu proveedor cloud preferido
3. **Diseñar** una arquitectura escalable para tu proyecto
4. **Implementar** una solución cloud básica

## Recursos Adicionales

### Documentación Oficial
- **AWS**: https://docs.aws.amazon.com/
- **Azure**: https://docs.microsoft.com/azure/
- **Google Cloud**: https://cloud.google.com/docs
- **Docker**: https://docs.docker.com/
- **Kubernetes**: https://kubernetes.io/docs/

### Cursos Online
- **AWS Certified Solutions Architect**
- **Azure Fundamentals**
- **Google Cloud Professional Developer**
- **Docker for Developers**
- **Kubernetes for Beginners**

### Herramientas
- **Terraform**: Infrastructure as Code
- **Ansible**: Automatización de configuración
- **Helm**: Gestión de paquetes en Kubernetes
- **Prometheus**: Monitoreo y alertas

---

**¡Siguiente Clase!** 🚀
En la próxima clase aprenderás sobre **Desarrollo de APIs y Microservicios** y cómo crear arquitecturas de servicios robustas.
