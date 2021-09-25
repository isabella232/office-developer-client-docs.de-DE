---
title: Indexes.Append-Methode (DAO)
TOCTitle: Append Method
ms:assetid: 60dce80f-505b-e988-3ac1-8ecaae3d3d09
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194835(v=office.15)
ms:contentKeyID: 48545191
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 6285970247b544b0f79937b64601aa4692510c99
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59572970"
---
# <a name="indexesappend-method-dao"></a>Indexes.Append-Methode (DAO)

**Gilt für**: Access 2013, Office 2013

Fügt der **Indexes**-Auflistung ein neues **Index**-Objekt hinzu.

## <a name="syntax"></a>Syntax

*expression* .Append(***Object***)

*Ausdruck* Eine Variable, die ein **Indexes** -Objekt darstellt.

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
<td><p><em>Objekt</em></p></td>
<td><p>Erforderlich</p></td>
<td><p><strong>Objekt</strong></p></td>
<td><p>Eine Objektvariable, die das Element darstellt, das an die Auflistung angefügt wird.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>HinwBemerkungeneise

Das angefügte Objekt wird zu einem beständigen Objekt und auf einem Datenträger gespeichert, bis Sie es mithilfe der **Delete**-Methode löschen.

Das Hinzufügen eines neuen Objekts geschieht ohne Verzögerung. Trotzdem sollten Sie die **Refresh**-Methode auf alle weiteren Auflistungen anwenden, die von Änderungen an der Datenbankstruktur betroffen sein könnten.

Falls das angefügte Objekt nicht vollständig ist (wenn Sie beispielsweise noch keine **Field**-Objekte an eine **Fields**-Auflistung eines **Index**-Objekts angefügt haben, bevor es an eine **Indexes**-Auflistung angefügt wird) bzw. die in mindestens einem untergeordneten Objekt festgelegten Eigenschaften falsch sind, wird mit der **Append**-Methode ein Fehler verursacht. Angenommen, Sie haben keinen Feldtyp angegeben und versuchen dann, das **Field**-Objekt an die **Fields**-Auflistung in einem **TableDef**-Objekt anzufügen, dann löst das Anwenden der **Append**-Methode einen Laufzeitfehler aus.

