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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 22a1a62f4ee6ff492f36eb18e2d92c8d70febd72
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326124"
---
# <a name="pidtagaddressbookhierarchicalrootdepartment"></a><span data-ttu-id="8e3cc-103">PidTagAddressBookHierarchicalRootDepartment</span><span class="sxs-lookup"><span data-stu-id="8e3cc-103">PidTagAddressBookHierarchicalRootDepartment</span></span>

  
  
<span data-ttu-id="8e3cc-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8e3cc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="8e3cc-105">Enthält den Distinguished Name (DN) des hierarchischen Adress Stamms (HAB).</span><span class="sxs-lookup"><span data-stu-id="8e3cc-105">Contains the distinguished name (DN) of the hierarchical address root (HAB).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8e3cc-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="8e3cc-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8e3cc-107">PR_EMS_AB_HAB_ROOT_DEPARTMENT, PR_EMS_AB_HAB_ROOT_DEPARTMENT_A</span><span class="sxs-lookup"><span data-stu-id="8e3cc-107">PR_EMS_AB_HAB_ROOT_DEPARTMENT, PR_EMS_AB_HAB_ROOT_DEPARTMENT_A</span></span>  <br/> |
|<span data-ttu-id="8e3cc-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="8e3cc-108">Property set:</span></span>  <br/> |<span data-ttu-id="8e3cc-109">Adressbuch</span><span class="sxs-lookup"><span data-stu-id="8e3cc-109">Address Book</span></span>  <br/> |
|<span data-ttu-id="8e3cc-110">Long-ID (Deckel):</span><span class="sxs-lookup"><span data-stu-id="8e3cc-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="8e3cc-111">0x8C98</span><span class="sxs-lookup"><span data-stu-id="8e3cc-111">0x8C98</span></span>  <br/> |
|<span data-ttu-id="8e3cc-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="8e3cc-112">Data type:</span></span>  <br/> |<span data-ttu-id="8e3cc-113">PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="8e3cc-113">PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="8e3cc-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="8e3cc-114">Area:</span></span>  <br/> |<span data-ttu-id="8e3cc-115">Exchange-Adressbuch</span><span class="sxs-lookup"><span data-stu-id="8e3cc-115">Exchange Address Book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8e3cc-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8e3cc-116">Remarks</span></span>

<span data-ttu-id="8e3cc-117">Hierbei handelt es sich um eine Eigenschaft im GAL-Container (Global Address List), die den Distinguished Name des hierarchischen Adress Stamms darstellt.</span><span class="sxs-lookup"><span data-stu-id="8e3cc-117">This is a property on the global address list (GAL) container and represents the distinguished name of the hierarchical address root.</span></span> <span data-ttu-id="8e3cc-118">Diese Eigenschaft ist nur im Offlineadressbuch und nie in Active Directory-Domänendiensten (AD DS) vorhanden.</span><span class="sxs-lookup"><span data-stu-id="8e3cc-118">This property is only present in the offline address book and never in Active Directory Domain Services (AD DS).</span></span> <span data-ttu-id="8e3cc-119">Anrufer sollten MAPI_CACHE_ONLY an den getProps-Aufruf weiterleiten, um einen Remoteprozeduraufruf zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="8e3cc-119">Callers should pass MAPI_CACHE_ONLY to the GetProps call to avoid a remote procedure call.</span></span> <span data-ttu-id="8e3cc-120">Wenn dies nicht der Fall ist, sollten Aufrufer PR_EMS_AB_HAB_ROOT_DEPARTMENT, die vom Typ PT_OBJECT, verwenden, um die Stammabteilung zu finden.</span><span class="sxs-lookup"><span data-stu-id="8e3cc-120">If this is not present, callers should use PR_EMS_AB_HAB_ROOT_DEPARTMENT, which is of type PT_OBJECT, to find the root department.</span></span> 
  
<span data-ttu-id="8e3cc-121">Nachdem die Stammabteilung abgerufen wurde, kann Sie einen Objekttyp MAPI_MAILUSER oder MAPI_DISTLIST aufweisen.</span><span class="sxs-lookup"><span data-stu-id="8e3cc-121">Once the root department is obtained, it can have an object type MAPI_MAILUSER or MAPI_DISTLIST.</span></span> <span data-ttu-id="8e3cc-122">Wenn der Objekttyp MAPI_DISTLIST ist, wird das neue Schema verwendet.</span><span class="sxs-lookup"><span data-stu-id="8e3cc-122">If the object type is MAPI_DISTLIST, the new schema is being employed.</span></span> <span data-ttu-id="8e3cc-123">Wenn der Objekttyp MAPI_MAILUSER ist, wird das vorherige Schema verwendet.</span><span class="sxs-lookup"><span data-stu-id="8e3cc-123">If the object type is MAPI_MAILUSER, the previous schema is being employed.</span></span> 
  
- <span data-ttu-id="8e3cc-124">Microsoft Office Outlook 2007 Service Pack 2 unterstützt beide Schemas.</span><span class="sxs-lookup"><span data-stu-id="8e3cc-124">Microsoft Office Outlook 2007 Service Pack 2 supports both schemas.</span></span> 
    
- <span data-ttu-id="8e3cc-125">Microsoft Outlook 2010 und Microsoft Outlook 2013 unterstützen das neue Schema.</span><span class="sxs-lookup"><span data-stu-id="8e3cc-125">Microsoft Outlook 2010 and Microsoft Outlook 2013 support the new schema.</span></span>
    
<span data-ttu-id="8e3cc-126">Im neuen Schema sind alle Abteilungsgruppen auch Verteilerlisten und sind vom Typ MAPI_DISTLIST.</span><span class="sxs-lookup"><span data-stu-id="8e3cc-126">In the new schema, all departmental groups are also distribution lists and are of type MAPI_DISTLIST.</span></span> <span data-ttu-id="8e3cc-127">Mitglieder von Abteilungsgruppen und Abteilungen innerhalb von Abteilungsgruppen werden mithilfe von PR_EMS_AB_MEMBER abgerufen, genau wie Verteilerlistenmitglieder.</span><span class="sxs-lookup"><span data-stu-id="8e3cc-127">Members of departmental groups, and departments within departmental groups are obtained by using PR_EMS_AB_MEMBER, exactly like distribution list members.</span></span>
  
<span data-ttu-id="8e3cc-128">Nachdem die Stammabteilung abgerufen wurde, kann Sie einen Objekttyp MAPI_MAILUSER oder MAPI_DISTLIST aufweisen.</span><span class="sxs-lookup"><span data-stu-id="8e3cc-128">Once the root department is obtained, it can have an object type MAPI_MAILUSER or MAPI_DISTLIST.</span></span> <span data-ttu-id="8e3cc-129">Wenn der Objekttyp MAPI_DISTLIST ist, wird das neue Schema verwendet.</span><span class="sxs-lookup"><span data-stu-id="8e3cc-129">If the object type is MAPI_DISTLIST, the new schema is being used.</span></span> <span data-ttu-id="8e3cc-130">Wenn der Objekttyp MAPI_MAILUSER ist, wird das alte Schema verwendet.</span><span class="sxs-lookup"><span data-stu-id="8e3cc-130">If the object type is MAPI_MAILUSER, the old schema is being used.</span></span> 
  
<span data-ttu-id="8e3cc-131">Im neuen Schema sind alle Abteilungsgruppen auch Verteilerlisten und sind vom Typ MAPI_DISTLIST.</span><span class="sxs-lookup"><span data-stu-id="8e3cc-131">In the new schema, all departmental groups are also DLs and are of type MAPI_DISTLIST.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="8e3cc-132">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="8e3cc-132">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8e3cc-133">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="8e3cc-133">Protocol specifications</span></span>

<span data-ttu-id="8e3cc-134">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8e3cc-134">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8e3cc-135">Stellt Eigenschaftensatz Definitionen und Verweise auf zugehörige Microsoft Exchange Server-Protokollspezifikationen bereit.</span><span class="sxs-lookup"><span data-stu-id="8e3cc-135">Provides property set definitions and references to related Microsoft Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8e3cc-136">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="8e3cc-136">Header files</span></span>

<span data-ttu-id="8e3cc-137">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="8e3cc-137">Mapidefs.h</span></span>
  
> <span data-ttu-id="8e3cc-138">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="8e3cc-138">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8e3cc-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8e3cc-139">See also</span></span>



[<span data-ttu-id="8e3cc-140">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8e3cc-140">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8e3cc-141">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8e3cc-141">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8e3cc-142">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="8e3cc-142">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8e3cc-143">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="8e3cc-143">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

