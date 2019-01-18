---
title: Database.ReplicaID-Eigenschaft (DAO)
TOCTitle: ReplicaID Property
ms:assetid: cf2ca8a1-d13f-30e0-2ca1-dd32ac736c56
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834672(v=office.15)
ms:contentKeyID: 48547805
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053375
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 2ada9bf23a4b8fc34c5f9b4f24350fc6af91dc85
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28703930"
---
# <a name="databasereplicaid-property-dao"></a><span data-ttu-id="f56d6-102">Database.ReplicaID-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="f56d6-102">Database.ReplicaID property (DAO)</span></span>


<span data-ttu-id="f56d6-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f56d6-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="f56d6-104">Gibt einen 16-Byte-Wert zurück, der ein Replikat einer Datenbank eindeutig kennzeichnet (nur Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="f56d6-104">Returns a 16-byte value that uniquely identifies a database replica (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="f56d6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f56d6-105">Syntax</span></span>

<span data-ttu-id="f56d6-106">*Ausdruck* . ReplicaID</span><span class="sxs-lookup"><span data-stu-id="f56d6-106">*expression* .ReplicaID</span></span>

<span data-ttu-id="f56d6-107">*Ausdruck* Eine Variable, die ein **Database** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="f56d6-107">*expression* A variable that represents a **Database** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="f56d6-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f56d6-108">Remarks</span></span>

<span data-ttu-id="f56d6-109">Der Rückgabewert ist ein **GUID**-Wert, der das Replikat oder den Designmaster eindeutig kennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="f56d6-109">The return value is a **GUID** value that uniquely identifies the replica or Design Master.</span></span>

<span data-ttu-id="f56d6-110">Die Microsoft Access-Datenbank-Engine generiert diesen Wert automatisch, wenn Sie ein neues Replikat erstellen.</span><span class="sxs-lookup"><span data-stu-id="f56d6-110">The Microsoft Access database engine automatically generates this value when you create a new replica.</span></span>

<span data-ttu-id="f56d6-111">Die **ReplicaID**-Eigenschaft jedes Replikats (und der Designmaster) ist in der MSysReplicas-Systemtabelle gespeichert.</span><span class="sxs-lookup"><span data-stu-id="f56d6-111">The **ReplicaID** property of each replica (and the Design Master) is stored in the MSysReplicas system table.</span></span>

## <a name="example"></a><span data-ttu-id="f56d6-112">Beispiel</span><span class="sxs-lookup"><span data-stu-id="f56d6-112">Example</span></span>

<span data-ttu-id="f56d6-p101">In diesem Beispiel wird ein Replikat des Designmasters von Northwind.mdb erstellt. Anschließend wird die ReplicaID-Eigenschaft des Replikats zurückgegeben, die automatisch von der Microsoft Access-Datenbank-Engine erstellt wird. (Wenn Sie noch keinen Designmaster von Northwind erstellt haben, lesen Sie unter der Replicable-Eigenschaft nach oder ändern Sie den Namen der Datenbank im Code in einen vorhandenen Designmaster.)</span><span class="sxs-lookup"><span data-stu-id="f56d6-p101">This example makes a replica from the Design Master of Northwind.mdb, and then returns the replica's **ReplicaID**, which is automatically created by the Microsoft Access database engine. (If you have not yet created a Design Master of Northwind, refer to the **Replicable** property, or change the name of the database in the code to an existing Design Master.)</span></span>

```vb 
Sub MakeReplicaReplicaIDX() 
 
 Dim dbsNorthwind As Database 
 Dim prpReplicaID As Property 
 Dim dbsReplica As Database 
 
 Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 
 ' Makes a new replica. 
 dbsNorthwind.MakeReplica "Nwreplica2.mdb", _ 
 "second replica" 
 dbsNorthwind.Close 
 
 ' Opens the new replica to read its ReplicaID. 
 Set dbsReplica = OpenDatabase("Nwreplica2.mdb") 
 
 Debug.Print dbsReplica.ReplicaID 
 dbsReplica.Close 
 
End Sub 
 
```

