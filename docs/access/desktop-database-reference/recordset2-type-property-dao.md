---
title: Recordset2.Type Property (DAO)
TOCTitle: Type Property
ms:assetid: 9bec543e-7f59-ea59-dc79-41d0e08b5ab6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198080(v=office.15)
ms:contentKeyID: 48546583
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052880
f1_categories:
- Office.Version=v15
ms.openlocfilehash: ee9afcd5367135da2d39fe889d17d089ae6f4c25
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25472983"
---
# <a name="recordset2type-property-dao"></a>Recordset2.Type Property (DAO)


**Betrifft**: Access 2013 | Office 2013

Legt einen Wert fest, der den Funktions- oder Datentyp eines Objekts angibt, oder gibt diesen Wert zurück. Schreibgeschützter **Integer**-Wert.

## <a name="syntax"></a>Syntax

*Ausdruck* . Typ

*Ausdruck* Eine Variable, die ein **Recordset2** -Objekt darstellt.

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

