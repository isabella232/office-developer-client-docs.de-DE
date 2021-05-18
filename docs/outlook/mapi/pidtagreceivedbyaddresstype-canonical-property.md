---
title: PidTagReceivedByAddressType (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReceivedByAddressType
api_type:
- COM
ms.assetid: 0eef299d-6923-4dae-9a18-91ea82ea0f3e
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 00c07069ed174fe55556dfe48398d65b4e64100e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359227"
---
# <a name="pidtagreceivedbyaddresstype-canonical-property"></a><span data-ttu-id="4ed04-103">PidTagReceivedByAddressType (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="4ed04-103">PidTagReceivedByAddressType Canonical Property</span></span>

  
  
<span data-ttu-id="4ed04-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4ed04-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4ed04-105">Enthält den E-Mail-Adresstyp, z. B. SMTP, für den Messagingbenutzer, der die Nachricht tatsächlich empfängt.</span><span class="sxs-lookup"><span data-stu-id="4ed04-105">Contains the email address type, such as SMTP, for the messaging user who actually receives the message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4ed04-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="4ed04-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4ed04-107">PR_RECEIVED_BY_ADDRTYPE, PR_RECEIVED_BY_ADDRTYPE_A, PR_RECEIVED_BY_ADDRTYPE_W</span><span class="sxs-lookup"><span data-stu-id="4ed04-107">PR_RECEIVED_BY_ADDRTYPE, PR_RECEIVED_BY_ADDRTYPE_A, PR_RECEIVED_BY_ADDRTYPE_W</span></span>  <br/> |
|<span data-ttu-id="4ed04-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="4ed04-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4ed04-109">0x0075</span><span class="sxs-lookup"><span data-stu-id="4ed04-109">0x0075</span></span>  <br/> |
|<span data-ttu-id="4ed04-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="4ed04-110">Data type:</span></span>  <br/> |<span data-ttu-id="4ed04-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="4ed04-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="4ed04-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="4ed04-112">Area:</span></span>  <br/> |<span data-ttu-id="4ed04-113">MAPI-Umschlag</span><span class="sxs-lookup"><span data-stu-id="4ed04-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4ed04-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="4ed04-114">Remarks</span></span>

<span data-ttu-id="4ed04-115">Diese Eigenschaften sind Beispiele für die Adresseigenschaften für den Messagingbenutzer, der die Nachricht tatsächlich empfängt.</span><span class="sxs-lookup"><span data-stu-id="4ed04-115">These properties are examples of the address properties for the messaging user who actually receives the message.</span></span> <span data-ttu-id="4ed04-116">Sie müssen vom eingehenden Transportanbieter festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="4ed04-116">They must be set by the incoming transport provider.</span></span>
  
<span data-ttu-id="4ed04-117">Die Adresstypzeichenfolge kann nur die Großbuchstaben A bis Z und die Zahlen null bis neun enthalten.</span><span class="sxs-lookup"><span data-stu-id="4ed04-117">The address type string can contain only the uppercase alphabetic characters A through Z and the numbers zero through nine.</span></span> <span data-ttu-id="4ed04-118">Diese Eigenschaften qualifizieren die **PR_RECEIVED_BY_EMAIL_ADDRESS** ([PidTagReceivedByEmailAddress](pidtagreceivedbyemailaddress-canonical-property.md)) -Eigenschaft, indem sie einen Adresstyp angeben, z. B. SMTP, wodurch angegeben wird, wie die Adresse erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="4ed04-118">These properties qualify the **PR_RECEIVED_BY_EMAIL_ADDRESS** ([PidTagReceivedByEmailAddress](pidtagreceivedbyemailaddress-canonical-property.md)) property by specifying an address type, such as SMTP, thereby indicating how the address should be constructed.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="4ed04-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="4ed04-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4ed04-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="4ed04-120">Protocol specifications</span></span>

<span data-ttu-id="4ed04-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4ed04-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4ed04-122">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="4ed04-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4ed04-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4ed04-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4ed04-124">Gibt die Eigenschaften und Vorgänge an, die für E-Mail-Nachrichten zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="4ed04-124">Specifies the properties and operations that are permissible on email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4ed04-125">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="4ed04-125">Header files</span></span>

<span data-ttu-id="4ed04-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4ed04-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="4ed04-127">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="4ed04-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="4ed04-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="4ed04-128">Mapitags.h</span></span>
  
> <span data-ttu-id="4ed04-129">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="4ed04-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4ed04-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4ed04-130">See also</span></span>



[<span data-ttu-id="4ed04-131">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4ed04-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4ed04-132">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="4ed04-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4ed04-133">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="4ed04-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4ed04-134">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="4ed04-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

