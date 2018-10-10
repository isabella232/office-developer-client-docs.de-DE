---
title: Recordset.Type Property (DAO)
TOCTitle: Type Property
ms:assetid: d841b088-50bf-16d9-33e0-2140050e1ac6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835080(v=office.15)
ms:contentKeyID: 48548030
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f56af1af04ea2cbd603a2f4a0c71bc8e67e5be51
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25472630"
---
# <a name="recordsettype-property-dao"></a>Recordset.Type Property (DAO)


**Betrifft**: Access 2013 | Office 2013

Legt einen Wert fest, der den Funktions- oder Datentyp eines Objekts angibt, oder gibt diesen Wert zurück. Schreibgeschützter **Integer**-Wert.

## <a name="syntax"></a>Syntax

*Ausdruck* . Typ

*Ausdruck* Eine Variable, die ein **Recordset** -Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

Ein **Recordset**-Objekt kann folgende Einstellungen und Rückgabewerte haben.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Konstante</p></th>
<th><p>Typ der Datensatzgruppe</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Übergeben</strong></p></td>
<td><p>Tabelle (nur Microsoft Access-Arbeitsbereiche)</p></td>
</tr>
<tr class="even">
<td><p><strong>dbOpenDynamic</strong></p></td>
<td><p>Dynamisch (nur ODBCDirect-Arbeitsbereiche)</p>

> [!NOTE]
> <P>[!HINWEIS] ODBCDirect-Arbeitsbereiche werden in Microsoft Access 2013 nicht unterstützt. Verwenden Sie ADO, wenn Sie auf externe Datenquellen zugreifen möchten, ohne das Microsoft Access-Datenbankmodul zu verwenden.</P>


<p></p></td>
</tr>
<tr class="odd">
<td><p><strong>dbOpenDynaset</strong></p></td>
<td><p>Dynaset</p></td>
</tr>
<tr class="even">
<td><p><strong>dbOpenSnapshot</strong></p></td>
<td><p>Snapshot</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbOpenForwardOnly</strong></p></td>
<td><p>Vorwärtsgerichtet</p></td>
</tr>
</tbody>
</table>

