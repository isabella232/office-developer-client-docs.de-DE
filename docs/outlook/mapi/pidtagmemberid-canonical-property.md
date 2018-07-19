---
title: PidTagMemberId (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: ce6925f40e09261494e4edbcbd7314728debbe2b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794608"
---
# <a name="pidtagmemberid-canonical-property"></a><span data-ttu-id="98d1c-103">PidTagMemberId (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="98d1c-103">PidTagMemberId Canonical Property</span></span>

  
  
<span data-ttu-id="98d1c-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="98d1c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="98d1c-105">Enthält die ID eines Elements Tabelle, das die beschriebenen Rechte auf einem Microsoft Exchange Server-Ordner oder einem Postfach verfügt.</span><span class="sxs-lookup"><span data-stu-id="98d1c-105">Contains the identifier of a table member that has the described rights on a Microsoft Exchange Server folder or mailbox.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="98d1c-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="98d1c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="98d1c-107">PR_MEMBER_ID</span><span class="sxs-lookup"><span data-stu-id="98d1c-107">PR_MEMBER_ID</span></span>  <br/> |
|<span data-ttu-id="98d1c-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="98d1c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="98d1c-109">0x6671</span><span class="sxs-lookup"><span data-stu-id="98d1c-109">0x6671</span></span>  <br/> |
|<span data-ttu-id="98d1c-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="98d1c-110">Data type:</span></span>  <br/> |<span data-ttu-id="98d1c-111">PT_I8</span><span class="sxs-lookup"><span data-stu-id="98d1c-111">PT_I8</span></span>  <br/> |
|<span data-ttu-id="98d1c-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="98d1c-112">Area:</span></span>  <br/> |<span data-ttu-id="98d1c-113">Steuerung des Zugriffs</span><span class="sxs-lookup"><span data-stu-id="98d1c-113">Access Control</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="98d1c-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="98d1c-114">Remarks</span></span>

<span data-ttu-id="98d1c-115">Diese Eigenschaft gibt einen Bezeichner in der Tabelle eindeutig.</span><span class="sxs-lookup"><span data-stu-id="98d1c-115">This property returns an identifier unique to the table.</span></span> <span data-ttu-id="98d1c-116">Eine Directory-Benutzer-ID jedes Element-ID zugeordnet ist und von dieser Eigenschaft angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="98d1c-116">A directory user identifier is associated with each member identifier and is given by this property.</span></span> <span data-ttu-id="98d1c-117">Diese Eigenschaft wird von der [IExchangeModifyTable](iexchangemodifytableiunknown.md) -Schnittstelle verwendet, die Directory Eintrags-ID eines Elements mit expliziten Berechtigungen für einen Ordner abrufen.</span><span class="sxs-lookup"><span data-stu-id="98d1c-117">This property is used by the [IExchangeModifyTable](iexchangemodifytableiunknown.md) interface to retrieve the directory entry identifier of a member with explicit rights on a folder.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="98d1c-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="98d1c-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="98d1c-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="98d1c-119">Protocol specifications</span></span>

<span data-ttu-id="98d1c-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="98d1c-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="98d1c-121">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="98d1c-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="98d1c-122">[[MS-OXCPERM]](http://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="98d1c-122">[[MS-OXCPERM]](http://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="98d1c-123">Behandelt das Abrufen von Ordner Berechtigungslisten, die auf dem Server gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="98d1c-123">Handles the retrieval of folder permission lists that are stored on the server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="98d1c-124">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="98d1c-124">Header files</span></span>

<span data-ttu-id="98d1c-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="98d1c-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="98d1c-126">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="98d1c-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="98d1c-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="98d1c-127">Mapitags.h</span></span>
  
> <span data-ttu-id="98d1c-128">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="98d1c-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="98d1c-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="98d1c-129">See also</span></span>



[<span data-ttu-id="98d1c-130">PidTagMemberEntryId (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="98d1c-130">PidTagMemberEntryId Canonical Property</span></span>](pidtagmemberentryid-canonical-property.md)


[<span data-ttu-id="98d1c-131">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="98d1c-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="98d1c-132">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="98d1c-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="98d1c-133">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="98d1c-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="98d1c-134">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="98d1c-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

