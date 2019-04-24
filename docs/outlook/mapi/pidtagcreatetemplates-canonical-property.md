---
title: Kanonische Pidtagcreatetemplates (-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 08cf1faa0c3cc4cf61e2253b0026361704fdd0e2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32269937"
---
# <a name="pidtagcreatetemplates-canonical-property"></a><span data-ttu-id="ee4cb-103">Kanonische Pidtagcreatetemplates (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="ee4cb-103">PidTagCreateTemplates Canonical Property</span></span>

  
  
<span data-ttu-id="ee4cb-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ee4cb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ee4cb-105">Enthält ein eingebettetes Table-Objekt, das Eingabe-IDs für Dialogfeldvorlagen enthält.</span><span class="sxs-lookup"><span data-stu-id="ee4cb-105">Contains an embedded table object that contains dialog box template entry identifiers.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ee4cb-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="ee4cb-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ee4cb-107">PR_CREATE_TEMPLATES</span><span class="sxs-lookup"><span data-stu-id="ee4cb-107">PR_CREATE_TEMPLATES</span></span>  <br/> |
|<span data-ttu-id="ee4cb-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="ee4cb-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ee4cb-109">0x3604</span><span class="sxs-lookup"><span data-stu-id="ee4cb-109">0x3604</span></span>  <br/> |
|<span data-ttu-id="ee4cb-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="ee4cb-110">Data type:</span></span>  <br/> |<span data-ttu-id="ee4cb-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="ee4cb-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="ee4cb-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="ee4cb-112">Area:</span></span>  <br/> |<span data-ttu-id="ee4cb-113">Adressbuch</span><span class="sxs-lookup"><span data-stu-id="ee4cb-113">Address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ee4cb-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ee4cb-114">Remarks</span></span>

<span data-ttu-id="ee4cb-115">Um zu erfahren, welche Vorlagenobjekte innerhalb eines Containers erstellt werden können, rufen Sie die [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) -Methode für diese Eigenschaft auf.</span><span class="sxs-lookup"><span data-stu-id="ee4cb-115">To learn what template objects can be created inside a container, call the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method on this property.</span></span> <span data-ttu-id="ee4cb-116">Das resultierende Objekt ist die einmalige Tabelle, die die Eintragsbezeichner für alle Vorlagen enthält, die Sie innerhalb des Containers erstellen können.</span><span class="sxs-lookup"><span data-stu-id="ee4cb-116">The resulting object is the one-off table that gives the entry identifiers for all the templates that you can create inside the container.</span></span> 
  
<span data-ttu-id="ee4cb-117">Zum Erstellen der Template-Objekte rufen Sie die createEntry \*\*\*\* -Methode des Container-Objekts für die **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) aus der einmaligen Tabelle auf.</span><span class="sxs-lookup"><span data-stu-id="ee4cb-117">To create the template objects, call the container object's **CreateEntry** method on the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) column values from the one-off table.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="ee4cb-118">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="ee4cb-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="ee4cb-119">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="ee4cb-119">Header files</span></span>

<span data-ttu-id="ee4cb-120">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="ee4cb-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="ee4cb-121">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="ee4cb-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="ee4cb-122">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="ee4cb-122">Mapitags.h</span></span>
  
> <span data-ttu-id="ee4cb-123">Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="ee4cb-123">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ee4cb-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ee4cb-124">See also</span></span>



[<span data-ttu-id="ee4cb-125">IABContainer::CreateEntry</span><span class="sxs-lookup"><span data-stu-id="ee4cb-125">IABContainer::CreateEntry</span></span>](iabcontainer-createentry.md)


[<span data-ttu-id="ee4cb-126">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ee4cb-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ee4cb-127">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ee4cb-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ee4cb-128">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="ee4cb-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ee4cb-129">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="ee4cb-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

