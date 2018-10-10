---
title: Workspaces Collection (DAO)
TOCTitle: Workspaces Collection
ms:assetid: 88b851ce-4180-964f-582e-bc9571bf554c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197057(v=office.15)
ms:contentKeyID: 48546142
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 37fd4ce04dbd35fccb2356b8088450d07af203d4
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25473858"
---
# <a name="workspaces-collection-dao"></a>Workspaces Collection (DAO)


**Betrifft**: Access 2013 | Office 2013

Eine **Workspaces**-Auflistung enthält alle aktiven, nicht ausgeblendeten **Workspace**-Objekte des **DBEngine**-Objekts. (Ausgeblendete **Workspace**-Objekte werden nicht an die Auflistung angefügt, und auf sie wird nicht durch die Variable verwiesen, der sie zugeordnet sind.)

## <a name="remarks"></a>Bemerkungen

Verwenden Sie das **Workspace**-Objekt, um die aktuelle Sitzung zu verwalten oder eine zusätzliche Sitzung zu starten.

Wenn Sie zuerst finden Sie unter oder ein **Workspace** -Objekt verwenden, erstellen Sie automatisch den Standard-Arbeitsbereich DBEngine.Workspaces(0). Die Einstellungen der Eigenschaften **Name** und **UserName** des Standard-Arbeitsbereich sind "\#Standard-Arbeitsbereich\#" und "Admin" fest. Wenn die Sicherheit aktiviert ist, lautet ist die **UserName** -Eigenschaftseinstellung der Name des angemeldeten Benutzers.

Sie können mit der [**CreateWorkspace**](dbengine-createworkspace-method-dao.md) -Methode neue **Workspace**-Objekte erstellen. Wenn Sie ein neues **Workspace**-Objekt erstellt haben, müssen Sie es an die **Workspaces**-Auflistung anfügen, um von der **Workspaces**-Auflistung auf dieses Objekt verweisen zu können. Sie können ein neu erstelltes **Workspace**-Objekt jedoch auch verwenden, ohne es an die **Workspaces**-Auflistung anzufügen.

Der Verweis auf ein **Workspace**-Objekt in einer Auflistung erfolgt über dessen Ordnungszahl oder den Wert der **Name**-Eigenschaft, wobei Sie die folgenden Syntaxformen verwenden können:

**DBEngine**. **Arbeitsbereiche** (0)

**DBEngine**. **Arbeitsbereiche** ("Name")

**DBEngine**. **Arbeitsbereiche** \! \[Namen\]


> [!NOTE]
> [!HINWEIS] ODBCDirect-Arbeitsbereiche werden in Microsoft Access 2013 nicht unterstützt. Verwenden Sie ADO, wenn Sie auf externe Datenquellen zugreifen möchten, ohne das Microsoft Access-Datenbankmodul zu verwenden.



## <a name="example"></a>Beispiel

In diesem Beispiel wird ein neues Microsoft Access-Arbeitsbereichsobjekt erstellt und an die **Arbeitsbereichs** auflistung angehängt. Anschließend werden die **Arbeitsbereichs** auflistungen und die **Eigenschafts** auflistung des **Arbeitsbereichs** objekts aufgezählt.

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

In diesem Beispiel wird die **CreateWorkspace**-Methode verwendet, um einen Microsoft Access-Arbeitsbereich zu erstellen. Danach werden die Eigenschaften des Arbeitsbereichs aufgelistet.

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

