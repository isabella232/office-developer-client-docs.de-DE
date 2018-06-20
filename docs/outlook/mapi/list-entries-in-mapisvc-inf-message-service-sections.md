---
title: Die Einträge aus MapiSvc.inf Nachricht Service Abschnitte
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f4f052d6-ef63-421a-9d8c-4f3c6df83863
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: cfb06e8dd305add6049d035c44685be047dc744f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792894"
---
# <a name="list-entries-in-mapisvcinf-message-service-sections"></a><span data-ttu-id="74209-103">Die Einträge aus MapiSvc.inf Nachricht Service Abschnitte</span><span class="sxs-lookup"><span data-stu-id="74209-103">List Entries in MapiSvc.inf Message Service Sections</span></span>

  
  
<span data-ttu-id="74209-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="74209-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="74209-105">Es gibt zwei Arten der Abschnitt Listeneinträge: eine, die auflistet Service Provider Abschnitte und eine, die verschiedene Nachricht dienstspezifische Abschnitte auflistet.</span><span class="sxs-lookup"><span data-stu-id="74209-105">There are two types of section list entries: one that lists service provider sections and one that lists miscellaneous message service-specific sections.</span></span> <span data-ttu-id="74209-106">Diese zwei Arten von Einträgen in mapisvc.inf über die folgenden Formate angezeigt:</span><span class="sxs-lookup"><span data-stu-id="74209-106">These two types of entries appear in mapisvc.inf using the following formats:</span></span>
  
```cpp
Providersprovider section1, provider section2, ...... provider sectionX
Sectionssection name1, section name2, ......section nameX

```

<span data-ttu-id="74209-107">Alle Abschnitte in der **Anbieter** -Eintrag ordnet einen einzelnen Bereich Bereitstellen von Konfigurationsinformationen für einen-Dienstanbieter, der den Dienst gehört.</span><span class="sxs-lookup"><span data-stu-id="74209-107">Each section in the **Providers** entry maps to an individual section providing configuration information for a service provider that belongs to the message service.</span></span> <span data-ttu-id="74209-108">Jeder Abschnitt in den **Abschnitten** Eintrag ordnet einen Abschnitt, der zusätzliche Konfigurationsinformationen enthält, die den Dienst benötigt.</span><span class="sxs-lookup"><span data-stu-id="74209-108">Each section in the **Sections** entry maps to a section that contains extra configuration information needed by the message service.</span></span> <span data-ttu-id="74209-109">Nachricht Service Implementierer definieren Sie zusätzliche Abschnitte Wenn werden spezielle Informationen enthalten, die nicht in den Abschnitten standard passt sollen.</span><span class="sxs-lookup"><span data-stu-id="74209-109">Message service implementers define extra sections when they want to include special information that does not fit in the standard sections.</span></span> <span data-ttu-id="74209-110">Message-Dienste, die in der Regel Konfigurationen kompliziert haben verwenden den Eintrag **Abschnitte** , um zusätzliche Informationen hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="74209-110">Message services that have complicated configurations typically use the **Sections** entry to add extra information.</span></span> <span data-ttu-id="74209-111">Jede Nachricht Dienste im Abschnitt hat einen **Anbieter** -Eintrag mit mindestens einem Bereich in der Liste. nicht alle Abschnitte der Nachricht-Dienst über einen Datensatz **Abschnitte** verfügen.</span><span class="sxs-lookup"><span data-stu-id="74209-111">Every message services section has a **Providers** entry with at least one section in the list; not all message service sections have a **Sections** entry.</span></span> 
  
<span data-ttu-id="74209-112">Führen Sie die beiden Beispiele für Nachricht Service Abschnitte.</span><span class="sxs-lookup"><span data-stu-id="74209-112">Two examples of message service sections follow.</span></span> <span data-ttu-id="74209-113">Der erste Abschnitt ist für den Standard-Adressbuch-Dienst aus der früheren Abbildung eine einfache Message Service mit einem einzelnen Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="74209-113">The first section is for the Default Address Book service from the earlier illustration, a straightforward message service with a single service provider.</span></span> <span data-ttu-id="74209-114">Im zweite Abschnitt ist für den MsgService-Dienst ein komplexeres Beispiel Messagingdiensts mit drei-Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="74209-114">The second section is for the MsgService service, a more complex sample message service with three service providers.</span></span> 
  
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

<span data-ttu-id="74209-115">Der **Abschnitte** Eintrag im Abschnitt **[MsgService]** listet zwei zusätzliche Abschnitte, eine gewählte **[First_Special_Section]** und weitere mit der Bezeichnung **[Second_Special_Section]**.</span><span class="sxs-lookup"><span data-stu-id="74209-115">The **Sections** entry in the **[MsgService]** section lists two additional sections, one called **[First_Special_Section]** and the other called **[Second_Special_Section]**.</span></span> <span data-ttu-id="74209-116">Die Daten, die sich in zusätzlichen Abschnitten anscheinend ist sinnvoll, mit dem Dienst bestimmte Nachricht.</span><span class="sxs-lookup"><span data-stu-id="74209-116">The data that might appear in extra sections is meaningful to the specific message service.</span></span> <span data-ttu-id="74209-117">In diesen Abschnitten werden folgende zusätzliche Abschnitte erläutern.</span><span class="sxs-lookup"><span data-stu-id="74209-117">These sections appear following to illustrate extra sections.</span></span> 
  
```cpp
[First_Special_Section]
UID=13DB0C8AA05101A9BB000AA002FC45A
66020003=01000000
66000003=00040000
66010003=06000000
66050003=03000000

```


