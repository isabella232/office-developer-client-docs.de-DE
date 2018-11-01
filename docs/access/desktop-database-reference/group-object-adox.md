---
title: Group-Objekt (ADOX)
TOCTitle: Group Object (ADOX)
ms:assetid: 91cf1b87-c928-1d89-2731-138f6299cc60
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249642(v=office.15)
ms:contentKeyID: 48546359
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c6f98e65522ebefdb8f3897234d04e54d9599dda
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25883680"
---
# <a name="group-object-adox"></a><span data-ttu-id="77fb0-102">Group-Objekt (ADOX)</span><span class="sxs-lookup"><span data-stu-id="77fb0-102">Group Object (ADOX)</span></span>


<span data-ttu-id="77fb0-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="77fb0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="77fb0-104">Stellt ein Gruppenkonto dar, das über Zugriffsberechtigungen in einer gesicherten Datenbank verfügt.</span><span class="sxs-lookup"><span data-stu-id="77fb0-104">Represents a group account that has access permissions within a secured database.</span></span>

## <a name="remarks"></a><span data-ttu-id="77fb0-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="77fb0-105">Remarks</span></span>

<span data-ttu-id="77fb0-p101">Die [Groups](groups-collection-adox.md)-Auflistung eines [Catalog](catalog-object-adox.md)-Objekts stellt alle Gruppenkonten des Katalogs dar. Die **Groups** -Auflistung für ein [User](user-object-adox.md)-Objekt stellt lediglich die Gruppe dar, zu der der Benutzer gehört.</span><span class="sxs-lookup"><span data-stu-id="77fb0-p101">The [Groups](groups-collection-adox.md) collection of a [Catalog](catalog-object-adox.md) represents all the catalog's group accounts. The **Groups** collection for a [User](user-object-adox.md) represents only the group to which the user belongs.</span></span>

<span data-ttu-id="77fb0-108">Die Eigenschaften, Auflistungen und Methoden eines **Group** -Objekts ermöglichen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="77fb0-108">With the properties, collections, and methods of a **Group** object, you can:</span></span>

  - <span data-ttu-id="77fb0-109">Identifizieren der Gruppe, indem Sie die [Name](name-property-adox.md)-Eigenschaft verwenden.</span><span class="sxs-lookup"><span data-stu-id="77fb0-109">Identify the group with the [Name](name-property-adox.md) property.</span></span>

  - <span data-ttu-id="77fb0-110">Bestimmen, ob eine Gruppe Lese-, Schreib- oder Löschberechtigungen hat, indem Sie die Methoden [GetPermissions](getpermissions-method-adox.md) und [SetPermissions](setpermissions-method-adox.md) verwenden.</span><span class="sxs-lookup"><span data-stu-id="77fb0-110">Determine whether a group has read, write, or delete permissions with the [GetPermissions](getpermissions-method-adox.md) and [SetPermissions](setpermissions-method-adox.md) methods.</span></span>

  - <span data-ttu-id="77fb0-111">Zugreifen auf die Benutzerkonten, die Mitgliedschaften in der Gruppe haben, indem Sie die [Users](users-collection-adox.md)-Auflistung verwenden.</span><span class="sxs-lookup"><span data-stu-id="77fb0-111">Access the user accounts that have memberships in the group with the [Users](users-collection-adox.md) collection.</span></span>

  - <span data-ttu-id="77fb0-112">Zugreifen auf anbieterspezifische Eigenschaften mit der [Properties](properties-collection-ado.md)-Auflistung.</span><span class="sxs-lookup"><span data-stu-id="77fb0-112">Access provider-specific properties with the [Properties](properties-collection-ado.md) collection.</span></span>

