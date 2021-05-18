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
ms.openlocfilehash: 33a7545f9b2719615617d46e2d5ed1f6952b5522
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422313"
---
# <a name="pidtagreportname-canonical-property"></a><span data-ttu-id="3f75e-103">PidTagReportName (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="3f75e-103">PidTagReportName Canonical Property</span></span>

  
  
<span data-ttu-id="3f75e-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3f75e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3f75e-105">Enthält den Anzeigenamen für den Empfänger, der Berichte für diese Nachricht erhalten soll.</span><span class="sxs-lookup"><span data-stu-id="3f75e-105">Contains the display name for the recipient that should get reports for this message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3f75e-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="3f75e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3f75e-107">PR_REPORT_NAME, PR_REPORT_NAME_A, PR_REPORT_NAME_W</span><span class="sxs-lookup"><span data-stu-id="3f75e-107">PR_REPORT_NAME, PR_REPORT_NAME_A, PR_REPORT_NAME_W</span></span>  <br/> |
|<span data-ttu-id="3f75e-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="3f75e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="3f75e-109">0x003A</span><span class="sxs-lookup"><span data-stu-id="3f75e-109">0x003A</span></span>  <br/> |
|<span data-ttu-id="3f75e-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="3f75e-110">Data type:</span></span>  <br/> |<span data-ttu-id="3f75e-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="3f75e-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="3f75e-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="3f75e-112">Area:</span></span>  <br/> |<span data-ttu-id="3f75e-113">MAPI-Umschlag</span><span class="sxs-lookup"><span data-stu-id="3f75e-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3f75e-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="3f75e-114">Remarks</span></span>

<span data-ttu-id="3f75e-115">Diese Eigenschaften sind Beispiele für die Adresseigenschaften für den Empfänger, den der Absender delegiert hat, um berichte zu empfangen, die für diese Nachricht generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="3f75e-115">These properties are examples of the address properties for the recipient that the sender has delegated to receive any reports generated for this message.</span></span>
  
<span data-ttu-id="3f75e-116">Eine Clientanwendung, die Berichte an einen anderen Benutzer weiter routen muss, sollte diese Eigenschaften zum Zeitpunkt der Nachrichtenübermittlung festlegen.</span><span class="sxs-lookup"><span data-stu-id="3f75e-116">A client application that must route reports to another user should set these properties at message submission time.</span></span> <span data-ttu-id="3f75e-117">Wenn sie nicht festgelegt sind, werden die Berichte an den Nachrichtensender gesendet.</span><span class="sxs-lookup"><span data-stu-id="3f75e-117">If they are not set, the reports are sent to the message sender.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="3f75e-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="3f75e-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="3f75e-119">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="3f75e-119">Header files</span></span>

<span data-ttu-id="3f75e-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3f75e-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="3f75e-121">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="3f75e-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="3f75e-122">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="3f75e-122">Mapitags.h</span></span>
  
> <span data-ttu-id="3f75e-123">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="3f75e-123">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3f75e-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3f75e-124">See also</span></span>



[<span data-ttu-id="3f75e-125">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3f75e-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3f75e-126">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="3f75e-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3f75e-127">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="3f75e-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3f75e-128">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="3f75e-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

