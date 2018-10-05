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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25390891"
---
# <a name="pidtagmembername-canonical-property"></a><span data-ttu-id="aca78-103">PidTagMemberName (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="aca78-103">PidTagMemberName Canonical Property</span></span>

  
  
<span data-ttu-id="aca78-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="aca78-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="aca78-105">Enthält den Anzeigenamen eines Mitglieds der Access-Steuerelement (List, ACL)-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="aca78-105">Contains the display name of a member of the access control list (ACL) table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="aca78-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="aca78-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="aca78-107">PR_MEMBER_NAME, PR_MEMBER_NAME_A, PR_MEMBER_NAME_W</span><span class="sxs-lookup"><span data-stu-id="aca78-107">PR_MEMBER_NAME, PR_MEMBER_NAME_A, PR_MEMBER_NAME_W</span></span>  <br/> |
|<span data-ttu-id="aca78-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="aca78-108">Identifier:</span></span>  <br/> |<span data-ttu-id="aca78-109">0x6672</span><span class="sxs-lookup"><span data-stu-id="aca78-109">0x6672</span></span>  <br/> |
|<span data-ttu-id="aca78-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="aca78-110">Data type:</span></span>  <br/> |<span data-ttu-id="aca78-111">PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="aca78-111">PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="aca78-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="aca78-112">Area:</span></span>  <br/> |<span data-ttu-id="aca78-113">Steuerung des Zugriffs</span><span class="sxs-lookup"><span data-stu-id="aca78-113">Access Control</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="aca78-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="aca78-114">Remarks</span></span>

<span data-ttu-id="aca78-115">Diese Eigenschaften werden verwendet, indem die [IExchangeModifyTable: IUnknown](iexchangemodifytableiunknown.md) Schnittstelle den Namen eines Mitglieds der einer ACL-Tabelle angezeigt werden, die eine Person oder Rolle mit expliziten Berechtigungen für einen Ordner oder Postfach ist.</span><span class="sxs-lookup"><span data-stu-id="aca78-115">These properties are used by the [IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md) interface to display the name of a member of an ACL table, which is a person or role with explicit rights on a folder or mailbox.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="aca78-116">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="aca78-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="aca78-117">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="aca78-117">Protocol specifications</span></span>

<span data-ttu-id="aca78-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="aca78-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="aca78-119">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="aca78-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="aca78-120">[[MS-OXCPERM]](https://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="aca78-120">[[MS-OXCPERM]](https://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="aca78-121">Behandelt das Abrufen von Ordner Berechtigungslisten, die auf dem Server gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="aca78-121">Handles the retrieval of folder permission lists that are stored on the server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="aca78-122">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="aca78-122">Header files</span></span>

<span data-ttu-id="aca78-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="aca78-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="aca78-124">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="aca78-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="aca78-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="aca78-125">Mapitags.h</span></span>
  
> <span data-ttu-id="aca78-126">Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="aca78-126">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="aca78-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="aca78-127">See also</span></span>



[<span data-ttu-id="aca78-128">IExchangeModifyTable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="aca78-128">IExchangeModifyTable : IUnknown</span></span>](iexchangemodifytableiunknown.md)


[<span data-ttu-id="aca78-129">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="aca78-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="aca78-130">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="aca78-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="aca78-131">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="aca78-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="aca78-132">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="aca78-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

