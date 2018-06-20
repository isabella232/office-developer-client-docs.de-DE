---
title: Kanonische PidLidAddressBookProviderArrayType-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAddressBookProviderArrayType
api_type:
- COM
ms.assetid: ca4eb6c2-98e9-4dbc-9f5a-f0f257456ead
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 3515d0f751cb6d8d0d427079691456519bac97dc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793332"
---
# <a name="pidlidaddressbookproviderarraytype-canonical-property"></a><span data-ttu-id="5f3bf-103">Kanonische PidLidAddressBookProviderArrayType-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="5f3bf-103">PidLidAddressBookProviderArrayType Canonical Property</span></span>

  
  
<span data-ttu-id="5f3bf-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5f3bf-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5f3bf-105">Gibt den Status des Kontakts elektronische Adressen und stellt einen Satz von Bit-Flags dar.</span><span class="sxs-lookup"><span data-stu-id="5f3bf-105">Specifies the state of the contact's electronic addresses and represents a set of bit flags.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5f3bf-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="5f3bf-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5f3bf-107">dispidABPArrayType</span><span class="sxs-lookup"><span data-stu-id="5f3bf-107">dispidABPArrayType</span></span>  <br/> |
|<span data-ttu-id="5f3bf-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="5f3bf-108">Property set:</span></span>  <br/> |<span data-ttu-id="5f3bf-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="5f3bf-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="5f3bf-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="5f3bf-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="5f3bf-111">0x00008029</span><span class="sxs-lookup"><span data-stu-id="5f3bf-111">0x00008029</span></span>  <br/> |
|<span data-ttu-id="5f3bf-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="5f3bf-112">Data type:</span></span>  <br/> |<span data-ttu-id="5f3bf-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="5f3bf-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="5f3bf-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="5f3bf-114">Area:</span></span>  <br/> |<span data-ttu-id="5f3bf-115">Kontakt</span><span class="sxs-lookup"><span data-stu-id="5f3bf-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5f3bf-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5f3bf-116">Remarks</span></span>

<span data-ttu-id="5f3bf-117">Der Wert der **DispidABPArrayType** -Eigenschaft muss eine Kombination von Flags, die den Zustand des Kontaktobjekts angeben.</span><span class="sxs-lookup"><span data-stu-id="5f3bf-117">The value of the **dispidABPArrayType** property must be a combination of flags that specify the state of the contact object.</span></span> <span data-ttu-id="5f3bf-118">Einzelne Flags werden in der folgenden Tabelle angegeben.</span><span class="sxs-lookup"><span data-stu-id="5f3bf-118">Individual flags are specified in the following table.</span></span> <span data-ttu-id="5f3bf-119">Wenn diese Eigenschaft festgelegt ist, muss die Eigenschaft **DispidABPEmailList** ([PidLidAddressBookProviderEmailList](pidlidaddressbookprovideremaillist-canonical-property.md)), auch festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="5f3bf-119">If this property is set, the **dispidABPEmailList** ([PidLidAddressBookProviderEmailList](pidlidaddressbookprovideremaillist-canonical-property.md)) property must be set, as well.</span></span> <span data-ttu-id="5f3bf-120">Diese beiden Eigenschaften müssen miteinander synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="5f3bf-120">These two properties must be kept synchronized with each other.</span></span> <span data-ttu-id="5f3bf-121">Wenn **DispidABPArrayType** das Bit "0 x 00000001 Set" aufweist, muss einer der Werte der **DispidABPEmailList** "0 x 00000000" sein.</span><span class="sxs-lookup"><span data-stu-id="5f3bf-121">For example, if **dispidABPArrayType** has the bit "0x00000001 set", one of the values of **dispidABPEmailList** must be "0x00000000".</span></span> 
  
|<span data-ttu-id="5f3bf-122">**Bit**</span><span class="sxs-lookup"><span data-stu-id="5f3bf-122">**Bit**</span></span>|<span data-ttu-id="5f3bf-123">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5f3bf-123">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5f3bf-124">0x00000001</span><span class="sxs-lookup"><span data-stu-id="5f3bf-124">0x00000001</span></span>  <br/> |<span data-ttu-id="5f3bf-125">Email1 ist für den Kontakt definiert.</span><span class="sxs-lookup"><span data-stu-id="5f3bf-125">Email1 is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="5f3bf-126">0x00000002</span><span class="sxs-lookup"><span data-stu-id="5f3bf-126">0x00000002</span></span>  <br/> |<span data-ttu-id="5f3bf-127">Email2 ist für den Kontakt definiert.</span><span class="sxs-lookup"><span data-stu-id="5f3bf-127">Email2 is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="5f3bf-128">0 x 00000004</span><span class="sxs-lookup"><span data-stu-id="5f3bf-128">0x00000004</span></span>  <br/> |<span data-ttu-id="5f3bf-129">Email3 ist für den Kontakt definiert.</span><span class="sxs-lookup"><span data-stu-id="5f3bf-129">Email3 is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="5f3bf-130">0 x 00000008</span><span class="sxs-lookup"><span data-stu-id="5f3bf-130">0x00000008</span></span>  <br/> |<span data-ttu-id="5f3bf-131">Fax (geschäftlich) ist für den Kontakt definiert.</span><span class="sxs-lookup"><span data-stu-id="5f3bf-131">Business fax is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="5f3bf-132">0 x 00000010</span><span class="sxs-lookup"><span data-stu-id="5f3bf-132">0x00000010</span></span>  <br/> |<span data-ttu-id="5f3bf-133">Fax privat ist für den Kontakt definiert.</span><span class="sxs-lookup"><span data-stu-id="5f3bf-133">Home fax is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="5f3bf-134">0 x 00000020</span><span class="sxs-lookup"><span data-stu-id="5f3bf-134">0x00000020</span></span>  <br/> |<span data-ttu-id="5f3bf-135">Primäre Faxnummer ist für den Kontakt definiert.</span><span class="sxs-lookup"><span data-stu-id="5f3bf-135">Primary fax is defined for the contact.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="5f3bf-136">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="5f3bf-136">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5f3bf-137">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="5f3bf-137">Protocol specifications</span></span>

<span data-ttu-id="5f3bf-138">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5f3bf-138">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5f3bf-139">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="5f3bf-139">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5f3bf-140">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5f3bf-140">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5f3bf-141">Gibt die Eigenschaften und Operationen, die für Kontakte und persönliche Verteilerlisten zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="5f3bf-141">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5f3bf-142">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="5f3bf-142">Header files</span></span>

<span data-ttu-id="5f3bf-143">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5f3bf-143">Mapidefs.h</span></span>
  
> <span data-ttu-id="5f3bf-144">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="5f3bf-144">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5f3bf-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5f3bf-145">See also</span></span>



[<span data-ttu-id="5f3bf-146">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5f3bf-146">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5f3bf-147">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5f3bf-147">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5f3bf-148">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="5f3bf-148">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5f3bf-149">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="5f3bf-149">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

