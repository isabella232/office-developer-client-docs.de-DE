---
title: GRANT-Anweisung (Microsoft Access SQL)
TOCTitle: GRANT statement (Microsoft Access SQL)
ms:assetid: 50ae97ae-d5be-57e5-d9da-f3fc42f01d83
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193820(v=office.15)
ms:contentKeyID: 48544800
ms.date: 10/18/2018
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277478
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 4357099f8bcb9b2308b5cda3543949765b8c3420
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292132"
---
# <a name="grant-statement-microsoft-access-sql"></a><span data-ttu-id="8050b-102">GRANT-Anweisung (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="8050b-102">GRANT statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="8050b-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8050b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8050b-104">Erteilt Rechte für einen vorhandenen Benutzer oder ein vorhandene Gruppe.</span><span class="sxs-lookup"><span data-stu-id="8050b-104">Grants specific privileges to an existing user or group.</span></span>

## <a name="syntax"></a><span data-ttu-id="8050b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8050b-105">Syntax</span></span>

<span data-ttu-id="8050b-106">Grant {*Berechtigung*\[, *Privileg*,... \]} On {Table *Tabelle* | Objekt *Objekt*|</span><span class="sxs-lookup"><span data-stu-id="8050b-106">GRANT {*privilege*\[, *privilege*, …\]} ON{TABLE *table* | OBJECT *object*|</span></span>

<span data-ttu-id="8050b-107">Container *Container* } an {*authorizationname*\[, *authorizationname*,... \]}</span><span class="sxs-lookup"><span data-stu-id="8050b-107">CONTAINER *container* } TO {*authorizationname*\[, *authorizationname*, …\]}</span></span>

<span data-ttu-id="8050b-108">Die GRANT-Anweisung besteht aus folgenden Komponenten:</span><span class="sxs-lookup"><span data-stu-id="8050b-108">The GRANT statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8050b-109">Teil</span><span class="sxs-lookup"><span data-stu-id="8050b-109">Part</span></span></p></th>
<th><p><span data-ttu-id="8050b-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8050b-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8050b-111"><em>Berechtigungen</em></span><span class="sxs-lookup"><span data-stu-id="8050b-111"><em>privilege</em></span></span></p></td>
<td><p><span data-ttu-id="8050b-112">Das oder die zu erteilenden Rechte.</span><span class="sxs-lookup"><span data-stu-id="8050b-112">The privilege or privileges to be granted.</span></span> <span data-ttu-id="8050b-113">Berechtigungen werden mithilfe der folgenden Schlüsselwörter angegeben: SELECT, DELETE, INSERT, UPDATE, DROP, SELECTSECURITY, UPDATESECURITY, dbPASSWORD, UPDATEIDENTITY, CREATE, SELECTSCHEMA, SCHEMA und UPDATEOWNER.</span><span class="sxs-lookup"><span data-stu-id="8050b-113">Privileges are specified using the following keywords: SELECT, DELETE, INSERT, UPDATE, DROP, SELECTSECURITY, UPDATESECURITY, DBPASSWORD, UPDATEIDENTITY, CREATE, SELECTSCHEMA, SCHEMA, and UPDATEOWNER.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8050b-114"><em>TableName</em></span><span class="sxs-lookup"><span data-stu-id="8050b-114"><em>tablename</em></span></span></p></td>
<td><p><span data-ttu-id="8050b-115">Ein gültiger Tabellenname.</span><span class="sxs-lookup"><span data-stu-id="8050b-115">Any valid table name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8050b-116"><em>object</em></span><span class="sxs-lookup"><span data-stu-id="8050b-116"><em>object</em></span></span></p></td>
<td><p><span data-ttu-id="8050b-117">Ein Objekt kann jedes Objekt umfassen, bei dem es sich nicht um eine Tabelle handelt.</span><span class="sxs-lookup"><span data-stu-id="8050b-117">This can encompass any non-table object.</span></span> <span data-ttu-id="8050b-118">Beispiele für solche Objekte sind gespeicherte Abfragen, Sichten oder Prozeduren.</span><span class="sxs-lookup"><span data-stu-id="8050b-118">A stored query (view or procedure) is one example.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8050b-119"><em>Container</em></span><span class="sxs-lookup"><span data-stu-id="8050b-119"><em>container</em></span></span></p></td>
<td><p><span data-ttu-id="8050b-120">Der Name eines gültigen Containers.</span><span class="sxs-lookup"><span data-stu-id="8050b-120">The name of a valid container.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8050b-121"><em>Autorisierungsname</em></span><span class="sxs-lookup"><span data-stu-id="8050b-121"><em>authorizationname</em></span></span></p></td>
<td><p><span data-ttu-id="8050b-122">Der Name eines Benutzers oder einer Gruppe.</span><span class="sxs-lookup"><span data-stu-id="8050b-122">A user or group name.</span></span></p></td>
</tr>
</tbody>
</table>

