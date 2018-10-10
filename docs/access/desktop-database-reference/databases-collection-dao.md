---
title: Databases Collection (DAO)
TOCTitle: Databases Collection
ms:assetid: 988ae6f5-ec15-cd1c-191d-f295624425f4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197944(v=office.15)
ms:contentKeyID: 48546493
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 23096391566f9d3f7649ef09839900e9ca009af6
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25475164"
---
# <a name="databases-collection-dao"></a>Databases Collection (DAO)

**Betrifft**: Access 2013 | Office 2013

Eine **Databases**-Auflistung enthält alle offenen **Database**-Objekte, die in einem **Workspace**-Objekt erstellt oder geöffnet wurden.

## <a name="remarks"></a>Bemerkungen

Wenn Sie ein vorhandenes **Database**-Objekt öffnen oder ein neues aus einem **Workspace**-Objekt erstellen, wird es automatisch der **Databases**-Auflistung hinzugefügt. Wenn Sie ein **Database**-Objekt mit der **[Close](connection-close-method-dao.md)** -Methode schließen, wird es aus der **Databases**-Auflistung entfernt, aber nicht von der Festplatte gelöscht. Sie müssen alle geöffneten **Recordset**-Objekte schließen, bevor Sie ein **Database**-Objekt schließen.

In einem Microsoft Access-Arbeitsbereich handelt es sich bei der Einstellung der **Name**-Eigenschaft für eine Datenbank um eine Zeichenfolge, die den Pfad der Datenbankdatei angibt.

Der Verweis auf ein **Database**-Objekt in einer Auflistung erfolgt über dessen Ordnungszahl oder den Wert der **Name**-Eigenschaft, wobei Sie die folgenden Syntaxformen verwenden können:

- **Databases**(0)

- **Datenbanken** ("*Name*")

- **Datenbanken**\!\[*Namen*\]

> [!NOTE]
> [!HINWEIS] Sie können dieselbe Datenquelle oder Datenbank mehrmals öffnen, wodurch Duplikatnamen in der **Databases**-Auflistung erstellt werden. Sie sollten Objektvariablen **Database**-Objekte zuweisen und mit Variablennamen auf sie verweisen.

## <a name="example"></a>Beispiel

In diesem Beispiel wird ein neues **Database** -Objekt erstellt und ein vorhandenes **Database** -Objekt im standardmäßigen **Workspace** -Objekt geöffnet. Dann wird die **Database** -Auflistung und die **Properties** -Auflistung der einzelnen **Database** -Objekte aufgezählt.

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

In diesem Beispiel wird **CreateDatabase** zum Erstellen eines neuen verschlüsselten **Database** -Objekts verwendet.

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
