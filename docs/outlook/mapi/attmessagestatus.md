---
title: attMessageStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8f55470a-65b3-4210-a7d2-9031cb17ca80
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 158e4db4b0f80b80385e85c8afa16fa515dc61b1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791344"
---
# <a name="attmessagestatus"></a><span data-ttu-id="3e4c3-103">attMessageStatus</span><span class="sxs-lookup"><span data-stu-id="3e4c3-103">attMessageStatus</span></span>

  
  
<span data-ttu-id="3e4c3-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3e4c3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3e4c3-105">TNEF-Flags Abwärtskompatibilität beibehalten werden MAPI Nachrichtenflags zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="3e4c3-105">MAPI message flags are mapped to TNEF flags to preserve backward compatibility.</span></span> <span data-ttu-id="3e4c3-106">Alle Flags werden zusammengefasst und in ein einzelnes Byte codiert.</span><span class="sxs-lookup"><span data-stu-id="3e4c3-106">All the flags are grouped together and encoded in a single byte.</span></span> <span data-ttu-id="3e4c3-107">Die Zuordnungen lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="3e4c3-107">The mappings are as follows:</span></span>
  
|<span data-ttu-id="3e4c3-108">**MAPI-Nachrichtenflags**</span><span class="sxs-lookup"><span data-stu-id="3e4c3-108">**MAPI message flags**</span></span>|<span data-ttu-id="3e4c3-109">**TNEF-Kennzeichen**</span><span class="sxs-lookup"><span data-stu-id="3e4c3-109">**TNEF flags**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3e4c3-110">MSGFLAG_READ</span><span class="sxs-lookup"><span data-stu-id="3e4c3-110">MSGFLAG_READ</span></span>  <br/> |<span data-ttu-id="3e4c3-111">fmsRead</span><span class="sxs-lookup"><span data-stu-id="3e4c3-111">fmsRead</span></span>  <br/> |
|<span data-ttu-id="3e4c3-112">MSGFLAG_UNMODIFED</span><span class="sxs-lookup"><span data-stu-id="3e4c3-112">MSGFLAG_UNMODIFED</span></span>  <br/> |<span data-ttu-id="3e4c3-113">~ FmsModified</span><span class="sxs-lookup"><span data-stu-id="3e4c3-113">~fmsModified</span></span>  <br/> |
|<span data-ttu-id="3e4c3-114">MSGFLAG_SUBMIT</span><span class="sxs-lookup"><span data-stu-id="3e4c3-114">MSGFLAG_SUBMIT</span></span>  <br/> |<span data-ttu-id="3e4c3-115">fmsSubmitted</span><span class="sxs-lookup"><span data-stu-id="3e4c3-115">fmsSubmitted</span></span>  <br/> |
|<span data-ttu-id="3e4c3-116">MSGFLAG_HASATTACH</span><span class="sxs-lookup"><span data-stu-id="3e4c3-116">MSGFLAG_HASATTACH</span></span>  <br/> |<span data-ttu-id="3e4c3-117">fmsHasAttach</span><span class="sxs-lookup"><span data-stu-id="3e4c3-117">fmsHasAttach</span></span>  <br/> |
|<span data-ttu-id="3e4c3-118">MSGFLAG_UNSENT</span><span class="sxs-lookup"><span data-stu-id="3e4c3-118">MSGFLAG_UNSENT</span></span>  <br/> |<span data-ttu-id="3e4c3-119">fmsLocal</span><span class="sxs-lookup"><span data-stu-id="3e4c3-119">fmsLocal</span></span>  <br/> |
   
<span data-ttu-id="3e4c3-120">Diese Flags werden in die TNEF definiert. H-Headerdatei.</span><span class="sxs-lookup"><span data-stu-id="3e4c3-120">These flags are defined in the TNEF.H header file.</span></span>
  

