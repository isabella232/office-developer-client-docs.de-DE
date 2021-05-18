---
title: PidNameRightsManagementLicense (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 889b823a55c39ebc19e52c8cc9a1d078a5732a01
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315022"
---
# <a name="pidnamerightsmanagementlicense-canonical-property"></a><span data-ttu-id="9aecd-103">PidNameRightsManagementLicense (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="9aecd-103">PidNameRightsManagementLicense Canonical Property</span></span>

  
  
<span data-ttu-id="9aecd-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9aecd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9aecd-105">Speichert die Verwendungslizenz für die E-Mail-Nachricht mit verwalteten Rechten zwischen.</span><span class="sxs-lookup"><span data-stu-id="9aecd-105">Caches the use license for the rights-managed email message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9aecd-106">Anzeigenamen:</span><span class="sxs-lookup"><span data-stu-id="9aecd-106">Friendly names:</span></span>  <br/> |<span data-ttu-id="9aecd-107">Keine</span><span class="sxs-lookup"><span data-stu-id="9aecd-107">None</span></span>  <br/> |
|<span data-ttu-id="9aecd-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="9aecd-108">Property set:</span></span>  <br/> |<span data-ttu-id="9aecd-109">PS_PUBLIC_STRINGS</span><span class="sxs-lookup"><span data-stu-id="9aecd-109">PS_PUBLIC_STRINGS</span></span>  <br/> |
|<span data-ttu-id="9aecd-110">Eigenschaftsname:</span><span class="sxs-lookup"><span data-stu-id="9aecd-110">Property name:</span></span>  <br/> |<span data-ttu-id="9aecd-111">DRMLicense</span><span class="sxs-lookup"><span data-stu-id="9aecd-111">DRMLicense</span></span>  <br/> |
|<span data-ttu-id="9aecd-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="9aecd-112">Data type:</span></span>  <br/> |<span data-ttu-id="9aecd-113">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="9aecd-113">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="9aecd-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="9aecd-114">Area:</span></span>  <br/> |<span data-ttu-id="9aecd-115">Sicheres Messaging</span><span class="sxs-lookup"><span data-stu-id="9aecd-115">Secure messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9aecd-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9aecd-116">Remarks</span></span>

<span data-ttu-id="9aecd-117">Wenn die Eigenschaft in einer E-Mail-Nachricht mit verwalteten Rechten vorhanden ist, muss der erste Wert dieser mehreren binären Eigenschaft die komprimierte ZLIB-Lizenz (wie in [RFC1950]) angegeben für die E-Mail-Nachricht mit verwalteten Rechten enthalten.</span><span class="sxs-lookup"><span data-stu-id="9aecd-117">If the property is present on a rights-managed email message, the first value of this multiple binary property must contain the ZLIB (as specified in [RFC1950]) compressed use license for the rights-managed email message.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="9aecd-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="9aecd-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9aecd-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="9aecd-119">Protocol specifications</span></span>

<span data-ttu-id="9aecd-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9aecd-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9aecd-121">Stellt Eigenschaftensatzdefinitionen und Verweise auf verwandte Exchange Server zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="9aecd-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9aecd-122">[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9aecd-122">[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9aecd-123">Gibt die Eigenschaften von mit Rechten verwalteten codierten Nachrichten an.</span><span class="sxs-lookup"><span data-stu-id="9aecd-123">Specifies the properties of rights-managed encoded messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9aecd-124">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="9aecd-124">Header files</span></span>

<span data-ttu-id="9aecd-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9aecd-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="9aecd-126">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="9aecd-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9aecd-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9aecd-127">See also</span></span>



[<span data-ttu-id="9aecd-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9aecd-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9aecd-129">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="9aecd-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9aecd-130">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="9aecd-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9aecd-131">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="9aecd-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

