---
title: Microsoft OLE DB-Anbieter für Persistenz (ADO-Dienstanbieter)
TOCTitle: Microsoft OLE DB Persistence Provider (ADO Service Provider)
ms:assetid: 22e41769-36eb-5a88-05ed-870938657624
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249007(v=office.15)
ms:contentKeyID: 48543719
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4045445120d42f1ca88fce22ce566fc970fce28b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288953"
---
# <a name="microsoft-ole-db-persistence-provider-ado-service-provider"></a>Microsoft OLE DB Persistence Provider (ADO Service Provider)


**Gilt für**: Access 2013, Office 2013 

The Microsoft OLE DB Persistence Provider enables you to save a [Recordset](recordset-object-ado.md) object into a file, and later restore that **Recordset** object from the file. Schema information, data, and pending changes are preserved.

Sie können das **Recordset**-Objekt entweder im proprietären ADTG-Format (Advanced Data Table Gram) oder im offenen XML-Format (Extensible Markup Language) speichern.

## <a name="provider-keyword"></a>Schlüsselwort für den Anbieter

Um diesen Anbieter aufzurufen, geben Sie das folgende Schlüsselwort und den folgenden Wert in die Verbindungszeichenfolge ein.

```vb 
 
"Provider=MSPersist" 
```

## <a name="errors"></a>Fehler

Die folgenden Fehler, die von diesem Anbieter ausgegeben werden, können in Ihrer Anwendung erkannt werden.

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
<td><p>E_BADSTREAM</p></td>
<td><p>Die geöffnete Datei weist kein gültiges Format auf (d. h. das Format ist weder ADTG noch XML).</p></td>
</tr>
<tr class="even">
<td><p>E_CANTPERSISTROWSET</p></td>
<td><p>Das <strong>Recordset</strong>-Objekt weist Merkmale auf, die verhindern, dass das Objekt gespeichert werden kann.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Bemerkungen

Der Microsoft OLE DB-Anbieter für Persistenz macht keine dynamischen Eigenschaften verfügbar.

Derzeit können nur parametrisierte hierarchische **Recordset** -Objekte nicht gespeichert werden.

Weitere Informationen zum permanenten Speichern von **Recordset**-Objekten finden Sie unter [Weitere Informationen zur Permanenz von Recordsets ](more-about-recordset-persistence.md).

Wenn zum Öffnen eines **Recordset**-Objekts ein Stream verwendet wird, dürfen außer dem *Source*-Parameter der **Open**-Methode keine anderen Parameter angegeben werden.

