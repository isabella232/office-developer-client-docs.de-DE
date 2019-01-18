---
title: Relation.PartialReplica-Eigenschaft (DAO)
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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28698407"
---
# <a name="relationpartialreplica-property-dao"></a><span data-ttu-id="eba48-102">Relation.PartialReplica-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="eba48-102">Relation.PartialReplica property (DAO)</span></span>

<span data-ttu-id="eba48-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="eba48-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="eba48-p101">Legt einen Wert für ein **Relation**-Objekt fest, der angibt, ob die Beziehung berücksichtigt werden soll, wenn ein Teilreplikat von einem vollständigen Replikat aufgefüllt wird, oder gibt den betreffenden Wert zurück (nur Microsoft Access-Datenbanken). **Boolean**-Wert mit Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="eba48-p101">Sets or returns a value on a **Relation** object indicating whether that relation should be considered when populating a partial replica from a full replica. (Microsoft Access database engine databases only). Read/write **Boolean**.</span></span>

## <a name="syntax"></a><span data-ttu-id="eba48-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="eba48-107">Syntax</span></span>

<span data-ttu-id="eba48-108">*Ausdruck* . PartialReplica</span><span class="sxs-lookup"><span data-stu-id="eba48-108">*expression* .PartialReplica</span></span>

<span data-ttu-id="eba48-109">*Ausdruck* Ein Ausdruck, der ein **Relation** -Objekt zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="eba48-109">*expression* An expression that returns a **Relation** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="eba48-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="eba48-110">Remarks</span></span>

<span data-ttu-id="eba48-111">Die Einstellung bzw. der Rückgabewert ist ein boolescher Datentyp, der **True** ist, wenn die Beziehung während der Synchronisation erzwungen werden soll.</span><span class="sxs-lookup"><span data-stu-id="eba48-111">The setting or return value is a Boolean data type that is **True** when the relation should be enforced during synchronization.</span></span>

<span data-ttu-id="eba48-p102">Diese Eigenschaft gestattet es Ihnen, Daten vom vollständigen Replikat basierend auf Beziehungen zwischen Tabellen auf das Teilreplikat zu replizieren. Sie können die PartialReplica-Eigenschaft verwenden, wenn die Einstellung der ReplicaFilter-Eigenschaft alleine nicht ausreicht, um festzulegen, welche Daten auf das Teilreplikat repliziert werden sollen. Beispiel: Sie haben eine Datenbank, in der die Tabelle Customers eine 1:n-Beziehung zur Tabelle Orders hat. Sie möchten ein Teilreplikat konfigurieren, bei der nur Bestellungen von Kunden aus der Region Kalifornien (CA) repliziert werden (anstelle aller Bestellungen). Es ist nicht möglich, die ReplicaFilter-Eigenschaft für die Tabelle Orders auf Region = 'CA' festzulegen, da sich das Feld Region in der Tabelle Customers befindet und nicht in der Tabelle Orders.</span><span class="sxs-lookup"><span data-stu-id="eba48-p102">This property enables you to replicate data from the full replica to the partial replica based on relationships between tables. You can use the **PartialReplica** property when setting the **ReplicaFilter** property alone can't adequately specify what data should be replicated to the partial. For example, suppose you have a database in which the Customers table has a one-to-many relationship with the Orders table, and you want to configure a partial replica that only replicates orders from customers in the California region (instead of all orders). It is not possible to set the **ReplicaFilter** property on the Orders table to Region = 'CA' because the Region field is in the Customers table, not the Orders table.</span></span>

<span data-ttu-id="eba48-p103">Um alle Bestellungen aus der Region Kalifornien (CA) zu replizieren, müssen Sie angeben, dass die Beziehung zwischen den Tabellen Orders und Customers während der Replikation aktiv sein soll. Nach der Erstellung eines Teilreplikats wird es mit den folgenden Schritten mit allen Bestellungen aus der Region Kalifornien aufgefüllt:</span><span class="sxs-lookup"><span data-stu-id="eba48-p103">To replicate all orders from the California region, you must indicate that the relation between the Orders and Customers tables will be active during replication. Once you've created a partial replica, the following steps will populate it with all orders from the California region:</span></span>

1.  <span data-ttu-id="eba48-118">Legen Sie die **ReplicaFilter** -Eigenschaft für das Kunden **TableDef** -Objekt zum "Region = 'CA'".</span><span class="sxs-lookup"><span data-stu-id="eba48-118">Set the **ReplicaFilter** property on the Customers **TableDef** object to "Region = 'CA'".</span></span>

2.  <span data-ttu-id="eba48-119">Legen Sie den Wert der PartialReplica-Eigenschaft für das Relation-Objekt entsprechend der Beziehung zwischen Orders und Customers auf True fest.</span><span class="sxs-lookup"><span data-stu-id="eba48-119">Set the value of the **PartialReplica** property to **True** on the **Relation** object corresponding to the relationship between Orders and Customers.</span></span>

3.  <span data-ttu-id="eba48-120">Rufen Sie die **PopulatePartial**-Methode auf.</span><span class="sxs-lookup"><span data-stu-id="eba48-120">Invoke the **PopulatePartial** method.</span></span>
    

> [!NOTE]
> <span data-ttu-id="eba48-121">Wenn Sie einen Replikatfilter oder Replikat Relation festlegen, achten Sie darauf, dass Datensätze aus dem Teilreplikat, die die Einschränkungskriterien erfüllen, nicht aus dem Teilreplikat, aber nicht aus dem vollständigen Replikat entfernt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="eba48-121">When you set a replica filter or replica relation, be aware that records in the partial replica that don't satisfy the restriction criteria will be removed from the partial replica, but not from the full replica.</span></span> <span data-ttu-id="eba48-122">Angenommen, Sie die **ReplicaFilter** -Eigenschaft festlegen, auf die Kunden **TableDef** in dem Teilreplikat zu "Region = 'CA'" und Sie dann erneut die Datenbank aufzufüllen.</span><span class="sxs-lookup"><span data-stu-id="eba48-122">For example, suppose you set the **ReplicaFilter** property on the Customers **TableDef** in the partial replica to "Region = 'CA'" and you then repopulate the database.</span></span> <span data-ttu-id="eba48-123">Dies wird einfügen oder aktualisieren alle Datensätze für Kunden-basierte Kalifornien (CA).</span><span class="sxs-lookup"><span data-stu-id="eba48-123">This will insert or update all records for California-based customers.</span></span> 
> 
> <span data-ttu-id="eba48-124">Wenn Sie dann die **ReplicaFilter** -Eigenschaft zum Zurücksetzen "Region = 'FL'" und die Datenbank wieder auffüllen, alle Kalifornien (CA) Region Datensätze aus dem Teilreplikat entfernt werden und alle Datensätze aus Florida-basierte Kunden aus dem vollständigen Replikat eingefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="eba48-124">If you then reset the **ReplicaFilter** property to "Region = 'FL'" and repopulate the database, all California region records in the partial replica will be removed, and all records from Florida-based customers will be inserted from the full replica.</span></span> <span data-ttu-id="eba48-125">Es werden keine Datensätze aus dem vollständigen Replikat gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="eba48-125">No records in the full replica will be deleted.</span></span> 
>
> <span data-ttu-id="eba48-126">Bevor Sie die **ReplicaFilter** - oder **PartialReplica** -Eigenschaft festlegen, ist es ratsam, synchronisieren das Teilreplikat, in dem Sie diese Eigenschaften mit dem vollständigen Replikat festlegen.</span><span class="sxs-lookup"><span data-stu-id="eba48-126">Before setting either the **ReplicaFilter** or **PartialReplica** property, it's a good idea to synchronize the partial replica in which you are setting these properties with the full replica.</span></span> <span data-ttu-id="eba48-127">Dadurch wird sichergestellt, dass mit dem vollständigen Replikat ausstehenden Änderungen aus dem Teilreplikat zusammengeführt wird, bevor alle Datensätze aus dem Teilreplikat entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="eba48-127">This will ensure that pending changes in the partial replica will be merged into the full replica before any records are removed in the partial replica.</span></span>


