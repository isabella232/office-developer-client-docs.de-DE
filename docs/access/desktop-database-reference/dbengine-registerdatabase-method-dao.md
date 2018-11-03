---
title: DBEngine.RegisterDatabase-Methode (DAO)
TOCTitle: RegisterDatabase Method
ms:assetid: ed87a694-2c89-0a78-5d8b-0cc7e09fadff
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836347(v=office.15)
ms:contentKeyID: 48548541
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052938
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 767bd146de7a5568d7441024adb9ad6816cb806e
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25923511"
---
# <a name="dbengineregisterdatabase-method-dao"></a><span data-ttu-id="f33d4-102">DBEngine.RegisterDatabase-Methode (DAO)</span><span class="sxs-lookup"><span data-stu-id="f33d4-102">DBEngine.RegisterDatabase method (DAO)</span></span>


<span data-ttu-id="f33d4-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f33d4-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="f33d4-p101">Gibt Verbindungsinformationen für eine ODBC-Datenquelle in die Windows-Registrierung ein. Der ODBC-Treiber benötigt Verbindungsinformationen, wenn die ODBC-Datenquelle während einer Sitzung geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="f33d4-p101">Enters connection information for an ODBC data source in the Windows Registry. The ODBC driver needs connection information when the ODBC data source is opened during a session.</span></span>

## <a name="syntax"></a><span data-ttu-id="f33d4-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="f33d4-106">Syntax</span></span>

<span data-ttu-id="f33d4-107">*Ausdruck* . RegisterDatabase (***Dsn***, ***Treiber***, ***Automatische***, ***Attribute***)</span><span class="sxs-lookup"><span data-stu-id="f33d4-107">*expression* .RegisterDatabase(***Dsn***, ***Driver***, ***Silent***, ***Attributes***)</span></span>

<span data-ttu-id="f33d4-108">*Ausdruck* Eine Variable, die ein **DBEngine** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="f33d4-108">*expression* A variable that represents a **DBEngine** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="f33d4-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="f33d4-109">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f33d4-110">Name</span><span class="sxs-lookup"><span data-stu-id="f33d4-110">Name</span></span></p></th>
<th><p><span data-ttu-id="f33d4-111">Erforderlich/Optional</span><span class="sxs-lookup"><span data-stu-id="f33d4-111">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="f33d4-112">Datentyp</span><span class="sxs-lookup"><span data-stu-id="f33d4-112">Data Type</span></span></p></th>
<th><p><span data-ttu-id="f33d4-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f33d4-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f33d4-114">DSN</span><span class="sxs-lookup"><span data-stu-id="f33d4-114">Dsn</span></span></p></td>
<td><p><span data-ttu-id="f33d4-115">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="f33d4-115">Required</span></span></p></td>
<td><p><span data-ttu-id="f33d4-116"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="f33d4-116"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="f33d4-p102">Der in der <strong><a href="dbengine-opendatabase-method-dao.md">OpenDatabase</a></strong>-Methode verwendete Name. Er verweist auf einen Block mit beschreibenden Informationen zur Datenquelle. Ist die Datenquelle beispielsweise eine ODBC-Remote-Datenquelle, könnte diese der Name des Servers sein.</span><span class="sxs-lookup"><span data-stu-id="f33d4-p102">the name used in the <strong><a href="dbengine-opendatabase-method-dao.md">OpenDatabase</a></strong> method. It refers to a block of descriptive information about the data source. For example, if the data source is an ODBC remote database, it could be the name of the server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f33d4-120">Treiber</span><span class="sxs-lookup"><span data-stu-id="f33d4-120">Driver</span></span></p></td>
<td><p><span data-ttu-id="f33d4-121">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="f33d4-121">Required</span></span></p></td>
<td><p><span data-ttu-id="f33d4-122"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="f33d4-122"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="f33d4-p103">Der Name des ODBC-Treibers. Er entspricht nicht dem Namen der DLL-Datei des ODBC-Treibers.</span><span class="sxs-lookup"><span data-stu-id="f33d4-p103">The name of the ODBC driver. This isn't the name of the ODBC driver DLL file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f33d4-125">Automatische</span><span class="sxs-lookup"><span data-stu-id="f33d4-125">Silent</span></span></p></td>
<td><p><span data-ttu-id="f33d4-126">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="f33d4-126">Required</span></span></p></td>
<td><p><span data-ttu-id="f33d4-127"><strong>Boolean</strong></span><span class="sxs-lookup"><span data-stu-id="f33d4-127"><strong>Boolean</strong></span></span></p></td>
<td><p><span data-ttu-id="f33d4-128"><strong>True,</strong> Wenn Sie nicht möchten, um die ODBC-Treiber-Dialogfelder anzuzeigen, die Treiber-spezifische Informationen aufgefordert. oder <strong>False,</strong> Wenn Sie die ODBC-Treiber Dialogfelder anzeigen möchten.</span><span class="sxs-lookup"><span data-stu-id="f33d4-128"><strong>True</strong> if you don't want to display the ODBC driver dialog boxes that prompt for driver-specific information; or <strong>False</strong> if you want to display the ODBC driver dialog boxes.</span></span> <span data-ttu-id="f33d4-129">Wenn im Hintergrund ist <strong>True</strong>, Attribute müssen alle erforderliche Treiber-spezifische Informationen enthalten oder die Dialogfelder trotzdem angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f33d4-129">If silent is <strong>True</strong>, attributes must contain all the necessary driver-specific information or the dialog boxes are displayed anyway.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f33d4-130">Attribute</span><span class="sxs-lookup"><span data-stu-id="f33d4-130">Attributes</span></span></p></td>
<td><p><span data-ttu-id="f33d4-131">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="f33d4-131">Required</span></span></p></td>
<td><p><span data-ttu-id="f33d4-132"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="f33d4-132"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="f33d4-p105">Eine Liste der Schlüsselwörter, die zur Windows-Registrierung hinzugefügt werden sollen. Die Schlüsselwörter sind in Zeichenfolgen enthalten, die durch Wagenrücklaufzeichen getrennt sind.</span><span class="sxs-lookup"><span data-stu-id="f33d4-p105">A list of keywords to be added to the Windows Registry. The keywords are in a carriage-return–delimited string.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="f33d4-135">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f33d4-135">Remarks</span></span>

<span data-ttu-id="f33d4-136">Ist die Datenbank beim Verwenden der **RegisterDatabase**-Methode bereits in der Windows-Registrierung registriert (Verbindungsinformationen wurden eingegeben), werden die Verbindungsinformationen aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="f33d4-136">If the database is already registered (connection information is already entered) in the Windows Registry when you use the **RegisterDatabase** method, the connection information is updated.</span></span>

<span data-ttu-id="f33d4-137">Wenn die **RegisterDatabase**-Methode fehlschlägt, werden keine Änderungen in der Windows-Registrierung vorgenommen, und es tritt ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="f33d4-137">If the **RegisterDatabase** method fails for any reason, no changes are made to the Windows Registry, and an error occurs.</span></span>

<span data-ttu-id="f33d4-138">Weitere Informationen zu ODBC-Treibern wie SQL Server finden Sie in der vom Treiber bereitgestellten Hilfedatei.</span><span class="sxs-lookup"><span data-stu-id="f33d4-138">For more information about ODBC drivers such as SQL Server, see the Help file provided with the driver.</span></span>

## <a name="example"></a><span data-ttu-id="f33d4-139">Beispiel</span><span class="sxs-lookup"><span data-stu-id="f33d4-139">Example</span></span>

<span data-ttu-id="f33d4-140">In diesem Beispiel wird die **RegisterDatabase**-Methode verwendet, um eine Microsoft SQL Server-Datenquelle namens Publishers in der Windows-Registrierung zu erfassen.</span><span class="sxs-lookup"><span data-stu-id="f33d4-140">This example uses the **RegisterDatabase** method to register a Microsoft SQL Server data source named Publishers in the Windows Registry.</span></span>

```vb 
Sub RegisterDatabaseX() 
 
 Dim dbsRegister As Database 
 Dim strDescription As String 
 Dim strAttributes As String 
 Dim errLoop As Error 
 
 ' Build keywords string. 
 strDescription = InputBox( "Enter a description " & _ 
 "for the database to be registered.") 
 strAttributes = "Database=pubs" & _ 
 vbCr & "Description=" & strDescription & _ 
 vbCr & "OemToAnsi=No" & _ 
 vbCr & "Server=Server1" 
 
 ' Update Windows Registry. 
 On Error GoTo Err_Register 
 DBEngine.RegisterDatabase "Publishers", "SQL Server", _ 
 True, strAttributes 
 On Error GoTo 0 
 
 MsgBox "Use regedit.exe to view changes: " & _ 
 "HKEY_CURRENT_USER\" & _ 
 "Software\ODBC\ODBC.INI" 
 
 Exit Sub 
 
Err_Register: 
 
 ' Notify user of any errors that result from 
 ' the invalid data. 
 If DBEngine.Errors.Count > 0 Then 
 For Each errLoop In DBEngine.Errors 
 MsgBox "Error number: " & errLoop.Number & _ 
 vbCr & errLoop.Description 
 Next errLoop 
 End If 
 
 Resume Next 
 
End Sub 
 
```

