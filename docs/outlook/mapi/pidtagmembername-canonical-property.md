---
title: PidTagMemberName (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: a119cf1446600153e433c4aae99037d9810015c0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342483"
---
# <a name="pidtagmembername-canonical-property"></a><span data-ttu-id="f4d0e-103">PidTagMemberName (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="f4d0e-103">PidTagMemberName Canonical Property</span></span>

  
  
<span data-ttu-id="f4d0e-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f4d0e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f4d0e-105">Enthält den Anzeigenamen eines Mitglieds der Zugriffssteuerungsliste (Access Control List, ACL).</span><span class="sxs-lookup"><span data-stu-id="f4d0e-105">Contains the display name of a member of the access control list (ACL) table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f4d0e-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="f4d0e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f4d0e-107">PR_MEMBER_NAME, PR_MEMBER_NAME_A, PR_MEMBER_NAME_W</span><span class="sxs-lookup"><span data-stu-id="f4d0e-107">PR_MEMBER_NAME, PR_MEMBER_NAME_A, PR_MEMBER_NAME_W</span></span>  <br/> |
|<span data-ttu-id="f4d0e-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="f4d0e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f4d0e-109">0x6672</span><span class="sxs-lookup"><span data-stu-id="f4d0e-109">0x6672</span></span>  <br/> |
|<span data-ttu-id="f4d0e-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="f4d0e-110">Data type:</span></span>  <br/> |<span data-ttu-id="f4d0e-111">PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="f4d0e-111">PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="f4d0e-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="f4d0e-112">Area:</span></span>  <br/> |<span data-ttu-id="f4d0e-113">Zugriffssteuerung</span><span class="sxs-lookup"><span data-stu-id="f4d0e-113">Access Control</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f4d0e-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f4d0e-114">Remarks</span></span>

<span data-ttu-id="f4d0e-115">Diese Eigenschaften werden von der [IExchangeModifyTable : IUnknown-Schnittstelle](iexchangemodifytableiunknown.md) zum Anzeigen des Namens eines Mitglieds einer ACL-Tabelle verwendet, bei der es sich um eine Person oder Rolle mit expliziten Rechten für einen Ordner oder ein Postfach handelt.</span><span class="sxs-lookup"><span data-stu-id="f4d0e-115">These properties are used by the [IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md) interface to display the name of a member of an ACL table, which is a person or role with explicit rights on a folder or mailbox.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="f4d0e-116">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="f4d0e-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f4d0e-117">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="f4d0e-117">Protocol specifications</span></span>

<span data-ttu-id="f4d0e-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f4d0e-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f4d0e-119">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="f4d0e-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f4d0e-120">[[MS-OXCPERM]](https://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f4d0e-120">[[MS-OXCPERM]](https://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f4d0e-121">Behandelt das Abrufen von Ordnerberechtigungslisten, die auf dem Server gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="f4d0e-121">Handles the retrieval of folder permission lists that are stored on the server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f4d0e-122">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="f4d0e-122">Header files</span></span>

<span data-ttu-id="f4d0e-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f4d0e-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="f4d0e-124">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="f4d0e-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="f4d0e-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f4d0e-125">Mapitags.h</span></span>
  
> <span data-ttu-id="f4d0e-126">Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="f4d0e-126">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f4d0e-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f4d0e-127">See also</span></span>



[<span data-ttu-id="f4d0e-128">IExchangeModifyTable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f4d0e-128">IExchangeModifyTable : IUnknown</span></span>](iexchangemodifytableiunknown.md)


[<span data-ttu-id="f4d0e-129">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f4d0e-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f4d0e-130">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="f4d0e-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f4d0e-131">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="f4d0e-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f4d0e-132">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="f4d0e-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

