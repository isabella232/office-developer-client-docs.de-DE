---
title: User-Objekt (ADOX - Access-desktop-Datenbank (engl.))
TOCTitle: User Object (ADOX)
ms:assetid: e88b9a8a-e70f-c7ca-cb8c-bd274ff24948
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250178(v=office.15)
ms:contentKeyID: 48548426
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ab5d92a67737774d817046538200d0ebd4337e74
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25474687"
---
# <a name="user-object-adox"></a><span data-ttu-id="d7e78-102">User-Objekt (ADOX)</span><span class="sxs-lookup"><span data-stu-id="d7e78-102">User Object (ADOX)</span></span>


<span data-ttu-id="d7e78-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="d7e78-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="d7e78-104">Stellt ein Benutzerkonto dar, das über Zugriffsberechtigungen in einer gesicherten Datenbank verfügt.</span><span class="sxs-lookup"><span data-stu-id="d7e78-104">Represents a user account that has access permissions within a secured database.</span></span>

## <a name="remarks"></a><span data-ttu-id="d7e78-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d7e78-105">Remarks</span></span>

<span data-ttu-id="d7e78-p101">Die [Users](users-collection-adox.md)-Auflistung eines [Catalog](catalog-object-adox.md)-Objekts stellt alle Benutzer des Katalogs dar. Die **Users** -Auflistung für ein [Group](group-object-adox.md)-Objekt stellt nur die Benutzer dieser Gruppe dar.</span><span class="sxs-lookup"><span data-stu-id="d7e78-p101">The [Users](users-collection-adox.md) collection of a [Catalog](catalog-object-adox.md) represents all the catalog's users. The **Users** collection for a [Group](group-object-adox.md) represents only the users of the specific group.</span></span>

<span data-ttu-id="d7e78-108">Die Eigenschaften, Auflistungen und Methoden eines **User** -Objekts ermöglichen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="d7e78-108">With the properties, collections, and methods of a **User** object, you can:</span></span>

  - <span data-ttu-id="d7e78-109">Identifizieren des Benutzers, indem Sie die [Name](name-property-adox.md)-Eigenschaft verwenden.</span><span class="sxs-lookup"><span data-stu-id="d7e78-109">Identify the user with the [Name](name-property-adox.md) property.</span></span>

  - <span data-ttu-id="d7e78-110">Ändern des Kennworts eines Benutzers, indem Sie die [ChangePassword](changepassword-method-adox.md)-Methode verwenden.</span><span class="sxs-lookup"><span data-stu-id="d7e78-110">Change the password for a user with the [ChangePassword](changepassword-method-adox.md) method.</span></span>

  - <span data-ttu-id="d7e78-111">Bestimmen, ob ein Benutzer Lese-, Schreib- oder Löschberechtigungen hat, indem Sie die Methoden [GetPermissions](getpermissions-method-adox.md) und [SetPermissions](setpermissions-method-adox.md) verwenden.</span><span class="sxs-lookup"><span data-stu-id="d7e78-111">Determine whether a user has read, write, or delete permissions with the [GetPermissions](getpermissions-method-adox.md) and [SetPermissions](setpermissions-method-adox.md) methods.</span></span>

  - <span data-ttu-id="d7e78-112">Zugreifen auf die Gruppen, denen ein Benutzer angehört, indem Sie die [Groups](groups-collection-adox.md)-Auflistung verwenden.</span><span class="sxs-lookup"><span data-stu-id="d7e78-112">Access the groups to which a user belongs with the [Groups](groups-collection-adox.md) collection.</span></span>

  - <span data-ttu-id="d7e78-113">Zugreifen auf anbieterspezifische Eigenschaften mit der [Properties](properties-collection-ado.md)-Auflistung.</span><span class="sxs-lookup"><span data-stu-id="d7e78-113">Access provider-specific properties with the [Properties](properties-collection-ado.md) collection.</span></span>

