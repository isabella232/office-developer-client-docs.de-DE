---
title: Das Field-Objekt (Access PC-Datenbank-Referenz)
TOCTitle: The Field Object
ms:assetid: 55531e04-d74f-6394-df64-1660e5d572ca
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249284(v=office.15)
ms:contentKeyID: 48544926
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: cf5e5de6c45cd3b8cc8827a794f5c2ce394d8f43
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2018
ms.locfileid: "25947294"
---
# <a name="field-object"></a>Field-Objekt


**Betrifft**: Access 2013, Office 2013

Jedes **Field** -Objekt entspricht gewöhnlich einer Spalte in einer Datenbanktabelle. Ein **Field** -Objekt kann jedoch auch einen Zeiger auf ein anderes **Recordset** -Objekt darstellen, ein so genanntes Kapitel. Ausnahmen, wie z. B. Kapitelspalten, werden weiter unten in diesem Handbuch behandelt.

Verwenden Sie die **Value** -Eigenschaft von **Field** -Objekten, um Daten für den aktuellen Datensatz festzulegen oder zurückzugeben. In Abhängigkeit von der vom Anbieter unterstützten Funktionalität können bestimmte Auflistungen, Methoden oder Eigenschaften eines **Field** -Objekts nicht verfügbar sein.

Die Auflistungen, Methoden und Eigenschaften eines **Field** -Objekts ermöglichen Folgendes:

  - Zurückgeben des Namens eines Felds mithilfe der **Name** -Eigenschaft.

  - Anzeigen oder Ändern der Daten im Feld mithilfe der **Value** -Eigenschaft. **Value** ist die Standardeigenschaft des **Field** -Objekts.

  - Zurückgeben der grundlegenden Merkmale eines Felds mithilfe der Eigenschaften **Type**, **Precision** und **NumericScale**.

  - Zurückgeben der deklarierten Größe eines Felds mithilfe der **DefinedSize** -Eigenschaft.

  - Zurückgeben der tatsächlichen Größe der Daten in einem bestimmten Feld mithilfe der **ActualSize** -Eigenschaft.

  - Bestimmen der für ein bestimmtes Feld unterstützten Funktionalitätstypen mithilfe der **Attributes** -Eigenschaft und der **Properties** -Auflistung.

  - Bearbeiten der Werte von Feldern, die Daten vom Typ Long Binary oder Long enthalten, mithilfe der Methoden AppendChunk und GetChunk.

Auflösen von Diskrepanzen in Feldwerten während der Batchaktualisierung mithilfe der Eigenschaften **OriginalValue** und **UnderlyingValue**, falls der Anbieter Batchaktualisierungen unterstützt.

## <a name="describing-a-field"></a>Beschreiben eines Field-Objekts

In den folgenden Themen werden Eigenschaften des [Field](field-object-ado.md)-Objekts behandelt, die Informationen darstellen, die das **Field** -Objekt selbst beschreiben - also Metadaten zu dem Feld. Diese Informationen helfen bei der Bestimmung des Schemas des **Recordset** -Objekts. Zu diesen Eigenschaften zählen **Type**, **DefinedSize**, **ActualSize**, **Name**, **NumericScale** und **Precision**.

## <a name="discovering-the-data-type"></a>Ermitteln des Datentyps

Die **Type** -Eigenschaft gibt den Datentyp des Felds an. Konstanten Typ, der Daten, die von ADO unterstützt werden, werden in [DataTypeEnum-Wert](datatypeenum.md) in der *ADO-Programmierreferenz*beschrieben.

Für numerische Gleitkomma-Datentypen wie z. B. **adNumeric** können Sie weitere Informationen abrufen. Die **NumericScale** -Eigenschaft gibt an, wie viele Stellen rechts des Dezimalzeichens zur Darstellung von Werten für das **Field** -Objekt verwendet werden. Die **Precision** -Eigenschaft gibt die maximale Anzahl von Stellen zur Darstellung von Werten für das **Field** -Objekt an.

## <a name="determining-field-size"></a>Bestimmen der Größe eines Field-Objekts

Mithilfe der **DefinedSize** -Eigenschaft bestimmen Sie die Datenkapazität eines **Field** -Objekts.

Mithilfe der **ActualSize** -Eigenschaft geben Sie die tatsächliche Länge des Werts eines **Field** -Objekts zurück. Die **ActualSize** -Eigenschaft ist für alle Felder schreibgeschützt. Falls ADO die Länge des Werts für das **Field** -Objekt nicht bestimmen kann, wird **adUnknown** von der **ActualSize** -Eigenschaft zurückgegeben.

Die Eigenschaften **DefinedSize** und **ActualSize** haben unterschiedliche Verwendungszwecke. Angenommen, ein **Field** -Objekt mit dem deklarierten Typ **adVarChar** und einer **DefinedSize** -Eigenschaft von 50 enthält ein einzelnes Zeichen. Für die **ActualSize** -Eigenschaft wird als Wert die Länge in Bytes dieses Einzelzeichens zurückgegeben.

## <a name="determining-field-contents"></a>Bestimmen des Inhalts von Field-Objekten

Der Bezeichner der Spalte aus der Datenquelle wird durch die **Name** -Eigenschaft des **Field** -Objekts dargestellt. Mit der **Value** -Eigenschaft des **Field** -Objekts wird der tatsächliche Dateninhalt des Felds zurückgegeben oder festgelegt. Dies ist die Standardeigenschaft.

Zum Ändern der Daten in einem Feld legen Sie die **Value** -Eigenschaft auf einen neuen Wert mit dem richtigen Datentyp fest. Der Cursortyp muss Aktualisierungen unterstützen, um die Inhalte eines Felds zu ändern. Die Überprüfung der Datenbank erfolgt in diesem Fall nicht im Batchmodus. Deshalb müssen Sie in einem solchen Fall beim Aufrufen von **UpdateBatch** nach Fehlern suchen. Manche Anbieter unterstützen auch die Eigenschaften **UnderlyingValue** und **OriginalValue** des **Field** -Objekts von ADO, damit Sie Konflikte beim Ausführen von Batchaktualisierungen lösen können. Weitere Informationen zum Lösen solcher Konflikte finden Sie in [Kapitel 4: Bearbeiten von Daten](chapter-4-editing-data.md).


> [!NOTE]
> <P>Werte für ein Field-Objekt in einem Recordset-Objekt können nicht festgelegt werden, wenn neue Field-Objekte an ein Recordset-Objekt angefügt werden. Neue Field-Objekte können aber an ein geschlossenes Recordset-Objekt angefügt werden. Das Recordset-Objekt muss dann geöffnet werden, und erst dann können diesen Field-Objekten Werte zugewiesen werden.</P>



## <a name="getting-more-field-information"></a>Abrufen weiterer Informationen zum Field-Objekt

ADO-Objekte weisen zwei Arten von Eigenschaften auf, nämlich integrierte und dynamische Eigenschaften. Bisher wurden nur die integrierten Eigenschaften des **Field** -Objekts behandelt.

Integrierte Eigenschaften sind diese Eigenschaften in ADO implementiert und für jedes neue Objekt mithilfe der Syntax. Sie werden nicht als **Property** -Objekte in der **Properties** -Auflistung eines Objekts angezeigt.

Dynamische Eigenschaften werden durch den zugrunde liegenden Datenprovider definiert und in der **Properties** -Auflistung für das entsprechende ADO-Objekt angezeigt. Beispielsweise kann eine anbieterspezifische Eigenschaft anzeigen, ob Transaktionen oder Aktualisierungen von einem **Recordset** -Objekt unterstützt werden. Diese zusätzlichen Eigenschaften werden als **Property** -Objekte in der **Properties** -Auflistung dieses **Recordset** -Objekts angezeigt. Dynamische Eigenschaften kann nur über die Auflistung mithilfe der Syntax MyObject.Properties(0) verwiesen werden oder oder MyObject.Properties("Name").

Keiner der beiden Eigenschaftstypen kann gelöscht werden.

Ein dynamisches **Property** -Objekt weist vier integrierte Eigenschaften auf:

  - Die **Name** -Eigenschaft ist eine Zeichenfolge zur Identifizierung der Eigenschaft.

  - Die **Type** -Eigenschaft ist eine ganze Zahl zur Angabe des Datentyps der Eigenschaft.

  - Die Value-Eigenschaft ist vom Datentyp Variant und enthält die Eigenschaftseinstellung. Value ist die Standardeigenschaft für ein Property-Objekt.

  - Die **Attributes** -Eigenschaft ist ein Wert vom Typ **Long** zur Angabe der Merkmale der anbieterspezifischen Eigenschaft.

Die **Properties** -Auflistung für das **Field** -Objekt enthält zusätzliche Metadaten zum Feld. Der Inhalt dieser Auflistung hängt vom Anbieter ab. Im folgenden Codebeispiel wird die **Properties** -Auflistung des **Recordset** -Beispielobjekts, das zu Beginn dieses Kapitels vorgestellt wurde, untersucht. Zunächst wird der Inhalt der Auflistung betrachtet. In diesem Code wird der [OLE DB-Anbieter für SQL Server](microsoft-ole-db-provider-for-sql-server.md) verwendet, weshalb die **Properties** -Auflistung relevante Informationen zu diesem Anbieter enthält.

```vb 
 
'BeginFieldProps 
 Dim objProp As ADODB.Property 
 
 For intLoop = 0 To (objFields.Count - 1) 
 Debug.Print objFields.Item(intLoop).Name 
 
 For Each objProp In objFields(intLoop).Properties 
 Debug.Print vbTab & objProp.Name & " = " & objProp.Value 
 Next objProp 
 Next intLoop 
'EndFieldProps 
```

## <a name="dealing-with-binary-data"></a>Verwenden von Binärdaten

Verwenden Sie die AppendChunk-Methode in einem Field-Objekt, um es mit Daten vom Typ Long Binary oder mit Zeichendaten zu füllen. Wenn der Arbeitsspeicher begrenzt ist, können Sie mit der AppendChunk-Methode umfangreiche Werte abschnittsweise anstatt in ihrer Gesamtheit bearbeiten.

Wenn das **adFldLong** -Bit in der **Attributes** -Eigenschaft eines **Field** -Objekts auf **True** festgelegt ist, können Sie die **AppendChunk** -Methode für dieses Feld verwenden.

Der erste Aufruf von **AppendChunk** für ein **Field** -Objekt schreibt Daten in das Feld, wobei vorhandene Daten überschrieben werden. Bei nachfolgenden Aufrufen von **AppendChunk** wird an die vorhandenen Daten angefügt. Wenn Sie Daten an ein Feld anfügen und dann den Wert eines anderen Felds im aktuellen Datensatz festlegen oder lesen, geht ADO davon aus, dass Sie keine Daten mehr an das erste Feld anfügen möchten. Wenn Sie die **AppendChunk** -Methode erneut für das erste Feld aufrufen, interpretiert ADO den Aufruf als neuen **AppendChunk** -Vorgang und überschreibt die vorhandenen Daten. Durch den Zugriff auf Felder in anderen **Recordset** -Objekten, die keine Klone des ersten **Recordset** -Objekts sind, werden **AppendChunk** -Vorgänge nicht unterbrochen.

Verwenden Sie die **GetChunk** -Methode für ein **Field** -Objekt, um einen Teil der bzw. die gesamten umfangreichen Binär- oder Zeichendaten abzurufen. In Situationen, bei denen der Systemspeicher beschränkt ist, können Sie die **GetChunk** -Methode verwenden, um umfangreiche Werte in kleinere Einheiten aufzuteilen, statt deren Gesamtheit beizubehalten.

Die Daten, die von einem Aufruf von **GetChunk** zurückgegeben werden, werden einer *Variablen* zugewiesen. Falls die *Größe* die Größe der restlichen Daten überschreitet, gibt die **GetChunk**-Methode nur die restlichen Daten zurück, ohne die *Variable* mit Leerzeichen aufzufüllen. Falls das Feld leer ist, gibt die **GetChunk**-Methode einen NULL-Wert zurück.

Mit jedem nachfolgenden Aufruf von **GetChunk** werden Daten ab dem Punkt abgerufen, an dem der vorherige Aufruf von **GetChunk** beendet wurde. Wenn Sie jedoch Daten aus einem Feld abrufen und dann den Wert eines anderen Felds im aktuellen Datensatz festlegen oder lesen, geht ADO davon aus, dass Sie keine Daten mehr aus dem ersten Feld abrufen möchten. Wenn Sie die **GetChunk** -Methode erneut für das erste Feld aufrufen, interpretiert ADO den Aufruf als neuen **GetChunk** -Vorgang und liest ausgehend vom Anfang der Daten. Durch den Zugriff auf Felder in anderen **Recordset** -Objekten, die keine Klone des ersten **Recordset** -Objekts sind, werden **GetChunk** -Vorgänge nicht unterbrochen.

Wenn das **adFldLong** -Bit in der **Attributes** -Eigenschaft eines **Field** -Objekts auf **True** festgelegt ist, können Sie die **GetChunk** -Methode für dieses Feld verwenden.

Der Fehler 3021 (kein aktueller Datensatz) wird generiert, falls kein aktueller Datensatz vorhanden ist, wenn Sie die Methode **GetChunk** oder **AppendChunk** für ein **Field** -Objekt verwenden.

Ein Beispiel für die Verwendung dieser Methoden zum Bearbeiten von Binärdaten finden Sie in den Beispielen [AppendChunk-Methode](appendchunk-method-ado.md) und [GetChunk-Methode](getchunk-method-ado.md) in der *ADO-Programmierreferenz*.

