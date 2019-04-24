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
localization_priority: Priority
ms.openlocfilehash: 77d56efd63d6a0841b595f12456baa808751706e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295520"
---
# <a name="convert-dao-code-to-ado"></a><span data-ttu-id="38202-102">Konvertieren von DAO-Code in ADO</span><span class="sxs-lookup"><span data-stu-id="38202-102">Convert DAO code to ADO</span></span>

<span data-ttu-id="38202-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="38202-103">**Applies to**: Access 2013, Office 2013</span></span>

> [!NOTE]
> <span data-ttu-id="38202-104">Versionen der DAO-Bibliothek, die älter als Version 3.6 sind, werden in Access nicht bereitgestellt und nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="38202-104">Versions of the DAO library prior to 3.6 are not provided or supported in Microsoft Access 2013.</span></span>

## <a name="dao-to-ado-object-map"></a><span data-ttu-id="38202-105">Umwandlung von DAO-Objekten in ADO-Objekte</span><span class="sxs-lookup"><span data-stu-id="38202-105">DAO to ADO object Map</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="38202-106"><strong>DAO</strong></span><span class="sxs-lookup"><span data-stu-id="38202-106"><strong>DAO</strong></span></span></p></th>
<th><p><span data-ttu-id="38202-107"><strong>ADO (ADODB)</strong></span><span class="sxs-lookup"><span data-stu-id="38202-107"><strong>ADO (ADODB)</strong></span></span></p></th>
<th><p><span data-ttu-id="38202-108"><strong>Hinweis</strong></span><span class="sxs-lookup"><span data-stu-id="38202-108"><strong>Note</strong></span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="38202-109">DBEngine</span><span class="sxs-lookup"><span data-stu-id="38202-109">DBEngine</span></span></p></td>
<td><p><span data-ttu-id="38202-110">Keine</span><span class="sxs-lookup"><span data-stu-id="38202-110">None</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38202-111">Workspace</span><span class="sxs-lookup"><span data-stu-id="38202-111">Workspace</span></span></p></td>
<td><p><span data-ttu-id="38202-112">Keine</span><span class="sxs-lookup"><span data-stu-id="38202-112">None</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38202-113">Datenbank</span><span class="sxs-lookup"><span data-stu-id="38202-113">Database</span></span></p></td>
<td><p><span data-ttu-id="38202-114">Verbindung</span><span class="sxs-lookup"><span data-stu-id="38202-114">Connection</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38202-115">Recordset</span><span class="sxs-lookup"><span data-stu-id="38202-115">Recordset</span></span></p></td>
<td><p><span data-ttu-id="38202-116">Recordset</span><span class="sxs-lookup"><span data-stu-id="38202-116">Recordset</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38202-117">Dynaset-Type</span><span class="sxs-lookup"><span data-stu-id="38202-117">Dynaset-Type</span></span></p></td>
<td><p><span data-ttu-id="38202-118">Keyset</span><span class="sxs-lookup"><span data-stu-id="38202-118">Keyset</span></span></p></td>
<td><p><span data-ttu-id="38202-119">Ruft eine Gruppe von Zeigern für die Datensätze der Datensatzgruppe ab.</span><span class="sxs-lookup"><span data-stu-id="38202-119">Retrieves a set of pointers to the records in the recordset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38202-120">Snapshot-Type</span><span class="sxs-lookup"><span data-stu-id="38202-120">Snapshot-Type</span></span></p></td>
<td><p><span data-ttu-id="38202-121">Static</span><span class="sxs-lookup"><span data-stu-id="38202-121">Static</span></span></p></td>
<td><p><span data-ttu-id="38202-122">Rufen beide vollständige Datensätze ab, doch eine Datensatzgruppe vom Typ Static kann aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="38202-122">Both retrieve full records but a Static recordset can be updated.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38202-123">Table-Type</span><span class="sxs-lookup"><span data-stu-id="38202-123">Table-Type</span></span></p></td>
<td><p><span data-ttu-id="38202-124">Keyset mit Option adCmdTableDirect.</span><span class="sxs-lookup"><span data-stu-id="38202-124">Keyset with adCmdTableDirect Option</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38202-125">Feld</span><span class="sxs-lookup"><span data-stu-id="38202-125">Field</span></span></p></td>
<td><p><span data-ttu-id="38202-126">Feld</span><span class="sxs-lookup"><span data-stu-id="38202-126">Field</span></span></p></td>
<td><p><span data-ttu-id="38202-127">Wenn darauf in einer Datensatzgruppe verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="38202-127">When referred to in a recordset</span></span></p></td>
</tr>
</tbody>
</table>

<br/>
<br/>

### <a name="dao"></a><span data-ttu-id="38202-128">DAO</span><span class="sxs-lookup"><span data-stu-id="38202-128">DAO</span></span>

#### <a name="open-a-recordset"></a><span data-ttu-id="38202-129">Recordset öffnen</span><span class="sxs-lookup"><span data-stu-id="38202-129">Open a Recordset</span></span>

```vb
 Dim db as Database
 Dim rs as DAO.Recordset
 Set db = CurrentDB()
 Set rs = db.OpenRecordset("Employees")
```

#### <a name="edit-a-recordset"></a><span data-ttu-id="38202-130">Recordset bearbeiten</span><span class="sxs-lookup"><span data-stu-id="38202-130">Edit a Recordset</span></span>

```vb
 rs.Edit 
 rs("TextFieldName") = "NewValue"
 rs.Update
```

### <a name="ado"></a><span data-ttu-id="38202-131">ADO</span><span class="sxs-lookup"><span data-stu-id="38202-131">ADO</span></span>

#### <a name="open-a-recordset"></a><span data-ttu-id="38202-132">Recordset öffnen</span><span class="sxs-lookup"><span data-stu-id="38202-132">Open a Recordset</span></span>

```vb
 Dim rs as New ADODB.Recordset
 rs.Open "Employees", CurrentProject.Connection, _
         adOpenKeySet, adLockOptimistic
```

#### <a name="edit-a-recordset"></a><span data-ttu-id="38202-133">Recordset bearbeiten</span><span class="sxs-lookup"><span data-stu-id="38202-133">Edit a Recordset</span></span>

```vb
 rs("TextFieldName") = "NewValue" 
 rs.Update
```


> [!NOTE]
> <span data-ttu-id="38202-134">Wenn der Fokus über **MoveNext, MoveLast, MoveFirst, MovePrevious** vom aktuellen Datensatz verschoben wird, ohne zuerst die **CancelUpdate**-Methode zu verwenden, wird die **Update**-Methode implizit ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="38202-134">Moving focus from current record via **MoveNext, MoveLast, MoveFirst, MovePrevious** without first using the **CancelUpdate** method will implicitly execute the **Update** method.</span></span>

### <a name="about-the-contributors"></a><span data-ttu-id="38202-135">Informationen zu den Mitwirkenden</span><span class="sxs-lookup"><span data-stu-id="38202-135">About the contributors</span></span>

<span data-ttu-id="38202-136">\*\*Link zur Verfügung gestellt von: \*\* [UtterAccess](https://www.utteraccess.com)-Community.</span><span class="sxs-lookup"><span data-stu-id="38202-136">**Link provided by:Community Member Icon** The [UtterAccess](https://www.utteraccess.com) community</span></span> <span data-ttu-id="38202-137">UtterAccess ist das führende Microsoft Access-Wiki und -Hilfeforum.</span><span class="sxs-lookup"><span data-stu-id="38202-137">UtterAccess is the premier Microsoft Access wiki and help forum.</span></span>

- [<span data-ttu-id="38202-138">Entscheidung zwischen DAO und ADO</span><span class="sxs-lookup"><span data-stu-id="38202-138">Choosing between DAO and ADO</span></span>](https://www.utteraccess.com/wiki/index.php/choosing_between_dao_and_ado)

<br/>

