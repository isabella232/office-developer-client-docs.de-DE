---
title: Für schnelle Ablage Dialogfeld Feld Schnittstellen (OneNote 2013)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: d83e39f0-b259-4c33-8f3e-e03e94c2403d
description: In diesem Thema werden die Schnittstellen, die Sie zum programmgesteuerten Anpassung des Dialogfelds Quick Ablegen in OneNote 2013 verwenden können.
ms.openlocfilehash: dd6b28ae6cb2acb007bae26ea661facaf1f8d4be
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317098"
---
# <a name="quick-filing-dialog-box-interfaces-onenote"></a><span data-ttu-id="818bb-103">Für schnelle Ablage Dialogfeld Feld Schnittstellen (OneNote 2013)</span><span class="sxs-lookup"><span data-stu-id="818bb-103">Quick Filing dialog box interfaces (OneNote)</span></span>

<span data-ttu-id="818bb-104">In diesem Thema werden die Schnittstellen, die Sie zum programmgesteuerten Anpassung des Dialogfelds Quick Ablegen in OneNote 2013 verwenden können.</span><span class="sxs-lookup"><span data-stu-id="818bb-104">This topic describes the interfaces that you can use to programmatically customize the Quick Filing dialog box in OneNote 2013.</span></span>
  
## <a name="quick-filing-dialog-box"></a><span data-ttu-id="818bb-105">Dialogfeld "schnell Ablage"</span><span class="sxs-lookup"><span data-stu-id="818bb-105">Quick Filing dialog box</span></span>

<span data-ttu-id="818bb-p101">Das Dialogfeld Quick Ablegen in OneNote 2013 ist anpassbare Dialogfeld, in dem Benutzer eine Position in der Hierarchiestruktur OneNote auswählen kann. Auswählbar Speicherorte enthalten Notebooks, Abschnittsgruppen, Abschnitte, Seiten und Unterseiten. Das Dialogfeld wird sowohl in der OneNote-Anwendung und externen Anwendungen über die OneNote 2013 API verwendet. Abbildung 1 zeigt das Dialogfeld Quick Ablegen im Standardzustand.</span><span class="sxs-lookup"><span data-stu-id="818bb-p101">The Quick Filing dialog box in OneNote 2013 is a customizable dialog box that allows users to select a location within the OneNote hierarchy structure. Selectable locations include notebooks, section groups, sections, pages, and subpages. The dialog box is used both within the OneNote application and by external applications through the OneNote 2013 API. Figure 1 shows the Quick Filing dialog box in its default state.</span></span>
  
<span data-ttu-id="818bb-110">**Abbildung 1. Dialogfeld für schnelle Ablage ohne Anpassungen**</span><span class="sxs-lookup"><span data-stu-id="818bb-110">**Figure 1. Quick Filing dialog box without customizations**</span></span>

<span data-ttu-id="818bb-111">![Dialogfeld "schnell Ablage" ohne Anpassungen] (media/ON15Con_quick_filing_dialog.jpg "Dialogfeld \"schnell Ablage\" ohne Anpassungen")</span><span class="sxs-lookup"><span data-stu-id="818bb-111">![Quick Filing dialog box without customizations](media/ON15Con_quick_filing_dialog.jpg "Quick Filing dialog box without customizations")</span></span>
  
<span data-ttu-id="818bb-p102">Innerhalb des Dialogfelds können Benutzer die Hierarchie alle Notizbücher zum Suchen für bestimmte Standorte oder die OneNote-Struktur durch Eingabe in das Textfeld Suchen navigieren. Aspekten im Dialogfeld angepasst werden kann, gehören Titel, Beschreibung, letzte Liste "Suchergebnisse", das Kontrollkästchen Text und Zustand, Strukturtiefe, Schaltflächen und auswählbar Speicherorttypen.</span><span class="sxs-lookup"><span data-stu-id="818bb-p102">Within the dialog box, users can navigate the All Notebooks hierarchy to look for specific locations or search the OneNote tree structure by typing into the text box. Aspects of the dialog box that can be customized include the title, description, recent results list, check box text and state, tree depth, buttons, and selectable location types.</span></span>

<span data-ttu-id="818bb-p103">Sie können die schnelle ablegen Dialogfeldfunktionen über zwei OneNote 2013 Schnittstellen zugreifen. Die **IQuickFilingDialog** -Schnittstelle ermöglicht es Benutzern, instanziieren, einrichten, und führen das Dialogfeld. Die **IQuickFilingDialogCallback** -Schnittstelle wird aufgerufen, nachdem das Dialogfeld geschlossen wird. Das Dialogfeld in der OneNote-Prozess ausgeführt wird, sodass ein Mechanismus benötigt werden, um das Dialogfeld Thread ausgeführt weiter und dann die Auswahl des Benutzers als auch den Status des Dialogfelds erfasst werden, wenn er geschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="818bb-p103">You can access the Quick Filing dialog box functionality through two OneNote 2013 interfaces. The **IQuickFilingDialog** interface allows users to instantiate, set up, and run the dialog box. The **IQuickFilingDialogCallback** interface is called after the dialog box is closed. The dialog box is run in the OneNote process, so a mechanism is needed to keep the dialog box's thread running and then to capture the user's selection and the state of the dialog box when it is closed.</span></span> 
  
## <a name="iquickfilingdialog-interface"></a><span data-ttu-id="818bb-118">IQuickFilingDialog-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="818bb-118">IQuickFilingDialog interface</span></span>
<span data-ttu-id="818bb-119"><a name="odc_IQuickFilingDialog"> </a></span><span class="sxs-lookup"><span data-stu-id="818bb-119"></span></span>

<span data-ttu-id="818bb-p104">Diese Schnittstelle ermöglicht es dem Benutzer anpassen, und führen Sie das Dialogfeld. Der Benutzer kann ein Dialogfeld über die **Application** -Klasse instanziiert werden mithilfe der **Application.QuickFilingDialog** -Methode. Die Methode gibt eine Instanz des Dialogfelds zurück. Nachdem Sie die Eigenschaften des Dialogfelds festgelegt sind, wird die **IQuickFilingDialog.Run** -Methode das Dialogfeld ausgeführt. Diese Methode wird das Dialogfeld in einem neuen Thread ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="818bb-p104">This interface allows the user to customize and run the dialog box. The user can instantiate a dialog box through the **Application** class by using the **Application.QuickFilingDialog** method. The method returns an instance of the dialog box. Once the properties of the dialog box are set, the **IQuickFilingDialog.Run** method is used to run the dialog box. This method runs the dialog box on a new thread.</span></span> 
  
<span data-ttu-id="818bb-125">**Eigenschaften**</span><span class="sxs-lookup"><span data-stu-id="818bb-125">**Properties**</span></span>

|<span data-ttu-id="818bb-126">**Name**</span><span class="sxs-lookup"><span data-stu-id="818bb-126">**Name**</span></span>|<span data-ttu-id="818bb-127">**Typ**</span><span class="sxs-lookup"><span data-stu-id="818bb-127">**Type**</span></span>|<span data-ttu-id="818bb-128">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="818bb-128">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="818bb-129">**Title**</span><span class="sxs-lookup"><span data-stu-id="818bb-129">**Title**</span></span> <br/> |<span data-ttu-id="818bb-130">string</span><span class="sxs-lookup"><span data-stu-id="818bb-130">string</span></span>  <br/> |<span data-ttu-id="818bb-131">Dient zum Abrufen oder wird der Titeltext, der angezeigt wird in der Titelleiste des Fensters Feld Dialogfeld.</span><span class="sxs-lookup"><span data-stu-id="818bb-131">Gets or sets the title text that appears in the title bar of the dialog box window.</span></span>  <br/> |
|<span data-ttu-id="818bb-132">**Description**</span><span class="sxs-lookup"><span data-stu-id="818bb-132">**Description**</span></span> <br/> |<span data-ttu-id="818bb-133">string</span><span class="sxs-lookup"><span data-stu-id="818bb-133">string</span></span>  <br/> |<span data-ttu-id="818bb-p105">Dient zum Abrufen oder Festlegen der Textbeschreibung und was Sie wählen den Benutzer auffordern. Dieser Wert kann mehrere Zeilen Text sein.</span><span class="sxs-lookup"><span data-stu-id="818bb-p105">Gets or sets the text description to instruct the user about what to select. This value can be multiple-line text.</span></span>  <br/> |
|<span data-ttu-id="818bb-136">**CheckboxText**</span><span class="sxs-lookup"><span data-stu-id="818bb-136">**CheckboxText**</span></span> <br/> |<span data-ttu-id="818bb-137">string</span><span class="sxs-lookup"><span data-stu-id="818bb-137">string</span></span>  <br/> |<span data-ttu-id="818bb-p106">Ruft ab oder legt den Text, der das Kontrollkästchen bildet. Wenn dieser Wert auf eine nicht leere Zeichenfolge festgelegt ist, wird ein Kontrollkästchen im Dialogfeld angezeigt. Wenn der Wert auf eine leere Zeichenfolge ist, wird kein Kontrollkästchen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="818bb-p106">Gets or sets the text that follows the check box. If this value is set to a non-empty string, a check box appears in the dialog box. If the value is an empty string, no check box appears.</span></span>  <br/> |
|<span data-ttu-id="818bb-141">**CheckboxState**</span><span class="sxs-lookup"><span data-stu-id="818bb-141">**CheckboxState**</span></span> <br/> |<span data-ttu-id="818bb-142">bool</span><span class="sxs-lookup"><span data-stu-id="818bb-142">bool</span></span>  <br/> |<span data-ttu-id="818bb-p107">Dient zum Abrufen oder Festlegen des Status des Kontrollkästchens. Wenn der Wert auf **false**festgelegt ist, ist das Kontrollkästchen deaktiviert, wenn das Dialogfeld gestartet wird. Wenn der Wert auf **true**festgelegt ist, ist das Kontrollkästchen aktiviert, wenn das Dialogfeld gestartet wird solange **CheckboxText** eine nicht leere Zeichenfolge ist.  </span><span class="sxs-lookup"><span data-stu-id="818bb-p107">Gets or sets the state of the check box. If value is set to **false**, the check box is cleared when the dialog box is started. If the value is set to **true**, the check box is selected when the dialog box is started as long as **CheckboxText** is a non-empty string.  </span></span><br/> |
|<span data-ttu-id="818bb-146">**WindowHandle**</span><span class="sxs-lookup"><span data-stu-id="818bb-146">**WindowHandle**</span></span> <br/> |<span data-ttu-id="818bb-147">ulong</span><span class="sxs-lookup"><span data-stu-id="818bb-147">ulong</span></span>  <br/> |<span data-ttu-id="818bb-148">Ruft die ID Handle des Fensters Feld Dialogfeld Quick ablegen.</span><span class="sxs-lookup"><span data-stu-id="818bb-148">Gets the handle ID of the Quick Filing dialog box window.</span></span>  <br/> |
|<span data-ttu-id="818bb-149">**TreeDepth**</span><span class="sxs-lookup"><span data-stu-id="818bb-149">**TreeDepth**</span></span> <br/> |<span data-ttu-id="818bb-150">**HierarchyElement**</span><span class="sxs-lookup"><span data-stu-id="818bb-150">**HierarchyElement**</span></span> <br/> |<span data-ttu-id="818bb-p108">Ruft ab oder legt fest, wie tief die OneNote-Struktur im Abschnitt alle Notizbücher angezeigt werden soll. Standardmäßig ist die Struktur bis zu den Abschnitten angezeigt. Diese Eigenschaft wirkt sich nicht auf welche Typen von Elementen ausgewählt werden kann. </span><span class="sxs-lookup"><span data-stu-id="818bb-p108">Gets or sets how deep the OneNote tree should be displayed in the All Notebooks section. By default, the tree is displayed up to the sections. This property does not affect what type of elements can be selected.  </span></span><br/> <span data-ttu-id="818bb-p109">Wenn **TreeDepth** auf ein Element festgelegt ist der weiter unten in der OneNote-Hierarchie als von eine der Schaltflächen ausgewählt werden kann, wird die Tiefe angezeigte Struktur der niedrigste mögliche auswählbar Element. D. h., wenn Strukturtiefe festgelegt wird, dass nach unten zu Seiten angezeigt, aber das niedrigste auswählbare-Element ein Abschnitt ist, die Struktur nach unten zu Abschnitten angezeigt.  </span><span class="sxs-lookup"><span data-stu-id="818bb-p109">If **TreeDepth** is set to an element lower in the OneNote hierarchy than can be selected by any of the buttons, the displayed tree depth will be the lowest possible selectable element. That is, if tree depth is set to display down to pages, but the lowest selectable element is a section, the tree is displayed down to sections.  </span></span><br/> |
|<span data-ttu-id="818bb-156">**ParentWindowHandle**</span><span class="sxs-lookup"><span data-stu-id="818bb-156">**ParentWindowHandle**</span></span> <br/> |<span data-ttu-id="818bb-157">ulong</span><span class="sxs-lookup"><span data-stu-id="818bb-157">ulong</span></span>  <br/> |<span data-ttu-id="818bb-p110">Dient zum Abrufen oder Festlegen der Handle-ID des übergeordneten Fensters des Dialogfelds. Wenn diese Eigenschaft festgelegt ist, werden im Dialogfeld für die schnelle ablegen an die zugewiesene übergeordnetes Fenster modal, wenn das Dialogfeld wird geöffnet. D. h., werden Benutzer nicht auf das übergeordnete Fenster zugreifen, bis das Dialogfeld Quick ablegen geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="818bb-p110">Gets or sets the handle ID of the parent window of the dialog box. If this property is set, the Quick Filing dialog box will be modal to the assigned parent window when the dialog box opens. That is, a user will not be able to access the parent window until the Quick Filing dialog box is closed.</span></span>  <br/> |
|<span data-ttu-id="818bb-161">**Position**</span><span class="sxs-lookup"><span data-stu-id="818bb-161">**Position**</span></span> <br/> |<span data-ttu-id="818bb-162">tagPOINT</span><span class="sxs-lookup"><span data-stu-id="818bb-162">tagPOINT</span></span>  <br/> |<span data-ttu-id="818bb-p111">Dient zum Abrufen oder Festlegen der Position des Fensters in Bezug auf dem Bildschirm. Standardmäßig wird das Dialogfeld in der Mitte des übergeordneten Fensters oder auf dem Desktop angezeigt.</span><span class="sxs-lookup"><span data-stu-id="818bb-p111">Gets or sets the position of the window in relation to the screen. By default, the dialog box appears in the middle of the parent window or the desktop.</span></span>  <br/> |
|<span data-ttu-id="818bb-165">**SelectedItem**</span><span class="sxs-lookup"><span data-stu-id="818bb-165">**SelectedItem**</span></span> <br/> |<span data-ttu-id="818bb-166">string</span><span class="sxs-lookup"><span data-stu-id="818bb-166">string</span></span>  <br/> |<span data-ttu-id="818bb-p112">Ruft die Objekt-ID des OneNote-Speicherorts, die vom Benutzer ausgewählt werden, wenn das Dialogfeld geschlossen wird. Wenn der Benutzer auf die Schaltfläche **Abbrechen** klickt, wird das Objekt festgelegt auf Null.  </span><span class="sxs-lookup"><span data-stu-id="818bb-p112">Gets the object ID of the OneNote location selected by the user when the dialog box is closed. If the user clicks the **Cancel** button, the object is set to null.  </span></span><br/> |
|<span data-ttu-id="818bb-169">**PressedButton**</span><span class="sxs-lookup"><span data-stu-id="818bb-169">**PressedButton**</span></span> <br/> |<span data-ttu-id="818bb-170">ulong</span><span class="sxs-lookup"><span data-stu-id="818bb-170">ulong</span></span>  <br/> |<span data-ttu-id="818bb-p113">Ruft ab, welche Schaltfläche geklickt wurde, wenn das Dialogfeld geschlossen wurde. Wenn die Schaltfläche **Abbrechen** geklickt wurde, gibt diese Eigenschaft den Wert-1 zurück. Alle anderen Schaltflächen werden Werte für ganze Zahl im Bereich von 0, um 1 für jede Schaltfläche hinzugefügt, um das Dialogfeld erhöht zugewiesen. Der Integer-Wert, der die Standardschaltfläche **OK** ist 0.  </span><span class="sxs-lookup"><span data-stu-id="818bb-p113">Gets which button was clicked when the dialog box was closed. If the **Cancel** button was clicked, this property returns a value of -1. All other buttons are assigned integer values from 0, incremented by 1 for each button added to the dialog box. The integer value of the default **OK** button is 0.  </span></span><br/> |
   
### <a name="methods"></a><span data-ttu-id="818bb-175">Methoden</span><span class="sxs-lookup"><span data-stu-id="818bb-175">Methods</span></span>

<span data-ttu-id="818bb-176">**SetRecentResults**</span><span class="sxs-lookup"><span data-stu-id="818bb-176">**SetRecentResults**</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="818bb-177">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="818bb-177">**Description**</span></span> <br/> |<span data-ttu-id="818bb-p114">Legt fest, welche Ergebnisliste der zuletzt verwendeten im Dialogfeld Quick ablegen angezeigt wird, und gibt an, ob einige besondere Einreichung Speicherorten in der Liste enthalten. Benutzer können eine Ergebnisliste der zuletzt verwendeten aus der [RecentResultType](enumerations-onenote-developer-reference.md#odc_RecentResultType) -Enumeration auswählen. Benutzer können auch die folgenden Optionen zur Liste hinzufügen: aktuellen Abschnitt, die aktuelle Seite oder abgelegte Notizen. Wenn **RecentResultType.rrtNone** ausgewählt ist, wird keine Ergebnisliste der zuletzt verwendeten angezeigt.  </span><span class="sxs-lookup"><span data-stu-id="818bb-p114">Sets what recent result list will be displayed in the Quick Filing dialog box, and indicates whether to include some special filing locations in the list. Users can select a recent result list from the [RecentResultType](enumerations-onenote-developer-reference.md#odc_RecentResultType) enumeration. Users can also choose to add the following options to the list: Current Section, Current Page, or Unfiled Notes. If **RecentResultType.rrtNone** is selected, no recent result list is shown.  </span></span><br/> |
|<span data-ttu-id="818bb-182">**Syntax**</span><span class="sxs-lookup"><span data-stu-id="818bb-182">**Syntax**</span></span> <br/> | `HRESULT SetRecentResults (`<br/>`[in]RecentResultType recentResults,`<br/>`[in]VARIANT_BOOL fShowCurrentSection,`<br/>`[in]VARIANT_BOOL fShowCurrentPage,`<br/>`[in]VARIANT_BOOL fShowUnfiledNotes);` <br/> |
|<span data-ttu-id="818bb-183">**Parameter**</span><span class="sxs-lookup"><span data-stu-id="818bb-183">**Parameters**</span></span> <br/> | <span data-ttu-id="818bb-184">_recentResults_ &ndash; Ein Objekt vom Typ **RecentResultType** , das angibt, welche Liste der zuletzt geöffneten Ergebnisse angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="818bb-184">_recentResults_ &ndash; An object of type **RecentResultType** that indicates which recent result list, if any, should appear.</span></span> <span data-ttu-id="818bb-185">Wenn **rrtNone** ausgewählt ist, wird keine Ergebnisliste der zuletzt verwendeten im Dialogfeld angezeigt.</span><span class="sxs-lookup"><span data-stu-id="818bb-185">If **rrtNone** is selected, no recent result list appears in the dialog box.</span></span><br/><br/>  <span data-ttu-id="818bb-186">_fShowCurrentSection_ &ndash; Ein boolescher Wert, der angibt, ob der aktuelle Abschnitt in der Liste der zuletzt verwendeten Ergebnisse enthalten sein soll.</span><span class="sxs-lookup"><span data-stu-id="818bb-186">_fShowCurrentSection_ &ndash; A Boolean value that indicates whether the current section should be included in the recent result list.</span></span><br/><br/>  <span data-ttu-id="818bb-187">_fShowCurrentPage_ &ndash; Ein boolescher Wert, der angibt, ob die aktuelle Seite in der Liste der zuletzt verwendeten Ergebnisse enthalten sein soll.</span><span class="sxs-lookup"><span data-stu-id="818bb-187">_fShowCurrentPage_ &ndash; A Boolean value that indicates whether the current page should be included in the recent result list.</span></span><br/><br/>  <span data-ttu-id="818bb-188">_fShowUnfiledNotes_ &ndash; Ein boolescher Wert, der angibt, ob der Abschnitt nicht gegebene Notizen in der Liste der zuletzt verwendeten Ergebnisse enthalten sein soll.</span><span class="sxs-lookup"><span data-stu-id="818bb-188">_fShowUnfiledNotes_ &ndash; A Boolean value that indicates whether the Unfiled Notes section should be included in the recent result list.</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="818bb-p116">[!HINWEIS] Wenn Sie ein speziellen Einreichung Speicherort mithilfe einer der Schaltflächen im Dialogfeld aktiviert werden kann, wird es nicht in der Liste angezeigt. Wenn kein Element ausgewählt werden in der Ergebnisliste der zuletzt geöffneten gefunden wird, wird keine Ergebnisliste der zuletzt verwendeten angezeigt.</span><span class="sxs-lookup"><span data-stu-id="818bb-p116">If a special filing location cannot be selected by using any of the buttons in the dialog box, it is not shown in the list. If no selectable item in the recent results list is found, no recent result list is displayed.</span></span> 
  
<span data-ttu-id="818bb-191">Das folgende Beispiel verwendet die **SetRecentResults** -Methode des aktuellen Abschnitts, OneNote und aktuelle Seite in der Ergebnisliste der zuletzt geöffneten angezeigt.</span><span class="sxs-lookup"><span data-stu-id="818bb-191">The following example uses the **SetRecentResults** method to display the current section, current page, and the Unfiled Notes section in the recent result list.</span></span> 
  
```cs
        static void Main(string[] args)
        {
            Microsoft.Office.Interop.OneNote.Application app = 
                new Microsoft.Office.Interop.OneNote.Application();
            ... 
            // RECENT RESULTS
            qfDialog.SetRecentResults(RecentResultType.rrtFiling,
                /*Current Section*/ true,
                /*Current Page*/ true,
                /*Unfiled Notes*/ true);
            ...
        }

```

<span data-ttu-id="818bb-192">**AddButton**</span><span class="sxs-lookup"><span data-stu-id="818bb-192">**AddButton**</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="818bb-193">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="818bb-193">**Description**</span></span> <br/> |<span data-ttu-id="818bb-p117">Ermöglicht Benutzern das Hinzufügen und Schaltflächen im Dialogfeld anpassen. Benutzer können Geben Sie den Text auf die Schaltflächen und welche Elemente der OneNote-Hierarchie von jede Schaltfläche ausgewählt werden können.</span><span class="sxs-lookup"><span data-stu-id="818bb-p117">Allows users to add and customize buttons in the dialog box. Users can specify the text on the buttons and what elements of the OneNote hierarchy can be selected by each button.</span></span>  <br/> |
|<span data-ttu-id="818bb-196">**Syntax**</span><span class="sxs-lookup"><span data-stu-id="818bb-196">**Syntax**</span></span> <br/> | `HRESULT AddButton (`<br/>`[in]BSTR bstrText,`<br/>`[in]HierarchyElement allowedElements,`<br/>`[in]HierarchyElement allowedReadOnlyElements,`<br/>`[in]VARIANT_BOOL fDefault);` <br/> |
|<span data-ttu-id="818bb-197">**Parameter**</span><span class="sxs-lookup"><span data-stu-id="818bb-197">**Parameters**</span></span> <br/> | <span data-ttu-id="818bb-198">_bstrText_ &ndash; Eine Zeichenfolge, die den Text angibt, der auf der Schaltfläche angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="818bb-198">_bstrText_ &ndash; A string that specifies the text to appear on the button.</span></span> <span data-ttu-id="818bb-199">Um die Standardschaltfläche **OK** anzupassen, übergeben Sie einen null-Wert als **bstrText**.</span><span class="sxs-lookup"><span data-stu-id="818bb-199">To customize the default **OK** button, pass in a null value as **bstrText**.</span></span>  <br/><br/><span data-ttu-id="818bb-200">_allowedElements_ &ndash; Ein **hierarchyelement** , das angibt, welche nicht-schreibgeschützten OneNote-Hierarchieelemente ein Benutzer mithilfe der-Schaltfläche auswählen kann.</span><span class="sxs-lookup"><span data-stu-id="818bb-200">_allowedElements_ &ndash; A **HierarchyElement** that indicates what non-read-only OneNote hierarchy elements a user is allowed to select by using the button.</span></span> <span data-ttu-id="818bb-201">Für die Auswahl mehrere Elemente, sollte der Benutzer für alle Uint äquivalente **HierarchyElement** Typen als eine **HierarchyElement**zulässig Operators **OR** übergeben.</span><span class="sxs-lookup"><span data-stu-id="818bb-201">For selecting multiple items, the user should pass in the **OR** operator for all the uint equivalent values of the **HierarchyElement** types allowed as a **HierarchyElement**.</span></span><br/><br/>  <span data-ttu-id="818bb-202">_allowedReadOnlyElements_ &ndash; Ein **hierarchyelement** , das angibt, welche OneNote-schreibgeschützten Hierarchieelemente ein Benutzer mithilfe der-Schaltfläche auswählen kann.</span><span class="sxs-lookup"><span data-stu-id="818bb-202">_allowedReadOnlyElements_ &ndash; A **HierarchyElement** that indicates what OneNote read-only hierarchy elements a user is allowed to select by using the button.</span></span> <span data-ttu-id="818bb-203">Für die Auswahl mehrere Elemente, sollte der Benutzer nach allen Werten **Uint** -Entsprechungen **HierarchyElement** Typen als eine **HierarchyElement**zulässig Operators **OR** übergeben.</span><span class="sxs-lookup"><span data-stu-id="818bb-203">For selecting multiple items, the user should pass in the **OR** operator for all the **uint** equivalents values of the **HierarchyElement** types allowed as a **HierarchyElement**.</span></span><br/><br/>  <span data-ttu-id="818bb-204">_fDefault_ &ndash; Ein boolescher Wert, der angibt, ob diese Schaltfläche als Standardschaltfläche verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="818bb-204">_fDefault_ &ndash; A Boolean value that specifies whether this button should be the default button.</span></span> <span data-ttu-id="818bb-205">Wenn mehrere Schaltflächen als Standard festgelegt sind, wird die letzte angegebene Schaltfläche die Standardschaltfläche.</span><span class="sxs-lookup"><span data-stu-id="818bb-205">If multiple buttons are set as default, the last specified button becomes the default button.</span></span>  <br/> |
   
<span data-ttu-id="818bb-p122">Im folgenden Beispiel wird das Dialogfeld Quick ablegen drei Schaltflächen hinzugefügt. Das erste aus, die **alle**, kann von allen Elementen in der Hierarchiestruktur OneNote ausgewählt werden. Andere, **Notebooks** und **Seiten** anzeigen, können ausgewählt werden nur, wenn ihre entsprechenden Elemente, Notebooks und Seiten, ausgewählt sind.</span><span class="sxs-lookup"><span data-stu-id="818bb-p122">The following example adds three buttons to the Quick Filing dialog box. The first one, **All**, can be selected by all elements in the OneNote hierarchy tree. The others, **Notebooks** and **Pages**, can be selected only if their corresponding elements, Notebooks and Pages, are selected.</span></span>
  
```cs
        static void Main(string[] args)
        {
            Microsoft.Office.Interop.OneNote.Application app = 
                new Microsoft.Office.Interop.OneNote.Application();
            ... 
            
            // BUTTONS
            HierarchyElement heAll = (HierarchyElement) 
                ((uint)HierarchyElement.heNotebooks | 
                (uint)HierarchyElement.heSectionGroups | 
                (uint)HierarchyElement.heSections |  
                (uint)HierarchyElement.hePages);
            
            qfDialog.AddButton("All", heAll, heAll, true);
            qfDialog.AddButton("Notebooks", HierarchyElement.heNotebooks, 
                HierarchyElement.heNotebooks, false);
            qfDialog.AddButton("Pages", HierarchyElement.hePages, 
                HierarchyElement.hePages, false);
            ... 
        }

```

<span data-ttu-id="818bb-209">**Run**</span><span class="sxs-lookup"><span data-stu-id="818bb-209">**Run**</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="818bb-210">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="818bb-210">**Description**</span></span> <br/> |<span data-ttu-id="818bb-p123">Zeigt das Dialogfeld Quick ablegen, von einem neuen Thread an. Es erfordert einen Verweis auf die **IQuickFilingDialogCallback** -Schnittstelle, deren **OnDialogClosed** -Methode aufgerufen wird, sobald das Dialogfeld wird geschlossen.  </span><span class="sxs-lookup"><span data-stu-id="818bb-p123">Displays the Quick Filing dialog box from a new thread. It takes a reference to the **IQuickFilingDialogCallback** interface, whose **OnDialogClosed** method will be called once the dialog box closes.  </span></span><br/> |
|<span data-ttu-id="818bb-213">**Syntax**</span><span class="sxs-lookup"><span data-stu-id="818bb-213">**Syntax**</span></span> <br/> | `HRESULT Run (`<br/>`[in]IQuickFilingDialogCallback piCallback);` <br/> |
|<span data-ttu-id="818bb-214">**Parameter**</span><span class="sxs-lookup"><span data-stu-id="818bb-214">**Parameters**</span></span> <br/> | <span data-ttu-id="818bb-215">_piCallback_ &ndash; Ein Verweis auf die **IQuickFilingDialogCallback** -Schnittstelle, die instanziiert wird, sobald das Dialogfeld geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="818bb-215">_piCallback_ &ndash; A reference to the **IQuickFilingDialogCallback** interface that will be instantiated once the dialog box closes.</span></span>  <br/> |
   
<span data-ttu-id="818bb-216">Im folgenden Beispiel wird mithilfe die **Run** -Methode das Dialogfeld Quick Ablegen von einem neuen Thread an.</span><span class="sxs-lookup"><span data-stu-id="818bb-216">The following example uses the **Run** method to display the Quick Filing dialog box from a new thread.</span></span> 
  
```cs
    class OpenQuickFilingDialog
    {
            ... 
        static void Main(string[] args)
        {
            Microsoft.Office.Interop.OneNote.Application app = 
                new Microsoft.Office.Interop.OneNote.Application();
            ... 
            // Display Quick Filing UI
            qfDialog.Run(new Callback());
            ... 
        }
    }

```

<span data-ttu-id="818bb-217">**TreeCollapsedState**</span><span class="sxs-lookup"><span data-stu-id="818bb-217">**TreeCollapsedState**</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="818bb-218">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="818bb-218">**Description**</span></span> <br/> |<span data-ttu-id="818bb-219">Gibt an, ob die Hierarchiestruktur erweitert oder reduziert werden.</span><span class="sxs-lookup"><span data-stu-id="818bb-219">Indicates whether the hierarchy tree should be expanded or collapsed.</span></span>  <br/> |
|<span data-ttu-id="818bb-220">**Syntax**</span><span class="sxs-lookup"><span data-stu-id="818bb-220">**Syntax**</span></span> <br/> | `HRESULT TreeCollapsedState(`<br/>`[in] TreeCollapsedStateType tcs);` <br/> |
|<span data-ttu-id="818bb-221">**Parameter**</span><span class="sxs-lookup"><span data-stu-id="818bb-221">**Parameters**</span></span> <br/> | <span data-ttu-id="818bb-222">_tcs_ - gibt an, ob die Struktur erweitert oder reduziert ist.</span><span class="sxs-lookup"><span data-stu-id="818bb-222">_tcs_ - Specifies whether the tree is expanded or collapsed.</span></span>  <br/> |
   
<span data-ttu-id="818bb-223">**NotebookFilterOut**</span><span class="sxs-lookup"><span data-stu-id="818bb-223">**NotebookFilterOut**</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="818bb-224">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="818bb-224">**Description**</span></span> <br/> |<span data-ttu-id="818bb-225">Filtert die Liste der Notizbücher nach Typ dargestellt.</span><span class="sxs-lookup"><span data-stu-id="818bb-225">Filters the list of notebooks shown by type.</span></span>  <br/> |
|<span data-ttu-id="818bb-226">**Syntax**</span><span class="sxs-lookup"><span data-stu-id="818bb-226">**Syntax**</span></span> <br/> | `HRESULT NotebookFilterOut(`<br/>`[in] NotebookFilterOutType nfo);` <br/> |
|<span data-ttu-id="818bb-227">**Parameter**</span><span class="sxs-lookup"><span data-stu-id="818bb-227">**Parameters**</span></span> <br/> | <span data-ttu-id="818bb-228">_nfo_ - gibt den Satz von Notebooks, die aus der Liste gefiltert werden sollen</span><span class="sxs-lookup"><span data-stu-id="818bb-228">_nfo_ - Specifies the set of notebooks that are to be filtered out of the list</span></span>  <br/> |
   
<span data-ttu-id="818bb-229">**ShowCreateNewNotebook**</span><span class="sxs-lookup"><span data-stu-id="818bb-229">**ShowCreateNewNotebook**</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="818bb-230">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="818bb-230">**Description**</span></span> <br/> |<span data-ttu-id="818bb-231">Die Option neue Notizbuch erstellen in das Dialogfeld angezeigt.</span><span class="sxs-lookup"><span data-stu-id="818bb-231">Displays the create new notebook option in the dialog.</span></span>  <br/> |
|<span data-ttu-id="818bb-232">**Syntax**</span><span class="sxs-lookup"><span data-stu-id="818bb-232">**Syntax**</span></span> <br/> | `HRESULT ShowCreateNewNotebook ();` <br/> |
|<span data-ttu-id="818bb-233">**Parameter**</span><span class="sxs-lookup"><span data-stu-id="818bb-233">**Parameters**</span></span> <br/> |<span data-ttu-id="818bb-234">Keines</span><span class="sxs-lookup"><span data-stu-id="818bb-234">None</span></span>  <br/> |
   
<span data-ttu-id="818bb-235">**AddInitialEditor**</span><span class="sxs-lookup"><span data-stu-id="818bb-235">**AddInitialEditor**</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="818bb-236">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="818bb-236">**Description**</span></span> <br/> |<span data-ttu-id="818bb-237">Fügt einen Benutzer als ersten-Editor in ein Notizbuch in das Dialogfeld Quick ablegen.</span><span class="sxs-lookup"><span data-stu-id="818bb-237">Adds a user as an initial editor to a notebook in the Quick Filing dialog box.</span></span>  <br/> |
|<span data-ttu-id="818bb-238">**Syntax**</span><span class="sxs-lookup"><span data-stu-id="818bb-238">**Syntax**</span></span> <br/> | `HRESULT AddInitialEditor (BSTR initialEditor);` <br/> |
|<span data-ttu-id="818bb-239">**Parameter**</span><span class="sxs-lookup"><span data-stu-id="818bb-239">**Parameters**</span></span> <br/> | <span data-ttu-id="818bb-p124">_initialEditor_ - die e-Mail-Adresse des Benutzers, die Sie als Editor in das Notizbuch hinzufügen möchten. Wenn das Notizbuch über das Dialogfeld für schnelle Ablage erstellt wird, wird es automatisch für alle ursprünglichen Editoren freigegeben.  </span><span class="sxs-lookup"><span data-stu-id="818bb-p124">_initialEditor_ - The email address of the user you wish to add as an editor to the notebook. When the notebook is created via the Quick Filing dialog box, it is automatically shared with all Initial Editors.  </span></span><br/> |
   
<span data-ttu-id="818bb-242">**ClearInitialEditors**</span><span class="sxs-lookup"><span data-stu-id="818bb-242">**ClearInitialEditors**</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="818bb-243">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="818bb-243">**Description**</span></span> <br/> |<span data-ttu-id="818bb-244">Entfernt alle ursprüngliche Editoren aus dem Dialogfeld Quick ablegen.</span><span class="sxs-lookup"><span data-stu-id="818bb-244">Removes all initial editors from the Quick Filing dialog box.</span></span>  <br/> |
|<span data-ttu-id="818bb-245">**Syntax**</span><span class="sxs-lookup"><span data-stu-id="818bb-245">**Syntax**</span></span> <br/> | `HRESULT ClearInitialEditors ();` <br/> |
|<span data-ttu-id="818bb-246">**Parameter**</span><span class="sxs-lookup"><span data-stu-id="818bb-246">**Parameters**</span></span> <br/> |<span data-ttu-id="818bb-247">Keine</span><span class="sxs-lookup"><span data-stu-id="818bb-247">None</span></span>  <br/> |
   
<span data-ttu-id="818bb-248">**ShowSharingHyperlink**</span><span class="sxs-lookup"><span data-stu-id="818bb-248">**ShowSharingHyperlink**</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="818bb-249">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="818bb-249">**Description**</span></span> <br/> |<span data-ttu-id="818bb-250">Zeigt den Hyperlink Hilfethema Freigabe im Dialogfeld Quick ablegen.</span><span class="sxs-lookup"><span data-stu-id="818bb-250">Displays the Sharing Help Topic Hyperlink in the Quick Filing dialog box.</span></span>  <br/> |
|<span data-ttu-id="818bb-251">**Syntax**</span><span class="sxs-lookup"><span data-stu-id="818bb-251">**Syntax**</span></span> <br/> | `HRESULT ShowSharingHyperlink();` <br/> |
|<span data-ttu-id="818bb-252">**Parameter**</span><span class="sxs-lookup"><span data-stu-id="818bb-252">**Parameters**</span></span> <br/> |<span data-ttu-id="818bb-253">Keine</span><span class="sxs-lookup"><span data-stu-id="818bb-253">None</span></span>  <br/> |
   
## <a name="iquickfilingdialogcallback-interface"></a><span data-ttu-id="818bb-254">IQuickFilingDialogCallback-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="818bb-254">IQuickFilingDialogCallback interface</span></span>
<span data-ttu-id="818bb-255"><a name="odc_IQuickFilingDialog"> </a></span><span class="sxs-lookup"><span data-stu-id="818bb-255"></span></span>

<span data-ttu-id="818bb-p125">Diese Schnittstelle ermöglicht es dem Benutzer auf die Eigenschaften des Dialogfelds zugreifen, nachdem das Dialogfeld wird geschlossen. Nachdem das Dialogfeld wird geschlossen, ruft OneNote 2013 die **IQuickFilingDialogCallback.OnDialogClose** -Methode in dieser Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="818bb-p125">This interface allows the user to access the dialog box properties after the dialog box closes. Once the dialog box closes, OneNote 2013 calls the **IQuickFilingDialogCallback.OnDialogClose** method in this interface.</span></span> 
  
<span data-ttu-id="818bb-258">Eine Klasse, die diese Schnittstelle erbt muss definiert werden.</span><span class="sxs-lookup"><span data-stu-id="818bb-258">A class that inherits this interface has to be defined.</span></span>
  
### <a name="methods"></a><span data-ttu-id="818bb-259">Methoden</span><span class="sxs-lookup"><span data-stu-id="818bb-259">Methods</span></span>

<span data-ttu-id="818bb-260">Im folgende Abschnitt werden die Schnittstellen im zuvor zugeordneten Methoden beschrieben.</span><span class="sxs-lookup"><span data-stu-id="818bb-260">The following section describes the methods associated with the interfaces detailed previously.</span></span>
  
<span data-ttu-id="818bb-261">**OnDialogClosed**</span><span class="sxs-lookup"><span data-stu-id="818bb-261">**OnDialogClosed**</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="818bb-262">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="818bb-262">**Description**</span></span> <br/> |<span data-ttu-id="818bb-p126">Ermöglicht Benutzern das Hinzufügen von Funktionen zum Erfassen und verwenden Sie die Auswahl des Benutzers aus dem Dialogfeld. Diese Methode wird aufgerufen, nachdem das Dialogfeld Quick ablegen geschlossen wurde. Diese Methode ist eine Funktion, die **IQuickFilingDialogCallback** Schnittstellen definieren.  </span><span class="sxs-lookup"><span data-stu-id="818bb-p126">Enables users to add functionality to capture and use the user selection from the dialog box. This method is called after the Quick Filing dialog box is closed. This method is a function that **IQuickFilingDialogCallback** interfaces have to define.  </span></span><br/> |
|<span data-ttu-id="818bb-266">**Syntax**</span><span class="sxs-lookup"><span data-stu-id="818bb-266">**Syntax**</span></span> <br/> | `HRESULT OnDialogClosed (`<br/>`[in]IQuickFilingDialog dialog);` <br/> |
|<span data-ttu-id="818bb-267">**Parameter**</span><span class="sxs-lookup"><span data-stu-id="818bb-267">**Parameters**</span></span> <br/> | <span data-ttu-id="818bb-268">_Dialogfeld_ &ndash; Das **IQuickFilingDialog** -Objekt, das die **OnDialogClose** -Methode aufgerufen hat.</span><span class="sxs-lookup"><span data-stu-id="818bb-268">_dialog_ &ndash; The **IQuickFilingDialog** object that called the **OnDialogClose** method.</span></span>  <br/> |
   
<span data-ttu-id="818bb-p127">Das folgende Beispiel ist ein Beispiel **IQuickFilingDialogCallback** -Schnittstelle. Die **OnDialogClose** -Methode wird die Auswahl des Benutzers aus dem Dialogfeld Quick Ablegen in der Konsole gedruckt.</span><span class="sxs-lookup"><span data-stu-id="818bb-p127">The following example is a sample **IQuickFilingDialogCallback** interface. The **OnDialogClose** method prints the user's selection from the Quick Filing dialog box to the console.</span></span> 
  
```cs
    class Callback : IQuickFilingDialogCallback
    {
        public Callback(){}
        public void OnDialogClosed(IQuickFilingDialog qfDialog)
        {
            Console.WriteLine(qfDialog.SelectedItem);
            Console.WriteLine(qfDialog.PressedButton);
            Console.WriteLine(qfDialog.CheckboxState);
        }
    }

```

## <a name="example"></a><span data-ttu-id="818bb-271">Beispiel</span><span class="sxs-lookup"><span data-stu-id="818bb-271">Example</span></span>
<span data-ttu-id="818bb-272"><a name="odc_IQuickFilingDialog"> </a></span><span class="sxs-lookup"><span data-stu-id="818bb-272"></span></span>

<span data-ttu-id="818bb-p128">Im folgenden Codebeispiel wird ein Dialogfeld Quick ablegen, die eine angepasste Titel, Beschreibung, letzte Ergebnisliste, Strukturtiefe, das Kontrollkästchen und Schaltflächen hat geöffnet. Des Benutzers ausgewähltes Element, gedrückt, und das Kontrollkästchen Statusdienst in einem Konsolenfenster angezeigt werden, wenn das Dialogfeld geschlossen wird. Um die Seitenschaltfläche aktiviert angezeigt wird, verfügt der Benutzer zum Suchen nach einer Seite, und wählen Sie ihn, da die Strukturtiefe nach unten zu Abschnitten festgelegt ist. Das Dialogfeld ist kein untergeordnetes Element des Fensters.</span><span class="sxs-lookup"><span data-stu-id="818bb-p128">The following code example opens a Quick Filing dialog box that has a customized title, description, recent result list, tree depth, check box, and buttons. The user's selected item, pressed button, and check-box state will be displayed in a console window when the dialog box is closed. To see the page button enabled, the user will have to search for a page and select it, because the tree depth is set down to sections. The dialog box is not a child of any window.</span></span>
  
```cs
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading;
using Microsoft.Office.Interop.OneNote;
namespace SampleQFD
{
    class OpenQuickFilingDialog
    {
        private static EventWaitHandle wh = new AutoResetEvent(false);
        private static IQuickFilingDialog qfDialog;
        private static String strTitle = "Sample Title";
        private static String strDescription = "Sample Description";
        private static String strCheckboxText = "Sample Checkbox";
        static void Main(string[] args)
        {
            Microsoft.Office.Interop.OneNote.Application app = 
                new Microsoft.Office.Interop.OneNote.Application();
            // Instantiate Quick Filing UI
            qfDialog = app.QuickFiling();
            #region//SET API PARAMETERS
            // TITLE
            qfDialog.Title = strTitle;
            // DESCRIPTION
            qfDialog.Description = strDescription;
            // RECENT RESULTS
            qfDialog.SetRecentResults(RecentResultType.rrtFiling,
                /*Current Section*/ true,
                /*Current Page*/ true,
                /*Unfiled Notes*/ true);
            // TREE DEPTH
            qfDialog.TreeDepth = HierarchyElement.heSections;
            // CHECKBOX
            qfDialog.CheckboxText = strCheckboxText;
            qfDialog.CheckboxState = false;
            // BUTTONS
            HierarchyElement heAll = (HierarchyElement) 
                ((uint)HierarchyElement.heNotebooks | 
                (uint)HierarchyElement.heSectionGroups | 
                (uint)HierarchyElement.heSections |  
                (uint)HierarchyElement.hePages);
            
            qfDialog.AddButton("All", heAll, heAll, true);
            qfDialog.AddButton("Notebooks", HierarchyElement.heNotebooks, 
                HierarchyElement.heNotebooks, false);
            qfDialog.AddButton("Pages", HierarchyElement.hePages, 
                HierarchyElement.hePages, false);
            // PARENTWINDOW
            #endregion
            // Display Quick Filing UI
            qfDialog.Run(new Callback());
            // Clean up and Wait so console window does not close
            qfDialog = null;
            wh.WaitOne();
        }
    }
    class Callback : IQuickFilingDialogCallback
    {
        public Callback(){}
        public void OnDialogClosed(IQuickFilingDialog qfDialog)
        {
            Console.WriteLine(qfDialog.SelectedItem);
            Console.WriteLine(qfDialog.PressedButton);
            Console.WriteLine(qfDialog.CheckboxState);
        }
    }
}

```

## <a name="see-also"></a><span data-ttu-id="818bb-277">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="818bb-277">See also</span></span>

- [<span data-ttu-id="818bb-278">OneNote-Entwicklerreferenz</span><span class="sxs-lookup"><span data-stu-id="818bb-278">OneNote developer reference</span></span>](onenote-developer-reference.md)

