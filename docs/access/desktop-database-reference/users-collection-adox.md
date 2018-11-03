---
title: Users-Auflistung (ADOX)
TOCTitle: Users collection (ADOX)
ms:assetid: bc61c862-1637-02e7-4b56-5ad984bdbcb0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249905(v=office.15)
ms:contentKeyID: 48547413
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b44b7b858adca5672266eb1898213d8f28429f2e
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25931134"
---
# <a name="users-collection-adox"></a><span data-ttu-id="acbd9-102">Users-Auflistung (ADOX)</span><span class="sxs-lookup"><span data-stu-id="acbd9-102">Users collection (ADOX)</span></span>


<span data-ttu-id="acbd9-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="acbd9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="acbd9-104">Enthält alle gespeicherten [User](user-object-adox.md)-Objekte eines Katalogs oder einer Gruppe.</span><span class="sxs-lookup"><span data-stu-id="acbd9-104">Contains all stored [User](user-object-adox.md) objects of a catalog or group.</span></span>

## <a name="remarks"></a><span data-ttu-id="acbd9-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="acbd9-105">Remarks</span></span>

<span data-ttu-id="acbd9-p101">Die **Users** Auflistung eines [Catalog](catalog-object-adox.md)-Objekts stellt alle Benutzer des Katalogs dar. Die **Users** -Auflistung für ein [Group](group-object-adox.md)-Objekt stellt nur die Benutzer dar, die Elemente dieser bestimmten Gruppe sind.</span><span class="sxs-lookup"><span data-stu-id="acbd9-p101">The **Users** collection of a [Catalog](catalog-object-adox.md) represents all the catalog's users. The **Users** collection for a [Group](group-object-adox.md) represents only the users that have a membership in the specific group.</span></span>

<span data-ttu-id="acbd9-p102">Die [Append](append-method-adox-users.md)-Methode für eine **Users** -Auflistung wird nur für ADOX bereitgestellt. Sie haben folgende Möglichkeiten:</span><span class="sxs-lookup"><span data-stu-id="acbd9-p102">The [Append](append-method-adox-users.md) method for a **Users** collection is unique for ADOX. You can:</span></span>

  - <span data-ttu-id="acbd9-110">Hinzufügen eines neuen Benutzers zur Auflistung, indem Sie die **Append** -Methode verwenden.</span><span class="sxs-lookup"><span data-stu-id="acbd9-110">Add a new user to the collection with the **Append** method.</span></span>

<span data-ttu-id="acbd9-p103">Die verbleibenden Eigenschaften und Methoden sind Standardbestandteile von ADO-Auflistungen. Sie haben folgende Möglichkeiten:</span><span class="sxs-lookup"><span data-stu-id="acbd9-p103">The remaining properties and methods are standard to ADO collections. You can:</span></span>

  - <span data-ttu-id="acbd9-113">Zugreifen auf einen Benutzer in der Auflistung, indem Sie die [Item](item-property-ado.md)-Eigenschaft verwenden.</span><span class="sxs-lookup"><span data-stu-id="acbd9-113">Access a user in the collection with the [Item](item-property-ado.md) property.</span></span>

  - <span data-ttu-id="acbd9-114">Zurückgeben der Anzahl der Benutzer, die in der Auflistung vorhanden sind, indem Sie die [Count](count-property-ado.md)-Eigenschaft verwenden.</span><span class="sxs-lookup"><span data-stu-id="acbd9-114">Return the number of users contained in the collection with the [Count](count-property-ado.md) property.</span></span>

  - <span data-ttu-id="acbd9-115">Entfernen eines Benutzers aus der Auflistung, indem Sie die [Delete](delete-method-adox-collections.md)-Methode verwenden.</span><span class="sxs-lookup"><span data-stu-id="acbd9-115">Remove a user from the collection with the [Delete](delete-method-adox-collections.md) method.</span></span>

  - <span data-ttu-id="acbd9-116">Aktualisieren der Objekte in der Auflistung entsprechend dem aktuellen Datenbankschema, indem Sie die [Refresh](refresh-method-ado.md)-Methode verwenden.</span><span class="sxs-lookup"><span data-stu-id="acbd9-116">Update the objects in the collection to reflect the current database's schema with the [Refresh](refresh-method-ado.md) method.</span></span>


> [!NOTE]
> <P><span data-ttu-id="acbd9-117">[!HINWEIS] Bevor ein <STRONG>User</STRONG> -Objekt an die <STRONG>Users</STRONG> -Auflistung eines <STRONG>Group</STRONG> -Objekts angefügt wird, muss ein <STRONG>User</STRONG> -Objekt mit demselben <A href="name-property-adox.md">Namen</A> wie das anzufügende Objekt bereits in der <STRONG>Users</STRONG> -Auflistung des <STRONG>Catalog</STRONG> -Objekts vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="acbd9-117">Before appending a <STRONG>User</STRONG> object to the <STRONG>Users</STRONG> collection of a <STRONG>Group</STRONG> object, a <STRONG>User</STRONG> object with the same <A href="name-property-adox.md">Name</A> as the one to be appended must already exist in the <STRONG>Users</STRONG> collection of the <STRONG>Catalog</STRONG>.</span></span></P>


