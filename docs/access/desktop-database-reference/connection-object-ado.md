---
title: Connection-Objekt (ADO)
TOCTitle: Connection object (ADO)
ms:assetid: c16023aa-0321-2513-ee71-255d6ffba03d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249940(v=office.15)
ms:contentKeyID: 48547528
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231105
f1_categories:
- Office.Version=v15
ms.openlocfilehash: d7f35c2f76ec8cf2fd671f5ef9eefb42f8555237
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25931386"
---
# <a name="connection-object-ado"></a>Connection-Objekt (ADO)

**Betrifft**: Access 2013, Office 2013

Stellt eine offene Verbindung zu einer Datenquelle dar.

## <a name="remarks"></a>Hinweise

Ein **Connection** -Objekt stellt eine eindeutige Sitzung mit einer Datenquelle dar. Bei einem Client-/Server-Datenbanksystem kann es einer tatsächlichen Netzwerkverbindung mit dem Server entsprechen. Abhängig von der vom Anbieter unterstützten Funktionalität sind bestimmte Auflistungen, Methoden oder Eigenschaften eines **Connection** -Objekts möglicherweise nicht verfügbar.

Die Auflistungen, Methoden und Eigenschaften eines **Connection** -Objekts ermöglichen Folgendes:

  - Konfigurieren der Verbindung vor dem Öffnen mit den Eigenschaften [ConnectionString](connectionstring-property-ado.md), [ConnectionTimeout](connectiontimeout-property-ado.md) und [Mode](mode-property-ado.md). **ConnectionString** ist die Standardeigenschaft des **Connection** -Objekts.

  - Festlegen der [CursorLocation](cursorlocation-property-ado.md)-Eigenschaft auf den Client, der den [Microsoft Cursor Service für OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md), der Batchaktualisierungen unterstützt, aufrufen soll.

  - Festlegen der Standarddatenbank für die Verbindung mit der [DefaultDatabase](defaultdatabase-property-ado.md)-Eigenschaft.

  - Festlegen der Isolationsebene für die Transaktionen, die auf der Verbindung geöffnet wurden, mit der [IsolationLevel](isolationlevel-property-ado.md)-Eigenschaft.

  - Festlegen eines OLE DB-Anbieters mit der [Provider](provider-property-ado.md)-Eigenschaft.

  - Einrichten und nachfolgendes Beenden der physikalischen Verbindung mit der Datenquelle mit den Methoden [Open](open-method-ado-connection.md) und [Close](close-method-ado.md).

  - Ausführen eines Befehls auf der Verbindung mit der [Execute](https://msdn.microsoft.com/library/jj249832\(v=office.15\))-Methode und Konfigurieren der Ausführung mit der [CommandTimeout](commandtimeout-property-ado.md)-Eigenschaft.
    

    > [!NOTE]
    > Um eine Abfrage auszuführen, ohne die Verwendung eines Command-Objekts, übergeben Sie eine Abfragezeichenfolge an der **Execute** -Methode eines **Connection** -Objekts. Ein [Command](command-object-ado.md) -Objekt ist jedoch erforderlich, wenn den Befehlstext beibehalten und erneut ausführen oder Verwenden von Abfrageparametern werden soll.

  - Verwalten der Transaktionen auf der offenen Verbindung, einschließlich geschachtelter Transaktionen, sofern sie vom Anbieter unterstützt werden, mit den Methoden [BeginTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md), [CommitTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) und [RollbackTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) und der [Attributes](attributes-property-ado.md)-Eigenschaft.

  - Untersuchen der von der Datenquelle zurückgegebenen Fehler mit der [Errors](errors-collection-ado.md)-Auflistung.

  - Lesen der Version der ADO-Implementierung mit der [Version](version-property-ado.md)-Eigenschaft.

  - Erhalten von Schemainformationen über die Datenbank mit der [OpenSchema](openschema-method-ado.md)-Methode.

Sie können **Connection** -Objekte unabhängig von allen zuvor definierten Objekten erstellen.

Sie können Befehle oder gespeicherte Prozeduren wie systemeigene Methoden des **Connection** -Objekts verwenden, wie im Folgenden beschrieben.

### <a name="execute-a-command-as-a-native-method-of-a-connection-object"></a>Ausführen eines Befehls als systemeigene Methode eines Connection-Objekts

Zum Ausführen eines Befehls geben Sie ihm zunächst mithilfe der **Name**-Eigenschaft des [Command](name-property-ado.md) -Objekts einen Namen. Geben Sie für die **ActiveConnection** -Eigenschaft des **Command** -Objekts die entsprechende Verbindung an. Verwenden Sie anschließend eine Anweisung, in der Sie den Befehlsnamen wie eine Methode des **Connection** -Objekts verwenden, gefolgt von beliebigen Parametern und einem **Recordset** -Objekt, sofern Zeilen zurückgegeben werden. Legen Sie die **Recordset** -Eigenschaften fest, um das resultierende **Recordset** -Objekt anzupassen. Beispiel:

```vb
    Dim cnn As New ADODB.Connection
    Dim cmd As New ADODB.Command
    Dim rst As New ADODB.Recordset
    ...
    cnn.Open "..."
    cmd.Name = "yourCommandName"
    cmd.ActiveConnection = cnn
    ...
    'Your command name, any parameters, and an optional Recordset.
    cnn.yourCommandName "parameter", rst
```

### <a name="execute-a-stored-procedure-as-a-native-method-of-a-connection-object"></a>Ausführen einer gespeicherten Prozedur als systemeigene Methode eines Connection-Objekts

Verwenden Sie zum Ausführen einer gespeicherten Prozedur eine Anweisung, in der Sie den Namen der gespeicherten Prozedur wie eine Methode des **Connection** -Objekts und gefolgt von beliebigen Parametern angeben. ADO verwendet geeignet erscheinende Parametertypen. Beispiel:

```vb
    Dim cnn As New ADODB.Connection
    ...
    'Your stored procedure name and any parameters.
    cnn.sp_yourStoredProcedureName "parameter"
```
