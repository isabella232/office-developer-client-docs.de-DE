---
title: Workspaces Collection (DAO)
TOCTitle: Workspaces Collection
ms:assetid: 88b851ce-4180-964f-582e-bc9571bf554c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197057(v=office.15)
ms:contentKeyID: 48546142
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4108be7d6c1b2ee66ec5cddf4d26599796bf844c
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870268"
---
# <a name="workspaces-collection-dao"></a><span data-ttu-id="e343f-102">Workspaces Collection (DAO)</span><span class="sxs-lookup"><span data-stu-id="e343f-102">Workspaces Collection (DAO)</span></span>


<span data-ttu-id="e343f-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e343f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e343f-p101">Eine **Workspaces**-Auflistung enthält alle aktiven, nicht ausgeblendeten **Workspace**-Objekte des **DBEngine**-Objekts. (Ausgeblendete **Workspace**-Objekte werden nicht an die Auflistung angefügt, und auf sie wird nicht durch die Variable verwiesen, der sie zugeordnet sind.)</span><span class="sxs-lookup"><span data-stu-id="e343f-p101">A **Workspaces** collection contains all active, unhidden **Workspace** objects of the **DBEngine** object. (Hidden **Workspace** objects are not appended to the collection and referenced by the variable to which they are assigned.)</span></span>

## <a name="remarks"></a><span data-ttu-id="e343f-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e343f-106">Remarks</span></span>

<span data-ttu-id="e343f-107">Verwenden Sie das **Workspace**-Objekt, um die aktuelle Sitzung zu verwalten oder eine zusätzliche Sitzung zu starten.</span><span class="sxs-lookup"><span data-stu-id="e343f-107">Use the **Workspace** object to manage the current session or to start an additional session.</span></span>

<span data-ttu-id="e343f-108">Wenn Sie zuerst finden Sie unter oder ein **Workspace** -Objekt verwenden, erstellen Sie automatisch den Standard-Arbeitsbereich DBEngine.Workspaces(0).</span><span class="sxs-lookup"><span data-stu-id="e343f-108">When you first refer to or use a **Workspace** object, you automatically create the default workspace, DBEngine.Workspaces(0).</span></span> <span data-ttu-id="e343f-109">Die Einstellungen der Eigenschaften **Name** und **UserName** des Standard-Arbeitsbereich sind "\#Standard-Arbeitsbereich\#" und "Admin" fest.</span><span class="sxs-lookup"><span data-stu-id="e343f-109">The settings of the **Name** and **UserName** properties of the default workspace are "\#Default Workspace\#" and "Admin," respectively.</span></span> <span data-ttu-id="e343f-110">Wenn die Sicherheit aktiviert ist, lautet ist die **UserName** -Eigenschaftseinstellung der Name des angemeldeten Benutzers.</span><span class="sxs-lookup"><span data-stu-id="e343f-110">If security is enabled, the **UserName** property setting is the name of the user who logged on.</span></span>

<span data-ttu-id="e343f-p103">Sie können mit der [**CreateWorkspace**](dbengine-createworkspace-method-dao.md) -Methode neue **Workspace**-Objekte erstellen. Wenn Sie ein neues **Workspace**-Objekt erstellt haben, müssen Sie es an die **Workspaces**-Auflistung anfügen, um von der **Workspaces**-Auflistung auf dieses Objekt verweisen zu können. Sie können ein neu erstelltes **Workspace**-Objekt jedoch auch verwenden, ohne es an die **Workspaces**-Auflistung anzufügen.</span><span class="sxs-lookup"><span data-stu-id="e343f-p103">You can create new **Workspace** objects with the **[CreateWorkspace](dbengine-createworkspace-method-dao.md)** method. After you create a new **Workspace** object, you must append it to the **Workspaces** collection if you need to refer to it from the **Workspaces** collection. You can, however, use a newly created **Workspace** object without appending it to the **Workspaces** collection.</span></span>

<span data-ttu-id="e343f-114">Der Verweis auf ein **Workspace**-Objekt in einer Auflistung erfolgt über dessen Ordnungszahl oder den Wert der **Name**-Eigenschaft, wobei Sie die folgenden Syntaxformen verwenden können:</span><span class="sxs-lookup"><span data-stu-id="e343f-114">To refer to a **Workspace** object in a collection by its ordinal number or by its **Name** property setting, use any of the following syntax forms:</span></span>

<span data-ttu-id="e343f-115">**DBEngine**. **Arbeitsbereiche** (0)</span><span class="sxs-lookup"><span data-stu-id="e343f-115">**DBEngine**.**Workspaces**(0)</span></span>

<span data-ttu-id="e343f-116">**DBEngine**. **Arbeitsbereiche** ("Name")</span><span class="sxs-lookup"><span data-stu-id="e343f-116">**DBEngine**.**Workspaces**("name")</span></span>

<span data-ttu-id="e343f-117">**DBEngine**. **Arbeitsbereiche** \! \[Namen\]</span><span class="sxs-lookup"><span data-stu-id="e343f-117">**DBEngine**.**Workspaces**\!\[name\]</span></span>


> [!NOTE]
> <span data-ttu-id="e343f-p104">[!HINWEIS] ODBCDirect-Arbeitsbereiche werden in Microsoft Access 2013 nicht unterstützt. Verwenden Sie ADO, wenn Sie auf externe Datenquellen zugreifen möchten, ohne das Microsoft Access-Datenbankmodul zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="e343f-p104">ODBCDirect workspaces are not supported in Microsoft Access 2013. Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span>



## <a name="example"></a><span data-ttu-id="e343f-120">Beispiel</span><span class="sxs-lookup"><span data-stu-id="e343f-120">Example</span></span>

<span data-ttu-id="e343f-p105">In diesem Beispiel wird ein neues Microsoft Access-Arbeitsbereichsobjekt erstellt und an die **Arbeitsbereichs** auflistung angehängt. Anschließend werden die **Arbeitsbereichs** auflistungen und die **Eigenschafts** auflistung des **Arbeitsbereichs** objekts aufgezählt.</span><span class="sxs-lookup"><span data-stu-id="e343f-p105">This example creates a new Microsoft Access Workspace object and appends it to the **Workspaces** collection. It then enumerates the **Workspaces** collections and the **Properties** collection of the **Workspace** object.</span></span>

```vb 
Sub WorkspaceX() 
 
 Dim wrkNewAcc As Workspace 
 Dim wrkLoop As Workspace 
 Dim prpLoop As Property 
 
 ' Create a new Microsoft Access workspace. 
 Set wrkNewAcc = CreateWorkspace("NewAccessWorkspace", _ 
 "admin", "", dbUseJet) 
 Workspaces.Append wrkNewAcc 
 
 ' Enumerate the Workspaces collection. 
 For Each wrkLoop In Workspaces 
 With wrkLoop 
 Debug.Print "Properties of " & .Name 
 ' Enumerate the Properties collection of the new 
 ' Workspace object. 
 For Each prpLoop In .Properties 
 On Error Resume Next 
 If prpLoop <> "" Then Debug.Print " " & _ 
 prpLoop.Name & " = " & prpLoop 
 On Error GoTo 0 
 Next prpLoop 
 End With 
 Next wrkLoop 
 
 wrkNewAcc.Close 
End Sub 
```

<br/>

<span data-ttu-id="e343f-p106">In diesem Beispiel wird die **CreateWorkspace**-Methode verwendet, um einen Microsoft Access-Arbeitsbereich zu erstellen. Danach werden die Eigenschaften des Arbeitsbereichs aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="e343f-p106">This example uses the **CreateWorkspace** method to create a Microsoft Access workspace. It then lists the properties of theworkspace.</span></span>

```vb 
Sub CreateWorkspaceX() 
 
 Dim wrkAcc As Workspace 
 Dim wrkLoop As Workspace 
 Dim prpLoop As Property 
 
 
 DefaultType = dbUseJet 
 ' Create an unnamed Workspace object of the type 
 ' specified by the DefaultType property of DBEngine 
 ' (dbUseJet). 
 Set wrkAcc = CreateWorkspace("", "admin", "") 
 
 ' Enumerate Workspaces collection. 
 Debug.Print "Workspace objects in Workspaces collection:" 
 For Each wrkLoop In Workspaces 
 Debug.Print " " & wrkLoop.Name 
 Next wrkLoop 
 
 With wrkAcc 
 ' Enumerate Properties collection of Microsoft Access 
 ' workspace. 
 Debug.Print _ 
 "Properties of unnamed Microsoft Access workspace" 
 On Error Resume Next 
 For Each prpLoop In .Properties 
 Debug.Print " " & prpLoop.Name & " = " & prpLoop 
 Next prpLoop 
 On Error GoTo 0 
 End With 
 
 wrkAcc.Close 
 
End Sub 
 
```

