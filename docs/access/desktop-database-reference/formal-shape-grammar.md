---
title: Formal Shape Grammar
TOCTitle: Formal shape grammar
ms:assetid: a3220569-8804-3dc3-7f9f-b4f8cdab1316
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249752(v=office.15)
ms:contentKeyID: 48546774
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d30ff9146146bb0457a5aa383b2b720a4fdaeb78
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28708046"
---
# <a name="formal-shape-grammar"></a>Formal Shape Grammar

**Betrifft**: Access 2013, Office 2013

Dies ist die formale Grammatik zum Erstellen von Shape-Befehlen:

  - Erforderliche Grammatikbegriffe sind Textzeichenfolgen, die durch spitze Klammern ("\<\>") getrennt sind.

  - Optionale Begriffe werden getrennt in eckigen Klammern ("\[ \]").

  - Alternativen werden durch einen Schrägstrich ("|") angegeben.

  - Wiederholte Alternativen werden durch Auslassungspunkte ("...") angegeben.

  - *Alpha* wird eine Zeichenfolge aus alphabetischen Buchstaben angegeben.

  - *Digit* wird eine Zeichenfolge aus Zahlen angegeben.

  - *Unicode-Digit* wird eine Zeichenfolge aus Unicode-Ziffern angegeben.

Alle andere Begriffe sind Literale.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Begriff</p></th>
<th><p>Definition</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>&lt;Shape-Befehl&gt;</p></td>
<td><p>SHAPE [&lt;Tabelle exp&gt; [[AS] &lt;Alias&gt;]] [&lt;Shape-Aktion&gt;]</p></td>
</tr>
<tr class="even">
<td><p>&lt;Tabelle exp&gt;</p></td>
<td><p>{&lt;Anbieter Befehlstext&gt;} |<br />
(&lt;Shape-Befehl&gt;) |<br />
Tabelle &lt;quoted-Name&gt; |<br />
&lt;Quoted-name&gt;</p></td>
</tr>
<tr class="odd">
<td><p>&lt;Shape-Aktion&gt;</p></td>
<td><p>APPEND &lt;Alias-Feldliste&gt; |</p>
<p>BERECHNEN &lt;Alias Feldliste&gt; [BY &lt;-Feldliste&gt;]</p></td>
</tr>
<tr class="even">
<td><p>&lt;Alias-Feldliste&gt;</p></td>
<td><p>&lt;Alias-Feld&gt; [, &lt;mit Aliasing-Feld &gt;]</p></td>
</tr>
<tr class="odd">
<td><p>&lt;Alias-Feld&gt;</p></td>
<td><p>&lt;Feld exp&gt; [[AS] &lt;Alias&gt;]</p></td>
</tr>
<tr class="even">
<td><p>&lt;Feld exp&gt;</p></td>
<td><p>(&lt;Relation exp&gt;) |</p>
<p>&lt;berechnet exp&gt; |</p>
<p>&lt;Aggregat-exp&gt; |</p>
<p>&lt;neue exp&gt;</p></td>
</tr>
<tr class="odd">
<td><p>&lt;relation_exp&gt;</p></td>
<td><p>&lt;Tabelle exp&gt; [[AS] &lt;Alias&gt;]</p>
<p>&lt;Tabelle exp&gt; [[AS] &lt;Alias&gt;]</p></td>
</tr>
<tr class="even">
<td><p>&lt;Relation-Cond-Liste&gt;</p></td>
<td><p>&lt;Relation Cond&gt; [, &lt;Relation Cond&gt;...]</p></td>
</tr>
<tr class="odd">
<td><p>&lt;Relation cond&gt;</p></td>
<td><p>&lt;Name des Felds&gt; an &lt;untergeordneten Ref&gt;</p></td>
</tr>
<tr class="even">
<td><p>&lt;untergeordnete ref&gt;</p></td>
<td><p>&lt;Name des Felds&gt; |</p>
<p>PARAMETER &lt;Param-Ref&gt;</p></td>
</tr>
<tr class="odd">
<td><p>&lt;Param-ref&gt;</p></td>
<td><p>&lt;number&gt;</p></td>
</tr>
<tr class="even">
<td><p>&lt;Feldliste&gt;</p></td>
<td><p>&lt;Name des Felds&gt; [, &lt;Feldnamen&gt;]</p></td>
</tr>
<tr class="odd">
<td><p>&lt;Aggregat-exp&gt;</p></td>
<td><p>SUM (&lt;qualifizierte Feldname&gt;) |</p>
<p>AVG (&lt;qualifizierte Feldname&gt;) |</p>
<p>MIN (&lt;qualifizierte Feldname&gt;) |</p>
<p>MAX (&lt;qualifizierte Feldname&gt;) |</p>
<p>COUNT (&lt;qualifizierte Alias&gt; | &lt;qualifizierten Namen&gt;) |</p>
<p>STDEV (&lt;qualifizierte Feldname&gt;) |</p>
<p>Alle (&lt;qualifizierte Feldname&gt;)</p></td>
</tr>
<tr class="even">
<td><p>&lt;berechnet exp&gt;</p></td>
<td><p>CALC(&lt;Ausdruck&gt;)</p></td>
</tr>
<tr class="odd">
<td><p>&lt;qualifizierte Feldname&gt;</p></td>
<td><p>&lt;Alias&gt;. [&lt;Alias&gt;...] &lt;Feldnamen&gt;</p></td>
</tr>
<tr class="even">
<td><p>&lt;Alias&gt;</p></td>
<td><p>&lt;Quoted-name&gt;</p></td>
</tr>
<tr class="odd">
<td><p>&lt;Name des Felds&gt;</p></td>
<td><p>&lt;Quoted-Name&gt; [[AS] &lt;Alias&gt;]</p></td>
</tr>
<tr class="even">
<td><p>&lt;Quoted-name&gt;</p></td>
<td><p>&quot;&lt;Zeichenfolge&gt;&quot; |</p>
<p>'&lt;Zeichenfolge&gt;' |</p>
<p>[&lt;Zeichenfolge&gt;] |</p>
<p>&lt;Name&gt;</p></td>
</tr>
<tr class="odd">
<td><p>&lt;Vollständiger name&gt;</p></td>
<td><p>Alias [.alias...]</p></td>
</tr>
<tr class="even">
<td><p>&lt;Name&gt;</p></td>
<td><p>Alpha [Alpha | Ziffer | _ | # |: |...]</p></td>
</tr>
<tr class="odd">
<td><p>&lt;number&gt;</p></td>
<td><p>Ziffer [Ziffer...]</p></td>
</tr>
<tr class="even">
<td><p>&lt;neue exp&gt;</p></td>
<td><p>NEUE &lt;Feldtyp&gt; [(&lt;Anzahl&gt; [, &lt;Anzahl&gt;])]</p></td>
</tr>
<tr class="odd">
<td><p>&lt;Feldtyp&gt;</p></td>
<td><p>Ein OLE DB- oder ADO-Datentyp.</p></td>
</tr>
<tr class="even">
<td><p>&lt;Zeichenfolge&gt;</p></td>
<td><p>Unicode-Zeichen [Unicode-Zeichen...]</p></td>
</tr>
<tr class="odd">
<td><p>&lt;expression&gt;</p></td>
<td><p>Ein Visual Basic für Applikationen-Ausdruck, dessen Operanden andere Nicht-CALC-Spalten in der gleichen Zeile sind.</p></td>
</tr>
</tbody>
</table>

