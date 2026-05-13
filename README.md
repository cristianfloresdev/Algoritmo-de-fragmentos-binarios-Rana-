# 🐸 RANA 2.0 — Algoritmo Biomimético de Similitud y Deduplicación

Inspirado en la simbiosis entre *Chiasmocleis ventrimaculata* y la tarántula amazónica.

---

## 🧠 ¿Qué es RANA 2.0?

**RANA 2.0** es un algoritmo de detección de similitud y deduplicación de archivos basado en huellas criptográficas **SHA-256**.

Fragmenta cualquier archivo en bloques de bytes y compara sus firmas digitales, sin importar el tipo de archivo:
- Texto
- Imágenes
- PDF
- Binarios

El sistema no modifica los datos originales, solo los analiza de forma no destructiva.

---

## 🐸 Inspiración biomimética

El comportamiento del algoritmo está inspirado en la rana  
*Chiasmocleis ventrimaculata*, que convive en simbiosis con tarántulas del género *Xenesthis*.

| Naturaleza | Algoritmo |
|------------|-----------|
| La rana distingue huevos propios vs ajenos | RANA identifica bloques únicos vs duplicados |
| Simbiosis no destructiva | Análisis sin alterar archivos |
| Reconocimiento por patrones químicos | Reconocimiento por SHA-256 |

---

## 🏗️ Arquitectura — Pipeline

### 📁 Estructura del proyecto

```

src/main/java/com/artemisa/Rana/
├── core/
│   ├── Fragmentador.java     # Divide archivos en bloques de bytes
│   └── HashUtil.java         # Genera SHA-256 nativo
├── model/
│   ├── Fragmentos.java       # Representación inmutable de datos
│   └── ResultadoRana.java    # Métricas finales del análisis
└── Rana.java                 # Motor principal del algoritmo
