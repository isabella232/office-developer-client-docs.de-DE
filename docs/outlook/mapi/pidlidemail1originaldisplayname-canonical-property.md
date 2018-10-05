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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399865"
---
# <a name="pidlidemail1originaldisplayname-canonical-property"></a><span data-ttu-id="25bb4-103">PidLidEmail1OriginalDisplayName (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="25bb4-103">PidLidEmail1OriginalDisplayName Canonical Property</span></span>

  
  
<span data-ttu-id="25bb4-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="25bb4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="25bb4-105">Gibt den ersten Anzeigenamen, der die die e-Mail-Adresse entspricht, die für den Kontakt angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="25bb4-105">Specifies the first display name that corresponds to the email address that is specified for the contact.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="25bb4-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="25bb4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="25bb4-107">dispidEmail1OriginalDisplayName</span><span class="sxs-lookup"><span data-stu-id="25bb4-107">dispidEmail1OriginalDisplayName</span></span>  <br/> |
|<span data-ttu-id="25bb4-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="25bb4-108">Property set:</span></span>  <br/> |<span data-ttu-id="25bb4-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="25bb4-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="25bb4-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="25bb4-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="25bb4-111">0x00008084</span><span class="sxs-lookup"><span data-stu-id="25bb4-111">0x00008084</span></span>  <br/> |
|<span data-ttu-id="25bb4-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="25bb4-112">Data type:</span></span>  <br/> |<span data-ttu-id="25bb4-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="25bb4-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="25bb4-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="25bb4-114">Area:</span></span>  <br/> |<span data-ttu-id="25bb4-115">Kontakt</span><span class="sxs-lookup"><span data-stu-id="25bb4-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="25bb4-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="25bb4-116">Remarks</span></span>

<span data-ttu-id="25bb4-117">Wenn der Wert der Eigenschaft **dispidEmail1AddrType** ([PidLidEmail1AddressType](pidlidemail1addresstype-canonical-property.md)) "SMTP" ist, sollte der Wert der jeweiligen **dispidEmail1OriginalDisplayName** -Eigenschaft den Wert der jeweiligen **entsprechen. dispidEmail1EmailAddress** -Eigenschaft ([PidLidEmail1EmailAddress](pidlidemail1emailaddress-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="25bb4-117">If the value of the **dispidEmail1AddrType** ([PidLidEmail1AddressType](pidlidemail1addresstype-canonical-property.md)) property is "SMTP", the value of the respective **dispidEmail1OriginalDisplayName** property should equal the value of the respective **dispidEmail1EmailAddress** ([PidLidEmail1EmailAddress](pidlidemail1emailaddress-canonical-property.md)) property.</span></span> <span data-ttu-id="25bb4-118">Diese Eigenschaft zeigt eine alternative benutzerfreundliche Adresse, die in der **dispidEmail1EmailAddress** -Eigenschaft entspricht.</span><span class="sxs-lookup"><span data-stu-id="25bb4-118">This property displays an alternative user-friendly address that is equivalent to the one in the **dispidEmail1EmailAddress** property.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="25bb4-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="25bb4-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="25bb4-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="25bb4-120">Protocol specifications</span></span>

<span data-ttu-id="25bb4-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="25bb4-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="25bb4-122">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="25bb4-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="25bb4-123">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="25bb4-123">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="25bb4-124">Gibt die Eigenschaften und Operationen, die für Kontakte und persönliche Verteilerlisten zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="25bb4-124">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="25bb4-125">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="25bb4-125">Header files</span></span>

<span data-ttu-id="25bb4-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="25bb4-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="25bb4-127">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="25bb4-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="25bb4-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="25bb4-128">See also</span></span>



[<span data-ttu-id="25bb4-129">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="25bb4-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="25bb4-130">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="25bb4-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="25bb4-131">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="25bb4-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="25bb4-132">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="25bb4-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

