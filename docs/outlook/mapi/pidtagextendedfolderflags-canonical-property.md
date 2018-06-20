---
title: Kanonische PidTagExtendedFolderFlags-Eigenschaft
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
ms.openlocfilehash: 4a4d3c940539c23be8ec212cb85e3dd4f3a04aab
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794368"
---
# <a name="pidtagextendedfolderflags-canonical-property"></a><span data-ttu-id="b0c00-103">Kanonische PidTagExtendedFolderFlags-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="b0c00-103">PidTagExtendedFolderFlags Canonical Property</span></span>
 
<span data-ttu-id="b0c00-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b0c00-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b0c00-105">Erweiterte Flags zu einem Ordner enthält.</span><span class="sxs-lookup"><span data-stu-id="b0c00-105">Contains extended flags about a folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b0c00-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="b0c00-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b0c00-107">PR_EXTENDED_FOLDER_FLAGS</span><span class="sxs-lookup"><span data-stu-id="b0c00-107">PR_EXTENDED_FOLDER_FLAGS</span></span>  <br/> |
|<span data-ttu-id="b0c00-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="b0c00-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b0c00-109">0x36DA</span><span class="sxs-lookup"><span data-stu-id="b0c00-109">0x36DA</span></span>  <br/> |
|<span data-ttu-id="b0c00-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="b0c00-110">Data type:</span></span>  <br/> |<span data-ttu-id="b0c00-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="b0c00-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="b0c00-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="b0c00-112">Area:</span></span>  <br/> |<span data-ttu-id="b0c00-113">MAPI-container</span><span class="sxs-lookup"><span data-stu-id="b0c00-113">MAPI container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b0c00-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b0c00-114">Remarks</span></span>

<span data-ttu-id="b0c00-115">Diese Eigenschaft ist ein binären Stream, der codierte untergeordnete Eigenschaften für den Ordner enthält.</span><span class="sxs-lookup"><span data-stu-id="b0c00-115">This property is a binary stream that contains encoded sub-properties for the folder.</span></span> <span data-ttu-id="b0c00-116">Es wird als eine Reihe von variabler Länge Sub-Elemente formatiert.</span><span class="sxs-lookup"><span data-stu-id="b0c00-116">It is formatted as a series of variable length sub items.</span></span> <span data-ttu-id="b0c00-117">Die ersten 8 Bits des Elements Sub ist ein Feld-ID, die angibt, welche Art von Flag das Sub-Element darstellt.</span><span class="sxs-lookup"><span data-stu-id="b0c00-117">The first 8 bits of the sub item is an ID field, which indicates what kind of flag the sub item represents.</span></span> <span data-ttu-id="b0c00-118">Die zweite 8 Bits ist die Anzahl von Bytes der Daten, die folgen.</span><span class="sxs-lookup"><span data-stu-id="b0c00-118">The second 8 bits is the number of bytes of data that follow.</span></span>
  
<span data-ttu-id="b0c00-119">Mögliche Werte für ID:</span><span class="sxs-lookup"><span data-stu-id="b0c00-119">Possible ID values include:</span></span>
  
- <span data-ttu-id="b0c00-120">Ungültig</span><span class="sxs-lookup"><span data-stu-id="b0c00-120">Invalid</span></span>
    
   <span data-ttu-id="b0c00-121">Verwenden Sie diesen Wert nicht</span><span class="sxs-lookup"><span data-stu-id="b0c00-121">Do not use this value</span></span>
    
- <span data-ttu-id="b0c00-122">ExtendedFlags</span><span class="sxs-lookup"><span data-stu-id="b0c00-122">ExtendedFlags</span></span>
    
   <span data-ttu-id="b0c00-123">Die Daten ist ein hochgestelltes vier Byte-Wert:</span><span class="sxs-lookup"><span data-stu-id="b0c00-123">The data is a four byte value formatted as:</span></span>
    
   |<span data-ttu-id="b0c00-124">**Bits**</span><span class="sxs-lookup"><span data-stu-id="b0c00-124">**Bits**</span></span>|<span data-ttu-id="b0c00-125">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b0c00-125">**Description**</span></span>|
   |:-----|:-----|
   |<span data-ttu-id="b0c00-126">0-1</span><span class="sxs-lookup"><span data-stu-id="b0c00-126">0-1</span></span>  <br/> |<span data-ttu-id="b0c00-127">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="b0c00-127">Reserved.</span></span>  <br/> |
   |<span data-ttu-id="b0c00-128">2</span><span class="sxs-lookup"><span data-stu-id="b0c00-128">2</span></span>  <br/> |<span data-ttu-id="b0c00-129">Auf 0 festgelegt, wenn die Anwendung eine Beschreibung der Richtlinie angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="b0c00-129">Set to 0 if the application should show a policy description.</span></span>  <br/> |
   |<span data-ttu-id="b0c00-130">3 bis 5</span><span class="sxs-lookup"><span data-stu-id="b0c00-130">3-5</span></span>  <br/> |<span data-ttu-id="b0c00-131">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="b0c00-131">Reserved.</span></span>  <br/> |
   |<span data-ttu-id="b0c00-132">6 und 7</span><span class="sxs-lookup"><span data-stu-id="b0c00-132">6-7</span></span>  <br/> |<span data-ttu-id="b0c00-133">Steuert die Anzeige der Anzahl von Nachrichten in den Ordner.</span><span class="sxs-lookup"><span data-stu-id="b0c00-133">Controls the display of the number of messages in the folder.</span></span>  <br/> <span data-ttu-id="b0c00-134">0 – verwenden Sie die Standardeinstellung</span><span class="sxs-lookup"><span data-stu-id="b0c00-134">0 - Use the default setting</span></span>  <br/> <span data-ttu-id="b0c00-135">1 – die Anzahl der ungelesenen Nachrichten verwenden</span><span class="sxs-lookup"><span data-stu-id="b0c00-135">1 - Use the number of unread messages</span></span>  <br/> <span data-ttu-id="b0c00-136">3 - verwenden Sie die Gesamtzahl der Nachrichten</span><span class="sxs-lookup"><span data-stu-id="b0c00-136">3 - Use the total number of messages</span></span>  <br/> |
   |<span data-ttu-id="b0c00-137">8-31</span><span class="sxs-lookup"><span data-stu-id="b0c00-137">8-31</span></span>  <br/> |<span data-ttu-id="b0c00-138">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="b0c00-138">Reserved.</span></span>  <br/> |
   
<span data-ttu-id="b0c00-139">Reservierte Artikel können ignoriert werden, aber die vorhandenen Werte beibehalten werden müssen.</span><span class="sxs-lookup"><span data-stu-id="b0c00-139">Reserved items can be ignored, but existing values must be preserved.</span></span>
    
- <span data-ttu-id="b0c00-140">SearchFolderID</span><span class="sxs-lookup"><span data-stu-id="b0c00-140">SearchFolderID</span></span>
    
   <span data-ttu-id="b0c00-141">Das Datenfeld ist ein 16-Byte-Feld.</span><span class="sxs-lookup"><span data-stu-id="b0c00-141">The data field is a 16-byte field.</span></span> <span data-ttu-id="b0c00-142">Wenn die Anwendung einen beständigen Suchordner erstellt, muss dieses Feld für den Ordner auf den gleichen Wert wie der **PR_WB_SF_TAG** festgelegt ([PidTagSearchFolderId)](pidtagsearchfolderid-canonical-property.md)) binäre Eigenschaft für die Suche Ordner Nachricht.</span><span class="sxs-lookup"><span data-stu-id="b0c00-142">When the application creates a persistent search folder, it must set this field on the folder to the same value as the **PR_WB_SF_TAG** ([PidTagSearchFolderId)](pidtagsearchfolderid-canonical-property.md)) binary property on the Search Folder Message.</span></span>
    
- <span data-ttu-id="b0c00-143">ToDoFolderVersion</span><span class="sxs-lookup"><span data-stu-id="b0c00-143">ToDoFolderVersion</span></span>
    
   <span data-ttu-id="b0c00-144">Das Datenfeld ist ein 4-Byte-Feld.</span><span class="sxs-lookup"><span data-stu-id="b0c00-144">The data field is a 4-byte field.</span></span> <span data-ttu-id="b0c00-145">Wenn die Anwendung den Suchordner Aufgabe erstellt, muss den Wert dieses Felds für den Ordner der little-Endian-Ganzzahlwert der "0x000c0000" festgelegt:</span><span class="sxs-lookup"><span data-stu-id="b0c00-145">When the application creates the to-do search folder, it must set the value of this field on the folder to the little-endian integer value of" 0x000c0000":</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="b0c00-146">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="b0c00-146">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b0c00-147">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="b0c00-147">Protocol specifications</span></span>

<span data-ttu-id="b0c00-148">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b0c00-148">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b0c00-149">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="b0c00-149">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b0c00-150">[[MS-OXOCFG]](http://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b0c00-150">[[MS-OXOCFG]](http://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b0c00-151">Gibt den Speicherort und die Eigenschaften von Client- und Konfigurationsdaten, wie etwa freigegebene Kategorielisten und Arbeitszeiten.</span><span class="sxs-lookup"><span data-stu-id="b0c00-151">Specifies the location and properties of client and server configuration data, such as shared category lists and working hours.</span></span>
    
<span data-ttu-id="b0c00-152">[[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b0c00-152">[[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b0c00-153">Gibt die Eigenschaften und Operationen für das Bearbeiten der Liste einer Suchkonfiguration-Ordner.</span><span class="sxs-lookup"><span data-stu-id="b0c00-153">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b0c00-154">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="b0c00-154">Header files</span></span>

<span data-ttu-id="b0c00-155">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b0c00-155">Mapidefs.h</span></span>
  
> <span data-ttu-id="b0c00-156">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="b0c00-156">Provides data type definitions.</span></span>
    
<span data-ttu-id="b0c00-157">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="b0c00-157">Mapitags.h</span></span>
  
> <span data-ttu-id="b0c00-158">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="b0c00-158">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b0c00-159">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b0c00-159">See also</span></span>

- [<span data-ttu-id="b0c00-160">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b0c00-160">MAPI Properties</span></span>](mapi-properties.md)
- [<span data-ttu-id="b0c00-161">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b0c00-161">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
- [<span data-ttu-id="b0c00-162">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="b0c00-162">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
- [<span data-ttu-id="b0c00-163">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="b0c00-163">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

