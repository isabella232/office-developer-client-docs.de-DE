---
title: CursorOptionEnum (Access PC-Datenbank-Referenz)
TOCTitle: CursorOptionEnum
ms:assetid: 3c118c08-02f2-5290-1cef-29e97c35fddc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249155(v=office.15)
ms:contentKeyID: 48544303
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 9dda0ef3b268c164e1bb1f8fbad91f96328c30c2
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25881986"
---
# <a name="cursoroptionenum"></a>CursorOptionEnum

**Betrifft**: Access 2013, Office 2013

Gibt an, welche Funktionalität die [Supports](supports-method-ado.md)-Methode testen soll.

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Konstante</p></th>
<th><p>Wert</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>adAddNew</strong></p></td>
<td><p>0x1000400</p></td>
<td><p>Unterstützt die <a href="addnew-method-ado.md">AddNew</a>-Methode, um neue Datensätze hinzuzufügen.</p></td>
</tr>
<tr class="even">
<td><p><strong>adApproxPosition</strong></p></td>
<td><p>0x4000</p></td>
<td><p>Unterstützt die Eigenschaften <a href="absoluteposition-property-ado.md">AbsolutePosition</a> und <a href="absolutepage-property-ado.md">AbsolutePage</a>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>zulässt</strong></p></td>
<td><p>0 x 2000</p></td>
<td><p>Unterstützt die <a href="bookmark-property-ado.md">Bookmark</a>-Eigenschaft, um Zugriff auf bestimmte Datensätze zu erhalten.</p></td>
</tr>
<tr class="even">
<td><p><strong>adDelete</strong></p></td>
<td><p>0x1000800</p></td>
<td><p>Unterstützt die <a href="delete-method-ado-recordset.md">Delete</a>-Methode, um Datensätze zu löschen.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFind</strong></p></td>
<td><p>0 x 80000</p></td>
<td><p>Unterstützt die <a href="find-method-ado.md">Find</a>-Methode, um eine Zeile in einem <a href="recordset-object-ado.md">Recordset</a> zu finden.</p></td>
</tr>
<tr class="even">
<td><p><strong>adHoldRecords</strong></p></td>
<td><p>0 x 100</p></td>
<td><p>Ruft mehrere Datensätze ab oder ändert die nächste Position, ohne ein Commit für alle ausstehenden Änderungen auszuführen.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adIndex</strong></p></td>
<td><p>0 x 100000</p></td>
<td><p>Unterstützt die <a href="index-property-ado.md">Index</a>-Eigenschaft, um einen Index zu benennen.</p></td>
</tr>
<tr class="even">
<td><p><strong>adMovePrevious</strong></p></td>
<td><p>0 x 200</p></td>
<td><p>Unterstützt die Methoden <a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst</a> und <a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MovePrevious</a> sowie die Methoden <a href="move-method-ado.md">Move</a> oder <a href="getrows-method-ado.md">GetRows</a>, um die aktuelle Datensatzposition rückwärts zu verschieben, ohne Textmarken erforderlich zu machen.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adNotify</strong></p></td>
<td><p>0 x 40000</p></td>
<td><p>Gibt an, dass der zugrunde liegende Datenprovider Benachrichtigungen unterstützt (was bestimmt, ob <strong>Recordset</strong>-Ereignisse unterstützt werden).</p></td>
</tr>
<tr class="even">
<td><p><strong>adResync</strong></p></td>
<td><p>0 x 20000</p></td>
<td><p>Unterstützt die <a href="resync-method-ado.md">Resync</a>-Methode, um den Cursor mit den Daten zu aktualisieren, die in der zugrunde liegenden Datenbank sichtbar sind.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSeek</strong></p></td>
<td><p>0x200000</p></td>
<td><p>Unterstützt die <a href="seek-method-ado.md">Seek</a> -Methode, um eine Zeile in einem <strong>Recordset</strong>zu finden.</p></td>
</tr>
<tr class="even">
<td><p><strong>adUpdate</strong></p></td>
<td><p>0x1008000</p></td>
<td><p>Unterstützt die <a href="update-method-ado.md">Update</a>-Methode, um vorhandene Daten zu ändern.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adUpdateBatch</strong></p></td>
<td><p>0 x 10000</p></td>
<td><p>Unterstützt die Stapelaktualisierung (Methoden <a href="updatebatch-method-ado.md">UpdateBatch</a> und <a href="cancelbatch-method-ado.md">CancelBatch</a>), um mehrere Änderungen an den Anbieter zu übermitteln.</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>ADO/WFC-Entsprechung

Paket: **com.ms.wfc.data**

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Konstante</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>AdoEnums.CursorOption.ADDNEW</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.CursorOption.APPROXPOSITION</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.CursorOption.BOOKMARK</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.CursorOption.DELETE</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.CursorOption.FIND</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.CursorOption.HOLDRECORDS</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.CursorOption.INDEX</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.CursorOption.MOVEPREVIOUS</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.CursorOption.NOTIFY</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.CursorOption.RESYNC</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.CursorOption.SEEK</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.CursorOption.UPDATE</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.CursorOption.UPDATEBATCH</p></td>
</tr>
</tbody>
</table>

