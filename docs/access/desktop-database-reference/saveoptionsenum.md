---
title: SaveOptionsEnum (Access Desktop Database Reference)
TOCTitle: SaveOptionsEnum
ms:assetid: 2a4e4c7a-6331-7270-0514-cc549c721ffd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249053(v=office.15)
ms:contentKeyID: 48543906
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 77a617dc54d8acd145648d926e10cf7c9a3cf252
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314742"
---
# <a name="saveoptionsenum"></a><span data-ttu-id="2803e-102">SaveOptionsEnum</span><span class="sxs-lookup"><span data-stu-id="2803e-102">SaveOptionsEnum</span></span>

<span data-ttu-id="2803e-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2803e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2803e-p101">Gibt an, ob eine Datei erstellt oder gespeichert werden sollte, wenn die Speicherung in einem [Stream](stream-object-ado.md)-Objekt erfolgt. Die Werte können mit einem AND-Operator kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="2803e-p101">Specifies whether a file should be created or overwritten when saving from a [Stream](stream-object-ado.md) object. The values can be combined with an AND operator.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2803e-106">Konstante</span><span class="sxs-lookup"><span data-stu-id="2803e-106">Constant</span></span></p></th>
<th><p><span data-ttu-id="2803e-107">Wert</span><span class="sxs-lookup"><span data-stu-id="2803e-107">Value</span></span></p></th>
<th><p><span data-ttu-id="2803e-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2803e-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2803e-109"><strong>adSaveCreateNotExist</strong></span><span class="sxs-lookup"><span data-stu-id="2803e-109"><strong>adSaveCreateNotExist</strong></span></span></p></td>
<td><p><span data-ttu-id="2803e-110">1</span><span class="sxs-lookup"><span data-stu-id="2803e-110">1</span></span></p></td>
<td><p><span data-ttu-id="2803e-p102">Standardwert. Erstellt eine neue Datei, wenn die vom <em>FileName</em>-Parameter angegebene Datei nicht bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="2803e-p102">Default. Creates a new file if the file specified by the <em>FileName</em> parameter does not already exist.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2803e-113"><strong>adSaveCreateOverwrite festgelegt</strong></span><span class="sxs-lookup"><span data-stu-id="2803e-113"><strong>adSaveCreateOverWrite</strong></span></span></p></td>
<td><p><span data-ttu-id="2803e-114">2</span><span class="sxs-lookup"><span data-stu-id="2803e-114">2</span></span></p></td>
<td><p><span data-ttu-id="2803e-115">Überschreibt die Datei mit den Daten des aktuell geöffneten <strong>Stream</strong>-Objekts, wenn die vom <em>Filename</em>-Parameter angegebene Datei bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="2803e-115">Overwrites the file with the data from the currently open <strong>Stream</strong> object, if the file specified by the <em>Filename</em> parameter already exists.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="2803e-116">ADO/WFC-Äquivalent</span><span class="sxs-lookup"><span data-stu-id="2803e-116">ADO/WFC equivalent</span></span>

<span data-ttu-id="2803e-117">Diese Konstanten haben keine ADO/WFC-Entsprechungen.</span><span class="sxs-lookup"><span data-stu-id="2803e-117">These constants do not have ADO/WFC equivalents.</span></span>

