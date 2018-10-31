---
title: CopyRecordOptionsEnum
TOCTitle: CopyRecordOptionsEnum
ms:assetid: ab9426e9-0e4e-6c85-43cf-e4a205a7c4c0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249795(v=office.15)
ms:contentKeyID: 48546975
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b33347492562d868781e8bbca346918d55ed597b
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25860280"
---
# <a name="copyrecordoptionsenum"></a><span data-ttu-id="daef2-102">CopyRecordOptionsEnum</span><span class="sxs-lookup"><span data-stu-id="daef2-102">CopyRecordOptionsEnum</span></span>


<span data-ttu-id="daef2-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="daef2-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="daef2-104">Gibt das Verhalten der [CopyRecord](copyrecord-method-ado.md)-Methode an.</span><span class="sxs-lookup"><span data-stu-id="daef2-104">Specifies the behavior of the [CopyRecord](copyrecord-method-ado.md) method.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="daef2-105">Konstante</span><span class="sxs-lookup"><span data-stu-id="daef2-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="daef2-106">Wert</span><span class="sxs-lookup"><span data-stu-id="daef2-106">Value</span></span></p></th>
<th><p><span data-ttu-id="daef2-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="daef2-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="daef2-108"><strong>adCopyAllowEmulation</strong></span><span class="sxs-lookup"><span data-stu-id="daef2-108"><strong>adCopyAllowEmulation</strong></span></span></p></td>
<td><p><span data-ttu-id="daef2-109">4</span><span class="sxs-lookup"><span data-stu-id="daef2-109">4</span></span></p></td>
<td><p><span data-ttu-id="daef2-p101">Gibt an, dass der Anbieter <em>Quelle</em> versucht, die Kopie mithilfe von Download- und Uploadvorgängen zu simulieren, wenn diese Methode aufgrund des <em>Ziels</em> fehlschlägt, das sich auf einem anderen Server befindet, oder wenn sie von einem anderen Anbieter als <em>Quelle</em> bedient wird. Beachten Sie, dass abweichende Anbieterfunktionen die Leistung einschränken oder zu Datenverlusten führen können.</span><span class="sxs-lookup"><span data-stu-id="daef2-p101">Indicates that the <em>Source</em> provider attempts to simulate the copy using download and upload operations if this method fails due to <em>Destination</em> being on a different server or is serviced by a different provider than <em>Source</em>. Note that differing provider capabilities may hamper performance or lose data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="daef2-112"><strong>adCopyNonRecursive</strong></span><span class="sxs-lookup"><span data-stu-id="daef2-112"><strong>adCopyNonRecursive</strong></span></span></p></td>
<td><p><span data-ttu-id="daef2-113">2</span><span class="sxs-lookup"><span data-stu-id="daef2-113">2</span></span></p></td>
<td><p><span data-ttu-id="daef2-p102">Kopiert das aktuelle Verzeichnis, aber keines seiner Unterverzeichnisse an das Ziel. Der Kopiervorgang ist nicht rekursiv.</span><span class="sxs-lookup"><span data-stu-id="daef2-p102">Copies the current directory, but none of its subdirectories, to the destination. The copy operation is not recursive.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="daef2-116"><strong>adCopyOverWrite</strong></span><span class="sxs-lookup"><span data-stu-id="daef2-116"><strong>adCopyOverWrite</strong></span></span></p></td>
<td><p><span data-ttu-id="daef2-117">1</span><span class="sxs-lookup"><span data-stu-id="daef2-117">1</span></span></p></td>
<td><p><span data-ttu-id="daef2-118">Überschreibt die Datei oder das Verzeichnis, wenn das <em>Ziel</em> auf eine bereits vorhandene Datei oder ein bereits vorhandenes Verzeichnis verweist.</span><span class="sxs-lookup"><span data-stu-id="daef2-118">Overwrites the file or directory if the <em>Destination</em> points to an existing file or directory.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="daef2-119"><strong>adCopyUnspecified</strong></span><span class="sxs-lookup"><span data-stu-id="daef2-119"><strong>adCopyUnspecified</strong></span></span></p></td>
<td><p><span data-ttu-id="daef2-120">-1</span><span class="sxs-lookup"><span data-stu-id="daef2-120">-1</span></span></p></td>
<td><p><span data-ttu-id="daef2-p103">Standardwert. Führt den Standardkopiervorgang aus: Der Vorgang schlägt fehl, wenn die Zieldatei oder das Zielverzeichnis bereits vorhanden ist, und der Vorgang rekursiv kopiert.</span><span class="sxs-lookup"><span data-stu-id="daef2-p103">Default. Performs the default copy operation: The operation fails if the destination file or directory already exists, and the operation copies recursively.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="daef2-123">ADO/WFC-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="daef2-123">ADO/WFC equivalent</span></span>

<span data-ttu-id="daef2-124">Diese Konstanten haben keine ADO/WFC-Entsprechungen.</span><span class="sxs-lookup"><span data-stu-id="daef2-124">These constants do not have ADO/WFC equivalents.</span></span>

