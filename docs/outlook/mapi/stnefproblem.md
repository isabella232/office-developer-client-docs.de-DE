---
title: STnefProblem
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.STnefProblem
api_type:
- COM
ms.assetid: 3fe651b7-0ddf-42fd-8277-9224505be1a8
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 8595cdb411e68f2aed3ac063b2b81965e9b4d975
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795647"
---
# <a name="stnefproblem"></a><span data-ttu-id="88bd0-103">STnefProblem</span><span class="sxs-lookup"><span data-stu-id="88bd0-103">STnefProblem</span></span>

  
  
<span data-ttu-id="88bd0-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="88bd0-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="88bd0-105">Enthält Informationen zu einer Eigenschaft oder eines Attributs Verarbeitungsproblem, das in die Codierung oder Decodierung eines Streams Transport Neutral Encapsulation Format (TNEF) aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="88bd0-105">Contains information about a property or attribute processing problem that occurred during the encoding or decoding of a Transport Neutral Encapsulation Format (TNEF) stream.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="88bd0-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="88bd0-106">Header file:</span></span>  <br/> |<span data-ttu-id="88bd0-107">TNEF.h</span><span class="sxs-lookup"><span data-stu-id="88bd0-107">Tnef.h</span></span>  <br/> |
   
```cpp
typedef struct _STnefProblem
{
  ULONG ulComponent;
  ULONG ulAttribute;
  ULONG ulPropTag;
  SCODE scode;
} STnefProblem;

```

## <a name="members"></a><span data-ttu-id="88bd0-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="88bd0-108">Members</span></span>

 <span data-ttu-id="88bd0-109">**ulComponent**</span><span class="sxs-lookup"><span data-stu-id="88bd0-109">**ulComponent**</span></span>
  
> <span data-ttu-id="88bd0-110">Der Typ der Verarbeitung während der das Problem aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="88bd0-110">The type of processing during which the problem occurred.</span></span> <span data-ttu-id="88bd0-111">Wenn während der Verarbeitung das Problem aufgetreten ist, wird das Element **UlComponent** auf NULL gesetzt.</span><span class="sxs-lookup"><span data-stu-id="88bd0-111">If the problem occurred during message processing, the **ulComponent** member is set to zero.</span></span> <span data-ttu-id="88bd0-112">Wenn während der Verarbeitung von Anlagen das Problem aufgetreten ist, wird die **UlComponent** auf die entsprechende Anlage **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) Wert festgelegt.</span><span class="sxs-lookup"><span data-stu-id="88bd0-112">If the problem occurred during attachment processing, **ulComponent** is set equal to the corresponding attachment's **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) value.</span></span>
    
 <span data-ttu-id="88bd0-113">**ulAttribute**</span><span class="sxs-lookup"><span data-stu-id="88bd0-113">**ulAttribute**</span></span>
  
> <span data-ttu-id="88bd0-114">Attribut der Eigenschaft zugeordneten angegeben durch die **UlPropTag** Mitglied oder, wenn das TNEF Verarbeitungsproblem tritt auf, wenn eine Kapselung Decodierung zu blockieren, einen der folgenden Werte:</span><span class="sxs-lookup"><span data-stu-id="88bd0-114">Attribute associated with the property indicated by the **ulPropTag** member or, when the TNEF processing problem occurs when decoding an encapsulation block, one of the following values:</span></span> 
    
 <span data-ttu-id="88bd0-115">_attMAPIProps_</span><span class="sxs-lookup"><span data-stu-id="88bd0-115">_attMAPIProps_</span></span>
  
> <span data-ttu-id="88bd0-116">Nachrichtenebene</span><span class="sxs-lookup"><span data-stu-id="88bd0-116">Message level</span></span>
    
 <span data-ttu-id="88bd0-117">_attAttachment_</span><span class="sxs-lookup"><span data-stu-id="88bd0-117">_attAttachment_</span></span>
  
> <span data-ttu-id="88bd0-118">Anlage-Ebene</span><span class="sxs-lookup"><span data-stu-id="88bd0-118">Attachment level</span></span>
    
 <span data-ttu-id="88bd0-119">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="88bd0-119">**ulPropTag**</span></span>
  
> <span data-ttu-id="88bd0-120">Eigenschaftentag der Eigenschaft, die Ursache für das Problem der TNEF-Verarbeitung, außer wenn das Problem auftritt, wenn einen Block Encapsulation Decodierung in dem Groß-/Kleinschreibung **UlPropTag** auf 0 (null) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="88bd0-120">Property tag of the property that caused the TNEF processing problem, except when the problem occurs when decoding an encapsulation block, in which case **ulPropTag** is set to zero.</span></span> 
    
 <span data-ttu-id="88bd0-121">**SCODE**</span><span class="sxs-lookup"><span data-stu-id="88bd0-121">**scode**</span></span>
  
> <span data-ttu-id="88bd0-122">Fehler-Wert zurück, der das Problem aufgetreten ist, während der Verarbeitung angibt.</span><span class="sxs-lookup"><span data-stu-id="88bd0-122">Error value indicating the problem encountered during processing.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="88bd0-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="88bd0-123">Remarks</span></span>

<span data-ttu-id="88bd0-124">Wenn eine Struktur **STnefProblem** während der Verarbeitung eines Attribut oder Eigenschaft nicht generiert wird, kann die Anwendung unter der Annahme fortgesetzt, die die Verarbeitung dieses Attribut oder Eigenschaft erfolgreich waren.</span><span class="sxs-lookup"><span data-stu-id="88bd0-124">If an **STnefProblem** structure is not generated during the processing of an attribute or property, the application can continue under the assumption that the processing of that attribute or property succeeded.</span></span> <span data-ttu-id="88bd0-125">Die einzige Ausnahme tritt auf, wenn das Problem aufgetreten ist, während der Decodierung eines Blocks Kapselung.</span><span class="sxs-lookup"><span data-stu-id="88bd0-125">The only exception occurs when the problem arose during decoding of an encapsulation block.</span></span> <span data-ttu-id="88bd0-126">In diesem Fall die Decodierung der die entsprechende Komponente für den Block wird angehalten und der Decodierung in einer anderen Komponente fortgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="88bd0-126">In this case, the decoding of the component corresponding to the block is stopped and decoding is continued in another component.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="88bd0-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="88bd0-127">See also</span></span>



[<span data-ttu-id="88bd0-128">STnefProblemArray</span><span class="sxs-lookup"><span data-stu-id="88bd0-128">STnefProblemArray</span></span>](stnefproblemarray.md)
  
[<span data-ttu-id="88bd0-129">PidTagAttachNumber (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="88bd0-129">PidTagAttachNumber Canonical Property</span></span>](pidtagattachnumber-canonical-property.md)


[<span data-ttu-id="88bd0-130">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="88bd0-130">MAPI Structures</span></span>](mapi-structures.md)

