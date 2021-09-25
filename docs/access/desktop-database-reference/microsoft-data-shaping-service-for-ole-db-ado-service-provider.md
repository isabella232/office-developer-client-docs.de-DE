---
title: Microsoft Data Shaping Dienst für OLE DB (ADO-Dienstanbieter)
TOCTitle: Microsoft Data Shaping Service for OLE DB (ADO Service Provider)
ms:assetid: 6e6e5f39-6f43-7c7b-5812-796096d1d31b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249436(v=office.15)
ms:contentKeyID: 48545511
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: ec94d323cd4bd967006e82ea9d08da65a1565299
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59565268"
---
# <a name="microsoft-data-shaping-service-for-ole-db-ado-service-provider"></a>Microsoft Data Shaping Service for OLE DB (ADO Service Provider)


**Gilt für**: Access 2013, Office 2013

Der Dienstanbieter Microsoft Data Shaping Dienst für OLE DB unterstützt das Erstellen von hierarchischen (strukturierten) [Recordset](recordset-object-ado.md)-Objekten aus einem Datenanbieter.

## <a name="provider-keyword"></a>Schlüsselwort für den Anbieter

Um den Data Shaping Service for OLE DB aufzurufen, geben Sie das folgende Schlüsselwort und den folgenden Wert in die Verbindungszeichenfolge ein.

```vb 
 
"Provider=MSDataShape" 
```

## <a name="dynamic-properties"></a>Dynamische Eigenschaften

Beim Aufrufen dieses Dienstanbieters werden der [Properties](connection-object-ado.md)-Auflistung des [Connection](properties-collection-ado.md)-Objekts die folgenden dynamischen Eigenschaften hinzugefügt.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Name der dynamischen Eigenschaft</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Unique Reshape Names</strong></p></td>
<td><p>Gibt an, ob <strong>Recordset-Objekte</strong> mit doppelten Werten für ihre <strong>Reshape Name-Eigenschaften</strong> zulässig sind. Wenn diese dynamische Eigenschaft <strong>True</strong> ist und ein neues <strong>Recordset-Objekt</strong> mit demselben benutzerdefinierten Namen einer Neuform wie ein vorhandenes <strong>Recordset-Objekt</strong>erstellt wird, wird der Name der neuen <strong>Recordset-Objektumform</strong> so geändert, dass er eindeutig ist. Wenn diese Eigenschaft <strong>False</strong> ist und ein neues <strong>Recordset-Objekt</strong> mit demselben benutzerdefinierten Namen für die Neuform wie das vorhandene <strong>Recordset</strong>erstellt wird, haben beide <strong>Recordset-Objekte</strong> denselben Namen für die Neuform. Daher kann kein <strong>Recordset</strong> neu gestaltet werden, solange beide Recordsets vorhanden sind. Der Standardwert der Eigenschaft lautet <strong>False</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>Data Provider</strong></p></td>
<td><p>Gibt den Namen des Anbieters an, der Zeilen zum Strukturieren bereitstellt. Dieser Wert kann NONE sein, wenn der Anbieter nicht zum Bereitstellen von Zeilen verwendet wird.</p></td>
</tr>
</tbody>
</table>


You may also set writable dynamic properties by specifying their names as keywords in the connection string. For example, in Microsoft Visual Basic, set the **Data Provider** dynamic property to "MSDASQL" by specifying:

```vb 
 
Dim cn as New ADODB.Connection 
cn.Open "Provider=MSDataShape;Data Provider=MSDASQL" 
```

Sie können auch eine dynamische Eigenschaft festlegen oder abrufen, indem Sie deren Namen als Index für die [Properties](properties-collection-ado.md)-Eigenschaft angeben. Beispiel: Rufen Sie den aktuellen Wert der dynamischen Eigenschaft **Data Provider** ab, und drucken Sie ihn. Legen Sie anschließend einen neuen Wert fest. Gehen Sie dazu wie folgt vor:

```vb 
 
Debug.Print cn.Properties("Data Provider") 
cn.Properties("Data Provider") = "MSDASQL" 
```

Weitere Informationen zur Datenstrukturierung finden Sie unter [Datenstrukturierung (Zusammenfassung)](data-shaping.md).

