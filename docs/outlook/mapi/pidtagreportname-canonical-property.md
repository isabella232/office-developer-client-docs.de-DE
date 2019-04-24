---
title: Kanonische Pidtagreportname (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReportName
api_type:
- COM
ms.assetid: 4ec3100f-7cf1-4702-b326-e6da586a7bb2
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 33a7545f9b2719615617d46e2d5ed1f6952b5522
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335427"
---
# <a name="pidtagreportname-canonical-property"></a><span data-ttu-id="55fde-103">Kanonische Pidtagreportname (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="55fde-103">PidTagReportName Canonical Property</span></span>

  
  
<span data-ttu-id="55fde-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="55fde-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="55fde-105">Enthält den Anzeigenamen für den Empfänger, der Berichte für diese Nachricht erhalten soll.</span><span class="sxs-lookup"><span data-stu-id="55fde-105">Contains the display name for the recipient that should get reports for this message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="55fde-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="55fde-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="55fde-107">PR_REPORT_NAME, PR_REPORT_NAME_A, PR_REPORT_NAME_W</span><span class="sxs-lookup"><span data-stu-id="55fde-107">PR_REPORT_NAME, PR_REPORT_NAME_A, PR_REPORT_NAME_W</span></span>  <br/> |
|<span data-ttu-id="55fde-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="55fde-108">Identifier:</span></span>  <br/> |<span data-ttu-id="55fde-109">0x003A</span><span class="sxs-lookup"><span data-stu-id="55fde-109">0x003A</span></span>  <br/> |
|<span data-ttu-id="55fde-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="55fde-110">Data type:</span></span>  <br/> |<span data-ttu-id="55fde-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="55fde-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="55fde-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="55fde-112">Area:</span></span>  <br/> |<span data-ttu-id="55fde-113">MAPI-Umschlag</span><span class="sxs-lookup"><span data-stu-id="55fde-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="55fde-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="55fde-114">Remarks</span></span>

<span data-ttu-id="55fde-115">Diese Eigenschaften sind Beispiele für die Adresseigenschaften des Empfängers, an den der Absender delegiert wurde, um alle für diese Nachricht generierten Berichte zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="55fde-115">These properties are examples of the address properties for the recipient that the sender has delegated to receive any reports generated for this message.</span></span>
  
<span data-ttu-id="55fde-116">Eine Clientanwendung, die Berichte an einen anderen Benutzer weiterleiten muss, sollte diese Eigenschaften bei der Nachrichten Übermittlungszeit festlegen.</span><span class="sxs-lookup"><span data-stu-id="55fde-116">A client application that must route reports to another user should set these properties at message submission time.</span></span> <span data-ttu-id="55fde-117">Wenn Sie nicht festgelegt sind, werden die Berichte an den Absender der Nachricht gesendet.</span><span class="sxs-lookup"><span data-stu-id="55fde-117">If they are not set, the reports are sent to the message sender.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="55fde-118">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="55fde-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="55fde-119">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="55fde-119">Header files</span></span>

<span data-ttu-id="55fde-120">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="55fde-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="55fde-121">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="55fde-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="55fde-122">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="55fde-122">Mapitags.h</span></span>
  
> <span data-ttu-id="55fde-123">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="55fde-123">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="55fde-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="55fde-124">See also</span></span>



[<span data-ttu-id="55fde-125">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="55fde-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="55fde-126">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="55fde-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="55fde-127">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="55fde-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="55fde-128">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="55fde-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

