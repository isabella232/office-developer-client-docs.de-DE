---
title: CursorLocation-Eigenschaft (ADO)
TOCTitle: CursorLocation property (ADO)
ms:assetid: 8a048bd4-ae25-a555-1c07-14364b7e6560
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249606(v=office.15)
ms:contentKeyID: 48546182
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 874662585292b9d9a9b2bc53f5b6fe5178e3517b
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/07/2018
ms.locfileid: "26025847"
---
# <a name="cursorlocation-property-ado"></a>CursorLocation-Eigenschaft (ADO)


**Betrifft**: Access 2013, Office 2013

Gibt die Position des Cursordiensts an.

## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte

Mit dieser Eigenschaft wird ein Wert vom Datentyp **Long** festgelegt oder zurückgegeben, für den einer der [CursorLocationEnum](cursorlocationenum.md)-Werte festgelegt werden kann.

## <a name="remarks"></a>Hinweise

Diese Eigenschaft ermöglicht es Ihnen, zwischen verschiedenen Cursorbibliotheken auszuwählen, auf die der Anbieter zugreifen kann. In der Regel können Sie wählen zwischen einer clientseitigen Cursorbibliothek und einer Cursorbibliothek auf dem Server.

Diese Eigenschaftseinstellung wirkt sich nur auf Verbindungen aus, die nach dem Festlegen der Eigenschaft eingerichtet wurden. Das Ändern der **CursorLocation** -Eigenschaft hat keine Auswirkung auf vorhandene Verbindungen.

Cursor, die von der [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection)-Methode zurückgegeben werden, erben diese Einstellung. **Recordset** -Objekte erben diese Einstellung automatisch von den zugeordneten Verbindungen.

Diese Eigenschaft hat Lese-/Schreibzugriff für ein [Connection](connection-object-ado.md)-Objekt oder ein geschlossenes [Recordset](recordset-object-ado.md)-Objekt. Für ein geöffnetes **Recordset** -Objekt ist sie schreibgeschützt.

**Remote Data Service-Verwendung** Wenn in einem clientseitigen **Recordset** oder **Connection** -Objekt verwendet wird, kann die **CursorLocation** -Eigenschaft nur auf **AdUseClient**festgelegt werden.

