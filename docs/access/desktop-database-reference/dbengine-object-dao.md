---
title: DBEngine-Objekt (DAO)
TOCTitle: DBEngine Object
ms:assetid: ceaeb505-615e-37ba-4633-27240ef8c5de
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834506(v=office.15)
ms:contentKeyID: 48547792
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0d0ebafc885e02d0098c67bb55e56a1744557973
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25923602"
---
# <a name="dbengine-object-dao"></a><span data-ttu-id="4f728-102">DBEngine-Objekt (DAO)</span><span class="sxs-lookup"><span data-stu-id="4f728-102">DBEngine object (DAO)</span></span>

<span data-ttu-id="4f728-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4f728-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4f728-104">Das **DBEngine**-Objekt ist im DAO-Objektmodell das Objekt der obersten Ebene.</span><span class="sxs-lookup"><span data-stu-id="4f728-104">The **DBEngine** object is the top level object in the DAO object model.</span></span>

## <a name="remarks"></a><span data-ttu-id="4f728-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4f728-105">Remarks</span></span>

<span data-ttu-id="4f728-p101">Das **DBEngine**-Objekt enthält und steuert alle anderen Objekte in der DAO-Objekthierarchie. Sie können keine weiteren **DBEngine**-Objekte erstellen, und das **DBEngine**-Objekt ist kein Element einer Auflistung.</span><span class="sxs-lookup"><span data-stu-id="4f728-p101">The **DBEngine** object contains and controls all other objects in the hierarchy of DAO objects. You can't create additional **DBEngine** objects, and the **DBEngine** object isn't an element of any collection.</span></span>

<span data-ttu-id="4f728-108">Bei jedem Datenbank- oder Verbindungstyp können Sie die folgenden Aktionen ausführen:</span><span class="sxs-lookup"><span data-stu-id="4f728-108">With any type of database or connection, you can:</span></span>

  - <span data-ttu-id="4f728-109">Rufen Sie mit der **Version**-Eigenschaft die DAO-Versionsnummer ab.</span><span class="sxs-lookup"><span data-stu-id="4f728-109">Use the **Version** property to obtain the DAO version number.</span></span>

  - <span data-ttu-id="4f728-110">Verwenden Sie die **LoginTimeout**-Eigenschaft, um das ODBC-Anmeldungstimeout abzurufen oder festzulegen, und die **RegisterDatabase**-Methode, um ODBC-Informationen für das Microsoft Access-Datenbankmodul bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="4f728-110">Use the **LoginTimeout** property to obtain or set the ODBC login timeout, and the **RegisterDatabase** method to provide ODBC information to the Microsoft Access database engine.</span></span>

  - <span data-ttu-id="4f728-111">Legen Sie mit den Eigenschaften **DefaultPassword** und **DefaultUser** die Benutzeridentifikation und das Kennwort für das **Workspace**-Standardobjekt fest.</span><span class="sxs-lookup"><span data-stu-id="4f728-111">Use the **DefaultPassword** and **DefaultUser** properties to set the user identification and password for the default **Workspace** object.</span></span>

  - <span data-ttu-id="4f728-p102">Erstellen Sie mit der **CreateWorkspace**-Methode ein neues **Workspace**-Objekt. Sie können mit optionalen Argumenten die Einstellungen der Eigenschaften **DefaultType**, **DefaultPassword** und **DefaultUser** überschreiben.</span><span class="sxs-lookup"><span data-stu-id="4f728-p102">Use the **CreateWorkspace** method to create a new **Workspace** object. You can use optional arguments to override the settings of the **DefaultType**, **DefaultPassword**, and **DefaultUser** properties.</span></span>

  - <span data-ttu-id="4f728-114">Öffnen Sie mit der **OpenDatabase**-Methode eine Datenbank im **Workspace**-Standardobjekt, und steuern Sie mit den Methoden **BeginTrans**, **Commit** und **Rollback** Transaktionen zum **Workspace**-Standardobjekt.</span><span class="sxs-lookup"><span data-stu-id="4f728-114">Use the **OpenDatabase** method to open a database in the default **Workspace**, and use the **BeginTrans**, **Commit**, and **Rollback** methods to control transactions on the default **Workspace**.</span></span>

  - <span data-ttu-id="4f728-115">Verweisen Sie mit der **Workspaces**-Auflistung auf bestimmte **Workspace**-Objekte.</span><span class="sxs-lookup"><span data-stu-id="4f728-115">Use the **Workspaces** collection to reference specific **Workspace** objects.</span></span>

  - <span data-ttu-id="4f728-116">Überprüfen Sie mit der **Errors**-Auflistung die Details zu Datenzugriffsfehlern.</span><span class="sxs-lookup"><span data-stu-id="4f728-116">Use the **Errors** collection to examine data access error details.</span></span>

<span data-ttu-id="4f728-p103">Weitere Eigenschaften und Methoden sind nur verfügbar, wenn Sie DAO mit dem Microsoft Access-Datenbankmodul verwenden. Mit diesen Eigenschaften und Methoden können Sie das Microsoft Access-Datenbankmodul steuern, Eigenschaften bearbeiten und Tasks zu temporären Objekten ausführen, die keine Elemente von Auflistungen sind. Sie können z. B. die folgenden Aktionen ausführen:</span><span class="sxs-lookup"><span data-stu-id="4f728-p103">Other properties and methods are only available when you use DAO with the Microsoft Access database engine. You can use them to control the Microsoft Access database engine, manipulate its properties, and perform tasks on temporary objects that aren't elements of collections. For example, you can:</span></span>

  - <span data-ttu-id="4f728-120">Erstellen Sie mit der **CreateDatabase**-Methode ein neues **Database**-Objekt des Microsoft Access-Datenbankmoduls.</span><span class="sxs-lookup"><span data-stu-id="4f728-120">Use the **CreateDatabase** method to create a new Microsoft Access database engine **Database** object.</span></span>

  - <span data-ttu-id="4f728-121">Verwenden Sie die **Idle**-Methode, um dem Microsoft Access-Datenbankmodul das Abschließen ausstehender Tasks zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="4f728-121">Use the **Idle** method to enable the Microsoft Access database engine to complete any pending tasks.</span></span>

  - <span data-ttu-id="4f728-122">Verwenden Sie die Methoden **CompactDatabase** und **RepairDatabase** zum Verwalten von Datenbankdateien.</span><span class="sxs-lookup"><span data-stu-id="4f728-122">Use the **CompactDatabase** and **RepairDatabase** methods to maintain database files.</span></span>

  - <span data-ttu-id="4f728-p104">Geben Sie mit den Eigenschaften **IniPath** und **SystemDB** jeweils den Speicherort der Windows-Registrierungsinformationen des Microsoft Access-Datenbankmoduls und der Informationsdatei für Arbeitsgruppen von Microsoft Access an. Mit der **SetOption**-Methode können Sie Einstellungen der Windows-Registrierung für das Microsoft Access-Datenbankmodul überschreiben.</span><span class="sxs-lookup"><span data-stu-id="4f728-p104">Use the **IniPath** and **SystemDB** properties to specify the location of Microsoft Access database engine Windows Registry information and the Microsoft Access workgroup information file, respectively. The **SetOption** method allows you override windows registry settings for the Microsoft Access database engine.</span></span>

<span data-ttu-id="4f728-125">Wenn Sie die Einstellungen der Eigenschaften **DefaultType** und **IniPath** geändert haben, werden diese Änderungen nur in folgenden **Workspace**-Objekten wiedergegeben.</span><span class="sxs-lookup"><span data-stu-id="4f728-125">After you change the **DefaultType** and **IniPath** property settings, only subsequent **Workspace** objects will reflect these changes.</span></span>

<span data-ttu-id="4f728-126">Verwenden Sie die folgende Syntax, um auf eine zum **DBEngine**-Objekt gehörende Auflistung oder auf eine Methode oder Eigenschaft zu verweisen, die auf dieses Objekt angewendet wird:</span><span class="sxs-lookup"><span data-stu-id="4f728-126">To refer to a collection that belongs to the **DBEngine** object, or to refer to a method or property that applies to this object, use this syntax:</span></span>

<span data-ttu-id="4f728-127">\[**DBEngine**. \] \[Auflistung | Methode | Eigenschaft\]</span><span class="sxs-lookup"><span data-stu-id="4f728-127">\[**DBEngine**.\]\[collection | method | property\]</span></span>

## <a name="example"></a><span data-ttu-id="4f728-128">Beispiel</span><span class="sxs-lookup"><span data-stu-id="4f728-128">Example</span></span>

<span data-ttu-id="4f728-129">Dieses Beispiel führt die Auflistungen des **DBEngine**-Objekts auf.</span><span class="sxs-lookup"><span data-stu-id="4f728-129">This example enumerates the collections of the **DBEngine** object.</span></span>

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
