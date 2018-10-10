---
title: Weitere Informationen zur Permanenz von Recordsets
TOCTitle: More About Recordset Persistence
ms:assetid: f3248de7-6eef-1dd0-ff96-557b411789e7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250232(v=office.15)
ms:contentKeyID: 48548666
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 05287befde90319ad2844effef8ef2d47e1241b7
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25474843"
---
# <a name="more-about-recordset-persistence"></a><span data-ttu-id="2303f-102">Weitere Informationen zur Permanenz von Recordsets</span><span class="sxs-lookup"><span data-stu-id="2303f-102">More About Recordset Persistence</span></span>


<span data-ttu-id="2303f-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="2303f-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="2303f-104">Das ADO-Recordset-Objekt unterstützt das Speichern von Inhalt für ein **Recordset** -Objekt mithilfe der [Save](save-method-ado.md) -Methode in einer Datei.</span><span class="sxs-lookup"><span data-stu-id="2303f-104">The ADO Recordset object supports storing a **Recordset** object's contents in a file using its [Save](save-method-ado.md) method.</span></span> <span data-ttu-id="2303f-105">Die permanent gespeicherte Datei kann auf einem lokalen Laufwerk, Netzwerkserver oder als URL auf einer Website vorhanden.</span><span class="sxs-lookup"><span data-stu-id="2303f-105">The persistently stored file may exist on a local drive, network server, or as a URL on a website.</span></span> <span data-ttu-id="2303f-106">Die Datei kann später mit der [Open](open-method-ado-recordset.md) -Methode entweder des **Recordset** -Objekts oder die [Execute](https://msdn.microsoft.com/library/jj249832\(v=office.15\)) -Methode des [Connection](connection-object-ado.md) -Objekts wiederhergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="2303f-106">Later, the file can be restored with either the **Recordset** object's [Open](open-method-ado-recordset.md) method or the [Connection](connection-object-ado.md) object's [Execute](https://msdn.microsoft.com/library/jj249832\(v=office.15\)) method.</span></span>

<span data-ttu-id="2303f-107">Außerdem wird durch die [GetString](getstring-method-ado.md)-Methode ein **Recordset** -Objekt in ein Formular konvertiert, dessen Spalten und Zeilen durch die von Ihnen angegebenen Zeichen getrennt sind.</span><span class="sxs-lookup"><span data-stu-id="2303f-107">In addition, the [GetString](getstring-method-ado.md) method converts a **Recordset** object to a form in which the columns and rows are delimited with characters you specify.</span></span>

<span data-ttu-id="2303f-p102">Beginnen Sie, ein **Recordset** permanent zu machen, indem Sie es in ein Formular konvertieren, das in einer Datei gespeichert werden kann. **Recordset** -Objekte können im proprietären ADTG-Format (Advanced Data TableGram) oder im offenen XML-Format (Extensible Markup Language) gespeichert werden. ADTG-Beispiele werden weiter unten gezeigt. Weitere Informationen zur XML-Permanenz finden Sie unter [Speichern von Datensätzen im XML-Format](persisting-records-in-xml-format.md).</span><span class="sxs-lookup"><span data-stu-id="2303f-p102">To persist a **Recordset**, begin by converting it to a form that can be stored in a file. **Recordset** objects can be stored in the proprietary Advanced Data TableGram (ADTG) format or the open Extensible Markup Language (XML) format. ADTG examples are shown below. For more information about XML persistence, see [Persisting Records in XML format](persisting-records-in-xml-format.md).</span></span>

<span data-ttu-id="2303f-p103">Speichern Sie alle ausstehenden Änderungen der permanenten Datei. Dadurch können Sie eine Abfrage ausgeben, von der ein **Recordset** -Objekt zurückgegeben wird und das **Recordset** bearbeitet und zusammen mit den ausstehenden Änderungen gespeichert wird. Später wird das **Recordset** wiederhergestellt, und dann wird die Datenquelle mit den gespeicherten ausstehenden Änderungen aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="2303f-p103">Save any pending changes in the persisted file. Doing this allows you to issue a query that returns a **Recordset** object, edits the **Recordset**, saves it and the pending changes, later restores the **Recordset**, and then updates the data source with the saved pending changes.</span></span>

<span data-ttu-id="2303f-114">Weitere Informationen zum permanenten Speichern von **Stream** -Objekten finden Sie unter [Datenströme und Permanenz](streams-and-persistence.md) in Kapitel 10.</span><span class="sxs-lookup"><span data-stu-id="2303f-114">For information about persistently storing **Stream** objects, see [Streams and Persistence](streams-and-persistence.md) in Chapter 10.</span></span>

<span data-ttu-id="2303f-115">Ein Beispiel für die **Recordset** -Permanenz finden Sie unter [Speicherszenario für XML-Recordset](xml-recordset-persistence-scenario.md).</span><span class="sxs-lookup"><span data-stu-id="2303f-115">For an example of **Recordset** persistence, see the [XML Recordset Persistence Scenario](xml-recordset-persistence-scenario.md).</span></span>

## <a name="example"></a><span data-ttu-id="2303f-116">Beispiel</span><span class="sxs-lookup"><span data-stu-id="2303f-116">Example</span></span>

<span data-ttu-id="2303f-117">**Speichern eines Recordsets:**</span><span class="sxs-lookup"><span data-stu-id="2303f-117">**Save a Recordset:**</span></span>

```vb 
 
Dim rs as New ADODB.Recordset 
rs.Save "c:\yourFile.adtg", adPersistADTG 
```

<span data-ttu-id="2303f-118">**Öffnen einer permanenten Datei mit "Recordset.Open":**</span><span class="sxs-lookup"><span data-stu-id="2303f-118">**Open a persisted file with Recordset.Open:**</span></span>

```vb 
 
Dim rs as New ADODB.Recordset 
rs.Open "c:\yourFile.adtg", "Provider='MSPersist'",,,adCmdFile
```

<span data-ttu-id="2303f-119">Wenn das **Recordset** nicht über eine aktive Verbindung verfügt, können Sie optional alle Standardeinstellungen akzeptieren und einfach folgenden Code schreiben:</span><span class="sxs-lookup"><span data-stu-id="2303f-119">Optionally, if the **Recordset** does not have an active connection, you can accept all the defaults and simply code the following:</span></span>

```vb 
 
Dim rs as New ADODB.Recordset 
rs.Open "c:\yourFile.adtg" 
```

<span data-ttu-id="2303f-120">**Öffnen einer permanenten Datei mit "Connection.Execute":**</span><span class="sxs-lookup"><span data-stu-id="2303f-120">**Open a persisted file with Connection.Execute:**</span></span>

```vb 
 
Dim conn as New ADODB.Connection 
Dim rs as ADODB.Recordset 
conn.Open "Provider='MSPersist'" 
Set rs = conn.execute("c:\yourFile.adtg") 
```

<span data-ttu-id="2303f-121">**Öffnen einer permanenten Datei mit "RDS.DataControl":**</span><span class="sxs-lookup"><span data-stu-id="2303f-121">**Open a persisted file with RDS.DataControl:**</span></span>

<span data-ttu-id="2303f-122">In diesem Fall ist die **Server** -Eigenschaft nicht festgelegt.</span><span class="sxs-lookup"><span data-stu-id="2303f-122">In this case, the **Server** property is not set.</span></span>

```vb 
 
Dim dc as New RDS.DataControl 
dc.Connection = "Provider='MSPersist'" 
dc.SQL = "c:\yourFile.adtg" 
dc.Refresh
```

