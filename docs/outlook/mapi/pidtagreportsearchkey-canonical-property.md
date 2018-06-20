---
title: Kanonische PidTagReportSearchKey-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReportSearchKey
api_type:
- COM
ms.assetid: d4f4c40b-b6a8-45f3-b750-07b92c535322
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: fa2770daf38fe93eb9fb69990eebc2a6fcfd6a27
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794979"
---
# <a name="pidtagreportsearchkey-canonical-property"></a><span data-ttu-id="2a903-103">Kanonische PidTagReportSearchKey-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="2a903-103">PidTagReportSearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="2a903-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2a903-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2a903-105">Enthält den Search-Schlüssel für den Empfänger, der Berichte für diese Nachricht erhalten soll.</span><span class="sxs-lookup"><span data-stu-id="2a903-105">Contains the search key for the recipient that should get reports for this message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2a903-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="2a903-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2a903-107">PR_REPORT_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="2a903-107">PR_REPORT_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="2a903-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="2a903-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2a903-109">0x0054</span><span class="sxs-lookup"><span data-stu-id="2a903-109">0x0054</span></span>  <br/> |
|<span data-ttu-id="2a903-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="2a903-110">Data type:</span></span>  <br/> |<span data-ttu-id="2a903-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="2a903-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="2a903-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="2a903-112">Area:</span></span>  <br/> |<span data-ttu-id="2a903-113">MAPI-Umschlag</span><span class="sxs-lookup"><span data-stu-id="2a903-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2a903-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2a903-114">Remarks</span></span>

<span data-ttu-id="2a903-115">Diese Eigenschaft ist eine der Adresseigenschaften für den Empfänger, den alle für diese Nachricht generierten Berichte empfangen der Absender delegiert wurde.</span><span class="sxs-lookup"><span data-stu-id="2a903-115">This property is one of the address properties for the recipient that the sender has delegated to receive any reports generated for this message.</span></span>
  
<span data-ttu-id="2a903-116">Eine Clientanwendung, die Berichte an einen anderen Benutzer weitergeleitet werden muss, sollten diese Eigenschaft Zeitpunkt der Übermittlung von Nachricht festgelegt.</span><span class="sxs-lookup"><span data-stu-id="2a903-116">A client application that must route reports to another user should set this property at message submission time.</span></span> <span data-ttu-id="2a903-117">Wenn sie nicht festgelegt ist, werden die Berichte an den Absender der Nachricht gesendet.</span><span class="sxs-lookup"><span data-stu-id="2a903-117">If it is not set, the reports are sent to the message sender.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="2a903-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="2a903-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="2a903-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="2a903-119">Protocol specifications</span></span>

<span data-ttu-id="2a903-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2a903-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2a903-121">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="2a903-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="2a903-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2a903-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2a903-123">Gibt die Eigenschaften und Operationen, die für e-Mail-Nachrichten zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="2a903-123">Specifies the properties and operations that are permissible on email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="2a903-124">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="2a903-124">Header files</span></span>

<span data-ttu-id="2a903-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2a903-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="2a903-126">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="2a903-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="2a903-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="2a903-127">Mapitags.h</span></span>
  
> <span data-ttu-id="2a903-128">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="2a903-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2a903-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2a903-129">See also</span></span>



[<span data-ttu-id="2a903-130">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2a903-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2a903-131">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2a903-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2a903-132">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="2a903-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2a903-133">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="2a903-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

