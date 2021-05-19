---
title: Stream für automatisches Vervollständigen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: d4f380fa-2ed9-4c7c-9ef3-b32f8409f657
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: aadfba3e2674c35019a2e5f3eb374fbed1ad2a75
ms.sourcegitcommit: 0419850d5c1b3439d9da59070201fb4952ca5d07
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/28/2020
ms.locfileid: "49734224"
---
# <a name="autocomplete-stream"></a><span data-ttu-id="b93f8-103">Stream für automatisches Vervollständigen</span><span class="sxs-lookup"><span data-stu-id="b93f8-103">Autocomplete Stream</span></span>

  
  
<span data-ttu-id="b93f8-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b93f8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b93f8-105">Sie müssen nicht nur wissen, wie Microsoft Outlook mit dem Stream für automatisches Vervollständigen interagiert, sondern auch das Binärformat von AutoVervollständigen verstehen.</span><span class="sxs-lookup"><span data-stu-id="b93f8-105">In addition to knowing how Microsoft Outlook interacts with the autocomplete stream, you must also understand the binary format of the autocomplete stream.</span></span>
  
<span data-ttu-id="b93f8-106">Der Stream für automatisches Vervollständigen besteht aus mehreren Zeilen mit Empfänger-Eigenschaften, die als binärer Stream zusammen mit einigen Verwaltungsmetadaten gespeichert und nur von Microsoft Outlook 2013, Microsoft Outlook 2010, Microsoft Office Outlook 2007 und Microsoft Outlook 2003 verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b93f8-106">The autocomplete stream is a set of recipient property rows that are saved as a binary stream together with some bookkeeping metadata that is used only by Microsoft Outlook 2013, Microsoft Outlook 2010, Microsoft Office Outlook 2007, and Microsoft Outlook 2003.</span></span> <span data-ttu-id="b93f8-107">Die Metadaten sind relevant für Outlook-Interaktionen mit dem Stream für automatisches Vervollständigen, sodass Dritte die Inhalte jedes Metadatenblocks beibehalten müssen, wenn sie einen geänderten Stream für automatisches Vervollständigen speichern.</span><span class="sxs-lookup"><span data-stu-id="b93f8-107">The metadata is relevant to Outlook interactions with the autocomplete stream so third parties must preserve what is in each metadata block when they save a modified autocomplete stream.</span></span> <span data-ttu-id="b93f8-108">Dritte sollten also nur den Zeilensatz des Binärformats ändern und die Inhalte der Metadatenblöcke des Streams für automatisches Vervollständigen beibehalten.</span><span class="sxs-lookup"><span data-stu-id="b93f8-108">In other words, third parties should modify only the row-set part of the binary format and preserve what was already in the metadata blocks of the autocomplete stream.</span></span>
  
## <a name="stream-visualization"></a><span data-ttu-id="b93f8-109">Stream-Visualisierung</span><span class="sxs-lookup"><span data-stu-id="b93f8-109">Stream Visualization</span></span>

<span data-ttu-id="b93f8-110">Das allgemeine Layout des Streams für automatisches Vervollständigen lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="b93f8-110">The high-level layout of the autocomplete stream is as follows:</span></span>
  
<span data-ttu-id="b93f8-111">Metadaten (4 Bytes)</span><span class="sxs-lookup"><span data-stu-id="b93f8-111">Metadata (4 bytes)</span></span>
  
<span data-ttu-id="b93f8-112">Hauptversionsnummer (4 Bytes)</span><span class="sxs-lookup"><span data-stu-id="b93f8-112">Major Version Number (4 bytes)</span></span>
  
<span data-ttu-id="b93f8-113">Nebenversionsnummer (4 Bytes)</span><span class="sxs-lookup"><span data-stu-id="b93f8-113">Minor Version Number (4 bytes)</span></span>
  
<span data-ttu-id="b93f8-114">Anzahl der Zeilen n (4 Bytes)</span><span class="sxs-lookup"><span data-stu-id="b93f8-114">Number of rows n (4 bytes)</span></span>
  
<span data-ttu-id="b93f8-115">Anzahl der Eigenschaften p in der ersten Zeile (4 Bytes)</span><span class="sxs-lookup"><span data-stu-id="b93f8-115">Number of properties p in row one (4 bytes)</span></span>
  
<span data-ttu-id="b93f8-116">Tag der Eigenschaft 1 (4 Bytes)</span><span class="sxs-lookup"><span data-stu-id="b93f8-116">Property 1's property tag (4 bytes)</span></span>
  
<span data-ttu-id="b93f8-117">Reservierte Daten der Eigenschaft 1 (4 Bytes)</span><span class="sxs-lookup"><span data-stu-id="b93f8-117">Property 1's reserved data (4 bytes)</span></span>
  
<span data-ttu-id="b93f8-118">Wertvereinigung der Eigenschaft 1 (8 Bytes)</span><span class="sxs-lookup"><span data-stu-id="b93f8-118">Property 1's value union (8 bytes)</span></span>
  
<span data-ttu-id="b93f8-119">Wertdaten der Eigenschaft 1 (0 oder variable Bytes)</span><span class="sxs-lookup"><span data-stu-id="b93f8-119">Property 1's value data (0 or variable bytes)</span></span>
  
<span data-ttu-id="b93f8-120">…</span><span class="sxs-lookup"><span data-stu-id="b93f8-120">…</span></span> <span data-ttu-id="b93f8-121">(Eigenschaft 2 bis Eigenschaft P-1)</span><span class="sxs-lookup"><span data-stu-id="b93f8-121">(property 2 through property P-1)</span></span>
  
<span data-ttu-id="b93f8-122">Tag der Eigenschaft p (4 Bytes)</span><span class="sxs-lookup"><span data-stu-id="b93f8-122">Property p's property tag (4 bytes)</span></span>
  
<span data-ttu-id="b93f8-123">Reservierte Daten der Eigenschaft p (4 Bytes)</span><span class="sxs-lookup"><span data-stu-id="b93f8-123">Property p's reserved data (4 bytes)</span></span>
  
<span data-ttu-id="b93f8-124">Wertvereinigung der Eigenschaft p (8 Bytes)</span><span class="sxs-lookup"><span data-stu-id="b93f8-124">Property p's value union (8 bytes)</span></span>
  
<span data-ttu-id="b93f8-125">Wertdaten der Eigenschaft p (0 oder variable Bytes)</span><span class="sxs-lookup"><span data-stu-id="b93f8-125">Property p's value data (0 or variable bytes)</span></span>
  
<span data-ttu-id="b93f8-126">Anzahl der Eigenschaften q in der zweiten Zeile (4 Bytes)</span><span class="sxs-lookup"><span data-stu-id="b93f8-126">Number of properties q in row two (4 bytes)</span></span>
  
<span data-ttu-id="b93f8-127">…</span><span class="sxs-lookup"><span data-stu-id="b93f8-127">…</span></span> <span data-ttu-id="b93f8-128">(Eigenschaften der zweiten Zeile)</span><span class="sxs-lookup"><span data-stu-id="b93f8-128">(row two's properties)</span></span>
  
<span data-ttu-id="b93f8-129">…</span><span class="sxs-lookup"><span data-stu-id="b93f8-129">…</span></span> <span data-ttu-id="b93f8-130">(Zeile 3 bis Zeile n-1)</span><span class="sxs-lookup"><span data-stu-id="b93f8-130">(row 3 through row n-1)</span></span>
  
<span data-ttu-id="b93f8-131">Anzahl der Eigenschaften r in Zeile n (4 Bytes)</span><span class="sxs-lookup"><span data-stu-id="b93f8-131">Number of properties r in row n (4 bytes)</span></span>
  
<span data-ttu-id="b93f8-132">…</span><span class="sxs-lookup"><span data-stu-id="b93f8-132">…</span></span> <span data-ttu-id="b93f8-133">(Eigenschaften der Zeile n)</span><span class="sxs-lookup"><span data-stu-id="b93f8-133">(row n's properties)</span></span>
  
<span data-ttu-id="b93f8-134">Zusätzliche Informationen Byteanzahl EI (4 Bytes)</span><span class="sxs-lookup"><span data-stu-id="b93f8-134">Extra information byte count EI (4 bytes)</span></span>
  
<span data-ttu-id="b93f8-135">Zusätzliche Informationen (EI-Bytes)</span><span class="sxs-lookup"><span data-stu-id="b93f8-135">Extra information (EI bytes)</span></span>
  
<span data-ttu-id="b93f8-136">Metadaten (8 Bytes)</span><span class="sxs-lookup"><span data-stu-id="b93f8-136">Metadata (8 bytes)</span></span>
  
<span data-ttu-id="b93f8-137">Ein Beispiel für eine binäre Struktur finden Sie im Binärbeispiel in den [Outlook 2003/2007 NK2-Dateiformat- und Entwicklerrichtlinien.](https://portalvhds6gyn3khqwmgzd.blob.core.windows.net/files/NK2/NK2WithBinaryExample.pdf)</span><span class="sxs-lookup"><span data-stu-id="b93f8-137">For an example of a binary structure, see Binary Example in the [Outlook 2003/2007 NK2 File Format and Developer Guidelines.](https://portalvhds6gyn3khqwmgzd.blob.core.windows.net/files/NK2/NK2WithBinaryExample.pdf)</span></span>
  
## <a name="high-level-layout"></a><span data-ttu-id="b93f8-138">Allgemeines Layout</span><span class="sxs-lookup"><span data-stu-id="b93f8-138">High-level Layout</span></span>

<span data-ttu-id="b93f8-139">Das allgemeine Layout des Streams für automatisches Vervollständigen lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="b93f8-139">Broadly speaking, the layout of the autocomplete stream is as follows:</span></span>
  
|<span data-ttu-id="b93f8-140">**Wertdaten**</span><span class="sxs-lookup"><span data-stu-id="b93f8-140">**Value Data**</span></span>|<span data-ttu-id="b93f8-141">**Anzahl der Bytes**</span><span class="sxs-lookup"><span data-stu-id="b93f8-141">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b93f8-142">Metadaten</span><span class="sxs-lookup"><span data-stu-id="b93f8-142">Metadata</span></span>  <br/> |<span data-ttu-id="b93f8-143">4 </span><span class="sxs-lookup"><span data-stu-id="b93f8-143">4</span></span>  <br/> |
|<span data-ttu-id="b93f8-144">Nummer der Hauptversion</span><span class="sxs-lookup"><span data-stu-id="b93f8-144">Major Version Number</span></span>  <br/> |<span data-ttu-id="b93f8-145">4 </span><span class="sxs-lookup"><span data-stu-id="b93f8-145">4</span></span>  <br/> |
|<span data-ttu-id="b93f8-146">Nummer der Nebenversion</span><span class="sxs-lookup"><span data-stu-id="b93f8-146">Minor Version Number</span></span>  <br/> |<span data-ttu-id="b93f8-147">4 </span><span class="sxs-lookup"><span data-stu-id="b93f8-147">4</span></span>  <br/> |
|<span data-ttu-id="b93f8-148">Zeilensatz</span><span class="sxs-lookup"><span data-stu-id="b93f8-148">Row-set</span></span>  <br/> |<span data-ttu-id="b93f8-149">Variable</span><span class="sxs-lookup"><span data-stu-id="b93f8-149">Variable</span></span>  <br/> |
|<span data-ttu-id="b93f8-150">Zusätzliche Informationen Byteanzahl EI</span><span class="sxs-lookup"><span data-stu-id="b93f8-150">Extra information byte count EI</span></span>  <br/> |<span data-ttu-id="b93f8-151">4 </span><span class="sxs-lookup"><span data-stu-id="b93f8-151">4</span></span>  <br/> |
|<span data-ttu-id="b93f8-152">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="b93f8-152">Extra information</span></span>  <br/> |<span data-ttu-id="b93f8-153">EI</span><span class="sxs-lookup"><span data-stu-id="b93f8-153">EI</span></span>  <br/> |
|<span data-ttu-id="b93f8-154">Metadaten</span><span class="sxs-lookup"><span data-stu-id="b93f8-154">Metadata</span></span>  <br/> |<span data-ttu-id="b93f8-155">8 </span><span class="sxs-lookup"><span data-stu-id="b93f8-155">8</span></span>  <br/> |
   
<span data-ttu-id="b93f8-156">Wenn die Hauptversion nicht 12, sollte dieser Datenstrom nicht gelesen oder geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="b93f8-156">When reading this stream, if the major version is different than 12, then this stream should not be read or written.</span></span> <span data-ttu-id="b93f8-157">Die aktuelle Nebenversion des Streams für automatisches Vervollständigen ist 0, d. h. die Bytes für die zusätzlichen Informationen sind auf "0" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b93f8-157">The current minor version of the autocomplete stream is 0, which has the Extra Information Byte count set to 0.</span></span> <span data-ttu-id="b93f8-158">Wenn die Nebenversion nicht 0 ist, befinden sich Informationen in den zusätzlichen Informationen, die beim Lesen des Streams gelesen und beim Schreiben des Streams beibehalten werden müssen.</span><span class="sxs-lookup"><span data-stu-id="b93f8-158">If the minor version is different than 0, then there will be information in the extra information that needs to be read when reading the stream and preserved when writing the stream.</span></span> <span data-ttu-id="b93f8-159">Die Nebenversion muss auch beim Schreiben des Streams beibehalten werden.</span><span class="sxs-lookup"><span data-stu-id="b93f8-159">The minor version will also need to be preserved when writing the stream.</span></span> <span data-ttu-id="b93f8-160">Wenn beide nicht beibehalten werden, verlieren Instanzen von Outlook, die die zusätzlichen Informationen schreiben, Daten.</span><span class="sxs-lookup"><span data-stu-id="b93f8-160">If both of these are not preserved, instances of Outlook that wrote the extra information will lose data.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="b93f8-161">Anwendungen dürfen keine benutzerdefinierten Daten zum Feld Zusätzliche Informationen hinzufügen und nicht die Nebenversion ändern, da diese Funktion Outlook-Erweiterungen des Formats und keine beliebigen Erweiterungen von Drittanbietern unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b93f8-161">Applications must not add custom data to the Extra Information field or change the minor version as this functionality is to support Outlook extensions to the format and not arbitrary third-party extensions.</span></span> 
  
## <a name="row-set-layout"></a><span data-ttu-id="b93f8-162">Zeilensatz-Layout</span><span class="sxs-lookup"><span data-stu-id="b93f8-162">Row-set Layout</span></span>

<span data-ttu-id="b93f8-163">Das Zeilensatz-Layout lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="b93f8-163">The row-set layout is as follows:</span></span> 
  
|<span data-ttu-id="b93f8-164">**Wertdaten**</span><span class="sxs-lookup"><span data-stu-id="b93f8-164">**Value Data**</span></span>|<span data-ttu-id="b93f8-165">**Anzahl der Bytes**</span><span class="sxs-lookup"><span data-stu-id="b93f8-165">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b93f8-166">Anzahl der Zeilen</span><span class="sxs-lookup"><span data-stu-id="b93f8-166">Number of rows</span></span>  <br/> |<span data-ttu-id="b93f8-167">4 </span><span class="sxs-lookup"><span data-stu-id="b93f8-167">4</span></span>  <br/> |
|<span data-ttu-id="b93f8-168">Zeilen</span><span class="sxs-lookup"><span data-stu-id="b93f8-168">Rows</span></span>  <br/> |<span data-ttu-id="b93f8-169">Variable</span><span class="sxs-lookup"><span data-stu-id="b93f8-169">Variable</span></span>  <br/> |
   
<span data-ttu-id="b93f8-170">Die Anzahl der Zeilen gibt an, wie viele Zeilen im nächsten Teil der binären Datenstromsequenz enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="b93f8-170">The number of rows identifies how many rows come in the next part of the binary stream sequence.</span></span>
  
## <a name="row-layout"></a><span data-ttu-id="b93f8-171">Zeilen-Layout</span><span class="sxs-lookup"><span data-stu-id="b93f8-171">Row Layout</span></span>

<span data-ttu-id="b93f8-172">Jede Zeile besitzt das folgende Format:</span><span class="sxs-lookup"><span data-stu-id="b93f8-172">Each row is of the following format:</span></span>
  
|<span data-ttu-id="b93f8-173">**Wertdaten**</span><span class="sxs-lookup"><span data-stu-id="b93f8-173">**Value Data**</span></span>|<span data-ttu-id="b93f8-174">**Anzahl der Bytes**</span><span class="sxs-lookup"><span data-stu-id="b93f8-174">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b93f8-175">Anzahl der Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b93f8-175">Number of properties</span></span>  <br/> |<span data-ttu-id="b93f8-176">4 </span><span class="sxs-lookup"><span data-stu-id="b93f8-176">4</span></span>  <br/> |
|<span data-ttu-id="b93f8-177">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b93f8-177">Properties</span></span>  <br/> |<span data-ttu-id="b93f8-178">Variable</span><span class="sxs-lookup"><span data-stu-id="b93f8-178">Variable</span></span>  <br/> |
   
<span data-ttu-id="b93f8-179">Die Anzahl der Eigenschaften gibt an, wie viele Eigenschaften im nächsten Teil der binären Datenstromsequenz enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="b93f8-179">The number of properties identifies how many properties come in the next part of the binary stream sequence.</span></span>
  
## <a name="property-layout"></a><span data-ttu-id="b93f8-180">Eigenschaften-Layout</span><span class="sxs-lookup"><span data-stu-id="b93f8-180">Property Layout</span></span>

<span data-ttu-id="b93f8-181">Jede Eigenschaft besitzt das folgende Format:</span><span class="sxs-lookup"><span data-stu-id="b93f8-181">Each property is of the following format:</span></span>
  
|<span data-ttu-id="b93f8-182">**Wertdaten**</span><span class="sxs-lookup"><span data-stu-id="b93f8-182">**Value Data**</span></span>|<span data-ttu-id="b93f8-183">**Anzahl der Bytes**</span><span class="sxs-lookup"><span data-stu-id="b93f8-183">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b93f8-184">Tag der Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="b93f8-184">Property Tag</span></span>  <br/> |<span data-ttu-id="b93f8-185">4 </span><span class="sxs-lookup"><span data-stu-id="b93f8-185">4</span></span>  <br/> |
|<span data-ttu-id="b93f8-186">Reservierte Daten</span><span class="sxs-lookup"><span data-stu-id="b93f8-186">Reserved Data</span></span>  <br/> |<span data-ttu-id="b93f8-187">4 </span><span class="sxs-lookup"><span data-stu-id="b93f8-187">4</span></span>  <br/> |
|<span data-ttu-id="b93f8-188">Eigenschaftswertvereinigung</span><span class="sxs-lookup"><span data-stu-id="b93f8-188">Property Value Union</span></span>  <br/> ||
|<span data-ttu-id="b93f8-189">Wertdaten</span><span class="sxs-lookup"><span data-stu-id="b93f8-189">Value Data</span></span>  <br/> |<span data-ttu-id="b93f8-190">0 oder Variable (abhängig vom Tag der Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="b93f8-190">0 or variable (depending on the prop tag)</span></span>  <br/> |
   
## <a name="interpreting-the-property-value"></a><span data-ttu-id="b93f8-191">Interpretation des Eigenschaftswerts</span><span class="sxs-lookup"><span data-stu-id="b93f8-191">Interpreting the Property Value</span></span>

<span data-ttu-id="b93f8-192">Die Eigenschaftswertvereinigung und die Wertdaten werden basierend auf dem Tag der Eigenschaft in den ersten 4 Bytes des Eigenschaftsblocks interpretiert.</span><span class="sxs-lookup"><span data-stu-id="b93f8-192">The Property Value Union and the Value Data are to be interpreted based on the property tag in the first 4 bytes of the property block.</span></span> <span data-ttu-id="b93f8-193">Das Tag der Eigenschaft liegt im selben Format vor wie das Tag der MAPI-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="b93f8-193">This property tag is in the same format as a MAPI property tag.</span></span> <span data-ttu-id="b93f8-194">Die Bits 0 bis 15 des Tags der Eigenschaft geben den Typ der Eigenschaft an.</span><span class="sxs-lookup"><span data-stu-id="b93f8-194">Bits 0 through 15 of the property tag are the property's type.</span></span> <span data-ttu-id="b93f8-195">Die Bits 16 bis 31 sind Bezeichner der Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="b93f8-195">Bits 16 through 31 are the property's identifier.</span></span> <span data-ttu-id="b93f8-196">Der Eigenschaftentyp bestimmt, wie der Rest der Eigenschaft gelesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="b93f8-196">The property type determines how the rest of the property should be read.</span></span>
  
## <a name="static-value"></a><span data-ttu-id="b93f8-197">Statischer Wert</span><span class="sxs-lookup"><span data-stu-id="b93f8-197">Static Value</span></span>

<span data-ttu-id="b93f8-198">Einige Eigenschaften besitzen keine Wertdaten und verfügen nur in der Vereinigung über Daten.</span><span class="sxs-lookup"><span data-stu-id="b93f8-198">Some properties have no Value Data and only have data in the union.</span></span> <span data-ttu-id="b93f8-199">Die folgenden Eigenschaftstypen (die aus dem Eigenschafts-Tag stammen) sollten die 8 Byte Daten der Eigenschaftsvereinigung wie folgt interpretieren:</span><span class="sxs-lookup"><span data-stu-id="b93f8-199">The following property types (which come from the Property Tag) should interpret the 8-byte Property Union data as follows:</span></span>
  
|<span data-ttu-id="b93f8-200">**Eigenschaftstyp**</span><span class="sxs-lookup"><span data-stu-id="b93f8-200">**Prop Type**</span></span>|<span data-ttu-id="b93f8-201">**Interpretation der Eigenschaftsvereinigung**</span><span class="sxs-lookup"><span data-stu-id="b93f8-201">**Property Union Interpretation**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b93f8-202">PT_I2</span><span class="sxs-lookup"><span data-stu-id="b93f8-202">PT_I2</span></span>  <br/> |<span data-ttu-id="b93f8-203">short int</span><span class="sxs-lookup"><span data-stu-id="b93f8-203">short int</span></span>  <br/> |
|<span data-ttu-id="b93f8-204">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="b93f8-204">PT_LONG</span></span>  <br/> |<span data-ttu-id="b93f8-205">long</span><span class="sxs-lookup"><span data-stu-id="b93f8-205">long</span></span>  <br/> |
|<span data-ttu-id="b93f8-206">PT_ERROR</span><span class="sxs-lookup"><span data-stu-id="b93f8-206">PT_ERROR</span></span>  <br/> |<span data-ttu-id="b93f8-207">long</span><span class="sxs-lookup"><span data-stu-id="b93f8-207">long</span></span>  <br/> |
|<span data-ttu-id="b93f8-208">PT_R4</span><span class="sxs-lookup"><span data-stu-id="b93f8-208">PT_R4</span></span>  <br/> |<span data-ttu-id="b93f8-209">float</span><span class="sxs-lookup"><span data-stu-id="b93f8-209">float</span></span>  <br/> |
|<span data-ttu-id="b93f8-210">PT_DOUBLE</span><span class="sxs-lookup"><span data-stu-id="b93f8-210">PT_DOUBLE</span></span>  <br/> |<span data-ttu-id="b93f8-211">double</span><span class="sxs-lookup"><span data-stu-id="b93f8-211">double</span></span>  <br/> |
|<span data-ttu-id="b93f8-212">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="b93f8-212">PT_BOOLEAN</span></span>  <br/> |<span data-ttu-id="b93f8-213">short int</span><span class="sxs-lookup"><span data-stu-id="b93f8-213">short int</span></span>  <br/> |
|<span data-ttu-id="b93f8-214">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="b93f8-214">PT_SYSTIME</span></span>  <br/> |<span data-ttu-id="b93f8-215">FILETIME</span><span class="sxs-lookup"><span data-stu-id="b93f8-215">FILETIME</span></span>  <br/> |
|<span data-ttu-id="b93f8-216">PT_I8</span><span class="sxs-lookup"><span data-stu-id="b93f8-216">PT_I8</span></span>  <br/> |<span data-ttu-id="b93f8-217">LARGE_INTEGER</span><span class="sxs-lookup"><span data-stu-id="b93f8-217">LARGE_INTEGER</span></span>  <br/> |
   
## <a name="dynamic-values"></a><span data-ttu-id="b93f8-218">Dynamische Werte</span><span class="sxs-lookup"><span data-stu-id="b93f8-218">Dynamic Values</span></span>

<span data-ttu-id="b93f8-219">Andere Eigenschaften weisen nach den 16 Bytes Daten in einem Wertdatenblock auf, die das Tag der Eigenschaft, die Reservierten Daten und die Eigenschaftswertvereinigung enthalten.</span><span class="sxs-lookup"><span data-stu-id="b93f8-219">Other properties have data in a Value Data block after the first 16 bytes that contain the Property Tag, the Reserved Data, and the Property Value Union.</span></span> <span data-ttu-id="b93f8-220">Im Gegensatz zu statischen Werten sind die Daten, die in der 8-Byte-Eigenschaftswertvereinigung gespeichert sind, irrelevant für das Lesen.</span><span class="sxs-lookup"><span data-stu-id="b93f8-220">Unlike static values, the data that is stored in the 8-byte Property Value union is irrelevant on reading.</span></span> <span data-ttu-id="b93f8-221">Stellen Sie beim Schreiben sicher, dass die 8 Bytes mit Werten gefüllt werden.</span><span class="sxs-lookup"><span data-stu-id="b93f8-221">When writing, make sure that you fill these 8 bytes with something.</span></span> <span data-ttu-id="b93f8-222">Der Inhalt der 8 Bytes ist jedoch nicht wichtig.</span><span class="sxs-lookup"><span data-stu-id="b93f8-222">However, the content of the 8 bytes is not important.</span></span> <span data-ttu-id="b93f8-223">Bei dynamischen Werten bestimmt der Tagtyp der Eigenschaft die Interpretation der Wertdaten.</span><span class="sxs-lookup"><span data-stu-id="b93f8-223">In dynamic values, the property tag's type determines how to interpret the Value Data.</span></span>
  
<span data-ttu-id="b93f8-224">PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="b93f8-224">PT_STRING8</span></span> 
  
|<span data-ttu-id="b93f8-225">**Wertdaten**</span><span class="sxs-lookup"><span data-stu-id="b93f8-225">**Value Data**</span></span>|<span data-ttu-id="b93f8-226">**Anzahl der Bytes**</span><span class="sxs-lookup"><span data-stu-id="b93f8-226">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b93f8-227">Anzahl der Bytes n</span><span class="sxs-lookup"><span data-stu-id="b93f8-227">Number of bytes n</span></span>  <br/> |<span data-ttu-id="b93f8-228">4 </span><span class="sxs-lookup"><span data-stu-id="b93f8-228">4</span></span>  <br/> |
|<span data-ttu-id="b93f8-229">Bytes werden als ANSI-Zeichenfolge interpretiert (beinhaltet NULL-Abschlusszeichen)</span><span class="sxs-lookup"><span data-stu-id="b93f8-229">Bytes to be interpreted as an ANSI string (includes NULL terminator)</span></span>  <br/> |<span data-ttu-id="b93f8-230">n</span><span class="sxs-lookup"><span data-stu-id="b93f8-230">n</span></span>  <br/> |
   
<span data-ttu-id="b93f8-231">PT_CLSID</span><span class="sxs-lookup"><span data-stu-id="b93f8-231">PT_CLSID</span></span>
  
|<span data-ttu-id="b93f8-232">**Wertdaten**</span><span class="sxs-lookup"><span data-stu-id="b93f8-232">**Value Data**</span></span>|<span data-ttu-id="b93f8-233">**Anzahl der Bytes**</span><span class="sxs-lookup"><span data-stu-id="b93f8-233">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b93f8-234">Bytes, die als GUID interpretiert werden</span><span class="sxs-lookup"><span data-stu-id="b93f8-234">Bytes to be interpreted as a GUID</span></span>  <br/> |<span data-ttu-id="b93f8-235">16 </span><span class="sxs-lookup"><span data-stu-id="b93f8-235">16</span></span>  <br/> |
|||
   
<span data-ttu-id="b93f8-236">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="b93f8-236">PT_BINARY</span></span> 
  
|<span data-ttu-id="b93f8-237">**Wertdaten**</span><span class="sxs-lookup"><span data-stu-id="b93f8-237">**Value Data**</span></span>|<span data-ttu-id="b93f8-238">**Anzahl der Bytes**</span><span class="sxs-lookup"><span data-stu-id="b93f8-238">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b93f8-239">Anzahl der Bytes n</span><span class="sxs-lookup"><span data-stu-id="b93f8-239">Number of bytes n</span></span>  <br/> |<span data-ttu-id="b93f8-240">4 </span><span class="sxs-lookup"><span data-stu-id="b93f8-240">4</span></span>  <br/> |
|<span data-ttu-id="b93f8-241">Bytes, die als Byte-Array interpretiert werden</span><span class="sxs-lookup"><span data-stu-id="b93f8-241">Bytes to be interpreted as a byte array</span></span>  <br/> |<span data-ttu-id="b93f8-242">n</span><span class="sxs-lookup"><span data-stu-id="b93f8-242">n</span></span>  <br/> |
   
<span data-ttu-id="b93f8-243">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="b93f8-243">PT_MV_BINARY</span></span>
  
|<span data-ttu-id="b93f8-244">**Wertdaten**</span><span class="sxs-lookup"><span data-stu-id="b93f8-244">**Value Data**</span></span>|<span data-ttu-id="b93f8-245">**Anzahl der Bytes**</span><span class="sxs-lookup"><span data-stu-id="b93f8-245">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b93f8-246">Anzahl der binären Arrays X</span><span class="sxs-lookup"><span data-stu-id="b93f8-246">Number of binary arrays X</span></span>  <br/> |<span data-ttu-id="b93f8-247">4 </span><span class="sxs-lookup"><span data-stu-id="b93f8-247">4</span></span>  <br/> |
|<span data-ttu-id="b93f8-248">Eine Ausführung von Bytes, die X binäre Arrays enthält.</span><span class="sxs-lookup"><span data-stu-id="b93f8-248">A run of bytes that contains X binary arrays.</span></span> <span data-ttu-id="b93f8-249">Jedes Array sollten exakt wie die PT_BINARY-Byte-Ausführung interpretiert werden.</span><span class="sxs-lookup"><span data-stu-id="b93f8-249">Each array should be interpreted exactly like the PT_BINARY byte run.</span></span>  <br/> |<span data-ttu-id="b93f8-250">Variable</span><span class="sxs-lookup"><span data-stu-id="b93f8-250">Variable</span></span>  <br/> |
   
<span data-ttu-id="b93f8-251">PT_MV_STRING8 (Outlook 2007, Outlook 2010, and Outlook 2013)</span><span class="sxs-lookup"><span data-stu-id="b93f8-251">PT_MV_STRING8 (Outlook 2007, Outlook 2010, and Outlook 2013)</span></span>
  
|<span data-ttu-id="b93f8-252">**Wertdaten**</span><span class="sxs-lookup"><span data-stu-id="b93f8-252">**Value Data**</span></span>|<span data-ttu-id="b93f8-253">**Anzahl der Bytes**</span><span class="sxs-lookup"><span data-stu-id="b93f8-253">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b93f8-254">Anzahl der ANSI-Zeichenfolgen X</span><span class="sxs-lookup"><span data-stu-id="b93f8-254">Number of ANSI strings X</span></span>  <br/> |<span data-ttu-id="b93f8-255">4 </span><span class="sxs-lookup"><span data-stu-id="b93f8-255">4</span></span>  <br/> |
|<span data-ttu-id="b93f8-256">Eine Ausführung von Bytes, die X ANSI-Zeichenfolgen enthält.</span><span class="sxs-lookup"><span data-stu-id="b93f8-256">A run of bytes that contains X ANSI strings.</span></span> <span data-ttu-id="b93f8-257">Jede Zeichenfolge sollte exakt wie die PT_STRING8-Byte-Ausführung interpretiert werden.</span><span class="sxs-lookup"><span data-stu-id="b93f8-257">Each string should be interpreted exactly like the PT_STRING8 byte run.</span></span>  <br/> |<span data-ttu-id="b93f8-258">Variable</span><span class="sxs-lookup"><span data-stu-id="b93f8-258">Variable</span></span>  <br/> |
   
<span data-ttu-id="b93f8-259">PT_MV_UNICODE (Outlook 2007, Outlook 2010, Outlook 2013)</span><span class="sxs-lookup"><span data-stu-id="b93f8-259">PT_MV_UNICODE (Outlook 2007, Outlook 2010, Outlook 2013)</span></span>
  
|<span data-ttu-id="b93f8-260">**Wertdaten**</span><span class="sxs-lookup"><span data-stu-id="b93f8-260">**Value Data**</span></span>|<span data-ttu-id="b93f8-261">**Anzahl der Bytes**</span><span class="sxs-lookup"><span data-stu-id="b93f8-261">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b93f8-262">Anzahl der Unicode-Zeichenfolgen X</span><span class="sxs-lookup"><span data-stu-id="b93f8-262">Number of UNICODE strings X</span></span>  <br/> |<span data-ttu-id="b93f8-263">4 </span><span class="sxs-lookup"><span data-stu-id="b93f8-263">4</span></span>  <br/> |
|<span data-ttu-id="b93f8-264">Eine Ausführung von Bytes, die X UNICODE-Zeichenfolgen enthält.</span><span class="sxs-lookup"><span data-stu-id="b93f8-264">A run of bytes that contains X UNICODE strings.</span></span> <span data-ttu-id="b93f8-265">Jede Zeichenfolge sollte exakt wie die PT_UNICODE-Byte-Ausführung interpretiert werden.</span><span class="sxs-lookup"><span data-stu-id="b93f8-265">Each string should be interpreted exactly like the PT_UNICODE byte run.</span></span>  <br/> |<span data-ttu-id="b93f8-266">Variable</span><span class="sxs-lookup"><span data-stu-id="b93f8-266">Variable</span></span>  <br/> |
   
## <a name="significant-properties"></a><span data-ttu-id="b93f8-267">Wesentliche Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b93f8-267">Significant properties</span></span>

<span data-ttu-id="b93f8-268">Wie zuvor in diesem Artikel erwähnt, besitzen die binären Blöcke, die Eigenschaften darstellen, Eigenschafts-Tags, die Eigenschaften von Adressbuchempfängern entsprechen.</span><span class="sxs-lookup"><span data-stu-id="b93f8-268">As mentioned previously in this topic, the binary blocks that represent properties have property tags that correspond to properties on address book recipients.</span></span> <span data-ttu-id="b93f8-269">Eine Beschreibung der Eigenschaften, die hier nicht aufgeführt sind, finden Sie unter https://msdn.microsoft.com/library/cc433490(EXCHG.80).aspx.</span><span class="sxs-lookup"><span data-stu-id="b93f8-269">For properties that are not listed here, you can look up the property description at https://msdn.microsoft.com/library/cc433490(EXCHG.80).aspx.</span></span>
  
|<span data-ttu-id="b93f8-270">**Eigenschaftsname**</span><span class="sxs-lookup"><span data-stu-id="b93f8-270">**Property Name**</span></span>|<span data-ttu-id="b93f8-271">**Eigenschafts-Tag**</span><span class="sxs-lookup"><span data-stu-id="b93f8-271">**Property Tag**</span></span>|<span data-ttu-id="b93f8-272">**Beschreibung (weitere Informationen finden Sie unter MSDN)**</span><span class="sxs-lookup"><span data-stu-id="b93f8-272">**Description (see MSDN for more information)**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b93f8-273">PR_NICK_NAME_W (nicht auf Empfänger übertragen, spezifisch für den Stream für automatisches Vervollständigen)</span><span class="sxs-lookup"><span data-stu-id="b93f8-273">PR_NICK_NAME_W (not transmitted on recipients, specific to autocomplete stream only)</span></span>  <br/> |<span data-ttu-id="b93f8-274">0x6001001f</span><span class="sxs-lookup"><span data-stu-id="b93f8-274">0x6001001f</span></span>  <br/> |<span data-ttu-id="b93f8-275">Diese Eigenschaft muss in jeder Empfängerzeile zuerst stehen.</span><span class="sxs-lookup"><span data-stu-id="b93f8-275">This property must be first in each recipient row.</span></span> <span data-ttu-id="b93f8-276">Die Funktion dient als Schlüssel-ID für die Empfängerzeile.</span><span class="sxs-lookup"><span data-stu-id="b93f8-276">It functionally serves as a key identifier for the recipient row.</span></span>  <br/> |
|<span data-ttu-id="b93f8-277">PR_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="b93f8-277">PR_ENTRYID</span></span>  <br/> |<span data-ttu-id="b93f8-278">0x0FFF0102</span><span class="sxs-lookup"><span data-stu-id="b93f8-278">0x0FFF0102</span></span>  <br/> |<span data-ttu-id="b93f8-279">Eintrag-ID des Adressbuchs für den Empfänger</span><span class="sxs-lookup"><span data-stu-id="b93f8-279">The address book entry identifier for the recipient.</span></span>  <br/> |
|<span data-ttu-id="b93f8-280">PR_DISPLAY_NAME_W</span><span class="sxs-lookup"><span data-stu-id="b93f8-280">PR_DISPLAY_NAME_W</span></span>  <br/> |<span data-ttu-id="b93f8-281">0x3001001F</span><span class="sxs-lookup"><span data-stu-id="b93f8-281">0x3001001F</span></span>  <br/> |<span data-ttu-id="b93f8-282">Anzeigename des Empfängers</span><span class="sxs-lookup"><span data-stu-id="b93f8-282">The recipient's display name.</span></span>  <br/> |
|<span data-ttu-id="b93f8-283">PR_EMAIL_ADDRESS_W</span><span class="sxs-lookup"><span data-stu-id="b93f8-283">PR_EMAIL_ADDRESS_W</span></span>  <br/> |<span data-ttu-id="b93f8-284">0x3003001F</span><span class="sxs-lookup"><span data-stu-id="b93f8-284">0x3003001F</span></span>  <br/> |<span data-ttu-id="b93f8-285">E-Mail-Adresse des Empfängers (z. B. johndoe@contoso.com oder /o=Contoso/OU=Foo/cn=Recipients/cn=johndoe)</span><span class="sxs-lookup"><span data-stu-id="b93f8-285">The recipient's email address (e.g. johndoe@contoso.com or /o=Contoso/OU=Foo/cn=Recipients/cn=johndoe)</span></span>  <br/> |
|<span data-ttu-id="b93f8-286">PR_ADDRTYPE_W</span><span class="sxs-lookup"><span data-stu-id="b93f8-286">PR_ADDRTYPE_W</span></span>  <br/> |<span data-ttu-id="b93f8-287">0x3002001F</span><span class="sxs-lookup"><span data-stu-id="b93f8-287">0x3002001F</span></span>  <br/> |<span data-ttu-id="b93f8-288">Adresstyp des Empfängers (z. B. SMTP oder EX).</span><span class="sxs-lookup"><span data-stu-id="b93f8-288">The recipient's address type (e.g. SMTP or EX).</span></span>  <br/> |
|<span data-ttu-id="b93f8-289">PR_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="b93f8-289">PR_SEARCH_KEY</span></span>  <br/> |<span data-ttu-id="b93f8-290">0x300B0102</span><span class="sxs-lookup"><span data-stu-id="b93f8-290">0x300B0102</span></span>  <br/> |<span data-ttu-id="b93f8-291">MAPI-Suchschlüssel des Empfängers</span><span class="sxs-lookup"><span data-stu-id="b93f8-291">The recipient's MAPI search key.</span></span>  <br/> |
|<span data-ttu-id="b93f8-292">PR_SMTP_ADDRESS_W</span><span class="sxs-lookup"><span data-stu-id="b93f8-292">PR_SMTP_ADDRESS_W</span></span>  <br/> |<span data-ttu-id="b93f8-293">0x39FE001f</span><span class="sxs-lookup"><span data-stu-id="b93f8-293">0x39FE001f</span></span>  <br/> |<span data-ttu-id="b93f8-294">SMTP-Adresse des Empfängers</span><span class="sxs-lookup"><span data-stu-id="b93f8-294">The recipient's SMTP address.</span></span>  <br/> |
|<span data-ttu-id="b93f8-295">PR_DROPDOWN_DISPLAY_NAME_W (nicht auf Empfänger übertragen, spezifisch für den Stream für automatisches Vervollständigen)</span><span class="sxs-lookup"><span data-stu-id="b93f8-295">PR_DROPDOWN_DISPLAY_NAME_W (not transmitted on recipients, specific to autocomplete stream only)</span></span>  <br/> |<span data-ttu-id="b93f8-296">0X6003001f</span><span class="sxs-lookup"><span data-stu-id="b93f8-296">0X6003001f</span></span>  <br/> |<span data-ttu-id="b93f8-297">Zeichenfolge, die in der AutoVervollständigen-Liste angezeigt wird</span><span class="sxs-lookup"><span data-stu-id="b93f8-297">The display string that appears in the autocomplete list.</span></span>  <br/> |
|<span data-ttu-id="b93f8-298">PR_NICK_NAME_WEIGHT (nicht auf Empfänger übertragen, spezifisch für den Stream für automatisches Vervollständigen)</span><span class="sxs-lookup"><span data-stu-id="b93f8-298">PR_NICK_NAME_WEIGHT (not transmitted on recipients, specific to autocomplete stream only)</span></span>  <br/> |<span data-ttu-id="b93f8-299">0x60040003</span><span class="sxs-lookup"><span data-stu-id="b93f8-299">0x60040003</span></span>  <br/> |<span data-ttu-id="b93f8-300">Gewichtung dieses AutoVervollständigen-Eintrags</span><span class="sxs-lookup"><span data-stu-id="b93f8-300">The weight of this autocomplete entry.</span></span> <span data-ttu-id="b93f8-301">Mit der Gewichtung wird bestimmt, in welcher Reihenfolge AutoVervollständigen-Einträge beim Abgleich der AutoVervollständigen-Liste ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="b93f8-301">The weight is used to determine in what order autocomplete entries occur when matching the autocomplete list.</span></span> <span data-ttu-id="b93f8-302">Einträge mit höherer Gewichtung werden vor Einträgen mit geringerer Gewichtung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b93f8-302">Entries with higher weight will show before entries with lower weight.</span></span> <span data-ttu-id="b93f8-303">Die komplette AutoVervollständigen-Liste wird nach dieser Eigenschaft sortiert.</span><span class="sxs-lookup"><span data-stu-id="b93f8-303">The complete autocomplete list is sorted by this property.</span></span> <span data-ttu-id="b93f8-304">Die Gewichtung wird in regelmäßigen Abständen über einen Zeitraum verringert und wird vergrößert, wenn der Benutzer eine E-Mail-Nachricht an diesen Empfänger sendet.</span><span class="sxs-lookup"><span data-stu-id="b93f8-304">The weight periodically decreases over time and increases when the user sends an email to this recipient.</span></span> <span data-ttu-id="b93f8-305">Weitere Informationen zu dieser Eigenschaft finden Sie weiter unten in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="b93f8-305">See the description later in this topic for more information about this property.</span></span>  <br/> |
   
<span data-ttu-id="b93f8-306">PR_NICK_NAME_WEIGHT</span><span class="sxs-lookup"><span data-stu-id="b93f8-306">PR_NICK_NAME_WEIGHT</span></span>
  
<span data-ttu-id="b93f8-307">Der Zeilensatz dieses Streams für automatisches Vervollständigen ist in absteigender Reihenfolge nach der Eigenschaft PR_NICK_NAME_WEIGHT sortiert, und der Stream für automatisches Vervollständigen sollte dieses Sortierverhalten immer beibehalten.</span><span class="sxs-lookup"><span data-stu-id="b93f8-307">The set of rows in the autocomplete stream is sorted in descending order by the PR_NICK_NAME_WEIGHT property and the autocomplete stream should always preserve this sorted characteristic.</span></span> <span data-ttu-id="b93f8-308">Aus diesem Grund sollte bei Änderungen an der Gewichtung einer Zeile sichergestellt werden, dass die Position der Zeile die Sortierreihenfolge des kompletten Zeilensatzes beibehält.</span><span class="sxs-lookup"><span data-stu-id="b93f8-308">Therefore, any changes to a row's weight should also ensure that the row's position maintains the sorted order of the complete set of rows.</span></span> <span data-ttu-id="b93f8-309">Zusätze zum Zeilensatz sollten an der richtigen Stelle eingefügt werden, um die Sortierreihenfolge beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="b93f8-309">Any additions to the row-set should be inserted to the correct position to maintain the sorted order.</span></span>
  
<span data-ttu-id="b93f8-310">Der Mindestwert für diese Gewichtung ist 0x1, und der Maximalwert beträgt LONG_MAX.</span><span class="sxs-lookup"><span data-stu-id="b93f8-310">The minimum value of this weight is 0x1 and the maximum value is LONG_MAX.</span></span> <span data-ttu-id="b93f8-311">Alle anderen Werte für die Gewichtung werden als ungültig betrachtet.</span><span class="sxs-lookup"><span data-stu-id="b93f8-311">Any other values for the weight are considered invalid.</span></span>
  
<span data-ttu-id="b93f8-312">Wenn Outlook 2007 eine E-Mail an einen Empfänger versendet oder einen Empfänger auflöst, wird die Gewichtung dieses Empfängers um 0x2000 erhöht.</span><span class="sxs-lookup"><span data-stu-id="b93f8-312">When Outlook 2007 sends a mail to or resolves a recipient, it will increase that recipient's weight by 0x2000.</span></span>
  

