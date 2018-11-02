---
title: Cell-Objekt (ADO MD)
TOCTitle: Cell object (ADO MD)
ms:assetid: b9d00b71-1f40-5bd1-4b89-fbdb59c552ba
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249892(v=office.15)
ms:contentKeyID: 48547356
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2e119600567c8d3c6cd23348d9b9560011e27a87
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25924610"
---
# <a name="cell-object-ado-md"></a><span data-ttu-id="1f82d-102">Cell-Objekt (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="1f82d-102">Cell object (ADO MD)</span></span>


<span data-ttu-id="1f82d-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1f82d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1f82d-104">Stellt die Daten am Kreuzungspunkt von Achsenkoordinaten dar, die in einer Zellmenge enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="1f82d-104">Represents the data at the intersection of axis coordinates contained in a cellset.</span></span>

## <a name="remarks"></a><span data-ttu-id="1f82d-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1f82d-105">Remarks</span></span>

<span data-ttu-id="1f82d-106">Ein **Cell** -Objekt wird von der [Item](item-property-ado-md-cellset.md)-Eigenschaft eines [Cellset](cellset-object-ado-md.md)-Objekts zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="1f82d-106">A **Cell** object is returned by the [Item](item-property-ado-md-cellset.md) property of a [Cellset](cellset-object-ado-md.md) object.</span></span>

<span data-ttu-id="1f82d-107">Die Auflistungen und Eigenschaften eines **Cell** -Objekts ermöglichen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="1f82d-107">With the collections and properties of a **Cell** object, you can do the following:</span></span>

  - <span data-ttu-id="1f82d-108">Zurückgeben der Daten in der\*\*\*\* Zelle, indem Sie die [Value](value-property-ado-md.md)-Eigenschaft verwenden.</span><span class="sxs-lookup"><span data-stu-id="1f82d-108">Return the data in the **Cell** with the [Value](value-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="1f82d-109">Zurückgeben der Zeichenfolge, die die formatierte **Value** -Eigenschaft darstellt, indem Sie die [FormattedValue](formattedvalue-property-ado-md.md)-Eigenschaft verwenden.</span><span class="sxs-lookup"><span data-stu-id="1f82d-109">Return the string representing the formatted display of the **Value** property with the [FormattedValue](formattedvalue-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="1f82d-110">Zurückgeben des Ordnungswerts der\*\*\*\* Zelle innerhalb der\*\*\*\* Zellmenge, indem Sie die [Ordinal](ordinal-property-ado-md-cell.md)-Eigenschaft verwenden.</span><span class="sxs-lookup"><span data-stu-id="1f82d-110">Return the ordinal value of the **Cell** within the **Cellset** with the [Ordinal](ordinal-property-ado-md-cell.md) property.</span></span>

  - <span data-ttu-id="1f82d-111">Bestimmen der Zellenposition\*\*\*\* innerhalb des [CubeDef](cubedef-object-ado-md.md)-Objekts, indem Sie die [Positions](positions-collection-ado-md.md)-Auflistung verwenden.</span><span class="sxs-lookup"><span data-stu-id="1f82d-111">Determine the position of the **Cell** within the [CubeDef](cubedef-object-ado-md.md) with the [Positions](positions-collection-ado-md.md) collection.</span></span>

  - <span data-ttu-id="1f82d-112">Abrufen anderer Informationen zur\*\*\*\* Zelle, indem Sie die [Properties](properties-collection-ado.md)-ADO-Standardauflistung verwenden.</span><span class="sxs-lookup"><span data-stu-id="1f82d-112">Retrieve other information about the **Cell** with the standard ADO [Properties](properties-collection-ado.md) collection.</span></span>

<span data-ttu-id="1f82d-p101">Die **Properties** -Auflistung enthält Eigenschaften, die vom Anbieter bereitgestellt werden. In der folgenden Tabelle sind Eigenschaften aufgeführt, die möglicherweise verfügbar sind. Die tatsächliche Eigenschaftenliste kann je nach Anbieterimplementierung davon abweichen. Eine ausführlichere Liste mit verfügbaren Eigenschaften finden Sie in Ihrer Anbieterdokumentation.</span><span class="sxs-lookup"><span data-stu-id="1f82d-p101">The **Properties** collection contains provider-supplied properties. The following table lists properties that might be available. The actual property list may differ depending upon the implementation of the provider. See the documentation for your provider for a more complete list of available properties.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1f82d-117">Name</span><span class="sxs-lookup"><span data-stu-id="1f82d-117">Name</span></span></p></th>
<th><p><span data-ttu-id="1f82d-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1f82d-118">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1f82d-119">BackColor</span><span class="sxs-lookup"><span data-stu-id="1f82d-119">BackColor</span></span></p></td>
<td><p><span data-ttu-id="1f82d-120">Hintergrundfarbe, die beim Anzeigen der Zelle verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1f82d-120">Background color used when displaying the cell.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f82d-121">FontFlags</span><span class="sxs-lookup"><span data-stu-id="1f82d-121">FontFlags</span></span></p></td>
<td><p><span data-ttu-id="1f82d-122">Bitmaske für Schriftarteffekte.</span><span class="sxs-lookup"><span data-stu-id="1f82d-122">Bitmask detailing effects on the font.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f82d-123">FontName</span><span class="sxs-lookup"><span data-stu-id="1f82d-123">FontName</span></span></p></td>
<td><p><span data-ttu-id="1f82d-124">Schriftart, die beim Anzeigen des Zellwerts verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1f82d-124">Font used to display the cell value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f82d-125">FontSize</span><span class="sxs-lookup"><span data-stu-id="1f82d-125">FontSize</span></span></p></td>
<td><p><span data-ttu-id="1f82d-126">Schriftgrad, der beim Anzeigen des Zellwerts verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1f82d-126">Font size used to display the cell value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f82d-127">ForeColor</span><span class="sxs-lookup"><span data-stu-id="1f82d-127">ForeColor</span></span></p></td>
<td><p><span data-ttu-id="1f82d-128">Vordergrundfarbe, die beim Anzeigen der Zelle verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1f82d-128">Foreground color used when displaying the cell.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f82d-129">FormatString</span><span class="sxs-lookup"><span data-stu-id="1f82d-129">FormatString</span></span></p></td>
<td><p><span data-ttu-id="1f82d-130">Wert in einer formatierten Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="1f82d-130">Value in a formatted string.</span></span></p></td>
</tr>
</tbody>
</table>

