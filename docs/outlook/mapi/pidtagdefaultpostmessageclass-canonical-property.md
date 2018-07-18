---
title: PidTagDefaultPostMessageClass (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDefaultPostMessageClass
api_type:
- HeaderDef
ms.assetid: 231c288f-547b-4463-9442-1499661b925e
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 538cc7cdc6dcb281beead6d06ff8644c534ed569
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794271"
---
# <a name="pidtagdefaultpostmessageclass-canonical-property"></a><span data-ttu-id="a9ac3-103">PidTagDefaultPostMessageClass (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="a9ac3-103">PidTagDefaultPostMessageClass Canonical Property</span></span>

  
  
<span data-ttu-id="a9ac3-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a9ac3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a9ac3-105">Enthält den Namen eines benutzerdefinierten Formulars Nachrichtenklasse.</span><span class="sxs-lookup"><span data-stu-id="a9ac3-105">Contains the name of a custom form Message class.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a9ac3-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="a9ac3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a9ac3-107">PR_DEF_POST_MSGCLASS</span><span class="sxs-lookup"><span data-stu-id="a9ac3-107">PR_DEF_POST_MSGCLASS</span></span>  <br/> |
|<span data-ttu-id="a9ac3-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="a9ac3-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a9ac3-109">0x36E5</span><span class="sxs-lookup"><span data-stu-id="a9ac3-109">0x36E5</span></span>  <br/> |
|<span data-ttu-id="a9ac3-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="a9ac3-110">Data type:</span></span>  <br/> |<span data-ttu-id="a9ac3-111">PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="a9ac3-111">PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="a9ac3-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="a9ac3-112">Area:</span></span>  <br/> |<span data-ttu-id="a9ac3-113">MAPI-container</span><span class="sxs-lookup"><span data-stu-id="a9ac3-113">MAPI container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a9ac3-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a9ac3-114">Remarks</span></span>

<span data-ttu-id="a9ac3-115">Wenn diese Eigenschaft auf einen Ordner festgelegt ist, muss der Wert enthalten entweder genau Basisnachrichtenklasse (z. B. "IPM. Kontakt"für einen Ordner" Kontakte "oder"IPM. Termin"für einen Kalenderordner), oder Sie zunächst die Basisnachrichtenklasse (z. B." IPM. Contact.MyContact").</span><span class="sxs-lookup"><span data-stu-id="a9ac3-115">If this property is set on a folder, the value must contain either exactly the base message class (for example, "IPM.Contact" for a contacts folder or "IPM.Appointment" for a calendar folder), or begin with the base message class (for example, "IPM.Contact.MyContact").</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="a9ac3-116">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="a9ac3-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a9ac3-117">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="a9ac3-117">Protocol specifications</span></span>

<span data-ttu-id="a9ac3-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a9ac3-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a9ac3-119">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="a9ac3-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a9ac3-120">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a9ac3-120">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a9ac3-121">Gibt die Eigenschaften und Vorgänge für den Termin, einer Besprechungsanfrage und Antwortnachrichten.</span><span class="sxs-lookup"><span data-stu-id="a9ac3-121">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a9ac3-122">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="a9ac3-122">Header files</span></span>

<span data-ttu-id="a9ac3-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a9ac3-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="a9ac3-124">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="a9ac3-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="a9ac3-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a9ac3-125">Mapitags.h</span></span>
  
> <span data-ttu-id="a9ac3-126">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="a9ac3-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a9ac3-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a9ac3-127">See also</span></span>



[<span data-ttu-id="a9ac3-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a9ac3-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a9ac3-129">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a9ac3-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a9ac3-130">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="a9ac3-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a9ac3-131">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="a9ac3-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

