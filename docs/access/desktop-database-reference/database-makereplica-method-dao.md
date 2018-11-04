---
title: Database.MakeReplica-Methode (DAO)
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
ms.openlocfilehash: 632bf0af35dd49951d58ba126b6e03678a1a12db
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2018
ms.locfileid: "25950251"
---
# <a name="databasemakereplica-method-dao"></a><span data-ttu-id="0489f-102">Database.MakeReplica-Methode (DAO)</span><span class="sxs-lookup"><span data-stu-id="0489f-102">Database.MakeReplica method (DAO)</span></span>

<span data-ttu-id="0489f-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0489f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0489f-104">Macht aus einem Datenbankreplikat ein neues Replikat (gilt nur für Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="0489f-104">Makes a new replica from another database replica (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="0489f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0489f-105">Syntax</span></span>

<span data-ttu-id="0489f-106">*Ausdruck* . MakeReplica (***Pfadname***, ***Beschreibung***, ***Optionen***)</span><span class="sxs-lookup"><span data-stu-id="0489f-106">*expression* .MakeReplica(***PathName***, ***Description***, ***Options***)</span></span>

<span data-ttu-id="0489f-107">*Ausdruck* Eine Variable, die ein **Database** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="0489f-107">*expression* A variable that represents a **Database** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="0489f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="0489f-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0489f-109">Name</span><span class="sxs-lookup"><span data-stu-id="0489f-109">Name</span></span></p></th>
<th><p><span data-ttu-id="0489f-110">Erforderlich/Optional</span><span class="sxs-lookup"><span data-stu-id="0489f-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="0489f-111">Datentyp</span><span class="sxs-lookup"><span data-stu-id="0489f-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="0489f-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0489f-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0489f-113"><em>Pfadname</em></span><span class="sxs-lookup"><span data-stu-id="0489f-113"><em>PathName</em></span></span></p></td>
<td><p><span data-ttu-id="0489f-114">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="0489f-114">Required</span></span></p></td>
<td><p><span data-ttu-id="0489f-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="0489f-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="0489f-p101">Der Pfad- und Dateiname des neuen Replikats. Wenn replica ein vorhandener Dateiname ist, tritt ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="0489f-p101">The path and file name of the new replica. If replica is an existing file name, then an error occurs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0489f-118"><em>Description</em></span><span class="sxs-lookup"><span data-stu-id="0489f-118"><em>Description</em></span></span></p></td>
<td><p><span data-ttu-id="0489f-119">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="0489f-119">Required</span></span></p></td>
<td><p><span data-ttu-id="0489f-120"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="0489f-120"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="0489f-121">Ein <strong>String</strong>-Wert, der das Replikat beschreibt, das Sie erstellen.</span><span class="sxs-lookup"><span data-stu-id="0489f-121">A <strong>String</strong> that describes the replica that you are creating</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0489f-122"><em>Options</em></span><span class="sxs-lookup"><span data-stu-id="0489f-122"><em>Options</em></span></span></p></td>
<td><p><span data-ttu-id="0489f-123">Optional</span><span class="sxs-lookup"><span data-stu-id="0489f-123">Optional</span></span></p></td>
<td><p><span data-ttu-id="0489f-124"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="0489f-124"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="0489f-125">Eine <strong><a href="replicatypeenum-enumeration-dao.md">ReplicaTypeEnum</a></strong> -Konstante, die Eigenschaften des Replikats angibt, die Sie erstellen.</span><span class="sxs-lookup"><span data-stu-id="0489f-125">A <strong><a href="replicatypeenum-enumeration-dao.md">ReplicaTypeEnum</a></strong> constant that specifies characteristics of the replica you are creating.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="0489f-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0489f-126">Remarks</span></span>

<span data-ttu-id="0489f-127">Für ein neu erstelltes Teilreplikat werden sämtliche **[ReplicaFilter](tabledef-replicafilter-property-dao.md)** -Eigenschaften auf **False** festgelegt, was bedeutet, dass die Tabelle keine Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="0489f-127">A newly created partial replica will have all **[ReplicaFilter](tabledef-replicafilter-property-dao.md)** properties set to **False**, meaning that no data will be in the tables.</span></span>

## <a name="example"></a><span data-ttu-id="0489f-128">Beispiel</span><span class="sxs-lookup"><span data-stu-id="0489f-128">Example</span></span>

<span data-ttu-id="0489f-129">Diese Funktion verwendet die **MakeReplica** -Methode, um ein zusätzliches Replikat eines vorhandenen Designmasters zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="0489f-129">This function uses the **MakeReplica** method to create an additional replica of an existing Design Master.</span></span> <span data-ttu-id="0489f-130">Das IntOptions-Argument kann eine Kombination aus Konstanten **DbRepMakeReadOnly** und **DbRepMakePartial**sein, oder es kann 0 sein.</span><span class="sxs-lookup"><span data-stu-id="0489f-130">The intOptions argument can be a combination of the constants **dbRepMakeReadOnly** and **dbRepMakePartial**, or it can be 0.</span></span> <span data-ttu-id="0489f-131">Beispielsweise zum Erstellen eines Teilreplikats schreibgeschützt sollten, übergeben Sie den Wert **DbRepMakeReadOnly** + **DbRepMakePartial** als Wert des IntOptions.</span><span class="sxs-lookup"><span data-stu-id="0489f-131">For example, to create a read-only partial replica, you should pass the value **dbRepMakeReadOnly** + **dbRepMakePartial** as the value of intOptions.</span></span>

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

