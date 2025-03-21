# 📚 Retrieval-Augmented Generation (RAG) con LangChain y Pinecone

Este proyecto implementa un sistema **RAG (Retrieval-Augmented Generation)** usando **LangChain** y **Pinecone** para la búsqueda de información y generación de respuestas inteligentes.

## 🚀 Características
- Indexación de documentos en **Pinecone**.
- Recuperación eficiente con embeddings de **OpenAI**.
- Flujo de ejecución con **LangGraph** para estructurar la búsqueda y generación de respuestas.
- Capacidad de realizar preguntas y obtener respuestas contextualizadas.

---

## 🛠️ Instalación y Configuración

### 1️⃣ **Clona el repositorio**
```bash
git clone https://github.com/tomassuarez49/AREP-LAB09
```

### 2️⃣ **Configura tus claves API**
Debes establecer las claves API para OpenAI y Pinecone en tu entorno.

```bash
export OPENAI_API_KEY='tu_openai_api_key'
export PINECONE_API_KEY='tu_pinecone_api_key'
export PINECONE_ENV='us-east-1'
```
O puedes configurarlas dentro del código:
```python
import os
os.environ["OPENAI_API_KEY"] = "tu_openai_api_key"
os.environ["PINECONE_API_KEY"] = "tu_pinecone_api_key"
os.environ["PINECONE_ENV"] = "us-east-1"
```

---

## 🔎 Uso en Google Colab

### 1️⃣ **Abrir en Colab**
Sigue estos pasos para ejecutar el proyecto en **Google Colab**:
1. Ve a [Google Colab](https://colab.research.google.com/).
2. Haz clic en **Archivo > Abrir cuaderno**.
3. Selecciona la pestaña **GitHub** y pega el enlace del repositorio.
4. Abre el archivo `Build_a_Retrieval_Augmented_Generation_(RAG)_App_Part_2.ipynb`.

### 2️⃣ **Ejecutar las celdas**
Ejecuta cada celda secuencialmente usando `Shift + Enter` o haciendo clic en el botón **▶**.

### 3️⃣ **Configurar las claves API**
Cuando te lo solicite, ingresa las claves de OpenAI y Pinecone en las casillas de entrada.

### 4️⃣ **Ejecutar consultas**
Después de indexar los documentos en Pinecone, prueba la recuperación de información con:
```python
response = graph.invoke({"question": "What is Task Decomposition?"})
print(response["answer"])
```

---

## 📌 Arquitectura

1. **Carga de datos**: Se usa `WebBaseLoader` para extraer contenido de una URL.
2. **Procesamiento**: Se divide en fragmentos (`RecursiveCharacterTextSplitter`).
3. **Vectorización**: Se convierten los textos en embeddings con `OpenAIEmbeddings`.
4. **Almacenamiento**: Se indexan en **Pinecone**.
5. **Consulta**: Se recuperan los documentos más relevantes con `similarity_search`.
6. **Generación de respuesta**: El modelo genera una respuesta basada en el contexto recuperado.

---

## 📝 Pruebas

![image](https://github.com/user-attachments/assets/364832d1-be4e-421d-ad2e-b4d76d70b6c8)

![image](https://github.com/user-attachments/assets/edaa1d7c-6120-4e04-b8cf-d169adf691e2)

👨‍💻 **Desarrollado por Tomas Suarez Piratova** 🚀




