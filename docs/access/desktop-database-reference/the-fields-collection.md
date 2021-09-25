---
title: Fields-Auflistung
TOCTitle: The Fields Collection
ms:assetid: 3bda8e5d-eceb-9605-c4d7-c1f4cc00ce6b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249154(v=office.15)
ms:contentKeyID: 48544297
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 3722b240b45203757f59fb5e4a9e7a45ec3df6ef
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59588973"
---
# <a name="fields-collection"></a>Fields-Auflistung


**Gilt für**: Access 2013, Office 2013

Die **Fields** -Auflistung ist eine der systeminternen Auflistungen von ADO. Eine Auflistung ist eine geordnete Menge von Elementen, auf die als Einheit Bezug genommen werden kann.

Die **Fields** -Auflistung enthält ein **Field** -Objekt für jedes Feld (Spalte) im **Recordset** -Objekt. Wie alle ADO-Auflistungen weist sie die Eigenschaften **Count** und **Item** sowie die Methoden **Append** und **Refresh** auf. Darüber hinaus enthält diese Auflistung die Methoden **CancelUpdate**, **Delete**, **Resync** und **Update**, die für andere ADO-Auflistungen nicht verfügbar sind.

## <a name="examining-the-fields-collection"></a>Analyse der Fields-Auflistung

Ziehen Sie die **Fields** -Auflistung des **Recordset** -Beispielobjekts heran, das in diesem Kapitel vorgestellt wurde. Das **Recordset** -Beispielobjekt wurde von der SQL-Anweisung abgeleitet.

```sql 
 
SELECT ProductID, ProductName, UnitPrice FROM Products WHERE CategoryID = 7 
```

Die **Fields** -Auflistung des **Recordset** -Objekts sollte demnach drei Felder enthalten.

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

Mit diesem Code wird einfach die Anzahl von **Field** -Objekten in der **Fields** -Auflistung mithilfe der **Count** -Eigenschaft zurückgegeben, und es werden Schleifen durch die Auflistung ausgeführt, um den Wert der **Name** -Eigenschaft für jedes **Field** -Objekt zurückzugeben. Sie können mit vielen weiteren **Field** -Eigenschaften Informationen zu einem Feld abrufen. Weitere Informationen zum Abfragen eines **Field** -Objekts finden Sie unter [Field-Objekt](the-field-object.md).

## <a name="counting-columns"></a>Zählen von Spalten

Die **Count** -Eigenschaft gibt erwartungsgemäß die tatsächliche Anzahl von **Field** -Objekten in der **Fields** -Auflistung zurück. Die Nummerierung für Auflistungselemente beginnt bei null, weshalb Sie im Code Schleifen stets mit dem Element Null beginnen und mit dem Wert der **Count** -Eigenschaft minus 1 beenden sollten. Falls Sie Microsoft Visual Basic verwenden und Schleifen durch die Auflistungselemente ausführen möchten, ohne die **Count** -Eigenschaft zu überprüfen, verwenden Sie den Befehl **For** **Each...Next**.

Wenn die **Count** -Eigenschaft gleich null ist, sind in der Auflistung keine Objekte vorhanden.

## <a name="getting-to-the-field"></a>Navigieren zum Feld

Wie bei jeder ADO-Auflistung ist die **Item** -Eigenschaft die Standardeigenschaft der Auflistung. Sie gibt das einzelne **Field** -Objekt zurück, das durch den Namen oder den übergebenen Index angegeben ist. Deshalb sind die folgenden Anweisungen für das **Recordset** -Beispielobjekt gleichwertig:

```vb 
 
objField = objRecordset.Fields.Item("ProductID") 
objField = objRecordset.Fields("ProductID") 
objField = objRecordset.Fields.Item(0) 
objField = objRecordset.Fields(0) 
```

Wenn diese Methoden gleichwertig sind, welches ist dann die beste Methode? Nun, das kommt ganz darauf an. Das Verwenden eines Indexes zum Abrufen eines **Field** -Objekts von der Auflistung ist schneller, weil direkt auf das **Field** -Objekt zugegriffen wird, ohne dass eine Zeichenfolge nachgeschlagen werden muss. Andererseits muss die Reihenfolge von **Field** -Objekten innerhalb der Auflistung bekannt sein. Und wenn sich die Reihenfolge ändert, muss auch der Verweis auf den Index des **Field** -Objekts überall geändert werden. Die Verwendung des Namens des **Field** -Objekts ist zwar geringfügig langsamer, aber flexibler, weil die Reihenfolge der **Field** -Objekte in der Auflistung keine Rolle spielt.

## <a name="using-the-refresh-method"></a>Verwenden der Refresh-Methode

Im Gegensatz zu manch anderen ADO-Auflistungen hat das Verwenden der **Refresh**-Methode in der **Fields**-Auflistung keinen sichtbaren Effekt. Zum Abrufen von Änderungen aus der zugrunde liegenden Datenbankstruktur müssen Sie entweder die **Requery**-Methode verwenden, oder falls Lesezeichen vom **Recordset**-Objekt nicht unterstützt werden, die **MoveFirst**-Methode, mit der der Befehl erneut für den Anbieter ausgeführt wird.

## <a name="adding-fields-to-a-recordset"></a>Hinzufügen von Feldern zu einem Recordset

Mit der **Append**-Methode werden einem **Recordset**-Objekt Felder hinzugefügt.

Mithilfe der **Append** -Methode können Sie ein **Recordset** -Objekt programmgesteuert erstellen, ohne eine Verbindung mit einer Datenquelle zu öffnen. Ein Laufzeitfehler wird gemeldet, falls die **Append** -Methode in der **Fields** -Auflistung eines geöffneten **Recordset** -Objekts oder eines **Recordset** -Objekts, in dem die **ActiveConnection** -Eigenschaft festgelegt wurde, aufgerufen wird. Felder können nur an ein **Recordset** -Objekt angefügt werden, das nicht geöffnet ist und noch nicht mit einer Datenquelle verbunden wurde. Das **Recordset** -Objekt muss jedoch zuerst geöffnet werden, um Werte für das neu angefügte **Fields** -Objekt anzugeben.

Entwickler benötigen häufig einen Bereich für die vorübergehende Speicherung von Daten oder möchten, dass sich Daten so verhalten, als ob sie von einem Server stammten, damit sie für die Datenbindung in einer Benutzeroberfläche verwendet werden können. Mit ADO (in Verbindung mit dem [Microsoft Cursor Service für OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md)) kann der Entwickler ein leeres **Recordset** -Objekt erstellen, indem er Spalteninformationen angibt und die **Open** -Methode aufruft. Im folgenden Beispiel werden drei neue Felder an ein neues **Recordset** -Objekt angefügt. Anschließend wird das **Recordset** -Objekt geöffnet, zwei neue Datensätze werden hinzugefügt, und das **Recordset** -Objekt wird in einer Datei gespeichert. (Weitere Informationen zum Speichern des **Recordset** -Objekts finden Sie unter [Kapitel 5: Aktualisieren und Speichern von Daten](chapter-5-updating-and-persisting-data.md).)

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

Die Verwendung der **Append** -Methode des **Fields** -Objekts unterscheidet sich beim **Recordset** -Objekt und beim **Record** -Objekt. Weitere Informationen zum **Record** -Objekt finden Sie unter [Kapitel 10: Datensätze und Datenströme](chapter-10-records-and-streams.md).

