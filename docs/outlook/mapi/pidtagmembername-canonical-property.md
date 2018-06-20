---
title: Kanonische PidTagMemberName-Eigenschaft
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
ms.openlocfilehash: 694cc4e4626fb9070927232bb72252f716eb458e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794584"
---
# <a name="pidtagmembername-canonical-property"></a><span data-ttu-id="940c4-103">Kanonische PidTagMemberName-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="940c4-103">PidTagMemberName Canonical Property</span></span>

  
  
<span data-ttu-id="940c4-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="940c4-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="940c4-105">Enthält den Anzeigenamen eines Mitglieds der Access-Steuerelement (List, ACL)-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="940c4-105">Contains the display name of a member of the access control list (ACL) table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="940c4-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="940c4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="940c4-107">PR_MEMBER_NAME, PR_MEMBER_NAME_A, PR_MEMBER_NAME_W</span><span class="sxs-lookup"><span data-stu-id="940c4-107">PR_MEMBER_NAME, PR_MEMBER_NAME_A, PR_MEMBER_NAME_W</span></span>  <br/> |
|<span data-ttu-id="940c4-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="940c4-108">Identifier:</span></span>  <br/> |<span data-ttu-id="940c4-109">0x6672</span><span class="sxs-lookup"><span data-stu-id="940c4-109">0x6672</span></span>  <br/> |
|<span data-ttu-id="940c4-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="940c4-110">Data type:</span></span>  <br/> |<span data-ttu-id="940c4-111">PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="940c4-111">PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="940c4-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="940c4-112">Area:</span></span>  <br/> |<span data-ttu-id="940c4-113">Steuerung des Zugriffs</span><span class="sxs-lookup"><span data-stu-id="940c4-113">Access Control</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="940c4-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="940c4-114">Remarks</span></span>

<span data-ttu-id="940c4-115">Diese Eigenschaften werden verwendet, indem die [IExchangeModifyTable: IUnknown](iexchangemodifytableiunknown.md) Schnittstelle den Namen eines Mitglieds der einer ACL-Tabelle angezeigt werden, die eine Person oder Rolle mit expliziten Berechtigungen für einen Ordner oder Postfach ist.</span><span class="sxs-lookup"><span data-stu-id="940c4-115">These properties are used by the [IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md) interface to display the name of a member of an ACL table, which is a person or role with explicit rights on a folder or mailbox.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="940c4-116">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="940c4-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="940c4-117">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="940c4-117">Protocol specifications</span></span>

<span data-ttu-id="940c4-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="940c4-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="940c4-119">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="940c4-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="940c4-120">[[MS-OXCPERM]](http://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="940c4-120">[[MS-OXCPERM]](http://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="940c4-121">Behandelt das Abrufen von Ordner Berechtigungslisten, die auf dem Server gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="940c4-121">Handles the retrieval of folder permission lists that are stored on the server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="940c4-122">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="940c4-122">Header files</span></span>

<span data-ttu-id="940c4-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="940c4-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="940c4-124">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="940c4-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="940c4-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="940c4-125">Mapitags.h</span></span>
  
> <span data-ttu-id="940c4-126">Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="940c4-126">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="940c4-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="940c4-127">See also</span></span>



[<span data-ttu-id="940c4-128">IExchangeModifyTable: IUnknown</span><span class="sxs-lookup"><span data-stu-id="940c4-128">IExchangeModifyTable : IUnknown</span></span>](iexchangemodifytableiunknown.md)


[<span data-ttu-id="940c4-129">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="940c4-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="940c4-130">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="940c4-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="940c4-131">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="940c4-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="940c4-132">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="940c4-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

