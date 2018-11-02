---
title: Optimieren der Leistung von dynamischen-Eigenschaft (ADO)
TOCTitle: Optimize dynamic property (ADO)
ms:assetid: 2253b052-2d8a-f6f0-f8b8-f56e79d243de
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249001(v=office.15)
ms:contentKeyID: 48543705
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4a1fff5911080811bc2556a20667ff2f2391f22e
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25926780"
---
# <a name="optimize-dynamic-property-ado"></a>Optimieren der Leistung von dynamischen-Eigenschaft (ADO)


**Betrifft**: Access 2013, Office 2013

Gibt an, ob für ein Feld ein Index erstellt werden soll.

## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte

Legt einen **Boolean** -Wert fest, der angibt, ob ein Index erstellt werden soll.

## <a name="remarks"></a>Hinweise

Ein Index kann die Leistung von Operationen verbessern, bei denen Werte in einem [Recordset](recordset-object-ado.md) gesucht oder sortiert werden. Der Index ist in ADO integriert, Sie können nicht explizit darauf zugreifen oder ihn in der Anwendung verwenden.

Legen Sie die **Optimize** -Eigenschaft auf **True** fest, um einen Index für ein Feld zu erstellen. Legen Sie diese Eigenschaft auf **False** fest, um den Index zu löschen.

**Optimize** ist eine dynamische Eigenschaft, die der [Properties](field-object-ado.md)-Auflistung des [Field](properties-collection-ado.md)-Objekts angefügt wird, wenn die [CursorLocation](cursorlocation-property-ado.md)-Eigenschaft auf **adUseClient** festgelegt wird.

**Verwendung**

```vb
    Dim rs As New Recordset
    Dim fld As Field
    rs.CursorLocation = adUseClient      'Enable index creation
    rs.Fields.Append "Field1", adChar, 35, adFldIsNullable
    rs.Open
    Set fld = rs.Fields(0)
    fld.Properties("Optimize") = True    'Create an index
    fld.Properties("Optimize") = False   'Delete an index
```
