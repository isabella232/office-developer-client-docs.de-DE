---
title: PidTagAccessControlListTable (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAccess
api_type:
- HeaderDef
ms.assetid: 48667fda-ddc4-42ac-9231-761db0a4c1a9
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 40a2bc8a27ec3ce3df610b9c7364719c2b5ee750
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572788"
---
# <a name="pidtagaccesscontrollisttable-canonical-property"></a><span data-ttu-id="a237a-103">PidTagAccessControlListTable (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="a237a-103">PidTagAccessControlListTable Canonical Property</span></span>

  
  
<span data-ttu-id="a237a-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a237a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a237a-105">Enthält eine Tabelle, die alle System Access Control Lists (SACL) in einen Ordner angewendet besteht.</span><span class="sxs-lookup"><span data-stu-id="a237a-105">Contains a table that consists of all the system access control lists (SACL) applied to a folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a237a-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="a237a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a237a-107">PR_ACL_TABLE</span><span class="sxs-lookup"><span data-stu-id="a237a-107">PR_ACL_TABLE</span></span>  <br/> |
|<span data-ttu-id="a237a-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="a237a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a237a-109">0x3FE0</span><span class="sxs-lookup"><span data-stu-id="a237a-109">0x3FE0</span></span>  <br/> |
|<span data-ttu-id="a237a-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="a237a-110">Data type:</span></span>  <br/> |<span data-ttu-id="a237a-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="a237a-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="a237a-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="a237a-112">Area:</span></span>  <br/> |<span data-ttu-id="a237a-113">Steuerung des Zugriffs</span><span class="sxs-lookup"><span data-stu-id="a237a-113">Access Control</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a237a-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a237a-114">Remarks</span></span>

<span data-ttu-id="a237a-115">Diese Eigenschaft ist für alle Ordnerobjekte, die auf einem Exchange-Server vorhanden.</span><span class="sxs-lookup"><span data-stu-id="a237a-115">This property is present on all folder objects on an Exchange Server.</span></span> <span data-ttu-id="a237a-116">Werte enthalten, die in dieser Eigenschaft wird zum Lesen und ändern die Steuerung des Zugriffs Zugriffssteuerungslisten (ACLs) für Ordner.</span><span class="sxs-lookup"><span data-stu-id="a237a-116">Values included in this property are used for reading and modifying access control lists (ACLs) on folders.</span></span> <span data-ttu-id="a237a-117">Sie können die [IMAPIProp::OpenProperty](imapiprop-openproperty.md) -Methode mit der **IID_IExchangeModifyTable** Interface Identifier verwenden, erhalten eine [IExchangeModifyTable: IUnknown](iexchangemodifytableiunknown.md) -Schnittstelle für die ACL-Tabelle in einem Ordner.</span><span class="sxs-lookup"><span data-stu-id="a237a-117">You can use the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method with the **IID_IExchangeModifyTable** interface identifier to obtain an [IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md) interface to the ACL table on a folder.</span></span> <span data-ttu-id="a237a-118">Sie können diese Schnittstelle zum Lesen und Ändern von ACLs verwenden.</span><span class="sxs-lookup"><span data-stu-id="a237a-118">You can use this interface to read and modify those ACLs.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="a237a-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="a237a-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="a237a-120">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="a237a-120">Header files</span></span>

<span data-ttu-id="a237a-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a237a-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="a237a-122">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="a237a-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="a237a-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a237a-123">Mapitags.h</span></span>
  
> <span data-ttu-id="a237a-124">Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="a237a-124">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a237a-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a237a-125">See also</span></span>



[<span data-ttu-id="a237a-126">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a237a-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a237a-127">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a237a-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a237a-128">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="a237a-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a237a-129">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="a237a-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

