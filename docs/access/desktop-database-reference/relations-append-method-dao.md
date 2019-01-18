---
title: Relations.Append-Methode (DAO)
TOCTitle: Append Method
ms:assetid: dafcc7b8-b30d-2ba2-631d-eca0f882fc2d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835334(v=office.15)
ms:contentKeyID: 48548094
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052904
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: b8374832ad6cd6bac30fa9d129e54fb6ab4c8fd4
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718847"
---
# <a name="relationsappend-method-dao"></a>Relations.Append-Methode (DAO)

**Betrifft**: Access 2013, Office 2013

Fügt der **Relations**-Auflistung ein neues **Relation**-Objekt hinzu.

## <a name="syntax"></a>Syntax

*Ausdruck* . Fügen Sie (***Objekt***)

*Ausdruck* Eine Variable, die ein **Relations** -Objekt darstellt.

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
<th><p>Erforderlich oder optional</p></th>
<th><p>Datentyp</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Object</em></p></td>
<td><p>Erforderlich</p></td>
<td><p><strong>Objekt</strong></p></td>
<td><p>Eine Objektvariable, die das Feld darstellt, das an die Auflistung angefügt wird.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Bemerkungen

Das angefügte Objekt wird zu einem beständigen Objekt und auf einem Datenträger gespeichert, bis Sie es mithilfe der **Delete**-Methode löschen.

Das Hinzufügen eines neuen Objekts geschieht ohne Verzögerung. Trotzdem sollten Sie die **Refresh**-Methode auf alle weiteren Auflistungen anwenden, die von Änderungen an der Datenbankstruktur betroffen sein könnten.

Wenn das Objekt an die, das Sie anfügen möchten (beispielsweise wenn Sie, alle **Field** -Objekte **Fields** -Auflistung eines **Index** -Objekts angefügt haben, bevor es an eine **Indexes** -Auflistung angehängt wird) abgeschlossen ist oder wenn die Eigenschaften in einem oder mehreren festlegen untergeordnete Objekte sind falsch ist, verwenden die **Append** -Methode einen Fehler verursacht. Angenommen, wenn Sie keinen Feldtyp angegeben und versuchen Sie es dann das **Field** -Objekt an die **Fields** -Auflistung in ein **TableDef** -Objekt angefügt werden soll, löst mit der **Append** -Methode einen Laufzeitfehler.

