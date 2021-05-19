---
title: PidTagInitialDetailsPane (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagInitialDetailsPane
api_type:
- HeaderDef
ms.assetid: c4712133-6fbd-4c50-a258-5f4317120476
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 3bf0f52dbeda37ac35024ae3bf38df8919e37b60
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346578"
---
# <a name="pidtaginitialdetailspane-canonical-property"></a><span data-ttu-id="4148c-103">PidTagInitialDetailsPane (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="4148c-103">PidTagInitialDetailsPane Canonical Property</span></span>

  
  
<span data-ttu-id="4148c-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4148c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4148c-105">Gibt die Seite einer Anzeigevorlage an, die zuerst angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="4148c-105">Indicates the page of a display template to display first.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4148c-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="4148c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4148c-107">PR_INITIAL_DETAILS_PANE</span><span class="sxs-lookup"><span data-stu-id="4148c-107">PR_INITIAL_DETAILS_PANE</span></span>  <br/> |
|<span data-ttu-id="4148c-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="4148c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4148c-109">0x3F08</span><span class="sxs-lookup"><span data-stu-id="4148c-109">0x3F08</span></span>  <br/> |
|<span data-ttu-id="4148c-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="4148c-110">Data type:</span></span>  <br/> |<span data-ttu-id="4148c-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="4148c-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="4148c-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="4148c-112">Area:</span></span>  <br/> |<span data-ttu-id="4148c-113">MAPI-Anzeigetabellen</span><span class="sxs-lookup"><span data-stu-id="4148c-113">MAPI Display Tables</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4148c-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="4148c-114">Remarks</span></span>

<span data-ttu-id="4148c-115">Sie muss auf allen Adressbuchobjekten auf einem NSPI-Server (Name Service Provider Interface) vorhanden sein und den Wert Null (0) haben.</span><span class="sxs-lookup"><span data-stu-id="4148c-115">It must be present on all address book objects on an Name Service Provider Interface (NSPI) server, and must have the value zero (0).</span></span> <span data-ttu-id="4148c-116">Sie darf nicht für Objekte in einem Offlineadressbuch definiert werden.</span><span class="sxs-lookup"><span data-stu-id="4148c-116">It must not be defined for any objects in an Offline Address Book.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="4148c-117">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="4148c-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4148c-118">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="4148c-118">Protocol specifications</span></span>

<span data-ttu-id="4148c-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4148c-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4148c-120">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="4148c-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4148c-121">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4148c-121">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4148c-122">Gibt die Eigenschaften und Vorgänge für Listen von Benutzern, Kontakten, Gruppen und Ressourcen an.</span><span class="sxs-lookup"><span data-stu-id="4148c-122">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4148c-123">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="4148c-123">Header files</span></span>

<span data-ttu-id="4148c-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4148c-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="4148c-125">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="4148c-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="4148c-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="4148c-126">Mapitags.h</span></span>
  
> <span data-ttu-id="4148c-127">Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="4148c-127">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4148c-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4148c-128">See also</span></span>



[<span data-ttu-id="4148c-129">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4148c-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4148c-130">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="4148c-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4148c-131">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="4148c-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4148c-132">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="4148c-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

