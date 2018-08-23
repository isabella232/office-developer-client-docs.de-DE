---
title: PidTagReportName (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 3c1a848eec84c7d81792a95baa3f47fa6779e95f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569582"
---
# <a name="pidtagreportname-canonical-property"></a><span data-ttu-id="5eea5-103">PidTagReportName (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="5eea5-103">PidTagReportName Canonical Property</span></span>

  
  
<span data-ttu-id="5eea5-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5eea5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5eea5-105">Enthält den Anzeigenamen für den Empfänger, der Berichte für diese Nachricht erhalten soll.</span><span class="sxs-lookup"><span data-stu-id="5eea5-105">Contains the display name for the recipient that should get reports for this message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5eea5-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="5eea5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5eea5-107">PR_REPORT_NAME, PR_REPORT_NAME_A, PR_REPORT_NAME_W</span><span class="sxs-lookup"><span data-stu-id="5eea5-107">PR_REPORT_NAME, PR_REPORT_NAME_A, PR_REPORT_NAME_W</span></span>  <br/> |
|<span data-ttu-id="5eea5-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="5eea5-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5eea5-109">0x003A</span><span class="sxs-lookup"><span data-stu-id="5eea5-109">0x003A</span></span>  <br/> |
|<span data-ttu-id="5eea5-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="5eea5-110">Data type:</span></span>  <br/> |<span data-ttu-id="5eea5-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="5eea5-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="5eea5-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="5eea5-112">Area:</span></span>  <br/> |<span data-ttu-id="5eea5-113">MAPI-Umschlag</span><span class="sxs-lookup"><span data-stu-id="5eea5-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5eea5-114">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="5eea5-114">Remarks</span></span>

<span data-ttu-id="5eea5-115">Diese Eigenschaften sind Beispiele für die Adresseigenschaften für den Empfänger, den alle für diese Nachricht generierten Berichte empfangen der Absender delegiert wurde.</span><span class="sxs-lookup"><span data-stu-id="5eea5-115">These properties are examples of the address properties for the recipient that the sender has delegated to receive any reports generated for this message.</span></span>
  
<span data-ttu-id="5eea5-116">Eine Clientanwendung, die Berichte an einen anderen Benutzer weitergeleitet werden muss, sollten diese Eigenschaften Zeitpunkt der Übermittlung von Nachricht festlegen.</span><span class="sxs-lookup"><span data-stu-id="5eea5-116">A client application that must route reports to another user should set these properties at message submission time.</span></span> <span data-ttu-id="5eea5-117">Wenn sie nicht festgelegt sind, werden die Berichte an den Absender der Nachricht gesendet.</span><span class="sxs-lookup"><span data-stu-id="5eea5-117">If they are not set, the reports are sent to the message sender.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="5eea5-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="5eea5-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="5eea5-119">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="5eea5-119">Header files</span></span>

<span data-ttu-id="5eea5-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5eea5-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="5eea5-121">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="5eea5-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="5eea5-122">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="5eea5-122">Mapitags.h</span></span>
  
> <span data-ttu-id="5eea5-123">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="5eea5-123">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5eea5-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5eea5-124">See also</span></span>



[<span data-ttu-id="5eea5-125">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5eea5-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5eea5-126">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5eea5-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5eea5-127">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="5eea5-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5eea5-128">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="5eea5-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

