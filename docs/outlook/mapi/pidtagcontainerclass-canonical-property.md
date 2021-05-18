---
title: PidTagContainerClass (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContainerClass
api_type:
- HeaderDef
ms.assetid: db249e9e-f1f0-4b95-8cd9-daa7c53ddb32
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: c5b80831607f473208ce987a720c7e80e44b6d80
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283149"
---
# <a name="pidtagcontainerclass-canonical-property"></a><span data-ttu-id="f8721-103">PidTagContainerClass (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="f8721-103">PidTagContainerClass Canonical Property</span></span>

  
  
<span data-ttu-id="f8721-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f8721-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f8721-105">Enthält eine Textzeichenfolge, die den Typ eines Ordners beschreibt.</span><span class="sxs-lookup"><span data-stu-id="f8721-105">Contains a text string describing the type of a folder.</span></span> <span data-ttu-id="f8721-106">Obwohl diese Eigenschaft im Allgemeinen ignoriert wird, erwarten Versionen von Microsoft® Exchange Server vor Exchange Server 2003 Mailbox Manager, dass diese Eigenschaft vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="f8721-106">Although this property is generally ignored, versions of Microsoft® Exchange Server prior to Exchange Server 2003 Mailbox Manager expect this property to be present.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f8721-107">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="f8721-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="f8721-108">PR_CONTAINER_CLASS, PR_CONTAINER_CLASS_A, PR_CONTAINER_CLASS_W</span><span class="sxs-lookup"><span data-stu-id="f8721-108">PR_CONTAINER_CLASS, PR_CONTAINER_CLASS_A, PR_CONTAINER_CLASS_W</span></span>  <br/> |
|<span data-ttu-id="f8721-109">Kennung:</span><span class="sxs-lookup"><span data-stu-id="f8721-109">Identifier:</span></span>  <br/> |<span data-ttu-id="f8721-110">0x3613</span><span class="sxs-lookup"><span data-stu-id="f8721-110">0x3613</span></span>  <br/> |
|<span data-ttu-id="f8721-111">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="f8721-111">Data type:</span></span>  <br/> |<span data-ttu-id="f8721-112">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="f8721-112">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="f8721-113">Bereich:</span><span class="sxs-lookup"><span data-stu-id="f8721-113">Area:</span></span>  <br/> |<span data-ttu-id="f8721-114">Container</span><span class="sxs-lookup"><span data-stu-id="f8721-114">Container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f8721-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f8721-115">Remarks</span></span>

<span data-ttu-id="f8721-116">Diese Eigenschaften werden normalerweise nicht von Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="f8721-116">These properties are not normally used by Exchange Server.</span></span> <span data-ttu-id="f8721-117">Sie Microsoft Office Outlook® jedoch an Postfachordner anfügen.</span><span class="sxs-lookup"><span data-stu-id="f8721-117">However, Microsoft Office Outlook® attaches them to mailbox folders.</span></span> <span data-ttu-id="f8721-118">Darüber hinaus behandeln Versionen von Exchange Server vor Exchange Server 2003 Mailbox Manager ordner, die nicht über diese Eigenschaften verfügen, möglicherweise falsch.</span><span class="sxs-lookup"><span data-stu-id="f8721-118">In addition, versions of Exchange Server prior to Exchange Server 2003 Mailbox Manager might incorrectly handle folders that do not have these properties.</span></span>
  
<span data-ttu-id="f8721-119">Diesen Eigenschaften können die Zeichenfolgenwerte in der folgenden Tabelle zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="f8721-119">These properties can be assigned the string values in the following table.</span></span>
  
|<span data-ttu-id="f8721-120">**Wert**</span><span class="sxs-lookup"><span data-stu-id="f8721-120">**Value**</span></span>|<span data-ttu-id="f8721-121">**Inhalt des Ordners**</span><span class="sxs-lookup"><span data-stu-id="f8721-121">**Contents of Folder**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f8721-122">IPF.Appointment</span><span class="sxs-lookup"><span data-stu-id="f8721-122">IPF.Appointment</span></span>  <br/> |<span data-ttu-id="f8721-123">Termine</span><span class="sxs-lookup"><span data-stu-id="f8721-123">Appointments</span></span>  <br/> |
|<span data-ttu-id="f8721-124">IPF.Contact</span><span class="sxs-lookup"><span data-stu-id="f8721-124">IPF.Contact</span></span>  <br/> |<span data-ttu-id="f8721-125">Kontakte</span><span class="sxs-lookup"><span data-stu-id="f8721-125">Contacts</span></span>  <br/> |
|<span data-ttu-id="f8721-126">IPF. Journal</span><span class="sxs-lookup"><span data-stu-id="f8721-126">IPF.Journal</span></span>  <br/> |<span data-ttu-id="f8721-127">Outlook Journaleinträge</span><span class="sxs-lookup"><span data-stu-id="f8721-127">Outlook Journal entries</span></span>  <br/> |
|<span data-ttu-id="f8721-128">IPF.Note</span><span class="sxs-lookup"><span data-stu-id="f8721-128">IPF.Note</span></span>  <br/> |<span data-ttu-id="f8721-129">E-Mail-Nachrichten und Notizen</span><span class="sxs-lookup"><span data-stu-id="f8721-129">Mail Messages and notes</span></span>  <br/> |
|<span data-ttu-id="f8721-130">IPF. StickyNote</span><span class="sxs-lookup"><span data-stu-id="f8721-130">IPF.StickyNote</span></span>  <br/> |<span data-ttu-id="f8721-131">Outlook Kurznotizen</span><span class="sxs-lookup"><span data-stu-id="f8721-131">Outlook Sticky Notes</span></span>  <br/> |
|<span data-ttu-id="f8721-132">IPF.Task</span><span class="sxs-lookup"><span data-stu-id="f8721-132">IPF.Task</span></span>  <br/> |<span data-ttu-id="f8721-133">Outlook-Aufgaben</span><span class="sxs-lookup"><span data-stu-id="f8721-133">Outlook Tasks</span></span>  <br/> |
   
<span data-ttu-id="f8721-134">Für Ordner, die E-Mail-Nachrichten enthalten, sollten diese Eigenschaften auf IPF festgelegt werden. Hinweis.</span><span class="sxs-lookup"><span data-stu-id="f8721-134">For folders that contain mail messages, these properties should be set to IPF.Note.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f8721-135">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="f8721-135">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f8721-136">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="f8721-136">Protocol specifications</span></span>

<span data-ttu-id="f8721-137">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f8721-137">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f8721-138">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="f8721-138">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f8721-139">[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f8721-139">[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f8721-140">Gibt die Eigenschaften und Vorgänge zum Erstellen und Suchen der speziellen Ordner in einem Postfach an.</span><span class="sxs-lookup"><span data-stu-id="f8721-140">Specifies the properties and operations for creating and locating the special folders in a mailbox.</span></span>
    
<span data-ttu-id="f8721-141">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f8721-141">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f8721-142">Gibt die Eigenschaften und Vorgänge für Termin-, Besprechungs- und Antwortnachrichten an.</span><span class="sxs-lookup"><span data-stu-id="f8721-142">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="f8721-143">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f8721-143">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f8721-144">Gibt die Eigenschaften und Vorgänge an, die für Kontakt- und persönliche Verteilerlistenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="f8721-144">Specifies the properties and operations that are permissible for contact and personal distribution list objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f8721-145">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="f8721-145">Header files</span></span>

<span data-ttu-id="f8721-146">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f8721-146">Mapidefs.h</span></span>
  
> <span data-ttu-id="f8721-147">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="f8721-147">Provides data type definitions.</span></span>
    
<span data-ttu-id="f8721-148">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f8721-148">Mapitags.h</span></span>
  
> <span data-ttu-id="f8721-149">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="f8721-149">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f8721-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f8721-150">See also</span></span>



[<span data-ttu-id="f8721-151">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f8721-151">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f8721-152">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="f8721-152">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f8721-153">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="f8721-153">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f8721-154">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="f8721-154">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

