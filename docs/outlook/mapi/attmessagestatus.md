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
ms.openlocfilehash: d4dc72309ff090317b2353cab0b4fc2c5be41181
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430315"
---
# <a name="attmessagestatus"></a><span data-ttu-id="62182-103">attMessageStatus</span><span class="sxs-lookup"><span data-stu-id="62182-103">attMessageStatus</span></span>

  
  
<span data-ttu-id="62182-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="62182-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="62182-105">MAPI-Nachrichtenflags werden TNEF-Flags zugeordnet, um die Abwärtskompatibilität zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="62182-105">MAPI message flags are mapped to TNEF flags to preserve backward compatibility.</span></span> <span data-ttu-id="62182-106">Alle Flags werden in einem einzelnen Byte gruppieren und codiert.</span><span class="sxs-lookup"><span data-stu-id="62182-106">All the flags are grouped together and encoded in a single byte.</span></span> <span data-ttu-id="62182-107">Die Zuordnungen sind wie folgt:</span><span class="sxs-lookup"><span data-stu-id="62182-107">The mappings are as follows:</span></span>
  
|<span data-ttu-id="62182-108">**MAPI-Nachrichtenflags**</span><span class="sxs-lookup"><span data-stu-id="62182-108">**MAPI message flags**</span></span>|<span data-ttu-id="62182-109">**TNEF-Flags**</span><span class="sxs-lookup"><span data-stu-id="62182-109">**TNEF flags**</span></span>|
|:-----|:-----|
|<span data-ttu-id="62182-110">MSGFLAG_READ</span><span class="sxs-lookup"><span data-stu-id="62182-110">MSGFLAG_READ</span></span>  <br/> |<span data-ttu-id="62182-111">fmsRead</span><span class="sxs-lookup"><span data-stu-id="62182-111">fmsRead</span></span>  <br/> |
|<span data-ttu-id="62182-112">MSGFLAG_UNMODIFED</span><span class="sxs-lookup"><span data-stu-id="62182-112">MSGFLAG_UNMODIFED</span></span>  <br/> |<span data-ttu-id="62182-113">~fmsModified</span><span class="sxs-lookup"><span data-stu-id="62182-113">~fmsModified</span></span>  <br/> |
|<span data-ttu-id="62182-114">MSGFLAG_SUBMIT</span><span class="sxs-lookup"><span data-stu-id="62182-114">MSGFLAG_SUBMIT</span></span>  <br/> |<span data-ttu-id="62182-115">fmsSubmitted</span><span class="sxs-lookup"><span data-stu-id="62182-115">fmsSubmitted</span></span>  <br/> |
|<span data-ttu-id="62182-116">MSGFLAG_HASATTACH</span><span class="sxs-lookup"><span data-stu-id="62182-116">MSGFLAG_HASATTACH</span></span>  <br/> |<span data-ttu-id="62182-117">fmsHasAttach</span><span class="sxs-lookup"><span data-stu-id="62182-117">fmsHasAttach</span></span>  <br/> |
|<span data-ttu-id="62182-118">MSGFLAG_UNSENT</span><span class="sxs-lookup"><span data-stu-id="62182-118">MSGFLAG_UNSENT</span></span>  <br/> |<span data-ttu-id="62182-119">fmsLocal</span><span class="sxs-lookup"><span data-stu-id="62182-119">fmsLocal</span></span>  <br/> |
   
<span data-ttu-id="62182-120">Diese Flags werden im TNEF definiert. H-Headerdatei.</span><span class="sxs-lookup"><span data-stu-id="62182-120">These flags are defined in the TNEF.H header file.</span></span>
  

