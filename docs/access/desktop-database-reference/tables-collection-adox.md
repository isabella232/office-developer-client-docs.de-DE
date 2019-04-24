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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314049"
---
# <a name="tables-collection-adox"></a><span data-ttu-id="452e3-102">Tables-Auflistung (ADOX)</span><span class="sxs-lookup"><span data-stu-id="452e3-102">Tables collection (ADOX)</span></span>


<span data-ttu-id="452e3-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="452e3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="452e3-104">Enthält alle [Table](table-object-adox.md)-Objekte eines Katalogs.</span><span class="sxs-lookup"><span data-stu-id="452e3-104">Contains all [Table](table-object-adox.md) objects of a catalog.</span></span>

## <a name="remarks"></a><span data-ttu-id="452e3-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="452e3-105">Remarks</span></span>

<span data-ttu-id="452e3-p101">Die [Append](append-method-adox-tables.md)-Methode für eine **Tables** -Auflistung wird nur für ADOX bereitgestellt. Sie haben folgende Möglichkeiten:</span><span class="sxs-lookup"><span data-stu-id="452e3-p101">The [Append](append-method-adox-tables.md) method for a **Tables** collection is unique for ADOX. You can:</span></span>

  - <span data-ttu-id="452e3-108">Hinzufügen einer neuen Tabelle zur Auflistung, indem Sie die **Append** -Methode verwenden.</span><span class="sxs-lookup"><span data-stu-id="452e3-108">Add a new table to the collection with the **Append** method.</span></span>

<span data-ttu-id="452e3-p102">Die verbleibenden Eigenschaften und Methoden sind Standardbestandteile von ADO-Auflistungen. Sie haben folgende Möglichkeiten:</span><span class="sxs-lookup"><span data-stu-id="452e3-p102">The remaining properties and methods are standard to ADO collections. You can:</span></span>

  - <span data-ttu-id="452e3-111">Zugreifen auf eine Tabelle in der Auflistung, indem Sie die [Item](item-property-ado.md)-Eigenschaft verwenden.</span><span class="sxs-lookup"><span data-stu-id="452e3-111">Access a table in the collection with the [Item](item-property-ado.md) property.</span></span>

  - <span data-ttu-id="452e3-112">Zurückgeben der Anzahl der Tabellen, die in der Auflistung vorhanden sind, indem Sie die [Count](count-property-ado.md)-Eigenschaft verwenden.</span><span class="sxs-lookup"><span data-stu-id="452e3-112">Return the number of tables contained in the collection with the [Count](count-property-ado.md) property.</span></span>

  - <span data-ttu-id="452e3-113">Entfernen einer Tabelle aus der Auflistung, indem Sie die [Delete](delete-method-adox-collections.md)-Methode verwenden.</span><span class="sxs-lookup"><span data-stu-id="452e3-113">Remove a table from the collection with the [Delete](delete-method-adox-collections.md) method.</span></span>

  - <span data-ttu-id="452e3-114">Aktualisieren der Objekte in der Auflistung entsprechend dem aktuellen Datenbankschema, indem Sie die [Refresh](refresh-method-ado.md)-Methode verwenden.</span><span class="sxs-lookup"><span data-stu-id="452e3-114">Update the objects in the collection to reflect the current database's schema with the [Refresh](refresh-method-ado.md) method.</span></span>

<span data-ttu-id="452e3-p103">Some providers may return other schema objects, such as a View, in the Tables collection. Therefore, some ADOX collections may contain references to the same object. Should you delete the object from one collection, the change will not be visible in another collection that references the deleted object until the Refresh method is called on the collection. For example, with the OLE DB Provider for Microsoft Jet, Views are returned with the Tables collection. If you drop a View, you must Refresh the Tables collection before the collection will reflect the change.</span><span class="sxs-lookup"><span data-stu-id="452e3-p103">Some providers may return other schema objects, such as a View, in the Tables collection. Therefore, some ADOX collections may contain references to the same object. Should you delete the object from one collection, the change will not be visible in another collection that references the deleted object until the Refresh method is called on the collection. For example, with the OLE DB Provider for Microsoft Jet, Views are returned with the Tables collection. If you drop a View, you must Refresh the Tables collection before the collection will reflect the change.</span></span>

