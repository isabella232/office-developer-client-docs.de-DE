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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382610"
---
# <a name="pidtagaddressbookhierarchicalrootdepartment"></a><span data-ttu-id="18ba5-103">PidTagAddressBookHierarchicalRootDepartment</span><span class="sxs-lookup"><span data-stu-id="18ba5-103">PidTagAddressBookHierarchicalRootDepartment</span></span>

  
  
<span data-ttu-id="18ba5-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="18ba5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="18ba5-105">Enthält den distinguished Name (DN) des Stammverzeichnisses hierarchische Adresse (eines hierarchischen Adressbuchs).</span><span class="sxs-lookup"><span data-stu-id="18ba5-105">Contains the distinguished name (DN) of the hierarchical address root (HAB).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="18ba5-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="18ba5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="18ba5-107">PR_EMS_AB_HAB_ROOT_DEPARTMENT PR_EMS_AB_HAB_ROOT_DEPARTMENT_A</span><span class="sxs-lookup"><span data-stu-id="18ba5-107">PR_EMS_AB_HAB_ROOT_DEPARTMENT, PR_EMS_AB_HAB_ROOT_DEPARTMENT_A</span></span>  <br/> |
|<span data-ttu-id="18ba5-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="18ba5-108">Property set:</span></span>  <br/> |<span data-ttu-id="18ba5-109">Adressbuch</span><span class="sxs-lookup"><span data-stu-id="18ba5-109">Address Book</span></span>  <br/> |
|<span data-ttu-id="18ba5-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="18ba5-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="18ba5-111">0x8C98</span><span class="sxs-lookup"><span data-stu-id="18ba5-111">0x8C98</span></span>  <br/> |
|<span data-ttu-id="18ba5-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="18ba5-112">Data type:</span></span>  <br/> |<span data-ttu-id="18ba5-113">PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="18ba5-113">PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="18ba5-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="18ba5-114">Area:</span></span>  <br/> |<span data-ttu-id="18ba5-115">Exchange-Adressbuch</span><span class="sxs-lookup"><span data-stu-id="18ba5-115">Exchange Address Book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="18ba5-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="18ba5-116">Remarks</span></span>

<span data-ttu-id="18ba5-117">Dies ist eine Eigenschaft für den Container der globalen Adressliste (GAL) Liste und den distinguished Name des Stammverzeichnisses hierarchische Adresse darstellt.</span><span class="sxs-lookup"><span data-stu-id="18ba5-117">This is a property on the global address list (GAL) container and represents the distinguished name of the hierarchical address root.</span></span> <span data-ttu-id="18ba5-118">Diese Eigenschaft ist nur in das Offlineadressbuch und nie in Active Directory-Domänendienste (AD DS) vorhanden.</span><span class="sxs-lookup"><span data-stu-id="18ba5-118">This property is only present in the offline address book and never in Active Directory Domain Services (AD DS).</span></span> <span data-ttu-id="18ba5-119">Anrufer sollten den GetProps Anruf an ein remote Procedure Call vermeiden MAPI_CACHE_ONLY übergeben.</span><span class="sxs-lookup"><span data-stu-id="18ba5-119">Callers should pass MAPI_CACHE_ONLY to the GetProps call to avoid a remote procedure call.</span></span> <span data-ttu-id="18ba5-120">Wenn dies nicht vorhanden ist, sollte Anrufer PR_EMS_AB_HAB_ROOT_DEPARTMENT, die vom Typ PT_OBJECT ist, verwenden, um die Stamm-Abteilung suchen.</span><span class="sxs-lookup"><span data-stu-id="18ba5-120">If this is not present, callers should use PR_EMS_AB_HAB_ROOT_DEPARTMENT, which is of type PT_OBJECT, to find the root department.</span></span> 
  
<span data-ttu-id="18ba5-121">Nachdem Sie die Stamm-Abteilung erhalten haben, können sie einen Objekttyp MAPI_MAILUSER oder MAPI_DISTLIST haben.</span><span class="sxs-lookup"><span data-stu-id="18ba5-121">Once the root department is obtained, it can have an object type MAPI_MAILUSER or MAPI_DISTLIST.</span></span> <span data-ttu-id="18ba5-122">Wenn der Objekttyp MAPI_DISTLIST ist, wird das neue Schema eingesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="18ba5-122">If the object type is MAPI_DISTLIST, the new schema is being employed.</span></span> <span data-ttu-id="18ba5-123">Wenn der Objekttyp MAPI_MAILUSER ist, wird das vorherige Schema eingesetzt.</span><span class="sxs-lookup"><span data-stu-id="18ba5-123">If the object type is MAPI_MAILUSER, the previous schema is being employed.</span></span> 
  
- <span data-ttu-id="18ba5-124">Microsoft Office Outlook 2007 Service Pack 2 unterstützt sowohl Schemas.</span><span class="sxs-lookup"><span data-stu-id="18ba5-124">Microsoft Office Outlook 2007 Service Pack 2 supports both schemas.</span></span> 
    
- <span data-ttu-id="18ba5-125">Microsoft Outlook 2010 und Microsoft Outlook 2013 unterstützen das neue Schema.</span><span class="sxs-lookup"><span data-stu-id="18ba5-125">Microsoft Outlook 2010 and Microsoft Outlook 2013 support the new schema.</span></span>
    
<span data-ttu-id="18ba5-126">In der neuen Schema alle Gruppen auf Abteilungsebene sind auch Verteilerlisten und vom Typ MAPI_DISTLIST.</span><span class="sxs-lookup"><span data-stu-id="18ba5-126">In the new schema, all departmental groups are also distribution lists and are of type MAPI_DISTLIST.</span></span> <span data-ttu-id="18ba5-127">Mitglieder von Gruppen auf Abteilungsebene und Abteilungen in Gruppen auf Abteilungsebene werden mit PR_EMS_AB_MEMBER, genau wie Mitglieder der Verteilerliste abgerufen.</span><span class="sxs-lookup"><span data-stu-id="18ba5-127">Members of departmental groups, and departments within departmental groups are obtained by using PR_EMS_AB_MEMBER, exactly like distribution list members.</span></span>
  
<span data-ttu-id="18ba5-128">Nachdem Sie die Stamm-Abteilung erhalten haben, können sie einen Objekttyp MAPI_MAILUSER oder MAPI_DISTLIST haben.</span><span class="sxs-lookup"><span data-stu-id="18ba5-128">Once the root department is obtained, it can have an object type MAPI_MAILUSER or MAPI_DISTLIST.</span></span> <span data-ttu-id="18ba5-129">Wenn der Objekttyp MAPI_DISTLIST ist, wird das neue Schema verwendet.</span><span class="sxs-lookup"><span data-stu-id="18ba5-129">If the object type is MAPI_DISTLIST, the new schema is being used.</span></span> <span data-ttu-id="18ba5-130">Wenn der Objekttyp MAPI_MAILUSER ist, wird das alte Schema verwendet.</span><span class="sxs-lookup"><span data-stu-id="18ba5-130">If the object type is MAPI_MAILUSER, the old schema is being used.</span></span> 
  
<span data-ttu-id="18ba5-131">In der neuen Schema alle Gruppen auf Abteilungsebene sind auch Verteilerlisten und vom Typ MAPI_DISTLIST.</span><span class="sxs-lookup"><span data-stu-id="18ba5-131">In the new schema, all departmental groups are also DLs and are of type MAPI_DISTLIST.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="18ba5-132">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="18ba5-132">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="18ba5-133">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="18ba5-133">Protocol specifications</span></span>

<span data-ttu-id="18ba5-134">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="18ba5-134">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="18ba5-135">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Spezifikationen von Microsoft Exchange Server-Protokoll.</span><span class="sxs-lookup"><span data-stu-id="18ba5-135">Provides property set definitions and references to related Microsoft Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="18ba5-136">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="18ba5-136">Header files</span></span>

<span data-ttu-id="18ba5-137">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="18ba5-137">Mapidefs.h</span></span>
  
> <span data-ttu-id="18ba5-138">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="18ba5-138">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="18ba5-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="18ba5-139">See also</span></span>



[<span data-ttu-id="18ba5-140">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="18ba5-140">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="18ba5-141">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="18ba5-141">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="18ba5-142">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="18ba5-142">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="18ba5-143">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="18ba5-143">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

