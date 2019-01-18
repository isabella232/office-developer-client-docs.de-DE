---
title: Field2.CollatingOrder-Eigenschaft (DAO)
TOCTitle: CollatingOrder Property
ms:assetid: cb1d6fc9-a2a6-54c2-abf5-48b609e38738
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834380(v=office.15)
ms:contentKeyID: 48547709
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 02711fbbf39b058bb88e9568716169825ae4a923
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28700731"
---
# <a name="field2collatingorder-property-dao"></a>Field2.CollatingOrder-Eigenschaft (DAO)


**Betrifft**: Access 2013, Office 2013

Gibt einen Wert zurück, der die Sequenz der Sortierreihenfolge im Text für den Zeichenfolgenvergleich oder die Sortierung angibt (gilt nur für Microsoft Access-Arbeitsbereiche). Schreibgeschützter **Long**-Wert.

## <a name="syntax"></a>Syntax

*Ausdruck* . CollatingOrder

*Ausdruck* Eine Variable, die ein **Field2** -Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

Der Rückgabewert ist ein **Long**-Wert oder eine Konstante, die einem der folgenden Werte entsprechen kann.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Konstante</p></th>
<th><p>Sortierreihenfolge</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>dbSortGeneral</strong></p></td>
<td><p>Allgemein (Englisch, Französisch, Deutsch, Portugiesisch, Italienisch und modernes Spanisch)</p></td>
</tr>
<tr class="even">
<td><p><strong>dbSortArabic</strong></p></td>
<td><p>Arabisch</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbSortChineseSimplified</strong></p></td>
<td><p>Chinesisch (Vereinfacht)</p></td>
</tr>
<tr class="even">
<td><p><strong>dbSortChineseTraditional</strong></p></td>
<td><p>Chinesisch (Traditionell)</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbSortCyrillic</strong></p></td>
<td><p>Russisch</p></td>
</tr>
<tr class="even">
<td><p><strong>dbSortCzech</strong></p></td>
<td><p>Tschechisch</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbSortDutch</strong></p></td>
<td><p>Niederländisch</p></td>
</tr>
<tr class="even">
<td><p><strong>dbSortGreek</strong></p></td>
<td><p>Griechisch</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbSortHebrew</strong></p></td>
<td><p>Hebräisch</p></td>
</tr>
<tr class="even">
<td><p><strong>dbSortHungarian</strong></p></td>
<td><p>Ungarisch</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbSortIcelandic</strong></p></td>
<td><p>Isländisch</p></td>
</tr>
<tr class="even">
<td><p><strong>dbSortJapanese</strong></p></td>
<td><p>Japanisch</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbSortKorean</strong></p></td>
<td><p>Koreanisch</p></td>
</tr>
<tr class="even">
<td><p><strong>dbSortNeutral</strong></p></td>
<td><p>Neutral</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbSortNorwDan</strong></p></td>
<td><p>Norwegisch oder Dänisch</p></td>
</tr>
<tr class="even">
<td><p><strong>dbSortPDXIntl</strong></p></td>
<td><p>Paradox International</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbSortPDXNor</strong></p></td>
<td><p>Paradox Norwegisch oder Dänisch</p></td>
</tr>
<tr class="even">
<td><p><strong>dbSortPDXSwe</strong></p></td>
<td><p>Paradox Schwedisch oder Finnisch</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbSortPolish</strong></p></td>
<td><p>Polnisch</p></td>
</tr>
<tr class="even">
<td><p><strong>dbSortSlovenian</strong></p></td>
<td><p>Slowenisch</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbSortSpanish</strong></p></td>
<td><p>Spanisch</p></td>
</tr>
<tr class="even">
<td><p><strong>dbSortSwedFin</strong></p></td>
<td><p>Schwedisch oder Finnisch</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbSortThai</strong></p></td>
<td><p>Thailändisch</p></td>
</tr>
<tr class="even">
<td><p><strong>dbSortTurkish</strong></p></td>
<td><p>Türkisch</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbSortUndefined</strong></p></td>
<td><p>Nicht definiert oder unbekannt</p></td>
</tr>
</tbody>
</table>


Die Verfügbarkeit der **CollatingOrder**-Eigenschaft hängt vom Objekt ab, in dem die **Fields**-Auflistung enthalten ist (siehe folgende Tabelle).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Zugehörigkeit der Fields-Auflistung</p></th>
<th><p>Verfügbarkeit von CollatingOrder</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Index</strong>-Objekt</p></td>
<td><p>Nicht unterstützt</p></td>
</tr>
<tr class="even">
<td><p><strong>QueryDef</strong> -Objekt</p></td>
<td><p>Schreibgeschützt.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Recordset</strong> -Objekt</p></td>
<td><p>Schreibgeschützt.</p></td>
</tr>
<tr class="even">
<td><p><strong>Relation</strong> -Objekt</p></td>
<td><p>Nicht unterstützt</p></td>
</tr>
<tr class="odd">
<td><p><strong>TableDef</strong>-Objekt</p></td>
<td><p>Schreibgeschützt.</p></td>
</tr>
</tbody>
</table>


Die Einstellung der **CollatingOrder** -Eigenschaft entspricht dem Argument Locale der **CreateDatabase** -Methode, wenn die Datenbank erstellt wurde oder der **CompactDatabase** -Methode, wenn die Datenbank kürzlich komprimiert wurde.

Die Einstellungen der Eigenschaften **CollatingOrder** und **Attributes** eines **Field2**-Objekts in einer **Fields**-Auflistung eines **Index** bestimmen zusammen die Sequenz und Richtung der Sortierreihenfolge in einem Index. Die Sortierreihenfolge kann nicht für einen einzelnen Index festgelegt werden, sondern nur für eine gesamte Tabelle.

