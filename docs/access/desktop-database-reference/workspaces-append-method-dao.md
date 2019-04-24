---
title: Workspaces. Append-Methode (DAO)
TOCTitle: Append Method
ms:assetid: 195c26a6-a1d1-40a8-7e7e-13cd632008b6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845644(v=office.15)
ms:contentKeyID: 48543498
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 11d721d58301d2adb33b2e381d88d7245531ff06
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302492"
---
# <a name="workspacesappend-method-dao"></a>Workspaces. Append-Methode (DAO)

**Gilt für**: Access 2013, Office 2013

Fügt der **Workspaces**-Auflistung ein neues **Workspace**-Objekt hinzu.

## <a name="syntax"></a>Syntax

*Ausdruck* . Append (***Objekt***)

*Ausdruck* Eine Variable, die ein **Workspaces** -Objekt darstellt.

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

Wenn das Objekt, das Sie anfügen, nicht vollständig ist (beispielsweise, wenn Sie keine **Field** -Objekte an eine **Fields** -Auflistung eines **Index** -Objekts angefügt haben, **** bevor es an eine Indexes-Auflistung angefügt wird) oder wenn die Eigenschaften, die in einem oder mehreren festgelegt sind untergeordnete Objekte sind falsch, bei Verwendung der **Append** -Methode wird ein Fehler verursacht. Wenn Sie beispielsweise noch keinen Feldtyp angegeben haben und dann versuchen, das **Field** -Objekt an die **Fields** -Auflistung in einem **TableDef** -Objekt anzufügen, löst mithilfe der **Append** -Methode ein Laufzeitfehler aus.

