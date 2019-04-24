---
title: Kanonische Pidtagrecipientnumberforadvice (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRecipientNumberForAdvice
api_type:
- COM
ms.assetid: 636c1e75-3024-43ca-a7dd-1bb480dfbb5b
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 79ef85955f15e0ca829ac6f206dddc17031b0562
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356693"
---
# <a name="pidtagrecipientnumberforadvice-canonical-property"></a><span data-ttu-id="7f58e-103">Kanonische Pidtagrecipientnumberforadvice (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="7f58e-103">PidTagRecipientNumberForAdvice Canonical Property</span></span>

  
  
<span data-ttu-id="7f58e-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7f58e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7f58e-105">Diese Eigenschaft enthält die Telefonnummer eines Nachrichtenempfängers, die für die physische Übermittlung einer Nachricht aufgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="7f58e-105">This property contains a message recipient's telephone number to call to advise of the physical delivery of a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7f58e-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="7f58e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7f58e-107">PR_RECIPIENT_NUMBER_FOR_ADVICE, PR_RECIPIENT_NUMBER_FOR_ADVICE_A, PR_RECIPIENT_NUMBER_FOR_ADVICE_W</span><span class="sxs-lookup"><span data-stu-id="7f58e-107">PR_RECIPIENT_NUMBER_FOR_ADVICE, PR_RECIPIENT_NUMBER_FOR_ADVICE_A, PR_RECIPIENT_NUMBER_FOR_ADVICE_W</span></span>  <br/> |
|<span data-ttu-id="7f58e-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="7f58e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7f58e-109">0x0C14</span><span class="sxs-lookup"><span data-stu-id="7f58e-109">0x0C14</span></span>  <br/> |
|<span data-ttu-id="7f58e-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="7f58e-110">Data type:</span></span>  <br/> |<span data-ttu-id="7f58e-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="7f58e-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="7f58e-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="7f58e-112">Area:</span></span>  <br/> |<span data-ttu-id="7f58e-113">MAPI-Empfänger</span><span class="sxs-lookup"><span data-stu-id="7f58e-113">MAPI Recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7f58e-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7f58e-114">Remarks</span></span>

<span data-ttu-id="7f58e-115">Diese Eigenschaften sind für die Verwendung in Verbindung mit der Übertragung an ein physisches Ziel gedacht, statt für ein elektronisches Postfach, wenn der menschliche Empfänger nicht bei der Lieferung anwesend sein soll.</span><span class="sxs-lookup"><span data-stu-id="7f58e-115">These properties are meant to be used in conjunction with delivery to a physical destination, rather than an electronic mailbox, when the human recipient is not expected to be present at delivery.</span></span> <span data-ttu-id="7f58e-116">Ein Beispiel ist die Telefonnummer auf einem Faxdeckblatt.</span><span class="sxs-lookup"><span data-stu-id="7f58e-116">An example is the telephone number on a fax cover sheet.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="7f58e-117">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="7f58e-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="7f58e-118">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="7f58e-118">Header files</span></span>

<span data-ttu-id="7f58e-119">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="7f58e-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="7f58e-120">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="7f58e-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="7f58e-121">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="7f58e-121">Mapitags.h</span></span>
  
> <span data-ttu-id="7f58e-122">Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="7f58e-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7f58e-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7f58e-123">See also</span></span>



[<span data-ttu-id="7f58e-124">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7f58e-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7f58e-125">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7f58e-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7f58e-126">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="7f58e-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7f58e-127">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="7f58e-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

