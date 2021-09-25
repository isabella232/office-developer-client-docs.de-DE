---
title: ExecuteOptions-Eigenschaft (RDS)
TOCTitle: ExecuteOptions property (RDS)
ms:assetid: fb244cbd-9a03-9128-1373-694c9061c9da
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250285(v=office.15)
ms:contentKeyID: 48548864
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: c316893e29856169b4176ef5f1f5f3fc11e78178
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59558373"
---
# <a name="executeoptions-property-rds"></a>ExecuteOptions-Eigenschaft (RDS)


**Gilt für**: Access 2013, Office 2013

Gibt an, ob die asynchrone Ausführung aktiviert ist.

## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte

Legt einen der folgenden Werte fest oder gibt ihn zurück.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Konstante</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>adcExecSync</strong></p></td>
<td><p>Führt die nächste Aktualisierung des <a href="recordset-object-ado.md">Recordsets</a> synchron aus.</p></td>
</tr>
<tr class="even">
<td><p><strong>adcExecAsync</strong></p></td>
<td><p>Standard. Führt die nächste Aktualisierung des <strong>Recordsets</strong> asynchron aus.</p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> Each client-side executable file that uses these constants must provide declarations for them. You can cut and paste the constant declarations that you want from the file Adcvbs.inc, located in the C:\Program Files\Common Files\System\MSADC folder.

## <a name="remarks"></a>HinwBemerkungeneise

Wenn **ExecuteOptions** auf **adcExecAsync** festgelegt ist, wird dadurch der nächste **Refresh**-Aufruf für das **Recordset**-Objekt des [RDS.DataControl](datacontrol-object-rds.md)-Objekts ausgeführt.

Ein Fehler tritt auf, wenn Sie versuchen, [Reset](reset-method-rds.md), [Refresh](refresh-method-rds.md), [SubmitChanges](submitchanges-method-rds.md), [CancelUpdate](cancelupdate-method-ado.md) oder [Recordset](recordset-sourcerecordset-properties-rds.md) aufzurufen, während eine andere asynchrone Operation ausgeführt wird, die das **Recordset**-Objekt des [RDS.DataControl](datacontrol-object-rds.md)-Objekts möglicherweise ändert.

Wenn bei einer asynchronen Operation ein Fehler auftritt, ändert sich der [ReadyState](readystate-property-rds.md)-Wert des **RDS.DataControl**-Objekts von **adcReadyStateLoaded** zu **adcReadyStateComplete**, und der **Recordset**-Eigenschaftswert bleibt *Nothing*.

