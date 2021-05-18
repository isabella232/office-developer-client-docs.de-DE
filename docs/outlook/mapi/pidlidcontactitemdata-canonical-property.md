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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319510"
---
# <a name="pidlidcontactitemdata-canonical-property"></a><span data-ttu-id="ef3cf-103">PidLidContactItemData (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="ef3cf-103">PidLidContactItemData Canonical Property</span></span>

  
  
<span data-ttu-id="ef3cf-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ef3cf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ef3cf-105">Wird zum Anzeigen der Kontaktinformationen verwendet.</span><span class="sxs-lookup"><span data-stu-id="ef3cf-105">Used to display the contact information.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ef3cf-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="ef3cf-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ef3cf-107">dispidContactItemData</span><span class="sxs-lookup"><span data-stu-id="ef3cf-107">dispidContactItemData</span></span>  <br/> |
|<span data-ttu-id="ef3cf-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="ef3cf-108">Property set:</span></span>  <br/> |<span data-ttu-id="ef3cf-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="ef3cf-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="ef3cf-110">Lange ID (LID):</span><span class="sxs-lookup"><span data-stu-id="ef3cf-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="ef3cf-111">0x00008007</span><span class="sxs-lookup"><span data-stu-id="ef3cf-111">0x00008007</span></span>  <br/> |
|<span data-ttu-id="ef3cf-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="ef3cf-112">Data type:</span></span>  <br/> |<span data-ttu-id="ef3cf-113">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="ef3cf-113">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="ef3cf-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="ef3cf-114">Area:</span></span>  <br/> |<span data-ttu-id="ef3cf-115">Kontakt</span><span class="sxs-lookup"><span data-stu-id="ef3cf-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ef3cf-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ef3cf-116">Remarks</span></span>

<span data-ttu-id="ef3cf-117">Wenn vorhanden, muss die Eigenschaft sechs Einträge enthalten, die jeweils einem sichtbaren Feld auf der Benutzeroberfläche der Anwendung entspricht.</span><span class="sxs-lookup"><span data-stu-id="ef3cf-117">If present, the property must have six entries, each corresponding to a visible field in the application's user interface.</span></span>
  
|<span data-ttu-id="ef3cf-118">**Ein basierter Index in die mehrwertige Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="ef3cf-118">**One-based index into the multi-valued property**</span></span>|<span data-ttu-id="ef3cf-119">**Der Wert muss einer der folgenden Werte sein:**</span><span class="sxs-lookup"><span data-stu-id="ef3cf-119">**The value must be one of the following**</span></span>|<span data-ttu-id="ef3cf-120">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ef3cf-120">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ef3cf-121">1</span><span class="sxs-lookup"><span data-stu-id="ef3cf-121">1</span></span>  <br/> |<span data-ttu-id="ef3cf-122">0x00000001</span><span class="sxs-lookup"><span data-stu-id="ef3cf-122">0x00000001</span></span>  <br/> |<span data-ttu-id="ef3cf-123">Die Anwendung sollte die Privatadresse des Kontakts anzeigen.</span><span class="sxs-lookup"><span data-stu-id="ef3cf-123">The application should display the contact's home address.</span></span>  <br/> |
|<span data-ttu-id="ef3cf-124">1</span><span class="sxs-lookup"><span data-stu-id="ef3cf-124">1</span></span>  <br/> |<span data-ttu-id="ef3cf-125">0x00000002 oder 0x00000000</span><span class="sxs-lookup"><span data-stu-id="ef3cf-125">0x00000002 or 0x00000000</span></span>  <br/> |<span data-ttu-id="ef3cf-126">Die Anwendung sollte die Arbeit des Kontakts anzeigen.</span><span class="sxs-lookup"><span data-stu-id="ef3cf-126">The application should display the contact's work.</span></span>  <br/> |
|<span data-ttu-id="ef3cf-127">1</span><span class="sxs-lookup"><span data-stu-id="ef3cf-127">1</span></span>  <br/> |<span data-ttu-id="ef3cf-128">0x00000003</span><span class="sxs-lookup"><span data-stu-id="ef3cf-128">0x00000003</span></span>  <br/> |<span data-ttu-id="ef3cf-129">Die Anwendung sollte die andere Adresse des Kontakts anzeigen.</span><span class="sxs-lookup"><span data-stu-id="ef3cf-129">The application should display the contact's other address.</span></span>  <br/> |
|<span data-ttu-id="ef3cf-130">2</span><span class="sxs-lookup"><span data-stu-id="ef3cf-130">2</span></span>  <br/> |<span data-ttu-id="ef3cf-131">0x00008080</span><span class="sxs-lookup"><span data-stu-id="ef3cf-131">0x00008080</span></span>  <br/> |<span data-ttu-id="ef3cf-132">Die Anwendung sollte Email1 anzeigen.</span><span class="sxs-lookup"><span data-stu-id="ef3cf-132">The application should display Email1.</span></span>  <br/> |
|<span data-ttu-id="ef3cf-133">2</span><span class="sxs-lookup"><span data-stu-id="ef3cf-133">2</span></span>  <br/> |<span data-ttu-id="ef3cf-134">0x00008090</span><span class="sxs-lookup"><span data-stu-id="ef3cf-134">0x00008090</span></span>  <br/> |<span data-ttu-id="ef3cf-135">Die Anwendung sollte Email2 anzeigen.</span><span class="sxs-lookup"><span data-stu-id="ef3cf-135">The application should display Email2.</span></span>  <br/> |
|<span data-ttu-id="ef3cf-136">2</span><span class="sxs-lookup"><span data-stu-id="ef3cf-136">2</span></span>  <br/> |<span data-ttu-id="ef3cf-137">0x000080A0</span><span class="sxs-lookup"><span data-stu-id="ef3cf-137">0x000080A0</span></span>  <br/> |<span data-ttu-id="ef3cf-138">Die Anwendung sollte Email3 anzeigen.</span><span class="sxs-lookup"><span data-stu-id="ef3cf-138">The application should display Email3.</span></span>  <br/> |
|<span data-ttu-id="ef3cf-139">3,4,5,6</span><span class="sxs-lookup"><span data-stu-id="ef3cf-139">3,4,5,6</span></span>  <br/> |<span data-ttu-id="ef3cf-140">PropertyID aller Telefoneigenschaften oder faxnummern, die in [[MS-OXOCNTC] angegeben sind.](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ef3cf-140">PropertyID of any of the telephone properties or any of the fax numbers that are specified in [[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx).</span></span>  <br/> |<span data-ttu-id="ef3cf-141">Die Anwendung sollte die entsprechende Eigenschaft anzeigen.</span><span class="sxs-lookup"><span data-stu-id="ef3cf-141">The application should display the corresponding property.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="ef3cf-142">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="ef3cf-142">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ef3cf-143">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="ef3cf-143">Protocol specifications</span></span>

<span data-ttu-id="ef3cf-144">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ef3cf-144">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ef3cf-145">Stellt Eigenschaftensatzdefinitionen und Verweise auf verwandte Exchange Server zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="ef3cf-145">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ef3cf-146">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ef3cf-146">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ef3cf-147">Gibt die Eigenschaften und Vorgänge an, die für Kontakte und persönliche Verteilerlisten zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="ef3cf-147">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ef3cf-148">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="ef3cf-148">Header files</span></span>

<span data-ttu-id="ef3cf-149">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ef3cf-149">Mapidefs.h</span></span>
  
> <span data-ttu-id="ef3cf-150">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="ef3cf-150">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ef3cf-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ef3cf-151">See also</span></span>



[<span data-ttu-id="ef3cf-152">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ef3cf-152">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ef3cf-153">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="ef3cf-153">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ef3cf-154">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="ef3cf-154">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ef3cf-155">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="ef3cf-155">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

