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
ms.openlocfilehash: d721102039a0fffbc8bbdc4696712bc530967fd8
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25936854"
---
# <a name="databasenewpassword-method-dao"></a><span data-ttu-id="bee27-102">Database.NewPassword-Methode (DAO)</span><span class="sxs-lookup"><span data-stu-id="bee27-102">Database.NewPassword method (DAO)</span></span>


<span data-ttu-id="bee27-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="bee27-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="bee27-104">Ändert das Kennwort einer vorhandenen Microsoft Access-Datenbank (gilt nur für Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="bee27-104">Changes the password of an existing Microsoft Access database engine database (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="bee27-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="bee27-105">Syntax</span></span>

<span data-ttu-id="bee27-106">*Ausdruck* . NewPassword (***BstrOld***, ***BstrNew***)</span><span class="sxs-lookup"><span data-stu-id="bee27-106">*expression* .NewPassword(***bstrOld***, ***bstrNew***)</span></span>

<span data-ttu-id="bee27-107">*Ausdruck* Ein Ausdruck, der ein **Database** -Objekt zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="bee27-107">*expression* An expression that returns a **Database** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="bee27-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="bee27-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bee27-109">Name</span><span class="sxs-lookup"><span data-stu-id="bee27-109">Name</span></span></p></th>
<th><p><span data-ttu-id="bee27-110">Erforderlich/Optional</span><span class="sxs-lookup"><span data-stu-id="bee27-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="bee27-111">Datentyp</span><span class="sxs-lookup"><span data-stu-id="bee27-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="bee27-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bee27-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bee27-113">bstrOld</span><span class="sxs-lookup"><span data-stu-id="bee27-113">bstrOld</span></span></p></td>
<td><p><span data-ttu-id="bee27-114">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="bee27-114">Required</span></span></p></td>
<td><p><span data-ttu-id="bee27-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="bee27-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="bee27-116">Die aktuelle Einstellung der <strong>Password</strong>-Eigenschaft des <strong>Database</strong>-Objekts.</span><span class="sxs-lookup"><span data-stu-id="bee27-116">The current setting of the <strong>Password</strong> property of the <strong>Database</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bee27-117">bstrNew</span><span class="sxs-lookup"><span data-stu-id="bee27-117">bstrNew</span></span></p></td>
<td><p><span data-ttu-id="bee27-118">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="bee27-118">Required</span></span></p></td>
<td><p><span data-ttu-id="bee27-119"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="bee27-119"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="bee27-120">Die neue Einstellung der <strong>Password</strong> -Eigenschaft des <strong>Database</strong> -Objekts.</span><span class="sxs-lookup"><span data-stu-id="bee27-120">The new setting of the <strong>Password</strong> property of the <strong>Database</strong> object.</span></span></p>
<p><span data-ttu-id="bee27-121"><strong>Hinweis</strong> Verwenden Sie sichere Kennwörter, die Groß- und Kleinbuchstaben, Zahlen und Symbole kombinieren.</span><span class="sxs-lookup"><span data-stu-id="bee27-121"><strong>NOTE</strong>Use strong passwords that combine upper- and lowercase letters, numbers, and symbols.</span></span> <span data-ttu-id="bee27-122">Unsichere Kennwörter enthalten keine Kombination dieser Elemente.</span><span class="sxs-lookup"><span data-stu-id="bee27-122">Weak passwords don't mix these elements.</span></span> <span data-ttu-id="bee27-123">Sicheres Kennwort: Y6dh!et5.</span><span class="sxs-lookup"><span data-stu-id="bee27-123">Strong password: Y6dh!et5.</span></span> <span data-ttu-id="bee27-124">Unsicheres Kennwort: Haus27.</span><span class="sxs-lookup"><span data-stu-id="bee27-124">Weak password: House27.</span></span> <span data-ttu-id="bee27-125">Verwenden Sie ein sicheres Kennwort, das Sie sich gut merken können, damit Sie es nicht aufschreiben müssen.</span><span class="sxs-lookup"><span data-stu-id="bee27-125">Use a strong password that you can remember so that you don't have to write it down.</span></span></p>
</td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="bee27-126">Hinweise</span><span class="sxs-lookup"><span data-stu-id="bee27-126">Remarks</span></span>

<span data-ttu-id="bee27-127">Die Zeichenfolgen BstrOld und BstrNew können bis zu 20 Zeichen lang sein und alle Zeichen außer ASCII-Zeichen, 0 (null) enthalten.</span><span class="sxs-lookup"><span data-stu-id="bee27-127">The bstrOld and bstrNew strings can be up to 20 characters long and can include any characters except the ASCII character 0 (null).</span></span> <span data-ttu-id="bee27-128">Das Kennwort verwenden, um eine leere Zeichenfolge ("") für BstrNew.</span><span class="sxs-lookup"><span data-stu-id="bee27-128">To clear the password, use a zero-length string ("") for bstrNew.</span></span>

<span data-ttu-id="bee27-129">Bei Kennwörtern wird Groß-/Kleinschreibung beachtet.</span><span class="sxs-lookup"><span data-stu-id="bee27-129">Passwords are case-sensitive.</span></span>

<span data-ttu-id="bee27-130">Wurde für eine Datenbank kein Kennwort festgelegt, erstellt das Microsoft Access-Datenbankmodul automatisch ein Kennwort, indem es eine leere Zeichenfolge ("") für das alte Kennwort übergibt.</span><span class="sxs-lookup"><span data-stu-id="bee27-130">If a database has no password, the Microsoft Access database engine will automatically create one by passing a zero-length string ("") for the old password.</span></span>


> [!IMPORTANT]
> <span data-ttu-id="bee27-131">[!WICHTIG] Wenn Sie das Kennwort verlieren, können Sie die Datenbank nicht mehr öffnen.</span><span class="sxs-lookup"><span data-stu-id="bee27-131">If you lose your password, you can never open the database again.</span></span>


