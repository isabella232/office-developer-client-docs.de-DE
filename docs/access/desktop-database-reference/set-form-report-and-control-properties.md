---
title: Festlegen von Formular-, Berichts- und Steuerelementeigenschaften
TOCTitle: Set form, report, and control properties
description: Jedes Formular, jeder Bericht, jeder Bereich und jedes Steuerelement verfügt über Eigenschafteneinstellungen, mit denen Sie das Aussehen und die Funktionsweise eines Elements in Access 2013 ändern können.
ms:assetid: 03349d86-f107-9e49-89df-62f55f3a0735
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844789(v=office.15)
ms:contentKeyID: 48542977
ms.date: 10/16/2018
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm12286
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: bacbdc100d147be8bf4327a5a775b199c79347bb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308736"
---
# <a name="set-form-report-and-control-properties"></a><span data-ttu-id="242e5-103">Festlegen von Formular-, Berichts- und Steuerelementeigenschaften</span><span class="sxs-lookup"><span data-stu-id="242e5-103">Set form, report, and control properties</span></span>

<span data-ttu-id="242e5-104">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="242e5-104">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="242e5-p101">Jedes Formular, jeder Bericht, jeder Bereich und jedes Steuerelement verfügt über Eigenschafteneinstellungen, mit denen Sie das Aussehen und die Funktionsweise eines Elements ändern können. Sie können die Eigenschaften im Eigenschaftenfenster, in einem Makro oder in Visual Basic anzeigen und ändern.</span><span class="sxs-lookup"><span data-stu-id="242e5-p101">Each form, report, section, and control has property settings that you can change to alter the look or behavior of that particular item. You view and change properties by using the property sheet, macro, or Visual Basic.</span></span>

## <a name="set-properties"></a><span data-ttu-id="242e5-107">Festlegen von Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="242e5-107">Set properties</span></span>

1. <span data-ttu-id="242e5-p102">Wählen Sie in der Formularentwurfsansicht oder Berichtsentwurfsansicht das Steuerelement, den Bereich, das Formular oder den Bericht aus, für das bzw. den Sie die Eigenschaft einstellen möchten. Sie haben folgende Auswahlmöglichkeiten:</span><span class="sxs-lookup"><span data-stu-id="242e5-p102">In form Design view or report Design view, select the control, section, form, or report for which you want to set the property. You can select:</span></span>
    
   - <span data-ttu-id="242e5-110">Ein oder mehrere Steuerelemente.</span><span class="sxs-lookup"><span data-stu-id="242e5-110">One or more controls.</span></span> <span data-ttu-id="242e5-111">Wenn Sie mehrere Steuerelemente auswählen möchten, klicken Sie bei gedrückter UMSCHALTTASTE auf die gewünschten Steuerelemente, oder ziehen Sie den Mauszeiger über die gewünschten Steuerelemente.</span><span class="sxs-lookup"><span data-stu-id="242e5-111">To select multiple controls, hold down the SHIFT key and click the controls, or drag the mouse pointer over the controls you wish to select.</span></span> <span data-ttu-id="242e5-112">Wenn Sie mehrere Steuerelemente auswählen, zeigt das Eigenschaftenfenster nur die Eigenschaften an, die alle markierten Steuerelemente gemeinsam besitzen.</span><span class="sxs-lookup"><span data-stu-id="242e5-112">If you select multiple controls, the property sheet will display only those properties that the selected controls have in common.</span></span>
    
   - <span data-ttu-id="242e5-113">Einen Bereich.</span><span class="sxs-lookup"><span data-stu-id="242e5-113">One section.</span></span> <span data-ttu-id="242e5-114">Klicken Sie auf den Bereichsmarkierer des gewünschten Bereichs.</span><span class="sxs-lookup"><span data-stu-id="242e5-114">Click the section selector of the section you wish to select.</span></span>
    
   - <span data-ttu-id="242e5-115">Das gesamte Formular oder den gesamten Bericht.</span><span class="sxs-lookup"><span data-stu-id="242e5-115">The form or report is hidden.</span></span> <span data-ttu-id="242e5-116">Klicken Sie auf den Formularmarkierer oder Berichtsmarkierer in der oberen linken Ecke des Formulars bzw. Berichts.</span><span class="sxs-lookup"><span data-stu-id="242e5-116">The entire form or report. Click the form selector or report selector in the upper-left corner of the form or report.</span></span>

2. <span data-ttu-id="242e5-117">Zeigen Sie das Eigenschaftenfenster an, indem Sie zuerst mit der rechten Maustaste auf das Objekt oder den Bereich und dann im Kontextmenü auf **Eigenschaften** klicken, oder indem Sie auf der Symbolleiste auf **Eigenschaften** klicken.</span><span class="sxs-lookup"><span data-stu-id="242e5-117">Display the property sheet by right-clicking the object or section and then clicking **Properties** on the shortcut menu, or by clicking **Properties** on the toolbar.</span></span>

3. <span data-ttu-id="242e5-118">Klicken Sie auf die Eigenschaft, deren Wert Sie festlegen möchten, und führen Sie dann einen der folgenden Schritte durch:</span><span class="sxs-lookup"><span data-stu-id="242e5-118">Click the property for which you want to set the value, and then do one of the following:</span></span>
    
   - <span data-ttu-id="242e5-119">Geben Sie im Eigenschaftenfeld die entsprechende Einstellung oder den entsprechenden Ausdruck an.</span><span class="sxs-lookup"><span data-stu-id="242e5-119">In the property box, type the appropriate setting or expression.</span></span>
    
   - <span data-ttu-id="242e5-120">Wenn das Einstellungsfeld der Eigenschaft einen Pfeil enthält, klicken Sie auf den Pfeil, und klicken Sie dann in der Liste auf einen Wert.</span><span class="sxs-lookup"><span data-stu-id="242e5-120">If the property box contains an arrow, click the arrow and then click a value in the list.</span></span>
    
   - <span data-ttu-id="242e5-121">Wenn eine **Build**-Schaltfläche rechts neben dem Eigenschaftenfeld angezeigt wird, wählen Sie diese aus, um einen Generator oder ein Dialogfeld anzuzeigen, in dem Sie eine Auswahl von Generatoren finden.</span><span class="sxs-lookup"><span data-stu-id="242e5-121">If a **Build** button appears to the right of the property box, click it to display a builder or to display a dialog box giving you a choice of builders.</span></span> <span data-ttu-id="242e5-122">Sie können z. B. den Code-Generator, den Makro-Generator oder den Abfrage-Generator verwenden, um einige Eigenschaften festzulegen.</span><span class="sxs-lookup"><span data-stu-id="242e5-122">For example, you can use the Code Builder, Macro Builder, or Query Builder to set some properties.</span></span>

## <a name="tips"></a><span data-ttu-id="242e5-123">Tipps </span><span class="sxs-lookup"><span data-stu-id="242e5-123">Tips</span></span>

- <span data-ttu-id="242e5-124">Microsoft Access bietet ein **Zoom**-Feld, in dem Sie Ausdrücke oder andere Eigenschafteneinstellungen eingeben oder anzeigen können.</span><span class="sxs-lookup"><span data-stu-id="242e5-124">Microsoft Access provides a **Zoom** box for typing and viewing expressions or other long property settings.</span></span> <span data-ttu-id="242e5-125">Um das **Zoom**-Feld anzuzeigen, klicken Sie im Eigenschaftenfenster auf das Eigenschaftenfeld.</span><span class="sxs-lookup"><span data-stu-id="242e5-125">To display the **Zoom** box, click a property box in the property sheet.</span></span> <span data-ttu-id="242e5-126">Drücken Sie UMSCHALT+F2, oder klicken Sie zuerst mit der rechten Maustaste, und klicken Sie dann im Kontextmenü auf **Zoom**.</span><span class="sxs-lookup"><span data-stu-id="242e5-126">Then press SHIFT+F2, or right-click and then click **Zoom** on the shortcut menu.</span></span>

- <span data-ttu-id="242e5-127">Sie können die Eigenschaft **Steuerelementinhalt** für einige Steuerelemente einstellen, indem Sie die Eigenschafteneinstellung im Steuerelement selbst vornehmen.</span><span class="sxs-lookup"><span data-stu-id="242e5-127">You can set the **ControlSource** property for some controls by typing the property setting in the control itself.</span></span>

- <span data-ttu-id="242e5-128">Durch Ändern der Standardeigenschafteneinstellungen für einen Steuerelementtyp erreichen Sie, dass später von Ihnen erstellte Steuerelemente über die neuen Standardeinstellungen verfügen.</span><span class="sxs-lookup"><span data-stu-id="242e5-128">You can change the default property settings for a type of control so that future controls you create will have the new default settings.</span></span>

- <span data-ttu-id="242e5-129">Die Eigenschafteneinstellungen eines gebundenen Steuerelements stimmen nicht immer mit den entsprechenden Einstellungen im Feld der zugrunde liegenden Tabelle oder Abfrage überein, an die das Steuerelement gebunden ist.</span><span class="sxs-lookup"><span data-stu-id="242e5-129">The property settings of a bound control might not match the corresponding settings in the field in the underlying table or query to which the control is bound.</span></span> <span data-ttu-id="242e5-130">In diesem Fall setzen die Einstellungen des Formulars oder Berichts in der Regel die Einstellungen der Tabelle oder Abfrage außer Kraft.</span><span class="sxs-lookup"><span data-stu-id="242e5-130">If the settings are different, the form or report settings typically override those in the table or query.</span></span>

