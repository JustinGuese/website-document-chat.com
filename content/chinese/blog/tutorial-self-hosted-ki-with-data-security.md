---
author: 贾斯丁·古斯
author_profile: https://www.linkedin.com/in/justin-guese/
categories:
- 聊天机器人
- KI
- DIY
- 教程
date: '2020-04-09T07:40:24+06:00'
description: 这是一个元描述
draft: false
image: images/blogs/chatbox.jpeg
title: 教程：使用 Ollama 和 Chatbox 进行数据安全自托管 AI(或更详细的翻译，更符合语境，需要提供更多上下文)

---
## 问题：75% 的公司禁止使用 ChatGPT

尽管最初对生成式 AI 工具（例如 ChatGPT）充满热情，但由于日益增长的数据隐私和网络安全担忧，公司正在考虑限制其使用。主要担忧是这些 AI 工具会存储用户数据并从中学习，这可能会导致意外的数据泄露。尽管 ChatGPT 的开发商 OpenAI 提供了拒绝参与训练用户数据的选项，但数据在系统内的处理方式仍然不明确。此外，缺乏明确的法律法规来规范由 AI 造成的违规行为。因此，公司越来越谨慎，并等待着该技术的进一步发展和监管。

微软已警告其员工不要与 ChatGPT（由 OpenAI 开发的聊天机器人）共享敏感数据 [来源](https://www.businessinsider.com/chatgpt-microsoft-warns-employees-not-to-share-sensitive-data-openai-2023-1)。担忧的是，机密信息可能会意外地与聊天机器人共享，然后该聊天机器人可能会与其他用户共享这些信息。考虑到微软与 OpenAI 建立了合作关系并投资于 OpenAI，其谨慎的做法值得关注。亚马逊也向其员工发出了类似的警告。目前，对于保护机密数据的责任尚不明确，并且需要针对这种情况制定更清晰的政策和法规。OpenAI 的用户协议允许该公司使用用户和 ChatGPT 生成的所有输入和输出，同时应删除个人数据。但是，人们仍然担心通过精心设计的输入提示提取私人公司数据的能力。

## 解决方法：自托管 AI 模型

解决使用 AI 模型时数据安全和数据隐私的担忧的一种方法是自托管这些模型。这使公司能够控制其数据，并确保数据不会落入不当之手。自托管 AI 模型提供了一种安全可靠的方式来使用 AI 技术，而无需担心数据隐私和网络安全问题。

我们将使用 **Ollama** 和 **Chatbox**。Ollama 是一个优化的工具，用于在本地运行开源大型语言模型（LLM），例如 Mistral 和 Llama 2。Chatbox 是一种应用程序，可用于可视化对不同模型的 API 调用。

> 这听起来太麻烦了吗？还是托管 API 更合适？请使用 [document-chat.com](/de/) 或 [与我们进行免费的初步咨询](https://datafortress.cloud/de/contact/)。


### 第 1 步：Ollama 下载和安装

您需要一台拥有 GPU 的服务器或计算机。不幸的是，这必须是具有至少 8GB VRAM 的 NVidia GPU，或具有 M 系列芯片的 Macbook。
您可以从以下文章中找到确切的要求： [自托管 AI 模型的优势是什么？](/de/blog/vorteile-von-selbst-gehosteten-ki-modellen/)


> TLDR 版本：
> 1. https://ollama.com/download
> 2. `ollama run llama2`
> 3. 可以在 localhost:11434 访问 ollama


#### Ollama 是什么？

Ollama 是一个优化的工具，用于在本地运行开源大型语言模型（LLM），例如 Mistral 和 Llama 2。Ollama 将模型权重、配置和数据集组合成一个统一的实体，由一个模型文件管理。


> 这听起来太麻烦了吗？还是托管 API 更合适？请使用 [document-chat.com](/de/) 或 [与我们进行免费的初步咨询](https://datafortress.cloud/de/contact/)。


Ollama 支持各种 LLM，包括 LLaMA-2、未经审查的 LLaMA、CodeLLaMA、Falcon、Mistral、Vicuna 模型、WizardCoder 和未经审查的 Wizard。

Ollama 支持多种模型，包括 Llama 2、Code Llama 和其他模型。它将模型权重、配置和数据组合到一个单元中，该单元由模型文件定义。

Ollama 上五个最受欢迎的模型是：

- llama2：最常用的通用模型。
- mistral：Mistral AI 的 7B 模型，更新到 0.2 版本。
- codellama：一种大型语言模型，使用文本输入生成和讨论代码。
- dolphin-mixtral：基于 Mixtral MoE 的未经审查的微调模型，特别适用于编码任务。
- mistral-openorca：Mistral 7b，使用 OpenOrca 数据集微调。

Ollama 还支持创建和使用自定义模型。您可以使用模型文件创建模型，在其中传递模型文件、创建各种层、编写权重并最终获得成功消息。


其他一些可在 Ollama 上使用的模型包括：

- Llama2：Meta 的基本“开源”模型
- Mistral/Mixtral：一个 70 亿参数模型，基于 Mistral 7B 模型，已使用 OpenOrca 数据集微调。
- Llava：一种名为 LLaVA（大型语言和视觉助手）的多模态模型，可以解释视觉输入。
- CodeLlama：在英语的代码和自然语言上都经过训练的模型。
- DeepSeek Coder：从头开始在英语的 87% 代码和 13% 自然语言上训练。
- Meditron：一种开源医疗模型，已将 Llama 2 适配到医疗领域。


#### Ollama 安装和配置

- 从官方网站下载 Ollama。
- 下载后，安装过程简单，类似于其他软件的安装过程。对于 macOS 和 Linux 用户，可以使用命令 curl https://ollama.ai/install.sh | sh 安装 Ollama。
- 一旦安装好 Ollama，它就会创建一个 API，通过该 API 提供模型，因此用户可以直接从本地计算机与模型进行交互。
- Ollama 与 macOS 和 Linux 兼容，对 Windows 的支持即将推出。它易于安装和使用，用于在本地运行各种开源模型。您可以从 Ollama 库中选择所需的模型。


使用 Ollama 运行模型

使用 Ollama 运行模型是一个简单的过程。用户可以下载模型，并使用终端应用程序中的“运行”命令运行模型。如果模型未安装，Ollama 会自动下载它。例如，要运行 CodeLlama 模型，请使用命令“ollama run codellama”。

模型存储在您本地计算机的 ~/.ollama/models 目录结构中。如果您使用命令“ollama pull”下载模型，它将存储在 ~/.ollama/models/manifests/registry.ollama.ai/library/<模型系列>/latest 目录中。

Ollama 还支持通过 REST API 使用模型进行实时交互。


其他功能

Ollama 的独特功能之一是支持在模型文件中导入 GGUF 和 GGML 文件格式。这意味着您可以创建模型、在此基础上构建、迭代改进模型并将其上传，以便在准备好时与其他人共享。


可用模型

Ollama 支持多种模型，您可以在 Ollama 模型库页面上找到可用模型的列表。


总而言之，Ollama 提供了一个易于使用的环境，用于在本地运行大型语言模型。对于开发人员、研究人员和 AI 爱好者而言，这是一个强大的工具，可用于利用 LLM 的潜力。


### 第 2 步：使用 Chatbox GUI 控制和利用 Ollama

Chatbox 是一种应用程序，可用于可视化对不同模型的 API 调用。

![Chatbox GUI](/images/blogs/chatbox.png)


### Chatbox 安装

访问 https://chatboxai.app 并安装应用程序到您的计算机上。


### 连接 Chatbox 和 Ollama

如前文所述，我们的本地 AI 模型现在可以在 localhost:11434 上访问。
幸运的是，Chatbox 提供了一种简单的方法来与 Ollama 进行交互。为此，请点击“设置”，并在“AI 模型提供商”中选择 Ollama。


![Chatbox 设置 Ollama](/images/blogs/chatbox-settings.png)


然后，您只需要从模型对话框中选择要使用 `olama run` 命令选择的模型，例如在我们的例子中为 `llama2`。

> 这听起来太麻烦了吗？还是托管 API 更合适？请使用 [document-chat.com](/de/) 或 [与我们进行免费的初步咨询](https://datafortress.cloud/de/contact/)。
