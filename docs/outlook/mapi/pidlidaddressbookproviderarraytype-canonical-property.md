---
title: PidLidAddressBookProviderArrayType (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 68396f210aab465da9cec4a74a3c24cc4e8578a5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348440"
---
# <a name="pidlidaddressbookproviderarraytype-canonical-property"></a><span data-ttu-id="d1e49-103">PidLidAddressBookProviderArrayType (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="d1e49-103">PidLidAddressBookProviderArrayType Canonical Property</span></span>

  
  
<span data-ttu-id="d1e49-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d1e49-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d1e49-105">Gibt den Status der elektronischen Adressen des Kontakts an und stellt eine Reihe von Bitflags dar.</span><span class="sxs-lookup"><span data-stu-id="d1e49-105">Specifies the state of the contact's electronic addresses and represents a set of bit flags.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d1e49-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="d1e49-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d1e49-107">dispidABPArrayType</span><span class="sxs-lookup"><span data-stu-id="d1e49-107">dispidABPArrayType</span></span>  <br/> |
|<span data-ttu-id="d1e49-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="d1e49-108">Property set:</span></span>  <br/> |<span data-ttu-id="d1e49-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="d1e49-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="d1e49-110">Lange ID (LID):</span><span class="sxs-lookup"><span data-stu-id="d1e49-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="d1e49-111">0x00008029</span><span class="sxs-lookup"><span data-stu-id="d1e49-111">0x00008029</span></span>  <br/> |
|<span data-ttu-id="d1e49-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="d1e49-112">Data type:</span></span>  <br/> |<span data-ttu-id="d1e49-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="d1e49-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="d1e49-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="d1e49-114">Area:</span></span>  <br/> |<span data-ttu-id="d1e49-115">Kontakt</span><span class="sxs-lookup"><span data-stu-id="d1e49-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d1e49-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d1e49-116">Remarks</span></span>

<span data-ttu-id="d1e49-117">Der Wert der **dispidABPArrayType-Eigenschaft** muss eine Kombination aus Flags sein, die den Status des Contact-Objekts angeben.</span><span class="sxs-lookup"><span data-stu-id="d1e49-117">The value of the **dispidABPArrayType** property must be a combination of flags that specify the state of the contact object.</span></span> <span data-ttu-id="d1e49-118">Einzelne Flags werden in der folgenden Tabelle angegeben.</span><span class="sxs-lookup"><span data-stu-id="d1e49-118">Individual flags are specified in the following table.</span></span> <span data-ttu-id="d1e49-119">Wenn diese Eigenschaft festgelegt ist, muss auch die **dispidABPEmailList** ([PidLidAddressBookProviderEmailList](pidlidaddressbookprovideremaillist-canonical-property.md)) -Eigenschaft festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="d1e49-119">If this property is set, the **dispidABPEmailList** ([PidLidAddressBookProviderEmailList](pidlidaddressbookprovideremaillist-canonical-property.md)) property must be set, as well.</span></span> <span data-ttu-id="d1e49-120">Diese beiden Eigenschaften müssen miteinander synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="d1e49-120">These two properties must be kept synchronized with each other.</span></span> <span data-ttu-id="d1e49-121">Wenn beispielsweise **dispidABPArrayType** das Bit "0x00000001 set" hat, muss einer der Werte von **dispidABPEmailList** "0x00000000" sein.</span><span class="sxs-lookup"><span data-stu-id="d1e49-121">For example, if **dispidABPArrayType** has the bit "0x00000001 set", one of the values of **dispidABPEmailList** must be "0x00000000".</span></span> 
  
|<span data-ttu-id="d1e49-122">**Bit**</span><span class="sxs-lookup"><span data-stu-id="d1e49-122">**Bit**</span></span>|<span data-ttu-id="d1e49-123">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d1e49-123">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d1e49-124">0x00000001</span><span class="sxs-lookup"><span data-stu-id="d1e49-124">0x00000001</span></span>  <br/> |<span data-ttu-id="d1e49-125">Email1 ist für den Kontakt definiert.</span><span class="sxs-lookup"><span data-stu-id="d1e49-125">Email1 is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="d1e49-126">0x00000002</span><span class="sxs-lookup"><span data-stu-id="d1e49-126">0x00000002</span></span>  <br/> |<span data-ttu-id="d1e49-127">Email2 ist für den Kontakt definiert.</span><span class="sxs-lookup"><span data-stu-id="d1e49-127">Email2 is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="d1e49-128">0x00000004</span><span class="sxs-lookup"><span data-stu-id="d1e49-128">0x00000004</span></span>  <br/> |<span data-ttu-id="d1e49-129">Email3 ist für den Kontakt definiert.</span><span class="sxs-lookup"><span data-stu-id="d1e49-129">Email3 is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="d1e49-130">0x00000008</span><span class="sxs-lookup"><span data-stu-id="d1e49-130">0x00000008</span></span>  <br/> |<span data-ttu-id="d1e49-131">Geschäftsfax ist für den Kontakt definiert.</span><span class="sxs-lookup"><span data-stu-id="d1e49-131">Business fax is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="d1e49-132">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d1e49-132">0x00000010</span></span>  <br/> |<span data-ttu-id="d1e49-133">Für den Kontakt wird ein Homefax definiert.</span><span class="sxs-lookup"><span data-stu-id="d1e49-133">Home fax is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="d1e49-134">0x00000020</span><span class="sxs-lookup"><span data-stu-id="d1e49-134">0x00000020</span></span>  <br/> |<span data-ttu-id="d1e49-135">Primäres Fax wird für den Kontakt definiert.</span><span class="sxs-lookup"><span data-stu-id="d1e49-135">Primary fax is defined for the contact.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="d1e49-136">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="d1e49-136">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d1e49-137">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="d1e49-137">Protocol specifications</span></span>

<span data-ttu-id="d1e49-138">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d1e49-138">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d1e49-139">Stellt Eigenschaftensatzdefinitionen und Verweise auf verwandte Exchange Server zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="d1e49-139">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d1e49-140">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d1e49-140">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d1e49-141">Gibt die Eigenschaften und Vorgänge an, die für Kontakte und persönliche Verteilerlisten zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="d1e49-141">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d1e49-142">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="d1e49-142">Header files</span></span>

<span data-ttu-id="d1e49-143">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d1e49-143">Mapidefs.h</span></span>
  
> <span data-ttu-id="d1e49-144">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="d1e49-144">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d1e49-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d1e49-145">See also</span></span>



[<span data-ttu-id="d1e49-146">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d1e49-146">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d1e49-147">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="d1e49-147">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d1e49-148">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="d1e49-148">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d1e49-149">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="d1e49-149">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

