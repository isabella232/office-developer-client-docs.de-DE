---
title: Kanonische Pidtagaccesscontrollisttable (-Eigenschaft
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
ms.openlocfilehash: 9c71a2b806b810906c13ea4750e5491b1544f640
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424504"
---
# <a name="pidtagaccesscontrollisttable-canonical-property"></a><span data-ttu-id="371cd-103">Kanonische Pidtagaccesscontrollisttable (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="371cd-103">PidTagAccessControlListTable Canonical Property</span></span>

  
  
<span data-ttu-id="371cd-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="371cd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="371cd-105">Enthält eine Tabelle, die aus allen SACL-Systemen (System Access Control Lists) besteht, die auf einen Ordner angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="371cd-105">Contains a table that consists of all the system access control lists (SACL) applied to a folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="371cd-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="371cd-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="371cd-107">PR_ACL_TABLE</span><span class="sxs-lookup"><span data-stu-id="371cd-107">PR_ACL_TABLE</span></span>  <br/> |
|<span data-ttu-id="371cd-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="371cd-108">Identifier:</span></span>  <br/> |<span data-ttu-id="371cd-109">0x3FE0</span><span class="sxs-lookup"><span data-stu-id="371cd-109">0x3FE0</span></span>  <br/> |
|<span data-ttu-id="371cd-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="371cd-110">Data type:</span></span>  <br/> |<span data-ttu-id="371cd-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="371cd-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="371cd-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="371cd-112">Area:</span></span>  <br/> |<span data-ttu-id="371cd-113">Zugriffssteuerung</span><span class="sxs-lookup"><span data-stu-id="371cd-113">Access Control</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="371cd-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="371cd-114">Remarks</span></span>

<span data-ttu-id="371cd-115">Diese Eigenschaft ist für alle Folder-Objekte auf einem Exchange-Server vorhanden.</span><span class="sxs-lookup"><span data-stu-id="371cd-115">This property is present on all folder objects on an Exchange Server.</span></span> <span data-ttu-id="371cd-116">In dieser Eigenschaft enthaltene Werte werden zum Lesen und Ändern von Zugriffssteuerungslisten (Access Control Lists, ACLs) für Ordner verwendet.</span><span class="sxs-lookup"><span data-stu-id="371cd-116">Values included in this property are used for reading and modifying access control lists (ACLs) on folders.</span></span> <span data-ttu-id="371cd-117">Sie können die [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) -Methode mit dem **IID_IExchangeModifyTable** -Schnittstellenbezeichner verwenden, um eine [IExchangeModifyTable: IUnknown](iexchangemodifytableiunknown.md) -Schnittstelle für die ACL-Tabelle in einem Ordner abzurufen.</span><span class="sxs-lookup"><span data-stu-id="371cd-117">You can use the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method with the **IID_IExchangeModifyTable** interface identifier to obtain an [IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md) interface to the ACL table on a folder.</span></span> <span data-ttu-id="371cd-118">Sie können diese Schnittstelle verwenden, um diese ACLs zu lesen und zu ändern.</span><span class="sxs-lookup"><span data-stu-id="371cd-118">You can use this interface to read and modify those ACLs.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="371cd-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="371cd-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="371cd-120">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="371cd-120">Header files</span></span>

<span data-ttu-id="371cd-121">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="371cd-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="371cd-122">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="371cd-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="371cd-123">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="371cd-123">Mapitags.h</span></span>
  
> <span data-ttu-id="371cd-124">Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="371cd-124">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="371cd-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="371cd-125">See also</span></span>



[<span data-ttu-id="371cd-126">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="371cd-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="371cd-127">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="371cd-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="371cd-128">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="371cd-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="371cd-129">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="371cd-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

