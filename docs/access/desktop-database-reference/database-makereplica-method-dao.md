---
title: Database.MakeReplica Method (DAO)
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
ms.openlocfilehash: c8274d441c246d7363ec5d5c603c3079da732c84
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25880803"
---
# <a name="databasemakereplica-method-dao"></a><span data-ttu-id="ae2c3-102">Database.MakeReplica Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="ae2c3-102">Database.MakeReplica Method (DAO)</span></span>

<span data-ttu-id="ae2c3-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ae2c3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ae2c3-104">Macht aus einem Datenbankreplikat ein neues Replikat (gilt nur für Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="ae2c3-104">Makes a new replica from another database replica (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="ae2c3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ae2c3-105">Syntax</span></span>

<span data-ttu-id="ae2c3-106">*Ausdruck* . MakeReplica (***Pfadname***, ***Beschreibung***, ***Optionen***)</span><span class="sxs-lookup"><span data-stu-id="ae2c3-106">*expression* .MakeReplica(***PathName***, ***Description***, ***Options***)</span></span>

<span data-ttu-id="ae2c3-107">*Ausdruck* Eine Variable, die ein **Database** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="ae2c3-107">*expression* A variable that represents a **Database** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="ae2c3-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="ae2c3-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ae2c3-109">Name</span><span class="sxs-lookup"><span data-stu-id="ae2c3-109">Name</span></span></p></th>
<th><p><span data-ttu-id="ae2c3-110">Erforderlich/Optional</span><span class="sxs-lookup"><span data-stu-id="ae2c3-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="ae2c3-111">Datentyp</span><span class="sxs-lookup"><span data-stu-id="ae2c3-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="ae2c3-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ae2c3-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ae2c3-113">Pfadname</span><span class="sxs-lookup"><span data-stu-id="ae2c3-113">PathName</span></span></p></td>
<td><p><span data-ttu-id="ae2c3-114">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="ae2c3-114">Required</span></span></p></td>
<td><p><span data-ttu-id="ae2c3-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="ae2c3-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="ae2c3-p101">Der Pfad- und Dateiname des neuen Replikats. Wenn replica ein vorhandener Dateiname ist, tritt ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="ae2c3-p101">The path and file name of the new replica. If replica is an existing file name, then an error occurs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae2c3-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ae2c3-118">Description</span></span></p></td>
<td><p><span data-ttu-id="ae2c3-119">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="ae2c3-119">Required</span></span></p></td>
<td><p><span data-ttu-id="ae2c3-120"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="ae2c3-120"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="ae2c3-121">Ein <strong>String</strong>-Wert, der das Replikat beschreibt, das Sie erstellen.</span><span class="sxs-lookup"><span data-stu-id="ae2c3-121">A <strong>String</strong> that describes the replica that you are creating</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae2c3-122">Options</span><span class="sxs-lookup"><span data-stu-id="ae2c3-122">Options</span></span></p></td>
<td><p><span data-ttu-id="ae2c3-123">Optional</span><span class="sxs-lookup"><span data-stu-id="ae2c3-123">Optional</span></span></p></td>
<td><p><span data-ttu-id="ae2c3-124"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="ae2c3-124"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="ae2c3-125">Eine <strong><a href="replicatypeenum-enumeration-dao.md">ReplicaTypeEnum</a></strong> -Konstante, die Eigenschaften des Replikats angibt, die Sie erstellen.</span><span class="sxs-lookup"><span data-stu-id="ae2c3-125">A <strong><a href="replicatypeenum-enumeration-dao.md">ReplicaTypeEnum</a></strong> constant that specifies characteristics of the replica you are creating.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="ae2c3-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ae2c3-126">Remarks</span></span>

<span data-ttu-id="ae2c3-127">Für ein neu erstelltes Teilreplikat werden sämtliche **[ReplicaFilter](tabledef-replicafilter-property-dao.md)** -Eigenschaften auf **False** festgelegt, was bedeutet, dass die Tabelle keine Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="ae2c3-127">A newly created partial replica will have all **[ReplicaFilter](tabledef-replicafilter-property-dao.md)** properties set to **False**, meaning that no data will be in the tables.</span></span>

## <a name="example"></a><span data-ttu-id="ae2c3-128">Beispiel</span><span class="sxs-lookup"><span data-stu-id="ae2c3-128">Example</span></span>

<span data-ttu-id="ae2c3-129">Diese Funktion verwendet die **MakeReplica** -Methode, um ein zusätzliches Replikat eines vorhandenen Designmasters zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="ae2c3-129">This function uses the **MakeReplica** method to create an additional replica of an existing Design Master.</span></span> <span data-ttu-id="ae2c3-130">Das IntOptions-Argument kann eine Kombination aus Konstanten **DbRepMakeReadOnly** und **DbRepMakePartial**sein, oder es kann 0 sein.</span><span class="sxs-lookup"><span data-stu-id="ae2c3-130">The intOptions argument can be a combination of the constants **dbRepMakeReadOnly** and **dbRepMakePartial**, or it can be 0.</span></span> <span data-ttu-id="ae2c3-131">Beispielsweise zum Erstellen eines Teilreplikats schreibgeschützt sollten, übergeben Sie den Wert **DbRepMakeReadOnly** + **DbRepMakePartial** als Wert des IntOptions.</span><span class="sxs-lookup"><span data-stu-id="ae2c3-131">For example, to create a read-only partial replica, you should pass the value **dbRepMakeReadOnly** + **dbRepMakePartial** as the value of intOptions.</span></span>

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

