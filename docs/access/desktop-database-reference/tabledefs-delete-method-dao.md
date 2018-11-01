---
title: TableDefs.Delete Method (DAO)
TOCTitle: Delete Method
ms:assetid: 130bb50d-17c3-b2ab-9360-0d91d0cee131
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845419(v=office.15)
ms:contentKeyID: 48543358
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: bc4d0c467d80c0eb78ea75f36b87e97ce3551631
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25887187"
---
# <a name="tabledefsdelete-method-dao"></a>TableDefs.Delete Method (DAO)


**Betrifft**: Access 2013, Office 2013

Löscht das angegebene **TableDef**-Objekt aus der **TableDefs**-Auflistung.

## <a name="syntax"></a>Syntax

*Ausdruck* . Löschen Sie die (***Name***)

*Ausdruck* Eine Variable, die ein **TableDefs** -Objekt darstellt.

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
<td><p>Der Name des zu löschenden TableDef-Objekts.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Bemerkungen

Die Delete-Methode wird nur dann unterstützt, wenn das TableDef-Objekt neu ist und noch nicht an die Datenbank angefügt wurde, oder wenn die Updatable-Eigenschaft des TableDef-Objekts auf True festgelegt ist.

