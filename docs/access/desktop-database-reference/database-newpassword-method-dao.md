---
title: Database. neuPassword-Methode (DAO)
TOCTitle: NewPassword Method
ms:assetid: 01c1c454-d651-222c-225a-2b02734a1b7a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844754(v=office.15)
ms:contentKeyID: 48542941
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052943
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 20f09dbfba50526409472f7eb804ba2c47e4d1d5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294855"
---
# <a name="databasenewpassword-method-dao"></a><span data-ttu-id="1b35c-102">Database. neuPassword-Methode (DAO)</span><span class="sxs-lookup"><span data-stu-id="1b35c-102">Database.NewPassword method (DAO)</span></span>

<span data-ttu-id="1b35c-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1b35c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1b35c-104">Ändert das Kennwort einer vorhandenen Microsoft Access-Datenbank (gilt nur für Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="1b35c-104">Changes the password of an existing Microsoft Access database engine database (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="1b35c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1b35c-105">Syntax</span></span>

<span data-ttu-id="1b35c-106">*Ausdruck* . Neues Kennwort (***bstrOld***, ***bstrNew***)</span><span class="sxs-lookup"><span data-stu-id="1b35c-106">*expression* .NewPassword(***bstrOld***, ***bstrNew***)</span></span>

<span data-ttu-id="1b35c-107">*Ausdruck* Ein Ausdruck, der ein **Database** -Objekt zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="1b35c-107">*expression* An expression that returns a **Database** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="1b35c-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="1b35c-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1b35c-109">Name</span><span class="sxs-lookup"><span data-stu-id="1b35c-109">Name</span></span></p></th>
<th><p><span data-ttu-id="1b35c-110">Erforderlich/optional</span><span class="sxs-lookup"><span data-stu-id="1b35c-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="1b35c-111">Datentyp</span><span class="sxs-lookup"><span data-stu-id="1b35c-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="1b35c-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1b35c-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1b35c-113"><em>bstrOld</em></span><span class="sxs-lookup"><span data-stu-id="1b35c-113"><em>bstrOld</em></span></span></p></td>
<td><p><span data-ttu-id="1b35c-114">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="1b35c-114">Required</span></span></p></td>
<td><p><span data-ttu-id="1b35c-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="1b35c-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="1b35c-116">Die aktuelle Einstellung der <strong>Password</strong>-Eigenschaft des <strong>Database</strong>-Objekts.</span><span class="sxs-lookup"><span data-stu-id="1b35c-116">The current setting of the <strong>Password</strong> property of the <strong>Database</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1b35c-117"><em>bstrNew</em></span><span class="sxs-lookup"><span data-stu-id="1b35c-117"><em>bstrNew</em></span></span></p></td>
<td><p><span data-ttu-id="1b35c-118">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="1b35c-118">Required</span></span></p></td>
<td><p><span data-ttu-id="1b35c-119"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="1b35c-119"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="1b35c-120">Die neue Einstellung der <strong>Password</strong> -Eigenschaft des <strong>Database</strong> -Objekts.</span><span class="sxs-lookup"><span data-stu-id="1b35c-120">The new setting of the <strong>Password</strong> property of the <strong>Database</strong> object.</span></span></p>
<p><span data-ttu-id="1b35c-121"><strong>Hinweis</strong>: Verwenden Sie sichere Kennwörter, die Groß-und Kleinbuchstaben, Zahlen und Symbole kombinieren.</span><span class="sxs-lookup"><span data-stu-id="1b35c-121"><strong>NOTE</strong>: Use strong passwords that combine upper- and lowercase letters, numbers, and symbols.</span></span> <span data-ttu-id="1b35c-122">Unsichere Kennwörter kombinieren diese Elemente nicht.</span><span class="sxs-lookup"><span data-stu-id="1b35c-122">Weak passwords don't mix these elements.</span></span> <span data-ttu-id="1b35c-123">Sicheres Kennwort: Y6dh!et5.</span><span class="sxs-lookup"><span data-stu-id="1b35c-123">Strong password: Y6dh!et5.</span></span> <span data-ttu-id="1b35c-124">Schwaches Kennwort: House27.</span><span class="sxs-lookup"><span data-stu-id="1b35c-124">Weak password: House27.</span></span> <span data-ttu-id="1b35c-125">Verwenden Sie ein sicheres Kennwort, das Sie sich merken können, damit Sie es nicht aufschreiben müssen.</span><span class="sxs-lookup"><span data-stu-id="1b35c-125">Use a strong password that you can remember so that you don't have to write it down.</span></span></p>
</td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="1b35c-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1b35c-126">Remarks</span></span>

<span data-ttu-id="1b35c-127">Die Zeichenfolgen bstrOld und bstrNew können bis zu 20 Zeichen lang sein und alle Zeichen mit Ausnahme des ASCII-Zeichens 0 (null) enthalten.</span><span class="sxs-lookup"><span data-stu-id="1b35c-127">The bstrOld and bstrNew strings can be up to 20 characters long and can include any characters except the ASCII character 0 (null).</span></span> <span data-ttu-id="1b35c-128">Verwenden Sie zum Löschen des Kennworts eine leere Zeichenfolge ("") für bstrNew.</span><span class="sxs-lookup"><span data-stu-id="1b35c-128">To clear the password, use a zero-length string ("") for bstrNew.</span></span>

<span data-ttu-id="1b35c-129">Bei Kennwörtern wird Groß-/Kleinschreibung beachtet.</span><span class="sxs-lookup"><span data-stu-id="1b35c-129">Passwords are case-sensitive.</span></span>

<span data-ttu-id="1b35c-130">Wurde für eine Datenbank kein Kennwort festgelegt, erstellt das Microsoft Access-Datenbankmodul automatisch ein Kennwort, indem es eine leere Zeichenfolge ("") für das alte Kennwort übergibt.</span><span class="sxs-lookup"><span data-stu-id="1b35c-130">If a database has no password, the Microsoft Access database engine will automatically create one by passing a zero-length string ("") for the old password.</span></span>


> [!IMPORTANT]
> <span data-ttu-id="1b35c-131">[!WICHTIG] Wenn Sie das Kennwort verlieren, können Sie die Datenbank nicht mehr öffnen.</span><span class="sxs-lookup"><span data-stu-id="1b35c-131">If you lose your password, you can never open the database again.</span></span>


