---
############################ 横幅 ##################################
banner:
  enable: true
  title: '与您的**文档**聊天！'
  content: '**ChatGPT & co 太过通用**？**document-chat.com**了解您上传的文档，并以**具体的公司知识和来源**进行回应！'
  image: 'images/screenshots/banner-shot.png'
  video:
    enable: true
    video_embed_link: 'https://youtube.com/embed/DyKzi8NznQ0'
  form:
    enable: true
    form_action: 'https://formspree.io/f/xbjnpgko'
    button_label: '预约个人演示'
  form_freebie:
    enable: true
    form_action: 'https://formspree.io/f/xbjnpgko'
    button_label: '免费PDF教程'
    pdf_explanation: '在这份免费的PDF中，您将学习如何使用ChatGPT与文档，了解GDPR等的挑战，并获得设置自托管解决方案的分步说明。'
  button:
    enable: true
    label: '免费试用'
    link: 'pricing'
    content: '无需信用卡。适用于所有浏览器。'

########################## 客户标志滑块 #########################
clients_logo_slider:
  enable: false
  logos:
    - 'images/brands/01-colored.png'
    - 'images/brands/02-colored.png'
    - 'images/brands/03-colored.png'
    - 'images/brands/04-colored.png'
    - 'images/brands/05-colored.png'
    - 'images/brands/06-colored.png'
    - 'images/brands/01-colored.png'
    - 'images/brands/02-colored.png'
    - 'images/brands/03-colored.png'
    - 'images/brands/04-colored.png'
    - 'images/brands/05-colored.png'
    - 'images/brands/06-colored.png'

########################## 工作原理 #########################
homepage_tab:
  enable: true
  title: '工作**原理**'
  content: '上传您的文档和电子邮件，并向我们的AI询问相关问题。它会记住所有的笔记和电子邮件，并以具体的公司知识进行回应！有团队吗？建立一个只有您的团队可以看到的知识库！'
  tablist:
    # tab item
    - name: '上传文档'
      title: '**上传**文档'
      image: 'images/screenshots/mainscreen.png'
      content: '上传文档（word、powerpoint、txt、pdf等）、电子邮件或笔记，我们的AI将在安全的德国服务器上读取它们。'
      button:
        enable: true
        label: '了解更多'
        link: 'how-it-works'

    # tab item
    - name: '开始聊天'
      title: '**开始**聊天'
      image: 'images/screenshots/chat-zoom.png'
      content: '上传后，您可以向AI询问任何问题，它将以文档中的知识进行回答，甚至包括来源和引用！'
      button:
        enable: true
        label: '了解更多'
        link: 'how-it-works'

    # tab item
    - name: '不同项目'
      title: '**不同**项目'
      image: 'images/screenshots/mainscreen.png'
      content: 'ChatGPT & Co 不允许按项目分离知识。如果某些团队成员只能看到某些项目怎么办？如果您不断收到来自其他项目的知识回答怎么办？document-chat.com 允许按项目和团队分离知识。'
      button:
        enable: true
        label: '了解更多'
        link: 'how-it-works'

    # tab item
    - name: '公司知识'
      title: '**公司知识**'
      image: 'images/screenshots/chat.png'
      content: '建立终极公司知识数据库。我们很乐意帮助读取内部文档，如Confluence、Jira、Gitlab等，以便您可以为员工或客户提供一个包含所有公司知识的内部聊天机器人！'
      button:
        enable: true
        label: '了解更多'
        link: 'how-it-works'

########################## 使用案例 #########################
homepage_howtouse:
  enable: true
  title: '**使用案例**'
  content: 'document-chat.com 可以在许多领域使用。以下是一些您可以为自己和公司使用 document-chat.com 的示例。'
  tablist:
    # tab item
    - name: '电子邮件搜索'
      title: '**搜索**电子邮件'
      image: 'images/screenshots/chat-history.png'
      content: '与Outlook等不同，您不必准确输入单词，我们的AI也可以从上下文中检索知识。因此，您还会找到诸如“XY报价中的价格是多少？”之类的搜索结果，而不是滚动时间线。'
      button:
        enable: true
        label: '了解更多'
        link: 'how-it-works'

    # tab item
    - name: '总结文档'
      title: '**总结**文档'
      image: 'images/screenshots/documents.png'
      content: '您的文档杂乱无章，只命名为“final_final_final.docx”？我们的AI可以为您创建摘要，帮助您更快地获取重要信息。'
      button:
        enable: true
        label: '了解更多'
        link: 'how-it-works'

    # tab item
    - name: '营销的公司知识'
      title: '**公司知识**用于营销'
      image: 'images/screenshots/documents.png'
      content: 'ChatGPT & Co 对您的公司一无所知。诸如“为XY冰箱写一段广告文案”之类的命令不起作用。只要有足够的文档信息，我们的AI可以做到这一点。这使您可以给出具体的指示，例如“为18-25岁的人群写一段针对XY冰箱的广告文案”。'
      button:
        enable: true
        label: '了解更多'
        link: 'how-it-works'

    # tab item
    - name: '战略决策'
      title: '**战略**决策'
      image: 'images/screenshots/chat-zoom.png'
      content: '您是否遇到过在一个话题中迷失太久，可能有更重要的关注点？我们的AI可以帮助您掌握全局，因为它可以记住比您更多的信息。这样，您可以更快、更高效地做出决策。'
      button:
        enable: true
        label: '了解更多'
        link: 'how-it-works'

############################## 使用工具 ########################
tools:
  enable: false
  title: '使用您**现有的工具**作为信息来源'
  content: '我们支持'
  logos:
    - 'images/tools/01.png'
    - 'images/tools/02.png'
    - 'images/tools/03.png'
    - 'images/tools/04.png'
    - 'images/tools/05.png'
    - 'images/tools/06.png'
    - 'images/tools/07.png'
    - 'images/tools/08.png'
    - 'images/tools/05.png'

############################## 成就 ##############################
achivement:
  enable: true
  title: '通过**全知助手**提升您的生产力'
  content: '您花费多少时间搜索旧电子邮件和笔记？如果您的虚拟助手可以记住过去几年的每一份文档、电子邮件和笔记呢？'
  funfacts:
    - name: '每周平均节省时间'
      count: '18'
      extension: '小时'

    - name: '每次总结'
      count: '5'
      extension: '秒'

    - name: '错误信息减少'
      count: '34'
      extension: '%'

  services:
    - name: '24/7个人AI助手'
      icon: 'far fa-thumbs-up' # fontawesome图标 : https://fontawesome.com/icons

    - name: '个人入职培训'
      icon: 'far fa-comment-dots' # fontawesome图标 : https://fontawesome.com/icons

    - name: '德国制造'
      icon: 'fas fa-globe' # fontawesome图标 : https://fontawesome.com/icons

    - name: '符合GDPR'
      icon: 'fas fa-shield-alt' # fontawesome图标 : https://fontawesome.com/icons

############################## 工作流程 ################################
workflow:
  enable: true
  title: '您有**敏感数据**吗？'
  image: 'images/screenshots/mainscreen.png'
  content: '我们还提供在德国托管的AI模型选项，以便您可以遵守所有信息安全要求（BaFin / 医院信息安全法）。'

############################## 关于我们 ################################
about_us:
  enable: true
  title: '我们是**谁？**'
  image: 'images/about/01.jpg'
  content: 'DataFortress.cloud 是一家总部位于德国奥格斯堡的公司，专注于机器学习/大数据领域的数据工程。我们的客户包括大众、宝马、保时捷、HPE、Atruvia（Sparkasse & Volksbank）等。现在，我们还以SaaS产品的形式提供我们的专业知识。'
  bulletpoints:
    - '企业客户（大众、宝马、保时捷、HPE、Atruvia（Sparkasse & Volksbank）等）'
    - '金融/健康领域的数据工程数据保护知识'
    - '在此解决方案中缺少什么？我们还可以为您开发定制解决方案！'

############################# 客户评价 ############################
testimonial:
  enable: true
  title: '我们的**客户**怎么说'
  content: '亲自体验我们的AI性能！'
  button:
    enable: true
    label: '查看所有评价'
    link: 'testimonial'

  testimonial_item:
    - name: '马克斯·林内曼'
      image: 'images/users/01.jpg'
      designation: '创始人'
      content: '我使用document-chat.com搜索我的电子邮件。Outlook搜索对我来说从未真正奏效，但document-chat.com总能找到我想要的东西！顶级！'

    - name: '马克·赫尔曼'
      image: 'images/users/02.jpg'
      designation: '首席执行官'
      content: '我们使用document-chat.com作为内部知识数据库。我们的Confluence页面维护得相对较好，但搜索功能不够好，或者信息丢失。document-chat.com聊天机器人集成到我们的内部网中，可以更快地回答员工的问题。'
---
