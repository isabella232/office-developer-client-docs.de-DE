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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 2b4013b311289816f778d7559ee3bcc7dc061538
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574335"
---
# <a name="pidtagdefaultpostmessageclass-canonical-property"></a><span data-ttu-id="eaf85-103">PidTagDefaultPostMessageClass (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="eaf85-103">PidTagDefaultPostMessageClass Canonical Property</span></span>

  
  
<span data-ttu-id="eaf85-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="eaf85-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="eaf85-105">Enthält den Namen eines benutzerdefinierten Formulars Nachrichtenklasse.</span><span class="sxs-lookup"><span data-stu-id="eaf85-105">Contains the name of a custom form Message class.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="eaf85-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="eaf85-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="eaf85-107">PR_DEF_POST_MSGCLASS</span><span class="sxs-lookup"><span data-stu-id="eaf85-107">PR_DEF_POST_MSGCLASS</span></span>  <br/> |
|<span data-ttu-id="eaf85-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="eaf85-108">Identifier:</span></span>  <br/> |<span data-ttu-id="eaf85-109">0x36E5</span><span class="sxs-lookup"><span data-stu-id="eaf85-109">0x36E5</span></span>  <br/> |
|<span data-ttu-id="eaf85-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="eaf85-110">Data type:</span></span>  <br/> |<span data-ttu-id="eaf85-111">PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="eaf85-111">PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="eaf85-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="eaf85-112">Area:</span></span>  <br/> |<span data-ttu-id="eaf85-113">MAPI-container</span><span class="sxs-lookup"><span data-stu-id="eaf85-113">MAPI container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="eaf85-114">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="eaf85-114">Remarks</span></span>

<span data-ttu-id="eaf85-115">Wenn diese Eigenschaft auf einen Ordner festgelegt ist, muss der Wert enthalten entweder genau Basisnachrichtenklasse (z. B. "IPM. Kontakt"für einen Ordner" Kontakte "oder"IPM. Termin"für einen Kalenderordner), oder Sie zunächst die Basisnachrichtenklasse (z. B." IPM. Contact.MyContact").</span><span class="sxs-lookup"><span data-stu-id="eaf85-115">If this property is set on a folder, the value must contain either exactly the base message class (for example, "IPM.Contact" for a contacts folder or "IPM.Appointment" for a calendar folder), or begin with the base message class (for example, "IPM.Contact.MyContact").</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="eaf85-116">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="eaf85-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="eaf85-117">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="eaf85-117">Protocol specifications</span></span>

<span data-ttu-id="eaf85-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="eaf85-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="eaf85-119">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="eaf85-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="eaf85-120">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="eaf85-120">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="eaf85-121">Gibt die Eigenschaften und Vorgänge für den Termin, einer Besprechungsanfrage und Antwortnachrichten.</span><span class="sxs-lookup"><span data-stu-id="eaf85-121">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="eaf85-122">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="eaf85-122">Header files</span></span>

<span data-ttu-id="eaf85-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="eaf85-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="eaf85-124">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="eaf85-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="eaf85-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="eaf85-125">Mapitags.h</span></span>
  
> <span data-ttu-id="eaf85-126">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="eaf85-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="eaf85-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eaf85-127">See also</span></span>



[<span data-ttu-id="eaf85-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="eaf85-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="eaf85-129">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="eaf85-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="eaf85-130">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="eaf85-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="eaf85-131">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="eaf85-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

