---
title: PidTagEmailAddress (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagEmailAddress
api_type:
- HeaderDef
ms.assetid: bbd1e187-172e-4612-9efe-7c8e52967dfe
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: efcb72d872836adce544f3a90cf093de1f3713a7
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25393880"
---
# <a name="pidtagemailaddress-canonical-property"></a><span data-ttu-id="0b0c0-103">PidTagEmailAddress (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="0b0c0-103">PidTagEmailAddress Canonical Property</span></span>

  
  
<span data-ttu-id="0b0c0-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0b0c0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0b0c0-105">Messaging-Benutzer e-Mail-Adresse enthält.</span><span class="sxs-lookup"><span data-stu-id="0b0c0-105">Contains the messaging user's email address.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0b0c0-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="0b0c0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0b0c0-107">PR_EMAIL_ADDRESS, PR_EMAIL_ADDRESS_A, PR_EMAIL_ADDRESS_W</span><span class="sxs-lookup"><span data-stu-id="0b0c0-107">PR_EMAIL_ADDRESS, PR_EMAIL_ADDRESS_A, PR_EMAIL_ADDRESS_W</span></span>  <br/> |
|<span data-ttu-id="0b0c0-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="0b0c0-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0b0c0-109">0x3003</span><span class="sxs-lookup"><span data-stu-id="0b0c0-109">0x3003</span></span>  <br/> |
|<span data-ttu-id="0b0c0-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="0b0c0-110">Data type:</span></span>  <br/> |<span data-ttu-id="0b0c0-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="0b0c0-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="0b0c0-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="0b0c0-112">Area:</span></span>  <br/> |<span data-ttu-id="0b0c0-113">Allgemeine MAPI</span><span class="sxs-lookup"><span data-stu-id="0b0c0-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0b0c0-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="0b0c0-114">Remarks</span></span>

<span data-ttu-id="0b0c0-115">Diese Eigenschaften sind Beispiele für die Basisadresse Eigenschaften für alle Benutzer messaging.</span><span class="sxs-lookup"><span data-stu-id="0b0c0-115">These properties are examples of the base address properties for all messaging users.</span></span> <span data-ttu-id="0b0c0-116">Es ist eine Null endende Zeichenfolge, deren Format Bedeutung nur für das zugrunde liegende messaging-System hat.</span><span class="sxs-lookup"><span data-stu-id="0b0c0-116">It is a null-terminated string whose format has meaning only for the underlying messaging system.</span></span> 
  
<span data-ttu-id="0b0c0-117">Diese Eigenschaften werden in Verbindung mit dem **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) und **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))-Eigenschaften in die Adressierung von Nachrichten verwendet.</span><span class="sxs-lookup"><span data-stu-id="0b0c0-117">These properties are used in conjunction with the **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) and **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) properties in addressing messages.</span></span> <span data-ttu-id="0b0c0-118">Das Format der Zeichenfolge wird durch **PR_ADDRTYPE**gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="0b0c0-118">The string format is qualified by **PR_ADDRTYPE**.</span></span> 
  
<span data-ttu-id="0b0c0-119">Gültige Werte für diese Eigenschaft sind:</span><span class="sxs-lookup"><span data-stu-id="0b0c0-119">Valid values for this property include:</span></span> 
  
```cpp
network/postoffice/user 
Bruce@XYZZY.COM 
/c=US/a=att/p=Microsoft/o=Finance/ou=Purchasing/s=Furthur/g=Joe 
 
```

## <a name="related-resources"></a><span data-ttu-id="0b0c0-120">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="0b0c0-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0b0c0-121">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="0b0c0-121">Protocol specifications</span></span>

<span data-ttu-id="0b0c0-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0b0c0-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0b0c0-123">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="0b0c0-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0b0c0-124">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0b0c0-124">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0b0c0-125">Gibt die Eigenschaften und Operationen für Listen der Benutzer, Kontakte, Gruppen und Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="0b0c0-125">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
<span data-ttu-id="0b0c0-126">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0b0c0-126">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0b0c0-127">Konvertiert von Internet-standard-e-Mail-Konventionen in Message-Objekten.</span><span class="sxs-lookup"><span data-stu-id="0b0c0-127">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0b0c0-128">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="0b0c0-128">Header files</span></span>

<span data-ttu-id="0b0c0-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0b0c0-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="0b0c0-130">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="0b0c0-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="0b0c0-131">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="0b0c0-131">Mapitags.h</span></span>
  
> <span data-ttu-id="0b0c0-132">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="0b0c0-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0b0c0-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0b0c0-133">See also</span></span>



[<span data-ttu-id="0b0c0-134">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0b0c0-134">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0b0c0-135">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0b0c0-135">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0b0c0-136">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="0b0c0-136">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0b0c0-137">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="0b0c0-137">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

