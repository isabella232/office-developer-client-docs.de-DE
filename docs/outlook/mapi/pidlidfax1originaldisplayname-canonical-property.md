---
title: PidLidFax1OriginalDisplayName (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidFax1OriginalDisplayName
api_type:
- COM
ms.assetid: 1520e27f-e261-4a94-be06-31cd47bea4a0
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: e24637ed9e29ab887833b6ed5ff7453353684a47
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398479"
---
# <a name="pidlidfax1originaldisplayname-canonical-property"></a><span data-ttu-id="80ef0-103">PidLidFax1OriginalDisplayName (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="80ef0-103">PidLidFax1OriginalDisplayName Canonical Property</span></span>

  
  
<span data-ttu-id="80ef0-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="80ef0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="80ef0-105">Gibt den ursprünglichen Anzeigenamen des Business Fax-Adresse des Kontakts an.</span><span class="sxs-lookup"><span data-stu-id="80ef0-105">Specifies the original display name of the contact's business fax address.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="80ef0-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="80ef0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="80ef0-107">dispidFax1OriginalDisplayName</span><span class="sxs-lookup"><span data-stu-id="80ef0-107">dispidFax1OriginalDisplayName</span></span>  <br/> |
|<span data-ttu-id="80ef0-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="80ef0-108">Property set:</span></span>  <br/> |<span data-ttu-id="80ef0-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="80ef0-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="80ef0-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="80ef0-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="80ef0-111">0x000080B4</span><span class="sxs-lookup"><span data-stu-id="80ef0-111">0x000080B4</span></span>  <br/> |
|<span data-ttu-id="80ef0-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="80ef0-112">Data type:</span></span>  <br/> |<span data-ttu-id="80ef0-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="80ef0-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="80ef0-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="80ef0-114">Area:</span></span>  <br/> |<span data-ttu-id="80ef0-115">Kontakt</span><span class="sxs-lookup"><span data-stu-id="80ef0-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="80ef0-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="80ef0-116">Remarks</span></span>

<span data-ttu-id="80ef0-117">Diese Eigenschaft muss falls vorhanden, auf den gleichen Wert wie die **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md))-Eigenschaft festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="80ef0-117">This property, if present, must be set to the same value as the **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="80ef0-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="80ef0-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="80ef0-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="80ef0-119">Protocol specifications</span></span>

<span data-ttu-id="80ef0-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="80ef0-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="80ef0-121">Enthält Set Eigenschaftendefinition und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="80ef0-121">Provides property set definition and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="80ef0-122">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="80ef0-122">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="80ef0-123">Gibt die Eigenschaften und Operationen, die für Kontakte und persönliche Verteilerlisten zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="80ef0-123">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="80ef0-124">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="80ef0-124">Header files</span></span>

<span data-ttu-id="80ef0-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="80ef0-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="80ef0-126">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="80ef0-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="80ef0-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="80ef0-127">See also</span></span>



[<span data-ttu-id="80ef0-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="80ef0-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="80ef0-129">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="80ef0-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="80ef0-130">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="80ef0-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="80ef0-131">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="80ef0-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

