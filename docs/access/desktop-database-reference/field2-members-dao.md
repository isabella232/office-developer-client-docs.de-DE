---
title: Field2-Elemente (DAO)
TOCTitle: Field2 Members
ms:assetid: 27829bbc-8b4e-c7eb-f29b-bcbef341f9fd
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191913(v=office.15)
ms:contentKeyID: 48543839
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 6dfad2cb2dd650b93bb04c8322b0ccf9b8cd4228
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59622298"
---
# <a name="field2-members-dao"></a>Field2-Elemente (DAO)


**Gilt für**: Access 2013, Office 2013

Ein Field2-Objekt stellt Daten mit einem gemeinsamen Datentyp in einer Spalte und einer typischen Gruppe von Eigenschaften dar.

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
<td><p><strong><a href="field2-appendchunk-method-dao.md">AppendChunk</a></strong></p></td>
<td><p>Appends data from a string expression to a Memo or Long Binary <strong>Field2</strong> object in a <strong><a href="recordset-object-dao.md">Recordset</a></strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field2-createproperty-method-dao.md">Createproperty</a></strong></p></td>
<td><p>Erstellt ein neues, benutzerdefiniertes <strong><a href="property-object-dao.md">Property</a></strong> -Objekt (gilt nur für Microsoft Access-Arbeitsbereiche).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field2-getchunk-method-dao.md">GetChunk</a></strong></p></td>
<td><p>Gibt den gesamten Inhalt oder einen Teil des Inhalts eines <strong>Memo-</strong> oder <strong>Long BinaryField2 -Objekts</strong> in der <strong><a href="fields-collection-dao.md">Fields -Auflistung</a></strong> eines <strong><a href="recordset-object-dao.md">Recordset -Objekts</a></strong> zurück.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field2-loadfromfile-method-dao.md">LoadFromFile</a></strong></p></td>
<td><p>Lädt die angegebene Datei vom Datenträger.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field2-savetofile-method-dao.md">SaveToFile</a></strong></p></td>
<td><p>Speichert eine Anlage auf Datenträger.</p></td>
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
<td><p><strong><a href="field2-allowzerolength-property-dao.md">AllowZeroLength</a></strong></p></td>
<td><p>Legt einen Wert fest, der angibt, ob eine leere Zeichenfolge ( &quot; &quot; ) eine gültige Einstellung für die <strong><a href="field-value-property-dao.md">Value-Eigenschaft</a></strong> des <strong>Field2-Objekts</strong> mit einem Text- oder Memo-Datentyp ist, oder gibt diesen wert zurück (gilt nur für Microsoft Access-Arbeitsbereiche).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field2-appendonly-property-dao.md">AppendOnly</a></strong></p></td>
<td><p>Ruft einen <strong>Boolean</strong>-Wert ab oder legt diesen fest, der angibt, ob für das angegebene Feld festgelegt ist, dass neue Werte beim Hinzufügen an vorhandene Inhalte des Felds angefügt werden. Lese-/Schreibzugriff.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field2-attributes-property-dao.md">Attribute</a></strong></p></td>
<td><p>Mit dieser Eigenschaft wird ein Wert festgelegt oder zurückgegeben, der ein oder mehrere Merkmale eines <strong>Field2</strong>-Objekts angibt. <strong>Long</strong>-Wert mit Lese-/Schreibzugriff.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field2-collatingorder-property-dao.md">CollatingOrder</a></strong></p></td>
<td><p>Gibt einen Wert zurück, der die Sequenz der Sortierreihenfolge im Text für den Zeichenfolgenvergleich oder die Sortierung angibt (gilt nur für Microsoft Access-Arbeitsbereiche). Schreibgeschützter <strong>Long</strong>-Wert.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field2-complextype-property-dao.md">ComplexType</a></strong></p></td>
<td><p>Gibt ein <strong><a href="complextype-object-dao.md">ComplexType</a></strong> -Objekt zurück, das ein mehrwertiges Feld darstellt. Schreibgeschützt.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field2-dataupdatable-property-dao.md">DataUpdatable</a></strong></p></td>
<td><p>Gibt einen Wert zurück, der angibt, ob die Daten eines durch ein <strong>Field2</strong>-Objekt dargestellten Felds aktualisiert werden können.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field2-defaultvalue-property-dao.md">DefaultValue</a></strong></p></td>
<td><p>Legt den Standardwert eines <strong>Field2</strong>-Objekts fest oder gibt den Wert zurück. Bei einem <strong>Field2</strong>-Objekt, das der <strong><a href="fields-collection-dao.md">Fields</a></strong> -Auflistung noch nicht angefügt wurde, besteht für diese Eigenschaft Lese-/Schreibzugriff (gilt nur für Microsoft Access-Arbeitsbereiche).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field2-expression-property-dao.md">Ausdruck</a></strong></p></td>
<td><p>Lesen/Schreiben</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field2-fieldsize-property-dao.md">Feldgröße</a></strong></p></td>
<td><p>Returns the number of bytes used in the database (rather than in memory) of a Memo or Long Binary <strong>Field2</strong> object in the <strong><a href="fields-collection-dao.md">Fields</a></strong> collection of a <strong><a href="recordset-object-dao.md">Recordset</a></strong> object.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field2-foreignname-property-dao.md">ForeignName</a></strong></p></td>
<td><p>Mit dieser Eigenschaft wird ein Wert festgelegt oder zurückgegeben, der den Namen des <strong>Field2</strong>-Objekts in einer Fremdtabelle angibt, das einem Feld in einer Primärtabelle für eine Beziehung entspricht (gilt nur für Microsoft Access-Arbeitsbereiche).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field2-iscomplex-property-dao.md">IsComplex</a></strong></p></td>
<td><p>Gibt einen <strong>Boolean</strong>-Wert zurück, der angibt, ob das angegebene Feld ein mehrwertiger Datentyp ist. Schreibgeschützt.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field2-name-property-dao.md">Name</a></strong></p></td>
<td><p>Gibt den Namen des angegebenen Objekts zurück oder legt diesen fest. <strong>String</strong>-Wert mit Lese-/Schreibzugriff, wenn das Objekt noch keiner Auflistung angefügt wurde. Schreibgeschützter <strong>String</strong>-Wert, wenn das Objekt einer Auflistung angefügt wurde.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field2-ordinalposition-property-dao.md">OrdinalPosition</a></strong></p></td>
<td><p>Mit dieser Eigenschaft wird die relative Position eines <strong>Field2</strong>-Objekts in einer <strong><a href="fields-collection-dao.md">Fields</a></strong> -Auflistung festgelegt oder zurückgegeben.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field2-originalvalue-property-dao.md">OriginalValue</a></strong></p></td>
<td><p>Einer der <strong><a href="workspacetypeenum-enumeration-dao.md">WorkspaceTypeEnum</a></strong> -Werte.</p>
<td><p><strong>HINWEIS</strong>: ODBCDirect-Arbeitsbereiche werden in Microsoft Access 2013 nicht unterstützt. Verwenden Sie ADO, wenn Sie auf externe Datenquellen zugreifen möchten, ohne das Microsoft Access-Datenbankmodul zu verwenden.</p>
<p>Gibt den Wert eines <strong>Field2</strong>-Objekts in der Datenbank zurück, der bei Beginn der letzten Batchaktualisierung vorhanden war (gilt nur für ODBCDirect-Arbeitsbereiche).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field2-properties-property-dao.md">Properties</a></strong></p></td>
<td><p>Gibt die <strong><a href="properties-collection-dao.md">Properties</a></strong> -Auflistung des angegebenen Objekts zurück. Schreibgeschützt.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field2-required-property-dao.md">Erforderlich</a></strong></p></td>
<td><p>Mit dieser Eigenschaft wird ein Wert festgelegt oder zurückgegeben, der angibt, ob ein <strong>Field2</strong>-Objekt einen Nicht-Nullwert erfordert.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field2-size-property-dao.md">Größe</a></strong></p></td>
<td><p>Mit dieser Eigenschaft wird ein Wert festgelegt oder zurückgegeben, der die maximale Größe eines <strong>Field2</strong>-Objekts in Bytes angibt.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field2-sourcefield-property-dao.md">SourceField</a></strong></p></td>
<td><p>Gibt einen Wert zurück, der den Namen eines Felds enthält, bei dem es sich um die ursprüngliche Datenquelle für ein <strong>Field2</strong>-Objekt handelt. Schreibgeschützter <strong>String</strong>-Wert.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field2-sourcetable-property-dao.md">Sourcetable</a></strong></p></td>
<td><p>Gibt einen Wert zurück, der den Namen einer Tabelle enthält, bei der es sich um die ursprüngliche Datenquelle für ein <strong>Field2</strong>-Objekt handelt. Schreibgeschützter <strong>String</strong>-Wert.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field2-type-property-dao.md">Typ</a></strong></p></td>
<td><p>Legt einen Wert fest, der den Funktions- oder Datentyp eines Objekts angibt, oder gibt diesen Wert zurück. <strong>Integer</strong>-Wert mit Lese-/Schreibzugriff.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field2-validateonset-property-dao.md">ValidateOnSet</a></strong></p></td>
<td><p>Mit dieser Eigenschaft wird ein Wert festgelegt oder zurückgegeben, der angibt, ob der Wert eines <strong>Field2</strong>-Objekts sofort beim Festlegen der <strong>Value</strong>-Eigenschaft überprüft wird (gilt nur für Microsoft Access-Arbeitsbereiche).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field2-validationrule-property-dao.md">ValidationRule</a></strong></p></td>
<td><p>Mit dieser Eigenschaft wird ein Wert festgelegt oder zurückgegeben, der die Daten in einem Feld direkt bei der Eingabe oder dem Hinzufügen zu einer Tabelle überprüft (gilt nur für Microsoft Access-Arbeitsbereiche). <strong>String</strong>-Wert mit Lese-/Schreibzugriff.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field2-validationtext-property-dao.md">ValidationText</a></strong></p></td>
<td><p>Mit dieser Eigenschaft wird ein Wert festgelegt oder zurückgegeben, der den Text oder die Meldung angibt, mit der die Anwendung anzeigt, dass der Wert eines <strong>Field2</strong>-Objekts nicht der in der Einstellung der <strong>ValidationRule</strong>-Eigenschaft angegebenen Gütigkeitsregel entspricht (gilt nur für Microsoft Access-Arbeitsbereiche). <strong>String</strong>-Wert mit Lese-/Schreibzugriff.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field2-value-property-dao.md">Wert</a></strong></p></td>
<td><p>Legt den Wert eines Objekts fest oder gibt ihn zurück. <strong>Variant</strong>-Wert mit Lese-/Schreibzugriff.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field2-visiblevalue-property-dao.md">VisibleValue</a></strong></p></td>
<td><p>Einer der <strong><a href="workspacetypeenum-enumeration-dao.md">WorkspaceTypeEnum</a></strong> -Werte.</p>
<td><p><strong>HINWEIS</strong>: ODBCDirect-Arbeitsbereiche werden in Microsoft Access 2013 nicht unterstützt. Verwenden Sie ADO, wenn Sie auf externe Datenquellen zugreifen möchten, ohne das Microsoft Access-Datenbankmodul zu verwenden.</p>
<p>Gibt einen aktuellen Wert in der Datenbank zurück, der neuer ist als die durch einen Konflikt bei der Batchaktualisierung ermittelte <strong>OriginalValue</strong>-Eigenschaft (gilt nur für ODBCDirect-Arbeitsbereiche).</p></td>
</tr>
</tbody>
</table>

