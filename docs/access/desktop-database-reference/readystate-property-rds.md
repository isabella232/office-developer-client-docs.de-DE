---
title: ReadyState-Eigenschaft (RDS)
TOCTitle: ReadyState property (RDS)
ms:assetid: e7b62205-a604-ef43-2f5d-9b51b46d2b5a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250175(v=office.15)
ms:contentKeyID: 48548412
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c284c39c69a337a940ea09d396328bd8a01d01dd
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25928796"
---
# <a name="readystate-property-rds"></a>ReadyState-Eigenschaft (RDS)


**Betrifft**: Access 2013, Office 2013

Gibt den Status eines [DataControl](datacontrol-object-rds.md)-Objekts beim Abrufen von Daten in dessen [Recordset](recordset-object-ado.md)-Objekt an.

## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte

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
<td><p>Alle von der aktuellen Abfrage abgerufenen Zeilen wurden im <strong>Recordset</strong>-Objekt des <strong>DataControl</strong>-Objekts gespeichert und sind verfügbar.
 Dieser Status ist auch vorhanden, wenn eine Operation aufgrund eines Fehlers abgebrochen wurde oder wenn das <strong>Recordset</strong>-Objekt nicht initialisiert wird.</p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> <P>Jede mithilfe der clientseitigen ausführbare Datei, die die folgenden Konstanten verwendet, muss Deklarationen bereitstellen. Sie können Ausschneiden und Einfügen aus der Datei Datei Adcvbs.inc, befindet sich im Ordner C:\Program Files\Common Dateien\System\MSADC gewünschten Konstantendeklarationen.</P>



## <a name="remarks"></a>Hinweise

Verwenden Sie das [onReadyStateChange](onreadystatechange-event-rds.md)-Ereignis, um Änderungen in der **ReadyState** -Eigenschaft während einer asynchronen Abfrageoperation zu überwachen. Das ist effizienter, als den Wert der Eigenschaft regelmäßig zu überprüfen.

Wenn ein Fehler, während einer asynchronen Operation die **ReadyState** -eigenschaftsänderungen zu **AdcReadyStateComplete auftritt**, ändert sich die [State](state-property-ado.md) -Eigenschaft von **AdStateExecuting** in **AdStateClosed**, und das **Recordset-Objekt** Objekt [Value](value-property-ado.md) -Eigenschaft bleibt *Nothing*.

