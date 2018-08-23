---
title: Abschnitt [Default Services] in MapiSvc.inf
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: dec42f8d-0f5c-4665-b53a-11cbc58b8b76
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: a7270bce12f6d91dbb5632f739f4644df866924d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573145"
---
# <a name="mapisvcinf-default-services-section"></a><span data-ttu-id="f8681-103">Abschnitt [Default Services] in MapiSvc.inf</span><span class="sxs-lookup"><span data-stu-id="f8681-103">MapiSvc.inf [Default Services] Section</span></span>

  
  
<span data-ttu-id="f8681-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f8681-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f8681-105">Der Abschnitt **[Default Services]** enthält eine Liste aller Message-Dienste, die als Standard-Nachrichtendienste ausgewählt sind.</span><span class="sxs-lookup"><span data-stu-id="f8681-105">The **[Default Services]** section lists all of the message services that are selected as default message services.</span></span> <span data-ttu-id="f8681-106">Diese Standard-Message-Dienste sind eine Teilmenge der Nachricht Dienstleistungen im Abschnitt **[Services]** .</span><span class="sxs-lookup"><span data-stu-id="f8681-106">These default message services are a subset of the message services listed in the **[Services]** section.</span></span> <span data-ttu-id="f8681-107">Wenn ein Profil Konfigurationsprogramm ein Standardprofil erstellt werden, sind die Message-Dienste in diesem Abschnitt automatisch enthalten.</span><span class="sxs-lookup"><span data-stu-id="f8681-107">When a profile configuration program creates a default profile, the message services in this section are automatically included.</span></span> 
  
<span data-ttu-id="f8681-108">Die Einträge verwenden das gleiche Format als Einträge im Abschnitt **[Services]** wie folgt dargestellt:</span><span class="sxs-lookup"><span data-stu-id="f8681-108">The entries use the same format as entries in the **[Services]** section, as shown following:</span></span> 
  
 <span data-ttu-id="f8681-109">**[Default Services]**</span><span class="sxs-lookup"><span data-stu-id="f8681-109">**[Default Services]**</span></span>
  
 <span data-ttu-id="f8681-110">_Message-Dienst im Abschnittsname_ =  _Dienstname Nachricht_</span><span class="sxs-lookup"><span data-stu-id="f8681-110">_message-service section name_ =  _message service name_</span></span>
  
<span data-ttu-id="f8681-111">Die folgenden Einträge wären im Abschnitt **[Services Default]** für die in der vorherigen Abbildung gezeigten mapisvc.inf enthalten:</span><span class="sxs-lookup"><span data-stu-id="f8681-111">The following entries would be included in the **[Default Services]** section for the mapisvc.inf shown in the earlier illustration:</span></span> 
  
```cpp
[Default Services]
AB=Default Address Book
MsgService=My Own Service

```


