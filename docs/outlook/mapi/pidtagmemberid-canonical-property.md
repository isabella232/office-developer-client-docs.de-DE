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
ms.openlocfilehash: b5d1d4456856f1640bbed8589fc0583060cd2520
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342637"
---
# <a name="pidtagmemberid-canonical-property"></a><span data-ttu-id="48c1d-103">PidTagMemberId (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="48c1d-103">PidTagMemberId Canonical Property</span></span>

  
  
<span data-ttu-id="48c1d-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="48c1d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="48c1d-105">Enthält den Bezeichner eines Tabellenmitglieds, das über die beschriebenen Rechte für Microsoft Exchange Server oder Postfach verfügt.</span><span class="sxs-lookup"><span data-stu-id="48c1d-105">Contains the identifier of a table member that has the described rights on a Microsoft Exchange Server folder or mailbox.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="48c1d-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="48c1d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="48c1d-107">PR_MEMBER_ID</span><span class="sxs-lookup"><span data-stu-id="48c1d-107">PR_MEMBER_ID</span></span>  <br/> |
|<span data-ttu-id="48c1d-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="48c1d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="48c1d-109">0x6671</span><span class="sxs-lookup"><span data-stu-id="48c1d-109">0x6671</span></span>  <br/> |
|<span data-ttu-id="48c1d-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="48c1d-110">Data type:</span></span>  <br/> |<span data-ttu-id="48c1d-111">PT_I8</span><span class="sxs-lookup"><span data-stu-id="48c1d-111">PT_I8</span></span>  <br/> |
|<span data-ttu-id="48c1d-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="48c1d-112">Area:</span></span>  <br/> |<span data-ttu-id="48c1d-113">Zugriffssteuerung</span><span class="sxs-lookup"><span data-stu-id="48c1d-113">Access Control</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="48c1d-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="48c1d-114">Remarks</span></span>

<span data-ttu-id="48c1d-115">Diese Eigenschaft gibt einen bezeichner zurück, der für die Tabelle eindeutig ist.</span><span class="sxs-lookup"><span data-stu-id="48c1d-115">This property returns an identifier unique to the table.</span></span> <span data-ttu-id="48c1d-116">Jeder Element-ID ist ein Verzeichnisbenutzerbezeichner zugeordnet, der von dieser Eigenschaft angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="48c1d-116">A directory user identifier is associated with each member identifier and is given by this property.</span></span> <span data-ttu-id="48c1d-117">Diese Eigenschaft wird von der [IExchangeModifyTable-Schnittstelle](iexchangemodifytableiunknown.md) verwendet, um die Verzeichniseintrags-ID eines Mitglieds mit expliziten Rechten für einen Ordner abzurufen.</span><span class="sxs-lookup"><span data-stu-id="48c1d-117">This property is used by the [IExchangeModifyTable](iexchangemodifytableiunknown.md) interface to retrieve the directory entry identifier of a member with explicit rights on a folder.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="48c1d-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="48c1d-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="48c1d-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="48c1d-119">Protocol specifications</span></span>

<span data-ttu-id="48c1d-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="48c1d-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="48c1d-121">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="48c1d-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="48c1d-122">[[MS-OXCPERM]](https://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="48c1d-122">[[MS-OXCPERM]](https://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="48c1d-123">Behandelt das Abrufen von Ordnerberechtigungslisten, die auf dem Server gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="48c1d-123">Handles the retrieval of folder permission lists that are stored on the server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="48c1d-124">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="48c1d-124">Header files</span></span>

<span data-ttu-id="48c1d-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="48c1d-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="48c1d-126">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="48c1d-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="48c1d-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="48c1d-127">Mapitags.h</span></span>
  
> <span data-ttu-id="48c1d-128">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="48c1d-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="48c1d-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="48c1d-129">See also</span></span>



[<span data-ttu-id="48c1d-130">PidTagMemberEntryId (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="48c1d-130">PidTagMemberEntryId Canonical Property</span></span>](pidtagmemberentryid-canonical-property.md)


[<span data-ttu-id="48c1d-131">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="48c1d-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="48c1d-132">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="48c1d-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="48c1d-133">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="48c1d-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="48c1d-134">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="48c1d-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

