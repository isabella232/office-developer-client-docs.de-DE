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
ms.openlocfilehash: e59c0ba7810741943883b9e86e84c6fe141f3050
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791707"
---
# <a name="followupstatus"></a><span data-ttu-id="34e26-103">FollowUpStatus</span><span class="sxs-lookup"><span data-stu-id="34e26-103">FollowUpStatus</span></span>

  
  
<span data-ttu-id="34e26-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="34e26-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="34e26-105">Gibt die verschiedenen weiteren Statusarten für eine Nachricht an.</span><span class="sxs-lookup"><span data-stu-id="34e26-105">Specifies the different follow-up statuses for a message.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="34e26-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="34e26-106">Quick info</span></span>

```cpp
enum FollowUpStatus { 
    flwupNone = 0, 
    flwupComplete, 
    flwupMarked, 
    flwupMAX}; 

```

## <a name="members"></a><span data-ttu-id="34e26-107">Elemente</span><span class="sxs-lookup"><span data-stu-id="34e26-107">Members</span></span>

 <span data-ttu-id="34e26-108">_flwupNone_</span><span class="sxs-lookup"><span data-stu-id="34e26-108">_flwupNone_</span></span>
  
> <span data-ttu-id="34e26-109">Keine Nachsorge es wurde angegeben.</span><span class="sxs-lookup"><span data-stu-id="34e26-109">No follow-up has been specified.</span></span>
    
 <span data-ttu-id="34e26-110">_flwupComplete_</span><span class="sxs-lookup"><span data-stu-id="34e26-110">_flwupComplete_</span></span>
  
> <span data-ttu-id="34e26-111">Die Nachricht ist abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="34e26-111">The message is complete.</span></span>
    
 <span data-ttu-id="34e26-112">_flwupMarked_</span><span class="sxs-lookup"><span data-stu-id="34e26-112">_flwupMarked_</span></span>
  
> <span data-ttu-id="34e26-113">Die Nachricht ist für die nachverfolgung gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="34e26-113">The message is marked for follow-up.</span></span>
    
 <span data-ttu-id="34e26-114">_flwupMAX_</span><span class="sxs-lookup"><span data-stu-id="34e26-114">_flwupMAX_</span></span>
  
> <span data-ttu-id="34e26-115">Die Anzahl der verschiedenen Statusarten für Nachsorge unterstützt.</span><span class="sxs-lookup"><span data-stu-id="34e26-115">The number of different statuses supported for follow-up.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="34e26-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="34e26-116">See also</span></span>



[<span data-ttu-id="34e26-117">PidTagFlagStatus (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="34e26-117">PidTagFlagStatus Canonical Property</span></span>](pidtagflagstatus-canonical-property.md)

