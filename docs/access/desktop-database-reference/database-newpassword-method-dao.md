---
title: Database.NewPassword Method (DAO)
TOCTitle: NewPassword Method
ms:assetid: 01c1c454-d651-222c-225a-2b02734a1b7a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844754(v=office.15)
ms:contentKeyID: 48542941
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052943
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 892dc16d0422572e83f92316ce2c1c67f9ce5cc0
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25860644"
---
# <a name="databasenewpassword-method-dao"></a>Database.NewPassword Method (DAO)


**Betrifft**: Access 2013 | Office 2013

Ändert das Kennwort einer vorhandenen Microsoft Access-Datenbank (gilt nur für Microsoft Access-Arbeitsbereiche).

## <a name="syntax"></a>Syntax

*Ausdruck* . NewPassword (***BstrOld***, ***BstrNew***)

*Ausdruck* Ein Ausdruck, der ein **Database** -Objekt zurückgibt.

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
<td><p>bstrOld</p></td>
<td><p>Erforderlich</p></td>
<td><p><strong>String</strong></p></td>
<td><p>Die aktuelle Einstellung der <strong>Password</strong>-Eigenschaft des <strong>Database</strong>-Objekts.</p></td>
</tr>
<tr class="even">
<td><p>bstrNew</p></td>
<td><p>Erforderlich</p></td>
<td><p><strong>String</strong></p></td>
<td><p>Die neue Einstellung der <strong>Password</strong> -Eigenschaft des <strong>Database</strong> -Objekts.</p>

> [!NOTE]
> Verwenden Sie sichere Kennwörter, die Groß- und Kleinbuchstaben, Ziffern und Symbole kombinieren. Schwache Kennwörter enthalten keine Kombination dieser Elemente. Sicheres Kennwort: Y6dh!et5. Schwaches Kennwort: House27. Verwenden Sie ein sicheres Kennwort, das Sie sich merken können, damit Sie es nicht aufschreiben müssen.


</td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Hinweise

Die Zeichenfolgen BstrOld und BstrNew können bis zu 20 Zeichen lang sein und alle Zeichen außer ASCII-Zeichen, 0 (null) enthalten. Das Kennwort verwenden, um eine leere Zeichenfolge ("") für BstrNew.

Bei Kennwörtern wird Groß-/Kleinschreibung beachtet.

Wurde für eine Datenbank kein Kennwort festgelegt, erstellt das Microsoft Access-Datenbankmodul automatisch ein Kennwort, indem es eine leere Zeichenfolge ("") für das alte Kennwort übergibt.


> [!IMPORTANT]
> [!WICHTIG] Wenn Sie das Kennwort verlieren, können Sie die Datenbank nicht mehr öffnen.


