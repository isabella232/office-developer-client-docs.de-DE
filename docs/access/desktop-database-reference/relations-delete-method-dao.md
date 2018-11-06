---
title: Relations.Delete-Methode (DAO)
TOCTitle: Delete Method
ms:assetid: e95408d2-9dde-44e7-875e-8f2d4b837cf6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836064(v=office.15)
ms:contentKeyID: 48548438
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7c7a42098bcc64a58f8a004c0f1d5a35fd4f34b7
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998924"
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

