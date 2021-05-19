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
ms.openlocfilehash: 0ab904625d3a23462a4fedf3b64f49c54b34ad28
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357904"
---
# <a name="pidtagdefaultpostmessageclass-canonical-property"></a><span data-ttu-id="a8e65-103">PidTagDefaultPostMessageClass (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="a8e65-103">PidTagDefaultPostMessageClass Canonical Property</span></span>

  
  
<span data-ttu-id="a8e65-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a8e65-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a8e65-105">Enthält den Namen einer benutzerdefinierten Form Nachrichtenklasse.</span><span class="sxs-lookup"><span data-stu-id="a8e65-105">Contains the name of a custom form Message class.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a8e65-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="a8e65-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a8e65-107">PR_DEF_POST_MSGCLASS</span><span class="sxs-lookup"><span data-stu-id="a8e65-107">PR_DEF_POST_MSGCLASS</span></span>  <br/> |
|<span data-ttu-id="a8e65-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="a8e65-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a8e65-109">0x36E5</span><span class="sxs-lookup"><span data-stu-id="a8e65-109">0x36E5</span></span>  <br/> |
|<span data-ttu-id="a8e65-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="a8e65-110">Data type:</span></span>  <br/> |<span data-ttu-id="a8e65-111">PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="a8e65-111">PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="a8e65-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="a8e65-112">Area:</span></span>  <br/> |<span data-ttu-id="a8e65-113">MAPI-Container</span><span class="sxs-lookup"><span data-stu-id="a8e65-113">MAPI container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a8e65-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a8e65-114">Remarks</span></span>

<span data-ttu-id="a8e65-115">Wenn diese Eigenschaft für einen Ordner festgelegt ist, muss der Wert entweder genau die Basisnachrichtenklasse enthalten (z. B. "IPM. Contact" für einen Kontaktordner oder "IPM. Appointment" für einen Kalenderordner) oder mit der Basisnachrichtenklasse beginnen (z. B. "IPM. Contact.MyContact").</span><span class="sxs-lookup"><span data-stu-id="a8e65-115">If this property is set on a folder, the value must contain either exactly the base message class (for example, "IPM.Contact" for a contacts folder or "IPM.Appointment" for a calendar folder), or begin with the base message class (for example, "IPM.Contact.MyContact").</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="a8e65-116">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="a8e65-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a8e65-117">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="a8e65-117">Protocol specifications</span></span>

<span data-ttu-id="a8e65-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a8e65-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a8e65-119">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="a8e65-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a8e65-120">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a8e65-120">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a8e65-121">Gibt die Eigenschaften und Vorgänge für Termin-, Besprechungs- und Antwortnachrichten an.</span><span class="sxs-lookup"><span data-stu-id="a8e65-121">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a8e65-122">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="a8e65-122">Header files</span></span>

<span data-ttu-id="a8e65-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a8e65-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="a8e65-124">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="a8e65-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="a8e65-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a8e65-125">Mapitags.h</span></span>
  
> <span data-ttu-id="a8e65-126">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="a8e65-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a8e65-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a8e65-127">See also</span></span>



[<span data-ttu-id="a8e65-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a8e65-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a8e65-129">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="a8e65-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a8e65-130">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="a8e65-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a8e65-131">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="a8e65-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

