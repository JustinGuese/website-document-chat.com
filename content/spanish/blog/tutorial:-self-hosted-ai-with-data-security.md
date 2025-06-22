---
author: Justin Güse
author_profile: https://www.linkedin.com/in/justin-guese/
categories:
  - Chatbot
  - AI
  - DIY
  - Tutorial
date: '2020-04-09T07:40:24+06:00'
description: this is meta description
draft: false
image: images/blogs/chatbox.jpeg
title: 'Tutorial: IA Autohospedada con Seguridad de Datos usando Ollama y Chatbox'
---

# El Problema: El 75% de las Empresas Prohíbe ChatGPT

A pesar del entusiasmo inicial por las herramientas de IA generativa como ChatGPT, las empresas están restringiendo su uso debido a las crecientes preocupaciones sobre la privacidad de los datos y la ciberseguridad. La principal preocupación es que estas herramientas de IA almacenan y aprenden de los datos del usuario, lo que potencialmente puede dar lugar a violaciones de datos no deseadas. Aunque OpenAI, el desarrollador de ChatGPT, ofrece una opción para optar por no participar en el entrenamiento con datos de usuario, la gestión de los datos dentro del sistema sigue sin estar clara. Además, faltan regulaciones legales claras sobre la responsabilidad de las violaciones de datos causadas por la IA. En consecuencia, las empresas se muestran reticentes y esperan que la tecnología y su regulación evolucionen.

Microsoft ha advertido a sus empleados contra compartir datos confidenciales con ChatGPT, el chatbot desarrollado por OpenAI [Fuente](https://www.businessinsider.com/chatgpt-microsoft-warns-employees-not-to-share-sensitive-data-openai-2023-1). Surgen preocupaciones de que la información confidencial pueda compartirse inadvertidamente con el chatbot, lo que podría dar lugar a su difusión a otros usuarios. El enfoque cauteloso de Microsoft es notable considerando la asociación e inversión de la empresa en OpenAI. Amazon también ha emitido una advertencia similar a sus empleados. La responsabilidad de proteger los datos confidenciales sigue sin estar clara, y se necesitan directrices y regulaciones más claras para situaciones como esta. Los términos de servicio de OpenAI permiten a la empresa usar todas las entradas y salidas generadas por los usuarios y ChatGPT, aunque se pretende eliminar los datos personales. Sin embargo, persisten las preocupaciones sobre la posibilidad de extraer datos confidenciales de la empresa a través de indicaciones de entrada cuidadosamente elaboradas.

## La Solución: Modelos de IA Autohospedados

Una solución a las preocupaciones sobre la seguridad y la privacidad de los datos de los modelos de IA es hospedar estos modelos en sus propios servidores. Esto permite a las empresas conservar el control sobre sus datos y garantizar que no caigan en las manos equivocadas. Los modelos de IA autohospedados ofrecen una forma segura y confiable de utilizar la tecnología de IA sin tener que preocuparse por la privacidad de los datos y la ciberseguridad.

Utilizaremos **Ollama** y **Chatbox**. Ollama es una herramienta optimizada para ejecutar modelos lingüísticos grandes (LLMs) de código abierto como Mistral y Llama 2 localmente. Chatbox es una aplicación que visualiza las llamadas a la API de varios modelos.

¿Te parece demasiado complejo? ¿O sería mejor una API alojada? Visita [document-chat.com](/de/) o [programa una llamada introductoria gratuita con nosotros](https://datafortress.cloud/de/contact/).

### Paso 1: Descarga e Instalación de Ollama

Necesitarás un servidor o computadora con una GPU. Desafortunadamente, debe ser una GPU NVIDIA con al menos 8 GB de VRAM, o un Mac Apple con un chip de la serie M.
Encuentra los requisitos exactos en esta publicación: [¿Cuáles son las ventajas de los modelos de IA autohospedados?](/de/blog/vorteile-von-selbst-gehosteten-ki-modellen/)

> Versión TLDR:
>
> 1. https://ollama.com/download
> 2. `ollama run llama2`
> 3. ollama es accesible en localhost:11434

#### ¿Qué es Ollama?

Ollama es una herramienta optimizada para ejecutar modelos lingüísticos grandes (LLMs) de código abierto como Mistral y Llama 2 localmente. Ollama agrupa los pesos del modelo, las configuraciones y los conjuntos de datos en una sola entidad administrada por un archivo de modelo.

¿Te parece demasiado complejo? ¿O sería mejor una API alojada? Visita [document-chat.com](/de/) o [programa una llamada introductoria gratuita con nosotros](https://datafortress.cloud/de/contact/).

Ollama admite varios LLMs, incluyendo LLaMA-2, LLaMA sin censura, CodeLLaMA, Falcon, Mistral, Vicuna, WizardCoder y Wizard sin censura.

Ollama admite una variedad de modelos, incluyendo Llama 2, Code Llama y otros. Agrupa los pesos del modelo, las configuraciones y los datos en una sola unidad, definida por un archivo de modelo.

Los cinco modelos más populares en Ollama son:

- llama2: El modelo más popular para uso general.
- mistral: El modelo 7B de Mistral AI, actualizado a la versión 0.2.
- codellama: Un modelo lingüístico grande que utiliza entradas de texto para generar y discutir código.
- dolphin-mixtral: Un modelo sin censura y afinado basado en Mixtral MoE, particularmente adecuado para tareas de codificación.
- mistral-openorca: Mistral 7b, afinado con el conjunto de datos OpenOrca.

Ollama también admite modelos personalizados. Puedes crear un modelo usando un archivo de modelo, especificando capas, escribiendo pesos y recibiendo un mensaje de éxito.

Otros modelos disponibles incluyen:

- Llama2: El modelo "de código abierto" fundamental de Meta.
- Mistral/Mixtral: Un modelo de 7 mil millones de parámetros afinado en el modelo Mistral 7B con el conjunto de datos OpenOrca.
- LLaVA: Un modelo multimodal (Large Language and Vision Assistant) capaz de interpretar entradas visuales.
- CodeLlama: Un modelo entrenado en código y lenguaje natural en inglés.
- DeepSeek Coder: Entrenado en un 87% de código y un 13% de lenguaje natural en inglés.
- Meditron: Un modelo médico de código abierto adaptado de Llama 2 al dominio médico.

#### Instalación y configuración de Ollama

- Descarga Ollama desde el sitio web oficial.
- La instalación es sencilla, similar a otros softwares. Para macOS y Linux, usa `curl https://ollama.ai/install.sh | sh`.
- Ollama crea una API para interactuar con el modelo localmente.
- Ollama es compatible con macOS y Linux; la compatibilidad con Windows llegará pronto.

Ejecutando Modelos con Ollama

Ejecutar modelos es sencillo. Descarga los modelos y ejecútalos usando el comando "run" en la terminal. Si un modelo no está instalado, Ollama lo descarga automáticamente. Por ejemplo, ejecuta CodeLlama con "ollama run codellama".

Los modelos se guardan en el directorio ~/.ollama/models. Al descargar un modelo a través de "ollama pull", se almacena en ~/.ollama/models/manifests/registry.ollama.ai/library/<model-family>/latest.

Ollama también ofrece acceso a la API REST para interacciones en tiempo real.

Características adicionales

Ollama admite la importación de archivos de modelos GGUF y GGML, lo que permite la creación, la iteración y el intercambio de modelos.

Modelos disponibles

Puedes encontrar una lista de modelos disponibles en la página de la Biblioteca de Modelos de Ollama.

En resumen, Ollama proporciona una plataforma fácil de usar para ejecutar LLMs localmente. Es un recurso valioso para desarrolladores, investigadores y entusiastas de la IA.

### Paso 2: Control y utilización de Ollama con la interfaz gráfica de Chatbox

Chatbox es una aplicación que visualiza las llamadas a la API de varios modelos.

![Interfaz gráfica de Chatbox](/images/blogs/chatbox.png)

### Instalación de Chatbox

Visita https://chatboxai.app e instala la aplicación en tu computadora.

### Conexión de Chatbox y Ollama

Nuestro modelo de IA local es accesible en localhost:11434. Chatbox permite una interacción sencilla con Ollama. Haz clic en "Configuración" y selecciona Ollama como "Proveedor de Modelo de IA".

![Configuración de Chatbox Ollama](/images/blogs/chatbox-settings.png)

Luego, selecciona el modelo deseado (por ejemplo, `llama2`) en el cuadro de diálogo de modelos.

¿Te parece demasiado complejo? ¿O sería mejor una API alojada? Visita [document-chat.com](/de/) o [programa una llamada introductoria gratuita con nosotros](https://datafortress.cloud/de/contact/).
