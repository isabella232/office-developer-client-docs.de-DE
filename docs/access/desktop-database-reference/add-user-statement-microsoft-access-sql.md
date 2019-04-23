---
title: ADD USER-Anweisung (Microsoft Access SQL)
TOCTitle: ADD USER statement (Microsoft Access SQL)
ms:assetid: 1feb631f-cb8c-14ae-6214-276f1faf1a55
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845862(v=office.15)
ms:contentKeyID: 48543652
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8ba60a646fd234748bcc39b9a5604a33675caee5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280425"
---
# <a name="add-user-statement-microsoft-access-sql"></a><span data-ttu-id="060c3-102">ADD USER-Anweisung (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="060c3-102">ADD USER statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="060c3-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="060c3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="060c3-104">Fügt einer bestehenden *Gruppe* einen oder mehrere *Benutzer* hinzu.</span><span class="sxs-lookup"><span data-stu-id="060c3-104">Adds one or more existing *user*s to an existing *group*.</span></span>

## <a name="syntax"></a><span data-ttu-id="060c3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="060c3-105">Syntax</span></span>

<span data-ttu-id="060c3-106">Hinzufügen \*\*\[von Benutzer \*\* Benutzer, Benutzer,... \] Zur *Gruppe*</span><span class="sxs-lookup"><span data-stu-id="060c3-106">ADD USER *user*\[, *user*, …\] TO *group*</span></span>

<span data-ttu-id="060c3-107">Die ADD USER-Anweisung besteht aus den folgenden Komponenten:</span><span class="sxs-lookup"><span data-stu-id="060c3-107">The ADD USER statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="060c3-108">Teil</span><span class="sxs-lookup"><span data-stu-id="060c3-108">Part</span></span></p></th>
<th><p><span data-ttu-id="060c3-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="060c3-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="060c3-110"><em>user</em></span><span class="sxs-lookup"><span data-stu-id="060c3-110"><em>user</em></span></span></p></td>
<td><p><span data-ttu-id="060c3-111">Der Name eines Benutzers, der zur Informationsdatei der Arbeitsgruppe hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="060c3-111">The name of a user to be added to the workgroup information file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="060c3-112"><em>group</em></span><span class="sxs-lookup"><span data-stu-id="060c3-112"><em>group</em></span></span></p></td>
<td><p><span data-ttu-id="060c3-113">Der Name einer Gruppe, der zur Informationsdatei der Arbeitsgruppe hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="060c3-113">The name of a group to be added to the workgroup information file.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="060c3-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="060c3-114">Remarks</span></span>

<span data-ttu-id="060c3-115">Nachdem ein *Benutzer* einer *Gruppe*hinzugefügt wurde, verfügt der *Benutzer* über alle Berechtigungen, die der *Gruppe*erteilt wurden.</span><span class="sxs-lookup"><span data-stu-id="060c3-115">After a *user* had been added to a *group*, the *user* has all the permissions that have been granted to the *group*.</span></span>

