---
title: Columns-Auflistung (ADOX)
TOCTitle: Columns Collection (ADOX)
ms:assetid: 231645db-70da-9ad1-fb27-02145ce32e66
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249008(v=office.15)
ms:contentKeyID: 48543723
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 13f9a17d7dfcd9e621e4f4b1f1fcc03e88b4d832
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25475461"
---
# <a name="columns-collection-adox"></a><span data-ttu-id="c5753-102">Columns-Auflistung (ADOX)</span><span class="sxs-lookup"><span data-stu-id="c5753-102">Columns Collection (ADOX)</span></span>


<span data-ttu-id="c5753-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="c5753-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="c5753-104">Enthält alle [Column](column-object-adox.md)-Objekte einer Tabelle, eines Indexes oder eines Schlüssels.</span><span class="sxs-lookup"><span data-stu-id="c5753-104">Contains all [Column](column-object-adox.md) objects of a table, index, or key.</span></span>

## <a name="remarks"></a><span data-ttu-id="c5753-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c5753-105">Remarks</span></span>

<span data-ttu-id="c5753-p101">Die [Append](append-method-adox-columns.md)-Methode für eine **Columns** -Auflistung wird nur für ADOX bereitgestellt. Sie haben folgende Möglichkeiten:</span><span class="sxs-lookup"><span data-stu-id="c5753-p101">The [Append](append-method-adox-columns.md) method for a **Columns** collection is unique for ADOX. You can:</span></span>

  - <span data-ttu-id="c5753-108">Hinzufügen einer neuen Spalte zur Auflistung, indem Sie die **Append** -Methode verwenden.</span><span class="sxs-lookup"><span data-stu-id="c5753-108">Add a new column to the collection with the **Append** method.</span></span>

<span data-ttu-id="c5753-p102">Die verbleibenden Eigenschaften und Methoden sind Standardbestandteile von ADO-Auflistungen. Sie haben folgende Möglichkeiten:</span><span class="sxs-lookup"><span data-stu-id="c5753-p102">The remaining properties and methods are standard to ADO collections. You can:</span></span>

  - <span data-ttu-id="c5753-111">Zugreifen auf eine Spalte in der Auflistung, indem Sie die [Item](item-property-ado.md)-Eigenschaft verwenden.</span><span class="sxs-lookup"><span data-stu-id="c5753-111">Access a column in the collection with the [Item](item-property-ado.md) property.</span></span>

  - <span data-ttu-id="c5753-112">Zurückgeben der Anzahl der Spalten, die in der Auflistung vorhanden sind, indem Sie die [Count](count-property-ado.md)-Eigenschaft verwenden.</span><span class="sxs-lookup"><span data-stu-id="c5753-112">Return the number of columns contained in the collection with the [Count](count-property-ado.md) property.</span></span>

  - <span data-ttu-id="c5753-113">Entfernen einer Spalte aus der Auflistung, indem Sie die [Delete](delete-method-adox-collections.md)-Methode verwenden.</span><span class="sxs-lookup"><span data-stu-id="c5753-113">Remove a column from the collection with the [Delete](delete-method-adox-collections.md) method.</span></span>

  - <span data-ttu-id="c5753-114">Aktualisieren der Objekte in der Auflistung entsprechend dem aktuellen Datenbankschema, indem Sie die [Refresh](refresh-method-ado.md)-Methode verwenden.</span><span class="sxs-lookup"><span data-stu-id="c5753-114">Update the objects in the collection to reflect the current database's schema with the [Refresh](refresh-method-ado.md) method.</span></span>


> [!NOTE]
> <P><span data-ttu-id="c5753-115">[!HINWEIS] Es tritt ein Fehler auf, wenn ein <STRONG>Column</STRONG> -Objekt an die <STRONG>Columns</STRONG> -Auflistung eines <A href="index-object-adox.md">Index</A>-Objekts angefügt wird und das <STRONG>Column</STRONG> -Objekt nicht in einem <A href="table-object-adox.md">Table</A>-Objekt vorhanden ist, das bereits an die <A href="tables-collection-adox.md">Tables</A>-Auflistung angefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="c5753-115">An error will occur when appending a <STRONG>Column</STRONG> to the <STRONG>Columns</STRONG> collection of an <A href="index-object-adox.md">Index</A> if the <STRONG>Column</STRONG> does not exist in a <A href="table-object-adox.md">Table</A> that is already appended to the <A href="tables-collection-adox.md">Tables</A> collection.</span></span></P>


