---
title: Kanonische Pidtagmembername (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMemberName
api_type:
- HeaderDef
ms.assetid: e19129bf-d07c-4d2e-9d4d-edbfda088ea7
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: a119cf1446600153e433c4aae99037d9810015c0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342483"
---
# <a name="pidtagmembername-canonical-property"></a><span data-ttu-id="cc790-103">Kanonische Pidtagmembername (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="cc790-103">PidTagMemberName Canonical Property</span></span>

  
  
<span data-ttu-id="cc790-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cc790-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cc790-105">Enthält den Anzeigenamen eines Members der ACL-Tabelle (Access Control List).</span><span class="sxs-lookup"><span data-stu-id="cc790-105">Contains the display name of a member of the access control list (ACL) table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="cc790-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="cc790-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="cc790-107">PR_MEMBER_NAME, PR_MEMBER_NAME_A, PR_MEMBER_NAME_W</span><span class="sxs-lookup"><span data-stu-id="cc790-107">PR_MEMBER_NAME, PR_MEMBER_NAME_A, PR_MEMBER_NAME_W</span></span>  <br/> |
|<span data-ttu-id="cc790-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="cc790-108">Identifier:</span></span>  <br/> |<span data-ttu-id="cc790-109">0x6672</span><span class="sxs-lookup"><span data-stu-id="cc790-109">0x6672</span></span>  <br/> |
|<span data-ttu-id="cc790-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="cc790-110">Data type:</span></span>  <br/> |<span data-ttu-id="cc790-111">PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="cc790-111">PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="cc790-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="cc790-112">Area:</span></span>  <br/> |<span data-ttu-id="cc790-113">Zugriffssteuerung</span><span class="sxs-lookup"><span data-stu-id="cc790-113">Access Control</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cc790-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cc790-114">Remarks</span></span>

<span data-ttu-id="cc790-115">Diese Eigenschaften werden von der [IExchangeModifyTable: IUnknown](iexchangemodifytableiunknown.md) -Schnittstelle verwendet, um den Namen eines Members einer ACL-Tabelle anzuzeigen, bei dem es sich um eine Person oder Rolle mit expliziten rechten für einen Ordner oder ein Postfach handelt.</span><span class="sxs-lookup"><span data-stu-id="cc790-115">These properties are used by the [IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md) interface to display the name of a member of an ACL table, which is a person or role with explicit rights on a folder or mailbox.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="cc790-116">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="cc790-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="cc790-117">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="cc790-117">Protocol specifications</span></span>

<span data-ttu-id="cc790-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cc790-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cc790-119">Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="cc790-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="cc790-120">[[MS-OXCPERM]](https://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cc790-120">[[MS-OXCPERM]](https://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cc790-121">Behandelt das Abrufen von Ordner Berechtigungslisten, die auf dem Server gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="cc790-121">Handles the retrieval of folder permission lists that are stored on the server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="cc790-122">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="cc790-122">Header files</span></span>

<span data-ttu-id="cc790-123">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="cc790-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="cc790-124">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="cc790-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="cc790-125">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="cc790-125">Mapitags.h</span></span>
  
> <span data-ttu-id="cc790-126">Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="cc790-126">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="cc790-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cc790-127">See also</span></span>



[<span data-ttu-id="cc790-128">IExchangeModifyTable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="cc790-128">IExchangeModifyTable : IUnknown</span></span>](iexchangemodifytableiunknown.md)


[<span data-ttu-id="cc790-129">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="cc790-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="cc790-130">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="cc790-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="cc790-131">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="cc790-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="cc790-132">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="cc790-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

