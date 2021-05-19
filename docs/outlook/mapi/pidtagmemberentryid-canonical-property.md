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
ms.openlocfilehash: 83a645b49e5bb48051bbaedb26058d2da053348b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433038"
---
# <a name="pidtagmemberentryid-canonical-property"></a><span data-ttu-id="becae-103">PidTagMemberEntryId (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="becae-103">PidTagMemberEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="becae-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="becae-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="becae-105">Enthält die Verzeichnisobjekteintrags-ID eines Sacl-Tabellenmitglieds (System Access Control List).</span><span class="sxs-lookup"><span data-stu-id="becae-105">Contains the directory object entry identifier of a system access control list (SACL) table member.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="becae-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="becae-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="becae-107">PR_MEMBER_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="becae-107">PR_MEMBER_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="becae-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="becae-108">Identifier:</span></span>  <br/> |<span data-ttu-id="becae-109">0x0FFF</span><span class="sxs-lookup"><span data-stu-id="becae-109">0x0FFF</span></span>  <br/> |
|<span data-ttu-id="becae-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="becae-110">Data type:</span></span>  <br/> |<span data-ttu-id="becae-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="becae-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="becae-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="becae-112">Area:</span></span>  <br/> |<span data-ttu-id="becae-113">Serverseitige Regeln</span><span class="sxs-lookup"><span data-stu-id="becae-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="becae-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="becae-114">Remarks</span></span>

<span data-ttu-id="becae-115">Diese Eigenschaft wird von der [IExchangeModifyTable-Schnittstelle](iexchangemodifytableiunknown.md) verwendet, um eine Person oder Rolle eindeutig zu identifizieren, auf die die SACL angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="becae-115">This property is used by the [IExchangeModifyTable](iexchangemodifytableiunknown.md) interface to uniquely identify a person or role to whom the SACL applies.</span></span> <span data-ttu-id="becae-116">Nachdem ein Element in der SACL-Tabelle erstellt wurde, kann **die ENTRYID** nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="becae-116">After a member is created in the SACL table, the **ENTRYID** cannot be changed.</span></span> <span data-ttu-id="becae-117">Um es zu ändern, müssen Sie das Tabellenmitglied löschen und es mit einer anderen **ENTRYID neu erstellen.**</span><span class="sxs-lookup"><span data-stu-id="becae-117">To change it, you must delete the table member and re-create it with a different **ENTRYID**.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="becae-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="becae-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="becae-119">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="becae-119">Header files</span></span>

<span data-ttu-id="becae-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="becae-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="becae-121">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="becae-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="becae-122">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="becae-122">Mapitags.h</span></span>
  
> <span data-ttu-id="becae-123">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="becae-123">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="becae-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="becae-124">See also</span></span>



[<span data-ttu-id="becae-125">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="becae-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="becae-126">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="becae-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="becae-127">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="becae-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="becae-128">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="becae-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

