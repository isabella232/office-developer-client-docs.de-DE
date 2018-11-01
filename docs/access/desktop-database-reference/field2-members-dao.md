---
title: Field2 Members (DAO)
TOCTitle: Field2 Members
ms:assetid: 27829bbc-8b4e-c7eb-f29b-bcbef341f9fd
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191913(v=office.15)
ms:contentKeyID: 48543839
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 915a733d59d938e77f32a051b267b5e26bddf6a0
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25877121"
---
# <a name="field2-members-dao"></a>Field2 Members (DAO)


**Betrifft**: Access 2013, Office 2013

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
<td><p><strong><a href="field2-appendchunk-method-dao.md">Methoden "AppendChunk"</a></strong></p></td>
<td><p>Fügt Daten aus einem Zeichenfolgenausdruck an ein Field2-Objekt vom Typ Memo oder Long Binary in einem Recordset an.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field2-createproperty-method-dao.md">CreateProperty</a></strong></p></td>
<td><p>Erstellt ein neues, benutzerdefiniertes <strong><a href="property-object-dao.md">Property</a></strong> -Objekt (gilt nur für Microsoft Access-Arbeitsbereiche).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field2-getchunk-method-dao.md">GetChunk</a></strong></p></td>
<td><p>Gibt den gesamten oder einen Teil des Inhalts eines Objekts <strong>vom Typ Memo</strong> oder <strong>Long Field2</strong> in der <strong><a href="fields-collection-dao.md">Fields</a></strong> -Auflistung eines <strong><a href="recordset-object-dao.md">Recordset</a></strong> -Objekts.</p></td>
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
<td><p>Legt fest oder gibt einen Wert, der angibt, ob eine leere Zeichenfolge (&quot;&quot;) ist eine gültige Einstellung für die <strong><a href="field-value-property-dao.md">Value</a></strong> -Eigenschaft das <strong>Field2</strong> -Objekt mit einem Text- oder Memo-Datentyp (nur Microsoft Access-Arbeitsbereiche).</p></td>
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
<td><p><strong><a href="field2-expression-property-dao.md">Expression</a></strong></p></td>
<td><p>Lese-/Schreibzugriff</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field2-fieldsize-property-dao.md">Feldgröße</a></strong></p></td>
<td><p>Gibt die Anzahl von Bytes in der Datenbank (nicht im Arbeitsspeicher) verwendete eines Objekts vom Typ Memo oder Long Binary <strong>Field2</strong> in der <strong><a href="fields-collection-dao.md">Fields</a></strong> -Auflistung eines <strong><a href="recordset-object-dao.md">Recordset</a></strong> -Objekts.</p></td>
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
<td><p></p>

> [!NOTE]
> <P>[!HINWEIS] ODBCDirect-Arbeitsbereiche werden in Microsoft Access 2013 nicht unterstützt. Verwenden Sie ADO, wenn Sie auf externe Datenquellen zugreifen möchten, ohne das Microsoft Access-Datenbankmodul zu verwenden.</P>


<p>Gibt den Wert eines <strong>Field2</strong>-Objekts in der Datenbank zurück, der bei Beginn der letzten Batchaktualisierung vorhanden war (gilt nur für ODBCDirect-Arbeitsbereiche).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field2-properties-property-dao.md">Eigenschaften</a></strong></p></td>
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
<td><p><strong><a href="field2-sourcetable-property-dao.md">SourceTable</a></strong></p></td>
<td><p>Gibt einen Wert zurück, der den Namen einer Tabelle enthält, bei der es sich um die ursprüngliche Datenquelle für ein <strong>Field2</strong>-Objekt handelt. Schreibgeschützter <strong>String</strong>-Wert.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field2-type-property-dao.md">Typ</a></strong></p></td>
<td><p>Legt einen Wert fest, der den Funktions- oder Datentyp eines Objekts angibt, oder gibt einen solchen Wert zurück. Lese-/Schreibzugriff <strong>Integer</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field2-validateonset-property-dao.md">ValidateOnSet</a></strong></p></td>
<td><p>Mit dieser Eigenschaft wird ein Wert festgelegt oder zurückgegeben, der angibt, ob der Wert eines <strong>Field2</strong>-Objekts sofort beim Festlegen der <strong>Value</strong>-Eigenschaft überprüft wird (gilt nur für Microsoft Access-Arbeitsbereiche).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field2-validationrule-property-dao.md">ValidationRule</a></strong></p></td>
<td><p>Legt einen Wert fest, der die Daten in einem Feld überprüft, wenn es geändert oder einer Tabelle hinzugefügt wird, oder gibt den betreffenden Wert zurück (nur Microsoft Access-Arbeitsbereiche). <strong>String</strong>-Wert mit Lese-/Schreibzugriff.</p></td>
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
<td><p></p>

> [!NOTE]
> <P>[!HINWEIS] ODBCDirect-Arbeitsbereiche werden in Microsoft Access 2013 nicht unterstützt. Verwenden Sie ADO, wenn Sie auf externe Datenquellen zugreifen möchten, ohne das Microsoft Access-Datenbankmodul zu verwenden.</P>


<p>Gibt einen Wert zurück, der aktuell in der Datenbank vorhanden und neuer ist als die <strong>OriginalValue</strong>-Eigenschaft, wie von einem Konflikt der Batchaktualisierung festgestellt wurde (nur ODBCDirect-Arbeitsbereiche).</p></td>
</tr>
</tbody>
</table>

