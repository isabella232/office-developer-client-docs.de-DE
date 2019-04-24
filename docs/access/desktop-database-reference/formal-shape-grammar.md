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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292321"
---
# <a name="formal-shape-grammar"></a><span data-ttu-id="63942-102">Formal Shape Grammar</span><span class="sxs-lookup"><span data-stu-id="63942-102">Formal shape grammar</span></span>

<span data-ttu-id="63942-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="63942-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="63942-104">Dies ist die formale Grammatik zum Erstellen von Shape-Befehlen:</span><span class="sxs-lookup"><span data-stu-id="63942-104">This is the formal grammar for creating any shape command:</span></span>

  - <span data-ttu-id="63942-105">Erforderliche Grammatikbegriffe sind Textzeichenfolgen, die durch spitze Klammern ("\<\>") getrennt sind.</span><span class="sxs-lookup"><span data-stu-id="63942-105">Required grammatical terms are text strings delimited by angle brackets ("\<\>").</span></span>

  - <span data-ttu-id="63942-106">Optionale Ausdrücke werden durch eckige Klammern ("\[ \]") getrennt.</span><span class="sxs-lookup"><span data-stu-id="63942-106">Optional terms are delimited by square brackets ("\[ \]").</span></span>

  - <span data-ttu-id="63942-107">Alternativen werden durch einen Schrägstrich ("|") angegeben.</span><span class="sxs-lookup"><span data-stu-id="63942-107">Alternatives are indicated by a virgule ("|").</span></span>

  - <span data-ttu-id="63942-108">Wiederholte Alternativen werden durch Auslassungspunkte ("...") angegeben.</span><span class="sxs-lookup"><span data-stu-id="63942-108">Repeating alternatives are indicated by an ellipsis ("...").</span></span>

  - <span data-ttu-id="63942-109">Durch *Alpha* wird eine Zeichenfolge aus alphabetischen Buchstaben angegeben.</span><span class="sxs-lookup"><span data-stu-id="63942-109">*Alpha* indicates a string of alphabetical letters.</span></span>

  - <span data-ttu-id="63942-110">Durch *Digit* wird eine Zeichenfolge aus Zahlen angegeben.</span><span class="sxs-lookup"><span data-stu-id="63942-110">*Digit* indicates a string of numbers.</span></span>

  - <span data-ttu-id="63942-111">Durch *Unicode-digit* wird eine Zeichenfolge aus Unicode-Ziffern angegeben.</span><span class="sxs-lookup"><span data-stu-id="63942-111">*Unicode-digit* indicates a string of unicode digits.</span></span>

<span data-ttu-id="63942-112">Alle andere Begriffe sind Literale.</span><span class="sxs-lookup"><span data-stu-id="63942-112">All other terms are literals.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="63942-113">Begriff</span><span class="sxs-lookup"><span data-stu-id="63942-113">Term</span></span></p></th>
<th><p><span data-ttu-id="63942-114">Definition</span><span class="sxs-lookup"><span data-stu-id="63942-114">Definition</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="63942-115">&lt;Shape-Befehl&gt;</span><span class="sxs-lookup"><span data-stu-id="63942-115">&lt;shape-command&gt;</span></span></p></td>
<td><p><span data-ttu-id="63942-116">Shape [&lt;Tabelle-exp&gt; [[as] &lt;Alias&gt;]] [&lt;Shape-Aktion&gt;]</span><span class="sxs-lookup"><span data-stu-id="63942-116">SHAPE [&lt;table-exp&gt; [[AS] &lt;alias&gt;]][&lt;shape-action&gt;]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="63942-117">&lt;Tabelle-Exp&gt;</span><span class="sxs-lookup"><span data-stu-id="63942-117">&lt;table-exp&gt;</span></span></p></td>
<td><p><span data-ttu-id="63942-118">{&lt;Anbieter-Command-Text&gt;} |</span><span class="sxs-lookup"><span data-stu-id="63942-118">{&lt;provider-command-text&gt;} |</span></span><br />
<span data-ttu-id="63942-119">(&lt;Shape-Befehl&gt;) |</span><span class="sxs-lookup"><span data-stu-id="63942-119">(&lt;shape-command&gt;) |</span></span><br />
<span data-ttu-id="63942-120">Tabelle &lt;in Anführungszeichen-Name&gt; |</span><span class="sxs-lookup"><span data-stu-id="63942-120">TABLE &lt;quoted-name&gt; |</span></span><br />
<span data-ttu-id="63942-121">&lt;zitiert-Name&gt;</span><span class="sxs-lookup"><span data-stu-id="63942-121">&lt;quoted-name&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="63942-122">&lt;Shape-Aktion&gt;</span><span class="sxs-lookup"><span data-stu-id="63942-122">&lt;shape-action&gt;</span></span></p></td>
<td><p><span data-ttu-id="63942-123">Alias &lt;-field-list anfügen&gt; |</span><span class="sxs-lookup"><span data-stu-id="63942-123">APPEND &lt;aliased-field-list&gt; |</span></span></p>
<p><span data-ttu-id="63942-124">COMPUTE &lt;aliased-Field-List&gt; [by &lt;Field-List&gt;]</span><span class="sxs-lookup"><span data-stu-id="63942-124">COMPUTE &lt;aliased-field-list&gt; [BY &lt;field-list&gt;]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="63942-125">&lt;aliased-field-list&gt;</span><span class="sxs-lookup"><span data-stu-id="63942-125">&lt;aliased-field-list&gt;</span></span></p></td>
<td><p><span data-ttu-id="63942-126">&lt;aliased-Field&gt; [, &lt;aliased-Field... &gt;]</span><span class="sxs-lookup"><span data-stu-id="63942-126">&lt;aliased-field&gt; [, &lt;aliased-field...&gt;]</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="63942-127">&lt;Alias-Field&gt;</span><span class="sxs-lookup"><span data-stu-id="63942-127">&lt;aliased-field&gt;</span></span></p></td>
<td><p><span data-ttu-id="63942-128">&lt;Field-exp&gt; [[as] &lt;Alias&gt;]</span><span class="sxs-lookup"><span data-stu-id="63942-128">&lt;field-exp&gt; [[AS] &lt;alias&gt;]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="63942-129">&lt;Field-Exp&gt;</span><span class="sxs-lookup"><span data-stu-id="63942-129">&lt;field-exp&gt;</span></span></p></td>
<td><p><span data-ttu-id="63942-130">(&lt;Relation-exp&gt;) |</span><span class="sxs-lookup"><span data-stu-id="63942-130">(&lt;relation-exp&gt;) |</span></span></p>
<p><span data-ttu-id="63942-131">&lt;berechnet-Exp&gt; |</span><span class="sxs-lookup"><span data-stu-id="63942-131">&lt;calculated-exp&gt; |</span></span></p>
<p><span data-ttu-id="63942-132">&lt;Aggregieren-Exp&gt; |</span><span class="sxs-lookup"><span data-stu-id="63942-132">&lt;aggregate-exp&gt; |</span></span></p>
<p><span data-ttu-id="63942-133">&lt;neu-Exp&gt;</span><span class="sxs-lookup"><span data-stu-id="63942-133">&lt;new-exp&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="63942-134">&lt;relation_exp&gt;</span><span class="sxs-lookup"><span data-stu-id="63942-134">&lt;relation_exp&gt;</span></span></p></td>
<td><p><span data-ttu-id="63942-135">&lt;Tabelle-exp&gt; [[as] &lt;Alias&gt;]</span><span class="sxs-lookup"><span data-stu-id="63942-135">&lt;table-exp&gt; [[AS] &lt;alias&gt;]</span></span></p>
<p><span data-ttu-id="63942-136">&lt;Tabelle-exp&gt; [[as] &lt;Alias&gt;]</span><span class="sxs-lookup"><span data-stu-id="63942-136">&lt;table-exp&gt; [[AS] &lt;alias&gt;]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="63942-137">&lt;Relation-Ltg-Liste&gt;</span><span class="sxs-lookup"><span data-stu-id="63942-137">&lt;relation-cond-list&gt;</span></span></p></td>
<td><p><span data-ttu-id="63942-138">&lt;Relation-Ltg&gt; [, &lt;Relation-Ltg&gt;...]</span><span class="sxs-lookup"><span data-stu-id="63942-138">&lt;relation-cond&gt; [, &lt;relation-cond&gt;...]</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="63942-139">&lt;Relation-Ltg&gt;</span><span class="sxs-lookup"><span data-stu-id="63942-139">&lt;relation-cond&gt;</span></span></p></td>
<td><p><span data-ttu-id="63942-140">&lt;Field-Name&gt; unter &lt;Child-Ref&gt;</span><span class="sxs-lookup"><span data-stu-id="63942-140">&lt;field-name&gt; TO &lt;child-ref&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="63942-141">&lt;Child-Ref&gt;</span><span class="sxs-lookup"><span data-stu-id="63942-141">&lt;child-ref&gt;</span></span></p></td>
<td><p><span data-ttu-id="63942-142">&lt;Feldname&gt; |</span><span class="sxs-lookup"><span data-stu-id="63942-142">&lt;field-name&gt; |</span></span></p>
<p><span data-ttu-id="63942-143">PARAMETER &lt;param-Ref&gt;</span><span class="sxs-lookup"><span data-stu-id="63942-143">PARAMETER &lt;param-ref&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="63942-144">&lt;param-Ref&gt;</span><span class="sxs-lookup"><span data-stu-id="63942-144">&lt;param-ref&gt;</span></span></p></td>
<td><p><span data-ttu-id="63942-145">&lt;Anzahl&gt;</span><span class="sxs-lookup"><span data-stu-id="63942-145">&lt;number&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="63942-146">&lt;Field-List&gt;</span><span class="sxs-lookup"><span data-stu-id="63942-146">&lt;field-list&gt;</span></span></p></td>
<td><p><span data-ttu-id="63942-147">&lt;Feldnamen&gt; [, &lt;Feldname]&gt;</span><span class="sxs-lookup"><span data-stu-id="63942-147">&lt;field-name&gt; [, &lt;field-name&gt;]</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="63942-148">&lt;Aggregieren-Exp&gt;</span><span class="sxs-lookup"><span data-stu-id="63942-148">&lt;aggregate-exp&gt;</span></span></p></td>
<td><p><span data-ttu-id="63942-149">SUM (&lt;Qualified-Field-Name&gt;) |</span><span class="sxs-lookup"><span data-stu-id="63942-149">SUM(&lt;qualified-field-name&gt;) |</span></span></p>
<p><span data-ttu-id="63942-150">AVG (&lt;Qualified-Field-Name&gt;) |</span><span class="sxs-lookup"><span data-stu-id="63942-150">AVG(&lt;qualified-field-name&gt;) |</span></span></p>
<p><span data-ttu-id="63942-151">MIN (&lt;Qualified-Field-Name&gt;) |</span><span class="sxs-lookup"><span data-stu-id="63942-151">MIN(&lt;qualified-field-name&gt;) |</span></span></p>
<p><span data-ttu-id="63942-152">MAX (&lt;Qualified-Field-Name&gt;) |</span><span class="sxs-lookup"><span data-stu-id="63942-152">MAX(&lt;qualified-field-name&gt;) |</span></span></p>
<p><span data-ttu-id="63942-153">COUNT (&lt;Qualified-Alias&gt; | &lt;Qualified-Name&gt;) |</span><span class="sxs-lookup"><span data-stu-id="63942-153">COUNT(&lt;qualified-alias&gt; | &lt;qualified-name&gt;) |</span></span></p>
<p><span data-ttu-id="63942-154">STDEV (&lt;Qualified-Field-Name&gt;) |</span><span class="sxs-lookup"><span data-stu-id="63942-154">STDEV(&lt;qualified-field-name&gt;) |</span></span></p>
<p><span data-ttu-id="63942-155">ANY (&lt;Qualified-Field-Name&gt;)</span><span class="sxs-lookup"><span data-stu-id="63942-155">ANY(&lt;qualified-field-name&gt;)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="63942-156">&lt;berechnet-Exp&gt;</span><span class="sxs-lookup"><span data-stu-id="63942-156">&lt;calculated-exp&gt;</span></span></p></td>
<td><p><span data-ttu-id="63942-157">CALC (&lt;Ausdruck&gt;)</span><span class="sxs-lookup"><span data-stu-id="63942-157">CALC(&lt;expression&gt;)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="63942-158">&lt;Qualified-Field-Name&gt;</span><span class="sxs-lookup"><span data-stu-id="63942-158">&lt;qualified-field-name&gt;</span></span></p></td>
<td><p><span data-ttu-id="63942-159">&lt;Alias&gt;. [&lt;Alias&gt;...] &lt;Feldname&gt;</span><span class="sxs-lookup"><span data-stu-id="63942-159">&lt;alias&gt;.[&lt;alias&gt;...]&lt;field-name&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="63942-160">&lt;Alias&gt;</span><span class="sxs-lookup"><span data-stu-id="63942-160">&lt;alias&gt;</span></span></p></td>
<td><p><span data-ttu-id="63942-161">&lt;zitiert-Name&gt;</span><span class="sxs-lookup"><span data-stu-id="63942-161">&lt;quoted-name&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="63942-162">&lt;Feldname&gt;</span><span class="sxs-lookup"><span data-stu-id="63942-162">&lt;field-name&gt;</span></span></p></td>
<td><p><span data-ttu-id="63942-163">&lt;Anführungs&gt; Zeichen-Name [ &lt;[&gt;as] Alias]</span><span class="sxs-lookup"><span data-stu-id="63942-163">&lt;quoted-name&gt; [[AS] &lt;alias&gt;]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="63942-164">&lt;zitiert-Name&gt;</span><span class="sxs-lookup"><span data-stu-id="63942-164">&lt;quoted-name&gt;</span></span></p></td>
<td><p><span data-ttu-id="63942-165">&quot;&lt;Zeichenfolge&gt;&quot; |</span><span class="sxs-lookup"><span data-stu-id="63942-165">&quot;&lt;string&gt;&quot; |</span></span></p>
<p><span data-ttu-id="63942-166">'&lt;Zeichen&gt;Folge ' |</span><span class="sxs-lookup"><span data-stu-id="63942-166">'&lt;string&gt;' |</span></span></p>
<p><span data-ttu-id="63942-167">[&lt;Zeichen&gt;Folge] |</span><span class="sxs-lookup"><span data-stu-id="63942-167">[&lt;string&gt;] |</span></span></p>
<p><span data-ttu-id="63942-168">&lt;Namen&gt;</span><span class="sxs-lookup"><span data-stu-id="63942-168">&lt;name&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="63942-169">&lt;qualifizierter Name&gt;</span><span class="sxs-lookup"><span data-stu-id="63942-169">&lt;qualified-name&gt;</span></span></p></td>
<td><p><span data-ttu-id="63942-170">Alias [. Alias...]</span><span class="sxs-lookup"><span data-stu-id="63942-170">alias[.alias...]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="63942-171">&lt;Namen&gt;</span><span class="sxs-lookup"><span data-stu-id="63942-171">&lt;name&gt;</span></span></p></td>
<td><p><span data-ttu-id="63942-172">Alpha [alpha | Ziffer | _ | # |: |...]</span><span class="sxs-lookup"><span data-stu-id="63942-172">alpha [ alpha | digit | _ | # | : | ...]</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="63942-173">&lt;Anzahl&gt;</span><span class="sxs-lookup"><span data-stu-id="63942-173">&lt;number&gt;</span></span></p></td>
<td><p><span data-ttu-id="63942-174">Ziffer [Ziffer...]</span><span class="sxs-lookup"><span data-stu-id="63942-174">digit [digit...]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="63942-175">&lt;neu-Exp&gt;</span><span class="sxs-lookup"><span data-stu-id="63942-175">&lt;new-exp&gt;</span></span></p></td>
<td><p><span data-ttu-id="63942-176">Neuer &lt;field-type&gt; [(&lt;Number&gt; [, &lt;Number&gt;])]</span><span class="sxs-lookup"><span data-stu-id="63942-176">NEW &lt;field-type&gt; [(&lt;number&gt; [, &lt;number&gt;])]</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="63942-177">&lt;Field-Typ&gt;</span><span class="sxs-lookup"><span data-stu-id="63942-177">&lt;field-type&gt;</span></span></p></td>
<td><p><span data-ttu-id="63942-178">Ein OLE DB- oder ADO-Datentyp.</span><span class="sxs-lookup"><span data-stu-id="63942-178">An OLE DB or ADO data type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="63942-179">&lt;string&gt;</span><span class="sxs-lookup"><span data-stu-id="63942-179">&lt;string&gt;</span></span></p></td>
<td><p><span data-ttu-id="63942-180">Unicode-Char [Unicode-Char...]</span><span class="sxs-lookup"><span data-stu-id="63942-180">unicode-char [unicode-char...]</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="63942-181">&lt;Ausdruck&gt;</span><span class="sxs-lookup"><span data-stu-id="63942-181">&lt;expression&gt;</span></span></p></td>
<td><p><span data-ttu-id="63942-182">Ein Visual Basic für Applikationen-Ausdruck, dessen Operanden andere Nicht-CALC-Spalten in der gleichen Zeile sind.</span><span class="sxs-lookup"><span data-stu-id="63942-182">A Visual Basic for Applications expression whose operands are other non-CALC columns in the same row.</span></span></p></td>
</tr>
</tbody>
</table>

