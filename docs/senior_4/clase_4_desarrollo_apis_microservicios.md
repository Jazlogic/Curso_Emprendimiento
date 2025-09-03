# Clase 4: Desarrollo de APIs y Microservicios

## Objetivos de la Clase

- Dominar el diseño y desarrollo de APIs RESTful y GraphQL
- Implementar arquitecturas de microservicios robustas
- Gestionar la comunicación entre servicios y el manejo de datos
- Implementar monitoreo y observabilidad en sistemas distribuidos

## Navegación del Módulo

| Clase | Tema | Duración | Tipo |
|-------|------|----------|------|
| 1 | Fundamentos de Transformación Digital | 2 horas | Teórica |
| 2 | Estrategias de Adopción Tecnológica | 2 horas | Teórica |
| 3 | Cloud Computing y Arquitecturas Escalables | 3 horas | Práctica |
| 4 | **Desarrollo de APIs y Microservicios** | 3 horas | Práctica |
| 5 | Inteligencia Artificial y Machine Learning | 3 horas | Práctica |
| 6 | Blockchain y Tecnologías Descentralizadas | 2 horas | Teórica |
| 7 | IoT y Conectividad Empresarial | 2 horas | Teórica |
| 8 | Ciberseguridad y Protección de Datos | 2 horas | Teórica |
| 9 | Gestión de Proyectos Tecnológicos | 2 horas | Teórica |
| 10 | Proyecto Integrador: Plataforma Digital | 4 horas | Práctica |

## Contenido Teórico

### 1. Fundamentos de APIs

#### 1.1 ¿Qué es una API?
Una API (Application Programming Interface) es un conjunto de reglas y protocolos que permite que diferentes aplicaciones se comuniquen entre sí. Actúa como intermediario entre el frontend y el backend, facilitando el intercambio de datos.

#### 1.2 Tipos de APIs
- **REST (Representational State Transfer)**: Arquitectura basada en HTTP
- **GraphQL**: Lenguaje de consulta y manipulación de datos
- **SOAP**: Protocolo basado en XML
- **gRPC**: Framework de comunicación de alto rendimiento

#### 1.3 Principios REST
- **Stateless**: Cada petición es independiente
- **Client-Server**: Separación de responsabilidades
- **Cacheable**: Respuestas pueden ser cacheadas
- **Uniform Interface**: Interfaz consistente
- **Layered System**: Arquitectura en capas

### 2. Diseño de APIs RESTful

#### 2.1 Convenciones de Nomenclatura
```
GET    /api/users          # Obtener todos los usuarios
GET    /api/users/123      # Obtener usuario específico
POST   /api/users          # Crear nuevo usuario
PUT    /api/users/123      # Actualizar usuario completo
PATCH  /api/users/123      # Actualizar usuario parcial
DELETE /api/users/123      # Eliminar usuario
```

#### 2.2 Códigos de Estado HTTP
- **2xx Success**: 200 (OK), 201 (Created), 204 (No Content)
- **4xx Client Error**: 400 (Bad Request), 401 (Unauthorized), 404 (Not Found)
- **5xx Server Error**: 500 (Internal Server Error), 502 (Bad Gateway)

#### 2.3 Estructura de Respuesta
```json
{
  "status": "success",
  "data": {
    "id": 123,
    "name": "Juan Pérez",
    "email": "juan@example.com"
  },
  "message": "Usuario obtenido exitosamente",
  "timestamp": "2024-01-15T10:30:00Z"
}
```

### 3. GraphQL

#### 3.1 Conceptos Básicos
- **Schema**: Definición de tipos y operaciones
- **Query**: Consulta de datos
- **Mutation**: Modificación de datos
- **Subscription**: Actualizaciones en tiempo real

#### 3.2 Schema de Ejemplo
```graphql
type User {
  id: ID!
  name: String!
  email: String!
  posts: [Post!]!
}

type Post {
  id: ID!
  title: String!
  content: String!
  author: User!
}

type Query {
  user(id: ID!): User
  users: [User!]!
  post(id: ID!): Post
  posts: [Post!]!
}

type Mutation {
  createUser(name: String!, email: String!): User!
  updateUser(id: ID!, name: String, email: String): User!
  deleteUser(id: ID!): Boolean!
}
```

#### 3.3 Query de Ejemplo
```graphql
query GetUserWithPosts($userId: ID!) {
  user(id: $userId) {
    id
    name
    email
    posts {
      id
      title
      content
    }
  }
}
```

### 4. Arquitectura de Microservicios

#### 4.1 Características de Microservicios
- **Independencia**: Cada servicio es independiente
- **Escalabilidad**: Escalado individual por servicio
- **Tecnología**: Diferentes tecnologías por servicio
- **Despliegue**: Despliegue independiente
- **Falla**: Aislamiento de fallas

#### 4.2 Patrones de Comunicación
- **Síncrona**: HTTP/REST, gRPC
- **Asíncrona**: Message Queues, Event Streaming
- **Híbrida**: Combinación de ambos enfoques

#### 4.3 Arquitectura de Ejemplo
```
┌─────────────┐    ┌─────────────┐    ┌─────────────┐
│   Frontend  │    │   API       │    │  Database   │
│   (React)   │◄──►│   Gateway   │◄──►│  (PostgreSQL)│
└─────────────┘    └─────────────┘    └─────────────┘
                           │
                    ┌──────┴──────┐
                    │             │
            ┌───────▼──────┐ ┌────▼──────┐
            │   User       │ │  Product  │
            │   Service    │ │  Service  │
            │   (Node.js)  │ │  (Python) │
            └──────────────┘ └───────────┘
```

### 5. Gestión de Datos en Microservicios

#### 5.1 Patrones de Datos
- **Database per Service**: Cada servicio tiene su propia base de datos
- **Shared Database**: Base de datos compartida (anti-patrón)
- **Saga Pattern**: Transacciones distribuidas
- **CQRS**: Separación de comandos y consultas

#### 5.2 Consistencia de Datos
- **Eventual Consistency**: Consistencia eventual
- **Strong Consistency**: Consistencia fuerte
- **Event Sourcing**: Almacenamiento de eventos
- **Compensating Transactions**: Transacciones compensatorias

### 6. Monitoreo y Observabilidad

#### 6.1 Tres Pilares de Observabilidad
- **Logs**: Registros de eventos
- **Metrics**: Medidas cuantitativas
- **Traces**: Seguimiento de requests

#### 6.2 Herramientas de Monitoreo
- **APM**: New Relic, Datadog, AppDynamics
- **Logging**: ELK Stack, Splunk, Fluentd
- **Metrics**: Prometheus, Grafana, InfluxDB
- **Tracing**: Jaeger, Zipkin, OpenTelemetry

## Ejercicios Prácticos

### Ejercicio 1: API RESTful con Node.js
**Objetivo**: Crear una API RESTful completa

**Instrucciones**:
1. Crea un proyecto Node.js con Express
2. Implementa endpoints CRUD para usuarios
3. Agrega validación de datos
4. Implementa autenticación JWT

**Código de Ejemplo**:
```javascript
const express = require('express');
const app = express();

// Middleware
app.use(express.json());

// Rutas
app.get('/api/users', (req, res) => {
  res.json({ users: [] });
});

app.post('/api/users', (req, res) => {
  const { name, email } = req.body;
  // Validación y creación de usuario
  res.status(201).json({ message: 'Usuario creado' });
});

app.listen(3000, () => {
  console.log('Servidor corriendo en puerto 3000');
});
```

### Ejercicio 2: API GraphQL con Apollo Server
**Objetivo**: Implementar una API GraphQL

**Instrucciones**:
1. Configura Apollo Server
2. Define el schema GraphQL
3. Implementa resolvers
4. Agrega mutaciones y queries

**Código de Ejemplo**:
```javascript
const { ApolloServer, gql } = require('apollo-server');

const typeDefs = gql`
  type User {
    id: ID!
    name: String!
    email: String!
  }

  type Query {
    users: [User!]!
    user(id: ID!): User
  }
`;

const resolvers = {
  Query: {
    users: () => [],
    user: (_, { id }) => ({ id, name: 'Juan', email: 'juan@example.com' })
  }
};

const server = new ApolloServer({ typeDefs, resolvers });

server.listen().then(({ url }) => {
  console.log(`Servidor GraphQL en ${url}`);
});
```

### Ejercicio 3: Microservicio con Docker
**Objetivo**: Containerizar un microservicio

**Instrucciones**:
1. Crea un microservicio simple
2. Escribe un Dockerfile
3. Configura Docker Compose
4. Despliega con Kubernetes

**Dockerfile**:
```dockerfile
FROM node:18-alpine
WORKDIR /app
COPY package*.json ./
RUN npm install
COPY . .
EXPOSE 3000
CMD ["npm", "start"]
```

**Docker Compose**:
```yaml
version: '3.8'
services:
  user-service:
    build: ./user-service
    ports:
      - "3001:3000"
    environment:
      - NODE_ENV=production
  
  product-service:
    build: ./product-service
    ports:
      - "3002:3000"
    environment:
      - NODE_ENV=production
```

## Conceptos Clave

- **API**: Interfaz de programación de aplicaciones
- **REST**: Arquitectura de servicios web
- **GraphQL**: Lenguaje de consulta de datos
- **Microservicios**: Arquitectura de servicios independientes
- **Observabilidad**: Monitoreo de sistemas distribuidos
- **Containerización**: Empaquetado de aplicaciones

## Preguntas de Repaso

1. ¿Cuáles son las ventajas de GraphQL sobre REST?
2. ¿Cómo se maneja la consistencia de datos en microservicios?
3. ¿Qué es la observabilidad y por qué es importante?
4. ¿Cuáles son los patrones de comunicación entre microservicios?
5. ¿Cómo se implementa la autenticación en APIs?

## Próximos Pasos

1. **Practicar** con los ejercicios de APIs
2. **Explorar** frameworks como Express, FastAPI, Spring Boot
3. **Implementar** un microservicio completo
4. **Configurar** monitoreo y logging

## Recursos Adicionales

### Frameworks y Librerías
- **Node.js**: Express, Fastify, Koa
- **Python**: FastAPI, Django REST, Flask
- **Java**: Spring Boot, Micronaut
- **C#**: ASP.NET Core, Nancy
- **Go**: Gin, Echo, Fiber

### Herramientas de Desarrollo
- **Postman**: Testing de APIs
- **Insomnia**: Cliente REST alternativo
- **GraphQL Playground**: IDE para GraphQL
- **Swagger/OpenAPI**: Documentación de APIs

### Documentación
- **REST API Design**: https://restfulapi.net/
- **GraphQL**: https://graphql.org/
- **Microservices Patterns**: https://microservices.io/
- **OpenAPI Specification**: https://swagger.io/specification/

---

**¡Siguiente Clase!** 🚀
En la próxima clase aprenderás sobre **Inteligencia Artificial y Machine Learning** y cómo implementar soluciones de IA en tu negocio.
