---
title: Kanonische Pidnamerightsmanagementlicense (-Eigenschaft
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
ms.openlocfilehash: 889b823a55c39ebc19e52c8cc9a1d078a5732a01
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315022"
---
# <a name="pidnamerightsmanagementlicense-canonical-property"></a><span data-ttu-id="84de4-103">Kanonische Pidnamerightsmanagementlicense (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="84de4-103">PidNameRightsManagementLicense Canonical Property</span></span>

  
  
<span data-ttu-id="84de4-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="84de4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="84de4-105">Speichert die Nutzungslizenz für die mit rechten verwalteten e-Mail-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="84de4-105">Caches the use license for the rights-managed email message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="84de4-106">Angezeigte Namen:</span><span class="sxs-lookup"><span data-stu-id="84de4-106">Friendly names:</span></span>  <br/> |<span data-ttu-id="84de4-107">Keine</span><span class="sxs-lookup"><span data-stu-id="84de4-107">None</span></span>  <br/> |
|<span data-ttu-id="84de4-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="84de4-108">Property set:</span></span>  <br/> |<span data-ttu-id="84de4-109">PS_PUBLIC_STRINGS</span><span class="sxs-lookup"><span data-stu-id="84de4-109">PS_PUBLIC_STRINGS</span></span>  <br/> |
|<span data-ttu-id="84de4-110">Eigenschaftsname:</span><span class="sxs-lookup"><span data-stu-id="84de4-110">Property name:</span></span>  <br/> |<span data-ttu-id="84de4-111">DRMLicense</span><span class="sxs-lookup"><span data-stu-id="84de4-111">DRMLicense</span></span>  <br/> |
|<span data-ttu-id="84de4-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="84de4-112">Data type:</span></span>  <br/> |<span data-ttu-id="84de4-113">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="84de4-113">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="84de4-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="84de4-114">Area:</span></span>  <br/> |<span data-ttu-id="84de4-115">Sicheres Messaging</span><span class="sxs-lookup"><span data-stu-id="84de4-115">Secure messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="84de4-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="84de4-116">Remarks</span></span>

<span data-ttu-id="84de4-117">Wenn die Eigenschaft in einer e-Mail-Nachricht mit verwalteten Rechten vorhanden ist, muss der erste Wert dieser Eigenschaft mit mehreren Binärdateien die ZLIB (wie in [RFC1950]) komprimierte Nutzungslizenz für die mit rechten verwalteten e-Mail-Nachricht angegeben enthalten.</span><span class="sxs-lookup"><span data-stu-id="84de4-117">If the property is present on a rights-managed email message, the first value of this multiple binary property must contain the ZLIB (as specified in [RFC1950]) compressed use license for the rights-managed email message.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="84de4-118">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="84de4-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="84de4-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="84de4-119">Protocol specifications</span></span>

<span data-ttu-id="84de4-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="84de4-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="84de4-121">Stellt Eigenschaftensatz Definitionen und Verweise auf zugehörige Exchange Server-Protokollspezifikationen bereit.</span><span class="sxs-lookup"><span data-stu-id="84de4-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="84de4-122">[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="84de4-122">[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="84de4-123">Gibt die Eigenschaften von Nachrichten mit verwalteten Rechten an.</span><span class="sxs-lookup"><span data-stu-id="84de4-123">Specifies the properties of rights-managed encoded messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="84de4-124">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="84de4-124">Header files</span></span>

<span data-ttu-id="84de4-125">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="84de4-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="84de4-126">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="84de4-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="84de4-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="84de4-127">See also</span></span>



[<span data-ttu-id="84de4-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="84de4-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="84de4-129">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="84de4-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="84de4-130">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="84de4-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="84de4-131">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="84de4-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

