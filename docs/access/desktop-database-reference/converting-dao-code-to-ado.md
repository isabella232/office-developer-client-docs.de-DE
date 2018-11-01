---
title: Konvertieren von DAO-Code in ADO
TOCTitle: Convert DAO code to ADO
ms:assetid: 4720906b-d6b1-aa6d-3b18-ff828d16acae
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193201(v=office.15)
ms:contentKeyID: 48544585
ms.date: 10/16/2018
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm5267115
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 60baeabfce93c2987cb9621c7cc877a7525a954c
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25876743"
---
# <a name="convert-dao-code-to-ado"></a><span data-ttu-id="bfee0-102">Konvertieren von DAO-Code in ADO</span><span class="sxs-lookup"><span data-stu-id="bfee0-102">Convert DAO code to ADO</span></span>

<span data-ttu-id="bfee0-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="bfee0-103">**Applies to**: Access 2013, Office 2013</span></span>

> [!NOTE]
> <span data-ttu-id="bfee0-104">Versionen der DAO-Bibliothek vor Version 3.6 nicht bereitgestellt oder in Access unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bfee0-104">Versions of the DAO library prior to 3.6 are not provided or supported in Access.</span></span>

## <a name="dao-to-ado-object-map"></a><span data-ttu-id="bfee0-105">DAO-Objekten in ADO-objektzuordnung</span><span class="sxs-lookup"><span data-stu-id="bfee0-105">DAO to ADO object map</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bfee0-106"><strong>DAO</strong></span><span class="sxs-lookup"><span data-stu-id="bfee0-106"><strong>DAO</strong></span></span></p></th>
<th><p><span data-ttu-id="bfee0-107"><strong>ADO (ADODB)</strong></span><span class="sxs-lookup"><span data-stu-id="bfee0-107"><strong>ADO (ADODB)</strong></span></span></p></th>
<th><p><span data-ttu-id="bfee0-108"><strong>Hinweis</strong></span><span class="sxs-lookup"><span data-stu-id="bfee0-108"><strong>Note</strong></span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bfee0-109">DBEngine</span><span class="sxs-lookup"><span data-stu-id="bfee0-109">DBEngine</span></span></p></td>
<td><p><span data-ttu-id="bfee0-110">Keine</span><span class="sxs-lookup"><span data-stu-id="bfee0-110">None</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bfee0-111">Workspace</span><span class="sxs-lookup"><span data-stu-id="bfee0-111">Workspace</span></span></p></td>
<td><p><span data-ttu-id="bfee0-112">Keine</span><span class="sxs-lookup"><span data-stu-id="bfee0-112">None</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bfee0-113">Database</span><span class="sxs-lookup"><span data-stu-id="bfee0-113">Database</span></span></p></td>
<td><p><span data-ttu-id="bfee0-114">Connection</span><span class="sxs-lookup"><span data-stu-id="bfee0-114">Connection</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bfee0-115">Recordset</span><span class="sxs-lookup"><span data-stu-id="bfee0-115">Recordset</span></span></p></td>
<td><p><span data-ttu-id="bfee0-116">Recordset</span><span class="sxs-lookup"><span data-stu-id="bfee0-116">Recordset</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bfee0-117">Dynaset-Type</span><span class="sxs-lookup"><span data-stu-id="bfee0-117">Dynaset-Type</span></span></p></td>
<td><p><span data-ttu-id="bfee0-118">Keyset</span><span class="sxs-lookup"><span data-stu-id="bfee0-118">Keyset</span></span></p></td>
<td><p><span data-ttu-id="bfee0-119">Ruft eine Gruppe von Zeigern für die Datensätze im Recordset-Objekt ab.</span><span class="sxs-lookup"><span data-stu-id="bfee0-119">Retrieves a set of pointers to the records in the recordset.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bfee0-120">Snapshot-Type</span><span class="sxs-lookup"><span data-stu-id="bfee0-120">Snapshot-Type</span></span></p></td>
<td><p><span data-ttu-id="bfee0-121">Static</span><span class="sxs-lookup"><span data-stu-id="bfee0-121">Static</span></span></p></td>
<td><p><span data-ttu-id="bfee0-122">Beide vollständige Datensätze abrufen, jedoch kann eine statische Datensatzgruppe aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="bfee0-122">Both retrieve full records, but a Static recordset can be updated.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bfee0-123">Table-Type</span><span class="sxs-lookup"><span data-stu-id="bfee0-123">Table-Type</span></span></p></td>
<td><p><span data-ttu-id="bfee0-124">Keyset mit Option AdCmdTableDirect.</span><span class="sxs-lookup"><span data-stu-id="bfee0-124">Keyset with adCmdTableDirect option.</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bfee0-125">Field</span><span class="sxs-lookup"><span data-stu-id="bfee0-125">Field</span></span></p></td>
<td><p><span data-ttu-id="bfee0-126">Field</span><span class="sxs-lookup"><span data-stu-id="bfee0-126">Field</span></span></p></td>
<td><p><span data-ttu-id="bfee0-127">Wenn in einem Recordset bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="bfee0-127">When referred to in a recordset.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>
<br/>

### <a name="dao"></a><span data-ttu-id="bfee0-128">DAO</span><span class="sxs-lookup"><span data-stu-id="bfee0-128">DAO</span></span>

#### <a name="open-a-recordset"></a><span data-ttu-id="bfee0-129">Öffnen eines Recordsets</span><span class="sxs-lookup"><span data-stu-id="bfee0-129">Open a Recordset</span></span>

```vb
 Dim db as Database
 Dim rs as DAO.Recordset
 Set db = CurrentDB()
 Set rs = db.OpenRecordset("Employees")
```

#### <a name="edit-a-recordset"></a><span data-ttu-id="bfee0-130">Bearbeiten eines Recordsets</span><span class="sxs-lookup"><span data-stu-id="bfee0-130">Edit a Recordset</span></span>

```vb
 rs.Edit 
 rs("TextFieldName") = "NewValue"
 rs.Update
```

### <a name="ado"></a><span data-ttu-id="bfee0-131">ADO</span><span class="sxs-lookup"><span data-stu-id="bfee0-131">ADO</span></span>

#### <a name="open-a-recordset"></a><span data-ttu-id="bfee0-132">Öffnen eines Recordsets</span><span class="sxs-lookup"><span data-stu-id="bfee0-132">Open a Recordset</span></span>

```vb
 Dim rs as New ADODB.Recordset
 rs.Open "Employees", CurrentProject.Connection, _
         adOpenKeySet, adLockOptimistic
```

#### <a name="edit-a-recordset"></a><span data-ttu-id="bfee0-133">Bearbeiten eines Recordsets</span><span class="sxs-lookup"><span data-stu-id="bfee0-133">Edit a Recordset</span></span>

```vb
 rs("TextFieldName") = "NewValue" 
 rs.Update
```


> [!NOTE]
> <span data-ttu-id="bfee0-134">Verschieben den Fokus vom aktuellen Datensatz über **MoveNext, MoveLast, MoveFirst, MovePrevious** ohne zuerst die **CancelUpdate** -Methode implizit führt die **Update** -Methode.</span><span class="sxs-lookup"><span data-stu-id="bfee0-134">Moving focus from current record via **MoveNext, MoveLast, MoveFirst, MovePrevious** without first using the **CancelUpdate** method implicitly executes the **Update** method.</span></span>

### <a name="about-the-contributors"></a><span data-ttu-id="bfee0-135">Informationen zu den Mitwirkenden</span><span class="sxs-lookup"><span data-stu-id="bfee0-135">About the contributors</span></span>

<span data-ttu-id="bfee0-136">**Link bereitgestellt, von** der Community [UtterAccess](https://www.utteraccess.com) .</span><span class="sxs-lookup"><span data-stu-id="bfee0-136">**Link provided by** the [UtterAccess](https://www.utteraccess.com) community.</span></span> <span data-ttu-id="bfee0-137">UtterAccess ist das führende Microsoft Access-Wiki und -Hilfeforum.</span><span class="sxs-lookup"><span data-stu-id="bfee0-137">UtterAccess is the premier Microsoft Access wiki and help forum.</span></span>

- <span data-ttu-id="bfee0-138">[Choosing between DAO and ADO](https://www.utteraccess.com/wiki/index.php/choosing_between_dao_and_ado) (Wählen zwischen DAO und ADO)</span><span class="sxs-lookup"><span data-stu-id="bfee0-138">[Choosing between DAO and ADO](https://www.utteraccess.com/wiki/index.php/choosing_between_dao_and_ado)</span></span>

<br/>

