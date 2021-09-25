---
title: Relation.CreateField-Methode (DAO)
TOCTitle: CreateField Method
ms:assetid: bc60c91e-acef-1c90-7303-12f77cce15b8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822717(v=office.15)
ms:contentKeyID: 48547411
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: bed31b92222351ef6c74e3cb4f4452c29a1a8907
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59617524"
---
# <a name="relationcreatefield-method-dao"></a>Relation.CreateField-Methode (DAO)

**Gilt für**: Access 2013, Office 2013

Erstellt ein neues **[Field](field-object-dao.md)**-Objekt (nur Microsoft Access-Arbeitsbereiche).

## <a name="syntax"></a>Syntax

*Ausdruck* . CreateField(***Name** _, _*_Type_*_, _*_Size_**)

*Ausdruck* Eine Variable, die ein **Relation -Objekt** darstellt.

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
<td><p>Argument wird für dieses Objekt nicht unterstützt.</p></td>
</tr>
<tr class="odd">
<td><p><em>Size</em></p></td>
<td><p>Optional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Argument wird für dieses Objekt nicht unterstützt.</p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a>Rückgabewert

Feld

## <a name="remarks"></a>Hinweise

Mit der **CreateField**-Methode können Sie ein neues Feld erstellen und den Namen, den Datentyp sowie die Größe des Felds angeben. Wenn Sie einen oder mehrere der optionalen Teile für **CreateField** weglassen, können Sie die entsprechende Eigenschaft mithilfe einer entsprechenden Zuweisungsanweisung festlegen oder zurücksetzen, bevor Sie das neue Objekt an eine Auflistung anfügen. Nachdem Sie das neue Objekt angefügt haben, können Sie einige, aber nicht alle Eigenschafteneinstellungen ändern. Weitere Informationen finden Sie in den Themen zu den einzelnen Eigenschaften.

Die Argumente für Typ und Größe gelten nur für **Field-Objekte** in einem **TableDef-Objekt.** Diese Argumente werden ignoriert, wenn ein **Field**-Objekt einem **Index**- oder **Relation**-Objekt zugeordnet ist.

Wenn sich der Name auf ein Objekt bezieht, das bereits ein Element der Auflistung ist, tritt ein Laufzeitfehler auf, wenn Sie die **[Append-Methode](fields-append-method-dao.md)** verwenden.

Um ein **Field**-Objekt aus einer **Fields**-Auflistung zu entfernen, führen Sie die **[Delete](fields-delete-method-dao.md)**-Methode für die Auflistung aus. Sie können ein **Field**-Objekt nicht mehr aus der **Fields**-Auflistung eines **TableDef**-Objekts löschen, nachdem Sie einen Index erstellt haben, der auf das Feld verweist.

