---
title: PidLidAddressBookProviderEmailList (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 053ec531f69ff7734872466b7a661beff3177b2c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348482"
---
# <a name="pidlidaddressbookprovideremaillist-canonical-property"></a><span data-ttu-id="b044c-103">PidLidAddressBookProviderEmailList (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="b044c-103">PidLidAddressBookProviderEmailList Canonical Property</span></span>

  
  
<span data-ttu-id="b044c-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b044c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b044c-105">Gibt an, welche elektronischen Adresseigenschaften für den Kontakt festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="b044c-105">Specifies which electronic address properties are set on the contact.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b044c-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="b044c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b044c-107">dispidABPEmailList</span><span class="sxs-lookup"><span data-stu-id="b044c-107">dispidABPEmailList</span></span>  <br/> |
|<span data-ttu-id="b044c-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="b044c-108">Property set:</span></span>  <br/> |<span data-ttu-id="b044c-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="b044c-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="b044c-110">Lange ID (LID):</span><span class="sxs-lookup"><span data-stu-id="b044c-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="b044c-111">0x00008028</span><span class="sxs-lookup"><span data-stu-id="b044c-111">0x00008028</span></span>  <br/> |
|<span data-ttu-id="b044c-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="b044c-112">Data type:</span></span>  <br/> |<span data-ttu-id="b044c-113">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="b044c-113">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="b044c-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="b044c-114">Area:</span></span>  <br/> |<span data-ttu-id="b044c-115">Kontakt</span><span class="sxs-lookup"><span data-stu-id="b044c-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b044c-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b044c-116">Remarks</span></span>

<span data-ttu-id="b044c-117">Jeder PT_LONG in dieser Eigenschaft muss in der Eigenschaft eindeutig sein und auf einen der Werte in der folgenden Tabelle festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="b044c-117">Each PT_LONG value in this property must be unique in the property and must be set to one of the values in the following table.</span></span> <span data-ttu-id="b044c-118">Wenn diese Eigenschaft festgelegt ist, muss auch **die dispidABPArrayType** ([PidLidAddressBookProviderArrayType](pidlidaddressbookproviderarraytype-canonical-property.md)) -Eigenschaft festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="b044c-118">If this property is set, the **dispidABPArrayType** ([PidLidAddressBookProviderArrayType](pidlidaddressbookproviderarraytype-canonical-property.md)) property must also be set.</span></span> <span data-ttu-id="b044c-119">Diese beiden Eigenschaften müssen miteinander synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="b044c-119">These two properties must be kept synchronized with each other.</span></span> <span data-ttu-id="b044c-120">Wenn beispielsweise einer der Werte in **dispidABPEmailList** "0x00000000" ist, muss **für dispidABPArrayType** das Bit "0x00000001" festgelegt sein.</span><span class="sxs-lookup"><span data-stu-id="b044c-120">For example, if one of the values in **dispidABPEmailList** is "0x00000000", then **dispidABPArrayType** must have the bit "0x00000001" set.</span></span> 
  
|<span data-ttu-id="b044c-121">**Wert**</span><span class="sxs-lookup"><span data-stu-id="b044c-121">**Value**</span></span>|<span data-ttu-id="b044c-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b044c-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b044c-123">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b044c-123">0x00000000</span></span>  <br/> |<span data-ttu-id="b044c-124">Email1 ist für den Kontakt definiert.</span><span class="sxs-lookup"><span data-stu-id="b044c-124">Email1 is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="b044c-125">0x00000001</span><span class="sxs-lookup"><span data-stu-id="b044c-125">0x00000001</span></span>  <br/> |<span data-ttu-id="b044c-126">Email2 ist für den Kontakt definiert.</span><span class="sxs-lookup"><span data-stu-id="b044c-126">Email2 is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="b044c-127">0x00000002</span><span class="sxs-lookup"><span data-stu-id="b044c-127">0x00000002</span></span>  <br/> |<span data-ttu-id="b044c-128">Email3 ist für den Kontakt definiert.</span><span class="sxs-lookup"><span data-stu-id="b044c-128">Email3 is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="b044c-129">0x00000003</span><span class="sxs-lookup"><span data-stu-id="b044c-129">0x00000003</span></span>  <br/> |<span data-ttu-id="b044c-130">Geschäftsfax ist für den Kontakt definiert.</span><span class="sxs-lookup"><span data-stu-id="b044c-130">Business fax is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="b044c-131">0x00000004</span><span class="sxs-lookup"><span data-stu-id="b044c-131">0x00000004</span></span>  <br/> |<span data-ttu-id="b044c-132">Für den Kontakt wird ein Homefax definiert.</span><span class="sxs-lookup"><span data-stu-id="b044c-132">Home fax is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="b044c-133">0x00000005</span><span class="sxs-lookup"><span data-stu-id="b044c-133">0x00000005</span></span>  <br/> |<span data-ttu-id="b044c-134">Primäres Fax wird für den Kontakt definiert.</span><span class="sxs-lookup"><span data-stu-id="b044c-134">Primary fax is defined for the contact.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="b044c-135">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="b044c-135">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b044c-136">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="b044c-136">Protocol specifications</span></span>

<span data-ttu-id="b044c-137">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b044c-137">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b044c-138">Stellt Eigenschaftensatzdefinitionen und Verweise auf verwandte Exchange Server zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="b044c-138">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b044c-139">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b044c-139">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b044c-140">Gibt die Eigenschaften und Vorgänge an, die für Kontakte und persönliche Verteilerlisten zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="b044c-140">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b044c-141">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="b044c-141">Header files</span></span>

<span data-ttu-id="b044c-142">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b044c-142">Mapidefs.h</span></span>
  
> <span data-ttu-id="b044c-143">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="b044c-143">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b044c-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b044c-144">See also</span></span>



[<span data-ttu-id="b044c-145">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b044c-145">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b044c-146">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="b044c-146">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b044c-147">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="b044c-147">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b044c-148">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="b044c-148">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

