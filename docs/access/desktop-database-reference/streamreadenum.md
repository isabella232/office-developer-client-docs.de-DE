---
title: StreamReadEnum (Access Desktop Database Reference)
TOCTitle: StreamReadEnum
ms:assetid: 12432c0d-dc2e-10ea-13db-0c07b6ba29bc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248895(v=office.15)
ms:contentKeyID: 48543336
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e4d9c96a7bb34fe0ab3512a316a92e1f7a01ef4b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314721"
---
# <a name="streamreadenum"></a><span data-ttu-id="c8c55-102">StreamReadEnum</span><span class="sxs-lookup"><span data-stu-id="c8c55-102">StreamReadEnum</span></span>

<span data-ttu-id="c8c55-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c8c55-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c8c55-104">Gibt an, ob der gesamte Datenstrom oder die nächste Zeile aus einem [Stream](stream-object-ado.md)-Objekt gelesen werden sollte.</span><span class="sxs-lookup"><span data-stu-id="c8c55-104">Specifies whether the whole stream or the next line should be read from a [Stream](stream-object-ado.md) object.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c8c55-105">Konstante</span><span class="sxs-lookup"><span data-stu-id="c8c55-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="c8c55-106">Wert</span><span class="sxs-lookup"><span data-stu-id="c8c55-106">Value</span></span></p></th>
<th><p><span data-ttu-id="c8c55-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c8c55-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c8c55-108"><strong>adReadAll</strong></span><span class="sxs-lookup"><span data-stu-id="c8c55-108"><strong>adReadAll</strong></span></span></p></td>
<td><p><span data-ttu-id="c8c55-109">-1</span><span class="sxs-lookup"><span data-stu-id="c8c55-109">-1</span></span></p></td>
<td><p><span data-ttu-id="c8c55-p101">Standardwert. Liest alle Bytes aus dem Datenstrom, von der aktuellen Position bis zur <a href="eos-property-ado.md">EOS</a>-Markierung. Dies ist der einzige gültige <strong>StreamReadEnum</strong>-Wert mit binären Datenströmen (<a href="type-property-ado-stream.md">Typ</a> ist <strong>adTypeBinary</strong>).</span><span class="sxs-lookup"><span data-stu-id="c8c55-p101">Default. Reads all bytes from the stream, from the current position onwards to the <a href="eos-property-ado.md">EOS</a> marker. This is the only valid <strong>StreamReadEnum</strong> value with binary streams (<a href="type-property-ado-stream.md">Type</a> is <strong>adTypeBinary</strong>).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c8c55-113"><strong>Angleichen</strong></span><span class="sxs-lookup"><span data-stu-id="c8c55-113"><strong>adReadLine</strong></span></span></p></td>
<td><p><span data-ttu-id="c8c55-114">-2</span><span class="sxs-lookup"><span data-stu-id="c8c55-114">-2</span></span></p></td>
<td><p><span data-ttu-id="c8c55-115">Liest die nächste Zeile aus dem Datenstrom (angegeben durch die <a href="lineseparator-property-ado.md">LineSeparator</a>-Eigenschaft).</span><span class="sxs-lookup"><span data-stu-id="c8c55-115">Reads the next line from the stream (designated by the <a href="lineseparator-property-ado.md">LineSeparator</a> property).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="c8c55-116">ADO/WFC-Äquivalent</span><span class="sxs-lookup"><span data-stu-id="c8c55-116">ADO/WFC equivalent</span></span>

<span data-ttu-id="c8c55-117">Diese Konstanten haben keine ADO/WFC-Entsprechungen.</span><span class="sxs-lookup"><span data-stu-id="c8c55-117">These constants do not have ADO/WFC equivalents.</span></span>

