---
title : "Was sind die Vorteile von selbst gehosteten KI Modellen?"
image : "images/blogs/procontrakimodelle.jpg"
date: 2020-04-09T08:40:24+06:00
author: "Justin Güse"
author_profile: "https://www.linkedin.com/in/justin-guese/"
description : "this is meta description"
categories: [ "Chatbot", "AI", "DIY"]
draft : false
---

## Einleitung 

In der Welt der künstlichen Intelligenz (KI) haben sich große Sprachmodelle wie GPT (Generative Pre-trained Transformer) als leistungsstarke Werkzeuge für eine Vielzahl von Anwendungen etabliert. Unternehmen sollten jedoch vorsichtig sein, sich zu stark auf diese Modelle zu verlassen. Während sie Genauigkeit und Skalierbarkeit bieten, haben sie auch ihre Grenzen. Sie können aufgrund von Einschränkungen bei den Trainingsdaten voreingenommene oder falsche Antworten liefern und sind nicht in der Lage, den menschlichen Kontext und Feinheiten vollständig zu verstehen.

In diesem Blog-Beitrag werden wir uns mit den Vorteilen von selbst gehosteten KI-Modellen auseinandersetzen. Selbst gehostete Modelle bieten Unternehmen eine größere Kontrolle über ihre KI-Infrastruktur, was zu einer besseren Leistung, Anpassungsfähigkeit und Datenschutz führen kann. Indem sie das Modell auf ihren eigenen Servern hosten, können Unternehmen sicherstellen, dass ihre proprietären Daten unter ihrer Kontrolle bleiben und Bedenken hinsichtlich Datensicherheit und Datenschutz adressiert werden.

Allerdings birgt die Selbst-Hosting auch Herausforderungen. Es erfordert erhebliche Investitionen in Hardware und Fachkenntnisse, um die Infrastruktur zu verwalten und zu warten. Darüber hinaus liegt die Verantwortung für die Aktualisierung des Modells, um neue Informationen zu berücksichtigen, und für den Schutz vor Sicherheitslücken vollständig beim Unternehmen. Angesichts des raschen Fortschritts in der KI und der Cybersicherheit kann dies eine anspruchsvolle Aufgabe sein.

Insgesamt repräsentieren große Sprachmodelle einen bedeutenden Fortschritt in der KI und bieten Unternehmen das Potenzial für Innovation und Effizienzsteigerung. Doch ihre Grenzen und die Komplexität von Feinabstimmung und Selbst-Hosting erfordern einen vorsichtigen Ansatz. Unternehmen müssen die Vorteile dieser leistungsstarken Werkzeuge gegen die Risiken einer übermäßigen Abhängigkeit, Ungenauigkeiten und ethischen Bedenken abwägen. Indem sie dies tun, können sie das Potenzial von selbst gehosteten KI-Modellen nutzen und gleichzeitig die Risiken im Zusammenhang mit diesen wegweisenden Technologien mindern.

## Warum nicht einfach ein Cloud-Modell verwenden?

Es gibt mehrere Gründe, warum Unternehmen und Privatpersonen sich für das Selbsthosting von KI-Modellen entscheiden. Einer der Hauptgründe ist die Datensicherheit. Bei der Verwendung von Modellen von Anbietern wie OpenAI besteht die Möglichkeit, dass die eingegebenen Daten als Trainingsmaterial verwendet werden. Durch das Selbsthosting können Unternehmen sicherstellen, dass ihre sensiblen Daten unter ihrer Kontrolle bleiben und nicht für Trainingszwecke verwendet werden.

> Tipp: 
Um die Nutzung Ihrer Daten durch die amerikanischen AI Anbieter wie OpenAI zu vermeiden, sollten Sie ein „selbstgehostetes“ AI Modell betreiben.
Dazu benötigen Sie einen Server mit einer Nvidia GPU, und einem entsprechenden „torch“ setup. Für DIY empfiehlt sich z.B. das Open Source Projekt https://ollama.com.
Alternativ ist ein deutscher KI Provider nötig, wie z.B. https://document-chat.com oder https://datafortress.cloud. document-chat.com bietet außerdem die Unterteilung nach Projekten, nützliche Sharing/Team Features und viel mehr!

Ein weiterer wichtiger Aspekt ist die Kostenersparnis. Selbst gehostete Modelle sind in der Regel kostenfrei oder erfordern nur geringe Lizenzgebühren im Vergleich zu den hohen Kosten, die mit der Nutzung von Modellen von Drittanbietern verbunden sein können. Dies macht selbst gehostete Modelle zu einer wirtschaftlich attraktiven Option für Unternehmen jeder Größe.

Der Schutz der Privatsphäre ist ein weiterer entscheidender Faktor. Durch das Selbsthosting behalten Unternehmen die Kontrolle über ihre Daten und können sicherstellen, dass sie nicht an Dritte weitergegeben werden. Dies ist insbesondere in Branchen mit strengen Datenschutzbestimmungen von großer Bedeutung.

Zusammenfassend bietet das Selbsthosting von KI-Modellen Vorteile wie verbesserte Datensicherheit, Kostenersparnis und Wahrung der Privatsphäre. Unternehmen können die volle Kontrolle über ihre KI-Infrastruktur behalten und gleichzeitig von den Vorteilen dieser leistungsstarken Technologie profitieren.

## Was benötige ich um ein selbst gehostetes KI-Modell zu betreiben?

Um ein selbst gehostetes KI-Modell zu betreiben, benötigen Sie einige spezifische Ressourcen. Ein wichtiger Bestandteil ist ein Nvidia-GPU-Server, da GPUs für das Training und die Ausführung von KI-Modellen eine hohe Rechenleistung bieten. Es ist jedoch wichtig zu beachten, dass Nvidia-GPU-Server ziemlich teuer sein können und eine beträchtliche Investition erfordern können.

Glücklicherweise gibt es Open-Source-Projekte wie Ollama, die das Hosting von KI-Modellen erleichtern. Ollama ist ein Projekt auf GitHub (https://github.com/ollama/ollama), das eine einfache und benutzerfreundliche Möglichkeit bietet, Modelle selbst zu hosten. Es bietet Tools und Ressourcen, um den Prozess des Selbsthostings zu vereinfachen und zu automatisieren.

Mit Ollama und einem geeigneten Nvidia-GPU-Server können Sie Ihr eigenes KI-Modell betreiben und von den Vorteilen des Selbsthostings profitieren, ohne die volle finanzielle Belastung eines dedizierten Servers tragen zu müssen.

Es ist wichtig zu beachten, dass das Betreiben eines selbst gehosteten KI-Modells weiterhin technisches Fachwissen erfordert. Es kann hilfreich sein, über Kenntnisse in den Bereichen Maschinelles Lernen und Serververwaltung zu verfügen oder Experten hinzuzuziehen, um Ihnen bei der Einrichtung und Wartung zu helfen.

Mit den richtigen Ressourcen und Tools wie Ollama können Sie Ihr eigenes KI-Modell betreiben und die Vorteile des Selbsthostings nutzen, um Kontrolle, Datensicherheit und Kostenersparnis zu gewährleisten.

### Und was für einen Server brauche ich für die Modelle?

Zuerst sollte man abwegen, was man von dem Modell erwartet. "Coding Assistenten" á la Github Copilot brauchen weniger ressourcen und kommen mit einer GPU mit ~8GB VRAM aus. Für größere Modelle welche sich ähnlich ChatGPT verhalten braucht man schon mindestens 16 GB VRAM. Erwartet man eine Performance von GPT-4 muss man schon mehr Geschütze auffahren, und sollte sich an einem GPU Cluster mit mindestens 64 GB VRAM orientieren.

Eine kleine Übersicht der Modelle, und wie viel Speicherplatz sie benötigen findet man hier:


| Model              | Parameters | Benötigte VRAM  |
| ------------------ | ---------- | ----- |
| Llama 2            | 7B         | 8 GB |
| Mistral            | 7B         | 8 GB |
| Dolphin Phi        | 2.7B       | 8 GB |
| Phi-2              | 2.7B       | 8 GB |
| Neural Chat        | 7B         | 8 GB |
| Starling           | 7B         | 8 GB |
| Code Llama         | 7B         | 8 GB |
| Llama 2 Uncensored | 7B         | 8 GB |
| Llama 2 13B        | 13B        | 16 GB |
| Llama 2 70B        | 70B        | 64 GB |
| Orca Mini          | 3B         | 8 GB |
| Vicuna             | 7B         | 8 GB |
| LLaVA              | 7B         | 8 GB |
| Gemma              | 2B         | 8 GB |
| Gemma              | 7B         | 8 GB |


#### Und was für eine GPU ist das konkret?

Leider ist NVIDIA derzeit im Monopol was AI GPUs angeht. Man kann auch mit technischen "Hacks" eine AMD GPU verwenden, jedoch ist die Performance und Kompatibilität nicht mit allen Projekten gegeben, bzw. muss man die benötigte Arbeitszeit vs. die Kosten für eine NVIDIA GPU abwägen.

Die Server GPU Linie von NVIDIA kommt mit einem stolzen Preis daher, weshalb es durchaus Sinn machen kann die Gaming-GPU's von NVIDIA zu verwenden.

Da es nicht nur auf die VRAM, sondern auch die Tensor-Cores ("AI Cores") ankommt, macht es durchaus Sinn die 4000er Reihe von NVIDIA zu verwenden anstatt der 3000er Modelle. 

| NVIDIA GPU Name | VRAM | Geeignet für ... | Preis |
| --------------- | ---- | ---------------- | ----- |
| [RTX 4070](https://www.amazon.de/gp/search?ie=UTF8&tag=qaau-21&linkCode=ur2&linkId=94e67979004555721e100e26a68f7c05&camp=1638&creative=6742&index=computers&keywords=rtx+4070)        | 12 GB | Coding Completion, sehr simple Tasks (fasse Zusammen, korrigiere, sortiere, ...) | ~648€ |
| [RTX 4080](https://www.amazon.de/gp/search?ie=UTF8&tag=qaau-21&linkCode=ur2&linkId=94e67979004555721e100e26a68f7c05&camp=1638&creative=6742&index=computers&keywords=rtx+4080)        | 16 GB | Schreibe einen Text über, generiere Code, Leistung ~60% von gpt-3.5 | ~1.100€ |
| [RTX 4090](https://www.amazon.de/gp/search?ie=UTF8&tag=qaau-21&linkCode=ur2&linkId=94e67979004555721e100e26a68f7c05&camp=1638&creative=6742&index=computers&keywords=rtx+4090)       | 24 GB | Schreibe einen Text über, generiere Code, Leistung ~80% von gpt-3.5 | ~1.900€ |

> Das klingt zu stressig? Oder wäre besser als Hosted API? Nutzen Sie [document-chat.com](/de/) oder [lassen sie sich in einem kostenlosen Erstgespräch von uns beraten](https://datafortress.cloud/de/contact/).

## Die Vor- und Nachteile des selbst gehosteten KI-Modellen


Das selbst gehostete KI-Modell bietet eine Reihe von Vor- und Nachteilen im Vergleich zu anderen Hosting-Optionen wie Cloud-basierten Plattformen. Einer der Vorteile des selbst gehosteten Modells ist die Skalierbarkeit. Unternehmen haben die volle Kontrolle über ihre Infrastruktur und können das Modell an ihre spezifischen Anforderungen und Ressourcen anpassen. Dies ermöglicht eine bessere Skalierbarkeit und Leistungsoptimierung.

Ein weiterer Vorteil ist die Flexibilität. Durch das selbst gehostete Modell haben Unternehmen die Freiheit, eigene Anpassungen vorzunehmen und das Modell nach Belieben anzupassen. Dies ermöglicht eine größere Anpassungsfähigkeit an spezifische Anwendungsfälle und Geschäftsanforderungen.

Jedoch gibt es auch einige Nachteile beim selbst gehosteten Modell. Ein wesentlicher Aspekt ist der Wartungsaufwand. Unternehmen sind dafür verantwortlich, das Modell auf dem neuesten Stand zu halten, Patches und Updates einzuspielen und die Sicherheit zu gewährleisten. Dies erfordert technisches Fachwissen und Ressourcen für die Serververwaltung.

Ein weiterer Faktor ist die Kostenfrage. Obwohl das selbst gehostete Modell langfristig kosteneffizient sein kann, erfordert es zunächst eine erhebliche Investition in Hardware und Expertise. Dies kann für kleinere Unternehmen oder Start-ups eine finanzielle Herausforderung darstellen.

Es ist wichtig, die Vor- und Nachteile gründlich abzuwägen und die individuellen Anforderungen des Unternehmens zu berücksichtigen. Ein selbst gehostetes Modell bietet mehr Kontrolle und Anpassungsfähigkeit, erfordert aber auch mehr Verantwortung und Ressourcen. Cloud-basierte Plattformen können hingegen eine schnellere Bereitstellung und geringeren Wartungsaufwand bieten, jedoch mit weniger Kontrolle und Anpassungsmöglichkeiten. Es ist ratsam, die spezifischen Bedürfnisse und Möglichkeiten des Unternehmens zu analysieren, um die beste Hosting-Option zu wählen.

> Das klingt zu stressig? Oder wäre besser als Hosted API? Nutzen Sie [document-chat.com](/de/) oder [lassen sie sich in einem kostenlosen Erstgespräch von uns beraten](https://datafortress.cloud/de/contact/).