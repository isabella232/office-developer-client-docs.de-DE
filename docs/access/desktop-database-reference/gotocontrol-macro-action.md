---
title: GoToControl-Makroaktion
TOCTitle: GoToControl macro action
ms:assetid: caff76dc-7ca8-4f87-8144-89445ed4600d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834370(v=office.15)
ms:contentKeyID: 48547705
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3e5318652430f6cb9564fb1bb02832cc120b080b
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/07/2018
ms.locfileid: "26026246"
---
# <a name="gotocontrol-macro-action"></a><span data-ttu-id="45b8b-102">GoToControl-Makroaktion</span><span class="sxs-lookup"><span data-stu-id="45b8b-102">GoToControl macro action</span></span>

<span data-ttu-id="45b8b-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="45b8b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="45b8b-104">Sie können die **GeheZuSteuerelement** -Aktion verwenden, um den Fokus auf das angegebene Feld oder Steuerelement im aktuellen Datensatz des geöffneten Formulars, Datenblattes, Tabellendatenblatt oder Datenblatt Abfragen.</span><span class="sxs-lookup"><span data-stu-id="45b8b-104">You can use the **GoToControl** action to move the focus to the specified field or control in the current record of the open form, form datasheet, table datasheet, or query datasheet.</span></span> <span data-ttu-id="45b8b-105">Sie können diese Aktion verwenden, wenn ein bestimmtes Feld oder Steuerelement den Fokus haben soll.</span><span class="sxs-lookup"><span data-stu-id="45b8b-105">You can use this action when you want a particular field or control to have the focus.</span></span> <span data-ttu-id="45b8b-106">Dieses Feld oder Steuerelement kann dann für Vergleiche oder **SuchenDatensatz** -Aktionen verwendet.</span><span class="sxs-lookup"><span data-stu-id="45b8b-106">This field or control can then be used for comparisons or **FindRecord** actions.</span></span> <span data-ttu-id="45b8b-107">Sie können die Aktion auch zum Navigieren in einem Formular basierend auf bestimmten Bedingungen verwenden.</span><span class="sxs-lookup"><span data-stu-id="45b8b-107">You can also use this action to navigate in a form according to certain conditions.</span></span> <span data-ttu-id="45b8b-108">Wenn der Benutzer z. B. im Steuerelement „Verheiratet“ auf einem Versicherungsformular „Nein“ angibt, kann der Fokus automatisch das Steuerelement „Name des Partners/der Partnerin“ überspringen und zum nächsten Steuerelement wechseln.</span><span class="sxs-lookup"><span data-stu-id="45b8b-108">For example, if the user enters No in a Married control on a health insurance form, the focus can automatically skip the Spouse/partner Name control and move to the next control.</span></span>

## <a name="setting"></a><span data-ttu-id="45b8b-109">Einstellung</span><span class="sxs-lookup"><span data-stu-id="45b8b-109">Setting</span></span>

> [!NOTE]
> <span data-ttu-id="45b8b-110">Diese Aktion ist nicht für die Verwendung mit Datenzugriffsseiten verfügbar.</span><span class="sxs-lookup"><span data-stu-id="45b8b-110">This action is not available for use with data access pages.</span></span>

<span data-ttu-id="45b8b-111">Die **GeheZuSteuerelement**-Aktion hat die folgenden Argumente.</span><span class="sxs-lookup"><span data-stu-id="45b8b-111">The **GoToControl** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="45b8b-112">Aktionsargument</span><span class="sxs-lookup"><span data-stu-id="45b8b-112">Action argument</span></span></p></th>
<th><p><span data-ttu-id="45b8b-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="45b8b-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="45b8b-114"><strong>Steuerelementname</strong></span><span class="sxs-lookup"><span data-stu-id="45b8b-114"><strong>Control Name</strong></span></span></p></td>
<td><p><span data-ttu-id="45b8b-115">Der Name des Felds oder Steuerelements, das den Fokus erhalten soll.</span><span class="sxs-lookup"><span data-stu-id="45b8b-115">The name of the field or control where you want the focus.</span></span> <span data-ttu-id="45b8b-116">Geben Sie den Namen Feld oder Steuerelement in das Feld <strong>Steuerelementname</strong> im Abschnitt <strong>Aktionsargument</strong> des Makro-Generators ein.</span><span class="sxs-lookup"><span data-stu-id="45b8b-116">Enter the field or control name in the <strong>Control Name</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span> <span data-ttu-id="45b8b-117">Dies ist ein erforderliches Argument.</span><span class="sxs-lookup"><span data-stu-id="45b8b-117">This is a required argument.</span></span></p>
<p><span data-ttu-id="45b8b-118"><strong>Hinweis</strong>: Geben Sie nur den Namen des Felds oder Steuerelements in das Argument <strong>Steuerelementname</strong> nicht den vollqualifizierten Bezeichner wie Formulare! Produkte! [Produkt-ID].</span><span class="sxs-lookup"><span data-stu-id="45b8b-118"><strong>NOTE</strong>: Enter only the name of the field or control in the <strong>Control Name</strong> argument, not the fully qualified identifier, such as Forms!Products![Product ID].</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="45b8b-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="45b8b-119">Remarks</span></span>

<span data-ttu-id="45b8b-120">Sie können die **GeheZuSteuerelement** -Aktion um den Fokus auf ein Steuerelement in einem ausgeblendeten Formular zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="45b8b-120">You cannot use the **GoToControl** action to move the focus to a control on a hidden form.</span></span>

> [!TIP]
> <span data-ttu-id="45b8b-121">Die **GeheZuSteuerelement** -Aktion können Sie auf ein Unterformular setzen, das eine Art von Steuerelement ist.</span><span class="sxs-lookup"><span data-stu-id="45b8b-121">You can use the **GoToControl** action to move to a subform, which is a type of control.</span></span> <span data-ttu-id="45b8b-122">Die **GeheZuDatensatz** -Aktion können dann um auf einen bestimmten Datensatz im Unterformular zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="45b8b-122">You can then use the **GoToRecord** action to move to a particular record in the subform.</span></span> <span data-ttu-id="45b8b-123">Sie können auch auf ein Steuerelement eines Unterformulars verschieben, mit die **GeheZuSteuerelement** -Aktion um auf das Unterformular, und klicken Sie dann auf das Steuerelement des Unterformulars zuerst zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="45b8b-123">You can also move to a control on a subform by using the **GoToControl** action to move first to the subform and then to the control on the subform.</span></span>

<span data-ttu-id="45b8b-124">Führen Sie die **GeheZuSteuerelement** -Aktion in einem Visual Basic für Applikationen (VBA) Modul mit **der GoToControl** -Methode des **DoCmd** -Objekts.</span><span class="sxs-lookup"><span data-stu-id="45b8b-124">To run the **GoToControl** action in a Visual Basic for Applications (VBA) module, use the **GoToControl** method of the **DoCmd** object.</span></span> <span data-ttu-id="45b8b-125">Sie können auch die **SetFocus** -Methode verwenden, um den Fokus auf ein Steuerelement eines Formulars oder eines seiner Unterformulare oder an ein Feld in einer geöffneten Tabelle, Abfrage oder Formulardatenblatt.</span><span class="sxs-lookup"><span data-stu-id="45b8b-125">You can also use the **SetFocus** method to move the focus to a control on a form or any of its subforms, or to a field in an open table, query, or form datasheet.</span></span>

## <a name="examples"></a><span data-ttu-id="45b8b-126">Beispiele</span><span class="sxs-lookup"><span data-stu-id="45b8b-126">Examples</span></span>

<span data-ttu-id="45b8b-127">**Festlegen des Werts eines Steuerelements mithilfe eines Makros**</span><span class="sxs-lookup"><span data-stu-id="45b8b-127">**Set the value of a control by using a macro**</span></span>

<span data-ttu-id="45b8b-128">Mit dem folgende Makro wird das Formular Artikel Hinzufügen einer Schaltfläche auf dem Formular Lieferanten geöffnet.</span><span class="sxs-lookup"><span data-stu-id="45b8b-128">The following macro opens the Add Products form from a button on the Suppliers form.</span></span> <span data-ttu-id="45b8b-129">Es wird die Verwendung der **Echo**, **CloseWindow**, **ÖffnenFormular**, **SetzenWert**und **GeheZuSteuerelement** -Aktionen.</span><span class="sxs-lookup"><span data-stu-id="45b8b-129">It shows the use of the **Echo**, **CloseWindow**, **OpenForm**, **SetValue**, and **GoToControl** actions.</span></span> <span data-ttu-id="45b8b-130">Die **SetzenWert** -Aktion wird das Steuerelement Lieferanten-ID auf dem Formular auf den aktuellen Lieferanten im Formular Suppliers angezeigt.</span><span class="sxs-lookup"><span data-stu-id="45b8b-130">The **SetValue** action sets the Supplier ID control on the Products form to the current supplier on the Suppliers form.</span></span> <span data-ttu-id="45b8b-131">Klicken Sie dann die **GeheZuSteuerelement** -Aktion verschiebt den Fokus auf das Feld Kategorie-ID, beginnen Sie können Daten für das neue Produkt eingeben.</span><span class="sxs-lookup"><span data-stu-id="45b8b-131">The **GoToControl** action then moves the focus to the Category ID field, where you can begin to enter data for the new product.</span></span> <span data-ttu-id="45b8b-132">Dieses Makro sollte der Schaltfläche Artikel hinzufügen im Formular Lieferanten zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="45b8b-132">This macro should be attached to the Add Products button on the Suppliers form.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="45b8b-133">Aktion</span><span class="sxs-lookup"><span data-stu-id="45b8b-133">Action</span></span></p></th>
<th><p><span data-ttu-id="45b8b-134">Argumente: Einstellung</span><span class="sxs-lookup"><span data-stu-id="45b8b-134">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="45b8b-135">Kommentar</span><span class="sxs-lookup"><span data-stu-id="45b8b-135">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="45b8b-136"><strong>Echo</strong></span><span class="sxs-lookup"><span data-stu-id="45b8b-136"><strong>Echo</strong></span></span></p></td>
<td><p><span data-ttu-id="45b8b-137"><strong>Echo</strong>: <strong>Nein</strong></span><span class="sxs-lookup"><span data-stu-id="45b8b-137"><strong>Echo On</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="45b8b-138">Beenden der Bildschirmaktualisierung, während das Makro ausgeführt wird</span><span class="sxs-lookup"><span data-stu-id="45b8b-138">Stop screen updating while the macro is running.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="45b8b-139"><strong>FensterSchließen</strong></span><span class="sxs-lookup"><span data-stu-id="45b8b-139"><strong>CloseWindow</strong></span></span></p></td>
<td><p><span data-ttu-id="45b8b-140"><strong>Objekttyp</strong>: <strong>FormObject Name</strong>: Produkt Liste <strong>Speichern</strong>: <strong>Nein</strong></span><span class="sxs-lookup"><span data-stu-id="45b8b-140"><strong>Object Type</strong>: <strong>FormObject Name</strong>: Product List <strong>Save</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="45b8b-141">Produktliste Formular zu schließen.</span><span class="sxs-lookup"><span data-stu-id="45b8b-141">Close Product List form.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="45b8b-142"><strong>ÖffnenFormular</strong></span><span class="sxs-lookup"><span data-stu-id="45b8b-142"><strong>OpenForm</strong></span></span></p></td>
<td><p><span data-ttu-id="45b8b-143"><strong>Formularname</strong>: Produkte <strong>Anzeigen</strong>: <strong>FormData Modus</strong>: <strong>Fenster hinzufügen Modus</strong>: <strong>Normal</strong></span><span class="sxs-lookup"><span data-stu-id="45b8b-143"><strong>Form Name</strong>: Products <strong>View</strong>: <strong>FormData Mode</strong>: <strong>AddWindow Mode</strong>: <strong>Normal</strong></span></span></p></td>
<td><p><span data-ttu-id="45b8b-144">Öffnen des Produktformulars</span><span class="sxs-lookup"><span data-stu-id="45b8b-144">Open the Products form.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="45b8b-145"><strong>SetzenWert</strong></span><span class="sxs-lookup"><span data-stu-id="45b8b-145"><strong>SetValue</strong></span></span></p></td>
<td><p><span data-ttu-id="45b8b-146"><strong>Artikel</strong>: [Formulare]! [Artikel]! [Lieferanten-Nr] <strong>Ausdruck</strong>: SupplierID</span><span class="sxs-lookup"><span data-stu-id="45b8b-146"><strong>Item</strong>: [Forms]![Products]![SupplierID] <strong>Expression</strong>: SupplierID</span></span></p></td>
<td><p><span data-ttu-id="45b8b-147">Legen Sie das Steuerelement auf den aktuellen Lieferanten im Formular Suppliers angezeigt.</span><span class="sxs-lookup"><span data-stu-id="45b8b-147">Set the Supplier ID control to the current supplier on the Suppliers form.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="45b8b-148"><strong>GoToControl</strong></span><span class="sxs-lookup"><span data-stu-id="45b8b-148"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="45b8b-149"><strong>Steuerelementname</strong>: CategoryID</span><span class="sxs-lookup"><span data-stu-id="45b8b-149"><strong>Control Name</strong>: CategoryID</span></span></p></td>
<td><p><span data-ttu-id="45b8b-150">Wechseln Sie auf die Kategorie-ID-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="45b8b-150">Go to the Category ID control.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="45b8b-151">\*\* Überprüfen der Gültigkeit von Daten mithilfe eines Makros\*\*</span><span class="sxs-lookup"><span data-stu-id="45b8b-151">**Validate data by using a macro**</span></span>

<span data-ttu-id="45b8b-152">Mit dem folgenden Gültigkeitsprüfungsmakro werden die Postleitzahlen überprüft, die im Lieferantenformular eingegeben werden.</span><span class="sxs-lookup"><span data-stu-id="45b8b-152">The following validation macro checks the postal codes entered in a Suppliers form.</span></span> <span data-ttu-id="45b8b-153">Es zeigt die Verwendung der Aktionen **StopMacro**, **MessageBox**, **CancelEvent** und **GoToControl**.</span><span class="sxs-lookup"><span data-stu-id="45b8b-153">It shows the use of the **StopMacro**, **MessageBox**, **CancelEvent**, and **GoToControl** actions.</span></span> <span data-ttu-id="45b8b-154">Mit einem Bedingungsausdruck werden das Land, die Region und die Postleitzahl überprüft, die im Formular in einem Datensatz eingegeben werden.</span><span class="sxs-lookup"><span data-stu-id="45b8b-154">A conditional expression checks the country/region and postal code entered in a record on the form.</span></span> <span data-ttu-id="45b8b-155">Wenn die Postleitzahl nicht das richtige Format für das Land/Region ist, wird das Makro ein Meldungsfeld angezeigt und Speichern des Datensatzes wird abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="45b8b-155">If the postal code is not in the right format for the country/region, the macro displays a message box and cancels saving the record.</span></span> <span data-ttu-id="45b8b-156">Das Makro gibt dann Sie auf das Steuerelement Postleitzahl, in dem Sie den Fehler korrigieren.</span><span class="sxs-lookup"><span data-stu-id="45b8b-156">The macro then returns you to the Postal Code control, where you can correct the error.</span></span> <span data-ttu-id="45b8b-157">Dieses Makro sollte mit der **BeforeUpdate** -Eigenschaft des Lieferantenformulars verbunden sein.</span><span class="sxs-lookup"><span data-stu-id="45b8b-157">This macro should be attached to the **BeforeUpdate** property of the Suppliers form.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="45b8b-158">Bedingung</span><span class="sxs-lookup"><span data-stu-id="45b8b-158">Condition</span></span></p></th>
<th><p><span data-ttu-id="45b8b-159">Aktion</span><span class="sxs-lookup"><span data-stu-id="45b8b-159">Action</span></span></p></th>
<th><p><span data-ttu-id="45b8b-160">Argumente: Einstellung</span><span class="sxs-lookup"><span data-stu-id="45b8b-160">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="45b8b-161">Kommentar</span><span class="sxs-lookup"><span data-stu-id="45b8b-161">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="45b8b-162">IsNull([CountryRegion])</span><span class="sxs-lookup"><span data-stu-id="45b8b-162">IsNull([CountryRegion])</span></span></p></td>
<td><p><span data-ttu-id="45b8b-163"><strong>StopMacro</strong></span><span class="sxs-lookup"><span data-stu-id="45b8b-163"><strong>StopMacro</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="45b8b-164">Wenn Land/Region <strong>Null</strong>ist, kann die Postleitzahl nicht überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="45b8b-164">If CountryRegion is <strong>Null</strong>, postal code cannot be validated.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="45b8b-165">[Land/Region] In (&quot;Frankreich&quot;,&quot;Italien&quot;,&quot;Spanien&quot;) und Len ([Postleitzahl]) &lt; &gt; 5</span><span class="sxs-lookup"><span data-stu-id="45b8b-165">[CountryRegion] In (&quot;France&quot;,&quot;Italy&quot;,&quot;Spain&quot;) And Len([Postal Code]) &lt;&gt; 5</span></span></p></td>
<td><p><span data-ttu-id="45b8b-166"><strong>MessageBox</strong></span><span class="sxs-lookup"><span data-stu-id="45b8b-166"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="45b8b-167"><strong>Message</strong>: Die Postleitzahl muss 5 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="45b8b-167"><strong>Message</strong>: The postal code must be 5 characters.</span></span> <span data-ttu-id="45b8b-168"><strong>Signalton</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: Postleitzahl fehlerhaft</span><span class="sxs-lookup"><span data-stu-id="45b8b-168"><strong>Beep</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: Postal Code Error</span></span></p></td>
<td><p><span data-ttu-id="45b8b-169">Wenn die Postleitzahl nicht 5 Zeichen lang ist, wird eine Meldung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="45b8b-169">If the postal code is not 5 characters, display a message.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="45b8b-170">...</span><span class="sxs-lookup"><span data-stu-id="45b8b-170"></span></span></p></td>
<td><p><span data-ttu-id="45b8b-171"><strong>CancelEvent</strong></span><span class="sxs-lookup"><span data-stu-id="45b8b-171"><strong>CancelEvent</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="45b8b-172">Bricht das Ereignis ab.</span><span class="sxs-lookup"><span data-stu-id="45b8b-172">Cancel the event.</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="45b8b-173"><strong>GoToControl</strong></span><span class="sxs-lookup"><span data-stu-id="45b8b-173"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="45b8b-174"><strong>Steuerelementname</strong>: PostalCode</span><span class="sxs-lookup"><span data-stu-id="45b8b-174"><strong>Control Name</strong>: PostalCode</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="45b8b-175">[Land/Region] In (&quot;Australien&quot;,&quot;Singapur&quot;) und Len ([Postleitzahl]) &lt; &gt; 4</span><span class="sxs-lookup"><span data-stu-id="45b8b-175">[CountryRegion] In (&quot;Australia&quot;,&quot;Singapore&quot;) And Len([Postal Code]) &lt;&gt; 4</span></span></p></td>
<td><p><span data-ttu-id="45b8b-176"><strong>MessageBox</strong></span><span class="sxs-lookup"><span data-stu-id="45b8b-176"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="45b8b-177">Message: Die Postleitzahl muss 4 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="45b8b-177">Message: The postal code must be 4 characters.</span></span> <span data-ttu-id="45b8b-178"><strong>Signalton</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: Postleitzahl fehlerhaft</span><span class="sxs-lookup"><span data-stu-id="45b8b-178"><strong>Beep</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: Postal Code Error</span></span></p></td>
<td><p><span data-ttu-id="45b8b-179">Wenn die Postleitzahl nicht 4 Zeichen lang ist, wird eine Meldung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="45b8b-179">If the postal code is not 4 characters, display a message.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="45b8b-180">...</span><span class="sxs-lookup"><span data-stu-id="45b8b-180"></span></span></p></td>
<td><p><span data-ttu-id="45b8b-181"><strong>CancelEvent</strong></span><span class="sxs-lookup"><span data-stu-id="45b8b-181"><strong>CancelEvent</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="45b8b-182">Bricht das Ereignis ab.</span><span class="sxs-lookup"><span data-stu-id="45b8b-182">Cancel the event.</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="45b8b-183"><strong>GoToControl</strong></span><span class="sxs-lookup"><span data-stu-id="45b8b-183"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="45b8b-184"><strong>Steuerelementname</strong>: PostalCode</span><span class="sxs-lookup"><span data-stu-id="45b8b-184"><strong>Control Name</strong>: PostalCode</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="45b8b-185">([Land/Region] = &quot;Kanada&quot;) Und ([Postleitzahl] nicht wie&quot;[A-Z] [0-9] [A-Z] [0-9] [A-Z] [0-9]&quot;)</span><span class="sxs-lookup"><span data-stu-id="45b8b-185">([CountryRegion] = &quot;Canada&quot;) And ([Postal Code] Not Like&quot;[A-Z][0-9][A-Z] [0-9][A-Z][0-9]&quot;)</span></span></p></td>
<td><p><span data-ttu-id="45b8b-186"><strong>MessageBox</strong></span><span class="sxs-lookup"><span data-stu-id="45b8b-186"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="45b8b-187"><strong>Meldung</strong>: Die Postleitzahl ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="45b8b-187"><strong>Message</strong>: The postal code is not valid.</span></span> <span data-ttu-id="45b8b-188">Beispiel für kanadische Postleitzahl: H1J 1 c 3 <strong>Signalton</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: PLZ Codefehler</span><span class="sxs-lookup"><span data-stu-id="45b8b-188">Example of Canadian code: H1J 1C3 <strong>Beep</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: Postal Code Error</span></span></p></td>
<td><p><span data-ttu-id="45b8b-189">Wenn die Postleitzahl nicht korrekt für Kanada ist, wird eine Meldung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="45b8b-189">If the postal code is not correct for Canada, display a message.</span></span> <span data-ttu-id="45b8b-190">(Beispiel für eine kanadische Postleitzahl: H1J 1C3).</span><span class="sxs-lookup"><span data-stu-id="45b8b-190">(Example of Canadian code: H1J 1C3)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="45b8b-191">...</span><span class="sxs-lookup"><span data-stu-id="45b8b-191"></span></span></p></td>
<td><p><span data-ttu-id="45b8b-192"><strong>CancelEvent</strong></span><span class="sxs-lookup"><span data-stu-id="45b8b-192"><strong>CancelEvent</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="45b8b-193">Bricht das Ereignis ab.</span><span class="sxs-lookup"><span data-stu-id="45b8b-193">Cancel the event.</span></span></p></td>
</tr>
</tbody>
</table>

