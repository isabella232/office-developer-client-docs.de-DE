---
title: Kanonische Pidtagextendedfolderflags (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagExtendedFolderFlags
api_type:
- HeaderDef
ms.assetid: e0c04f98-3d66-4ab5-ba05-69f9df539fcf
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: fe14f6ca101e6a546f99989ecc87b0c516ee5df4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316352"
---
# <a name="pidtagextendedfolderflags-canonical-property"></a><span data-ttu-id="0eeef-103">Kanonische Pidtagextendedfolderflags (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="0eeef-103">PidTagExtendedFolderFlags Canonical Property</span></span>
 
<span data-ttu-id="0eeef-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0eeef-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0eeef-105">Enthält erweiterte Kennzeichnungen zu einem Ordner.</span><span class="sxs-lookup"><span data-stu-id="0eeef-105">Contains extended flags about a folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0eeef-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="0eeef-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0eeef-107">PR_EXTENDED_FOLDER_FLAGS</span><span class="sxs-lookup"><span data-stu-id="0eeef-107">PR_EXTENDED_FOLDER_FLAGS</span></span>  <br/> |
|<span data-ttu-id="0eeef-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="0eeef-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0eeef-109">0x36DA</span><span class="sxs-lookup"><span data-stu-id="0eeef-109">0x36DA</span></span>  <br/> |
|<span data-ttu-id="0eeef-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="0eeef-110">Data type:</span></span>  <br/> |<span data-ttu-id="0eeef-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="0eeef-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="0eeef-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="0eeef-112">Area:</span></span>  <br/> |<span data-ttu-id="0eeef-113">MAPI-Container</span><span class="sxs-lookup"><span data-stu-id="0eeef-113">MAPI container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0eeef-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0eeef-114">Remarks</span></span>

<span data-ttu-id="0eeef-115">Diese Eigenschaft ist ein binärer Datenstrom, der codierte unter Eigenschaften für den Ordner enthält.</span><span class="sxs-lookup"><span data-stu-id="0eeef-115">This property is a binary stream that contains encoded sub-properties for the folder.</span></span> <span data-ttu-id="0eeef-116">Es ist als eine Reihe von Unterelementen mit variabler Länge formatiert.</span><span class="sxs-lookup"><span data-stu-id="0eeef-116">It is formatted as a series of variable length sub items.</span></span> <span data-ttu-id="0eeef-117">Die ersten 8 Bits des Unterelements sind ein ID-Feld, das angibt, welche Art von Flag das Unterelement darstellt.</span><span class="sxs-lookup"><span data-stu-id="0eeef-117">The first 8 bits of the sub item is an ID field, which indicates what kind of flag the sub item represents.</span></span> <span data-ttu-id="0eeef-118">Die zweite 8 Bits ist die Anzahl der Datenbytes, die Folgen.</span><span class="sxs-lookup"><span data-stu-id="0eeef-118">The second 8 bits is the number of bytes of data that follow.</span></span>
  
<span data-ttu-id="0eeef-119">Mögliche ID-Werte sind:</span><span class="sxs-lookup"><span data-stu-id="0eeef-119">Possible ID values include:</span></span>
  
- <span data-ttu-id="0eeef-120">Ungültig</span><span class="sxs-lookup"><span data-stu-id="0eeef-120">Invalid</span></span>
    
   <span data-ttu-id="0eeef-121">Diesen Wert nicht verwenden</span><span class="sxs-lookup"><span data-stu-id="0eeef-121">Do not use this value</span></span>
    
- <span data-ttu-id="0eeef-122">ExtendedFlags</span><span class="sxs-lookup"><span data-stu-id="0eeef-122">ExtendedFlags</span></span>
    
   <span data-ttu-id="0eeef-123">Die Daten sind ein vier-Byte-Wert, der wie folgt formatiert ist:</span><span class="sxs-lookup"><span data-stu-id="0eeef-123">The data is a four byte value formatted as:</span></span>
    
   |<span data-ttu-id="0eeef-124">**Bit**</span><span class="sxs-lookup"><span data-stu-id="0eeef-124">**Bits**</span></span>|<span data-ttu-id="0eeef-125">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0eeef-125">**Description**</span></span>|
   |:-----|:-----|
   |<span data-ttu-id="0eeef-126">0-1</span><span class="sxs-lookup"><span data-stu-id="0eeef-126">0-1</span></span>  <br/> |<span data-ttu-id="0eeef-127">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="0eeef-127">Reserved.</span></span>  <br/> |
   |<span data-ttu-id="0eeef-128">2</span><span class="sxs-lookup"><span data-stu-id="0eeef-128">2</span></span>  <br/> |<span data-ttu-id="0eeef-129">Wird auf 0 festgelegt, wenn die Anwendung eine Richtlinienbeschreibung anzeigen soll.</span><span class="sxs-lookup"><span data-stu-id="0eeef-129">Set to 0 if the application should show a policy description.</span></span>  <br/> |
   |<span data-ttu-id="0eeef-130">3-5</span><span class="sxs-lookup"><span data-stu-id="0eeef-130">3-5</span></span>  <br/> |<span data-ttu-id="0eeef-131">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="0eeef-131">Reserved.</span></span>  <br/> |
   |<span data-ttu-id="0eeef-132">6-7</span><span class="sxs-lookup"><span data-stu-id="0eeef-132">6-7</span></span>  <br/> |<span data-ttu-id="0eeef-133">Steuert die Anzeige der Anzahl von Nachrichten im Ordner.</span><span class="sxs-lookup"><span data-stu-id="0eeef-133">Controls the display of the number of messages in the folder.</span></span>  <br/> <span data-ttu-id="0eeef-134">0-verwenden der Standardeinstellung</span><span class="sxs-lookup"><span data-stu-id="0eeef-134">0 - Use the default setting</span></span>  <br/> <span data-ttu-id="0eeef-135">1-die Anzahl der ungelesenen Nachrichten verwenden</span><span class="sxs-lookup"><span data-stu-id="0eeef-135">1 - Use the number of unread messages</span></span>  <br/> <span data-ttu-id="0eeef-136">3-Verwenden der Gesamtanzahl von Nachrichten</span><span class="sxs-lookup"><span data-stu-id="0eeef-136">3 - Use the total number of messages</span></span>  <br/> |
   |<span data-ttu-id="0eeef-137">8-31</span><span class="sxs-lookup"><span data-stu-id="0eeef-137">8-31</span></span>  <br/> |<span data-ttu-id="0eeef-138">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="0eeef-138">Reserved.</span></span>  <br/> |
   
<span data-ttu-id="0eeef-139">ReServierte Elemente können ignoriert werden, aber vorhandene Werte müssen beibehalten werden.</span><span class="sxs-lookup"><span data-stu-id="0eeef-139">Reserved items can be ignored, but existing values must be preserved.</span></span>
    
- <span data-ttu-id="0eeef-140">SearchFolderID</span><span class="sxs-lookup"><span data-stu-id="0eeef-140">SearchFolderID</span></span>
    
   <span data-ttu-id="0eeef-141">Das Datenfeld ist ein 16-Byte-Feld.</span><span class="sxs-lookup"><span data-stu-id="0eeef-141">The data field is a 16-byte field.</span></span> <span data-ttu-id="0eeef-142">Wenn die Anwendung einen beständigen Suchordner erstellt, muss dieses Feld für den Ordner auf den gleichen Wert wie die binäre **PR_WB_SF_TAG** ([pidtagsearchfolderid ()](pidtagsearchfolderid-canonical-property.md))-Eigenschaft für die Suchordner Nachricht festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="0eeef-142">When the application creates a persistent search folder, it must set this field on the folder to the same value as the **PR_WB_SF_TAG** ([PidTagSearchFolderId)](pidtagsearchfolderid-canonical-property.md)) binary property on the Search Folder Message.</span></span>
    
- <span data-ttu-id="0eeef-143">ToDoFolderVersion</span><span class="sxs-lookup"><span data-stu-id="0eeef-143">ToDoFolderVersion</span></span>
    
   <span data-ttu-id="0eeef-144">Das Datenfeld ist ein 4-Byte-Feld.</span><span class="sxs-lookup"><span data-stu-id="0eeef-144">The data field is a 4-byte field.</span></span> <span data-ttu-id="0eeef-145">Wenn die Anwendung den Aufgaben Suchordner erstellt, muss der Wert dieses Felds für den Ordner auf den Little-Endian-ganzzahligen Wert "0x000c0000" festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="0eeef-145">When the application creates the to-do search folder, it must set the value of this field on the folder to the little-endian integer value of" 0x000c0000":</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="0eeef-146">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="0eeef-146">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0eeef-147">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="0eeef-147">Protocol specifications</span></span>

<span data-ttu-id="0eeef-148">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0eeef-148">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0eeef-149">Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="0eeef-149">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0eeef-150">[[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0eeef-150">[[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0eeef-151">Gibt den Speicherort und die Eigenschaften von Client-und Serverkonfigurationsdaten an, wie beispielsweise Listen mit freigegebenen Kategorien und Arbeitszeiten.</span><span class="sxs-lookup"><span data-stu-id="0eeef-151">Specifies the location and properties of client and server configuration data, such as shared category lists and working hours.</span></span>
    
<span data-ttu-id="0eeef-152">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0eeef-152">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0eeef-153">Gibt die Eigenschaften und Vorgänge zum Bearbeiten einer Suchordner Listen Konfiguration an.</span><span class="sxs-lookup"><span data-stu-id="0eeef-153">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0eeef-154">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="0eeef-154">Header files</span></span>

<span data-ttu-id="0eeef-155">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="0eeef-155">Mapidefs.h</span></span>
  
> <span data-ttu-id="0eeef-156">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="0eeef-156">Provides data type definitions.</span></span>
    
<span data-ttu-id="0eeef-157">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="0eeef-157">Mapitags.h</span></span>
  
> <span data-ttu-id="0eeef-158">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="0eeef-158">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0eeef-159">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0eeef-159">See also</span></span>

- [<span data-ttu-id="0eeef-160">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0eeef-160">MAPI Properties</span></span>](mapi-properties.md)
- [<span data-ttu-id="0eeef-161">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0eeef-161">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
- [<span data-ttu-id="0eeef-162">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="0eeef-162">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
- [<span data-ttu-id="0eeef-163">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="0eeef-163">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

