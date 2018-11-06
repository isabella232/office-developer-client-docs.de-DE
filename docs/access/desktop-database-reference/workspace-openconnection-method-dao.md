---
title: Workspace.OpenConnection-Methode (DAO)
TOCTitle: OpenConnection Method
ms:assetid: 9d97f298-a2d5-3b91-2efd-57f06fbd4654
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198249(v=office.15)
ms:contentKeyID: 48546628
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6a2c7e64d691564eca90c1cf80d57766e04637bb
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998882"
---
# <a name="workspaceopenconnection-method-dao"></a><span data-ttu-id="538e6-102">Workspace.OpenConnection-Methode (DAO)</span><span class="sxs-lookup"><span data-stu-id="538e6-102">Workspace.OpenConnection method (DAO)</span></span>

<span data-ttu-id="538e6-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="538e6-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="538e6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="538e6-104">Syntax</span></span>

<span data-ttu-id="538e6-105">*Ausdruck* . OpenConnection (***Name***, ***Optionen***, ***ReadOnly***, ***Verbinden***)</span><span class="sxs-lookup"><span data-stu-id="538e6-105">*expression* .OpenConnection(***Name***, ***Options***, ***ReadOnly***, ***Connect***)</span></span>

<span data-ttu-id="538e6-106">*Ausdruck* Eine Variable, die ein **Workspace** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="538e6-106">*expression* A variable that represents a **Workspace** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="538e6-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="538e6-107">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="538e6-108">Name</span><span class="sxs-lookup"><span data-stu-id="538e6-108">Name</span></span></p></th>
<th><p><span data-ttu-id="538e6-109">Erforderlich oder optional</span><span class="sxs-lookup"><span data-stu-id="538e6-109">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="538e6-110">Datentyp</span><span class="sxs-lookup"><span data-stu-id="538e6-110">Data type</span></span></p></th>
<th><p><span data-ttu-id="538e6-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="538e6-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="538e6-112"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="538e6-112"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="538e6-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="538e6-113">Required</span></span></p></td>
<td><p><span data-ttu-id="538e6-114"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="538e6-114"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="538e6-p101">Ein Zeichenfolgenausdruck. Weitere Informationen erhalten Sie im Abschnitt "Hinweise".</span><span class="sxs-lookup"><span data-stu-id="538e6-p101">A string expression. See the discussion under Remarks.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="538e6-117"><em>Options</em></span><span class="sxs-lookup"><span data-stu-id="538e6-117"><em>Options</em></span></span></p></td>
<td><p><span data-ttu-id="538e6-118">Optional</span><span class="sxs-lookup"><span data-stu-id="538e6-118">Optional</span></span></p></td>
<td><p><span data-ttu-id="538e6-119"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="538e6-119"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="538e6-p102">Legt verschiedene Optionen für die Verbindung fest, wie unter "Hinweise" beschrieben. Basierend auf diesem Wert fordert der ODBC-Treibermanager den Benutzer auf, Verbindungsdaten einzugeben, z. B. den Datenquellennamen (Data Source Name, DSN), den Benutzernamen oder das Kennwort.</span><span class="sxs-lookup"><span data-stu-id="538e6-p102">sets various options for the connection, as specified in Remarks. Based on this value, the ODBC driver manager prompts the user for connection information such as data source name (DSN), user name, and password.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="538e6-122"><em>ReadOnly</em></span><span class="sxs-lookup"><span data-stu-id="538e6-122"><em>ReadOnly</em></span></span></p></td>
<td><p><span data-ttu-id="538e6-123">Optional</span><span class="sxs-lookup"><span data-stu-id="538e6-123">Optional</span></span></p></td>
<td><p><span data-ttu-id="538e6-124"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="538e6-124"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="538e6-125"><strong>True</strong>, um die Verbindung nur mit Lesezugriff zu öffnen, und <strong>False</strong>, wenn die Verbindung mit Lese-/Schreibzugriff geöffnet werden soll (Standard).</span><span class="sxs-lookup"><span data-stu-id="538e6-125"><strong>True</strong> if the connection is to be opened for read-only access and <strong>False</strong> if the connection is to be opened for read/write access (default).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="538e6-126"><em>Connect</em></span><span class="sxs-lookup"><span data-stu-id="538e6-126"><em>Connect</em></span></span></p></td>
<td><p><span data-ttu-id="538e6-127">Optional</span><span class="sxs-lookup"><span data-stu-id="538e6-127">Optional</span></span></p></td>
<td><p><span data-ttu-id="538e6-128"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="538e6-128"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="538e6-129">Eine ODBC-Verbindungszeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="538e6-129">An ODBC connection string.</span></span> <span data-ttu-id="538e6-130">Finden Sie unter der <strong><a href="connection-connect-property-dao.md">Connect</a></strong> -Eigenschaft für die bestimmte Elemente und die Syntax dieser Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="538e6-130">See the <strong><a href="connection-connect-property-dao.md">Connect</a></strong> property for the specific elements and syntax of this string.</span></span> <span data-ttu-id="538e6-131">Eine vorangestellt &quot;ODBC; &quot; ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="538e6-131">A prepended &quot;ODBC;&quot; is required.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="538e6-132">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="538e6-132">Return value</span></span>

<span data-ttu-id="538e6-133">Connection</span><span class="sxs-lookup"><span data-stu-id="538e6-133">Connection</span></span>

## <a name="remarks"></a><span data-ttu-id="538e6-134">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="538e6-134">Remarks</span></span>

<span data-ttu-id="538e6-p104">Mit der **OpenConnection**-Methode können Sie aus einem ODBC-Arbeitsbereich eine Verbindung zu einer ODBC-Datenquelle herstellen. Die **OpenConnection**-Methode ähnelt der **OpenDatabase**-Methode. Der wichtigste Unterschied besteht darin, dass **OpenConnection** nur in einem ODBCDirect-Arbeitsbereich verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="538e6-p104">Use the **OpenConnection** method to establish a connection to an ODBC data source from an ODBCDirect workspace. The **OpenConnection** method is similar but not equivalent to **OpenDatabase**. The main difference is that **OpenConnection** is available only in an ODBCDirect workspace.</span></span>

<span data-ttu-id="538e6-138">Wenn Sie einen registrierten ODBC-Datenquellennamen (DSN) in der Connect-Argument angeben, klicken Sie dann im Name-Argument kann eine beliebige gültige Zeichenfolge sein, und stellt auch die **Name** -Eigenschaft für das **Connection** -Objekt bereit.</span><span class="sxs-lookup"><span data-stu-id="538e6-138">If you specify a registered ODBC data source name (DSN) in the connect argument, then the name argument can be any valid string, and will also provide the **Name** property for the **Connection** object.</span></span> <span data-ttu-id="538e6-139">Wenn Sie ein gültiger DSN in der Connect-Argument nicht enthalten ist, muss Name auf einen gültigen ODBC DSN verweisen, die auch die **Name** -Eigenschaft verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="538e6-139">If a valid DSN is not included in the connect argument, then name must refer to a valid ODBC DSN, which will also be the **Name** property.</span></span> <span data-ttu-id="538e6-140">Wenn weder name noch connect enthält keinen gültigen DSN, kann der ODBC-Treiber-Manager auf der Benutzer für die erforderlichen Verbindungsinformationen aufgefordert (über das Argument Options) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="538e6-140">If neither name nor connect contains a valid DSN, the ODBC driver manager can be set (via the options argument) to prompt the user for the required connection information.</span></span> <span data-ttu-id="538e6-141">Der durch die Eingabeaufforderung bereitgestellte DSN gibt dann die **Name**-Eigenschaft an.</span><span class="sxs-lookup"><span data-stu-id="538e6-141">The DSN supplied through the prompt then provides the **Name** property.</span></span>

<span data-ttu-id="538e6-p106">Durch das Argument options ist festgelegt, ob und zu welchem Zeitpunkt der Benutzer aufgefordert wird, die Verbindung herzustellen, und ob die Verbindung asynchron geöffnet werden soll. Sie können eine der folgenden Konstanten verwenden.</span><span class="sxs-lookup"><span data-stu-id="538e6-p106">The options argument determines if and when to prompt the user to establish the connection, and whether or not to open the connection asynchronously. You can use one of the following constants.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="538e6-144">Konstante</span><span class="sxs-lookup"><span data-stu-id="538e6-144">Constant</span></span></p></th>
<th><p><span data-ttu-id="538e6-145">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="538e6-145">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="538e6-146"><strong>dbDriverNoPrompt</strong></span><span class="sxs-lookup"><span data-stu-id="538e6-146"><strong>dbDriverNoPrompt</strong></span></span></p></td>
<td><p><span data-ttu-id="538e6-p107">Der ODBC-Treibermanager verwendet die in <em>dbname</em> und <em>connect</em> angegebene Verbindungszeichenfolge. Es tritt ein Laufzeitfehler auf, wenn Sie nicht genügend Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="538e6-p107">The ODBC Driver Manager uses the connection string provided in <em>dbname</em> and <em>connect</em>. If you don't provide sufficient information, a run-time error occurs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="538e6-149"><strong>dbDriverPrompt</strong></span><span class="sxs-lookup"><span data-stu-id="538e6-149"><strong>dbDriverPrompt</strong></span></span></p></td>
<td><p><span data-ttu-id="538e6-p108">Der ODBC-Treibermanager zeigt das Dialogfeld <strong>ODBC-Datenquelle</strong> an, das alle relevanten Informationen enthält, die in <em>dbname</em> oder <em>connect</em> angegeben wurden. Die Verbindungszeichenfolge entspricht dem DSN, den der Benutzer über Dialogfelder auswählt. Wenn der Benutzer keinen DSN angegeben hat, wird der standardmäßige DSN verwendet.</span><span class="sxs-lookup"><span data-stu-id="538e6-p108">The ODBC Driver Manager displays the <strong>ODBC Data Sources</strong> dialog box, which displays any relevant information supplied in <em>dbname</em> or <em>connect</em>. The connection string is made up of the DSN that the user selects via the dialog boxes, or, if the user doesn't specify a DSN, the default DSN is used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="538e6-152"><strong>dbDriverComplete</strong></span><span class="sxs-lookup"><span data-stu-id="538e6-152"><strong>dbDriverComplete</strong></span></span></p></td>
<td><p><span data-ttu-id="538e6-p109">Standard. Enthält das Argument <em>connect</em> alle für die Verbindung erforderlichen Informationen, verwendet der ODBC-Treibermanager die Zeichenfolge in <em>connect</em>. Andernfalls verhält er sich so, als hätten Sie <strong>dbDriverPrompt</strong> angegeben.</span><span class="sxs-lookup"><span data-stu-id="538e6-p109">Default. If the <em>connect</em> argument includes all the necessary information to complete a connection, the ODBC Driver Manager uses the string in <em>connect</em>. Otherwise it behaves as it does when you specify <strong>dbDriverPrompt</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="538e6-156"><strong>dbDriverCompleteRequired</strong></span><span class="sxs-lookup"><span data-stu-id="538e6-156"><strong>dbDriverCompleteRequired</strong></span></span></p></td>
<td><p><span data-ttu-id="538e6-157">Das Verhalten dieser Option entspricht dem von <strong>dbDriverComplete</strong>, mit der Ausnahme, dass der ODBC-Treiber die Eingabeaufforderungen für alle Informationen deaktiviert, die nicht für die Verbindung erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="538e6-157">This option behaves like <strong>dbDriverComplete</strong> except the ODBC driver disables the prompts for any information not required to complete the connection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="538e6-158"><strong>dbRunAsync</strong></span><span class="sxs-lookup"><span data-stu-id="538e6-158"><strong>dbRunAsync</strong></span></span></p></td>
<td><p><span data-ttu-id="538e6-p110">Die Methode wird asynchron ausgeführt. Diese Konstante kann mit jeder anderen <em>options</em>-Konstante verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="538e6-p110">Execute the method asynchronously. This constant may be used with any of the other <em>options</em> constants.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<span data-ttu-id="538e6-p111">**OpenConnection** gibt ein **Connection**-Objekt zurück, das Informationen zur Verbindung enthält. Das **Connection**-Objekt ähnelt einem **[Database](database-object-dao.md)** -Objekt. Der Hauptunterschied liegt darin, dass ein **Database**-Objekt in der Regel eine Datenbank repräsentiert, aber auch verwendet werden kann, um eine Verbindung zu einer ODBC-Datenquelle aus einem Microsoft Access-Arbeitsbereich darzustellen.</span><span class="sxs-lookup"><span data-stu-id="538e6-p111">**OpenConnection** returns a **Connection** object which contains information about the connection. The **Connection** object is similar to a **[Database](database-object-dao.md)** object. The principal difference is that a **Database** object usually represents a database, although it can be used to represent a connection to an ODBC data source from a Microsoft Access workspace.</span></span>

## <a name="example"></a><span data-ttu-id="538e6-164">Beispiel</span><span class="sxs-lookup"><span data-stu-id="538e6-164">Example</span></span>

<span data-ttu-id="538e6-165">In diesem Beispiel wird die **OpenConnection**-Methode mit verschiedenen Parametern verwendet, um drei verschiedene **Connection**-Objekte zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="538e6-165">This example uses the **OpenConnection** method with different parameters to open three different **Connection** objects.</span></span>

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
 ' use Microsoft Windows NT Authentication Mode to 
 ' authorize user access to the Microsoft SQL Server. 
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
 Debug.Print " Connect = " & .Connect 
 ' Property actually returns a Database object. 
 Debug.Print " Database[.Name] = " & _ 
 .Database.Name 
 Debug.Print " Name = " & .Name 
 Debug.Print " QueryTimeout = " & .QueryTimeout 
 Debug.Print " RecordsAffected = " & _ 
 .RecordsAffected 
 Debug.Print " StillExecuting = " & _ 
 .StillExecuting 
 Debug.Print " Transactions = " & .Transactions 
 Debug.Print " Updatable = " & .Updatable 
 End With 
 
 Next conLoop 
 
 conPubs.Close 
 conPubs2.Close 
 conPubs3.Close 
 wrkODBC.Close 
 
End Sub 
 
```

<br/>

<span data-ttu-id="538e6-166">In diesem Beispiel werden das **Connection**-Objekt und die **Connections**-Auflistung veranschaulicht. Dazu werden ein **Database**-Objekt von Microsoft Access und zwei **Connection**-Objekte von ODBCDirect geöffnet, und die für die einzelnen Objekte verfügbaren Eigenschaften werden aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="538e6-166">This example demonstrates the **Connection** object and **Connections** collection by opening a Microsoft Access **Database** object and two ODBCDirect **Connection** objects and listing the properties available to each object.</span></span>

```vb 
Sub ConnectionObjectX() 
 
 Dim wrkAcc as Workspace 
 Dim dbsNorthwind As Database 
 Dim wrkODBC As Workspace 
 Dim conPubs As Connection 
 Dim conPubs2 As Connection 
 Dim conLoop As Connection 
 Dim prpLoop As Property 
 
 ' Open Microsoft Access Database object. 
 Set wrkAcc = CreateWorkspace("NewWorkspace", _ 
 "admin", "", dbUseJet) 
 Set dbsNorthwind = wrkAcc.OpenDatabase("Northwind.mdb") 
 
 ' Create ODBCDirect Workspace object and open Connection 
 ' objects. 
 Set wrkODBC = CreateWorkspace("NewODBCWorkspace", _ 
 "admin", "", dbUseODBC) 
 
 ' Note: The DSNs referenced below must be configured to 
 ' use Microsoft Windows NT Authentication Mode to 
 ' authorize user access to the Microsoft SQL Server. 
 Set conPubs = wrkODBC.OpenConnection("Connection1", , , _ 
 "ODBC;DATABASE=pubs;DSN=Publishers") 
 
 Set conPubs2 = wrkODBC.OpenConnection("Connection2", , _ 
 True, "ODBC;DATABASE=pubs;DSN=Publishers") 
 
 Debug.Print "Database properties:" 
 
 With dbsNorthwind 
 ' Enumerate Properties collection of Database object. 
 For Each prpLoop In .Properties 
 On Error Resume Next 
 Debug.Print " " & prpLoop.Name & " = " & _ 
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
 Debug.Print " Connect = " & .Connect 
 ' Property actually returns a Database object. 
 Debug.Print " Database[.Name] = " & _ 
 .Database.Name 
 Debug.Print " Name = " & .Name 
 Debug.Print " QueryTimeout = " & .QueryTimeout 
 Debug.Print " RecordsAffected = " & _ 
 .RecordsAffected 
 Debug.Print " StillExecuting = " & _ 
 .StillExecuting 
 Debug.Print " Transactions = " & .Transactions 
 Debug.Print " Updatable = " & .Updatable 
 End With 
 
 Next conLoop 
 
 dbsNorthwind.Close 
 conPubs.Close 
 conPubs2.Close 
 wrkAcc.Close 
 wrkODBC.Close 
 
End Sub 
 
```

