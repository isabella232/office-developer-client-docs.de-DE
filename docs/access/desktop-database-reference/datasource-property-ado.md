---
title: DataSource-Eigenschaft (ADO)
TOCTitle: DataSource property (ADO)
ms:assetid: 5c5d6c9b-b7d4-45a5-0f6a-a5580a74361e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249325(v=office.15)
ms:contentKeyID: 48545087
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0dec30715d1eb4e31d7490db4cedd015ecf3c040
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28700031"
---
# <a name="datasource-property-ado"></a>DataSource-Eigenschaft (ADO)


**Betrifft**: Access 2013, Office 2013

Gibt ein Objekt an, das als [Recordset](recordset-object-ado.md)-Objekt darzustellende Daten enthält.

## <a name="remarks"></a>Hinweise

Mithilfe dieser Eigenschaft werden datengebundene Steuerelemente mit der Datenumgebung erstellt. Die Datenumgebung verwaltet Datensammlungen (Datenquellen), die benannte Objekte (*Datenelemente*) enthalten und als **Recordset**-Objekt dargestellt werden.**

Die Eigenschaften [DataMember](datamember-property-ado.md) und **DataSource** müssen in Kombination verwendet werden.

Das Objekt, auf das verwiesen wird, muss die **IDataSource** -Schnittstelle implementieren und eine **IRowset** -Schnittstelle enthalten.

**Verwendung**

```vb
    Dim rs as New ADODB.Recordset
    rs.DataMember = "Command"     'Name of the rowset to bind to
    Set rs.DataSource = myDE      'Name of the object containing an IRowset
```
