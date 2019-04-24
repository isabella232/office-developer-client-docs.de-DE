---
title: SRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SRestriction
api_type:
- COM
ms.assetid: c12b4409-da6f-480b-87af-1e5baea2e8bd
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: a2a6d273495df52adb83393dc5549b0872c8f6f3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341741"
---
# <a name="srestriction"></a><span data-ttu-id="9f341-103">SRestriction</span><span class="sxs-lookup"><span data-stu-id="9f341-103">SRestriction</span></span>

  
  
<span data-ttu-id="9f341-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9f341-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9f341-105">Beschreibt einen Filter zum Einschränken der Ansicht einer Tabelle auf bestimmte Zeilen.</span><span class="sxs-lookup"><span data-stu-id="9f341-105">Describes a filter for limiting the view of a table to particular rows.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9f341-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="9f341-106">Header file:</span></span>  <br/> |<span data-ttu-id="9f341-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="9f341-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SRestriction
{
  ULONG rt;
  union
  {
    SComparePropsRestriction resCompareProps;
    SAndRestriction resAnd;
    SOrRestriction resOr;
    SNotRestriction resNot;
    SContentRestriction resContent;
    SPropertyRestriction resProperty;
    SBitMaskRestriction resBitMask;
    SSizeRestriction resSize;
    SExistRestriction resExist;
    SSubRestriction resSub;
    SCommentRestriction resComment;
  } res;
} SRestriction;

```

## <a name="members"></a><span data-ttu-id="9f341-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="9f341-108">Members</span></span>

 <span data-ttu-id="9f341-109">**RT**</span><span class="sxs-lookup"><span data-stu-id="9f341-109">**rt**</span></span>
  
> <span data-ttu-id="9f341-110">Der Einschränkungs.</span><span class="sxs-lookup"><span data-stu-id="9f341-110">The restriction type.</span></span> <span data-ttu-id="9f341-111">Folgende Werte sind möglich:</span><span class="sxs-lookup"><span data-stu-id="9f341-111">Possible values are as follows:</span></span> 
    
<span data-ttu-id="9f341-112">RES_AND</span><span class="sxs-lookup"><span data-stu-id="9f341-112">RES_AND</span></span> 
  
> <span data-ttu-id="9f341-113">Eine **and-** Einschränkung, die eine bitweise **and-** Operation auf eine Einschränkung anwendet.</span><span class="sxs-lookup"><span data-stu-id="9f341-113">An **AND** restriction, which applies a bitwise **AND** operation to a restriction.</span></span> 
    
<span data-ttu-id="9f341-114">RES_BITMASK</span><span class="sxs-lookup"><span data-stu-id="9f341-114">RES_BITMASK</span></span> 
  
> <span data-ttu-id="9f341-115">Eine Bitmasken Einschränkung, die eine Bitmaske auf einen Eigenschaftswert anwendet.</span><span class="sxs-lookup"><span data-stu-id="9f341-115">A bitmask restriction, which applies a bitmask to a property value.</span></span>
    
<span data-ttu-id="9f341-116">RES_COMMENT</span><span class="sxs-lookup"><span data-stu-id="9f341-116">RES_COMMENT</span></span> 
  
> <span data-ttu-id="9f341-117">Eine Kommentar Einschränkung, die einer Einschränkung einen Kommentar zuordnet.</span><span class="sxs-lookup"><span data-stu-id="9f341-117">A comment restriction, which associates a comment with a restriction.</span></span>
    
<span data-ttu-id="9f341-118">RES_COMPAREPROPS</span><span class="sxs-lookup"><span data-stu-id="9f341-118">RES_COMPAREPROPS</span></span> 
  
> <span data-ttu-id="9f341-119">Eine Eigenschafts Vergleichs Einschränkung, die zwei Eigenschaftswerte vergleicht.</span><span class="sxs-lookup"><span data-stu-id="9f341-119">A property comparison restriction, which compares two property values.</span></span>
    
<span data-ttu-id="9f341-120">RES_CONTENT</span><span class="sxs-lookup"><span data-stu-id="9f341-120">RES_CONTENT</span></span> 
  
> <span data-ttu-id="9f341-121">Eine Inhaltseinschränkung, die einen Eigenschaftswert nach bestimmten Inhalten durchsucht.</span><span class="sxs-lookup"><span data-stu-id="9f341-121">A content restriction, which searches a property value for specific content.</span></span>
    
<span data-ttu-id="9f341-122">RES_EXIST</span><span class="sxs-lookup"><span data-stu-id="9f341-122">RES_EXIST</span></span> 
  
> <span data-ttu-id="9f341-123">Eine exist-Einschränkung, die bestimmt, ob eine Eigenschaft unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="9f341-123">An exist restriction, which determines whether a property is supported.</span></span>
    
<span data-ttu-id="9f341-124">RES_NOT</span><span class="sxs-lookup"><span data-stu-id="9f341-124">RES_NOT</span></span> 
  
> <span data-ttu-id="9f341-125">Eine **nicht** -Einschränkung, die einen logischen **Not** -Vorgang auf eine Einschränkung anwendet.</span><span class="sxs-lookup"><span data-stu-id="9f341-125">A **NOT** restriction, which applies a logical **NOT** operation to a restriction.</span></span> 
    
<span data-ttu-id="9f341-126">RES_OR</span><span class="sxs-lookup"><span data-stu-id="9f341-126">RES_OR</span></span> 
  
> <span data-ttu-id="9f341-127">Eine **oder** -Einschränkung, die eine logische **or** -Operation auf eine Einschränkung anwendet.</span><span class="sxs-lookup"><span data-stu-id="9f341-127">An **OR** restriction, which applies a logical **OR** operation to a restriction.</span></span> 
    
<span data-ttu-id="9f341-128">RES_PROPERTY</span><span class="sxs-lookup"><span data-stu-id="9f341-128">RES_PROPERTY</span></span> 
  
> <span data-ttu-id="9f341-129">Eine Eigenschaftseinschränkung, die bestimmt, ob ein Eigenschaftswert einem bestimmten Wert entspricht.</span><span class="sxs-lookup"><span data-stu-id="9f341-129">A property restriction, which determines whether a property value matches a particular value.</span></span>
    
<span data-ttu-id="9f341-130">RES_SIZE</span><span class="sxs-lookup"><span data-stu-id="9f341-130">RES_SIZE</span></span> 
  
> <span data-ttu-id="9f341-131">Eine Größeneinschränkung, die bestimmt, ob ein Eigenschaftswert eine bestimmte Größe aufweist.</span><span class="sxs-lookup"><span data-stu-id="9f341-131">A size restriction, which determines whether a property value is a particular size.</span></span>
    
<span data-ttu-id="9f341-132">RES_SUBRESTRICTION</span><span class="sxs-lookup"><span data-stu-id="9f341-132">RES_SUBRESTRICTION</span></span> 
  
> <span data-ttu-id="9f341-133">Eine Unterobjekt Einschränkung, die eine Einschränkung auf die Anlagen oder Empfänger einer Nachricht anwendet.</span><span class="sxs-lookup"><span data-stu-id="9f341-133">A sub-object restriction, which applies a restriction to a message's attachments or recipients.</span></span>
    
 <span data-ttu-id="9f341-134">**res**</span><span class="sxs-lookup"><span data-stu-id="9f341-134">**res**</span></span>
  
> <span data-ttu-id="9f341-135">Vereinigung von Einschränkungs Strukturen zur Beschreibung des anzuwendenden Filters.</span><span class="sxs-lookup"><span data-stu-id="9f341-135">Union of restriction structures describing the filter to be applied.</span></span> <span data-ttu-id="9f341-136">Die im **Res** -Element enthaltene spezifische Struktur hängt vom Wert des **RT** -Members ab.</span><span class="sxs-lookup"><span data-stu-id="9f341-136">The specific structure included in the **res** member depends on the value of the **rt** member.</span></span> <span data-ttu-id="9f341-137">Die Zuordnung zwischen dem Einschränkungs und der Struktur ist in der folgenden Tabelle aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="9f341-137">The mapping between restriction type and structure is listed in the following table.</span></span> 
    
|||
|:-----|:-----|
|<span data-ttu-id="9f341-138">**Einschränkungs**</span><span class="sxs-lookup"><span data-stu-id="9f341-138">**Restriction type**</span></span> <br/> |<span data-ttu-id="9f341-139">**Einschränkungs Struktur**</span><span class="sxs-lookup"><span data-stu-id="9f341-139">**Restriction structure**</span></span> <br/> |
|<span data-ttu-id="9f341-140">RES_AND</span><span class="sxs-lookup"><span data-stu-id="9f341-140">RES_AND</span></span>  <br/> |[<span data-ttu-id="9f341-141">SAndRestriction</span><span class="sxs-lookup"><span data-stu-id="9f341-141">SAndRestriction</span></span>](sandrestriction.md) <br/> |
|<span data-ttu-id="9f341-142">RES_BITMASK</span><span class="sxs-lookup"><span data-stu-id="9f341-142">RES_BITMASK</span></span>  <br/> |[<span data-ttu-id="9f341-143">SBitMaskRestriction</span><span class="sxs-lookup"><span data-stu-id="9f341-143">SBitMaskRestriction</span></span>](sbitmaskrestriction.md) <br/> |
|<span data-ttu-id="9f341-144">RES_COMMENT</span><span class="sxs-lookup"><span data-stu-id="9f341-144">RES_COMMENT</span></span>  <br/> |[<span data-ttu-id="9f341-145">SCommentRestriction</span><span class="sxs-lookup"><span data-stu-id="9f341-145">SCommentRestriction</span></span>](scommentrestriction.md) <br/> |
|<span data-ttu-id="9f341-146">RES_COMPAREPROPS</span><span class="sxs-lookup"><span data-stu-id="9f341-146">RES_COMPAREPROPS</span></span>  <br/> |[<span data-ttu-id="9f341-147">SComparePropsRestriction</span><span class="sxs-lookup"><span data-stu-id="9f341-147">SComparePropsRestriction</span></span>](scomparepropsrestriction.md) <br/> |
|<span data-ttu-id="9f341-148">RES_CONTENT</span><span class="sxs-lookup"><span data-stu-id="9f341-148">RES_CONTENT</span></span>  <br/> |[<span data-ttu-id="9f341-149">SContentRestriction</span><span class="sxs-lookup"><span data-stu-id="9f341-149">SContentRestriction</span></span>](scontentrestriction.md) <br/> |
|<span data-ttu-id="9f341-150">RES_EXIST</span><span class="sxs-lookup"><span data-stu-id="9f341-150">RES_EXIST</span></span>  <br/> |[<span data-ttu-id="9f341-151">SExistRestriction</span><span class="sxs-lookup"><span data-stu-id="9f341-151">SExistRestriction</span></span>](sexistrestriction.md) <br/> |
|<span data-ttu-id="9f341-152">RES_NOT</span><span class="sxs-lookup"><span data-stu-id="9f341-152">RES_NOT</span></span>  <br/> |[<span data-ttu-id="9f341-153">SNotRestriction</span><span class="sxs-lookup"><span data-stu-id="9f341-153">SNotRestriction</span></span>](snotrestriction.md) <br/> |
|<span data-ttu-id="9f341-154">RES_OR</span><span class="sxs-lookup"><span data-stu-id="9f341-154">RES_OR</span></span>  <br/> |[<span data-ttu-id="9f341-155">SOrRestriction</span><span class="sxs-lookup"><span data-stu-id="9f341-155">SOrRestriction</span></span>](sorrestriction.md) <br/> |
|<span data-ttu-id="9f341-156">RES_PROPERTY</span><span class="sxs-lookup"><span data-stu-id="9f341-156">RES_PROPERTY</span></span>  <br/> |[<span data-ttu-id="9f341-157">SPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="9f341-157">SPropertyRestriction</span></span>](spropertyrestriction.md) <br/> |
|<span data-ttu-id="9f341-158">RES_SIZE</span><span class="sxs-lookup"><span data-stu-id="9f341-158">RES_SIZE</span></span>  <br/> |[<span data-ttu-id="9f341-159">SSizeRestriction</span><span class="sxs-lookup"><span data-stu-id="9f341-159">SSizeRestriction</span></span>](ssizerestriction.md) <br/> |
|<span data-ttu-id="9f341-160">RES_SUBRESTRICTION</span><span class="sxs-lookup"><span data-stu-id="9f341-160">RES_SUBRESTRICTION</span></span>  <br/> |[<span data-ttu-id="9f341-161">SSubRestriction</span><span class="sxs-lookup"><span data-stu-id="9f341-161">SSubRestriction</span></span>](ssubrestriction.md) <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9f341-162">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9f341-162">Remarks</span></span>

<span data-ttu-id="9f341-163">Clients verwenden eine **SRestriction** -Struktur, um die Anzahl und den Typ von Zeilen in der Ansicht einer Tabelle zu begrenzen und nach bestimmten Nachrichten in einem Ordner zu suchen.</span><span class="sxs-lookup"><span data-stu-id="9f341-163">Clients use an **SRestriction** structure to limit the number and type of rows in their view of a table and to search for specific messages in a folder.</span></span> <span data-ttu-id="9f341-164">Um die Einschränkung für eine Tabelle aufzuerlegen, rufen die Clients entweder [IMAPITable:: Restrict](imapitable-restrict.md) oder [IMAPITable:: FindRow](imapitable-findrow.md)auf.</span><span class="sxs-lookup"><span data-stu-id="9f341-164">To impose the limitation on a table, clients call either [IMAPITable::Restrict](imapitable-restrict.md) or [IMAPITable::FindRow](imapitable-findrow.md).</span></span> <span data-ttu-id="9f341-165">Um die Einschränkung für einen Ordner aufzuerlegen, rufen die Clients die [IMAPIContainer:: SetSearchCriteria](imapicontainer-setsearchcriteria.md) -Methode des Ordners auf.</span><span class="sxs-lookup"><span data-stu-id="9f341-165">To impose the limitation on a folder, clients call the folder's [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) method.</span></span> 
  
<span data-ttu-id="9f341-166">Informationen zur Verwendung von Einschränkungen mit Tabellen finden Sie unter [Informationen zu Einschränkungen](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="9f341-166">For information about how to use restrictions with tables, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9f341-167">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9f341-167">See also</span></span>



[<span data-ttu-id="9f341-168">SAndRestriction</span><span class="sxs-lookup"><span data-stu-id="9f341-168">SAndRestriction</span></span>](sandrestriction.md)
  
[<span data-ttu-id="9f341-169">SBitMaskRestriction</span><span class="sxs-lookup"><span data-stu-id="9f341-169">SBitMaskRestriction</span></span>](sbitmaskrestriction.md)
  
[<span data-ttu-id="9f341-170">SCommentRestriction</span><span class="sxs-lookup"><span data-stu-id="9f341-170">SCommentRestriction</span></span>](scommentrestriction.md)
  
[<span data-ttu-id="9f341-171">SComparePropsRestriction</span><span class="sxs-lookup"><span data-stu-id="9f341-171">SComparePropsRestriction</span></span>](scomparepropsrestriction.md)
  
[<span data-ttu-id="9f341-172">SContentRestriction</span><span class="sxs-lookup"><span data-stu-id="9f341-172">SContentRestriction</span></span>](scontentrestriction.md)
  
[<span data-ttu-id="9f341-173">SExistRestriction</span><span class="sxs-lookup"><span data-stu-id="9f341-173">SExistRestriction</span></span>](sexistrestriction.md)
  
[<span data-ttu-id="9f341-174">SNotRestriction</span><span class="sxs-lookup"><span data-stu-id="9f341-174">SNotRestriction</span></span>](snotrestriction.md)
  
[<span data-ttu-id="9f341-175">SOrRestriction</span><span class="sxs-lookup"><span data-stu-id="9f341-175">SOrRestriction</span></span>](sorrestriction.md)
  
[<span data-ttu-id="9f341-176">SPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="9f341-176">SPropertyRestriction</span></span>](spropertyrestriction.md)
  
[<span data-ttu-id="9f341-177">SSizeRestriction</span><span class="sxs-lookup"><span data-stu-id="9f341-177">SSizeRestriction</span></span>](ssizerestriction.md)
  
[<span data-ttu-id="9f341-178">SSubRestriction</span><span class="sxs-lookup"><span data-stu-id="9f341-178">SSubRestriction</span></span>](ssubrestriction.md)


[<span data-ttu-id="9f341-179">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="9f341-179">MAPI Structures</span></span>](mapi-structures.md)

