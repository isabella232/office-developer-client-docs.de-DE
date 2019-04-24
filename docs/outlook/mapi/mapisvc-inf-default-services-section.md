---
title: Abschnitt "MapiSvc. inf [Standarddienste]"
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: dec42f8d-0f5c-4665-b53a-11cbc58b8b76
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: a7906a9a5e953332dba5c4776c63bb433a937a5d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32270070"
---
# <a name="mapisvcinf-default-services-section"></a><span data-ttu-id="6137f-103">Abschnitt "MapiSvc. inf [Standarddienste]"</span><span class="sxs-lookup"><span data-stu-id="6137f-103">MapiSvc.inf [Default Services] Section</span></span>

  
  
<span data-ttu-id="6137f-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6137f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6137f-105">Im Abschnitt **[Default Services]** werden alle Nachrichtendienste aufgelistet, die als Standardnachrichten Dienste ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="6137f-105">The **[Default Services]** section lists all of the message services that are selected as default message services.</span></span> <span data-ttu-id="6137f-106">Diese Standardnachrichten Dienste sind eine Teilmenge der Nachrichtendienste, die im Abschnitt **[Dienste]** aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="6137f-106">These default message services are a subset of the message services listed in the **[Services]** section.</span></span> <span data-ttu-id="6137f-107">Wenn ein Profil Konfigurationsprogramm ein Standardprofil erstellt, werden die Nachrichtendienste in diesem Abschnitt automatisch eingeschlossen.</span><span class="sxs-lookup"><span data-stu-id="6137f-107">When a profile configuration program creates a default profile, the message services in this section are automatically included.</span></span> 
  
<span data-ttu-id="6137f-108">Die Einträge verwenden dasselbe Format wie Einträge im Abschnitt **[Dienste]** , wie nachfolgend gezeigt:</span><span class="sxs-lookup"><span data-stu-id="6137f-108">The entries use the same format as entries in the **[Services]** section, as shown following:</span></span> 
  
 <span data-ttu-id="6137f-109">**[Standarddienste]**</span><span class="sxs-lookup"><span data-stu-id="6137f-109">**[Default Services]**</span></span>
  
 <span data-ttu-id="6137f-110">_Message-Service section Name_ =  _Message Service Name_</span><span class="sxs-lookup"><span data-stu-id="6137f-110">_message-service section name_ =  _message service name_</span></span>
  
<span data-ttu-id="6137f-111">Die folgenden Einträge würden im Abschnitt **[Default Services]** für die in der vorherigen Abbildung gezeigte MAPISVC. inf enthalten sein:</span><span class="sxs-lookup"><span data-stu-id="6137f-111">The following entries would be included in the **[Default Services]** section for the mapisvc.inf shown in the earlier illustration:</span></span> 
  
```cpp
[Default Services]
AB=Default Address Book
MsgService=My Own Service

```


