---
title: PidTagEmsAbServer (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 0d31272e63df7f68a83b23ca7a3824c081de3c1d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569267"
---
# <a name="pidtagemsabserver-canonical-property"></a><span data-ttu-id="d0cac-103">PidTagEmsAbServer (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="d0cac-103">PidTagEmsAbServer Canonical Property</span></span>

  
  
<span data-ttu-id="d0cac-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d0cac-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d0cac-105">Gibt entweder den Pfad einer Adressbuchcontainer in einem Szenario offline oder den vollqualifizierten Domänennamen des globalen Katalogservers Adressbuchcontainer sich in einem Szenario online befindet.</span><span class="sxs-lookup"><span data-stu-id="d0cac-105">Specifies either the path of an address book container in an offline scenario or the fully qualified domain name of the global catalog server where the address book container resides in an online scenario.</span></span>
  
## 

|||
|:-----|:-----|
|<span data-ttu-id="d0cac-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="d0cac-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d0cac-107">PR_EMS_AB_SERVER, PR_EMS_AB_SERVER_A, PR_EMS_AB_SERVER_W</span><span class="sxs-lookup"><span data-stu-id="d0cac-107">PR_EMS_AB_SERVER, PR_EMS_AB_SERVER_A, PR_EMS_AB_SERVER_W</span></span>  <br/> |
|<span data-ttu-id="d0cac-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="d0cac-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d0cac-109">0xFFFE</span><span class="sxs-lookup"><span data-stu-id="d0cac-109">0xFFFE</span></span>  <br/> |
|<span data-ttu-id="d0cac-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="d0cac-110">Data type:</span></span>  <br/> |<span data-ttu-id="d0cac-111">PT_TSTRING</span><span class="sxs-lookup"><span data-stu-id="d0cac-111">PT_TSTRING</span></span>  <br/> |
|<span data-ttu-id="d0cac-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="d0cac-112">Area:</span></span>  <br/> |<span data-ttu-id="d0cac-113">Adressbuch</span><span class="sxs-lookup"><span data-stu-id="d0cac-113">Address Book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d0cac-114">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="d0cac-114">Remarks</span></span>

<span data-ttu-id="d0cac-115">Diese Eigenschaft hat den Eigenschaftentyp auf **PT_UNICODE** zurückzusetzen, wenn die Kompilierung der `UNICODE` Symbol auf einer Unicode-Plattform und **PT_STRING8** bei der Kompilierung nicht mit der `UNICODE` Symbol.</span><span class="sxs-lookup"><span data-stu-id="d0cac-115">This property has the property type reset to **PT_UNICODE** when it is compiled with the  `UNICODE` symbol on a Unicode platform, and to **PT_STRING8** when it is not compiled with the  `UNICODE` symbol.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="d0cac-116">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="d0cac-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d0cac-117">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="d0cac-117">Protocol specifications</span></span>

<span data-ttu-id="d0cac-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d0cac-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d0cac-119">Enthält Eigenschaftendefinitionen an.</span><span class="sxs-lookup"><span data-stu-id="d0cac-119">Provides property set definitions.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d0cac-120">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="d0cac-120">Header files</span></span>

<span data-ttu-id="d0cac-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d0cac-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="d0cac-122">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="d0cac-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="d0cac-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="d0cac-123">Mapitags.h</span></span>
  
> <span data-ttu-id="d0cac-124">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="d0cac-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d0cac-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d0cac-125">See also</span></span>



[<span data-ttu-id="d0cac-126">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d0cac-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d0cac-127">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d0cac-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d0cac-128">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="d0cac-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d0cac-129">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="d0cac-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

