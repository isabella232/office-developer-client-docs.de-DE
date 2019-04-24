---
title: Kanonische PidTagEmailAddress-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: efcb72d872836adce544f3a90cf093de1f3713a7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338640"
---
# <a name="pidtagemailaddress-canonical-property"></a><span data-ttu-id="bb016-103">Kanonische PidTagEmailAddress-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="bb016-103">PidTagEmailAddress Canonical Property</span></span>

  
  
<span data-ttu-id="bb016-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bb016-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bb016-105">Enthält die e-Mail-Adresse des Messaging Benutzers.</span><span class="sxs-lookup"><span data-stu-id="bb016-105">Contains the messaging user's email address.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bb016-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="bb016-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bb016-107">PR_EMAIL_ADDRESS, PR_EMAIL_ADDRESS_A, PR_EMAIL_ADDRESS_W</span><span class="sxs-lookup"><span data-stu-id="bb016-107">PR_EMAIL_ADDRESS, PR_EMAIL_ADDRESS_A, PR_EMAIL_ADDRESS_W</span></span>  <br/> |
|<span data-ttu-id="bb016-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="bb016-108">Identifier:</span></span>  <br/> |<span data-ttu-id="bb016-109">0x3003</span><span class="sxs-lookup"><span data-stu-id="bb016-109">0x3003</span></span>  <br/> |
|<span data-ttu-id="bb016-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="bb016-110">Data type:</span></span>  <br/> |<span data-ttu-id="bb016-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="bb016-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="bb016-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="bb016-112">Area:</span></span>  <br/> |<span data-ttu-id="bb016-113">MAPI allgemein</span><span class="sxs-lookup"><span data-stu-id="bb016-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bb016-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bb016-114">Remarks</span></span>

<span data-ttu-id="bb016-115">Diese Eigenschaften sind Beispiele für die Eigenschaften der Basisadresse für alle Messagingbenutzer.</span><span class="sxs-lookup"><span data-stu-id="bb016-115">These properties are examples of the base address properties for all messaging users.</span></span> <span data-ttu-id="bb016-116">Es handelt sich um eine nullterminierte Zeichenfolge, deren Format nur für das zugrunde liegende Messagingsystem eine Bedeutung hat.</span><span class="sxs-lookup"><span data-stu-id="bb016-116">It is a null-terminated string whose format has meaning only for the underlying messaging system.</span></span> 
  
<span data-ttu-id="bb016-117">Diese Eigenschaften werden in Verbindung mit den Eigenschaften **PR_ADDRTYPE** ([Pidtagaddresstype (](pidtagaddresstype-canonical-property.md)) und **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) in Addressing Messages verwendet.</span><span class="sxs-lookup"><span data-stu-id="bb016-117">These properties are used in conjunction with the **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) and **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) properties in addressing messages.</span></span> <span data-ttu-id="bb016-118">Das Zeichenfolgenformat wird von **PR_ADDRTYPE**qualifiziert.</span><span class="sxs-lookup"><span data-stu-id="bb016-118">The string format is qualified by **PR_ADDRTYPE**.</span></span> 
  
<span data-ttu-id="bb016-119">Gültige Werte für diese Eigenschaft sind:</span><span class="sxs-lookup"><span data-stu-id="bb016-119">Valid values for this property include:</span></span> 
  
```cpp
network/postoffice/user 
Bruce@XYZZY.COM 
/c=US/a=att/p=Microsoft/o=Finance/ou=Purchasing/s=Furthur/g=Joe 
 
```

## <a name="related-resources"></a><span data-ttu-id="bb016-120">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="bb016-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="bb016-121">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="bb016-121">Protocol specifications</span></span>

<span data-ttu-id="bb016-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bb016-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bb016-123">Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="bb016-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="bb016-124">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bb016-124">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bb016-125">Gibt die Eigenschaften und Vorgänge für Listen von Benutzern, Kontakten, Gruppen und Ressourcen an.</span><span class="sxs-lookup"><span data-stu-id="bb016-125">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
<span data-ttu-id="bb016-126">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bb016-126">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bb016-127">Konvertiert von Internet Standard-e-Mail-Konventionen in Nachrichtenobjekte.</span><span class="sxs-lookup"><span data-stu-id="bb016-127">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="bb016-128">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="bb016-128">Header files</span></span>

<span data-ttu-id="bb016-129">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="bb016-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="bb016-130">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="bb016-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="bb016-131">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="bb016-131">Mapitags.h</span></span>
  
> <span data-ttu-id="bb016-132">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="bb016-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bb016-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bb016-133">See also</span></span>



[<span data-ttu-id="bb016-134">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="bb016-134">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bb016-135">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="bb016-135">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bb016-136">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="bb016-136">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bb016-137">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="bb016-137">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

