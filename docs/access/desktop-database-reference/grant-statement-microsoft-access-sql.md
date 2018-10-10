---
title: GRANT-Anweisung (Microsoft Access SQL)
TOCTitle: GRANT Statement (Microsoft Access SQL)
ms:assetid: 50ae97ae-d5be-57e5-d9da-f3fc42f01d83
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193820(v=office.15)
ms:contentKeyID: 48544800
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277478
f1_categories:
- Office.Version=v15
ms.openlocfilehash: d4fffc9ac40586be899de0dd4054ba39dd3a6489
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25472668"
---
# <a name="grant-statement-microsoft-access-sql"></a><span data-ttu-id="c930b-102">GRANT-Anweisung (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="c930b-102">GRANT Statement (Microsoft Access SQL)</span></span>


<span data-ttu-id="c930b-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="c930b-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="c930b-104">Erteilt Rechte für einen vorhandenen Benutzer oder ein vorhandene Gruppe.</span><span class="sxs-lookup"><span data-stu-id="c930b-104">Grants specific privileges to an existing user or group.</span></span>

## <a name="syntax"></a><span data-ttu-id="c930b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c930b-105">Syntax</span></span>

<span data-ttu-id="c930b-106">GRANT {*Recht*\[, *Berechtigung*,... \]} ON {Tabelle *Tabelle* | OBJECT- *Objekt*|</span><span class="sxs-lookup"><span data-stu-id="c930b-106">GRANT {*privilege*\[, *privilege*, …\]} ON{TABLE *table* | OBJECT *object*|</span></span>

<span data-ttu-id="c930b-107">CONTAINER *Container* } TO {*autorisierungsname*\[, *autorisierungsname*,... \]}</span><span class="sxs-lookup"><span data-stu-id="c930b-107">CONTAINER *container* } TO {*authorizationname*\[, *authorizationname*, …\]}</span></span>

<span data-ttu-id="c930b-108">Die GRANT-Anweisung besteht aus folgenden Komponenten:</span><span class="sxs-lookup"><span data-stu-id="c930b-108">The GRANT statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c930b-109">Komponente</span><span class="sxs-lookup"><span data-stu-id="c930b-109">Part</span></span></p></th>
<th><p><span data-ttu-id="c930b-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c930b-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c930b-111"><em>Berechtigung</em></span><span class="sxs-lookup"><span data-stu-id="c930b-111"><em>privilege</em></span></span></p></td>
<td><p><span data-ttu-id="c930b-112">Der geringsten Rechte oder Berechtigungen erteilt werden.</span><span class="sxs-lookup"><span data-stu-id="c930b-112">The privilege or privileges to be granted.</span></span> <span data-ttu-id="c930b-113">Berechtigungen werden mithilfe der folgenden Schlüsselwörter angegeben: auswählen, löschen, einfügen, aktualisieren und DROP, SELECTSECURITY, UPDATESECURITY, DBPASSWORD, UPDATEIDENTITY, CREATE, SELECTSCHEMA, SCHEMA und UPDATEOWNER.</span><span class="sxs-lookup"><span data-stu-id="c930b-113">Privileges are specified using the following keywords: SELECT, DELETE, INSERT, UPDATE, DROP, SELECTSECURITY, UPDATESECURITY, DBPASSWORD, UPDATEIDENTITY, CREATE, SELECTSCHEMA, SCHEMA and UPDATEOWNER.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c930b-114"><em>Tabellenname</em></span><span class="sxs-lookup"><span data-stu-id="c930b-114"><em>tablename</em></span></span></p></td>
<td><p><span data-ttu-id="c930b-115">Ein gültiger Tabellenname.</span><span class="sxs-lookup"><span data-stu-id="c930b-115">Any valid table name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c930b-116"><em>Objekt</em></span><span class="sxs-lookup"><span data-stu-id="c930b-116"><em>object</em></span></span></p></td>
<td><p><span data-ttu-id="c930b-p102">Dies kann jedes Objekt sein, das nicht aus einer Tabelle stammt. Ein Beispiel ist eine gespeicherte Abfrage (Sicht oder Prozedur).</span><span class="sxs-lookup"><span data-stu-id="c930b-p102">This can encompass any non-table object. A stored query (view or procedure) is one example.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c930b-119"><em>Container</em></span><span class="sxs-lookup"><span data-stu-id="c930b-119"><em>container</em></span></span></p></td>
<td><p><span data-ttu-id="c930b-120">Der Name eines gültigen Containers.</span><span class="sxs-lookup"><span data-stu-id="c930b-120">The name of a valid container.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c930b-121"><em>Autorisierungsname</em></span><span class="sxs-lookup"><span data-stu-id="c930b-121"><em>authorizationname</em></span></span></p></td>
<td><p><span data-ttu-id="c930b-122">Ein Benutzer- oder Gruppenname.</span><span class="sxs-lookup"><span data-stu-id="c930b-122">A user or group name.</span></span></p></td>
</tr>
</tbody>
</table>

