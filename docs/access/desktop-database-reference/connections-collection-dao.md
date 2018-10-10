---
title: Connections Collection (DAO)
TOCTitle: Connections Collection
ms:assetid: 65d073be-a84b-e3f2-cb43-b87ffa60e497
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195178(v=office.15)
ms:contentKeyID: 48545330
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: cb8c41917ab6834cda15a706ae550751698543eb
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25474686"
---
# <a name="connections-collection-dao"></a><span data-ttu-id="8db17-102">Connections Collection (DAO)</span><span class="sxs-lookup"><span data-stu-id="8db17-102">Connections Collection (DAO)</span></span>


<span data-ttu-id="8db17-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="8db17-103">**Applies to**: Access 2013 | Office 2013</span></span>


> [!NOTE]
> <span data-ttu-id="8db17-p101">[!HINWEIS] ODBCDirect-Arbeitsbereiche werden in Microsoft Access 2013 nicht unterstützt. Verwenden Sie ADO, wenn Sie auf externe Datenquellen zugreifen möchten, ohne das Microsoft Access-Datenbankmodul zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="8db17-p101">ODBCDirect workspaces are not supported in Microsoft Access 2013. Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span>



<span data-ttu-id="8db17-p102">Eine **Connections**-Auflistung enthält die aktuellen **Connection**-Objekte eines **Workspace**-Objekts. (Gilt nur für ODBCDirect-Arbeitsbereiche.)</span><span class="sxs-lookup"><span data-stu-id="8db17-p102">A **Connections** collection contains the current **Connection** objects of a **Workspace** object. (ODBCDirect workspaces only).</span></span>

## <a name="remarks"></a><span data-ttu-id="8db17-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8db17-108">Remarks</span></span>

<span data-ttu-id="8db17-p103">Wenn Sie ein **Connection**-Objekt öffnen, wird es automatisch an die **Connections**-Auflistung des **Workspace**-Objekts angefügt. Wenn Sie ein **Connection**-Objekt über die **[Close](connection-close-method-dao.md)** -Methode schließen, wird es aus der **Connections**-Auflistung entfernt. Bevor Sie das Objekt schließen, sollten Sie alle geöffneten **[Recordset](recordset-object-dao.md)** -Objekte im **Connection**-Objekt schließen.</span><span class="sxs-lookup"><span data-stu-id="8db17-p103">When you open a **Connection** object, it is automatically appended to the **Connections** collection of the **Workspace**. When you close a **Connection** object with the **[Close](connection-close-method-dao.md)** method, it is removed from the **Connections** collection. You should close all open **[Recordset](recordset-object-dao.md)** objects within the **Connection** before closing it.</span></span>

<span data-ttu-id="8db17-p104">Wenn Sie ein **Connection**-Objekt öffnen, wird gleichzeitig ein entsprechendes **[Database](database-object-dao.md)** -Objekt erstellt und an die **[Databases](databases-collection-dao.md)** -Auflistung in demselben **Workspace**-Objekt angefügt (und umgekehrt). Und wenn Sie das **Connection**-Objekt schließen, wird das entsprechende **Database**-Objekt aus der **Databases**-Auflistung entfernt usw.</span><span class="sxs-lookup"><span data-stu-id="8db17-p104">At the same time you open a **Connection** object, a corresponding **[Database](database-object-dao.md)** object is created and appended to the **[Databases](databases-collection-dao.md)** collection in the same **Workspace**, and vice versa. Similarly, when you close the **Connection**, the corresponding **Database** is deleted from the **Databases** collection, and so on.</span></span>

<span data-ttu-id="8db17-p105">Die Einstellung der **Name**-Eigenschaft eines **Connection**-Objekts ist eine Zeichenfolge, die den Pfad zur Datenbankdatei angibt. Der Verweis auf ein **Connection**-Objekt in einer Auflistung erfolgt über dessen Ordnungszahl oder den Wert der **Name**-Eigenschaft, wobei Sie die folgenden Syntaxformen verwenden können:</span><span class="sxs-lookup"><span data-stu-id="8db17-p105">The **Name** property setting of a **Connection** is a string that specifies the path of the database file. To refer to a **Connection** object in a collection by its ordinal number or by its **Name** property setting, use any of the following syntax forms:</span></span>

  - <span data-ttu-id="8db17-116">**Connections**(0)</span><span class="sxs-lookup"><span data-stu-id="8db17-116">**Connections**(0)</span></span>

  - <span data-ttu-id="8db17-117">**Verbindungen** ("*Name*")</span><span class="sxs-lookup"><span data-stu-id="8db17-117">**Connections**("*name*")</span></span>

  - <span data-ttu-id="8db17-118">**Verbindungen**\!\[*Namen*\]</span><span class="sxs-lookup"><span data-stu-id="8db17-118">**Connections**\!\[*name*\]</span></span>


> [!NOTE]
> <P><span data-ttu-id="8db17-p106">[!HINWEIS] Sie können dieselbe Datenquelle mehrmals öffnen, wodurch Duplikatnamen in der <STRONG>Connections</STRONG>-Auflistung erstellt werden. Sie sollten Objektvariablen <STRONG>Connection</STRONG>-Objekte zuweisen und mit Variablennamen auf sie verweisen.</span><span class="sxs-lookup"><span data-stu-id="8db17-p106">You can open the same data source more than once, creating duplicate names in the <STRONG>Connections</STRONG> collection. You should assign <STRONG>Connection</STRONG> objects to object variables and refer to them by variable name.</span></span></P>



## <a name="example"></a><span data-ttu-id="8db17-121">Beispiel</span><span class="sxs-lookup"><span data-stu-id="8db17-121">Example</span></span>

<span data-ttu-id="8db17-122">In diesem Beispiel werden das **Connection**-Objekt und die **Connections**-Auflistung veranschaulicht, indem ein **Database**-Objekt und zwei **Connection**-ODBCDirect-Objekte geöffnet und die für die Objekte verfügbaren Eigenschaften aufgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="8db17-122">This example demonstrates the **Connection** object and **Connections** collection by opening a **Database** object and two ODBCDirect **Connection** objects and listing the properties available to each object.</span></span>

```vb 
Sub ConnectionObjectX() 
 
   Dim wrkAcc as Workspace 
   Dim dbsNorthwind As Database 
   Dim wrkODBC As Workspace 
   Dim conPubs As Connection 
   Dim conPubs2 As Connection 
   Dim conLoop As Connection 
   Dim prpLoop As Property 
 
   ' Open a Database object. 
   Set wrkAcc = CreateWorkspace("NewWorkspace", _ 
      "admin", "", dbUseJet) 
   Set dbsNorthwind = wrkAcc.OpenDatabase("Northwind.mdb") 
 
   ' Create ODBCDirect Workspace object and open Connection 
   ' objects. 
   Set wrkODBC = CreateWorkspace("NewODBCWorkspace", _ 
      "admin", "", dbUseODBC) 
       
   ' Note: The DSNs referenced below must be configured to  
   '       use Microsoft Windows NT Authentication Mode to  
   '       authorize user access to the Microsoft SQL Server. 
   Set conPubs = wrkODBC.OpenConnection("Connection1", , , _ 
      "ODBC;DATABASE=pubs;DSN=Publishers") 
       
   Set conPubs2 = wrkODBC.OpenConnection("Connection2", , _ 
      True, "ODBC;DATABASE=pubs;DSN=Publishers") 
 
   Debug.Print "Database properties:" 
 
   With dbsNorthwind 
      ' Enumerate Properties collection of Database object. 
      For Each prpLoop In .Properties 
         On Error Resume Next 
         Debug.Print "  " & prpLoop.Name & " = " & _ 
            prpLoop.Value 
         On Error GoTo 0 
      Next prpLoop 
   End With 
 
   ' Enumerate the Connections collection. 
   For Each conLoop In wrkODBC.Connections 
      Debug.Print "Connection properties for " & _ 
         conLoop.Name & ":" 
 
      With conLoop 
         ' Print property values by explicitly calling each 
         ' Property object; the Connection object does not 
         ' support a Properties collection. 
         Debug.Print "  Connect = " & .Connect 
         ' Property actually returns a Database object. 
         Debug.Print "  Database[.Name] = " & _ 
            .Database.Name 
         Debug.Print "  Name = " & .Name 
         Debug.Print "  QueryTimeout = " & .QueryTimeout 
         Debug.Print "  RecordsAffected = " & _ 
            .RecordsAffected 
         Debug.Print "  StillExecuting = " & _ 
            .StillExecuting 
         Debug.Print "  Transactions = " & .Transactions 
         Debug.Print "  Updatable = " & .Updatable 
      End With 
 
   Next conLoop 
 
   dbsNorthwind.Close 
   conPubs.Close 
   conPubs2.Close 
   wrkAcc.Close 
   wrkODBC.Close 
 
End Sub 
 
```

<span data-ttu-id="8db17-123">In diesem Beispiel wird die **OpenConnection**-Methode mit verschiedenen Parametern verwendet, um drei verschiedene **Connection**-Objekte zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="8db17-123">This example uses the **OpenConnection** method with different parameters to open three different **Connection** objects.</span></span>

```vb 
Sub OpenConnectionX() 
 
   Dim wrkODBC As Workspace 
   Dim conPubs As Connection 
   Dim conPubs2 As Connection 
   Dim conPubs3 As Connection 
   Dim conLoop As Connection 
 
   ' Create ODBCDirect Workspace object. 
   Set wrkODBC = CreateWorkspace("NewODBCWorkspace", _ 
      "admin", "", dbUseODBC) 
 
   ' Open Connection object using supplied information in  
   ' the connect string. If this information were  
   ' insufficient, you could trap for an error rather than  
   ' go to an ODBC Driver Manager dialog box. 
   MsgBox "Opening Connection1..." 
       
    ' Note: The DSN referenced below must be set to  
    '       use Microsoft Windows NT Authentication Mode to  
    '       authorize user access to the Microsoft SQL Server. 
    Set conPubs = wrkODBC.OpenConnection("Connection1", _ 
       dbDriverNoPrompt, , _ 
       "ODBC;DATABASE=pubs;DSN=Publishers") 
 
   ' Open read-only Connection object based on information  
   ' you enter in the ODBC Driver Manager dialog box. 
   MsgBox "Opening Connection2..." 
   Set conPubs2 = wrkODBC.OpenConnection("Connection2", _ 
      dbDriverPrompt, True, "ODBC;DSN=Publishers;") 
 
   ' Open read-only Connection object by entering only the  
   ' missing information in the ODBC Driver Manager dialog  
   ' box. 
   MsgBox "Opening Connection3..." 
   Set conPubs3 = wrkODBC.OpenConnection("Connection3", _ 
      dbDriverCompleteRequired, True, _ 
      "ODBC;DATABASE=pubs;DSN=Publishers;") 
 
   ' Enumerate the Connections collection. 
   For Each conLoop In wrkODBC.Connections 
      Debug.Print "Connection properties for " & _ 
         conLoop.Name & ":" 
 
      With conLoop 
         ' Print property values by explicitly calling each 
         ' Property object; the Connection object does not 
         ' support a Properties collection. 
         Debug.Print "  Connect = " & .Connect 
         ' Property actually returns a Database object. 
         Debug.Print "  Database[.Name] = " & _ 
            .Database.Name 
         Debug.Print "  Name = " & .Name 
         Debug.Print "  QueryTimeout = " & .QueryTimeout 
         Debug.Print "  RecordsAffected = " & _ 
            .RecordsAffected 
         Debug.Print "  StillExecuting = " & _ 
            .StillExecuting 
         Debug.Print "  Transactions = " & .Transactions 
         Debug.Print "  Updatable = " & .Updatable 
      End With 
 
   Next conLoop 
 
   conPubs.Close 
   conPubs2.Close 
   conPubs3.Close 
   wrkODBC.Close 
 
End Sub 
 
```

