---
title: Microsoft OLE DB-Anbieter für Oracle
TOCTitle: Microsoft OLE DB Provider for Oracle
ms:assetid: 97508e3f-077f-9b85-f4dd-8dd01a201aba
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249674(v=office.15)
ms:contentKeyID: 48546465
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b9b506f40039ff91a6b1985606322fd86a9e7c0e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288932"
---
# <a name="microsoft-ole-db-provider-for-oracle"></a>Microsoft OLE DB Provider for Oracle

**Gilt für**: Access 2013, Office 2013

Der Microsoft OLE DB-Anbieter für Oracle ermöglicht ADO den Zugriff auf Oracle-Datenbanken.

## <a name="connection-string-parameters"></a>Verbindungszeichenfolgen-Parameter

Um eine Verbindung mit diesem Anbieter herzustellen, legen Sie das *Provider*-Argument der [ConnectionString](connectionstring-property-ado.md)-Eigenschaft fest auf:

```vb 
 
MSDAORA 
```

Beim Lesen der [Provider](provider-property-ado.md)-Eigenschaft wird diese Zeichenfolge ebenfalls zurückgegeben.

Wenn eine JOIN-Abfrage mit einem dynamischen oder einem Keyset-Cursor in einer Oracle-Datenbank ausgeführt wird, tritt ein Fehler auf. Oracle unterstützt nur schreibgeschützte statische Cursor.

## <a name="typical-connection-string"></a>Typische Verbindungszeichenfolge

Eine typische Verbindungszeichenfolge für diesen Anbieter lautet:

```vb 
 
"Provider=MSDAORA;Data Source=serverName;User ID=userName; Password=userPassword;" 
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
<td><p>Gibt den OLE DB-Anbieter für Oracle an.</p></td>
</tr>
<tr class="even">
<td><p><strong>Data Source</strong></p></td>
<td><p>Gibt den Namen eines Servers an.</p></td>
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


## <a name="provider-specific-connection-parameters"></a>Anbieterspezifische Verbindungsparameter

Der Anbieter unterstützt neben den von ADO definierten verschiedene anbieterspezifische Verbindungsparameter. Wie die ADO-Verbindungseigenschaften können diese anbieterspezifischen Eigenschaften über die [Properties](properties-collection-ado.md)-Auflistung eines [Connection](connection-object-ado.md)-Objekts oder als Teil der **ConnectionString** -Eigenschaft festgelegt werden.

These parameters are fully described in the OLE DB Programmer's Reference. (The [ADO Dynamic Property Index](ado-dynamic-property-index.md) provides a cross-reference between these parameter names and the corresponding OLE DB properties.)

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Parameter</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Window Handle</strong></p></td>
<td><p>Gibt den Fensterhandle an, der verwendet werden soll, um nach zusätzlichen Informationen anzufragen.</p></td>
</tr>
<tr class="even">
<td><p><strong>Locale Identifier</strong></p></td>
<td><p>Gibt eine eindeutige 32-Bit-Zahl (z. B. 1033) an, mit der Einstellungen für die Sprache des Benutzers festgelegt werden. Diese Einstellungen geben an, wie Datum und Uhrzeit formatiert, Elemente alphabetisch sortiert, Zeichenfolgen verglichen werden usw.</p></td>
</tr>
<tr class="odd">
<td><p><strong>OLE DB Services</strong></p></td>
<td><p>Gibt eine Bitmaske an, die angibt, welche OLE DB-Dienste aktiviert oder deaktiviert werden sollen.</p></td>
</tr>
<tr class="even">
<td><p><strong>Prompt</strong></p></td>
<td><p>Gibt an, ob für den Benutzer eine Eingabeaufforderung angezeigt wird, während eine Verbindung hergestellt wird.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Extended Properties</strong></p></td>
<td><p>Eine Zeichenfolge mit anbieterspezifischen erweiterten Verbindungsinformationen. Verwenden Sie diese Eigenschaft nur für anbieterspezifische Verbindungsinformationen, die nicht über den Eigenschaftenmechanismus beschrieben werden können.</p></td>
</tr>
</tbody>
</table>

