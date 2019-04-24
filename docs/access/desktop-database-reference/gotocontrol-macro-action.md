---
title: GoToControl-Makroaktion
TOCTitle: GoToControl macro action
ms:assetid: caff76dc-7ca8-4f87-8144-89445ed4600d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834370(v=office.15)
ms:contentKeyID: 48547705
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c056f2b0922402ea7cde7cf767969b73f912f572
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292167"
---
# <a name="gotocontrol-macro-action"></a><span data-ttu-id="79ad9-102">GoToControl-Makroaktion</span><span class="sxs-lookup"><span data-stu-id="79ad9-102">GoToControl macro action</span></span>

<span data-ttu-id="79ad9-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="79ad9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="79ad9-104">Sie können die **GoToControl** -Aktion verwenden, um den Fokus auf das angegebene Feld oder Steuerelement im aktuellen Datensatz des geöffneten Formulars, des Formulardatenblatts, des Tabellendatenblatts oder des Abfragedatenblatts zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="79ad9-104">You can use the **GoToControl** action to move the focus to the specified field or control in the current record of the open form, form datasheet, table datasheet, or query datasheet.</span></span> <span data-ttu-id="79ad9-105">Sie können diese Aktion verwenden, wenn ein bestimmtes Feld oder Steuerelement den Fokus haben soll.</span><span class="sxs-lookup"><span data-stu-id="79ad9-105">You can use this action when you want a particular field or control to have the focus.</span></span> <span data-ttu-id="79ad9-106">Dieses Feld oder Steuerelement kann dann zu Vergleichszwecken oder für **FindRecord**-Aktionen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="79ad9-106">This field or control can then be used for comparisons or **FindRecord** actions.</span></span> <span data-ttu-id="79ad9-107">Sie können die Aktion auch zum Navigieren in einem Formular basierend auf bestimmten Bedingungen verwenden.</span><span class="sxs-lookup"><span data-stu-id="79ad9-107">You can also use this action to navigate in a form according to certain conditions.</span></span> <span data-ttu-id="79ad9-108">Wenn der Benutzer z. B. im Steuerelement „Verheiratet“ auf einem Versicherungsformular „Nein“ angibt, kann der Fokus automatisch das Steuerelement „Name des Partners/der Partnerin“ überspringen und zum nächsten Steuerelement wechseln.</span><span class="sxs-lookup"><span data-stu-id="79ad9-108">For example, if the user enters No in a Married control on a health insurance form, the focus can automatically skip the Spouse/partner Name control and move to the next control.</span></span>

## <a name="setting"></a><span data-ttu-id="79ad9-109">Einstellung</span><span class="sxs-lookup"><span data-stu-id="79ad9-109">Setting</span></span>

> [!NOTE]
> <span data-ttu-id="79ad9-110">Diese Aktion steht nicht für die Verwendung mit Datenzugriffsseiten zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="79ad9-110">This action is not available for use with data access pages.</span></span>

<span data-ttu-id="79ad9-111">Die **GeheZuSteuerelement**-Aktion hat die folgenden Argumente.</span><span class="sxs-lookup"><span data-stu-id="79ad9-111">The **GoToControl** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="79ad9-112">Aktionsargument</span><span class="sxs-lookup"><span data-stu-id="79ad9-112">Action argument</span></span></p></th>
<th><p><span data-ttu-id="79ad9-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="79ad9-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="79ad9-114"><strong>Steuerelementname</strong></span><span class="sxs-lookup"><span data-stu-id="79ad9-114"><strong>Control Name</strong></span></span></p></td>
<td><p><span data-ttu-id="79ad9-115">Der Name des Felds oder Steuerelements, das den Fokus erhalten soll.</span><span class="sxs-lookup"><span data-stu-id="79ad9-115">The name of the field or control where you want the focus.</span></span> <span data-ttu-id="79ad9-116">Geben Sie das Feld oder den Steuerelementnamen in das Feld <strong>Steuerelementname</strong> im Abschnitt <strong>Aktionsargumente</strong> des Bereichs Makro-Generator ein.</span><span class="sxs-lookup"><span data-stu-id="79ad9-116">Enter the field or control name in the <strong>Control Name</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span> <span data-ttu-id="79ad9-117">Dies ist ein erforderliches Argument.</span><span class="sxs-lookup"><span data-stu-id="79ad9-117">This is a required argument.</span></span></p>
<p><span data-ttu-id="79ad9-118"><strong>Hinweis</strong>: Geben Sie in das Argument <strong>Steuerelementname</strong> nur den Namen des Felds oder Steuerelements ein, nicht den vollqualifizierten Bezeichner, wie beispielsweise Formulare! Produkte! [Produkt-ID].</span><span class="sxs-lookup"><span data-stu-id="79ad9-118"><strong>NOTE</strong>: Enter only the name of the field or control in the <strong>Control Name</strong> argument, not the fully qualified identifier, such as Forms!Products![Product ID].</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="79ad9-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="79ad9-119">Remarks</span></span>

<span data-ttu-id="79ad9-120">Sie können die **GoToControl** -Aktion nicht verwenden, um den Fokus auf ein Steuerelement in einem ausgeblendeten Formular zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="79ad9-120">You cannot use the **GoToControl** action to move the focus to a control on a hidden form.</span></span>

> [!TIP]
> <span data-ttu-id="79ad9-121">Sie können die **GoToControl** -Aktion verwenden, um zu einem Unterformular zu wechseln, bei dem es sich um einen Steuerelementtyp handelt.</span><span class="sxs-lookup"><span data-stu-id="79ad9-121">You can use the **GoToControl** action to move to a subform, which is a type of control.</span></span> <span data-ttu-id="79ad9-122">Sie können dann die **GoToRecord** -Aktion verwenden, um zu einem bestimmten Datensatz im Unterformular zu wechseln.</span><span class="sxs-lookup"><span data-stu-id="79ad9-122">You can then use the **GoToRecord** action to move to a particular record in the subform.</span></span> <span data-ttu-id="79ad9-123">Sie können auch zu einem Steuerelement in einem Unterformular wechseln, indem \*\*\*\* Sie die GoToControl-Aktion verwenden, um zuerst zum Unterformular und dann zum Steuerelement des Unterformulars zu wechseln.</span><span class="sxs-lookup"><span data-stu-id="79ad9-123">You can also move to a control on a subform by using the **GoToControl** action to move first to the subform and then to the control on the subform.</span></span>

<span data-ttu-id="79ad9-124">Verwenden Sie die GoToControl-Methode des **DoCmd** -Objekts, um die **GoToControl** -Aktion in \*\*\*\* einem VBA-Modul (Visual Basic für Applikationen) auszuführen.</span><span class="sxs-lookup"><span data-stu-id="79ad9-124">To run the **GoToControl** action in a Visual Basic for Applications (VBA) module, use the **GoToControl** method of the **DoCmd** object.</span></span> <span data-ttu-id="79ad9-125">Sie können die SetFocus \*\*\*\* -Methode auch verwenden, um den Fokus auf ein Steuerelement in einem Formular oder einem seiner Unterformulare oder auf ein Feld in einem geöffneten Tabellen-, Abfrage-oder Formulardatenblatt zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="79ad9-125">You can also use the **SetFocus** method to move the focus to a control on a form or any of its subforms, or to a field in an open table, query, or form datasheet.</span></span>

## <a name="examples"></a><span data-ttu-id="79ad9-126">Beispiele</span><span class="sxs-lookup"><span data-stu-id="79ad9-126">Examples</span></span>

<span data-ttu-id="79ad9-127">**Festlegen des Werts eines Steuerelements mithilfe eines Makros**</span><span class="sxs-lookup"><span data-stu-id="79ad9-127">**Set the value of a control by using a macro**</span></span>

<span data-ttu-id="79ad9-128">Das folgende Makro öffnet das Formular zum Hinzufügen von Produkten über eine Schaltfläche im Formular für Lieferanten.</span><span class="sxs-lookup"><span data-stu-id="79ad9-128">The following macro opens the Add Products form from a button on the Suppliers form.</span></span> <span data-ttu-id="79ad9-129">Es zeigt die Verwendung der Aktionen **Echo**, **FensterSchließen**, **ÖffnenFormular**, \*\*SetzenWert \*\* und **GeheZuSteuerelement**.</span><span class="sxs-lookup"><span data-stu-id="79ad9-129">It shows the use of the **Echo**, **CloseWindow**, **OpenForm**, **SetValue**, and **GoToControl** actions.</span></span> <span data-ttu-id="79ad9-130">Mit \*\*\*\* der SetValue-Aktion wird das Lieferanten-ID-Steuerelement im Formular Produkte auf den aktuellen Lieferanten im Formular Lieferanten festgelegt.</span><span class="sxs-lookup"><span data-stu-id="79ad9-130">The **SetValue** action sets the Supplier ID control on the Products form to the current supplier on the Suppliers form.</span></span> <span data-ttu-id="79ad9-131">Die **gotoCONTROL** -Aktion verschiebt dann den Fokus auf das Feld Kategorie-ID, in dem Sie mit der Eingabe von Daten für das neue Produkt beginnen können.</span><span class="sxs-lookup"><span data-stu-id="79ad9-131">The **GoToControl** action then moves the focus to the Category ID field, where you can begin to enter data for the new product.</span></span> <span data-ttu-id="79ad9-132">Dieses Makro sollte der Schaltfläche zum Hinzufügen von Produkten im Formular für Lieferanten zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="79ad9-132">This macro should be attached to the Add Products button on the Suppliers form.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="79ad9-133">Aktion</span><span class="sxs-lookup"><span data-stu-id="79ad9-133">Action</span></span></p></th>
<th><p><span data-ttu-id="79ad9-134">Argumente: Einstellung</span><span class="sxs-lookup"><span data-stu-id="79ad9-134">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="79ad9-135">Kommentar</span><span class="sxs-lookup"><span data-stu-id="79ad9-135">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="79ad9-136"><strong>Echo</strong></span><span class="sxs-lookup"><span data-stu-id="79ad9-136"><strong>Echo</strong></span></span></p></td>
<td><p><span data-ttu-id="79ad9-137"><strong>Echo</strong>: <strong>Nein</strong></span><span class="sxs-lookup"><span data-stu-id="79ad9-137"><strong>Echo On</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="79ad9-138">Beenden der Bildschirmaktualisierung, während das Makro ausgeführt wird</span><span class="sxs-lookup"><span data-stu-id="79ad9-138">Stop screen updating while the macro is running.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="79ad9-139"><strong>Fenster schließen</strong></span><span class="sxs-lookup"><span data-stu-id="79ad9-139"><strong>CloseWindow</strong></span></span></p></td>
<td><p><span data-ttu-id="79ad9-140"><strong>Objekttyp</strong>: <strong>Formularobjekt Name</strong>: Produktlisten <strong>Speicher</strong>: <strong>Nein</strong></span><span class="sxs-lookup"><span data-stu-id="79ad9-140"><strong>Object Type</strong>: <strong>FormObject Name</strong>: Product List <strong>Save</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="79ad9-141">Produktlisten Formular abschließen.</span><span class="sxs-lookup"><span data-stu-id="79ad9-141">Close Product List form.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="79ad9-142"><strong>OpenForm</strong></span><span class="sxs-lookup"><span data-stu-id="79ad9-142"><strong>OpenForm</strong></span></span></p></td>
<td><p><span data-ttu-id="79ad9-143"><strong>Formular Name</strong>: Produkt <strong>Ansicht</strong>: <strong>FormData Modus</strong>: <strong>addwindow Mode</strong>: <strong>Normal</strong></span><span class="sxs-lookup"><span data-stu-id="79ad9-143"><strong>Form Name</strong>: Products <strong>View</strong>: <strong>FormData Mode</strong>: <strong>AddWindow Mode</strong>: <strong>Normal</strong></span></span></p></td>
<td><p><span data-ttu-id="79ad9-144">Öffnen des Produktformulars</span><span class="sxs-lookup"><span data-stu-id="79ad9-144">Open the Products form.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="79ad9-145"><strong>SetzenWert</strong></span><span class="sxs-lookup"><span data-stu-id="79ad9-145"><strong>SetValue</strong></span></span></p></td>
<td><p><span data-ttu-id="79ad9-146"><strong>Element</strong>: [Formulare]! [Products]! LieferantenNr <strong>Ausdruck</strong>: Lieferanten-Nr.</span><span class="sxs-lookup"><span data-stu-id="79ad9-146"><strong>Item</strong>: [Forms]![Products]![SupplierID] <strong>Expression</strong>: SupplierID</span></span></p></td>
<td><p><span data-ttu-id="79ad9-147">Legen Sie das Lieferanten-ID-Steuerelement auf den aktuellen Lieferanten im Formular Lieferanten fest.</span><span class="sxs-lookup"><span data-stu-id="79ad9-147">Set the Supplier ID control to the current supplier on the Suppliers form.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="79ad9-148"><strong>GoToControl</strong></span><span class="sxs-lookup"><span data-stu-id="79ad9-148"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="79ad9-149"><strong>Steuerelementname</strong>: CategoryID</span><span class="sxs-lookup"><span data-stu-id="79ad9-149"><strong>Control Name</strong>: CategoryID</span></span></p></td>
<td><p><span data-ttu-id="79ad9-150">Wechseln Sie zum Steuerelement Category ID.</span><span class="sxs-lookup"><span data-stu-id="79ad9-150">Go to the Category ID control.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="79ad9-151">**Validate data by using a macro**</span><span class="sxs-lookup"><span data-stu-id="79ad9-151">**Validate data by using a macro**</span></span>

<span data-ttu-id="79ad9-152">Mit dem folgenden Gültigkeitsprüfungsmakro werden die Postleitzahlen überprüft, die im Lieferantenformular eingegeben werden.</span><span class="sxs-lookup"><span data-stu-id="79ad9-152">The following validation macro checks the postal codes entered in a Suppliers form.</span></span> <span data-ttu-id="79ad9-153">Es zeigt die Verwendung der Aktionen **StopMacro**, **MessageBox**, **CancelEvent** und **GoToControl**.</span><span class="sxs-lookup"><span data-stu-id="79ad9-153">It shows the use of the **StopMacro**, **MessageBox**, **CancelEvent**, and **GoToControl** actions.</span></span> <span data-ttu-id="79ad9-154">A conditional expression checks the country/region and postal code entered in a record on the form.</span><span class="sxs-lookup"><span data-stu-id="79ad9-154">A conditional expression checks the country/region and postal code entered in a record on the form.</span></span> <span data-ttu-id="79ad9-155">If the postal code is not in the right format for the country/region, the macro displays a message box and cancels saving the record.</span><span class="sxs-lookup"><span data-stu-id="79ad9-155">If the postal code is not in the right format for the country/region, the macro displays a message box and cancels saving the record.</span></span> <span data-ttu-id="79ad9-156">Das Makro gibt Sie dann an das Postleitzahl-Steuerelement zurück, in dem Sie den Fehler korrigieren können.</span><span class="sxs-lookup"><span data-stu-id="79ad9-156">The macro then returns you to the Postal Code control, where you can correct the error.</span></span> <span data-ttu-id="79ad9-157">Dieses Makro sollte mit der  **BeforeUpdate**-Eigenschaft des Lieferantenformulars verbunden sein.</span><span class="sxs-lookup"><span data-stu-id="79ad9-157">This macro should be attached to the **BeforeUpdate** property of the Suppliers form.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="79ad9-158">Bedingung</span><span class="sxs-lookup"><span data-stu-id="79ad9-158">Condition</span></span></p></th>
<th><p><span data-ttu-id="79ad9-159">Aktion</span><span class="sxs-lookup"><span data-stu-id="79ad9-159">Action</span></span></p></th>
<th><p><span data-ttu-id="79ad9-160">Argumente: Einstellung</span><span class="sxs-lookup"><span data-stu-id="79ad9-160">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="79ad9-161">Kommentar</span><span class="sxs-lookup"><span data-stu-id="79ad9-161">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="79ad9-162">IsNull ([CountryRegion])</span><span class="sxs-lookup"><span data-stu-id="79ad9-162">IsNull([CountryRegion])</span></span></p></td>
<td><p><span data-ttu-id="79ad9-163"><strong>StopMacro</strong></span><span class="sxs-lookup"><span data-stu-id="79ad9-163"><strong>StopMacro</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="79ad9-164">Wenn CountryRegion ist <strong></strong>, kann die Postleitzahl nicht validiert werden.</span><span class="sxs-lookup"><span data-stu-id="79ad9-164">If CountryRegion is <strong>Null</strong>, postal code cannot be validated.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="79ad9-165">CountryRegion In (&quot;Frankreich&quot;,&quot;Italien&quot;,&quot;Spanien&quot;) und Len ([Postleitzahl] &lt; &gt; ) 5</span><span class="sxs-lookup"><span data-stu-id="79ad9-165">[CountryRegion] In (&quot;France&quot;,&quot;Italy&quot;,&quot;Spain&quot;) And Len([Postal Code]) &lt;&gt; 5</span></span></p></td>
<td><p><span data-ttu-id="79ad9-166"><strong>MessageBox</strong></span><span class="sxs-lookup"><span data-stu-id="79ad9-166"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="79ad9-167"><strong>Message</strong>: Die Postleitzahl muss 5 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="79ad9-167"><strong>Message</strong>: The postal code must be 5 characters.</span></span> <span data-ttu-id="79ad9-168"><strong>Beep</strong>: <strong>jatyp</strong>: <strong>informationtitel</strong>: PLZ-Fehler</span><span class="sxs-lookup"><span data-stu-id="79ad9-168"><strong>Beep</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: Postal Code Error</span></span></p></td>
<td><p><span data-ttu-id="79ad9-169">Wenn die Postleitzahl nicht 5 Zeichen ist, wird eine Meldung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="79ad9-169">If the postal code is not 5 characters, display a message.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="79ad9-170">...</span><span class="sxs-lookup"><span data-stu-id="79ad9-170"></span></span></p></td>
<td><p><span data-ttu-id="79ad9-171"><strong>CancelEvent</strong></span><span class="sxs-lookup"><span data-stu-id="79ad9-171"><strong>CancelEvent</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="79ad9-172">Bricht das Ereignis ab.</span><span class="sxs-lookup"><span data-stu-id="79ad9-172">Cancel the event.</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="79ad9-173"><strong>GoToControl</strong></span><span class="sxs-lookup"><span data-stu-id="79ad9-173"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="79ad9-174"><strong>Steuerelementname</strong>: PostalCode</span><span class="sxs-lookup"><span data-stu-id="79ad9-174"><strong>Control Name</strong>: PostalCode</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="79ad9-175">CountryRegion In (&quot;Australien&quot;,&quot;Singapur&quot;) und Len ([Postleitzahl] &lt; &gt; ) 4</span><span class="sxs-lookup"><span data-stu-id="79ad9-175">[CountryRegion] In (&quot;Australia&quot;,&quot;Singapore&quot;) And Len([Postal Code]) &lt;&gt; 4</span></span></p></td>
<td><p><span data-ttu-id="79ad9-176"><strong>MessageBox</strong></span><span class="sxs-lookup"><span data-stu-id="79ad9-176"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="79ad9-177">Meldung: Die Postleitzahl muss 4 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="79ad9-177">Message: The postal code must be 4 characters.</span></span> <span data-ttu-id="79ad9-178"><strong>Beep</strong>: <strong>jatyp</strong>: <strong>informationtitel</strong>: PLZ-Fehler</span><span class="sxs-lookup"><span data-stu-id="79ad9-178"><strong>Beep</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: Postal Code Error</span></span></p></td>
<td><p><span data-ttu-id="79ad9-179">Wenn die Postleitzahl nicht 4 Zeichen ist, zeigen Sie eine Nachricht an.</span><span class="sxs-lookup"><span data-stu-id="79ad9-179">If the postal code is not 4 characters, display a message.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="79ad9-180">...</span><span class="sxs-lookup"><span data-stu-id="79ad9-180"></span></span></p></td>
<td><p><span data-ttu-id="79ad9-181"><strong>CancelEvent</strong></span><span class="sxs-lookup"><span data-stu-id="79ad9-181"><strong>CancelEvent</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="79ad9-182">Bricht das Ereignis ab.</span><span class="sxs-lookup"><span data-stu-id="79ad9-182">Cancel the event.</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="79ad9-183"><strong>GoToControl</strong></span><span class="sxs-lookup"><span data-stu-id="79ad9-183"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="79ad9-184"><strong>Steuerelementname</strong>: PostalCode</span><span class="sxs-lookup"><span data-stu-id="79ad9-184"><strong>Control Name</strong>: PostalCode</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="79ad9-185">([CountryRegion] = &quot;Kanada&quot;) Und ([Postleitzahl] nicht&quot;wie [A-z] [0-9] [A-z] [0-9] [A-z] [0-9&quot;])</span><span class="sxs-lookup"><span data-stu-id="79ad9-185">([CountryRegion] = &quot;Canada&quot;) And ([Postal Code] Not Like&quot;[A-Z][0-9][A-Z] [0-9][A-Z][0-9]&quot;)</span></span></p></td>
<td><p><span data-ttu-id="79ad9-186"><strong>MessageBox</strong></span><span class="sxs-lookup"><span data-stu-id="79ad9-186"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="79ad9-187"><strong>Meldung</strong>: Die Postleitzahl ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="79ad9-187"><strong>Message</strong>: The postal code is not valid.</span></span> <span data-ttu-id="79ad9-188">Beispiel für kanadischen Code: H1J 1C3 <strong>Beep</strong>: <strong>jatyp</strong>: <strong>informationtitel</strong>: PLZ Error</span><span class="sxs-lookup"><span data-stu-id="79ad9-188">Example of Canadian code: H1J 1C3 <strong>Beep</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: Postal Code Error</span></span></p></td>
<td><p><span data-ttu-id="79ad9-189">Wenn die Postleitzahl für Kanada nicht korrekt ist, zeigen Sie eine Nachricht an.</span><span class="sxs-lookup"><span data-stu-id="79ad9-189">If the postal code is not correct for Canada, display a message.</span></span> <span data-ttu-id="79ad9-190">(Beispiel für eine kanadische Postleitzahl: H1J 1C3).</span><span class="sxs-lookup"><span data-stu-id="79ad9-190">(Example of Canadian code: H1J 1C3)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="79ad9-191">...</span><span class="sxs-lookup"><span data-stu-id="79ad9-191"></span></span></p></td>
<td><p><span data-ttu-id="79ad9-192"><strong>CancelEvent</strong></span><span class="sxs-lookup"><span data-stu-id="79ad9-192"><strong>CancelEvent</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="79ad9-193">Bricht das Ereignis ab.</span><span class="sxs-lookup"><span data-stu-id="79ad9-193">Cancel the event.</span></span></p></td>
</tr>
</tbody>
</table>

