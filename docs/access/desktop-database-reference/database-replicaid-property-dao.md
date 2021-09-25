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
ms.localizationpriority: medium
ms.openlocfilehash: 6e756f4037ff9c8708ac5df79061623c3dadba9a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59569139"
---
# <a name="databasereplicaid-property-dao"></a>Database.ReplicaID-Eigenschaft (DAO)


**Gilt für**: Access 2013, Office 2013


Gibt einen 16-Byte-Wert zurück, der ein Replikat einer Datenbank eindeutig kennzeichnet (nur Microsoft Access-Arbeitsbereiche).

## <a name="syntax"></a>Syntax

*Ausdruck* . Replicaid

*Ausdruck* Eine Variable, die ein **Database** -Objekt darstellt.

## <a name="remarks"></a>HinwBemerkungeneise

Der Rückgabewert ist ein **GUID**-Wert, der das Replikat oder den Designmaster eindeutig kennzeichnet.

Die Microsoft Access-Datenbank-Engine generiert diesen Wert automatisch, wenn Sie ein neues Replikat erstellen.

Die **ReplicaID**-Eigenschaft jedes Replikats (und der Designmaster) ist in der MSysReplicas-Systemtabelle gespeichert.

## <a name="example"></a>Beispiel

This example makes a replica from the Design Master of Northwind.mdb, and then returns the replica's **ReplicaID**, which is automatically created by the Microsoft Access database engine. (If you have not yet created a Design Master of Northwind, refer to the **Replicable** property, or change the name of the database in the code to an existing Design Master.)

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

