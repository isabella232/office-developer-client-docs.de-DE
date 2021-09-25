---
title: Listeneinträge in MapiSvc.inf-Nachrichtendienstabschnitten
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: f4f052d6-ef63-421a-9d8c-4f3c6df83863
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 8c2fe2dfbe3783f60f48a0d36fd5bef139f7347b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59571528"
---
# <a name="list-entries-in-mapisvcinf-message-service-sections"></a>Listeneinträge in MapiSvc.inf-Nachrichtendienstabschnitten

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Es gibt zwei Arten von Abschnittslisteneinträgen: einen, der Dienstanbieterabschnitte auflistet, und einen, der verschiedene nachrichtendienstspezifische Abschnitte auflistet. Diese beiden Arten von Einträgen werden in mapisvc.inf in den folgenden Formaten angezeigt:
  
```cpp
Providersprovider section1, provider section2, ...... provider sectionX
Sectionssection name1, section name2, ......section nameX

```

Jeder Abschnitt im **Anbietereintrag** ist einem einzelnen Abschnitt zugeordnet, der Konfigurationsinformationen für einen Dienstanbieter bereitstellt, der zum Nachrichtendienst gehört. Jeder Abschnitt im **Abschnittseintrag** wird einem Abschnitt zugeordnet, der zusätzliche Konfigurationsinformationen enthält, die vom Nachrichtendienst benötigt werden. Nachrichtendienst-Implementierer definieren zusätzliche Abschnitte, wenn sie spezielle Informationen enthalten möchten, die nicht in die Standardabschnitte passen. Nachrichtendienste mit komplizierten Konfigurationen verwenden in der Regel den **Abschnittseintrag,** um zusätzliche Informationen hinzuzufügen. Jeder Nachrichtendienstabschnitt verfügt über einen **Anbietereintrag** mit mindestens einem Abschnitt in der Liste. Nicht alle Nachrichtendienstabschnitte verfügen über einen **Abschnittseintrag.** 
  
Es folgen zwei Beispiele für Nachrichtendienstabschnitte. Der erste Abschnitt behebt den Standardadressbuchdienst aus der vorherigen Abbildung, einen einfachen Nachrichtendienst mit einem einzigen Dienstanbieter. Der zweite Abschnitt ist für den MsgService-Dienst, einen komplexeren Beispielnachrichtendienst mit drei Dienstanbietern. 
  
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

Der **Abschnittseintrag** im **Abschnitt [MsgService]** listet zwei zusätzliche Abschnitte auf, einen mit dem Namen **[First_Special_Section]** und den anderen mit dem Namen **[Second_Special_Section]**. Die Daten, die in zusätzlichen Abschnitten angezeigt werden können, sind für den jeweiligen Nachrichtendienst von Bedeutung. Diese Abschnitte werden im Folgenden angezeigt, um zusätzliche Abschnitte zu veranschaulichen. 
  
```cpp
[First_Special_Section]
UID=13DB0C8AA05101A9BB000AA002FC45A
66020003=01000000
66000003=00040000
66010003=06000000
66050003=03000000

```


