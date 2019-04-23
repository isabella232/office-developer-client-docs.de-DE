---
title: MoveRecordOptionsEnum
TOCTitle: MoveRecordOptionsEnum
ms:assetid: 2785bca0-777c-a802-51d7-6f5cf0fb4210
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249039(v=office.15)
ms:contentKeyID: 48543842
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5bd8196670513156011d69f08eacf790fa4a0a03
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288672"
---
# <a name="moverecordoptionsenum"></a><span data-ttu-id="0feba-102">MoveRecordOptionsEnum</span><span class="sxs-lookup"><span data-stu-id="0feba-102">MoveRecordOptionsEnum</span></span>


<span data-ttu-id="0feba-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0feba-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0feba-104">Gibt das Verhalten der [MoveRecord](moverecord-method-ado.md)-Methode des [Record](record-object-ado.md)-Objekts an.</span><span class="sxs-lookup"><span data-stu-id="0feba-104">Specifies the behavior of the [Record](record-object-ado.md) object [MoveRecord](moverecord-method-ado.md) method.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0feba-105">Konstante</span><span class="sxs-lookup"><span data-stu-id="0feba-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="0feba-106">Wert</span><span class="sxs-lookup"><span data-stu-id="0feba-106">Value</span></span></p></th>
<th><p><span data-ttu-id="0feba-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0feba-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0feba-108"><strong>adMoveUnspecified</strong></span><span class="sxs-lookup"><span data-stu-id="0feba-108"><strong>adMoveUnspecified</strong></span></span></p></td>
<td><p><span data-ttu-id="0feba-109">-1</span><span class="sxs-lookup"><span data-stu-id="0feba-109">-1</span></span></p></td>
<td><p><span data-ttu-id="0feba-p101">Standardwert. Führt den Standardverschiebevorgang aus: Der Vorgang schlägt fehl, wenn die Zieldatei oder das Zielverzeichnis bereits vorhanden ist und der Vorgang Hypertextverknüpfungen aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="0feba-p101">Default. Performs the default move operation: The operation fails if the destination file or directory already exists, and the operation updates hypertext links.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0feba-112"><strong>adMoveOverWrite</strong></span><span class="sxs-lookup"><span data-stu-id="0feba-112"><strong>adMoveOverWrite</strong></span></span></p></td>
<td><p><span data-ttu-id="0feba-113">1</span><span class="sxs-lookup"><span data-stu-id="0feba-113">1</span></span></p></td>
<td><p><span data-ttu-id="0feba-114">Überschreibt die Zieldatei oder das Verzeichnis, selbst wenn es bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="0feba-114">Overwrites the destination file or directory, even if it already exists.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0feba-115"><strong>adMoveDontUpdateLinks</strong></span><span class="sxs-lookup"><span data-stu-id="0feba-115"><strong>adMoveDontUpdateLinks</strong></span></span></p></td>
<td><p><span data-ttu-id="0feba-116">2</span><span class="sxs-lookup"><span data-stu-id="0feba-116">2</span></span></p></td>
<td><p><span data-ttu-id="0feba-117">Ändert das Standardverhalten der <strong>MoveRecord</strong> -Methode, indem die Hypertext-Links des Quell <strong>Datensatzes</strong>nicht aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="0feba-117">Modifies the default behavior of <strong>MoveRecord</strong> method by not updating the hypertext links of the source <strong>Record</strong>.</span></span> <span data-ttu-id="0feba-118">Das Standardverhalten hängt von den Funktionen des Anbieters ab.</span><span class="sxs-lookup"><span data-stu-id="0feba-118">The default behavior depends on the capabilities of the provider.</span></span> <span data-ttu-id="0feba-119">Move-Vorgangs Updates Links, wenn der Anbieter fähig ist.</span><span class="sxs-lookup"><span data-stu-id="0feba-119">Move operation updates links if the provider is capable.</span></span> <span data-ttu-id="0feba-120">Wenn der Anbieter keine Verknüpfungen korrigieren kann oder wenn dieser Wert nicht angegeben ist, wird die Verschiebung auch dann erfolgreich ausgeführt, wenn die Verknüpfungen nicht behoben wurden.</span><span class="sxs-lookup"><span data-stu-id="0feba-120">If the provider cannot fix links or if this value is not specified, then the move succeeds even when links have not been fixed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0feba-121"><strong>adMoveAllowEmulation</strong></span><span class="sxs-lookup"><span data-stu-id="0feba-121"><strong>adMoveAllowEmulation</strong></span></span></p></td>
<td><p><span data-ttu-id="0feba-122">4</span><span class="sxs-lookup"><span data-stu-id="0feba-122">4</span></span></p></td>
<td><p><span data-ttu-id="0feba-p103">Fordert an, dass der Anbieter das Verschieben (mit Download-, Upload- und Löschvorgängen) simuliert. Wenn das Verschieben des Datensatzes fehlschlägt, weil sich die Ziel-URL auf einem anderen Server befindet oder von einem anderen Anbieter als die Quelle bedient wird, kann dies aufgrund verschiedener Anbieterfunktionen beim Verschieben von Ressourcen zwischen den Anbietern zu einer erhöhten Latenz oder zu Datenverlust führen.</span><span class="sxs-lookup"><span data-stu-id="0feba-p103">Requests that the provider attempt to simulate the move (using download, upload, and delete operations). If the attempt to move the <strong>Record</strong> fails because the destination URL is on a different server or serviced by a different provider than the source, this may cause increased latency or data loss, due to different provider capabilities when moving resources between providers.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="0feba-125">ADO/WFC-Äquivalent</span><span class="sxs-lookup"><span data-stu-id="0feba-125">ADO/WFC equivalent</span></span>

<span data-ttu-id="0feba-126">Diese Konstanten haben keine ADO/WFC-Entsprechungen.</span><span class="sxs-lookup"><span data-stu-id="0feba-126">These constants do not have ADO/WFC equivalents.</span></span>

