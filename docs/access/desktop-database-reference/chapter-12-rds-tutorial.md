---
title: 'Kapitel 12: RdS-Lernprogramm (Remote Data Service)'
TOCTitle: 'Chapter 12: RDS tutorial'
ms:assetid: fa44a5e8-e4df-dfdd-d7a1-a870ec3cabdd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250277(v=office.15)
ms:contentKeyID: 48548837
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 9eacebd7dca32012a9bc645133796158d42abea8
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59586145"
---
# <a name="chapter-12-remote-data-service-rds-tutorial"></a>Kapitel 12: RdS-Lernprogramm (Remote Data Service)

**Gilt für**: Access 2013, Office 2013

Dieses Lernprogramm zeigt, wie eine Datenquelle mit dem RDS-Programmiermodell abgefragt und aktualisiert wird. Zunächst werden die Schritte beschrieben, die für diese Aufgabe nötig sind. Anschließend wird das Lernprogramm in Microsoft Visual Basic Scripting Edition und Microsoft Visual J++ wiederholt und bietet ADO für Windows Foundation Classes (ADO/WFC).

Aus zwei Gründen enthält dieses Lernprogramm Code in verschiedenen Sprachen:

- Die Dokumentation für RDS setzt voraus, dass der Leser Visual Basic-Code verwendet. Dadurch eignet sich die Dokumentation besonders für Visual Basic-Programmierer, für Programmierer anderer Sprachen ist sie jedoch weniger praktisch.

- Wenn Sie bei einem bestimmten Feature von RDS unsicher sind und gewisse Sprachkenntnisse in einer anderen Sprache haben, finden Sie vielleicht eine Lösung zu Ihrer Frage, indem Sie nach demselben Feature in einer anderen Sprache suchen.

Dieses Lernprogramm basiert auf dem RDS-Programmiermodell. Die jeweiligen Schritte des Programmiermodells werden dabei einzeln vorgestellt. Darüber hinaus wird jeder Schritt durch einen Ausschnitt eines Visual Basic-Codes veranschaulicht.

Das Codebeispiel wird ohne ausführliche Erläuterungen in weiteren Sprachen wiederholt. Jeder Schritt in einem Lernprogramm einer bestimmten Sprache ist mit dem entsprechenden Schritt im Programmiermodell und dem erläuternden Lernprogramm gekennzeichnet. Anhand der Schrittnummer finden Sie die Erläuterungen im Lernprogramm.

Das RDS-Programmiermodell wird unten aufgeführt. Verwenden Sie es als Leitfaden, wenn Sie das Lernprogramm durchgehen.

### <a name="rds-programming-model-with-objects"></a>RDS-Programmiermodell mit Objekten

- Geben Sie das auf dem Server aufzurufende Programm an, und ermitteln Sie eine Möglichkeit (Proxy), vom Client darauf zu verweisen.

- Aufrufen des Serverprogramms. Übergeben von Parametern an das Serverprogramm, die die Datenquelle und den auszugebenden Befehl identifizieren.

- Das Serverprogramm ruft ein [Recordset](recordset-object-ado.md)-Objekt aus der Datenquelle ab, in der Regel unter Verwendung von ADO. Das **Recordset** -Objekt kann optional auf dem Server verarbeitet werden.

- Das Serverprogramm gibt das endgültige **Recordset** -Objekt an die Clientanwendung zurück.

- Auf dem Client wird das **Recordset**-Objekt optional in eine Form gebracht, die leicht von visuellen Steuerelementen verwendet werden kann.

- Änderungen am **Recordset**-Objekt werden zurück an den Server gesendet und zur Aktualisierung der Datenquelle verwendet.

## <a name="step-1-specify-a-server-program"></a>Schritt 1: Angeben eines Serverprogramms

Verwenden Sie ganz allgemein die [CreateObject](createobject-method-rds.md)-Methode des [RDS.DataSpace](dataspace-object-rds.md)-Objekts zum Angeben des Standardserverprogramms, [RDSServer.DataFactory](datafactory-object-rdsserver.md), oder Ihres eigenen benutzerdefinierten Serverprogramms (Geschäftsobjekt). Ein Serverprogramm wird auf dem Server instanziiert, und ein Verweis auf das Serverprogramm bzw. den *Proxy* wird zurückgegeben.

In diesem Lernprogramm wird das Standardserverprogramm verwendet:

```vb 
 
Sub RDSTutorial1() 
 Dim DS as New RDS.DataSpace 
 Dim DF as Object 
 Set DF = DS.CreateObject("RDSServer.DataFactory", "https://yourServer") 
... 
``` 

## <a name="step-2-invoke-the-server-program"></a>Schritt 2: Aufrufen des Serverprogramms 

Wenn Sie auf dem Client *proxy* eine Methode aufrufen, wird die Methode vom tatsächlichen Programm auf dem Server ausgeführt. In diesem Schritt führen Sie eine Abfrage auf dem Server durch.

### <a name="part-a"></a>Teil A 

Wenn Sie in diesem Lernprogramm nicht [RDSServer.DataFactory](datafactory-object-rdsserver.md) verwenden würden, wäre die Verwendung des [RDS.DataControl](datacontrol-object-rds.md)-Objekts bei diesem Schritt am praktischsten. Das **RDS.DataControl**-Objekt verbindet den vorherigen Schritt des Erstellens eines Proxys mit diesem Schritt des Erstellens einer Abfrage.

1. Legen Sie den **RDS fest. DataControl-Objekt** [Servereigenschaft,](server-property-rds.md) um zu bestimmen, wo das Serverprogramm instanziiert werden soll.

2. Legen Sie die [eigenschaft Verbinden](connect-property-rds.md) fest, um die Verbindungszeichenfolge für den Zugriff auf die Datenquelle anzugeben.

3. Legen Sie die [SQL-Eigenschaft](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/sql-property-ado) fest, um den Abfragebefehlstext anzugeben. 

4. Stellen Sie die [Refresh-Methode](refresh-method-rds.md) aus, damit das Serverprogramm eine Verbindung mit der Datenquelle herstellt, die von der Abfrage angegebenen Zeilen abruft und ein **Recordset-Objekt** an den Client zurückgibt.

In diesem Lernprogramm wird zwar kein **RDS.DataControl** -Objekt verwendet, es würde jedoch folgendermaßen auftreten:

```vb 
 
Sub RDSTutorial2A() 
 Dim DC as New RDS.DataControl 
 DC.Server = "https://yourServer" 
 DC.Connect = "DSN=Pubs" 
 DC.SQL = "SELECT * FROM Authors" 
 DC.Refresh 
... 
```

<br/>

In diesem Lernprogramm wird RDS auch nicht mit ADO-Objekten aufgerufen, was folgendermaßen aussehen würde:

```vb 
 
Dim rs as New ADODB.Recordset 
rs.Open "SELECT * FROM Authors","Provider=MS Remote;Data Source=Pubs;" & _ 
"Remote Server=https://yourServer;Remote Provider=SQLOLEDB;" 
```

### <a name="part-b"></a>Teil B 

Im Allgemeinen wird dieser Schritt ausgeführt, indem die [Query](query-method-rds.md)-Methode des **RDSServer.DataFactory**-Objekts aufgerufen wird. In diese Methode wird anhand einer Verbindungszeichenfolge eine Verbindung mit der Datenquelle hergestellt, und mit einem Befehlstext werden die Zeilen angegeben, die aus der Datenquelle zurückgegeben werden sollen.

In diesem Lernprogramm wird die **Query** -Methode des **DataFactory** -Objekts verwendet:

```vb 
 
Sub RDSTutorial2B() 
 Dim DS as New RDS.DataSpace 
 Dim DF 
 Dim RS as ADODB.Recordset 
 Set DF = DS.CreateObject("RDSServer.DataFactory", "https://yourServer") 
 Set RS = DF.Query ("DSN=Pubs", "SELECT * FROM Authors") 
... 
```

## <a name="step-3-server-obtains-a-recordset"></a>Schritt 3: Server ruft ein Recordset ab 

Das Serverprogramm verwendet die Verbindungszeichenfolge und den Befehlstext, um die gewünschten Zeilen in der Datenquelle abzufragen. In der Regel wird ADO zum Abrufen dieses **Recordset** -Objekts verwendet, obwohl auch andere Datenzugriffsschnittstellen verwendet werden könnten (z. B. OLE DB).

Ein benutzerdefiniertes Serverprogramm kann folgendermaßen aussehen:

```vb 
 
Public Function ServerProgram(cn as String, qry as String) as Object 
Dim rs as New ADODB.Recordset 
 rs.CursorLocation = adUseClient 
 rs.Open qry, cn 
 rs.ActiveConnection = Nothing 
 Set ServerProgram = rs 
End Function 
```

## <a name="step-4-server-returns-the-recordset"></a>Schritt 4: Server gibt das Recordset zurück 

RDS konvertiert das abgerufene **Recordset**-Objekt in eine Form, die zurück an den Client gesendet werden kann (d. h. das **Recordset**-Objekt wird *gemarshallt*). In welcher Form das Objekt genau konvertiert und gesendet wird, hängt davon ab, ob sich der Server im Internet, dem Intranet oder einem LAN befindet oder ob es sich um eine DLL handelt. Diese Details ist jedoch nicht wichtig. Entscheidend ist, dass RDS das **Recordset**-Objekt zurück an den Client sendet.

Auf dem Client wird ein **Recordset**-Objekt an eine lokale Variable zurückgegeben und dieser Variablen zugewiesen.

```vb 
 
Sub RDSTutorial4() 
 Dim DS as New RDS.DataSpace 
 Dim RS as ADODB.Recordset 
 Dim DF as Object 
 Set DF = DS.CreateObject("RDSServer.DataFactory", "https://yourServer") 
 Set RS = DF.Query("DSN=Pubs", "SELECT * FROM Authors") 
... 
```

## <a name="step-5-datacontrol-is-made-usable"></a>Schritt 5: DataControl wird verwendbar gemacht 

Das zurückgegebene **Recordset**-Objekt kann verwendet werden. Sie können es wie jedes andere **Recordset**-Objekt überprüfen, bearbeiten oder darin navigieren. Die Bearbeitungsmöglichkeiten des **Recordset**-Objekts hängen von der Umgebung ab. Visual Basic und Visual C++ besitzen visuelle Steuerelemente, die ein **Recordset**-Objekt direkt oder indirekt mithilfe eines aktivierenden Datensteuerelements verwenden können.

Wenn Sie beispielsweise eine Webseite in Internet Explorer anzeigen, sollten Sie die **Recordset-Objektdaten** in einem visuellen Steuerelement anzeigen. Visuelle Steuerelemente auf einer Webseite können nicht direkt auf ein **Recordset-Objekt** zugreifen. Der Zugriff auf das **Recordset** ist jedoch über das [RDS.DataControl](datacontrol-object-rds.md)-Objekt möglich. Das **RDS.DataControl**-Objekt kann von einem visuellen Steuerelement verwendet werden, wenn seine [SourceRecordset](recordset-sourcerecordset-properties-rds.md)-Eigenschaft auf das **Recordset**-Objekt festgelegt ist.

Der **DATASRC**-Parameter eines visuellen Steuerelements muss auf **RDS.DataControl** und seine **DATAFLD**-Eigenschaft auf ein **Recordset**-Objektfeld (Spalte) festgelegt sein.

In diesem Lernprogramm legen Sie die **SourceRecordset**-Eigenschaft fest:

```vb 
 
Sub RDSTutorial5() 
 Dim DS as New RDS.DataSpace 
 Dim RS as ADODB.Recordset 
 Dim DC as New RDS.DataControl 
 Dim DF as Object 
 Set DF = DS.CreateObject("RDSServer.DataFactory", "https://yourServer") 
 Set RS = DF.Query ("DSN=Pubs", "SELECT * FROM Authors") 
 DC.SourceRecordset = RS ' Visual controls can now bind to DC. 
... 
```

## <a name="step-6-changes-are-sent-to-the-server"></a>Schritt 6: Änderungen werden an den Server gesendet

Beim Bearbeiten eines **Recordset** -Objekts können alle Änderungen (d. h. hinzugefügte, geänderte oder gelöschte Zeilen) zurück an den Server gesendet werden.

[!HINWEIS] Das Standardverhalten von RDS kann implizit mit ADO-Objekten und dem Microsoft OLE DB-Anbieter für Remoting aufgerufen werden. Abfragen können **Recordsets** zurückgeben, und **bearbeitete Recordsets** können die Datenquelle aktualisieren. In diesem Lernprogramm wird RDS nicht mit ADO-Objekten aufgerufen, was folgendermaßen aussehen würde:

```vb 
 
Dim rs as New ADODB.Recordset 
rs.Open "SELECT * FROM Authors","Provider=MS Remote;Data Source=Pubs;" & _ 
 "Remote Server=https://yourServer;Remote Provider=SQLOLEDB;" 
... ' Edit the Recordset. 
rs.UpdateBatch ' The equivalent of SubmitChanges. 
... 
```

### <a name="part-a"></a>Teil A 

Gehen Sie in diesem Fall davon aus, dass Sie nur das [RDS.DataControl](datacontrol-object-rds.md)-Objekt verwendet haben und dass ein **Recordset**-Objekt nun mit dem **RDS.DataControl**-Objekt verknüpft ist. Die Datenquelle wird durch die [SubmitChanges](submitchanges-method-rds.md)-Methode mit allen Änderungen am **Recordset**-Objekt aktualisiert, wenn die Eigenschaften [Server](server-property-rds.md) und [Connect](connect-property-rds.md) noch festgelegt sind.

```vb 
 
Sub RDSTutorial6A() 
Dim DC as New RDS.DataControl 
Dim RS as ADODB.Recordset 
DC.Server = "https://yourServer" 
DC.Connect = "DSN=Pubs" 
DC.SQL = "SELECT * FROM Authors" 
DC.Refresh 
... 
Set RS = DC.Recordset 
 ' Edit the Recordset. 
... 
DC.SubmitChanges 
... 
```

### <a name="part-b"></a>Teil B 

Sie können alternativ den Server mit dem [RDSServer.DataFactory](datafactory-object-rdsserver.md)-Objekt aktualisieren und eine Verbindung sowie ein **Recordset**-Objekt angeben.

```vb 
 
Sub RDSTutorial6B() 
Dim DS As New RDS.DataSpace 
Dim RS As ADODB.Recordset 
Dim DC As New RDS.DataControl 
Dim DF As Object 
Dim blnStatus As Boolean 
Set DF = DS.CreateObject("RDSServer.DataFactory", "https://yourServer") 
Set RS = DF.Query ("DSN=Pubs", "SELECT * FROM Authors") 
DC.SourceRecordset = RS ' Visual controls can now bind to DC. 
 ' Edit the Recordset. 
blnStatus = DF.SubmitChanges "DSN=Pubs", RS 
End Sub 
```


## <a name="appendix-a-rds-tutorial-vbscript"></a>Anhang A: RDS-Lernprogramm (VBScript)

Dies ist das RDS-Lernprogramm, das in Microsoft Visual Basic Scripting Edition geschrieben wurde. Eine Beschreibung des Zwecks dieses Lernprogramms finden Sie in der Einführung in dieses Thema.

In diesem Lernprogramm: [RDS. DataControl](datacontrol-object-rds.md) und [RDS. DataSpace](dataspace-object-rds.md) werden zur Entwurfszeit erstellt. d. h., sie werden mit Objekttags definiert. Alternativ können diese Objekte auch zur Laufzeit mit der **Server.CreateObject** -Methode erstellt werden. 

Sie können das **RDS.DataControl** -Objekt beispielsweise folgendermaßen erstellen:

```vb
    Set DC = Server.CreateObject("RDS.DataControl") 
     <!-- RDS.DataControl --> 
     <OBJECT 
     ID="DC1" CLASSID="CLSID:BD96C556-65A3-11D0-983A-00C04FC29E33"> 
     </OBJECT> 
     
     <!-- RDS.DataSpace --> 
     <OBJECT 
     ID="DS1" WIDTH=1 HEIGHT=1 
     CLASSID="CLSID:BD96C556-65A3-11D0-983A-00C04FC29E36"> 
     </OBJECT> 
     
     <SCRIPT LANGUAGE="VBScript"> 
     
     Sub RDSTutorial() 
     Dim DF1 
```

### <a name="step-1-specify-a-server-program"></a>Schritt 1: Angeben eines Serverprogramms

VBScript kann den Namen des IIS-Webservers ermitteln, auf dem er ausgeführt wird, indem auf die VBScript **Request.ServerVariables-Methode** zugegriffen wird, die für Active Server Pages verfügbar ist:

```vb 
 
"https://<%=Request.ServerVariables("SERVER_NAME")%>" 
```

Verwenden Sie für dieses Lernprogramm jedoch den imaginären Server "yourServer".

> [!NOTE]
> Pay attention to the data type of **ByRef** arguments. VBScript does not let you specify the variable type, so you must always pass a Variant. When using HTTP, RDS will allow you to pass a Variant to a method that expects a non-Variant if you invoke it with the **RDS.DataSpace** object [CreateObject](createobject-method-rds.md) method. When using DCOM or an in-process server, match the parameter types on the client and server sides or you will receive a "Type Mismatch" error.

```vb
 
Set DF1 = DS1.CreateObject("RDSServer.DataFactory", "https://yourServer") 
```

### <a name="step-2-part-a-invoke-the-server-program-with-rdsdatacontrol"></a>Schritt 2, Teil A: Aufrufen des Serverprogramms mit RDS. DataControl

Das folgende Beispiel dient lediglich zur Veranschaulichung, dass das Standardverhalten des **RDS.DataControl** -Objekts im Ausführen der angegebenen Abfrage besteht.

```vb
 
<OBJECT CLASSID="clsid:BD96C556-65A3-11D0-983A-00C04FC29E33" ID="DC1"> 
 <PARAM NAME="SQL" VALUE="SELECT * FROM Authors"> 
 <PARAM NAME="Connect" VALUE="DSN=Pubs;"> 
 <PARAM NAME="Server" VALUE="https://yourServer/"> 
</OBJECT> 
... 
<SCRIPT LANGUAGE="VBScript"> 
 
Sub RDSTutorial2A() 
 Dim RS 
 DC1.Refresh 
 Set RS = DC1.Recordset 
... 
```

Fahren Sie mit dem folgenden Schritt fort.

### <a name="step-4-server-returns-the-recordset"></a>Schritt 4: Server gibt das Recordset zurück

```vb
 
Set RS = DF1.Query("DSN=Pubs;", "SELECT * FROM Authors") 
```

### <a name="step-5-datacontrol-is-made-usable-by-visual-controls"></a>Schritt 5: DataControl wird von visuellen Steuerelementen verwendet

```vb
 
' Assign the returned recordset to the DataControl. 
 
DC1.SourceRecordset = RS 
```

### <a name="step-6-part-a-changes-are-sent-to-the-server-with-rdsdatacontrol"></a>Schritt 6, Teil A: Änderungen werden mit RDS an den Server gesendet. DataControl

Das folgende Beispiel dient lediglich zur Veranschaulichung, wie das **RDS.DataControl** -Objekt Aktualisierungen ausführt.

```vb
 
<OBJECT CLASSID="clsid:BD96C556-65A3-11D0-983A-00C04FC29E33" ID="DC1"> 
 <PARAM NAME="SQL" VALUE="SELECT * FROM Authors"> 
 <PARAM NAME="Connect" VALUE="DSN=Pubs;"> 
 <PARAM NAME="Server" VALUE="https://yourServer/"> 
</OBJECT> 
... 
<SCRIPT LANGUAGE="VBScript"> 
 
Sub RDSTutorial6A() 
Dim RS 
DC1.Refresh 
... 
Set RS = DC1.Recordset 
' Edit the Recordset object... 
' The SERVER and CONNECT properties are already set from Step 2A. 
Set DC1.SourceRecordset = RS 
... 
DC1.SubmitChanges 
```

### <a name="step-6-part-b-changes-are-sent-to-the-server-with-rdsserverdatafactory"></a>Schritt 6, Teil B: Änderungen werden mit RDSServer.DataFactory an den Server gesendet.

```vb
 
DF.SubmitChanges"DSN=Pubs", RS 
 
End Sub 
</SCRIPT> 
</BODY> 
</HTML> 
```

## <a name="appendix-b-rds-tutorial-visual-j"></a>Anhang B: RDS-Lernprogramm (Visual J++)

ADO/WFC entspricht insofern, als das [RDS.DataControl](datacontrol-object-rds.md)-Objekt nicht implementiert wird, nicht vollständig dem RDS-Objektmodell. ADO/WFC implementiert lediglich die clientseitige Klasse [RDS.DataSpace](dataspace-object-rds.md).

Die **DataSpace** -Klasse implementiert eine [CreateObject](createobject-method-rds.md)-Methode, die wiederum ein [ObjectProxy](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/objectproxy-ado-wfc-syntax)-Objekt zurückgibt. Die **DataSpace** -Klasse implementiert auch die [InternetTimeout](internettimeout-property-rds.md)-Eigenschaft.

The **ObjectProxy** class implements one method, call, which can invoke any server-side business object.

```java 
 
import com.ms.wfc.data.*; 
public class RDSTutorial 
{ 
 public void tutorial() 
 { 
// Step 1: Specify a server program. 
 ObjectProxy obj = 
 DataSpace.createObject( 
 "RDSServer.DataFactory", 
 "https://YourServer"); 
 
// Step 2: Server returns a Recordset. 
 Recordset rs = (Recordset) obj.call( 
 "Query", 
 new Object[] {"DSN=Pubs;", "SELECT * FROM Authors"}); 
 
// Step 3: Changes are sent to the server. 
 ... // Edit Recordset. 
 obj.call( 
 "SubmitChanges", 
 new Object[] {"DSN=Pubs;", rs}); 
 return; 
 } 
} 
```



