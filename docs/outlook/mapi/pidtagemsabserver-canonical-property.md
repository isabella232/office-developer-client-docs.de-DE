---
title: Kanonische PidTagEmsAbServer-Eigenschaft
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
ms.openlocfilehash: 27e3a9687d66bd1cd3586a25a3ca5792523096c2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794337"
---
# <a name="pidtagemsabserver-canonical-property"></a><span data-ttu-id="62421-103">Kanonische PidTagEmsAbServer-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="62421-103">PidTagEmsAbServer Canonical Property</span></span>

  
  
<span data-ttu-id="62421-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="62421-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="62421-105">Gibt entweder den Pfad einer Adressbuchcontainer in einem Szenario offline oder den vollqualifizierten Domänennamen des globalen Katalogservers Adressbuchcontainer sich in einem Szenario online befindet.</span><span class="sxs-lookup"><span data-stu-id="62421-105">Specifies either the path of an address book container in an offline scenario or the fully qualified domain name of the global catalog server where the address book container resides in an online scenario.</span></span>
  
## 

|||
|:-----|:-----|
|<span data-ttu-id="62421-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="62421-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="62421-107">PR_EMS_AB_SERVER, PR_EMS_AB_SERVER_A, PR_EMS_AB_SERVER_W</span><span class="sxs-lookup"><span data-stu-id="62421-107">PR_EMS_AB_SERVER, PR_EMS_AB_SERVER_A, PR_EMS_AB_SERVER_W</span></span>  <br/> |
|<span data-ttu-id="62421-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="62421-108">Identifier:</span></span>  <br/> |<span data-ttu-id="62421-109">0xFFFE</span><span class="sxs-lookup"><span data-stu-id="62421-109">0xFFFE</span></span>  <br/> |
|<span data-ttu-id="62421-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="62421-110">Data type:</span></span>  <br/> |<span data-ttu-id="62421-111">PT_TSTRING</span><span class="sxs-lookup"><span data-stu-id="62421-111">PT_TSTRING</span></span>  <br/> |
|<span data-ttu-id="62421-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="62421-112">Area:</span></span>  <br/> |<span data-ttu-id="62421-113">Adressbuch</span><span class="sxs-lookup"><span data-stu-id="62421-113">Address Book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="62421-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="62421-114">Remarks</span></span>

<span data-ttu-id="62421-115">Diese Eigenschaft hat den Eigenschaftentyp auf **PT_UNICODE** zurückzusetzen, wenn die Kompilierung der `UNICODE` Symbol auf einer Unicode-Plattform und **PT_STRING8** bei der Kompilierung nicht mit der `UNICODE` Symbol.</span><span class="sxs-lookup"><span data-stu-id="62421-115">This property has the property type reset to **PT_UNICODE** when it is compiled with the  `UNICODE` symbol on a Unicode platform, and to **PT_STRING8** when it is not compiled with the  `UNICODE` symbol.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="62421-116">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="62421-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="62421-117">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="62421-117">Protocol specifications</span></span>

<span data-ttu-id="62421-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="62421-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="62421-119">Enthält Eigenschaftendefinitionen an.</span><span class="sxs-lookup"><span data-stu-id="62421-119">Provides property set definitions.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="62421-120">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="62421-120">Header files</span></span>

<span data-ttu-id="62421-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="62421-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="62421-122">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="62421-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="62421-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="62421-123">Mapitags.h</span></span>
  
> <span data-ttu-id="62421-124">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="62421-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="62421-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="62421-125">See also</span></span>



[<span data-ttu-id="62421-126">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="62421-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="62421-127">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="62421-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="62421-128">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="62421-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="62421-129">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="62421-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
