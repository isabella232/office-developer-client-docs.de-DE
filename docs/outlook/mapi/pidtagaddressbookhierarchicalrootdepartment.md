---
title: PidTagAddressBookHierarchicalRootDepartment
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAddressBookHierarchicalRootDepartment
api_type:
- HeaderDef
ms.assetid: c611640b-1a70-4a76-b7ff-c8ad8d320892
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 22a1a62f4ee6ff492f36eb18e2d92c8d70febd72
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326124"
---
# <a name="pidtagaddressbookhierarchicalrootdepartment"></a><span data-ttu-id="15632-103">PidTagAddressBookHierarchicalRootDepartment</span><span class="sxs-lookup"><span data-stu-id="15632-103">PidTagAddressBookHierarchicalRootDepartment</span></span>

  
  
<span data-ttu-id="15632-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="15632-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="15632-105">Enthält den Distinguished Name (DN) des hierarchischen Adressstamms (HAB).</span><span class="sxs-lookup"><span data-stu-id="15632-105">Contains the distinguished name (DN) of the hierarchical address root (HAB).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="15632-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="15632-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="15632-107">PR_EMS_AB_HAB_ROOT_DEPARTMENT, PR_EMS_AB_HAB_ROOT_DEPARTMENT_A</span><span class="sxs-lookup"><span data-stu-id="15632-107">PR_EMS_AB_HAB_ROOT_DEPARTMENT, PR_EMS_AB_HAB_ROOT_DEPARTMENT_A</span></span>  <br/> |
|<span data-ttu-id="15632-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="15632-108">Property set:</span></span>  <br/> |<span data-ttu-id="15632-109">Adressbuch</span><span class="sxs-lookup"><span data-stu-id="15632-109">Address Book</span></span>  <br/> |
|<span data-ttu-id="15632-110">Lange ID (LID):</span><span class="sxs-lookup"><span data-stu-id="15632-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="15632-111">0x8C98</span><span class="sxs-lookup"><span data-stu-id="15632-111">0x8C98</span></span>  <br/> |
|<span data-ttu-id="15632-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="15632-112">Data type:</span></span>  <br/> |<span data-ttu-id="15632-113">PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="15632-113">PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="15632-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="15632-114">Area:</span></span>  <br/> |<span data-ttu-id="15632-115">Exchange-Adressbuch</span><span class="sxs-lookup"><span data-stu-id="15632-115">Exchange Address Book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="15632-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="15632-116">Remarks</span></span>

<span data-ttu-id="15632-117">Dies ist eine Eigenschaft im Globalen Adresslistencontainer (GAL) und stellt den Distinguished Name des hierarchischen Adressstamms dar.</span><span class="sxs-lookup"><span data-stu-id="15632-117">This is a property on the global address list (GAL) container and represents the distinguished name of the hierarchical address root.</span></span> <span data-ttu-id="15632-118">Diese Eigenschaft ist nur im Offlineadressbuch und niemals in Active Directory Domain Services (AD DS) vorhanden.</span><span class="sxs-lookup"><span data-stu-id="15632-118">This property is only present in the offline address book and never in Active Directory Domain Services (AD DS).</span></span> <span data-ttu-id="15632-119">Anrufer sollten MAPI_CACHE_ONLY an den GetProps-Aufruf übergeben, um einen Remoteprozeduraufruf zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="15632-119">Callers should pass MAPI_CACHE_ONLY to the GetProps call to avoid a remote procedure call.</span></span> <span data-ttu-id="15632-120">Wenn dies nicht der Fall ist, sollten Anrufer die PR_EMS_AB_HAB_ROOT_DEPARTMENT, die vom Typ PT_OBJECT ist, verwenden, um die Stammabteilung zu finden.</span><span class="sxs-lookup"><span data-stu-id="15632-120">If this is not present, callers should use PR_EMS_AB_HAB_ROOT_DEPARTMENT, which is of type PT_OBJECT, to find the root department.</span></span> 
  
<span data-ttu-id="15632-121">Sobald die Stammabteilung erhalten wurde, kann sie einen Objekttyp MAPI_MAILUSER oder MAPI_DISTLIST.</span><span class="sxs-lookup"><span data-stu-id="15632-121">Once the root department is obtained, it can have an object type MAPI_MAILUSER or MAPI_DISTLIST.</span></span> <span data-ttu-id="15632-122">Wenn der Objekttyp MAPI_DISTLIST wird das neue Schema verwendet.</span><span class="sxs-lookup"><span data-stu-id="15632-122">If the object type is MAPI_DISTLIST, the new schema is being employed.</span></span> <span data-ttu-id="15632-123">Wenn der Objekttyp MAPI_MAILUSER, wird das vorherige Schema verwendet.</span><span class="sxs-lookup"><span data-stu-id="15632-123">If the object type is MAPI_MAILUSER, the previous schema is being employed.</span></span> 
  
- <span data-ttu-id="15632-124">Microsoft Office Outlook 2007 Service Pack 2 unterstützt beide Schemas.</span><span class="sxs-lookup"><span data-stu-id="15632-124">Microsoft Office Outlook 2007 Service Pack 2 supports both schemas.</span></span> 
    
- <span data-ttu-id="15632-125">Microsoft Outlook 2010 und Microsoft Outlook 2013 unterstützen das neue Schema.</span><span class="sxs-lookup"><span data-stu-id="15632-125">Microsoft Outlook 2010 and Microsoft Outlook 2013 support the new schema.</span></span>
    
<span data-ttu-id="15632-126">Im neuen Schema sind alle Abteilungsgruppen auch Verteilerlisten und vom Typ MAPI_DISTLIST.</span><span class="sxs-lookup"><span data-stu-id="15632-126">In the new schema, all departmental groups are also distribution lists and are of type MAPI_DISTLIST.</span></span> <span data-ttu-id="15632-127">Mitglieder von Abteilungsgruppen und Abteilungen innerhalb von Abteilungsgruppen werden mithilfe von PR_EMS_AB_MEMBER, genau wie Verteilerlistenmitglieder.</span><span class="sxs-lookup"><span data-stu-id="15632-127">Members of departmental groups, and departments within departmental groups are obtained by using PR_EMS_AB_MEMBER, exactly like distribution list members.</span></span>
  
<span data-ttu-id="15632-128">Sobald die Stammabteilung erhalten wurde, kann sie einen Objekttyp MAPI_MAILUSER oder MAPI_DISTLIST.</span><span class="sxs-lookup"><span data-stu-id="15632-128">Once the root department is obtained, it can have an object type MAPI_MAILUSER or MAPI_DISTLIST.</span></span> <span data-ttu-id="15632-129">Wenn der Objekttyp MAPI_DISTLIST wird das neue Schema verwendet.</span><span class="sxs-lookup"><span data-stu-id="15632-129">If the object type is MAPI_DISTLIST, the new schema is being used.</span></span> <span data-ttu-id="15632-130">Wenn der Objekttyp MAPI_MAILUSER wird das alte Schema verwendet.</span><span class="sxs-lookup"><span data-stu-id="15632-130">If the object type is MAPI_MAILUSER, the old schema is being used.</span></span> 
  
<span data-ttu-id="15632-131">Im neuen Schema sind alle Abteilungsgruppen auch DLs und vom Typ MAPI_DISTLIST.</span><span class="sxs-lookup"><span data-stu-id="15632-131">In the new schema, all departmental groups are also DLs and are of type MAPI_DISTLIST.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="15632-132">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="15632-132">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="15632-133">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="15632-133">Protocol specifications</span></span>

<span data-ttu-id="15632-134">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="15632-134">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="15632-135">Stellt Eigenschaftensatzdefinitionen und Verweise auf verwandte Microsoft Exchange Server zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="15632-135">Provides property set definitions and references to related Microsoft Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="15632-136">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="15632-136">Header files</span></span>

<span data-ttu-id="15632-137">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="15632-137">Mapidefs.h</span></span>
  
> <span data-ttu-id="15632-138">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="15632-138">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="15632-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="15632-139">See also</span></span>



[<span data-ttu-id="15632-140">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="15632-140">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="15632-141">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="15632-141">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="15632-142">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="15632-142">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="15632-143">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="15632-143">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

