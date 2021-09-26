---
title: Connection.CreateQueryDef-Methode (DAO)
TOCTitle: CreateQueryDef Method
ms:assetid: 254fe81a-9b45-e8e7-108d-503c1c1c0fcc
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191860(v=office.15)
ms:contentKeyID: 48543781
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053067
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: 6f54768e9c6297fb9e0d129f9545f88aaad8cdf7
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59590085"
---
# <a name="connectioncreatequerydef-method-dao"></a>Connection.CreateQueryDef-Methode (DAO)

**Gilt für**: Access 2013, Office 2013

Erstellt ein neues **[QueryDef](querydef-object-dao.md)**-Objekt.

## <a name="syntax"></a>Syntax

*Ausdruck* . CreateQueryDef(***Name** _, _*_SQLText_**)

*Ausdruck* Eine Variable, die ein **Connection** -Objekt darstellt.

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
<td><p>Eine <strong>Variant</strong> (Untertyp <strong>String</strong>), die die neue <strong>QueryDef</strong> eindeutig benennt.</p></td>
</tr>
<tr class="even">
<td><p><em>SQLText</em></p></td>
<td><p>Optional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Ein <strong>Variant</strong>-Wert (Untertyp <strong>String</strong>), bei dem es sich um eine SQL-Anweisung handelt, die das <strong>QueryDef</strong>-Objekt definiert. Wenn Sie dieses Argument nicht angeben, können Sie das <strong>QueryDef</strong>-Objekt definieren, indem Sie seine <strong><a href="querydef-sql-property-dao.md">SQL</a></strong>-Eigenschaft festlegen, bevor oder nachdem Sie es an eine Auflistung anfügen.</p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a>Rückgabewert

QueryDef

## <a name="remarks"></a>Bemerkungen

Wenn Sie in einem Microsoft Access-Arbeitsbereich bei der Erstellung einer **QueryDef** einen anderen Wert als eine Zeichenfolge der Länge 0 (null) für den Namen angeben, wird das resultierende **QueryDef**-Objekt automatisch an die **[QueryDefs](querydefs-collection-dao.md)**-Auflistung angefügt.

Wenn das von name angegebene Objekt bereits ein Mitglied der **QueryDefs**-Auflistung ist, tritt ein Laufzeitfehler auf. Sie können eine temporäre **QueryDef** erstellen, indem Sie beim Ausführen der CreateQueryDef-Methode eine Zeichenfolge der Länge 0 (null) für das **name**-Argument verwenden. Ein andere Methode besteht darin, die **[Name](connection-name-property-dao.md)** -Eigenschaft einer neu erstellten **QueryDef** auf eine Zeichenfolge der Länge 0 ("") festzulegen. Temporäre **QueryDef** -Objekte sind nützlich, wenn Sie dynamische SQL-Anweisungen wiederholt verwenden möchten, ohne neue dauerhafte Objekte in der **QueryDefs** -Auflistung zu erstellen. Sie können eine temporäre **QueryDef** nicht an eine Auflistung anfügen, da eine Zeichenfolge der Länge 0 (null) kein gültiger Name für ein dauerhaftes **QueryDef** -Objekt ist. Sie können immer die Eigenschaften **Name** und **SQL** des neu erstellten **QueryDef** -Objekts festlegen und die **QueryDef** anschließend an die **QueryDefs** -Auflistung anfügen.

Zum Ausführen der SQL-Anweisung in einem **QueryDef**-Objekt verwenden Sie die **[Execute](connection-execute-method-dao.md)**- oder die **[OpenRecordset](connection-openrecordset-method-dao.md)**-Methode.

Die Verwendung eines **QueryDef**-Objekts ist das bevorzugte Verfahren zum Ausführen von SQL-Pass-Through-Abfragen mit ODBC-Datenbanken.

Um ein **QueryDef**-Objekt aus einer **QueryDefs**-Auflistung in einer Datenbank des Microsoft Access-Datenbankmoduls zu entfernen, führen Sie die **[Delete](fields-delete-method-dao.md)**-Methode für die Auflistung aus.

