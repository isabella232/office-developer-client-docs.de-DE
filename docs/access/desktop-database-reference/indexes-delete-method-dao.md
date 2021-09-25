---
title: Indexes.Delete-Methode (DAO)
TOCTitle: Delete Method
ms:assetid: 8d3c3221-3b2e-15ba-32ff-f2dfc592d82c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197351(v=office.15)
ms:contentKeyID: 48546252
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: ed6fa376b4e0205f33ee5515d908c810f4b4b31d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59615332"
---
# <a name="indexesdelete-method-dao"></a>Indexes.Delete-Methode (DAO)

**Gilt für**: Access 2013, Office 2013

Löscht das angegebene **Index**-Objekt aus der **Indexes**-Auflistung.

## <a name="syntax"></a>Syntax

*Ausdruck* . Delete(***Name***)

*Ausdruck* Eine Variable, die ein **Indexes** -Objekt darstellt.

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
<td><p>Der Name des zu löschenden Index.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Bemerkungen

Die **Delete**-Methode wird nur unterstützt, wenn das **Index**-Objekt neu ist und noch nicht an die Datenbank angefügt wurde.

