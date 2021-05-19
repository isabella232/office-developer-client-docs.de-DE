---
title: Erstellen einer Formularvorlage mithilfe des InfoPath 2003-Objektmodells
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- infopath 2003-kompatible Formularvorlagen,Formularvorlagen [InfoPath 2007], Erstellen von InfoPath 2003-kompatiblen,InfoPath 2007, Erstellen von InfoPath 2003-kompatiblen Formularvorlagen
localization_priority: Normal
ms.assetid: c746aeb1-902c-440e-830b-5b9efad0ca04
description: Die Verfahren in diesem Thema beschreiben das Erstellen einer Formularvorlage, die mit dem InfoPath 2003-kompatiblen Objektmodell kompatibel ist.
ms.openlocfilehash: 35a9fcfbb0d93a19e013bde6980bc94af3bb5dd9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418183"
---
# <a name="create-a-form-template-using-the-infopath-2003-object-model"></a><span data-ttu-id="2eb0f-104">Erstellen einer Formularvorlage mithilfe des InfoPath 2003-Objektmodells</span><span class="sxs-lookup"><span data-stu-id="2eb0f-104">Create a Form Template Using the InfoPath 2003 Object Model</span></span>

<span data-ttu-id="2eb0f-105">Die Verfahren in diesem Thema beschreiben das Erstellen einer Formularvorlage, die mit dem InfoPath 2003-kompatiblen Objektmodell kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="2eb0f-105">The procedures in this topic describe how to create a form template that works with the InfoPath 2003-compatible object model.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="2eb0f-106">Zusätzlich zu den folgenden Verfahren müssen  Sie auch auf die Registerkarte Datei klicken, auf Speichern unter **klicken** und dann **infoPath 2003-Formularvorlage** im Feld Als Typ speichern auswählen, um die Formularvorlage im InfoPath 2003-kompatiblen Dateiformat zu speichern. </span><span class="sxs-lookup"><span data-stu-id="2eb0f-106">In addition to the procedures below, you must also click the **File** tab, click **Save As**, and then select **InfoPath 2003 Form Template** in the **Save as type** box to save the form template to the InfoPath 2003-compatible file format.</span></span> <span data-ttu-id="2eb0f-107">Zum Öffnen von InfoPath 2003-kompatiblen Formularvorlagen, die mit InfoPath erstellt wurden, müssen alle InfoPath 2003-Benutzer die .NET Framework 2.0 oder höher auf ihren Computern installiert haben.</span><span class="sxs-lookup"><span data-stu-id="2eb0f-107">Also, to open InfoPath 2003-compatible form templates created with InfoPath, all InfoPath 2003 users must have the .NET Framework 2.0 or later installed on their computers.</span></span> 
  
### <a name="to-create-an-infopath-2003-compatible-form-template-in-infopath-with-visual-studio-tools-for-applications"></a><span data-ttu-id="2eb0f-108">So erstellen Sie eine InfoPath 2003-kompatible Formularvorlage in InfoPath mit Visual Studio Tools for Applications</span><span class="sxs-lookup"><span data-stu-id="2eb0f-108">To create an InfoPath 2003-compatible form template in InfoPath with Visual Studio Tools for Applications</span></span>

1. <span data-ttu-id="2eb0f-109">Starten Sie den InfoPath-Designer.</span><span class="sxs-lookup"><span data-stu-id="2eb0f-109">Start the InfoPath Designer.</span></span>
    
2. <span data-ttu-id="2eb0f-110">Klicken Sie auf die Registerkarte **Datei**, und klicken Sie dann auf **Formularoptionen**.</span><span class="sxs-lookup"><span data-stu-id="2eb0f-110">Click the **File** tab, and then click **Form Options**.</span></span>
    
3. <span data-ttu-id="2eb0f-111">Wählen Sie in der Kategorie **Kompatibilität** die Option **InfoPath 2003-Editorformulare** aus.</span><span class="sxs-lookup"><span data-stu-id="2eb0f-111">In the **Compatibility** category, select **InfoPath 2003 Editor Form**.</span></span>
    
4. <span data-ttu-id="2eb0f-112">Wählen Sie in der Kategorie **Programmierung** in der Dropdownliste **Codesprache der Formularvorlage** entweder **C# (kompatibel mit InfoPath 2003)** oder **Visual Basic (kompatibel mit InfoPath 2003)** aus.</span><span class="sxs-lookup"><span data-stu-id="2eb0f-112">In the **Programming** category, select either **C# (InfoPath 2003 Compatible)** or **Visual Basic (InfoPath 2003 Compatible)** from the **Form template code language** drop-down list.</span></span> 
    
5. <span data-ttu-id="2eb0f-113">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="2eb0f-113">Click **OK**.</span></span>
    
6. <span data-ttu-id="2eb0f-114">Entwerfen Sie Ihre Formularvorlage, und fügen Sie dann Ereignishandler in Visual Studio 2012 hinzu, wie unter Hinzufügen eines Ereignishandlers mithilfe des [InfoPath 2003-Objektmodells beschrieben.](how-to-add-an-event-handler-using-the-infopath-2003-object-model.md)</span><span class="sxs-lookup"><span data-stu-id="2eb0f-114">Design your form template, and then add event handlers in Visual Studio 2012, as described in [Add an Event Handler Using the InfoPath 2003 Object Model](how-to-add-an-event-handler-using-the-infopath-2003-object-model.md).</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2eb0f-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2eb0f-115">See also</span></span>



[<span data-ttu-id="2eb0f-116">Exemplarische Vorgehensweise: Erstellen und Debuggen einer einfachen Formularvorlage mit dem InfoPath 2003-Objektmodell</span><span class="sxs-lookup"><span data-stu-id="2eb0f-116">Walkthrough: Creating and Debugging a Basic Form Template Using the InfoPath 2003 Object Model</span></span>](walkthrough-create-and-debug-basic-form-template-using-infopath-object-model.md)
  
[<span data-ttu-id="2eb0f-117">Erstellen von Formularvorlagen mithilfe des InfoPath 2003-Objektmodells</span><span class="sxs-lookup"><span data-stu-id="2eb0f-117">Creating Form Templates Using the InfoPath 2003 Object Model</span></span>](creating-form-templates-using-the-infopath-2003-object-model.md)

