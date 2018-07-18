---
title: SMAPIVerb
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SMAPIVerb
api_type:
- COM
ms.assetid: 45066528-2447-4178-aaa3-7513ed0b3ba4
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 4d060d62deb685b4691846c2b8e48a82ae3195ea
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795599"
---
# <a name="smapiverb"></a><span data-ttu-id="62a9b-103">SMAPIVerb</span><span class="sxs-lookup"><span data-stu-id="62a9b-103">SMAPIVerb</span></span>

  
  
<span data-ttu-id="62a9b-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="62a9b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="62a9b-105">Beschreibt ein MAPI-Verb an.</span><span class="sxs-lookup"><span data-stu-id="62a9b-105">Describes a MAPI verb.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="62a9b-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="62a9b-106">Header file:</span></span>  <br/> |<span data-ttu-id="62a9b-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="62a9b-107">Mapiform.h</span></span>  <br/> |
   
```cpp
typedef struct
{
  ULONG lVerb;
  LPSTR szVerbname;
  DWORD fuFlags;
  DWORD grfAttribs;
  ULONG ulFlags; /* Either 0 or MAPI_UNICODE */
} SMAPIVerb, FAR * LPMAPIVERB;

```

## <a name="members"></a><span data-ttu-id="62a9b-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="62a9b-108">Members</span></span>

 <span data-ttu-id="62a9b-109">**lVerb**</span><span class="sxs-lookup"><span data-stu-id="62a9b-109">**lVerb**</span></span>
  
> <span data-ttu-id="62a9b-110">Code, der das Verb an, das an [IMAPIForm::DoVerb](imapiform-doverb.md)übergeben wird, darstellt.</span><span class="sxs-lookup"><span data-stu-id="62a9b-110">Code representing the verb that is passed to [IMAPIForm::DoVerb](imapiform-doverb.md).</span></span> <span data-ttu-id="62a9b-111">Standard-Verben sind in der Headerdatei Exchform.h definiert.</span><span class="sxs-lookup"><span data-stu-id="62a9b-111">Standard verbs are defined in the header file Exchform.h.</span></span>
    
 <span data-ttu-id="62a9b-112">**szVerbname**</span><span class="sxs-lookup"><span data-stu-id="62a9b-112">**szVerbname**</span></span>
  
> <span data-ttu-id="62a9b-113">Anzeigename des Verbs, die im Formular angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="62a9b-113">Display name of the verb as it appears on the form menu.</span></span>
    
 <span data-ttu-id="62a9b-114">**fuFlags**</span><span class="sxs-lookup"><span data-stu-id="62a9b-114">**fuFlags**</span></span>
  
> <span data-ttu-id="62a9b-115">Flags für das Verb.</span><span class="sxs-lookup"><span data-stu-id="62a9b-115">Flags for the verb.</span></span>
    
 <span data-ttu-id="62a9b-116">**grfAttribs**</span><span class="sxs-lookup"><span data-stu-id="62a9b-116">**grfAttribs**</span></span>
  
> <span data-ttu-id="62a9b-117">Attribute des Verbs.</span><span class="sxs-lookup"><span data-stu-id="62a9b-117">Attributes of the verb.</span></span> 
    
 <span data-ttu-id="62a9b-118">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="62a9b-118">**ulFlags**</span></span>
  
> <span data-ttu-id="62a9b-119">Kennzeichen Sie, die das Format des Anzeigenamens des Verbs.</span><span class="sxs-lookup"><span data-stu-id="62a9b-119">Flag indicating the format of the verb's display name.</span></span> <span data-ttu-id="62a9b-120">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="62a9b-120">The following flag can be set:</span></span>
    
<span data-ttu-id="62a9b-121">PARAMETER MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="62a9b-121">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="62a9b-122">Der Anzeigename ist im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="62a9b-122">The display name is in Unicode format.</span></span> <span data-ttu-id="62a9b-123">Wenn die Option MAPI_UNICODE nicht festgelegt ist, ist der Anzeigename im ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="62a9b-123">If the MAPI_UNICODE flag is not set, the display name is in ANSI format.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="62a9b-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="62a9b-124">Remarks</span></span>

<span data-ttu-id="62a9b-125">Die Struktur **SMAPIVerb** wird als Parameter in der folgenden Methoden übergeben:</span><span class="sxs-lookup"><span data-stu-id="62a9b-125">The **SMAPIVerb** structure is passed as a parameter in the following methods:</span></span> 
  
- [<span data-ttu-id="62a9b-126">IMAPIFormContainer::ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="62a9b-126">IMAPIFormContainer::ResolveMultipleMessageClasses</span></span>](imapiformcontainer-resolvemultiplemessageclasses.md)
    
- [<span data-ttu-id="62a9b-127">IMAPIFormMgr::ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="62a9b-127">IMAPIFormMgr::ResolveMultipleMessageClasses</span></span>](imapiformmgr-resolvemultiplemessageclasses.md)
    
## <a name="see-also"></a><span data-ttu-id="62a9b-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="62a9b-128">See also</span></span>



[<span data-ttu-id="62a9b-129">CbMessageClassArray</span><span class="sxs-lookup"><span data-stu-id="62a9b-129">CbMessageClassArray</span></span>](cbmessageclassarray.md)


[<span data-ttu-id="62a9b-130">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="62a9b-130">MAPI Structures</span></span>](mapi-structures.md)

