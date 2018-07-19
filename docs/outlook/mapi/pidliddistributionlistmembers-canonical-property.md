---
title: PidLidDistributionListMembers (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidDistributionListMembers
api_type:
- COM
ms.assetid: 029767ab-de72-4402-9cc3-31b006591042
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: c27513474048e9805bc29116aa094bc47f8f0cae
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793494"
---
# <a name="pidliddistributionlistmembers-canonical-property"></a><span data-ttu-id="bb21c-103">PidLidDistributionListMembers (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="bb21c-103">PidLidDistributionListMembers Canonical Property</span></span>

  
  
<span data-ttu-id="bb21c-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="bb21c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="bb21c-105">Gibt die Liste der EntryIds-Objekte, die die Elemente der persönlichen Verteilerliste entsprechen.</span><span class="sxs-lookup"><span data-stu-id="bb21c-105">Specifies the list of EntryIds of the objects that correspond to the members of the personal distribution list.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="bb21c-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="bb21c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bb21c-107">dispidDLMembers</span><span class="sxs-lookup"><span data-stu-id="bb21c-107">dispidDLMembers</span></span>  <br/> |
|<span data-ttu-id="bb21c-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="bb21c-108">Property set:</span></span>  <br/> |<span data-ttu-id="bb21c-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="bb21c-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="bb21c-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="bb21c-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="bb21c-111">0x00008055</span><span class="sxs-lookup"><span data-stu-id="bb21c-111">0x00008055</span></span>  <br/> |
|<span data-ttu-id="bb21c-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="bb21c-112">Data type:</span></span>  <br/> |<span data-ttu-id="bb21c-113">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="bb21c-113">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="bb21c-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="bb21c-114">Area:</span></span>  <br/> |<span data-ttu-id="bb21c-115">Kontakt</span><span class="sxs-lookup"><span data-stu-id="bb21c-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bb21c-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bb21c-116">Remarks</span></span>

<span data-ttu-id="bb21c-117">Mitglieder der persönlichen Verteilerliste möglicherweise andere persönlichen Verteilerlisten, elektronische Adressen, die in einem Kontakt, Global Address List Benutzer oder Verteilerlisten oder einmaligen e-Mail-Adressen enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="bb21c-117">Members of the personal distribution list can be other personal distribution lists, electronic addresses contained in a contact, Global Address List users or distribution lists, or one-off email addresses.</span></span> <span data-ttu-id="bb21c-118">Das Format der einzelnen EntryId muss es sich um einen einmaligen Eintrags-ID, wie in [[MS-OXCDATA]](http://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx) angegeben oder eine gepackten EntryId sein.</span><span class="sxs-lookup"><span data-stu-id="bb21c-118">The format of each EntryId must be either a one-off EntryId, as specified in [[MS-OXCDATA],](http://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx) or a wrapped EntryId.</span></span> 
  
<span data-ttu-id="bb21c-119">Beim Festlegen dieser Eigenschaft muss der Client oder der Server sicher, dass die Gesamtgröße der kleiner als 15.000 Bytes.</span><span class="sxs-lookup"><span data-stu-id="bb21c-119">When setting this property, the client or the server must ensure its total size is less than 15,000 bytes.</span></span>
  
<span data-ttu-id="bb21c-120">Diese Eigenschaft gibt die Liste der einmaligen EntryIds, die die Elemente der persönlichen Verteilerliste entsprechen.</span><span class="sxs-lookup"><span data-stu-id="bb21c-120">This property specifies the list of one-off EntryIds that correspond to the members of the personal distribution list.</span></span> <span data-ttu-id="bb21c-121">Diese einmaligen EntryIds kapseln Anzeigenamen und e-Mail-Adressen der Mitglieder der persönlichen Verteilerliste.</span><span class="sxs-lookup"><span data-stu-id="bb21c-121">These one-off EntryIds encapsulate display names and email addresses of the personal distribution list members.</span></span>
  
<span data-ttu-id="bb21c-122">Wenn der Client oder der Server wird diese Eigenschaft festzulegen, müssen Sie mit dieser Eigenschaft **DispidDLMembers** für jeden Eintrag in der Eigenschaft **DispidDLOneOffMembers** ([PidLidDistributionListOneOffMembers](pidliddistributionlistoneoffmembers-canonical-property.md)) synchronisiert werden, muss ein Eintrag in der derselben Position in der **DispidDLOneOffMembers**.</span><span class="sxs-lookup"><span data-stu-id="bb21c-122">If the client or the server set this property, it must be synchronized with this property **dispidDLMembers** for each entry in the **dispidDLOneOffMembers** ([PidLidDistributionListOneOffMembers](pidliddistributionlistoneoffmembers-canonical-property.md)) property, there must be an entry in the same position in the **dispidDLOneOffMembers**.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="bb21c-123">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="bb21c-123">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="bb21c-124">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="bb21c-124">Protocol specifications</span></span>

<span data-ttu-id="bb21c-125">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bb21c-125">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bb21c-126">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="bb21c-126">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="bb21c-127">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bb21c-127">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bb21c-128">Gibt die Eigenschaften und Operationen, die für Kontakte und persönliche Verteilerlisten zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="bb21c-128">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="bb21c-129">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="bb21c-129">Header files</span></span>

<span data-ttu-id="bb21c-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bb21c-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="bb21c-131">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="bb21c-131">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bb21c-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bb21c-132">See also</span></span>



[<span data-ttu-id="bb21c-133">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="bb21c-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bb21c-134">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="bb21c-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bb21c-135">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="bb21c-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bb21c-136">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="bb21c-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

