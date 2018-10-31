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
ms.openlocfilehash: 4bcdd7aa77823a53ba2a2c0cde4badbac571611a
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25860546"
---
# <a name="revoke-statement-microsoft-access-sql"></a><span data-ttu-id="f0033-102">REVOKE-Anweisung (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="f0033-102">REVOKE statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="f0033-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="f0033-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="f0033-104">Widerruft bestimmte Berechtigungen eines vorhandenen Benutzers oder einer Gruppe.</span><span class="sxs-lookup"><span data-stu-id="f0033-104">Revokes specific privileges from an existing user or group.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0033-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f0033-105">Syntax</span></span>

<span data-ttu-id="f0033-106">REVOKE {*Berechtigung*\[, *Berechtigung*,... \]} ON {Tabelle *Tabelle* | OBJECT- *Objekt*|</span><span class="sxs-lookup"><span data-stu-id="f0033-106">REVOKE {*privilege*\[, *privilege*, …\]} ON {TABLE *table* | OBJECT *object*|</span></span>

<span data-ttu-id="f0033-107">CONTAINTER *Container*} FROM {*autorisierungsname*\[, *autorisierungsname*,... \]}</span><span class="sxs-lookup"><span data-stu-id="f0033-107">CONTAINTER *container*} FROM {*authorizationname*\[, *authorizationname*, …\]}</span></span>

<span data-ttu-id="f0033-108">Die REVOKE-Anweisung enthält folgende Bestandteile:</span><span class="sxs-lookup"><span data-stu-id="f0033-108">The REVOKE statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f0033-109">Argument</span><span class="sxs-lookup"><span data-stu-id="f0033-109">Part</span></span></p></th>
<th><p><span data-ttu-id="f0033-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f0033-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f0033-111"><em>Berechtigung</em></span><span class="sxs-lookup"><span data-stu-id="f0033-111"><em>privilege</em></span></span></p></td>
<td><p><span data-ttu-id="f0033-112">Der geringsten Rechte oder Berechtigungen, die widerrufen werden.</span><span class="sxs-lookup"><span data-stu-id="f0033-112">The privilege or privileges to be revoked.</span></span> <span data-ttu-id="f0033-113">Berechtigungen werden mithilfe der folgenden Schlüsselwörter angegeben: auswählen, DELETE, INSERT, UPDATE, DROP, SELECTSECURITY, UPDATESECURITY, DBPASSWORD, UPDATEIDENTITY, erstellen, SELECTSCHEMA, SCHEMA und UPDATEOWNER.</span><span class="sxs-lookup"><span data-stu-id="f0033-113">Privileges are specified using the following keywords: SELECT, DELETE, INSERT, UPDATE, DROP, SELECTSECURITY, UPDATESECURITY, DBPASSWORD, UPDATEIDENTITY, CREATE, SELECTSCHEMA, SCHEMA, and UPDATEOWNER.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f0033-114"><em>Tabelle</em></span><span class="sxs-lookup"><span data-stu-id="f0033-114"><em>table</em></span></span></p></td>
<td><p><span data-ttu-id="f0033-115">Ein gültiger Tabellenname.</span><span class="sxs-lookup"><span data-stu-id="f0033-115">Any valid table name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f0033-116"><em>Objekt</em></span><span class="sxs-lookup"><span data-stu-id="f0033-116"><em>object</em></span></span></p></td>
<td><p><span data-ttu-id="f0033-p102">Dies kann jedes Objekt sein, das nicht aus einer Tabelle stammt. Ein Beispiel ist eine gespeicherte Abfrage (Sicht oder Prozedur).</span><span class="sxs-lookup"><span data-stu-id="f0033-p102">This can encompass any non-table object. A stored query (view or procedure) is one example.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f0033-119"><em>Container</em></span><span class="sxs-lookup"><span data-stu-id="f0033-119"><em>container</em></span></span></p></td>
<td><p><span data-ttu-id="f0033-120">Der Name eines gültigen Containers.</span><span class="sxs-lookup"><span data-stu-id="f0033-120">The name of a valid container.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f0033-121"><em>Autorisierungsname</em></span><span class="sxs-lookup"><span data-stu-id="f0033-121"><em>authorizationname</em></span></span></p></td>
<td><p><span data-ttu-id="f0033-122">Ein Benutzer- oder Gruppenname.</span><span class="sxs-lookup"><span data-stu-id="f0033-122">A user or group name.</span></span></p></td>
</tr>
</tbody>
</table>

