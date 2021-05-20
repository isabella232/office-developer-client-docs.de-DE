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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: a2a6d273495df52adb83393dc5549b0872c8f6f3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439359"
---
# <a name="srestriction"></a><span data-ttu-id="f27e0-103">SRestriction</span><span class="sxs-lookup"><span data-stu-id="f27e0-103">SRestriction</span></span>

  
  
<span data-ttu-id="f27e0-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f27e0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f27e0-105">Beschreibt einen Filter zum Einschränken der Ansicht einer Tabelle auf bestimmte Zeilen.</span><span class="sxs-lookup"><span data-stu-id="f27e0-105">Describes a filter for limiting the view of a table to particular rows.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f27e0-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="f27e0-106">Header file:</span></span>  <br/> |<span data-ttu-id="f27e0-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f27e0-107">Mapidefs.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="f27e0-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="f27e0-108">Members</span></span>

 <span data-ttu-id="f27e0-109">**rt**</span><span class="sxs-lookup"><span data-stu-id="f27e0-109">**rt**</span></span>
  
> <span data-ttu-id="f27e0-110">Der Einschränkungstyp.</span><span class="sxs-lookup"><span data-stu-id="f27e0-110">The restriction type.</span></span> <span data-ttu-id="f27e0-111">Mögliche Werte sind:</span><span class="sxs-lookup"><span data-stu-id="f27e0-111">Possible values are as follows:</span></span> 
    
<span data-ttu-id="f27e0-112">RES_AND</span><span class="sxs-lookup"><span data-stu-id="f27e0-112">RES_AND</span></span> 
  
> <span data-ttu-id="f27e0-113">Eine **AND-Einschränkung,** die einen bitweisen **AND-Vorgang** auf eine Einschränkung angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="f27e0-113">An **AND** restriction, which applies a bitwise **AND** operation to a restriction.</span></span> 
    
<span data-ttu-id="f27e0-114">RES_BITMASK</span><span class="sxs-lookup"><span data-stu-id="f27e0-114">RES_BITMASK</span></span> 
  
> <span data-ttu-id="f27e0-115">Eine Bitmaskeneinschränkung, die eine Bitmaske auf einen Eigenschaftswert angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="f27e0-115">A bitmask restriction, which applies a bitmask to a property value.</span></span>
    
<span data-ttu-id="f27e0-116">RES_COMMENT</span><span class="sxs-lookup"><span data-stu-id="f27e0-116">RES_COMMENT</span></span> 
  
> <span data-ttu-id="f27e0-117">Eine Kommentareinschränkung, die einen Kommentar einer Einschränkung zu ordnet.</span><span class="sxs-lookup"><span data-stu-id="f27e0-117">A comment restriction, which associates a comment with a restriction.</span></span>
    
<span data-ttu-id="f27e0-118">RES_COMPAREPROPS</span><span class="sxs-lookup"><span data-stu-id="f27e0-118">RES_COMPAREPROPS</span></span> 
  
> <span data-ttu-id="f27e0-119">Eine Eigenschaftsvergleichseinschränkung, die zwei Eigenschaftswerte vergleicht.</span><span class="sxs-lookup"><span data-stu-id="f27e0-119">A property comparison restriction, which compares two property values.</span></span>
    
<span data-ttu-id="f27e0-120">RES_CONTENT</span><span class="sxs-lookup"><span data-stu-id="f27e0-120">RES_CONTENT</span></span> 
  
> <span data-ttu-id="f27e0-121">Eine Inhaltseinschränkung, die einen Eigenschaftswert nach bestimmten Inhalten durchsucht.</span><span class="sxs-lookup"><span data-stu-id="f27e0-121">A content restriction, which searches a property value for specific content.</span></span>
    
<span data-ttu-id="f27e0-122">RES_EXIST</span><span class="sxs-lookup"><span data-stu-id="f27e0-122">RES_EXIST</span></span> 
  
> <span data-ttu-id="f27e0-123">Eine exist-Einschränkung, die bestimmt, ob eine Eigenschaft unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="f27e0-123">An exist restriction, which determines whether a property is supported.</span></span>
    
<span data-ttu-id="f27e0-124">RES_NOT</span><span class="sxs-lookup"><span data-stu-id="f27e0-124">RES_NOT</span></span> 
  
> <span data-ttu-id="f27e0-125">Eine **NOT-Einschränkung,** die einen logischen **NOT-Vorgang** auf eine Einschränkung angewendet.</span><span class="sxs-lookup"><span data-stu-id="f27e0-125">A **NOT** restriction, which applies a logical **NOT** operation to a restriction.</span></span> 
    
<span data-ttu-id="f27e0-126">RES_OR</span><span class="sxs-lookup"><span data-stu-id="f27e0-126">RES_OR</span></span> 
  
> <span data-ttu-id="f27e0-127">Eine **OR-Einschränkung,** die einen logischen **OR-Vorgang** auf eine Einschränkung angewendet.</span><span class="sxs-lookup"><span data-stu-id="f27e0-127">An **OR** restriction, which applies a logical **OR** operation to a restriction.</span></span> 
    
<span data-ttu-id="f27e0-128">RES_PROPERTY</span><span class="sxs-lookup"><span data-stu-id="f27e0-128">RES_PROPERTY</span></span> 
  
> <span data-ttu-id="f27e0-129">Eine Eigenschaftseinschränkung, die bestimmt, ob ein Eigenschaftswert einem bestimmten Wert entspricht.</span><span class="sxs-lookup"><span data-stu-id="f27e0-129">A property restriction, which determines whether a property value matches a particular value.</span></span>
    
<span data-ttu-id="f27e0-130">RES_SIZE</span><span class="sxs-lookup"><span data-stu-id="f27e0-130">RES_SIZE</span></span> 
  
> <span data-ttu-id="f27e0-131">Eine Größeneinschränkung, die bestimmt, ob ein Eigenschaftswert eine bestimmte Größe ist.</span><span class="sxs-lookup"><span data-stu-id="f27e0-131">A size restriction, which determines whether a property value is a particular size.</span></span>
    
<span data-ttu-id="f27e0-132">RES_SUBRESTRICTION</span><span class="sxs-lookup"><span data-stu-id="f27e0-132">RES_SUBRESTRICTION</span></span> 
  
> <span data-ttu-id="f27e0-133">Eine Unterobjekteinschränkung, die eine Einschränkung auf die Anlagen oder Empfänger einer Nachricht angewendet.</span><span class="sxs-lookup"><span data-stu-id="f27e0-133">A sub-object restriction, which applies a restriction to a message's attachments or recipients.</span></span>
    
 <span data-ttu-id="f27e0-134">**res**</span><span class="sxs-lookup"><span data-stu-id="f27e0-134">**res**</span></span>
  
> <span data-ttu-id="f27e0-135">Union von Einschränkungsstrukturen, die den anzuwendende Filter beschreiben.</span><span class="sxs-lookup"><span data-stu-id="f27e0-135">Union of restriction structures describing the filter to be applied.</span></span> <span data-ttu-id="f27e0-136">Die spezifische Struktur, die im **res-Element** enthalten ist, hängt vom Wert des **rt-Mitglieds** ab.</span><span class="sxs-lookup"><span data-stu-id="f27e0-136">The specific structure included in the **res** member depends on the value of the **rt** member.</span></span> <span data-ttu-id="f27e0-137">Die Zuordnung zwischen Einschränkungstyp und Struktur ist in der folgenden Tabelle aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="f27e0-137">The mapping between restriction type and structure is listed in the following table.</span></span> 
    
|||
|:-----|:-----|
|<span data-ttu-id="f27e0-138">**Einschränkungstyp**</span><span class="sxs-lookup"><span data-stu-id="f27e0-138">**Restriction type**</span></span> <br/> |<span data-ttu-id="f27e0-139">**Einschränkungsstruktur**</span><span class="sxs-lookup"><span data-stu-id="f27e0-139">**Restriction structure**</span></span> <br/> |
|<span data-ttu-id="f27e0-140">RES_AND</span><span class="sxs-lookup"><span data-stu-id="f27e0-140">RES_AND</span></span>  <br/> |[<span data-ttu-id="f27e0-141">SAndRestriction</span><span class="sxs-lookup"><span data-stu-id="f27e0-141">SAndRestriction</span></span>](sandrestriction.md) <br/> |
|<span data-ttu-id="f27e0-142">RES_BITMASK</span><span class="sxs-lookup"><span data-stu-id="f27e0-142">RES_BITMASK</span></span>  <br/> |[<span data-ttu-id="f27e0-143">SBitMaskRestriction</span><span class="sxs-lookup"><span data-stu-id="f27e0-143">SBitMaskRestriction</span></span>](sbitmaskrestriction.md) <br/> |
|<span data-ttu-id="f27e0-144">RES_COMMENT</span><span class="sxs-lookup"><span data-stu-id="f27e0-144">RES_COMMENT</span></span>  <br/> |[<span data-ttu-id="f27e0-145">SCommentRestriction</span><span class="sxs-lookup"><span data-stu-id="f27e0-145">SCommentRestriction</span></span>](scommentrestriction.md) <br/> |
|<span data-ttu-id="f27e0-146">RES_COMPAREPROPS</span><span class="sxs-lookup"><span data-stu-id="f27e0-146">RES_COMPAREPROPS</span></span>  <br/> |[<span data-ttu-id="f27e0-147">SComparePropsRestriction</span><span class="sxs-lookup"><span data-stu-id="f27e0-147">SComparePropsRestriction</span></span>](scomparepropsrestriction.md) <br/> |
|<span data-ttu-id="f27e0-148">RES_CONTENT</span><span class="sxs-lookup"><span data-stu-id="f27e0-148">RES_CONTENT</span></span>  <br/> |[<span data-ttu-id="f27e0-149">SContentRestriction</span><span class="sxs-lookup"><span data-stu-id="f27e0-149">SContentRestriction</span></span>](scontentrestriction.md) <br/> |
|<span data-ttu-id="f27e0-150">RES_EXIST</span><span class="sxs-lookup"><span data-stu-id="f27e0-150">RES_EXIST</span></span>  <br/> |[<span data-ttu-id="f27e0-151">SExistRestriction</span><span class="sxs-lookup"><span data-stu-id="f27e0-151">SExistRestriction</span></span>](sexistrestriction.md) <br/> |
|<span data-ttu-id="f27e0-152">RES_NOT</span><span class="sxs-lookup"><span data-stu-id="f27e0-152">RES_NOT</span></span>  <br/> |[<span data-ttu-id="f27e0-153">SNotRestriction</span><span class="sxs-lookup"><span data-stu-id="f27e0-153">SNotRestriction</span></span>](snotrestriction.md) <br/> |
|<span data-ttu-id="f27e0-154">RES_OR</span><span class="sxs-lookup"><span data-stu-id="f27e0-154">RES_OR</span></span>  <br/> |[<span data-ttu-id="f27e0-155">SOrRestriction</span><span class="sxs-lookup"><span data-stu-id="f27e0-155">SOrRestriction</span></span>](sorrestriction.md) <br/> |
|<span data-ttu-id="f27e0-156">RES_PROPERTY</span><span class="sxs-lookup"><span data-stu-id="f27e0-156">RES_PROPERTY</span></span>  <br/> |[<span data-ttu-id="f27e0-157">SPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="f27e0-157">SPropertyRestriction</span></span>](spropertyrestriction.md) <br/> |
|<span data-ttu-id="f27e0-158">RES_SIZE</span><span class="sxs-lookup"><span data-stu-id="f27e0-158">RES_SIZE</span></span>  <br/> |[<span data-ttu-id="f27e0-159">SSizeRestriction</span><span class="sxs-lookup"><span data-stu-id="f27e0-159">SSizeRestriction</span></span>](ssizerestriction.md) <br/> |
|<span data-ttu-id="f27e0-160">RES_SUBRESTRICTION</span><span class="sxs-lookup"><span data-stu-id="f27e0-160">RES_SUBRESTRICTION</span></span>  <br/> |[<span data-ttu-id="f27e0-161">SSubRestriction</span><span class="sxs-lookup"><span data-stu-id="f27e0-161">SSubRestriction</span></span>](ssubrestriction.md) <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f27e0-162">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f27e0-162">Remarks</span></span>

<span data-ttu-id="f27e0-163">Clients verwenden eine **SRestriction-Struktur,** um die Anzahl und den Typ der Zeilen in ihrer Tabellenansicht zu begrenzen und nach bestimmten Nachrichten in einem Ordner zu suchen.</span><span class="sxs-lookup"><span data-stu-id="f27e0-163">Clients use an **SRestriction** structure to limit the number and type of rows in their view of a table and to search for specific messages in a folder.</span></span> <span data-ttu-id="f27e0-164">Um eine Tabelle zu beschränken, rufen Clients [entweder IMAPITable::Restrict](imapitable-restrict.md) oder [IMAPITable::FindRow auf.](imapitable-findrow.md)</span><span class="sxs-lookup"><span data-stu-id="f27e0-164">To impose the limitation on a table, clients call either [IMAPITable::Restrict](imapitable-restrict.md) or [IMAPITable::FindRow](imapitable-findrow.md).</span></span> <span data-ttu-id="f27e0-165">Um die Einschränkung für einen Ordner zu verhängen, rufen Clients die [IMAPIContainer::SetSearchCriteria-Methode](imapicontainer-setsearchcriteria.md) des Ordners auf.</span><span class="sxs-lookup"><span data-stu-id="f27e0-165">To impose the limitation on a folder, clients call the folder's [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) method.</span></span> 
  
<span data-ttu-id="f27e0-166">Informationen zur Verwendung von Einschränkungen für Tabellen finden Sie unter [Informationen zu Einschränkungen](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="f27e0-166">For information about how to use restrictions with tables, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f27e0-167">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f27e0-167">See also</span></span>



[<span data-ttu-id="f27e0-168">SAndRestriction</span><span class="sxs-lookup"><span data-stu-id="f27e0-168">SAndRestriction</span></span>](sandrestriction.md)
  
[<span data-ttu-id="f27e0-169">SBitMaskRestriction</span><span class="sxs-lookup"><span data-stu-id="f27e0-169">SBitMaskRestriction</span></span>](sbitmaskrestriction.md)
  
[<span data-ttu-id="f27e0-170">SCommentRestriction</span><span class="sxs-lookup"><span data-stu-id="f27e0-170">SCommentRestriction</span></span>](scommentrestriction.md)
  
[<span data-ttu-id="f27e0-171">SComparePropsRestriction</span><span class="sxs-lookup"><span data-stu-id="f27e0-171">SComparePropsRestriction</span></span>](scomparepropsrestriction.md)
  
[<span data-ttu-id="f27e0-172">SContentRestriction</span><span class="sxs-lookup"><span data-stu-id="f27e0-172">SContentRestriction</span></span>](scontentrestriction.md)
  
[<span data-ttu-id="f27e0-173">SExistRestriction</span><span class="sxs-lookup"><span data-stu-id="f27e0-173">SExistRestriction</span></span>](sexistrestriction.md)
  
[<span data-ttu-id="f27e0-174">SNotRestriction</span><span class="sxs-lookup"><span data-stu-id="f27e0-174">SNotRestriction</span></span>](snotrestriction.md)
  
[<span data-ttu-id="f27e0-175">SOrRestriction</span><span class="sxs-lookup"><span data-stu-id="f27e0-175">SOrRestriction</span></span>](sorrestriction.md)
  
[<span data-ttu-id="f27e0-176">SPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="f27e0-176">SPropertyRestriction</span></span>](spropertyrestriction.md)
  
[<span data-ttu-id="f27e0-177">SSizeRestriction</span><span class="sxs-lookup"><span data-stu-id="f27e0-177">SSizeRestriction</span></span>](ssizerestriction.md)
  
[<span data-ttu-id="f27e0-178">SSubRestriction</span><span class="sxs-lookup"><span data-stu-id="f27e0-178">SSubRestriction</span></span>](ssubrestriction.md)


[<span data-ttu-id="f27e0-179">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="f27e0-179">MAPI Structures</span></span>](mapi-structures.md)

