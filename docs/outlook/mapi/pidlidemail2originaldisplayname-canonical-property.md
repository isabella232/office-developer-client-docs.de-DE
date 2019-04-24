---
title: Kanonische Pidlidemail2originaldisplayname (-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 7fb7e5afa6a1c050a5d91274bc4f82439fb98640
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337961"
---
# <a name="pidlidemail2originaldisplayname-canonical-property"></a><span data-ttu-id="a0dc2-103">Kanonische Pidlidemail2originaldisplayname (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="a0dc2-103">PidLidEmail2OriginalDisplayName Canonical Property</span></span>

  
  
<span data-ttu-id="a0dc2-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a0dc2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a0dc2-105">Gibt den zweiten Anzeigenamen an, der der für den Kontakt angegebenen e-Mail-Adresse entspricht.</span><span class="sxs-lookup"><span data-stu-id="a0dc2-105">Specifies the second display name that corresponds to the email address specified for the contact.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a0dc2-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="a0dc2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a0dc2-107">dispidEmail2OriginalDisplayName</span><span class="sxs-lookup"><span data-stu-id="a0dc2-107">dispidEmail2OriginalDisplayName</span></span>  <br/> |
|<span data-ttu-id="a0dc2-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="a0dc2-108">Property set:</span></span>  <br/> |<span data-ttu-id="a0dc2-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="a0dc2-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="a0dc2-110">Long-ID (Deckel):</span><span class="sxs-lookup"><span data-stu-id="a0dc2-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="a0dc2-111">0x00008094</span><span class="sxs-lookup"><span data-stu-id="a0dc2-111">0x00008094</span></span>  <br/> |
|<span data-ttu-id="a0dc2-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="a0dc2-112">Data type:</span></span>  <br/> |<span data-ttu-id="a0dc2-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="a0dc2-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="a0dc2-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="a0dc2-114">Area:</span></span>  <br/> |<span data-ttu-id="a0dc2-115">Kontakt</span><span class="sxs-lookup"><span data-stu-id="a0dc2-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a0dc2-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a0dc2-116">Remarks</span></span>

<span data-ttu-id="a0dc2-117">Wenn der Wert der **dispidEmail2AddrType** ([pidlidemail2addresstype (](pidlidemail2addresstype-canonical-property.md))-Eigenschaft "SMTP" lautet, sollte der Wert der entsprechenden **pidlidemail2originaldisplayname (** -Eigenschaft dem Wert der entsprechenden \*\* dispidEmail2EmailAddress\*\* ([pidlidemail2emailaddress (](pidlidemail2emailaddress-canonical-property.md))-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="a0dc2-117">If the value of the **dispidEmail2AddrType** ([PidLidEmail2AddressType](pidlidemail2addresstype-canonical-property.md)) property is "SMTP", the value of the respective **PidLidEmail2OriginalDisplayName** property should equal the value of the respective **dispidEmail2EmailAddress** ([PidLidEmail2EmailAddress](pidlidemail2emailaddress-canonical-property.md)) property.</span></span> <span data-ttu-id="a0dc2-118">Der Zweck dieser Eigenschaft ist es, eine Alternative benutzerfreundliche Adresse anzuzeigen, die dem in der **dispidEmail2EmailAddress**entspricht.</span><span class="sxs-lookup"><span data-stu-id="a0dc2-118">The purpose of this property is to display an alternative user-friendly address that is equivalent to the one in the **dispidEmail2EmailAddress**.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="a0dc2-119">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="a0dc2-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a0dc2-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="a0dc2-120">Protocol specifications</span></span>

<span data-ttu-id="a0dc2-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a0dc2-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a0dc2-122">Stellt Eigenschaftensatz Definitionen und Verweise auf zugehörige Exchange Server-Protokollspezifikationen bereit.</span><span class="sxs-lookup"><span data-stu-id="a0dc2-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a0dc2-123">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a0dc2-123">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a0dc2-124">Gibt die Eigenschaften und Vorgänge an, die für Kontakte und persönliche Verteilerlisten zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="a0dc2-124">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a0dc2-125">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="a0dc2-125">Header files</span></span>

<span data-ttu-id="a0dc2-126">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="a0dc2-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="a0dc2-127">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="a0dc2-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a0dc2-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a0dc2-128">See also</span></span>



[<span data-ttu-id="a0dc2-129">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a0dc2-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a0dc2-130">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a0dc2-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a0dc2-131">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="a0dc2-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a0dc2-132">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="a0dc2-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

