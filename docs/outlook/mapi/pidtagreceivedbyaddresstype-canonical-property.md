---
title: Kanonische PidTagReceivedByAddressType-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 96a53e427460990983242009500ade9ae0c5ada5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794867"
---
# <a name="pidtagreceivedbyaddresstype-canonical-property"></a><span data-ttu-id="07d31-103">Kanonische PidTagReceivedByAddressType-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="07d31-103">PidTagReceivedByAddressType Canonical Property</span></span>

  
  
<span data-ttu-id="07d31-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="07d31-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="07d31-105">Enthält den e-Mail-Adresse ein, beispielsweise SMTP, für den messaging-Benutzer, der tatsächlich die Nachricht empfängt.</span><span class="sxs-lookup"><span data-stu-id="07d31-105">Contains the email address type, such as SMTP, for the messaging user who actually receives the message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="07d31-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="07d31-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="07d31-107">PR_RECEIVED_BY_ADDRTYPE, PR_RECEIVED_BY_ADDRTYPE_A, PR_RECEIVED_BY_ADDRTYPE_W</span><span class="sxs-lookup"><span data-stu-id="07d31-107">PR_RECEIVED_BY_ADDRTYPE, PR_RECEIVED_BY_ADDRTYPE_A, PR_RECEIVED_BY_ADDRTYPE_W</span></span>  <br/> |
|<span data-ttu-id="07d31-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="07d31-108">Identifier:</span></span>  <br/> |<span data-ttu-id="07d31-109">0x0075</span><span class="sxs-lookup"><span data-stu-id="07d31-109">0x0075</span></span>  <br/> |
|<span data-ttu-id="07d31-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="07d31-110">Data type:</span></span>  <br/> |<span data-ttu-id="07d31-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="07d31-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="07d31-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="07d31-112">Area:</span></span>  <br/> |<span data-ttu-id="07d31-113">MAPI-Umschlag</span><span class="sxs-lookup"><span data-stu-id="07d31-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="07d31-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="07d31-114">Remarks</span></span>

<span data-ttu-id="07d31-115">Diese Eigenschaften sind Beispiele für die Adresseigenschaften für den messaging-Benutzer, der tatsächlich die Nachricht empfängt.</span><span class="sxs-lookup"><span data-stu-id="07d31-115">These properties are examples of the address properties for the messaging user who actually receives the message.</span></span> <span data-ttu-id="07d31-116">Sie müssen von der eingehenden Adressbuchhierarchie festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="07d31-116">They must be set by the incoming transport provider.</span></span>
  
<span data-ttu-id="07d31-117">Die Typ Adresszeichenfolge kann nur Großbuchstaben A bis Z und die Zahlen null bis neun enthalten.</span><span class="sxs-lookup"><span data-stu-id="07d31-117">The address type string can contain only the uppercase alphabetic characters A through Z and the numbers zero through nine.</span></span> <span data-ttu-id="07d31-118">Diese Eigenschaften kennzeichnen die **PR_RECEIVED_BY_EMAIL_ADDRESS** ([PidTagReceivedByEmailAddress](pidtagreceivedbyemailaddress-canonical-property.md))-Eigenschaft angeben einen Adresstyp, beispielsweise SMTP, wodurch, die angibt, wie die Adresse erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="07d31-118">These properties qualify the **PR_RECEIVED_BY_EMAIL_ADDRESS** ([PidTagReceivedByEmailAddress](pidtagreceivedbyemailaddress-canonical-property.md)) property by specifying an address type, such as SMTP, thereby indicating how the address should be constructed.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="07d31-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="07d31-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="07d31-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="07d31-120">Protocol specifications</span></span>

<span data-ttu-id="07d31-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="07d31-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="07d31-122">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="07d31-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="07d31-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="07d31-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="07d31-124">Gibt die Eigenschaften und Operationen, die für e-Mail-Nachrichten zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="07d31-124">Specifies the properties and operations that are permissible on email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="07d31-125">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="07d31-125">Header files</span></span>

<span data-ttu-id="07d31-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="07d31-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="07d31-127">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="07d31-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="07d31-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="07d31-128">Mapitags.h</span></span>
  
> <span data-ttu-id="07d31-129">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="07d31-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="07d31-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="07d31-130">See also</span></span>



[<span data-ttu-id="07d31-131">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="07d31-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="07d31-132">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="07d31-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="07d31-133">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="07d31-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="07d31-134">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="07d31-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

