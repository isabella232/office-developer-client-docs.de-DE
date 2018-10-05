---
title: PidLidBusinessCardDisplayDefinition (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidBusinessCardDisplayDefinition
api_type:
- COM
ms.assetid: c0b956dd-7139-49e3-a32a-d70bfb11e0b1
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: f25f8a538ff61bc7e04c234efd7404b1c866d64d
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399102"
---
# <a name="pidlidbusinesscarddisplaydefinition-canonical-property"></a><span data-ttu-id="b71b5-103">PidLidBusinessCardDisplayDefinition (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="b71b5-103">PidLidBusinessCardDisplayDefinition Canonical Property</span></span>

  
  
<span data-ttu-id="b71b5-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b71b5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b71b5-105">Enthält benutzeranpassungen Details für einen Kontakt als Visitenkarte anzeigen.</span><span class="sxs-lookup"><span data-stu-id="b71b5-105">Contains user-customization details for displaying a contact as a business card.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b71b5-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="b71b5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b71b5-107">dispidBCDisplayDefinition</span><span class="sxs-lookup"><span data-stu-id="b71b5-107">dispidBCDisplayDefinition</span></span>  <br/> |
|<span data-ttu-id="b71b5-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="b71b5-108">Property set:</span></span>  <br/> |<span data-ttu-id="b71b5-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="b71b5-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="b71b5-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="b71b5-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="b71b5-111">0x00008040</span><span class="sxs-lookup"><span data-stu-id="b71b5-111">0x00008040</span></span>  <br/> |
|<span data-ttu-id="b71b5-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="b71b5-112">Data type:</span></span>  <br/> |<span data-ttu-id="b71b5-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="b71b5-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="b71b5-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="b71b5-114">Area:</span></span>  <br/> |<span data-ttu-id="b71b5-115">Kontakt</span><span class="sxs-lookup"><span data-stu-id="b71b5-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b71b5-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b71b5-116">Remarks</span></span>

<span data-ttu-id="b71b5-117">Das Layout einer Visitenkarte kann als ein Bild und eine Reihe von Textfeldern dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="b71b5-117">The layout of a business card can be represented as an image and a number of text fields.</span></span> <span data-ttu-id="b71b5-118">Das Bild kann entweder ein Foto des Kontakts oder ein Bild der Visitenkarte sein.</span><span class="sxs-lookup"><span data-stu-id="b71b5-118">The image can be either a contact photo, or a card picture.</span></span> <span data-ttu-id="b71b5-119">Textfelder bestehen einen Wert aus einer anderen-Eigenschaft auf den Kontakt festlegen und eine optionale benutzerdefinierte Bezeichnung-Zeichenfolge, die vom Benutzer bereitgestellten.</span><span class="sxs-lookup"><span data-stu-id="b71b5-119">Text fields consist of a value from another property set on the contact and an optional customized label string provided by the user.</span></span> <span data-ttu-id="b71b5-120">Beachten Sie, dass Sie Multibyte-Werte in little-Endian-Format im Puffer gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="b71b5-120">Note that multi-byte values are stored in little-endian format in the buffer.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="b71b5-121">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="b71b5-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b71b5-122">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="b71b5-122">Protocol specifications</span></span>

<span data-ttu-id="b71b5-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b71b5-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b71b5-124">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="b71b5-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b71b5-125">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b71b5-125">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b71b5-126">Gibt die Eigenschaften und Operationen, die für Kontakte und persönliche Verteilerlisten zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="b71b5-126">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b71b5-127">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="b71b5-127">Header files</span></span>

<span data-ttu-id="b71b5-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b71b5-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="b71b5-129">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="b71b5-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b71b5-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b71b5-130">See also</span></span>



[<span data-ttu-id="b71b5-131">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b71b5-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b71b5-132">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b71b5-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b71b5-133">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="b71b5-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b71b5-134">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="b71b5-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

