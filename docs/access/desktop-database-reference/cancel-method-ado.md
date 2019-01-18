---
title: Cancel-Methode (ADO)
TOCTitle: Cancel method (ADO)
ms:assetid: 747edc04-a5cc-3631-2d0b-82e7e41a76b7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249476(v=office.15)
ms:contentKeyID: 48545662
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231032
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 791803bb8935ffab24e5aed7e4e6a77360e82b65
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28713233"
---
# <a name="cancel-method-ado"></a>Cancel-Methode (ADO)

**Betrifft**: Access 2013, Office 2013

Bricht die Ausführung eines ausstehenden asynchronen Methodenaufrufs ab.

## <a name="syntax"></a>Syntax

- *Objekt*. Abbrechen

## <a name="remarks"></a>Hinweise

Verwenden Sie die **Cancel** -Methode, um die Ausführung eines asynchronen Methodenaufrufs (d. h. einer mit der Option **adAsyncConnect**, **adAsyncExecute** oder **adAsyncFetch** aufgerufenen Methode) zu beenden.

In der folgenden Tabelle wird gezeigt, welcher Task beendet wird, wenn Sie die **Cancel** -Methode für einen bestimmten Objekttyp verwenden.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><br />
<em>Objekt</em></p></th>
<th><p>Der letzte asynchrone Aufruf dieser Methode wird beendet</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="command-object-ado.md">Command</a></p></td>
<td><p><a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command">Ausführen</a></p></td>
</tr>
<tr class="even">
<td><p><a href="connection-object-ado.md">Connection</a></p></td>
<td><p><a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection">Execute</a> oder <a href="open-method-ado-connection.md">Open</a></p></td>
</tr>
<tr class="odd">
<td><p><a href="record-object-ado.md">Record</a></p></td>
<td><p><a href="copyrecord-method-ado.md">CopyRecord</a>, <a href="deleterecord-method-ado.md">DeleteRecord</a>, <a href="moverecord-method-ado.md">MoveRecord</a> oder <a href="open-method-ado-record.md">Open</a></p></td>
</tr>
<tr class="even">
<td><p><a href="recordset-object-ado.md">Recordset</a></p></td>
<td><p><a href="open-method-ado-recordset.md">Open</a></p></td>
</tr>
<tr class="odd">
<td><p><a href="stream-object-ado.md">Stream</a></p></td>
<td><p><a href="open-method-ado-stream.md">Open</a></p></td>
</tr>
</tbody>
</table>

