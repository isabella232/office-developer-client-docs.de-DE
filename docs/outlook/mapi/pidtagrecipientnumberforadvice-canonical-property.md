---
title: PidTagRecipientNumberForAdvice (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 3f23a332ee6778f71ce0809dfae8c0b6a92246a8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595146"
---
# <a name="pidtagrecipientnumberforadvice-canonical-property"></a><span data-ttu-id="0650a-103">PidTagRecipientNumberForAdvice (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="0650a-103">PidTagRecipientNumberForAdvice Canonical Property</span></span>

  
  
<span data-ttu-id="0650a-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0650a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0650a-105">Diese Eigenschaft enthält einen Nachrichtenempfänger Telefonnummer von der physischen Übermittlung einer Nachricht informiert.</span><span class="sxs-lookup"><span data-stu-id="0650a-105">This property contains a message recipient's telephone number to call to advise of the physical delivery of a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0650a-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="0650a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0650a-107">PR_RECIPIENT_NUMBER_FOR_ADVICE, PR_RECIPIENT_NUMBER_FOR_ADVICE_A, PR_RECIPIENT_NUMBER_FOR_ADVICE_W</span><span class="sxs-lookup"><span data-stu-id="0650a-107">PR_RECIPIENT_NUMBER_FOR_ADVICE, PR_RECIPIENT_NUMBER_FOR_ADVICE_A, PR_RECIPIENT_NUMBER_FOR_ADVICE_W</span></span>  <br/> |
|<span data-ttu-id="0650a-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="0650a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0650a-109">0x0C14</span><span class="sxs-lookup"><span data-stu-id="0650a-109">0x0C14</span></span>  <br/> |
|<span data-ttu-id="0650a-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="0650a-110">Data type:</span></span>  <br/> |<span data-ttu-id="0650a-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="0650a-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="0650a-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="0650a-112">Area:</span></span>  <br/> |<span data-ttu-id="0650a-113">MAPI-Empfänger</span><span class="sxs-lookup"><span data-stu-id="0650a-113">MAPI Recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0650a-114">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="0650a-114">Remarks</span></span>

<span data-ttu-id="0650a-115">Diese Eigenschaften sind in Verbindung mit der Zustellung an eine physische Ziel, statt ein elektronisches-Postfach verwendet werden, wenn der menschliche Empfänger nicht erwartet wird, Übermittlung vorhanden sein soll.</span><span class="sxs-lookup"><span data-stu-id="0650a-115">These properties are meant to be used in conjunction with delivery to a physical destination, rather than an electronic mailbox, when the human recipient is not expected to be present at delivery.</span></span> <span data-ttu-id="0650a-116">Ein Beispiel ist die Telefonnummer auf ein Faxdeckblatt.</span><span class="sxs-lookup"><span data-stu-id="0650a-116">An example is the telephone number on a fax cover sheet.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="0650a-117">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="0650a-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="0650a-118">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="0650a-118">Header files</span></span>

<span data-ttu-id="0650a-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0650a-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="0650a-120">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="0650a-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="0650a-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="0650a-121">Mapitags.h</span></span>
  
> <span data-ttu-id="0650a-122">Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="0650a-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0650a-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0650a-123">See also</span></span>



[<span data-ttu-id="0650a-124">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0650a-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0650a-125">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0650a-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0650a-126">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="0650a-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0650a-127">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="0650a-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

