---
title: PidTagCreateTemplates (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagCreateTemplates
api_type:
- HeaderDef
ms.assetid: d2530009-5de3-4872-a0a5-be1389c4206e
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 28611e442f816e4d091cc6b29e2ee69195a63d09
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563359"
---
# <a name="pidtagcreatetemplates-canonical-property"></a><span data-ttu-id="2005a-103">PidTagCreateTemplates (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="2005a-103">PidTagCreateTemplates Canonical Property</span></span>

  
  
<span data-ttu-id="2005a-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2005a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2005a-105">Enthält eine eingebettete Table-Objekt, das Dialogfeld Feld Vorlage-Eintragsbezeichner enthält.</span><span class="sxs-lookup"><span data-stu-id="2005a-105">Contains an embedded table object that contains dialog box template entry identifiers.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2005a-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="2005a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2005a-107">PR_CREATE_TEMPLATES</span><span class="sxs-lookup"><span data-stu-id="2005a-107">PR_CREATE_TEMPLATES</span></span>  <br/> |
|<span data-ttu-id="2005a-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="2005a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2005a-109">0x3604</span><span class="sxs-lookup"><span data-stu-id="2005a-109">0x3604</span></span>  <br/> |
|<span data-ttu-id="2005a-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="2005a-110">Data type:</span></span>  <br/> |<span data-ttu-id="2005a-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="2005a-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="2005a-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="2005a-112">Area:</span></span>  <br/> |<span data-ttu-id="2005a-113">Adressbuch</span><span class="sxs-lookup"><span data-stu-id="2005a-113">Address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2005a-114">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="2005a-114">Remarks</span></span>

<span data-ttu-id="2005a-115">Welche Vorlage erhalten Sie Objekte in einem Container erstellt werden können, rufen Sie die [IMAPIProp::OpenProperty](imapiprop-openproperty.md) -Methode für diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="2005a-115">To learn what template objects can be created inside a container, call the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method on this property.</span></span> <span data-ttu-id="2005a-116">Das resultierende Objekt ist der einmaligen Tabelle mit den Eintrag-IDs für alle Vorlagen, die Sie innerhalb des Containers erstellen können.</span><span class="sxs-lookup"><span data-stu-id="2005a-116">The resulting object is the one-off table that gives the entry identifiers for all the templates that you can create inside the container.</span></span> 
  
<span data-ttu-id="2005a-117">Rufen Sie das Containerobjekt **CreateEntry** -Methode zum Erstellen der Vorlagenobjekte auf die Spaltenwerte **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) aus der einmaligen Tabelle.</span><span class="sxs-lookup"><span data-stu-id="2005a-117">To create the template objects, call the container object's **CreateEntry** method on the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) column values from the one-off table.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="2005a-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="2005a-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="2005a-119">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="2005a-119">Header files</span></span>

<span data-ttu-id="2005a-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2005a-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="2005a-121">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="2005a-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="2005a-122">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="2005a-122">Mapitags.h</span></span>
  
> <span data-ttu-id="2005a-123">Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="2005a-123">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2005a-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2005a-124">See also</span></span>



[<span data-ttu-id="2005a-125">IABContainer::CreateEntry</span><span class="sxs-lookup"><span data-stu-id="2005a-125">IABContainer::CreateEntry</span></span>](iabcontainer-createentry.md)


[<span data-ttu-id="2005a-126">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2005a-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2005a-127">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2005a-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2005a-128">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="2005a-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2005a-129">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="2005a-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

