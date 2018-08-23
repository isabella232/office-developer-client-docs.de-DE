---
title: FollowUpStatus
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c3d0f6c4-4597-784f-8d44-6e5d905895b4
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 6b57ed45e067ce2debd40e033d386ad2b5ae895a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568518"
---
# <a name="followupstatus"></a><span data-ttu-id="abfc5-103">FollowUpStatus</span><span class="sxs-lookup"><span data-stu-id="abfc5-103">FollowUpStatus</span></span>

  
  
<span data-ttu-id="abfc5-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="abfc5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="abfc5-105">Gibt die verschiedenen weiteren Statusarten für eine Nachricht an.</span><span class="sxs-lookup"><span data-stu-id="abfc5-105">Specifies the different follow-up statuses for a message.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="abfc5-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="abfc5-106">Quick info</span></span>

```cpp
enum FollowUpStatus { 
    flwupNone = 0, 
    flwupComplete, 
    flwupMarked, 
    flwupMAX}; 

```

## <a name="members"></a><span data-ttu-id="abfc5-107">Elemente</span><span class="sxs-lookup"><span data-stu-id="abfc5-107">Members</span></span>

 <span data-ttu-id="abfc5-108">_flwupNone_</span><span class="sxs-lookup"><span data-stu-id="abfc5-108">_flwupNone_</span></span>
  
> <span data-ttu-id="abfc5-109">Keine Nachsorge es wurde angegeben.</span><span class="sxs-lookup"><span data-stu-id="abfc5-109">No follow-up has been specified.</span></span>
    
 <span data-ttu-id="abfc5-110">_flwupComplete_</span><span class="sxs-lookup"><span data-stu-id="abfc5-110">_flwupComplete_</span></span>
  
> <span data-ttu-id="abfc5-111">Die Nachricht ist abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="abfc5-111">The message is complete.</span></span>
    
 <span data-ttu-id="abfc5-112">_flwupMarked_</span><span class="sxs-lookup"><span data-stu-id="abfc5-112">_flwupMarked_</span></span>
  
> <span data-ttu-id="abfc5-113">Die Nachricht ist für die nachverfolgung gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="abfc5-113">The message is marked for follow-up.</span></span>
    
 <span data-ttu-id="abfc5-114">_flwupMAX_</span><span class="sxs-lookup"><span data-stu-id="abfc5-114">_flwupMAX_</span></span>
  
> <span data-ttu-id="abfc5-115">Die Anzahl der verschiedenen Statusarten für Nachsorge unterstützt.</span><span class="sxs-lookup"><span data-stu-id="abfc5-115">The number of different statuses supported for follow-up.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="abfc5-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="abfc5-116">See also</span></span>



[<span data-ttu-id="abfc5-117">PidTagFlagStatus (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="abfc5-117">PidTagFlagStatus Canonical Property</span></span>](pidtagflagstatus-canonical-property.md)

