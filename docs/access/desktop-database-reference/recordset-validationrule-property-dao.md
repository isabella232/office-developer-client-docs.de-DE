---
title: Recordset. ValidationRule-Eigenschaft (DAO)
TOCTitle: ValidationRule Property
ms:assetid: c9250c13-18fe-1ff7-7846-7872c49a1e3b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823208(v=office.15)
ms:contentKeyID: 48547671
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e73d81cd890930952835ca6529cc3bfb455e6c21
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307504"
---
# <a name="recordsetvalidationrule-property-dao"></a><span data-ttu-id="b820d-102">Recordset. ValidationRule-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="b820d-102">Recordset.ValidationRule property (DAO)</span></span>

<span data-ttu-id="b820d-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b820d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b820d-104">Legt einen Wert fest, der die Daten in einem Feld überprüft, wenn es geändert oder einer Tabelle hinzugefügt wird, oder gibt den betreffenden Wert zurück (nur Microsoft Access-Arbeitsbereiche). **String**-Wert mit Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="b820d-104">Sets or returns a value that validates the data in a field as it's changed or added to a table (Microsoft Access workspaces only).Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="b820d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b820d-105">Syntax</span></span>

<span data-ttu-id="b820d-106">*Ausdruck* . ValidationRule</span><span class="sxs-lookup"><span data-stu-id="b820d-106">*expression* .ValidationRule</span></span>

<span data-ttu-id="b820d-107">*Ausdruck* Eine Variable, die ein **Recordset** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="b820d-107">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="b820d-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b820d-108">Remarks</span></span>

<span data-ttu-id="b820d-p101">Die Einstellung bzw. der Rückgabewert ist ein **String**-Wert, der einen Vergleich in der Form einer SQL WHERE-Klausel ohne das reservierte Wort WHERE beschreibt. Für ein Objekt, das noch nicht an die **Fields**-Auflistung angehängt wurde, besteht Lese-/Schreibzugriff für diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="b820d-p101">The settings or return values is a **String** that describes a comparison in the form of an SQL WHERE clause without the WHERE reserved word. For an object not yet appended to the **Fields** collection, this property is read/write.</span></span>

<span data-ttu-id="b820d-p102">Die **ValidationRule**-Eigenschaft legt fest, ob ein Feld gültige Daten enthält. Wenn die Daten nicht gültig sind, tritt ein auffangbarer Laufzeitfehler auf. Die zurückgegebene Fehlermeldung ist der Text der **ValidationText**-Eigenschaft, sofern er festgelegt wurde, oder der Text des Ausdrucks aus **ValidationRule**.</span><span class="sxs-lookup"><span data-stu-id="b820d-p102">The **ValidationRule** property determines whether or not a field contains valid data. If the data is not valid, a trappable run-time error occurs. The returned error message is the text of the **ValidationText** property, if specified, or the text of the expression specified by **ValidationRule**.</span></span>

<span data-ttu-id="b820d-p103">Für ein **Recordset**-Objekt ist die **ValidationRule**-Eigenschaft schreibgeschützt. Für ein **TableDef**-Objekt hängt die Verwendung der **ValidationRule**-Eigenschaft vom Status des **TableDef**-Objekts ab, wie in der folgenden Tabelle dargestellt.</span><span class="sxs-lookup"><span data-stu-id="b820d-p103">For a **Recordset** object, use of the **ValidationRule** property is read-only. For a **TableDef** object, use of the **ValidationRule** property depends on the status of the **TableDef** object, as the following table shows.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b820d-116">TableDef</span><span class="sxs-lookup"><span data-stu-id="b820d-116">TableDef</span></span></p></th>
<th><p><span data-ttu-id="b820d-117">Verwendung</span><span class="sxs-lookup"><span data-stu-id="b820d-117">Usage</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b820d-118">Basistabelle</span><span class="sxs-lookup"><span data-stu-id="b820d-118">Base table</span></span></p></td>
<td><p><span data-ttu-id="b820d-119">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b820d-119">Read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b820d-120">Verknüpfte Tabelle</span><span class="sxs-lookup"><span data-stu-id="b820d-120">Linked table</span></span></p></td>
<td><p><span data-ttu-id="b820d-121">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b820d-121">Read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b820d-122">Die Gültigkeitsprüfung wird nur für Datenbanken unterstützt, die die Microsoft Access-Datenbank-Engine verwenden.</span><span class="sxs-lookup"><span data-stu-id="b820d-122">Validation is supported only for databases that use the Microsoft Access database engine.</span></span>

<span data-ttu-id="b820d-p104">Der von der **ValidationRule**-Eigenschaft eines **Field**-Objekts festgelegte Zeichenfolgenausdruck kann sich nur auf das betreffende **Field**-Objekt beziehen. Der Ausdruck kann sich nicht auf benutzerdefinierte Funktionen, SQL-Aggregatfunktionen oder Abfragen beziehen. Um die **ValidationRule**-Eigenschaft eines **Field**-Objekts festzulegen, wenn seine **ValidateOnSet**-Eigenschaft den Wert **True** hat, muss der Ausdruck erfolgreich analysiert werden (mit dem Feldnamen als impliziter Operand) und den Wert **True** ergeben. Wenn die **ValidateOnSet**-Eigenschaft des Objekts den Wert **False** hat, wird die **ValidationRule**-Einstellung ignoriert.</span><span class="sxs-lookup"><span data-stu-id="b820d-p104">The string expression specified by the **ValidationRule** property of a **Field** object can refer only to that **Field**. The expression can't refer to user-defined functions, SQL aggregate functions, or queries. To set a **Field** object's **ValidationRule** property when its **ValidateOnSet** property setting is **True**, the expression must successfully parse (with the field name as an implied operand) and evaluate to **True**. If its **ValidateOnSet** property setting is **False**, the **ValidationRule** property setting is ignored.</span></span>

<span data-ttu-id="b820d-p105">Die **ValidationRule**-Eigenschaft eines **Recordset**- oder **TableDef**-Objekts kann sich auf mehrere Felder in diesem Objekt beziehen. Es gelten die weiter oben in diesem Thema genannten Einschränkungen für das **Field**-Objekt.</span><span class="sxs-lookup"><span data-stu-id="b820d-p105">The **ValidationRule** property of a **Recordset** or **TableDef** object can refer to multiple fields in that object. The restrictions noted earlier in this topic for the **Field** object apply.</span></span>

<span data-ttu-id="b820d-129">For a table-type **Recordset** object, the **ValidationRule** property inherits the **ValidationRule** property setting of the **TableDef** object that you use to create the table-type **Recordset** object.</span><span class="sxs-lookup"><span data-stu-id="b820d-129">For a table-type **Recordset** object, the **ValidationRule** property inherits the **ValidationRule** property setting of the **TableDef** object that you use to create the table-type **Recordset** object.</span></span>

> [!NOTE]
> <span data-ttu-id="b820d-130">Wenn Sie die-Eigenschaft auf eine Zeichenfolge festlegen, die mit einem nicht-ganzzahligen Wert verkettet ist, und die Systemparameter ein nicht-U. S. Decimal-Zeichen wie ein Komma (beispielsweise strRule &gt; = &amp; "Price" lngPrice und lngPrice = 125, 50) angeben, tritt ein Fehler auf, wenn Ihr Code versucht, alle Daten zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="b820d-130">If you set the property to a string concatenated with a non-integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example, strRule = "PRICE &gt; " &amp; lngPrice, and lngPrice = 125,50), an error will result when your code attempts to validate any data.</span></span> <span data-ttu-id="b820d-131">Dies liegt daran, dass der Wert während der Verkettung mithilfe des Standard-Dezimaltrennzeichens in eine Zeichenfolge konvertiert wird und Microsoft Access SQL nur US-Dezimaltrennzeichen akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="b820d-131">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and Microsoft Access SQL only accepts U.S. decimal characters.</span></span>
