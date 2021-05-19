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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 3ef284a2c036abb9eac10ecf33de4adbf61f3c54
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410959"
---
# <a name="smapiverb"></a><span data-ttu-id="7e544-103">SMAPIVerb</span><span class="sxs-lookup"><span data-stu-id="7e544-103">SMAPIVerb</span></span>

  
  
<span data-ttu-id="7e544-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7e544-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7e544-105">Beschreibt ein MAPI-Verb.</span><span class="sxs-lookup"><span data-stu-id="7e544-105">Describes a MAPI verb.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7e544-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="7e544-106">Header file:</span></span>  <br/> |<span data-ttu-id="7e544-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="7e544-107">Mapiform.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="7e544-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="7e544-108">Members</span></span>

 <span data-ttu-id="7e544-109">**lVerb**</span><span class="sxs-lookup"><span data-stu-id="7e544-109">**lVerb**</span></span>
  
> <span data-ttu-id="7e544-110">Code, der das Verb darstellt, das an [IMAPIForm::D oVerb übergeben wird.](imapiform-doverb.md)</span><span class="sxs-lookup"><span data-stu-id="7e544-110">Code representing the verb that is passed to [IMAPIForm::DoVerb](imapiform-doverb.md).</span></span> <span data-ttu-id="7e544-111">Standardverben werden in der Headerdatei Exchform.h definiert.</span><span class="sxs-lookup"><span data-stu-id="7e544-111">Standard verbs are defined in the header file Exchform.h.</span></span>
    
 <span data-ttu-id="7e544-112">**szVerbname**</span><span class="sxs-lookup"><span data-stu-id="7e544-112">**szVerbname**</span></span>
  
> <span data-ttu-id="7e544-113">Anzeigename des Verbs, wie es im Formularmenü angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="7e544-113">Display name of the verb as it appears on the form menu.</span></span>
    
 <span data-ttu-id="7e544-114">**fuFlags**</span><span class="sxs-lookup"><span data-stu-id="7e544-114">**fuFlags**</span></span>
  
> <span data-ttu-id="7e544-115">Flags für das Verb.</span><span class="sxs-lookup"><span data-stu-id="7e544-115">Flags for the verb.</span></span>
    
 <span data-ttu-id="7e544-116">**grfAttribs**</span><span class="sxs-lookup"><span data-stu-id="7e544-116">**grfAttribs**</span></span>
  
> <span data-ttu-id="7e544-117">Attribute des Verbs.</span><span class="sxs-lookup"><span data-stu-id="7e544-117">Attributes of the verb.</span></span> 
    
 <span data-ttu-id="7e544-118">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="7e544-118">**ulFlags**</span></span>
  
> <span data-ttu-id="7e544-119">Flag, das das Format des Anzeigenamens des Verbs angibt.</span><span class="sxs-lookup"><span data-stu-id="7e544-119">Flag indicating the format of the verb's display name.</span></span> <span data-ttu-id="7e544-120">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="7e544-120">The following flag can be set:</span></span>
    
<span data-ttu-id="7e544-121">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="7e544-121">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="7e544-122">Der Anzeigename ist im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="7e544-122">The display name is in Unicode format.</span></span> <span data-ttu-id="7e544-123">Wenn das MAPI_UNICODE nicht festgelegt ist, befindet sich der Anzeigename im ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="7e544-123">If the MAPI_UNICODE flag is not set, the display name is in ANSI format.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7e544-124">Hinweise</span><span class="sxs-lookup"><span data-stu-id="7e544-124">Remarks</span></span>

<span data-ttu-id="7e544-125">Die **SMAPIVerb-Struktur** wird in den folgenden Methoden als Parameter übergeben:</span><span class="sxs-lookup"><span data-stu-id="7e544-125">The **SMAPIVerb** structure is passed as a parameter in the following methods:</span></span> 
  
- [<span data-ttu-id="7e544-126">IMAPIFormContainer::ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="7e544-126">IMAPIFormContainer::ResolveMultipleMessageClasses</span></span>](imapiformcontainer-resolvemultiplemessageclasses.md)
    
- [<span data-ttu-id="7e544-127">IMAPIFormMgr::ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="7e544-127">IMAPIFormMgr::ResolveMultipleMessageClasses</span></span>](imapiformmgr-resolvemultiplemessageclasses.md)
    
## <a name="see-also"></a><span data-ttu-id="7e544-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7e544-128">See also</span></span>



[<span data-ttu-id="7e544-129">CbMessageClassArray</span><span class="sxs-lookup"><span data-stu-id="7e544-129">CbMessageClassArray</span></span>](cbmessageclassarray.md)


[<span data-ttu-id="7e544-130">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="7e544-130">MAPI Structures</span></span>](mapi-structures.md)

