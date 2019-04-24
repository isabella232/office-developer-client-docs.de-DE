---
title: MaxRecords-Eigenschaft (ADO)
TOCTitle: MaxRecords property (ADO)
ms:assetid: 424b2d41-073a-3fbe-30aa-99fac94f9a81
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249195(v=office.15)
ms:contentKeyID: 48544475
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8ed643ca3b1341d7f933901e15c20c84acb025f5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32289721"
---
# <a name="maxrecords-property-ado"></a>MaxRecords-Eigenschaft (ADO)


**Gilt für**: Access 2013, Office 2013

Gibt die maximale Anzahl von Datensätzen an, die von einer Abfrage an ein [Recordset](recordset-object-ado.md) zurückgegeben werden.

## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte

Sets or returns a **Long** value that indicates the maximum number of records to return. Default is zero (no limit).

## <a name="remarks"></a>Bemerkungen

Use the **MaxRecords** property to limit the number of records that the provider returns from the data source. The default setting of this property is zero, which means the provider returns all requested records.

Die **MaxRecords**-Eigenschaft ist nicht schreibgeschützt, wenn das **Recordset**-Objekt geschlossen ist, und schreibgeschützt, wenn es geöffnet ist.

