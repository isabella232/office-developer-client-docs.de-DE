---
title: Kanonische Pidtaginitialdetailspane (-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 3bf0f52dbeda37ac35024ae3bf38df8919e37b60
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346578"
---
# <a name="pidtaginitialdetailspane-canonical-property"></a><span data-ttu-id="69ae4-103">Kanonische Pidtaginitialdetailspane (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="69ae4-103">PidTagInitialDetailsPane Canonical Property</span></span>

  
  
<span data-ttu-id="69ae4-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="69ae4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="69ae4-105">Gibt die Seite einer Anzeigevorlage an, die zuerst angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="69ae4-105">Indicates the page of a display template to display first.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="69ae4-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="69ae4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="69ae4-107">PR_INITIAL_DETAILS_PANE</span><span class="sxs-lookup"><span data-stu-id="69ae4-107">PR_INITIAL_DETAILS_PANE</span></span>  <br/> |
|<span data-ttu-id="69ae4-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="69ae4-108">Identifier:</span></span>  <br/> |<span data-ttu-id="69ae4-109">0x3F08</span><span class="sxs-lookup"><span data-stu-id="69ae4-109">0x3F08</span></span>  <br/> |
|<span data-ttu-id="69ae4-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="69ae4-110">Data type:</span></span>  <br/> |<span data-ttu-id="69ae4-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="69ae4-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="69ae4-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="69ae4-112">Area:</span></span>  <br/> |<span data-ttu-id="69ae4-113">MAPI-Anzeige Tabellen</span><span class="sxs-lookup"><span data-stu-id="69ae4-113">MAPI Display Tables</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="69ae4-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="69ae4-114">Remarks</span></span>

<span data-ttu-id="69ae4-115">Er muss für alle Adressbuch Objekte auf einem NSPI-Server (Name Service Provider Interface) vorhanden sein und den Wert NULL (0) haben.</span><span class="sxs-lookup"><span data-stu-id="69ae4-115">It must be present on all address book objects on an Name Service Provider Interface (NSPI) server, and must have the value zero (0).</span></span> <span data-ttu-id="69ae4-116">Sie darf nicht für Objekte in einem Offline Adressbuch definiert werden.</span><span class="sxs-lookup"><span data-stu-id="69ae4-116">It must not be defined for any objects in an Offline Address Book.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="69ae4-117">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="69ae4-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="69ae4-118">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="69ae4-118">Protocol specifications</span></span>

<span data-ttu-id="69ae4-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="69ae4-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="69ae4-120">Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="69ae4-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="69ae4-121">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="69ae4-121">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="69ae4-122">Gibt die Eigenschaften und Vorgänge für Listen von Benutzern, Kontakten, Gruppen und Ressourcen an.</span><span class="sxs-lookup"><span data-stu-id="69ae4-122">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="69ae4-123">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="69ae4-123">Header files</span></span>

<span data-ttu-id="69ae4-124">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="69ae4-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="69ae4-125">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="69ae4-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="69ae4-126">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="69ae4-126">Mapitags.h</span></span>
  
> <span data-ttu-id="69ae4-127">Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="69ae4-127">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="69ae4-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="69ae4-128">See also</span></span>



[<span data-ttu-id="69ae4-129">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="69ae4-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="69ae4-130">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="69ae4-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="69ae4-131">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="69ae4-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="69ae4-132">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="69ae4-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

