---
title: Kanonische Pidlidaddressbookprovideremaillist (-Eigenschaft
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
ms.openlocfilehash: 053ec531f69ff7734872466b7a661beff3177b2c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348482"
---
# <a name="pidlidaddressbookprovideremaillist-canonical-property"></a><span data-ttu-id="7d718-103">Kanonische Pidlidaddressbookprovideremaillist (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="7d718-103">PidLidAddressBookProviderEmailList Canonical Property</span></span>

  
  
<span data-ttu-id="7d718-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7d718-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7d718-105">Gibt an, welche Eigenschaften für elektronische Adressen für den Kontakt festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="7d718-105">Specifies which electronic address properties are set on the contact.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7d718-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="7d718-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7d718-107">dispidABPEmailList</span><span class="sxs-lookup"><span data-stu-id="7d718-107">dispidABPEmailList</span></span>  <br/> |
|<span data-ttu-id="7d718-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="7d718-108">Property set:</span></span>  <br/> |<span data-ttu-id="7d718-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="7d718-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="7d718-110">Long-ID (Deckel):</span><span class="sxs-lookup"><span data-stu-id="7d718-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="7d718-111">0x00008028</span><span class="sxs-lookup"><span data-stu-id="7d718-111">0x00008028</span></span>  <br/> |
|<span data-ttu-id="7d718-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="7d718-112">Data type:</span></span>  <br/> |<span data-ttu-id="7d718-113">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="7d718-113">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="7d718-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="7d718-114">Area:</span></span>  <br/> |<span data-ttu-id="7d718-115">Kontakt</span><span class="sxs-lookup"><span data-stu-id="7d718-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7d718-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7d718-116">Remarks</span></span>

<span data-ttu-id="7d718-117">Jeder PT_LONG-Wert in dieser Eigenschaft muss in der-Eigenschaft eindeutig sein und auf einen der Werte in der folgenden Tabelle festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="7d718-117">Each PT_LONG value in this property must be unique in the property and must be set to one of the values in the following table.</span></span> <span data-ttu-id="7d718-118">Wenn diese Eigenschaft festgelegt ist, muss auch die **dispidABPArrayType** ([pidlidaddressbookproviderarraytype (](pidlidaddressbookproviderarraytype-canonical-property.md))-Eigenschaft festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="7d718-118">If this property is set, the **dispidABPArrayType** ([PidLidAddressBookProviderArrayType](pidlidaddressbookproviderarraytype-canonical-property.md)) property must also be set.</span></span> <span data-ttu-id="7d718-119">Diese beiden Eigenschaften müssen synchron gehalten werden.</span><span class="sxs-lookup"><span data-stu-id="7d718-119">These two properties must be kept synchronized with each other.</span></span> <span data-ttu-id="7d718-120">Wenn beispielsweise einer der Werte in **dispidABPEmailList** "0x00000000" lautet, muss für **dispidABPArrayType** das Bit "0x00000001" festgelegt sein.</span><span class="sxs-lookup"><span data-stu-id="7d718-120">For example, if one of the values in **dispidABPEmailList** is "0x00000000", then **dispidABPArrayType** must have the bit "0x00000001" set.</span></span> 
  
|<span data-ttu-id="7d718-121">**Wert**</span><span class="sxs-lookup"><span data-stu-id="7d718-121">**Value**</span></span>|<span data-ttu-id="7d718-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7d718-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7d718-123">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7d718-123">0x00000000</span></span>  <br/> |<span data-ttu-id="7d718-124">Mail1 ist für den Kontakt definiert.</span><span class="sxs-lookup"><span data-stu-id="7d718-124">Email1 is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="7d718-125">0x00000001</span><span class="sxs-lookup"><span data-stu-id="7d718-125">0x00000001</span></span>  <br/> |<span data-ttu-id="7d718-126">Mail2 ist für den Kontakt definiert.</span><span class="sxs-lookup"><span data-stu-id="7d718-126">Email2 is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="7d718-127">0x00000002</span><span class="sxs-lookup"><span data-stu-id="7d718-127">0x00000002</span></span>  <br/> |<span data-ttu-id="7d718-128">Email3 ist für den Kontakt definiert.</span><span class="sxs-lookup"><span data-stu-id="7d718-128">Email3 is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="7d718-129">0x00000003</span><span class="sxs-lookup"><span data-stu-id="7d718-129">0x00000003</span></span>  <br/> |<span data-ttu-id="7d718-130">Business Fax ist für den Kontakt definiert.</span><span class="sxs-lookup"><span data-stu-id="7d718-130">Business fax is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="7d718-131">0x00000004</span><span class="sxs-lookup"><span data-stu-id="7d718-131">0x00000004</span></span>  <br/> |<span data-ttu-id="7d718-132">Privat Fax ist für den Kontakt definiert.</span><span class="sxs-lookup"><span data-stu-id="7d718-132">Home fax is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="7d718-133">0x00000005</span><span class="sxs-lookup"><span data-stu-id="7d718-133">0x00000005</span></span>  <br/> |<span data-ttu-id="7d718-134">Das primäre Fax ist für den Kontakt definiert.</span><span class="sxs-lookup"><span data-stu-id="7d718-134">Primary fax is defined for the contact.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="7d718-135">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="7d718-135">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7d718-136">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="7d718-136">Protocol specifications</span></span>

<span data-ttu-id="7d718-137">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7d718-137">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7d718-138">Stellt Eigenschaftensatz Definitionen und Verweise auf zugehörige Exchange Server-Protokollspezifikationen bereit.</span><span class="sxs-lookup"><span data-stu-id="7d718-138">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7d718-139">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7d718-139">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7d718-140">Gibt die Eigenschaften und Vorgänge an, die für Kontakte und persönliche Verteilerlisten zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="7d718-140">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7d718-141">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="7d718-141">Header files</span></span>

<span data-ttu-id="7d718-142">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="7d718-142">Mapidefs.h</span></span>
  
> <span data-ttu-id="7d718-143">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="7d718-143">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7d718-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7d718-144">See also</span></span>



[<span data-ttu-id="7d718-145">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7d718-145">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7d718-146">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7d718-146">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7d718-147">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="7d718-147">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7d718-148">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="7d718-148">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

