---
title: Zusätzlichen Eigenschaftenfensters eines ActiveX-Steuerelements
TOCTitle: ActiveX Control's Custom Properties Dialog Box
ms:assetid: 124cf679-6efc-567a-84d1-8057dec93bde
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845396(v=office.15)
ms:contentKeyID: 48543338
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm4040
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 6f5924d04e9ea4febee1434f6ef99f95b02eab6b
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25474652"
---
# <a name="activex-controls-custom-properties-dialog-box"></a><span data-ttu-id="720d1-102">Zusätzlichen Eigenschaftenfensters eines ActiveX-Steuerelements</span><span class="sxs-lookup"><span data-stu-id="720d1-102">ActiveX Control's Custom Properties Dialog Box</span></span>

<span data-ttu-id="720d1-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="720d1-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="720d1-p101">Wenn Sie die Eigenschaften eines ActiveX-Steuerelements einstellen, möchten Sie möglicherweise das zusätzliche Eigenschaftenfenster des Steuerelements verwenden. Das zusätzliche Eigenschaftenfenster ist eine Alternative zur Eigenschaftenliste im Microsoft Access-Eigenschaftenfenster zum Einstellen der Eigenschaften des ActiveX-Steuerelements in der Entwurfsansicht.</span><span class="sxs-lookup"><span data-stu-id="720d1-p101">When setting the properties of an ActiveX control, you may need or prefer to use the control's custom properties dialog box. This custom properties dialog box provides an alternative to the list of properties in the Microsoft Access property sheet for setting ActiveX control properties in Design view.</span></span>

> [!NOTE]
> <span data-ttu-id="720d1-106">[!HINWEIS] Diese Informationen betreffen nur ActiveX-Steuerelemente in einer Microsoft Access-Datenbankumgebung.</span><span class="sxs-lookup"><span data-stu-id="720d1-106">This information only applies to ActiveX controls in a Microsoft Access database environment.</span></span>



## <a name="two-ways-to-set-properties"></a><span data-ttu-id="720d1-107">Zwei Möglichkeiten zum Einstellen von Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="720d1-107">Two Ways to Set Properties</span></span>

<span data-ttu-id="720d1-p102">Der Grund für das Vorhandensein des zusätzlichen Eigenschaftenfensters besteht darin, dass nicht alle Anwendungen, die ActiveX-Steuerelemente benutzen, ein Eigenschaftenfenster wie das von Microsoft Access besitzen. Das zusätzliche Eigenschaftenfenster stellt eine Schnittstelle zum Einstellen der wichtigsten Steuerelementeigenschaften bereit, unabhängig von der Oberfläche der Host-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="720d1-p102">The reason for the custom properties dialog box is that not all applications that use ActiveX controls provide a property sheet like the one in Microsoft Access. The custom properties dialog box provides an interface for setting key control properties regardless of the interface supplied by the hosting application.</span></span>

<span data-ttu-id="720d1-110">Die Eigenschaften einiger ActiveX-Steuerelemente können Sie in beiden Eigenschaftenfenstern festlegen:</span><span class="sxs-lookup"><span data-stu-id="720d1-110">For some ActiveX control properties, you can choose either of these two locations to set the property:</span></span>

  - <span data-ttu-id="720d1-111">Im Microsoft Access-Eigenschaftenfenster</span><span class="sxs-lookup"><span data-stu-id="720d1-111">The Microsoft Access property sheet.</span></span>

  - <span data-ttu-id="720d1-112">Im zusätzlichen Eigenschaftenfenster eines ActiveX-Steuerelements</span><span class="sxs-lookup"><span data-stu-id="720d1-112">The ActiveX control's custom properties dialog box.</span></span>

<span data-ttu-id="720d1-p103">In einigen Fällen können Sie nur das zusätzliche Eigenschaftenfenster zum Einstellen einer Eigenschaft in der Entwurfsansicht verwenden. Dies ist normalerweise dann der Fall, wenn die Schnittstelle, die zum Einstellen einer Eigenschaft benötigt wird, nicht innerhalb des Microsoft Access-Eigenschaftenfensters funktioniert. Beispielsweise besitzt die Eigenschaft **GridFont** des Kalender-Steuerelements mehrere Argumente; Sie können jedoch im Microsoft Access-Eigenschaftenfenster nur ein Argument pro Eigenschaft einstellen.</span><span class="sxs-lookup"><span data-stu-id="720d1-p103">In some cases, the custom properties dialog box is the only way to set a property in Design view. This is usually the situation when the interface needed to set a property doesn't work inside the Microsoft Access property sheet. For example, the **GridFont** property for the Calendar control has a number of arguments; you can't set more than one argument per property in the Microsoft Access property sheet.</span></span>

## <a name="finding-the-custom-properties-dialog-box"></a><span data-ttu-id="720d1-116">Suchen des zusätzlichen Eigenschaftenfensters</span><span class="sxs-lookup"><span data-stu-id="720d1-116">Finding the Custom Properties Dialog Box</span></span>

<span data-ttu-id="720d1-p104">Nicht alle ActiveX-Steuerelemente stellen ein zusätzliches Eigenschaftenfenster bereit. Um herauszufinden, ob ein Steuerelement ein zusätzliches Eigenschaftenfenster bereitstellt, suchen Sie im Microsoft Access-Eigenschaftenfenster für dieses Steuerelement nach der **Custom** -Eigenschaft. Wenn in der Liste der Eigenschaften der Name **Benutzerdefiniert** enthalten ist, stellt das Steuerelement das zusätzliche Eigenschaftenfenster bereit.</span><span class="sxs-lookup"><span data-stu-id="720d1-p104">Not all ActiveX controls provide a custom properties dialog box. To see whether a control provides this custom properties dialog box, look for the **Custom** property in the Microsoft Access property sheet for this control. If the list of properties contains the name **Custom**, then the control provides the custom properties dialog box.</span></span>

## <a name="using-the-custom-properties-dialog-box"></a><span data-ttu-id="720d1-120">Verwenden des zusätzlichen Eigenschaftenfensters</span><span class="sxs-lookup"><span data-stu-id="720d1-120">Using the Custom Properties Dialog Box</span></span>

<span data-ttu-id="720d1-p105">Klicken Sie im Microsoft Access-Eigenschaftenfenster auf das Eigenschaftenfeld **Benutzerdefiniert** und anschließend auf die** **Generator-Schaltfläche rechts neben dem Eigenschaftenfeld, um das zusätzliche Eigenschaftenfenster des Steuerelements anzuzeigen. Es wird häufig als Dialogfeld mit Registerkarten dargestellt. Klicken Sie auf die entsprechende Registerkarte zum Festlegen der gewünschten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="720d1-p105">After you click the **Custom** property box in the Microsoft Access property sheet, click the **Build** button to the right of the property box to display the control's custom properties dialog box, often presented as a tabbed dialog box. Choose the tab that contains the interface for setting the properties that you want to set.</span></span>

<span data-ttu-id="720d1-p106">Nachdem Sie Änderungen auf einer Registerkarte vorgenommen haben, können Sie diese Änderungen häufig direkt anwenden, indem Sie auf die Schaltfläche **Übernehmen** (falls vorhanden) klicken. Sie können auch auf andere Registerkarten klicken, um bei Bedarf weitere Eigenschaften festzulegen. Damit alle im zusätzlichen Eigenschaftenfenster vorgenommenen Änderungen wirksam werden, klicken Sie auf die Schaltfläche **OK**. Wenn Sie zum Microsoft Access-Eigenschaftenfenster zurückkehren möchten, ohne Eigenschafteneinstellungen zu ändern, klicken Sie auf die Schaltfläche **Abbrechen**.</span><span class="sxs-lookup"><span data-stu-id="720d1-p106">After you make changes on one tab, you can often apply those changes immediately by clicking the **Apply** button (if provided). You can click other tabs to set other properties as needed. To approve all changes made in the custom properties dialog box, click the **OK** button. To return to the Microsoft Access property sheet without changing any property settings, click the **Cancel** button.</span></span>

<span data-ttu-id="720d1-p107">Sie können das zusätzliche Eigenschaftenfenster auch anzeigen, indem Sie im Menü **Bearbeiten** auf den Eintrag für das ActiveX-Steuerelement (z. B. **Kalender**-**Objekt**) und dann auf den Unterbefehl **Eigenschaften** klicken, oder indem Sie im Kontextmenü des ActiveX-Steuerelements auf diesen Unterbefehl klicken. Außerdem besitzen einige Eigenschaften, wie z. B. die **GridFontColor**-Eigenschaft, im Microsoft Access-Eigenschaftenfenster für das ActiveX-Steuerelement eine** **Generator-Schaltfläche rechts neben dem Eigenschaftenfeld. Wenn Sie auf die** **Generator-Schaltfläche klicken, wird das zusätzliche Eigenschaftenfenster angezeigt, wobei die entsprechende Registerkarte (z. B. **Farbe**) ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="720d1-p107">You can also view the custom properties dialog box by clicking the **Properties** subcommand of the ActiveX control **Object** command (for example, **Calendar Control Object**) on the **Edit** menu, or by clicking this same subcommand on the shortcut menu for the ActiveX control. In addition, some properties in the Microsoft Access property sheet for the ActiveX control, like the **GridFontColor** property of the Calendar control, have a **Build** button to the right of the property box. When you click the **Build** button, the custom properties dialog box is displayed, with the appropriate tab selected (for example, **Colors**).</span></span>

