---
title: Users-Auflistung (ADOX)
TOCTitle: Users collection (ADOX)
ms:assetid: bc61c862-1637-02e7-4b56-5ad984bdbcb0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249905(v=office.15)
ms:contentKeyID: 48547413
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 24d7a5cab3260dac80b39e5134938c5f55175851
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32312936"
---
# <a name="users-collection-adox"></a><span data-ttu-id="98610-102">Users-Auflistung (ADOX)</span><span class="sxs-lookup"><span data-stu-id="98610-102">Users collection (ADOX)</span></span>

<span data-ttu-id="98610-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="98610-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="98610-104">Enthält alle gespeicherten [User](user-object-adox.md)-Objekte eines Katalogs oder einer Gruppe.</span><span class="sxs-lookup"><span data-stu-id="98610-104">Contains all stored [User](user-object-adox.md) objects of a catalog or group.</span></span>

## <a name="remarks"></a><span data-ttu-id="98610-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="98610-105">Remarks</span></span>

<span data-ttu-id="98610-p101">Die **Users** Auflistung eines [Catalog](catalog-object-adox.md)-Objekts stellt alle Benutzer des Katalogs dar. Die **Users** -Auflistung für ein [Group](group-object-adox.md)-Objekt stellt nur die Benutzer dar, die Elemente dieser bestimmten Gruppe sind.</span><span class="sxs-lookup"><span data-stu-id="98610-p101">The **Users** collection of a [Catalog](catalog-object-adox.md) represents all the catalog's users. The **Users** collection for a [Group](group-object-adox.md) represents only the users that have a membership in the specific group.</span></span>

<span data-ttu-id="98610-p102">Die [Append](append-method-adox-users.md)-Methode für eine **Users** -Auflistung wird nur für ADOX bereitgestellt. Sie haben folgende Möglichkeiten:</span><span class="sxs-lookup"><span data-stu-id="98610-p102">The [Append](append-method-adox-users.md) method for a **Users** collection is unique for ADOX. You can:</span></span>

- <span data-ttu-id="98610-110">Hinzufügen eines neuen Benutzers zur Auflistung, indem Sie die **Append** -Methode verwenden.</span><span class="sxs-lookup"><span data-stu-id="98610-110">Add a new user to the collection with the **Append** method.</span></span>

<span data-ttu-id="98610-p103">Die verbleibenden Eigenschaften und Methoden sind Standardbestandteile von ADO-Auflistungen. Sie haben folgende Möglichkeiten:</span><span class="sxs-lookup"><span data-stu-id="98610-p103">The remaining properties and methods are standard to ADO collections. You can:</span></span>

- <span data-ttu-id="98610-113">Zugreifen auf einen Benutzer in der Auflistung, indem Sie die [Item](item-property-ado.md)-Eigenschaft verwenden.</span><span class="sxs-lookup"><span data-stu-id="98610-113">Access a user in the collection with the [Item](item-property-ado.md) property.</span></span>

- <span data-ttu-id="98610-114">Zurückgeben der Anzahl der Benutzer, die in der Auflistung vorhanden sind, indem Sie die [Count](count-property-ado.md)-Eigenschaft verwenden.</span><span class="sxs-lookup"><span data-stu-id="98610-114">Return the number of users contained in the collection with the [Count](count-property-ado.md) property.</span></span>

- <span data-ttu-id="98610-115">Entfernen eines Benutzers aus der Auflistung, indem Sie die [Delete](delete-method-adox-collections.md)-Methode verwenden.</span><span class="sxs-lookup"><span data-stu-id="98610-115">Remove a user from the collection with the [Delete](delete-method-adox-collections.md) method.</span></span>

- <span data-ttu-id="98610-116">Aktualisieren der Objekte in der Auflistung entsprechend dem aktuellen Datenbankschema, indem Sie die [Refresh](refresh-method-ado.md)-Methode verwenden.</span><span class="sxs-lookup"><span data-stu-id="98610-116">Update the objects in the collection to reflect the current database's schema with the [Refresh](refresh-method-ado.md) method.</span></span>

> [!NOTE]
> <span data-ttu-id="98610-117">[!HINWEIS] Bevor ein **User** -Objekt an die **Users** -Auflistung eines **Group** -Objekts angefügt wird, muss ein **User** -Objekt mit demselben [Namen](name-property-adox.md) wie das anzufügende Objekt bereits in der **Users** -Auflistung des **Catalog** -Objekts vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="98610-117">Before appending a **User** object to the **Users** collection of a **Group** object, a **User** object with the same [Name](name-property-adox.md) as the one to be appended must already exist in the **Users** collection of the **Catalog**.</span></span>

