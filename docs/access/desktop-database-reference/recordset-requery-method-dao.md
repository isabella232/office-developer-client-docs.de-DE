---
title: Recordset.Requery-Methode (DAO)
TOCTitle: Requery Method
ms:assetid: a5d66eb5-499c-4133-f6c3-c7a1619a8a11
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821155(v=office.15)
ms:contentKeyID: 48546840
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d5c98eeb94e49693cf13d358987307f61f15069c
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998336"
---
# <a name="recordsetrequery-method-dao"></a><span data-ttu-id="43a7a-102">Recordset.Requery-Methode (DAO)</span><span class="sxs-lookup"><span data-stu-id="43a7a-102">Recordset.Requery method (DAO)</span></span>

<span data-ttu-id="43a7a-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="43a7a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="43a7a-104">Die Daten in einem **[Recordset](recordset-object-dao.md)** -Objekt werden aktualisiert durch erneutes Ausführen der Abfrage, auf der das Objekt basiert.</span><span class="sxs-lookup"><span data-stu-id="43a7a-104">Updates the data in a **[Recordset](recordset-object-dao.md)** object by re-executing the query on which the object is based.</span></span>

## <a name="syntax"></a><span data-ttu-id="43a7a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="43a7a-105">Syntax</span></span>

<span data-ttu-id="43a7a-106">*Ausdruck* . Requery (***NewQueryDef***)</span><span class="sxs-lookup"><span data-stu-id="43a7a-106">*expression* .Requery(***NewQueryDef***)</span></span>

<span data-ttu-id="43a7a-107">*Ausdruck* Eine Variable, die ein **Recordset** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="43a7a-107">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="43a7a-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="43a7a-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="43a7a-109">Name</span><span class="sxs-lookup"><span data-stu-id="43a7a-109">Name</span></span></p></th>
<th><p><span data-ttu-id="43a7a-110">Erforderlich oder optional</span><span class="sxs-lookup"><span data-stu-id="43a7a-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="43a7a-111">Datentyp</span><span class="sxs-lookup"><span data-stu-id="43a7a-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="43a7a-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="43a7a-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="43a7a-113"><em>NewQueryDef</em></span><span class="sxs-lookup"><span data-stu-id="43a7a-113"><em>NewQueryDef</em></span></span></p></td>
<td><p><span data-ttu-id="43a7a-114">Optional</span><span class="sxs-lookup"><span data-stu-id="43a7a-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="43a7a-115"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="43a7a-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="43a7a-116">Stellt den <strong>Name</strong> -Eigenschaftenwert eines <strong><a href="querydef-object-dao.md">QueryDef</a></strong> -Objekts dar</span><span class="sxs-lookup"><span data-stu-id="43a7a-116">Represents the <strong>Name</strong> property value of a <strong><a href="querydef-object-dao.md">QueryDef</a></strong> object</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="43a7a-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="43a7a-117">Remarks</span></span>

<span data-ttu-id="43a7a-118">Verwenden Sie diese Methode, um sicherzustellen, dass ein **Recordset** die aktuellsten Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="43a7a-118">Use this method to make sure that a **Recordset** contains the most recent data.</span></span> <span data-ttu-id="43a7a-119">Diese Methode füllt das aktuelle **Recordset** erneut mithilfe der aktuellen Abfrageparameter oder (in einem Microsoft Access-Arbeitsbereich) die neuen Dateien durch das Argument Newquerydef angegeben.</span><span class="sxs-lookup"><span data-stu-id="43a7a-119">This method re-populates the current **Recordset** by using either the current query parameters or (in a Microsoft Access workspace) the new ones supplied by the newquerydef argument.</span></span>

<span data-ttu-id="43a7a-120">Wenn Sie ein Argument Newquerydef nicht angeben, wird das **Recordset-Objekt** neu aufgefüllt basierend auf dem gleichen Abfragedefinition und Parameter verwendet, um das **Recordset**ursprünglich aufzufüllen.</span><span class="sxs-lookup"><span data-stu-id="43a7a-120">If you don't specify a newquerydef argument, the **Recordset** is re-populated based on the same query definition and parameters used to originally populate the **Recordset**.</span></span> <span data-ttu-id="43a7a-121">Änderungen an zugrunde liegenden Daten werden während des Auffüllvorgangs angezeigt.</span><span class="sxs-lookup"><span data-stu-id="43a7a-121">Any changes to the underlying data will be reflected during this re-population.</span></span> <span data-ttu-id="43a7a-122">Wenn Sie zum Erstellen des **Recordset**-Objekts kein **QueryDef**-Objekt verwendet haben, wird das **Recordset** ganz neu erstellt.</span><span class="sxs-lookup"><span data-stu-id="43a7a-122">If you didn't use a **QueryDef** to create the **Recordset**, the **Recordset** is re-created from scratch.</span></span>

<span data-ttu-id="43a7a-123">Wenn Sie die ursprünglichen **QueryDef-Objekt** im Newquerydef Argument angeben, wird das **Recordset** erneut abgefragt mit den Parametern von **QueryDef-Objekt**angegeben.</span><span class="sxs-lookup"><span data-stu-id="43a7a-123">If you specify the original **QueryDef** in the newquerydef argument, then the **Recordset** is requeried using the parameters specified by the **QueryDef**.</span></span> <span data-ttu-id="43a7a-124">Änderungen an zugrunde liegenden Daten werden während des Auffüllvorgangs angezeigt.</span><span class="sxs-lookup"><span data-stu-id="43a7a-124">Any changes to the underlying data will be reflected during this re-population.</span></span> <span data-ttu-id="43a7a-125">Alle Änderungen an der Abfrageparameterwerte im **Recordset-Objekt**aktualisiert, müssen Sie das Argument Newquerydef angeben.</span><span class="sxs-lookup"><span data-stu-id="43a7a-125">To reflect any changes to the query parameter values in the **Recordset**, you must supply the newquerydef argument.</span></span>

<span data-ttu-id="43a7a-126">Wenn Sie ein anderes **QueryDef** angeben als das, mit dem das **Recordset** ursprünglich erstellt wurde, wird das **Recordset** völlig neu erstellt.</span><span class="sxs-lookup"><span data-stu-id="43a7a-126">If you specify a different **QueryDef** than what was originally used to create the **Recordset**, the **Recordset** is re-created from scratch.</span></span>

<span data-ttu-id="43a7a-127">Beim Anwenden von **Requery** wird der erste Datensatz im **Recordset** zum aktuellen Datensatz.</span><span class="sxs-lookup"><span data-stu-id="43a7a-127">When you use **Requery**, the first record in the **Recordset** becomes the current record.</span></span>

<span data-ttu-id="43a7a-128">Sie können die **Requery** -Methode nicht für **Recordset** -Objekte des dynaset- oder snapshot-Typs verwenden, deren **[Restartable](recordset-restartable-property-dao.md)** -Eigenschaft auf **False** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="43a7a-128">You can't use the **Requery** method on dynaset- or snapshot-type **Recordset** objects whose **[Restartable](recordset-restartable-property-dao.md)** property is set to **False**.</span></span> <span data-ttu-id="43a7a-129">Wenn Sie das Argument optional Newquerydef angeben, wird jedoch die **Restartable** -Eigenschaft ignoriert.</span><span class="sxs-lookup"><span data-stu-id="43a7a-129">However, if you supply the optional newquerydef argument, the **Restartable** property is ignored.</span></span>

<span data-ttu-id="43a7a-130">Ist für die beiden Eigenschafteneinstellungen **[BOF](recordset-bof-property-dao.md)** und **[EOF](recordset-eof-property-dao.md)** des **Recordset**-Objekts nach dem Verwenden der **Requery**-Methode **True** festgelegt, hat die Abfrage keine Datensätze zurückgegeben, und das **Recordset** enthält keine Daten.</span><span class="sxs-lookup"><span data-stu-id="43a7a-130">If both the **[BOF](recordset-bof-property-dao.md)** and **[EOF](recordset-eof-property-dao.md)** property settings of the **Recordset** object are **True** after you use the **Requery** method, the query didn't return any records and the **Recordset** contains no data.</span></span>

## <a name="example"></a><span data-ttu-id="43a7a-131">Beispiel</span><span class="sxs-lookup"><span data-stu-id="43a7a-131">Example</span></span>

<span data-ttu-id="43a7a-132">Dieses Beispiel zeigt, wie die **Requery** -Methode zum Aktualisieren einer Abfrage verwendet werden kann, nachdem die zugrunde liegenden Daten geändert wurden.</span><span class="sxs-lookup"><span data-stu-id="43a7a-132">This example shows how the **Requery** method can be used to refresh a query after underlying data has been changed.</span></span>

```vb
    Sub RequeryX() 
     
     Dim dbsNorthwind As Database 
     Dim qdfTemp As QueryDef 
     Dim rstView As Recordset 
     Dim rstChange As Recordset 
     
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

<span data-ttu-id="43a7a-133">Dieses Beispiel zeigt, wie die **Requery** -Methode zum Aktualisieren einer Abfrage verwendet werden kann, nachdem die Abfrageparamter geändert wurden.</span><span class="sxs-lookup"><span data-stu-id="43a7a-133">This example shows how the **Requery** method can be used to refresh a query after the query parameters have been changed.</span></span>

```vb 
Sub RequeryX2() 
 
 Dim dbsNorthwind As Database 
 Dim qdfTemp As QueryDef 
 Dim prmCountry As Parameter 
 Dim rstView As Recordset 
 
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

