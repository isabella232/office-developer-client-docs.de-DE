---
title: Datenströme und Permanenz
TOCTitle: Streams and Persistence
ms:assetid: 564fc098-52bf-77d7-9d48-75186483e3fe
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249289(v=office.15)
ms:contentKeyID: 48544949
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: d4446f6577edbdc855596482a19cc44772942b1a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59564841"
---
# <a name="streams-and-persistence"></a>Datenströme und Speicherung


**Gilt für**: Access 2013, Office 2013

Mit der [Save](save-method-ado.md)-Methode des [Recordset](recordset-object-ado.md)-Objekts wird ein **Recordset**-Objekt in einer Datei gespeichert (*permanent gespeichert*), und mit der [Open](open-method-ado-recordset.md)-Methode wird das **Recordset**-Objekt aus dieser Datei wiederhergestellt.

Mit ADO 2.5 kann ein **Recordset** -Objekt auch mit den Methoden **Save** und **Open** in einem [Stream](stream-object-ado.md)-Objekt permanent gespeichert werden. Dieses Feature ist besonders hilfreich beim Arbeiten mit Remote Data Service (RDS) und Active Server Pages (ASP).

Weitere Informationen zur alleinigen Verwendung von Permanenz auf ASP-Seiten finden Sie in der aktuellen ASP-Dokumentation.

Die folgenden Szenarios zeigen, wie **Stream**-Objekte und Permanenz verwendet werden können.

## <a name="scenario-1"></a>Szenario 1

In diesem Szenario wird einfach ein **Recordset**-Objekt in einer Datei und dann in einem **Stream**-Objekt gespeichert. Dann wird der permanent gespeicherte Datenstrom in einem anderen **Recordset**-Objekt geöffnet.

```vb 
 
Dim rs1 As ADODB.Recordset 
Dim rs2 As ADODB.Recordset 
Dim stm As ADODB.Stream 
 
Set rs1 = New ADODB.Recordset 
Set rs2 = New ADODB.Recordset 
Set stm = New ADODB.Stream 
 
rs1.Open "SELECT * FROM Customers", "Provider=sqloledb;" & _ 
 "Data Source=MyServer;Initial Catalog=Northwind;" & _ 
 "Integrated Security=SSPI;""", adopenStatic, adLockReadOnly, adCmdText 
rs1.Save "c:\myfolder\mysubfolder\myrs.xml", adPersistXML 
rs1.Save stm, adPersistXML 
rs2.Open stm 
```

## <a name="scenario-2"></a>Szenario 2

In diesem Szenario wird ein **Recordset**-Objekt permanent in einem **Stream**-Objekt im XML-Format gespeichert. Dann wird das **Stream**-Objekt in eine Zeichenfolge eingelesen, die Sie untersuchen, bearbeiten oder anzeigen können.

```vb 
 
Dim rs As ADODB.Recordset 
Dim stm As ADODB.Stream 
Dim strRst As String 
 
Set rs = New ADODB.Recordset 
Set stm = New ADODB.Stream 
 
' Open, save, and close the recordset. 
rs.Open "SELECT * FROM Customers", "Provider=sqloledb;" & _ 
 "Data Source=MyServer;Initial Catalog=Northwind;" & _ 
 "Integrated Security=SSPI;""" 
rs.Save stm, adPersistXML 
rs.Close 
Set rs = nothing 
 
' Put saved Recordset into a string variable. 
strRst = stm.ReadText(adReadAll) 
 
' Examine, manipulate, or display the XML data. 
... 
```

## <a name="scenario-3"></a>Szenario 3

In diesem Beispielcode wird gezeigt, wie mit ASP-Code ein **Recordset**-Objekt permanent als XML direkt im **Response**-Objekt gespeichert wird:

```vb 
 
... 
<% 
response.ContentType = "text/xml" 
 
' Create and open a Recordset. 
Set rs = Server.CreateObject("ADODB.Recordset") 
rs.Open "select * from Customers", "Provider=sqloledb;" & _ 
 "Data Source=MyServer;Initial Catalog=Northwind;" & _ 
 "Integrated Security=SSPI;""" 
 
' Save Recordset directly into output stream. 
rs.Save Response, adPersistXML 
 
' Close Recordset. 
rs.Close 
Set rs = nothing 
%> 
... 
```

## <a name="scenario-4"></a>Szenario 4

In diesem Szenario wird vom ASP-Code der Inhalt des **Recordset** -Objekts im ADTG-Format auf dem Client geschrieben. Diese Daten können vom [Microsoft Cursor Service für OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md) zum Erstellen eines getrennten **Recordset** -Objekts verwendet werden.

Eine neue Eigenschaft für das [DataControl](datacontrol-object-rds.md)-RDS-Objekt, [URL](url-property-rds.md), zeigt auf die ASP, durch die das **Recordset** -Objekt generiert wird. Das heißt, dass ein **Recordset** -Objekt ohne RDS mithilfe des serverseitigen [DataFactory](datafactory-object-rdsserver.md)-Objekts oder mithilfe eines vom Benutzer geschriebenen Geschäftsobjekts abgerufen werden kann. Dadurch wird das RDS-Programmiermodell erheblich vereinfacht.

Server-side code, named https://server/directory/recordset.asp:

```vb 
 
<% 
Dim rs 
Set rs = Server.CreateObject("ADODB.Recordset") 
rs.Open "select au_fname, au_lname, phone from Authors", ""& _ 
 "Provider=sqloledb;Data Source=MyServer;" & _ 
 "Initial Catalog=Pubs;Integrated Security=SSPI;" 
response.ContentType = "multipart/mixed" 
rs.Save response, adPersistADTG 
%> 
```

Clientseitiger Code:

```html 
 
<HTML> 
<HEAD> 
<TITLE>RDS Query Page</TITLE> 
</HEAD> 
<body> 
<CENTER> 
<H1>Remote Data Service 2.5</H1> 
<TABLE DATASRC="#DC1"> 
 <TR> 
 <TD><SPAN DATAFLD="au_fname"></SPAN></TD> 
 <TD><SPAN DATAFLD="au_lname"></SPAN></TD> 
 <TD><SPAN DATAFLD="phone"></SPAN></TD> 
 </TR> 
</TABLE> 

<BR> 
 
<OBJECT classid="clsid:BD96C556-65A3-11D0-983A-00C04FC29E33" 
 ID=DC1 HEIGHT=1 WIDTH = 1> 
 <PARAM NAME="URL" VALUE="https://server/directory/recordset.asp"> 
</OBJECT> 
 
</SCRIPT> 
</BODY> 
</HTML> 
```

Entwickler verfügen außerdem über die Option, ein **Recordset** -Objekt auf dem Client zu verwenden:

```vb
... 
function GetRs() 
 { 
 rs = CreateObject("ADODB.Recordset"); 
 rs.Open "https://server/directory/recordset.asp" 
 DC1.SourceRecordset = rs; 
 } 
... 
```

