---
title: PidTagInternetMessageId (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagInternetMessageId
api_type:
- HeaderDef
ms.assetid: 5c93d00c-a199-4d45-9bf6-87bd2ffe4784
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: c2cc0eabd9c329953d9b0d252418549ea1c588a1
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25391927"
---
# <a name="pidtaginternetmessageid-canonical-property"></a><span data-ttu-id="4e53a-103">PidTagInternetMessageId (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="4e53a-103">PidTagInternetMessageId Canonical Property</span></span>

  
  
<span data-ttu-id="4e53a-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4e53a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4e53a-105">Im Feld Meldung ID gemäß [RFC2822] entspricht.</span><span class="sxs-lookup"><span data-stu-id="4e53a-105">Corresponds to the message ID field as specified in [RFC2822].</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4e53a-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="4e53a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4e53a-107">PR_INTERNET_MESSAGE_ID, PR_INTERNET_MESSAGE_ID_A, PR_INTERNET_MESSAGE_ID_W</span><span class="sxs-lookup"><span data-stu-id="4e53a-107">PR_INTERNET_MESSAGE_ID, PR_INTERNET_MESSAGE_ID_A, PR_INTERNET_MESSAGE_ID_W</span></span>  <br/> |
|<span data-ttu-id="4e53a-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="4e53a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4e53a-109">0x1035</span><span class="sxs-lookup"><span data-stu-id="4e53a-109">0x1035</span></span>  <br/> |
|<span data-ttu-id="4e53a-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="4e53a-110">Data type:</span></span>  <br/> |<span data-ttu-id="4e53a-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="4e53a-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="4e53a-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="4e53a-112">Area:</span></span>  <br/> |<span data-ttu-id="4e53a-113">MIME</span><span class="sxs-lookup"><span data-stu-id="4e53a-113">MIME</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4e53a-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="4e53a-114">Remarks</span></span>

<span data-ttu-id="4e53a-115">Diese Eigenschaften sollten für alle e-Mail-Nachrichten vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="4e53a-115">These properties should be present on all email messages.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="4e53a-116">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="4e53a-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4e53a-117">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="4e53a-117">Protocol specifications</span></span>

<span data-ttu-id="4e53a-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4e53a-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4e53a-119">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="4e53a-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4e53a-120">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4e53a-120">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4e53a-121">Gibt die Eigenschaften und Operationen, die für e-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="4e53a-121">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4e53a-122">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="4e53a-122">Header files</span></span>

<span data-ttu-id="4e53a-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4e53a-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="4e53a-124">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="4e53a-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="4e53a-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="4e53a-125">Mapitags.h</span></span>
  
> <span data-ttu-id="4e53a-126">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="4e53a-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4e53a-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4e53a-127">See also</span></span>



[<span data-ttu-id="4e53a-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4e53a-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4e53a-129">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4e53a-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4e53a-130">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="4e53a-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4e53a-131">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="4e53a-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

