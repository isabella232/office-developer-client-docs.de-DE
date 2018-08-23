---
title: PidTagListUnsubscribe (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 1a4011a22f1029cc4002d4506eb4d335bd280bec
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593438"
---
# <a name="pidtaglistunsubscribe-canonical-property"></a><span data-ttu-id="b11c3-103">PidTagListUnsubscribe (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="b11c3-103">PidTagListUnsubscribe Canonical Property</span></span>

  
  
<span data-ttu-id="b11c3-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b11c3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b11c3-105">Enthält den Wert der Liste abmelden Header ein Feld einer Nachricht Multipurpose Internet Mail Extensions (MIME).</span><span class="sxs-lookup"><span data-stu-id="b11c3-105">Contains the value of a Multipurpose Internet Mail Extensions (MIME) message's List-Unsubscribe header field.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b11c3-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="b11c3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b11c3-107">PR_LIST_UNSUBSCRIBE, PR_LIST_UNSUBSCRIBE_A, PR_LIST_UNSUBSCRIBE_W</span><span class="sxs-lookup"><span data-stu-id="b11c3-107">PR_LIST_UNSUBSCRIBE, PR_LIST_UNSUBSCRIBE_A, PR_LIST_UNSUBSCRIBE_W</span></span>  <br/> |
|<span data-ttu-id="b11c3-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="b11c3-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b11c3-109">0x1045</span><span class="sxs-lookup"><span data-stu-id="b11c3-109">0x1045</span></span>  <br/> |
|<span data-ttu-id="b11c3-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="b11c3-110">Data type:</span></span>  <br/> |<span data-ttu-id="b11c3-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="b11c3-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="b11c3-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="b11c3-112">Area:</span></span>  <br/> |<span data-ttu-id="b11c3-113">Verschiedenes</span><span class="sxs-lookup"><span data-stu-id="b11c3-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b11c3-114">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="b11c3-114">Remarks</span></span>

<span data-ttu-id="b11c3-115">Um eine Liste abmelden Kopfzeilenfeld generiert werden soll, müssen die Clients diese Eigenschaften auf den gewünschten Wert festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b11c3-115">To generate a List-Unsubscribe header field, clients must set these properties to the desired value.</span></span> <span data-ttu-id="b11c3-116">MIME-Writer müssen den Wert dieser Eigenschaften in der Liste abmelden Kopfzeilenfeld kopieren.</span><span class="sxs-lookup"><span data-stu-id="b11c3-116">MIME writers must copy the value of these properties to the List-Unsubscribe header field.</span></span>
  
<span data-ttu-id="b11c3-117">Wenn den Wert dieser Liste Server-bezogene Eigenschaften festlegen möchten, müssen MIME-Clients die Kopfzeile Felder wie in der folgenden Tabelle angegebenen schreiben.</span><span class="sxs-lookup"><span data-stu-id="b11c3-117">To set the value of these list server-related properties, MIME clients must write the header fields as specified in the following table.</span></span>
  
|<span data-ttu-id="b11c3-118">**Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="b11c3-118">**Property**</span></span>|<span data-ttu-id="b11c3-119">**Bevorzugte Header-Feldname**</span><span class="sxs-lookup"><span data-stu-id="b11c3-119">**Preferred header field name**</span></span>|<span data-ttu-id="b11c3-120">**Alternative Header-Feldname**</span><span class="sxs-lookup"><span data-stu-id="b11c3-120">**Alternate header field name**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b11c3-121">**PR_LIST_UNSUBSCRIBE**</span><span class="sxs-lookup"><span data-stu-id="b11c3-121">**PR_LIST_UNSUBSCRIBE**</span></span> <br/> |<span data-ttu-id="b11c3-122">Liste sich abzumelden</span><span class="sxs-lookup"><span data-stu-id="b11c3-122">List-Unsubscribe</span></span>  <br/> |<span data-ttu-id="b11c3-123">X-Liste abmelden</span><span class="sxs-lookup"><span data-stu-id="b11c3-123">X-List-Unsubscribe</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="b11c3-124">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="b11c3-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b11c3-125">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="b11c3-125">Protocol specifications</span></span>

<span data-ttu-id="b11c3-126">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b11c3-126">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b11c3-127">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="b11c3-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b11c3-128">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b11c3-128">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b11c3-129">Konvertiert von Internet-standard-e-Mail-Konventionen in Message-Objekten.</span><span class="sxs-lookup"><span data-stu-id="b11c3-129">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b11c3-130">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="b11c3-130">Header files</span></span>

<span data-ttu-id="b11c3-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b11c3-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="b11c3-132">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="b11c3-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="b11c3-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="b11c3-133">Mapitags.h</span></span>
  
> <span data-ttu-id="b11c3-134">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="b11c3-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b11c3-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b11c3-135">See also</span></span>



[<span data-ttu-id="b11c3-136">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b11c3-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b11c3-137">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b11c3-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b11c3-138">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="b11c3-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b11c3-139">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="b11c3-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

