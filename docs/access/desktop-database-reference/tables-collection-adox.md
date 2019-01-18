---
title: Tables-Auflistung (ADOX)
TOCTitle: Tables collection (ADOX)
ms:assetid: 07bc0541-c528-1c25-c8c4-05736836eda3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248821(v=office.15)
ms:contentKeyID: 48543082
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e53cd4b6d4a61a226103eb443bac7f3b4f92d908
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28716172"
---
# <a name="tables-collection-adox"></a><span data-ttu-id="5d58a-102">Tables-Auflistung (ADOX)</span><span class="sxs-lookup"><span data-stu-id="5d58a-102">Tables collection (ADOX)</span></span>


<span data-ttu-id="5d58a-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5d58a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5d58a-104">Enthält alle [Table](table-object-adox.md)-Objekte eines Katalogs.</span><span class="sxs-lookup"><span data-stu-id="5d58a-104">Contains all [Table](table-object-adox.md) objects of a catalog.</span></span>

## <a name="remarks"></a><span data-ttu-id="5d58a-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5d58a-105">Remarks</span></span>

<span data-ttu-id="5d58a-p101">Die [Append](append-method-adox-tables.md)-Methode für eine **Tables** -Auflistung wird nur für ADOX bereitgestellt. Sie haben folgende Möglichkeiten:</span><span class="sxs-lookup"><span data-stu-id="5d58a-p101">The [Append](append-method-adox-tables.md) method for a **Tables** collection is unique for ADOX. You can:</span></span>

  - <span data-ttu-id="5d58a-108">Hinzufügen einer neuen Tabelle zur Auflistung, indem Sie die **Append** -Methode verwenden.</span><span class="sxs-lookup"><span data-stu-id="5d58a-108">Add a new table to the collection with the **Append** method.</span></span>

<span data-ttu-id="5d58a-p102">Die verbleibenden Eigenschaften und Methoden sind Standardbestandteile von ADO-Auflistungen. Sie haben folgende Möglichkeiten:</span><span class="sxs-lookup"><span data-stu-id="5d58a-p102">The remaining properties and methods are standard to ADO collections. You can:</span></span>

  - <span data-ttu-id="5d58a-111">Zugreifen auf eine Tabelle in der Auflistung, indem Sie die [Item](item-property-ado.md)-Eigenschaft verwenden.</span><span class="sxs-lookup"><span data-stu-id="5d58a-111">Access a table in the collection with the [Item](item-property-ado.md) property.</span></span>

  - <span data-ttu-id="5d58a-112">Zurückgeben der Anzahl der Tabellen, die in der Auflistung vorhanden sind, indem Sie die [Count](count-property-ado.md)-Eigenschaft verwenden.</span><span class="sxs-lookup"><span data-stu-id="5d58a-112">Return the number of tables contained in the collection with the [Count](count-property-ado.md) property.</span></span>

  - <span data-ttu-id="5d58a-113">Entfernen einer Tabelle aus der Auflistung, indem Sie die [Delete](delete-method-adox-collections.md)-Methode verwenden.</span><span class="sxs-lookup"><span data-stu-id="5d58a-113">Remove a table from the collection with the [Delete](delete-method-adox-collections.md) method.</span></span>

  - <span data-ttu-id="5d58a-114">Aktualisieren der Objekte in der Auflistung entsprechend dem aktuellen Datenbankschema, indem Sie die [Refresh](refresh-method-ado.md)-Methode verwenden.</span><span class="sxs-lookup"><span data-stu-id="5d58a-114">Update the objects in the collection to reflect the current database's schema with the [Refresh](refresh-method-ado.md) method.</span></span>

<span data-ttu-id="5d58a-p103">Einige Anbieter geben möglicherweise andere Schemaobjekte in der Tables-Auflistung zurück, z. B. eine Sicht. Bestimmte ADOX-Auflistungen können daher Verweise auf dasselbe Objekt enthalten. Wenn Sie das Objekt aus einer Auflistung löschen, wird diese Änderung in einer anderen Auflistung, die auf das gelöschte Objekt verweist, erst sichtbar, wenn für diese Auflistung die Refresh-Methode aufgerufen wird. Mit dem OLE DB-Anbieter für Microsoft Jet werden beispielsweise Sichten zusammen mit der Tables-Auflistung zurückgegeben. Wenn Sie eine Sicht löschen, müssen Sie die Tables-Auflistung zunächst aktualisieren, damit die Änderung für diese Auflistung angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="5d58a-p103">Some providers may return other schema objects, such as a View, in the Tables collection. Therefore, some ADOX collections may contain references to the same object. Should you delete the object from one collection, the change will not be visible in another collection that references the deleted object until the Refresh method is called on the collection. For example, with the OLE DB Provider for Microsoft Jet, Views are returned with the Tables collection. If you drop a View, you must Refresh the Tables collection before the collection will reflect the change.</span></span>

