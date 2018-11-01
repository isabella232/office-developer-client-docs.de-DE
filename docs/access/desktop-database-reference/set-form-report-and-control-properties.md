---
title: Einstellen von Formular-, Berichts- und Steuerelementeigenschaften
TOCTitle: Set form, report, and control properties
description: Jedes Formular, Bericht, Abschnitt und Steuerelement verfügt über die Einstellungen, die Sie bearbeiten können, um das Aussehen und das Verhalten des betreffenden Elements auf bestimmten in Access 2013 ändern.
ms:assetid: 03349d86-f107-9e49-89df-62f55f3a0735
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844789(v=office.15)
ms:contentKeyID: 48542977
ms.date: 10/16/2018
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm12286
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 2ffb02f78bbf9d9f4c5d5b07c1ee08e3f19453b7
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25874605"
---
# <a name="set-form-report-and-control-properties"></a><span data-ttu-id="108c6-103">Einstellen von Formular-, Berichts- und Steuerelementeigenschaften</span><span class="sxs-lookup"><span data-stu-id="108c6-103">Set form, report, and control properties</span></span>

<span data-ttu-id="108c6-104">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="108c6-104">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="108c6-p101">Jedes Formular, jeder Bericht, jeder Bereich und jedes Steuerelement verfügt über Eigenschafteneinstellungen, mit denen Sie das Aussehen und die Funktionsweise eines Elements ändern können. Sie können die Eigenschaften im Eigenschaftenfenster, in einem Makro oder in Visual Basic anzeigen und ändern.</span><span class="sxs-lookup"><span data-stu-id="108c6-p101">Each form, report, section, and control has property settings that you can change to alter the look or behavior of that particular item. You view and change properties by using the property sheet, macro, or Visual Basic.</span></span>

## <a name="set-properties"></a><span data-ttu-id="108c6-107">Eigenschaften festlegen</span><span class="sxs-lookup"><span data-stu-id="108c6-107">Set properties</span></span>

1. <span data-ttu-id="108c6-p102">Wählen Sie in der Formularentwurfsansicht oder Berichtsentwurfsansicht das Steuerelement, den Bereich, das Formular oder den Bericht aus, für das bzw. den Sie die Eigenschaft einstellen möchten. Sie haben folgende Auswahlmöglichkeiten:</span><span class="sxs-lookup"><span data-stu-id="108c6-p102">In form Design view or report Design view, select the control, section, form, or report for which you want to set the property. You can select:</span></span>
    
   - <span data-ttu-id="108c6-110">Steuerelemente.</span><span class="sxs-lookup"><span data-stu-id="108c6-110">One or more controls.</span></span> <span data-ttu-id="108c6-111">Zum Auswählen mehrerer Steuerelemente die UMSCHALTTASTE gedrückt halten Sie und wählen Sie die Steuerelemente, oder ziehen Sie den Mauszeiger über die Steuerelemente, die Sie auswählen möchten.</span><span class="sxs-lookup"><span data-stu-id="108c6-111">To select multiple controls, hold down the SHIFT key and choose the controls, or drag the mouse pointer over the controls you wish to select.</span></span> <span data-ttu-id="108c6-112">Wenn Sie mehrere Steuerelemente auswählen, zeigt das Eigenschaftenfenster nur die Eigenschaften an, die alle markierten Steuerelemente gemeinsam besitzen.</span><span class="sxs-lookup"><span data-stu-id="108c6-112">If you select multiple controls, the property sheet will display only those properties that the selected controls have in common.</span></span>
    
   - <span data-ttu-id="108c6-113">Einen Bereich.</span><span class="sxs-lookup"><span data-stu-id="108c6-113">One section.</span></span> <span data-ttu-id="108c6-114">Wählen Sie die Bereichsauswahl des Abschnitts, den Sie auswählen möchten.</span><span class="sxs-lookup"><span data-stu-id="108c6-114">Choose the section selector of the section you wish to select.</span></span>
    
   - <span data-ttu-id="108c6-115">Das gesamte Formular oder den Bericht.</span><span class="sxs-lookup"><span data-stu-id="108c6-115">The entire form or report.</span></span> <span data-ttu-id="108c6-116">Wählen Sie die Formular- oder Berichtsauswahl in der oberen linken Ecke des Formulars oder Berichts.</span><span class="sxs-lookup"><span data-stu-id="108c6-116">Choose the form selector or report selector in the upper-left corner of the form or report.</span></span>

2. <span data-ttu-id="108c6-117">Anzuzeigen Sie das Eigenschaftenfenster durch das Objekt oder den Bereich mit der rechten Maustaste, und klicken Sie dann im Kontextmenü auf **Eigenschaften** auswählen oder durch Auswählen von **Eigenschaften** auf der Symbolleiste.</span><span class="sxs-lookup"><span data-stu-id="108c6-117">Display the property sheet by right-clicking the object or section and then choosing **Properties** on the shortcut menu, or by choosing **Properties** on the toolbar.</span></span>

3. <span data-ttu-id="108c6-118">Wählen Sie die Eigenschaft für die Sie den Wert festlegen möchten, und führen Sie dann eine der folgenden:</span><span class="sxs-lookup"><span data-stu-id="108c6-118">Choose the property for which you want to set the value, and then do one of the following:</span></span>
    
   - <span data-ttu-id="108c6-119">Geben Sie im Einstellungsfeld der Eigenschaft die gewünschte Einstellung oder einen geeigneten Ausdruck ein.</span><span class="sxs-lookup"><span data-stu-id="108c6-119">In the property box, type the appropriate setting or expression.</span></span>
    
   - <span data-ttu-id="108c6-120">Wenn das Einstellungsfeld der Eigenschaft einen Pfeil enthält, wählen Sie den Pfeil, und wählen Sie dann einen Wert in der Liste.</span><span class="sxs-lookup"><span data-stu-id="108c6-120">If the property box contains an arrow, choose the arrow and then choose a value in the list.</span></span>
    
   - <span data-ttu-id="108c6-121">Wenn eine **Generator** -Schaltfläche rechts neben dem Eigenschaftenfeld angezeigt wird, wählen Sie darauf, um ein Generator anzuzeigen oder Anzeigen eines Dialogfelds bietet Ihnen eine Auswahl von Generatoren.</span><span class="sxs-lookup"><span data-stu-id="108c6-121">If a **Build** button appears to the right of the property box, choose it to display a builder or to display a dialog box giving you a choice of builders.</span></span> <span data-ttu-id="108c6-122">Beispielsweise können Sie die Code-Generators, Makro-Generator oder Abfrage-Generator verwenden, um bestimmte Eigenschaften festzulegen.</span><span class="sxs-lookup"><span data-stu-id="108c6-122">For example, you can use the Code Builder, Macro Builder, or Query Builder to set some properties.</span></span>

## <a name="tips"></a><span data-ttu-id="108c6-123">Tipps</span><span class="sxs-lookup"><span data-stu-id="108c6-123">Tips</span></span>

- <span data-ttu-id="108c6-124">Microsoft Access stellt ein **Zoom** -Feld für die Eingabe und die Anzeige von Ausdrücken oder anderen langen Eigenschafteneinstellungen bereit.</span><span class="sxs-lookup"><span data-stu-id="108c6-124">Microsoft Access provides a **Zoom** box for typing and viewing expressions or other long property settings.</span></span> <span data-ttu-id="108c6-125">Um das Dialogfeld **Zoom** anzuzeigen, wählen Sie ein Eigenschaftenfeld im Eigenschaftenfenster.</span><span class="sxs-lookup"><span data-stu-id="108c6-125">To display the **Zoom** box, choose a property box in the property sheet.</span></span> <span data-ttu-id="108c6-126">Drücken Sie UMSCHALT + F2 oder mit der rechten Maustaste, und wählen Sie dann im Kontextmenü auf **Zoom** .</span><span class="sxs-lookup"><span data-stu-id="108c6-126">Press SHIFT+F2, or right-click, and then choose **Zoom** on the shortcut menu.</span></span>

- <span data-ttu-id="108c6-127">Sie können die Eigenschaft **Steuerelementinhalt** für einige Steuerelemente einstellen, indem Sie die Eigenschafteneinstellung im Steuerelement selbst vornehmen.</span><span class="sxs-lookup"><span data-stu-id="108c6-127">You can set the **ControlSource** property for some controls by typing the property setting in the control itself.</span></span>

- <span data-ttu-id="108c6-128">Durch Ändern der Standardeigenschafteneinstellungen für einen Steuerelementtyp erreichen Sie, dass später von Ihnen erstellte Steuerelemente über die neuen Standardeinstellungen verfügen.</span><span class="sxs-lookup"><span data-stu-id="108c6-128">You can change the default property settings for a type of control so that future controls you create will have the new default settings.</span></span>

- <span data-ttu-id="108c6-129">Die Eigenschafteneinstellungen eines gebundenen Steuerelements stimmen nicht immer mit den entsprechenden Einstellungen im Feld der zugrunde liegenden Tabelle oder Abfrage überein, an die das Steuerelement gebunden ist.</span><span class="sxs-lookup"><span data-stu-id="108c6-129">The property settings of a bound control might not match the corresponding settings in the field in the underlying table or query to which the control is bound.</span></span> <span data-ttu-id="108c6-130">In diesem Fall setzen die Einstellungen des Formulars oder Berichts in der Regel die Einstellungen der Tabelle oder Abfrage außer Kraft.</span><span class="sxs-lookup"><span data-stu-id="108c6-130">If the settings are different, the form or report settings typically override those in the table or query.</span></span>

