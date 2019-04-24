---
title: Kanonische Pidtagmemberentryid (-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 83a645b49e5bb48051bbaedb26058d2da053348b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342497"
---
# <a name="pidtagmemberentryid-canonical-property"></a><span data-ttu-id="50c91-103">Kanonische Pidtagmemberentryid (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="50c91-103">PidTagMemberEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="50c91-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="50c91-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="50c91-105">Enthält den Eintragsbezeichner des Verzeichnisobjekts für ein SACL-Tabellenelement (System Access Control List).</span><span class="sxs-lookup"><span data-stu-id="50c91-105">Contains the directory object entry identifier of a system access control list (SACL) table member.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="50c91-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="50c91-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="50c91-107">PR_MEMBER_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="50c91-107">PR_MEMBER_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="50c91-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="50c91-108">Identifier:</span></span>  <br/> |<span data-ttu-id="50c91-109">0X0fff dar</span><span class="sxs-lookup"><span data-stu-id="50c91-109">0x0FFF</span></span>  <br/> |
|<span data-ttu-id="50c91-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="50c91-110">Data type:</span></span>  <br/> |<span data-ttu-id="50c91-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="50c91-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="50c91-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="50c91-112">Area:</span></span>  <br/> |<span data-ttu-id="50c91-113">Server seitige Regeln</span><span class="sxs-lookup"><span data-stu-id="50c91-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="50c91-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="50c91-114">Remarks</span></span>

<span data-ttu-id="50c91-115">Diese Eigenschaft wird von der [IExchangeModifyTable](iexchangemodifytableiunknown.md) -Schnittstelle verwendet, um eine Person oder Rolle, für die die SACL gilt, eindeutig zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="50c91-115">This property is used by the [IExchangeModifyTable](iexchangemodifytableiunknown.md) interface to uniquely identify a person or role to whom the SACL applies.</span></span> <span data-ttu-id="50c91-116">Nachdem ein Element in der SACL-Tabelle erstellt wurde, \*\*\*\* kann es nicht mehr geändert werden.</span><span class="sxs-lookup"><span data-stu-id="50c91-116">After a member is created in the SACL table, the **ENTRYID** cannot be changed.</span></span> <span data-ttu-id="50c91-117">Um Sie zu ändern, müssen Sie das Table-Element löschen und es mit einer anderen **Eintrags**-Nr. neu erstellen.</span><span class="sxs-lookup"><span data-stu-id="50c91-117">To change it, you must delete the table member and re-create it with a different **ENTRYID**.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="50c91-118">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="50c91-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="50c91-119">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="50c91-119">Header files</span></span>

<span data-ttu-id="50c91-120">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="50c91-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="50c91-121">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="50c91-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="50c91-122">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="50c91-122">Mapitags.h</span></span>
  
> <span data-ttu-id="50c91-123">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="50c91-123">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="50c91-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="50c91-124">See also</span></span>



[<span data-ttu-id="50c91-125">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="50c91-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="50c91-126">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="50c91-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="50c91-127">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="50c91-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="50c91-128">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="50c91-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

