---
title: Kanonische Pidliddistributionlistmembers (-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: f04d1593e2a13a2bfc23412340d7eb9f38f5d9ef
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335070"
---
# <a name="pidliddistributionlistmembers-canonical-property"></a><span data-ttu-id="0f952-103">Kanonische Pidliddistributionlistmembers (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="0f952-103">PidLidDistributionListMembers Canonical Property</span></span>

  
  
<span data-ttu-id="0f952-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0f952-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0f952-105">Gibt die Liste der EntryIds der Objekte an, die den Mitgliedern der persönlichen Verteilerliste entsprechen.</span><span class="sxs-lookup"><span data-stu-id="0f952-105">Specifies the list of EntryIds of the objects that correspond to the members of the personal distribution list.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0f952-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="0f952-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0f952-107">dispidDLMembers</span><span class="sxs-lookup"><span data-stu-id="0f952-107">dispidDLMembers</span></span>  <br/> |
|<span data-ttu-id="0f952-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="0f952-108">Property set:</span></span>  <br/> |<span data-ttu-id="0f952-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="0f952-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="0f952-110">Long-ID (Deckel):</span><span class="sxs-lookup"><span data-stu-id="0f952-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="0f952-111">0x00008055</span><span class="sxs-lookup"><span data-stu-id="0f952-111">0x00008055</span></span>  <br/> |
|<span data-ttu-id="0f952-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="0f952-112">Data type:</span></span>  <br/> |<span data-ttu-id="0f952-113">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="0f952-113">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="0f952-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="0f952-114">Area:</span></span>  <br/> |<span data-ttu-id="0f952-115">Kontakt</span><span class="sxs-lookup"><span data-stu-id="0f952-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0f952-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0f952-116">Remarks</span></span>

<span data-ttu-id="0f952-117">Mitglieder der persönlichen Verteilerliste können andere persönliche Verteilerlisten, Elektronische Adressen in einem Kontakt, globale Adresslisten Benutzer oder Verteilerlisten oder einmalige e-Mail-Adressen sein.</span><span class="sxs-lookup"><span data-stu-id="0f952-117">Members of the personal distribution list can be other personal distribution lists, electronic addresses contained in a contact, Global Address List users or distribution lists, or one-off email addresses.</span></span> <span data-ttu-id="0f952-118">Das Format jeder Eintrags-Nr. muss eine einmalige Eintrags-oder Eingabe-Nr sein, wie in [[MS-OXCDATA] angegeben,](https://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx) oder eine einGebundene Eintrags-Nr.</span><span class="sxs-lookup"><span data-stu-id="0f952-118">The format of each EntryId must be either a one-off EntryId, as specified in [[MS-OXCDATA],](https://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx) or a wrapped EntryId.</span></span> 
  
<span data-ttu-id="0f952-119">Beim Festlegen dieser Eigenschaft muss der Client oder der Server sicherstellen, dass die Gesamtgröße kleiner als 15.000 Byte ist.</span><span class="sxs-lookup"><span data-stu-id="0f952-119">When setting this property, the client or the server must ensure its total size is less than 15,000 bytes.</span></span>
  
<span data-ttu-id="0f952-120">Diese Eigenschaft gibt die Liste der einmaligen EntryIds an, die den Mitgliedern der persönlichen Verteilerliste entsprechen.</span><span class="sxs-lookup"><span data-stu-id="0f952-120">This property specifies the list of one-off EntryIds that correspond to the members of the personal distribution list.</span></span> <span data-ttu-id="0f952-121">Diese einmalige EntryIds Kapseln Anzeigenamen und e-Mail-Adressen der Mitglieder der persönlichen Verteilerliste.</span><span class="sxs-lookup"><span data-stu-id="0f952-121">These one-off EntryIds encapsulate display names and email addresses of the personal distribution list members.</span></span>
  
<span data-ttu-id="0f952-122">Wenn der Client oder der Server diese Eigenschaft festlegen, muss Sie mit dieser Eigenschaft **dispidDLMembers** für jeden Eintrag in der **dispidDLOneOffMembers** ([pidliddistributionlistoneoffmembers (](pidliddistributionlistoneoffmembers-canonical-property.md))-Eigenschaft synchronisiert werden, es muss einen Eintrag in der dieselbe Position in der **dispidDLOneOffMembers**.</span><span class="sxs-lookup"><span data-stu-id="0f952-122">If the client or the server set this property, it must be synchronized with this property **dispidDLMembers** for each entry in the **dispidDLOneOffMembers** ([PidLidDistributionListOneOffMembers](pidliddistributionlistoneoffmembers-canonical-property.md)) property, there must be an entry in the same position in the **dispidDLOneOffMembers**.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="0f952-123">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="0f952-123">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0f952-124">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="0f952-124">Protocol specifications</span></span>

<span data-ttu-id="0f952-125">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0f952-125">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0f952-126">Stellt Eigenschaftensatz Definitionen und Verweise auf zugehörige Exchange Server-Protokollspezifikationen bereit.</span><span class="sxs-lookup"><span data-stu-id="0f952-126">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0f952-127">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0f952-127">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0f952-128">Gibt die Eigenschaften und Vorgänge an, die für Kontakte und persönliche Verteilerlisten zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="0f952-128">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0f952-129">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="0f952-129">Header files</span></span>

<span data-ttu-id="0f952-130">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="0f952-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="0f952-131">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="0f952-131">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0f952-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0f952-132">See also</span></span>



[<span data-ttu-id="0f952-133">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0f952-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0f952-134">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0f952-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0f952-135">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="0f952-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0f952-136">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="0f952-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

