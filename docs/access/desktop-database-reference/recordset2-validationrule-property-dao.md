---
title: Recordset2.ValidationRule-Eigenschaft (DAO)
TOCTitle: ValidationRule Property
ms:assetid: d46cc255-e588-e9e6-66d7-31fc26ae45b8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835002(v=office.15)
ms:contentKeyID: 48547940
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 107841ac3f67507adbf1f8aa722dce163b821d1e
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25931323"
---
# <a name="recordset2validationrule-property-dao"></a><span data-ttu-id="c90d2-102">Recordset2.ValidationRule-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="c90d2-102">Recordset2.ValidationRule property (DAO)</span></span>


<span data-ttu-id="c90d2-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c90d2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c90d2-104">Legt einen Wert fest, der die Daten in einem Feld überprüft, wenn es geändert oder einer Tabelle hinzugefügt wird, oder gibt den betreffenden Wert zurück (nur Microsoft Access-Arbeitsbereiche). **String**-Wert mit Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="c90d2-104">Sets or returns a value that validates the data in a field as it's changed or added to a table (Microsoft Access workspaces only).Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="c90d2-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c90d2-105">Syntax</span></span>

<span data-ttu-id="c90d2-106">*Ausdruck* . ValidationRule</span><span class="sxs-lookup"><span data-stu-id="c90d2-106">*expression* .ValidationRule</span></span>

<span data-ttu-id="c90d2-107">*Ausdruck* Eine Variable, die ein **Recordset2** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="c90d2-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="c90d2-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c90d2-108">Remarks</span></span>

<span data-ttu-id="c90d2-p101">Die Einstellung bzw. der Rückgabewert ist ein **String**-Wert, der einen Vergleich in der Form einer SQL WHERE-Klausel ohne das reservierte Wort WHERE beschreibt. Für ein Objekt, das noch nicht an die **Fields**-Auflistung angehängt wurde, besteht Lese-/Schreibzugriff für diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="c90d2-p101">The settings or return values is a **String** that describes a comparison in the form of an SQL WHERE clause without the WHERE reserved word. For an object not yet appended to the **Fields** collection, this property is read/write.</span></span>

<span data-ttu-id="c90d2-p102">Die **ValidationRule**-Eigenschaft legt fest, ob ein Feld gültige Daten enthält. Wenn die Daten nicht gültig sind, tritt ein auffangbarer Laufzeitfehler auf. Die zurückgegebene Fehlermeldung ist der Text der **ValidationText**-Eigenschaft, sofern er festgelegt wurde, oder der Text des Ausdrucks aus **ValidationRule**.</span><span class="sxs-lookup"><span data-stu-id="c90d2-p102">The **ValidationRule** property determines whether or not a field contains valid data. If the data is not valid, a trappable run-time error occurs. The returned error message is the text of the **ValidationText** property, if specified, or the text of the expression specified by **ValidationRule**.</span></span>

<span data-ttu-id="c90d2-p103">Für ein **Recordset**-Objekt ist die **ValidationRule**-Eigenschaft schreibgeschützt. Für ein **TableDef**-Objekt hängt die Verwendung der **ValidationRule**-Eigenschaft vom Status des **TableDef**-Objekts ab, wie in der folgenden Tabelle dargestellt.</span><span class="sxs-lookup"><span data-stu-id="c90d2-p103">For a **Recordset** object, use of the **ValidationRule** property is read-only. For a **TableDef** object, use of the **ValidationRule** property depends on the status of the **TableDef** object, as the following table shows.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c90d2-116">TableDef</span><span class="sxs-lookup"><span data-stu-id="c90d2-116">TableDef</span></span></p></th>
<th><p><span data-ttu-id="c90d2-117">Verwendung</span><span class="sxs-lookup"><span data-stu-id="c90d2-117">Usage</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c90d2-118">Basistabelle</span><span class="sxs-lookup"><span data-stu-id="c90d2-118">Base table</span></span></p></td>
<td><p><span data-ttu-id="c90d2-119">Lese-/Schreibzugriff</span><span class="sxs-lookup"><span data-stu-id="c90d2-119">Read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c90d2-120">Verknüpfte Tabelle</span><span class="sxs-lookup"><span data-stu-id="c90d2-120">Linked table</span></span></p></td>
<td><p><span data-ttu-id="c90d2-121">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c90d2-121">Read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c90d2-122">Die Gültigkeitsprüfung wird nur für Datenbanken unterstützt, die die Microsoft Access-Datenbank-Engine verwenden.</span><span class="sxs-lookup"><span data-stu-id="c90d2-122">Validation is supported only for databases that use the Microsoft Access database engine.</span></span>

<span data-ttu-id="c90d2-p104">Der von der **ValidationRule**-Eigenschaft eines **Field**-Objekts festgelegte Zeichenfolgenausdruck kann sich nur auf das betreffende **Field**-Objekt beziehen. Der Ausdruck kann sich nicht auf benutzerdefinierte Funktionen, SQL-Aggregatfunktionen oder Abfragen beziehen. Um die **ValidationRule**-Eigenschaft eines **Field**-Objekts festzulegen, wenn seine **ValidateOnSet**-Eigenschaft den Wert **True** hat, muss der Ausdruck erfolgreich analysiert werden (mit dem Feldnamen als impliziter Operand) und den Wert **True** ergeben. Wenn die **ValidateOnSet**-Eigenschaft des Objekts den Wert **False** hat, wird die **ValidationRule**-Einstellung ignoriert.</span><span class="sxs-lookup"><span data-stu-id="c90d2-p104">The string expression specified by the **ValidationRule** property of a **Field** object can refer only to that **Field**. The expression can't refer to user-defined functions, SQL aggregate functions, or queries. To set a **Field** object's **ValidationRule** property when its **ValidateOnSet** property setting is **True**, the expression must successfully parse (with the field name as an implied operand) and evaluate to **True**. If its **ValidateOnSet** property setting is **False**, the **ValidationRule** property setting is ignored.</span></span>

<span data-ttu-id="c90d2-p105">Die **ValidationRule**-Eigenschaft eines **Recordset**- oder **TableDef**-Objekts kann sich auf mehrere Felder in diesem Objekt beziehen. Es gelten die weiter oben in diesem Thema genannten Einschränkungen für das **Field**-Objekt.</span><span class="sxs-lookup"><span data-stu-id="c90d2-p105">The **ValidationRule** property of a **Recordset** or **TableDef** object can refer to multiple fields in that object. The restrictions noted earlier in this topic for the **Field** object apply.</span></span>

<span data-ttu-id="c90d2-129">Bei einem Recordset-Objekt vom Typ Tabelle erbt die ValidationRule-Eigenschaft die ValidationRule-Eigenschaft des TableDef-Objekts, das Sie zum Erstellen des Recordset-Objekts vom Typ Tabelle verwenden.</span><span class="sxs-lookup"><span data-stu-id="c90d2-129">For a table-type **Recordset** object, the **ValidationRule** property inherits the **ValidationRule** property setting of the **TableDef** object that you use to create the table-type **Recordset** object.</span></span>


> [!NOTE]
> <P><span data-ttu-id="c90d2-130">Wenn Sie die Eigenschaft auf eine Zeichenfolge mit einem nicht-Integer-Wert verkettet festlegen und die Systemparameter einer US-decimal Zeichen wie etwa ein Komma angeben (beispielsweise StrRule = "Preis &gt; " &amp; LngPrice, und LngPrice = 125,50), ein Fehler ausgegeben, wenn der Code versucht, Daten zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="c90d2-130">If you set the property to a string concatenated with a non-integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example, strRule = "PRICE &gt; " &amp; lngPrice, and lngPrice = 125,50), an error will result when your code attempts to validate any data.</span></span> <span data-ttu-id="c90d2-131">Dies liegt daran, dass der Wert während der Verkettung mithilfe des Standard-Dezimaltrennzeichens in eine Zeichenfolge konvertiert wird und Microsoft Access SQL nur US-Dezimaltrennzeichen akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="c90d2-131">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and Microsoft Access SQL only accepts U.S. decimal characters.</span></span></P>


