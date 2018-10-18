---
title: Connection.CreateQueryDef Method (DAO)
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
ms.openlocfilehash: 35bf71742133b65c2e55583e1c62922cb5bc91e8
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/17/2018
ms.locfileid: "25606038"
---
# <a name="connectioncreatequerydef-method-dao"></a>Connection.CreateQueryDef Method (DAO)


**Betrifft**: Access 2013 | Office 2013

Erstellt ein neues **[QueryDef](querydef-object-dao.md)** -Objekt.

## <a name="syntax"></a>Syntax

*Ausdruck* . CreateQueryDef (***Name***, ***SQLText***)

*Ausdruck* Eine Variable, die ein **Connection** -Objekt darstellt.

### <a name="parameters"></a>Parameter

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
<th><p>Erforderlich/Optional</p></th>
<th><p>Datentyp</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Name</p></td>
<td><p>Optional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Eine <strong>Variant</strong> (Untertyp <strong>String</strong>), die die neue <strong>QueryDef</strong> eindeutig benennt.</p></td>
</tr>
<tr class="even">
<td><p>SQLText</p></td>
<td><p>Optional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Eine <strong>Variant</strong> (Untertyp <strong>String</strong>), bei er es sich um eine SQL Anweisung handelt, die die <strong>QueryDef</strong> definiert. Wenn dieses Argument ausgelassen wird, können Sie die <strong>QueryDef</strong> durch Festlegen ihrer <strong><a href="querydef-sql-property-dao.md">SQL</a></strong>-Eigenschaft definieren, bevor oder nachdem Sie sie an eine Auflistung anfügen.</p></td>
</tr>
</tbody>
</table>


<<<<<<< Kopf
### <a name="return-value"></a>Rückgabewert
=======
### <a name="return-value"></a>Rückgabewert
>>>>>>> master

QueryDef-Objekt

## <a name="remarks"></a>Hinweise

Wenn Sie in einem Microsoft Access-Arbeitsbereich beim Erstellen eines **QueryDef**-Objekts für den Namen einen anderen Wert angeben als eine leere Zeichenfolge, wird das resultierende **QueryDef**-Objekt automatisch an die **[QueryDefs](querydefs-collection-dao.md)** -Auflistung angefügt.

Wenn das durch Name angegebene Objekt bereits ein Mitglied der **QueryDefs** -Auflistung ist, tritt ein Laufzeitfehler. Sie können eine temporäre **QueryDef-Objekt** erstellen, indem Sie eine leere Zeichenfolge für das Namenargument verwenden, wenn Sie die **CreateQueryDef** -Methode ausführen. Sie können aber auch die **[Name](connection-name-property-dao.md)** -Eigenschaft eines neu erstellten **QueryDef**-Objekts auf eine leere Zeichenfolge ("") festlegen. Temporäre **QueryDef**-Objekte sind nützlich, wenn Sie dynamische SQL-Anweisungen mehrmals verwenden möchten, ohne dass Sie neue permanente Objekte in der **QueryDefs**-Auflistung erstellen müssen. Sie können ein temporäres **QueryDef**-Objekt nicht an jede Auflistung anfügen, da eine leere Zeichenfolge kein gültiger Name für ein permanentes **QueryDef**-Objekt ist. Sie haben jedoch immer die Möglichkeit, die **Name**- und **SQL**-Eigenschaften des neu erstellten **QueryDef**-Objekts festzulegen und anschließend das **QueryDef**-Objekt an die **QueryDefs**-Auflistung anzufügen.

Verwenden Sie zum Ausführen der SQL-Anweisung in einem **QueryDef**-Objekt die **[Execute](connection-execute-method-dao.md)** - oder **[OpenRecordset](connection-openrecordset-method-dao.md)** -Methode.

Das Verwenden eines **QueryDef**-Objekts ist die empfohlene Methode für SQL Pass-Through-Abfragen in ODBC-Datenbanken.

Verwenden Sie die ****Delete**** -Methode für die Auflistung, um ein [QueryDef](fields-delete-method-dao.md)-Objekt aus einer **QueryDefs**-Auflistung in einer Microsoft Access-Datenbank zu entfernen.

