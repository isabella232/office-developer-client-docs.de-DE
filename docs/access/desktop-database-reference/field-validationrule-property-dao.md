---
title: Field.ValidationRule-Eigenschaft (DAO)
TOCTitle: ValidationRule Property
ms:assetid: b07e644d-54d3-7199-6f99-178774e54398
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821784(v=office.15)
ms:contentKeyID: 48547123
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1ef68db39b7dcad380eae16f789f4dd5b0eab75f
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28722109"
---
# <a name="fieldvalidationrule-property-dao"></a><span data-ttu-id="4d459-102">Field.ValidationRule-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="4d459-102">Field.ValidationRule property (DAO)</span></span>


<span data-ttu-id="4d459-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4d459-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4d459-p101">Legt einen Wert fest, der die Daten in einem Feld überprüft, wenn es geändert oder einer Tabelle hinzugefügt wird, oder gibt den betreffenden Wert zurück (nur Microsoft Access-Arbeitsbereiche). **String**-Wert mit Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="4d459-p101">Sets or returns a value that validates the data in a field as it's changed or added to a table (Microsoft Access workspaces only). Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d459-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="4d459-106">Syntax</span></span>

<span data-ttu-id="4d459-107">*Ausdruck* . ValidationRule</span><span class="sxs-lookup"><span data-stu-id="4d459-107">*expression* .ValidationRule</span></span>

<span data-ttu-id="4d459-108">*Ausdruck* Ein Ausdruck, der ein **Field** -Objekt zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="4d459-108">*expression* An expression that returns a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="4d459-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4d459-109">Remarks</span></span>

<span data-ttu-id="4d459-110">Die Einstellungen oder Rückgabewerte ist eine Zeichenfolge, die einen Vergleich in der Form einer SQL WHERE-Klausel ohne das WHERE reservierte Wort beschreibt.</span><span class="sxs-lookup"><span data-stu-id="4d459-110">The settings or return values is a String that describes a comparison in the form of an SQL WHERE clause without the WHERE reserved word.</span></span> <span data-ttu-id="4d459-111">Für ein Objekt, das noch nicht an die **[Fields](fields-collection-dao.md)** -Auflistung angehängt wurde, besteht Lese-/Schreibzugriff für diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="4d459-111">For an object not yet appended to the **[Fields](fields-collection-dao.md)** collection, this property is read/write.</span></span>

<span data-ttu-id="4d459-p103">Die **ValidationRule**-Eigenschaft legt fest, ob ein Feld gültige Daten enthält. Wenn die Daten nicht gültig sind, tritt ein auffangbarer Laufzeitfehler auf. Die zurückgegebene Fehlermeldung ist der Text der **[ValidationText](field-validationtext-property-dao.md)** -Eigenschaft, sofern er angegeben wurde, oder der von **ValidationRule** angegebene Text.</span><span class="sxs-lookup"><span data-stu-id="4d459-p103">The **ValidationRule** property determines whether or not a field contains valid data. If the data is not valid, a trappable run-time error occurs. The returned error message is the text of the **[ValidationText](field-validationtext-property-dao.md)** property, if specified, or the text of the expression specified by **ValidationRule**.</span></span>

<span data-ttu-id="4d459-115">Bei einem **[Field](field-object-dao.md)** -Objekt hängt die Verwendung der **ValidationRule**-Eigenschaft von dem Objekt ab, das die **Fields**-Auflistung enthält, an die das **Field**-Objekt angefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="4d459-115">For a **[Field](field-object-dao.md)** object, use of the **ValidationRule** property depends on the object that contains the **Fields** collection to which the **Field** object is appended.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4d459-116">Zugehörigkeit zu Objekt</span><span class="sxs-lookup"><span data-stu-id="4d459-116">Object appended to</span></span></p></th>
<th><p><span data-ttu-id="4d459-117">Verwendung</span><span class="sxs-lookup"><span data-stu-id="4d459-117">Usage</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4d459-118"><strong>Index</strong></span><span class="sxs-lookup"><span data-stu-id="4d459-118"><strong>Index</strong></span></span></p></td>
<td><p><span data-ttu-id="4d459-119">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="4d459-119">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4d459-120"><strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="4d459-120"><strong>QueryDef</strong></span></span></p></td>
<td><p><span data-ttu-id="4d459-121">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="4d459-121">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4d459-122"><strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="4d459-122"><strong>Recordset</strong></span></span></p></td>
<td><p><span data-ttu-id="4d459-123">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="4d459-123">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4d459-124"><strong>Beziehung</strong></span><span class="sxs-lookup"><span data-stu-id="4d459-124"><strong>Relation</strong></span></span></p></td>
<td><p><span data-ttu-id="4d459-125">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="4d459-125">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4d459-126"><strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="4d459-126"><strong>TableDef</strong></span></span></p></td>
<td><p><span data-ttu-id="4d459-127">Lese-/Schreibzugriff</span><span class="sxs-lookup"><span data-stu-id="4d459-127">Read/write</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="4d459-128">Die Gültigkeitsprüfung wird nur für Datenbanken unterstützt, die die Microsoft Access-Datenbank-Engine verwenden.</span><span class="sxs-lookup"><span data-stu-id="4d459-128">Validation is supported only for databases that use the Microsoft Access database engine.</span></span>

<span data-ttu-id="4d459-p104">Der von der **ValidationRule**-Eigenschaft eines **Field**-Objekts festgelegte Zeichenfolgenausdruck kann sich nur auf das betreffende **Field**-Objekt beziehen. Der Ausdruck kann sich nicht auf benutzerdefinierte Funktionen, SQL-Aggregatfunktionen oder Abfragen beziehen. Um die **ValidationRule**-Eigenschaft eines **Field**-Objekts festzulegen, wenn seine **ValidateOnSet**-Eigenschaft den Wert **True** hat, muss der Ausdruck erfolgreich analysiert werden (mit dem Feldnamen als impliziter Operand) und den Wert **True** ergeben. Wenn die **ValidateOnSet**-Eigenschaft des Objekts den Wert **False** hat, wird die **ValidationRule**-Einstellung ignoriert.</span><span class="sxs-lookup"><span data-stu-id="4d459-p104">The string expression specified by the **ValidationRule** property of a **Field** object can refer only to that **Field**. The expression can't refer to user-defined functions, SQL aggregate functions, or queries. To set a **Field** object's **ValidationRule** property when its **ValidateOnSet** property setting is **True**, the expression must successfully parse (with the field name as an implied operand) and evaluate to **True**. If its **ValidateOnSet** property setting is **False**, the **ValidationRule** property setting is ignored.</span></span>


> [!NOTE]
> <span data-ttu-id="4d459-133">Wenn Sie die Eigenschaft auf eine Zeichenfolge mit einem nicht-Integer-Wert verkettet festlegen und die Systemparameter einer US-decimal Zeichen wie etwa ein Komma angeben (beispielsweise StrRule = "Preis &gt; " &amp; LngPrice, und LngPrice = 125,50), ein Fehler ausgegeben, wenn der Code versucht, Daten zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="4d459-133">If you set the property to a string concatenated with a non-integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example, strRule = "PRICE &gt; " &amp; lngPrice, and lngPrice = 125,50), an error will result when your code attempts to validate any data.</span></span> <span data-ttu-id="4d459-134">Dies ist, da während der Verkettung die Zahl in eine Zeichenfolge mit Ihr System vorgegebenen Standardzeichen für Dezimalzahlen konvertiert und Microsoft Access-Datenbankmodul SQL nur US-Dezimaltrennzeichen akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="4d459-134">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and Microsoft Access database engine SQL only accepts U.S. decimal characters.</span></span>


