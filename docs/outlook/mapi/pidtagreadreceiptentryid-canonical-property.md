---
title: PidTagReadReceiptEntryId (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReadReceiptEntryId
api_type:
- COM
ms.assetid: 141d49c8-87cf-4d80-a33b-ccbf3eeae19e
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 662c191f36f9ca30dcdf0f559ea5385bfe5fd305
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356510"
---
# <a name="pidtagreadreceiptentryid-canonical-property"></a><span data-ttu-id="aecba-103">PidTagReadReceiptEntryId (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="aecba-103">PidTagReadReceiptEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="aecba-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="aecba-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="aecba-105">Enthält eine Eintrags-ID für den Messagingbenutzer, an den das Messagingsystem einen Lesebericht für diese Nachricht senden soll.</span><span class="sxs-lookup"><span data-stu-id="aecba-105">Contains an entry identifier for the messaging user where the messaging system should direct a read report for this message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="aecba-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="aecba-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="aecba-107">PR_READ_RECEIPT_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="aecba-107">PR_READ_RECEIPT_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="aecba-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="aecba-108">Identifier:</span></span>  <br/> |<span data-ttu-id="aecba-109">0x0046</span><span class="sxs-lookup"><span data-stu-id="aecba-109">0x0046</span></span>  <br/> |
|<span data-ttu-id="aecba-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="aecba-110">Data type:</span></span>  <br/> |<span data-ttu-id="aecba-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="aecba-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="aecba-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="aecba-112">Area:</span></span>  <br/> |<span data-ttu-id="aecba-113">MAPI-Umschlag</span><span class="sxs-lookup"><span data-stu-id="aecba-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="aecba-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="aecba-114">Remarks</span></span>

<span data-ttu-id="aecba-115">Diese Eigenschaft wird ignoriert, es sei **denn, die PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) -Eigenschaft ist auf TRUE festgelegt.</span><span class="sxs-lookup"><span data-stu-id="aecba-115">This property is ignored unless the **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) property is set to TRUE.</span></span>
  
<span data-ttu-id="aecba-116">Wenn eine Clientanwendung Leseberichte selbst empfangen möchte, kann sie diese Eigenschaft nicht festlegen oder auf den Eintragsbezeichner festlegen, der zur Zeit der Nachrichtenübermittlung in der **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md))-Eigenschaft enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="aecba-116">If a client application wants to receive read reports itself, it can leave this property unset or set it to the entry identifier contained in the **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)) property at message submission time.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="aecba-117">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="aecba-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="aecba-118">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="aecba-118">Protocol specifications</span></span>

<span data-ttu-id="aecba-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="aecba-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="aecba-120">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="aecba-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="aecba-121">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="aecba-121">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="aecba-122">Gibt die Eigenschaften und Vorgänge an, die für E-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="aecba-122">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="aecba-123">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="aecba-123">Header files</span></span>

<span data-ttu-id="aecba-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="aecba-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="aecba-125">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="aecba-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="aecba-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="aecba-126">Mapitags.h</span></span>
  
> <span data-ttu-id="aecba-127">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="aecba-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="aecba-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="aecba-128">See also</span></span>



[<span data-ttu-id="aecba-129">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="aecba-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="aecba-130">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="aecba-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="aecba-131">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="aecba-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="aecba-132">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="aecba-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

