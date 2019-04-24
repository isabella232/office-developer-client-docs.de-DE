---
title: Recordset2. reQuery-Methode (DAO)
TOCTitle: Requery Method
ms:assetid: d063c1e0-2fb7-b5cf-4d98-6f77a5a13cec
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834712(v=office.15)
ms:contentKeyID: 48547837
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052940
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 44f573d179c26677fc801dac82e0deecc3874fb1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307210"
---
# <a name="recordset2requery-method-dao"></a><span data-ttu-id="5a07c-102">Recordset2. reQuery-Methode (DAO)</span><span class="sxs-lookup"><span data-stu-id="5a07c-102">Recordset2.Requery method (DAO)</span></span>

<span data-ttu-id="5a07c-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5a07c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5a07c-104">Die Daten in einem **[Recordset](recordset-object-dao.md)** -Objekt werden aktualisiert durch erneutes Ausführen der Abfrage, auf der das Objekt basiert.</span><span class="sxs-lookup"><span data-stu-id="5a07c-104">Updates the data in a **[Recordset](recordset-object-dao.md)** object by re-executing the query on which the object is based.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a07c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5a07c-105">Syntax</span></span>

<span data-ttu-id="5a07c-106">*Ausdruck* . ReQuery (***NewQueryDef***)</span><span class="sxs-lookup"><span data-stu-id="5a07c-106">*expression* .Requery(***NewQueryDef***)</span></span>

<span data-ttu-id="5a07c-107">*Ausdruck* Eine Variable, die ein **Recordset2** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="5a07c-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="5a07c-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="5a07c-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5a07c-109">Name</span><span class="sxs-lookup"><span data-stu-id="5a07c-109">Name</span></span></p></th>
<th><p><span data-ttu-id="5a07c-110">Erforderlich/optional</span><span class="sxs-lookup"><span data-stu-id="5a07c-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="5a07c-111">Datentyp</span><span class="sxs-lookup"><span data-stu-id="5a07c-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="5a07c-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5a07c-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5a07c-113"><em>NewQueryDef</em></span><span class="sxs-lookup"><span data-stu-id="5a07c-113"><em>NewQueryDef</em></span></span></p></td>
<td><p><span data-ttu-id="5a07c-114">Optional</span><span class="sxs-lookup"><span data-stu-id="5a07c-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="5a07c-115"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="5a07c-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="5a07c-116">Stellt den <strong>Name</strong> -Eigenschaftenwert eines <strong><a href="querydef-object-dao.md">QueryDef</a></strong> -Objekts dar</span><span class="sxs-lookup"><span data-stu-id="5a07c-116">Represents the <strong>Name</strong> property value of a <strong><a href="querydef-object-dao.md">QueryDef</a></strong> object</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="5a07c-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5a07c-117">Remarks</span></span>

<span data-ttu-id="5a07c-118">Verwenden Sie diese Methode, um sicherzustellen, dass ein **Recordset** die neuesten Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="5a07c-118">Use this method to make sure that a **Recordset** contains the most recent data.</span></span> <span data-ttu-id="5a07c-119">Diese Methode füllt das aktuelle  **Recordset** neu aus, indem sie entweder die aktuellen Abfrageparameter oder (in einem Microsoft Access-Arbeitsbereich) die vom newquerydef-Argument neu bereitgestgellten verwendet.</span><span class="sxs-lookup"><span data-stu-id="5a07c-119">This method re-populates the current **Recordset** by using either the current query parameters or (in a Microsoft Access workspace) the new ones supplied by the newquerydef argument.</span></span>

<span data-ttu-id="5a07c-120">Wenn Sie kein newquerydef-Argument angeben haben, wird das **Recordset** basierend auf der gleichen Abfragedefinition und den gleichen Parametern neu ausgefüllt, die ursprünglich zum Ausfüllen des **Recordset** verwendet wurden.</span><span class="sxs-lookup"><span data-stu-id="5a07c-120">If you don't specify a newquerydef argument, the **Recordset** is re-populated based on the same query definition and parameters used to originally populate the **Recordset**.</span></span> <span data-ttu-id="5a07c-121">Änderungen der zugrunde liegenden Daten werden während des erneuten Ausfüllens berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="5a07c-121">Any changes to the underlying data will be reflected during this re-population.</span></span> <span data-ttu-id="5a07c-122">Wenn Sie keine **QueryDef** zum Erstellen des **Recordset** verwendet haben, wird das **Recordset** komplett neu erstellt.</span><span class="sxs-lookup"><span data-stu-id="5a07c-122">If you didn't use a **QueryDef** to create the **Recordset**, the **Recordset** is re-created from scratch.</span></span>

<span data-ttu-id="5a07c-123">Wenn Sie das ursprüngliche **QueryDef** -Objekt im newquerydef-Argument angeben, wird das **Recordset** mithilfe der vom **QueryDef**-Objekt angegebenen Parameter erneut abgefragt.</span><span class="sxs-lookup"><span data-stu-id="5a07c-123">If you specify the original **QueryDef** in the newquerydef argument, then the **Recordset** is requeried using the parameters specified by the **QueryDef**.</span></span> <span data-ttu-id="5a07c-124">Änderungen der zugrunde liegenden Daten werden während des erneuten Ausfüllens übernommen.</span><span class="sxs-lookup"><span data-stu-id="5a07c-124">Any changes to the underlying data will be reflected during this re-population.</span></span> <span data-ttu-id="5a07c-125">Um Änderungen der Abfrageparameterwerte im **Recordset** zu übernehmen, müssen Sie das newquerydef-Argument angeben.</span><span class="sxs-lookup"><span data-stu-id="5a07c-125">To reflect any changes to the query parameter values in the **Recordset**, you must supply the newquerydef argument.</span></span>

<span data-ttu-id="5a07c-126">Wenn Sie eine andere **QueryDef** als die angeben, die ursprünglich zum Erstellen des **Recordset** verwendet wurde, wird das **Recordset** komplett neu erstellt.</span><span class="sxs-lookup"><span data-stu-id="5a07c-126">If you specify a different **QueryDef** than what was originally used to create the **Recordset**, the **Recordset** is re-created from scratch.</span></span>

<span data-ttu-id="5a07c-127">Wenn Sie **Requery** verwenden, wird der erste Datensatz im **Recordset** der aktuelle Datensatz.</span><span class="sxs-lookup"><span data-stu-id="5a07c-127">When you use **Requery**, the first record in the **Recordset** becomes the current record.</span></span>

<span data-ttu-id="5a07c-128">You can't use the **Requery** method on dynaset- or snapshot-type **Recordset** objects whose **[Restartable](recordset2-restartable-property-dao.md)** property is set to **False**.</span><span class="sxs-lookup"><span data-stu-id="5a07c-128">You can't use the **Requery** method on dynaset- or snapshot-type **Recordset** objects whose **[Restartable](recordset2-restartable-property-dao.md)** property is set to **False**.</span></span> <span data-ttu-id="5a07c-129">Wenn Sie jedoch das optionale newquerydef-Argument angeben, wird \*\*\*\* die Restartable-Eigenschaft ignoriert.</span><span class="sxs-lookup"><span data-stu-id="5a07c-129">However, if you supply the optional newquerydef argument, the **Restartable** property is ignored.</span></span>

<span data-ttu-id="5a07c-130">Ist für die beiden Eigenschafteneinstellungen **[BOF](recordset2-bof-property-dao.md)** und **[EOF](recordset2-eof-property-dao.md)** des **Recordset**-Objekts nach dem Verwenden der **Requery**-Methode **True** festgelegt, hat die Abfrage keine Datensätze zurückgegeben, und das **Recordset** enthält keine Daten.</span><span class="sxs-lookup"><span data-stu-id="5a07c-130">If both the **[BOF](recordset2-bof-property-dao.md)** and **[EOF](recordset2-eof-property-dao.md)** property settings of the **Recordset** object are **True** after you use the **Requery** method, the query didn't return any records and the **Recordset** contains no data.</span></span>

## <a name="example"></a><span data-ttu-id="5a07c-131">Beispiel</span><span class="sxs-lookup"><span data-stu-id="5a07c-131">Example</span></span>

<span data-ttu-id="5a07c-132">Dieses Beispiel zeigt, wie die **Requery**-Methode zum Aktualisieren einer Abfrage verwendet werden kann, nachdem die zugrunde liegenden Daten geändert wurden.</span><span class="sxs-lookup"><span data-stu-id="5a07c-132">This example shows how the **Requery** method can be used to refresh a query after underlying data has been changed.</span></span>

```vb
    Sub RequeryX() 
     
     Dim dbsNorthwind As Database 
     Dim qdfTemp As QueryDef 
     Dim rstView As Recordset2 
     Dim rstChange As Recordset2 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set qdfTemp = dbsNorthwind.CreateQueryDef("", _ 
     "PARAMETERS ViewCountry Text; " & _ 
     "SELECT FirstName, LastName, Country FROM " & _ 
     "Employees WHERE Country = [ViewCountry] " & _ 
     "ORDER BY LastName") 
     
     qdfTemp.Parameters!ViewCountry = "USA" 
     Debug.Print "Data after initial query, " & _ 
     [ViewCountry] = USA" 
     Set rstView = qdfTemp.OpenRecordset 
     Do While Not rstView.EOF 
     Debug.Print " " & rstView!FirstName & " " & _ 
     rstView!LastName & ", " & rstView!Country 
     rstView.MoveNext 
     Loop 
     
     ' Change underlying data. 
     Set rstChange = dbsNorthwind.OpenRecordset("Employees") 
     rstChange.AddNew 
     rstChange!FirstName = "Nina" 
     rstChange!LastName = "Roberts" 
     rstChange!Country = "USA" 
     rstChange.Update 
     
     rstView.Requery 
     Debug.Print "Requery after changing underlying data" 
     Set rstView = qdfTemp.OpenRecordset 
     Do While Not rstView.EOF 
     Debug.Print " " & rstView!FirstName & " " & _ 
     rstView!LastName & ", " & rstView!Country 
     rstView.MoveNext 
     Loop 
     
     ' Restore original data because this is only a 
     ' demonstration. 
     rstChange.Bookmark = rstChange.LastModified 
     rstChange.Delete 
     rstChange.Close 
     
     rstView.Close 
     dbsNorthwind.Close 
     
    End Sub 
```

<br/>

<span data-ttu-id="5a07c-133">Dieses Beispiel zeigt, wie die **Requery**-Methode zum Aktualisieren einer Abfrage verwendet werden kann, nachdem die Abfrageparamter geändert wurden.</span><span class="sxs-lookup"><span data-stu-id="5a07c-133">This example shows how the **Requery** method can be used to refresh a query after the query parameters have been changed.</span></span>

```vb
Sub RequeryX2() 
 
 Dim dbsNorthwind As Database 
 Dim qdfTemp As QueryDef 
 Dim prmCountry As Parameter 
 Dim rstView As Recordset2 
 
 Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 Set qdfTemp = dbsNorthwind.CreateQueryDef("", _ 
 "PARAMETERS ViewCountry Text; " & _ 
 "SELECT FirstName, LastName, Country FROM " & _ 
 "Employees WHERE Country = [ViewCountry] " & _ 
 "ORDER BY LastName") 
 Set prmCountry = qdfTemp.Parameters!ViewCountry 
 
 qdfTemp.Parameters!ViewCountry = "USA" 
 Debug.Print "Data after initial query, " & _ 
 [ViewCountry] = USA" 
 Set rstView = qdfTemp.OpenRecordset 
 Do While Not rstView.EOF 
 Debug.Print " " & rstView!FirstName & " " & _ 
 rstView!LastName & ", " & rstView!Country 
 rstView.MoveNext 
 Loop 
 
 ' Change query parameter. 
 qdfTemp.Parameters!ViewCountry = "UK" 
 ' QueryDef argument must be included so that the 
 ' resulting Recordset reflects the change in the query 
 ' parameter. 
 rstView.Requery qdfTemp 
 Debug.Print "Requery after changing parameter, " & _ 
 "[ViewCountry] = UK" 
 Do While Not rstView.EOF 
 Debug.Print " " & rstView!FirstName & " " & _ 
 rstView!LastName & ", " & rstView!Country 
 rstView.MoveNext 
 Loop 
 
 rstView.Close 
 dbsNorthwind.Close 
 
End Sub 
 
```

