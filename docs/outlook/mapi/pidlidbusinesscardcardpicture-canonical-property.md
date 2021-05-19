---
title: PidLidBusinessCardCardPicture (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidBusinessCardCardPicture
api_type:
- COM
ms.assetid: 2c7af147-f7eb-41ef-8403-93584a2041ba
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: fd1ad923acca5a75d06e6b15ae7ae7411edefb92
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342007"
---
# <a name="pidlidbusinesscardcardpicture-canonical-property"></a><span data-ttu-id="b21ee-103">PidLidBusinessCardCardPicture (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="b21ee-103">PidLidBusinessCardCardPicture Canonical Property</span></span>

  
  
<span data-ttu-id="b21ee-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b21ee-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b21ee-105">Enthält das Bild, das auf einer Visitenkarte verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b21ee-105">Contains the image to use on a business card.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b21ee-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="b21ee-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b21ee-107">dispidBCCardPicture</span><span class="sxs-lookup"><span data-stu-id="b21ee-107">dispidBCCardPicture</span></span>  <br/> |
|<span data-ttu-id="b21ee-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="b21ee-108">Property set:</span></span>  <br/> |<span data-ttu-id="b21ee-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="b21ee-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="b21ee-110">Lange ID (LID):</span><span class="sxs-lookup"><span data-stu-id="b21ee-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="b21ee-111">0x00008041</span><span class="sxs-lookup"><span data-stu-id="b21ee-111">0x00008041</span></span>  <br/> |
|<span data-ttu-id="b21ee-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="b21ee-112">Data type:</span></span>  <br/> |<span data-ttu-id="b21ee-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="b21ee-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="b21ee-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="b21ee-114">Area:</span></span>  <br/> |<span data-ttu-id="b21ee-115">Kontakt</span><span class="sxs-lookup"><span data-stu-id="b21ee-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b21ee-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b21ee-116">Remarks</span></span>

<span data-ttu-id="b21ee-117">Der Wert dieser Eigenschaft muss entweder eine portable Netzwerkgrafik (PNG) oder ein JPEG-Stream sein.</span><span class="sxs-lookup"><span data-stu-id="b21ee-117">The value of this property must be either a portable network graphics (PNG) or JPEG stream.</span></span> <span data-ttu-id="b21ee-118">Diese Eigenschaft sollte in Verbindung mit der **dispidBCDisplayDefinition** ([PidLidBusinessCardDisplayDefinition](pidlidbusinesscarddisplaydefinition-canonical-property.md)) -Eigenschaft wie folgt verwendet werden: **dispidBCCardPicture** sollte nicht in einem Kontakt vorhanden sein, wenn **dispidBCDisplayDefinition** nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="b21ee-118">This property should be used in conjunction with the **dispidBCDisplayDefinition** ([PidLidBusinessCardDisplayDefinition](pidlidbusinesscarddisplaydefinition-canonical-property.md)) property as follows: **dispidBCCardPicture** should not be present on a contact if **dispidBCDisplayDefinition** is not present.</span></span> <span data-ttu-id="b21ee-119">Diese Eigenschaft sollte auch nicht vorhanden sein, wenn die Daten in **dispidBCCardPicture** kein Kartenbild erfordern.</span><span class="sxs-lookup"><span data-stu-id="b21ee-119">This property also should not be present if the data in **dispidBCCardPicture** does not require a card image.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="b21ee-120">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="b21ee-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b21ee-121">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="b21ee-121">Protocol specifications</span></span>

<span data-ttu-id="b21ee-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b21ee-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b21ee-123">Stellt Eigenschaftensatzdefinitionen und Verweise auf verwandte Exchange Server zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="b21ee-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b21ee-124">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b21ee-124">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b21ee-125">Gibt die Eigenschaften und Vorgänge an, die für Kontakte und persönliche Verteilerlisten zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="b21ee-125">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b21ee-126">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="b21ee-126">Header files</span></span>

<span data-ttu-id="b21ee-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b21ee-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="b21ee-128">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="b21ee-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b21ee-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b21ee-129">See also</span></span>



[<span data-ttu-id="b21ee-130">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b21ee-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b21ee-131">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="b21ee-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b21ee-132">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="b21ee-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b21ee-133">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="b21ee-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

