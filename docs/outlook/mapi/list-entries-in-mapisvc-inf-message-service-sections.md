---
title: Listeneinträge in den Nachrichtendienstabschnitten von MapiSvc.inf
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f4f052d6-ef63-421a-9d8c-4f3c6df83863
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: c5b5c468b56e5b34d265e7f00bbee96142a88e1c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591121"
---
# <a name="list-entries-in-mapisvcinf-message-service-sections"></a>Listeneinträge in den Nachrichtendienstabschnitten von MapiSvc.inf

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Es gibt zwei Arten der Abschnitt Listeneinträge: eine, die auflistet Service Provider Abschnitte und eine, die verschiedene Nachricht dienstspezifische Abschnitte auflistet. Diese zwei Arten von Einträgen in mapisvc.inf über die folgenden Formate angezeigt:
  
```cpp
Providersprovider section1, provider section2, ...... provider sectionX
Sectionssection name1, section name2, ......section nameX

```

Alle Abschnitte in der **Anbieter** -Eintrag ordnet einen einzelnen Bereich Bereitstellen von Konfigurationsinformationen für einen-Dienstanbieter, der den Dienst gehört. Jeder Abschnitt in den **Abschnitten** Eintrag ordnet einen Abschnitt, der zusätzliche Konfigurationsinformationen enthält, die den Dienst benötigt. Nachricht Service Implementierer definieren Sie zusätzliche Abschnitte Wenn werden spezielle Informationen enthalten, die nicht in den Abschnitten standard passt sollen. Message-Dienste, die in der Regel Konfigurationen kompliziert haben verwenden den Eintrag **Abschnitte** , um zusätzliche Informationen hinzuzufügen. Jede Nachricht Dienste im Abschnitt hat einen **Anbieter** -Eintrag mit mindestens einem Bereich in der Liste. nicht alle Abschnitte der Nachricht-Dienst über einen Datensatz **Abschnitte** verfügen. 
  
Führen Sie die beiden Beispiele für Nachricht Service Abschnitte. Der erste Abschnitt ist für den Standard-Adressbuch-Dienst aus der früheren Abbildung eine einfache Message Service mit einem einzelnen Dienstanbieter. Im zweite Abschnitt ist für den MsgService-Dienst ein komplexeres Beispiel Messagingdiensts mit drei-Dienstanbieter. 
  
```cpp
[AB]
PR_DISPLAY_NAME=Default Address Book
Providers=AB Provider
PR_SERVICE_DLL_NAME=AB.DLL
PR_SERVICE_SUPPORT_FILES=AB.DLL
PR_SERVICE_ENTRY_NAME=DABServiceEntry
PR_RESOURCE_FLAGS=SERVICE_NO_PRIMARY_IDENTITY
[MsgService]
PR_DISPLAY_NAME=My Own Service
Providers=MsgService Prov1, MsgService Prov2, MsgService Prov3
Sections=First_Special_Section, Second_Special_Section
PR_SERVICE_DLL_NAME=MYSERV.DLL
PR_SERVICE_SUPPORT_FILES=MYSERV.DLL, MYXXX.DLL, MYZZZ.DLL
PR_SERVICE_ENTRY_NAME=MyServiceEntry
PR_RESOURCE_FLAGS=SERVICE_SINGLE_COPY
66040003=00000000

```

Der **Abschnitte** Eintrag im Abschnitt **[MsgService]** listet zwei zusätzliche Abschnitte, eine gewählte **[First_Special_Section]** und weitere mit der Bezeichnung **[Second_Special_Section]**. Die Daten, die sich in zusätzlichen Abschnitten anscheinend ist sinnvoll, mit dem Dienst bestimmte Nachricht. In diesen Abschnitten werden folgende zusätzliche Abschnitte erläutern. 
  
```cpp
[First_Special_Section]
UID=13DB0C8AA05101A9BB000AA002FC45A
66020003=01000000
66000003=00040000
66010003=06000000
66050003=03000000

```


