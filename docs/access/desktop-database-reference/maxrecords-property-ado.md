---
title: MaxRecords-Eigenschaft (ADO)
TOCTitle: MaxRecords Property (ADO)
ms:assetid: 424b2d41-073a-3fbe-30aa-99fac94f9a81
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249195(v=office.15)
ms:contentKeyID: 48544475
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d8753bf09655371042e97ead083c6849f1736b8b
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25474176"
---
# <a name="maxrecords-property-ado"></a>MaxRecords-Eigenschaft (ADO)


**Betrifft**: Access 2013 | Office 2013

Gibt die maximale Anzahl von Datensätzen an, die von einer Abfrage an ein [Recordset](recordset-object-ado.md) zurückgegeben werden.

## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte

Legt einen Long-Wert fest, der die maximale Anzahl von zurückgegebenen Datensätzen angibt, oder gibt den Wert zurück. Der Standardwert ist Null (kein Limit).

## <a name="remarks"></a>Hinweise

Verwenden Sie die **MaxRecords** -Eigenschaft zur Begrenzung der Anzahl von Datensätzen, die der Anbieter aus der Datenquelle zurückgibt. Die Standardeinstellung dieser Eigenschaft ist NULL und bedeutet, dass der Anbieter alle angeforderten Datensätze zurückgibt.

Die **MaxRecords** -Eigenschaft ist nicht schreibgeschützt, wenn das **Recordset** -Objekt geschlossen ist, und schreibgeschützt, wenn es geöffnet ist.

