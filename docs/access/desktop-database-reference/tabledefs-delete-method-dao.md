---
title: TableDefs.Delete-Methode (DAO)
TOCTitle: Delete Method
ms:assetid: 130bb50d-17c3-b2ab-9360-0d91d0cee131
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845419(v=office.15)
ms:contentKeyID: 48543358
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: b7c4c2176f43a6ae586131ad44567208ff7c0ae5
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59621717"
---
# <a name="tabledefsdelete-method-dao"></a>TableDefs.Delete-Methode (DAO)

**Gilt für**: Access 2013, Office 2013

Löscht das angegebene **TableDef**-Objekt aus der **TableDefs**-Auflistung.

## <a name="syntax"></a>Syntax

*Ausdruck* . Delete(***Name***)

*Ausdruck* Eine Variable, die ein **TableDefs-Objekt** darstellt.

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

Die Delete -Methode wird nur unterstützt, wenn das **TableDef** -Objekt neu ist und nicht an die Datenbank angefügt wurde, oder wenn die **Updatable** -Eigenschaft der **TableDef** auf **True** festgelegt ist.

