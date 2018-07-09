---
title: AutoVervollständigen-Stream
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: d4f380fa-2ed9-4c7c-9ef3-b32f8409f657
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 7fc1fae4ed648d59c273b20ced247f6d20e01a6f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791354"
---
# <a name="autocomplete-stream"></a><span data-ttu-id="cc195-103">AutoVervollständigen-Stream</span><span class="sxs-lookup"><span data-stu-id="cc195-103">Autocomplete Stream</span></span>

  
  
<span data-ttu-id="cc195-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="cc195-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="cc195-105">Zusätzlich zu wissen, wie Microsoft Outlook mit den AutoVervollständigen-Stream interagiert, müssen Sie auch das Binärformat des Datenstroms AutoVervollständigen verstehen.</span><span class="sxs-lookup"><span data-stu-id="cc195-105">In addition to knowing how Microsoft Outlook interacts with the autocomplete stream, you must also understand the binary format of the autocomplete stream.</span></span>
  
<span data-ttu-id="cc195-106">Die AutoVervollständigen-Datenstrom ist ein Satz von Zeilen Empfänger-Eigenschaft, die als einen binären Datenstrom zusammen mit einigen Metadaten, die Buchhaltung gespeichert sind, die nur von Microsoft Outlook 2013, Microsoft Outlook 2010, Microsoft Office Outlook 2007 und Microsoft Outlook 2003 verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="cc195-106">The autocomplete stream is a set of recipient property rows that are saved as a binary stream together with some bookkeeping metadata that is used only by Microsoft Outlook 2013, Microsoft Outlook 2010, Microsoft Office Outlook 2007, and Microsoft Outlook 2003.</span></span> <span data-ttu-id="cc195-107">Die Metadaten ist Outlook Interaktionen mit dem AutoVervollständigen-Stream für die Überprüfung relevante, sodass dritte beibehalten müssen, was in jedem Metadaten-Block ist, wenn sie einen geänderte AutoVervollständigen-Stream speichern.</span><span class="sxs-lookup"><span data-stu-id="cc195-107">The metadata is relevant to Outlook interactions with the autocomplete stream so third parties must preserve what is in each metadata block when they save a modified autocomplete stream.</span></span> <span data-ttu-id="cc195-108">Anders ausgedrückt, sollten dritte nur den Zeile Set Teil der Binärformat ändern und beibehalten, was bereits in der die Metadaten-Blöcke des Datenstroms AutoVervollständigen ist.</span><span class="sxs-lookup"><span data-stu-id="cc195-108">In other words, third parties should modify only the row-set part of the binary format and preserve what was already in the metadata blocks of the autocomplete stream.</span></span>
  
## <a name="stream-visualization"></a><span data-ttu-id="cc195-109">Stream Visualisierung</span><span class="sxs-lookup"><span data-stu-id="cc195-109">Stream Visualization</span></span>

<span data-ttu-id="cc195-110">Das allgemeine Layout des Datenstroms AutoVervollständigen lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="cc195-110">The high-level layout of the autocomplete stream is as follows:</span></span>
  
<span data-ttu-id="cc195-111">Metadaten (4 Bytes)</span><span class="sxs-lookup"><span data-stu-id="cc195-111">Metadata (4 bytes)</span></span>
  
<span data-ttu-id="cc195-112">Nummer der Hauptversion (4 Bytes)</span><span class="sxs-lookup"><span data-stu-id="cc195-112">Major Version Number (4 bytes)</span></span>
  
<span data-ttu-id="cc195-113">Minor Versionsnummer (4 Bytes)</span><span class="sxs-lookup"><span data-stu-id="cc195-113">Minor Version Number (4 bytes)</span></span>
  
<span data-ttu-id="cc195-114">Anzahl der Zeilen n (4 Bytes)</span><span class="sxs-lookup"><span data-stu-id="cc195-114">Number of rows n (4 bytes)</span></span>
  
<span data-ttu-id="cc195-115">Anzahl der Eigenschaften p in Zeile 1 (4 Bytes)</span><span class="sxs-lookup"><span data-stu-id="cc195-115">Number of properties p in row one (4 bytes)</span></span>
  
<span data-ttu-id="cc195-116">Eigenschafts-Tag 1-Eigenschaft (4 Bytes)</span><span class="sxs-lookup"><span data-stu-id="cc195-116">Property 1's property tag (4 bytes)</span></span>
  
<span data-ttu-id="cc195-117">1-Eigenschaft des Daten (4 Bytes) reserviert.</span><span class="sxs-lookup"><span data-stu-id="cc195-117">Property 1's reserved data (4 bytes)</span></span>
  
<span data-ttu-id="cc195-118">Eigenschaft 1 Wert Union (8 Byte)</span><span class="sxs-lookup"><span data-stu-id="cc195-118">Property 1's value union (8 bytes)</span></span>
  
<span data-ttu-id="cc195-119">Wertdaten 1 Eigenschaft (0 oder Variable Bytes)</span><span class="sxs-lookup"><span data-stu-id="cc195-119">Property 1's value data (0 or variable bytes)</span></span>
  
<span data-ttu-id="cc195-120">…</span><span class="sxs-lookup"><span data-stu-id="cc195-120"></span></span> <span data-ttu-id="cc195-121">(über-Eigenschaft P-1-Eigenschaft 2)</span><span class="sxs-lookup"><span data-stu-id="cc195-121">(property 2 through property P-1)</span></span>
  
<span data-ttu-id="cc195-122">Eigenschaft p des Eigenschafts-Tag (4 Bytes)</span><span class="sxs-lookup"><span data-stu-id="cc195-122">Property p's property tag (4 bytes)</span></span>
  
<span data-ttu-id="cc195-123">Eigenschaft p der Daten (4 Bytes) reserviert.</span><span class="sxs-lookup"><span data-stu-id="cc195-123">Property p's reserved data (4 bytes)</span></span>
  
<span data-ttu-id="cc195-124">Eigenschaft p Wert Union (8 Byte)</span><span class="sxs-lookup"><span data-stu-id="cc195-124">Property p's value union (8 bytes)</span></span>
  
<span data-ttu-id="cc195-125">Eigenschaft p des Wertdaten (0 oder Variable Bytes)</span><span class="sxs-lookup"><span data-stu-id="cc195-125">Property p's value data (0 or variable bytes)</span></span>
  
<span data-ttu-id="cc195-126">Anzahl der Eigenschaften Q in Zeile 2 (4 Bytes)</span><span class="sxs-lookup"><span data-stu-id="cc195-126">Number of properties q in row two (4 bytes)</span></span>
  
<span data-ttu-id="cc195-127">…</span><span class="sxs-lookup"><span data-stu-id="cc195-127"></span></span> <span data-ttu-id="cc195-128">(die zweite Zeileneigenschaften)</span><span class="sxs-lookup"><span data-stu-id="cc195-128">(row two's properties)</span></span>
  
<span data-ttu-id="cc195-129">…</span><span class="sxs-lookup"><span data-stu-id="cc195-129"></span></span> <span data-ttu-id="cc195-130">(Zeile 3 über Zeile n-1)</span><span class="sxs-lookup"><span data-stu-id="cc195-130">(row 3 through row n-1)</span></span>
  
<span data-ttu-id="cc195-131">Anzahl der Eigenschaften R in Zeile n (4 Bytes)</span><span class="sxs-lookup"><span data-stu-id="cc195-131">Number of properties r in row n (4 bytes)</span></span>
  
<span data-ttu-id="cc195-132">…</span><span class="sxs-lookup"><span data-stu-id="cc195-132"></span></span> <span data-ttu-id="cc195-133">(Zeile n's Eigenschaften)</span><span class="sxs-lookup"><span data-stu-id="cc195-133">(row n's properties)</span></span>
  
<span data-ttu-id="cc195-134">Zusätzliche Informationen Byteanzahl EI (4 Bytes)</span><span class="sxs-lookup"><span data-stu-id="cc195-134">Extra information byte count EI (4 bytes)</span></span>
  
<span data-ttu-id="cc195-135">Zusätzliche Informationen (EI Bytes)</span><span class="sxs-lookup"><span data-stu-id="cc195-135">Extra information (EI bytes)</span></span>
  
<span data-ttu-id="cc195-136">Metadaten (8 Byte)</span><span class="sxs-lookup"><span data-stu-id="cc195-136">Metadata (8 bytes)</span></span>
  
<span data-ttu-id="cc195-137">Ein Beispiel für eine binäre Struktur, finden Sie unter Binary für das Beispiel in der [Outlook 2003/2007 NK2-Dateiformat und Richtlinien für Entwickler.](http://portalvhds6gyn3khqwmgzd.blob.core.windows.net/files/NK2/NK2WithBinaryExample.pdf)</span><span class="sxs-lookup"><span data-stu-id="cc195-137">For an example of a binary structure, see Binary Example in the [Outlook 2003/2007 NK2 File Format and Developer Guidelines.](http://portalvhds6gyn3khqwmgzd.blob.core.windows.net/files/NK2/NK2WithBinaryExample.pdf)</span></span>
  
## <a name="high-level-layout"></a><span data-ttu-id="cc195-138">Allgemeine Layout</span><span class="sxs-lookup"><span data-stu-id="cc195-138">High-level Layout</span></span>

<span data-ttu-id="cc195-139">Generell wird das Layout des Datenstroms AutoVervollständigen wie folgt:</span><span class="sxs-lookup"><span data-stu-id="cc195-139">Broadly speaking, the layout of the autocomplete stream is as follows:</span></span>
  
|<span data-ttu-id="cc195-140">**Wertdaten**</span><span class="sxs-lookup"><span data-stu-id="cc195-140">**Value Data**</span></span>|<span data-ttu-id="cc195-141">**Anzahl von Bytes**</span><span class="sxs-lookup"><span data-stu-id="cc195-141">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="cc195-142">Metadaten</span><span class="sxs-lookup"><span data-stu-id="cc195-142">Metadata</span></span>  <br/> |<span data-ttu-id="cc195-143">4</span><span class="sxs-lookup"><span data-stu-id="cc195-143">4</span></span>  <br/> |
|<span data-ttu-id="cc195-144">Nummer der Hauptversion</span><span class="sxs-lookup"><span data-stu-id="cc195-144">Major Version Number</span></span>  <br/> |<span data-ttu-id="cc195-145">4</span><span class="sxs-lookup"><span data-stu-id="cc195-145">4</span></span>  <br/> |
|<span data-ttu-id="cc195-146">Nummer der Nebenversion</span><span class="sxs-lookup"><span data-stu-id="cc195-146">Minor Version Number</span></span>  <br/> |<span data-ttu-id="cc195-147">4</span><span class="sxs-lookup"><span data-stu-id="cc195-147">4</span></span>  <br/> |
|<span data-ttu-id="cc195-148">Rowset-fest</span><span class="sxs-lookup"><span data-stu-id="cc195-148">Row-set</span></span>  <br/> |<span data-ttu-id="cc195-149">Variable</span><span class="sxs-lookup"><span data-stu-id="cc195-149">Variable</span></span>  <br/> |
|<span data-ttu-id="cc195-150">Zusätzliche Informationen Byteanzahl EI</span><span class="sxs-lookup"><span data-stu-id="cc195-150">Extra information byte count EI</span></span>  <br/> |<span data-ttu-id="cc195-151">4</span><span class="sxs-lookup"><span data-stu-id="cc195-151">4</span></span>  <br/> |
|<span data-ttu-id="cc195-152">Zusätzliche Informationen</span><span class="sxs-lookup"><span data-stu-id="cc195-152">Extra information</span></span>  <br/> |<span data-ttu-id="cc195-153">EI</span><span class="sxs-lookup"><span data-stu-id="cc195-153">EI</span></span>  <br/> |
|<span data-ttu-id="cc195-154">Metadaten</span><span class="sxs-lookup"><span data-stu-id="cc195-154">Metadata</span></span>  <br/> |<span data-ttu-id="cc195-155">8</span><span class="sxs-lookup"><span data-stu-id="cc195-155">8</span></span>  <br/> |
   
<span data-ttu-id="cc195-156">Wenn dieser Datenstrom lesen, wenn die Hauptversion 12 unterscheidet, sollte klicken Sie dann diesen Datenstrom nicht lesen oder schreiben.</span><span class="sxs-lookup"><span data-stu-id="cc195-156">When reading this stream, if the major version is different than 12, then this stream should not be read or written.</span></span> <span data-ttu-id="cc195-157">Die aktuelle Nebenversion des Datenstroms AutoVervollständigen ist 0, womit die zusätzlichen Informationen Byteanzahl auf 0 festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="cc195-157">The current minor version of the autocomplete stream is 0, which has the Extra Information Byte count set to 0.</span></span> <span data-ttu-id="cc195-158">Wenn die Nebenversion 0 unterscheidet, wird die Informationen in die zusätzlichen Informationen, die beim Lesen der Streams lesen und beim Schreiben des Streams beibehalten werden muss vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="cc195-158">If the minor version is different than 0, then there will be information in the extra information that needs to be read when reading the stream and preserved when writing the stream.</span></span> <span data-ttu-id="cc195-159">Die Nebenversion müssen auch beim Schreiben des Streams beibehalten werden soll.</span><span class="sxs-lookup"><span data-stu-id="cc195-159">The minor version will also need to be preserved when writing the stream.</span></span> <span data-ttu-id="cc195-160">Wenn beide nicht beibehalten werden, verlieren Instanzen von Outlook, die die zusätzliche Informationen geschrieben haben Daten.</span><span class="sxs-lookup"><span data-stu-id="cc195-160">If both of these are not preserved, instances of Outlook that wrote the extra information will lose data.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="cc195-161">Applikationen dürfen keine benutzerdefinierte Daten in das Feld zusätzliche Informationen hinzufügen oder ändern die Nebenversion, wie diese Funktionalität zur Unterstützung von Outlook-Erweiterungen für das Format und nicht beliebige Drittanbieter-Erweiterungen ist.</span><span class="sxs-lookup"><span data-stu-id="cc195-161">Applications must not add custom data to the Extra Information field or change the minor version as this functionality is to support Outlook extensions to the format and not arbitrary third-party extensions.</span></span> 
  
## <a name="row-set-layout"></a><span data-ttu-id="cc195-162">Rowset Layout</span><span class="sxs-lookup"><span data-stu-id="cc195-162">Row-set Layout</span></span>

<span data-ttu-id="cc195-163">Das Layout Rowset lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="cc195-163">The row-set layout is as follows:</span></span> 
  
|<span data-ttu-id="cc195-164">**Wertdaten**</span><span class="sxs-lookup"><span data-stu-id="cc195-164">**Value Data**</span></span>|<span data-ttu-id="cc195-165">**Anzahl von Bytes**</span><span class="sxs-lookup"><span data-stu-id="cc195-165">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="cc195-166">Anzahl von Zeilen</span><span class="sxs-lookup"><span data-stu-id="cc195-166">Number of rows</span></span>  <br/> |<span data-ttu-id="cc195-167">4</span><span class="sxs-lookup"><span data-stu-id="cc195-167">4</span></span>  <br/> |
|<span data-ttu-id="cc195-168">Rows</span><span class="sxs-lookup"><span data-stu-id="cc195-168">Rows</span></span>  <br/> |<span data-ttu-id="cc195-169">Variable</span><span class="sxs-lookup"><span data-stu-id="cc195-169">Variable</span></span>  <br/> |
   
<span data-ttu-id="cc195-170">Die Anzahl der Zeilen identifiziert, wie viele Zeilen in der nächsten Teil der Sequenz binären Stream stammen.</span><span class="sxs-lookup"><span data-stu-id="cc195-170">The number of rows identifies how many rows come in the next part of the binary stream sequence.</span></span>
  
## <a name="row-layout"></a><span data-ttu-id="cc195-171">Zeilenlayout</span><span class="sxs-lookup"><span data-stu-id="cc195-171">Row Layout</span></span>

<span data-ttu-id="cc195-172">Jede Zeile hat Folgendes Format:</span><span class="sxs-lookup"><span data-stu-id="cc195-172">Each row is of the following format:</span></span>
  
|<span data-ttu-id="cc195-173">**Wertdaten**</span><span class="sxs-lookup"><span data-stu-id="cc195-173">**Value Data**</span></span>|<span data-ttu-id="cc195-174">**Anzahl von Bytes**</span><span class="sxs-lookup"><span data-stu-id="cc195-174">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="cc195-175">Anzahl der Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="cc195-175">Number of properties</span></span>  <br/> |<span data-ttu-id="cc195-176">4</span><span class="sxs-lookup"><span data-stu-id="cc195-176">4</span></span>  <br/> |
|<span data-ttu-id="cc195-177">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="cc195-177">Properties</span></span>  <br/> |<span data-ttu-id="cc195-178">Variable</span><span class="sxs-lookup"><span data-stu-id="cc195-178">Variable</span></span>  <br/> |
   
<span data-ttu-id="cc195-179">Die Anzahl der Eigenschaften bestimmt, wie viele Eigenschaften in der nächsten Teil der Sequenz binären Stream stammen.</span><span class="sxs-lookup"><span data-stu-id="cc195-179">The number of properties identifies how many properties come in the next part of the binary stream sequence.</span></span>
  
## <a name="property-layout"></a><span data-ttu-id="cc195-180">Eigenschaft Layout</span><span class="sxs-lookup"><span data-stu-id="cc195-180">Property Layout</span></span>

<span data-ttu-id="cc195-181">Jede Eigenschaft hat das folgende Format:</span><span class="sxs-lookup"><span data-stu-id="cc195-181">Each property is of the following format:</span></span>
  
|<span data-ttu-id="cc195-182">**Wertdaten**</span><span class="sxs-lookup"><span data-stu-id="cc195-182">**Value Data**</span></span>|<span data-ttu-id="cc195-183">**Anzahl von Bytes**</span><span class="sxs-lookup"><span data-stu-id="cc195-183">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="cc195-184">Eigenschafts-Tag</span><span class="sxs-lookup"><span data-stu-id="cc195-184">Property Tag</span></span>  <br/> |<span data-ttu-id="cc195-185">4</span><span class="sxs-lookup"><span data-stu-id="cc195-185">4</span></span>  <br/> |
|<span data-ttu-id="cc195-186">Reservierte Daten</span><span class="sxs-lookup"><span data-stu-id="cc195-186">Reserved Data</span></span>  <br/> |<span data-ttu-id="cc195-187">4</span><span class="sxs-lookup"><span data-stu-id="cc195-187">4</span></span>  <br/> |
|<span data-ttu-id="cc195-188">Eigenschaft Wert Union</span><span class="sxs-lookup"><span data-stu-id="cc195-188">Property Value Union</span></span>  <br/> ||
|<span data-ttu-id="cc195-189">Wertdaten</span><span class="sxs-lookup"><span data-stu-id="cc195-189">Value Data</span></span>  <br/> |<span data-ttu-id="cc195-190">0 oder Variable (je nach Eigenschaft-Tag)</span><span class="sxs-lookup"><span data-stu-id="cc195-190">0 or variable (depending on the prop tag)</span></span>  <br/> |
   
## <a name="interpreting-the-property-value"></a><span data-ttu-id="cc195-191">Interpretieren den Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="cc195-191">Interpreting the Property Value</span></span>

<span data-ttu-id="cc195-192">Die Union-Eigenschaft Wert und die Daten des Werts sind interpretiert werden das Eigenschafts-Tag in den ersten 4 Byte des Blocks Eigenschaft basierend auf.</span><span class="sxs-lookup"><span data-stu-id="cc195-192">The Property Value Union and the Value Data are to be interpreted based on the property tag in the first 4 bytes of the property block.</span></span> <span data-ttu-id="cc195-193">Dieses Eigenschaftentag befindet sich in demselben Format wie ein MAPI-Eigenschaftentag.</span><span class="sxs-lookup"><span data-stu-id="cc195-193">This property tag is in the same format as a MAPI property tag.</span></span> <span data-ttu-id="cc195-194">Bits 0 bis 15 des Eigenschaftstags sind den Typ der Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="cc195-194">Bits 0 through 15 of the property tag are the property's type.</span></span> <span data-ttu-id="cc195-195">Bits 16 bis 31 sind die Eigenschaft Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="cc195-195">Bits 16 through 31 are the property's identifier.</span></span> <span data-ttu-id="cc195-196">Der Eigenschaftstyp bestimmt, wie die-Eigenschaft die restlichen gelesen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="cc195-196">The property type determines how the rest of the property should be read.</span></span>
  
## <a name="static-value"></a><span data-ttu-id="cc195-197">Statische Wert</span><span class="sxs-lookup"><span data-stu-id="cc195-197">Static Value</span></span>

<span data-ttu-id="cc195-198">Einige Eigenschaften haben keine Wertdaten und haben nur Daten in der Union.</span><span class="sxs-lookup"><span data-stu-id="cc195-198">Some properties have no Value Data and only have data in the union.</span></span> <span data-ttu-id="cc195-199">Die folgenden Eigenschaftentypen (die aus dem Tag-Eigenschaft stammen) sollte die Union-Eigenschaft 8-Byte-Daten wie folgt interpretiert werden:</span><span class="sxs-lookup"><span data-stu-id="cc195-199">The following property types (which come from the Property Tag) should interpret the 8-byte Property Union data as follows:</span></span>
  
|<span data-ttu-id="cc195-200">**Eigenschaft Type**</span><span class="sxs-lookup"><span data-stu-id="cc195-200">**Prop Type**</span></span>|<span data-ttu-id="cc195-201">**Eigenschaft Union Interpretation**</span><span class="sxs-lookup"><span data-stu-id="cc195-201">**Property Union Interpretation**</span></span>|
|:-----|:-----|
|<span data-ttu-id="cc195-202">PT_I2</span><span class="sxs-lookup"><span data-stu-id="cc195-202">PT_I2</span></span>  <br/> |<span data-ttu-id="cc195-203">kurze int</span><span class="sxs-lookup"><span data-stu-id="cc195-203">short int</span></span>  <br/> |
|<span data-ttu-id="cc195-204">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="cc195-204">PT_LONG</span></span>  <br/> |<span data-ttu-id="cc195-205">long</span><span class="sxs-lookup"><span data-stu-id="cc195-205">long</span></span>  <br/> |
|<span data-ttu-id="cc195-206">PT_R4</span><span class="sxs-lookup"><span data-stu-id="cc195-206">PT_R4</span></span>  <br/> |<span data-ttu-id="cc195-207">Gleitkommazahl</span><span class="sxs-lookup"><span data-stu-id="cc195-207">float</span></span>  <br/> |
|<span data-ttu-id="cc195-208">PT_DOUBLE</span><span class="sxs-lookup"><span data-stu-id="cc195-208">PT_DOUBLE</span></span>  <br/> |<span data-ttu-id="cc195-209">double</span><span class="sxs-lookup"><span data-stu-id="cc195-209">double</span></span>  <br/> |
|<span data-ttu-id="cc195-210">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="cc195-210">PT_BOOLEAN</span></span>  <br/> |<span data-ttu-id="cc195-211">kurze int</span><span class="sxs-lookup"><span data-stu-id="cc195-211">short int</span></span>  <br/> |
|<span data-ttu-id="cc195-212">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="cc195-212">PT_SYSTIME</span></span>  <br/> |<span data-ttu-id="cc195-213">FILETIME</span><span class="sxs-lookup"><span data-stu-id="cc195-213">FILETIME</span></span>  <br/> |
|<span data-ttu-id="cc195-214">PT_I8</span><span class="sxs-lookup"><span data-stu-id="cc195-214">PT_I8</span></span>  <br/> |<span data-ttu-id="cc195-215">LARGE_INTEGER</span><span class="sxs-lookup"><span data-stu-id="cc195-215">LARGE_INTEGER</span></span>  <br/> |
   
## <a name="dynamic-values"></a><span data-ttu-id="cc195-216">Dynamische Werte</span><span class="sxs-lookup"><span data-stu-id="cc195-216">Dynamic Values</span></span>

<span data-ttu-id="cc195-217">Andere Eigenschaften aufweisen Daten in einem Wert Datenblock, nachdem die ersten 16 Bytes, die die Tag-Eigenschaft, die reservierte Daten und der Union-Eigenschaft Wert enthalten.</span><span class="sxs-lookup"><span data-stu-id="cc195-217">Other properties have data in a Value Data block after the first 16 bytes that contain the Property Tag, the Reserved Data, and the Property Value Union.</span></span> <span data-ttu-id="cc195-218">Im Gegensatz zu statische Werte spielt die Daten, die in der 8-Byte-Eigenschaftswert Union gespeichert werden beim Lesen.</span><span class="sxs-lookup"><span data-stu-id="cc195-218">Unlike static values, the data that is stored in the 8-byte Property Value union is irrelevant on reading.</span></span> <span data-ttu-id="cc195-219">Beim Schreiben, stellen Sie sicher, dass diese 8 Bytes mit etwas zu füllen.</span><span class="sxs-lookup"><span data-stu-id="cc195-219">When writing, make sure that you fill these 8 bytes with something.</span></span> <span data-ttu-id="cc195-220">Der Inhalt von 8 Bytes ist jedoch nicht wichtig.</span><span class="sxs-lookup"><span data-stu-id="cc195-220">However, the content of the 8 bytes is not important.</span></span> <span data-ttu-id="cc195-221">Dynamische Werte bestimmt das Eigenschafts-Tag-Typ wie die Daten des Werts interpretiert werden.</span><span class="sxs-lookup"><span data-stu-id="cc195-221">In dynamic values, the property tag's type determines how to interpret the Value Data.</span></span>
  
<span data-ttu-id="cc195-222">PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="cc195-222">PT_STRING8</span></span> 
  
|<span data-ttu-id="cc195-223">**Wertdaten**</span><span class="sxs-lookup"><span data-stu-id="cc195-223">**Value Data**</span></span>|<span data-ttu-id="cc195-224">**Anzahl von Bytes**</span><span class="sxs-lookup"><span data-stu-id="cc195-224">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="cc195-225">Anzahl von Bytes n</span><span class="sxs-lookup"><span data-stu-id="cc195-225">Number of bytes n</span></span>  <br/> |<span data-ttu-id="cc195-226">4</span><span class="sxs-lookup"><span data-stu-id="cc195-226">4</span></span>  <br/> |
|<span data-ttu-id="cc195-227">Bytes als ANSI-Zeichenfolge interpretiert werden soll (einschließlich der NULL-Terminator)</span><span class="sxs-lookup"><span data-stu-id="cc195-227">Bytes to be interpreted as an ANSI string (includes NULL terminator)</span></span>  <br/> |<span data-ttu-id="cc195-228">n</span><span class="sxs-lookup"><span data-stu-id="cc195-228">n</span></span>  <br/> |
   
<span data-ttu-id="cc195-229">PT_CLSID</span><span class="sxs-lookup"><span data-stu-id="cc195-229">PT_CLSID</span></span>
  
|<span data-ttu-id="cc195-230">**Wertdaten**</span><span class="sxs-lookup"><span data-stu-id="cc195-230">**Value Data**</span></span>|<span data-ttu-id="cc195-231">**Anzahl von Bytes**</span><span class="sxs-lookup"><span data-stu-id="cc195-231">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="cc195-232">Bytes als GUID interpretiert werden soll</span><span class="sxs-lookup"><span data-stu-id="cc195-232">Bytes to be interpreted as a GUID</span></span>  <br/> |<span data-ttu-id="cc195-233">16</span><span class="sxs-lookup"><span data-stu-id="cc195-233">16</span></span>  <br/> |
|||
   
<span data-ttu-id="cc195-234">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="cc195-234">PT_BINARY</span></span> 
  
|<span data-ttu-id="cc195-235">**Wertdaten**</span><span class="sxs-lookup"><span data-stu-id="cc195-235">**Value Data**</span></span>|<span data-ttu-id="cc195-236">**Anzahl von Bytes**</span><span class="sxs-lookup"><span data-stu-id="cc195-236">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="cc195-237">Anzahl von Bytes n</span><span class="sxs-lookup"><span data-stu-id="cc195-237">Number of bytes n</span></span>  <br/> |<span data-ttu-id="cc195-238">4</span><span class="sxs-lookup"><span data-stu-id="cc195-238">4</span></span>  <br/> |
|<span data-ttu-id="cc195-239">Bytes als Bytearray interpretiert werden soll</span><span class="sxs-lookup"><span data-stu-id="cc195-239">Bytes to be interpreted as a byte array</span></span>  <br/> |<span data-ttu-id="cc195-240">n</span><span class="sxs-lookup"><span data-stu-id="cc195-240">n</span></span>  <br/> |
   
<span data-ttu-id="cc195-241">PT_ERROR</span><span class="sxs-lookup"><span data-stu-id="cc195-241">PT_ERROR</span></span>
  
|<span data-ttu-id="cc195-242">**Wertdaten**</span><span class="sxs-lookup"><span data-stu-id="cc195-242">**Value Data**</span></span>|<span data-ttu-id="cc195-243">**Anzahl von Bytes**</span><span class="sxs-lookup"><span data-stu-id="cc195-243">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="cc195-244">Anzahl von Bytes n</span><span class="sxs-lookup"><span data-stu-id="cc195-244">Number of bytes n</span></span>  <br/> |<span data-ttu-id="cc195-245">4</span><span class="sxs-lookup"><span data-stu-id="cc195-245">4</span></span>  <br/> |
|<span data-ttu-id="cc195-246">Bytes als Bytearray interpretiert werden soll</span><span class="sxs-lookup"><span data-stu-id="cc195-246">Bytes to be interpreted as a byte array</span></span>  <br/> |<span data-ttu-id="cc195-247">n</span><span class="sxs-lookup"><span data-stu-id="cc195-247">n</span></span>  <br/> |
   
<span data-ttu-id="cc195-248">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="cc195-248">PT_MV_BINARY</span></span>
  
|<span data-ttu-id="cc195-249">**Wertdaten**</span><span class="sxs-lookup"><span data-stu-id="cc195-249">**Value Data**</span></span>|<span data-ttu-id="cc195-250">**Anzahl von Bytes**</span><span class="sxs-lookup"><span data-stu-id="cc195-250">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="cc195-251">Anzahl der binären Arrays X</span><span class="sxs-lookup"><span data-stu-id="cc195-251">Number of binary arrays X</span></span>  <br/> |<span data-ttu-id="cc195-252">4</span><span class="sxs-lookup"><span data-stu-id="cc195-252">4</span></span>  <br/> |
|<span data-ttu-id="cc195-253">Ausführung von Bytes, die X enthält binäre Arrays.</span><span class="sxs-lookup"><span data-stu-id="cc195-253">A run of bytes that contains X binary arrays.</span></span> <span data-ttu-id="cc195-254">Jedes Array sollte genau wie das Ausführen PT_BINARY Byte interpretiert werden.</span><span class="sxs-lookup"><span data-stu-id="cc195-254">Each array should be interpreted exactly like the PT_BINARY byte run.</span></span>  <br/> |<span data-ttu-id="cc195-255">Variable</span><span class="sxs-lookup"><span data-stu-id="cc195-255">Variable</span></span>  <br/> |
   
<span data-ttu-id="cc195-256">PT_MV_STRING8 (Outlook 2007, Outlook 2010 und Outlook 2013)</span><span class="sxs-lookup"><span data-stu-id="cc195-256">PT_MV_STRING8 (Outlook 2007, Outlook 2010, and Outlook 2013)</span></span>
  
|<span data-ttu-id="cc195-257">**Wertdaten**</span><span class="sxs-lookup"><span data-stu-id="cc195-257">**Value Data**</span></span>|<span data-ttu-id="cc195-258">**Anzahl von Bytes**</span><span class="sxs-lookup"><span data-stu-id="cc195-258">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="cc195-259">Anzahl von ANSI-Zeichenfolgen X</span><span class="sxs-lookup"><span data-stu-id="cc195-259">Number of ANSI strings X</span></span>  <br/> |<span data-ttu-id="cc195-260">4</span><span class="sxs-lookup"><span data-stu-id="cc195-260">4</span></span>  <br/> |
|<span data-ttu-id="cc195-261">Ein Lauf von Bytes, die X-ANSI-Zeichenfolgen enthält.</span><span class="sxs-lookup"><span data-stu-id="cc195-261">A run of bytes that contains X ANSI strings.</span></span> <span data-ttu-id="cc195-262">Jede Zeichenfolge sollte genau wie das Ausführen PT_STRING8 Byte interpretiert werden.</span><span class="sxs-lookup"><span data-stu-id="cc195-262">Each string should be interpreted exactly like the PT_STRING8 byte run.</span></span>  <br/> |<span data-ttu-id="cc195-263">Variable</span><span class="sxs-lookup"><span data-stu-id="cc195-263">Variable</span></span>  <br/> |
   
<span data-ttu-id="cc195-264">PT_MV_UNICODE (Outlook 2007, Outlook 2010, Outlook 2013)</span><span class="sxs-lookup"><span data-stu-id="cc195-264">PT_MV_UNICODE (Outlook 2007, Outlook 2010, Outlook 2013)</span></span>
  
|<span data-ttu-id="cc195-265">**Wertdaten**</span><span class="sxs-lookup"><span data-stu-id="cc195-265">**Value Data**</span></span>|<span data-ttu-id="cc195-266">**Anzahl von Bytes**</span><span class="sxs-lookup"><span data-stu-id="cc195-266">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="cc195-267">Anzahl der Unicode-Zeichenfolgen X</span><span class="sxs-lookup"><span data-stu-id="cc195-267">Number of UNICODE strings X</span></span>  <br/> |<span data-ttu-id="cc195-268">4</span><span class="sxs-lookup"><span data-stu-id="cc195-268">4</span></span>  <br/> |
|<span data-ttu-id="cc195-269">Ein Lauf von Bytes, die X UNICODE Zeichenfolgen enthält.</span><span class="sxs-lookup"><span data-stu-id="cc195-269">A run of bytes that contains X UNICODE strings.</span></span> <span data-ttu-id="cc195-270">Jede Zeichenfolge sollte genau wie das Ausführen PT_UNICODE Byte interpretiert werden.</span><span class="sxs-lookup"><span data-stu-id="cc195-270">Each string should be interpreted exactly like the PT_UNICODE byte run.</span></span>  <br/> |<span data-ttu-id="cc195-271">Variable</span><span class="sxs-lookup"><span data-stu-id="cc195-271">Variable</span></span>  <br/> |
   
## <a name="significant-properties"></a><span data-ttu-id="cc195-272">Wesentliche Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="cc195-272">Significant properties</span></span>

<span data-ttu-id="cc195-273">Wie zuvor in diesem Thema erwähnt, müssen die binären Blöcke, die Eigenschaften darstellen Eigenschaftentags, die die Eigenschaften Address Book Empfänger entsprechen.</span><span class="sxs-lookup"><span data-stu-id="cc195-273">As mentioned previously in this topic, the binary blocks that represent properties have property tags that correspond to properties on address book recipients.</span></span> <span data-ttu-id="cc195-274">Für Eigenschaften, die hier nicht aufgeführt sind, können Sie Nachschlagen der Beschreibung unter http://msdn.microsoft.com/de-de/library/cc433490(EXCHG.80).aspx.</span><span class="sxs-lookup"><span data-stu-id="cc195-274">For properties that are not listed here, you can look up the property description at http://msdn.microsoft.com/de-de/library/cc433490(EXCHG.80).aspx.</span></span>
  
|<span data-ttu-id="cc195-275">**Eigenschaftenname**</span><span class="sxs-lookup"><span data-stu-id="cc195-275">**Property Name**</span></span>|<span data-ttu-id="cc195-276">**Eigenschafts-Tag**</span><span class="sxs-lookup"><span data-stu-id="cc195-276">**Property Tag**</span></span>|<span data-ttu-id="cc195-277">**Beschreibung (Weitere Informationen finden Sie unter MSDN)**</span><span class="sxs-lookup"><span data-stu-id="cc195-277">**Description (see MSDN for more information)**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="cc195-278">PR_NICK_NAME_W (nicht auf in AutoVervollständigen-Stream nur bestimmte Empfänger gesendeten)</span><span class="sxs-lookup"><span data-stu-id="cc195-278">PR_NICK_NAME_W (not transmitted on recipients, specific to autocomplete stream only)</span></span>  <br/> |<span data-ttu-id="cc195-279">0x6001001f</span><span class="sxs-lookup"><span data-stu-id="cc195-279">0x6001001f</span></span>  <br/> |<span data-ttu-id="cc195-280">Diese Eigenschaft muss in jeder Zeile Empfänger ersten sein.</span><span class="sxs-lookup"><span data-stu-id="cc195-280">This property must be first in each recipient row.</span></span> <span data-ttu-id="cc195-281">Es dient funktional als eine Schlüssel-ID für die Empfänger Zeile.</span><span class="sxs-lookup"><span data-stu-id="cc195-281">It functionally serves as a key identifier for the recipient row.</span></span>  <br/> |
|<span data-ttu-id="cc195-282">PR_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="cc195-282">PR_ENTRYID</span></span>  <br/> |<span data-ttu-id="cc195-283">0x0FFF0102</span><span class="sxs-lookup"><span data-stu-id="cc195-283">0x0FFF0102</span></span>  <br/> |<span data-ttu-id="cc195-284">Der Address Book Eintrag Bezeichner für den Empfänger.</span><span class="sxs-lookup"><span data-stu-id="cc195-284">The address book entry identifier for the recipient.</span></span>  <br/> |
|<span data-ttu-id="cc195-285">PR_DISPLAY_NAME_W</span><span class="sxs-lookup"><span data-stu-id="cc195-285">PR_DISPLAY_NAME_W</span></span>  <br/> |<span data-ttu-id="cc195-286">0x3001001F</span><span class="sxs-lookup"><span data-stu-id="cc195-286">0x3001001F</span></span>  <br/> |<span data-ttu-id="cc195-287">Der Name des Empfängers anzeigen.</span><span class="sxs-lookup"><span data-stu-id="cc195-287">The recipient's display name.</span></span>  <br/> |
|<span data-ttu-id="cc195-288">PR_EMAIL_ADDRESS_W</span><span class="sxs-lookup"><span data-stu-id="cc195-288">PR_EMAIL_ADDRESS_W</span></span>  <br/> |<span data-ttu-id="cc195-289">0x3003001F</span><span class="sxs-lookup"><span data-stu-id="cc195-289">0x3003001F</span></span>  <br/> |<span data-ttu-id="cc195-290">E-Mail-Adresse des Empfängers (z. B. johndoe@contoso.com oder/o = Contoso/OU = "Foo" / Cn = Recipients/Cn = Johndoe)</span><span class="sxs-lookup"><span data-stu-id="cc195-290">The recipient's email address (e.g. johndoe@contoso.com or /o=Contoso/OU=Foo/cn=Recipients/cn=johndoe)</span></span>  <br/> |
|<span data-ttu-id="cc195-291">PR_ADDRTYPE_W</span><span class="sxs-lookup"><span data-stu-id="cc195-291">PR_ADDRTYPE_W</span></span>  <br/> |<span data-ttu-id="cc195-292">0x3002001F</span><span class="sxs-lookup"><span data-stu-id="cc195-292">0x3002001F</span></span>  <br/> |<span data-ttu-id="cc195-293">Der Empfänger Adresstyp (z. B. SMTP oder EX).</span><span class="sxs-lookup"><span data-stu-id="cc195-293">The recipient's address type (e.g. SMTP or EX).</span></span>  <br/> |
|<span data-ttu-id="cc195-294">PR_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="cc195-294">PR_SEARCH_KEY</span></span>  <br/> |<span data-ttu-id="cc195-295">0x300B0102</span><span class="sxs-lookup"><span data-stu-id="cc195-295">0x300B0102</span></span>  <br/> |<span data-ttu-id="cc195-296">Der Empfänger MAPI-Suchen-Taste.</span><span class="sxs-lookup"><span data-stu-id="cc195-296">The recipient's MAPI search key.</span></span>  <br/> |
|<span data-ttu-id="cc195-297">PR_SMTP_ADDRESS_W</span><span class="sxs-lookup"><span data-stu-id="cc195-297">PR_SMTP_ADDRESS_W</span></span>  <br/> |<span data-ttu-id="cc195-298">0x39FE001f</span><span class="sxs-lookup"><span data-stu-id="cc195-298">0x39FE001f</span></span>  <br/> |<span data-ttu-id="cc195-299">SMTP-Adresse des Empfängers.</span><span class="sxs-lookup"><span data-stu-id="cc195-299">The recipient's SMTP address.</span></span>  <br/> |
|<span data-ttu-id="cc195-300">PR_DROPDOWN_DISPLAY_NAME_W (nicht auf in AutoVervollständigen-Stream nur bestimmte Empfänger gesendeten)</span><span class="sxs-lookup"><span data-stu-id="cc195-300">PR_DROPDOWN_DISPLAY_NAME_W (not transmitted on recipients, specific to autocomplete stream only)</span></span>  <br/> |<span data-ttu-id="cc195-301">0X6003001f</span><span class="sxs-lookup"><span data-stu-id="cc195-301">0X6003001f</span></span>  <br/> |<span data-ttu-id="cc195-302">Die Zeichenfolge, die in der AutoVervollständigen-Liste angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="cc195-302">The display string that appears in the autocomplete list.</span></span>  <br/> |
|<span data-ttu-id="cc195-303">PR_NICK_NAME_WEIGHT (nicht auf in AutoVervollständigen-Stream nur bestimmte Empfänger gesendeten)</span><span class="sxs-lookup"><span data-stu-id="cc195-303">PR_NICK_NAME_WEIGHT (not transmitted on recipients, specific to autocomplete stream only)</span></span>  <br/> |<span data-ttu-id="cc195-304">0x60040003</span><span class="sxs-lookup"><span data-stu-id="cc195-304">0x60040003</span></span>  <br/> |<span data-ttu-id="cc195-305">Die Stärke des in AutoVervollständigen-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="cc195-305">The weight of this autocomplete entry.</span></span> <span data-ttu-id="cc195-306">Die Gewichtung wird verwendet, um zu bestimmen, in welcher Reihenfolge AutoVervollständigen Einträge auftreten, wenn die AutoVervollständigen-Liste entsprechen.</span><span class="sxs-lookup"><span data-stu-id="cc195-306">The weight is used to determine in what order autocomplete entries occur when matching the autocomplete list.</span></span> <span data-ttu-id="cc195-307">Einträge mit höheren Gewichtung werden vor Einträgen mit geringeren Gewichtung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="cc195-307">Entries with higher weight will show before entries with lower weight.</span></span> <span data-ttu-id="cc195-308">Die vollständige AutoVervollständigen-Liste wird von dieser Eigenschaft sortiert.</span><span class="sxs-lookup"><span data-stu-id="cc195-308">The complete autocomplete list is sorted by this property.</span></span> <span data-ttu-id="cc195-309">Die Gewichtung in regelmäßigen Abständen nimmt mit der Zeit und erhöht, wenn der Benutzer eine e-Mail an diesen Empfänger sendet.</span><span class="sxs-lookup"><span data-stu-id="cc195-309">The weight periodically decreases over time and increases when the user sends an email to this recipient.</span></span> <span data-ttu-id="cc195-310">Siehe Beschreibung weiter unten in diesem Thema für Weitere Informationen zu dieser Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="cc195-310">See the description later in this topic for more information about this property.</span></span>  <br/> |
   
<span data-ttu-id="cc195-311">PR_NICK_NAME_WEIGHT</span><span class="sxs-lookup"><span data-stu-id="cc195-311">PR_NICK_NAME_WEIGHT</span></span>
  
<span data-ttu-id="cc195-312">Der Satz von Zeilen im Datenstrom AutoVervollständigen wird von der PR_NICK_NAME_WEIGHT-Eigenschaft in absteigender Reihenfolge sortiert und des AutoVervollständigen-Streams sollte immer dieses sortierte Merkmal beibehalten.</span><span class="sxs-lookup"><span data-stu-id="cc195-312">The set of rows in the autocomplete stream is sorted in descending order by the PR_NICK_NAME_WEIGHT property and the autocomplete stream should always preserve this sorted characteristic.</span></span> <span data-ttu-id="cc195-313">Aus diesem Grund sollten Änderungen an einer Zeile Gewichtung auch Stellen Sie sicher, dass die Zeilenposition wird die Sortierreihenfolge der der vollständige Satz von Zeilen verwaltet.</span><span class="sxs-lookup"><span data-stu-id="cc195-313">Therefore, any changes to a row's weight should also ensure that the row's position maintains the sorted order of the complete set of rows.</span></span> <span data-ttu-id="cc195-314">Hinzufügen der Zeile-Set sollte auf die richtige Position zur Aufrechterhaltung der Sortierreihenfolge eingefügt werden.</span><span class="sxs-lookup"><span data-stu-id="cc195-314">Any additions to the row-set should be inserted to the correct position to maintain the sorted order.</span></span>
  
<span data-ttu-id="cc195-315">Der Mindestwert für dieses Gewicht ist 0 x 1 und der Höchstwert ist LONG_MAX.</span><span class="sxs-lookup"><span data-stu-id="cc195-315">The minimum value of this weight is 0x1 and the maximum value is LONG_MAX.</span></span> <span data-ttu-id="cc195-316">Alle anderen Werte für die Gewichtung gelten als ungültig.</span><span class="sxs-lookup"><span data-stu-id="cc195-316">Any other values for the weight are considered invalid.</span></span>
  
<span data-ttu-id="cc195-317">Wenn Outlook 2007 sendet eine e-Mail an oder löst einen Empfänger wird es Stärke des Empfängers um 0 x 2000 erhöht.</span><span class="sxs-lookup"><span data-stu-id="cc195-317">When Outlook 2007 sends a mail to or resolves a recipient, it will increase that recipient's weight by 0x2000.</span></span>
  

