---
title: ExecuteOptions-Eigenschaft (RDS)
TOCTitle: ExecuteOptions Property (RDS)
ms:assetid: fb244cbd-9a03-9128-1373-694c9061c9da
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250285(v=office.15)
ms:contentKeyID: 48548864
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 641e7942f5336f230d396db7e06b9d0601645cb6
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25473117"
---
# <a name="executeoptions-property-rds"></a>ExecuteOptions-Eigenschaft (RDS)


**Betrifft**: Access 2013 | Office 2013

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
> <P>Jede mithilfe der clientseitigen ausführbare Datei, die die folgenden Konstanten verwendet, muss Deklarationen bereitstellen. Sie können Ausschneiden und Einfügen die Konstantendeklarationen auf, denen Sie aus der Datei Datei Adcvbs.inc, befindet sich im Ordner C:\Program Files\Common Dateien\System\MSADC möchten.</P>



## <a name="remarks"></a>Hinweise

Wenn **ExecuteOptions** auf **adcExecAsync** festgelegt ist, wird dadurch der nächste **Refresh** -Aufruf für das [Recordset](datacontrol-object-rds.md) -Objekt des **RDS.DataControl**-Objekts ausgeführt.

Ein Fehler tritt auf, wenn Sie versuchen, [Reset](reset-method-rds.md), [Refresh](refresh-method-rds.md), [SubmitChanges](submitchanges-method-rds.md), [CancelUpdate](cancelupdate-method-ado.md) oder [Recordset](recordset-sourcerecordset-properties-rds.md) aufzurufen, während eine andere asynchrone Operation ausgeführt wird, die das [Recordset](datacontrol-object-rds.md) -Objekt des **RDS.DataControl**-Objekts möglicherweise ändert.

Wenn bei einer asynchronen Operation ein Fehler auftritt, ändert sich der [ReadyState](readystate-property-rds.md)-Wert des **RDS.DataControl**-Objekts von **adcReadyStateLoaded** zu **adcReadyStateComplete**, und der **Recordset**-Eigenschaftswert bleibt *Nothing*.

