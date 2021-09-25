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
ms.localizationpriority: medium
ms.openlocfilehash: c674003234bb4b5e961651e85b87342ad49486e7
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59564932"
---
# <a name="relationpartialreplica-property-dao"></a>Relation.PartialReplica-Eigenschaft (DAO)

**Gilt für**: Access 2013, Office 2013

Legt einen Wert für ein **Relation**-Objekt fest, der angibt, ob die Beziehung berücksichtigt werden soll, wenn ein Teilreplikat von einem vollständigen Replikat aufgefüllt wird, oder gibt den betreffenden Wert zurück (nur Microsoft Access-Datenbanken). **Boolean**-Wert mit Lese-/Schreibzugriff.

## <a name="syntax"></a>Syntax

*Ausdruck* . PartialReplica

*Ausdruck* Ein Ausdruck, der ein **Relation -Objekt** zurückgibt.

## <a name="remarks"></a>HinwBemerkungeneise

Die Einstellung bzw. der Rückgabewert ist ein boolescher Datentyp, der **True** ist, wenn die Beziehung während der Synchronisation erzwungen werden soll.

This property enables you to replicate data from the full replica to the partial replica based on relationships between tables. You can use the **PartialReplica** property when setting the **ReplicaFilter** property alone can't adequately specify what data should be replicated to the partial. For example, suppose you have a database in which the Customers table has a one-to-many relationship with the Orders table, and you want to configure a partial replica that only replicates orders from customers in the California region (instead of all orders). Es ist nicht möglich, die **ReplicaFilter-Eigenschaft** in der Tabelle Bestellungen auf Region = 'CA' festzulegen, da sich das Feld Region in der Tabelle "Customers" befindet, nicht in der Tabelle "Orders".

To replicate all orders from the California region, you must indicate that the relation between the Orders and Customers tables will be active during replication. Once you've created a partial replica, the following steps will populate it with all orders from the California region:

1.  Legen Sie die **ReplicaFilter-Eigenschaft** für das Customers **TableDef-Objekt** auf "Region = 'CA'" fest.

2.  Set the value of the **PartialReplica** property to **True** on the **Relation** object corresponding to the relationship between Orders and Customers.

3.  Rufen Sie die **PopulatePartial**-Methode auf.
    

> [!NOTE]
> When you set a replica filter or replica relation, be aware that records in the partial replica that don't satisfy the restriction criteria will be removed from the partial replica, but not from the full replica. Angenommen, Sie legen die **ReplicaFilter-Eigenschaft** für "Customers **TableDef"** im Teilreplikat auf "Region = 'CA'" fest, und führen sie dann ein Repository für die Datenbank aus. This will insert or update all records for California-based customers. 
> 
> Wenn Sie dann die **ReplicaFilter-Eigenschaft** auf "Region = 'FL'" zurücksetzen und die Datenbank erneut auffüllen, werden alle Einträge aus der Region Kalifornien im Teilreplikat entfernt, und alle Datensätze von mandantenbasierten Kunden werden aus dem vollständigen Replikat eingefügt. No records in the full replica will be deleted. 
>
> Before setting either the **ReplicaFilter** or **PartialReplica** property, it's a good idea to synchronize the partial replica in which you are setting these properties with the full replica. This will ensure that pending changes in the partial replica will be merged into the full replica before any records are removed in the partial replica.


