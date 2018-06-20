---
title: Kanonische PidTagReportEntryId-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReportEntryId
api_type:
- COM
ms.assetid: ea2bcc06-0089-4999-b115-06a14de4a0f1
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: a1d81581afa3bb9df8bd7aded5c265dfa8f04676
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794961"
---
# <a name="pidtagreportentryid-canonical-property"></a><span data-ttu-id="74ad9-103">Kanonische PidTagReportEntryId-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="74ad9-103">PidTagReportEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="74ad9-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="74ad9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="74ad9-105">Enthält die Eintrags-ID für den Empfänger, der Berichte für diese Nachricht empfangen sollen.</span><span class="sxs-lookup"><span data-stu-id="74ad9-105">Contains the entry identifier for the recipient who should receive reports for this message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="74ad9-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="74ad9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="74ad9-107">PR_REPORT_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="74ad9-107">PR_REPORT_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="74ad9-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="74ad9-108">Identifier:</span></span>  <br/> |<span data-ttu-id="74ad9-109">0x0045</span><span class="sxs-lookup"><span data-stu-id="74ad9-109">0x0045</span></span>  <br/> |
|<span data-ttu-id="74ad9-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="74ad9-110">Data type:</span></span>  <br/> |<span data-ttu-id="74ad9-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="74ad9-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="74ad9-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="74ad9-112">Area:</span></span>  <br/> |<span data-ttu-id="74ad9-113">MAPI-Umschlag</span><span class="sxs-lookup"><span data-stu-id="74ad9-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="74ad9-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="74ad9-114">Remarks</span></span>

<span data-ttu-id="74ad9-115">Diese Eigenschaft ist eine der Adresseigenschaften für den Empfänger, Absender delegiert alle für diese Nachricht generierten Berichte empfangen hat.</span><span class="sxs-lookup"><span data-stu-id="74ad9-115">This property is one of the address properties for the recipient who the sender has delegated to receive any reports generated for this message.</span></span>
  
<span data-ttu-id="74ad9-116">Eine Clientanwendung, die Berichte an einen anderen Benutzer weitergeleitet werden muss, sollten diese Eigenschaft Zeitpunkt der Übermittlung von Nachricht festgelegt.</span><span class="sxs-lookup"><span data-stu-id="74ad9-116">A client application that must route reports to another user should set this property at message submission time.</span></span> <span data-ttu-id="74ad9-117">Wenn sie nicht festgelegt ist, werden die Berichte an den Absender der Nachricht gesendet.</span><span class="sxs-lookup"><span data-stu-id="74ad9-117">If it is not set, the reports are sent to the message sender.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="74ad9-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="74ad9-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="74ad9-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="74ad9-119">Protocol specifications</span></span>

<span data-ttu-id="74ad9-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="74ad9-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="74ad9-121">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="74ad9-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="74ad9-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="74ad9-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="74ad9-123">Gibt die Eigenschaften und Operationen, die für e-Mail-Nachrichten zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="74ad9-123">Specifies the properties and operations that are permissible on email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="74ad9-124">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="74ad9-124">Header files</span></span>

<span data-ttu-id="74ad9-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="74ad9-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="74ad9-126">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="74ad9-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="74ad9-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="74ad9-127">Mapitags.h</span></span>
  
> <span data-ttu-id="74ad9-128">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="74ad9-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="74ad9-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="74ad9-129">See also</span></span>



[<span data-ttu-id="74ad9-130">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="74ad9-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="74ad9-131">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="74ad9-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="74ad9-132">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="74ad9-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="74ad9-133">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="74ad9-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

