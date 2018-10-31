---
title: DROP USER- oder GROUP-Anweisung (Microsoft Access SQL)
TOCTitle: DROP USER or GROUP statement (Microsoft Access SQL)
ms:assetid: 46bc5916-556b-17df-2f4c-8fd7bbd21ef7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193192(v=office.15)
ms:contentKeyID: 48544575
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: a7988a2124af13dc84cefe678342da969e349a06
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25864029"
---
# <a name="drop-user-or-group-statement-microsoft-access-sql"></a><span data-ttu-id="093d5-102">DROP USER- oder GROUP-Anweisung (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="093d5-102">DROP USER or GROUP statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="093d5-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="093d5-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="093d5-104">Löscht eine oder mehrere vorhandene *Benutzer* oder *Gruppen*, oder einen oder mehrere vorhandene *Benutzer* aus einer vorhandenen *Gruppe*entfernt.</span><span class="sxs-lookup"><span data-stu-id="093d5-104">Deletes one or more existing *users* or *groups*, or removes one or more existing *users* from an existing *group*.</span></span>

## <a name="syntax"></a><span data-ttu-id="093d5-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="093d5-105">Syntax</span></span>

<span data-ttu-id="093d5-106">**Löschen Sie einen oder mehrere _Benutzer_ oder eine oder mehrere _Benutzer_ aus einer _Gruppe_entfernen**:</span><span class="sxs-lookup"><span data-stu-id="093d5-106">**Delete one or more _users_ or remove one or more _users_ from a _group_**:</span></span>

<span data-ttu-id="093d5-107">DROP USER *Benutzer*\[, *Benutzer*,... \] \[Aus *Gruppe*\]</span><span class="sxs-lookup"><span data-stu-id="093d5-107">DROP USER *user*\[, *user*, …\] \[FROM *group*\]</span></span>

<span data-ttu-id="093d5-108">**Löschen einer oder mehrerer _Gruppen_**:</span><span class="sxs-lookup"><span data-stu-id="093d5-108">**Delete one or more _groups_**:</span></span>

<span data-ttu-id="093d5-109">DROP GROUP *Gruppe*\[, *Gruppe*,...\]</span><span class="sxs-lookup"><span data-stu-id="093d5-109">DROP GROUP *group*\[, *group*, …\]</span></span>

<span data-ttu-id="093d5-110">Die DROP USER- oder GROUP-Anweisung besteht aus folgenden Komponenten:</span><span class="sxs-lookup"><span data-stu-id="093d5-110">The DROP USER or GROUP statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="093d5-111">Komponente</span><span class="sxs-lookup"><span data-stu-id="093d5-111">Part</span></span></p></th>
<th><p><span data-ttu-id="093d5-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="093d5-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="093d5-113"><em>Benutzer</em></span><span class="sxs-lookup"><span data-stu-id="093d5-113"><em>user</em></span></span></p></td>
<td><p><span data-ttu-id="093d5-114">Der Name eines Benutzers, der aus der Informationsdatei für die Arbeitsgruppe entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="093d5-114">The name of a user to be removed from the workgroup information file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="093d5-115"><em>Gruppe</em></span><span class="sxs-lookup"><span data-stu-id="093d5-115"><em>group</em></span></span></p></td>
<td><p><span data-ttu-id="093d5-116">Der Name einer Gruppe, die aus der Informationsdatei für die Arbeitsgruppe entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="093d5-116">The name of a group to be removed from the workgroup information file.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="093d5-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="093d5-117">Remarks</span></span>

<span data-ttu-id="093d5-118">Wenn das FROM-Schlüsselwort in der DROP USER-Anweisung verwendet wird, wird jeder in der Anweisung aufgeführte *Benutzer* aus der *Gruppe* angegeben nach der FROM-Schlüsselwort entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="093d5-118">If the FROM keyword is used in the DROP USER statement, each of the *users* listed in the statement will be removed from the *group* specified following the FROM keyword.</span></span> <span data-ttu-id="093d5-119">Jedoch die *Benutzer* selbst nicht gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="093d5-119">However, the *users* themselves will not be deleted.</span></span>

<span data-ttu-id="093d5-120">Die DROP GROUP-Anweisung löscht die angegebene *Gruppe*(s).</span><span class="sxs-lookup"><span data-stu-id="093d5-120">The DROP GROUP statement will delete the specified *group*(s).</span></span> <span data-ttu-id="093d5-121">Der *Benutzer* , die Mitglieder der *Gruppe*(s) sind nicht betroffen sind, aber sie werden nicht mehr Mitglieder der gelöschten *Gruppe*(s).</span><span class="sxs-lookup"><span data-stu-id="093d5-121">The *users* who are members of the *group*(s) will not be affected, but they will no longer be members of the deleted *group*(s).</span></span>

