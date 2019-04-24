---
title: DbEngine. Idle-Methode (DAO)
TOCTitle: Idle Method
ms:assetid: c90b565e-626e-139d-102a-0386601ce0c8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823202(v=office.15)
ms:contentKeyID: 48547666
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052978
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 7a84e3cc4b35886a12b2e6b4cf92b7483fea293a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294330"
---
# <a name="dbengineidle-method-dao"></a><span data-ttu-id="b15a6-102">DbEngine. Idle-Methode (DAO)</span><span class="sxs-lookup"><span data-stu-id="b15a6-102">DBEngine.Idle method (DAO)</span></span>

<span data-ttu-id="b15a6-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b15a6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b15a6-104">Unterbricht die Datenverarbeitung und ermöglicht es dem Microsoft Access-Datenbankmodul, anstehende Aufgaben auszuführen, z. B. Speicheroptimierung oder Timeouts von Seiten (gilt nur für Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="b15a6-104">Suspends data processing, enabling the Microsoft Access database engine to complete any pending tasks, such as memory optimization or page timeouts (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="b15a6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b15a6-105">Syntax</span></span>

<span data-ttu-id="b15a6-106">*Ausdruck* . Leerlauf (***Aktion***)</span><span class="sxs-lookup"><span data-stu-id="b15a6-106">*expression* .Idle(***Action***)</span></span>

<span data-ttu-id="b15a6-107">*Ausdruck* Eine Variable, die ein **DBEngine** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="b15a6-107">*expression* A variable that represents a **DBEngine** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="b15a6-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="b15a6-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b15a6-109">Name</span><span class="sxs-lookup"><span data-stu-id="b15a6-109">Name</span></span></p></th>
<th><p><span data-ttu-id="b15a6-110">Erforderlich/optional</span><span class="sxs-lookup"><span data-stu-id="b15a6-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="b15a6-111">Datentyp</span><span class="sxs-lookup"><span data-stu-id="b15a6-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="b15a6-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b15a6-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b15a6-113"><em>Action</em></span><span class="sxs-lookup"><span data-stu-id="b15a6-113"><em>Action</em></span></span></p></td>
<td><p><span data-ttu-id="b15a6-114">Optional</span><span class="sxs-lookup"><span data-stu-id="b15a6-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="b15a6-115"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="b15a6-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="b15a6-116">Gibt die auszuführende Aktion an.</span><span class="sxs-lookup"><span data-stu-id="b15a6-116">Specifies the action to take.</span></span> <span data-ttu-id="b15a6-117">Dies kann eine der <strong><a href="idleenum-enumeration-dao.md">IdleEnum</a></strong> -Konstanten sein.</span><span class="sxs-lookup"><span data-stu-id="b15a6-117">Can be one of the <strong><a href="idleenum-enumeration-dao.md">IdleEnum</a></strong> constants.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="b15a6-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b15a6-118">Remarks</span></span>

<span data-ttu-id="b15a6-p102">Mit der **Idle**-Methode kann das Microsoft Access-Datenbankmodul Hintergrundaufgaben ausführen, die wegen der umfangreichen Datenverarbeitung möglicherweise nicht mehr aktuell sind. Dies kommt oft in Multitaskingumgebungen mit mehreren Benutzern vor, in denen die Hintergrundverarbeitungszeit nicht ausreicht, um alls Datensätze in einem **[Recordset](recordset-object-dao.md)** auf dem aktuellen Stand zu halten.</span><span class="sxs-lookup"><span data-stu-id="b15a6-p102">The **Idle** method allows the Microsoft Access database engine to perform background tasks that may not be up-to-date because of intense data processing. This is often true in multiuser, multitasking environments that don't have enough background processing time to keep all records in a **[Recordset](recordset-object-dao.md)** current.</span></span>

<span data-ttu-id="b15a6-p103">Usually, read locks are removed and data in local dynaset-type **Recordset** objects are updated only when no other actions (including mouse movements) occur. If you periodically use the **Idle** method, the Microsoft Access database engine can catch up on background processing tasks by releasing unneeded read locks.</span><span class="sxs-lookup"><span data-stu-id="b15a6-p103">Usually, read locks are removed and data in local dynaset-type **Recordset** objects are updated only when no other actions (including mouse movements) occur. If you periodically use the **Idle** method, the Microsoft Access database engine can catch up on background processing tasks by releasing unneeded read locks.</span></span>

<span data-ttu-id="b15a6-123">Durch Angabe des optionalen Arguments **dbRefreshCache** wird der Speicher nur mit den aktuellsten Daten aus der Datenbank aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="b15a6-123">Specifying the optional **dbRefreshCache** argument refreshes memory with only the most current data from the database.</span></span>

<span data-ttu-id="b15a6-p104">Sie müssen diese Methode nur dann in Einzelbenutzerumgebungen anrwenden, wenn mehrere Instanzen einer Anwendung ausgeführt werden. Durch die **Idle**-Methode kann die Leistung in einer Mehrbenutzerumgebung verbessert werden, da das Datenbankmodul gezwungen wird, Daten auf einen Datenträger zu schreiben und Sperren im Speicher freizugeben.</span><span class="sxs-lookup"><span data-stu-id="b15a6-p104">You don't need to use this method in single-user environments unless multiple instances of an application are running. The **Idle** method may increase performance in a multiuser environment because it forces the database engine to write data to disk, releasing locks on memory.</span></span>


> [!NOTE]
> <span data-ttu-id="b15a6-126">[!HINWEIS] Sie können Lesesperren auch dadurch freigeben, dass Sie Operationen zum Bestandteil einer Transaktion machen.</span><span class="sxs-lookup"><span data-stu-id="b15a6-126">You can also release read locks by making operations part of a transaction.</span></span>

## <a name="example"></a><span data-ttu-id="b15a6-127">Beispiel</span><span class="sxs-lookup"><span data-stu-id="b15a6-127">Example</span></span>

<span data-ttu-id="b15a6-p105">This example uses the **Idle** method to ensure that an output procedure is accessing the most current data available from the database. The IdleOutput procedure is required for this procedure to run.</span><span class="sxs-lookup"><span data-stu-id="b15a6-p105">This example uses the **Idle** method to ensure that an output procedure is accessing the most current data available from the database. The IdleOutput procedure is required for this procedure to run.</span></span>

```vb 
Sub IdleX() 
 
 Dim dbsNorthwind As Database 
 Dim strCountry As String 
 Dim strSQL As String 
 Dim rstOrders As Recordset 
 
 Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 
 ' Get name of country from user and build SQL statement 
 ' with it. 
 strCountry = Trim(InputBox("Enter country:")) 
 strSQL = "SELECT * FROM Orders WHERE ShipCountry = '" & _ 
 strCountry & "' ORDER BY OrderID" 
 
 ' Open Recordset object with SQL statement. 
 Set rstOrders = dbsNorthwind.OpenRecordset(strSQL) 
 
 ' Display contents of Recordset object. 
 IdleOutput rstOrders, strCountry 
 
 rstOrders.Close 
 dbsNorthwind.Close 
 
End Sub 
 
Sub IdleOutput(rstTemp As Recordset, strTemp As String) 
 
 ' Call the Idle method to release unneeded locks, force 
 ' pending writes, and refresh the memory with the current 
 ' data in the .mdb file. 
 DBEngine.Idle dbRefreshCache 
 
 ' Enumerate the Recordset object. 
 With rstTemp 
 Debug.Print "Orders from " & strTemp & ":" 
 Debug.Print , "OrderID", "CustomerID", "OrderDate" 
 Do While Not .EOF 
 Debug.Print , !OrderID, !CustomerID, !OrderDate 
 .MoveNext 
 Loop 
 End With 
 
End Sub 
 
```

