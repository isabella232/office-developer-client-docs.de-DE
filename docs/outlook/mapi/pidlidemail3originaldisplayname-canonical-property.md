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
ms.openlocfilehash: e69bcde35bcfec7746893ee18423aca3a24a6c4a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338073"
---
# <a name="pidlidemail3originaldisplayname-canonical-property"></a><span data-ttu-id="6e190-103">PidLidEmail3OriginalDisplayName (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="6e190-103">PidLidEmail3OriginalDisplayName Canonical Property</span></span>

  
  
<span data-ttu-id="6e190-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6e190-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6e190-105">Gibt den dritten Anzeigenamen an, der der für den Kontakt angegebenen E-Mail-Adresse entspricht.</span><span class="sxs-lookup"><span data-stu-id="6e190-105">Specifies the third display name that corresponds to the email address that is specified for the contact.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6e190-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="6e190-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6e190-107">dispidEmail3OriginalDisplayName</span><span class="sxs-lookup"><span data-stu-id="6e190-107">dispidEmail3OriginalDisplayName</span></span>  <br/> |
|<span data-ttu-id="6e190-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="6e190-108">Property set:</span></span>  <br/> |<span data-ttu-id="6e190-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="6e190-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="6e190-110">Lange ID (LID):</span><span class="sxs-lookup"><span data-stu-id="6e190-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="6e190-111">0x000080A4</span><span class="sxs-lookup"><span data-stu-id="6e190-111">0x000080A4</span></span>  <br/> |
|<span data-ttu-id="6e190-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="6e190-112">Data type:</span></span>  <br/> |<span data-ttu-id="6e190-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="6e190-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="6e190-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="6e190-114">Area:</span></span>  <br/> |<span data-ttu-id="6e190-115">Kontakt</span><span class="sxs-lookup"><span data-stu-id="6e190-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6e190-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="6e190-116">Remarks</span></span>

<span data-ttu-id="6e190-117">Wenn der Wert der **dispidEmail3AddrType** ([PidLidEmail3AddressType](pidlidemail3addresstype-canonical-property.md))-Eigenschaft "SMTP" ist, sollte der Wert der entsprechenden **dispidEmail3OriginalDisplayName-Eigenschaft** dem Wert der entsprechenden **dispidEmail3EmailAddress** ([PidLidEmail3EmailAddress](pidlidemail3emailaddress-canonical-property.md)) entspricht.</span><span class="sxs-lookup"><span data-stu-id="6e190-117">If the value of the **dispidEmail3AddrType** ([PidLidEmail3AddressType](pidlidemail3addresstype-canonical-property.md)) property is "SMTP", the value of the respective **dispidEmail3OriginalDisplayName** property should equal the value of the respective **dispidEmail3EmailAddress** ([PidLidEmail3EmailAddress](pidlidemail3emailaddress-canonical-property.md)).</span></span> <span data-ttu-id="6e190-118">Der Zweck dieser Eigenschaft besteht in der Anzeige einer alternativen benutzerfreundlichen Adresse, die der in **dispidEmail3EmailAddress entspricht.**</span><span class="sxs-lookup"><span data-stu-id="6e190-118">The purpose of this property is to display an alternative user-friendly address that is equivalent to the one in the **dispidEmail3EmailAddress**.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="6e190-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="6e190-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6e190-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="6e190-120">Protocol specifications</span></span>

<span data-ttu-id="6e190-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6e190-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6e190-122">Stellt Eigenschaftensatzdefinitionen und Verweise auf verwandte Exchange Server zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="6e190-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6e190-123">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6e190-123">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6e190-124">Gibt die Eigenschaften und Vorgänge an, die für Kontakte und persönliche Verteilerlisten zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="6e190-124">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6e190-125">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="6e190-125">Header files</span></span>

<span data-ttu-id="6e190-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6e190-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="6e190-127">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="6e190-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6e190-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6e190-128">See also</span></span>



[<span data-ttu-id="6e190-129">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6e190-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6e190-130">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="6e190-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6e190-131">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="6e190-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6e190-132">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="6e190-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

