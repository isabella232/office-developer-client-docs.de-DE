---
title: MaxRecords-Eigenschaft (ADO)
TOCTitle: MaxRecords property (ADO)
ms:assetid: 424b2d41-073a-3fbe-30aa-99fac94f9a81
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249195(v=office.15)
ms:contentKeyID: 48544475
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 9904e6b3f0b8db702cb1ccc6c45cc7f81d632238
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59552815"
---
# <a name="maxrecords-property-ado"></a>MaxRecords-Eigenschaft (ADO)


**Gilt für**: Access 2013, Office 2013

Gibt die maximale Anzahl von Datensätzen an, die von einer Abfrage an ein [Recordset](recordset-object-ado.md) zurückgegeben werden.

## <a name="settings-and-return-values"></a>Einstellungen- und Rückgabewerte

Sets or returns a **Long** value that indicates the maximum number of records to return. Default is zero (no limit).

## <a name="remarks"></a>HinwBemerkungeneise

Use the **MaxRecords** property to limit the number of records that the provider returns from the data source. The default setting of this property is zero, which means the provider returns all requested records.

Die **MaxRecords**-Eigenschaft ist nicht schreibgeschützt, wenn das **Recordset**-Objekt geschlossen ist, und schreibgeschützt, wenn es geöffnet ist.

