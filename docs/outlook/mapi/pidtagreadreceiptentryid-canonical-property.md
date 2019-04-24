---
title: Kanonische Pidtagreadreceiptentryid (-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 662c191f36f9ca30dcdf0f559ea5385bfe5fd305
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356510"
---
# <a name="pidtagreadreceiptentryid-canonical-property"></a><span data-ttu-id="f3e30-103">Kanonische Pidtagreadreceiptentryid (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="f3e30-103">PidTagReadReceiptEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="f3e30-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f3e30-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f3e30-105">Enthält eine Eintrags-ID für den Messaging-Benutzer, bei dem das Messagingsystem einen Lesebericht für diese Nachricht leiten soll.</span><span class="sxs-lookup"><span data-stu-id="f3e30-105">Contains an entry identifier for the messaging user where the messaging system should direct a read report for this message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f3e30-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="f3e30-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f3e30-107">PR_READ_RECEIPT_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="f3e30-107">PR_READ_RECEIPT_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="f3e30-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="f3e30-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f3e30-109">0x0046</span><span class="sxs-lookup"><span data-stu-id="f3e30-109">0x0046</span></span>  <br/> |
|<span data-ttu-id="f3e30-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="f3e30-110">Data type:</span></span>  <br/> |<span data-ttu-id="f3e30-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="f3e30-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="f3e30-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="f3e30-112">Area:</span></span>  <br/> |<span data-ttu-id="f3e30-113">MAPI-Umschlag</span><span class="sxs-lookup"><span data-stu-id="f3e30-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f3e30-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f3e30-114">Remarks</span></span>

<span data-ttu-id="f3e30-115">Diese Eigenschaft wird ignoriert, wenn die **PR_READ_RECEIPT_REQUESTED** ([pidtagreadreceiptrequested (](pidtagreadreceiptrequested-canonical-property.md))-Eigenschaft auf true festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="f3e30-115">This property is ignored unless the **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) property is set to TRUE.</span></span>
  
<span data-ttu-id="f3e30-116">Wenn eine Clientanwendung Lese Berichte selbst empfangen möchte, kann diese Eigenschaft nicht festgelegt werden, oder Sie wird auf die in der **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md))-Eigenschaft enthaltene Eintrags-ID für die Nachrichtenübermittlungs Zeit gesetzt.</span><span class="sxs-lookup"><span data-stu-id="f3e30-116">If a client application wants to receive read reports itself, it can leave this property unset or set it to the entry identifier contained in the **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)) property at message submission time.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f3e30-117">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="f3e30-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f3e30-118">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="f3e30-118">Protocol specifications</span></span>

<span data-ttu-id="f3e30-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f3e30-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f3e30-120">Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="f3e30-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f3e30-121">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f3e30-121">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f3e30-122">Gibt die Eigenschaften und Vorgänge an, die für e-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="f3e30-122">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f3e30-123">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="f3e30-123">Header files</span></span>

<span data-ttu-id="f3e30-124">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="f3e30-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="f3e30-125">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="f3e30-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="f3e30-126">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="f3e30-126">Mapitags.h</span></span>
  
> <span data-ttu-id="f3e30-127">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="f3e30-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f3e30-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f3e30-128">See also</span></span>



[<span data-ttu-id="f3e30-129">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f3e30-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f3e30-130">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f3e30-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f3e30-131">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="f3e30-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f3e30-132">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="f3e30-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

