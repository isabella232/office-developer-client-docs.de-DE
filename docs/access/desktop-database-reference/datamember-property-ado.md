---
title: DataMember-Eigenschaft (ADO)
TOCTitle: DataMember property (ADO)
ms:assetid: f89e1d42-7993-764b-4e8a-2f449903f792
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250263(v=office.15)
ms:contentKeyID: 48548787
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: acdfe44352b85644c0c27e624b1dbb07afb235b8
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59565534"
---
# <a name="datamember-property-ado"></a>DataMember-Eigenschaft (ADO)

**Gilt für**: Access 2013, Office 2013

Gibt den Namen des Datenelements an, das von dem durch die [DataSource](datasource-property-ado.md)-Eigenschaft angegebenen Objekt abgerufen wird.

## <a name="settings-and-return-values"></a>Einstellungen- und Rückgabewerte

Mit dieser Eigenschaft wird ein Wert vom Datentyp **Long** festgelegt oder zurückgegeben. Die Groß-/Kleinschreibung wird für den Namen ignoriert.

## <a name="remarks"></a>HinwBemerkungeneise

Mithilfe dieser Eigenschaft werden datengebundene Steuerelemente mit der Datenumgebung erstellt. Die Datenumgebung verwaltet Datensammlungen (Datenquellen), die benannte Objekte (*Datenelemente*) enthalten und als [Recordset](recordset-object-ado.md)-Objekt dargestellt werden.

Die Eigenschaften **DataMember** und **DataSource** müssen in Kombination verwendet werden.

Die **DataMember** -Eigenschaft bestimmt, welches durch die **DataSource** -Eigenschaft angegebene Objekt als **Recordset** -Objekt dargestellt wird. Das **Recordset** -Objekt muss geschlossen werden, bevor diese Eigenschaft festgelegt wird. Ein Fehler wird generiert, falls die **DataMember** -Eigenschaft nicht vor der **DataSource** -Eigenschaft festgelegt wird oder falls der Name der **DataMember** -Eigenschaft von dem in der **DataSource** -Eigenschaft angegebenen Objekt nicht erkannt wird.

**Verwendung**

```vb
    Dim rs as New ADODB.Recordset
    rs.DataMember = "Command"     'Name of the rowset to bind to
    Set rs.DataSource = myDE      'Name of the object containing an IRowset
```
