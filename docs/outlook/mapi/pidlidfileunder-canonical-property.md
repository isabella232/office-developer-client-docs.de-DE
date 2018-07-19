---
title: PidLidFileUnder (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidFileUnder
api_type:
- COM
ms.assetid: 55afc4bb-c5fc-4162-a293-7d82644b1965
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: aa0a7f958ed1a5ed4140e87e25bd540123616568
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793595"
---
# <a name="pidlidfileunder-canonical-property"></a><span data-ttu-id="44d38-103">PidLidFileUnder (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="44d38-103">PidLidFileUnder Canonical Property</span></span>

  
  
<span data-ttu-id="44d38-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="44d38-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="44d38-105">Gibt den Namen an, unter dem die Kontakts beim Anzeigen einer Liste von Kontakten.</span><span class="sxs-lookup"><span data-stu-id="44d38-105">Specifies the name under which the contact is filed when displaying a list of contacts.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="44d38-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="44d38-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="44d38-107">dispidFileUnder</span><span class="sxs-lookup"><span data-stu-id="44d38-107">dispidFileUnder</span></span>  <br/> |
|<span data-ttu-id="44d38-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="44d38-108">Property set:</span></span>  <br/> |<span data-ttu-id="44d38-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="44d38-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="44d38-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="44d38-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="44d38-111">0x00008005</span><span class="sxs-lookup"><span data-stu-id="44d38-111">0x00008005</span></span>  <br/> |
|<span data-ttu-id="44d38-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="44d38-112">Data type:</span></span>  <br/> |<span data-ttu-id="44d38-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="44d38-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="44d38-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="44d38-114">Area:</span></span>  <br/> |<span data-ttu-id="44d38-115">Kontakt</span><span class="sxs-lookup"><span data-stu-id="44d38-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="44d38-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="44d38-116">Remarks</span></span>

<span data-ttu-id="44d38-117">Die Anwendung sollten diese Eigenschaft als eine leere PT_UNICODE behandeln, wenn sie von der Kontakt nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="44d38-117">The application should treat this property as an empty PT_UNICODE if it is missing from the contact.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="44d38-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="44d38-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="44d38-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="44d38-119">Protocol specifications</span></span>

<span data-ttu-id="44d38-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="44d38-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="44d38-121">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="44d38-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="44d38-122">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="44d38-122">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="44d38-123">Gibt die Eigenschaften und Operationen, die für Kontakte und persönliche Verteilerlisten zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="44d38-123">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="44d38-124">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="44d38-124">Header files</span></span>

<span data-ttu-id="44d38-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="44d38-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="44d38-126">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="44d38-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="44d38-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="44d38-127">See also</span></span>



[<span data-ttu-id="44d38-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="44d38-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="44d38-129">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="44d38-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="44d38-130">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="44d38-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="44d38-131">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="44d38-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

