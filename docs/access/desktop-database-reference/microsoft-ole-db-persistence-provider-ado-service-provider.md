---
title: Microsoft OLE DB-Anbieter für Persistenz (ADO-Dienstanbieter)
TOCTitle: Microsoft OLE DB Persistence Provider (ADO Service Provider)
ms:assetid: 22e41769-36eb-5a88-05ed-870938657624
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249007(v=office.15)
ms:contentKeyID: 48543719
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ee7f29fa12b7158f2886f908666fa485ddf291cd
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25474084"
---
# <a name="microsoft-ole-db-persistence-provider-ado-service-provider"></a>Microsoft OLE DB-Anbieter für Persistenz (ADO-Dienstanbieter)


**Betrifft**: Access 2013 | Office 2013 

Microsoft OLE DB-Anbieter für Persistenz können Sie ein [Recordset](recordset-object-ado.md) -Objekt in einer Datei zu speichern und später dieses **Recordset** -Objekt aus der Datei wiederherstellen. Schemainformationen, Daten und ausstehende Änderungen werden beibehalten.

Sie können das **Recordset** -Objekt entweder im proprietären ADTG-Format (Advanced Data Table Gram) oder im offenen XML-Format (Extensible Markup Language) speichern.

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


## <a name="remarks"></a>Hinweise

Der Microsoft OLE DB-Anbieter für Persistenz macht keine dynamischen Eigenschaften verfügbar.

Derzeit können nur parametrisierte hierarchische **Recordset** -Objekte nicht gespeichert werden.

Weitere Informationen zum permanenten Speichern von **Recordset** -Objekten finden Sie unter [Weitere Informationen zur Permanenz von Recordsets ](more-about-recordset-persistence.md).

Beim Öffnen eines **Recordset-Objekts**ein Stream verwendet wird, gibt es soll keine Parameter angegeben, andere als die *Source* -Parameter der **Open** -Methode.
