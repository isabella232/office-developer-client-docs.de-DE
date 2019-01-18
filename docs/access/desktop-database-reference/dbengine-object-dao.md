---
title: DBEngine-Objekt (DAO)
TOCTitle: DBEngine Object
ms:assetid: ceaeb505-615e-37ba-4633-27240ef8c5de
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834506(v=office.15)
ms:contentKeyID: 48547792
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 479eff80d25279a1c5e918a3b639443ad3b25c6c
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28703685"
---
# <a name="dbengine-object-dao"></a>DBEngine-Objekt (DAO)

**Betrifft**: Access 2013, Office 2013

Das **DBEngine**-Objekt ist im DAO-Objektmodell das Objekt der obersten Ebene.

## <a name="remarks"></a>Bemerkungen

Das **DBEngine**-Objekt enthält und steuert alle anderen Objekte in der DAO-Objekthierarchie. Sie können keine weiteren **DBEngine**-Objekte erstellen, und das **DBEngine**-Objekt ist kein Element einer Auflistung.

Bei jedem Datenbank- oder Verbindungstyp können Sie die folgenden Aktionen ausführen:

  - Rufen Sie mit der **Version**-Eigenschaft die DAO-Versionsnummer ab.

  - Verwenden Sie die **LoginTimeout**-Eigenschaft, um das ODBC-Anmeldungstimeout abzurufen oder festzulegen, und die **RegisterDatabase**-Methode, um ODBC-Informationen für das Microsoft Access-Datenbankmodul bereitzustellen.

  - Legen Sie mit den Eigenschaften **DefaultPassword** und **DefaultUser** die Benutzeridentifikation und das Kennwort für das **Workspace**-Standardobjekt fest.

  - Erstellen Sie mit der **CreateWorkspace**-Methode ein neues **Workspace**-Objekt. Sie können mit optionalen Argumenten die Einstellungen der Eigenschaften **DefaultType**, **DefaultPassword** und **DefaultUser** überschreiben.

  - Öffnen Sie mit der **OpenDatabase**-Methode eine Datenbank im **Workspace**-Standardobjekt, und steuern Sie mit den Methoden **BeginTrans**, **Commit** und **Rollback** Transaktionen zum **Workspace**-Standardobjekt.

  - Verweisen Sie mit der **Workspaces**-Auflistung auf bestimmte **Workspace**-Objekte.

  - Überprüfen Sie mit der **Errors**-Auflistung die Details zu Datenzugriffsfehlern.

Weitere Eigenschaften und Methoden sind nur verfügbar, wenn Sie DAO mit dem Microsoft Access-Datenbankmodul verwenden. Mit diesen Eigenschaften und Methoden können Sie das Microsoft Access-Datenbankmodul steuern, Eigenschaften bearbeiten und Tasks zu temporären Objekten ausführen, die keine Elemente von Auflistungen sind. Sie können z. B. die folgenden Aktionen ausführen:

  - Erstellen Sie mit der **CreateDatabase**-Methode ein neues **Database**-Objekt des Microsoft Access-Datenbankmoduls.

  - Verwenden Sie die **Idle**-Methode, um dem Microsoft Access-Datenbankmodul das Abschließen ausstehender Tasks zu ermöglichen.

  - Verwenden Sie die Methoden **CompactDatabase** und **RepairDatabase** zum Verwalten von Datenbankdateien.

  - Geben Sie mit den Eigenschaften **IniPath** und **SystemDB** jeweils den Speicherort der Windows-Registrierungsinformationen des Microsoft Access-Datenbankmoduls und der Informationsdatei für Arbeitsgruppen von Microsoft Access an. Mit der **SetOption**-Methode können Sie Einstellungen der Windows-Registrierung für das Microsoft Access-Datenbankmodul überschreiben.

Wenn Sie die Einstellungen der Eigenschaften **DefaultType** und **IniPath** geändert haben, werden diese Änderungen nur in folgenden **Workspace**-Objekten wiedergegeben.

Verwenden Sie die folgende Syntax, um auf eine zum **DBEngine**-Objekt gehörende Auflistung oder auf eine Methode oder Eigenschaft zu verweisen, die auf dieses Objekt angewendet wird:

\[**DBEngine**. \] \[Auflistung | Methode | Eigenschaft\]

## <a name="example"></a>Beispiel

Dieses Beispiel führt die Auflistungen des **DBEngine**-Objekts auf.

```vb
    Sub DBEngineX() 
     
     Dim wrkLoop As Workspace 
     Dim prpLoop As Property 
     
     With DBEngine 
     Debug.Print "DBEngine Properties" 
     
     ' Enumerate Properties collection of DBEngine, 
     ' trapping for properties whose values are 
     ' invalid in this context. 
     For Each prpLoop In .Properties 
     On Error Resume Next 
     Debug.Print " " & prpLoop.Name & " = " _ 
     & prpLoop 
     On Error GoTo 0 
     Next prpLoop 
     
     Debug.Print "Workspaces collection of DBEngine" 
     
     ' Enumerate Workspaces collection of DBEngine. 
     For Each wrkLoop In .Workspaces 
     Debug.Print " " & wrkLoop.Name 
     
     ' Enumerate Properties collection of each 
     ' Workspace object, trapping for properties 
     ' whose values are invalid in this context. 
     For Each prpLoop In wrkLoop.Properties 
     On Error Resume Next 
     Debug.Print " " & prpLoop.Name & _ 
     " = " & prpLoop 
     On Error GoTo 0 
     Next prpLoop 
     
     Next wrkLoop 
     
     End With 
     
    End Sub
```
