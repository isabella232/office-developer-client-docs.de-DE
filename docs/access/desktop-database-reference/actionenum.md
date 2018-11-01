---
title: ActionEnum (Access PC-Datenbank-Referenz)
TOCTitle: ActionEnum
ms:assetid: 225024c1-9088-b532-2a23-04c1aaaaa892
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248998(v=office.15)
ms:contentKeyID: 48543704
ms.date: 10/17/2018
mtps_version: v=office.15
ms.openlocfilehash: 65fe30c558d5fc22563e002f8d19cb78d7ca3e3d
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25879998"
---
# <a name="actionenum"></a><span data-ttu-id="f0137-102">ActionEnum</span><span class="sxs-lookup"><span data-stu-id="f0137-102">ActionEnum</span></span>

<span data-ttu-id="f0137-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f0137-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f0137-104">Gibt den Aktionstyp an, der beim Aufruf von [SetPermissions](setpermissions-method-adox.md) ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f0137-104">Specifies the type of action to be performed when [SetPermissions](setpermissions-method-adox.md) is called.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f0137-105">Konstante</span><span class="sxs-lookup"><span data-stu-id="f0137-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="f0137-106">Wert</span><span class="sxs-lookup"><span data-stu-id="f0137-106">Value</span></span></p></th>
<th><p><span data-ttu-id="f0137-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f0137-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f0137-108"><strong>adAccessDeny</strong></span><span class="sxs-lookup"><span data-stu-id="f0137-108"><strong>adAccessDeny</strong></span></span></p></td>
<td><p><span data-ttu-id="f0137-109">3</span><span class="sxs-lookup"><span data-stu-id="f0137-109">3</span></span></p></td>
<td><p><span data-ttu-id="f0137-110">Der Gruppe oder dem Benutzer werden die angegebenen Berechtigungen verweigert.</span><span class="sxs-lookup"><span data-stu-id="f0137-110">The group or user will be denied the specified permissions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f0137-111"><strong>adAccessGrant</strong></span><span class="sxs-lookup"><span data-stu-id="f0137-111"><strong>adAccessGrant</strong></span></span></p></td>
<td><p><span data-ttu-id="f0137-112">1</span><span class="sxs-lookup"><span data-stu-id="f0137-112">1</span></span></p></td>
<td><p><span data-ttu-id="f0137-113">Die Gruppe oder der Benutzer verfügt mindestens über die angeforderten Berechtigungen.</span><span class="sxs-lookup"><span data-stu-id="f0137-113">The group or user will have at least the requested permissions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f0137-114"><strong>adAccessRevoke</strong></span><span class="sxs-lookup"><span data-stu-id="f0137-114"><strong>adAccessRevoke</strong></span></span></p></td>
<td><p><span data-ttu-id="f0137-115">4</span><span class="sxs-lookup"><span data-stu-id="f0137-115">4</span></span></p></td>
<td><p><span data-ttu-id="f0137-116">Alle expliziten Zugriffsrechte der Gruppe oder des Benutzers werden aufgehoben.</span><span class="sxs-lookup"><span data-stu-id="f0137-116">Any explicit access rights the group or user has will be revoked.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f0137-117"><strong>adAccessSet</strong></span><span class="sxs-lookup"><span data-stu-id="f0137-117"><strong>adAccessSet</strong></span></span></p></td>
<td><p><span data-ttu-id="f0137-118">2</span><span class="sxs-lookup"><span data-stu-id="f0137-118">2</span></span></p></td>
<td><p><span data-ttu-id="f0137-119">Die Gruppe oder der Benutzer verfügen genau über die angeforderten Berechtigungen.</span><span class="sxs-lookup"><span data-stu-id="f0137-119">The group or user will have exactly the requested permissions.</span></span></p></td>
</tr>
</tbody>
</table>

