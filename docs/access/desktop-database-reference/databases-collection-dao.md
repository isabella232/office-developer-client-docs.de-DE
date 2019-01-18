---
title: Databases-Auflistung (DAO)
TOCTitle: Databases Collection
ms:assetid: 988ae6f5-ec15-cd1c-191d-f295624425f4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197944(v=office.15)
ms:contentKeyID: 48546493
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: dbaa0fe7aaa50c8aec582e2f03cd2849268816b9
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28715550"
---
# <a name="databases-collection-dao"></a><span data-ttu-id="79152-102">Databases-Auflistung (DAO)</span><span class="sxs-lookup"><span data-stu-id="79152-102">Databases collection (DAO)</span></span>

<span data-ttu-id="79152-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="79152-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="79152-104">Eine **Databases**-Auflistung enthält alle offenen **Database**-Objekte, die in einem **Workspace**-Objekt erstellt oder geöffnet wurden.</span><span class="sxs-lookup"><span data-stu-id="79152-104">A **Databases** collection contains all open **Database** objects opened or created in a **Workspace** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="79152-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="79152-105">Remarks</span></span>

<span data-ttu-id="79152-p101">Wenn Sie ein vorhandenes **Database**-Objekt öffnen oder ein neues aus einem **Workspace**-Objekt erstellen, wird es automatisch der **Databases**-Auflistung hinzugefügt. Wenn Sie ein **Database**-Objekt mit der **[Close](connection-close-method-dao.md)** -Methode schließen, wird es aus der **Databases**-Auflistung entfernt, aber nicht von der Festplatte gelöscht. Sie müssen alle geöffneten **Recordset**-Objekte schließen, bevor Sie ein **Database**-Objekt schließen.</span><span class="sxs-lookup"><span data-stu-id="79152-p101">When you open an existing **Database** object or create a new one from a **Workspace**, it is automatically appended to the **Databases** collection. When you close a **Database** object with the **[Close](connection-close-method-dao.md)** method, it is removed from the **Databases** collection but not deleted from disk. You should close all open **Recordset** objects before closing a **Database** object.</span></span>

<span data-ttu-id="79152-109">In einem Microsoft Access-Arbeitsbereich handelt es sich bei der Einstellung der **Name**-Eigenschaft für eine Datenbank um eine Zeichenfolge, die den Pfad der Datenbankdatei angibt.</span><span class="sxs-lookup"><span data-stu-id="79152-109">In a Microsoft Access workspace, the **Name** property setting of a database is a string that specifies the path of the database file.</span></span>

<span data-ttu-id="79152-110">Der Verweis auf ein **Database**-Objekt in einer Auflistung erfolgt über dessen Ordnungszahl oder den Wert der **Name**-Eigenschaft, wobei Sie die folgenden Syntaxformen verwenden können:</span><span class="sxs-lookup"><span data-stu-id="79152-110">To refer to a **Database** object in a collection by its ordinal number or by its **Name** property setting, use any of the following syntax forms:</span></span>

- <span data-ttu-id="79152-111">**Databases**(0)</span><span class="sxs-lookup"><span data-stu-id="79152-111">**Databases**(0)</span></span>

- <span data-ttu-id="79152-112">**Datenbanken** ("*Name*")</span><span class="sxs-lookup"><span data-stu-id="79152-112">**Databases**("*name*")</span></span>

- <span data-ttu-id="79152-113">**Datenbanken**\!\[*Namen*\]</span><span class="sxs-lookup"><span data-stu-id="79152-113">**Databases**\!\[*name*\]</span></span>

> [!NOTE]
> <span data-ttu-id="79152-p102">[!HINWEIS] Sie können dieselbe Datenquelle oder Datenbank mehrmals öffnen, wodurch Duplikatnamen in der **Databases**-Auflistung erstellt werden. Sie sollten Objektvariablen **Database**-Objekte zuweisen und mit Variablennamen auf sie verweisen.</span><span class="sxs-lookup"><span data-stu-id="79152-p102">You can open the same data source or database more than once, creating duplicate names in the **Databases** collection. You should assign **Database** objects to object variables and refer to them by variable name.</span></span>

## <a name="example"></a><span data-ttu-id="79152-116">Beispiel</span><span class="sxs-lookup"><span data-stu-id="79152-116">Example</span></span>

<span data-ttu-id="79152-p103">In diesem Beispiel wird ein neues **Database** -Objekt erstellt und ein vorhandenes **Database** -Objekt im standardmäßigen **Workspace** -Objekt geöffnet. Dann wird die **Database** -Auflistung und die **Properties** -Auflistung der einzelnen **Database** -Objekte aufgezählt.</span><span class="sxs-lookup"><span data-stu-id="79152-p103">This example creates a new **Database** object and opens an existing **Database** object in the default **Workspace** object. Then it enumerates the **Database** collection and the **Properties** collection of each **Database** object.</span></span>

```vb 
Sub DatabaseObjectX() 
 
 Dim wrkAcc As Workspace 
 Dim dbsNorthwind As Database 
 Dim dbsNew As Database 
 Dim dbsLoop As Database 
 Dim prpLoop As Property 
 
 Set wrkAcc = CreateWorkspace("AccWorkspace", "admin", _ 
 "", dbUseJet) 
 
 ' Make sure there isn't already a file with the name of 
 ' the new database. 
 If Dir("NewDB.mdb") <> "" Then Kill "NewDB.mdb" 
 
 ' Create a new database with the specified 
 ' collating order. 
 Set dbsNew = wrkAcc.CreateDatabase("NewDB.mdb", _ 
 dbLangGeneral) 
 Set dbsNorthwind = wrkAcc.OpenDatabase("Northwind.mdb") 
 
 ' Enumerate the Databases collection. 
 For Each dbsLoop In wrkAcc.Databases 
 With dbsLoop 
 Debug.Print "Properties of " & .Name 
 ' Enumerate the Properties collection of each 
 ' Database object. 
 For Each prpLoop In .Properties 
 If prpLoop <> "" Then Debug.Print " " & _ 
 prpLoop.Name & " = " & prpLoop 
 Next prpLoop 
 End With 
 Next dbsLoop 
 
 dbsNew.Close 
 dbsNorthwind.Close 
 wrkAcc.Close 
 
End Sub 
 
```

<br/>

<span data-ttu-id="79152-119">In diesem Beispiel wird **CreateDatabase** zum Erstellen eines neuen verschlüsselten **Database** -Objekts verwendet.</span><span class="sxs-lookup"><span data-stu-id="79152-119">This example uses **CreateDatabase** to create a new, encrypted **Database** object.</span></span>

```vb
    Sub CreateDatabaseX() 
     
     Dim wrkDefault As Workspace 
     Dim dbsNew As DATABASE 
     Dim prpLoop As Property 
     
     ' Get default Workspace. 
     Set wrkDefault = DBEngine.Workspaces(0) 
     
     ' Make sure there isn't already a file with the name of 
     ' the new database. 
     If Dir("NewDB.mdb") <> "" Then Kill "NewDB.mdb" 
     
     ' Create a new encrypted database with the specified 
     ' collating order. 
     Set dbsNew = wrkDefault.CreateDatabase("NewDB.mdb", _ 
     dbLangGeneral, dbEncrypt) 
     
     With dbsNew 
     Debug.Print "Properties of " & .Name 
     ' Enumerate the Properties collection of the new 
     ' Database object. 
     For Each prpLoop In .Properties 
     If prpLoop <> "" Then Debug.Print " " & _ 
     prpLoop.Name & " = " & prpLoop 
     Next prpLoop 
     End With 
     
     dbsNew.Close 
     
    End Sub
```
