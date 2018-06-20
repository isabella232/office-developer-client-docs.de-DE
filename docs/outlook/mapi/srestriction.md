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
ms.openlocfilehash: 9748229799641d62b1649491c432f10164b49192
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795621"
---
# <a name="srestriction"></a><span data-ttu-id="128e6-103">SRestriction</span><span class="sxs-lookup"><span data-stu-id="128e6-103">SRestriction</span></span>

  
  
<span data-ttu-id="128e6-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="128e6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="128e6-105">Beschreibt einen Filter zum Einschränken der Ansicht in bestimmten Zeilen einer Tabelle.</span><span class="sxs-lookup"><span data-stu-id="128e6-105">Describes a filter for limiting the view of a table to particular rows.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="128e6-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="128e6-106">Header file:</span></span>  <br/> |<span data-ttu-id="128e6-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="128e6-107">Mapidefs.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="128e6-108">Members</span><span class="sxs-lookup"><span data-stu-id="128e6-108">Members</span></span>

 <span data-ttu-id="128e6-109">**RT**</span><span class="sxs-lookup"><span data-stu-id="128e6-109">**rt**</span></span>
  
> <span data-ttu-id="128e6-110">Der Typ der Einschränkung.</span><span class="sxs-lookup"><span data-stu-id="128e6-110">The restriction type.</span></span> <span data-ttu-id="128e6-111">Mögliche Werte sind wie folgt:</span><span class="sxs-lookup"><span data-stu-id="128e6-111">Possible values are as follows:</span></span> 
    
<span data-ttu-id="128e6-112">RES_AND</span><span class="sxs-lookup"><span data-stu-id="128e6-112">RES_AND</span></span> 
  
> <span data-ttu-id="128e6-113">Eine **AND** -Einschränkung, die eine bitweise **AND** -Operation für eine Beschränkung gilt.</span><span class="sxs-lookup"><span data-stu-id="128e6-113">An **AND** restriction, which applies a bitwise **AND** operation to a restriction.</span></span> 
    
<span data-ttu-id="128e6-114">RES_BITMASK</span><span class="sxs-lookup"><span data-stu-id="128e6-114">RES_BITMASK</span></span> 
  
> <span data-ttu-id="128e6-115">Eine Bitmaske-Einschränkung, die eine Bitmaske mit einem Eigenschaftswert angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="128e6-115">A bitmask restriction, which applies a bitmask to a property value.</span></span>
    
<span data-ttu-id="128e6-116">RES_COMMENT</span><span class="sxs-lookup"><span data-stu-id="128e6-116">RES_COMMENT</span></span> 
  
> <span data-ttu-id="128e6-117">Eine Einschränkung Kommentar, die einen Kommentar mit einer Einschränkung verknüpft.</span><span class="sxs-lookup"><span data-stu-id="128e6-117">A comment restriction, which associates a comment with a restriction.</span></span>
    
<span data-ttu-id="128e6-118">RES_COMPAREPROPS</span><span class="sxs-lookup"><span data-stu-id="128e6-118">RES_COMPAREPROPS</span></span> 
  
> <span data-ttu-id="128e6-119">Einen Vergleich eigenschaftseinschränkung, die zwei Eigenschaftswerten vergleicht.</span><span class="sxs-lookup"><span data-stu-id="128e6-119">A property comparison restriction, which compares two property values.</span></span>
    
<span data-ttu-id="128e6-120">RES_CONTENT</span><span class="sxs-lookup"><span data-stu-id="128e6-120">RES_CONTENT</span></span> 
  
> <span data-ttu-id="128e6-121">Eine Content Einschränkung, die einen Eigenschaftswert nach bestimmten Inhalten sucht.</span><span class="sxs-lookup"><span data-stu-id="128e6-121">A content restriction, which searches a property value for specific content.</span></span>
    
<span data-ttu-id="128e6-122">RES_EXIST</span><span class="sxs-lookup"><span data-stu-id="128e6-122">RES_EXIST</span></span> 
  
> <span data-ttu-id="128e6-123">Eine Einschränkung vorhanden, die bestimmt, ob eine Eigenschaft unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="128e6-123">An exist restriction, which determines whether a property is supported.</span></span>
    
<span data-ttu-id="128e6-124">RES_NOT</span><span class="sxs-lookup"><span data-stu-id="128e6-124">RES_NOT</span></span> 
  
> <span data-ttu-id="128e6-125">Eine **nicht** Einschränkung, die eine logische **NOT** -Operation für eine Beschränkung gilt.</span><span class="sxs-lookup"><span data-stu-id="128e6-125">A **NOT** restriction, which applies a logical **NOT** operation to a restriction.</span></span> 
    
<span data-ttu-id="128e6-126">RES_OR</span><span class="sxs-lookup"><span data-stu-id="128e6-126">RES_OR</span></span> 
  
> <span data-ttu-id="128e6-127">Eine **oder** -Einschränkung, die eine logische **OR** -Operation für eine Beschränkung gilt.</span><span class="sxs-lookup"><span data-stu-id="128e6-127">An **OR** restriction, which applies a logical **OR** operation to a restriction.</span></span> 
    
<span data-ttu-id="128e6-128">RES_PROPERTY</span><span class="sxs-lookup"><span data-stu-id="128e6-128">RES_PROPERTY</span></span> 
  
> <span data-ttu-id="128e6-129">Eine eigenschaftseinschränkung, die bestimmt, ob der Wert einer Eigenschaft mit einem bestimmten Wert übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="128e6-129">A property restriction, which determines whether a property value matches a particular value.</span></span>
    
<span data-ttu-id="128e6-130">RES_SIZE</span><span class="sxs-lookup"><span data-stu-id="128e6-130">RES_SIZE</span></span> 
  
> <span data-ttu-id="128e6-131">Eine Einschränkung Größe, die bestimmt, ob der Wert einer Eigenschaft eine bestimmte Größe ist.</span><span class="sxs-lookup"><span data-stu-id="128e6-131">A size restriction, which determines whether a property value is a particular size.</span></span>
    
<span data-ttu-id="128e6-132">RES_SUBRESTRICTION</span><span class="sxs-lookup"><span data-stu-id="128e6-132">RES_SUBRESTRICTION</span></span> 
  
> <span data-ttu-id="128e6-133">Eine Einschränkung Sub-Objekt, die eine Beschränkung auf Anlagen oder Empfänger einer Nachricht angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="128e6-133">A sub-object restriction, which applies a restriction to a message's attachments or recipients.</span></span>
    
 <span data-ttu-id="128e6-134">**res**</span><span class="sxs-lookup"><span data-stu-id="128e6-134">**res**</span></span>
  
> <span data-ttu-id="128e6-135">Union der Einschränkung Strukturen zur Beschreibung des Filters angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="128e6-135">Union of restriction structures describing the filter to be applied.</span></span> <span data-ttu-id="128e6-136">Die spezifische Struktur im **Res** -Member enthalten, hängt von den Wert des Elements **rt** ab.</span><span class="sxs-lookup"><span data-stu-id="128e6-136">The specific structure included in the **res** member depends on the value of the **rt** member.</span></span> <span data-ttu-id="128e6-137">Die Zuordnung zwischen mygal und Struktur wird in der folgenden Tabelle aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="128e6-137">The mapping between restriction type and structure is listed in the following table.</span></span> 
    
|||
|:-----|:-----|
|<span data-ttu-id="128e6-138">**Einschränkungstyp**</span><span class="sxs-lookup"><span data-stu-id="128e6-138">**Restriction type**</span></span> <br/> |<span data-ttu-id="128e6-139">**Struktur der Einschränkung**</span><span class="sxs-lookup"><span data-stu-id="128e6-139">**Restriction structure**</span></span> <br/> |
|<span data-ttu-id="128e6-140">RES_AND</span><span class="sxs-lookup"><span data-stu-id="128e6-140">RES_AND</span></span>  <br/> |[<span data-ttu-id="128e6-141">SAndRestriction</span><span class="sxs-lookup"><span data-stu-id="128e6-141">SAndRestriction</span></span>](sandrestriction.md) <br/> |
|<span data-ttu-id="128e6-142">RES_BITMASK</span><span class="sxs-lookup"><span data-stu-id="128e6-142">RES_BITMASK</span></span>  <br/> |[<span data-ttu-id="128e6-143">SBitMaskRestriction</span><span class="sxs-lookup"><span data-stu-id="128e6-143">SBitMaskRestriction</span></span>](sbitmaskrestriction.md) <br/> |
|<span data-ttu-id="128e6-144">RES_COMMENT</span><span class="sxs-lookup"><span data-stu-id="128e6-144">RES_COMMENT</span></span>  <br/> |[<span data-ttu-id="128e6-145">SCommentRestriction</span><span class="sxs-lookup"><span data-stu-id="128e6-145">SCommentRestriction</span></span>](scommentrestriction.md) <br/> |
|<span data-ttu-id="128e6-146">RES_COMPAREPROPS</span><span class="sxs-lookup"><span data-stu-id="128e6-146">RES_COMPAREPROPS</span></span>  <br/> |[<span data-ttu-id="128e6-147">SComparePropsRestriction</span><span class="sxs-lookup"><span data-stu-id="128e6-147">SComparePropsRestriction</span></span>](scomparepropsrestriction.md) <br/> |
|<span data-ttu-id="128e6-148">RES_CONTENT</span><span class="sxs-lookup"><span data-stu-id="128e6-148">RES_CONTENT</span></span>  <br/> |[<span data-ttu-id="128e6-149">SContentRestriction</span><span class="sxs-lookup"><span data-stu-id="128e6-149">SContentRestriction</span></span>](scontentrestriction.md) <br/> |
|<span data-ttu-id="128e6-150">RES_EXIST</span><span class="sxs-lookup"><span data-stu-id="128e6-150">RES_EXIST</span></span>  <br/> |[<span data-ttu-id="128e6-151">SExistRestriction</span><span class="sxs-lookup"><span data-stu-id="128e6-151">SExistRestriction</span></span>](sexistrestriction.md) <br/> |
|<span data-ttu-id="128e6-152">RES_NOT</span><span class="sxs-lookup"><span data-stu-id="128e6-152">RES_NOT</span></span>  <br/> |[<span data-ttu-id="128e6-153">SNotRestriction</span><span class="sxs-lookup"><span data-stu-id="128e6-153">SNotRestriction</span></span>](snotrestriction.md) <br/> |
|<span data-ttu-id="128e6-154">RES_OR</span><span class="sxs-lookup"><span data-stu-id="128e6-154">RES_OR</span></span>  <br/> |[<span data-ttu-id="128e6-155">SOrRestriction</span><span class="sxs-lookup"><span data-stu-id="128e6-155">SOrRestriction</span></span>](sorrestriction.md) <br/> |
|<span data-ttu-id="128e6-156">RES_PROPERTY</span><span class="sxs-lookup"><span data-stu-id="128e6-156">RES_PROPERTY</span></span>  <br/> |[<span data-ttu-id="128e6-157">SPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="128e6-157">SPropertyRestriction</span></span>](spropertyrestriction.md) <br/> |
|<span data-ttu-id="128e6-158">RES_SIZE</span><span class="sxs-lookup"><span data-stu-id="128e6-158">RES_SIZE</span></span>  <br/> |[<span data-ttu-id="128e6-159">SSizeRestriction</span><span class="sxs-lookup"><span data-stu-id="128e6-159">SSizeRestriction</span></span>](ssizerestriction.md) <br/> |
|<span data-ttu-id="128e6-160">RES_SUBRESTRICTION</span><span class="sxs-lookup"><span data-stu-id="128e6-160">RES_SUBRESTRICTION</span></span>  <br/> |[<span data-ttu-id="128e6-161">SSubRestriction</span><span class="sxs-lookup"><span data-stu-id="128e6-161">SSubRestriction</span></span>](ssubrestriction.md) <br/> |
   
## <a name="remarks"></a><span data-ttu-id="128e6-162">Hinweise</span><span class="sxs-lookup"><span data-stu-id="128e6-162">Remarks</span></span>

<span data-ttu-id="128e6-163">Clients verwenden eine **SRestriction** -Struktur, Anzahl und Typ der Zeilen in einer Tabelle ihre Ansicht einzuschränken und bestimmte Nachrichten in einem Ordner suchen.</span><span class="sxs-lookup"><span data-stu-id="128e6-163">Clients use an **SRestriction** structure to limit the number and type of rows in their view of a table and to search for specific messages in a folder.</span></span> <span data-ttu-id="128e6-164">Um die Einschränkung für eine Tabelle zu erzwingen, rufen Clients [Methode IMAPITable:: Restrict](imapitable-restrict.md) oder [IMAPITable](imapitable-findrow.md).</span><span class="sxs-lookup"><span data-stu-id="128e6-164">To impose the limitation on a table, clients call either [IMAPITable::Restrict](imapitable-restrict.md) or [IMAPITable::FindRow](imapitable-findrow.md).</span></span> <span data-ttu-id="128e6-165">Um die Einschränkung für einen Ordner zu erzwingen, rufen Clients auf den Ordner [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="128e6-165">To impose the limitation on a folder, clients call the folder's [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) method.</span></span> 
  
<span data-ttu-id="128e6-166">Informationen zur Verwendung von Einschränkungen mit Tabellen finden Sie unter [Informationen zu Einschränkungen](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="128e6-166">For information about how to use restrictions with tables, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="128e6-167">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="128e6-167">See also</span></span>



[<span data-ttu-id="128e6-168">SAndRestriction</span><span class="sxs-lookup"><span data-stu-id="128e6-168">SAndRestriction</span></span>](sandrestriction.md)
  
[<span data-ttu-id="128e6-169">SBitMaskRestriction</span><span class="sxs-lookup"><span data-stu-id="128e6-169">SBitMaskRestriction</span></span>](sbitmaskrestriction.md)
  
[<span data-ttu-id="128e6-170">SCommentRestriction</span><span class="sxs-lookup"><span data-stu-id="128e6-170">SCommentRestriction</span></span>](scommentrestriction.md)
  
[<span data-ttu-id="128e6-171">SComparePropsRestriction</span><span class="sxs-lookup"><span data-stu-id="128e6-171">SComparePropsRestriction</span></span>](scomparepropsrestriction.md)
  
[<span data-ttu-id="128e6-172">SContentRestriction</span><span class="sxs-lookup"><span data-stu-id="128e6-172">SContentRestriction</span></span>](scontentrestriction.md)
  
[<span data-ttu-id="128e6-173">SExistRestriction</span><span class="sxs-lookup"><span data-stu-id="128e6-173">SExistRestriction</span></span>](sexistrestriction.md)
  
[<span data-ttu-id="128e6-174">SNotRestriction</span><span class="sxs-lookup"><span data-stu-id="128e6-174">SNotRestriction</span></span>](snotrestriction.md)
  
[<span data-ttu-id="128e6-175">SOrRestriction</span><span class="sxs-lookup"><span data-stu-id="128e6-175">SOrRestriction</span></span>](sorrestriction.md)
  
[<span data-ttu-id="128e6-176">SPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="128e6-176">SPropertyRestriction</span></span>](spropertyrestriction.md)
  
[<span data-ttu-id="128e6-177">SSizeRestriction</span><span class="sxs-lookup"><span data-stu-id="128e6-177">SSizeRestriction</span></span>](ssizerestriction.md)
  
[<span data-ttu-id="128e6-178">SSubRestriction</span><span class="sxs-lookup"><span data-stu-id="128e6-178">SSubRestriction</span></span>](ssubrestriction.md)


[<span data-ttu-id="128e6-179">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="128e6-179">MAPI Structures</span></span>](mapi-structures.md)

