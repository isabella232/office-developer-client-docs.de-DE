---
title: DataSource-Eigenschaft (ADO)
TOCTitle: DataSource Property (ADO)
ms:assetid: 5c5d6c9b-b7d4-45a5-0f6a-a5580a74361e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249325(v=office.15)
ms:contentKeyID: 48545087
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: fb1c65adcc6e7c513feeea1a506fc222c6b13e19
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25475857"
---
# <a name="datasource-property-ado"></a>DataSource-Eigenschaft (ADO)


**Betrifft**: Access 2013 | Office 2013

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
