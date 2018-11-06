---
title: 'Schritt 6: Senden von Änderungen an den Server (RDS-Lernprogramm)'
TOCTitle: 'Step 6: Changes are Sent to the Server (RDS Tutorial)'
ms:assetid: c5915d89-77b6-bb3f-a962-49378160751f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249965(v=office.15)
ms:contentKeyID: 48547611
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a9f75e5215e3e3d79363ab7110f7c16bcacf3cbb
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998994"
---
# <a name="step-6-changes-are-sent-to-the-server-rds-tutorial"></a><span data-ttu-id="642e1-102">Schritt 6: Änderungen werden an den Server (RDS-Lernprogramm) gesendet.</span><span class="sxs-lookup"><span data-stu-id="642e1-102">Step 6: Changes are sent to the server (RDS Tutorial)</span></span>

<span data-ttu-id="642e1-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="642e1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="642e1-104">Beim Bearbeiten eines **Recordset** -Objekts können alle Änderungen (d. h. hinzugefügte, geänderte oder gelöschte Zeilen) zurück an den Server gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="642e1-104">If the **Recordset** object is edited, any changes (that is, rows that are added, changed, or deleted) can be sent back to the server.</span></span>

<span data-ttu-id="642e1-105">[!HINWEIS] Das Standardverhalten von RDS kann implizit mit ADO-Objekten und dem Microsoft OLE DB-Anbieter für Remoting aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="642e1-105">The default behavior of RDS can be invoked implicitly with ADO objects and the Microsoft OLE DB Remoting Provider.</span></span> <span data-ttu-id="642e1-106">Abfragen können **Recordsets**zurückgegeben und bearbeiteten **Recordsets** kann die Datenquelle aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="642e1-106">Queries can return **Recordsets**, and edited **Recordsets** can update the data source.</span></span> <span data-ttu-id="642e1-107">In diesem Lernprogramm wird RDS nicht mit ADO-Objekten aufgerufen, was folgendermaßen aussehen würde:</span><span class="sxs-lookup"><span data-stu-id="642e1-107">This tutorial does not invoke RDS with ADO objects, but this is how it would look if it did:</span></span>

```vb 
 
Dim rs as New ADODB.Recordset 
rs.Open "SELECT * FROM Authors","Provider=MS Remote;Data Source=Pubs;" & _ 
 "Remote Server=https://yourServer;Remote Provider=SQLOLEDB;" 
... ' Edit the Recordset. 
rs.UpdateBatch ' The equivalent of SubmitChanges. 
... 
```

<span data-ttu-id="642e1-108">**Teil A**</span><span class="sxs-lookup"><span data-stu-id="642e1-108">**Part A**</span></span> 

<span data-ttu-id="642e1-109">In diesem Fall: Angenommen Sie, Sie nur die [RDS. verwendet haben DataControl](datacontrol-object-rds.md) zugeordnet und ein **Recordset** -Objekt ist jetzt die **RDS. DataControl**.</span><span class="sxs-lookup"><span data-stu-id="642e1-109">Assume for this case that you have only used the [RDS.DataControl](datacontrol-object-rds.md) and that a **Recordset** object is now associated with the **RDS.DataControl**.</span></span> <span data-ttu-id="642e1-110">Die Datenquelle wird durch die [SubmitChanges](submitchanges-method-rds.md)-Methode mit allen Änderungen am **Recordset** -Objekt aktualisiert, wenn die Eigenschaften [Server](server-property-rds.md) und [Connect](connect-property-rds.md) noch festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="642e1-110">The [SubmitChanges](submitchanges-method-rds.md) method updates the data source with any changes to the **Recordset** object if the [Server](server-property-rds.md) and [Connect](connect-property-rds.md) properties are still set.</span></span>

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

<span data-ttu-id="642e1-111">**Teil B**</span><span class="sxs-lookup"><span data-stu-id="642e1-111">**Part B**</span></span> 

<span data-ttu-id="642e1-112">Alternativ können Sie den Server mit dem [RDSServer.DataFactory](datafactory-object-rdsserver.md) -Objekt aktualisieren und eine Verbindung sowie ein **Recordset** -Objekt angeben.</span><span class="sxs-lookup"><span data-stu-id="642e1-112">Alternatively, you could update the server with the [RDSServer.DataFactory](datafactory-object-rdsserver.md) object, specifying a connection and a **Recordset** object.</span></span>

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

<span data-ttu-id="642e1-113">**Dies ist das Ende des Lernprogramms.**</span><span class="sxs-lookup"><span data-stu-id="642e1-113">**This is the end of the tutorial.**</span></span>

