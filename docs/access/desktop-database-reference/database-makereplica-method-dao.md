---
title: Database. MakeReplica-Methode (DAO)
TOCTitle: MakeReplica Method
ms:assetid: b6bf4982-0804-12ce-849f-d2b4ac2e48a5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822413(v=office.15)
ms:contentKeyID: 48547286
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053371
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 9b9e2eac360d157f28b986b6598ade58b8c34ec6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294918"
---
# <a name="databasemakereplica-method-dao"></a><span data-ttu-id="d067b-102">Database. MakeReplica-Methode (DAO)</span><span class="sxs-lookup"><span data-stu-id="d067b-102">Database.MakeReplica method (DAO)</span></span>

<span data-ttu-id="d067b-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d067b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d067b-104">Macht aus einem Datenbankreplikat ein neues Replikat (gilt nur für Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="d067b-104">Makes a new replica from another database replica (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="d067b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d067b-105">Syntax</span></span>

<span data-ttu-id="d067b-106">*Ausdruck* . MakeReplica (***Pfadname***, ***Beschreibung***, ***Optionen***)</span><span class="sxs-lookup"><span data-stu-id="d067b-106">*expression* .MakeReplica(***PathName***, ***Description***, ***Options***)</span></span>

<span data-ttu-id="d067b-107">*Ausdruck* Eine Variable, die ein **Database** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="d067b-107">*expression* A variable that represents a **Database** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="d067b-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="d067b-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d067b-109">Name</span><span class="sxs-lookup"><span data-stu-id="d067b-109">Name</span></span></p></th>
<th><p><span data-ttu-id="d067b-110">Erforderlich/optional</span><span class="sxs-lookup"><span data-stu-id="d067b-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="d067b-111">Datentyp</span><span class="sxs-lookup"><span data-stu-id="d067b-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="d067b-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d067b-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d067b-113"><em>PathName</em></span><span class="sxs-lookup"><span data-stu-id="d067b-113"><em>PathName</em></span></span></p></td>
<td><p><span data-ttu-id="d067b-114">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="d067b-114">Required</span></span></p></td>
<td><p><span data-ttu-id="d067b-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="d067b-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="d067b-116">Der Pfad- und Dateiname des neuen Replikats.</span><span class="sxs-lookup"><span data-stu-id="d067b-116">The path and file name of the new replica.</span></span> <span data-ttu-id="d067b-117">Wenn replica ein vorhandener Dateiname ist, tritt ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="d067b-117">If replica is an existing file name, then an error occurs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d067b-118"><em>Description</em></span><span class="sxs-lookup"><span data-stu-id="d067b-118"><em>Description</em></span></span></p></td>
<td><p><span data-ttu-id="d067b-119">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="d067b-119">Required</span></span></p></td>
<td><p><span data-ttu-id="d067b-120"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="d067b-120"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="d067b-121">Ein <strong>String</strong>-Wert, der das Replikat beschreibt, das Sie erstellen.</span><span class="sxs-lookup"><span data-stu-id="d067b-121">A <strong>String</strong> that describes the replica that you are creating</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d067b-122"><em>Options</em></span><span class="sxs-lookup"><span data-stu-id="d067b-122"><em>Options</em></span></span></p></td>
<td><p><span data-ttu-id="d067b-123">Optional</span><span class="sxs-lookup"><span data-stu-id="d067b-123">Optional</span></span></p></td>
<td><p><span data-ttu-id="d067b-124"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="d067b-124"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="d067b-125">Eine <strong><a href="replicatypeenum-enumeration-dao.md">ReplicaTypeEnum</a></strong> -Konstante, die die Merkmale des Replikats angibt, das Sie erstellen.</span><span class="sxs-lookup"><span data-stu-id="d067b-125">A <strong><a href="replicatypeenum-enumeration-dao.md">ReplicaTypeEnum</a></strong> constant that specifies characteristics of the replica you are creating.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="d067b-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d067b-126">Remarks</span></span>

<span data-ttu-id="d067b-127">Für ein neu erstelltes Teilreplikat werden sämtliche **[ReplicaFilter](tabledef-replicafilter-property-dao.md)** -Eigenschaften auf **False** festgelegt, was bedeutet, dass die Tabelle keine Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="d067b-127">A newly created partial replica will have all **[ReplicaFilter](tabledef-replicafilter-property-dao.md)** properties set to **False**, meaning that no data will be in the tables.</span></span>

## <a name="example"></a><span data-ttu-id="d067b-128">Beispiel</span><span class="sxs-lookup"><span data-stu-id="d067b-128">Example</span></span>

<span data-ttu-id="d067b-129">This function uses the **MakeReplica** method to create an additional replica of an existing Design Master.</span><span class="sxs-lookup"><span data-stu-id="d067b-129">This function uses the **MakeReplica** method to create an additional replica of an existing Design Master.</span></span> <span data-ttu-id="d067b-130">Das intOptions-Argument kann eine Kombination aus den Konstanten **dbRepMakeReadOnly** und **dbRepMakePartial**oder 0 sein.</span><span class="sxs-lookup"><span data-stu-id="d067b-130">The intOptions argument can be a combination of the constants **dbRepMakeReadOnly** and **dbRepMakePartial**, or it can be 0.</span></span> <span data-ttu-id="d067b-131">Wenn Sie beispielsweise ein nur-Lese-Teilreplikat erstellen möchten, sollten Sie den Wert **dbRepMakeReadOnly** + **dbRepMakePartial** als Wert von intOptions.</span><span class="sxs-lookup"><span data-stu-id="d067b-131">For example, to create a read-only partial replica, you should pass the value **dbRepMakeReadOnly** + **dbRepMakePartial** as the value of intOptions.</span></span>

```vb 
Function MakeAdditionalReplica(strReplicableDB As _ 
 String, strNewReplica As String, intOptions As _ 
 Integer) As Integer 
 
 Dim dbsTemp As Database 
 On Error GoTo ErrorHandler 
 
 Set dbsTemp = OpenDatabase(strReplicableDB) 
 
 ' If no options are passed to 
 ' MakeAdditionalReplica, omit the 
 ' options argument, which defaults to 
 ' a full, read/write replica. Otherwise, 
 ' use the value of intOptions. 
 
 If intOptions = 0 Then 
 dbsTemp.MakeReplica strNewReplica, _ 
 "Replica of " & strReplicableDB 
 Else 
 dbsTemp.MakeReplica strNewReplica, _ 
 "Replica of " & strReplicableDB, _ 
 intOptions 
 End If 
 
 dbsTemp.Close 
 
ErrorHandler: 
 Select Case Err 
 Case 0: 
 MakeAdditionalReplica = 0 
 Exit Function 
 Case Else: 
 MsgBox "Error " & Err & " : " & Error 
 MakeAdditionalReplica = Err 
 Exit Function 
 End Select 
 
End Function 
 
```

