---
title: attMessageStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8f55470a-65b3-4210-a7d2-9031cb17ca80
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 158e4db4b0f80b80385e85c8afa16fa515dc61b1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791344"
---
# <a name="attmessagestatus"></a><span data-ttu-id="b703b-103">attMessageStatus</span><span class="sxs-lookup"><span data-stu-id="b703b-103">attMessageStatus</span></span>

  
  
<span data-ttu-id="b703b-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b703b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b703b-105">TNEF-Flags Abwärtskompatibilität beibehalten werden MAPI Nachrichtenflags zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="b703b-105">MAPI message flags are mapped to TNEF flags to preserve backward compatibility.</span></span> <span data-ttu-id="b703b-106">Alle Flags werden zusammengefasst und in ein einzelnes Byte codiert.</span><span class="sxs-lookup"><span data-stu-id="b703b-106">All the flags are grouped together and encoded in a single byte.</span></span> <span data-ttu-id="b703b-107">Die Zuordnungen lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="b703b-107">The mappings are as follows:</span></span>
  
|<span data-ttu-id="b703b-108">**MAPI-Nachrichtenflags**</span><span class="sxs-lookup"><span data-stu-id="b703b-108">**MAPI message flags**</span></span>|<span data-ttu-id="b703b-109">**TNEF-Kennzeichen**</span><span class="sxs-lookup"><span data-stu-id="b703b-109">**TNEF flags**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b703b-110">MSGFLAG_READ</span><span class="sxs-lookup"><span data-stu-id="b703b-110">MSGFLAG_READ</span></span>  <br/> |<span data-ttu-id="b703b-111">fmsRead</span><span class="sxs-lookup"><span data-stu-id="b703b-111">fmsRead</span></span>  <br/> |
|<span data-ttu-id="b703b-112">MSGFLAG_UNMODIFED</span><span class="sxs-lookup"><span data-stu-id="b703b-112">MSGFLAG_UNMODIFED</span></span>  <br/> |<span data-ttu-id="b703b-113">~ FmsModified</span><span class="sxs-lookup"><span data-stu-id="b703b-113">~fmsModified</span></span>  <br/> |
|<span data-ttu-id="b703b-114">MSGFLAG_SUBMIT</span><span class="sxs-lookup"><span data-stu-id="b703b-114">MSGFLAG_SUBMIT</span></span>  <br/> |<span data-ttu-id="b703b-115">fmsSubmitted</span><span class="sxs-lookup"><span data-stu-id="b703b-115">fmsSubmitted</span></span>  <br/> |
|<span data-ttu-id="b703b-116">MSGFLAG_HASATTACH</span><span class="sxs-lookup"><span data-stu-id="b703b-116">MSGFLAG_HASATTACH</span></span>  <br/> |<span data-ttu-id="b703b-117">fmsHasAttach</span><span class="sxs-lookup"><span data-stu-id="b703b-117">fmsHasAttach</span></span>  <br/> |
|<span data-ttu-id="b703b-118">MSGFLAG_UNSENT</span><span class="sxs-lookup"><span data-stu-id="b703b-118">MSGFLAG_UNSENT</span></span>  <br/> |<span data-ttu-id="b703b-119">fmsLocal</span><span class="sxs-lookup"><span data-stu-id="b703b-119">fmsLocal</span></span>  <br/> |
   
<span data-ttu-id="b703b-120">Diese Flags werden in die TNEF definiert. H-Headerdatei.</span><span class="sxs-lookup"><span data-stu-id="b703b-120">These flags are defined in the TNEF.H header file.</span></span>
  

