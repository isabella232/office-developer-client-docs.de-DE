---
title: Stream für automatisches Vervollständigen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: d4f380fa-2ed9-4c7c-9ef3-b32f8409f657
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 8b5c5fee71db0fc7bdd6e01c58e9c9a9c3d9fa22
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318081"
---
# <a name="autocomplete-stream"></a><span data-ttu-id="4806d-103">Stream für automatisches Vervollständigen</span><span class="sxs-lookup"><span data-stu-id="4806d-103">Autocomplete Stream</span></span>

  
  
<span data-ttu-id="4806d-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4806d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4806d-105">Sie müssen nicht nur wissen, wie Microsoft Outlook mit dem Stream für automatisches Vervollständigen interagiert, sondern auch das Binärformat von AutoVervollständigen verstehen.</span><span class="sxs-lookup"><span data-stu-id="4806d-105">In addition to knowing how Microsoft Outlook interacts with the autocomplete stream, you must also understand the binary format of the autocomplete stream.</span></span>
  
<span data-ttu-id="4806d-106">Der Stream für automatisches Vervollständigen besteht aus mehreren Zeilen mit Empfänger-Eigenschaften, die als binärer Stream zusammen mit einigen Verwaltungsmetadaten gespeichert und nur von Microsoft Outlook 2013, Microsoft Outlook 2010, Microsoft Office Outlook 2007 und Microsoft Outlook 2003 verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4806d-106">The autocomplete stream is a set of recipient property rows that are saved as a binary stream together with some bookkeeping metadata that is used only by Microsoft Outlook 2013, Microsoft Outlook 2010, Microsoft Office Outlook 2007, and Microsoft Outlook 2003.</span></span> <span data-ttu-id="4806d-107">Die Metadaten sind relevant für Outlook-Interaktionen mit dem Stream für automatisches Vervollständigen, sodass Dritte die Inhalte jedes Metadatenblocks beibehalten müssen, wenn sie einen geänderten Stream für automatisches Vervollständigen speichern.</span><span class="sxs-lookup"><span data-stu-id="4806d-107">The metadata is relevant to Outlook interactions with the autocomplete stream so third parties must preserve what is in each metadata block when they save a modified autocomplete stream.</span></span> <span data-ttu-id="4806d-108">Dritte sollten also nur den Zeilensatz des Binärformats ändern und die Inhalte der Metadatenblöcke des Streams für automatisches Vervollständigen beibehalten.</span><span class="sxs-lookup"><span data-stu-id="4806d-108">In other words, third parties should modify only the row-set part of the binary format and preserve what was already in the metadata blocks of the autocomplete stream.</span></span>
  
## <a name="stream-visualization"></a><span data-ttu-id="4806d-109">Stream-Visualisierung</span><span class="sxs-lookup"><span data-stu-id="4806d-109">Stream Visualization</span></span>

<span data-ttu-id="4806d-110">Das allgemeine Layout des Streams für automatisches Vervollständigen lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="4806d-110">The high-level layout of the autocomplete stream is as follows:</span></span>
  
<span data-ttu-id="4806d-111">Metadaten (4 Bytes)</span><span class="sxs-lookup"><span data-stu-id="4806d-111">Metadata (4 bytes)</span></span>
  
<span data-ttu-id="4806d-112">Hauptversionsnummer (4 Bytes)</span><span class="sxs-lookup"><span data-stu-id="4806d-112">Major Version Number (4 bytes)</span></span>
  
<span data-ttu-id="4806d-113">Nebenversionsnummer (4 Bytes)</span><span class="sxs-lookup"><span data-stu-id="4806d-113">Minor Version Number (4 bytes)</span></span>
  
<span data-ttu-id="4806d-114">Anzahl der Zeilen n (4 Bytes)</span><span class="sxs-lookup"><span data-stu-id="4806d-114">Number of rows n (4 bytes)</span></span>
  
<span data-ttu-id="4806d-115">Anzahl der Eigenschaften p in der ersten Zeile (4 Bytes)</span><span class="sxs-lookup"><span data-stu-id="4806d-115">Number of properties p in row one (4 bytes)</span></span>
  
<span data-ttu-id="4806d-116">Tag der Eigenschaft 1 (4 Bytes)</span><span class="sxs-lookup"><span data-stu-id="4806d-116">Property 1's property tag (4 bytes)</span></span>
  
<span data-ttu-id="4806d-117">Reservierte Daten der Eigenschaft 1 (4 Bytes)</span><span class="sxs-lookup"><span data-stu-id="4806d-117">Property 1's reserved data (4 bytes)</span></span>
  
<span data-ttu-id="4806d-118">Wertvereinigung der Eigenschaft 1 (8 Bytes)</span><span class="sxs-lookup"><span data-stu-id="4806d-118">Property 1's value union (8 bytes)</span></span>
  
<span data-ttu-id="4806d-119">Wertdaten der Eigenschaft 1 (0 oder variable Bytes)</span><span class="sxs-lookup"><span data-stu-id="4806d-119">Property 1's value data (0 or variable bytes)</span></span>
  
<span data-ttu-id="4806d-120">…</span><span class="sxs-lookup"><span data-stu-id="4806d-120"></span></span> <span data-ttu-id="4806d-121">(Eigenschaft 2 bis Eigenschaft P-1)</span><span class="sxs-lookup"><span data-stu-id="4806d-121">(property 2 through property P-1)</span></span>
  
<span data-ttu-id="4806d-122">Tag der Eigenschaft p (4 Bytes)</span><span class="sxs-lookup"><span data-stu-id="4806d-122">Property p's property tag (4 bytes)</span></span>
  
<span data-ttu-id="4806d-123">Reservierte Daten der Eigenschaft p (4 Bytes)</span><span class="sxs-lookup"><span data-stu-id="4806d-123">Property p's reserved data (4 bytes)</span></span>
  
<span data-ttu-id="4806d-124">Wertvereinigung der Eigenschaft p (8 Bytes)</span><span class="sxs-lookup"><span data-stu-id="4806d-124">Property p's value union (8 bytes)</span></span>
  
<span data-ttu-id="4806d-125">Wertdaten der Eigenschaft p (0 oder variable Bytes)</span><span class="sxs-lookup"><span data-stu-id="4806d-125">Property p's value data (0 or variable bytes)</span></span>
  
<span data-ttu-id="4806d-126">Anzahl der Eigenschaften q in der zweiten Zeile (4 Bytes)</span><span class="sxs-lookup"><span data-stu-id="4806d-126">Number of properties q in row two (4 bytes)</span></span>
  
<span data-ttu-id="4806d-127">…</span><span class="sxs-lookup"><span data-stu-id="4806d-127"></span></span> <span data-ttu-id="4806d-128">(Eigenschaften der zweiten Zeile)</span><span class="sxs-lookup"><span data-stu-id="4806d-128">(row two's properties)</span></span>
  
<span data-ttu-id="4806d-129">…</span><span class="sxs-lookup"><span data-stu-id="4806d-129"></span></span> <span data-ttu-id="4806d-130">(Zeile 3 bis Zeile n-1)</span><span class="sxs-lookup"><span data-stu-id="4806d-130">(row 3 through row n-1)</span></span>
  
<span data-ttu-id="4806d-131">Anzahl der Eigenschaften r in Zeile n (4 Bytes)</span><span class="sxs-lookup"><span data-stu-id="4806d-131">Number of properties r in row n (4 bytes)</span></span>
  
<span data-ttu-id="4806d-132">…</span><span class="sxs-lookup"><span data-stu-id="4806d-132"></span></span> <span data-ttu-id="4806d-133">(Eigenschaften der Zeile n)</span><span class="sxs-lookup"><span data-stu-id="4806d-133">(row n's properties)</span></span>
  
<span data-ttu-id="4806d-134">Zusätzliche Informationen Byteanzahl EI (4 Bytes)</span><span class="sxs-lookup"><span data-stu-id="4806d-134">Extra information byte count EI (4 bytes)</span></span>
  
<span data-ttu-id="4806d-135">Zusätzliche Informationen (EI-Bytes)</span><span class="sxs-lookup"><span data-stu-id="4806d-135">Extra information (EI bytes)</span></span>
  
<span data-ttu-id="4806d-136">Metadaten (8 Bytes)</span><span class="sxs-lookup"><span data-stu-id="4806d-136">Metadata (8 bytes)</span></span>
  
<span data-ttu-id="4806d-137">Ein Beispiel für eine binäre Struktur finden Sie im Binärbeispiel in den [Outlook 2003/2007 NK2-Dateiformat- und Entwicklerrichtlinien.](https://portalvhds6gyn3khqwmgzd.blob.core.windows.net/files/NK2/NK2WithBinaryExample.pdf)</span><span class="sxs-lookup"><span data-stu-id="4806d-137">For an example of a binary structure, see Binary Example in the [Outlook 2003/2007 NK2 File Format and Developer Guidelines.](https://portalvhds6gyn3khqwmgzd.blob.core.windows.net/files/NK2/NK2WithBinaryExample.pdf)</span></span>
  
## <a name="high-level-layout"></a><span data-ttu-id="4806d-138">Allgemeines Layout</span><span class="sxs-lookup"><span data-stu-id="4806d-138">High-level Layout</span></span>

<span data-ttu-id="4806d-139">Das allgemeine Layout des Streams für automatisches Vervollständigen lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="4806d-139">Broadly speaking, the layout of the autocomplete stream is as follows:</span></span>
  
|<span data-ttu-id="4806d-140">**Wertdaten**</span><span class="sxs-lookup"><span data-stu-id="4806d-140">**Value Data**</span></span>|<span data-ttu-id="4806d-141">**Anzahl der Bytes**</span><span class="sxs-lookup"><span data-stu-id="4806d-141">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4806d-142">Metadata</span><span class="sxs-lookup"><span data-stu-id="4806d-142">Metadata</span></span>  <br/> |<span data-ttu-id="4806d-143">4</span><span class="sxs-lookup"><span data-stu-id="4806d-143">4</span></span>  <br/> |
|<span data-ttu-id="4806d-144">Nummer der Hauptversion</span><span class="sxs-lookup"><span data-stu-id="4806d-144">Major Version Number</span></span>  <br/> |<span data-ttu-id="4806d-145">4</span><span class="sxs-lookup"><span data-stu-id="4806d-145">4</span></span>  <br/> |
|<span data-ttu-id="4806d-146">Nummer der Nebenversion</span><span class="sxs-lookup"><span data-stu-id="4806d-146">Minor Version Number</span></span>  <br/> |<span data-ttu-id="4806d-147">4</span><span class="sxs-lookup"><span data-stu-id="4806d-147">4</span></span>  <br/> |
|<span data-ttu-id="4806d-148">Zeilensatz</span><span class="sxs-lookup"><span data-stu-id="4806d-148">Row-set</span></span>  <br/> |<span data-ttu-id="4806d-149">Variable</span><span class="sxs-lookup"><span data-stu-id="4806d-149">Variable</span></span>  <br/> |
|<span data-ttu-id="4806d-150">Zusätzliche Informationen Byteanzahl EI</span><span class="sxs-lookup"><span data-stu-id="4806d-150">Extra information byte count EI</span></span>  <br/> |<span data-ttu-id="4806d-151">4</span><span class="sxs-lookup"><span data-stu-id="4806d-151">4</span></span>  <br/> |
|<span data-ttu-id="4806d-152">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="4806d-152">Extra information</span></span>  <br/> |<span data-ttu-id="4806d-153">EI</span><span class="sxs-lookup"><span data-stu-id="4806d-153">EI</span></span>  <br/> |
|<span data-ttu-id="4806d-154">Metadaten</span><span class="sxs-lookup"><span data-stu-id="4806d-154">Metadata</span></span>  <br/> |<span data-ttu-id="4806d-155">8</span><span class="sxs-lookup"><span data-stu-id="4806d-155">8</span></span>  <br/> |
   
<span data-ttu-id="4806d-156">Wenn die Hauptversion nicht 12, sollte dieser Datenstrom nicht gelesen oder geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="4806d-156">When reading this stream, if the major version is different than 12, then this stream should not be read or written.</span></span> <span data-ttu-id="4806d-157">Die aktuelle Nebenversion des Streams für automatisches Vervollständigen ist 0, d. h. die Bytes für die zusätzlichen Informationen sind auf "0" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="4806d-157">The current minor version of the autocomplete stream is 0, which has the Extra Information Byte count set to 0.</span></span> <span data-ttu-id="4806d-158">Wenn die Nebenversion nicht 0 ist, befinden sich Informationen in den zusätzlichen Informationen, die beim Lesen des Streams gelesen und beim Schreiben des Streams beibehalten werden müssen.</span><span class="sxs-lookup"><span data-stu-id="4806d-158">If the minor version is different than 0, then there will be information in the extra information that needs to be read when reading the stream and preserved when writing the stream.</span></span> <span data-ttu-id="4806d-159">Die Nebenversion muss auch beim Schreiben des Streams beibehalten werden.</span><span class="sxs-lookup"><span data-stu-id="4806d-159">The minor version will also need to be preserved when writing the stream.</span></span> <span data-ttu-id="4806d-160">Wenn beide nicht beibehalten werden, verlieren Instanzen von Outlook, die die zusätzlichen Informationen schreiben, Daten.</span><span class="sxs-lookup"><span data-stu-id="4806d-160">If both of these are not preserved, instances of Outlook that wrote the extra information will lose data.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="4806d-161">Anwendungen dürfen keine benutzerdefinierten Daten zum Feld Zusätzliche Informationen hinzufügen und nicht die Nebenversion ändern, da diese Funktion Outlook-Erweiterungen des Formats und keine beliebigen Erweiterungen von Drittanbietern unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4806d-161">Applications must not add custom data to the Extra Information field or change the minor version as this functionality is to support Outlook extensions to the format and not arbitrary third-party extensions.</span></span> 
  
## <a name="row-set-layout"></a><span data-ttu-id="4806d-162">Zeilensatz-Layout</span><span class="sxs-lookup"><span data-stu-id="4806d-162">Row-set Layout</span></span>

<span data-ttu-id="4806d-163">Das Zeilensatz-Layout lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="4806d-163">The row-set layout is as follows:</span></span> 
  
|<span data-ttu-id="4806d-164">**Wertdaten**</span><span class="sxs-lookup"><span data-stu-id="4806d-164">**Value Data**</span></span>|<span data-ttu-id="4806d-165">**Anzahl der Bytes**</span><span class="sxs-lookup"><span data-stu-id="4806d-165">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4806d-166">Anzahl der Zeilen</span><span class="sxs-lookup"><span data-stu-id="4806d-166">Number of rows</span></span>  <br/> |<span data-ttu-id="4806d-167">4</span><span class="sxs-lookup"><span data-stu-id="4806d-167">4</span></span>  <br/> |
|<span data-ttu-id="4806d-168">Zeilen</span><span class="sxs-lookup"><span data-stu-id="4806d-168">Rows</span></span>  <br/> |<span data-ttu-id="4806d-169">Variable</span><span class="sxs-lookup"><span data-stu-id="4806d-169">Variable</span></span>  <br/> |
   
<span data-ttu-id="4806d-170">Die Anzahl der Zeilen gibt an, wie viele Zeilen im nächsten Teil der binären Datenstromsequenz enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="4806d-170">The number of rows identifies how many rows come in the next part of the binary stream sequence.</span></span>
  
## <a name="row-layout"></a><span data-ttu-id="4806d-171">Zeilen-Layout</span><span class="sxs-lookup"><span data-stu-id="4806d-171">Row Layout</span></span>

<span data-ttu-id="4806d-172">Jede Zeile besitzt das folgende Format:</span><span class="sxs-lookup"><span data-stu-id="4806d-172">Each row is of the following format:</span></span>
  
|<span data-ttu-id="4806d-173">**Wertdaten**</span><span class="sxs-lookup"><span data-stu-id="4806d-173">**Value Data**</span></span>|<span data-ttu-id="4806d-174">**Anzahl der Bytes**</span><span class="sxs-lookup"><span data-stu-id="4806d-174">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4806d-175">Anzahl der Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4806d-175">Number of properties</span></span>  <br/> |<span data-ttu-id="4806d-176">4</span><span class="sxs-lookup"><span data-stu-id="4806d-176">4</span></span>  <br/> |
|<span data-ttu-id="4806d-177">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4806d-177">Properties</span></span>  <br/> |<span data-ttu-id="4806d-178">Variable</span><span class="sxs-lookup"><span data-stu-id="4806d-178">Variable</span></span>  <br/> |
   
<span data-ttu-id="4806d-179">Die Anzahl der Eigenschaften gibt an, wie viele Eigenschaften im nächsten Teil der binären Datenstromsequenz enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="4806d-179">The number of properties identifies how many properties come in the next part of the binary stream sequence.</span></span>
  
## <a name="property-layout"></a><span data-ttu-id="4806d-180">Eigenschaften-Layout</span><span class="sxs-lookup"><span data-stu-id="4806d-180">Property Layout</span></span>

<span data-ttu-id="4806d-181">Jede Eigenschaft besitzt das folgende Format:</span><span class="sxs-lookup"><span data-stu-id="4806d-181">Each property is of the following format:</span></span>
  
|<span data-ttu-id="4806d-182">**Wertdaten**</span><span class="sxs-lookup"><span data-stu-id="4806d-182">**Value Data**</span></span>|<span data-ttu-id="4806d-183">**Anzahl der Bytes**</span><span class="sxs-lookup"><span data-stu-id="4806d-183">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4806d-184">Tag der Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="4806d-184">Property Tag</span></span>  <br/> |<span data-ttu-id="4806d-185">4</span><span class="sxs-lookup"><span data-stu-id="4806d-185">4</span></span>  <br/> |
|<span data-ttu-id="4806d-186">Reservierte Daten</span><span class="sxs-lookup"><span data-stu-id="4806d-186">Reserved Data</span></span>  <br/> |<span data-ttu-id="4806d-187">4</span><span class="sxs-lookup"><span data-stu-id="4806d-187">4</span></span>  <br/> |
|<span data-ttu-id="4806d-188">Eigenschaftswertvereinigung</span><span class="sxs-lookup"><span data-stu-id="4806d-188">Property Value Union</span></span>  <br/> ||
|<span data-ttu-id="4806d-189">Wertdaten</span><span class="sxs-lookup"><span data-stu-id="4806d-189">Value Data</span></span>  <br/> |<span data-ttu-id="4806d-190">0 oder Variable (abhängig vom Tag der Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="4806d-190">0 or variable (depending on the prop tag)</span></span>  <br/> |
   
## <a name="interpreting-the-property-value"></a><span data-ttu-id="4806d-191">Interpretation des Eigenschaftswerts</span><span class="sxs-lookup"><span data-stu-id="4806d-191">Interpreting the Property Value</span></span>

<span data-ttu-id="4806d-192">Die Eigenschaftswertvereinigung und die Wertdaten werden basierend auf dem Tag der Eigenschaft in den ersten 4 Bytes des Eigenschaftsblocks interpretiert.</span><span class="sxs-lookup"><span data-stu-id="4806d-192">The Property Value Union and the Value Data are to be interpreted based on the property tag in the first 4 bytes of the property block.</span></span> <span data-ttu-id="4806d-193">Das Tag der Eigenschaft liegt im selben Format vor wie das Tag der MAPI-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="4806d-193">This property tag is in the same format as a MAPI property tag.</span></span> <span data-ttu-id="4806d-194">Die Bits 0 bis 15 des Tags der Eigenschaft geben den Typ der Eigenschaft an.</span><span class="sxs-lookup"><span data-stu-id="4806d-194">Bits 0 through 15 of the property tag are the property's type.</span></span> <span data-ttu-id="4806d-195">Die Bits 16 bis 31 sind Bezeichner der Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="4806d-195">Bits 16 through 31 are the property's identifier.</span></span> <span data-ttu-id="4806d-196">Der Eigenschaftentyp bestimmt, wie der Rest der Eigenschaft gelesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="4806d-196">The property type determines how the rest of the property should be read.</span></span>
  
## <a name="static-value"></a><span data-ttu-id="4806d-197">Statischer Wert</span><span class="sxs-lookup"><span data-stu-id="4806d-197">Static Value</span></span>

<span data-ttu-id="4806d-198">Einige Eigenschaften besitzen keine Wertdaten und verfügen nur in der Vereinigung über Daten.</span><span class="sxs-lookup"><span data-stu-id="4806d-198">Some properties have no Value Data and only have data in the union.</span></span> <span data-ttu-id="4806d-199">Die folgenden Eigenschaftstypen (die aus dem Eigenschafts-Tag stammen) sollten die 8 Byte Daten der Eigenschaftsvereinigung wie folgt interpretieren:</span><span class="sxs-lookup"><span data-stu-id="4806d-199">The following property types (which come from the Property Tag) should interpret the 8-byte Property Union data as follows:</span></span>
  
|<span data-ttu-id="4806d-200">**Eigenschaftstyp**</span><span class="sxs-lookup"><span data-stu-id="4806d-200">**Prop Type**</span></span>|<span data-ttu-id="4806d-201">**Interpretation der Eigenschaftsvereinigung**</span><span class="sxs-lookup"><span data-stu-id="4806d-201">**Property Union Interpretation**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4806d-202">PT_I2</span><span class="sxs-lookup"><span data-stu-id="4806d-202">PT_I2</span></span>  <br/> |<span data-ttu-id="4806d-203">short int</span><span class="sxs-lookup"><span data-stu-id="4806d-203">short int</span></span>  <br/> |
|<span data-ttu-id="4806d-204">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="4806d-204">PT_LONG</span></span>  <br/> |<span data-ttu-id="4806d-205">long</span><span class="sxs-lookup"><span data-stu-id="4806d-205">long</span></span>  <br/> |
|<span data-ttu-id="4806d-206">PT_R4</span><span class="sxs-lookup"><span data-stu-id="4806d-206">PT_R4</span></span>  <br/> |<span data-ttu-id="4806d-207">float</span><span class="sxs-lookup"><span data-stu-id="4806d-207">float</span></span>  <br/> |
|<span data-ttu-id="4806d-208">PT_DOUBLE</span><span class="sxs-lookup"><span data-stu-id="4806d-208">PT_DOUBLE</span></span>  <br/> |<span data-ttu-id="4806d-209">double</span><span class="sxs-lookup"><span data-stu-id="4806d-209">double</span></span>  <br/> |
|<span data-ttu-id="4806d-210">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="4806d-210">PT_BOOLEAN</span></span>  <br/> |<span data-ttu-id="4806d-211">short int</span><span class="sxs-lookup"><span data-stu-id="4806d-211">short int</span></span>  <br/> |
|<span data-ttu-id="4806d-212">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="4806d-212">PT_SYSTIME</span></span>  <br/> |<span data-ttu-id="4806d-213">FILETIME</span><span class="sxs-lookup"><span data-stu-id="4806d-213">FILETIME</span></span>  <br/> |
|<span data-ttu-id="4806d-214">PT_I8</span><span class="sxs-lookup"><span data-stu-id="4806d-214">PT_I8</span></span>  <br/> |<span data-ttu-id="4806d-215">LARGE_INTEGER</span><span class="sxs-lookup"><span data-stu-id="4806d-215">LARGE_INTEGER</span></span>  <br/> |
   
## <a name="dynamic-values"></a><span data-ttu-id="4806d-216">Dynamische Werte</span><span class="sxs-lookup"><span data-stu-id="4806d-216">Dynamic Values</span></span>

<span data-ttu-id="4806d-217">Andere Eigenschaften weisen nach den 16 Bytes Daten in einem Wertdatenblock auf, die das Tag der Eigenschaft, die Reservierten Daten und die Eigenschaftswertvereinigung enthalten.</span><span class="sxs-lookup"><span data-stu-id="4806d-217">Other properties have data in a Value Data block after the first 16 bytes that contain the Property Tag, the Reserved Data, and the Property Value Union.</span></span> <span data-ttu-id="4806d-218">Im Gegensatz zu statischen Werten sind die Daten, die in der 8-Byte-Eigenschaftswertvereinigung gespeichert sind, irrelevant für das Lesen.</span><span class="sxs-lookup"><span data-stu-id="4806d-218">Unlike static values, the data that is stored in the 8-byte Property Value union is irrelevant on reading.</span></span> <span data-ttu-id="4806d-219">Stellen Sie beim Schreiben sicher, dass die 8 Bytes mit Werten gefüllt werden.</span><span class="sxs-lookup"><span data-stu-id="4806d-219">When writing, make sure that you fill these 8 bytes with something.</span></span> <span data-ttu-id="4806d-220">Der Inhalt der 8 Bytes ist jedoch nicht wichtig.</span><span class="sxs-lookup"><span data-stu-id="4806d-220">However, the content of the 8 bytes is not important.</span></span> <span data-ttu-id="4806d-221">Bei dynamischen Werten bestimmt der Tagtyp der Eigenschaft die Interpretation der Wertdaten.</span><span class="sxs-lookup"><span data-stu-id="4806d-221">In dynamic values, the property tag's type determines how to interpret the Value Data.</span></span>
  
<span data-ttu-id="4806d-222">PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="4806d-222">PT_STRING8</span></span> 
  
|<span data-ttu-id="4806d-223">**Wertdaten**</span><span class="sxs-lookup"><span data-stu-id="4806d-223">**Value Data**</span></span>|<span data-ttu-id="4806d-224">**Anzahl der Bytes**</span><span class="sxs-lookup"><span data-stu-id="4806d-224">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4806d-225">Anzahl der Bytes n</span><span class="sxs-lookup"><span data-stu-id="4806d-225">Number of bytes n</span></span>  <br/> |<span data-ttu-id="4806d-226">4</span><span class="sxs-lookup"><span data-stu-id="4806d-226">4</span></span>  <br/> |
|<span data-ttu-id="4806d-227">Bytes werden als ANSI-Zeichenfolge interpretiert (beinhaltet NULL-Abschlusszeichen)</span><span class="sxs-lookup"><span data-stu-id="4806d-227">Bytes to be interpreted as an ANSI string (includes NULL terminator)</span></span>  <br/> |<span data-ttu-id="4806d-228">n</span><span class="sxs-lookup"><span data-stu-id="4806d-228">n</span></span>  <br/> |
   
<span data-ttu-id="4806d-229">PT_CLSID</span><span class="sxs-lookup"><span data-stu-id="4806d-229">PT_CLSID</span></span>
  
|<span data-ttu-id="4806d-230">**Wertdaten**</span><span class="sxs-lookup"><span data-stu-id="4806d-230">**Value Data**</span></span>|<span data-ttu-id="4806d-231">**Anzahl der Bytes**</span><span class="sxs-lookup"><span data-stu-id="4806d-231">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4806d-232">Bytes, die als GUID interpretiert werden</span><span class="sxs-lookup"><span data-stu-id="4806d-232">Bytes to be interpreted as a GUID</span></span>  <br/> |<span data-ttu-id="4806d-233">16</span><span class="sxs-lookup"><span data-stu-id="4806d-233">16</span></span>  <br/> |
|||
   
<span data-ttu-id="4806d-234">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="4806d-234">PT_BINARY</span></span> 
  
|<span data-ttu-id="4806d-235">**Wertdaten**</span><span class="sxs-lookup"><span data-stu-id="4806d-235">**Value Data**</span></span>|<span data-ttu-id="4806d-236">**Anzahl der Bytes**</span><span class="sxs-lookup"><span data-stu-id="4806d-236">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4806d-237">Anzahl der Bytes n</span><span class="sxs-lookup"><span data-stu-id="4806d-237">Number of bytes n</span></span>  <br/> |<span data-ttu-id="4806d-238">4</span><span class="sxs-lookup"><span data-stu-id="4806d-238">4</span></span>  <br/> |
|<span data-ttu-id="4806d-239">Bytes, die als Byte-Array interpretiert werden</span><span class="sxs-lookup"><span data-stu-id="4806d-239">Bytes to be interpreted as a byte array</span></span>  <br/> |<span data-ttu-id="4806d-240">n</span><span class="sxs-lookup"><span data-stu-id="4806d-240">n</span></span>  <br/> |
   
<span data-ttu-id="4806d-241">PT_ERROR</span><span class="sxs-lookup"><span data-stu-id="4806d-241">PT_ERROR</span></span>
  
|<span data-ttu-id="4806d-242">**Wertdaten**</span><span class="sxs-lookup"><span data-stu-id="4806d-242">**Value Data**</span></span>|<span data-ttu-id="4806d-243">**Anzahl der Bytes**</span><span class="sxs-lookup"><span data-stu-id="4806d-243">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4806d-244">Anzahl der Bytes n</span><span class="sxs-lookup"><span data-stu-id="4806d-244">Number of bytes n</span></span>  <br/> |<span data-ttu-id="4806d-245">4</span><span class="sxs-lookup"><span data-stu-id="4806d-245">4</span></span>  <br/> |
|<span data-ttu-id="4806d-246">Bytes, die als Byte-Array interpretiert werden</span><span class="sxs-lookup"><span data-stu-id="4806d-246">Bytes to be interpreted as a byte array</span></span>  <br/> |<span data-ttu-id="4806d-247">n</span><span class="sxs-lookup"><span data-stu-id="4806d-247">n</span></span>  <br/> |
   
<span data-ttu-id="4806d-248">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="4806d-248">PT_MV_BINARY</span></span>
  
|<span data-ttu-id="4806d-249">**Wertdaten**</span><span class="sxs-lookup"><span data-stu-id="4806d-249">**Value Data**</span></span>|<span data-ttu-id="4806d-250">**Anzahl der Bytes**</span><span class="sxs-lookup"><span data-stu-id="4806d-250">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4806d-251">Anzahl der binären Arrays X</span><span class="sxs-lookup"><span data-stu-id="4806d-251">Number of binary arrays X</span></span>  <br/> |<span data-ttu-id="4806d-252">4</span><span class="sxs-lookup"><span data-stu-id="4806d-252">4</span></span>  <br/> |
|<span data-ttu-id="4806d-253">Eine Ausführung von Bytes, die X binäre Arrays enthält.</span><span class="sxs-lookup"><span data-stu-id="4806d-253">A run of bytes that contains X binary arrays.</span></span> <span data-ttu-id="4806d-254">Jedes Array sollten exakt wie die PT_BINARY-Byte-Ausführung interpretiert werden.</span><span class="sxs-lookup"><span data-stu-id="4806d-254">Each array should be interpreted exactly like the PT_BINARY byte run.</span></span>  <br/> |<span data-ttu-id="4806d-255">Variable</span><span class="sxs-lookup"><span data-stu-id="4806d-255">Variable</span></span>  <br/> |
   
<span data-ttu-id="4806d-256">PT_MV_STRING8 (Outlook 2007, Outlook 2010, and Outlook 2013)</span><span class="sxs-lookup"><span data-stu-id="4806d-256">PT_MV_STRING8 (Outlook 2007, Outlook 2010, and Outlook 2013)</span></span>
  
|<span data-ttu-id="4806d-257">**Wertdaten**</span><span class="sxs-lookup"><span data-stu-id="4806d-257">**Value Data**</span></span>|<span data-ttu-id="4806d-258">**Anzahl der Bytes**</span><span class="sxs-lookup"><span data-stu-id="4806d-258">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4806d-259">Anzahl der ANSI-Zeichenfolgen X</span><span class="sxs-lookup"><span data-stu-id="4806d-259">Number of ANSI strings X</span></span>  <br/> |<span data-ttu-id="4806d-260">4</span><span class="sxs-lookup"><span data-stu-id="4806d-260">4</span></span>  <br/> |
|<span data-ttu-id="4806d-261">Eine Ausführung von Bytes, die X ANSI-Zeichenfolgen enthält.</span><span class="sxs-lookup"><span data-stu-id="4806d-261">A run of bytes that contains X ANSI strings.</span></span> <span data-ttu-id="4806d-262">Jede Zeichenfolge sollte exakt wie die PT_STRING8-Byte-Ausführung interpretiert werden.</span><span class="sxs-lookup"><span data-stu-id="4806d-262">Each string should be interpreted exactly like the PT_STRING8 byte run.</span></span>  <br/> |<span data-ttu-id="4806d-263">Variable</span><span class="sxs-lookup"><span data-stu-id="4806d-263">Variable</span></span>  <br/> |
   
<span data-ttu-id="4806d-264">PT_MV_UNICODE (Outlook 2007, Outlook 2010, Outlook 2013)</span><span class="sxs-lookup"><span data-stu-id="4806d-264">PT_MV_UNICODE (Outlook 2007, Outlook 2010, Outlook 2013)</span></span>
  
|<span data-ttu-id="4806d-265">**Wertdaten**</span><span class="sxs-lookup"><span data-stu-id="4806d-265">**Value Data**</span></span>|<span data-ttu-id="4806d-266">**Anzahl der Bytes**</span><span class="sxs-lookup"><span data-stu-id="4806d-266">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4806d-267">Anzahl der Unicode-Zeichenfolgen X</span><span class="sxs-lookup"><span data-stu-id="4806d-267">Number of UNICODE strings X</span></span>  <br/> |<span data-ttu-id="4806d-268">4</span><span class="sxs-lookup"><span data-stu-id="4806d-268">4</span></span>  <br/> |
|<span data-ttu-id="4806d-269">Eine Ausführung von Bytes, die X UNICODE-Zeichenfolgen enthält.</span><span class="sxs-lookup"><span data-stu-id="4806d-269">A run of bytes that contains X UNICODE strings.</span></span> <span data-ttu-id="4806d-270">Jede Zeichenfolge sollte exakt wie die PT_UNICODE-Byte-Ausführung interpretiert werden.</span><span class="sxs-lookup"><span data-stu-id="4806d-270">Each string should be interpreted exactly like the PT_UNICODE byte run.</span></span>  <br/> |<span data-ttu-id="4806d-271">Variable</span><span class="sxs-lookup"><span data-stu-id="4806d-271">Variable</span></span>  <br/> |
   
## <a name="significant-properties"></a><span data-ttu-id="4806d-272">Wesentliche Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4806d-272">Significant properties</span></span>

<span data-ttu-id="4806d-273">Wie zuvor in diesem Artikel erwähnt, besitzen die binären Blöcke, die Eigenschaften darstellen, Eigenschafts-Tags, die Eigenschaften von Adressbuchempfängern entsprechen.</span><span class="sxs-lookup"><span data-stu-id="4806d-273">As mentioned previously in this topic, the binary blocks that represent properties have property tags that correspond to properties on address book recipients.</span></span> <span data-ttu-id="4806d-274">Eine Beschreibung der Eigenschaften, die hier nicht aufgeführt sind, finden Sie unter https://msdn.microsoft.com/library/cc433490(EXCHG.80).aspx.</span><span class="sxs-lookup"><span data-stu-id="4806d-274">For properties that are not listed here, you can look up the property description at https://msdn.microsoft.com/library/cc433490(EXCHG.80).aspx.</span></span>
  
|<span data-ttu-id="4806d-275">**Eigenschaftsname**</span><span class="sxs-lookup"><span data-stu-id="4806d-275">**Property Name**</span></span>|<span data-ttu-id="4806d-276">**Eigenschafts-Tag**</span><span class="sxs-lookup"><span data-stu-id="4806d-276">**Property Tag**</span></span>|<span data-ttu-id="4806d-277">**Beschreibung (weitere Informationen finden Sie unter MSDN)**</span><span class="sxs-lookup"><span data-stu-id="4806d-277">**Description (see MSDN for more information)**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="4806d-278">PR_NICK_NAME_W (nicht auf Empfänger übertragen, spezifisch für den Stream für automatisches Vervollständigen)</span><span class="sxs-lookup"><span data-stu-id="4806d-278">PR_NICK_NAME_W (not transmitted on recipients, specific to autocomplete stream only)</span></span>  <br/> |<span data-ttu-id="4806d-279">0x6001001f</span><span class="sxs-lookup"><span data-stu-id="4806d-279">0x6001001f</span></span>  <br/> |<span data-ttu-id="4806d-280">Diese Eigenschaft muss in jeder Empfängerzeile zuerst stehen.</span><span class="sxs-lookup"><span data-stu-id="4806d-280">This property must be first in each recipient row.</span></span> <span data-ttu-id="4806d-281">Die Funktion dient als Schlüssel-ID für die Empfängerzeile.</span><span class="sxs-lookup"><span data-stu-id="4806d-281">It functionally serves as a key identifier for the recipient row.</span></span>  <br/> |
|<span data-ttu-id="4806d-282">PR_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="4806d-282">PR_ENTRYID</span></span>  <br/> |<span data-ttu-id="4806d-283">0x0FFF0102</span><span class="sxs-lookup"><span data-stu-id="4806d-283">0x0FFF0102</span></span>  <br/> |<span data-ttu-id="4806d-284">Eintrag-ID des Adressbuchs für den Empfänger</span><span class="sxs-lookup"><span data-stu-id="4806d-284">The address book entry identifier for the recipient.</span></span>  <br/> |
|<span data-ttu-id="4806d-285">PR_DISPLAY_NAME_W</span><span class="sxs-lookup"><span data-stu-id="4806d-285">PR_DISPLAY_NAME_W</span></span>  <br/> |<span data-ttu-id="4806d-286">0x3001001F</span><span class="sxs-lookup"><span data-stu-id="4806d-286">0x3001001F</span></span>  <br/> |<span data-ttu-id="4806d-287">Anzeigename des Empfängers</span><span class="sxs-lookup"><span data-stu-id="4806d-287">The recipient's display name.</span></span>  <br/> |
|<span data-ttu-id="4806d-288">PR_EMAIL_ADDRESS_W</span><span class="sxs-lookup"><span data-stu-id="4806d-288">PR_EMAIL_ADDRESS_W</span></span>  <br/> |<span data-ttu-id="4806d-289">0x3003001F</span><span class="sxs-lookup"><span data-stu-id="4806d-289">0x3003001F</span></span>  <br/> |<span data-ttu-id="4806d-290">E-Mail-Adresse des Empfängers (z. B. johndoe@contoso.com oder /o=Contoso/OU=Foo/cn=Recipients/cn=johndoe)</span><span class="sxs-lookup"><span data-stu-id="4806d-290">The recipient's email address (e.g. johndoe@contoso.com or /o=Contoso/OU=Foo/cn=Recipients/cn=johndoe)</span></span>  <br/> |
|<span data-ttu-id="4806d-291">PR_ADDRTYPE_W</span><span class="sxs-lookup"><span data-stu-id="4806d-291">PR_ADDRTYPE_W</span></span>  <br/> |<span data-ttu-id="4806d-292">0x3002001F</span><span class="sxs-lookup"><span data-stu-id="4806d-292">0x3002001F</span></span>  <br/> |<span data-ttu-id="4806d-293">Adresstyp des Empfängers (z. B. SMTP oder EX).</span><span class="sxs-lookup"><span data-stu-id="4806d-293">The recipient's address type (e.g. SMTP or EX).</span></span>  <br/> |
|<span data-ttu-id="4806d-294">PR_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="4806d-294">PR_SEARCH_KEY</span></span>  <br/> |<span data-ttu-id="4806d-295">0x300B0102</span><span class="sxs-lookup"><span data-stu-id="4806d-295">0x300B0102</span></span>  <br/> |<span data-ttu-id="4806d-296">MAPI-Suchschlüssel des Empfängers</span><span class="sxs-lookup"><span data-stu-id="4806d-296">The recipient's MAPI search key.</span></span>  <br/> |
|<span data-ttu-id="4806d-297">PR_SMTP_ADDRESS_W</span><span class="sxs-lookup"><span data-stu-id="4806d-297">PR_SMTP_ADDRESS_W</span></span>  <br/> |<span data-ttu-id="4806d-298">0x39FE001f</span><span class="sxs-lookup"><span data-stu-id="4806d-298">0x39FE001f</span></span>  <br/> |<span data-ttu-id="4806d-299">SMTP-Adresse des Empfängers</span><span class="sxs-lookup"><span data-stu-id="4806d-299">The recipient's SMTP address.</span></span>  <br/> |
|<span data-ttu-id="4806d-300">PR_DROPDOWN_DISPLAY_NAME_W (nicht auf Empfänger übertragen, spezifisch für den Stream für automatisches Vervollständigen)</span><span class="sxs-lookup"><span data-stu-id="4806d-300">PR_DROPDOWN_DISPLAY_NAME_W (not transmitted on recipients, specific to autocomplete stream only)</span></span>  <br/> |<span data-ttu-id="4806d-301">0X6003001f</span><span class="sxs-lookup"><span data-stu-id="4806d-301">0X6003001f</span></span>  <br/> |<span data-ttu-id="4806d-302">Zeichenfolge, die in der AutoVervollständigen-Liste angezeigt wird</span><span class="sxs-lookup"><span data-stu-id="4806d-302">The display string that appears in the autocomplete list.</span></span>  <br/> |
|<span data-ttu-id="4806d-303">PR_NICK_NAME_WEIGHT (nicht auf Empfänger übertragen, spezifisch für den Stream für automatisches Vervollständigen)</span><span class="sxs-lookup"><span data-stu-id="4806d-303">PR_NICK_NAME_WEIGHT (not transmitted on recipients, specific to autocomplete stream only)</span></span>  <br/> |<span data-ttu-id="4806d-304">0x60040003</span><span class="sxs-lookup"><span data-stu-id="4806d-304">0x60040003</span></span>  <br/> |<span data-ttu-id="4806d-305">Gewichtung dieses AutoVervollständigen-Eintrags</span><span class="sxs-lookup"><span data-stu-id="4806d-305">The weight of this autocomplete entry.</span></span> <span data-ttu-id="4806d-306">Mit der Gewichtung wird bestimmt, in welcher Reihenfolge AutoVervollständigen-Einträge beim Abgleich der AutoVervollständigen-Liste ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="4806d-306">The weight is used to determine in what order autocomplete entries occur when matching the autocomplete list.</span></span> <span data-ttu-id="4806d-307">Einträge mit höherer Gewichtung werden vor Einträgen mit geringerer Gewichtung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="4806d-307">Entries with higher weight will show before entries with lower weight.</span></span> <span data-ttu-id="4806d-308">Die komplette AutoVervollständigen-Liste wird nach dieser Eigenschaft sortiert.</span><span class="sxs-lookup"><span data-stu-id="4806d-308">The complete autocomplete list is sorted by this property.</span></span> <span data-ttu-id="4806d-309">Die Gewichtung wird in regelmäßigen Abständen über einen Zeitraum verringert und wird vergrößert, wenn der Benutzer eine E-Mail-Nachricht an diesen Empfänger sendet.</span><span class="sxs-lookup"><span data-stu-id="4806d-309">The weight periodically decreases over time and increases when the user sends an email to this recipient.</span></span> <span data-ttu-id="4806d-310">Weitere Informationen zu dieser Eigenschaft finden Sie weiter unten in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="4806d-310">See the description later in this topic for more information about this property.</span></span>  <br/> |
   
<span data-ttu-id="4806d-311">PR_NICK_NAME_WEIGHT</span><span class="sxs-lookup"><span data-stu-id="4806d-311">PR_NICK_NAME_WEIGHT</span></span>
  
<span data-ttu-id="4806d-312">Der Zeilensatz dieses Streams für automatisches Vervollständigen ist in absteigender Reihenfolge nach der Eigenschaft PR_NICK_NAME_WEIGHT sortiert, und der Stream für automatisches Vervollständigen sollte dieses Sortierverhalten immer beibehalten.</span><span class="sxs-lookup"><span data-stu-id="4806d-312">The set of rows in the autocomplete stream is sorted in descending order by the PR_NICK_NAME_WEIGHT property and the autocomplete stream should always preserve this sorted characteristic.</span></span> <span data-ttu-id="4806d-313">Aus diesem Grund sollte bei Änderungen an der Gewichtung einer Zeile sichergestellt werden, dass die Position der Zeile die Sortierreihenfolge des kompletten Zeilensatzes beibehält.</span><span class="sxs-lookup"><span data-stu-id="4806d-313">Therefore, any changes to a row's weight should also ensure that the row's position maintains the sorted order of the complete set of rows.</span></span> <span data-ttu-id="4806d-314">Zusätze zum Zeilensatz sollten an der richtigen Stelle eingefügt werden, um die Sortierreihenfolge beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="4806d-314">Any additions to the row-set should be inserted to the correct position to maintain the sorted order.</span></span>
  
<span data-ttu-id="4806d-315">Der Mindestwert für diese Gewichtung ist 0x1, und der Maximalwert beträgt LONG_MAX.</span><span class="sxs-lookup"><span data-stu-id="4806d-315">The minimum value of this weight is 0x1 and the maximum value is LONG_MAX.</span></span> <span data-ttu-id="4806d-316">Alle anderen Werte für die Gewichtung werden als ungültig betrachtet.</span><span class="sxs-lookup"><span data-stu-id="4806d-316">Any other values for the weight are considered invalid.</span></span>
  
<span data-ttu-id="4806d-317">Wenn Outlook 2007 eine E-Mail an einen Empfänger versendet oder einen Empfänger auflöst, wird die Gewichtung dieses Empfängers um 0x2000 erhöht.</span><span class="sxs-lookup"><span data-stu-id="4806d-317">When Outlook 2007 sends a mail to or resolves a recipient, it will increase that recipient's weight by 0x2000.</span></span>
  

