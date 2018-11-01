---
title: User-Objekt (ADOX - Access-desktop-Datenbank (engl.))
TOCTitle: User Object (ADOX)
ms:assetid: e88b9a8a-e70f-c7ca-cb8c-bd274ff24948
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250178(v=office.15)
ms:contentKeyID: 48548426
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0c37e43f09fb4187de246e687d81dbd72463d390
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25889315"
---
# <a name="user-object-adox"></a><span data-ttu-id="bd9fb-102">User-Objekt (ADOX)</span><span class="sxs-lookup"><span data-stu-id="bd9fb-102">User Object (ADOX)</span></span>


<span data-ttu-id="bd9fb-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="bd9fb-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="bd9fb-104">Stellt ein Benutzerkonto dar, das über Zugriffsberechtigungen in einer gesicherten Datenbank verfügt.</span><span class="sxs-lookup"><span data-stu-id="bd9fb-104">Represents a user account that has access permissions within a secured database.</span></span>

## <a name="remarks"></a><span data-ttu-id="bd9fb-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="bd9fb-105">Remarks</span></span>

<span data-ttu-id="bd9fb-p101">Die [Users](users-collection-adox.md)-Auflistung eines [Catalog](catalog-object-adox.md)-Objekts stellt alle Benutzer des Katalogs dar. Die **Users** -Auflistung für ein [Group](group-object-adox.md)-Objekt stellt nur die Benutzer dieser Gruppe dar.</span><span class="sxs-lookup"><span data-stu-id="bd9fb-p101">The [Users](users-collection-adox.md) collection of a [Catalog](catalog-object-adox.md) represents all the catalog's users. The **Users** collection for a [Group](group-object-adox.md) represents only the users of the specific group.</span></span>

<span data-ttu-id="bd9fb-108">Die Eigenschaften, Auflistungen und Methoden eines **User** -Objekts ermöglichen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="bd9fb-108">With the properties, collections, and methods of a **User** object, you can:</span></span>

  - <span data-ttu-id="bd9fb-109">Identifizieren des Benutzers, indem Sie die [Name](name-property-adox.md)-Eigenschaft verwenden.</span><span class="sxs-lookup"><span data-stu-id="bd9fb-109">Identify the user with the [Name](name-property-adox.md) property.</span></span>

  - <span data-ttu-id="bd9fb-110">Ändern des Kennworts eines Benutzers, indem Sie die [ChangePassword](changepassword-method-adox.md)-Methode verwenden.</span><span class="sxs-lookup"><span data-stu-id="bd9fb-110">Change the password for a user with the [ChangePassword](changepassword-method-adox.md) method.</span></span>

  - <span data-ttu-id="bd9fb-111">Bestimmen, ob ein Benutzer Lese-, Schreib- oder Löschberechtigungen hat, indem Sie die Methoden [GetPermissions](getpermissions-method-adox.md) und [SetPermissions](setpermissions-method-adox.md) verwenden.</span><span class="sxs-lookup"><span data-stu-id="bd9fb-111">Determine whether a user has read, write, or delete permissions with the [GetPermissions](getpermissions-method-adox.md) and [SetPermissions](setpermissions-method-adox.md) methods.</span></span>

  - <span data-ttu-id="bd9fb-112">Zugreifen auf die Gruppen, denen ein Benutzer angehört, indem Sie die [Groups](groups-collection-adox.md)-Auflistung verwenden.</span><span class="sxs-lookup"><span data-stu-id="bd9fb-112">Access the groups to which a user belongs with the [Groups](groups-collection-adox.md) collection.</span></span>

  - <span data-ttu-id="bd9fb-113">Zugreifen auf anbieterspezifische Eigenschaften mit der [Properties](properties-collection-ado.md)-Auflistung.</span><span class="sxs-lookup"><span data-stu-id="bd9fb-113">Access provider-specific properties with the [Properties](properties-collection-ado.md) collection.</span></span>

