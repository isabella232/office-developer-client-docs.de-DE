---
title: Index. CreateField-Methode (DAO)
TOCTitle: CreateField Method
ms:assetid: fc82b785-8768-b144-a2a4-c1f1798865a6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837208(v=office.15)
ms:contentKeyID: 48548892
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: aedda14273446ff6823776e535eb7995aa127fa5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291831"
---
# <a name="indexcreatefield-method-dao"></a>Index. CreateField-Methode (DAO)

**Gilt für**: Access 2013, Office 2013

Erstellt ein neues **[Field](field-object-dao.md)** -Objekt (nur Microsoft Access-Arbeitsbereiche).

## <a name="syntax"></a>Syntax

*Ausdruck* . CreateField (***Name***, ***Typ***, ***Größe***)

*Ausdruck* Eine Variable, die ein **Index** -Objekt darstellt.

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
<td><p>Eine Zeichenfolge, die das neue <strong>Field</strong> -Objekt eindeutig benennt. Unter der <strong><a href="connection-name-property-dao.md">Name</a></strong> -Eigenschaft finden Sie Einzelheiten zu gültigen <strong>Field</strong> -Namen.  </p></td>
</tr>
<tr class="even">
<td><p><em>Type</em></p></td>
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

## <a name="remarks"></a>Bemerkungen

Mit der **CreateField**-Methode können Sie ein neues Feld erstellen und den Namen, den Datentyp sowie die Größe des Felds angeben. Wenn Sie einen oder mehrere der optionalen Teile für **CreateField** weglassen, können Sie die entsprechende Eigenschaft mithilfe einer entsprechenden Zuweisungsanweisung festlegen oder zurücksetzen, bevor Sie das neue Objekt an eine Auflistung anfügen. Nachdem Sie das neue Objekt angefügt haben, können Sie einige, aber nicht alle Eigenschafteneinstellungen ändern. Weitere Informationen finden Sie in den Themen zu den einzelnen Eigenschaften.

Die Argumente Type und Size gelten nur für **Field** -Objekte in einem **TableDef** -Objekt. Diese Argumente werden ignoriert, wenn ein **Field**-Objekt einem **Index**- oder **Relation**-Objekt zugeordnet ist.

Wenn Name auf ein Objekt verweist, das bereits ein Element der Auflistung ist, tritt ein Laufzeitfehler auf, wenn Sie die **[Append](fields-append-method-dao.md)** -Methode verwenden.

Wenn Sie ein **Field**-Objekt aus einer **Fields**-Auflistung entfernen möchten, verwenden Sie die **[Delete](fields-delete-method-dao.md)** -Methode für die Auflistung. Sie können ein **Field**-Objekt nicht mehr aus der **Fields**-Auflistung eines **TableDef**-Objekts löschen, nachdem Sie einen Index erstellt haben, der auf das Feld verweist.

