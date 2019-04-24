---
title: Kanonische Pidtaglistunsubscribe (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagListUnsubscribe
api_type:
- HeaderDef
ms.assetid: 4e6bfbc7-7586-43cc-9380-daa0fe3d85a5
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: e057ab2ca0c75d5c0d749ebde8f1bdfb4f1ae66a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278879"
---
# <a name="pidtaglistunsubscribe-canonical-property"></a><span data-ttu-id="15c26-103">Kanonische Pidtaglistunsubscribe (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="15c26-103">PidTagListUnsubscribe Canonical Property</span></span>

  
  
<span data-ttu-id="15c26-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="15c26-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="15c26-105">Enthält den Wert einer MIME-Nachricht (Multipurpose Internet Mail Extensions) Liste-unsubscribe-Kopfzeilenfeld.</span><span class="sxs-lookup"><span data-stu-id="15c26-105">Contains the value of a Multipurpose Internet Mail Extensions (MIME) message's List-Unsubscribe header field.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="15c26-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="15c26-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="15c26-107">PR_LIST_UNSUBSCRIBE, PR_LIST_UNSUBSCRIBE_A, PR_LIST_UNSUBSCRIBE_W</span><span class="sxs-lookup"><span data-stu-id="15c26-107">PR_LIST_UNSUBSCRIBE, PR_LIST_UNSUBSCRIBE_A, PR_LIST_UNSUBSCRIBE_W</span></span>  <br/> |
|<span data-ttu-id="15c26-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="15c26-108">Identifier:</span></span>  <br/> |<span data-ttu-id="15c26-109">0x1045</span><span class="sxs-lookup"><span data-stu-id="15c26-109">0x1045</span></span>  <br/> |
|<span data-ttu-id="15c26-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="15c26-110">Data type:</span></span>  <br/> |<span data-ttu-id="15c26-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="15c26-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="15c26-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="15c26-112">Area:</span></span>  <br/> |<span data-ttu-id="15c26-113">Sonstiges</span><span class="sxs-lookup"><span data-stu-id="15c26-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="15c26-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="15c26-114">Remarks</span></span>

<span data-ttu-id="15c26-115">Um ein Listen-unsubscribe-Kopfzeilenfeld zu generieren, müssen Clients diese Eigenschaften auf den gewünschten Wert festlegen.</span><span class="sxs-lookup"><span data-stu-id="15c26-115">To generate a List-Unsubscribe header field, clients must set these properties to the desired value.</span></span> <span data-ttu-id="15c26-116">MIME-Writer müssen den Wert dieser Eigenschaften in das Kopfzeilenfeld List-unsubscribe kopieren.</span><span class="sxs-lookup"><span data-stu-id="15c26-116">MIME writers must copy the value of these properties to the List-Unsubscribe header field.</span></span>
  
<span data-ttu-id="15c26-117">Um den Wert dieser Listenserver bezogenen Eigenschaften festzulegen, müssen MIME-Clients die in der folgenden Tabelle angegebenen Kopfzeilenfelder schreiben.</span><span class="sxs-lookup"><span data-stu-id="15c26-117">To set the value of these list server-related properties, MIME clients must write the header fields as specified in the following table.</span></span>
  
|<span data-ttu-id="15c26-118">**Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="15c26-118">**Property**</span></span>|<span data-ttu-id="15c26-119">**Bevorzugter Kopfzeilen Feldname**</span><span class="sxs-lookup"><span data-stu-id="15c26-119">**Preferred header field name**</span></span>|<span data-ttu-id="15c26-120">**Name des alternativen Kopfzeilenfelds**</span><span class="sxs-lookup"><span data-stu-id="15c26-120">**Alternate header field name**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="15c26-121">**PR_LIST_UNSUBSCRIBE**</span><span class="sxs-lookup"><span data-stu-id="15c26-121">**PR_LIST_UNSUBSCRIBE**</span></span> <br/> |<span data-ttu-id="15c26-122">Liste-unsubscribe</span><span class="sxs-lookup"><span data-stu-id="15c26-122">List-Unsubscribe</span></span>  <br/> |<span data-ttu-id="15c26-123">X-List-unsubscribe</span><span class="sxs-lookup"><span data-stu-id="15c26-123">X-List-Unsubscribe</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="15c26-124">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="15c26-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="15c26-125">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="15c26-125">Protocol specifications</span></span>

<span data-ttu-id="15c26-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="15c26-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="15c26-127">Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="15c26-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="15c26-128">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="15c26-128">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="15c26-129">Konvertiert von Internet Standard-e-Mail-Konventionen in Nachrichtenobjekte.</span><span class="sxs-lookup"><span data-stu-id="15c26-129">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="15c26-130">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="15c26-130">Header files</span></span>

<span data-ttu-id="15c26-131">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="15c26-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="15c26-132">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="15c26-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="15c26-133">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="15c26-133">Mapitags.h</span></span>
  
> <span data-ttu-id="15c26-134">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="15c26-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="15c26-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="15c26-135">See also</span></span>



[<span data-ttu-id="15c26-136">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="15c26-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="15c26-137">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="15c26-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="15c26-138">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="15c26-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="15c26-139">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="15c26-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

