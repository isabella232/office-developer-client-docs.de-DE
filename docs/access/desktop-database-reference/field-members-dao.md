---
title: Field-Elemente (DAO)
TOCTitle: Field Members
ms:assetid: 4b6a587f-1fd0-37fb-db7d-75b587a8dc60
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193511(v=office.15)
ms:contentKeyID: 48544689
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: a89ed019d9ab725ddcaa420679f4fcf4b9362e0c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59552981"
---
# <a name="field-members-dao"></a>Field-Elemente (DAO)


**Gilt für**: Access 2013, Office 2013

Ein Field-Objekt stellt Daten mit einem gemeinsamen Datentyp in einer Spalte und einer typischen Gruppe von Eigenschaften dar.

## <a name="methods"></a>Methoden

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Name</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong><a href="field-appendchunk-method-dao.md">AppendChunk</a></strong></p></td>
<td><p>Appends data from a string expression to a Memo or Long Binary <strong><a href="field-object-dao.md">Field</a></strong> object in a <strong><a href="recordset-object-dao.md">Recordset</a></strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field-createproperty-method-dao.md">Createproperty</a></strong></p></td>
<td><p>Erstellt ein neues, benutzerdefiniertes <strong><a href="property-object-dao.md">Property</a></strong> -Objekt (gilt nur für Microsoft Access-Arbeitsbereiche).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field-getchunk-method-dao.md">GetChunk</a></strong></p></td>
<td><p>Gibt den gesamten Inhalt oder einen Teil des Inhalts eines <strong>Memo-</strong> oder <strong>Long Binary</strong> <strong><a href="field-object-dao.md">Field</a></strong> -Objekts in der <strong><a href="fields-collection-dao.md">Fields -Auflistung</a></strong> eines <strong><a href="recordset-object-dao.md">Recordset</a></strong> -Objekts zurück.</p></td>
</tr>
</tbody>
</table>


## <a name="properties"></a>Eigenschaften

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Name</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong><a href="field-allowzerolength-property-dao.md">AllowZeroLength</a></strong></p></td>
<td><p>Legt einen Wert fest, der angibt, ob eine leere Zeichenfolge ( &quot; &quot; ) eine gültige Einstellung für die <strong><a href="field-value-property-dao.md">Value-Eigenschaft</a></strong> des <strong><a href="field-object-dao.md">Field-Objekts</a></strong> mit einem Text- oder Memo-Datentyp ist, oder gibt diesen Wert zurück (gilt nur für Microsoft Access-Arbeitsbereiche).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field-attributes-property-dao.md">Attribute</a></strong></p></td>
<td><p>Mit dieser Eigenschaft wird ein Wert festgelegt oder zurückgegeben, der ein oder mehrere Merkmale eines <strong><a href="field-object-dao.md">Field</a></strong> -Objekts angibt. <strong>Long</strong>-Wert mit Lese-/Schreibzugriff.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field-collatingorder-property-dao.md">CollatingOrder</a></strong></p></td>
<td><p>Gibt einen Wert zurück, der die Sequenz der Sortierreihenfolge im Text für den Zeichenfolgenvergleich oder die Sortierung angibt (gilt nur für Microsoft Access-Arbeitsbereiche). Schreibgeschützter <strong>Long</strong>-Wert.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field-dataupdatable-property-dao.md">DataUpdatable</a></strong></p></td>
<td><p>Gibt einen Wert zurück, der angibt, ob die Daten eines durch ein <strong><a href="field-object-dao.md">Field</a></strong> -Objekt dargestellten Felds aktualisiert werden können.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field-defaultvalue-property-dao.md">DefaultValue</a></strong></p></td>
<td><p>Legt den Standardwert eines <strong><a href="field-object-dao.md">Field</a></strong> -Objekts fest oder gibt den Wert zurück. Bei einem <strong>Field</strong>-Objekt, das der <strong><a href="fields-collection-dao.md">Fields</a></strong> -Auflistung noch nicht angefügt wurde, besteht für diese Eigenschaft Lese-/Schreibzugriff (gilt nur für Microsoft Access-Arbeitsbereiche).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field-fieldsize-property-dao.md">Feldgröße</a></strong></p></td>
<td><p>Returns the number of bytes used in the database (rather than in memory) of a Memo or Long Binary <strong><a href="field-object-dao.md">Field</a></strong> object in the <strong><a href="fields-collection-dao.md">Fields</a></strong> collection of a <strong><a href="recordset-object-dao.md">Recordset</a></strong> object.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field-foreignname-property-dao.md">ForeignName</a></strong></p></td>
<td><p>Mit dieser Eigenschaft wird ein Wert festgelegt oder zurückgegeben, der den Namen des <strong><a href="field-object-dao.md">Field</a></strong> -Objekts in einer Fremdtabelle angibt, das einem Feld in einer Primärtabelle für eine Beziehung entspricht (gilt nur für Microsoft Access-Arbeitsbereiche).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field-name-property-dao.md">Name</a></strong></p></td>
<td><p>Gibt den Namen des angegebenen Objekts zurück oder legt diesen fest. <strong>String</strong>-Wert mit Lese-/Schreibzugriff, wenn das Objekt noch keiner Auflistung angefügt wurde. Schreibgeschützter <strong>String</strong>-Wert, wenn das Objekt einer Auflistung angefügt wurde.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field-ordinalposition-property-dao.md">OrdinalPosition</a></strong></p></td>
<td><p>Legt die relative Position eines <strong><a href="field-object-dao.md">Field</a></strong> -Objekts innerhalb einer <strong><a href="fields-collection-dao.md">Fields</a></strong> -Auflistung fest oder gibt die relative Position zurück.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field-originalvalue-property-dao.md">OriginalValue</a></strong></p></td>
<td><p>Einer der <strong><a href="workspacetypeenum-enumeration-dao.md">WorkspaceTypeEnum</a></strong> -Werte.</p>
<td><p><strong>HINWEIS</strong>: ODBCDirect-Arbeitsbereiche werden in Microsoft Access 2013 nicht unterstützt. Verwenden Sie ADO, wenn Sie auf externe Datenquellen zugreifen möchten, ohne das Microsoft Access-Datenbankmodul zu verwenden.</p>
<p>Gibt den Wert eines <strong>Field</strong>-Objekts in der Datenbank zurück, das vorhanden war, als die letzte Batchaktualisierung begann (nur ODBCDirect-Arbeitsbereiche).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field-properties-property-dao.md">Properties</a></strong></p></td>
<td><p>Gibt die <strong><a href="properties-collection-dao.md">Properties</a></strong> -Auflistung des angegebenen Objekts zurück. Schreibgeschützt.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field-required-property-dao.md">Erforderlich</a></strong></p></td>
<td><p>Gibt einen Wert zurück, der angibt, ob für ein <strong><a href="field-object-dao.md">Field</a></strong> -Objekt ein Nicht-Null-Wert erforderlich ist, oder legt den betreffenden Wert fest.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field-fieldsize-property-dao.md">Größe</a></strong></p></td>
<td><p>Returns the number of bytes used in the database (rather than in memory) of a Memo or Long Binary <strong><a href="field-object-dao.md">Field</a></strong> object in the <strong><a href="fields-collection-dao.md">Fields</a></strong> collection of a <strong><a href="recordset-object-dao.md">Recordset</a></strong> object.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field-sourcefield-property-dao.md">SourceField</a></strong></p></td>
<td><p>Gibt einen Wert zurück, der den Namen des Felds angibt, das die ursprüngliche Quelle der Daten für ein <strong>Field</strong>-Objekt ist. Schreibgeschützter <strong>String</strong>-Wert.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field-sourcetable-property-dao.md">Sourcetable</a></strong></p></td>
<td><p>Gibt einen Wert zurück, der den Namen einer Tabelle enthält, bei der es sich um die ursprüngliche Datenquelle für ein <strong>Field</strong>-Objekt handelt. Schreibgeschützter <strong>String</strong>-Wert.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field-type-property-dao.md">Typ</a></strong></p></td>
<td><p>Legt einen Wert fest, der den Funktions- oder Datentyp eines Objekts angibt, oder gibt diesen Wert zurück. <strong>Integer</strong>-Wert mit Lese-/Schreibzugriff.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field-validateonset-property-dao.md">ValidateOnSet</a></strong></p></td>
<td><p>Legt einen Wert fest, der angibt, ob der Wert eines <strong><a href="field-object-dao.md">Field</a></strong> -Objekts sofort der Gültigkeitsprüfung unterzogen wird, wenn die <strong><a href="field-value-property-dao.md">Value</a></strong> -Eigenschaft des Objekts festgelegt wird, oder gibt den betreffenden Wert zurück (nur Microsoft Access-Arbeitsbereiche).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field-validationrule-property-dao.md">ValidationRule</a></strong></p></td>
<td><p>Mit dieser Eigenschaft wird ein Wert festgelegt oder zurückgegeben, der die Daten in einem Feld direkt bei der Eingabe oder dem Hinzufügen zu einer Tabelle überprüft (gilt nur für Microsoft Access-Arbeitsbereiche). <strong>String</strong>-Wert mit Lese-/Schreibzugriff.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field-validationtext-property-dao.md">ValidationText</a></strong></p></td>
<td><p>Legt einen Wert fest, der den Text der Nachricht angibt, die von der Anwendung angezeigt wird, wenn der Wert eines <strong>Field</strong>-Objekts die von der <strong>ValidationRule</strong>-Eigenschaft festgelegte Gültigkeitsregel nicht unterstützt, oder gibt den betreffenden Wert zurück (nur Microsoft Access-Arbeitsbereiche). <strong>String</strong>-Wert mit Lese-/Schreibzugriff.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field-value-property-dao.md">Wert</a></strong></p></td>
<td><p>Legt den Wert eines Objekts fest oder gibt ihn zurück. <strong>Variant</strong>-Wert mit Lese-/Schreibzugriff.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field-visiblevalue-property-dao.md">VisibleValue</a></strong></p></td>
<td><p>Einer der <strong><a href="workspacetypeenum-enumeration-dao.md">WorkspaceTypeEnum</a></strong> -Werte.</p>
<td><p><strong>HINWEIS</strong>: ODBCDirect-Arbeitsbereiche werden in Microsoft Access 2013 nicht unterstützt. Verwenden Sie ADO, wenn Sie auf externe Datenquellen zugreifen möchten, ohne das Microsoft Access-Datenbankmodul zu verwenden.</p>
<p>Gibt einen aktuellen Wert in der Datenbank zurück, der neuer ist als die durch einen Konflikt bei der Batchaktualisierung ermittelte <strong>OriginalValue</strong>-Eigenschaft (gilt nur für ODBCDirect-Arbeitsbereiche).</p></td>
</tr>
</tbody>
</table>

