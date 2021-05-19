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
ms.openlocfilehash: 2280ae9271ca73af33f395bf9e41a9ee8fa62f96
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418330"
---
# <a name="followupstatus"></a><span data-ttu-id="1b735-103">FollowUpStatus</span><span class="sxs-lookup"><span data-stu-id="1b735-103">FollowUpStatus</span></span>

  
  
<span data-ttu-id="1b735-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1b735-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1b735-105">Gibt die unterschiedlichen Follow-up-Status für eine Nachricht an.</span><span class="sxs-lookup"><span data-stu-id="1b735-105">Specifies the different follow-up statuses for a message.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="1b735-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="1b735-106">Quick info</span></span>

```cpp
enum FollowUpStatus { 
    flwupNone = 0, 
    flwupComplete, 
    flwupMarked, 
    flwupMAX}; 

```

## <a name="members"></a><span data-ttu-id="1b735-107">Elemente</span><span class="sxs-lookup"><span data-stu-id="1b735-107">Members</span></span>

 <span data-ttu-id="1b735-108">_flwupNone_</span><span class="sxs-lookup"><span data-stu-id="1b735-108">_flwupNone_</span></span>
  
> <span data-ttu-id="1b735-109">Es wurde keine Nachgeh-nung angegeben.</span><span class="sxs-lookup"><span data-stu-id="1b735-109">No follow-up has been specified.</span></span>
    
 <span data-ttu-id="1b735-110">_flwupComplete_</span><span class="sxs-lookup"><span data-stu-id="1b735-110">_flwupComplete_</span></span>
  
> <span data-ttu-id="1b735-111">Die Nachricht ist abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="1b735-111">The message is complete.</span></span>
    
 <span data-ttu-id="1b735-112">_flwupMarked_</span><span class="sxs-lookup"><span data-stu-id="1b735-112">_flwupMarked_</span></span>
  
> <span data-ttu-id="1b735-113">Die Nachricht wird für die Nach-Nach-nach-Oben-Nachricht markiert.</span><span class="sxs-lookup"><span data-stu-id="1b735-113">The message is marked for follow-up.</span></span>
    
 <span data-ttu-id="1b735-114">_flwupMAX_</span><span class="sxs-lookup"><span data-stu-id="1b735-114">_flwupMAX_</span></span>
  
> <span data-ttu-id="1b735-115">Die Anzahl der verschiedenen Status, die für die Nach-nach-Oben-Schritte unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="1b735-115">The number of different statuses supported for follow-up.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1b735-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1b735-116">See also</span></span>



[<span data-ttu-id="1b735-117">PidTagFlagStatus (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="1b735-117">PidTagFlagStatus Canonical Property</span></span>](pidtagflagstatus-canonical-property.md)

