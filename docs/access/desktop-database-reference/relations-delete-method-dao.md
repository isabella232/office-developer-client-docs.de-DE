---
title: Relations.Delete Method (DAO)
TOCTitle: Delete Method
ms:assetid: e95408d2-9dde-44e7-875e-8f2d4b837cf6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836064(v=office.15)
ms:contentKeyID: 48548438
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6b228c21931131023d58efc91d0087ad76ca3b61
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25473593"
---
# <a name="relationsdelete-method-dao"></a>Relations.Delete Method (DAO)


**Betrifft**: Access 2013 | Office 2013

Löscht das angegebene **Relation**-Objekt aus der **Relations**-Auflistung.

## <a name="syntax"></a>Syntax

*Ausdruck* . Löschen Sie die (***Name***)

*Ausdruck* Eine Variable, die ein **Relations** -Objekt darstellt.

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
<td><p>Erforderlich</p></td>
<td><p><strong>String</strong></p></td>
<td><p>Der Name der zu löschenden Beziehung.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Bemerkungen

Die **Delete**-Methode wird nur unterstützt, wenn es sich bei dem **Relation**-Objekt um ein neues Objekt handelt, das noch nicht angefügt wurde.

