# Estadias_final

```markdown
# Organic Quimic Visualizator 🧪💻

Aplicación web para la visualización y análisis de moléculas orgánicas a partir de cadenas SMILES.  
Integra RDKit para cálculos químicos, Flask-SocketIO para comunicación en tiempo real, MediaPipe para interacción gestual y Gemini AI para análisis asistido.

---

## ✨ Características
- Carga de moléculas vía **SMILES** o selección predefinida.
- Cálculo de propiedades físico-químicas básicas con **RDKit**:
  - Peso molecular (MW)
  - LogP
  - Donadores y aceptores de H
  - TPSA (Topological Polar Surface Area)
  - Enlaces rotables
- Análisis básico de interacción ligando–receptor (prototipo conceptual).
- Análisis descriptivo con **Gemini AI**.
- Comunicación **en tiempo real** con Flask-SocketIO.
- Interacción experimental por cámara y gestos con **MediaPipe**.

---

## 📂 Arquitectura
```

Cliente (HTML + JS + Socket.IO + MediaPipe)
↕
Servidor Flask (endpoints + eventos SocketIO)
↘ RDKit (química, SMILES, propiedades)
↘ Gemini (análisis IA)

````

---

## 🚀 Instalación y ejecución

### 1. Clonar repositorio
```bash
git clone https://github.com/tuusuario/OrganicQuimicVisualizator.git
cd OrganicQuimicVisualizator
````

### 2. Crear entorno virtual (opcional)

```bash
python -m venv venv
source venv/bin/activate   # Linux/Mac
venv\Scripts\activate      # Windows
```

### 3. Instalar dependencias

```bash
pip install -r requirements.txt
```

> ⚠️ **Nunca subas tu API Key real a GitHub.**

### 4. Ejecutar servidor

```bash
python main.py
```

El servidor estará en:

```
http://localhost:5000
```

---

## 🧪 Ejemplo de uso

1. Abre la aplicación en tu navegador.
2. Introduce un SMILES (ej: `CCO` para etanol).
3. Visualiza propiedades como MW, LogP, TPSA.
4. Opcional: activa la cámara para pruebas gestuales.
5. Haz clic en **Analizar con IA** para obtener un reporte textual de Gemini.

---

## 📊 Resultados esperados

* Representación 2D de la molécula.
* Propiedades físico-químicas calculadas.
* Texto descriptivo de Gemini (potenciales usos, características, insights).

---

## ⚠️ Limitaciones

* El análisis de interacción **es un prototipo conceptual**; no es docking real.
* El “docking score” mostrado **no corresponde a energías físicas**.
* Para un docking real habría que integrar motores como **AutoDock Vina** o **smina**.

---

