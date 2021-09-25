---
title: ReadyState-Eigenschaft (RDS)
TOCTitle: ReadyState property (RDS)
ms:assetid: e7b62205-a604-ef43-2f5d-9b51b46d2b5a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250175(v=office.15)
ms:contentKeyID: 48548412
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: e1dab8baeeef547c93e8e3ced89ed3fc24ab97f0
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59562405"
---
# <a name="readystate-property-rds"></a>ReadyState-Eigenschaft (RDS)

**Gilt für**: Access 2013, Office 2013

Gibt den Status eines [DataControl](datacontrol-object-rds.md)-Objekts beim Abrufen von Daten in dessen [Recordset](recordset-object-ado.md)-Objekt an.

## <a name="settings-and-return-values"></a>Einstellungen- und Rückgabewerte

Legt einen der folgenden Werte fest oder gibt ihn zurück.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Wert</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>adcReadyStateLoaded</strong></p></td>
<td><p>Die aktuelle Abfrage wird noch ausgeführt, und es wurden noch keine Zeilen abgerufen. Das <strong>Recordset</strong>-Objekt des <strong>DataControl</strong>-Objekts ist nicht verfügbar.</p></td>
</tr>
<tr class="even">
<td><p><strong>adcReadyStateInteractive</strong></p></td>
<td><p>Eine erste von der aktuellen Abfrage abgerufene Datensatzgruppe wurde im <strong>Recordset</strong>-Objekt des <strong>DataControl</strong>-Objekts gespeichert und ist verfügbar. Die übrigen Zeilen werden noch abgerufen.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adcReadyStateComplete</strong></p></td>
<td><p>Alle von der aktuellen Abfrage abgerufenen Zeilen wurden im <strong>Recordset</strong>-Objekt des <strong>DataControl</strong>-Objekts gespeichert und sind verfügbar. Dieser Status ist auch vorhanden, wenn eine Operation aufgrund eines Fehlers abgebrochen wurde oder wenn das <strong>Recordset</strong>-Objekt nicht initialisiert wird.</p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> Each client-side executable file that uses these constants must provide declarations for them. You can cut and paste the constant declarations you want from the file Adcvbs.inc, located in the C:\Program Files\Common Files\System\MSADC folder.

## <a name="remarks"></a>HinwBemerkungeneise

Verwenden Sie das [onReadyStateChange](onreadystatechange-event-rds.md)-Ereignis, um Änderungen in der **ReadyState**-Eigenschaft während einer asynchronen Abfrageoperation zu überwachen. Das ist effizienter, als den Wert der Eigenschaft regelmäßig zu überprüfen.

Wenn während eines asynchronen Vorgangs ein Fehler auftritt, ändert sich die **ReadyState-Eigenschaft** in **adcReadyStateComplete,** die [State-Eigenschaft](state-property-ado.md) ändert sich von **adStateExecuting** in **adStateClosed,** und die Value-Eigenschaft [](value-property-ado.md) des **Recordset-Objekts** bleibt *Nothing*.

