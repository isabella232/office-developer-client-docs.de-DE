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
ms.openlocfilehash: f04d1593e2a13a2bfc23412340d7eb9f38f5d9ef
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335070"
---
# <a name="pidliddistributionlistmembers-canonical-property"></a><span data-ttu-id="15b6c-103">PidLidDistributionListMembers (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="15b6c-103">PidLidDistributionListMembers Canonical Property</span></span>

  
  
<span data-ttu-id="15b6c-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="15b6c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="15b6c-105">Gibt die Liste der EntryIds der Objekte an, die den Mitgliedern der persönlichen Verteilerliste entsprechen.</span><span class="sxs-lookup"><span data-stu-id="15b6c-105">Specifies the list of EntryIds of the objects that correspond to the members of the personal distribution list.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="15b6c-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="15b6c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="15b6c-107">dispidDLMembers</span><span class="sxs-lookup"><span data-stu-id="15b6c-107">dispidDLMembers</span></span>  <br/> |
|<span data-ttu-id="15b6c-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="15b6c-108">Property set:</span></span>  <br/> |<span data-ttu-id="15b6c-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="15b6c-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="15b6c-110">Lange ID (LID):</span><span class="sxs-lookup"><span data-stu-id="15b6c-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="15b6c-111">0x00008055</span><span class="sxs-lookup"><span data-stu-id="15b6c-111">0x00008055</span></span>  <br/> |
|<span data-ttu-id="15b6c-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="15b6c-112">Data type:</span></span>  <br/> |<span data-ttu-id="15b6c-113">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="15b6c-113">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="15b6c-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="15b6c-114">Area:</span></span>  <br/> |<span data-ttu-id="15b6c-115">Kontakt</span><span class="sxs-lookup"><span data-stu-id="15b6c-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="15b6c-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="15b6c-116">Remarks</span></span>

<span data-ttu-id="15b6c-117">Mitglieder der persönlichen Verteilerliste können andere persönliche Verteilerlisten, in einem Kontakt enthaltene elektronische Adressen, Globale Adresslistenbenutzer oder Verteilerlisten oder einmal E-Mail-Adressen sein.</span><span class="sxs-lookup"><span data-stu-id="15b6c-117">Members of the personal distribution list can be other personal distribution lists, electronic addresses contained in a contact, Global Address List users or distribution lists, or one-off email addresses.</span></span> <span data-ttu-id="15b6c-118">Das Format jeder EntryId muss entweder eine in [[MS-OXCDATA] angegebene one-off](https://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx) EntryId oder eine umschlossene EntryId sein.</span><span class="sxs-lookup"><span data-stu-id="15b6c-118">The format of each EntryId must be either a one-off EntryId, as specified in [[MS-OXCDATA],](https://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx) or a wrapped EntryId.</span></span> 
  
<span data-ttu-id="15b6c-119">Beim Festlegen dieser Eigenschaft muss der Client oder der Server sicherstellen, dass die Gesamtgröße weniger als 15.000 Byte beträgt.</span><span class="sxs-lookup"><span data-stu-id="15b6c-119">When setting this property, the client or the server must ensure its total size is less than 15,000 bytes.</span></span>
  
<span data-ttu-id="15b6c-120">Diese Eigenschaft gibt die Liste der einmal verwendeten EntryIds an, die den Mitgliedern der persönlichen Verteilerliste entsprechen.</span><span class="sxs-lookup"><span data-stu-id="15b6c-120">This property specifies the list of one-off EntryIds that correspond to the members of the personal distribution list.</span></span> <span data-ttu-id="15b6c-121">Diese einmal verwendeten EntryIds kapseln Anzeigenamen und E-Mail-Adressen der Mitglieder der persönlichen Verteilerliste.</span><span class="sxs-lookup"><span data-stu-id="15b6c-121">These one-off EntryIds encapsulate display names and email addresses of the personal distribution list members.</span></span>
  
<span data-ttu-id="15b6c-122">Wenn der Client oder der Server diese Eigenschaft festlegen, muss sie mit dieser Eigenschaft **dispidDLMembers** für jeden Eintrag in der **dispidDLOneOffMembers** ([PidLidDistributionListOneOffMembers](pidliddistributionlistoneoffmembers-canonical-property.md))-Eigenschaft synchronisiert werden, es muss ein Eintrag an der gleichen Position in der **dispidDLOneOffMembers**-Eigenschaft vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="15b6c-122">If the client or the server set this property, it must be synchronized with this property **dispidDLMembers** for each entry in the **dispidDLOneOffMembers** ([PidLidDistributionListOneOffMembers](pidliddistributionlistoneoffmembers-canonical-property.md)) property, there must be an entry in the same position in the **dispidDLOneOffMembers**.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="15b6c-123">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="15b6c-123">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="15b6c-124">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="15b6c-124">Protocol specifications</span></span>

<span data-ttu-id="15b6c-125">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="15b6c-125">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="15b6c-126">Stellt Eigenschaftensatzdefinitionen und Verweise auf verwandte Exchange Server zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="15b6c-126">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="15b6c-127">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="15b6c-127">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="15b6c-128">Gibt die Eigenschaften und Vorgänge an, die für Kontakte und persönliche Verteilerlisten zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="15b6c-128">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="15b6c-129">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="15b6c-129">Header files</span></span>

<span data-ttu-id="15b6c-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="15b6c-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="15b6c-131">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="15b6c-131">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="15b6c-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="15b6c-132">See also</span></span>



[<span data-ttu-id="15b6c-133">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="15b6c-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="15b6c-134">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="15b6c-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="15b6c-135">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="15b6c-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="15b6c-136">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="15b6c-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

