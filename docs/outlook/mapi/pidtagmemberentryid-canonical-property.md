---
title: PidTagMemberEntryId (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMemberEntryId
api_type:
- HeaderDef
ms.assetid: b1e166fd-7e15-4371-8510-63001317fb90
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 3139f7cc60d19048fb17c64101f279ce377e9b26
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794600"
---
# <a name="pidtagmemberentryid-canonical-property"></a><span data-ttu-id="5b250-103">PidTagMemberEntryId (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="5b250-103">PidTagMemberEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="5b250-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5b250-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5b250-105">Enthält den Directory Eintrag Objektbezeichner des Mitglied Tabelle System Access Control List (SACL).</span><span class="sxs-lookup"><span data-stu-id="5b250-105">Contains the directory object entry identifier of a system access control list (SACL) table member.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5b250-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="5b250-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5b250-107">PR_MEMBER_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="5b250-107">PR_MEMBER_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="5b250-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="5b250-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5b250-109">0x0FFF</span><span class="sxs-lookup"><span data-stu-id="5b250-109">0x0FFF</span></span>  <br/> |
|<span data-ttu-id="5b250-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="5b250-110">Data type:</span></span>  <br/> |<span data-ttu-id="5b250-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="5b250-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="5b250-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="5b250-112">Area:</span></span>  <br/> |<span data-ttu-id="5b250-113">Serverseitige Regeln</span><span class="sxs-lookup"><span data-stu-id="5b250-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5b250-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5b250-114">Remarks</span></span>

<span data-ttu-id="5b250-115">Diese Eigenschaft wird durch die [IExchangeModifyTable](iexchangemodifytableiunknown.md) -Schnittstelle verwendet, um eine Person oder Rolle, denen die SACL gilt, eindeutig zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="5b250-115">This property is used by the [IExchangeModifyTable](iexchangemodifytableiunknown.md) interface to uniquely identify a person or role to whom the SACL applies.</span></span> <span data-ttu-id="5b250-116">Nachdem ein Element in der SACL-Tabelle erstellt wurde, kann die **ENTRYID** geändert werden.</span><span class="sxs-lookup"><span data-stu-id="5b250-116">After a member is created in the SACL table, the **ENTRYID** cannot be changed.</span></span> <span data-ttu-id="5b250-117">Zum Ändern dieser Einstellung müssen Sie das Tabelle Element löschen und mit einem anderen **ENTRYID**neu erstellen.</span><span class="sxs-lookup"><span data-stu-id="5b250-117">To change it, you must delete the table member and re-create it with a different **ENTRYID**.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="5b250-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="5b250-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="5b250-119">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="5b250-119">Header files</span></span>

<span data-ttu-id="5b250-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5b250-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="5b250-121">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="5b250-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="5b250-122">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="5b250-122">Mapitags.h</span></span>
  
> <span data-ttu-id="5b250-123">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="5b250-123">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5b250-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5b250-124">See also</span></span>



[<span data-ttu-id="5b250-125">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5b250-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5b250-126">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5b250-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5b250-127">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="5b250-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5b250-128">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="5b250-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

