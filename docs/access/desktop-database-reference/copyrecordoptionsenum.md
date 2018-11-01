---
title: CopyRecordOptionsEnum
TOCTitle: CopyRecordOptionsEnum
ms:assetid: ab9426e9-0e4e-6c85-43cf-e4a205a7c4c0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249795(v=office.15)
ms:contentKeyID: 48546975
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d3c3ddd8174a646bccd37cec758e85e17f4cdaec
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25882777"
---
# <a name="copyrecordoptionsenum"></a><span data-ttu-id="c75a8-102">CopyRecordOptionsEnum</span><span class="sxs-lookup"><span data-stu-id="c75a8-102">CopyRecordOptionsEnum</span></span>


<span data-ttu-id="c75a8-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c75a8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c75a8-104">Gibt das Verhalten der [CopyRecord](copyrecord-method-ado.md)-Methode an.</span><span class="sxs-lookup"><span data-stu-id="c75a8-104">Specifies the behavior of the [CopyRecord](copyrecord-method-ado.md) method.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c75a8-105">Konstante</span><span class="sxs-lookup"><span data-stu-id="c75a8-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="c75a8-106">Wert</span><span class="sxs-lookup"><span data-stu-id="c75a8-106">Value</span></span></p></th>
<th><p><span data-ttu-id="c75a8-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c75a8-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c75a8-108"><strong>adCopyAllowEmulation</strong></span><span class="sxs-lookup"><span data-stu-id="c75a8-108"><strong>adCopyAllowEmulation</strong></span></span></p></td>
<td><p><span data-ttu-id="c75a8-109">4</span><span class="sxs-lookup"><span data-stu-id="c75a8-109">4</span></span></p></td>
<td><p><span data-ttu-id="c75a8-p101">Gibt an, dass der Anbieter <em>Quelle</em> versucht, die Kopie mithilfe von Download- und Uploadvorgängen zu simulieren, wenn diese Methode aufgrund des <em>Ziels</em> fehlschlägt, das sich auf einem anderen Server befindet, oder wenn sie von einem anderen Anbieter als <em>Quelle</em> bedient wird. Beachten Sie, dass abweichende Anbieterfunktionen die Leistung einschränken oder zu Datenverlusten führen können.</span><span class="sxs-lookup"><span data-stu-id="c75a8-p101">Indicates that the <em>Source</em> provider attempts to simulate the copy using download and upload operations if this method fails due to <em>Destination</em> being on a different server or is serviced by a different provider than <em>Source</em>. Note that differing provider capabilities may hamper performance or lose data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c75a8-112"><strong>adCopyNonRecursive</strong></span><span class="sxs-lookup"><span data-stu-id="c75a8-112"><strong>adCopyNonRecursive</strong></span></span></p></td>
<td><p><span data-ttu-id="c75a8-113">2</span><span class="sxs-lookup"><span data-stu-id="c75a8-113">2</span></span></p></td>
<td><p><span data-ttu-id="c75a8-p102">Kopiert das aktuelle Verzeichnis, aber keines seiner Unterverzeichnisse an das Ziel. Der Kopiervorgang ist nicht rekursiv.</span><span class="sxs-lookup"><span data-stu-id="c75a8-p102">Copies the current directory, but none of its subdirectories, to the destination. The copy operation is not recursive.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c75a8-116"><strong>adCopyOverWrite</strong></span><span class="sxs-lookup"><span data-stu-id="c75a8-116"><strong>adCopyOverWrite</strong></span></span></p></td>
<td><p><span data-ttu-id="c75a8-117">1</span><span class="sxs-lookup"><span data-stu-id="c75a8-117">1</span></span></p></td>
<td><p><span data-ttu-id="c75a8-118">Überschreibt die Datei oder das Verzeichnis, wenn das <em>Ziel</em> auf eine bereits vorhandene Datei oder ein bereits vorhandenes Verzeichnis verweist.</span><span class="sxs-lookup"><span data-stu-id="c75a8-118">Overwrites the file or directory if the <em>Destination</em> points to an existing file or directory.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c75a8-119"><strong>adCopyUnspecified</strong></span><span class="sxs-lookup"><span data-stu-id="c75a8-119"><strong>adCopyUnspecified</strong></span></span></p></td>
<td><p><span data-ttu-id="c75a8-120">-1</span><span class="sxs-lookup"><span data-stu-id="c75a8-120">-1</span></span></p></td>
<td><p><span data-ttu-id="c75a8-p103">Standardwert. Führt den Standardkopiervorgang aus: Der Vorgang schlägt fehl, wenn die Zieldatei oder das Zielverzeichnis bereits vorhanden ist, und der Vorgang rekursiv kopiert.</span><span class="sxs-lookup"><span data-stu-id="c75a8-p103">Default. Performs the default copy operation: The operation fails if the destination file or directory already exists, and the operation copies recursively.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="c75a8-123">ADO/WFC-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="c75a8-123">ADO/WFC equivalent</span></span>

<span data-ttu-id="c75a8-124">Diese Konstanten haben keine ADO/WFC-Entsprechungen.</span><span class="sxs-lookup"><span data-stu-id="c75a8-124">These constants do not have ADO/WFC equivalents.</span></span>

