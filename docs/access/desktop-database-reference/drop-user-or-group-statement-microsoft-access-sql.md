---
title: DROP USER- oder GROUP-Anweisung (Microsoft Access SQL)
TOCTitle: DROP USER or GROUP Statement (Microsoft Access SQL)
ms:assetid: 46bc5916-556b-17df-2f4c-8fd7bbd21ef7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193192(v=office.15)
ms:contentKeyID: 48544575
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3a5cf75de06c13e2452e5f33b8355b7fb480d8a3
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25473165"
---
# <a name="drop-user-or-group-statement-microsoft-access-sql"></a><span data-ttu-id="ea5a9-102">DROP USER- oder GROUP-Anweisung (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="ea5a9-102">DROP USER or GROUP Statement (Microsoft Access SQL)</span></span>


<span data-ttu-id="ea5a9-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="ea5a9-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="ea5a9-104">Löscht, sofern vorhanden, einen oder mehrere *Benutzer* bzw. eine oder mehrere *Gruppe*(n) oder entfernt, sofern vorhanden, einen oder mehrere *Benutzer* aus einer vorhandenen *Gruppe*.</span><span class="sxs-lookup"><span data-stu-id="ea5a9-104">Deletes one or more existing *user*s or *group*s, or removes one or more existing *user*s from an existing *group*.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea5a9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ea5a9-105">Syntax</span></span>

<span data-ttu-id="ea5a9-106">Zum Löschen eines oder mehrerer *Benutzer*(s) bzw. zum Entfernen eines oder mehrerer *Benutzer*(s) aus einer *Gruppe*:</span><span class="sxs-lookup"><span data-stu-id="ea5a9-106">Delete one or more *user*s or remove one or more *user*s from a *group*:</span></span>

<span data-ttu-id="ea5a9-107">DROP USER *Benutzer*\[, *Benutzer*,... \] \[Aus *Gruppe*\]</span><span class="sxs-lookup"><span data-stu-id="ea5a9-107">DROP USER *user*\[, *user*, …\] \[FROM *group*\]</span></span>

<span data-ttu-id="ea5a9-108">Zum Löschen einer oder mehrerer *Gruppe*(n):</span><span class="sxs-lookup"><span data-stu-id="ea5a9-108">Delete one or more *group*s:</span></span>

<span data-ttu-id="ea5a9-109">DROP GROUP *Gruppe*\[, *Gruppe*,...\]</span><span class="sxs-lookup"><span data-stu-id="ea5a9-109">DROP GROUP *group*\[, *group*, …\]</span></span>

<span data-ttu-id="ea5a9-110">Die DROP USER- oder GROUP-Anweisung besteht aus folgenden Komponenten:</span><span class="sxs-lookup"><span data-stu-id="ea5a9-110">The DROP USER or GROUP statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ea5a9-111">Komponente</span><span class="sxs-lookup"><span data-stu-id="ea5a9-111">Part</span></span></p></th>
<th><p><span data-ttu-id="ea5a9-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ea5a9-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ea5a9-113"><em>Benutzer</em></span><span class="sxs-lookup"><span data-stu-id="ea5a9-113"><em>user</em></span></span></p></td>
<td><p><span data-ttu-id="ea5a9-114">Der Name eines Benutzers, der aus der Informationsdatei für die Arbeitsgruppe entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="ea5a9-114">The name of a user to be removed from the workgroup information file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ea5a9-115"><em>Gruppe</em></span><span class="sxs-lookup"><span data-stu-id="ea5a9-115"><em>group</em></span></span></p></td>
<td><p><span data-ttu-id="ea5a9-116">Der Name einer Gruppe, die aus der Informationsdatei für die Arbeitsgruppe entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="ea5a9-116">The name of a group to be removed from the workgroup information file.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="ea5a9-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ea5a9-117">Remarks</span></span>

<span data-ttu-id="ea5a9-p101">Wenn das FROM-Schlüsselwort in der DROP USER-Anweisung verwendet wird, werden alle in der Anweisung aufgelisteten *Benutzer* aus der *Gruppe* entfernt, die im Anschluss an das FROM-Schlüsselwort angegeben wird. Die *Benutzer* selbst werden jedoch nicht gelöscht.</span><span class="sxs-lookup"><span data-stu-id="ea5a9-p101">If the FROM keyword is used in the DROP USER statement, then each of the *user*s listed in the statement will be removed from the *group* specified following the FROM keyword. However, the *user*s themselves will not be deleted.</span></span>

<span data-ttu-id="ea5a9-p102">Die DROP GROUP-Anweisung dient zum Löschen der angegebenen *Grupppe*(n). Dieser Löschvorgang hat keine Auswirkung auf die *Benutzer*, die Mitglieder der *Gruppe*(n) sind, sie sind lediglich keine Mitglieder der gelöschten *Gruppe*(n) mehr.</span><span class="sxs-lookup"><span data-stu-id="ea5a9-p102">The DROP GROUP statement will delete the specified *group*(s). The *user*s who are members of the *group*(s) will not be affected, but they will no longer be members of the deleted *group*(s).</span></span>

