---
title: MoveAndSizeWindow-Makroaktion
TOCTitle: MoveAndSizeWindow macro action
ms:assetid: 86bcf45f-90ce-4ca2-a7fb-efbe5347d137
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197001(v=office.15)
ms:contentKeyID: 48546090
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c1b127995a2f9a0af7da80e9df862259b570870e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288806"
---
# <a name="moveandsizewindow-macro-action"></a><span data-ttu-id="6395c-102">MoveAndSizeWindow-Makroaktion</span><span class="sxs-lookup"><span data-stu-id="6395c-102">MoveAndSizeWindow macro action</span></span>

<span data-ttu-id="6395c-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6395c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6395c-104">Wenn Sie Ihre Dokumentfensteroptionen für die Verwendung von überlappenden Fenstern anstelle von Dokumenten im Registerformat festgelegt haben, können Sie die **verschiebenundgrößeändernfenster** -Aktion verwenden, um das aktive Fenster zu verschieben oder die Größe zu ändern.</span><span class="sxs-lookup"><span data-stu-id="6395c-104">If you have set your document window options to use overlapping windows instead of tabbed documents, you can use the **MoveAndSizeWindow** action to move or resize the active window.</span></span> <span data-ttu-id="6395c-105">Informationen zum Festlegen von Dokumentfensteroptionen finden Sie im Abschnitt "Hinweise".</span><span class="sxs-lookup"><span data-stu-id="6395c-105">For information on how to set document window options, see the Remarks section.</span></span>

## <a name="setting"></a><span data-ttu-id="6395c-106">Einstellung</span><span class="sxs-lookup"><span data-stu-id="6395c-106">Setting</span></span>

<span data-ttu-id="6395c-107">Die **verschiebenundgrößeändernfenster** -Aktion hat die folgenden Argumente.</span><span class="sxs-lookup"><span data-stu-id="6395c-107">The **MoveAndSizeWindow** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6395c-108">Aktionsargument</span><span class="sxs-lookup"><span data-stu-id="6395c-108">Action argument</span></span></p></th>
<th><p><span data-ttu-id="6395c-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6395c-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6395c-110"><strong>Right</strong></span><span class="sxs-lookup"><span data-stu-id="6395c-110"><strong>Right</strong></span></span></p></td>
<td><p><span data-ttu-id="6395c-111">Die neue horizontale Position der linken oberen Ecke des Fensters, gemessen vom linken Rand des enthaltenden Fensters.</span><span class="sxs-lookup"><span data-stu-id="6395c-111">The new horizontal position of the window's upper-left corner, measured from the left edge of its containing window.</span></span> <span data-ttu-id="6395c-112">Geben Sie die Position in das <strong>Rechte</strong> Feld im Abschnitt <strong>Aktionsargumente</strong> des Bereichs Makro-Generator ein.</span><span class="sxs-lookup"><span data-stu-id="6395c-112">Enter the position in the <strong>Right</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6395c-113"><strong>Down</strong></span><span class="sxs-lookup"><span data-stu-id="6395c-113"><strong>Down</strong></span></span></p></td>
<td><p><span data-ttu-id="6395c-114">Die neue vertikale Position der linken oberen Ecke des Fensters, gemessen vom oberen Rand des enthaltenden Fensters.</span><span class="sxs-lookup"><span data-stu-id="6395c-114">The new vertical position of the window's upper-left corner, measured from the top edge of its containing window.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6395c-115"><strong>Width</strong></span><span class="sxs-lookup"><span data-stu-id="6395c-115"><strong>Width</strong></span></span></p></td>
<td><p><span data-ttu-id="6395c-116">Die neue Fensterbreite.</span><span class="sxs-lookup"><span data-stu-id="6395c-116">The window's new width.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6395c-117"><strong>Height</strong></span><span class="sxs-lookup"><span data-stu-id="6395c-117"><strong>Height</strong></span></span></p></td>
<td><p><span data-ttu-id="6395c-118">Die neue Fensterhöhe.</span><span class="sxs-lookup"><span data-stu-id="6395c-118">The window's new height.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6395c-119">Wenn Sie ein Argument leer lassen, verwendet Microsoft Access die aktuelle Einstellung des Fensters.</span><span class="sxs-lookup"><span data-stu-id="6395c-119">If you leave an argument blank, Microsoft Access uses the window's current setting.</span></span>

<span data-ttu-id="6395c-120">Sie müssen einen Wert für mindestens ein Argument eingeben.</span><span class="sxs-lookup"><span data-stu-id="6395c-120">You must enter a value for at least one argument.</span></span>

> [!NOTE]
> <span data-ttu-id="6395c-121">Jede Maßeinheit ist in Zoll oder Zentimetern abhängig von den regionalen Einstellungen in der Windows-Systemsteuerung.</span><span class="sxs-lookup"><span data-stu-id="6395c-121">Each measurement is in inches or centimeters, depending on the regional settings in Windows Control Panel.</span></span>

## <a name="remarks"></a><span data-ttu-id="6395c-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6395c-122">Remarks</span></span>

<span data-ttu-id="6395c-123">Gehen Sie folgendermaßen vor, um eine Anwendung für die Verwendung von überlappenden Fenstern anstelle von Registerkarten Dokumenten einzurichten:</span><span class="sxs-lookup"><span data-stu-id="6395c-123">To set up an application to use overlapping windows instead of tabbed documents, use the following procedure:</span></span>

1.  <span data-ttu-id="6395c-124">Klicken Sie auf **Optionen**</span><span class="sxs-lookup"><span data-stu-id="6395c-124">Click **Options**</span></span>

2.  <span data-ttu-id="6395c-125">Klicken Sie auf **aktuelle Datenbank**.</span><span class="sxs-lookup"><span data-stu-id="6395c-125">Click **Current Database**.</span></span>

3.  <span data-ttu-id="6395c-126">Klicken Sie im Abschnitt **Anwendungsoptionen** unter **Dokumentfensteroptionen** auf **Überlappende Fenster**.</span><span class="sxs-lookup"><span data-stu-id="6395c-126">In the **Application Options** section, under **Document Window Options**, click **Overlapping Windows**.</span></span>

4.  <span data-ttu-id="6395c-127">Klicken Sie auf **OK**, und schließen Sie die Datenbank, und öffnen Sie Sie erneut.</span><span class="sxs-lookup"><span data-stu-id="6395c-127">Click **OK**, and then close and reopen the database.</span></span>

<span data-ttu-id="6395c-128">Diese Aktion ähnelt dem Klicken auf **verschieben** oder **Größe** im **System** Menü des Fensters.</span><span class="sxs-lookup"><span data-stu-id="6395c-128">This action is similar to clicking **Move** or **Size** on the window's **Control** menu.</span></span> <span data-ttu-id="6395c-129">Mit den Menübefehlen können Sie die Pfeiltasten der Tastatur verwenden, um das Fenster zu verschieben oder die Größe zu ändern.</span><span class="sxs-lookup"><span data-stu-id="6395c-129">With the menu commands, you use the keyboard's arrow keys to move or resize the window.</span></span> <span data-ttu-id="6395c-130">Mit der **verschiebenundgrößeändernfenster** -Aktion geben Sie die Positions-und größenmessungen direkt ein.</span><span class="sxs-lookup"><span data-stu-id="6395c-130">With the **MoveAndSizeWindow** action, you enter the position and size measurements directly.</span></span> <span data-ttu-id="6395c-131">Sie können die Maus auch zum Verschieben und Vergrößern von Fenstern verwenden.</span><span class="sxs-lookup"><span data-stu-id="6395c-131">You can also use the mouse to move and size windows.</span></span>

<span data-ttu-id="6395c-132">Sie können diese Aktion für ein beliebiges Fenster in einer beliebigen Ansicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="6395c-132">You can use this action on any window, in any view.</span></span>

> [!TIP]
> - <span data-ttu-id="6395c-133">Wenn Sie ein Fenster ohne Größenänderung verschieben möchten, geben Sie Werte für die Argumente **right** und **down** ein, lassen jedoch die Argumente **Width** und **height** leer.</span><span class="sxs-lookup"><span data-stu-id="6395c-133">To move a window without resizing it, enter values for the **Right** and **Down** arguments but leave the **Width** and **Height** arguments blank.</span></span>
> - <span data-ttu-id="6395c-134">Um die Größe eines Fensters zu ändern, ohne es zu bewegen, geben Sie Werte für die Argumente **Breite** und **Höhe** ein, lassen jedoch die Argumente **Rechts** und **abwärts** leer.</span><span class="sxs-lookup"><span data-stu-id="6395c-134">To resize a window without moving it, enter values for the **Width** and **Height** arguments but leave the **Right** and **Down** arguments blank.</span></span>

<span data-ttu-id="6395c-135">Verwenden Sie die **Move** -Methode des **DoCmd** -Objekts, um die **VERSCHIEBENUNDGRÖßEÄNDERNFENSTER** -Aktion in einem VBA-Modul (Visual Basic für Applikationen) auszuführen.</span><span class="sxs-lookup"><span data-stu-id="6395c-135">To run the **MoveAndSizeWindow** action in a Visual Basic for Applications (VBA) module, use the **MoveSize** method of the **DoCmd** object.</span></span>

## <a name="example"></a><span data-ttu-id="6395c-136">Beispiel</span><span class="sxs-lookup"><span data-stu-id="6395c-136">Example</span></span>

<span data-ttu-id="6395c-137">**Synchronisieren von Formularen mithilfe eines Makros**</span><span class="sxs-lookup"><span data-stu-id="6395c-137">**Synchronize forms by using a macro**</span></span>

<span data-ttu-id="6395c-p104">Das folgende Makro öffnet ein Produktlistenformular in der unteren rechten Ecke des Lieferantenformulars, in dem die Produkte des aktuellen Lieferanten angezeigt werden. Es zeigt die Verwendung der Aktionen **Echo**, **MessageBox**, **GoToControl**, **StopMakro**, **OpenForm** und **MoveAndSizeWindow**. Es veranschaulicht außerdem die Verwendung eines bedingten Ausdrucks mit den Aktionen **MessageBox**, **GoToControl** und **StopMakro**. Dieses Makro sollte der Schaltfläche für die Überprüfung der Produkte im Lieferantenformular zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="6395c-p104">The following macro opens a Product List form in the lower-right corner of the Suppliers form, displaying the current supplier's products. It shows the use of the **Echo**, **MessageBox**, **GoToControl**, **StopMacro**, **OpenForm**, and **MoveAndSizeWindow** actions. It also shows the use of a conditional expression with the **MessageBox**, **GoToControl**, and **StopMacro** actions. This macro should be attached to the Review Products button on the Suppliers form.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6395c-142">Bedingung</span><span class="sxs-lookup"><span data-stu-id="6395c-142">Condition</span></span></p></th>
<th><p><span data-ttu-id="6395c-143">Aktion</span><span class="sxs-lookup"><span data-stu-id="6395c-143">Action</span></span></p></th>
<th><p><span data-ttu-id="6395c-144">Argumente: Einstellung</span><span class="sxs-lookup"><span data-stu-id="6395c-144">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="6395c-145">Kommentar</span><span class="sxs-lookup"><span data-stu-id="6395c-145">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="6395c-146"><strong>Echo</strong></span><span class="sxs-lookup"><span data-stu-id="6395c-146"><strong>Echo</strong></span></span></p></td>
<td><p><span data-ttu-id="6395c-147"><strong>Echo</strong>: <strong>Nein</strong></span><span class="sxs-lookup"><span data-stu-id="6395c-147"><strong>Echo On</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="6395c-148">Beenden der Bildschirmaktualisierung, während das Makro ausgeführt wird</span><span class="sxs-lookup"><span data-stu-id="6395c-148">Stop screen updating while the macro is running.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6395c-149">IsNull ([Lieferanten-ID])</span><span class="sxs-lookup"><span data-stu-id="6395c-149">IsNull([Supplier ID])</span></span></p></td>
<td><p><span data-ttu-id="6395c-150"><strong>MessageBox</strong></span><span class="sxs-lookup"><span data-stu-id="6395c-150"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="6395c-151"><strong>Message</strong>: Wechseln Sie zum Datensatz des Lieferanten, dessen Produkte Sie anzeigen möchten, und klicken Sie dann erneut auf die Schaltfläche für die Überprüfung der Produkte.</span><span class="sxs-lookup"><span data-stu-id="6395c-151"><strong>Message</strong>: Move to the supplier record whose products you want to see, then click the Review Products button again.</span></span> <span data-ttu-id="6395c-152"><strong>Beep</strong>: <strong>jatyp</strong>: <strong>Keinetitel</strong>: Wählen Sie einen Zulieferer aus</span><span class="sxs-lookup"><span data-stu-id="6395c-152"><strong>Beep</strong>: <strong>YesType</strong>: <strong>NoneTitle</strong>: Select a Supplier</span></span></p></td>
<td><p><span data-ttu-id="6395c-153">Wenn im Lieferantenformular kein aktueller Lieferant vorhanden ist, zeigen Sie eine Meldung an.</span><span class="sxs-lookup"><span data-stu-id="6395c-153">If there is no current supplier on the Suppliers form, display a message.</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="6395c-154"><strong>GoToControl</strong></span><span class="sxs-lookup"><span data-stu-id="6395c-154"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="6395c-155"><strong>Steuerelementname</strong>: Firma</span><span class="sxs-lookup"><span data-stu-id="6395c-155"><strong>Control Name</strong>: CompanyName</span></span></p></td>
<td><p><span data-ttu-id="6395c-156">Verschieben Sie den Fokus auf das CompanyName-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="6395c-156">Move focus to the CompanyName control.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6395c-157">...</span><span class="sxs-lookup"><span data-stu-id="6395c-157"></span></span></p></td>
<td><p><span data-ttu-id="6395c-158"><strong>StopMacro</strong></span><span class="sxs-lookup"><span data-stu-id="6395c-158"><strong>StopMacro</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="6395c-159">Halten Sie das Makro an.</span><span class="sxs-lookup"><span data-stu-id="6395c-159">Stop the macro.</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="6395c-160"><strong>OpenForm</strong></span><span class="sxs-lookup"><span data-stu-id="6395c-160"><strong>OpenForm</strong></span></span></p></td>
<td><p><span data-ttu-id="6395c-161"><strong>Formularname</strong>: Produktlisten <strong>Ansicht</strong>: <strong>Datenblatt Filtername</strong>: <strong>Where Condition</strong>: [Supplier ID] = [Forms]! [Lieferanten]! LieferantenNr <strong>Datenmodus</strong>: <strong>Lese-schreibgeschütztfenstermodus-Modus</strong>: <strong>Normal</strong></span><span class="sxs-lookup"><span data-stu-id="6395c-161"><strong>Form Name</strong>: Product List <strong>View</strong>: <strong>DatasheetFilter Name</strong>: <strong>Where Condition</strong>: [Supplier ID] = [Forms]![Suppliers]![SupplierID] <strong>Data Mode</strong>: <strong>Read OnlyWindow Mode</strong>: <strong>Normal</strong></span></span></p></td>
<td><p><span data-ttu-id="6395c-162">Öffnen Sie das Produktlistenformular, und ziegen Sie die Produkte des aktuellen Lieferanten an.</span><span class="sxs-lookup"><span data-stu-id="6395c-162">Open the Product List form and show the current supplier's products.</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="6395c-163"><strong>Verschiebenundgrößeändernfenster</strong></span><span class="sxs-lookup"><span data-stu-id="6395c-163"><strong>MoveAndSizeWindow</strong></span></span></p></td>
<td><p><span data-ttu-id="6395c-164"><strong>rechts</strong>: 0,7799&quot; <strong>unten</strong>: 1,8&quot;</span><span class="sxs-lookup"><span data-stu-id="6395c-164"><strong>Right</strong>: 0.7799&quot; <strong>Down</strong>: 1.8&quot;</span></span></p></td>
<td><p><span data-ttu-id="6395c-165">Positionieren Sie das Produktlistenformular in der unteren rechten Ecke des Lieferantenformulars.</span><span class="sxs-lookup"><span data-stu-id="6395c-165">Position the Product List form in the lower right of the Suppliers form.</span></span></p></td>
</tr>
</tbody>
</table>

