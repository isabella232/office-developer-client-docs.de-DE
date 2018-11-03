---
title: Groups-Auflistung (ADOX)
TOCTitle: Groups collection (ADOX)
ms:assetid: 9aec57df-bc5c-f9b3-5aec-e7e7efa47ba8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249702(v=office.15)
ms:contentKeyID: 48546553
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b7bd2519af3ea3c35d8cc32ef1ec31ea4f9efa1e
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25936672"
---
# <a name="groups-collection-adox"></a><span data-ttu-id="397a3-102">Groups-Auflistung (ADOX)</span><span class="sxs-lookup"><span data-stu-id="397a3-102">Groups collection (ADOX)</span></span>

<span data-ttu-id="397a3-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="397a3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="397a3-104">Enthält alle gespeicherten [Group](group-object-adox.md)-Objekte eines Katalogs oder Benutzers.</span><span class="sxs-lookup"><span data-stu-id="397a3-104">Contains all stored [Group](group-object-adox.md) objects of a catalog or user.</span></span>

## <a name="remarks"></a><span data-ttu-id="397a3-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="397a3-105">Remarks</span></span>

<span data-ttu-id="397a3-p101">Die **Groups** -Auflistung eines [Catalog](catalog-object-adox.md)-Objekts stellt alle Gruppenkonten des Katalogs dar. Die **Groups** -Auflistung für ein [User](user-object-adox.md)-Objekt stellt lediglich die Gruppe dar, zu der der Benutzer gehört.</span><span class="sxs-lookup"><span data-stu-id="397a3-p101">The **Groups** collection of a [Catalog](catalog-object-adox.md) represents all of the catalog's group accounts. The **Groups** collection for a [User](user-object-adox.md) represents only the group to which the user belongs.</span></span>

<span data-ttu-id="397a3-p102">Die [Append](append-method-adox-groups.md)-Methode für eine **Groups** -Auflistung wird nur für ADOX bereitgestellt. Sie haben folgende Möglichkeiten:</span><span class="sxs-lookup"><span data-stu-id="397a3-p102">The [Append](append-method-adox-groups.md) method for a **Groups** collection is unique for ADOX. You can:</span></span>

- <span data-ttu-id="397a3-110">Hinzufügen einer neuen Sicherheitsgruppe zur Auflistung, indem Sie die **Append** -Methode verwenden.</span><span class="sxs-lookup"><span data-stu-id="397a3-110">Add a new security group to the collection with the **Append** method.</span></span>

<span data-ttu-id="397a3-p103">Die verbleibenden Eigenschaften und Methoden sind Standardbestandteile von ADO-Auflistungen. Sie haben folgende Möglichkeiten:</span><span class="sxs-lookup"><span data-stu-id="397a3-p103">The remaining properties and methods are standard to ADO collections. You can:</span></span>

- <span data-ttu-id="397a3-113">Zugreifen auf eine Gruppe in der Auflistung, indem Sie die [Item](item-property-ado.md)-Eigenschaft verwenden.</span><span class="sxs-lookup"><span data-stu-id="397a3-113">Access a group in the collection with the [Item](item-property-ado.md) property.</span></span>

- <span data-ttu-id="397a3-114">Zurückgeben der Anzahl der Gruppen, die in der Auflistung vorhanden sind, indem Sie die [Count](count-property-ado.md)-Eigenschaft verwenden.</span><span class="sxs-lookup"><span data-stu-id="397a3-114">Return the number of groups contained in the collection with the [Count](count-property-ado.md) property.</span></span>

- <span data-ttu-id="397a3-115">Entfernen einer Gruppe aus der Auflistung, indem Sie die [Delete](delete-method-adox-collections.md)-Methode verwenden.</span><span class="sxs-lookup"><span data-stu-id="397a3-115">Remove a group from the collection with the [Delete](delete-method-adox-collections.md) method.</span></span>

- <span data-ttu-id="397a3-116">Aktualisieren der Objekte in der Auflistung entsprechend dem aktuellen Datenbankschema, indem Sie die [Refresh](refresh-method-ado.md)-Methode verwenden.</span><span class="sxs-lookup"><span data-stu-id="397a3-116">Update the objects in the collection to reflect the current database's schema with the [Refresh](refresh-method-ado.md) method.</span></span>

> [!NOTE]
> <span data-ttu-id="397a3-117">[!HINWEIS] Bevor ein **Group** -Objekt an die **Groups** -Auflistung eines **User** -Objekts angefügt wird, muss ein **Group** -Objekt mit demselben [Namen](name-property-adox.md) wie das anzufügende Objekt bereits in der **Groups** -Auflistung des **Catalog** -Objekts vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="397a3-117">Before appending a **Group** object to the **Groups** collection of a **User** object, a **Group** object with the same [Name](name-property-adox.md) as the one to be appended must already exist in the **Groups** collection of the **Catalog**.</span></span>


