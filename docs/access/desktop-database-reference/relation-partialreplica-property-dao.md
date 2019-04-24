---
title: Relation. PartialReplica-Eigenschaft (DAO)
TOCTitle: PartialReplica Property
ms:assetid: 3cb15639-371e-06e3-e2ba-30466ce09a72
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192692(v=office.15)
ms:contentKeyID: 48544324
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053557
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: fef48902b806f13947ae4b81728af4c5704c2b8e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307014"
---
# <a name="relationpartialreplica-property-dao"></a><span data-ttu-id="ed3fb-102">Relation. PartialReplica-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="ed3fb-102">Relation.PartialReplica property (DAO)</span></span>

<span data-ttu-id="ed3fb-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ed3fb-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ed3fb-p101">Legt einen Wert für ein **Relation**-Objekt fest, der angibt, ob die Beziehung berücksichtigt werden soll, wenn ein Teilreplikat von einem vollständigen Replikat aufgefüllt wird, oder gibt den betreffenden Wert zurück (nur Microsoft Access-Datenbanken). **Boolean**-Wert mit Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="ed3fb-p101">Sets or returns a value on a **Relation** object indicating whether that relation should be considered when populating a partial replica from a full replica. (Microsoft Access database engine databases only). Read/write **Boolean**.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed3fb-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="ed3fb-107">Syntax</span></span>

<span data-ttu-id="ed3fb-108">*Ausdruck* . PartialReplica</span><span class="sxs-lookup"><span data-stu-id="ed3fb-108">*expression* .PartialReplica</span></span>

<span data-ttu-id="ed3fb-109">*Ausdruck* Ein Ausdruck, der ein **Relation** -Objekt zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="ed3fb-109">*expression* An expression that returns a **Relation** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="ed3fb-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ed3fb-110">Remarks</span></span>

<span data-ttu-id="ed3fb-111">Die Einstellung bzw. der Rückgabewert ist ein boolescher Datentyp, der **True** ist, wenn die Beziehung während der Synchronisation erzwungen werden soll.</span><span class="sxs-lookup"><span data-stu-id="ed3fb-111">The setting or return value is a Boolean data type that is **True** when the relation should be enforced during synchronization.</span></span>

<span data-ttu-id="ed3fb-112">This property enables you to replicate data from the full replica to the partial replica based on relationships between tables.</span><span class="sxs-lookup"><span data-stu-id="ed3fb-112">This property enables you to replicate data from the full replica to the partial replica based on relationships between tables.</span></span> <span data-ttu-id="ed3fb-113">You can use the **PartialReplica** property when setting the **ReplicaFilter** property alone can't adequately specify what data should be replicated to the partial.</span><span class="sxs-lookup"><span data-stu-id="ed3fb-113">You can use the **PartialReplica** property when setting the **ReplicaFilter** property alone can't adequately specify what data should be replicated to the partial.</span></span> <span data-ttu-id="ed3fb-114">For example, suppose you have a database in which the Customers table has a one-to-many relationship with the Orders table, and you want to configure a partial replica that only replicates orders from customers in the California region (instead of all orders).</span><span class="sxs-lookup"><span data-stu-id="ed3fb-114">For example, suppose you have a database in which the Customers table has a one-to-many relationship with the Orders table, and you want to configure a partial replica that only replicates orders from customers in the California region (instead of all orders).</span></span> <span data-ttu-id="ed3fb-115">Die **ReplicaFilter** -Eigenschaft der Orders-Tabelle kann nicht auf Region = ' ca ' festgelegt werden, da sich das Feld Region in der Tabelle Customers befindet, nicht in der Tabelle Bestellungen.</span><span class="sxs-lookup"><span data-stu-id="ed3fb-115">It is not possible to set the **ReplicaFilter** property on the Orders table to Region = 'CA' because the Region field is in the Customers table, not the Orders table.</span></span>

<span data-ttu-id="ed3fb-p103">To replicate all orders from the California region, you must indicate that the relation between the Orders and Customers tables will be active during replication. Once you've created a partial replica, the following steps will populate it with all orders from the California region:</span><span class="sxs-lookup"><span data-stu-id="ed3fb-p103">To replicate all orders from the California region, you must indicate that the relation between the Orders and Customers tables will be active during replication. Once you've created a partial replica, the following steps will populate it with all orders from the California region:</span></span>

1.  <span data-ttu-id="ed3fb-118">Legen Sie die **ReplicaFilter** -Eigenschaft des **TableDef** -Objekts Customers auf "Region = ' ca '" fest.</span><span class="sxs-lookup"><span data-stu-id="ed3fb-118">Set the **ReplicaFilter** property on the Customers **TableDef** object to "Region = 'CA'".</span></span>

2.  <span data-ttu-id="ed3fb-119">Set the value of the **PartialReplica** property to **True** on the **Relation** object corresponding to the relationship between Orders and Customers.</span><span class="sxs-lookup"><span data-stu-id="ed3fb-119">Set the value of the **PartialReplica** property to **True** on the **Relation** object corresponding to the relationship between Orders and Customers.</span></span>

3.  <span data-ttu-id="ed3fb-120">Rufen Sie die **PopulatePartial**-Methode auf.</span><span class="sxs-lookup"><span data-stu-id="ed3fb-120">Invoke the **PopulatePartial** method.</span></span>
    

> [!NOTE]
> <span data-ttu-id="ed3fb-121">When you set a replica filter or replica relation, be aware that records in the partial replica that don't satisfy the restriction criteria will be removed from the partial replica, but not from the full replica.</span><span class="sxs-lookup"><span data-stu-id="ed3fb-121">When you set a replica filter or replica relation, be aware that records in the partial replica that don't satisfy the restriction criteria will be removed from the partial replica, but not from the full replica.</span></span> <span data-ttu-id="ed3fb-122">Nehmen Sie beispielsweise an, dass Sie die **ReplicaFilter** -Eigenschaft im **TableDef** Customers im Teilreplikat auf "Region = ' ca '" festlegen und dann die Datenbank erneut auffüllen.</span><span class="sxs-lookup"><span data-stu-id="ed3fb-122">For example, suppose you set the **ReplicaFilter** property on the Customers **TableDef** in the partial replica to "Region = 'CA'" and you then repopulate the database.</span></span> <span data-ttu-id="ed3fb-123">This will insert or update all records for California-based customers.</span><span class="sxs-lookup"><span data-stu-id="ed3fb-123">This will insert or update all records for California-based customers.</span></span> 
> 
> <span data-ttu-id="ed3fb-124">Wenn Sie die **ReplicaFilter** -Eigenschaft dann auf "Region = ' FL '" zurücksetzen und die Datenbank erneut auffüllen, werden alle Datensätze von California Region im Teilreplikat entfernt, und alle Datensätze aus Florida-basierten Kunden werden aus dem vollständigen Replikat eingefügt.</span><span class="sxs-lookup"><span data-stu-id="ed3fb-124">If you then reset the **ReplicaFilter** property to "Region = 'FL'" and repopulate the database, all California region records in the partial replica will be removed, and all records from Florida-based customers will be inserted from the full replica.</span></span> <span data-ttu-id="ed3fb-125">No records in the full replica will be deleted.</span><span class="sxs-lookup"><span data-stu-id="ed3fb-125">No records in the full replica will be deleted.</span></span> 
>
> <span data-ttu-id="ed3fb-126">Before setting either the **ReplicaFilter** or **PartialReplica** property, it's a good idea to synchronize the partial replica in which you are setting these properties with the full replica.</span><span class="sxs-lookup"><span data-stu-id="ed3fb-126">Before setting either the **ReplicaFilter** or **PartialReplica** property, it's a good idea to synchronize the partial replica in which you are setting these properties with the full replica.</span></span> <span data-ttu-id="ed3fb-127">This will ensure that pending changes in the partial replica will be merged into the full replica before any records are removed in the partial replica.</span><span class="sxs-lookup"><span data-stu-id="ed3fb-127">This will ensure that pending changes in the partial replica will be merged into the full replica before any records are removed in the partial replica.</span></span>


