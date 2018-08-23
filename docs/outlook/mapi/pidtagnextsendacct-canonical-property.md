---
title: PidTagNextSendAcct (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagNextSendAcct
api_type:
- HeaderDef
ms.assetid: b7429c2e-0d9d-4921-9f56-9ecad817f8cb
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 76584e248f03deac62af94e4638fcead15594b3e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581132"
---
# <a name="pidtagnextsendacct-canonical-property"></a><span data-ttu-id="4fea8-103">PidTagNextSendAcct (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="4fea8-103">PidTagNextSendAcct Canonical Property</span></span>

  
  
<span data-ttu-id="4fea8-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4fea8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4fea8-105">Gibt den Server, den ein Client derzeit versucht, Senden von e-Mails zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="4fea8-105">Specifies the server that a client is currently attempting to use to send email.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4fea8-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="4fea8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4fea8-107">PR_NEXT_SEND_ACCT</span><span class="sxs-lookup"><span data-stu-id="4fea8-107">PR_NEXT_SEND_ACCT</span></span>  <br/> |
|<span data-ttu-id="4fea8-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="4fea8-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4fea8-109">0x0E29</span><span class="sxs-lookup"><span data-stu-id="4fea8-109">0x0E29</span></span>  <br/> |
|<span data-ttu-id="4fea8-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="4fea8-110">Data type:</span></span>  <br/> |<span data-ttu-id="4fea8-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="4fea8-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="4fea8-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="4fea8-112">Area:</span></span>  <br/> |<span data-ttu-id="4fea8-113">Outlook-Anwendung</span><span class="sxs-lookup"><span data-stu-id="4fea8-113">Outlook application</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4fea8-114">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="4fea8-114">Remarks</span></span>

<span data-ttu-id="4fea8-115">Das Format dieser Eigenschaft ist die Implementierung ab.</span><span class="sxs-lookup"><span data-stu-id="4fea8-115">The format of this property is implementation dependent.</span></span> <span data-ttu-id="4fea8-116">Diese Eigenschaft kann zum Ermitteln des Servers, leiten Sie die e-Mail vom Client verwendet werden, jedoch ist optional, und der Wert hat keine Bedeutung für den Server.</span><span class="sxs-lookup"><span data-stu-id="4fea8-116">This property can be used by the client to determine which server to direct the email to, but is optional and the value has no meaning to the server.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="4fea8-117">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="4fea8-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4fea8-118">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="4fea8-118">Protocol specifications</span></span>

<span data-ttu-id="4fea8-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4fea8-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4fea8-120">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="4fea8-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4fea8-121">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4fea8-121">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4fea8-122">Konvertiert zwischen IETF RFC2445, RFC2446, RFC2447, und Termine und meeting-Objekte.</span><span class="sxs-lookup"><span data-stu-id="4fea8-122">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="4fea8-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4fea8-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4fea8-124">Gibt die Eigenschaften und Operationen, die für e-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="4fea8-124">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4fea8-125">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="4fea8-125">Header files</span></span>

<span data-ttu-id="4fea8-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4fea8-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="4fea8-127">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="4fea8-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="4fea8-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="4fea8-128">Mapitags.h</span></span>
  
> <span data-ttu-id="4fea8-129">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="4fea8-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4fea8-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4fea8-130">See also</span></span>



[<span data-ttu-id="4fea8-131">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4fea8-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4fea8-132">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4fea8-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4fea8-133">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="4fea8-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4fea8-134">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="4fea8-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

