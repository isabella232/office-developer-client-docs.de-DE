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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358566"
---
# <a name="pidtaginternetmessageid-canonical-property"></a><span data-ttu-id="0fd97-103">PidTagInternetMessageId (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="0fd97-103">PidTagInternetMessageId Canonical Property</span></span>

  
  
<span data-ttu-id="0fd97-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0fd97-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0fd97-105">Entspricht dem Meldungs-ID-Feld, das in [RFC2822] angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="0fd97-105">Corresponds to the message ID field as specified in [RFC2822].</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0fd97-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="0fd97-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0fd97-107">PR_INTERNET_MESSAGE_ID, PR_INTERNET_MESSAGE_ID_A, PR_INTERNET_MESSAGE_ID_W</span><span class="sxs-lookup"><span data-stu-id="0fd97-107">PR_INTERNET_MESSAGE_ID, PR_INTERNET_MESSAGE_ID_A, PR_INTERNET_MESSAGE_ID_W</span></span>  <br/> |
|<span data-ttu-id="0fd97-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="0fd97-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0fd97-109">0x1035</span><span class="sxs-lookup"><span data-stu-id="0fd97-109">0x1035</span></span>  <br/> |
|<span data-ttu-id="0fd97-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="0fd97-110">Data type:</span></span>  <br/> |<span data-ttu-id="0fd97-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="0fd97-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="0fd97-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="0fd97-112">Area:</span></span>  <br/> |<span data-ttu-id="0fd97-113">MIME</span><span class="sxs-lookup"><span data-stu-id="0fd97-113">MIME</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0fd97-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="0fd97-114">Remarks</span></span>

<span data-ttu-id="0fd97-115">Diese Eigenschaften sollten für alle E-Mail-Nachrichten vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="0fd97-115">These properties should be present on all email messages.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="0fd97-116">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="0fd97-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0fd97-117">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="0fd97-117">Protocol specifications</span></span>

<span data-ttu-id="0fd97-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0fd97-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0fd97-119">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="0fd97-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0fd97-120">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0fd97-120">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0fd97-121">Gibt die Eigenschaften und Vorgänge an, die für E-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="0fd97-121">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0fd97-122">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="0fd97-122">Header files</span></span>

<span data-ttu-id="0fd97-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0fd97-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="0fd97-124">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="0fd97-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="0fd97-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="0fd97-125">Mapitags.h</span></span>
  
> <span data-ttu-id="0fd97-126">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="0fd97-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0fd97-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0fd97-127">See also</span></span>



[<span data-ttu-id="0fd97-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0fd97-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0fd97-129">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="0fd97-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0fd97-130">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="0fd97-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0fd97-131">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="0fd97-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

