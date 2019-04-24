---
title: REVOKE-Anweisung (Microsoft Access SQL)
TOCTitle: REVOKE statement (Microsoft Access SQL)
ms:assetid: 69399fd6-c4e8-f2e2-e5f4-48ae779323f5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195272(v=office.15)
ms:contentKeyID: 48545409
ms.date: 10/18/2018
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277479
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 20122fee617597987940766a076d5f968a87c2d2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306531"
---
# <a name="revoke-statement-microsoft-access-sql"></a><span data-ttu-id="5dc1d-102">REVOKE-Anweisung (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="5dc1d-102">REVOKE statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="5dc1d-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5dc1d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5dc1d-104">Widerruft bestimmte Berechtigungen eines vorhandenen Benutzers oder einer Gruppe.</span><span class="sxs-lookup"><span data-stu-id="5dc1d-104">Revokes specific privileges from an existing user or group.</span></span>

## <a name="syntax"></a><span data-ttu-id="5dc1d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5dc1d-105">Syntax</span></span>

<span data-ttu-id="5dc1d-106">REVOKE {*Privilege*\[, *Privileg*,... \]} On {Table *Tabelle* | Objekt *Objekt*|</span><span class="sxs-lookup"><span data-stu-id="5dc1d-106">REVOKE {*privilege*\[, *privilege*, …\]} ON {TABLE *table* | OBJECT *object*|</span></span>

<span data-ttu-id="5dc1d-107">*Container*für "beflecker"\*\*\[von {authorizationname, *authorizationname*,... \]}</span><span class="sxs-lookup"><span data-stu-id="5dc1d-107">CONTAINTER *container*} FROM {*authorizationname*\[, *authorizationname*, …\]}</span></span>

<span data-ttu-id="5dc1d-108">Die REVOKE-Anweisung enthält folgende Bestandteile:</span><span class="sxs-lookup"><span data-stu-id="5dc1d-108">The REVOKE statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5dc1d-109">Teil</span><span class="sxs-lookup"><span data-stu-id="5dc1d-109">Part</span></span></p></th>
<th><p><span data-ttu-id="5dc1d-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5dc1d-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5dc1d-111"><em>Berechtigungen</em></span><span class="sxs-lookup"><span data-stu-id="5dc1d-111"><em>privilege</em></span></span></p></td>
<td><p><span data-ttu-id="5dc1d-112">Die zu widerrufenden Berechtigungen.</span><span class="sxs-lookup"><span data-stu-id="5dc1d-112">The privilege or privileges to be revoked.</span></span> <span data-ttu-id="5dc1d-113">Berechtigungen werden mithilfe der folgenden Schlüsselwörter angegeben: SELECT, DELETE, INSERT, UPDATE, DROP, SELECTSECURITY, UPDATESECURITY, dbPASSWORD, UPDATEIDENTITY, CREATE, SELECTSCHEMA, SCHEMA und UPDATEOWNER.</span><span class="sxs-lookup"><span data-stu-id="5dc1d-113">Privileges are specified using the following keywords: SELECT, DELETE, INSERT, UPDATE, DROP, SELECTSECURITY, UPDATESECURITY, DBPASSWORD, UPDATEIDENTITY, CREATE, SELECTSCHEMA, SCHEMA, and UPDATEOWNER.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dc1d-114"><em>table</em></span><span class="sxs-lookup"><span data-stu-id="5dc1d-114"><em>table</em></span></span></p></td>
<td><p><span data-ttu-id="5dc1d-115">Ein gültiger Tabellenname.</span><span class="sxs-lookup"><span data-stu-id="5dc1d-115">Any valid table name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dc1d-116"><em>object</em></span><span class="sxs-lookup"><span data-stu-id="5dc1d-116"><em>object</em></span></span></p></td>
<td><p><span data-ttu-id="5dc1d-117">Ein Objekt kann jedes Objekt umfassen, bei dem es sich nicht um eine Tabelle handelt.</span><span class="sxs-lookup"><span data-stu-id="5dc1d-117">This can encompass any non-table object.</span></span> <span data-ttu-id="5dc1d-118">Beispiele für solche Objekte sind gespeicherte Abfragen, Sichten oder Prozeduren.</span><span class="sxs-lookup"><span data-stu-id="5dc1d-118">A stored query (view or procedure) is one example.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dc1d-119"><em>Container</em></span><span class="sxs-lookup"><span data-stu-id="5dc1d-119"><em>container</em></span></span></p></td>
<td><p><span data-ttu-id="5dc1d-120">Der Name eines gültigen Containers.</span><span class="sxs-lookup"><span data-stu-id="5dc1d-120">The name of a valid container.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dc1d-121"><em>Autorisierungsname</em></span><span class="sxs-lookup"><span data-stu-id="5dc1d-121"><em>authorizationname</em></span></span></p></td>
<td><p><span data-ttu-id="5dc1d-122">Der Name eines Benutzers oder einer Gruppe.</span><span class="sxs-lookup"><span data-stu-id="5dc1d-122">A user or group name.</span></span></p></td>
</tr>
</tbody>
</table>

