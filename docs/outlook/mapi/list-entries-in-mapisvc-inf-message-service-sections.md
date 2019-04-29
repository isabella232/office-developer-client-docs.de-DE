---
title: Listeneinträge in den Nachrichtendienst Abschnitten von MapiSvc. inf
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f4f052d6-ef63-421a-9d8c-4f3c6df83863
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: b6b641a288cea8bac5a1990e85520f3583c02f22
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435929"
---
# <a name="list-entries-in-mapisvcinf-message-service-sections"></a>Listeneinträge in den Nachrichtendienst Abschnitten von MapiSvc. inf

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Es gibt zwei Arten von Abschnittslisten Einträgen: eine, die Dienstanbieter Abschnitte auflistet, und eine, die verschiedene Nachrichtendienst spezifische Abschnitte auflistet. Diese beiden Arten von Einträgen werden in MAPISVC. inf in den folgenden Formaten angezeigt:
  
```cpp
Providersprovider section1, provider section2, ...... provider sectionX
Sectionssection name1, section name2, ......section nameX

```

Jeder Abschnitt im **Anbieter** Eintrag wird einem einzelnen Abschnitt zugeordnet, der Konfigurationsinformationen für einen Dienstanbieter bereitstellt, der zum Nachrichtendienst gehört. Jeder Abschnitt des Abschnitts **** Eintrags wird einem Abschnitt zugeordnet, der zusätzliche Konfigurationsinformationen enthält, die vom Nachrichtendienst benötigt werden. Nachrichtendienst Implementierer definieren zusätzliche Abschnitte, wenn Sie spezielle Informationen enthalten möchten, die nicht in die Standardabschnitte passt. Nachrichtendienste mit komplizierten Konfigurationen verwenden in der Regel den Eintrag **Abschnitte** , um zusätzliche Informationen hinzuzufügen. Jeder Abschnitt für Nachrichtendienste hat einen **Anbieter** Eintrag mit mindestens einem Abschnitt in der Liste; nicht alle Nachrichtendienst Abschnitte weisen einen **Abschnitt** -Eintrag auf. 
  
Es folgen zwei Beispiele für Nachrichtendienst Abschnitte. Der erste Abschnitt ist für den standardmäßigen Adressbuchdienst aus der früheren Abbildung, einen einfachen Nachrichtendienst mit einem einzelnen Dienstanbieter. Der zweite Abschnitt richtet sich an den MsgService-Dienst, einen komplexeren Beispiel Nachrichtendienst mit drei Dienstanbietern. 
  
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

Der **** Eintrag Sections im Abschnitt **[MsgService]** listet zwei zusätzliche Abschnitte auf, eine mit dem Namen **[First_Special_Section]** und die andere als **[Second_Special_Section]**. Die Daten, die in zusätzlichen Abschnitten angezeigt werden können, sind für den jeweiligen Nachrichtendienst sinnvoll. In den folgenden Abschnitten werden weitere Abschnitte veranschaulicht. 
  
```cpp
[First_Special_Section]
UID=13DB0C8AA05101A9BB000AA002FC45A
66020003=01000000
66000003=00040000
66010003=06000000
66050003=03000000

```


