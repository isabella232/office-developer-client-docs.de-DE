---
title: Microsoft OLE DB-Anbieter für Internet Publishing
TOCTitle: Microsoft OLE DB Provider for Internet Publishing
ms:assetid: 5d1e8db5-dabb-0914-e11e-e2eac72bfa77
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249327(v=office.15)
ms:contentKeyID: 48545100
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 38183cd8306f2425a362bd2650639120a2d16845
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288967"
---
# <a name="microsoft-ole-db-provider-for-internet-publishing"></a>Microsoft OLE DB Provider for Internet Publishing

**Gilt für**: Access 2013, Office 2013

Der Microsoft OLE DB-Anbieter für Internet Publishing ermöglicht ADO den Zugriff auf Ressourcen, die von Microsoft FrontPage oder Microsoft Internet Information Server bedient werden. Zu den Ressourcen zählen Webquelldateien wie HTML-Dateien oder Windows 2000-Webordner.

## <a name="connection-string-parameters"></a>Verbindungszeichenfolgen-Parameter

Um eine Verbindung mit diesem Anbieter herzustellen, legen Sie das *Provider*-Argument der [ConnectionString](connectionstring-property-ado.md)-Eigenschaft fest auf:

```vb 
 
MSDAIPP.DSO 
```

Dieser Wert kann auch mithilfe der [Provider](provider-property-ado.md)-Eigenschaft festgelegt oder gelesen werden.

## <a name="typical-connection-string"></a>Typische Verbindungszeichenfolge

Eine typische Verbindungszeichenfolge für diesen Anbieter lautet:

```vb 
 
"Provider=MSDAIPP.DSO;Data Source=ResourceURL;User ID=userName;Password=userPassword;" 
```

\-oder

```vb 
 
"URL=ResourceURL;User ID=userName;Password=userPassword;" 
```

Die Zeichenfolge besteht aus den folgenden Schlüsselwörtern:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Schlüsselwort</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Provider</strong></p></td>
<td><p>Gibt den OLE DB-Anbieter für Internet Publishing an.</p></td>
</tr>
<tr class="even">
<td><p><strong>Data Source</strong> -oder- <strong>URL</strong></p></td>
<td><p>Gibt die URL einer Datei oder eines Verzeichnisses an, die in einem Webordner veröffentlicht wurde.</p></td>
</tr>
<tr class="odd">
<td><p><strong>User ID</strong></p></td>
<td><p>Gibt den Benutzernamen an.</p></td>
</tr>
<tr class="even">
<td><p><strong>Password</strong></p></td>
<td><p>Gibt das Benutzerkennwort an.</p></td>
</tr>
</tbody>
</table>


Wenn Sie für den *ResourceURL*-Wert aus "URL=" in der Verbindungszeichenfolge einen ungültigen Wert festlegen, zeigt der Anbieter für Internet Publishing standardmäßig ein Dialogfeld an und fordert zur Eingabe eines gültigen Werts auf. Dies ist ein unerwünschtes Verhalten für eine Komponente auf der mittleren Ebene einer Anwendung, da es die Ausführung des Programms unterbricht, bis das Dialogfeld geschlossen wird. Der Client scheint zu blockieren, weil er von der Komponente keine Antwort erhält.

> [!NOTE]
> Wenn MSDAIPP.DSO entweder mit dem Schlüsselwort der *Provider*-Verbindungszeichenfolge oder mit der **Provider**-Eigenschaft explizit als der Wert des Anbieters angegeben ist, kann "URL=" nicht in der Verbindungszeichenfolge verwendet werden. Wenn "URL=" dennoch verwendet wird, tritt ein Fehler auf. Geben Sie stattdessen einfach die URL an, wie im Thema [Verwenden von ADO mit dem OLE DB-Anbieter für Internet Publishing](the-ole-db-provider-for-internet-publishing.md) beschrieben.

