---
title: Fields-Auflistung
TOCTitle: The Fields Collection
ms:assetid: 3bda8e5d-eceb-9605-c4d7-c1f4cc00ce6b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249154(v=office.15)
ms:contentKeyID: 48544297
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ce08ac5952151471ce74afd9a8a49600d8e8f633
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314133"
---
# <a name="fields-collection"></a><span data-ttu-id="07030-102">Fields-Auflistung</span><span class="sxs-lookup"><span data-stu-id="07030-102">Fields collection</span></span>


<span data-ttu-id="07030-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="07030-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="07030-p101">Die **Fields** -Auflistung ist eine der systeminternen Auflistungen von ADO. Eine Auflistung ist eine geordnete Menge von Elementen, auf die als Einheit Bezug genommen werden kann.</span><span class="sxs-lookup"><span data-stu-id="07030-p101">The **Fields** collection is one of ADO's intrinsic collections. A collection is an ordered set of items that can be referred to as a unit.</span></span>

<span data-ttu-id="07030-p102">Die **Fields** -Auflistung enthält ein **Field** -Objekt für jedes Feld (Spalte) im **Recordset** -Objekt. Wie alle ADO-Auflistungen weist sie die Eigenschaften **Count** und **Item** sowie die Methoden **Append** und **Refresh** auf. Darüber hinaus enthält diese Auflistung die Methoden **CancelUpdate**, **Delete**, **Resync** und **Update**, die für andere ADO-Auflistungen nicht verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="07030-p102">The **Fields** collection contains a **Field** object for every field (column) in the **Recordset**. Like all ADO collections, it has **Count** and **Item** properties, as well as **Append** and **Refresh** methods. It also has **CancelUpdate**, **Delete**, **Resync**, and **Update** methods, which are not available to other ADO collections.</span></span>

## <a name="examining-the-fields-collection"></a><span data-ttu-id="07030-109">Analyse der Fields-Auflistung</span><span class="sxs-lookup"><span data-stu-id="07030-109">Examining the Fields Collection</span></span>

<span data-ttu-id="07030-p103">Ziehen Sie die **Fields** -Auflistung des **Recordset** -Beispielobjekts heran, das in diesem Kapitel vorgestellt wurde. Das **Recordset** -Beispielobjekt wurde von der SQL-Anweisung abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="07030-p103">Consider the **Fields** collection of the sample **Recordset** introduced in this chapter. The sample **Recordset** was derived from the SQL statement</span></span>

```sql 
 
SELECT ProductID, ProductName, UnitPrice FROM Products WHERE CategoryID = 7 
```

<span data-ttu-id="07030-112">Die **Fields** -Auflistung des **Recordset** -Objekts sollte demnach drei Felder enthalten.</span><span class="sxs-lookup"><span data-stu-id="07030-112">Thus, you should find that the **Recordset** **Fields** collection contains three fields.</span></span>

```vb 
 
'BeginWalkFields 
 Dim objFields As ADODB.Fields 
 
 objRs.Open strSQL, strConnStr, adOpenForwardOnly, adLockReadOnly, adCmdText 
 
 Set objFields = objRs.Fields 
 
 For intLoop = 0 To (objFields.Count - 1) 
 Debug.Print objFields.Item(intLoop).Name 
 Next 
'EndWalkFields 
```

<span data-ttu-id="07030-p104">Mit diesem Code wird einfach die Anzahl von **Field** -Objekten in der **Fields** -Auflistung mithilfe der **Count** -Eigenschaft zurückgegeben, und es werden Schleifen durch die Auflistung ausgeführt, um den Wert der **Name** -Eigenschaft für jedes **Field** -Objekt zurückzugeben. Sie können mit vielen weiteren **Field** -Eigenschaften Informationen zu einem Feld abrufen. Weitere Informationen zum Abfragen eines **Field** -Objekts finden Sie unter [Field-Objekt](the-field-object.md).</span><span class="sxs-lookup"><span data-stu-id="07030-p104">This code simply determines the number of **Field** objects in the **Fields** collection using the **Count** property and loops through the collection, returning the value of the **Name** property for each **Field** object. You can use many more **Field** properties to get information about a field. For more information about querying a **Field**, see [The Field Object](the-field-object.md).</span></span>

## <a name="counting-columns"></a><span data-ttu-id="07030-116">Zählen von Spalten</span><span class="sxs-lookup"><span data-stu-id="07030-116">Counting Columns</span></span>

<span data-ttu-id="07030-p105">Die **Count** -Eigenschaft gibt erwartungsgemäß die tatsächliche Anzahl von **Field** -Objekten in der **Fields** -Auflistung zurück. Die Nummerierung für Auflistungselemente beginnt bei null, weshalb Sie im Code Schleifen stets mit dem Element Null beginnen und mit dem Wert der **Count** -Eigenschaft minus 1 beenden sollten. Falls Sie Microsoft Visual Basic verwenden und Schleifen durch die Auflistungselemente ausführen möchten, ohne die **Count** -Eigenschaft zu überprüfen, verwenden Sie den Befehl **For** **Each...Next**.</span><span class="sxs-lookup"><span data-stu-id="07030-p105">As you might expect, the **Count** property returns the actual number of **Field** objects in the **Fields** collection. Because numbering for members of a collection begins with zero, you should always code loops starting with the zero member and ending with the value of the **Count** property minus 1. If you are using Microsoft Visual Basic and want to loop through the members of a collection without checking the **Count** property, use the **For** **Each...Next** command.</span></span>

<span data-ttu-id="07030-120">Wenn die **Count** -Eigenschaft gleich null ist, sind in der Auflistung keine Objekte vorhanden.</span><span class="sxs-lookup"><span data-stu-id="07030-120">If the **Count** property is zero, there are no objects in the collection.</span></span>

## <a name="getting-to-the-field"></a><span data-ttu-id="07030-121">Navigieren zum Feld</span><span class="sxs-lookup"><span data-stu-id="07030-121">Getting to the Field</span></span>

<span data-ttu-id="07030-p106">Wie bei jeder ADO-Auflistung ist die **Item** -Eigenschaft die Standardeigenschaft der Auflistung. Sie gibt das einzelne **Field** -Objekt zurück, das durch den Namen oder den übergebenen Index angegeben ist. Deshalb sind die folgenden Anweisungen für das **Recordset** -Beispielobjekt gleichwertig:</span><span class="sxs-lookup"><span data-stu-id="07030-p106">As with any ADO collection, the **Item** property is the default property of the collection. It returns the individual **Field** object specified by the name or index passed to it. Therefore, the following statements are equivalent for the sample **Recordset**:</span></span>

```vb 
 
objField = objRecordset.Fields.Item("ProductID") 
objField = objRecordset.Fields("ProductID") 
objField = objRecordset.Fields.Item(0) 
objField = objRecordset.Fields(0) 
```

<span data-ttu-id="07030-p107">Wenn diese Methoden gleichwertig sind, welches ist dann die beste Methode? Nun, das kommt ganz darauf an. Das Verwenden eines Indexes zum Abrufen eines **Field** -Objekts von der Auflistung ist schneller, weil direkt auf das **Field** -Objekt zugegriffen wird, ohne dass eine Zeichenfolge nachgeschlagen werden muss. Andererseits muss die Reihenfolge von **Field** -Objekten innerhalb der Auflistung bekannt sein. Und wenn sich die Reihenfolge ändert, muss auch der Verweis auf den Index des **Field** -Objekts überall geändert werden. Die Verwendung des Namens des **Field** -Objekts ist zwar geringfügig langsamer, aber flexibler, weil die Reihenfolge der **Field** -Objekte in der Auflistung keine Rolle spielt.</span><span class="sxs-lookup"><span data-stu-id="07030-p107">If these methods are equivalent, which is best? It depends. Using an index to retrieve a **Field** from the collection is faster because it accesses the **Field** directly without having to perform a string lookup. On the other hand, the order of **Fields** within the collection must be known, and if the order changes, the reference to the **Field's** index will have to be changed wherever it occurs. Although slightly slower, using the name of the **Field** is more flexible because it doesn't depend on the order of the **Fields** in the collection.</span></span>

## <a name="using-the-refresh-method"></a><span data-ttu-id="07030-130">Verwenden der Refresh-Methode</span><span class="sxs-lookup"><span data-stu-id="07030-130">Using the Refresh Method</span></span>

<span data-ttu-id="07030-p108">Im Gegensatz zu manch anderen ADO-Auflistungen hat das Verwenden der **Refresh**-Methode in der **Fields**-Auflistung keinen sichtbaren Effekt. Zum Abrufen von Änderungen aus der zugrunde liegenden Datenbankstruktur müssen Sie entweder die **Requery**-Methode verwenden, oder falls Lesezeichen vom **Recordset**-Objekt nicht unterstützt werden, die **MoveFirst**-Methode, mit der der Befehl erneut für den Anbieter ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="07030-p108">Unlike some other ADO collections, using the **Refresh** method on the **Fields** collection has no visible effect. To retrieve changes from the underlying database structure, you must use either the **Requery** method, or if the **Recordset** object does not support bookmarks, the **MoveFirst** method, which will cause the command to be executed against the provider again.</span></span>

## <a name="adding-fields-to-a-recordset"></a><span data-ttu-id="07030-133">Hinzufügen von Feldern zu einem Recordset</span><span class="sxs-lookup"><span data-stu-id="07030-133">Adding Fields to a Recordset</span></span>

<span data-ttu-id="07030-134">Mit der **Append**-Methode werden einem **Recordset**-Objekt Felder hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="07030-134">The **Append** method is used to add fields to a **Recordset**.</span></span>

<span data-ttu-id="07030-p109">Mithilfe der **Append** -Methode können Sie ein **Recordset** -Objekt programmgesteuert erstellen, ohne eine Verbindung mit einer Datenquelle zu öffnen. Ein Laufzeitfehler wird gemeldet, falls die **Append** -Methode in der **Fields** -Auflistung eines geöffneten **Recordset** -Objekts oder eines **Recordset** -Objekts, in dem die **ActiveConnection** -Eigenschaft festgelegt wurde, aufgerufen wird. Felder können nur an ein **Recordset** -Objekt angefügt werden, das nicht geöffnet ist und noch nicht mit einer Datenquelle verbunden wurde. Das **Recordset** -Objekt muss jedoch zuerst geöffnet werden, um Werte für das neu angefügte **Fields** -Objekt anzugeben.</span><span class="sxs-lookup"><span data-stu-id="07030-p109">You can use the **Append** method to fabricate a **Recordset** programmatically without opening a connection to a data source. A run-time error will occur if the **Append** method is called on the **Fields** collection of an open **Recordset** or on a **Recordset** where the **ActiveConnection** property has been set. You can append fields only to a **Recordset** that is not open and has not yet been connected to a data source. However, to specify values for the newly appended **Fields**, the **Recordset** must first be opened.</span></span>

<span data-ttu-id="07030-p110">Entwickler benötigen häufig einen Bereich für die vorübergehende Speicherung von Daten oder möchten, dass sich Daten so verhalten, als ob sie von einem Server stammten, damit sie für die Datenbindung in einer Benutzeroberfläche verwendet werden können. Mit ADO (in Verbindung mit dem [Microsoft Cursor Service für OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md)) kann der Entwickler ein leeres **Recordset** -Objekt erstellen, indem er Spalteninformationen angibt und die **Open** -Methode aufruft. Im folgenden Beispiel werden drei neue Felder an ein neues **Recordset** -Objekt angefügt. Anschließend wird das **Recordset** -Objekt geöffnet, zwei neue Datensätze werden hinzugefügt, und das **Recordset** -Objekt wird in einer Datei gespeichert. (Weitere Informationen zum Speichern des **Recordset** -Objekts finden Sie unter [Kapitel 5: Aktualisieren und Speichern von Daten](chapter-5-updating-and-persisting-data.md).)</span><span class="sxs-lookup"><span data-stu-id="07030-p110">Developers often need a place to temporarily store some data, or want some data to act as if it came from a server so it can participate in data binding in a user interface. ADO (in conjunction with the [Microsoft Cursor Service for OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md)) enables the developer to build an empty **Recordset** object by specifying column information and calling **Open**. In the following example, three new fields are appended to a new **Recordset** object. Then the **Recordset** is opened, two new records are added, and the **Recordset** is persisted to a file. (For more information about **Recordset** persistence, see [Chapter 5: Updating and Persisting Data](chapter-5-updating-and-persisting-data.md).)</span></span>

```vb 
 
 'BeginFabricate 
 Dim objRs As New ADODB.Recordset 
 
 With objRs.Fields 
 .Append "StudentID", adChar, 11, adFldUpdatable 
 .Append "FullName", adVarChar, 50, adFldUpdatable 
 .Append "PhoneNmbr", adVarChar, 20, adFldUpdatable 
 End With 
 
 With objRs 
 .Open 
 
 .AddNew 
 .Fields(0) = "123-45-6789" 
 .Fields(1) = "John Doe" 
 .Fields(2) = "(425) 555-5555" 
 .Update 
 
 .AddNew 
 .Fields(0) = "123-45-6780" 
 .Fields(1) = "Jane Doe" 
 .Fields(2) = "(615) 555-1212" 
 .Update 
 End With 
 
 objRs.Save App.Path & "\FabriTest.adtg", adPersistADTG 
 
 objRs.Close 
 'EndFabricate 
```

<span data-ttu-id="07030-p111">Die Verwendung der **Append** -Methode des **Fields** -Objekts unterscheidet sich beim **Recordset** -Objekt und beim **Record** -Objekt. Weitere Informationen zum **Record** -Objekt finden Sie unter [Kapitel 10: Datensätze und Datenströme](chapter-10-records-and-streams.md).</span><span class="sxs-lookup"><span data-stu-id="07030-p111">The usage of the **Fields** **Append** method differs between the **Recordset** object and the **Record** object. For more information about the **Record** object, see [Chapter 10: Records and Streams](chapter-10-records-and-streams.md).</span></span>

