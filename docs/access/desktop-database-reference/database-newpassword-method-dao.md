---
title: Database.NewPassword Method (DAO)
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
ms.openlocfilehash: 892dc16d0422572e83f92316ce2c1c67f9ce5cc0
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25860644"
---
# <a name="databasenewpassword-method-dao"></a><span data-ttu-id="acdef-102">Database.NewPassword Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="acdef-102">Database.NewPassword Method (DAO)</span></span>


<span data-ttu-id="acdef-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="acdef-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="acdef-104">Ändert das Kennwort einer vorhandenen Microsoft Access-Datenbank (gilt nur für Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="acdef-104">Changes the password of an existing Microsoft Access database engine database (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="acdef-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="acdef-105">Syntax</span></span>

<span data-ttu-id="acdef-106">*Ausdruck* . NewPassword (***BstrOld***, ***BstrNew***)</span><span class="sxs-lookup"><span data-stu-id="acdef-106">*expression* .NewPassword(***bstrOld***, ***bstrNew***)</span></span>

<span data-ttu-id="acdef-107">*Ausdruck* Ein Ausdruck, der ein **Database** -Objekt zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="acdef-107">*expression* An expression that returns a **Database** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="acdef-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="acdef-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="acdef-109">Name</span><span class="sxs-lookup"><span data-stu-id="acdef-109">Name</span></span></p></th>
<th><p><span data-ttu-id="acdef-110">Erforderlich/Optional</span><span class="sxs-lookup"><span data-stu-id="acdef-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="acdef-111">Datentyp</span><span class="sxs-lookup"><span data-stu-id="acdef-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="acdef-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="acdef-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="acdef-113">bstrOld</span><span class="sxs-lookup"><span data-stu-id="acdef-113">bstrOld</span></span></p></td>
<td><p><span data-ttu-id="acdef-114">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="acdef-114">Required</span></span></p></td>
<td><p><span data-ttu-id="acdef-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="acdef-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="acdef-116">Die aktuelle Einstellung der <strong>Password</strong>-Eigenschaft des <strong>Database</strong>-Objekts.</span><span class="sxs-lookup"><span data-stu-id="acdef-116">The current setting of the <strong>Password</strong> property of the <strong>Database</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="acdef-117">bstrNew</span><span class="sxs-lookup"><span data-stu-id="acdef-117">bstrNew</span></span></p></td>
<td><p><span data-ttu-id="acdef-118">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="acdef-118">Required</span></span></p></td>
<td><p><span data-ttu-id="acdef-119"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="acdef-119"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="acdef-120">Die neue Einstellung der <strong>Password</strong> -Eigenschaft des <strong>Database</strong> -Objekts.</span><span class="sxs-lookup"><span data-stu-id="acdef-120">The new setting of the <strong>Password</strong> property of the <strong>Database</strong> object.</span></span></p>

> [!NOTE]
> <span data-ttu-id="acdef-p101">Verwenden Sie sichere Kennwörter, die Groß- und Kleinbuchstaben, Ziffern und Symbole kombinieren. Schwache Kennwörter enthalten keine Kombination dieser Elemente. Sicheres Kennwort: Y6dh!et5. Schwaches Kennwort: House27. Verwenden Sie ein sicheres Kennwort, das Sie sich merken können, damit Sie es nicht aufschreiben müssen.</span><span class="sxs-lookup"><span data-stu-id="acdef-p101">Use strong passwords that combine upper- and lowercase letters, numbers, and symbols. Weak passwords don't mix these elements. Strong password: Y6dh!et5. Weak password: House27. Use a strong password that you can remember so that you don't have to write it down.</span></span>


</td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="acdef-126">Hinweise</span><span class="sxs-lookup"><span data-stu-id="acdef-126">Remarks</span></span>

<span data-ttu-id="acdef-127">Die Zeichenfolgen BstrOld und BstrNew können bis zu 20 Zeichen lang sein und alle Zeichen außer ASCII-Zeichen, 0 (null) enthalten.</span><span class="sxs-lookup"><span data-stu-id="acdef-127">The bstrOld and bstrNew strings can be up to 20 characters long and can include any characters except the ASCII character 0 (null).</span></span> <span data-ttu-id="acdef-128">Das Kennwort verwenden, um eine leere Zeichenfolge ("") für BstrNew.</span><span class="sxs-lookup"><span data-stu-id="acdef-128">To clear the password, use a zero-length string ("") for bstrNew.</span></span>

<span data-ttu-id="acdef-129">Bei Kennwörtern wird Groß-/Kleinschreibung beachtet.</span><span class="sxs-lookup"><span data-stu-id="acdef-129">Passwords are case-sensitive.</span></span>

<span data-ttu-id="acdef-130">Wurde für eine Datenbank kein Kennwort festgelegt, erstellt das Microsoft Access-Datenbankmodul automatisch ein Kennwort, indem es eine leere Zeichenfolge ("") für das alte Kennwort übergibt.</span><span class="sxs-lookup"><span data-stu-id="acdef-130">If a database has no password, the Microsoft Access database engine will automatically create one by passing a zero-length string ("") for the old password.</span></span>


> [!IMPORTANT]
> <span data-ttu-id="acdef-131">[!WICHTIG] Wenn Sie das Kennwort verlieren, können Sie die Datenbank nicht mehr öffnen.</span><span class="sxs-lookup"><span data-stu-id="acdef-131">If you lose your password, you can never open the database again.</span></span>


