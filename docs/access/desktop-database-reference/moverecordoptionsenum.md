---
title: MoveRecordOptionsEnum
TOCTitle: MoveRecordOptionsEnum
ms:assetid: 2785bca0-777c-a802-51d7-6f5cf0fb4210
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249039(v=office.15)
ms:contentKeyID: 48543842
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: fc621f620a7d55571aa55296a4d294fff9566bf5
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25862240"
---
# <a name="moverecordoptionsenum"></a><span data-ttu-id="46f75-102">MoveRecordOptionsEnum</span><span class="sxs-lookup"><span data-stu-id="46f75-102">MoveRecordOptionsEnum</span></span>


<span data-ttu-id="46f75-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="46f75-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="46f75-104">Gibt das Verhalten der [MoveRecord](record-object-ado.md)-Methode des [Record](moverecord-method-ado.md)-Objekts an.</span><span class="sxs-lookup"><span data-stu-id="46f75-104">Specifies the behavior of the [Record](record-object-ado.md) object [MoveRecord](moverecord-method-ado.md) method.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="46f75-105">Konstante</span><span class="sxs-lookup"><span data-stu-id="46f75-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="46f75-106">Wert</span><span class="sxs-lookup"><span data-stu-id="46f75-106">Value</span></span></p></th>
<th><p><span data-ttu-id="46f75-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="46f75-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="46f75-108"><strong>adMoveUnspecified</strong></span><span class="sxs-lookup"><span data-stu-id="46f75-108"><strong>adMoveUnspecified</strong></span></span></p></td>
<td><p><span data-ttu-id="46f75-109">-1</span><span class="sxs-lookup"><span data-stu-id="46f75-109">-1</span></span></p></td>
<td><p><span data-ttu-id="46f75-p101">Standardwert. Führt den Standardverschiebevorgang aus: Der Vorgang schlägt fehl, wenn die Zieldatei oder das Zielverzeichnis bereits vorhanden ist und der Vorgang Hypertextverknüpfungen aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="46f75-p101">Default. Performs the default move operation: The operation fails if the destination file or directory already exists, and the operation updates hypertext links.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="46f75-112"><strong>adMoveOverWrite an</strong></span><span class="sxs-lookup"><span data-stu-id="46f75-112"><strong>adMoveOverWrite</strong></span></span></p></td>
<td><p><span data-ttu-id="46f75-113">1</span><span class="sxs-lookup"><span data-stu-id="46f75-113">1</span></span></p></td>
<td><p><span data-ttu-id="46f75-114">Überschreibt die Zieldatei oder das Verzeichnis, selbst wenn es bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="46f75-114">Overwrites the destination file or directory, even if it already exists.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="46f75-115"><strong>adMoveDontUpdateLinks</strong></span><span class="sxs-lookup"><span data-stu-id="46f75-115"><strong>adMoveDontUpdateLinks</strong></span></span></p></td>
<td><p><span data-ttu-id="46f75-116">2</span><span class="sxs-lookup"><span data-stu-id="46f75-116">2</span></span></p></td>
<td><p><span data-ttu-id="46f75-117">Ändert das Standardverhalten des <strong>MoveRecord</strong> -Methode durch die Hyperlinks der Quelle <strong>Datensatz</strong>nicht aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="46f75-117">Modifies the default behavior of <strong>MoveRecord</strong> method by not updating the hypertext links of the source <strong>Record</strong>.</span></span> <span data-ttu-id="46f75-118">Das Standardverhalten, hängt von der Funktionalität des Anbieters ab.</span><span class="sxs-lookup"><span data-stu-id="46f75-118">The default behavior depends on the capabilities of the provider.</span></span> <span data-ttu-id="46f75-119">Verschiebevorgangs aktualisiert Verknüpfungen, wenn der Anbieter kann.</span><span class="sxs-lookup"><span data-stu-id="46f75-119">Move operation updates links if the provider is capable.</span></span> <span data-ttu-id="46f75-120">Wenn der Anbieter nicht Links beheben kann, oder wenn dieser Wert nicht angegeben wird, erfolgreich verschieben, selbst wenn Links nicht behoben wurden.</span><span class="sxs-lookup"><span data-stu-id="46f75-120">If the provider cannot fix links or if this value is not specified, then the move succeeds even when links have not been fixed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="46f75-121"><strong>adMoveAllowEmulation</strong></span><span class="sxs-lookup"><span data-stu-id="46f75-121"><strong>adMoveAllowEmulation</strong></span></span></p></td>
<td><p><span data-ttu-id="46f75-122">4</span><span class="sxs-lookup"><span data-stu-id="46f75-122">4</span></span></p></td>
<td><p><span data-ttu-id="46f75-123">Fordert an, dass der Anbieter das Verschieben (mit Download, hochladen und Löschvorgänge) simuliert.</span><span class="sxs-lookup"><span data-stu-id="46f75-123">Requests that the provider attempt to simulate the move (using download, upload, and delete operations).</span></span> <span data-ttu-id="46f75-124">Wenn der Versuch, den <strong>Datensatz</strong> zu verschieben, schlägt fehl, da das Ziel-URL auf einem anderen Server ist oder von einem anderen Anbieter als die Quelle bedient, kann dies eine erhöhte Wartezeit oder Datenverlust aufgrund von anderen Anbieterfunktionen beim Verschieben von Ressourcen führen. zwischen Anbietern.</span><span class="sxs-lookup"><span data-stu-id="46f75-124">If the attempt to move the <strong>Record</strong> fails because the destination URL is on a different server or serviced by a different provider than the source, this may cause increased latency or data loss, due to different provider capabilities when moving resources between providers.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="46f75-125">ADO/WFC-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="46f75-125">ADO/WFC equivalent</span></span>

<span data-ttu-id="46f75-126">Diese Konstanten haben keine ADO/WFC-Entsprechungen.</span><span class="sxs-lookup"><span data-stu-id="46f75-126">These constants do not have ADO/WFC equivalents.</span></span>

