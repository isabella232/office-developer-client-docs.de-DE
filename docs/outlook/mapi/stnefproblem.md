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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 90829f8fff530d22a7dee68dc227655064147cee
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575329"
---
# <a name="stnefproblem"></a><span data-ttu-id="39004-103">STnefProblem</span><span class="sxs-lookup"><span data-stu-id="39004-103">STnefProblem</span></span>

  
  
<span data-ttu-id="39004-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="39004-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="39004-105">Enthält Informationen zu einer Eigenschaft oder eines Attributs Verarbeitungsproblem, das in die Codierung oder Decodierung eines Streams Transport Neutral Encapsulation Format (TNEF) aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="39004-105">Contains information about a property or attribute processing problem that occurred during the encoding or decoding of a Transport Neutral Encapsulation Format (TNEF) stream.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="39004-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="39004-106">Header file:</span></span>  <br/> |<span data-ttu-id="39004-107">TNEF.h</span><span class="sxs-lookup"><span data-stu-id="39004-107">Tnef.h</span></span>  <br/> |
   
```cpp
typedef struct _STnefProblem
{
  ULONG ulComponent;
  ULONG ulAttribute;
  ULONG ulPropTag;
  SCODE scode;
} STnefProblem;

```

## <a name="members"></a><span data-ttu-id="39004-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="39004-108">Members</span></span>

 <span data-ttu-id="39004-109">**ulComponent**</span><span class="sxs-lookup"><span data-stu-id="39004-109">**ulComponent**</span></span>
  
> <span data-ttu-id="39004-110">Der Typ der Verarbeitung während der das Problem aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="39004-110">The type of processing during which the problem occurred.</span></span> <span data-ttu-id="39004-111">Wenn während der Verarbeitung das Problem aufgetreten ist, wird das Element **UlComponent** auf NULL gesetzt.</span><span class="sxs-lookup"><span data-stu-id="39004-111">If the problem occurred during message processing, the **ulComponent** member is set to zero.</span></span> <span data-ttu-id="39004-112">Wenn während der Verarbeitung von Anlagen das Problem aufgetreten ist, wird die **UlComponent** auf die entsprechende Anlage **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) Wert festgelegt.</span><span class="sxs-lookup"><span data-stu-id="39004-112">If the problem occurred during attachment processing, **ulComponent** is set equal to the corresponding attachment's **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) value.</span></span>
    
 <span data-ttu-id="39004-113">**ulAttribute**</span><span class="sxs-lookup"><span data-stu-id="39004-113">**ulAttribute**</span></span>
  
> <span data-ttu-id="39004-114">Attribut der Eigenschaft zugeordneten angegeben durch die **UlPropTag** Mitglied oder, wenn das TNEF Verarbeitungsproblem tritt auf, wenn eine Kapselung Decodierung zu blockieren, einen der folgenden Werte:</span><span class="sxs-lookup"><span data-stu-id="39004-114">Attribute associated with the property indicated by the **ulPropTag** member or, when the TNEF processing problem occurs when decoding an encapsulation block, one of the following values:</span></span> 
    
 <span data-ttu-id="39004-115">_attMAPIProps_</span><span class="sxs-lookup"><span data-stu-id="39004-115">_attMAPIProps_</span></span>
  
> <span data-ttu-id="39004-116">Nachrichtenebene</span><span class="sxs-lookup"><span data-stu-id="39004-116">Message level</span></span>
    
 <span data-ttu-id="39004-117">_attAttachment_</span><span class="sxs-lookup"><span data-stu-id="39004-117">_attAttachment_</span></span>
  
> <span data-ttu-id="39004-118">Anlage-Ebene</span><span class="sxs-lookup"><span data-stu-id="39004-118">Attachment level</span></span>
    
 <span data-ttu-id="39004-119">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="39004-119">**ulPropTag**</span></span>
  
> <span data-ttu-id="39004-120">Eigenschaftentag der Eigenschaft, die Ursache für das Problem der TNEF-Verarbeitung, außer wenn das Problem auftritt, wenn einen Block Encapsulation Decodierung in dem Groß-/Kleinschreibung **UlPropTag** auf 0 (null) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="39004-120">Property tag of the property that caused the TNEF processing problem, except when the problem occurs when decoding an encapsulation block, in which case **ulPropTag** is set to zero.</span></span> 
    
 <span data-ttu-id="39004-121">**SCODE**</span><span class="sxs-lookup"><span data-stu-id="39004-121">**scode**</span></span>
  
> <span data-ttu-id="39004-122">Fehler-Wert zurück, der das Problem aufgetreten ist, während der Verarbeitung angibt.</span><span class="sxs-lookup"><span data-stu-id="39004-122">Error value indicating the problem encountered during processing.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="39004-123">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="39004-123">Remarks</span></span>

<span data-ttu-id="39004-124">Wenn eine Struktur **STnefProblem** während der Verarbeitung eines Attribut oder Eigenschaft nicht generiert wird, kann die Anwendung unter der Annahme fortgesetzt, die die Verarbeitung dieses Attribut oder Eigenschaft erfolgreich waren.</span><span class="sxs-lookup"><span data-stu-id="39004-124">If an **STnefProblem** structure is not generated during the processing of an attribute or property, the application can continue under the assumption that the processing of that attribute or property succeeded.</span></span> <span data-ttu-id="39004-125">Die einzige Ausnahme tritt auf, wenn das Problem aufgetreten ist, während der Decodierung eines Blocks Kapselung.</span><span class="sxs-lookup"><span data-stu-id="39004-125">The only exception occurs when the problem arose during decoding of an encapsulation block.</span></span> <span data-ttu-id="39004-126">In diesem Fall die Decodierung der die entsprechende Komponente für den Block wird angehalten und der Decodierung in einer anderen Komponente fortgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="39004-126">In this case, the decoding of the component corresponding to the block is stopped and decoding is continued in another component.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="39004-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="39004-127">See also</span></span>



[<span data-ttu-id="39004-128">STnefProblemArray</span><span class="sxs-lookup"><span data-stu-id="39004-128">STnefProblemArray</span></span>](stnefproblemarray.md)
  
[<span data-ttu-id="39004-129">PidTagAttachNumber (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="39004-129">PidTagAttachNumber Canonical Property</span></span>](pidtagattachnumber-canonical-property.md)


[<span data-ttu-id="39004-130">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="39004-130">MAPI Structures</span></span>](mapi-structures.md)

