---
title: Relation.PartialReplica Property (DAO)
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
ms.openlocfilehash: 52ad71b0b9410a20fe848fb1428f3cdc83a966a8
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870821"
---
# <a name="relationpartialreplica-property-dao"></a><span data-ttu-id="0eb3b-102">Relation.PartialReplica Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="0eb3b-102">Relation.PartialReplica Property (DAO)</span></span>


<span data-ttu-id="0eb3b-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0eb3b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0eb3b-p101">Legt einen Wert für ein **Relation**-Objekt fest, der angibt, ob die Beziehung berücksichtigt werden soll, wenn ein Teilreplikat von einem vollständigen Replikat aufgefüllt wird, oder gibt den betreffenden Wert zurück (nur Microsoft Access-Datenbanken). **Boolean**-Wert mit Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="0eb3b-p101">Sets or returns a value on a **Relation** object indicating whether that relation should be considered when populating a partial replica from a full replica. (Microsoft Access database engine databases only). Read/write **Boolean**.</span></span>

## <a name="syntax"></a><span data-ttu-id="0eb3b-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="0eb3b-107">Syntax</span></span>

<span data-ttu-id="0eb3b-108">*Ausdruck* . PartialReplica</span><span class="sxs-lookup"><span data-stu-id="0eb3b-108">*expression* .PartialReplica</span></span>

<span data-ttu-id="0eb3b-109">*Ausdruck* Ein Ausdruck, der ein **Relation** -Objekt zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="0eb3b-109">*expression* An expression that returns a **Relation** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="0eb3b-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0eb3b-110">Remarks</span></span>

<span data-ttu-id="0eb3b-111">Die Einstellung bzw. der Rückgabewert ist ein boolescher Datentyp, der **True** ist, wenn die Beziehung während der Synchronisation erzwungen werden soll.</span><span class="sxs-lookup"><span data-stu-id="0eb3b-111">The setting or return value is a Boolean data type that is **True** when the relation should be enforced during synchronization.</span></span>

<span data-ttu-id="0eb3b-p102">Diese Eigenschaft gestattet es Ihnen, Daten vom vollständigen Replikat basierend auf Beziehungen zwischen Tabellen auf das Teilreplikat zu replizieren. Sie können die PartialReplica-Eigenschaft verwenden, wenn die Einstellung der ReplicaFilter-Eigenschaft alleine nicht ausreicht, um festzulegen, welche Daten auf das Teilreplikat repliziert werden sollen. Beispiel: Sie haben eine Datenbank, in der die Tabelle Customers eine 1:n-Beziehung zur Tabelle Orders hat. Sie möchten ein Teilreplikat konfigurieren, bei der nur Bestellungen von Kunden aus der Region Kalifornien (CA) repliziert werden (anstelle aller Bestellungen). Es ist nicht möglich, die ReplicaFilter-Eigenschaft für die Tabelle Orders auf Region = 'CA' festzulegen, da sich das Feld Region in der Tabelle Customers befindet und nicht in der Tabelle Orders.</span><span class="sxs-lookup"><span data-stu-id="0eb3b-p102">This property enables you to replicate data from the full replica to the partial replica based on relationships between tables. You can use the **PartialReplica** property when setting the **ReplicaFilter** property alone can't adequately specify what data should be replicated to the partial. For example, suppose you have a database in which the Customers table has a one-to-many relationship with the Orders table, and you want to configure a partial replica that only replicates orders from customers in the California region (instead of all orders). It is not possible to set the **ReplicaFilter** property on the Orders table to Region = 'CA' because the Region field is in the Customers table, not the Orders table.</span></span>

<span data-ttu-id="0eb3b-p103">Um alle Bestellungen aus der Region Kalifornien (CA) zu replizieren, müssen Sie angeben, dass die Beziehung zwischen den Tabellen Orders und Customers während der Replikation aktiv sein soll. Nach der Erstellung eines Teilreplikats wird es mit den folgenden Schritten mit allen Bestellungen aus der Region Kalifornien aufgefüllt:</span><span class="sxs-lookup"><span data-stu-id="0eb3b-p103">To replicate all orders from the California region, you must indicate that the relation between the Orders and Customers tables will be active during replication. Once you've created a partial replica, the following steps will populate it with all orders from the California region:</span></span>

1.  <span data-ttu-id="0eb3b-118">Legen Sie die **ReplicaFilter** -Eigenschaft für das Kunden **TableDef** -Objekt zum "Region = 'CA'".</span><span class="sxs-lookup"><span data-stu-id="0eb3b-118">Set the **ReplicaFilter** property on the Customers **TableDef** object to "Region = 'CA'".</span></span>

2.  <span data-ttu-id="0eb3b-119">Legen Sie den Wert der PartialReplica-Eigenschaft für das Relation-Objekt entsprechend der Beziehung zwischen Orders und Customers auf True fest.</span><span class="sxs-lookup"><span data-stu-id="0eb3b-119">Set the value of the **PartialReplica** property to **True** on the **Relation** object corresponding to the relationship between Orders and Customers.</span></span>

3.  <span data-ttu-id="0eb3b-120">Rufen Sie die **PopulatePartial**-Methode auf.</span><span class="sxs-lookup"><span data-stu-id="0eb3b-120">Invoke the **PopulatePartial** method.</span></span>
    

> [!NOTE]
> <P><span data-ttu-id="0eb3b-p104">Achten Sie beim Festlegen eines Replikatfilters oder einer Replikatbeziehung darauf, dass Datensätze im Teilreplikat, die die Einschränkungskriterien nicht erfüllen, aus dem Teilreplikat entfernt werden, jedoch nicht aus dem vollständigen Replikat. Wenn Sie z. B. die ReplicaFilter-Eigenschaft des TableDef-Objekts der Tabelle Customers im Teilreplikat auf "Region = 'CA'" festlegen und dann die Datenbank neu auffüllen, werden alle Datensätze für Kunden in Kalifornien eingefügt bzw. aktualisiert. Wenn Sie dann die ReplicaFilter-Eigenschaft auf "Region = 'FL'" (Florida) festlegen und die Datenbank neu auffüllen, werden alle Datensätze der Region Kalifornien aus dem Teilreplikat  entfernt. Alle Datensätze der Kunden aus Florida aus dem vollständigen Replikat werden eingefügt. Aus dem vollständigen Replikat werden keine Datensätze gelöscht. Vor dem Festlegen der ReplicaFilter- oder PartialReplica-Eigenschaft sollte das Teilreplikat, in dem Sie diese Eigenschaften festlegen, mit dem vollständigen Replikat synchronisiert werden. Damit wird sichergestellt, dass ausstehende Änderungen im Teilreplikat in das vollständige Replikat aufgenommen werden, bevor Datensätze aus dem Teilreplikat entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="0eb3b-p104">When you set a replica filter or replica relation, be aware that records in the partial replica that don't satisfy the restriction criteria will be removed from the partial replica, but not from the full replica. For example, suppose you set the <STRONG>ReplicaFilter</STRONG> property on the Customers <STRONG>TableDef</STRONG> in the partial replica to "Region = 'CA'" and you then repopulate the database. This will insert or update all records for California-based customers. If you then reset the <STRONG>ReplicaFilter</STRONG> property to "Region = 'FL'" and repopulate the database, all California region records in the partial replica will be removed, and all records from Florida-based customers will be inserted from the full replica. No records in the full replica will be deleted. Before setting either the <STRONG>ReplicaFilter</STRONG> or <STRONG>PartialReplica</STRONG> property, it's a good idea to synchronize the partial replica in which you are setting these properties with the full replica. This will ensure that pending changes in the partial replica will be merged into the full replica before any records are removed in the partial replica.</span></span></P>


