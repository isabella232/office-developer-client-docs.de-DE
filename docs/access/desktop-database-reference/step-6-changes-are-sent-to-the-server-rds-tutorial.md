---
title: 'Schritt 6: Senden von Änderungen an den Server (RDS-Lernprogramm)'
TOCTitle: 'Step 6: Changes are Sent to the Server (RDS Tutorial)'
ms:assetid: c5915d89-77b6-bb3f-a962-49378160751f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249965(v=office.15)
ms:contentKeyID: 48547611
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e125837b8f3d16e012d89374650182653f98a728
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870415"
---
# <a name="step-6-changes-are-sent-to-the-server-rds-tutorial"></a><span data-ttu-id="97e4e-102">Step 6: Changes are Sent to the Server (RDS Tutorial)</span><span class="sxs-lookup"><span data-stu-id="97e4e-102">Step 6: Changes are Sent to the Server (RDS Tutorial)</span></span>


<span data-ttu-id="97e4e-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="97e4e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="97e4e-104">Beim Bearbeiten eines **Recordset** -Objekts können alle Änderungen (d. h. hinzugefügte, geänderte oder gelöschte Zeilen) zurück an den Server gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="97e4e-104">If the **Recordset** object is edited, any changes (that is, rows that are added, changed, or deleted) can be sent back to the server.</span></span>


> [!NOTE]
> <P><span data-ttu-id="97e4e-p101">Das Standardverhalten von RDS kann implizit mit ADO-Objekten und dem Microsoft OLE DB-Anbieter für Remoting aufgerufen werden. <STRONG>Recordset</STRONG>-Objekte können in Abfragen zurückgegeben werden, und bearbeitete <STRONG>Recordset</STRONG>-Objekte können die Datenquelle aktualisieren. In diesem Lernprogramm wird RDS nicht mit ADO-Objekten aufgerufen, was folgendermaßen aussehen würde:</span><span class="sxs-lookup"><span data-stu-id="97e4e-p101">The default behavior of RDS can be invoked implicitly with ADO objects and the Microsoft OLE DB Remoting Provider. Queries can return <STRONG>Recordset</STRONG>s, and edited <STRONG>Recordset</STRONG>s can update the data source. This tutorial does not invoke RDS with ADO objects, but this is how it would look if it did:</span></span></P>



```vb 
 
Dim rs as New ADODB.Recordset 
rs.Open "SELECT * FROM Authors","Provider=MS Remote;Data Source=Pubs;" & _ 
 "Remote Server=https://yourServer;Remote Provider=SQLOLEDB;" 
... ' Edit the Recordset. 
rs.UpdateBatch ' The equivalent of SubmitChanges. 
... 
```

<span data-ttu-id="97e4e-108">**Teil A**</span><span class="sxs-lookup"><span data-stu-id="97e4e-108">**Part A**</span></span> 

<span data-ttu-id="97e4e-109">In diesem Fall: Angenommen Sie, Sie nur die [RDS. verwendet haben DataControl](datacontrol-object-rds.md) zugeordnet und ein **Recordset** -Objekt ist jetzt die **RDS. DataControl**.</span><span class="sxs-lookup"><span data-stu-id="97e4e-109">Assume for this case that you have only used the [RDS.DataControl](datacontrol-object-rds.md) and that a **Recordset** object is now associated with the **RDS.DataControl**.</span></span> <span data-ttu-id="97e4e-110">Die Datenquelle wird durch die [SubmitChanges](submitchanges-method-rds.md)-Methode mit allen Änderungen am **Recordset** -Objekt aktualisiert, wenn die Eigenschaften [Server](server-property-rds.md) und [Connect](connect-property-rds.md) noch festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="97e4e-110">The [SubmitChanges](submitchanges-method-rds.md) method updates the data source with any changes to the **Recordset** object if the [Server](server-property-rds.md) and [Connect](connect-property-rds.md) properties are still set.</span></span>

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

<span data-ttu-id="97e4e-111">**Teil B**</span><span class="sxs-lookup"><span data-stu-id="97e4e-111">**Part B**</span></span> 

<span data-ttu-id="97e4e-112">Alternativ können Sie den Server mit dem [RDSServer.DataFactory](datafactory-object-rdsserver.md) -Objekt aktualisieren und eine Verbindung sowie ein **Recordset** -Objekt angeben.</span><span class="sxs-lookup"><span data-stu-id="97e4e-112">Alternatively, you could update the server with the [RDSServer.DataFactory](datafactory-object-rdsserver.md) object, specifying a connection and a **Recordset** object.</span></span>

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

<span data-ttu-id="97e4e-113">**Dies ist das Ende des Lernprogramms.**</span><span class="sxs-lookup"><span data-stu-id="97e4e-113">**This is the end of the tutorial.**</span></span>

