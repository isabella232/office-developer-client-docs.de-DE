---
title: MapiSvc.inf [Default Services] Section
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: dec42f8d-0f5c-4665-b53a-11cbc58b8b76
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: a7906a9a5e953332dba5c4776c63bb433a937a5d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435320"
---
# <a name="mapisvcinf-default-services-section"></a><span data-ttu-id="3d186-103">MapiSvc.inf [Default Services] Section</span><span class="sxs-lookup"><span data-stu-id="3d186-103">MapiSvc.inf [Default Services] Section</span></span>

  
  
<span data-ttu-id="3d186-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3d186-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3d186-105">Im **Abschnitt [Standarddienste]** werden alle Nachrichtendienste aufgeführt, die als Standardnachrichtendienste ausgewählt sind.</span><span class="sxs-lookup"><span data-stu-id="3d186-105">The **[Default Services]** section lists all of the message services that are selected as default message services.</span></span> <span data-ttu-id="3d186-106">Diese Standardnachrichtendienste sind eine Teilmenge der Nachrichtendienste, die im **Abschnitt [Dienste] aufgeführt** sind.</span><span class="sxs-lookup"><span data-stu-id="3d186-106">These default message services are a subset of the message services listed in the **[Services]** section.</span></span> <span data-ttu-id="3d186-107">Wenn ein Profilkonfigurationsprogramm ein Standardprofil erstellt, werden die Nachrichtendienste in diesem Abschnitt automatisch einbezogen.</span><span class="sxs-lookup"><span data-stu-id="3d186-107">When a profile configuration program creates a default profile, the message services in this section are automatically included.</span></span> 
  
<span data-ttu-id="3d186-108">Die Einträge verwenden das gleiche Format wie Einträge im **Abschnitt [Dienste],** wie im Folgenden dargestellt:</span><span class="sxs-lookup"><span data-stu-id="3d186-108">The entries use the same format as entries in the **[Services]** section, as shown following:</span></span> 
  
 <span data-ttu-id="3d186-109">**[Standarddienste]**</span><span class="sxs-lookup"><span data-stu-id="3d186-109">**[Default Services]**</span></span>
  
 <span data-ttu-id="3d186-110">_Name des Message-Service-Abschnitts_  =   _Name des Nachrichtendiensts_</span><span class="sxs-lookup"><span data-stu-id="3d186-110">_message-service section name_ =  _message service name_</span></span>
  
<span data-ttu-id="3d186-111">Die folgenden Einträge würden im **Abschnitt [Standarddienste]** für mapisvc.inf in der früheren Abbildung enthalten sein:</span><span class="sxs-lookup"><span data-stu-id="3d186-111">The following entries would be included in the **[Default Services]** section for the mapisvc.inf shown in the earlier illustration:</span></span> 
  
```cpp
[Default Services]
AB=Default Address Book
MsgService=My Own Service

```


