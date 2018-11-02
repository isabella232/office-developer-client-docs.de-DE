---
title: Workspace.OpenDatabase-Methode (DAO)
TOCTitle: OpenDatabase Method
ms:assetid: dbb93908-ec3e-f3ee-c4ea-cca48340b4d3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835343(v=office.15)
ms:contentKeyID: 48548108
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1ef8c2399ec8a2ddedde47197388698c2b83c57c
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25926668"
---
# <a name="workspaceopendatabase-method-dao"></a><span data-ttu-id="8b0a3-102">Workspace.OpenDatabase-Methode (DAO)</span><span class="sxs-lookup"><span data-stu-id="8b0a3-102">Workspace.OpenDatabase method (DAO)</span></span>

<span data-ttu-id="8b0a3-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8b0a3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8b0a3-104">Öffnet eine bestimmte Datenbank in einem **[Workspace](workspace-object-dao.md)** -Objekt und gibt einen Verweis auf das **[Database](database-object-dao.md)** -Objekt zurück, das es darstellt.</span><span class="sxs-lookup"><span data-stu-id="8b0a3-104">Opens a specified database in a **[Workspace](workspace-object-dao.md)** object and returns a reference to the **[Database](database-object-dao.md)** object that represents it.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b0a3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8b0a3-105">Syntax</span></span>

<span data-ttu-id="8b0a3-106">*Ausdruck* . OpenDatabase (***Name***, ***Optionen***, ***ReadOnly***, ***Verbinden***)</span><span class="sxs-lookup"><span data-stu-id="8b0a3-106">*expression* .OpenDatabase(***Name***, ***Options***, ***ReadOnly***, ***Connect***)</span></span>

<span data-ttu-id="8b0a3-107">*Ausdruck* Eine Variable, die ein **Workspace** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="8b0a3-107">*expression* A variable that represents a **Workspace** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="8b0a3-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="8b0a3-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8b0a3-109">Name</span><span class="sxs-lookup"><span data-stu-id="8b0a3-109">Name</span></span></p></th>
<th><p><span data-ttu-id="8b0a3-110">Erforderlich/Optional</span><span class="sxs-lookup"><span data-stu-id="8b0a3-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="8b0a3-111">Datentyp</span><span class="sxs-lookup"><span data-stu-id="8b0a3-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="8b0a3-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8b0a3-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8b0a3-113">Name</span><span class="sxs-lookup"><span data-stu-id="8b0a3-113">Name</span></span></p></td>
<td><p><span data-ttu-id="8b0a3-114">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="8b0a3-114">Required</span></span></p></td>
<td><p><span data-ttu-id="8b0a3-115"><strong>Zeichenfolge</strong></span><span class="sxs-lookup"><span data-stu-id="8b0a3-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="8b0a3-p101">der Name einer vorhandenen Microsoft Access-Datenbankmoduldatei, oder der Dastenquellname (DSN) einer ODBC-Datenquelle. Weitere Informationen zum Festlegen dieses Werts finden Sie in der <strong><a href="connection-name-property-dao.md">Name</a></strong> -Eigenschaft.  </span><span class="sxs-lookup"><span data-stu-id="8b0a3-p101">the name of an existing Microsoft Access database engine database file, or the data source name (DSN) of an ODBC data source. See the <strong><a href="connection-name-property-dao.md">Name</a></strong> property for more information about setting this value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8b0a3-118">Options</span><span class="sxs-lookup"><span data-stu-id="8b0a3-118">Options</span></span></p></td>
<td><p><span data-ttu-id="8b0a3-119">Optional</span><span class="sxs-lookup"><span data-stu-id="8b0a3-119">Optional</span></span></p></td>
<td><p><span data-ttu-id="8b0a3-120"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="8b0a3-120"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="8b0a3-121">Legt entsprechend der Angaben unter den Hinweisen verschiedene Optionen für die Datenbank fest.</span><span class="sxs-lookup"><span data-stu-id="8b0a3-121">Sets various options for the database, as specified in Remarks.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8b0a3-122">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="8b0a3-122">ReadOnly</span></span></p></td>
<td><p><span data-ttu-id="8b0a3-123">Optional</span><span class="sxs-lookup"><span data-stu-id="8b0a3-123">Optional</span></span></p></td>
<td><p><span data-ttu-id="8b0a3-124"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="8b0a3-124"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="8b0a3-125"><strong>True</strong>, wenn Sie eine Datenbank nur mit Lesezugriff öffnen möchten, oder <strong>False</strong> (Standard), wenn Sie die Datenbank mit Lese-/Schreibzugriff öffnen möchten.</span><span class="sxs-lookup"><span data-stu-id="8b0a3-125"><strong>True</strong> if you want to open the database with read-only access, or <strong>False</strong> (default) if you want to open the database with read/write access.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8b0a3-126">Verbinden</span><span class="sxs-lookup"><span data-stu-id="8b0a3-126">Connect</span></span></p></td>
<td><p><span data-ttu-id="8b0a3-127">Optional</span><span class="sxs-lookup"><span data-stu-id="8b0a3-127">Optional</span></span></p></td>
<td><p><span data-ttu-id="8b0a3-128"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="8b0a3-128"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="8b0a3-129">Gibt verschiedene Verbindungsinformationen an, einschließlich der Kenntwörter.</span><span class="sxs-lookup"><span data-stu-id="8b0a3-129">Specifies various connection information, including passwords.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="8b0a3-130">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8b0a3-130">Return value</span></span>

<span data-ttu-id="8b0a3-131">Datenbank</span><span class="sxs-lookup"><span data-stu-id="8b0a3-131">Database</span></span>

## <a name="remarks"></a><span data-ttu-id="8b0a3-132">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8b0a3-132">Remarks</span></span>

<span data-ttu-id="8b0a3-133">Sie können für das options-Argument folgende Werte verwenden.</span><span class="sxs-lookup"><span data-stu-id="8b0a3-133">You can use the following values for the options argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8b0a3-134">Einstellung</span><span class="sxs-lookup"><span data-stu-id="8b0a3-134">Setting</span></span></p></th>
<th><p><span data-ttu-id="8b0a3-135">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8b0a3-135">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8b0a3-136"><strong>True</strong></span><span class="sxs-lookup"><span data-stu-id="8b0a3-136"><strong>True</strong></span></span></p></td>
<td><p><span data-ttu-id="8b0a3-137">Öffnet die Datenbank im Exklusivmodus.</span><span class="sxs-lookup"><span data-stu-id="8b0a3-137">Opens the database in exclusive mode.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8b0a3-138"><strong>False</strong></span><span class="sxs-lookup"><span data-stu-id="8b0a3-138"><strong>False</strong></span></span></p></td>
<td><p><span data-ttu-id="8b0a3-139">(Standard) Öffnet die Datenbank im Freigabemodus.</span><span class="sxs-lookup"><span data-stu-id="8b0a3-139">(Default) Opens the database in shared mode.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="8b0a3-140">Wenn Sie eine Datenbank öffnen, wird sie automatisch zur **Databases** -Sammlung hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="8b0a3-140">When you open a database, it is automatically added to the **Databases** collection.</span></span>

<span data-ttu-id="8b0a3-141">Einige Aspekte sollten bei Verwenden von Dbname:</span><span class="sxs-lookup"><span data-stu-id="8b0a3-141">Some considerations apply when you use dbname:</span></span>

- <span data-ttu-id="8b0a3-142">Wenn er sich auf eine Datenbank bezieht, die bereits für den Zugriff durch einen anderen Benutzer geöffnet wurde, tritt ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="8b0a3-142">If it refers to a database that is already open for access by another user, an error occurs.</span></span>

- <span data-ttu-id="8b0a3-143">Wenn er sich nicht auf eine vorhandene Datenbank oder einen gültigen ODBC-Datenquellennamen bezieht, tritt ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="8b0a3-143">If it doesn't refer to an existing database or valid ODBC data source name, an error occurs.</span></span>

- <span data-ttu-id="8b0a3-144">Ist eine leere Zeichenfolge ("") und "ODBC;" ist *eine Verbindung herstellen* , wird ein Dialogfeld mit allen registrierten ODBC-Datenquellennamen angezeigt, damit der Benutzer eine Datenbank auswählen kann.</span><span class="sxs-lookup"><span data-stu-id="8b0a3-144">If it's a zero-length string ("") and *connect* is "ODBC;" , a dialog box listing all registered ODBC data source names is displayed so the user can select a database.</span></span>

<span data-ttu-id="8b0a3-145">Um eine Datenbank zu schließen und so das **Database** -Objekt aus der **Databases** -Auflistung zu entfernen, verwenden Sie für das Objekt die **[Close](connection-close-method-dao.md)** -Methode.</span><span class="sxs-lookup"><span data-stu-id="8b0a3-145">To close a database, and thus remove the **Database** object from the **Databases** collection, use the **[Close](connection-close-method-dao.md)** method on the object.</span></span>

> [!NOTE]
> <span data-ttu-id="8b0a3-146">[!HINWEIS] Wenn Sie auf eine ODBC-Datenquelle zugreifen, die mit einem Microsoft Access-Datenbankmodul verbunden ist, können Sie die Leistung der Anwendung verbessern, indem Sie ein **Database** -Objekt öffnen, das mit der ODBC-Datenquelle verbunden ist, anstatt einzelne **[TableDef](tabledef-object-dao.md)** -Objekte mit bestimmten Tabellen in der ODBC-Datenquelle zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="8b0a3-146">When you access a Microsoft access database engine-connected ODBC data source, you can improve your application's performance by opening a **Database** object connected to the ODBC data source, rather than by linking individual **[TableDef](tabledef-object-dao.md)** objects to specific tables in the ODBC data source.</span></span>

## <a name="example"></a><span data-ttu-id="8b0a3-147">Beispiel</span><span class="sxs-lookup"><span data-stu-id="8b0a3-147">Example</span></span>

<span data-ttu-id="8b0a3-148">In diesem Beispiel wird die **OpenDatabase** Methode zum Öffnen einer Microsoft Access-Datenbank und zwei mit dem Microsoft Access-Datenbankmodul verbundenen ODBC-Datenbanken verwendet.</span><span class="sxs-lookup"><span data-stu-id="8b0a3-148">This example uses the **OpenDatabase** method to open one Microsoft Access database and two Microsoft Access database engine-connected ODBC databases.</span></span>

```vb 
Sub OpenDatabaseX() 
 
 Dim wrkAcc As Workspace 
 Dim dbsNorthwind As Database 
 Dim dbsPubs As Database 
 Dim dbsPubs2 As Database 
 Dim dbsLoop As Database 
 Dim prpLoop As Property 
 
 ' Create Microsoft Access Workspace object. 
 Set wrkAcc = CreateWorkspace("", "admin", "", dbUseJet) 
 
 ' Open Database object from saved Microsoft Access database 
 ' for exclusive use. 
 MsgBox "Opening Northwind..." 
 Set dbsNorthwind = wrkAcc.OpenDatabase("Northwind.mdb", _ 
 True) 
 
 ' Open read-only Database object based on information in 
 ' the connect string. 
 MsgBox "Opening pubs..." 
 
 ' Note: The DSN referenced below must be set to 
 ' use Microsoft Windows NT Authentication Mode to 
 ' authorize user access to the Microsoft SQL Server. 
 Set dbsPubs = wrkAcc.OpenDatabase("Publishers", _ 
 dbDriverNoPrompt, True, _ 
 "ODBC;DATABASE=pubs;DSN=Publishers") 
 
 ' Open read-only Database object by entering only the 
 ' missing information in the ODBC Driver Manager dialog 
 ' box. 
 MsgBox "Opening second copy of pubs..." 
 Set dbsPubs2 = wrkAcc.OpenDatabase("Publishers", _ 
 dbDriverCompleteRequired, True, _ 
 "ODBC;DATABASE=pubs;DSN=Publishers;") 
 
 ' Enumerate the Databases collection. 
 For Each dbsLoop In wrkAcc.Databases 
 Debug.Print "Database properties for " & _ 
 dbsLoop.Name & ":" 
 
 On Error Resume Next 
 ' Enumerate the Properties collection of each Database 
 ' object. 
 For Each prpLoop In dbsLoop.Properties 
 If prpLoop.Name = "Connection" Then 
 ' Property actually returns a Connection object. 
 Debug.Print " Connection[.Name] = " & _ 
 dbsLoop.Connection.Name 
 Else 
 Debug.Print " " & prpLoop.Name & " = " & _ 
 prpLoop 
 End If 
 Next prpLoop 
 On Error GoTo 0 
 
 Next dbsLoop 
 
 dbsNorthwind.Close 
 dbsPubs.Close 
 dbsPubs2.Close 
 wrkAcc.Close 
 
End Sub 
 
```

