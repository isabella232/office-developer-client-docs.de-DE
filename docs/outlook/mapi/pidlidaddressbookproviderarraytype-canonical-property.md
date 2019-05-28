---
title: Kanonische pidlidaddressbookproviderarraytype (-Eigenschaft
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
# <a name="pidlidaddressbookproviderarraytype-canonical-property"></a><span data-ttu-id="68374-103">Kanonische pidlidaddressbookproviderarraytype (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="68374-103">PidLidAddressBookProviderArrayType Canonical Property</span></span>

  
  
<span data-ttu-id="68374-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="68374-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="68374-105">Gibt den Status der elektronischen Adressen des Kontakts an und stellt eine Gruppe von Bitflags dar.</span><span class="sxs-lookup"><span data-stu-id="68374-105">Specifies the state of the contact's electronic addresses and represents a set of bit flags.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="68374-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="68374-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="68374-107">dispidABPArrayType</span><span class="sxs-lookup"><span data-stu-id="68374-107">dispidABPArrayType</span></span>  <br/> |
|<span data-ttu-id="68374-108">Eigenschaftengruppe:</span><span class="sxs-lookup"><span data-stu-id="68374-108">Property set:</span></span>  <br/> |<span data-ttu-id="68374-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="68374-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="68374-110">Lange ID (LID):</span><span class="sxs-lookup"><span data-stu-id="68374-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="68374-111">0x00008029</span><span class="sxs-lookup"><span data-stu-id="68374-111">0x00008029</span></span>  <br/> |
|<span data-ttu-id="68374-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="68374-112">Data type:</span></span>  <br/> |<span data-ttu-id="68374-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="68374-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="68374-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="68374-114">Area:</span></span>  <br/> |<span data-ttu-id="68374-115">Kontakt</span><span class="sxs-lookup"><span data-stu-id="68374-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="68374-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="68374-116">Remarks</span></span>

<span data-ttu-id="68374-117">Der Wert der **dispidABPArrayType** -Eigenschaft muss eine Kombination von Flags sein, die den Status des Contact-Objekts angeben.</span><span class="sxs-lookup"><span data-stu-id="68374-117">The value of the **dispidABPArrayType** property must be a combination of flags that specify the state of the contact object.</span></span> <span data-ttu-id="68374-118">In der folgenden Tabelle werden einzelne Flags angegeben.</span><span class="sxs-lookup"><span data-stu-id="68374-118">Individual flags are specified in the following table.</span></span> <span data-ttu-id="68374-119">Wenn diese Eigenschaft festgelegt ist, muss auch die **dispidABPEmailList** ([pidlidaddressbookprovideremaillist (](pidlidaddressbookprovideremaillist-canonical-property.md))-Eigenschaft festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="68374-119">If this property is set, the **dispidABPEmailList** ([PidLidAddressBookProviderEmailList](pidlidaddressbookprovideremaillist-canonical-property.md)) property must be set, as well.</span></span> <span data-ttu-id="68374-120">Diese beiden Eigenschaften müssen miteinander synchronisiert bleiben.</span><span class="sxs-lookup"><span data-stu-id="68374-120">These two properties must be kept synchronized with each other.</span></span> <span data-ttu-id="68374-121">Wenn **dispidABPArrayType** beispielsweise das Bit "0x00000001 festgelegt" hat, muss einer der Werte von **dispidABPEmailList** "0x00000000" lauten.</span><span class="sxs-lookup"><span data-stu-id="68374-121">For example, if **dispidABPArrayType** has the bit "0x00000001 set", one of the values of **dispidABPEmailList** must be "0x00000000".</span></span> 
  
|<span data-ttu-id="68374-122">**Bit**</span><span class="sxs-lookup"><span data-stu-id="68374-122">**Bit**</span></span>|<span data-ttu-id="68374-123">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="68374-123">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="68374-124">0x00000001</span><span class="sxs-lookup"><span data-stu-id="68374-124">0x00000001</span></span>  <br/> |<span data-ttu-id="68374-125">Mail1 ist für den Kontakt definiert.</span><span class="sxs-lookup"><span data-stu-id="68374-125">Email1 is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="68374-126">0x00000002</span><span class="sxs-lookup"><span data-stu-id="68374-126">0x00000002</span></span>  <br/> |<span data-ttu-id="68374-127">Mail2 ist für den Kontakt definiert.</span><span class="sxs-lookup"><span data-stu-id="68374-127">Email2 is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="68374-128">0x00000004</span><span class="sxs-lookup"><span data-stu-id="68374-128">0x00000004</span></span>  <br/> |<span data-ttu-id="68374-129">Email3 ist für den Kontakt definiert.</span><span class="sxs-lookup"><span data-stu-id="68374-129">Email3 is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="68374-130">0x00000008</span><span class="sxs-lookup"><span data-stu-id="68374-130">0x00000008</span></span>  <br/> |<span data-ttu-id="68374-131">Business Fax ist für den Kontakt definiert.</span><span class="sxs-lookup"><span data-stu-id="68374-131">Business fax is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="68374-132">0x00000010</span><span class="sxs-lookup"><span data-stu-id="68374-132">0x00000010</span></span>  <br/> |<span data-ttu-id="68374-133">Home Fax ist für den Kontakt definiert.</span><span class="sxs-lookup"><span data-stu-id="68374-133">Home fax is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="68374-134">0x00000020</span><span class="sxs-lookup"><span data-stu-id="68374-134">0x00000020</span></span>  <br/> |<span data-ttu-id="68374-135">Primäres Fax ist für den Kontakt definiert.</span><span class="sxs-lookup"><span data-stu-id="68374-135">Primary fax is defined for the contact.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="68374-136">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="68374-136">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="68374-137">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="68374-137">Protocol specifications</span></span>

<span data-ttu-id="68374-138">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="68374-138">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="68374-139">Stellt Eigenschaftenmengen Definitionen und Verweise auf zugehörige Exchange Server Protokollspezifikationen bereit.</span><span class="sxs-lookup"><span data-stu-id="68374-139">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="68374-140">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="68374-140">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="68374-141">Gibt die Eigenschaften und Vorgänge an, die für Kontakte und persönliche Verteilerlisten zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="68374-141">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="68374-142">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="68374-142">Header files</span></span>

<span data-ttu-id="68374-143">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="68374-143">Mapidefs.h</span></span>
  
> <span data-ttu-id="68374-144">Stellt Definitionen von Datentypen bereit.</span><span class="sxs-lookup"><span data-stu-id="68374-144">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="68374-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="68374-145">See also</span></span>



[<span data-ttu-id="68374-146">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="68374-146">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="68374-147">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="68374-147">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="68374-148">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="68374-148">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="68374-149">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="68374-149">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

