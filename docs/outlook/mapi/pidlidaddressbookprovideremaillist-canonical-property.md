---
title: Kanonische PidLidAddressBookProviderEmailList-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAddressBookProviderEmailList
api_type:
- COM
ms.assetid: 9c0527ea-e922-4514-b913-d3520350c452
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 4eb2897c1834715f3d937ef7946998943b386aef
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793357"
---
# <a name="pidlidaddressbookprovideremaillist-canonical-property"></a><span data-ttu-id="7881e-103">Kanonische PidLidAddressBookProviderEmailList-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="7881e-103">PidLidAddressBookProviderEmailList Canonical Property</span></span>

  
  
<span data-ttu-id="7881e-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7881e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7881e-105">Gibt an, welche Eigenschaften für e-Mail-Adresse auf den Kontakt festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="7881e-105">Specifies which electronic address properties are set on the contact.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7881e-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="7881e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7881e-107">dispidABPEmailList</span><span class="sxs-lookup"><span data-stu-id="7881e-107">dispidABPEmailList</span></span>  <br/> |
|<span data-ttu-id="7881e-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="7881e-108">Property set:</span></span>  <br/> |<span data-ttu-id="7881e-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="7881e-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="7881e-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="7881e-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="7881e-111">0x00008028</span><span class="sxs-lookup"><span data-stu-id="7881e-111">0x00008028</span></span>  <br/> |
|<span data-ttu-id="7881e-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="7881e-112">Data type:</span></span>  <br/> |<span data-ttu-id="7881e-113">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="7881e-113">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="7881e-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="7881e-114">Area:</span></span>  <br/> |<span data-ttu-id="7881e-115">Kontakt</span><span class="sxs-lookup"><span data-stu-id="7881e-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7881e-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="7881e-116">Remarks</span></span>

<span data-ttu-id="7881e-117">Jeder PT_LONG Wert in dieser Eigenschaft muss in der Eigenschaft eindeutig sein und muss auf einen der Werte in der folgenden Tabelle festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="7881e-117">Each PT_LONG value in this property must be unique in the property and must be set to one of the values in the following table.</span></span> <span data-ttu-id="7881e-118">Wenn diese Eigenschaft festgelegt ist, muss auch die **DispidABPArrayType** ([PidLidAddressBookProviderArrayType](pidlidaddressbookproviderarraytype-canonical-property.md))-Eigenschaft festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="7881e-118">If this property is set, the **dispidABPArrayType** ([PidLidAddressBookProviderArrayType](pidlidaddressbookproviderarraytype-canonical-property.md)) property must also be set.</span></span> <span data-ttu-id="7881e-119">Diese beiden Eigenschaften müssen miteinander synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="7881e-119">These two properties must be kept synchronized with each other.</span></span> <span data-ttu-id="7881e-120">Angenommen, wenn einer der Werte in **DispidABPEmailList** "0 x 00000000" **DispidABPArrayType** ist, muss das Bit "0 x 00000001" festgelegt haben.</span><span class="sxs-lookup"><span data-stu-id="7881e-120">For example, if one of the values in **dispidABPEmailList** is "0x00000000", then **dispidABPArrayType** must have the bit "0x00000001" set.</span></span> 
  
|<span data-ttu-id="7881e-121">**Wert**</span><span class="sxs-lookup"><span data-stu-id="7881e-121">**Value**</span></span>|<span data-ttu-id="7881e-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7881e-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7881e-123">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7881e-123">0x00000000</span></span>  <br/> |<span data-ttu-id="7881e-124">Email1 ist für den Kontakt definiert.</span><span class="sxs-lookup"><span data-stu-id="7881e-124">Email1 is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="7881e-125">0x00000001</span><span class="sxs-lookup"><span data-stu-id="7881e-125">0x00000001</span></span>  <br/> |<span data-ttu-id="7881e-126">Email2 ist für den Kontakt definiert.</span><span class="sxs-lookup"><span data-stu-id="7881e-126">Email2 is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="7881e-127">0x00000002</span><span class="sxs-lookup"><span data-stu-id="7881e-127">0x00000002</span></span>  <br/> |<span data-ttu-id="7881e-128">Email3 ist für den Kontakt definiert.</span><span class="sxs-lookup"><span data-stu-id="7881e-128">Email3 is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="7881e-129">0 x 00000003</span><span class="sxs-lookup"><span data-stu-id="7881e-129">0x00000003</span></span>  <br/> |<span data-ttu-id="7881e-130">Fax (geschäftlich) ist für den Kontakt definiert.</span><span class="sxs-lookup"><span data-stu-id="7881e-130">Business fax is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="7881e-131">0 x 00000004</span><span class="sxs-lookup"><span data-stu-id="7881e-131">0x00000004</span></span>  <br/> |<span data-ttu-id="7881e-132">Fax privat ist für den Kontakt definiert.</span><span class="sxs-lookup"><span data-stu-id="7881e-132">Home fax is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="7881e-133">0 x 00000005</span><span class="sxs-lookup"><span data-stu-id="7881e-133">0x00000005</span></span>  <br/> |<span data-ttu-id="7881e-134">Primäre Faxnummer ist für den Kontakt definiert.</span><span class="sxs-lookup"><span data-stu-id="7881e-134">Primary fax is defined for the contact.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="7881e-135">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="7881e-135">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7881e-136">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="7881e-136">Protocol specifications</span></span>

<span data-ttu-id="7881e-137">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7881e-137">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7881e-138">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="7881e-138">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7881e-139">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7881e-139">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7881e-140">Gibt die Eigenschaften und Operationen, die für Kontakte und persönliche Verteilerlisten zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="7881e-140">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7881e-141">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="7881e-141">Header files</span></span>

<span data-ttu-id="7881e-142">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7881e-142">Mapidefs.h</span></span>
  
> <span data-ttu-id="7881e-143">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="7881e-143">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7881e-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7881e-144">See also</span></span>



[<span data-ttu-id="7881e-145">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7881e-145">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7881e-146">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7881e-146">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7881e-147">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="7881e-147">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7881e-148">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="7881e-148">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

