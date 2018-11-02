---
title: Database.NewPassword-Methode (DAO)
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
ms.openlocfilehash: f4dca778da3c364d9e9b5a5eaf8ebbc32501853f
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25919360"
---
# <a name="databasenewpassword-method-dao"></a><span data-ttu-id="eebfe-102">Database.NewPassword-Methode (DAO)</span><span class="sxs-lookup"><span data-stu-id="eebfe-102">Database.NewPassword method (DAO)</span></span>


<span data-ttu-id="eebfe-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="eebfe-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="eebfe-104">Ändert das Kennwort einer vorhandenen Microsoft Access-Datenbank (gilt nur für Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="eebfe-104">Changes the password of an existing Microsoft Access database engine database (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="eebfe-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="eebfe-105">Syntax</span></span>

<span data-ttu-id="eebfe-106">*Ausdruck* . NewPassword (***BstrOld***, ***BstrNew***)</span><span class="sxs-lookup"><span data-stu-id="eebfe-106">*expression* .NewPassword(***bstrOld***, ***bstrNew***)</span></span>

<span data-ttu-id="eebfe-107">*Ausdruck* Ein Ausdruck, der ein **Database** -Objekt zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="eebfe-107">*expression* An expression that returns a **Database** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="eebfe-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="eebfe-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="eebfe-109">Name</span><span class="sxs-lookup"><span data-stu-id="eebfe-109">Name</span></span></p></th>
<th><p><span data-ttu-id="eebfe-110">Erforderlich/Optional</span><span class="sxs-lookup"><span data-stu-id="eebfe-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="eebfe-111">Datentyp</span><span class="sxs-lookup"><span data-stu-id="eebfe-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="eebfe-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="eebfe-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="eebfe-113">bstrOld</span><span class="sxs-lookup"><span data-stu-id="eebfe-113">bstrOld</span></span></p></td>
<td><p><span data-ttu-id="eebfe-114">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="eebfe-114">Required</span></span></p></td>
<td><p><span data-ttu-id="eebfe-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="eebfe-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="eebfe-116">Die aktuelle Einstellung der <strong>Password</strong>-Eigenschaft des <strong>Database</strong>-Objekts.</span><span class="sxs-lookup"><span data-stu-id="eebfe-116">The current setting of the <strong>Password</strong> property of the <strong>Database</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eebfe-117">bstrNew</span><span class="sxs-lookup"><span data-stu-id="eebfe-117">bstrNew</span></span></p></td>
<td><p><span data-ttu-id="eebfe-118">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="eebfe-118">Required</span></span></p></td>
<td><p><span data-ttu-id="eebfe-119"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="eebfe-119"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="eebfe-120">Die neue Einstellung der <strong>Password</strong> -Eigenschaft des <strong>Database</strong> -Objekts.</span><span class="sxs-lookup"><span data-stu-id="eebfe-120">The new setting of the <strong>Password</strong> property of the <strong>Database</strong> object.</span></span></p>

> [!NOTE]
> <span data-ttu-id="eebfe-p101">Verwenden Sie sichere Kennwörter, die Groß- und Kleinbuchstaben, Ziffern und Symbole kombinieren. Schwache Kennwörter enthalten keine Kombination dieser Elemente. Sicheres Kennwort: Y6dh!et5. Schwaches Kennwort: House27. Verwenden Sie ein sicheres Kennwort, das Sie sich merken können, damit Sie es nicht aufschreiben müssen.</span><span class="sxs-lookup"><span data-stu-id="eebfe-p101">Use strong passwords that combine upper- and lowercase letters, numbers, and symbols. Weak passwords don't mix these elements. Strong password: Y6dh!et5. Weak password: House27. Use a strong password that you can remember so that you don't have to write it down.</span></span>


</td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="eebfe-126">Hinweise</span><span class="sxs-lookup"><span data-stu-id="eebfe-126">Remarks</span></span>

<span data-ttu-id="eebfe-127">Die Zeichenfolgen BstrOld und BstrNew können bis zu 20 Zeichen lang sein und alle Zeichen außer ASCII-Zeichen, 0 (null) enthalten.</span><span class="sxs-lookup"><span data-stu-id="eebfe-127">The bstrOld and bstrNew strings can be up to 20 characters long and can include any characters except the ASCII character 0 (null).</span></span> <span data-ttu-id="eebfe-128">Das Kennwort verwenden, um eine leere Zeichenfolge ("") für BstrNew.</span><span class="sxs-lookup"><span data-stu-id="eebfe-128">To clear the password, use a zero-length string ("") for bstrNew.</span></span>

<span data-ttu-id="eebfe-129">Bei Kennwörtern wird Groß-/Kleinschreibung beachtet.</span><span class="sxs-lookup"><span data-stu-id="eebfe-129">Passwords are case-sensitive.</span></span>

<span data-ttu-id="eebfe-130">Wurde für eine Datenbank kein Kennwort festgelegt, erstellt das Microsoft Access-Datenbankmodul automatisch ein Kennwort, indem es eine leere Zeichenfolge ("") für das alte Kennwort übergibt.</span><span class="sxs-lookup"><span data-stu-id="eebfe-130">If a database has no password, the Microsoft Access database engine will automatically create one by passing a zero-length string ("") for the old password.</span></span>


> [!IMPORTANT]
> <span data-ttu-id="eebfe-131">[!WICHTIG] Wenn Sie das Kennwort verlieren, können Sie die Datenbank nicht mehr öffnen.</span><span class="sxs-lookup"><span data-stu-id="eebfe-131">If you lose your password, you can never open the database again.</span></span>


