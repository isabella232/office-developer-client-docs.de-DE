---
title: Database. neuPassword-Methode (DAO)
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
localization_priority: Normal
ms.openlocfilehash: 20f09dbfba50526409472f7eb804ba2c47e4d1d5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294855"
---
# <a name="databasenewpassword-method-dao"></a>Database. neuPassword-Methode (DAO)

**Gilt für**: Access 2013, Office 2013

Ändert das Kennwort einer vorhandenen Microsoft Access-Datenbank (gilt nur für Microsoft Access-Arbeitsbereiche).

## <a name="syntax"></a>Syntax

*Ausdruck* . Neues Kennwort (***bstrOld***, ***bstrNew***)

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
<th><p>Erforderlich/optional</p></th>
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
<p><strong>Hinweis</strong>: Verwenden Sie sichere Kennwörter, die Groß-und Kleinbuchstaben, Zahlen und Symbole kombinieren. Unsichere Kennwörter kombinieren diese Elemente nicht. Sicheres Kennwort: Y6dh!et5. Schwaches Kennwort: House27. Verwenden Sie ein sicheres Kennwort, das Sie sich merken können, damit Sie es nicht aufschreiben müssen.</p>
</td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Bemerkungen

Die Zeichenfolgen bstrOld und bstrNew können bis zu 20 Zeichen lang sein und alle Zeichen mit Ausnahme des ASCII-Zeichens 0 (null) enthalten. Verwenden Sie zum Löschen des Kennworts eine leere Zeichenfolge ("") für bstrNew.

Bei Kennwörtern wird Groß-/Kleinschreibung beachtet.

Wurde für eine Datenbank kein Kennwort festgelegt, erstellt das Microsoft Access-Datenbankmodul automatisch ein Kennwort, indem es eine leere Zeichenfolge ("") für das alte Kennwort übergibt.


> [!IMPORTANT]
> [!WICHTIG] Wenn Sie das Kennwort verlieren, können Sie die Datenbank nicht mehr öffnen.


