---
############################ Banner ##################################
banner:
  enable: true
  title: 'Chat with your **Documents**!'
  content: '**ChatGPT & co are too general**? **document-chat.com** knows your uploaded documents and responds with **specific company knowledge including sources**!'
  image: 'images/screenshots/banner-shot.png'
  video:
    enable: true
    video_embed_link: 'https://youtube.com/embed/DyKzi8NznQ0'
  form:
    enable: true
    form_action: 'https://formspree.io/f/xbjnpgko'
    button_label: 'Book a Personal Demo'
  form_freebie:
    enable: true
    form_action: 'https://formspree.io/f/xbjnpgko'
    button_label: 'Free PDF Tutorial'
    pdf_explanation: "In this free PDF, you'll learn how to use ChatGPT with documents, the challenges with GDPR & co, and step-by-step instructions on setting up a self-hosted solution."
  button:
    enable: true
    label: 'Try for Free'
    link: 'pricing'
    content: 'No credit card required. Works in all browsers.'

########################## Clients Logo Slider #########################
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

########################## How it works #########################
homepage_tab:
  enable: true
  title: 'How it **Works**'
  content: 'Upload your documents and emails, and ask our AI questions about them. It will remember all notes and emails, and respond with specific company knowledge! Have a team? Build a knowledge base that only your team can see!'
  tablist:
    # tab item
    - name: 'Upload Documents'
      title: '**Upload** Documents'
      image: 'images/screenshots/mainscreen.png'
      content: 'Upload documents (word, powerpoint, txt, pdf, ...), emails, or notes, and our AI will read them on secure German servers.'
      button:
        enable: true
        label: 'Learn More'
        link: 'how-it-works'

    # tab item
    - name: 'Start Chatting'
      title: '**Start** Chatting'
      image: 'images/screenshots/chat-zoom.png'
      content: 'After uploading, you can ask the AI any questions, and it will answer with knowledge from the documents, even including sources and citations!'
      button:
        enable: true
        label: 'Learn More'
        link: 'how-it-works'

    # tab item
    - name: 'Different Projects'
      title: '**Different** Projects'
      image: 'images/screenshots/mainscreen.png'
      content: "ChatGPT & Co don't really allow separation of knowledge by projects. What if certain team members are only allowed to see certain projects? What if you constantly get answers with knowledge from other projects? document-chat.com allows separation of knowledge by projects and teams."
      button:
        enable: true
        label: 'Learn More'
        link: 'how-it-works'

    # tab item
    - name: 'Company Knowledge'
      title: '**Company Knowledge**'
      image: 'images/screenshots/chat.png'
      content: "Build the ultimate company knowledge database. We're happy to help with reading in internal documentation such as Confluence, Jira, Gitlab, etc., so you can provide your employees or customers with an internal chatbot with all their company knowledge!"
      button:
        enable: true
        label: 'Learn More'
        link: 'how-it-works'

########################## How to use #########################
homepage_howtouse:
  enable: true
  title: '**Use Cases**'
  content: 'document-chat.com can be used in many areas. Here are some examples of how you can use document-chat.com for yourself and in your company.'
  tablist:
    # tab item
    - name: 'Email Search'
      title: '**Search** Emails'
      image: 'images/screenshots/chat-history.png'
      content: "Unlike Outlook & co, you don't have to hit the exact word, our AI can also retrieve knowledge from context. So you'll also find hits for searches like 'what was the price in the XY offer?', instead of scrolling through the timeline."
      button:
        enable: true
        label: 'Learn More'
        link: 'how-it-works'

    # tab item
    - name: 'Summarize Documents'
      title: '**Summarize** Documents'
      image: 'images/screenshots/documents.png'
      content: "Your documents are messy and only named 'final_final_final.docx'? Our AI can create a summary for you, helping you get to the important information faster."
      button:
        enable: true
        label: 'Learn More'
        link: 'how-it-works'

    # tab item
    - name: 'Company Knowledge for Marketing'
      title: '**Company Knowledge** for Marketing'
      image: 'images/screenshots/documents.png'
      content: "ChatGPT & Co know nothing about your company. Commands like 'write an ad text for the XY fridge' don't work. Our AI can do this, as long as it has been fed with enough information from the documents. This allows you to give specific instructions like 'write an ad text for the XY fridge targeting 18-25 year olds'."
      button:
        enable: true
        label: 'Learn More'
        link: 'how-it-works'

    # tab item
    - name: 'Strategic Decisions'
      title: '**Strategic** Decisions'
      image: 'images/screenshots/chat-zoom.png'
      content: 'Do you know the situation where you get too lost in a topic, and there may be more important focus areas? Our AI can help you with the overview, as it can remember much more information than you. This way, you can make decisions faster and more efficiently.'
      button:
        enable: true
        label: 'Learn More'
        link: 'how-it-works'

############################## Tools in Use ########################
tools:
  enable: false
  title: 'Use your **existing tools** as a source of information'
  content: 'We support'
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

############################## Achievement ##############################
achivement:
  enable: true
  title: 'Boost your productivity with an **all-knowing assistant**'
  content: 'How much time do you spend searching for old emails and notes? What if your virtual assistant could remember every document, email, and note from the past years?'
  funfacts:
    - name: 'Average time saved per week'
      count: '18'
      extension: 'h'

    - name: 'per summary'
      count: '5'
      extension: 's'

    - name: 'Reduction in misinformation'
      count: '34'
      extension: '%'

  services:
    - name: '24/7 personal AI assistant'
      icon: 'far fa-thumbs-up' # fontawesome icon : https://fontawesome.com/icons

    - name: 'Personal onboarding'
      icon: 'far fa-comment-dots' # fontawesome icon : https://fontawesome.com/icons

    - name: 'Made in Germany'
      icon: 'fas fa-globe' # fontawesome icon : https://fontawesome.com/icons

    - name: 'GDPR compliant'
      icon: 'fas fa-shield-alt' # fontawesome icon : https://fontawesome.com/icons

############################## Workflow ################################
workflow:
  enable: true
  title: 'Do you have **sensitive data**?'
  image: 'images/screenshots/mainscreen.png'
  content: 'We also offer the option to use our AI models hosted in Germany, so that you can comply with all information security requirements (BaFin / Hospital Information Security Law).'

############################## about us ################################
about_us:
  enable: true
  title: 'Who are **we?**'
  image: 'images/about/01.jpg'
  content: 'DataFortress.cloud is a company based in Augsburg, Germany, specializing in Data Engineering in the Machine Learning / Big Data field. Our clients include VW, BMW, Porsche, HPE, Atruvia (Sparkasse & Volksbank), and many more. Now, we also offer our expertise in the form of SaaS products.'
  bulletpoints:
    - 'Enterprise clients (VW, BMW, Porsche, HPE, Atruvia (Sparkasse & Volksbank), and many more)'
    - 'Data Engineering Data Protection Knowledge for Finance / Health'
    - 'Missing something in this solution? We can also develop a custom solution for you!'

############################# Testimonial ############################
testimonial:
  enable: true
  title: 'What our **customers** say'
  content: 'See for yourself the performance of our AI!'
  button:
    enable: true
    label: 'View all testimonials'
    link: 'testimonial'

  testimonial_item:
    - name: 'Max Linnemann'
      image: 'images/users/01.jpg'
      designation: 'Founder'
      content: "I use document-chat.com to search my emails. Outlook search never really worked for me, but document-chat.com always finds what I'm looking for! Top!"

    - name: 'Mark Hermann'
      image: 'images/users/02.jpg'
      designation: 'CEO'
      content: 'We use document-chat.com as an internal knowledge database. Our Confluence pages are relatively well maintained, but the search function is just not as good, or information gets lost. The document-chat.com chatbot is integrated into our intranet, and can answer questions from employees much faster.'
---
