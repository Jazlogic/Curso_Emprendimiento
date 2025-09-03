# Clase 10: Proyecto Integrador - Plataforma Digital

## Objetivos de la Clase

- Desarrollar una plataforma digital completa integrando múltiples tecnologías
- Implementar arquitectura escalable con microservicios
- Desplegar la solución en la nube con monitoreo
- Documentar y presentar el proyecto final

## Navegación del Módulo

| Clase | Tema | Duración | Tipo |
|-------|------|----------|------|
| 1 | Fundamentos de Transformación Digital | 2 horas | Teórica |
| 2 | Estrategias de Adopción Tecnológica | 2 horas | Teórica |
| 3 | Cloud Computing y Arquitecturas Escalables | 3 horas | Práctica |
| 4 | Desarrollo de APIs y Microservicios | 3 horas | Práctica |
| 5 | Inteligencia Artificial y Machine Learning | 3 horas | Práctica |
| 6 | Blockchain y Tecnologías Descentralizadas | 2 horas | Teórica |
| 7 | IoT y Conectividad Empresarial | 2 horas | Teórica |
| 8 | Ciberseguridad y Protección de Datos | 2 horas | Teórica |
| 9 | Gestión de Proyectos Tecnológicos | 2 horas | Teórica |
| 10 | **Proyecto Integrador: Plataforma Digital** | 4 horas | Práctica |

## Descripción del Proyecto

### Objetivo General
Desarrollar una plataforma digital empresarial que integre las tecnologías aprendidas en el módulo, demostrando competencias en transformación digital, arquitecturas escalables, desarrollo de APIs, inteligencia artificial, y gestión de proyectos tecnológicos.

### Alcance del Proyecto
- **Frontend**: Aplicación web moderna y responsive
- **Backend**: Arquitectura de microservicios
- **Base de Datos**: Almacenamiento escalable
- **Cloud**: Despliegue en plataforma cloud
- **IA/ML**: Funcionalidades inteligentes
- **Monitoreo**: Observabilidad y métricas
- **Seguridad**: Implementación de medidas de seguridad

## Arquitectura del Proyecto

### 1. Arquitectura General
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
                    │             │
            ┌───────▼──────┐ ┌────▼──────┐
            │  AI/ML       │ │  Analytics│
            │  Service     │ │  Service  │
            │  (Python)    │ │  (Node.js)│
            └──────────────┘ └───────────┘
```

### 2. Componentes del Sistema

#### 2.1 Frontend (React)
- **Dashboard**: Panel de control principal
- **Gestión de Usuarios**: CRUD de usuarios
- **Gestión de Productos**: CRUD de productos
- **Analytics**: Visualización de datos
- **Configuración**: Configuración del sistema

#### 2.2 Backend (Microservicios)
- **API Gateway**: Punto de entrada único
- **User Service**: Gestión de usuarios y autenticación
- **Product Service**: Gestión de productos
- **AI/ML Service**: Funcionalidades de inteligencia artificial
- **Analytics Service**: Análisis de datos

#### 2.3 Base de Datos
- **PostgreSQL**: Base de datos principal
- **Redis**: Cache y sesiones
- **MongoDB**: Datos no estructurados

#### 2.4 Infraestructura
- **Docker**: Containerización
- **Kubernetes**: Orquestación
- **Cloud Provider**: AWS/Azure/GCP
- **CI/CD**: Pipeline de despliegue

## Especificaciones Técnicas

### 1. Frontend
```javascript
// Estructura del proyecto React
src/
├── components/
│   ├── Dashboard/
│   ├── Users/
│   ├── Products/
│   └── Analytics/
├── services/
│   ├── api.js
│   └── auth.js
├── hooks/
│   ├── useAuth.js
│   └── useApi.js
└── utils/
    ├── constants.js
    └── helpers.js
```

### 2. Backend - User Service
```javascript
// Estructura del microservicio de usuarios
src/
├── controllers/
│   └── userController.js
├── models/
│   └── User.js
├── routes/
│   └── userRoutes.js
├── middleware/
│   ├── auth.js
│   └── validation.js
└── services/
    └── userService.js
```

### 3. Backend - AI/ML Service
```python
# Estructura del microservicio de IA
src/
├── models/
│   ├── recommendation_model.py
│   └── prediction_model.py
├── services/
│   ├── ml_service.py
│   └── data_service.py
├── api/
│   └── routes.py
└── utils/
    ├── preprocessing.py
    └── evaluation.py
```

## Funcionalidades Implementadas

### 1. Gestión de Usuarios
- **Registro**: Creación de cuentas de usuario
- **Autenticación**: Login con JWT
- **Perfiles**: Gestión de información de usuario
- **Roles**: Sistema de permisos y roles

### 2. Gestión de Productos
- **CRUD**: Crear, leer, actualizar, eliminar productos
- **Categorías**: Clasificación de productos
- **Inventario**: Control de stock
- **Precios**: Gestión de precios dinámicos

### 3. Inteligencia Artificial
- **Recomendaciones**: Sistema de recomendaciones
- **Predicciones**: Predicción de demanda
- **Análisis de Sentimientos**: Análisis de opiniones
- **Detección de Anomalías**: Identificación de patrones anómalos

### 4. Analytics y Reportes
- **Dashboard**: Métricas en tiempo real
- **Reportes**: Generación de reportes
- **Visualizaciones**: Gráficos y tablas
- **Exportación**: Exportar datos en diferentes formatos

## Implementación Paso a Paso

### Fase 1: Configuración del Proyecto (1 hora)
1. **Configurar repositorio Git**
2. **Crear estructura de directorios**
3. **Configurar Docker y Docker Compose**
4. **Configurar CI/CD pipeline**

### Fase 2: Desarrollo del Backend (2 horas)
1. **Implementar API Gateway**
2. **Desarrollar User Service**
3. **Desarrollar Product Service**
4. **Implementar AI/ML Service**
5. **Configurar base de datos**

### Fase 3: Desarrollo del Frontend (1 hora)
1. **Configurar aplicación React**
2. **Implementar componentes principales**
3. **Integrar con APIs**
4. **Implementar autenticación**

### Fase 4: Despliegue y Monitoreo (1 hora)
1. **Configurar infraestructura cloud**
2. **Desplegar con Kubernetes**
3. **Configurar monitoreo**
4. **Implementar logging**

## Código de Ejemplo

### 1. API Gateway
```javascript
const express = require('express');
const cors = require('cors');
const helmet = require('helmet');
const rateLimit = require('express-rate-limit');

const app = express();

// Middleware
app.use(helmet());
app.use(cors());
app.use(express.json());

// Rate limiting
const limiter = rateLimit({
  windowMs: 15 * 60 * 1000, // 15 minutes
  max: 100 // limit each IP to 100 requests per windowMs
});
app.use(limiter);

// Routes
app.use('/api/users', require('./routes/userRoutes'));
app.use('/api/products', require('./routes/productRoutes'));
app.use('/api/ai', require('./routes/aiRoutes'));

// Health check
app.get('/health', (req, res) => {
  res.status(200).json({ status: 'OK', timestamp: new Date().toISOString() });
});

module.exports = app;
```

### 2. User Service
```javascript
const express = require('express');
const bcrypt = require('bcrypt');
const jwt = require('jsonwebtoken');
const { User } = require('../models');

const router = express.Router();

// Register user
router.post('/register', async (req, res) => {
  try {
    const { email, password, name } = req.body;
    
    // Check if user exists
    const existingUser = await User.findOne({ email });
    if (existingUser) {
      return res.status(400).json({ error: 'User already exists' });
    }
    
    // Hash password
    const hashedPassword = await bcrypt.hash(password, 10);
    
    // Create user
    const user = new User({
      email,
      password: hashedPassword,
      name
    });
    
    await user.save();
    
    // Generate JWT
    const token = jwt.sign({ userId: user._id }, process.env.JWT_SECRET);
    
    res.status(201).json({
      message: 'User created successfully',
      token,
      user: { id: user._id, email: user.email, name: user.name }
    });
  } catch (error) {
    res.status(500).json({ error: error.message });
  }
});

// Login user
router.post('/login', async (req, res) => {
  try {
    const { email, password } = req.body;
    
    // Find user
    const user = await User.findOne({ email });
    if (!user) {
      return res.status(401).json({ error: 'Invalid credentials' });
    }
    
    // Check password
    const isValidPassword = await bcrypt.compare(password, user.password);
    if (!isValidPassword) {
      return res.status(401).json({ error: 'Invalid credentials' });
    }
    
    // Generate JWT
    const token = jwt.sign({ userId: user._id }, process.env.JWT_SECRET);
    
    res.json({
      message: 'Login successful',
      token,
      user: { id: user._id, email: user.email, name: user.name }
    });
  } catch (error) {
    res.status(500).json({ error: error.message });
  }
});

module.exports = router;
```

### 3. AI/ML Service
```python
from flask import Flask, request, jsonify
import pandas as pd
import numpy as np
from sklearn.ensemble import RandomForestClassifier
from sklearn.model_selection import train_test_split
import joblib
import os

app = Flask(__name__)

# Load or train model
def load_or_train_model():
    model_path = 'models/recommendation_model.pkl'
    
    if os.path.exists(model_path):
        return joblib.load(model_path)
    else:
        # Train a simple model for demonstration
        # In a real scenario, you would use actual data
        X = np.random.rand(100, 5)
        y = np.random.randint(0, 2, 100)
        
        model = RandomForestClassifier(n_estimators=100, random_state=42)
        model.fit(X, y)
        
        # Save model
        os.makedirs('models', exist_ok=True)
        joblib.dump(model, model_path)
        
        return model

model = load_or_train_model()

@app.route('/api/recommendations', methods=['POST'])
def get_recommendations():
    try:
        data = request.json
        user_features = np.array(data['features']).reshape(1, -1)
        
        # Get prediction
        prediction = model.predict(user_features)[0]
        probability = model.predict_proba(user_features)[0]
        
        return jsonify({
            'recommendation': int(prediction),
            'confidence': float(max(probability)),
            'features': data['features']
        })
    except Exception as e:
        return jsonify({'error': str(e)}), 500

@app.route('/api/predict', methods=['POST'])
def predict():
    try:
        data = request.json
        features = np.array(data['features']).reshape(1, -1)
        
        prediction = model.predict(features)[0]
        
        return jsonify({
            'prediction': int(prediction),
            'features': data['features']
        })
    except Exception as e:
        return jsonify({'error': str(e)}), 500

if __name__ == '__main__':
    app.run(host='0.0.0.0', port=5000)
```

### 4. Frontend Component
```jsx
import React, { useState, useEffect } from 'react';
import { useAuth } from '../hooks/useAuth';
import { api } from '../services/api';

const Dashboard = () => {
  const { user } = useAuth();
  const [stats, setStats] = useState({});
  const [loading, setLoading] = useState(true);

  useEffect(() => {
    fetchStats();
  }, []);

  const fetchStats = async () => {
    try {
      const response = await api.get('/stats');
      setStats(response.data);
    } catch (error) {
      console.error('Error fetching stats:', error);
    } finally {
      setLoading(false);
    }
  };

  if (loading) {
    return <div className="loading">Cargando...</div>;
  }

  return (
    <div className="dashboard">
      <h1>Bienvenido, {user?.name}</h1>
      
      <div className="stats-grid">
        <div className="stat-card">
          <h3>Usuarios Totales</h3>
          <p className="stat-number">{stats.totalUsers || 0}</p>
        </div>
        
        <div className="stat-card">
          <h3>Productos</h3>
          <p className="stat-number">{stats.totalProducts || 0}</p>
        </div>
        
        <div className="stat-card">
          <h3>Ventas del Mes</h3>
          <p className="stat-number">${stats.monthlySales || 0}</p>
        </div>
        
        <div className="stat-card">
          <h3>Conversión</h3>
          <p className="stat-number">{stats.conversionRate || 0}%</p>
        </div>
      </div>
      
      <div className="charts-section">
        <h2>Analytics</h2>
        {/* Aquí irían los gráficos */}
      </div>
    </div>
  );
};

export default Dashboard;
```

## Despliegue y Monitoreo

### 1. Docker Compose
```yaml
version: '3.8'
services:
  frontend:
    build: ./frontend
    ports:
      - "3000:3000"
    environment:
      - REACT_APP_API_URL=http://localhost:8000
  
  api-gateway:
    build: ./api-gateway
    ports:
      - "8000:8000"
    environment:
      - JWT_SECRET=your-secret-key
      - DB_URL=postgresql://user:password@db:5432/platform
    depends_on:
      - db
      - redis
  
  user-service:
    build: ./user-service
    environment:
      - DB_URL=postgresql://user:password@db:5432/platform
    depends_on:
      - db
  
  product-service:
    build: ./product-service
    environment:
      - DB_URL=postgresql://user:password@db:5432/platform
    depends_on:
      - db
  
  ai-service:
    build: ./ai-service
    ports:
      - "5000:5000"
  
  db:
    image: postgres:13
    environment:
      - POSTGRES_DB=platform
      - POSTGRES_USER=user
      - POSTGRES_PASSWORD=password
    volumes:
      - postgres_data:/var/lib/postgresql/data
  
  redis:
    image: redis:6-alpine
    ports:
      - "6379:6379"

volumes:
  postgres_data:
```

### 2. Kubernetes Deployment
```yaml
apiVersion: apps/v1
kind: Deployment
metadata:
  name: platform-frontend
spec:
  replicas: 3
  selector:
    matchLabels:
      app: platform-frontend
  template:
    metadata:
      labels:
        app: platform-frontend
    spec:
      containers:
      - name: frontend
        image: platform-frontend:latest
        ports:
        - containerPort: 3000
        env:
        - name: REACT_APP_API_URL
          value: "http://api-gateway-service:8000"
---
apiVersion: v1
kind: Service
metadata:
  name: platform-frontend-service
spec:
  selector:
    app: platform-frontend
  ports:
  - protocol: TCP
    port: 80
    targetPort: 3000
  type: LoadBalancer
```

## Evaluación del Proyecto

### Criterios de Evaluación
- **Funcionalidad**: 30%
- **Arquitectura**: 25%
- **Código**: 20%
- **Despliegue**: 15%
- **Documentación**: 10%

### Entregables
1. **Código fuente** completo del proyecto
2. **Documentación técnica** detallada
3. **Demo en vivo** de la plataforma
4. **Presentación** del proyecto
5. **Repositorio Git** con historial de commits

## Próximos Pasos

1. **Mejorar** la funcionalidad de IA/ML
2. **Implementar** más microservicios
3. **Agregar** testing automatizado
4. **Optimizar** el rendimiento
5. **Escalar** la infraestructura

## Recursos Adicionales

### Herramientas de Desarrollo
- **VS Code**: Editor de código
- **Postman**: Testing de APIs
- **Docker Desktop**: Containerización
- **Kubernetes**: Orquestación

### Documentación
- **React**: https://reactjs.org/docs
- **Node.js**: https://nodejs.org/docs
- **Python Flask**: https://flask.palletsprojects.com/
- **Docker**: https://docs.docker.com/
- **Kubernetes**: https://kubernetes.io/docs/

---

**¡Felicidades!** 🎉
Has completado el **Módulo 11: Tecnología y Transformación Digital**. Ahora tienes las competencias necesarias para liderar la transformación digital en tu empresa y desarrollar soluciones tecnológicas innovadoras.
