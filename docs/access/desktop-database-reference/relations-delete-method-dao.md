---
title: Relations.Delete-Methode (DAO)
TOCTitle: Delete Method
ms:assetid: e95408d2-9dde-44e7-875e-8f2d4b837cf6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836064(v=office.15)
ms:contentKeyID: 48548438
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e0b7fbf20a8732e8f4db525fd32bf4e5737b4d79
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28716432"
---
# <a name="relationsdelete-method-dao"></a>Relations.Delete-Methode (DAO)

**Betrifft**: Access 2013, Office 2013

Löscht das angegebene **Relation**-Objekt aus der **Relations**-Auflistung.

## <a name="syntax"></a>Syntax

*Ausdruck* . Löschen Sie die (***Name***)

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
<td><p><em>Name</em></p></td>
<td><p>Erforderlich</p></td>
<td><p><strong>String</strong></p></td>
<td><p>Der Name der zu löschenden Beziehung.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Bemerkungen

Die **Delete**-Methode wird nur unterstützt, wenn es sich bei dem **Relation**-Objekt um ein neues Objekt handelt, das noch nicht angefügt wurde.

