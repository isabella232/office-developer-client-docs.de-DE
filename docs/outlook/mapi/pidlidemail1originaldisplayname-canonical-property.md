---
title: PidLidEmail1OriginalDisplayName (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidEmail1OriginalDisplayName
api_type:
- COM
ms.assetid: 991c2969-0180-4c7d-95ee-e62fd24d67ef
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: a20ae8e3f19073bfb88d58db516a0e5f93d91445
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335042"
---
# <a name="pidlidemail1originaldisplayname-canonical-property"></a><span data-ttu-id="df62f-103">PidLidEmail1OriginalDisplayName (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="df62f-103">PidLidEmail1OriginalDisplayName Canonical Property</span></span>

  
  
<span data-ttu-id="df62f-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="df62f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="df62f-105">Gibt den ersten Anzeigenamen an, der der für den Kontakt angegebenen E-Mail-Adresse entspricht.</span><span class="sxs-lookup"><span data-stu-id="df62f-105">Specifies the first display name that corresponds to the email address that is specified for the contact.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="df62f-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="df62f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="df62f-107">dispidEmail1OriginalDisplayName</span><span class="sxs-lookup"><span data-stu-id="df62f-107">dispidEmail1OriginalDisplayName</span></span>  <br/> |
|<span data-ttu-id="df62f-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="df62f-108">Property set:</span></span>  <br/> |<span data-ttu-id="df62f-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="df62f-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="df62f-110">Lange ID (LID):</span><span class="sxs-lookup"><span data-stu-id="df62f-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="df62f-111">0x00008084</span><span class="sxs-lookup"><span data-stu-id="df62f-111">0x00008084</span></span>  <br/> |
|<span data-ttu-id="df62f-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="df62f-112">Data type:</span></span>  <br/> |<span data-ttu-id="df62f-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="df62f-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="df62f-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="df62f-114">Area:</span></span>  <br/> |<span data-ttu-id="df62f-115">Kontakt</span><span class="sxs-lookup"><span data-stu-id="df62f-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="df62f-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="df62f-116">Remarks</span></span>

<span data-ttu-id="df62f-117">Wenn der Wert der **dispidEmail1AddrType** ([PidLidEmail1AddressType](pidlidemail1addresstype-canonical-property.md)) -Eigenschaft "SMTP" ist, sollte der Wert der entsprechenden **dispidEmail1OriginalDisplayName** -Eigenschaft dem Wert der entsprechenden **dispidEmail1EmailAddress** ([PidLidEmail1EmailAddress](pidlidemail1emailaddress-canonical-property.md)) -Eigenschaft entspricht.</span><span class="sxs-lookup"><span data-stu-id="df62f-117">If the value of the **dispidEmail1AddrType** ([PidLidEmail1AddressType](pidlidemail1addresstype-canonical-property.md)) property is "SMTP", the value of the respective **dispidEmail1OriginalDisplayName** property should equal the value of the respective **dispidEmail1EmailAddress** ([PidLidEmail1EmailAddress](pidlidemail1emailaddress-canonical-property.md)) property.</span></span> <span data-ttu-id="df62f-118">Diese Eigenschaft zeigt eine alternative benutzerfreundlichen Adresse an, die der in der **eigenschaft dispidEmail1EmailAddress entspricht.**</span><span class="sxs-lookup"><span data-stu-id="df62f-118">This property displays an alternative user-friendly address that is equivalent to the one in the **dispidEmail1EmailAddress** property.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="df62f-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="df62f-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="df62f-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="df62f-120">Protocol specifications</span></span>

<span data-ttu-id="df62f-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="df62f-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="df62f-122">Stellt Eigenschaftensatzdefinitionen und Verweise auf verwandte Exchange Server zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="df62f-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="df62f-123">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="df62f-123">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="df62f-124">Gibt die Eigenschaften und Vorgänge an, die für Kontakte und persönliche Verteilerlisten zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="df62f-124">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="df62f-125">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="df62f-125">Header files</span></span>

<span data-ttu-id="df62f-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="df62f-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="df62f-127">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="df62f-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="df62f-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="df62f-128">See also</span></span>



[<span data-ttu-id="df62f-129">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="df62f-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="df62f-130">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="df62f-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="df62f-131">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="df62f-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="df62f-132">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="df62f-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

