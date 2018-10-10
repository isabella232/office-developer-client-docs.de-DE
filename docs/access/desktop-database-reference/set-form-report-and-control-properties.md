---
title: Einstellen von Formular-, Berichts- und Steuerelementeigenschaften
TOCTitle: Set form, report, and control properties
ms:assetid: 03349d86-f107-9e49-89df-62f55f3a0735
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844789(v=office.15)
ms:contentKeyID: 48542977
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm12286
f1_categories:
- Office.Version=v15
ms.openlocfilehash: f839ab2e2c6dfab32c49248f1be1878bf289eb6b
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25473825"
---
# <a name="set-form-report-and-control-properties"></a><span data-ttu-id="866fa-102">Einstellen von Formular-, Berichts- und Steuerelementeigenschaften</span><span class="sxs-lookup"><span data-stu-id="866fa-102">Set form, report, and control properties</span></span>

<span data-ttu-id="866fa-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="866fa-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="866fa-p101">Jedes Formular, jeder Bericht, jeder Bereich und jedes Steuerelement verfügt über Eigenschafteneinstellungen, mit denen Sie das Aussehen und die Funktionsweise eines Elements ändern können. Sie können die Eigenschaften im Eigenschaftenfenster, in einem Makro oder in Visual Basic anzeigen und ändern.</span><span class="sxs-lookup"><span data-stu-id="866fa-p101">Each form, report, section, and control has property settings that you can change to alter the look or behavior of that particular item. You view and change properties by using the property sheet, macro, or Visual Basic.</span></span>

## <a name="set-properties"></a><span data-ttu-id="866fa-106">Eigenschaften festlegen</span><span class="sxs-lookup"><span data-stu-id="866fa-106">Set properties</span></span>

1. <span data-ttu-id="866fa-p102">Wählen Sie in der Formularentwurfsansicht oder Berichtsentwurfsansicht das Steuerelement, den Bereich, das Formular oder den Bericht aus, für das bzw. den Sie die Eigenschaft einstellen möchten. Sie haben folgende Auswahlmöglichkeiten:</span><span class="sxs-lookup"><span data-stu-id="866fa-p102">In form Design view or report Design view, select the control, section, form, or report for which you want to set the property. You can select:</span></span>
    
   - <span data-ttu-id="866fa-p103">Steuerelemente. Wenn Sie mehrere Steuerelemente auswählen möchten, klicken Sie bei gedrückter UMSCHALTTASTE auf die gewünschten Steuerelemente, oder ziehen Sie den Mauszeiger über die gewünschten Steuerelemente. Wenn Sie mehrere Steuerelemente auswählen, zeigt das Eigenschaftenfenster nur die Eigenschaften an, die alle markierten Steuerelemente gemeinsam besitzen.</span><span class="sxs-lookup"><span data-stu-id="866fa-p103">One or more controls. To select multiple controls, hold down the SHIFT key and click the controls, or drag the mouse pointer over the controls you wish to select. If you select multiple controls, the property sheet will display only those properties that the selected controls have in common.</span></span>
    
   - <span data-ttu-id="866fa-p104">Einen Bereich. Klicken Sie auf den Bereichsmarkierer des gewünschten Bereichs.</span><span class="sxs-lookup"><span data-stu-id="866fa-p104">One section. Click the section selector of the section you wish to select.</span></span>
    
   - <span data-ttu-id="866fa-p105">Das gesamte Formular oder den gesamten Bericht. Klicken Sie auf den Formularmarkierer oder Berichtsmarkierer in der oberen linken Ecke des Formulars bzw. Berichts.</span><span class="sxs-lookup"><span data-stu-id="866fa-p105">The entire form or report. Click the form selector or report selector in the upper-left corner of the form or report.</span></span>

2. <span data-ttu-id="866fa-116">Zeigen Sie das Eigenschaftenfenster an, indem Sie zuerst mit der rechten Maustaste auf das Objekt oder den Bereich und dann im Kontextmenü auf **Eigenschaften** klicken, oder indem Sie auf der Symbolleiste auf **Eigenschaften** klicken.</span><span class="sxs-lookup"><span data-stu-id="866fa-116">Display the property sheet by right-clicking the object or section and then clicking **Properties** on the shortcut menu, or by clicking **Properties** on the toolbar.</span></span>

3. <span data-ttu-id="866fa-117">Klicken Sie auf die Eigenschaft, deren Wert Sie einstellen möchten, und führen Sie dann einen der folgenden Schritte durch:</span><span class="sxs-lookup"><span data-stu-id="866fa-117">Click the property for which you want to set the value, and then do one of the following:</span></span>
    
   - <span data-ttu-id="866fa-118">Geben Sie im Einstellungsfeld der Eigenschaft die gewünschte Einstellung oder einen geeigneten Ausdruck ein.</span><span class="sxs-lookup"><span data-stu-id="866fa-118">In the property box, type the appropriate setting or expression.</span></span>
    
   - <span data-ttu-id="866fa-119">Wenn das Einstellungsfeld der Eigenschaft einen Pfeil enthält, klicken Sie auf den Pfeil, und klicken Sie dann in der Liste auf einen Wert.</span><span class="sxs-lookup"><span data-stu-id="866fa-119">If the property box contains an arrow, click the arrow and then click a value in the list.</span></span>
    
   - <span data-ttu-id="866fa-120">Wenn eine **Generator** -Schaltfläche rechts neben dem Eigenschaftenfeld angezeigt wird, klicken Sie auf einen Generator anzuzeigen oder Anzeigen eines Dialogfelds bietet Ihnen eine Auswahl von Generatoren.</span><span class="sxs-lookup"><span data-stu-id="866fa-120">If a **Build** button appears to the right of the property box, click it to display a builder or to display a dialog box giving you a choice of builders.</span></span> <span data-ttu-id="866fa-121">Beispielsweise können Sie die Code-Generators, Makro-Generator oder Abfrage-Generator verwenden, um bestimmte Eigenschaften festzulegen.</span><span class="sxs-lookup"><span data-stu-id="866fa-121">For example, you can use the Code Builder, Macro Builder, or Query Builder to set some properties.</span></span>

## <a name="tips"></a><span data-ttu-id="866fa-122">Tipps</span><span class="sxs-lookup"><span data-stu-id="866fa-122">Tips</span></span>

- <span data-ttu-id="866fa-p107">Microsoft Access stellt ein **Zoom** -Feld für die Eingabe und die Anzeige von Ausdrücken oder anderen langen Eigenschafteneinstellungen bereit. Um das **Zoom** -Feld anzuzeigen, klicken Sie im Eigenschaftenfenster auf das Eigenschaftenfeld. Drücken Sie dann UMSCHALT+F2, oder klicken Sie zuerst mit der rechten Maustaste, und klicken Sie dann im Kontextmenü auf **Zoom**.</span><span class="sxs-lookup"><span data-stu-id="866fa-p107">Microsoft Access provides a **Zoom** box for typing and viewing expressions or other long property settings. To display the **Zoom** box, click a property box in the property sheet. Then press SHIFT+F2, or right-click and then click **Zoom** on the shortcut menu.</span></span>

- <span data-ttu-id="866fa-126">Sie können die Eigenschaft **Steuerelementinhalt** für einige Steuerelemente einstellen, indem Sie die Eigenschafteneinstellung im Steuerelement selbst vornehmen.</span><span class="sxs-lookup"><span data-stu-id="866fa-126">You can set the **ControlSource** property for some controls by typing the property setting in the control itself.</span></span>

- <span data-ttu-id="866fa-127">Durch Ändern der Standardeigenschafteneinstellungen für einen Steuerelementtyp erreichen Sie, dass später von Ihnen erstellte Steuerelemente über die neuen Standardeinstellungen verfügen.</span><span class="sxs-lookup"><span data-stu-id="866fa-127">You can change the default property settings for a type of control so that future controls you create will have the new default settings.</span></span>

- <span data-ttu-id="866fa-p108">Die Eigenschafteneinstellungen eines gebundenen Steuerelements stimmen nicht immer mit den entsprechenden Einstellungen im Feld der zugrunde liegenden Tabelle oder Abfrage überein, an die das Steuerelement gebunden ist. In diesem Fall setzen die Einstellungen des Formulars oder Berichts in der Regel die Einstellungen der Tabelle oder Abfrage außer Kraft. Weitere Informationen über die Vererbung von Eigenschaften finden Sie in den Erklärungen zur Beziehung zwischen Steuerelementeigenschaften und Eigenschaften in den zugrunde liegenden Feldern.</span><span class="sxs-lookup"><span data-stu-id="866fa-p108">The property settings of a bound control might not match the corresponding settings in the field in the underlying table or query to which the control is bound. If the settings are different, the form or report settings typically override those in the table or query. For more information about how properties are inherited, see How control properties relate to properties in their underlying fields.</span></span>

