---
title: PidTagReportSearchKey (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 889b43bb606cbe9c96d52c8a21ffda5dfcebb1da
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359178"
---
# <a name="pidtagreportsearchkey-canonical-property"></a><span data-ttu-id="2104c-103">PidTagReportSearchKey (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="2104c-103">PidTagReportSearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="2104c-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2104c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2104c-105">Enthält den Suchschlüssel für den Empfänger, der Berichte für diese Nachricht erhalten soll.</span><span class="sxs-lookup"><span data-stu-id="2104c-105">Contains the search key for the recipient that should get reports for this message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2104c-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="2104c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2104c-107">PR_REPORT_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="2104c-107">PR_REPORT_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="2104c-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="2104c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2104c-109">0x0054</span><span class="sxs-lookup"><span data-stu-id="2104c-109">0x0054</span></span>  <br/> |
|<span data-ttu-id="2104c-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="2104c-110">Data type:</span></span>  <br/> |<span data-ttu-id="2104c-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="2104c-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="2104c-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="2104c-112">Area:</span></span>  <br/> |<span data-ttu-id="2104c-113">MAPI-Umschlag</span><span class="sxs-lookup"><span data-stu-id="2104c-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2104c-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2104c-114">Remarks</span></span>

<span data-ttu-id="2104c-115">Diese Eigenschaft ist eine der Adresseigenschaften für den Empfänger, den der Absender delegiert hat, um berichte zu empfangen, die für diese Nachricht generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="2104c-115">This property is one of the address properties for the recipient that the sender has delegated to receive any reports generated for this message.</span></span>
  
<span data-ttu-id="2104c-116">Eine Clientanwendung, die Berichte an einen anderen Benutzer weiter routen muss, sollte diese Eigenschaft zum Zeitpunkt der Nachrichtenübermittlung festlegen.</span><span class="sxs-lookup"><span data-stu-id="2104c-116">A client application that must route reports to another user should set this property at message submission time.</span></span> <span data-ttu-id="2104c-117">Wenn er nicht festgelegt ist, werden die Berichte an den Nachrichtensender gesendet.</span><span class="sxs-lookup"><span data-stu-id="2104c-117">If it is not set, the reports are sent to the message sender.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="2104c-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="2104c-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="2104c-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="2104c-119">Protocol specifications</span></span>

<span data-ttu-id="2104c-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2104c-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2104c-121">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="2104c-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="2104c-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2104c-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2104c-123">Gibt die Eigenschaften und Vorgänge an, die für E-Mail-Nachrichten zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="2104c-123">Specifies the properties and operations that are permissible on email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="2104c-124">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="2104c-124">Header files</span></span>

<span data-ttu-id="2104c-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2104c-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="2104c-126">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="2104c-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="2104c-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="2104c-127">Mapitags.h</span></span>
  
> <span data-ttu-id="2104c-128">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="2104c-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2104c-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2104c-129">See also</span></span>



[<span data-ttu-id="2104c-130">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2104c-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2104c-131">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="2104c-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2104c-132">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="2104c-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2104c-133">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="2104c-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

