---
title: PidLidContactItemData (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidContactItemData
api_type:
- COM
ms.assetid: 411e8f81-c2b9-440a-9e9a-d6add5e4be63
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 031e5483539ce17c8b9b994690985c2349573e27
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400807"
---
# <a name="pidlidcontactitemdata-canonical-property"></a><span data-ttu-id="6ca2f-103">PidLidContactItemData (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="6ca2f-103">PidLidContactItemData Canonical Property</span></span>

  
  
<span data-ttu-id="6ca2f-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6ca2f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6ca2f-105">Verwendet, um die Kontaktinformationen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="6ca2f-105">Used to display the contact information.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6ca2f-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="6ca2f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6ca2f-107">dispidContactItemData</span><span class="sxs-lookup"><span data-stu-id="6ca2f-107">dispidContactItemData</span></span>  <br/> |
|<span data-ttu-id="6ca2f-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="6ca2f-108">Property set:</span></span>  <br/> |<span data-ttu-id="6ca2f-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="6ca2f-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="6ca2f-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="6ca2f-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="6ca2f-111">0x00008007</span><span class="sxs-lookup"><span data-stu-id="6ca2f-111">0x00008007</span></span>  <br/> |
|<span data-ttu-id="6ca2f-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="6ca2f-112">Data type:</span></span>  <br/> |<span data-ttu-id="6ca2f-113">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="6ca2f-113">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="6ca2f-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="6ca2f-114">Area:</span></span>  <br/> |<span data-ttu-id="6ca2f-115">Kontakt</span><span class="sxs-lookup"><span data-stu-id="6ca2f-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6ca2f-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="6ca2f-116">Remarks</span></span>

<span data-ttu-id="6ca2f-117">Wenn dieser Parameter angegeben wurde, muss die Eigenschaft sechs Einträge, die jeweils entsprechen einer eingeblendeten Felder in der Benutzeroberfläche der Anwendung verfügen.</span><span class="sxs-lookup"><span data-stu-id="6ca2f-117">If present, the property must have six entries, each corresponding to a visible field in the application's user interface.</span></span>
  
|<span data-ttu-id="6ca2f-118">**1 beginnenden Index in der mehrwertige Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="6ca2f-118">**One-based index into the multi-valued property**</span></span>|<span data-ttu-id="6ca2f-119">**Der Wert muss eine der folgenden sein:**</span><span class="sxs-lookup"><span data-stu-id="6ca2f-119">**The value must be one of the following**</span></span>|<span data-ttu-id="6ca2f-120">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6ca2f-120">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="6ca2f-121">1</span><span class="sxs-lookup"><span data-stu-id="6ca2f-121">1</span></span>  <br/> |<span data-ttu-id="6ca2f-122">0x00000001</span><span class="sxs-lookup"><span data-stu-id="6ca2f-122">0x00000001</span></span>  <br/> |<span data-ttu-id="6ca2f-123">Die Anwendung sollte home-Adresse des Kontakts angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="6ca2f-123">The application should display the contact's home address.</span></span>  <br/> |
|<span data-ttu-id="6ca2f-124">1</span><span class="sxs-lookup"><span data-stu-id="6ca2f-124">1</span></span>  <br/> |<span data-ttu-id="6ca2f-125">0 x 00000002 oder 0 x 00000000</span><span class="sxs-lookup"><span data-stu-id="6ca2f-125">0x00000002 or 0x00000000</span></span>  <br/> |<span data-ttu-id="6ca2f-126">Die Anwendung sollte Arbeit des Kontakts angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="6ca2f-126">The application should display the contact's work.</span></span>  <br/> |
|<span data-ttu-id="6ca2f-127">1</span><span class="sxs-lookup"><span data-stu-id="6ca2f-127">1</span></span>  <br/> |<span data-ttu-id="6ca2f-128">0 x 00000003</span><span class="sxs-lookup"><span data-stu-id="6ca2f-128">0x00000003</span></span>  <br/> |<span data-ttu-id="6ca2f-129">Die Anwendung sollte angezeigt werden des Kontakts die Adresse.</span><span class="sxs-lookup"><span data-stu-id="6ca2f-129">The application should display the contact's other address.</span></span>  <br/> |
|<span data-ttu-id="6ca2f-130">2</span><span class="sxs-lookup"><span data-stu-id="6ca2f-130">2</span></span>  <br/> |<span data-ttu-id="6ca2f-131">0x00008080</span><span class="sxs-lookup"><span data-stu-id="6ca2f-131">0x00008080</span></span>  <br/> |<span data-ttu-id="6ca2f-132">Die Anwendung sollte Email1 angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="6ca2f-132">The application should display Email1.</span></span>  <br/> |
|<span data-ttu-id="6ca2f-133">2</span><span class="sxs-lookup"><span data-stu-id="6ca2f-133">2</span></span>  <br/> |<span data-ttu-id="6ca2f-134">0x00008090</span><span class="sxs-lookup"><span data-stu-id="6ca2f-134">0x00008090</span></span>  <br/> |<span data-ttu-id="6ca2f-135">Die Anwendung sollte Email2 angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="6ca2f-135">The application should display Email2.</span></span>  <br/> |
|<span data-ttu-id="6ca2f-136">2</span><span class="sxs-lookup"><span data-stu-id="6ca2f-136">2</span></span>  <br/> |<span data-ttu-id="6ca2f-137">0x000080A0</span><span class="sxs-lookup"><span data-stu-id="6ca2f-137">0x000080A0</span></span>  <br/> |<span data-ttu-id="6ca2f-138">Die Anwendung sollte Email3 angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="6ca2f-138">The application should display Email3.</span></span>  <br/> |
|<span data-ttu-id="6ca2f-139">3,4,5,6</span><span class="sxs-lookup"><span data-stu-id="6ca2f-139">3,4,5,6</span></span>  <br/> |<span data-ttu-id="6ca2f-140">PropertyID Telefon Eigenschaften oder eine der Fax-Zahlen, die in [[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="6ca2f-140">PropertyID of any of the telephone properties or any of the fax numbers that are specified in [[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx).</span></span>  <br/> |<span data-ttu-id="6ca2f-141">Die Anwendung sollte die entsprechende Eigenschaft angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="6ca2f-141">The application should display the corresponding property.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="6ca2f-142">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="6ca2f-142">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6ca2f-143">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="6ca2f-143">Protocol specifications</span></span>

<span data-ttu-id="6ca2f-144">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6ca2f-144">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6ca2f-145">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="6ca2f-145">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6ca2f-146">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6ca2f-146">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6ca2f-147">Gibt die Eigenschaften und Operationen, die für Kontakte und persönliche Verteilerlisten zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="6ca2f-147">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6ca2f-148">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="6ca2f-148">Header files</span></span>

<span data-ttu-id="6ca2f-149">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6ca2f-149">Mapidefs.h</span></span>
  
> <span data-ttu-id="6ca2f-150">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="6ca2f-150">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6ca2f-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6ca2f-151">See also</span></span>



[<span data-ttu-id="6ca2f-152">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6ca2f-152">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6ca2f-153">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6ca2f-153">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6ca2f-154">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="6ca2f-154">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6ca2f-155">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="6ca2f-155">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

