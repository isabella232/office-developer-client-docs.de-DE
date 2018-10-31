---
title: Microsoft Data Shaping Dienst für OLE DB (ADO-Dienstanbieter)
TOCTitle: Microsoft Data Shaping Service for OLE DB (ADO Service Provider)
ms:assetid: 6e6e5f39-6f43-7c7b-5812-796096d1d31b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249436(v=office.15)
ms:contentKeyID: 48545511
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 526c333f774aaf77079279932f8d9adf39915984
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25861491"
---
# <a name="microsoft-data-shaping-service-for-ole-db-ado-service-provider"></a>Microsoft Data Shaping Dienst für OLE DB (ADO-Dienstanbieter)


**Betrifft**: Access 2013 | Office 2013

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
<td><p>Gibt an, ob <strong>Recordset</strong> -Objekte mit doppelten Werten für deren Eigenschaften <strong>Reshape Name</strong> zulässig sind. Wenn diese dynamische Eigenschaft <strong>True ist</strong> und ein neues <strong>Recordset-Objekt</strong> wird erstellt, mit derselben vom Benutzer angegebener reshape Name als ein bereits vorhandenes <strong>Recordset-Objekt</strong>, und klicken Sie dann das neue <strong>Recordset</strong> -Objekt Reshape Name wird geändert, damit es eindeutig ist. Wenn diese Eigenschaft <strong>False</strong> ist, und ein neues <strong>Recordset-Objekt</strong> wird erstellt, mit derselben vom Benutzer angegebener reshape Name als den vorhandenen <strong>Recordset</strong>, beide <strong>Recordset</strong> -Objekte haben dieselbe reshape Name. Aus diesem Grund kann weder <strong>Recordset</strong> strukturiert werden, solange beide Objekte vorhanden sind. Der Standardwert der Eigenschaft lautet <strong>False</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>Data Provider</strong></p></td>
<td><p>Gibt den Namen des Anbieters an, der Zeilen zum Strukturieren bereitstellt. Dieser Wert kann NONE sein, wenn der Anbieter nicht zum Bereitstellen von Zeilen verwendet wird.</p></td>
</tr>
</tbody>
</table>


Sie können auch beschreibbare dynamische Eigenschaften festlegen, indem Sie die zugehörigen Namen in der Verbindungszeichenfolge als Schlüsselwörter angeben. Legen Sie beispielsweise in Microsoft Visual Basic die dynamische Eigenschaft Data Provider auf MSDASQL fest, indem Sie Folgendes angeben:

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

