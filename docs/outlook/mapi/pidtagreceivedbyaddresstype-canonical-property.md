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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382666"
---
# <a name="pidtagreceivedbyaddresstype-canonical-property"></a><span data-ttu-id="3d6d1-103">PidTagReceivedByAddressType (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="3d6d1-103">PidTagReceivedByAddressType Canonical Property</span></span>

  
  
<span data-ttu-id="3d6d1-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3d6d1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3d6d1-105">Enthält den e-Mail-Adresse ein, beispielsweise SMTP, für den messaging-Benutzer, der tatsächlich die Nachricht empfängt.</span><span class="sxs-lookup"><span data-stu-id="3d6d1-105">Contains the email address type, such as SMTP, for the messaging user who actually receives the message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3d6d1-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="3d6d1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3d6d1-107">PR_RECEIVED_BY_ADDRTYPE, PR_RECEIVED_BY_ADDRTYPE_A, PR_RECEIVED_BY_ADDRTYPE_W</span><span class="sxs-lookup"><span data-stu-id="3d6d1-107">PR_RECEIVED_BY_ADDRTYPE, PR_RECEIVED_BY_ADDRTYPE_A, PR_RECEIVED_BY_ADDRTYPE_W</span></span>  <br/> |
|<span data-ttu-id="3d6d1-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="3d6d1-108">Identifier:</span></span>  <br/> |<span data-ttu-id="3d6d1-109">0x0075</span><span class="sxs-lookup"><span data-stu-id="3d6d1-109">0x0075</span></span>  <br/> |
|<span data-ttu-id="3d6d1-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="3d6d1-110">Data type:</span></span>  <br/> |<span data-ttu-id="3d6d1-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="3d6d1-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="3d6d1-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="3d6d1-112">Area:</span></span>  <br/> |<span data-ttu-id="3d6d1-113">MAPI-Umschlag</span><span class="sxs-lookup"><span data-stu-id="3d6d1-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3d6d1-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="3d6d1-114">Remarks</span></span>

<span data-ttu-id="3d6d1-115">Diese Eigenschaften sind Beispiele für die Adresseigenschaften für den messaging-Benutzer, der tatsächlich die Nachricht empfängt.</span><span class="sxs-lookup"><span data-stu-id="3d6d1-115">These properties are examples of the address properties for the messaging user who actually receives the message.</span></span> <span data-ttu-id="3d6d1-116">Sie müssen von der eingehenden Adressbuchhierarchie festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="3d6d1-116">They must be set by the incoming transport provider.</span></span>
  
<span data-ttu-id="3d6d1-117">Die Typ Adresszeichenfolge kann nur Großbuchstaben A bis Z und die Zahlen null bis neun enthalten.</span><span class="sxs-lookup"><span data-stu-id="3d6d1-117">The address type string can contain only the uppercase alphabetic characters A through Z and the numbers zero through nine.</span></span> <span data-ttu-id="3d6d1-118">Diese Eigenschaften kennzeichnen die **PR_RECEIVED_BY_EMAIL_ADDRESS** ([PidTagReceivedByEmailAddress](pidtagreceivedbyemailaddress-canonical-property.md))-Eigenschaft angeben einen Adresstyp, beispielsweise SMTP, wodurch, die angibt, wie die Adresse erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="3d6d1-118">These properties qualify the **PR_RECEIVED_BY_EMAIL_ADDRESS** ([PidTagReceivedByEmailAddress](pidtagreceivedbyemailaddress-canonical-property.md)) property by specifying an address type, such as SMTP, thereby indicating how the address should be constructed.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="3d6d1-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="3d6d1-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3d6d1-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="3d6d1-120">Protocol specifications</span></span>

<span data-ttu-id="3d6d1-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3d6d1-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3d6d1-122">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="3d6d1-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="3d6d1-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3d6d1-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3d6d1-124">Gibt die Eigenschaften und Operationen, die für e-Mail-Nachrichten zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="3d6d1-124">Specifies the properties and operations that are permissible on email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3d6d1-125">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="3d6d1-125">Header files</span></span>

<span data-ttu-id="3d6d1-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3d6d1-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="3d6d1-127">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="3d6d1-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="3d6d1-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="3d6d1-128">Mapitags.h</span></span>
  
> <span data-ttu-id="3d6d1-129">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="3d6d1-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3d6d1-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3d6d1-130">See also</span></span>



[<span data-ttu-id="3d6d1-131">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3d6d1-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3d6d1-132">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3d6d1-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3d6d1-133">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="3d6d1-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3d6d1-134">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="3d6d1-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

