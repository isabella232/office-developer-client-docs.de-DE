---
title: Grenzen eines Recordset-Objekts
TOCTitle: The Limits of a Recordset
ms:assetid: 51e27c95-e0c3-7fdc-ac11-891553620376
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249266(v=office.15)
ms:contentKeyID: 48544833
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 991c3cf1e28db385af06a71cfb6ba247455bda91
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59593446"
---
# <a name="limits-of-a-recordset"></a>Die Einschränkungen eines Recordsets


**Gilt für**: Access 2013, Office 2013

Bestimmen Sie mithilfe der Eigenschaften **BOF** und **EOF**, ob ein **Recordset**-Objekt Datensätze enthält oder ob Sie beim Navigieren in den Datensätzen die Grenzen eines **Recordset**-Objekts überschritten haben. Stellen Sie sich **BOF** und **EOF** als "Phantomdatensätze" vor, die am Anfang und am Ende des **Recordset**-Objekts positioniert sind. Basierend auf dem **Recordset**-Beispielobjekt unter [Untersuchen von Daten](chapter-3-examining-data.md) würde dies nun wie folgt aussehen:

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Productid</p></th>
<th><p>Productname</p></th>
<th><p>Einzelpreis</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>BOF</p></td>
<td><p><br />
</p></td>
<td><p><br />
</p></td>
</tr>
<tr class="even">
<td><p>7 </p></td>
<td><p>Uncle Bob's Organic Dried Pears</p></td>
<td><p>30.0000</p></td>
</tr>
<tr class="odd">
<td><p>14 </p></td>
<td><p>Tofu</p></td>
<td><p>23.2500</p></td>
</tr>
<tr class="even">
<td><p>28</p></td>
<td><p>Rssle Sauerkraut</p></td>
<td><p>45.6000</p></td>
</tr>
<tr class="odd">
<td><p>51</p></td>
<td><p>Manjimup Dried Apples</p></td>
<td><p>53.0000</p></td>
</tr>
<tr class="even">
<td><p>74</p></td>
<td><p>Longlife Tofu</p></td>
<td><p>10.0000</p></td>
</tr>
<tr class="odd">
<td><p>EOF</p></td>
<td><p><br />
</p></td>
<td><p><br />
</p></td>
</tr>
</tbody>
</table>


Die **BOF**-Eigenschaft gibt **True** (-1) zurück, falls sich die aktuelle Datensatzposition vor dem ersten Datensatz befindet, und **False** (0), falls sich die aktuelle Datensatzposition im oder nach dem ersten Datensatz befindet.

Die **EOF**-Eigenschaft gibt **True** zurück, falls sich die aktuelle Datensatzposition nach dem letzten Datensatz befindet, und **False**, falls sich die aktuelle Datensatzposition im oder vor dem letzten Datensatz befindet.

Wenn die **BOF** - oder die **EOF** -Eigenschaft **True** ist, gibt es wie im folgenden Code veranschaulicht keinen aktuellen Datensatz:

```vb 
 
If oRs.BOF And oRs.EOF Then 
 ' Command returned no records. 
End If 
```

If you open a **Recordset** object containing no records, the **BOF** and **EOF** properties are both set to **True** and the value of the **Recordset** object's **RecordCount** property setting depends on the cursor type. -1 wird für dynamische Cursor (**CursorType**  =  **adOpenDynamic**) und 0 für andere Cursor zurückgegeben.

Wenn Sie ein **Recordset**-Objekt öffnen, das mindestens einen Datensatz enthält, ist der erste Datensatz der aktuelle Datensatz, und die Eigenschaften **BOF** und **EOF** sind **False**.

Wenn Sie den letzten verbleibenden Datensatz im **Recordset** -Objekt löschen, befindet sich der Cursor in einem unbestimmten Status. Die Eigenschaften **BOF** und **EOF** bleiben je nach Anbieter **False**, bis Sie versuchen, den aktuellen Datensatz neu zu positionieren.

