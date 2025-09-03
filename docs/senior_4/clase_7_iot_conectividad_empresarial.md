# Clase 7: IoT y Conectividad Empresarial

## Objetivos de la Clase

- Comprender los fundamentos del Internet de las Cosas (IoT)
- Diseñar soluciones IoT para problemas empresariales
- Implementar sistemas de conectividad y comunicación
- Analizar datos en tiempo real de dispositivos IoT

## Navegación del Módulo

| Clase | Tema | Duración | Tipo |
|-------|------|----------|------|
| 1 | Fundamentos de Transformación Digital | 2 horas | Teórica |
| 2 | Estrategias de Adopción Tecnológica | 2 horas | Teórica |
| 3 | Cloud Computing y Arquitecturas Escalables | 3 horas | Práctica |
| 4 | Desarrollo de APIs y Microservicios | 3 horas | Práctica |
| 5 | Inteligencia Artificial y Machine Learning | 3 horas | Práctica |
| 6 | Blockchain y Tecnologías Descentralizadas | 2 horas | Teórica |
| 7 | **IoT y Conectividad Empresarial** | 2 horas | Teórica |
| 8 | Ciberseguridad y Protección de Datos | 2 horas | Teórica |
| 9 | Gestión de Proyectos Tecnológicos | 2 horas | Teórica |
| 10 | Proyecto Integrador: Plataforma Digital | 4 horas | Práctica |

## Contenido Teórico

### 1. Fundamentos del IoT

#### 1.1 ¿Qué es IoT?
El Internet de las Cosas (IoT) es una red de dispositivos físicos conectados que pueden recopilar, intercambiar y actuar sobre datos. Estos dispositivos están equipados con sensores, software y otras tecnologías para conectarse e intercambiar datos con otros dispositivos y sistemas.

#### 1.2 Componentes del IoT
- **Dispositivos/Sensores**: Hardware que recopila datos
- **Conectividad**: Redes de comunicación
- **Plataforma Cloud**: Procesamiento y almacenamiento
- **Aplicaciones**: Software para análisis y control
- **Seguridad**: Protección de datos y dispositivos

#### 1.3 Arquitectura IoT
```
┌─────────────┐    ┌─────────────┐    ┌─────────────┐
│ Dispositivos│    │ Conectividad│    │   Cloud     │
│   IoT       │◄──►│   (WiFi,    │◄──►│  Platform   │
│             │    │   5G, LoRa) │    │             │
└─────────────┘    └─────────────┘    └─────────────┘
                           │
                    ┌──────┴──────┐
                    │             │
            ┌───────▼──────┐ ┌────▼──────┐
            │  Aplicaciones│ │  Analytics │
            │  y Control   │ │  y ML      │
            └──────────────┘ └───────────┘
```

### 2. Tipos de Sensores y Dispositivos

#### 2.1 Sensores Ambientales
- **Temperatura**: Monitoreo de temperatura
- **Humedad**: Medición de humedad relativa
- **Presión**: Sensores de presión atmosférica
- **Calidad del Aire**: Monitoreo de contaminantes
- **Ruido**: Medición de niveles de sonido

#### 2.2 Sensores de Movimiento
- **Acelerómetros**: Detección de movimiento
- **Giroscopios**: Medición de orientación
- **Magnetómetros**: Detección de campos magnéticos
- **Proximidad**: Detección de objetos cercanos
- **Presencia**: Detección de personas

#### 2.3 Sensores de Imagen
- **Cámaras**: Captura de imágenes y video
- **Infrarrojos**: Detección de calor
- **Lidar**: Mapeo 3D y detección de distancia
- **Ultrasonidos**: Medición de distancia
- **Radar**: Detección de objetos en movimiento

### 3. Protocolos de Conectividad

#### 3.1 Conectividad de Corto Alcance
- **WiFi**: Conectividad de alta velocidad
- **Bluetooth**: Conexión de bajo consumo
- **Zigbee**: Red de malla de bajo consumo
- **Z-Wave**: Protocolo para hogar inteligente
- **NFC**: Comunicación de campo cercano

#### 3.2 Conectividad de Largo Alcance
- **Cellular (4G/5G)**: Conectividad móvil
- **LoRaWAN**: Red de área amplia de bajo consumo
- **Sigfox**: Red global de IoT
- **NB-IoT**: Internet de las cosas de banda estrecha
- **Satellite**: Conectividad por satélite

#### 3.3 Protocolos de Comunicación
- **MQTT**: Protocolo de mensajería ligero
- **CoAP**: Protocolo de aplicación restringida
- **HTTP/HTTPS**: Protocolo web estándar
- **WebSocket**: Comunicación bidireccional
- **AMQP**: Protocolo de mensajería avanzado

### 4. Plataformas IoT

#### 4.1 Plataformas Cloud
- **AWS IoT**: Servicios IoT de Amazon
- **Azure IoT**: Plataforma IoT de Microsoft
- **Google Cloud IoT**: Soluciones IoT de Google
- **IBM Watson IoT**: Plataforma cognitiva de IBM
- **ThingWorx**: Plataforma de PTC

#### 4.2 Características de las Plataformas
- **Gestión de Dispositivos**: Registro y configuración
- **Ingesta de Datos**: Recopilación y procesamiento
- **Analytics**: Análisis de datos en tiempo real
- **Visualización**: Dashboards y reportes
- **Integración**: APIs y conectores

### 5. Aplicaciones Empresariales del IoT

#### 5.1 Manufactura Inteligente
- **Monitoreo de Equipos**: Mantenimiento predictivo
- **Control de Calidad**: Detección de defectos
- **Optimización de Procesos**: Mejora de eficiencia
- **Gestión de Inventario**: Control automático de stock
- **Seguridad Industrial**: Monitoreo de seguridad

#### 5.2 Logística y Cadena de Suministro
- **Seguimiento de Envíos**: Localización en tiempo real
- **Monitoreo de Condiciones**: Temperatura, humedad
- **Gestión de Flotas**: Optimización de rutas
- **Control de Acceso**: Seguridad en almacenes
- **Predicción de Demanda**: Análisis predictivo

#### 5.3 Retail y Comercio
- **Inventario Inteligente**: Control automático
- **Experiencia del Cliente**: Personalización
- **Análisis de Comportamiento**: Patrones de compra
- **Gestión de Tiendas**: Optimización de espacios
- **Marketing Contextual**: Publicidad dirigida

#### 5.4 Agricultura Inteligente
- **Monitoreo de Cultivos**: Condiciones del suelo
- **Riego Automático**: Optimización de agua
- **Control de Plagas**: Detección temprana
- **Gestión de Ganado**: Monitoreo de salud
- **Predicción de Cosechas**: Análisis predictivo

### 6. Análisis de Datos IoT

#### 6.1 Tipos de Análisis
- **Análisis en Tiempo Real**: Procesamiento inmediato
- **Análisis Predictivo**: Predicción de eventos
- **Análisis Prescriptivo**: Recomendaciones de acción
- **Análisis de Tendencias**: Identificación de patrones
- **Análisis de Anomalías**: Detección de irregularidades

#### 6.2 Herramientas de Análisis
- **Streaming Analytics**: Apache Kafka, Apache Storm
- **Time Series Databases**: InfluxDB, TimescaleDB
- **Machine Learning**: TensorFlow, PyTorch
- **Visualization**: Grafana, Kibana, Tableau
- **Big Data**: Apache Spark, Hadoop

## Ejercicios Prácticos

### Ejercicio 1: Diseño de Solución IoT
**Objetivo**: Diseñar una solución IoT para tu empresa

**Instrucciones**:
1. Identifica un problema que IoT pueda resolver
2. Define los sensores y dispositivos necesarios
3. Selecciona protocolos de conectividad
4. Diseña la arquitectura de la solución

**Casos de Uso Sugeridos**:
- Monitoreo de oficina inteligente
- Sistema de seguridad empresarial
- Optimización de energía
- Control de inventario
- Monitoreo de equipos

### Ejercicio 2: Análisis de Datos IoT
**Objetivo**: Analizar datos de sensores IoT

**Instrucciones**:
1. Simula datos de sensores IoT
2. Implementa análisis en tiempo real
3. Crea visualizaciones de datos
4. Desarrolla alertas automáticas

**Código de Ejemplo**:
```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
from datetime import datetime, timedelta

# Simulación de datos IoT
def generate_iot_data():
    timestamps = pd.date_range(start='2024-01-01', periods=1000, freq='1min')
    temperature = np.random.normal(22, 5, 1000)
    humidity = np.random.normal(50, 10, 1000)
    
    df = pd.DataFrame({
        'timestamp': timestamps,
        'temperature': temperature,
        'humidity': humidity
    })
    
    return df

# Análisis de datos
def analyze_iot_data(df):
    # Estadísticas básicas
    print("Estadísticas de Temperatura:")
    print(df['temperature'].describe())
    
    # Detección de anomalías
    temp_mean = df['temperature'].mean()
    temp_std = df['temperature'].std()
    anomalies = df[abs(df['temperature'] - temp_mean) > 2 * temp_std]
    
    print(f"\nAnomalías detectadas: {len(anomalies)}")
    
    # Visualización
    plt.figure(figsize=(12, 6))
    plt.subplot(2, 1, 1)
    plt.plot(df['timestamp'], df['temperature'])
    plt.title('Temperatura en el Tiempo')
    plt.ylabel('Temperatura (°C)')
    
    plt.subplot(2, 1, 2)
    plt.plot(df['timestamp'], df['humidity'])
    plt.title('Humedad en el Tiempo')
    plt.ylabel('Humedad (%)')
    plt.xlabel('Tiempo')
    
    plt.tight_layout()
    plt.show()

# Ejecutar análisis
df = generate_iot_data()
analyze_iot_data(df)
```

### Ejercicio 3: Implementación de Dashboard IoT
**Objetivo**: Crear un dashboard para monitoreo IoT

**Instrucciones**:
1. Configura una base de datos de series temporales
2. Implementa ingesta de datos en tiempo real
3. Crea visualizaciones interactivas
4. Configura alertas y notificaciones

**Tecnologías Sugeridas**:
- **Backend**: Node.js con Express
- **Database**: InfluxDB o TimescaleDB
- **Frontend**: React con Chart.js
- **Real-time**: WebSocket o Server-Sent Events

## Conceptos Clave

- **IoT**: Internet de las Cosas
- **Sensores**: Dispositivos de recopilación de datos
- **Conectividad**: Protocolos de comunicación
- **Plataformas IoT**: Servicios cloud para IoT
- **Análisis en Tiempo Real**: Procesamiento inmediato de datos
- **Dashboard**: Visualización de datos IoT

## Preguntas de Repaso

1. ¿Cuáles son los componentes principales de una solución IoT?
2. ¿Qué protocolos de conectividad son más apropiados para diferentes casos de uso?
3. ¿Cómo se puede asegurar la seguridad en dispositivos IoT?
4. ¿Qué tipos de análisis son más útiles para datos IoT?
5. ¿Cuáles son los desafíos principales en la implementación de IoT?

## Próximos Pasos

1. **Experimentar** con sensores y dispositivos IoT
2. **Explorar** plataformas cloud de IoT
3. **Desarrollar** un prototipo de solución IoT
4. **Analizar** datos de sensores en tiempo real

## Recursos Adicionales

### Hardware y Sensores
- **Arduino**: Plataforma de desarrollo
- **Raspberry Pi**: Computadora de placa única
- **ESP32**: Microcontrolador con WiFi
- **Sensores**: DHT22, BMP280, PIR, etc.

### Plataformas de Desarrollo
- **Arduino IDE**: Entorno de desarrollo
- **PlatformIO**: IDE para IoT
- **Node-RED**: Programación visual
- **Home Assistant**: Automatización del hogar

### Cursos Online
- **Coursera**: IoT Specialization
- **edX**: Introduction to IoT
- **Udemy**: Complete IoT Course
- **YouTube**: Canales de IoT y electrónica

### Libros Recomendados
- "Building the Internet of Things" - Maciej Kranz
- "IoT Fundamentals" - David Hanes
- "The Internet of Things" - Samuel Greengard
- "IoT Security" - Cesar Cerrudo

---

**¡Siguiente Clase!** 🚀
En la próxima clase aprenderás sobre **Ciberseguridad y Protección de Datos** y cómo proteger tu empresa de amenazas digitales.
