---
title: Formale Grammatik für Formen
TOCTitle: Formal shape grammar
ms:assetid: a3220569-8804-3dc3-7f9f-b4f8cdab1316
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249752(v=office.15)
ms:contentKeyID: 48546774
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0de4f2eca0b5dd607cb9d93cc7e90f4af0ba8d89
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2018
ms.locfileid: "25945537"
---
# <a name="formal-shape-grammar"></a><span data-ttu-id="3654c-102">Formale Grammatik für Formen</span><span class="sxs-lookup"><span data-stu-id="3654c-102">Formal shape grammar</span></span>

<span data-ttu-id="3654c-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3654c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3654c-104">Dies ist die formale Grammatik zum Erstellen von Shape-Befehlen:</span><span class="sxs-lookup"><span data-stu-id="3654c-104">This is the formal grammar for creating any shape command:</span></span>

  - <span data-ttu-id="3654c-105">Erforderliche Grammatikbegriffe sind Textzeichenfolgen, die durch spitze Klammern ("\<\>") getrennt sind.</span><span class="sxs-lookup"><span data-stu-id="3654c-105">Required grammatical terms are text strings delimited by angle brackets ("\<\>").</span></span>

  - <span data-ttu-id="3654c-106">Optionale Begriffe werden getrennt in eckigen Klammern ("\[ \]").</span><span class="sxs-lookup"><span data-stu-id="3654c-106">Optional terms are delimited by square brackets ("\[ \]").</span></span>

  - <span data-ttu-id="3654c-107">Alternativen werden durch einen Schrägstrich ("|") angegeben.</span><span class="sxs-lookup"><span data-stu-id="3654c-107">Alternatives are indicated by a virgule ("|").</span></span>

  - <span data-ttu-id="3654c-108">Wiederholte Alternativen werden durch Auslassungspunkte ("...") angegeben.</span><span class="sxs-lookup"><span data-stu-id="3654c-108">Repeating alternatives are indicated by an ellipsis ("...").</span></span>

  - <span data-ttu-id="3654c-109">*Alpha* wird eine Zeichenfolge aus alphabetischen Buchstaben angegeben.</span><span class="sxs-lookup"><span data-stu-id="3654c-109">*Alpha* indicates a string of alphabetical letters.</span></span>

  - <span data-ttu-id="3654c-110">*Digit* wird eine Zeichenfolge aus Zahlen angegeben.</span><span class="sxs-lookup"><span data-stu-id="3654c-110">*Digit* indicates a string of numbers.</span></span>

  - <span data-ttu-id="3654c-111">*Unicode-Digit* wird eine Zeichenfolge aus Unicode-Ziffern angegeben.</span><span class="sxs-lookup"><span data-stu-id="3654c-111">*Unicode-digit* indicates a string of unicode digits.</span></span>

<span data-ttu-id="3654c-112">Alle andere Begriffe sind Literale.</span><span class="sxs-lookup"><span data-stu-id="3654c-112">All other terms are literals.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3654c-113">Begriff</span><span class="sxs-lookup"><span data-stu-id="3654c-113">Term</span></span></p></th>
<th><p><span data-ttu-id="3654c-114">Definition</span><span class="sxs-lookup"><span data-stu-id="3654c-114">Definition</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3654c-115">&lt;Shape-Befehl&gt;</span><span class="sxs-lookup"><span data-stu-id="3654c-115">&lt;shape-command&gt;</span></span></p></td>
<td><p><span data-ttu-id="3654c-116">SHAPE [&lt;Tabelle exp&gt; [[AS] &lt;Alias&gt;]] [&lt;Shape-Aktion&gt;]</span><span class="sxs-lookup"><span data-stu-id="3654c-116">SHAPE [&lt;table-exp&gt; [[AS] &lt;alias&gt;]][&lt;shape-action&gt;]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3654c-117">&lt;Tabelle exp&gt;</span><span class="sxs-lookup"><span data-stu-id="3654c-117">&lt;table-exp&gt;</span></span></p></td>
<td><p><span data-ttu-id="3654c-118">{&lt;Anbieter Befehlstext&gt;} |</span><span class="sxs-lookup"><span data-stu-id="3654c-118">{&lt;provider-command-text&gt;} |</span></span><br />
<span data-ttu-id="3654c-119">(&lt;Shape-Befehl&gt;) |</span><span class="sxs-lookup"><span data-stu-id="3654c-119">(&lt;shape-command&gt;) |</span></span><br />
<span data-ttu-id="3654c-120">Tabelle &lt;quoted-Name&gt; |</span><span class="sxs-lookup"><span data-stu-id="3654c-120">TABLE &lt;quoted-name&gt; |</span></span><br />
<span data-ttu-id="3654c-121">&lt;Quoted-name&gt;</span><span class="sxs-lookup"><span data-stu-id="3654c-121">&lt;quoted-name&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3654c-122">&lt;Shape-Aktion&gt;</span><span class="sxs-lookup"><span data-stu-id="3654c-122">&lt;shape-action&gt;</span></span></p></td>
<td><p><span data-ttu-id="3654c-123">APPEND &lt;Alias-Feldliste&gt; |</span><span class="sxs-lookup"><span data-stu-id="3654c-123">APPEND &lt;aliased-field-list&gt; |</span></span></p>
<p><span data-ttu-id="3654c-124">BERECHNEN &lt;Alias Feldliste&gt; [BY &lt;-Feldliste&gt;]</span><span class="sxs-lookup"><span data-stu-id="3654c-124">COMPUTE &lt;aliased-field-list&gt; [BY &lt;field-list&gt;]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3654c-125">&lt;Alias-Feldliste&gt;</span><span class="sxs-lookup"><span data-stu-id="3654c-125">&lt;aliased-field-list&gt;</span></span></p></td>
<td><p><span data-ttu-id="3654c-126">&lt;Alias-Feld&gt; [, &lt;mit Aliasing-Feld &gt;]</span><span class="sxs-lookup"><span data-stu-id="3654c-126">&lt;aliased-field&gt; [, &lt;aliased-field...&gt;]</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3654c-127">&lt;Alias-Feld&gt;</span><span class="sxs-lookup"><span data-stu-id="3654c-127">&lt;aliased-field&gt;</span></span></p></td>
<td><p><span data-ttu-id="3654c-128">&lt;Feld exp&gt; [[AS] &lt;Alias&gt;]</span><span class="sxs-lookup"><span data-stu-id="3654c-128">&lt;field-exp&gt; [[AS] &lt;alias&gt;]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3654c-129">&lt;Feld exp&gt;</span><span class="sxs-lookup"><span data-stu-id="3654c-129">&lt;field-exp&gt;</span></span></p></td>
<td><p><span data-ttu-id="3654c-130">(&lt;Relation exp&gt;) |</span><span class="sxs-lookup"><span data-stu-id="3654c-130">(&lt;relation-exp&gt;) |</span></span></p>
<p><span data-ttu-id="3654c-131">&lt;berechnet exp&gt; |</span><span class="sxs-lookup"><span data-stu-id="3654c-131">&lt;calculated-exp&gt; |</span></span></p>
<p><span data-ttu-id="3654c-132">&lt;Aggregat-exp&gt; |</span><span class="sxs-lookup"><span data-stu-id="3654c-132">&lt;aggregate-exp&gt; |</span></span></p>
<p><span data-ttu-id="3654c-133">&lt;neue exp&gt;</span><span class="sxs-lookup"><span data-stu-id="3654c-133">&lt;new-exp&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3654c-134">&lt;relation_exp&gt;</span><span class="sxs-lookup"><span data-stu-id="3654c-134">&lt;relation_exp&gt;</span></span></p></td>
<td><p><span data-ttu-id="3654c-135">&lt;Tabelle exp&gt; [[AS] &lt;Alias&gt;]</span><span class="sxs-lookup"><span data-stu-id="3654c-135">&lt;table-exp&gt; [[AS] &lt;alias&gt;]</span></span></p>
<p><span data-ttu-id="3654c-136">&lt;Tabelle exp&gt; [[AS] &lt;Alias&gt;]</span><span class="sxs-lookup"><span data-stu-id="3654c-136">&lt;table-exp&gt; [[AS] &lt;alias&gt;]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3654c-137">&lt;Relation-Cond-Liste&gt;</span><span class="sxs-lookup"><span data-stu-id="3654c-137">&lt;relation-cond-list&gt;</span></span></p></td>
<td><p><span data-ttu-id="3654c-138">&lt;Relation Cond&gt; [, &lt;Relation Cond&gt;...]</span><span class="sxs-lookup"><span data-stu-id="3654c-138">&lt;relation-cond&gt; [, &lt;relation-cond&gt;...]</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3654c-139">&lt;Relation cond&gt;</span><span class="sxs-lookup"><span data-stu-id="3654c-139">&lt;relation-cond&gt;</span></span></p></td>
<td><p><span data-ttu-id="3654c-140">&lt;Name des Felds&gt; an &lt;untergeordneten Ref&gt;</span><span class="sxs-lookup"><span data-stu-id="3654c-140">&lt;field-name&gt; TO &lt;child-ref&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3654c-141">&lt;untergeordnete ref&gt;</span><span class="sxs-lookup"><span data-stu-id="3654c-141">&lt;child-ref&gt;</span></span></p></td>
<td><p><span data-ttu-id="3654c-142">&lt;Name des Felds&gt; |</span><span class="sxs-lookup"><span data-stu-id="3654c-142">&lt;field-name&gt; |</span></span></p>
<p><span data-ttu-id="3654c-143">PARAMETER &lt;Param-Ref&gt;</span><span class="sxs-lookup"><span data-stu-id="3654c-143">PARAMETER &lt;param-ref&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3654c-144">&lt;Param-ref&gt;</span><span class="sxs-lookup"><span data-stu-id="3654c-144">&lt;param-ref&gt;</span></span></p></td>
<td><p><span data-ttu-id="3654c-145">&lt;Anzahl&gt;</span><span class="sxs-lookup"><span data-stu-id="3654c-145">&lt;number&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3654c-146">&lt;Feldliste&gt;</span><span class="sxs-lookup"><span data-stu-id="3654c-146">&lt;field-list&gt;</span></span></p></td>
<td><p><span data-ttu-id="3654c-147">&lt;Name des Felds&gt; [, &lt;Feldnamen&gt;]</span><span class="sxs-lookup"><span data-stu-id="3654c-147">&lt;field-name&gt; [, &lt;field-name&gt;]</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3654c-148">&lt;Aggregat-exp&gt;</span><span class="sxs-lookup"><span data-stu-id="3654c-148">&lt;aggregate-exp&gt;</span></span></p></td>
<td><p><span data-ttu-id="3654c-149">SUM (&lt;qualifizierte Feldname&gt;) |</span><span class="sxs-lookup"><span data-stu-id="3654c-149">SUM(&lt;qualified-field-name&gt;) |</span></span></p>
<p><span data-ttu-id="3654c-150">AVG (&lt;qualifizierte Feldname&gt;) |</span><span class="sxs-lookup"><span data-stu-id="3654c-150">AVG(&lt;qualified-field-name&gt;) |</span></span></p>
<p><span data-ttu-id="3654c-151">MIN (&lt;qualifizierte Feldname&gt;) |</span><span class="sxs-lookup"><span data-stu-id="3654c-151">MIN(&lt;qualified-field-name&gt;) |</span></span></p>
<p><span data-ttu-id="3654c-152">MAX (&lt;qualifizierte Feldname&gt;) |</span><span class="sxs-lookup"><span data-stu-id="3654c-152">MAX(&lt;qualified-field-name&gt;) |</span></span></p>
<p><span data-ttu-id="3654c-153">COUNT (&lt;qualifizierte Alias&gt; | &lt;qualifizierten Namen&gt;) |</span><span class="sxs-lookup"><span data-stu-id="3654c-153">COUNT(&lt;qualified-alias&gt; | &lt;qualified-name&gt;) |</span></span></p>
<p><span data-ttu-id="3654c-154">STDEV (&lt;qualifizierte Feldname&gt;) |</span><span class="sxs-lookup"><span data-stu-id="3654c-154">STDEV(&lt;qualified-field-name&gt;) |</span></span></p>
<p><span data-ttu-id="3654c-155">Alle (&lt;qualifizierte Feldname&gt;)</span><span class="sxs-lookup"><span data-stu-id="3654c-155">ANY(&lt;qualified-field-name&gt;)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3654c-156">&lt;berechnet exp&gt;</span><span class="sxs-lookup"><span data-stu-id="3654c-156">&lt;calculated-exp&gt;</span></span></p></td>
<td><p><span data-ttu-id="3654c-157">CALC(&lt;Ausdruck&gt;)</span><span class="sxs-lookup"><span data-stu-id="3654c-157">CALC(&lt;expression&gt;)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3654c-158">&lt;qualifizierte Feldname&gt;</span><span class="sxs-lookup"><span data-stu-id="3654c-158">&lt;qualified-field-name&gt;</span></span></p></td>
<td><p><span data-ttu-id="3654c-159">&lt;Alias&gt;. [&lt;Alias&gt;...] &lt;Feldnamen&gt;</span><span class="sxs-lookup"><span data-stu-id="3654c-159">&lt;alias&gt;.[&lt;alias&gt;...]&lt;field-name&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3654c-160">&lt;Alias&gt;</span><span class="sxs-lookup"><span data-stu-id="3654c-160">&lt;alias&gt;</span></span></p></td>
<td><p><span data-ttu-id="3654c-161">&lt;Quoted-name&gt;</span><span class="sxs-lookup"><span data-stu-id="3654c-161">&lt;quoted-name&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3654c-162">&lt;Name des Felds&gt;</span><span class="sxs-lookup"><span data-stu-id="3654c-162">&lt;field-name&gt;</span></span></p></td>
<td><p><span data-ttu-id="3654c-163">&lt;Quoted-Name&gt; [[AS] &lt;Alias&gt;]</span><span class="sxs-lookup"><span data-stu-id="3654c-163">&lt;quoted-name&gt; [[AS] &lt;alias&gt;]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3654c-164">&lt;Quoted-name&gt;</span><span class="sxs-lookup"><span data-stu-id="3654c-164">&lt;quoted-name&gt;</span></span></p></td>
<td><p><span data-ttu-id="3654c-165">&quot;&lt;Zeichenfolge&gt;&quot; |</span><span class="sxs-lookup"><span data-stu-id="3654c-165">&quot;&lt;string&gt;&quot; |</span></span></p>
<p><span data-ttu-id="3654c-166">'&lt;Zeichenfolge&gt;' |</span><span class="sxs-lookup"><span data-stu-id="3654c-166">'&lt;string&gt;' |</span></span></p>
<p><span data-ttu-id="3654c-167">[&lt;Zeichenfolge&gt;] |</span><span class="sxs-lookup"><span data-stu-id="3654c-167">[&lt;string&gt;] |</span></span></p>
<p><span data-ttu-id="3654c-168">&lt;Name&gt;</span><span class="sxs-lookup"><span data-stu-id="3654c-168">&lt;name&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3654c-169">&lt;Vollständiger name&gt;</span><span class="sxs-lookup"><span data-stu-id="3654c-169">&lt;qualified-name&gt;</span></span></p></td>
<td><p><span data-ttu-id="3654c-170">Alias [.alias...]</span><span class="sxs-lookup"><span data-stu-id="3654c-170">alias[.alias...]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3654c-171">&lt;Name&gt;</span><span class="sxs-lookup"><span data-stu-id="3654c-171">&lt;name&gt;</span></span></p></td>
<td><p><span data-ttu-id="3654c-172">Alpha [Alpha | Ziffer | _ | # |: |...]</span><span class="sxs-lookup"><span data-stu-id="3654c-172">alpha [ alpha | digit | _ | # | : | ...]</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3654c-173">&lt;Anzahl&gt;</span><span class="sxs-lookup"><span data-stu-id="3654c-173">&lt;number&gt;</span></span></p></td>
<td><p><span data-ttu-id="3654c-174">Ziffer [Ziffer...]</span><span class="sxs-lookup"><span data-stu-id="3654c-174">digit [digit...]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3654c-175">&lt;neue exp&gt;</span><span class="sxs-lookup"><span data-stu-id="3654c-175">&lt;new-exp&gt;</span></span></p></td>
<td><p><span data-ttu-id="3654c-176">NEUE &lt;Feldtyp&gt; [(&lt;Anzahl&gt; [, &lt;Anzahl&gt;])]</span><span class="sxs-lookup"><span data-stu-id="3654c-176">NEW &lt;field-type&gt; [(&lt;number&gt; [, &lt;number&gt;])]</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3654c-177">&lt;Feldtyp&gt;</span><span class="sxs-lookup"><span data-stu-id="3654c-177">&lt;field-type&gt;</span></span></p></td>
<td><p><span data-ttu-id="3654c-178">Ein OLE DB- oder ADO-Datentyp.</span><span class="sxs-lookup"><span data-stu-id="3654c-178">An OLE DB or ADO data type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3654c-179">&lt;Zeichenfolge&gt;</span><span class="sxs-lookup"><span data-stu-id="3654c-179">&lt;string&gt;</span></span></p></td>
<td><p><span data-ttu-id="3654c-180">Unicode-Zeichen [Unicode-Zeichen...]</span><span class="sxs-lookup"><span data-stu-id="3654c-180">unicode-char [unicode-char...]</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3654c-181">&lt;Ausdruck&gt;</span><span class="sxs-lookup"><span data-stu-id="3654c-181">&lt;expression&gt;</span></span></p></td>
<td><p><span data-ttu-id="3654c-182">Ein Visual Basic für Applikationen-Ausdruck, dessen Operanden andere Nicht-CALC-Spalten in der gleichen Zeile sind.</span><span class="sxs-lookup"><span data-stu-id="3654c-182">A Visual Basic for Applications expression whose operands are other non-CALC columns in the same row.</span></span></p></td>
</tr>
</tbody>
</table>

