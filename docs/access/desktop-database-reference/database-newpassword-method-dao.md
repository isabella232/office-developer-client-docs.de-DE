---
title: Database.NewPassword-Methode (DAO)
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
ms.openlocfilehash: e72d879482c3ed69b262f2f4d0f07a4e11f8fa4c
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998938"
---
# <a name="databasenewpassword-method-dao"></a>Database.NewPassword-Methode (DAO)

**Betrifft**: Access 2013, Office 2013

Ändert das Kennwort einer vorhandenen Microsoft Access-Datenbank (gilt nur für Microsoft Access-Arbeitsbereiche).

## <a name="syntax"></a>Syntax

*Ausdruck* . NewPassword (***BstrOld***, ***BstrNew***)

*Ausdruck* Ein Ausdruck, der ein **Database** -Objekt zurückgibt.

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
<td><p><em>bstrOld</em></p></td>
<td><p>Erforderlich</p></td>
<td><p><strong>String</strong></p></td>
<td><p>Die aktuelle Einstellung der <strong>Password</strong>-Eigenschaft des <strong>Database</strong>-Objekts.</p></td>
</tr>
<tr class="even">
<td><p><em>bstrNew</em></p></td>
<td><p>Erforderlich</p></td>
<td><p><strong>String</strong></p></td>
<td><p>Die neue Einstellung der <strong>Password</strong> -Eigenschaft des <strong>Database</strong> -Objekts.</p>
<p><strong>Hinweis</strong>: Verwenden Sie sichere Kennwörter, die Groß- und Kleinbuchstaben, Zahlen und Symbole kombinieren. Unsichere Kennwörter enthalten keine Kombination dieser Elemente. Sicheres Kennwort: Y6dh!et5. Unsicheres Kennwort: Haus27. Verwenden Sie ein sicheres Kennwort, das Sie sich gut merken können, damit Sie es nicht aufschreiben müssen.</p>
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


