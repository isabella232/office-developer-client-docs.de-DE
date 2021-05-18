---
title: PidTagRowid (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRowid
api_type:
- COM
ms.assetid: 0fdcb55a-2971-4c7d-b61e-7ada2d19d0e6
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 8d58342e0460352bd9d260cb6e73de358cb2fc23
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359535"
---
# <a name="pidtagrowid-canonical-property"></a><span data-ttu-id="a47ee-103">PidTagRowid (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="a47ee-103">PidTagRowid Canonical Property</span></span>

  
  
<span data-ttu-id="a47ee-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a47ee-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a47ee-105">Enthält einen eindeutigen Bezeichner für einen Empfänger in einer Empfängertabelle oder Statustabelle.</span><span class="sxs-lookup"><span data-stu-id="a47ee-105">Contains a unique identifier for a recipient in a recipient table or status table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a47ee-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="a47ee-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a47ee-107">PR_ROWID</span><span class="sxs-lookup"><span data-stu-id="a47ee-107">PR_ROWID</span></span>  <br/> |
|<span data-ttu-id="a47ee-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="a47ee-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a47ee-109">0x3000</span><span class="sxs-lookup"><span data-stu-id="a47ee-109">0x3000</span></span>  <br/> |
|<span data-ttu-id="a47ee-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="a47ee-110">Data type:</span></span>  <br/> |<span data-ttu-id="a47ee-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="a47ee-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="a47ee-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="a47ee-112">Area:</span></span>  <br/> |<span data-ttu-id="a47ee-113">MAPI allgemein</span><span class="sxs-lookup"><span data-stu-id="a47ee-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a47ee-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a47ee-114">Remarks</span></span>

<span data-ttu-id="a47ee-115">Diese Eigenschaft ist ein temporärer Wert, der nur für die Lebensdauer des Objekts gilt, das die Tabelle besitzt.</span><span class="sxs-lookup"><span data-stu-id="a47ee-115">This property is a temporary value that is valid only for the life of the object that owns the table.</span></span> <span data-ttu-id="a47ee-116">Es wird als Spalte der Tabelle angezeigt, aber nicht gespeichert.</span><span class="sxs-lookup"><span data-stu-id="a47ee-116">It appears as a column of the table but is not stored.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="a47ee-117">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="a47ee-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a47ee-118">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="a47ee-118">Protocol specifications</span></span>

<span data-ttu-id="a47ee-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a47ee-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a47ee-120">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="a47ee-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a47ee-121">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a47ee-121">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a47ee-122">Verarbeitet die Reihenfolge und den Fluss für Datenübertragungen zwischen einem Client und einem Server.</span><span class="sxs-lookup"><span data-stu-id="a47ee-122">Handles the order and flow for data transfers between a client and server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a47ee-123">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="a47ee-123">Header files</span></span>

<span data-ttu-id="a47ee-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a47ee-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="a47ee-125">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="a47ee-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="a47ee-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a47ee-126">Mapitags.h</span></span>
  
> <span data-ttu-id="a47ee-127">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="a47ee-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a47ee-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a47ee-128">See also</span></span>



[<span data-ttu-id="a47ee-129">IMessage::GetRecipientTable</span><span class="sxs-lookup"><span data-stu-id="a47ee-129">IMessage::GetRecipientTable</span></span>](imessage-getrecipienttable.md)
  
[<span data-ttu-id="a47ee-130">IMessage::ModifyRecipients</span><span class="sxs-lookup"><span data-stu-id="a47ee-130">IMessage::ModifyRecipients</span></span>](imessage-modifyrecipients.md)


[<span data-ttu-id="a47ee-131">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a47ee-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a47ee-132">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="a47ee-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a47ee-133">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="a47ee-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a47ee-134">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="a47ee-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

