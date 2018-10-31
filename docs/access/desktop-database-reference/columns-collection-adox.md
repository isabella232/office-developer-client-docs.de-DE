---
title: Columns-Auflistung (ADOX)
TOCTitle: Columns Collection (ADOX)
ms:assetid: 231645db-70da-9ad1-fb27-02145ce32e66
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249008(v=office.15)
ms:contentKeyID: 48543723
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d49fa1bf77a66dbab829aff20ee666ae1a5082cc
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25862217"
---
# <a name="columns-collection-adox"></a><span data-ttu-id="00ea9-102">Columns-Auflistung (ADOX)</span><span class="sxs-lookup"><span data-stu-id="00ea9-102">Columns Collection (ADOX)</span></span>


<span data-ttu-id="00ea9-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="00ea9-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="00ea9-104">Enthält alle [Column](column-object-adox.md)-Objekte einer Tabelle, eines Indexes oder eines Schlüssels.</span><span class="sxs-lookup"><span data-stu-id="00ea9-104">Contains all [Column](column-object-adox.md) objects of a table, index, or key.</span></span>

## <a name="remarks"></a><span data-ttu-id="00ea9-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="00ea9-105">Remarks</span></span>

<span data-ttu-id="00ea9-p101">Die [Append](append-method-adox-columns.md)-Methode für eine **Columns** -Auflistung wird nur für ADOX bereitgestellt. Sie haben folgende Möglichkeiten:</span><span class="sxs-lookup"><span data-stu-id="00ea9-p101">The [Append](append-method-adox-columns.md) method for a **Columns** collection is unique for ADOX. You can:</span></span>

  - <span data-ttu-id="00ea9-108">Hinzufügen einer neuen Spalte zur Auflistung, indem Sie die **Append** -Methode verwenden.</span><span class="sxs-lookup"><span data-stu-id="00ea9-108">Add a new column to the collection with the **Append** method.</span></span>

<span data-ttu-id="00ea9-p102">Die verbleibenden Eigenschaften und Methoden sind Standardbestandteile von ADO-Auflistungen. Sie haben folgende Möglichkeiten:</span><span class="sxs-lookup"><span data-stu-id="00ea9-p102">The remaining properties and methods are standard to ADO collections. You can:</span></span>

  - <span data-ttu-id="00ea9-111">Zugreifen auf eine Spalte in der Auflistung, indem Sie die [Item](item-property-ado.md)-Eigenschaft verwenden.</span><span class="sxs-lookup"><span data-stu-id="00ea9-111">Access a column in the collection with the [Item](item-property-ado.md) property.</span></span>

  - <span data-ttu-id="00ea9-112">Zurückgeben der Anzahl der Spalten, die in der Auflistung vorhanden sind, indem Sie die [Count](count-property-ado.md)-Eigenschaft verwenden.</span><span class="sxs-lookup"><span data-stu-id="00ea9-112">Return the number of columns contained in the collection with the [Count](count-property-ado.md) property.</span></span>

  - <span data-ttu-id="00ea9-113">Entfernen einer Spalte aus der Auflistung, indem Sie die [Delete](delete-method-adox-collections.md)-Methode verwenden.</span><span class="sxs-lookup"><span data-stu-id="00ea9-113">Remove a column from the collection with the [Delete](delete-method-adox-collections.md) method.</span></span>

  - <span data-ttu-id="00ea9-114">Aktualisieren der Objekte in der Auflistung entsprechend dem aktuellen Datenbankschema, indem Sie die [Refresh](refresh-method-ado.md)-Methode verwenden.</span><span class="sxs-lookup"><span data-stu-id="00ea9-114">Update the objects in the collection to reflect the current database's schema with the [Refresh](refresh-method-ado.md) method.</span></span>


> [!NOTE]
> <span data-ttu-id="00ea9-115">[!HINWEIS] Es tritt ein Fehler auf, wenn ein **Column** -Objekt an die **Columns** -Auflistung eines [Index](index-object-adox.md)-Objekts angefügt wird und das **Column** -Objekt nicht in einem [Table](table-object-adox.md)-Objekt vorhanden ist, das bereits an die [Tables](tables-collection-adox.md)-Auflistung angefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="00ea9-115">An error will occur when appending a **Column** to the **Columns** collection of an [Index](index-object-adox.md) if the **Column** does not exist in a [Table](table-object-adox.md) that is already appended to the [Tables](tables-collection-adox.md) collection.</span></span>


