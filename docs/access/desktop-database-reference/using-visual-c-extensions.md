---
title: Verwenden von Visual C++-Erweiterungen
TOCTitle: Using Visual C++ Extensions
ms:assetid: 0fb1014c-7ab6-6add-d09f-e5e48b2b32cb
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248866(v=office.15)
ms:contentKeyID: 48543270
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8bf2234e5935c2a1a13871e7e45c980fb9f33109
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32312061"
---
# <a name="using-visual-c-extensions"></a>Verwenden von Visual C++-Erweiterungen


**Gilt für**: Access 2013, Office 2013

## <a name="the-iadorecordbinding-interface"></a>Die IADORecordBinding-Schnittstelle

Durch die Microsoft Visual C++-Erweiterungen für ADO werden Felder eines [Recordset](recordset-object-ado.md)-Objekts C/C++-Variablen zugeordnet bzw. an diese gebunden. Wenn die aktuelle Zeile des gebundenen **Recordset**-Objekts geändert wird, werden alle gebundenen Felder in **Recordset** in die C/C++-Variablen kopiert. Gegebenenfalls werden die kopierten Daten in den deklarierten Typ der C/C++-Variablen konvertiert.

Durch die **BindToRecordset** -Methode der **IADORecordBinding** -Schnittstelle werden Felder an C/C++-Variablen gebunden. Durch die **AddNew** -Methode wird eine neue Zeile dem gebundenen **Recordset** hinzugefügt. Durch die **Update** -Methode werden Felder in neuen Zeilen des **Recordset** -Objekts mit dem Wert der C/C++-Variablen aufgefüllt oder Felder in vorhandenen Zeilen mit diesem Wert aktualisiert.

Die **IADORecordBinding** -Schnittstelle wird durch das **Recordset** -Objekt implementiert. Sie müssen den Code für die Implementierung nicht selbst schreiben.

## <a name="binding-entries"></a>Bindungseinträge

Durch die Visual C++-Erweiterungen für ADO werden Felder eines [Recordset](recordset-object-ado.md)-Objekts C/C++-Variablen zugeordnet. Die Definition einer Zuordnung zwischen einem Feld und einer Variablen wird als *Bindungseintrag* bezeichnet. Bindungseinträge für numerische Daten und Daten mit fester und variabler Länge werden von Makros bereitgestellt. Die Bindungseinträge und C/C++-Variablen werden in **CADORecordBinding**, einer von der Visual C++-Erweiterungsklasse abgeleiteten Klasse, deklariert. Die **CADORecordBinding**-Klasse wird intern durch die Bindungseintragsmakros definiert.

Die Parameter in diesen Makros werden von ADO intern einer **DBBINDING**-OLE DB-Struktur zugeordnet, und es wird ein **Accessor**-OLE DB-Objekt zum Verwalten der Verschiebung und Konvertierung von Daten zwischen Feldern und Variablen erstellt. Durch OLE DB werden Daten als aus drei Teilen bestehend definiert: ein *Puffer*, in dem die Daten gespeichert werden; ein *Status*, durch den angegeben wird, ob ein Feld erfolgreich im Puffer gespeichert wurde oder wie die Variable im Feld wiederhergestellt werden soll, und die *Länge* der Daten. (Weitere Informationen finden Sie unter *OLE DB-Programmierreferenz*, "Kapitel 6: Abrufen und Festlegen von Daten".)

## <a name="header-file"></a>Headerdatei

Schließen Sie die folgende Datei in die Anwendung ein, um die Visual C++-Erweiterungen für ADO zu verwenden:

```cpp 
 
#include <icrsint.h> 
```

## <a name="binding-recordset-fields"></a>Binden von Recordset-Feldern

**So binden Sie **Recordset** -Felder an C/C++-Variablen **

1.  Erstellen Sie eine Klasse, die von der **CADORecordBinding** -Klasse abgeleitet wird.

2.  Geben Sie Bindungseinträge und entsprechende C/C++-Variablen in der abgeleiteten Klasse an. Klammern Sie die Bindungs **Einträge\_zwischen\_BEGIN ADO-Bindung** und **\_End ADO\_-Bindungs** Makros. Beenden Sie die Makros nicht mit Kommas oder Semikolons. Die entsprechenden Trennzeichen werden automatisch durch die einzelnen Makros angegeben. Geben Sie einen Bindungseintrag für jedes Feld an, das einer C/C++-Variablen zugeordnet werden soll. Verwenden Sie ein entsprechendes Mitglied **aus\_dem\_ADO\_**-Eintrag mit fester Länge, dem **numerischen\_\_ADO-Eintrag**oder der ADO **\_-Eingabe Familie mit Variablen\_Längen\_** von Makros.

3.  Erstellen Sie in der Anwendung eine Instanz der von **CADORecordBinding** abgeleiteten Klasse. Rufen Sie die **IADORecordBinding** -Schnittstelle aus dem **Recordset** -Objekt ab. Rufen Sie dann die **BindToRecordset** -Methode auf, um die **Recordset** -Felder an die C/C++-Variablen zu binden.

Weitere Informationen finden Sie unter [Visual C++-Erweiterungen (Beispiel)](visual-c-extensions-example.md).

## <a name="interface-methods"></a>Schnittstellenmethoden

Die **IADORecordBinding** -Schnittstelle verfügt über drei Methoden: **BindToRecordset**, **AddNew** und **Update**. Das einzige Argument für jede Methode ist ein Zeiger auf eine Instanz der von **CADORecordBinding** abgeleiteten Klasse. Daher können mit den Methoden **AddNew** und **Update** keine Parameter der ADO-Methoden gleichen Namens angegeben werden.

**Syntax**

Durch die **BindToRecordset** -Methode werden die **Recordset** -Felder C/C++-Variablen zugeordnet.

`BindToRecordset(CADORecordBinding *binding)` 

Durch die **AddNew** -Methode wird die gleichnamige ADO-Methode, [AddNew](addnew-method-ado.md), aufgerufen, um dem **Recordset** -Objekt eine neue Zeile hinzuzufügen.

`AddNew(CADORecordBinding *binding)` 

Durch die **Update**-Methode wird die gleichnamige ADO-Methode, [Update](update-method-ado.md), aufgerufen, um das **Recordset**-Objekt zu aktualisieren.

`Update(CADORecordBinding *binding)` 

## <a name="binding-entry-macros"></a>Bindungseintragsmakros

Durch Bindungseintragsmakros wird die Zuordnung eines **Recordset** -Felds und einer Variablen definiert. Der Satz Bindungseinträge wird durch ein Anfangs- und ein Endmakro begrenzt.

Für Daten mit fester Länge (z. B. **adDate** oder **adBoolean** ), numerische Daten (z. B. **adTinyInt**, **adInteger** oder **adDouble** ) und Daten mit variabler Länge (z. B. **adChar**, **adVarChar** oder **adVarBinary** ) werden Makrofamilien bereitgestellt. Alle numerischen Typen, mit Ausnahme von **adVarNumeric**, sind auch Typen mit fester Länge. Jede Familie enthält unterschiedliche Parametersätze, sodass Sie Bindungsinformationen, die nicht von Interesse sind, ausschließen können.

Weitere Informationen finden Sie unter *OLE DB-Programmierreferenz*, "Anhang A: Datentypen".

_**Bindungsanfangseinträge**_

**\_ADO\_-Bindung beginnen**(*Klasse*)

_**Daten mit fester Länge**_

**ADO\_-\_Eintrag\_mit fester Länge**(*Ordnungszahl, Datentyp, Puffer, Status, Änderung*)  
**ADO\_-\_ENTRY2\_mit fester Länge**(*Ordnungszahl, Datentyp, Puffer, Änderung*)

_**Numerische Daten**_

**\_NUMERISCHEr\_ADO-Eintrag**(Ordnungs*Zahl, Datentyp, Puffer, Genauigkeit, Skalierung, Status, Änderung*)  
**ADO\_-\_numerische ENTRY2**(*Ordnungszahl, Datentyp, Puffer, Genauigkeit, Skalierung, Änderung*)

_**Daten mit variabler Länge**_

**\_VARIABLEr\_ADO\_-Eintrag**(*Ordnungszahl, Datentyp, Puffer, Größe, Status, Länge, Änderung*)  
**ADO\_-\_Variable\_Länge ENTRY2**(*Ordinal, DataType, Buffer, Size, Status, Modify*)  
**ADO\_-\_Variable\_Länge ENTRY3**(*Ordnungszahl, Datentyp, Puffer, Größe, Länge, ändern*)  
**ADO\_-\_Variable\_Länge ENTRY4**(*Ordinal, DataType, Buffer, Size, Modify*)

_**End-Bindungseinträge**_

**Beenden\_der\_ADO-Bindung** ()

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
<td><p><em>Klasse</em></p></td>
<td><p>Klasse, in der die Bindungseinträge und C/C++-Variablen definiert werden.</p></td>
</tr>
<tr class="even">
<td><p><em>Ordinal</em></p></td>
<td><p>Ab Eins gezählte Ordnungszahl des <strong>Recordset</strong>-Felds, das der C/C++-Variablen entspricht.</p></td>
</tr>
<tr class="odd">
<td><p><em>DataType</em></p></td>
<td><p>Entsprechender ADO-Datentyp der C/C++-Variablen (eine Liste der gültigen Datentypen finden Sie unter <a href="datatypeenum.md">DataTypeEnum</a>). Der Wert des <strong>Recordset</strong>-Felds wird gegebenenfalls in diesen Datentyp konvertiert.</p></td>
</tr>
<tr class="even">
<td><p><em>Buffer</em></p></td>
<td><p>Name der C/C++-Variablen, in der das <strong>Recordset</strong>-Feld gespeichert wird.</p></td>
</tr>
<tr class="odd">
<td><p><em>Size</em></p></td>
<td><p>Maximale Größe von <em>Buffer</em> in Byte. Wenn <em>Buffer</em> eine Zeichenfolge mit variabler Länge enthält, lassen Sie Platz für eine Null am Ende.</p></td>
</tr>
<tr class="even">
<td><p><em>Status</em></p></td>
<td><p>Name einer Variablen, durch die angegeben wird, ob der Inhalt von <em>Buffer</em> gültig ist und ob die Konvertierung des Felds in <em>DataType</em> erfolgreich war. Die beiden wichtigsten Werte für diese Variable sind <strong>adFldOK</strong> (die Konvertierung war erfolgreich) und <strong>adFldNull</strong> (der Wert des Felds wäre ein VARIANT vom Typ VT_NULL und nicht lediglich leer). Mögliche Werte für <em>Status</em> werden in der nächsten Tabelle, Status &quot;Werte, aufgeführt.&quot;</p></td>
</tr>
<tr class="odd">
<td><p><em>Modify</em></p></td>
<td><p>Boolesches Flag; durch TRUE wird angegeben, dass ADO das entsprechende <strong>Recordset</strong>-Feld mit dem in <em>Buffer</em> enthaltenen Wert aktualisieren darf. Legen Sie den booleschen <em>modify</em>-Parameter auf TRUE fest, um zu ermöglichen, dass das gebundene Feld durch ADO aktualisiert wird. Legen Sie ihn auf FALSE fest, wenn Sie das Feld untersuchen möchten, ohne es zu ändern.</p></td>
</tr>
<tr class="even">
<td><p><em>Genauigkeit</em></p></td>
<td><p>Anzahl der Ziffern, die in einer numerischen Variablen dargestellt werden können.</p></td>
</tr>
<tr class="odd">
<td><p><em>Scale</em></p></td>
<td><p>Anzahl der Dezimalstellen in einer numerischen Variablen.</p></td>
</tr>
<tr class="even">
<td><p><em>Length</em></p></td>
<td><p>Name einer 4-Byte-Variablen, die die tatsächliche Länge der Daten in <em>Buffer</em> enthält.</p></td>
</tr>
</tbody>
</table>


## <a name="status-values"></a>Statuswerte

Durch den Wert der *Status*-Variablen wird angegeben, ob ein Feld erfolgreich in eine Variable kopiert wurde.

Beim Festlegen von Daten kann *Status* auf **adFldNull** festgelegt werden, um anzugeben, dass das **Recordset**-Feld auf Null festgelegt werden soll.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Konstante</p></th>
<th><p>Wert</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>adFldOK</strong></p></td>
<td><p>0</p></td>
<td><p>Ein Feldwert ungleich Null wurde zurückgegeben.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFldBadAccessor</strong></p></td>
<td><p>1</p></td>
<td><p>Bindung war ungültig.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFldCantConvertValue</strong></p></td>
<td><p>2</p></td>
<td><p>Wert konnte aus anderen Gründen als nicht übereinstimmenden Vorzeichen oder einem Datenüberlauf nicht konvertiert werden.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFldNull</strong></p></td>
<td><p>3</p></td>
<td><p>Beim Abrufen eines Felds wird angegeben, dass ein Nullwert zurückgegeben wurde. Beim Festlegen eines Felds wird angegeben, dass das Feld auf <strong>NULL</strong> festgelegt werden soll, wenn <strong>NULL</strong> selbst vom Feld nicht codiert werden kann (z. B. ein Zeichenarray oder eine Ganzzahl).</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFldTruncated</strong></p></td>
<td><p>4</p></td>
<td><p>Daten mit variabler Länge oder numerische Ziffern wurden abgeschnitten.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFldSignMismatch</strong></p></td>
<td><p>5</p></td>
<td><p>Wert ist signiert und variabler Datentyp ist nicht signiert.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFldDataOverFlow</strong></p></td>
<td><p>6</p></td>
<td><p>Wert ist zu groß zum Speichern im variablen Datentyp.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFldCantCreate</strong></p></td>
<td><p>7</p></td>
<td><p>Unbekannter Spaltentyp und Feld bereits geöffnet.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFldUnavailable</strong></p></td>
<td><p>8</p></td>
<td><p>Feldwert konnte nicht ermittelt werden - z. B. in einem neuen nicht zugewiesenen Feld ohne Standardwert.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFldPermissionDenied</strong></p></td>
<td><p>9</p></td>
<td><p>Beim Aktualisieren keine Berechtigung zum Schreiben von Daten.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFldIntegrityViolation</strong></p></td>
<td><p>10</p></td>
<td><p>Beim Aktualisieren würde durch den Feldwert die Spaltenintegrität verletzt werden.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFldSchemaViolation</strong></p></td>
<td><p>11</p></td>
<td><p>Beim Aktualisieren würde durch den Feldwert das Spaltenschema verletzt werden.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFldBadStatus</strong></p></td>
<td><p>12</p></td>
<td><p>Beim Aktualisieren ungültiger Statusparameter.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFldDefault</strong></p></td>
<td><p>13</p></td>
<td><p>Beim Aktualisieren wurde ein Standardwert verwendet.</p></td>
</tr>
</tbody>
</table>

