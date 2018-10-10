---
title: Field Members (DAO)
TOCTitle: Field Members
ms:assetid: 4b6a587f-1fd0-37fb-db7d-75b587a8dc60
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193511(v=office.15)
ms:contentKeyID: 48544689
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5270acfe22d4b19447290be7f626185b5375cdbf
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25475746"
---
# <a name="field-members-dao"></a>Field Members (DAO)


**Betrifft**: Access 2013 | Office 2013

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
<td><p><strong><a href="field-appendchunk-method-dao.md">Methoden "AppendChunk"</a></strong></p></td>
<td><p>Fügt Daten aus einem Zeichenfolgenausdruck an ein Field-Objekt vom Typ Memo oder Long Binary in einem Recordset an.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field-createproperty-method-dao.md">CreateProperty</a></strong></p></td>
<td><p>Erstellt ein neues, benutzerdefiniertes <strong><a href="property-object-dao.md">Property</a></strong> -Objekt (gilt nur für Microsoft Access-Arbeitsbereiche).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field-getchunk-method-dao.md">GetChunk</a></strong></p></td>
<td><p>Gibt den gesamten Inhalt oder einen Teil des Inhalts eines <strong><strong>Field</strong></strong> -Objekts vom Typ <a href="field-object-dao.md">Memo</a> oder <strong>Long Binary</strong> in der <strong><a href="fields-collection-dao.md">Fields</a></strong> -Auflistung eines <strong><a href="recordset-object-dao.md">Recordset</a></strong> -Objekts zurück.</p></td>
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
<td><p>Legt fest oder gibt einen Wert, der angibt, ob eine leere Zeichenfolge (&quot;&quot;) ist eine gültige Einstellung für die <strong><a href="field-value-property-dao.md">Value</a></strong> -Eigenschaft des <strong><a href="field-object-dao.md">Field</a></strong> -Objekts mit einem Text- oder Memo-Datentyp (nur Microsoft Access-Arbeitsbereiche).</p></td>
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
<td><p>Gibt die Anzahl von Bytes in der Datenbank (nicht im Arbeitsspeicher) verwendete eines Objekts vom Typ Memo oder Long Binary- <strong><a href="field-object-dao.md">Feld</a></strong> in der <strong><a href="fields-collection-dao.md">Fields</a></strong> -Auflistung eines <strong><a href="recordset-object-dao.md">Recordset</a></strong> -Objekts.</p></td>
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
<td><p></p>

> [!NOTE]
> <P>[!HINWEIS] ODBCDirect-Arbeitsbereiche werden in Microsoft Access 2013 nicht unterstützt. Verwenden Sie ADO, wenn Sie auf externe Datenquellen zugreifen möchten, ohne das Microsoft Access-Datenbankmodul zu verwenden.</P>


<p>Gibt den Wert eines <strong>Field</strong>-Objekts in der Datenbank zurück, das vorhanden war, als die letzte Batchaktualisierung begann (nur ODBCDirect-Arbeitsbereiche).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field-properties-property-dao.md">Eigenschaften</a></strong></p></td>
<td><p>Gibt die <strong><a href="properties-collection-dao.md">Properties</a></strong> -Auflistung des angegebenen Objekts zurück. Schreibgeschützt.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field-required-property-dao.md">Erforderlich</a></strong></p></td>
<td><p>Gibt einen Wert zurück, der angibt, ob ein <strong><a href="field-object-dao.md">Field</a></strong> -Objekt einen Nicht-Null-Wert erfordert, oder legt den betreffenden Wert fest.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field-fieldsize-property-dao.md">Größe</a></strong></p></td>
<td><p>Gibt die Anzahl von Bytes in der Datenbank (nicht im Arbeitsspeicher) verwendete eines Objekts vom Typ Memo oder Long Binary- <strong><a href="field-object-dao.md">Feld</a></strong> in der <strong><a href="fields-collection-dao.md">Fields</a></strong> -Auflistung eines <strong><a href="recordset-object-dao.md">Recordset</a></strong> -Objekts.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field-sourcefield-property-dao.md">SourceField</a></strong></p></td>
<td><p>Gibt einen Wert zurück, der den Namen des Felds angibt, das die ursprüngliche Quelle der Daten für ein <strong>Field</strong>-Objekt ist. Schreibgeschützter <strong>String</strong>-Wert.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field-sourcetable-property-dao.md">SourceTable</a></strong></p></td>
<td><p>Gibt einen Wert zurück, der den Namen einer Tabelle enthält, bei der es sich um die ursprüngliche Datenquelle für ein <strong>Field</strong>-Objekt handelt. Schreibgeschützter <strong>String</strong>-Wert.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field-type-property-dao.md">Typ</a></strong></p></td>
<td><p>Legt einen Wert fest, der den Funktions- oder Datentyp eines Objekts angibt, oder gibt einen solchen Wert zurück. Lese-/Schreibzugriff <strong>Integer</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field-validateonset-property-dao.md">ValidateOnSet</a></strong></p></td>
<td><p>Legt einen Wert fest, der angibt, ob der Wert eines <strong><a href="field-object-dao.md">Field</a></strong> -Objekts sofort der Gültigkeitsprüfung unterzogen wird, wenn die <strong><a href="field-value-property-dao.md">Value</a></strong> -Eigenschaft des Objekts festgelegt wird, oder gibt den betreffenden Wert zurück (nur Microsoft Access-Arbeitsbereiche).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field-validationrule-property-dao.md">ValidationRule</a></strong></p></td>
<td><p>Legt einen Wert fest, der die Daten in einem Feld überprüft, wenn es geändert oder einer Tabelle hinzugefügt wird, oder gibt den betreffenden Wert zurück (nur Microsoft Access-Arbeitsbereiche). <strong>String</strong>-Wert mit Lese-/Schreibzugriff.</p></td>
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
<td><p></p>

> [!NOTE]
> <P>[!HINWEIS] ODBCDirect-Arbeitsbereiche werden in Microsoft Access 2013 nicht unterstützt. Verwenden Sie ADO, wenn Sie auf externe Datenquellen zugreifen möchten, ohne das Microsoft Access-Datenbankmodul zu verwenden.</P>


<p>Gibt einen Wert zurück, der aktuell in der Datenbank vorhanden und neuer ist als die <strong>OriginalValue</strong>-Eigenschaft, wie von einem Konflikt der Batchaktualisierung festgestellt wurde (nur ODBCDirect-Arbeitsbereiche).</p></td>
</tr>
</tbody>
</table>

