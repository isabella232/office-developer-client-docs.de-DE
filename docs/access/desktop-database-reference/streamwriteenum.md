---
title: StreamWriteEnum (Access PC-Datenbank-Referenz)
TOCTitle: StreamWriteEnum
ms:assetid: b4356999-d7a8-abfa-f6a8-6c2dd04b9257
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249861(v=office.15)
ms:contentKeyID: 48547216
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 87144e5409fb54cf0cb8f59ad4d593ab05d694a4
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28706170"
---
# <a name="streamwriteenum"></a><span data-ttu-id="b6dc1-102">StreamWriteEnum</span><span class="sxs-lookup"><span data-stu-id="b6dc1-102">StreamWriteEnum</span></span>

<span data-ttu-id="b6dc1-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b6dc1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b6dc1-104">Gibt an, ob der Zeichenfolge, die in ein [Stream](stream-object-ado.md)-Objekt geschrieben wird, ein Zeilentrennzeichen angehängt wird.</span><span class="sxs-lookup"><span data-stu-id="b6dc1-104">Specifies whether a line separator is appended to the string written to a [Stream](stream-object-ado.md) object.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b6dc1-105">Konstante</span><span class="sxs-lookup"><span data-stu-id="b6dc1-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="b6dc1-106">Wert</span><span class="sxs-lookup"><span data-stu-id="b6dc1-106">Value</span></span></p></th>
<th><p><span data-ttu-id="b6dc1-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b6dc1-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b6dc1-108"><strong>adWriteChar</strong></span><span class="sxs-lookup"><span data-stu-id="b6dc1-108"><strong>adWriteChar</strong></span></span></p></td>
<td><p><span data-ttu-id="b6dc1-109">0</span><span class="sxs-lookup"><span data-stu-id="b6dc1-109">0</span></span></p></td>
<td><p><span data-ttu-id="b6dc1-p101">Standardwert. Schreibt die angegebene Zeichenfolge (die vom <em>Data</em>-Parameter angegeben wird) in das <strong>Stream</strong>-Objekt.</span><span class="sxs-lookup"><span data-stu-id="b6dc1-p101">Default. Writes the specified text string (specified by the <em>Data</em> parameter) to the <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b6dc1-112"><strong>adWriteLine</strong></span><span class="sxs-lookup"><span data-stu-id="b6dc1-112"><strong>adWriteLine</strong></span></span></p></td>
<td><p><span data-ttu-id="b6dc1-113">1</span><span class="sxs-lookup"><span data-stu-id="b6dc1-113">1</span></span></p></td>
<td><p><span data-ttu-id="b6dc1-p102">Schreibt eine Textzeichenfolge und ein Zeilentrennzeichen in ein <strong>Stream</strong>-Objekt. Wenn keine <a href="lineseparator-property-ado.md">LineSeparator</a>-Eigenschaft definiert ist, wird ein Laufzeitfehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b6dc1-p102">Writes a text string and a line separator character to a <strong>Stream</strong> object. If the <a href="lineseparator-property-ado.md">LineSeparator</a> property is not defined, then this returns a run-time error.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="b6dc1-116">ADO/WFC-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="b6dc1-116">ADO/WFC equivalent</span></span>

<span data-ttu-id="b6dc1-117">Diese Konstanten haben keine ADO/WFC-Entsprechungen.</span><span class="sxs-lookup"><span data-stu-id="b6dc1-117">These constants do not have ADO/WFC equivalents.</span></span>

