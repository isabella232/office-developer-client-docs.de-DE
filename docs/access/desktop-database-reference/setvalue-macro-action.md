---
title: Makroaktion „SetzenWert“
TOCTitle: SetValue Macro Action
ms:assetid: a08be0c1-a053-45f9-b4ae-709fedc58e8b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff820771(v=office.15)
ms:contentKeyID: 48546712
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 36dd3e511a3ff252ca44aa6d10fd1be4acd5c5fb
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25878689"
---
# <a name="setvalue-macro-action"></a><span data-ttu-id="f9ed5-102">Makroaktion „SetzenWert“</span><span class="sxs-lookup"><span data-stu-id="f9ed5-102">SetValue Macro Action</span></span>


<span data-ttu-id="f9ed5-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f9ed5-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="f9ed5-104">Die **SetzenWert** -Aktion können Sie den Wert des Microsoft Access-Felds, eines Steuerelements oder einer Eigenschaft in einem Formular, einem Formulardatenblatt oder einen Bericht festzulegen.</span><span class="sxs-lookup"><span data-stu-id="f9ed5-104">You can use the **SetValue** action to set the value of a Microsoft Access field, control, or property on a form, a form datasheet, or a report.</span></span>


> [!NOTE]
> <P><span data-ttu-id="f9ed5-105">Sie können die Aktion <STRONG>SetzenWert</STRONG> nicht verwenden, um den Wert einer Access-Eigenschaft festzulegen, die ein Objekt zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="f9ed5-105">You cannot use the <STRONG>SetValue</STRONG> action to set the value of an Access property that returns an object.</span></span></P>




> [!NOTE]
> <P><span data-ttu-id="f9ed5-p101">[!HINWEIS] Diese Aktion wird nicht erlaubt, wenn die Datenbank nicht vertrauenswürdig ist. Informationen zur Aktivierung von Makros finden Sie unter den Links im Abschnitt See Also dieses Artikels.</span><span class="sxs-lookup"><span data-stu-id="f9ed5-p101">This action will not be allowed if the database is not trusted. For more information about enabling macros, see the links in the See Also section of this article.</span></span></P>



## <a name="setting"></a><span data-ttu-id="f9ed5-108">Einstellung</span><span class="sxs-lookup"><span data-stu-id="f9ed5-108">Setting</span></span>

<span data-ttu-id="f9ed5-109">Die Aktion **SetzenWert** kann mit den folgenden Argumenten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f9ed5-109">The **SetValue** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f9ed5-110">Aktionsargument</span><span class="sxs-lookup"><span data-stu-id="f9ed5-110">Action argument</span></span></p></th>
<th><p><span data-ttu-id="f9ed5-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f9ed5-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f9ed5-112"><strong>Element</strong></span><span class="sxs-lookup"><span data-stu-id="f9ed5-112"><strong>Item</strong></span></span></p></td>
<td><p><span data-ttu-id="f9ed5-p102">Der Name des Felds, des Steuerelements oder der Eigenschaft, dessen bzw. deren Wert Sie festlegen möchten. Geben Sie den Namen des Felds, des Steuerelements oder der Eigenschaft im Abschnitt <strong>Aktionsargument </strong> des Makro-Generators in das Feld <strong>Element </strong> ein. Verwenden Sie die vollständige Syntax, um auf dieses Element verweisen, z. B.  <em>Steuerelementname </em> (für ein Steuerelement im Formular oder Bericht, in dem das Makro aufgerufen wurde) oder <strong>Formulare</strong>!<em>Formularname</em>!<em>Steuerelementname</em>. Dies ist ein erforderliches Argument.</span><span class="sxs-lookup"><span data-stu-id="f9ed5-p102">The name of the field, control, or property whose value you want to set. Enter the field, control, or property name in the <strong>Item</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane. You must use the full syntax to refer to this item, such as <em>controlname</em> (for a control on the form or report from which the macro was called) or <strong>Forms</strong>!<em>formname</em>!<em>controlname</em>. This is a required argument.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f9ed5-117"><strong>Expression</strong></span><span class="sxs-lookup"><span data-stu-id="f9ed5-117"><strong>Expression</strong></span></span></p></td>
<td><p><span data-ttu-id="f9ed5-p103">Der Ausdruck, den Access verwendet, um den Wert für dieses Element festzulegen. Sie müssen immer die vollständige Syntax verwenden, um auf Objekte im Ausdruck zu verweisen. Um beispielsweise den Wert eines Steuerelements für das Gehalt in einem Formular für Mitarbeiter um 10 Prozent zu erhöhen, verwenden Sie Forms!Employees!Salary\*1.1. Dies ist ein erforderliches Argument.</span><span class="sxs-lookup"><span data-stu-id="f9ed5-p103">The expression Access uses to set the value for this item. You must always use the full syntax to refer to any objects in the expression. For example, to increase the value in a Salary control on an Employees form by 10 percent, use Forms!Employees!Salary\*1.1. This is a required argument.</span></span></p>

> [!NOTE]
> <P><span data-ttu-id="f9ed5-122">Verwenden Sie kein Gleichheitszeichen (<STRONG>=</STRONG>) vor dem Ausdruck in diesem Argument.</span><span class="sxs-lookup"><span data-stu-id="f9ed5-122">You shouldn't use an equal sign (<STRONG>=</STRONG>) before the expression in this argument.</span></span> <span data-ttu-id="f9ed5-123">In diesem Fall Access wertet den Ausdruck und verwendet diesen Wert als den Ausdruck in diesem Argument.</span><span class="sxs-lookup"><span data-stu-id="f9ed5-123">If you do, Access evaluates the expression and then uses this value as the expression in this argument.</span></span> <span data-ttu-id="f9ed5-124">Wenn der Ausdruck eine Zeichenfolge ist, können unerwartete Ergebnisse auftreten.</span><span class="sxs-lookup"><span data-stu-id="f9ed5-124">This can produce unexpected results if the expression is a string.</span></span></P>


<p><span data-ttu-id="f9ed5-125">Beispiel: bei Eingabe <strong> = &quot;Zeichenfolge1&quot; </strong> für dieses Argument wertet Access zuerst den Ausdruck als Zeichenfolge1.</span><span class="sxs-lookup"><span data-stu-id="f9ed5-125">For example, if you type <strong>=&quot;String1&quot;</strong> for this argument, Access first evaluates the expression as String1.</span></span> <span data-ttu-id="f9ed5-126">Klicken Sie dann verwendet Zeichenfolge1 als Ausdruck, der in diesem Argument und erwartet ein Steuerelement oder eine Eigenschaft mit dem Namen String1 im Formular oder Bericht, der das Makro aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="f9ed5-126">Then it uses String1 as the expression in this argument, expecting to find a control or property named String1 on the form or report that called the macro.</span></span></p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> <P><span data-ttu-id="f9ed5-127">Klicken Sie in einer Access-Datenbank (MDB oder ACCDB) auf die Schaltfläche <STRONG>Erstellen</STRONG> , um den Ausdrucks-Generator verwenden Sie zum Erstellen eines Ausdrucks für eines der folgenden Argumente.</span><span class="sxs-lookup"><span data-stu-id="f9ed5-127">In an Access database (.mdb or .accdb), click the <STRONG>Build</STRONG> button to use the Expression Builder to create an expression for either of these arguments.</span></span></P>



## <a name="remarks"></a><span data-ttu-id="f9ed5-128">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f9ed5-128">Remarks</span></span>

<span data-ttu-id="f9ed5-p106">Sie können diese Aktion verwenden, um einen Wert für ein Feld oder Steuerelement in einem Formular, einem Formulardatenblatt oder einem Bericht festzulegen. Sie können außerdem den Wert für nahezu alle Steuerelement-, Formular- und Berichtseigenschaften in jeder Ansicht festlegen. Informationen dazu, ob eine bestimmte Eigenschaft mit einem Makro und in welchen Ansichten die Eigenschaft festgelegt werden kann, finden Sie im Hilfethema für die jeweilige Eigenschaft im Visual Basic-Editor.</span><span class="sxs-lookup"><span data-stu-id="f9ed5-p106">You can use this action to set a value for a field or control on a form, a form datasheet, or a report. You can also set the value for almost all control, form, and report properties in any view. To find out whether a particular property can be set by using a macro and which views it can be set in, see the Help topic for that property in the Visual Basic Editor.</span></span>

<span data-ttu-id="f9ed5-132">Sie können auch den Wert für ein Feld in einem Formular zugrunde liegenden Tabelle festlegen, sogar dann, wenn das Formular ein Steuerelement, das an das Feld gebunden.</span><span class="sxs-lookup"><span data-stu-id="f9ed5-132">You can also set the value for a field in a form's underlying table even if the form doesn't contain a control bound to the field.</span></span> <span data-ttu-id="f9ed5-133">Verwenden Sie die Syntax **Forms**\!*Formname*\!*Fieldname* im **Element** um den Wert für ein solches Feld festzulegen.</span><span class="sxs-lookup"><span data-stu-id="f9ed5-133">Use the syntax **Forms**\!*formname*\!*fieldname* in the **Item** box to set the value for such a field.</span></span> <span data-ttu-id="f9ed5-134">Sie können auch auf ein Feld in einem Bericht zugrunde liegenden Tabelle verweisen, indem Sie mithilfe der Syntax **Berichte**\!*Reportname*\!*Fieldname*, aber es ein Steuerelement auf den Bericht an dieses Feld gebunden muss, oder das Feld werden, die in bezeichnet muss einer berechneten Steuerelement im Bericht.</span><span class="sxs-lookup"><span data-stu-id="f9ed5-134">You can also refer to a field in a report's underlying table by using the syntax **Reports**\!*reportname*\!*fieldname*, but there must be a control on the report bound to this field, or the field must be referred to in a calculated control on the report.</span></span>

<span data-ttu-id="f9ed5-p108">Wenn Sie den Wert eines Steuerelements in einem Formular festlegen, löst die Aktion **SetzenWert** nicht die Gültigkeitsprüfungsregeln auf Formularebene des Steuerelements, sondern die Gültigkeitsprüfungsregeln auf Tabellenebene des zugrunde liegendenen Felds aus, wenn das Steuerelement ein gebundenes Steuerelement ist. Die Aktion **SetzenWert** löst außerdem eine Neuberechnung aus, die aber nicht unbedingt sofort erfolgt. Um eine sofortige Aktualisierung auszulösen und den Abschluss der Neuberechnung zu erzwingen, verwenden Sie die Aktion **AktualisierenObjekt**. Der Wert, den Sie in einem Steuerelement mithilfe der Aktion \*\*SetzenWert \*\* festlegen, wird außerdem nicht vom Eingabeformat beeinflusst, das in der Eigenschaft **InputMask** des Steuerelements oder zugrunde liegenden Felds festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="f9ed5-p108">If you set the value of a control on a form, the **SetValue** action doesn't trigger the control's form-level validation rules, but it does trigger the underlying field's table-level validation rules if the control is a bound control. The **SetValue** action also triggers recalculation, but the recalculation may not happen immediately. To trigger immediate repainting and force the recalculation to completion, use the **RepaintObject** action. The value you set in a control by using the **SetValue** action is also not affected by an input mask set in the control's or underlying field's **InputMask** property.</span></span>

<span data-ttu-id="f9ed5-p109">Um den Wert eines Steuerelements zu ändern, können Sie die Aktion **SetzenWert** Aktion in einem Makro verwenden, das durch die Ereigniseigenschaft **NachAktualisierung** des Steuerelements angegeben ist. Sie können Aktion **SetzenWert** jedoch nicht in einem Makro verwenden, das durch die Ereigniseigenschaft **VorAktualisierung** eines Steuerelements angegeben ist, um den Wert des Steuerelements zu ändern (Sie können die Aktion \*\*SetzenWert \*\* aber zum Ändern des Werts anderer Steuerelemente verwenden). Sie können die Aktion **SetzenWert** außerdem in einem von der Eigenschaft **VorAktualisieurng** oder **NachAktualisierung** eines Formulars angegebenem Makro verwenden, um den Wert eines beliebigen Steuerelements im aktuellen Datensatz zu ändern.</span><span class="sxs-lookup"><span data-stu-id="f9ed5-p109">To change the value of a control, you can use the **SetValue** action in a macro specified by the control's **AfterUpdate** event property. However, you can't use the **SetValue** action in a macro specified by a control's **BeforeUpdate** event property to change the value of the control (although you can use the **SetValue** action to change the value of other controls). You can also use the **SetValue** action in a macro specified by the **BeforeUpdate** or **AfterUpdate** property of a form to change the value of any controls in the current record.</span></span>


> [!NOTE]
> <P><span data-ttu-id="f9ed5-142">Die Werte der folgenden Steuerelemente können nicht mit der Aktion <STRONG>SetzenWert </STRONG> festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="f9ed5-142">You can't use the <STRONG>SetValue</STRONG> action to set the value of the following controls:</span></span></P>
> <UL>
> <LI>
> <P><span data-ttu-id="f9ed5-143">Gebundene Steuerelemente und berechnete Steuerelemente in Berichten</span><span class="sxs-lookup"><span data-stu-id="f9ed5-143">Bound controls and calculated controls on reports.</span></span></P>
> <LI>
> <P><span data-ttu-id="f9ed5-144">Berechnete Steuerelemente in Formularen</span><span class="sxs-lookup"><span data-stu-id="f9ed5-144">Calculated controls on forms.</span></span></P></LI></UL>




> [!TIP]
> <P><span data-ttu-id="f9ed5-p110">Sie können die Aktion <STRONG>SetzenWert</STRONG> verwenden, um ein Formular in der Formularansicht ein- oder auszublenden. Geben Sie <STRONG>Formulare</STRONG>!<EM>Formularname</EM><STRONG>Sichtbar</STRONG> in das Feld <STRONG>Element</STRONG> und <STRONG>Nein</STRONG> oder <STRONG>Ja</STRONG> in das Feld <STRONG>Ausdruck</STRONG> ein. Wenn Sie die Eigenschaft <STRONG>Sichtbar</STRONG> eines modalen Formulars auf <STRONG>Nein</STRONG> festlegen, wird das Formular ausgeblendet und nicht modal. Wenn Sie die Eigenschaft auf <STRONG>Ja</STRONG>, wird das Formular eingeblendet und wieder modal.</span><span class="sxs-lookup"><span data-stu-id="f9ed5-p110">You can use the <STRONG>SetValue</STRONG> action to hide or show a form in Form view. Enter <STRONG>Forms</STRONG>!<EM>formname</EM><STRONG>.Visible</STRONG> in the <STRONG>Item</STRONG> box and <STRONG>No</STRONG> or <STRONG>Yes</STRONG> in the <STRONG>Expression</STRONG> box. Setting a modal form's <STRONG>Visible</STRONG> property to <STRONG>No</STRONG> hides the form and makes it modeless. Setting the property to <STRONG>Yes</STRONG> displays the form and makes it modal again.</span></span></P>



<span data-ttu-id="f9ed5-p111">Wenn Sie über die Aktion **SetzenWert** in einem Makro den Wert eines Steuerelements ändern oder neue Daten in einem Steuerelement hinzufügen, werden keine Ereignisse wie **VorAktualisierung**, **VorEingabe** oder **Änderung** ausgelöst, die auftreten, wenn Sie in diesen Steuerelementen in der Benutzeroberfläche Daten ändern oder Daten eingeben. Diese Ereignisse treten ebenfalls nicht auf, wenn Sie den Wert des Steuerelements mithilfe eines VBA-Moduls (Visual Basic for Applications) festlegen.</span><span class="sxs-lookup"><span data-stu-id="f9ed5-p111">Changing the value of or adding new data in a control by using the **SetValue** action in a macro doesn't trigger events such as **BeforeUpdate**, **BeforeInsert**, or **Change** that occur when you change or enter data in these controls in the user interface. These events also don't occur if you set the value of the control by using a Visual Basic for Applications (VBA) module.</span></span>

<span data-ttu-id="f9ed5-p112">Diese Aktion ist in einem VBA-Modul nicht verfügbar. Legen Sie den Wert direkt in VBA fest.</span><span class="sxs-lookup"><span data-stu-id="f9ed5-p112">This action isn't available in a VBA module. Set the value directly in VBA.</span></span>

## <a name="example"></a><span data-ttu-id="f9ed5-153">Beispiel</span><span class="sxs-lookup"><span data-stu-id="f9ed5-153">Example</span></span>

<span data-ttu-id="f9ed5-154">**Festlegen des Werts eines Steuerelements mithilfe eines Makros**</span><span class="sxs-lookup"><span data-stu-id="f9ed5-154">**Set the value of a control by using a macro**</span></span>

<span data-ttu-id="f9ed5-p113">Das folgende Makro öffnet das Formular zum Hinzufügen von Produkten über eine Schaltfläche im Formular für Lieferanten. Es zeigt die Verwendung der Aktionen **Echo**, **FensterSchließen**, **ÖffnenFormular**, \*\*SetzenWert \*\* und **GeheZuSteuerelement**. Die Aktion **SetzenWert** legt das SupplierID-Steuerelement im Produktformular auf den aktuellen Lieferanten im Lieferantenformular fest. Die Aktion **GeheZuSteuerelement** verschiebt dann den Fokus auf das Feld „CategoryID“, in dem Sie beginnen können, Daten für das neue Produkt einzugeben. Dieses Makro sollte der Schaltfläche zum Hinzufügen von Produkten im Formular für Lieferanten zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="f9ed5-p113">The following macro opens the Add Products form from a button on the Suppliers form. It shows the use of the **Echo**, **CloseWindow**, **OpenForm**, **SetValue**, and **GoToControl** actions. The **SetValue** action sets the SupplierID control on the Products form to the current supplier on the Suppliers form. The **GoToControl** action then moves the focus to the CategoryID field, where you can begin to enter data for the new product. This macro should be attached to the Add Products button on the Suppliers form.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f9ed5-160">Aktion</span><span class="sxs-lookup"><span data-stu-id="f9ed5-160">Action</span></span></p></th>
<th><p><span data-ttu-id="f9ed5-161">Argumente: Einstellung</span><span class="sxs-lookup"><span data-stu-id="f9ed5-161">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="f9ed5-162">Kommentar</span><span class="sxs-lookup"><span data-stu-id="f9ed5-162">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f9ed5-163"><strong>Echo</strong></span><span class="sxs-lookup"><span data-stu-id="f9ed5-163"><strong>Echo</strong></span></span></p></td>
<td><p><span data-ttu-id="f9ed5-164"><strong>Echo</strong>: <strong>Nein</strong></span><span class="sxs-lookup"><span data-stu-id="f9ed5-164"><strong>Echo On</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="f9ed5-165">Beenden der Bildschirmaktualisierung, während das Makro ausgeführt wird</span><span class="sxs-lookup"><span data-stu-id="f9ed5-165">Stop screen updating while the macro is running.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f9ed5-166"><strong>FensterSchließen</strong></span><span class="sxs-lookup"><span data-stu-id="f9ed5-166"><strong>CloseWindow</strong></span></span></p></td>
<td><p><span data-ttu-id="f9ed5-167"><strong>Objekttyp</strong>: <strong>FormObject Name</strong>: Produkt Liste <strong>Speichern</strong>: <strong>Nein</strong></span><span class="sxs-lookup"><span data-stu-id="f9ed5-167"><strong>Object Type</strong>: <strong>FormObject Name</strong>: Product List <strong>Save</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="f9ed5-168">Schließen des Produktlistenformulars</span><span class="sxs-lookup"><span data-stu-id="f9ed5-168">Close the Product List form.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f9ed5-169"><strong>ÖffnenFormular</strong></span><span class="sxs-lookup"><span data-stu-id="f9ed5-169"><strong>OpenForm</strong></span></span></p></td>
<td><p><span data-ttu-id="f9ed5-170"><strong>Formularname</strong>: Produkte <strong>Anzeigen</strong>: <strong>FormData Modus</strong>: <strong>Fenster hinzufügen Modus</strong>: <strong>Normal</strong></span><span class="sxs-lookup"><span data-stu-id="f9ed5-170"><strong>Form Name</strong>: Products <strong>View</strong>: <strong>FormData Mode</strong>: <strong>AddWindow Mode</strong>: <strong>Normal</strong></span></span></p></td>
<td><p><span data-ttu-id="f9ed5-171">Öffnen des Produktformulars</span><span class="sxs-lookup"><span data-stu-id="f9ed5-171">Open the Products form.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f9ed5-172"><strong>SetzenWert</strong></span><span class="sxs-lookup"><span data-stu-id="f9ed5-172"><strong>SetValue</strong></span></span></p></td>
<td><p><span data-ttu-id="f9ed5-173"><strong>Artikel</strong>: [Formulare]! [Artikel]! [Lieferanten-Nr] <strong>Ausdruck</strong>: SupplierID</span><span class="sxs-lookup"><span data-stu-id="f9ed5-173"><strong>Item</strong>: [Forms]![Products]![SupplierID] <strong>Expression</strong>: SupplierID</span></span></p></td>
<td><p><span data-ttu-id="f9ed5-174">Festlegen des SupplierID-Steuerelements auf den aktuellen Lieferanten im Formular für Lieferanten</span><span class="sxs-lookup"><span data-stu-id="f9ed5-174">Set the SupplierID control to the current supplier on the Suppliers form.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f9ed5-175"><strong>GeheZuSteuerelement</strong></span><span class="sxs-lookup"><span data-stu-id="f9ed5-175"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="f9ed5-176"><strong>Steuerelementname</strong>: CategoryID</span><span class="sxs-lookup"><span data-stu-id="f9ed5-176"><strong>Control Name</strong>: CategoryID</span></span></p></td>
<td><p><span data-ttu-id="f9ed5-177">Wechseln zum CategoryID-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="f9ed5-177">Go to the CategoryID control.</span></span></p></td>
</tr>
</tbody>
</table>

