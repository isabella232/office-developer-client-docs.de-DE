---
title: PidLidEmail2OriginalDisplayName (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidEmail2OriginalDisplayName
api_type:
- COM
ms.assetid: 0b648ef6-86ed-40ee-b068-8fcde7e0fe75
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 7fb7e5afa6a1c050a5d91274bc4f82439fb98640
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337961"
---
# <a name="pidlidemail2originaldisplayname-canonical-property"></a><span data-ttu-id="227ae-103">PidLidEmail2OriginalDisplayName (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="227ae-103">PidLidEmail2OriginalDisplayName Canonical Property</span></span>

  
  
<span data-ttu-id="227ae-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="227ae-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="227ae-105">Gibt den zweiten Anzeigenamen an, der der für den Kontakt angegebenen E-Mail-Adresse entspricht.</span><span class="sxs-lookup"><span data-stu-id="227ae-105">Specifies the second display name that corresponds to the email address specified for the contact.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="227ae-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="227ae-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="227ae-107">dispidEmail2OriginalDisplayName</span><span class="sxs-lookup"><span data-stu-id="227ae-107">dispidEmail2OriginalDisplayName</span></span>  <br/> |
|<span data-ttu-id="227ae-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="227ae-108">Property set:</span></span>  <br/> |<span data-ttu-id="227ae-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="227ae-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="227ae-110">Lange ID (LID):</span><span class="sxs-lookup"><span data-stu-id="227ae-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="227ae-111">0x00008094</span><span class="sxs-lookup"><span data-stu-id="227ae-111">0x00008094</span></span>  <br/> |
|<span data-ttu-id="227ae-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="227ae-112">Data type:</span></span>  <br/> |<span data-ttu-id="227ae-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="227ae-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="227ae-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="227ae-114">Area:</span></span>  <br/> |<span data-ttu-id="227ae-115">Kontakt</span><span class="sxs-lookup"><span data-stu-id="227ae-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="227ae-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="227ae-116">Remarks</span></span>

<span data-ttu-id="227ae-117">Wenn der Wert der **dispidEmail2AddrType** ([PidLidEmail2AddressType](pidlidemail2addresstype-canonical-property.md)) -Eigenschaft "SMTP" ist, sollte der Wert der entsprechenden **PidLidEmail2OriginalDisplayName** -Eigenschaft dem Wert der entsprechenden **dispidEmail2EmailAddress** ([PidLidEmail2EmailAddress](pidlidemail2emailaddress-canonical-property.md)) -Eigenschaft entspricht.</span><span class="sxs-lookup"><span data-stu-id="227ae-117">If the value of the **dispidEmail2AddrType** ([PidLidEmail2AddressType](pidlidemail2addresstype-canonical-property.md)) property is "SMTP", the value of the respective **PidLidEmail2OriginalDisplayName** property should equal the value of the respective **dispidEmail2EmailAddress** ([PidLidEmail2EmailAddress](pidlidemail2emailaddress-canonical-property.md)) property.</span></span> <span data-ttu-id="227ae-118">Der Zweck dieser Eigenschaft besteht in der Anzeige einer alternativen benutzerfreundlichen Adresse, die der in **dispidEmail2EmailAddress entspricht.**</span><span class="sxs-lookup"><span data-stu-id="227ae-118">The purpose of this property is to display an alternative user-friendly address that is equivalent to the one in the **dispidEmail2EmailAddress**.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="227ae-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="227ae-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="227ae-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="227ae-120">Protocol specifications</span></span>

<span data-ttu-id="227ae-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="227ae-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="227ae-122">Stellt Eigenschaftensatzdefinitionen und Verweise auf verwandte Exchange Server zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="227ae-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="227ae-123">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="227ae-123">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="227ae-124">Gibt die Eigenschaften und Vorgänge an, die für Kontakte und persönliche Verteilerlisten zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="227ae-124">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="227ae-125">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="227ae-125">Header files</span></span>

<span data-ttu-id="227ae-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="227ae-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="227ae-127">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="227ae-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="227ae-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="227ae-128">See also</span></span>



[<span data-ttu-id="227ae-129">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="227ae-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="227ae-130">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="227ae-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="227ae-131">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="227ae-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="227ae-132">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="227ae-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

