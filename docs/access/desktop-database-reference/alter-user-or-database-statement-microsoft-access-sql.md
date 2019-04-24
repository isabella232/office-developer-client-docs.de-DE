---
title: ALTER USER-oder DATABASE-Anweisung (Microsoft Access SQL)
TOCTitle: ALTER USER or DATABASE statement (Microsoft Access SQL)
ms:assetid: 86ccd296-5171-97e7-683f-cdaab4bde9ab
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197012(v=office.15)
ms:contentKeyID: 48546093
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2514ca6403ce70acae9e344d610fbd7b9ba7d73b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297179"
---
# <a name="alter-user-or-database-statement-microsoft-access-sql"></a><span data-ttu-id="3d2d1-102">ALTER USER-oder DATABASE-Anweisung (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="3d2d1-102">ALTER USER or DATABASE statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="3d2d1-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3d2d1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3d2d1-104">Ändert das Kennwort für einen vorhandenen Benutzer oder eine Datenbank.</span><span class="sxs-lookup"><span data-stu-id="3d2d1-104">Changes the password for an existing user or for a database.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d2d1-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3d2d1-105">Syntax</span></span>

<span data-ttu-id="3d2d1-106">ALTER DATABASE PASSWORD *NeuesKennwort AltesKennwort*</span><span class="sxs-lookup"><span data-stu-id="3d2d1-106">ALTER DATABASE PASSWORD *newpassword oldpassword*</span></span>

<span data-ttu-id="3d2d1-107">ALTER USER *Benutzer* PASSWORD *NeuesKennwort AltesKennwort*</span><span class="sxs-lookup"><span data-stu-id="3d2d1-107">ALTER USER *user* PASSWORD *newpassword oldpassword*</span></span>

<span data-ttu-id="3d2d1-108">Die ALTER USER- oder DATABASE-Anweisung besteht aus den folgenden Komponenten:</span><span class="sxs-lookup"><span data-stu-id="3d2d1-108">The ALTER USER or DATABASE statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3d2d1-109">Teil</span><span class="sxs-lookup"><span data-stu-id="3d2d1-109">Part</span></span></p></th>
<th><p><span data-ttu-id="3d2d1-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3d2d1-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3d2d1-111"><em>user</em></span><span class="sxs-lookup"><span data-stu-id="3d2d1-111"><em>user</em></span></span></p></td>
<td><p><span data-ttu-id="3d2d1-112">Der Name eines Benutzers, der der Arbeitsgruppen-Informationsdatei hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="3d2d1-112">The name of a user to be added to the workgroup information file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3d2d1-113"><em>NewPassword</em></span><span class="sxs-lookup"><span data-stu-id="3d2d1-113"><em>newpassword</em></span></span></p></td>
<td><p><span data-ttu-id="3d2d1-114">Das neue Kennwort, das dem <em>Benutzer</em> oder der <em>Datenbank</em> zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="3d2d1-114">The new password to be associated with the specified <em>user</em> or <em>database</em> name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3d2d1-115"><em>oldPassword</em></span><span class="sxs-lookup"><span data-stu-id="3d2d1-115"><em>oldpassword</em></span></span></p></td>
<td><p><span data-ttu-id="3d2d1-116">Das bestehende Kennwort, das dem angegebenen <em>Benutzer</em> oder der angegebenen <em>Gruppe</em> zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="3d2d1-116">The existing password to be associated with the specified <em>user</em> or <em>group</em> name.</span></span></p></td>
</tr>
</tbody>
</table>

