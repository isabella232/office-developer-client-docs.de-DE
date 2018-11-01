---
title: Field2.ValidationRule Property (DAO)
TOCTitle: ValidationRule Property
ms:assetid: 5464d2de-f3d7-5d6b-4fc5-66df6a5540cb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194105(v=office.15)
ms:contentKeyID: 48544896
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 006c9ce982aa98f28187d04fced12992d61548d9
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25880054"
---
# <a name="field2validationrule-property-dao"></a><span data-ttu-id="813ae-102">Field2.ValidationRule Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="813ae-102">Field2.ValidationRule Property (DAO)</span></span>


<span data-ttu-id="813ae-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="813ae-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="813ae-p101">Legt einen Wert fest, der die Daten in einem Feld überprüft, wenn es geändert oder einer Tabelle hinzugefügt wird, oder gibt den betreffenden Wert zurück (nur Microsoft Access-Arbeitsbereiche). **String**-Wert mit Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="813ae-p101">Sets or returns a value that validates the data in a field as it's changed or added to a table (Microsoft Access workspaces only). Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="813ae-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="813ae-106">Syntax</span></span>

<span data-ttu-id="813ae-107">*Ausdruck* . ValidationRule</span><span class="sxs-lookup"><span data-stu-id="813ae-107">*expression* .ValidationRule</span></span>

<span data-ttu-id="813ae-108">*Ausdruck* Ein Ausdruck, der ein **Field2** -Objekt zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="813ae-108">*expression* An expression that returns a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="813ae-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="813ae-109">Remarks</span></span>

<span data-ttu-id="813ae-110">Die Einstellungen oder Rückgabewerte ist eine Zeichenfolge, die einen Vergleich in der Form einer SQL WHERE-Klausel ohne das WHERE reservierte Wort beschreibt.</span><span class="sxs-lookup"><span data-stu-id="813ae-110">The settings or return values is a String that describes a comparison in the form of an SQL WHERE clause without the WHERE reserved word.</span></span> <span data-ttu-id="813ae-111">Für ein Objekt, das noch nicht an die **[Fields](fields-collection-dao.md)** -Auflistung angehängt wurde, besteht Lese-/Schreibzugriff für diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="813ae-111">For an object not yet appended to the **[Fields](fields-collection-dao.md)** collection, this property is read/write.</span></span>

<span data-ttu-id="813ae-p103">Die **ValidationRule**-Eigenschaft bestimmt, ob ein Feld gültige Daten enthält. Sind die Daten nicht gültig, tritt ein abfangbarer Fehler auf. Die zurückgegebene Fehlermeldung ist der Text der **ValidationText**-Eigenschaft, falls angegeben, oder der Text des von der **ValidationRule**-Eigenschaft angegebenen Ausdrucks.</span><span class="sxs-lookup"><span data-stu-id="813ae-p103">The **ValidationRule** property determines whether or not a field contains valid data. If the data is not valid, a trappable run-time error occurs. The returned error message is the text of the **ValidationText** property, if specified, or the text of the expression specified by **ValidationRule**.</span></span>

<span data-ttu-id="813ae-115">Bei einem **Field2**-Objekt hängt die Verwendung der **ValidationRule**-Eigenschaft vom Objekt ab, das die **Fields**-Auflistung enthält, der das **Field2**-Objekt angefügt wird.</span><span class="sxs-lookup"><span data-stu-id="813ae-115">For a **Field2** object, use of the **ValidationRule** property depends on the object that contains the **Fields** collection to which the **Field2** object is appended.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="813ae-116">Zugehörigkeit zu Objekt</span><span class="sxs-lookup"><span data-stu-id="813ae-116">Object appended to</span></span></p></th>
<th><p><span data-ttu-id="813ae-117">Verwendung</span><span class="sxs-lookup"><span data-stu-id="813ae-117">Usage</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="813ae-118"><strong>Index</strong></span><span class="sxs-lookup"><span data-stu-id="813ae-118"><strong>Index</strong></span></span></p></td>
<td><p><span data-ttu-id="813ae-119">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="813ae-119">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="813ae-120"><strong>QueryDef-Objekt</strong></span><span class="sxs-lookup"><span data-stu-id="813ae-120"><strong>QueryDef</strong></span></span></p></td>
<td><p><span data-ttu-id="813ae-121">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="813ae-121">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="813ae-122"><strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="813ae-122"><strong>Recordset</strong></span></span></p></td>
<td><p><span data-ttu-id="813ae-123">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="813ae-123">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="813ae-124"><strong>Beziehung</strong></span><span class="sxs-lookup"><span data-stu-id="813ae-124"><strong>Relation</strong></span></span></p></td>
<td><p><span data-ttu-id="813ae-125">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="813ae-125">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="813ae-126"><strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="813ae-126"><strong>TableDef</strong></span></span></p></td>
<td><p><span data-ttu-id="813ae-127">Lese-/Schreibzugriff</span><span class="sxs-lookup"><span data-stu-id="813ae-127">Read/write</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="813ae-128">Die Gültigkeitsprüfung wird nur für Datenbanken unterstützt, die die Microsoft Access-Datenbank-Engine verwenden.</span><span class="sxs-lookup"><span data-stu-id="813ae-128">Validation is supported only for databases that use the Microsoft Access database engine.</span></span>

<span data-ttu-id="813ae-p104">Der von der **ValidationRule**-Eigenschaft eines **Field2**-Objekts angegebene Zeichenfolgenausdruck kann sich nur auf dieses **Field2**-Objekt beziehen. Der Ausdruck kann sich nicht auf benutzerdefinierte Funktionen, SQL-Aggregatfunktionen oder Abfragen beziehen. Damit die **ValidationRule**-Eigenschaft eines **Field2**-Objekts festgelegt werden kann, wenn die Einstellung seiner **ValidateOnSet**-Eigenschaft auf **True** festgelegt ist, muss der Ausdruck erfolgreich analysiert (wobei der Feldname ein impliziter Operand sein muss) und mit **True** ausgewertet worden sein. Ist die Einstellung seiner **ValidateOnSet**-Eigenschaft auf **False** festgelegt, wird die Einstellung der **ValidationRule**-Eigenschaft ignoriert.</span><span class="sxs-lookup"><span data-stu-id="813ae-p104">The string expression specified by the **ValidationRule** property of a **Field2** object can refer only to that **Field2**. The expression can't refer to user-defined functions, SQL aggregate functions, or queries. To set a **Field2** object's **ValidationRule** property when its **ValidateOnSet** property setting is **True**, the expression must successfully parse (with the field name as an implied operand) and evaluate to **True**. If its **ValidateOnSet** property setting is **False**, the **ValidationRule** property setting is ignored.</span></span>


> [!NOTE]
> <P><span data-ttu-id="813ae-133">Wenn Sie die Eigenschaft auf eine Zeichenfolge mit einem nicht-Integer-Wert verkettet festlegen und die Systemparameter einer US-decimal Zeichen wie etwa ein Komma angeben (beispielsweise StrRule = "Preis &gt; " &amp; LngPrice, und LngPrice = 125,50), ein Fehler ausgegeben, wenn der Code versucht, Daten zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="813ae-133">If you set the property to a string concatenated with a non-integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example, strRule = "PRICE &gt; " &amp; lngPrice, and lngPrice = 125,50), an error will result when your code attempts to validate any data.</span></span> <span data-ttu-id="813ae-134">Dies ist, da während der Verkettung die Zahl in eine Zeichenfolge mit Ihr System vorgegebenen Standardzeichen für Dezimalzahlen konvertiert und Microsoft Access-Datenbankmodul SQL nur US-Dezimaltrennzeichen akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="813ae-134">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and Microsoft Access database engine SQL only accepts U.S. decimal characters.</span></span></P>


