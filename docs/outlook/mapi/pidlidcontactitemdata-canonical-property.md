---
title: Kanonische Pidlidcontactitemdata (-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 031e5483539ce17c8b9b994690985c2349573e27
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319510"
---
# <a name="pidlidcontactitemdata-canonical-property"></a><span data-ttu-id="44bd7-103">Kanonische Pidlidcontactitemdata (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="44bd7-103">PidLidContactItemData Canonical Property</span></span>

  
  
<span data-ttu-id="44bd7-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="44bd7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="44bd7-105">Wird verwendet, um die Kontaktinformationen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="44bd7-105">Used to display the contact information.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="44bd7-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="44bd7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="44bd7-107">dispidContactItemData</span><span class="sxs-lookup"><span data-stu-id="44bd7-107">dispidContactItemData</span></span>  <br/> |
|<span data-ttu-id="44bd7-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="44bd7-108">Property set:</span></span>  <br/> |<span data-ttu-id="44bd7-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="44bd7-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="44bd7-110">Long-ID (Deckel):</span><span class="sxs-lookup"><span data-stu-id="44bd7-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="44bd7-111">0x00008007</span><span class="sxs-lookup"><span data-stu-id="44bd7-111">0x00008007</span></span>  <br/> |
|<span data-ttu-id="44bd7-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="44bd7-112">Data type:</span></span>  <br/> |<span data-ttu-id="44bd7-113">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="44bd7-113">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="44bd7-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="44bd7-114">Area:</span></span>  <br/> |<span data-ttu-id="44bd7-115">Kontakt</span><span class="sxs-lookup"><span data-stu-id="44bd7-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="44bd7-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="44bd7-116">Remarks</span></span>

<span data-ttu-id="44bd7-117">Sofern vorhanden, muss die Eigenschaft sechs Einträge aufweisen, die jeweils einem sichtbaren Feld auf der Benutzeroberfläche der Anwendung entsprechen.</span><span class="sxs-lookup"><span data-stu-id="44bd7-117">If present, the property must have six entries, each corresponding to a visible field in the application's user interface.</span></span>
  
|<span data-ttu-id="44bd7-118">**1-basierter Index in der mehrwertigen Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="44bd7-118">**One-based index into the multi-valued property**</span></span>|<span data-ttu-id="44bd7-119">**Der Wert muss einer der folgenden Werte sein:**</span><span class="sxs-lookup"><span data-stu-id="44bd7-119">**The value must be one of the following**</span></span>|<span data-ttu-id="44bd7-120">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="44bd7-120">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="44bd7-121">1</span><span class="sxs-lookup"><span data-stu-id="44bd7-121">1</span></span>  <br/> |<span data-ttu-id="44bd7-122">0x00000001</span><span class="sxs-lookup"><span data-stu-id="44bd7-122">0x00000001</span></span>  <br/> |<span data-ttu-id="44bd7-123">Die Anwendung sollte die Privatadresse des Kontakts anzeigen.</span><span class="sxs-lookup"><span data-stu-id="44bd7-123">The application should display the contact's home address.</span></span>  <br/> |
|<span data-ttu-id="44bd7-124">1</span><span class="sxs-lookup"><span data-stu-id="44bd7-124">1</span></span>  <br/> |<span data-ttu-id="44bd7-125">0x00000002 oder 0x00000000</span><span class="sxs-lookup"><span data-stu-id="44bd7-125">0x00000002 or 0x00000000</span></span>  <br/> |<span data-ttu-id="44bd7-126">Die Anwendung sollte die Arbeit des Kontakts anzeigen.</span><span class="sxs-lookup"><span data-stu-id="44bd7-126">The application should display the contact's work.</span></span>  <br/> |
|<span data-ttu-id="44bd7-127">1</span><span class="sxs-lookup"><span data-stu-id="44bd7-127">1</span></span>  <br/> |<span data-ttu-id="44bd7-128">0x00000003</span><span class="sxs-lookup"><span data-stu-id="44bd7-128">0x00000003</span></span>  <br/> |<span data-ttu-id="44bd7-129">Die Anwendung sollte die andere Adresse des Kontakts anzeigen.</span><span class="sxs-lookup"><span data-stu-id="44bd7-129">The application should display the contact's other address.</span></span>  <br/> |
|<span data-ttu-id="44bd7-130">2</span><span class="sxs-lookup"><span data-stu-id="44bd7-130">2</span></span>  <br/> |<span data-ttu-id="44bd7-131">0x00008080</span><span class="sxs-lookup"><span data-stu-id="44bd7-131">0x00008080</span></span>  <br/> |<span data-ttu-id="44bd7-132">Die Anwendung sollte mail1 anzeigen.</span><span class="sxs-lookup"><span data-stu-id="44bd7-132">The application should display Email1.</span></span>  <br/> |
|<span data-ttu-id="44bd7-133">2</span><span class="sxs-lookup"><span data-stu-id="44bd7-133">2</span></span>  <br/> |<span data-ttu-id="44bd7-134">0x00008090</span><span class="sxs-lookup"><span data-stu-id="44bd7-134">0x00008090</span></span>  <br/> |<span data-ttu-id="44bd7-135">Die Anwendung sollte mail2 anzeigen.</span><span class="sxs-lookup"><span data-stu-id="44bd7-135">The application should display Email2.</span></span>  <br/> |
|<span data-ttu-id="44bd7-136">2</span><span class="sxs-lookup"><span data-stu-id="44bd7-136">2</span></span>  <br/> |<span data-ttu-id="44bd7-137">0x000080A0</span><span class="sxs-lookup"><span data-stu-id="44bd7-137">0x000080A0</span></span>  <br/> |<span data-ttu-id="44bd7-138">Die Anwendung sollte Email3 anzeigen.</span><span class="sxs-lookup"><span data-stu-id="44bd7-138">The application should display Email3.</span></span>  <br/> |
|<span data-ttu-id="44bd7-139">3, 4, 5, 6</span><span class="sxs-lookup"><span data-stu-id="44bd7-139">3,4,5,6</span></span>  <br/> |<span data-ttu-id="44bd7-140">Die Eigenschafts-IDs der Telefoneigenschaften oder der Faxnummern, die in [[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="44bd7-140">PropertyID of any of the telephone properties or any of the fax numbers that are specified in [[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx).</span></span>  <br/> |<span data-ttu-id="44bd7-141">Die Anwendung sollte die entsprechende Eigenschaft anzeigen.</span><span class="sxs-lookup"><span data-stu-id="44bd7-141">The application should display the corresponding property.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="44bd7-142">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="44bd7-142">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="44bd7-143">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="44bd7-143">Protocol specifications</span></span>

<span data-ttu-id="44bd7-144">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="44bd7-144">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="44bd7-145">Stellt Eigenschaftensatz Definitionen und Verweise auf zugehörige Exchange Server-Protokollspezifikationen bereit.</span><span class="sxs-lookup"><span data-stu-id="44bd7-145">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="44bd7-146">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="44bd7-146">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="44bd7-147">Gibt die Eigenschaften und Vorgänge an, die für Kontakte und persönliche Verteilerlisten zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="44bd7-147">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="44bd7-148">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="44bd7-148">Header files</span></span>

<span data-ttu-id="44bd7-149">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="44bd7-149">Mapidefs.h</span></span>
  
> <span data-ttu-id="44bd7-150">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="44bd7-150">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="44bd7-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="44bd7-151">See also</span></span>



[<span data-ttu-id="44bd7-152">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="44bd7-152">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="44bd7-153">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="44bd7-153">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="44bd7-154">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="44bd7-154">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="44bd7-155">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="44bd7-155">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

