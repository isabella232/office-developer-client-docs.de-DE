---
title: Speichern von Daten (Access PC-Datenbank-Referenz)
TOCTitle: Persisting Data
ms:assetid: cb8a32f7-2cdc-26ed-c6d4-dd93c1ac37ba
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250010(v=office.15)
ms:contentKeyID: 48547715
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1fdac02c2293088c60c3346b333b6619777b9a18
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25862912"
---
# <a name="persisting-data"></a><span data-ttu-id="a6a09-102">Speichern von Daten</span><span class="sxs-lookup"><span data-stu-id="a6a09-102">Persisting Data</span></span>


<span data-ttu-id="a6a09-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="a6a09-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="a6a09-p101">Tragbare Computer (z. B. Laptops) haben Anwendungen erforderlich gemacht, die online und offline ausgeführt werden können. ADO unterstützt dies nun, indem der Entwickler ein Clientcursor- **Recordset** auf einem Datenträger speichern und später erneut laden kann.</span><span class="sxs-lookup"><span data-stu-id="a6a09-p101">Portable computing (for example, using laptops) has generated the need for applications that can run in both a connected and disconnected state. ADO has added support for this by giving the developer the ability to save a client cursor **Recordset** to disk and reload it later.</span></span>

<span data-ttu-id="a6a09-106">Für dieses Feature gibt es verschiedene Einsatzmöglichkeiten:</span><span class="sxs-lookup"><span data-stu-id="a6a09-106">There are several scenarios in which you could use this type of feature, including the following:</span></span>

- <span data-ttu-id="a6a09-107">**Unterwegs:** Wenn Sie mit der Anwendung unterwegs sind, müssen unbedingt Änderungen vorgenommen und neue Datensätze hinzugefügt werden können, die dann später erneut mit der Datenbank verbunden werden können und für die ein Commit ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="a6a09-107">**Traveling:** When taking the application on the road, it is vital to supply the ability to make changes and add new records that can then be reconnected to the database later and committed.</span></span>

- <span data-ttu-id="a6a09-p102">**Selten aktualisierte Lookuptabellen:** Bei einer Anwendung werden Tabellen oft zum Nachschlagen verwendet, z. B. Steuertabellen. Sie werden selten aktualisiert und sind schreibgeschützt. Anstatt diese Daten bei jedem Start der Anwendung erneut vom Server einzulesen, kann die Anwendung die Daten einfach von einem lokal gespeicherten **Recordset** -Objekt laden.</span><span class="sxs-lookup"><span data-stu-id="a6a09-p102">**Infrequently updated lookups:** Often in an application, tables are used as lookups — for example, state tax tables. They are infrequently updated and are read-only. Instead of rereading this data from the server each time the application is started, the application can simply load the data from a locally persisted **Recordset**.</span></span>

<span data-ttu-id="a6a09-111">Verwenden Sie in ADO zum Speichern und Laden von **Recordset** -Objekten die Methoden **Recordset.Save** und **Recordset.Open(,,,,adCmdFile)** im **Recordset** -Objekt von ADO.</span><span class="sxs-lookup"><span data-stu-id="a6a09-111">In ADO, to save and load **Recordsets**, use the **Recordset.Save** and **Recordset.Open(,,,,adCmdFile)** methods on the ADO **Recordset** object.</span></span>

<span data-ttu-id="a6a09-p103">Sie können die **Save** -Methode des **Recordset** -Objekts zum Speichern des **Recordset** -Objekts von ADO in einer Datei auf einem Datenträger verwenden. (Ein **Recordset** -Objekt kann auch in einem **Stream** -Objekt von ADO gespeichert werden. **Stream** -Objekte werden weiter unten in diesem Handbuch behandelt.) Später können Sie mit der **Open** -Methode das **Recordset** -Objekt erneut öffnen, wenn Sie es benötigen. Standardmäßig speichert ADO das **Recordset** -Objekt im systemeigenen Microsoft Advanced Data TableGram-Format (ADTG). Dieses binäre Format wird mithilfe des **adPersistADTG** -Werts für **PersistFormatEnum** angegeben. Alternativ können Sie das **Recordset** -Objekt stattdessen mithilfe von **adPersistXML** im XML-Format speichern. Weitere Informationen zum Speichern von Datensätzen im XML-Format finden Sie unter [Speichern von Datensätzen im XML-Format](persisting-records-in-xml-format.md).</span><span class="sxs-lookup"><span data-stu-id="a6a09-p103">You can use the **Recordset** **Save** method to persist your ADO **Recordset** to a file on a disk. (You can also save a **Recordset** to an ADO **Stream** object. **Stream** objects are discussed later in the guide.) Later, you can use the **Open** method to reopen the **Recordset** when you are ready to use it. By default, ADO saves the **Recordset** into the proprietary Microsoft Advanced Data TableGram (ADTG) format. This binary format is specified using the **adPersistADTG** **PersistFormatEnum** value. Alternatively, you may choose to save your **Recordset** out as XML instead using **adPersistXML**. For more information about saving Recordsets as XML, see [Persisting Records in XML Format](persisting-records-in-xml-format.md).</span></span>

<span data-ttu-id="a6a09-119">Die **Save** -Methode weist die folgende Syntax auf:</span><span class="sxs-lookup"><span data-stu-id="a6a09-119">The syntax of the **Save** method is as follows:</span></span>

`recordset.Save Destination, PersistFormat`

<span data-ttu-id="a6a09-p104">Wenn Sie das **Recordset**-Objekt das erste Mal speichern, können Sie optional das *Ziel* angeben. Wenn Sie das *Ziel* auslassen, wird eine neue Datei erstellt, deren Namen auf den Wert der [Source](source-property-ado-recordset.md)-Eigenschaft des **Recordset**-Objekts festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="a6a09-p104">The first time you save the **Recordset**, it is optional to specify *Destination*. If you omit *Destination*, a new file will be created with a name set to the value of the [Source](source-property-ado-recordset.md) property of the **Recordset**.</span></span>

<span data-ttu-id="a6a09-p105">Lassen Sie das *Ziel* aus, wenn Sie anschließend **Save** nach dem ersten Speichern aufrufen, da ansonsten ein Laufzeitfehler generiert wird. Wenn Sie danach **Save** mit einem neuen *Ziel* aufrufen, wird das **Recordset**-Objekt im neuen Ziel gespeichert. Das neue Ziel und das ursprüngliche Ziel sind jedoch beide geöffnet.</span><span class="sxs-lookup"><span data-stu-id="a6a09-p105">Omit *Destination* when you subsequently call **Save** after the first save or a run-time error will occur. If you subsequently call **Save** with a new *Destination*, the **Recordset** is saved to the new destination. However, the new destination and the original destination will both be open.</span></span>

<span data-ttu-id="a6a09-p106">Mit **Save** wird das **Recordset**-Objekt oder das *Ziel* nicht geschlossen, weshalb Sie weiter mit dem **Recordset**-Objekt arbeiten und die neuesten Änderungen speichern können. Das *Ziel* bleibt so lange geöffnet, bis das **Recordset**-Objekt geschlossen wird. In dieser Zeit können andere Anwendungen das *Ziel* lesen, aber nicht in dieses schreiben.</span><span class="sxs-lookup"><span data-stu-id="a6a09-p106">**Save** does not close the **Recordset** or *Destination*, so you can continue to work with the **Recordset** and save your most recent changes. *Destination* remains open until the **Recordset** is closed, during which time other applications can read but not write to *Destination*.</span></span>

<span data-ttu-id="a6a09-p107">Aus Sicherheitsgründen gestattet die **Save** -Methode nur die Verwendung niedriger und benutzerdefinierter Sicherheitseinstellungen in einem von Microsoft Internet Explorer ausgeführten Skript. Ausführlichere Erläuterungen zu Sicherheitsproblemen finden Sie unter "ADO- und RDS-Sicherheitsprobleme in Microsoft Internet Explorer" (in englischer Sprache) im Abschnitt "ActiveX Data Objects (ADO) Technical Articles in Microsoft Data Access Technical Articles".</span><span class="sxs-lookup"><span data-stu-id="a6a09-p107">For reasons of security, the **Save** method permits only the use of low and custom security settings from a script executed by Microsoft Internet Explorer. For a more detailed explanation of security issues, see "ADO and RDS Security Issues in Microsoft Internet Explorer" under ActiveX Data Objects (ADO) Technical Articles in Microsoft Data Access Technical Articles.</span></span>

<span data-ttu-id="a6a09-129">Wenn die **Save** -Methode während eines asynchronen Abruf-, Ausführungs- oder Aktualisierungsvorgangs des **Recordset** -Objekts aufgerufen wird, wartet die **Save** -Methode, bis der asynchrone Vorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="a6a09-129">If the **Save** method is called while an asynchronous **Recordset** fetch, execute, or update operation is in progress, **Save** waits until the asynchronous operation is complete.</span></span>

<span data-ttu-id="a6a09-p108">Datensätze werden ab der ersten Zeile des **Recordset** -Objekts gespeichert. Wenn die **Save** -Methode abgeschlossen ist, wird die erste Zeile des **Recordset** -Objekts zur aktuellen Zeile.</span><span class="sxs-lookup"><span data-stu-id="a6a09-p108">Records are saved beginning with the first row of the **Recordset**. When the **Save** method is finished, the current row position is moved to the first row of the **Recordset**.</span></span>

<span data-ttu-id="a6a09-p109">Legen Sie die [CursorLocation](cursorlocation-property-ado.md)-Eigenschaft mithilfe von **Save** auf **adUseClient** fest, um optimale Ergebnisse zu erzielen. Wenn Ihr Anbieter nicht die gesamte zum Speichern von **Recordset** -Objekten erforderliche Funktionalität unterstützt, bietet der Cursordienst diese Funktionalität.</span><span class="sxs-lookup"><span data-stu-id="a6a09-p109">For best results, set the [CursorLocation](cursorlocation-property-ado.md) property to **adUseClient** with **Save**. If your provider does not support all of the functionality necessary to save **Recordset** objects, the Cursor Service will provide that functionality.</span></span>

<span data-ttu-id="a6a09-p110">Wenn ein **Recordset** -Objekt gespeichert wird, während die **CursorLocation** -Eigenschaft auf **adUseServer** festgelegt ist, sind die Aktualisierungsmöglichkeiten für das **Recordset** -Objekt eingeschränkt. Normalerweise ist nur das Aktualisieren, Einfügen und Löschen für eine einzelne Tabelle zulässig (in Abhängig von der Providerfunktionalität). Die [Resync](resync-method-ado.md)-Methode ist in dieser Konfiguration ebenfalls nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a6a09-p110">When a **Recordset** is persisted with the **CursorLocation** property set to **adUseServer**, the update capability for the **Recordset** is limited. Typically, only single-table updates, insertions, and deletions are allowed (dependent on provider functionality). The [Resync](resync-method-ado.md) method is also unavailable in this configuration.</span></span>

<span data-ttu-id="a6a09-137">Da *der Zielparameter* jedes Objekt, die die OLE DB **IStream** -Schnittstelle unterstützt akzeptieren kann, können Sie ein **Recordset-Objekt** direkt auf das ASP- **Response** -Objekt speichern.</span><span class="sxs-lookup"><span data-stu-id="a6a09-137">Because the *Destination* parameter can accept any object that supports the OLE DB **IStream** interface, you can save a **Recordset** directly to the ASP **Response** object.</span></span>

<span data-ttu-id="a6a09-138">Im folgenden Beispiel wird mit den Methoden **Save** und **Open** ein **Recordset** -Objekt gespeichert und später erneut geöffnet:</span><span class="sxs-lookup"><span data-stu-id="a6a09-138">In the following example, the **Save** and **Open** methods are used to persist a **Recordset** and later reopen it:</span></span>

```vb 
 
'BeginPersist 
 conn.ConnectionString = _ 
 "Provider='SQLOLEDB';Data Source='MySqlServer';" _ 
 & "Integrated Security='SSPI';Initial Catalog='pubs'" 
 conn.Open 
 
 conn.Execute "create table testtable (dbkey int " & _ 
 "primary key, field1 char(10))" 
 conn.Execute "insert into testtable values (1, 'string1')" 
 
 Set rst.ActiveConnection = conn 
 rst.CursorLocation = adUseClient 
 
 rst.Open "select * from testtable", conn, adOpenStatic, _ 
 adLockBatchOptimistic 
 
 'Change the row on the client 
 rst!field1 = "NewValue" 
 
 'Save to a file--the .dat extension is an example; choose 
 'your own extension. The changes will be saved in the file 
 'as well as the original data. 
 MyFile = Dir("c:\temp\temptbl.dat") 
 If MyFile <> "" Then 
 Kill "c:\temp\temptbl.dat" 
 End If 
 
 rst.Save "c:\temp\temptbl.dat", adPersistADTG 
 rst.Close 
 Set rst = Nothing 
 
 'Now reload the data from the file 
 Set rst = New ADODB.Recordset 
 rst.Open "c:\temp\temptbl.dat", , adOpenStatic, _ 
 adLockBatchOptimistic, adCmdFile 
 
 Debug.Print "After Loading the file from disk" 
 Debug.Print " Current Edited Value: " & rst!field1.Value 
 Debug.Print " Value Before Editing: " & rst!field1.OriginalValue 
 
 'Note that you can reconnect to a connection and 
 'submit the changes to the data source 
 Set rst.ActiveConnection = conn 
 rst.UpdateBatch 
'EndPersist 
```

<span data-ttu-id="a6a09-139">Dieser Abschnitt enthält die folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="a6a09-139">This section includes the following topics:</span></span>

- [<span data-ttu-id="a6a09-140">More About Recordset Persistence</span><span class="sxs-lookup"><span data-stu-id="a6a09-140">More About Recordset Persistence</span></span>](more-about-recordset-persistence.md)

- [<span data-ttu-id="a6a09-141">Beibehalten von gefilterten und hierarchischen Recordsets</span><span class="sxs-lookup"><span data-stu-id="a6a09-141">Persisting Filtered and Hierarchical Recordsets</span></span>](persisting-filtered-and-hierarchical-recordsets.md)

- [<span data-ttu-id="a6a09-142">Persisting Records in XML Format (ADO)</span><span class="sxs-lookup"><span data-stu-id="a6a09-142">Persisting Records in XML Format (ADO)</span></span>](persisting-records-in-xml-format.md)