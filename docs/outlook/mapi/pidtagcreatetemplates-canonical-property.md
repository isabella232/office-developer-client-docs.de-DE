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
ms.openlocfilehash: 08cf1faa0c3cc4cf61e2253b0026361704fdd0e2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438183"
---
# <a name="pidtagcreatetemplates-canonical-property"></a><span data-ttu-id="57427-103">PidTagCreateTemplates (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="57427-103">PidTagCreateTemplates Canonical Property</span></span>

  
  
<span data-ttu-id="57427-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="57427-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="57427-105">Enthält ein eingebettetes Tabellenobjekt, das Eingabebezeichner für Dialogfeldvorlagen enthält.</span><span class="sxs-lookup"><span data-stu-id="57427-105">Contains an embedded table object that contains dialog box template entry identifiers.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="57427-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="57427-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="57427-107">PR_CREATE_TEMPLATES</span><span class="sxs-lookup"><span data-stu-id="57427-107">PR_CREATE_TEMPLATES</span></span>  <br/> |
|<span data-ttu-id="57427-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="57427-108">Identifier:</span></span>  <br/> |<span data-ttu-id="57427-109">0x3604</span><span class="sxs-lookup"><span data-stu-id="57427-109">0x3604</span></span>  <br/> |
|<span data-ttu-id="57427-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="57427-110">Data type:</span></span>  <br/> |<span data-ttu-id="57427-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="57427-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="57427-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="57427-112">Area:</span></span>  <br/> |<span data-ttu-id="57427-113">Adressbuch</span><span class="sxs-lookup"><span data-stu-id="57427-113">Address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="57427-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="57427-114">Remarks</span></span>

<span data-ttu-id="57427-115">Um zu erfahren, welche Vorlagenobjekte in einem Container erstellt werden können, rufen Sie die [IMAPIProp::OpenProperty-Methode](imapiprop-openproperty.md) für diese Eigenschaft auf.</span><span class="sxs-lookup"><span data-stu-id="57427-115">To learn what template objects can be created inside a container, call the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method on this property.</span></span> <span data-ttu-id="57427-116">Das resultierende Objekt ist die einmal aufgeführte Tabelle, die die Eintragsbezeichner für alle Vorlagen angibt, die Sie innerhalb des Containers erstellen können.</span><span class="sxs-lookup"><span data-stu-id="57427-116">The resulting object is the one-off table that gives the entry identifiers for all the templates that you can create inside the container.</span></span> 
  
<span data-ttu-id="57427-117">Rufen Sie zum Erstellen der Vorlagenobjekte die **CreateEntry-Methode** des Containerobjekts in den **Spaltenwerten PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) aus der einmaltabelle auf.</span><span class="sxs-lookup"><span data-stu-id="57427-117">To create the template objects, call the container object's **CreateEntry** method on the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) column values from the one-off table.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="57427-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="57427-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="57427-119">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="57427-119">Header files</span></span>

<span data-ttu-id="57427-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="57427-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="57427-121">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="57427-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="57427-122">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="57427-122">Mapitags.h</span></span>
  
> <span data-ttu-id="57427-123">Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="57427-123">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="57427-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="57427-124">See also</span></span>



[<span data-ttu-id="57427-125">IABContainer::CreateEntry</span><span class="sxs-lookup"><span data-stu-id="57427-125">IABContainer::CreateEntry</span></span>](iabcontainer-createentry.md)


[<span data-ttu-id="57427-126">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="57427-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="57427-127">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="57427-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="57427-128">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="57427-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="57427-129">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="57427-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

