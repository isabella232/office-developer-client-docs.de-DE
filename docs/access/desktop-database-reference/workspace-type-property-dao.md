---
title: Workspace.Type-Eigenschaft (DAO)
TOCTitle: Type Property
ms:assetid: 89e59280-d2cd-b6a2-16c5-9f14f42fdd99
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197086(v=office.15)
ms:contentKeyID: 48546177
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 1d96bfc50d6dd653d667660ca48da84150fdbca1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59588563"
---
# <a name="workspacetype-property-dao"></a>Workspace.Type-Eigenschaft (DAO)


**Gilt für**: Access 2013, Office 2013

Legt einen Wert fest, der den Funktions- oder Datentyp eines Objekts angibt, oder gibt diesen Wert zurück. Schreibgeschützter **Integer**-Wert.

## <a name="syntax"></a>Syntax

*expression* .Type

*Ausdruck* Eine Variable, die ein **Workspace**-Objekt darstellt.

## <a name="remarks"></a>HinwBemerkungeneise

Ein **Workspace**-Objekt kann folgende Einstellungen und Rückgabewerte haben.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Konstante</p></th>
<th><p>Arbeitsbereichtyp</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>dbUseJet</strong></p></td>
<td><p>Der <strong>Arbeitsbereich</strong> ist mit der Microsoft Access-Datenbank-Engine verbunden.</p></td>
</tr>
<tr class="even">
<td><p><strong>dbUseODBC</strong></p></td>
<td><p>Der <strong>Arbeitsbereich</strong> ist mit einer ODBC-Datenquelle verbunden.</p></td>
</tr>
</tbody>
</table>

