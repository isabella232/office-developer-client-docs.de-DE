---
title: Kanonische Pidlidcontactcharacterset (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidContactCharacterSet
api_type:
- COM
ms.assetid: a167e199-a9b2-47f9-a90e-2abc7c29828c
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 0329147463db38fb8c547214788366444daed312
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319705"
---
# <a name="pidlidcontactcharacterset-canonical-property"></a><span data-ttu-id="3395f-103">Kanonische Pidlidcontactcharacterset (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="3395f-103">PidLidContactCharacterSet Canonical Property</span></span>

  
  
<span data-ttu-id="3395f-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3395f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3395f-105">Gibt den Zeichensatz an, der für diesen Kontakt verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3395f-105">Specifies the character set used for this contact.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3395f-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="3395f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3395f-107">dispidContactCharSet</span><span class="sxs-lookup"><span data-stu-id="3395f-107">dispidContactCharSet</span></span>  <br/> |
|<span data-ttu-id="3395f-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="3395f-108">Property set:</span></span>  <br/> |<span data-ttu-id="3395f-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="3395f-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="3395f-110">Long-ID (Deckel):</span><span class="sxs-lookup"><span data-stu-id="3395f-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="3395f-111">0x00008023</span><span class="sxs-lookup"><span data-stu-id="3395f-111">0x00008023</span></span>  <br/> |
|<span data-ttu-id="3395f-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="3395f-112">Data type:</span></span>  <br/> |<span data-ttu-id="3395f-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="3395f-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="3395f-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="3395f-114">Area:</span></span>  <br/> |<span data-ttu-id="3395f-115">Kontakt</span><span class="sxs-lookup"><span data-stu-id="3395f-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3395f-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3395f-116">Remarks</span></span>

<span data-ttu-id="3395f-117">Anwendungen können diese Eigenschaft verwenden, um eine abhängige Auswahlliste für die **dispidFileUnder** ([Pidlidfileunder (](pidlidfileunder-canonical-property.md)), **DispidFileUnderList** ([pidlidfileunderlist (](pidlidfileunderlist-canonical-property.md)) und dispidFileUnderId zu generieren. \*\* \*\*([Pidlidfileunderid (](pidlidfileunderid-canonical-property.md))-Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="3395f-117">Applications can use this property to aid in generating a character-set dependent list of choices for the **dispidFileUnder** ([PidLidFileUnder](pidlidfileunder-canonical-property.md)) , **dispidFileUnderList** ([PidLidFileUnderList](pidlidfileunderlist-canonical-property.md)) , and **dispidFileUnderId** ([PidLidFileUnderId](pidlidfileunderid-canonical-property.md)) properties.</span></span> <span data-ttu-id="3395f-118">Wenn der Wert der Eigenschaft "0x00000000" oder "0x00000001" ist, sollten Anwendungen die Eigenschaft als nicht festgelegt behandeln.</span><span class="sxs-lookup"><span data-stu-id="3395f-118">If the value of the property is "0x00000000" or "0x00000001", applications should treat the property as not being set.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="3395f-119">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="3395f-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3395f-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="3395f-120">Protocol specifications</span></span>

<span data-ttu-id="3395f-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3395f-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3395f-122">Stellt Eigenschaftensatz Definitionen und Verweise auf zugehörige Exchange Server-Protokollspezifikationen bereit.</span><span class="sxs-lookup"><span data-stu-id="3395f-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="3395f-123">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3395f-123">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3395f-124">Gibt die Eigenschaften und Vorgänge an, die für Kontakte und persönliche Verteilerlisten zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="3395f-124">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3395f-125">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="3395f-125">Header files</span></span>

<span data-ttu-id="3395f-126">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="3395f-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="3395f-127">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="3395f-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3395f-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3395f-128">See also</span></span>



[<span data-ttu-id="3395f-129">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3395f-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3395f-130">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3395f-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3395f-131">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="3395f-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3395f-132">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="3395f-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

