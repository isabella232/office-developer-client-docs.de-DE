---
title: Anzeigen der Vorschau und Debuggen von Formularvorlagen, die volle Vertrauenswürdigkeit erfordern
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- Debuggen [Infopath 2007] Infopath 2003-kompatible Formularvorlagen, Vorschau von InfoPath 2003-kompatible Formularvorlagen, Vorschau 2003-kompatible Formularvorlagen [InfoPath 2007], Debuggen von 2003-kompatible Debuggen Formularvorlagen [InfoPath 2007] InfoPath 2003-kompatible Formularvorlagen
localization_priority: Normal
ms.assetid: 5c491666-06f0-42ec-967e-1c70cd5e03a0
description: Standardmäßig, wenn Sie versuchen, Debuggen oder Vorschau einer verwalteten Code-Projekt, das Code enthält, der ein Objektmodellelement aufruft, die volle Vertrauenswürdigkeit erfordert, wie beispielsweise die LoginName-Eigenschaft der benötigt Zugriff auf Informationen zu Anmelde-Domäne des Benutzers, Microsoft InfoPath wird die folgenden Fehlermeldungen angezeigt.
ms.openlocfilehash: e9077b4ec0f8369b869e986020e4860f325fc023
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790733"
---
# <a name="preview-and-debug-form-templates-that-require-full-trust"></a><span data-ttu-id="ab383-104">Anzeigen der Vorschau und Debuggen von Formularvorlagen, die volle Vertrauenswürdigkeit erfordern</span><span class="sxs-lookup"><span data-stu-id="ab383-104">Preview and Debug Form Templates that Require Full Trust</span></span>

<span data-ttu-id="ab383-105">Standardmäßig, wenn Sie versuchen, Debuggen oder Vorschau einer verwalteten Code-Projekt, das Code enthält, der ein Objektmodellelement aufruft, die volle Vertrauenswürdigkeit erfordert, wie beispielsweise die **LoginName** -Eigenschaft der Zugriff auf Informationen über die Anmelde-Domäne des Benutzers erfordert, Microsoft InfoPath wird die folgenden Fehlermeldungen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ab383-105">By default, if you attempt to debug or preview a managed-code project that contains code that invokes an object model member that requires full trust, such as the **LoginName** property which requires access to information about the user's login domain, Microsoft InfoPath will display the following error messages.</span></span> 
  
<span data-ttu-id="ab383-106">Beim Anzeigen der Vorschau:</span><span class="sxs-lookup"><span data-stu-id="ab383-106">When previewing:</span></span>
  
<span data-ttu-id="ab383-p101">"Eine unbekannte Ausnahme ist im Formularcode aufgetreten." Gefolgt von: "Fehler im Formularcode beim Abschließen dieser Aktion von InfoPath."</span><span class="sxs-lookup"><span data-stu-id="ab383-p101">"An unhandled exception has occurred in the form's code." Followed by, "InfoPath cannot complete this action, because of an error in the form's code."</span></span>
  
<span data-ttu-id="ab383-109">Beim Debuggen:</span><span class="sxs-lookup"><span data-stu-id="ab383-109">When debugging:</span></span>
  
<span data-ttu-id="ab383-110">Wird der Fokus auf die Codezeile im Code-Editor, der das Element aufruft, die volle Vertrauenswürdigkeit erfordert, und die folgende Meldung angezeigt: **"SecurityException** wurde nicht von Benutzercode behandelt – Fehler bei Anforderung".</span><span class="sxs-lookup"><span data-stu-id="ab383-110">Focus will move to the line of code in the code editor that is calling the member that requires full trust, and the following message will be displayed: " **SecurityException** was unhandled by user code - Request failed".</span></span> 
  
<span data-ttu-id="ab383-111">Ermöglichen Sie die Formularvorlage von Geschäftslogik in diesen Member aufzurufen, wenn es gerade gedebuggt oder angezeigt werden, müssen Sie die Formularvorlage Sicherheitsstufe auf **Voll vertrauenswürdig** festlegen, wie im folgenden Verfahren beschrieben.</span><span class="sxs-lookup"><span data-stu-id="ab383-111">To allow the form template's business logic to call this member when it is being debugged or previewed, you must set your form template's security level to **Full Trust** as described in the following procedure.</span></span> 
  
## <a name="configuring-a-managed-code-form-template-that-requires-full-trust"></a><span data-ttu-id="ab383-112">Konfigurieren einer Formularvorlage mit verwaltetem Code, die vollständig vertrauenswürdig sein muss</span><span class="sxs-lookup"><span data-stu-id="ab383-112">Configuring a Managed Code Form Template that Requires Full Trust</span></span>

### <a name="set-your-forms-security-level-to-full-trust"></a><span data-ttu-id="ab383-113">Festlegen der Sicherheitsebene "Voll vertrauenswürdig" für ein Formular</span><span class="sxs-lookup"><span data-stu-id="ab383-113">Set your form's security level to Full Trust</span></span>

1. <span data-ttu-id="ab383-114">Öffnen Sie in InfoPath die Formularvorlage im Entwurfsmodus.</span><span class="sxs-lookup"><span data-stu-id="ab383-114">In InfoPath, open the form template in design mode.</span></span>
    
2. <span data-ttu-id="ab383-115">Klicken Sie auf der Registerkarte **Datei** , und klicken Sie dann auf der Registerkarte **Info** auf **Formularoptionen** .</span><span class="sxs-lookup"><span data-stu-id="ab383-115">Click the **File** tab, and then click **Form Options** on the **Info** tab.</span></span> 
    
3. <span data-ttu-id="ab383-116">Klicken Sie in der Liste **Kategorie** auf **Sicherheit und Vertrauensstellung.**</span><span class="sxs-lookup"><span data-stu-id="ab383-116">In the **Category** list, click **Security and Trust.**</span></span>
    
4. <span data-ttu-id="ab383-117">Deaktivieren Sie unter **Sicherheitsstufe** **Sicherheitsstufe automatisch ermitteln**.</span><span class="sxs-lookup"><span data-stu-id="ab383-117">Under **Security Level**, clear **Automatically determine security level**.</span></span>
    
5. <span data-ttu-id="ab383-118">Wählen Sie **Voll vertrauenswürdig**aus, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="ab383-118">Select **Full Trust**, and then click **OK**.</span></span>
    
<span data-ttu-id="ab383-119">Nachdem Sie dieses Verfahren durchgeführt wird, können Sie das Projekt debuggen, wie in der [Vorschau und Debuggen von InfoPath-Formularvorlagen mit Code](how-to-preview-and-debug-infopath-form-templates-with-code.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="ab383-119">After this procedure is performed, you can debug your project as described in [Preview and Debug InfoPath Form Templates with Code](how-to-preview-and-debug-infopath-form-templates-with-code.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="ab383-120">Erfolgreiche Bereitstellung von einer Formularvorlage für verwalteten Code, die volle Vertrauenswürdigkeit erfordert erfordert zusätzliche Schritte, wie digital signieren, oder installieren und registrieren die Formularvorlage.</span><span class="sxs-lookup"><span data-stu-id="ab383-120">Successfully deploying a managed code form template that requires full trust requires additional steps, such as digitally signing, or installing and registering the form template.</span></span> <span data-ttu-id="ab383-121">Informationen zur Bereitstellung von verwaltetem Code, um eine Formularvorlage nach dem Debuggen es finden Sie unter [Bereitstellen von InfoPath-Formularvorlagen mit Code](how-to-deploy-infopath-form-templates-with-code.md).</span><span class="sxs-lookup"><span data-stu-id="ab383-121">For information on deploying a managed code form template after it is debugged see, [Deploy InfoPath Form Templates with Code](how-to-deploy-infopath-form-templates-with-code.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ab383-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ab383-122">See also</span></span>



[<span data-ttu-id="ab383-123">Anzeigen der Vorschau und Debuggen von InfoPath-Formularvorlagen mit Code</span><span class="sxs-lookup"><span data-stu-id="ab383-123">Preview and Debug InfoPath Form Templates with Code</span></span>](how-to-preview-and-debug-infopath-form-templates-with-code.md)
  
[<span data-ttu-id="ab383-124">Bereitstellen von InfoPath-Formularvorlagen mit Code</span><span class="sxs-lookup"><span data-stu-id="ab383-124">Deploy InfoPath Form Templates with Code</span></span>](how-to-deploy-infopath-form-templates-with-code.md)

