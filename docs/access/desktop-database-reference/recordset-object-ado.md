---
title: Recordset-Objekt (ADO)
TOCTitle: Recordset object (ADO)
ms:assetid: 0f963bf8-f066-dc8a-b754-f427de712df1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248865(v=office.15)
ms:contentKeyID: 48543267
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 5baefaa562874eb3a654b6a7dd7ae4e4d7412a35
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59606128"
---
# <a name="recordset-object-ado"></a>Recordset-Objekt (ADO)

**Gilt für**: Access 2013, Office 2013

Stellt den gesamten Satz der Datensätze aus einer Basistabelle oder die Ergebnisse eines ausgeführten Befehls dar. Das **Recordset** -Objekt verweist immer nur auf einen einzelnen Datensatz innerhalb des Satzes als aktueller Datensatz.

## <a name="remarks"></a>HinwBemerkungeneise

Mit **Recordset** -Objekten können Sie Daten eines Anbieters ändern. Wenn Sie ADO verwenden, ändern Sie Daten fast ausschließlich mit **Recordset** -Objekten. Alle **Recordset** -Objekte bestehen aus Datensätzen (Zeilen) und Feldern (Spalten). Abhängig von der vom Anbieter unterstützten Funktionalität sind einige **Recordset** -Methoden oder -Eigenschaften möglicherweise nicht verfügbar.

ADODB.Recordset is the ProgID that should be used to create a **Recordset** object. Existing applications that reference the outdated ADOR.Recordset ProgID will continue to work without recompiling, but new development should reference ADODB.Recordset.

In ADO sind vier verschiedene Cursortypen definiert:

  - **Dynamischer Cursor**. Mit diesem Cursortyp können Sie Hinzufügungen, Änderungen und Löschungen anderer Benutzer anzeigen. Er gestattet alle Typen von Bewegungen innerhalb des **Recordset** -Objekts, für die keine Textmarken erforderlich sind. Außerdem gestattet er Textmarken, sofern der Anbieter Textmarken unterstützt.

  - **Keysetcursor**. Dieser Cursortyp verhält sich wie ein dynamischer Cursor mit dem Unterschied, dass er es Ihnen nicht gestattet, Datensätze anzuzeigen, die von anderen Benutzern hinzugefügt oder gelöscht werden. Datenänderungen anderer Benutzer sind sichtbar. Dieser Cursortyp unterstützt immer Textmarken und gestattet damit alle Typen von Bewegungen innerhalb des **Recordset** -Objekts.

  - **Statischer Cursor**. Dieser Cursortyp bietet eine statische Kopie einer Datensatzgruppe, die Sie zum Suchen von Daten oder Generieren von Berichten verwenden können. Der Cursortyp gestattet immer Textmarken und damit alle Typen von Bewegungen innerhalb des **Recordset** -Objekts. Hinzufügungen, Änderungen oder Löschungen anderer Benutzer sind nicht zu sehen. Dies ist der einzige erlaubte Cursortyp, wenn Sie ein clientseitiges **Recordset** -Objekt erstellen.

  - **Vorwärtsgerichteter Cursor** . Dieser Cursortyp gestattet nur ein vorwärtsgerichtetes Abrollen des **Recordset**-Objekts. Hinzufügungen, Änderungen und Löschungen anderer Benutzer sind nicht zu sehen. Dadurch wird die Leistung in Situationen verbessert, in denen Sie nur einen einzelnen Schritt durch ein **Recordset**-Objekt ausführen müssen.

Legen Sie vor dem Öffnen des **Recordset**-Objekts die [CursorType](cursortype-property-ado.md)-Eigenschaft fest, um den Cursortyp auszuwählen, oder übergeben Sie ein *CursorType*-Argument mit der [Open](open-method-ado-recordset.md)-Methode. Einige Anbieter unterstützen nicht alle Cursortypen. Überprüfen Sie die Dokumentation des Anbieters diesbezüglich. Wenn Sie keinen Cursortyp festlegen, öffnet ADO standardmäßig einen vorwärtsgerichteten Cursor.

Wenn die [CursorLocation](cursorlocation-property-ado.md)-Eigenschaft auf den Wert **adUseClient** festgelegt ist, um ein **Recordset** -Objekt zu öffnen, ist die **UnderlyingValue** -Eigenschaft des [Field](field-object-ado.md)-Objekts im zurückgegebenen **Recordset** -Objekt nicht verfügbar. Bei der Verwendung dieser Eigenschaft mit bestimmten Anbietern (z. B. der Microsoft OLE DB-Anwender für ODBC in Verbindung mit Microsoft SQL Server) können Sie **Recordset** -Objekte unabhängig von einem zuvor definierten [Connection](connection-object-ado.md)-Objekt erstellen, indem Sie eine Verbindungszeichenfolge mit der **Open** -Methode übergeben. ADO erstellt dennoch ein [Connection](connection-object-ado.md)-Objekt, weist dieses Objekt jedoch keiner Objektvariablen zu. Wenn Sie mehrere **Recordset** -Objekte über dieselbe Verbindung öffnen, sollten Sie explizit ein **Connection** -Objekt erstellen und öffnen. Dadurch wird das **Connection** -Objekt einer Objektvariablen zugewiesen. Wenn Sie diese Objektvariable beim Öffnen Ihrer **Recordset** -Objekte nicht verwenden, erstellt ADO für jedes neue **Recordset** -Objekt ein neues **Connection** -Objekt, selbst wenn Sie dieselbe Verbindungszeichenfolge übergeben.

Sie können beliebig viele **Recordset** -Objekte erstellen.

Wenn Sie ein **Recordset** -Objekt öffnen, wird der aktuelle Datensatz an die Position des ersten Datensatzes platziert (falls vorhanden), und die Eigenschaften [BOF](bof-eof-properties-ado.md) und [EOF](bof-eof-properties-ado.md) erhalten den Wert **False**. Wenn keine Datensätze enthalten sind, haben die Eigenschaften **BOF** und **EOF** den Wert **True**.

Mit den Methoden [MoveFirst](movefirst-movelast-movenext-and-moveprevious-methods-ado.md), **MoveLast**, **MoveNext** und **MovePrevious**, der [Move](move-method-ado.md)-Methode und den Eigenschaften [AbsolutePosition](absoluteposition-property-ado.md), [AbsolutePage](absolutepage-property-ado.md) und [Filter](filter-property-ado.md) können Sie den aktuellen Datensatz neu positionieren, sofern der Anbieter die betreffende Funktionalität unterstützt. Vorwärtsgerichtete **Recordset**-Objekte unterstützen nur die [MoveNext](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)-Methode. Wenn Sie die **Move**-Methoden verwenden, um zu den einzelnen Datensätzen zu navigieren (oder um das **Recordset**-Objekt in einer Schleife zu durchlaufen), können Sie mithilfe der Eigenschaften **BOF** und **EOF** feststellen, ob Sie vor den Anfang oder hinter das Ende des **Recordset**-Objekts navigiert sind.

**Recordset** -Objekte können zwei Typen von Aktualisierungen unterstützen: die sofortige Aktualisierung und die Batchaktualisierung. Bei der sofortigen Aktualisierung werden alle Datenänderungen sofort, wenn Sie die [Update](update-method-ado.md)-Methode aufrufen, in die zugrunde liegende Datenquelle geschrieben. Sie können auch mit den Methoden [AddNew](addnew-method-ado.md) und **Update** ein Array von Werten als Parameter übergeben und mehrere Felder in einem Datensatz gleichzeitig aktualisieren.

Wenn ein Anbieter die Batchaktualisierung unterstützt, können Sie dafür sorgen, dass der Anbieter Änderungen an mehreren Datensätzen zwischenspeichert und die Änderungen dann in einem einzigen Aufruf mit der [UpdateBatch](updatebatch-method-ado.md)-Methode an die Datenbank übergibt. Dies gilt für Änderungen, die mit den Methoden **AddNew**, **Update** und [Delete](delete-method-ado-recordset.md) vorgenommen werden. Wenn Sie die **UpdateBatch** -Methode aufgerufen haben, können Sie mit der [Status](status-property-ado-recordset.md)-Eigenschaft nach Datenkonflikten suchen, um sie zu lösen.

> [!NOTE]
> [!HINWEIS] Sie können eine Abfrage ohne Verwendung eines [Command](command-object-ado.md)-Objekts ausführen, indem Sie eine Abfragezeichenfolge an die **Open** -Methode eines **Recordset** -Objekts übergeben. Wenn Sie den Befehlstext speichern und erneut ausführen möchten, ist jedoch ein **Command** -Objekt erforderlich. Sie können aber auch Abfrageparameter verwenden.

Die [Mode](mode-property-ado.md)-Eigenschaft steuert die Zugriffsberechtigungen.

Die **Fields** -Auflistung ist das Standardmitglied des **Recordset** -Objekts. Die beiden folgenden Codeanweisungen haben daher dieselbe Bedeutung.

```vb
    Debug.Print objRs.Fields.Item(0)  ' Both statements print 
    Debug.Print objRs(0)              '  the Value of Item(0).
```
