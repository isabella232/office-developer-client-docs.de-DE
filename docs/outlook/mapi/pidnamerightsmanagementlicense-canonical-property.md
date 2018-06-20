---
title: Kanonische PidNameRightsManagementLicense-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidNameRightsManagementLicense
api_type:
- COM
ms.assetid: ca3c9317-7873-4f37-b78f-b35467c81c29
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: c75cb480b9a1a7ffdcff9c0f9b49aabba746fc3e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793995"
---
# <a name="pidnamerightsmanagementlicense-canonical-property"></a><span data-ttu-id="2511b-103">Kanonische PidNameRightsManagementLicense-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="2511b-103">PidNameRightsManagementLicense Canonical Property</span></span>

  
  
<span data-ttu-id="2511b-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2511b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2511b-105">Speichert die Lizenz für die rechteverwaltung e-Mail-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="2511b-105">Caches the use license for the rights-managed email message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2511b-106">Anzeigenamen:</span><span class="sxs-lookup"><span data-stu-id="2511b-106">Friendly names:</span></span>  <br/> |<span data-ttu-id="2511b-107">Keine</span><span class="sxs-lookup"><span data-stu-id="2511b-107">None</span></span>  <br/> |
|<span data-ttu-id="2511b-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="2511b-108">Property set:</span></span>  <br/> |<span data-ttu-id="2511b-109">PS_PUBLIC_STRINGS</span><span class="sxs-lookup"><span data-stu-id="2511b-109">PS_PUBLIC_STRINGS</span></span>  <br/> |
|<span data-ttu-id="2511b-110">Name der Eigenschaft:</span><span class="sxs-lookup"><span data-stu-id="2511b-110">Property name:</span></span>  <br/> |<span data-ttu-id="2511b-111">DRMLicense</span><span class="sxs-lookup"><span data-stu-id="2511b-111">DRMLicense</span></span>  <br/> |
|<span data-ttu-id="2511b-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="2511b-112">Data type:</span></span>  <br/> |<span data-ttu-id="2511b-113">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="2511b-113">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="2511b-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="2511b-114">Area:</span></span>  <br/> |<span data-ttu-id="2511b-115">Sichere Nachrichten</span><span class="sxs-lookup"><span data-stu-id="2511b-115">Secure messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2511b-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2511b-116">Remarks</span></span>

<span data-ttu-id="2511b-117">Wenn die Eigenschaft auf eine e-Mail mit verwalteten rechten vorhanden ist, muss der erste Wert dieser Eigenschaft für mehrere binäre komprimierte Nutzungslizenz ZLIB (wie in [RFC1950] angegeben) für die rechteverwaltung e-Mail-Nachricht enthalten.</span><span class="sxs-lookup"><span data-stu-id="2511b-117">If the property is present on a rights-managed email message, the first value of this multiple binary property must contain the ZLIB (as specified in [RFC1950]) compressed use license for the rights-managed email message.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="2511b-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="2511b-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="2511b-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="2511b-119">Protocol specifications</span></span>

<span data-ttu-id="2511b-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2511b-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2511b-121">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="2511b-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="2511b-122">[[MS-OXORMMS]](http://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2511b-122">[[MS-OXORMMS]](http://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2511b-123">Gibt die Eigenschaften der codierten Nachrichten, deren Rechte verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="2511b-123">Specifies the properties of rights-managed encoded messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="2511b-124">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="2511b-124">Header files</span></span>

<span data-ttu-id="2511b-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2511b-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="2511b-126">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="2511b-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2511b-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2511b-127">See also</span></span>



[<span data-ttu-id="2511b-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2511b-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2511b-129">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2511b-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2511b-130">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="2511b-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2511b-131">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="2511b-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

