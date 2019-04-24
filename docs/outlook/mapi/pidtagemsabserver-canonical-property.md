---
title: Kanonische Pidtagemsabserver (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagEmsAbServer
api_type:
- HeaderDef
ms.assetid: de942619-2507-8fe0-bc81-f9da9ef7266f
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: fba49b052a51bd498f61fc115f630d08fc6c8926
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335798"
---
# <a name="pidtagemsabserver-canonical-property"></a><span data-ttu-id="717fb-103">Kanonische Pidtagemsabserver (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="717fb-103">PidTagEmsAbServer Canonical Property</span></span>

  
  
<span data-ttu-id="717fb-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="717fb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="717fb-105">Gibt entweder den Pfad eines Adressbuch Containers in einem Offline Szenario oder den vollqualifizierten Domänennamen des globalen Katalogservers an, auf dem sich der Adressbuchcontainer in einem Online Szenario befindet.</span><span class="sxs-lookup"><span data-stu-id="717fb-105">Specifies either the path of an address book container in an offline scenario or the fully qualified domain name of the global catalog server where the address book container resides in an online scenario.</span></span>
  
## 

|||
|:-----|:-----|
|<span data-ttu-id="717fb-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="717fb-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="717fb-107">PR_EMS_AB_SERVER, PR_EMS_AB_SERVER_A, PR_EMS_AB_SERVER_W</span><span class="sxs-lookup"><span data-stu-id="717fb-107">PR_EMS_AB_SERVER, PR_EMS_AB_SERVER_A, PR_EMS_AB_SERVER_W</span></span>  <br/> |
|<span data-ttu-id="717fb-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="717fb-108">Identifier:</span></span>  <br/> |<span data-ttu-id="717fb-109">0xFFFE</span><span class="sxs-lookup"><span data-stu-id="717fb-109">0xFFFE</span></span>  <br/> |
|<span data-ttu-id="717fb-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="717fb-110">Data type:</span></span>  <br/> |<span data-ttu-id="717fb-111">PT_TSTRING</span><span class="sxs-lookup"><span data-stu-id="717fb-111">PT_TSTRING</span></span>  <br/> |
|<span data-ttu-id="717fb-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="717fb-112">Area:</span></span>  <br/> |<span data-ttu-id="717fb-113">Adressbuch</span><span class="sxs-lookup"><span data-stu-id="717fb-113">Address Book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="717fb-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="717fb-114">Remarks</span></span>

<span data-ttu-id="717fb-115">Diese Eigenschaft hat den Eigenschaftentyp auf **PT_UNICODE** zurückgesetzt, wenn Sie mit dem `UNICODE` Symbol auf einer Unicode-Plattform kompiliert wird, und zu **PT_String8** , wenn Sie nicht `UNICODE` mit dem Symbol kompiliert wird.</span><span class="sxs-lookup"><span data-stu-id="717fb-115">This property has the property type reset to **PT_UNICODE** when it is compiled with the  `UNICODE` symbol on a Unicode platform, and to **PT_STRING8** when it is not compiled with the  `UNICODE` symbol.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="717fb-116">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="717fb-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="717fb-117">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="717fb-117">Protocol specifications</span></span>

<span data-ttu-id="717fb-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="717fb-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="717fb-119">Stellt Definitionen für Eigenschaftensätze bereit.</span><span class="sxs-lookup"><span data-stu-id="717fb-119">Provides property set definitions.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="717fb-120">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="717fb-120">Header files</span></span>

<span data-ttu-id="717fb-121">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="717fb-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="717fb-122">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="717fb-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="717fb-123">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="717fb-123">Mapitags.h</span></span>
  
> <span data-ttu-id="717fb-124">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="717fb-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="717fb-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="717fb-125">See also</span></span>



[<span data-ttu-id="717fb-126">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="717fb-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="717fb-127">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="717fb-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="717fb-128">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="717fb-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="717fb-129">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="717fb-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

