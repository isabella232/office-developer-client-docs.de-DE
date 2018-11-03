---
title: Datenströme und Permanenz
TOCTitle: Streams and Persistence
ms:assetid: 564fc098-52bf-77d7-9d48-75186483e3fe
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249289(v=office.15)
ms:contentKeyID: 48544949
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a90031ac2f6d573631063edb0faf4893c2320d03
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944382"
---
# <a name="streams-and-persistence"></a><span data-ttu-id="2be4b-102">Datenströme und Permanenz</span><span class="sxs-lookup"><span data-stu-id="2be4b-102">Streams and persistence</span></span>


<span data-ttu-id="2be4b-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2be4b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2be4b-104">Mit der [Save](save-method-ado.md)-Methode des [Recordset](recordset-object-ado.md)-Objekts wird ein **Recordset**-Objekt in einer Datei gespeichert (*permanent gespeichert*), und mit der [Open](open-method-ado-recordset.md)-Methode wird das **Recordset**-Objekt aus dieser Datei wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="2be4b-104">The [Recordset](recordset-object-ado.md) object [Save](save-method-ado.md) method stores, or *persists*, a **Recordset** in a file, and the [Open](open-method-ado-recordset.md) method restores the **Recordset** from that file.</span></span>

<span data-ttu-id="2be4b-p101">Mit ADO 2.5 kann ein **Recordset** -Objekt auch mit den Methoden **Save** und **Open** in einem [Stream](stream-object-ado.md)-Objekt permanent gespeichert werden. Dieses Feature ist besonders hilfreich beim Arbeiten mit Remote Data Service (RDS) und Active Server Pages (ASP).</span><span class="sxs-lookup"><span data-stu-id="2be4b-p101">With ADO 2.5, the **Save** and **Open** methods can persist a **Recordset** to a [Stream](stream-object-ado.md) object as well. This feature is especially useful when working with Remote Data Service (RDS) and Active Server Pages (ASP).</span></span>

<span data-ttu-id="2be4b-107">Weitere Informationen zur alleinigen Verwendung von Permanenz auf ASP-Seiten finden Sie in der aktuellen ASP-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="2be4b-107">For more information about how persistence can be used by itself on ASP pages, see the current ASP documentation.</span></span>

<span data-ttu-id="2be4b-108">Die folgenden Szenarios zeigen, wie **Stream** -Objekte und Permanenz verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="2be4b-108">The following are a few scenarios that show how **Stream** objects and persistence can be used.</span></span>

## <a name="scenario-1"></a><span data-ttu-id="2be4b-109">Szenario 1</span><span class="sxs-lookup"><span data-stu-id="2be4b-109">Scenario 1</span></span>

<span data-ttu-id="2be4b-p102">In diesem Szenario wird einfach ein **Recordset** -Objekt in einer Datei und dann in einem **Stream** -Objekt gespeichert. Dann wird der permanent gespeicherte Datenstrom in einem anderen **Recordset** -Objekt geöffnet.</span><span class="sxs-lookup"><span data-stu-id="2be4b-p102">This scenario simply saves a **Recordset** to a file and then to a **Stream**. It then opens the persisted stream into another **Recordset**.</span></span>

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

## <a name="scenario-2"></a><span data-ttu-id="2be4b-112">Szenario 2</span><span class="sxs-lookup"><span data-stu-id="2be4b-112">Scenario 2</span></span>

<span data-ttu-id="2be4b-p103">In diesem Szenario wird ein **Recordset** -Objekt permanent in einem **Stream** -Objekt im XML-Format gespeichert. Dann wird das **Stream** -Objekt in eine Zeichenfolge eingelesen, die Sie untersuchen, bearbeiten oder anzeigen können.</span><span class="sxs-lookup"><span data-stu-id="2be4b-p103">This scenario persists a **Recordset** into a **Stream** in XML format. It then reads the **Stream** into a string that you can examine, manipulate, or display.</span></span>

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

## <a name="scenario-3"></a><span data-ttu-id="2be4b-115">Szenario 3</span><span class="sxs-lookup"><span data-stu-id="2be4b-115">Scenario 3</span></span>

<span data-ttu-id="2be4b-116">In diesem Beispielcode wird gezeigt, wie mit ASP-Code ein **Recordset** -Objekt permanent als XML direkt im **Response** -Objekt gespeichert wird:</span><span class="sxs-lookup"><span data-stu-id="2be4b-116">This example code shows ASP code persisting a **Recordset** as XML directly to the **Response** object:</span></span>

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

## <a name="scenario-4"></a><span data-ttu-id="2be4b-117">Szenario 4</span><span class="sxs-lookup"><span data-stu-id="2be4b-117">Scenario 4</span></span>

<span data-ttu-id="2be4b-p104">In diesem Szenario wird vom ASP-Code der Inhalt des **Recordset** -Objekts im ADTG-Format auf dem Client geschrieben. Diese Daten können vom [Microsoft Cursor Service für OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md) zum Erstellen eines getrennten **Recordset** -Objekts verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2be4b-p104">In this scenario, ASP code writes the contents of the **Recordset** in ADTG format to the client. The [Microsoft Cursor Service for OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md) can use this data to create a disconnected **Recordset**.</span></span>

<span data-ttu-id="2be4b-p105">Eine neue Eigenschaft für das [DataControl](datacontrol-object-rds.md)-RDS-Objekt, [URL](url-property-rds.md), zeigt auf die ASP, durch die das **Recordset** -Objekt generiert wird. Das heißt, dass ein **Recordset** -Objekt ohne RDS mithilfe des serverseitigen [DataFactory](datafactory-object-rdsserver.md)-Objekts oder mithilfe eines vom Benutzer geschriebenen Geschäftsobjekts abgerufen werden kann. Dadurch wird das RDS-Programmiermodell erheblich vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="2be4b-p105">A new property on the RDS [DataControl](datacontrol-object-rds.md), [URL](url-property-rds.md), points to the .asp page that generates the **Recordset**. This means a **Recordset** object can be obtained without RDS using the server-side [DataFactory](datafactory-object-rdsserver.md) object or the user writing a business object. This simplifies the RDS programming model significantly.</span></span>

<span data-ttu-id="2be4b-123">Serverseitigen Code, mit dem Namenhttps://server/directory/recordset.asp:</span><span class="sxs-lookup"><span data-stu-id="2be4b-123">Server-side code, named https://server/directory/recordset.asp:</span></span>

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

<span data-ttu-id="2be4b-124">Clientseitiger Code:</span><span class="sxs-lookup"><span data-stu-id="2be4b-124">Client-side code:</span></span>

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

<span data-ttu-id="2be4b-125">Entwickler verfügen außerdem über die Option, ein **Recordset** -Objekt auf dem Client zu verwenden:</span><span class="sxs-lookup"><span data-stu-id="2be4b-125">Developers also have the option of using a **Recordset** object on the client:</span></span>

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

