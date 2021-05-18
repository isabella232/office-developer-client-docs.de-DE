---
title: PidLidFileUnder (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidFileUnder
api_type:
- COM
ms.assetid: 55afc4bb-c5fc-4162-a293-7d82644b1965
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 02aa1766421f7c116eabac4c9661be1b5b1adee1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359570"
---
# <a name="pidlidfileunder-canonical-property"></a><span data-ttu-id="dc98b-103">PidLidFileUnder (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="dc98b-103">PidLidFileUnder Canonical Property</span></span>

  
  
<span data-ttu-id="dc98b-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dc98b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dc98b-105">Gibt den Namen an, unter dem der Kontakt beim Anzeigen einer Kontaktliste abgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="dc98b-105">Specifies the name under which the contact is filed when displaying a list of contacts.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="dc98b-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="dc98b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="dc98b-107">dispidFileUnder</span><span class="sxs-lookup"><span data-stu-id="dc98b-107">dispidFileUnder</span></span>  <br/> |
|<span data-ttu-id="dc98b-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="dc98b-108">Property set:</span></span>  <br/> |<span data-ttu-id="dc98b-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="dc98b-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="dc98b-110">Lange ID (LID):</span><span class="sxs-lookup"><span data-stu-id="dc98b-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="dc98b-111">0x00008005</span><span class="sxs-lookup"><span data-stu-id="dc98b-111">0x00008005</span></span>  <br/> |
|<span data-ttu-id="dc98b-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="dc98b-112">Data type:</span></span>  <br/> |<span data-ttu-id="dc98b-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="dc98b-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="dc98b-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="dc98b-114">Area:</span></span>  <br/> |<span data-ttu-id="dc98b-115">Kontakt</span><span class="sxs-lookup"><span data-stu-id="dc98b-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dc98b-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="dc98b-116">Remarks</span></span>

<span data-ttu-id="dc98b-117">Die Anwendung sollte diese Eigenschaft als leere PT_UNICODE, wenn sie im Kontakt fehlt.</span><span class="sxs-lookup"><span data-stu-id="dc98b-117">The application should treat this property as an empty PT_UNICODE if it is missing from the contact.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="dc98b-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="dc98b-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="dc98b-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="dc98b-119">Protocol specifications</span></span>

<span data-ttu-id="dc98b-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dc98b-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="dc98b-121">Stellt Eigenschaftensatzdefinitionen und Verweise auf verwandte Exchange Server zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="dc98b-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="dc98b-122">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dc98b-122">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="dc98b-123">Gibt die Eigenschaften und Vorgänge an, die für Kontakte und persönliche Verteilerlisten zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="dc98b-123">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="dc98b-124">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="dc98b-124">Header files</span></span>

<span data-ttu-id="dc98b-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="dc98b-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="dc98b-126">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="dc98b-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="dc98b-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dc98b-127">See also</span></span>



[<span data-ttu-id="dc98b-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="dc98b-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="dc98b-129">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="dc98b-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="dc98b-130">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="dc98b-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="dc98b-131">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="dc98b-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

