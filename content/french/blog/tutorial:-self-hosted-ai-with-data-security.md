---
author: Justin Güse
author_profile: https://www.linkedin.com/in/justin-guese/
categories:
  - Agent conversationnel
  - AI
  - DIY
  - Tutoriel
date: '2020-04-09T07:40:24+06:00'
description: this is meta description
draft: false
image: images/blogs/chatbox.jpeg
title: 'Tutoriel : IA auto-hébergée avec sécurité des données grâce à Ollama et Chatbox'
---

# Le Problème : 75 % des entreprises interdisent ChatGPT

Malgré l'enthousiasme initial suscité par les outils d'IA générative comme ChatGPT, les entreprises restreignent leur utilisation en raison des préoccupations croissantes concernant la confidentialité des données et la cybersécurité. La principale inquiétude est que ces outils d'IA stockent et apprennent à partir des données utilisateur, ce qui pourrait entraîner des violations de données non intentionnelles. Bien qu'OpenAI, le développeur de ChatGPT, propose une option de désinscription de la formation avec les données utilisateur, la gestion des données au sein du système reste imprécise. De plus, il manque de réglementations juridiques claires concernant la responsabilité des violations de données causées par l'IA. Par conséquent, les entreprises hésitent et attendent que la technologie et sa réglementation évoluent.

Microsoft a prévenu ses employés contre le partage de données sensibles avec ChatGPT, le chatbot développé par OpenAI [Source](https://www.businessinsider.com/chatgpt-microsoft-warns-employees-not-to-share-sensitive-data-openai-2023-1). Des inquiétudes se posent quant à la possibilité que des informations confidentielles soient accidentellement partagées avec le chatbot, potentiellement conduisant à leur diffusion à d'autres utilisateurs. L'approche prudente de Microsoft est notable étant donné le partenariat et l'investissement de l'entreprise dans OpenAI. Amazon a également adressé un avertissement similaire à ses employés. La responsabilité de la protection des données confidentielles reste floue, et des directives et réglementations plus claires pour de telles situations sont nécessaires. Les conditions d'utilisation d'OpenAI permettent à la société d'utiliser toutes les entrées et sorties générées par les utilisateurs et ChatGPT, même si les données personnelles sont censées être supprimées. Cependant, des inquiétudes persistent quant à la possibilité d'extraire des données confidentielles de l'entreprise par le biais de demandes d'entrée astucieusement conçues.

## La Solution : Modèles IA Auto-Hébergés

Une solution aux problèmes de sécurité et de confidentialité des données liés aux modèles IA est d'héberger ces modèles sur vos propres serveurs. Cela permet aux entreprises de conserver le contrôle de leurs données et de s'assurer qu'elles ne tombent pas entre de mauvaises mains. Les modèles IA auto-hébergés offrent un moyen sécurisé et fiable d'utiliser la technologie IA sans se soucier des problèmes de confidentialité et de cybersécurité des données.

Nous utiliserons **Ollama** et **Chatbox**. Ollama est un outil simplifié pour exécuter localement des modèles de langage de grande taille (LLM) open source comme Mistral et Llama 2. Chatbox est une application qui visualise les appels API vers différents modèles.

> Cela vous semble-t-il trop compliqué ? Ou un API hébergé serait-il préférable ? Utilisez [document-chat.com](/de/) ou [planifiez un appel introductif gratuit avec nous](https://datafortress.cloud/de/contact/).

### Étape 1 : Téléchargement et Installation d'Ollama

Vous aurez besoin d'un serveur ou d'un ordinateur avec une carte graphique. Malheureusement, il doit s'agir d'une carte graphique NVIDIA avec au moins 8 Go de VRAM, ou d'un Mac Apple avec une puce de la série M.
Trouvez les exigences exactes dans cet article : [Quels sont les avantages des modèles IA auto-hébergés ?](/de/blog/vorteile-von-selbst-gehosteten-ki-modellen/)

> Version TLDR :
>
> 1. https://ollama.com/download
> 2. `ollama run llama2`
> 3. ollama est accessible sous localhost :11434

#### Qu'est-ce qu'Ollama ?

Ollama est un outil simplifié pour exécuter localement des modèles de langage de grande taille (LLM) open source comme Mistral et Llama 2. Ollama regroupe les poids du modèle, les configurations et les ensembles de données dans une seule entité gérée par un fichier modèle.

> Cela vous semble-t-il trop compliqué ? Ou un API hébergé serait-il préférable ? Utilisez [document-chat.com](/de/) ou [planifiez un appel introductif gratuit avec nous](https://datafortress.cloud/de/contact/).

Ollama prend en charge divers LLM, notamment LLaMA-2, LLaMA non censuré, CodeLLaMA, Falcon, Mistral, Vicuna, WizardCoder et Wizard non censuré.

Ollama prend en charge une variété de modèles, notamment Llama 2, Code Llama et autres. Il regroupe les poids du modèle, les configurations et les données dans une seule unité, définie par un fichier modèle.

Les cinq modèles les plus populaires sur Ollama sont :

- llama2 : Le modèle le plus populaire pour une utilisation générale.
- mistral : Le modèle 7 B de Mistral AI, mis à jour vers la version 0.2.
- codellama : Un grand modèle linguistique qui utilise les entrées textuelles pour générer et discuter de code.
- dolphin-mixtral : Un modèle non censuré et affiné basé sur le Mixtral MoE, particulièrement adapté aux tâches de codage.
- mistral-openorca : Mistral 7 b, affiné avec l'ensemble de données OpenOrca.

Ollama prend également en charge les modèles personnalisés. Vous pouvez créer un modèle à l'aide d'un fichier modèle, en spécifiant les couches, en écrivant les poids et en recevant un message de réussite.

D'autres modèles disponibles incluent :

- Llama2 : Le modèle « open source » de base de Meta.
- Mistral/Mixtral : Un modèle à 7 milliards de paramètres affiné sur le modèle Mistral 7 B avec l'ensemble de données OpenOrca.
- LLaVA : Un modèle multimodal (assistant langage et vision) capable d'interpréter les entrées visuelles.
- CodeLlama : Un modèle entraîné sur le code et le langage naturel en anglais.
- DeepSeek Coder : Entraîné à 87 % sur du code et à 13 % sur du langage naturel en anglais.
- Meditron : Un modèle médical open source adapté de Llama 2 au domaine médical.

#### Installation et Configuration d'Ollama

- Téléchargez Ollama depuis le site officiel.
- L'installation est simple, similaire à celle d'autres logiciels. Pour macOS et Linux, utilisez `curl https://ollama.ai/install.sh | sh`.
- Ollama crée une API pour interagir avec le modèle localement.
- Ollama est compatible avec macOS et Linux. La prise en charge de Windows est en cours de développement.

Exécution de modèles avec Ollama

L'exécution des modèles est simple. Téléchargez les modèles et exécutez-les à l'aide de la commande "run" dans le terminal. Si un modèle n'est pas installé, Ollama le télécharge automatiquement. Par exemple, exécutez CodeLlama avec "ollama run codellama".

Les modèles sont enregistrés dans le répertoire ~/.ollama/models. Lors du téléchargement d'un modèle via "ollama pull", il est stocké dans ~/.ollama/models/manifests/registry.ollama.ai/library/<model-family>/latest.

Ollama offre également un accès API REST pour les interactions en temps réel.

Fonctionnalités supplémentaires

Ollama prend en charge l'importation de fichiers de modèles GGUF et GGML, permettant la création, l'itération et le partage des modèles.

Modèles disponibles

Une liste des modèles disponibles se trouve sur la page de la bibliothèque de modèles Ollama.

En résumé, Ollama fournit une plateforme conviviale pour exécuter les LLM localement. C'est une ressource précieuse pour les développeurs, les chercheurs et les passionnés d'IA.

### Étape 2 : Contrôle et Utilisation d'Ollama avec l'interface graphique Chatbox

Chatbox est une application qui visualise les appels API vers différents modèles.

![Interface graphique Chatbox](/images/blogs/chatbox.png)

### Installation de Chatbox

Visitez https://chatboxai.app et installez l'application sur votre ordinateur.

### Connexion de Chatbox et Ollama

Notre modèle IA local est accessible à l'adresse localhost :11434. Chatbox permet une interaction facile avec Ollama. Cliquez sur "Paramètres" et sélectionnez Ollama comme "Fournisseur de modèle IA".

![Paramètres Chatbox Ollama](/images/blogs/chatbox-settings.png)

Ensuite, sélectionnez le modèle souhaité (par exemple, `llama2`) dans la boîte de dialogue des modèles.

> Cela vous semble-t-il trop compliqué ? Ou un API hébergé serait-il préférable ? Utilisez [document-chat.com](/de/) ou [planifiez un appel introductif gratuit avec nous](https://datafortress.cloud/de/contact/).
