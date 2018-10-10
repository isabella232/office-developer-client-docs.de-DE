---
title: SaveOptionsEnum (Access PC-Datenbank-Referenz)
TOCTitle: SaveOptionsEnum
ms:assetid: 2a4e4c7a-6331-7270-0514-cc549c721ffd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249053(v=office.15)
ms:contentKeyID: 48543906
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 68526eca205fb41dd2789ec187514d0f9b11e35f
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25473559"
---
# <a name="saveoptionsenum"></a><span data-ttu-id="47184-102">SaveOptionsEnum</span><span class="sxs-lookup"><span data-stu-id="47184-102">SaveOptionsEnum</span></span>


<span data-ttu-id="47184-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="47184-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="47184-p101">Gibt an, ob eine Datei erstellt oder gespeichert werden sollte, wenn die Speicherung in einem [Stream](stream-object-ado.md)-Objekt erfolgt. Die Werte können mit einem AND-Operator kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="47184-p101">Specifies whether a file should be created or overwritten when saving from a [Stream](stream-object-ado.md) object. The values can be combined with an AND operator.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="47184-106">Konstante</span><span class="sxs-lookup"><span data-stu-id="47184-106">Constant</span></span></p></th>
<th><p><span data-ttu-id="47184-107">Wert</span><span class="sxs-lookup"><span data-stu-id="47184-107">Value</span></span></p></th>
<th><p><span data-ttu-id="47184-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="47184-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="47184-109"><strong>adSaveCreateNotExist</strong></span><span class="sxs-lookup"><span data-stu-id="47184-109"><strong>adSaveCreateNotExist</strong></span></span></p></td>
<td><p><span data-ttu-id="47184-110">1</span><span class="sxs-lookup"><span data-stu-id="47184-110">1</span></span></p></td>
<td><p><span data-ttu-id="47184-p102">Standardwert. Erstellt eine neue Datei, wenn die vom <em>FileName</em>-Parameter angegebene Datei nicht bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="47184-p102">Default. Creates a new file if the file specified by the <em>FileName</em> parameter does not already exist.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="47184-113"><strong>adSaveCreateOverWrite</strong></span><span class="sxs-lookup"><span data-stu-id="47184-113"><strong>adSaveCreateOverWrite</strong></span></span></p></td>
<td><p><span data-ttu-id="47184-114">2</span><span class="sxs-lookup"><span data-stu-id="47184-114">2</span></span></p></td>
<td><p><span data-ttu-id="47184-115">Überschreibt die Datei mit den Daten des aktuell geöffneten <strong>Stream</strong>-Objekts, wenn die vom <em>Filename</em>-Parameter angegebene Datei bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="47184-115">Overwrites the file with the data from the currently open <strong>Stream</strong> object, if the file specified by the <em>Filename</em> parameter already exists.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="47184-116">**ADO/WFC-Entsprechung**</span><span class="sxs-lookup"><span data-stu-id="47184-116">**ADO/WFC Equivalent**</span></span>

<span data-ttu-id="47184-117">Diese Konstanten haben keine ADO/WFC-Entsprechungen.</span><span class="sxs-lookup"><span data-stu-id="47184-117">These constants do not have ADO/WFC equivalents.</span></span>

