---
title: PidLidEmail3OriginalDisplayName (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidEmail3OriginalDisplayName
api_type:
- COM
ms.assetid: f3fa392a-c3b1-46dd-bf9b-5ce310719542
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 3ac90910e143d05c17b73aa6a1062cd0999b0d3c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793529"
---
# <a name="pidlidemail3originaldisplayname-canonical-property"></a><span data-ttu-id="47edc-103">PidLidEmail3OriginalDisplayName (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="47edc-103">PidLidEmail3OriginalDisplayName Canonical Property</span></span>

  
  
<span data-ttu-id="47edc-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="47edc-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="47edc-105">Gibt den dritten Anzeigenamen, der die die e-Mail-Adresse entspricht, die für den Kontakt angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="47edc-105">Specifies the third display name that corresponds to the email address that is specified for the contact.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="47edc-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="47edc-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="47edc-107">dispidEmail3OriginalDisplayName</span><span class="sxs-lookup"><span data-stu-id="47edc-107">dispidEmail3OriginalDisplayName</span></span>  <br/> |
|<span data-ttu-id="47edc-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="47edc-108">Property set:</span></span>  <br/> |<span data-ttu-id="47edc-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="47edc-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="47edc-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="47edc-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="47edc-111">0x000080A4</span><span class="sxs-lookup"><span data-stu-id="47edc-111">0x000080A4</span></span>  <br/> |
|<span data-ttu-id="47edc-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="47edc-112">Data type:</span></span>  <br/> |<span data-ttu-id="47edc-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="47edc-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="47edc-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="47edc-114">Area:</span></span>  <br/> |<span data-ttu-id="47edc-115">Kontakt</span><span class="sxs-lookup"><span data-stu-id="47edc-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="47edc-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="47edc-116">Remarks</span></span>

<span data-ttu-id="47edc-117">Wenn der Wert der Eigenschaft **dispidEmail3AddrType** ([PidLidEmail3AddressType](pidlidemail3addresstype-canonical-property.md)) "SMTP" ist, sollte der Wert der jeweiligen **dispidEmail3OriginalDisplayName** -Eigenschaft den Wert der jeweiligen **entsprechen. dispidEmail3EmailAddress** ([PidLidEmail3EmailAddress](pidlidemail3emailaddress-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="47edc-117">If the value of the **dispidEmail3AddrType** ([PidLidEmail3AddressType](pidlidemail3addresstype-canonical-property.md)) property is "SMTP", the value of the respective **dispidEmail3OriginalDisplayName** property should equal the value of the respective **dispidEmail3EmailAddress** ([PidLidEmail3EmailAddress](pidlidemail3emailaddress-canonical-property.md)).</span></span> <span data-ttu-id="47edc-118">Der Zweck dieser Eigenschaft wird eine alternative benutzerfreundliche Adresse angezeigt, die in der **dispidEmail3EmailAddress**entspricht.</span><span class="sxs-lookup"><span data-stu-id="47edc-118">The purpose of this property is to display an alternative user-friendly address that is equivalent to the one in the **dispidEmail3EmailAddress**.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="47edc-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="47edc-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="47edc-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="47edc-120">Protocol specifications</span></span>

<span data-ttu-id="47edc-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="47edc-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="47edc-122">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="47edc-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="47edc-123">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="47edc-123">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="47edc-124">Gibt die Eigenschaften und Operationen, die für Kontakte und persönliche Verteilerlisten zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="47edc-124">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="47edc-125">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="47edc-125">Header files</span></span>

<span data-ttu-id="47edc-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="47edc-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="47edc-127">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="47edc-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="47edc-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="47edc-128">See also</span></span>



[<span data-ttu-id="47edc-129">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="47edc-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="47edc-130">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="47edc-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="47edc-131">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="47edc-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="47edc-132">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="47edc-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

