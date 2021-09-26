---
title: TableDef.CreateField-Methode (DAO)
TOCTitle: CreateField Method
ms:assetid: a83d797f-ea42-4a07-dd9e-b254755f0891
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821396(v=office.15)
ms:contentKeyID: 48546897
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052971
f1_categories:
- Office.Version=v15
ms.localizationpriority: high
ms.openlocfilehash: 9a4f117592e58c282b83f3456c275c6b081c1419
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59601702"
---
# <a name="tabledefcreatefield-method-dao"></a>TableDef.CreateField-Methode (DAO)

**Gilt für:** Access 2013 | Office 2013

Erstellt ein neues **[Field](field-object-dao.md)**-Objekt (nur Microsoft Access-Arbeitsbereiche).

## <a name="syntax"></a>Syntax

*Ausdruck* .CreateField(_**Name**_, _**Type**_, _**Size**_)

*Ausdruck* Eine Variable, die ein **TableDef**-Objekt darstellt.

## <a name="parameters"></a>Parameter

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Name</p></th>
<th><p>Erforderlich/optional</p></th>
<th><p>Datentyp</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Name</em></p></td>
<td><p>Optional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Eine Zeichenfolge, die das neue <strong>Field</strong>-Objekt eindeutig benennt. Unter der <strong><a href="connection-name-property-dao.md">Name</a></strong>-Eigenschaft finden Sie Einzelheiten zu gültigen <strong>Field</strong>-Namen.</p></td>
</tr>
<tr class="even">
<td><p><em>Typ</em></p></td>
<td><p>Optional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Eine Konstante, die den Datentyp des neuen <strong>Field</strong>-Objekts bestimmt. Unter der <strong><a href="field-type-property-dao.md">Type</a></strong>-Eigenschaft finden Sie gültige Datentypen.</p></td>
</tr>
<tr class="odd">
<td><p><em>Size</em></p></td>
<td><p>Optional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Eine Ganzzahl, welche die maximale Größe in Bytes eines <strong>Field</strong>-Objekts angibt, das Text enthält. Siehe die Eigenschaft <strong><a href="field-size-property-dao.md">Size</a></strong> für gültige Größenwerte. Dieses Argument wird für numerische Felder und Felder mit fester Breite ignoriert.</p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a>Rückgabewert

Feld

## <a name="remarks"></a>Hinweise

Mit der **CreateField**-Methode können Sie ein neues Feld erstellen und den Namen, den Datentyp sowie die Größe des Felds angeben. Wenn Sie einen oder mehrere der optionalen Teile für **CreateField** weglassen, können Sie die entsprechende Eigenschaft mithilfe einer entsprechenden Zuweisungsanweisung festlegen oder zurücksetzen, bevor Sie das neue Objekt an eine Auflistung anfügen. Nachdem Sie das neue Objekt angefügt haben, können Sie einige, aber nicht alle Eigenschafteneinstellungen ändern. Weitere Informationen finden Sie in den Themen zu den einzelnen Eigenschaften.

Die Argumente „type“ und „Size“ gelten nur für **Field**-Objekte in einem **TableDef**-Objekt. Diese Argumente werden ignoriert, wenn ein **Field**-Objekt einem **Index**- oder **Relation**-Objekt zugeordnet ist.

Bezieht sich Name auf ein Objekt, das bereits ein Element der Auflistung ist, tritt ein Laufzeitfehler auf, wenn Sie die **[Append](fields-append-method-dao.md)**-Methode verwenden.

Um ein **Field**-Objekt aus einer **Fields**-Auflistung zu entfernen, führen Sie die **[Delete](fields-delete-method-dao.md)**-Methode für die Auflistung aus. Sie können ein **Field**-Objekt nicht mehr aus der **Fields**-Auflistung eines **TableDef**-Objekts löschen, nachdem Sie einen Index erstellt haben, der auf das Feld verweist.

**Link zur Verfügung gestellt von:** [UtterAccess](https://www.utteraccess.com)-Community. UtterAccess ist das führende Microsoft Access-Wiki und -Hilfeforum.

- [Hinzufügen eines Hyperlinkfelds zu einer vorhandenen Tabelle mit DAO](https://www.utteraccess.com/wiki/index.php/adding_a_hyperlink_field_to_an_existing_table_with_dao)

## <a name="example"></a>Beispiel

Im folgenden Beispiel wird veranschaulicht, wie Sie ein berechnetes Feld erstellen. Die CreateField-Methode erstellt ein Feld namens **FullName**. Die Expression-Eigenschaft wird dann auf den Ausdruck festgelegt, der den Wert des Felds berechnet.

**Der Beispielcode stammt von:**[Microsoft Access 2010 Programmer's Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

```vb
    Sub CreateCalculatedField()
        Dim dbs As DAO.Database
        Dim tdf As DAO.TableDef
        Dim fld As DAO.Field2
        
        ' get the database
        Set dbs = CurrentDb()
        
        ' create the table
        Set tdf = dbs.CreateTableDef("tblContactsCalcField")
        
        ' create the fields: first name, last name
        tdf.Fields.Append tdf.CreateField("FirstName", dbText, 20)
        tdf.Fields.Append tdf.CreateField("LastName", dbText, 20)
        
        ' create the calculated field: full name
        Set fld = tdf.CreateField("FullName", dbText, 50)
        fld.Expression = "[FirstName] & "" "" & [LastName]"
        tdf.Fields.Append fld
        
        ' append the table and cleanup
        dbs.TableDefs.Append tdf
        
    Cleanup:
        Set fld = Nothing
        Set tdf = Nothing
        Set dbs = Nothing
    End Sub
```

