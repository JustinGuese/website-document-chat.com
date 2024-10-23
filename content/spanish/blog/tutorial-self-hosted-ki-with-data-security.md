---
author: Justin Güse
author_profile: https://www.linkedin.com/in/justin-guese/
categories:
- Chatbot
- KI
- DIY
- Tutorial
date: '2020-04-09T07:40:24+06:00'
description: Esta es una metadescripción
draft: false
image: images/blogs/chatbox.jpeg
title: 'Tutorial: IA autohospedada con seguridad de datos con Ollama y Chatbox'

---
## El problema: El 75% de las empresas prohíbe el uso de ChatGPT

A pesar de la entusiasta acogida inicial a las herramientas de IA generativas como ChatGPT, las empresas están reconsiderando su uso debido a crecientes preocupaciones sobre la privacidad de datos y la ciberseguridad. La principal preocupación es que estas herramientas de IA almacenen y aprendan de los datos de los usuarios, lo que podría provocar filtraciones de datos no deseadas. Aunque OpenAI, el desarrollador de ChatGPT, ofrece una opción para "optar por no participar" en el entrenamiento con datos de usuarios, la forma en que se manejan los datos dentro del sistema sigue sin estar clara. Además, faltan normativas claras sobre la responsabilidad ante las violaciones de datos causadas por la IA. Por consiguiente, las empresas son cada vez más cautelosas y esperan a ver cómo evoluciona la tecnología y su regulación.

Microsoft ha advertido a sus empleados contra el uso de ChatGPT, el chatbot desarrollado por OpenAI, para compartir datos confidenciales [Fuente](https://www.businessinsider.com/chatgpt-microsoft-warns-employees-not-to-share-sensitive-data-openai-2023-1). La preocupación es que la información confidencial pueda compartirse accidentalmente con el chatbot, y que éste pueda, a su vez, compartirla con otros usuarios. El enfoque cauteloso de Microsoft es notable, teniendo en cuenta la colaboración e inversión de la empresa en OpenAI. Amazon también ha emitido una advertencia similar a sus empleados. La responsabilidad en la protección de los datos confidenciales es actualmente incierta, y existe una necesidad de directrices y regulaciones más claras para estas situaciones. Los términos de servicio de OpenAI permiten a la empresa utilizar todas las entradas y salidas de los usuarios y ChatGPT, aunque se supone que eliminarán los datos personales. Sin embargo, persisten las preocupaciones sobre la posibilidad de extraer datos confidenciales de la empresa mediante solicitudes de entrada bien diseñadas.

## La solución: Modelos de IA autohospedados

Una solución a las preocupaciones sobre la seguridad y la privacidad de los datos al usar modelos de IA es hospedarlos localmente. Esto permite a las empresas mantener el control de sus datos y asegurar que no caigan en manos equivocadas. Los modelos de IA autohospedados ofrecen una forma segura y confiable de utilizar la tecnología de IA sin tener que preocuparse por problemas de privacidad y ciberseguridad.

Vamos a utilizar **Ollama** y **Chatbox**. Ollama es una herramienta optimizada para ejecutar modelos lingüísticos grandes de código abierto (LLM) como Mistral y Llama 2 localmente. Chatbox es una aplicación que permite visualizar las llamadas a la API de varios modelos.

> ¿Te parece demasiado complicado? ¿O preferirías una API alojada? Utiliza [document-chat.com](/es/) o [agenda una sesión informativa gratuita](https://datafortress.cloud/es/contact/).

### Paso 1: Descarga e instalación de Ollama

Necesitarás un servidor o un equipo con una GPU. Lamentablemente, debe ser una GPU NVidia con al menos 8 GB de VRAM, o un equipo Mac con la serie de chips M.
Las necesidades exactas se pueden encontrar en la publicación: [¿Cuáles son las ventajas de los modelos de IA autohospedados?](/es/blog/ventajas-de-modelos-ia-autohospedados/)

> Versión TLDR:
> 1. https://ollama.com/download
> 2. `ollama run llama2`
> 3. ollama está disponible en localhost:11434

#### ¿Qué es Ollama?

Ollama es una herramienta optimizada para ejecutar modelos lingüísticos grandes de código abierto (LLM) como Mistral y Llama 2 localmente. Ollama agrupa los pesos del modelo, las configuraciones y los conjuntos de datos en una unidad unificada gestionada por un archivo de modelo.

> ¿Te parece demasiado complicado? ¿O preferirías una API alojada? Utiliza [document-chat.com](/es/) o [agenda una sesión informativa gratuita](https://datafortress.cloud/es/contact/).

Ollama admite varios LLM, incluyendo LLaMA-2, LLaMA sin censura, CodeLLaMA, Falcon, Mistral, el modelo Vicuna, WizardCoder y Wizard sin censura.

Ollama admite una variedad de modelos, incluyendo Llama 2, Code Llama y otros. Agrupa los pesos del modelo, las configuraciones y los datos en una sola unidad definida por un archivo de modelo.

Los cinco modelos más populares en Ollama son:

- llama2: El modelo más popular para uso general.
- mistral: El modelo de 7B de Mistral AI, actualizado a la versión 0.2.
- codellama: Un gran modelo lingüístico que utiliza entradas de texto para generar y discutir código.
- dolphin-mixtral: Un modelo sin censura y ajustado basado en el modelo Mixtral MoE, especialmente adecuado para tareas de codificación.
- mistral-openorca: Mistral 7b, ajustado con el conjunto de datos OpenOrca.


Ollama también admite la creación y uso de modelos personalizados. Puedes crear un modelo utilizando un archivo de modelo en el que proporciones el archivo del modelo, crees varias capas, escribas los pesos y, finalmente, recibas un mensaje de éxito.

Algunos de los otros modelos disponibles en Ollama incluyen:

- Llama2: El modelo "de código abierto" básico de Meta.
- Mistral/Mixtral: Un modelo de 7 mil millones de parámetros basado en el modelo Mistral 7B ajustado con el conjunto de datos OpenOrca.
- LLaVA: Un modelo multimodal llamado LLaVA (Large Language and Vision Assistant) que puede interpretar entradas visuales.
- CodeLlama: Modelo entrenado tanto en código como en lenguaje natural en inglés.
- DeepSeek Coder: Entrenado desde cero en un 87% de código y un 13% de lenguaje natural en inglés.
- Meditron: Un modelo de IA para medicina de código abierto adaptado desde Llama 2 al ámbito médico.


#### Instalación y configuración de Ollama

- Descarga Ollama desde el sitio web oficial.
- La instalación es sencilla y similar a la de otros softwares. Para usuarios de macOS y Linux, Ollama se puede instalar con el comando: `curl https://ollama.ai/install.sh | sh`.
- Una vez instalada Ollama, crea una API que proporciona el modelo, permitiendo a los usuarios interactuar directamente con el modelo desde su equipo local.
- Ollama es compatible con macOS y Linux, y la compatibilidad con Windows estará disponible próximamente. Se puede instalar y usar fácilmente para ejecutar varios modelos de código abierto localmente. Puedes seleccionar el modelo deseado de la biblioteca de Ollama.

Ejecución de modelos con Ollama

Ejecutar modelos con Ollama es un proceso sencillo. Los usuarios pueden descargar modelos y ejecutarlos con el comando "run" en la terminal. Si el modelo no está instalado, Ollama lo descargará automáticamente. Por ejemplo, para ejecutar el modelo CodeLlama, usa el comando "ollama run codellama".

Los modelos se guardan en la estructura de directorios ~/.ollama/models en tu equipo local. Si descargas un modelo con el comando "ollama pull", éste se guarda en el directorio ~/.ollama/models/manifests/registry.ollama.ai/library/<familia-del-modelo>/latest.

Ollama también admite la utilización del modelo mediante una API REST para interacciones en tiempo real.

Funciones adicionales

Una de las características únicas de Ollama es la compatibilidad con la importación de formatos de archivos GGUF y GGML en el archivo de modelo. Esto significa que puedes crear un modelo, construir sobre él, mejorarlo iterativamente y subirlo para compartirlo con otros cuando estés listo.

Modelos disponibles

Ollama admite una variedad de modelos, y puedes encontrar una lista de los modelos disponibles en la página de la biblioteca de modelos de Ollama.

En resumen, Ollama ofrece un entorno fácil de usar para ejecutar modelos lingüísticos grandes localmente. Es una herramienta potente para desarrolladores, investigadores y entusiastas de la IA para aprovechar las posibilidades de los LLM.

### Paso 2: Control y uso de Ollama con la GUI de Chatbox

Chatbox es una aplicación que permite visualizar las llamadas a la API de diversos modelos.

![Interfaz gráfica de Chatbox](/images/blogs/chatbox.png)

### Instalación de Chatbox

Visita https://chatboxai.app e instala la aplicación en tu equipo.


### Conexión de Chatbox y Ollama

Como se mencionó anteriormente, nuestro modelo de IA local ahora está disponible en localhost:11434.
Chatbox ofrece una forma sencilla de interactuar con Ollama. Para ello, haz clic en "Ajustes" y selecciona "Proveedor de modelos de IA" como Ollama.

![Ajustes de Chatbox para Ollama](/images/blogs/chatbox-settings.png)

Después, solo tienes que seleccionar el modelo que has elegido con el comando `ollama run` en el cuadro de diálogo del modelo, que en nuestro caso es `llama2`.

> ¿Te parece demasiado complicado? ¿O preferirías una API alojada? Utiliza [document-chat.com](/es/) o [agenda una sesión informativa gratuita](https://datafortress.cloud/es/contact/).
