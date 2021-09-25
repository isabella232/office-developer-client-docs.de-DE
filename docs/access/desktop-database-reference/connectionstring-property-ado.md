---
title: ConnectionString-Eigenschaft (ADO)
TOCTitle: ConnectionString property (ADO)
ms:assetid: c67a7daf-258f-d99d-6475-a4aa98d1e99d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249968(v=office.15)
ms:contentKeyID: 48547627
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 9c78651cc6a706fdf3fecc43258d39baea13bb3d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59615746"
---
# <a name="connectionstring-property-ado"></a>ConnectionString-Eigenschaft (ADO)


**Gilt für**: Access 2013, Office 2013

Gibt die Informationen an, mit denen eine Verbindung mit einer Datenquelle hergestellt wird.

## <a name="settings-and-return-values"></a>Einstellungen- und Rückgabewerte

Mit dieser Eigenschaft wird ein Wert vom Datentyp **Long** festgelegt oder zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Verwenden Sie die **ConnectionString-Eigenschaft,** um eine Datenquelle anzugeben, indem Sie eine detaillierte Verbindungszeichenfolge übergeben, die eine Reihe von *Argument* = Durch Semikolons getrennte *Wertanweisungen* enthält.

ADO unterstützt fünf Argumente für die **ConnectionString** -Eigenschaft. Alle anderen Argumente werden ohne weitere Verarbeitung durch ADO direkt an den Anbieter übergeben. ADO unterstützt die im Folgenden aufgeführten Argumente.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Argument</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Provider=</em></p></td>
<td><p>Gibt den Namen eines Anbieters an, der für die Verbindung verwendet werden soll.</p></td>
</tr>
<tr class="even">
<td><p><em>File Name=</em></p></td>
<td><p>Gibt den Namen einer anbieterspezifischen Datei an (z. B. ein gespeichertes Datenquellenobjekt), die voreingestellte Verbindungsinformationen enthält.</p></td>
</tr>
<tr class="odd">
<td><p><em>Remote Provider=</em></p></td>
<td><p>Gibt den Namen eines Anbieters an, der beim Öffnen einer clientseitigen Verbindung verwendet werden soll (nur Remote Data Service).</p></td>
</tr>
<tr class="even">
<td><p><em>Remote Server=</em></p></td>
<td><p>Gibt den Pfadnamen des Servers an, der beim Öffnen einer clientseitigen Verbindung verwendet werden soll (nur Remote Data Service).</p></td>
</tr>
<tr class="odd">
<td><p><em>URL=</em></p></td>
<td><p>Gibt die Verbindungszeichenfolge als absolute URL an, die eine Ressource wie z. B. eine Datei oder ein Verzeichnis identifiziert.</p></td>
</tr>
</tbody>
</table>


Nachdem Sie die **ConnectionString**-Eigenschaft festgelegt und das [Connection](connection-object-ado.md)-Objekt geöffnet haben, kann der Anbieter den Inhalt der Eigenschaft ändern, indem er z. B. die in ADO definierten Argumentnamen den entsprechenden Anbieternamen zuordnet.

Die **ConnectionString**-Eigenschaft erbt automatisch den für das Argument *ConnectionString* der [Open](open-method-ado-connection.md)-Methode verwendeten Wert, weshalb Sie die aktuelle **ConnectionString**-Eigenschaft beim Aufruf der **Open**-Methode außer Kraft setzen können.

Das Argument *File Name* bewirkt, dass ADO den zugehörigen Anbieter lädt. Deshalb können Sie nicht sowohl das Argument *Provider* als auch das Argument *File Name* übergeben.

Die **ConnectionString**-Eigenschaft hat Lese-/Schreibzugriff, wenn die Verbindung geschlossen ist. Wenn die Verbindung geöffnet ist, ist sie schreibgeschützt.

Duplikate eines Arguments in der **ConnectionString** -Eigenschaft werden ignoriert. Die letzte Instanz eines Arguments wird verwendet.

**Remote data service usage** Bei Verwendung in einem clientseitigen **Connection-Objekt** kann die **ConnectionString-Eigenschaft** nur die *Parameter Remoteanbieter* und *Remoteserver* enthalten.

