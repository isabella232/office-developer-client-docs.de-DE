---
title: Kanonische PidTagMemberId-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMemberId
api_type:
- HeaderDef
ms.assetid: 64faef3c-27b2-49d2-9d0c-8b9d33f1cb71
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: ce6925f40e09261494e4edbcbd7314728debbe2b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794608"
---
# <a name="pidtagmemberid-canonical-property"></a><span data-ttu-id="e210d-103">Kanonische PidTagMemberId-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="e210d-103">PidTagMemberId Canonical Property</span></span>

  
  
<span data-ttu-id="e210d-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e210d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e210d-105">Enthält die ID eines Elements Tabelle, das die beschriebenen Rechte auf einem Microsoft Exchange Server-Ordner oder einem Postfach verfügt.</span><span class="sxs-lookup"><span data-stu-id="e210d-105">Contains the identifier of a table member that has the described rights on a Microsoft Exchange Server folder or mailbox.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e210d-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="e210d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e210d-107">PR_MEMBER_ID</span><span class="sxs-lookup"><span data-stu-id="e210d-107">PR_MEMBER_ID</span></span>  <br/> |
|<span data-ttu-id="e210d-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="e210d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e210d-109">0x6671</span><span class="sxs-lookup"><span data-stu-id="e210d-109">0x6671</span></span>  <br/> |
|<span data-ttu-id="e210d-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="e210d-110">Data type:</span></span>  <br/> |<span data-ttu-id="e210d-111">PT_I8</span><span class="sxs-lookup"><span data-stu-id="e210d-111">PT_I8</span></span>  <br/> |
|<span data-ttu-id="e210d-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="e210d-112">Area:</span></span>  <br/> |<span data-ttu-id="e210d-113">Steuerung des Zugriffs</span><span class="sxs-lookup"><span data-stu-id="e210d-113">Access Control</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e210d-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e210d-114">Remarks</span></span>

<span data-ttu-id="e210d-115">Diese Eigenschaft gibt einen Bezeichner in der Tabelle eindeutig.</span><span class="sxs-lookup"><span data-stu-id="e210d-115">This property returns an identifier unique to the table.</span></span> <span data-ttu-id="e210d-116">Eine Directory-Benutzer-ID jedes Element-ID zugeordnet ist und von dieser Eigenschaft angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="e210d-116">A directory user identifier is associated with each member identifier and is given by this property.</span></span> <span data-ttu-id="e210d-117">Diese Eigenschaft wird von der [IExchangeModifyTable](iexchangemodifytableiunknown.md) -Schnittstelle verwendet, die Directory Eintrags-ID eines Elements mit expliziten Berechtigungen für einen Ordner abrufen.</span><span class="sxs-lookup"><span data-stu-id="e210d-117">This property is used by the [IExchangeModifyTable](iexchangemodifytableiunknown.md) interface to retrieve the directory entry identifier of a member with explicit rights on a folder.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="e210d-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="e210d-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e210d-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="e210d-119">Protocol specifications</span></span>

<span data-ttu-id="e210d-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e210d-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e210d-121">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="e210d-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e210d-122">[[MS-OXCPERM]](http://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e210d-122">[[MS-OXCPERM]](http://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e210d-123">Behandelt das Abrufen von Ordner Berechtigungslisten, die auf dem Server gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="e210d-123">Handles the retrieval of folder permission lists that are stored on the server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e210d-124">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="e210d-124">Header files</span></span>

<span data-ttu-id="e210d-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e210d-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="e210d-126">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="e210d-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="e210d-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e210d-127">Mapitags.h</span></span>
  
> <span data-ttu-id="e210d-128">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="e210d-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e210d-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e210d-129">See also</span></span>



[<span data-ttu-id="e210d-130">Kanonische PidTagMemberEntryId-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="e210d-130">PidTagMemberEntryId Canonical Property</span></span>](pidtagmemberentryid-canonical-property.md)


[<span data-ttu-id="e210d-131">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e210d-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e210d-132">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e210d-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e210d-133">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="e210d-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e210d-134">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="e210d-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

