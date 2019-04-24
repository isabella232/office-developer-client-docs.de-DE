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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307833"
---
# <a name="list-entries-in-mapisvcinf-message-service-sections"></a><span data-ttu-id="89256-103">Listeneinträge in den Nachrichtendienst Abschnitten von MapiSvc. inf</span><span class="sxs-lookup"><span data-stu-id="89256-103">List Entries in MapiSvc.inf Message Service Sections</span></span>

  
  
<span data-ttu-id="89256-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="89256-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="89256-105">Es gibt zwei Arten von Abschnittslisten Einträgen: eine, die Dienstanbieter Abschnitte auflistet, und eine, die verschiedene Nachrichtendienst spezifische Abschnitte auflistet.</span><span class="sxs-lookup"><span data-stu-id="89256-105">There are two types of section list entries: one that lists service provider sections and one that lists miscellaneous message service-specific sections.</span></span> <span data-ttu-id="89256-106">Diese beiden Arten von Einträgen werden in MAPISVC. inf in den folgenden Formaten angezeigt:</span><span class="sxs-lookup"><span data-stu-id="89256-106">These two types of entries appear in mapisvc.inf using the following formats:</span></span>
  
```cpp
Providersprovider section1, provider section2, ...... provider sectionX
Sectionssection name1, section name2, ......section nameX

```

<span data-ttu-id="89256-107">Jeder Abschnitt im **Anbieter** Eintrag wird einem einzelnen Abschnitt zugeordnet, der Konfigurationsinformationen für einen Dienstanbieter bereitstellt, der zum Nachrichtendienst gehört.</span><span class="sxs-lookup"><span data-stu-id="89256-107">Each section in the **Providers** entry maps to an individual section providing configuration information for a service provider that belongs to the message service.</span></span> <span data-ttu-id="89256-108">Jeder Abschnitt des Abschnitts \*\*\*\* Eintrags wird einem Abschnitt zugeordnet, der zusätzliche Konfigurationsinformationen enthält, die vom Nachrichtendienst benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="89256-108">Each section in the **Sections** entry maps to a section that contains extra configuration information needed by the message service.</span></span> <span data-ttu-id="89256-109">Nachrichtendienst Implementierer definieren zusätzliche Abschnitte, wenn Sie spezielle Informationen enthalten möchten, die nicht in die Standardabschnitte passt.</span><span class="sxs-lookup"><span data-stu-id="89256-109">Message service implementers define extra sections when they want to include special information that does not fit in the standard sections.</span></span> <span data-ttu-id="89256-110">Nachrichtendienste mit komplizierten Konfigurationen verwenden in der Regel den Eintrag **Abschnitte** , um zusätzliche Informationen hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="89256-110">Message services that have complicated configurations typically use the **Sections** entry to add extra information.</span></span> <span data-ttu-id="89256-111">Jeder Abschnitt für Nachrichtendienste hat einen **Anbieter** Eintrag mit mindestens einem Abschnitt in der Liste; nicht alle Nachrichtendienst Abschnitte weisen einen **Abschnitt** -Eintrag auf.</span><span class="sxs-lookup"><span data-stu-id="89256-111">Every message services section has a **Providers** entry with at least one section in the list; not all message service sections have a **Sections** entry.</span></span> 
  
<span data-ttu-id="89256-112">Es folgen zwei Beispiele für Nachrichtendienst Abschnitte.</span><span class="sxs-lookup"><span data-stu-id="89256-112">Two examples of message service sections follow.</span></span> <span data-ttu-id="89256-113">Der erste Abschnitt ist für den standardmäßigen Adressbuchdienst aus der früheren Abbildung, einen einfachen Nachrichtendienst mit einem einzelnen Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="89256-113">The first section is for the Default Address Book service from the earlier illustration, a straightforward message service with a single service provider.</span></span> <span data-ttu-id="89256-114">Der zweite Abschnitt richtet sich an den MsgService-Dienst, einen komplexeren Beispiel Nachrichtendienst mit drei Dienstanbietern.</span><span class="sxs-lookup"><span data-stu-id="89256-114">The second section is for the MsgService service, a more complex sample message service with three service providers.</span></span> 
  
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

<span data-ttu-id="89256-115">Der \*\*\*\* Eintrag Sections im Abschnitt **[MsgService]** listet zwei zusätzliche Abschnitte auf, eine mit dem Namen **[First_Special_Section]** und die andere als **[Second_Special_Section]**.</span><span class="sxs-lookup"><span data-stu-id="89256-115">The **Sections** entry in the **[MsgService]** section lists two additional sections, one called **[First_Special_Section]** and the other called **[Second_Special_Section]**.</span></span> <span data-ttu-id="89256-116">Die Daten, die in zusätzlichen Abschnitten angezeigt werden können, sind für den jeweiligen Nachrichtendienst sinnvoll.</span><span class="sxs-lookup"><span data-stu-id="89256-116">The data that might appear in extra sections is meaningful to the specific message service.</span></span> <span data-ttu-id="89256-117">In den folgenden Abschnitten werden weitere Abschnitte veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="89256-117">These sections appear following to illustrate extra sections.</span></span> 
  
```cpp
[First_Special_Section]
UID=13DB0C8AA05101A9BB000AA002FC45A
66020003=01000000
66000003=00040000
66010003=06000000
66050003=03000000

```


