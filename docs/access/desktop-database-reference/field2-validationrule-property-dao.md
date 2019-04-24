---
title: Field2. ValidationRule-Eigenschaft (DAO)
TOCTitle: ValidationRule Property
ms:assetid: 5464d2de-f3d7-5d6b-4fc5-66df6a5540cb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194105(v=office.15)
ms:contentKeyID: 48544896
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b6e9e50148f4b87a957ff2317b1b39522d7d4e1c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292650"
---
# <a name="field2validationrule-property-dao"></a><span data-ttu-id="d6461-102">Field2. ValidationRule-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="d6461-102">Field2.ValidationRule property (DAO)</span></span>


<span data-ttu-id="d6461-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d6461-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d6461-p101">Mit dieser Eigenschaft wird ein Wert festgelegt oder zurückgegeben, der die Daten in einem Feld direkt bei der Eingabe oder dem Hinzufügen zu einer Tabelle überprüft (gilt nur für Microsoft Access-Arbeitsbereiche). **String**-Wert mit Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="d6461-p101">Sets or returns a value that validates the data in a field as it's changed or added to a table (Microsoft Access workspaces only). Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6461-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="d6461-106">Syntax</span></span>

<span data-ttu-id="d6461-107">*Ausdruck* . ValidationRule</span><span class="sxs-lookup"><span data-stu-id="d6461-107">*expression* .ValidationRule</span></span>

<span data-ttu-id="d6461-108">*Ausdruck* Ein Ausdruck, der ein **Field2** -Objekt zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="d6461-108">*expression* An expression that returns a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="d6461-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d6461-109">Remarks</span></span>

<span data-ttu-id="d6461-p102">The settings or return values is a String that describes a comparison in the form of an SQL WHERE clause without the WHERE reserved word. For an object not yet appended to the **[Fields](fields-collection-dao.md)** collection, this property is read/write.</span><span class="sxs-lookup"><span data-stu-id="d6461-p102">The settings or return values is a String that describes a comparison in the form of an SQL WHERE clause without the WHERE reserved word. For an object not yet appended to the **[Fields](fields-collection-dao.md)** collection, this property is read/write.</span></span>

<span data-ttu-id="d6461-p103">Die **ValidationRule**-Eigenschaft bestimmt, ob ein Feld gültige Daten enthält. Sind die Daten nicht gültig, tritt ein abfangbarer Fehler auf. Die zurückgegebene Fehlermeldung ist der Text der **ValidationText**-Eigenschaft, falls angegeben, oder der Text des von der **ValidationRule**-Eigenschaft angegebenen Ausdrucks.</span><span class="sxs-lookup"><span data-stu-id="d6461-p103">The **ValidationRule** property determines whether or not a field contains valid data. If the data is not valid, a trappable run-time error occurs. The returned error message is the text of the **ValidationText** property, if specified, or the text of the expression specified by **ValidationRule**.</span></span>

<span data-ttu-id="d6461-115">Bei einem **Field2**-Objekt hängt die Verwendung der **ValidationRule**-Eigenschaft vom Objekt ab, das die **Fields**-Auflistung enthält, der das **Field2**-Objekt angefügt wird.</span><span class="sxs-lookup"><span data-stu-id="d6461-115">For a **Field2** object, use of the **ValidationRule** property depends on the object that contains the **Fields** collection to which the **Field2** object is appended.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d6461-116">Zugehörigkeit zu Objekt</span><span class="sxs-lookup"><span data-stu-id="d6461-116">Object appended to</span></span></p></th>
<th><p><span data-ttu-id="d6461-117">Verwendung</span><span class="sxs-lookup"><span data-stu-id="d6461-117">Usage</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d6461-118"><strong>Index</strong></span><span class="sxs-lookup"><span data-stu-id="d6461-118"><strong>Index</strong></span></span></p></td>
<td><p><span data-ttu-id="d6461-119">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="d6461-119">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d6461-120"><strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="d6461-120"><strong>QueryDef</strong></span></span></p></td>
<td><p><span data-ttu-id="d6461-121">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d6461-121">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d6461-122"><strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="d6461-122"><strong>Recordset</strong></span></span></p></td>
<td><p><span data-ttu-id="d6461-123">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d6461-123">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d6461-124"><strong>Beziehung</strong></span><span class="sxs-lookup"><span data-stu-id="d6461-124"><strong>Relation</strong></span></span></p></td>
<td><p><span data-ttu-id="d6461-125">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="d6461-125">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d6461-126"><strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="d6461-126"><strong>TableDef</strong></span></span></p></td>
<td><p><span data-ttu-id="d6461-127">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d6461-127">Read/write</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d6461-128">Die Überprüfung wird nur für Datenbanken unterstützt, die das Microsoft Access-Datenbankmodul verwenden.</span><span class="sxs-lookup"><span data-stu-id="d6461-128">Validation is supported only for databases that use the Microsoft Access database engine.</span></span>

<span data-ttu-id="d6461-p104">Der von der **ValidationRule**-Eigenschaft eines **Field2**-Objekts angegebene Zeichenfolgenausdruck kann sich nur auf dieses **Field2**-Objekt beziehen. Der Ausdruck kann sich nicht auf benutzerdefinierte Funktionen, SQL-Aggregatfunktionen oder Abfragen beziehen. Damit die **ValidationRule**-Eigenschaft eines **Field2**-Objekts festgelegt werden kann, wenn die Einstellung seiner **ValidateOnSet**-Eigenschaft auf **True** festgelegt ist, muss der Ausdruck erfolgreich analysiert (wobei der Feldname ein impliziter Operand sein muss) und mit **True** ausgewertet worden sein. Ist die Einstellung seiner **ValidateOnSet**-Eigenschaft auf **False** festgelegt, wird die Einstellung der **ValidationRule**-Eigenschaft ignoriert.</span><span class="sxs-lookup"><span data-stu-id="d6461-p104">The string expression specified by the **ValidationRule** property of a **Field2** object can refer only to that **Field2**. The expression can't refer to user-defined functions, SQL aggregate functions, or queries. To set a **Field2** object's **ValidationRule** property when its **ValidateOnSet** property setting is **True**, the expression must successfully parse (with the field name as an implied operand) and evaluate to **True**. If its **ValidateOnSet** property setting is **False**, the **ValidationRule** property setting is ignored.</span></span>


> [!NOTE]
> <span data-ttu-id="d6461-133">Wenn Sie die-Eigenschaft auf eine Zeichenfolge festlegen, die mit einem nicht-ganzzahligen Wert verkettet ist, und die Systemparameter ein nicht-U. S. Decimal-Zeichen wie ein Komma (beispielsweise strRule &gt; = &amp; "Price" lngPrice und lngPrice = 125, 50) angeben, tritt ein Fehler auf, wenn Ihr Code versucht, alle Daten zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="d6461-133">If you set the property to a string concatenated with a non-integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example, strRule = "PRICE &gt; " &amp; lngPrice, and lngPrice = 125,50), an error will result when your code attempts to validate any data.</span></span> <span data-ttu-id="d6461-134">Dies liegt daran, dass der Wert während der Verkettung mithilfe des Standard-Dezimaltrennzeichens in eine Zeichenfolge konvertiert wird und SQL der Microsoft Access-Datenbank-Engine nur US-Dezimaltrennzeichen akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="d6461-134">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and Microsoft Access database engine SQL only accepts U.S. decimal characters.</span></span>


