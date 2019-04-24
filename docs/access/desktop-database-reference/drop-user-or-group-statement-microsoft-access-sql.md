---
title: DROP USER-oder GROUP-Anweisung (Microsoft Access SQL)
TOCTitle: DROP USER or GROUP statement (Microsoft Access SQL)
ms:assetid: 46bc5916-556b-17df-2f4c-8fd7bbd21ef7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193192(v=office.15)
ms:contentKeyID: 48544575
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 995f935ceea5af3b740215c5a4137e02e7ebb1b2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293644"
---
# <a name="drop-user-or-group-statement-microsoft-access-sql"></a><span data-ttu-id="76c8b-102">DROP USER-oder GROUP-Anweisung (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="76c8b-102">DROP USER or GROUP statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="76c8b-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="76c8b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="76c8b-104">Löscht einen oder mehrere vorhandene *Benutzer* oder *Gruppen*oder entfernt einen oder mehrere vorhandene *Benutzer* aus einer vorhandenen *Gruppe*.</span><span class="sxs-lookup"><span data-stu-id="76c8b-104">Deletes one or more existing *users* or *groups*, or removes one or more existing *users* from an existing *group*.</span></span>

## <a name="syntax"></a><span data-ttu-id="76c8b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="76c8b-105">Syntax</span></span>

### <a name="delete-one-or-more-users-or-remove-one-or-more-users-from-a-group"></a><span data-ttu-id="76c8b-106">Löschen eines oder mehrerer Benutzer oder Entfernen eines oder mehrerer Benutzer aus einer Gruppe</span><span class="sxs-lookup"><span data-stu-id="76c8b-106">Delete one or more users or remove one or more users from a group</span></span>

<span data-ttu-id="76c8b-107">Benutzer Benutzer \*\*\[, Benutzer \*\*,... \] \[ \*\*\]</span><span class="sxs-lookup"><span data-stu-id="76c8b-107">DROP USER *user*\[, *user*, …\] \[FROM *group*\]</span></span>

### <a name="delete-one-or-more-groups"></a><span data-ttu-id="76c8b-108">Löschen einer oder mehrerer Gruppen</span><span class="sxs-lookup"><span data-stu-id="76c8b-108">Delete one or more groups</span></span>

<span data-ttu-id="76c8b-109">Drop Group *Group*\[, *Group*,...\]</span><span class="sxs-lookup"><span data-stu-id="76c8b-109">DROP GROUP *group*\[, *group*, …\]</span></span>

<span data-ttu-id="76c8b-110">Die DROP USER- oder GROUP-Anweisung besteht aus folgenden Komponenten:</span><span class="sxs-lookup"><span data-stu-id="76c8b-110">The DROP USER or GROUP statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="76c8b-111">Teil</span><span class="sxs-lookup"><span data-stu-id="76c8b-111">Part</span></span></p></th>
<th><p><span data-ttu-id="76c8b-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="76c8b-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="76c8b-113"><em>user</em></span><span class="sxs-lookup"><span data-stu-id="76c8b-113"><em>user</em></span></span></p></td>
<td><p><span data-ttu-id="76c8b-114">Der Name eines Benutzers, der aus der Informationsdatei für die Arbeitsgruppe entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="76c8b-114">The name of a user to be removed from the workgroup information file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="76c8b-115"><em>group</em></span><span class="sxs-lookup"><span data-stu-id="76c8b-115"><em>group</em></span></span></p></td>
<td><p><span data-ttu-id="76c8b-116">Der Name einer Gruppe, die aus der Informationsdatei für die Arbeitsgruppe entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="76c8b-116">The name of a group to be removed from the workgroup information file.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="76c8b-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="76c8b-117">Remarks</span></span>

<span data-ttu-id="76c8b-118">Wenn das FROM-Schlüsselwort in der DROP USER-Anweisung verwendet wird, werden alle in der Anweisung aufgeführten *Benutzer* aus der nach dem Schlüsselwort from angegebenen *Gruppe* entfernt.</span><span class="sxs-lookup"><span data-stu-id="76c8b-118">If the FROM keyword is used in the DROP USER statement, each of the *users* listed in the statement will be removed from the *group* specified following the FROM keyword.</span></span> <span data-ttu-id="76c8b-119">Die *Benutzer* selbst werden jedoch nicht gelöscht.</span><span class="sxs-lookup"><span data-stu-id="76c8b-119">However, the *users* themselves will not be deleted.</span></span>

<span data-ttu-id="76c8b-120">Die DROP GROUP-Anweisung dient zum Löschen der angegebenen *Grupppe*(n).</span><span class="sxs-lookup"><span data-stu-id="76c8b-120">The DROP GROUP statement will delete the specified *group*(s).</span></span> <span data-ttu-id="76c8b-121">Die *Benutzer* , die Mitglieder der *Gruppe*(n) sind, sind nicht betroffen, Sie sind jedoch nicht mehr Mitglied der gelöschten *Gruppe*(n).</span><span class="sxs-lookup"><span data-stu-id="76c8b-121">The *users* who are members of the *group*(s) will not be affected, but they will no longer be members of the deleted *group*(s).</span></span>

