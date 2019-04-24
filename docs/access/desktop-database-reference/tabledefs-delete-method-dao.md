---
title: TableDefs. Delete-Methode (DAO)
TOCTitle: Delete Method
ms:assetid: 130bb50d-17c3-b2ab-9360-0d91d0cee131
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845419(v=office.15)
ms:contentKeyID: 48543358
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 63f543fd86e309372e0432c3e45513cd9d3942ab
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32313993"
---
# <a name="tabledefsdelete-method-dao"></a>TableDefs. Delete-Methode (DAO)

**Gilt für**: Access 2013, Office 2013

Löscht das angegebene **TableDef**-Objekt aus der **TableDefs**-Auflistung.

## <a name="syntax"></a>Syntax

*Ausdruck* . Delete (***Name***)

*Ausdruck* Eine Variable, die ein **Tabledefs** -Objekt darstellt.

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
<td><p><em>Name</em></p></td>
<td><p>Erforderlich</p></td>
<td><p><strong>String</strong></p></td>
<td><p>Der Name des zu löschenden TableDef-Objekts.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Bemerkungen

Die Delete-Methode wird nur unterstützt, wenn das **TableDef** -Objekt neu ist und nicht an die Datenbank angefügt wurde oder wenn die **aktualisierbare** Eigenschaft des **TableDef** auf **true**festgelegt ist.

