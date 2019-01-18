---
title: CREATE USER- oder GROUP-Anweisung (Microsoft Access SQL)
TOCTitle: CREATE USER or GROUP statement (Microsoft Access SQL)
ms:assetid: 62148ce2-0f81-944e-a1ab-edef990fff9f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194914(v=office.15)
ms:contentKeyID: 48545229
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5b294af16498778eae94b38a7a31b93fd029585e
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28710923"
---
# <a name="create-user-or-group-statement-microsoft-access-sql"></a><span data-ttu-id="bf985-102">CREATE USER- oder GROUP-Anweisung (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="bf985-102">CREATE USER or GROUP statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="bf985-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="bf985-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="bf985-104">Erstellt einen oder mehrere neue Benutzer bzw. eine oder mehrere neue Gruppen.</span><span class="sxs-lookup"><span data-stu-id="bf985-104">Creates one or more new users or groups.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf985-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="bf985-105">Syntax</span></span>

### <a name="create-a-user"></a><span data-ttu-id="bf985-106">Erstellen eines Benutzers</span><span class="sxs-lookup"><span data-stu-id="bf985-106">Create a user</span></span>

<span data-ttu-id="bf985-107">CREATE USER *Benutzer* *Kennwort pid* \[, *Benutzer* *Kennwort pid*,...\]</span><span class="sxs-lookup"><span data-stu-id="bf985-107">CREATE USER *user* *password pid* \[, *user* *password pid*, …\]</span></span>

### <a name="create-a-group"></a><span data-ttu-id="bf985-108">Erstellen einer Gruppe</span><span class="sxs-lookup"><span data-stu-id="bf985-108">Create a group</span></span>

<span data-ttu-id="bf985-109">CREATE GROUP *Gruppe* *pid*\[, *Gruppe* *pid*,...\]</span><span class="sxs-lookup"><span data-stu-id="bf985-109">CREATE GROUP *group* *pid*\[, *group* *pid*, …\]</span></span>

<span data-ttu-id="bf985-110">Die CREATE USER- oder GROUP-Anweisung besteht aus folgenden Komponenten:</span><span class="sxs-lookup"><span data-stu-id="bf985-110">The CREATE USER or GROUP statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bf985-111">Komponente</span><span class="sxs-lookup"><span data-stu-id="bf985-111">Part</span></span></p></th>
<th><p><span data-ttu-id="bf985-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bf985-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bf985-113"><em>Benutzer</em></span><span class="sxs-lookup"><span data-stu-id="bf985-113"><em>user</em></span></span></p></td>
<td><p><span data-ttu-id="bf985-114">Der Name eines Benutzers, der der Arbeitsgruppen-Informationsdatei hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="bf985-114">The name of a user to be added to the workgroup information file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf985-115"><em>group</em></span><span class="sxs-lookup"><span data-stu-id="bf985-115"><em>group</em></span></span></p></td>
<td><p><span data-ttu-id="bf985-116">Der Name einer Gruppe, der zur Informationsdatei der Arbeitsgruppe hinzuzufügen ist.</span><span class="sxs-lookup"><span data-stu-id="bf985-116">The name of a group to be added to the workgroup information file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bf985-117"><em>password</em></span><span class="sxs-lookup"><span data-stu-id="bf985-117"><em>password</em></span></span></p></td>
<td><p><span data-ttu-id="bf985-118">Das Kennwort, das dem angegebenen <em>Benutzer</em> zuzuordnen ist.</span><span class="sxs-lookup"><span data-stu-id="bf985-118">The password to be associated with the specified <em>user</em> name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf985-119"><em>PID</em></span><span class="sxs-lookup"><span data-stu-id="bf985-119"><em>pid</em></span></span></p></td>
<td><p><span data-ttu-id="bf985-120">Die persönliche ID.</span><span class="sxs-lookup"><span data-stu-id="bf985-120">The personal id.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="bf985-121">Hinweise</span><span class="sxs-lookup"><span data-stu-id="bf985-121">Remarks</span></span>

<span data-ttu-id="bf985-122">Ein *Benutzer* und eine *Gruppe* können nicht den gleichen Namen haben.</span><span class="sxs-lookup"><span data-stu-id="bf985-122">A *user* and a *group* cannot have the same name.</span></span>

<span data-ttu-id="bf985-123">Ein *Kennwort* ist erforderlich für jeden *Benutzer* oder *Gruppe* , die erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="bf985-123">A *password* is required for each *user* or *group* that is created.</span></span>

