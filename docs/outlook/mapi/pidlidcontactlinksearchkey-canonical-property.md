---
title: Kanonische Pidlidcontactlinksearchkey (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidContactLinkSearchKey
api_type:
- COM
ms.assetid: 82d21d38-a6c6-4e12-85b1-8158b2f5cce7
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: ea815631f63b5585a3f2705cfbd2639b8c655e6e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319775"
---
# <a name="pidlidcontactlinksearchkey-canonical-property"></a><span data-ttu-id="79324-103">Kanonische Pidlidcontactlinksearchkey (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="79324-103">PidLidContactLinkSearchKey Canonical Property</span></span>

<span data-ttu-id="79324-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="79324-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="79324-105">Enthält die Liste der **SearchKeys** für den Kontakt, der mit diesem Nachrichtenobjekt verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="79324-105">Contains the list of **SearchKeys** for the contact linked to by this message object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="79324-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="79324-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="79324-107">dispidContactLinkSearchKey</span><span class="sxs-lookup"><span data-stu-id="79324-107">dispidContactLinkSearchKey</span></span>  <br/> |
|<span data-ttu-id="79324-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="79324-108">Property set:</span></span>  <br/> |<span data-ttu-id="79324-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="79324-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="79324-110">Long-ID (Deckel):</span><span class="sxs-lookup"><span data-stu-id="79324-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="79324-111">0x00008584</span><span class="sxs-lookup"><span data-stu-id="79324-111">0x00008584</span></span>  <br/> |
|<span data-ttu-id="79324-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="79324-112">Data type:</span></span>  <br/> |<span data-ttu-id="79324-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="79324-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="79324-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="79324-114">Area:</span></span>  <br/> |<span data-ttu-id="79324-115">Kontakt</span><span class="sxs-lookup"><span data-stu-id="79324-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="79324-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="79324-116">Remarks</span></span>

|<span data-ttu-id="79324-117">**Länge in Byte**</span><span class="sxs-lookup"><span data-stu-id="79324-117">**Length in bytes**</span></span>|<span data-ttu-id="79324-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="79324-118">**Description**</span></span>|<span data-ttu-id="79324-119">**Hinweise**</span><span class="sxs-lookup"><span data-stu-id="79324-119">**Notes**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="79324-120">2</span><span class="sxs-lookup"><span data-stu-id="79324-120">2</span></span>  <br/> |<span data-ttu-id="79324-121">ContactEntryCount</span><span class="sxs-lookup"><span data-stu-id="79324-121">ContactEntryCount</span></span>  <br/> |<span data-ttu-id="79324-122">Keine</span><span class="sxs-lookup"><span data-stu-id="79324-122">None</span></span>  <br/> |
|<span data-ttu-id="79324-123">Variable</span><span class="sxs-lookup"><span data-stu-id="79324-123">variable</span></span>  <br/> |<span data-ttu-id="79324-124">SearchKey-Daten</span><span class="sxs-lookup"><span data-stu-id="79324-124">SearchKey data</span></span>  <br/> |<span data-ttu-id="79324-125">Wiederholt ContactEntryCount-mal</span><span class="sxs-lookup"><span data-stu-id="79324-125">Repeats ContactEntryCount times</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="79324-126">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="79324-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="79324-127">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="79324-127">Protocol specifications</span></span>

<span data-ttu-id="79324-128">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="79324-128">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="79324-129">Stellt Eigenschaftensatz Definitionen und Verweise auf zugehörige Exchange Server-Protokollspezifikationen bereit.</span><span class="sxs-lookup"><span data-stu-id="79324-129">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="79324-130">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="79324-130">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="79324-131">Verarbeitet Nachrichten-und Anlagenobjekte.</span><span class="sxs-lookup"><span data-stu-id="79324-131">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="79324-132">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="79324-132">Header files</span></span>

<span data-ttu-id="79324-133">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="79324-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="79324-134">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="79324-134">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="79324-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="79324-135">See also</span></span>

- [<span data-ttu-id="79324-136">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="79324-136">MAPI Properties</span></span>](mapi-properties.md) 
- [<span data-ttu-id="79324-137">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="79324-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
- [<span data-ttu-id="79324-138">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="79324-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
- [<span data-ttu-id="79324-139">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="79324-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

