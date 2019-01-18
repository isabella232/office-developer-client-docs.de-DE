---
title: Properties.Append-Methode (DAO)
TOCTitle: Append Method
ms:assetid: 47f1e24f-975c-3fdc-5c3c-8c91f2920c81
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193232(v=office.15)
ms:contentKeyID: 48544609
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 528809495ebefd15a8895b15a9d51f84e6892980
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28722746"
---
# <a name="propertiesappend-method-dao"></a>Properties.Append-Methode (DAO)

**Betrifft**: Access 2013, Office 2013

Fügt der **Properties**-Auflistung ein neues **Property**-Objekt hinzu.

## <a name="syntax"></a>Syntax

*Ausdruck* . Fügen Sie (***Objekt***)

*Ausdruck* Eine Variable, die ein **Properties** -Objekt darstellt.

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

