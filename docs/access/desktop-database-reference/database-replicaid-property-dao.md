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
# <a name="databasereplicaid-property-dao"></a>Database.ReplicaID-Eigenschaft (DAO)


**Betrifft**: Access 2013, Office 2013


Gibt einen 16-Byte-Wert zurück, der ein Replikat einer Datenbank eindeutig kennzeichnet (nur Microsoft Access-Arbeitsbereiche).

## <a name="syntax"></a>Syntax

*Ausdruck* . ReplicaID

*Ausdruck* Eine Variable, die ein **Database** -Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

Der Rückgabewert ist ein **GUID**-Wert, der das Replikat oder den Designmaster eindeutig kennzeichnet.

Die Microsoft Access-Datenbank-Engine generiert diesen Wert automatisch, wenn Sie ein neues Replikat erstellen.

Die **ReplicaID**-Eigenschaft jedes Replikats (und der Designmaster) ist in der MSysReplicas-Systemtabelle gespeichert.

## <a name="example"></a>Beispiel

In diesem Beispiel wird ein Replikat des Designmasters von Northwind.mdb erstellt. Anschließend wird die ReplicaID-Eigenschaft des Replikats zurückgegeben, die automatisch von der Microsoft Access-Datenbank-Engine erstellt wird. (Wenn Sie noch keinen Designmaster von Northwind erstellt haben, lesen Sie unter der Replicable-Eigenschaft nach oder ändern Sie den Namen der Datenbank im Code in einen vorhandenen Designmaster.)

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

