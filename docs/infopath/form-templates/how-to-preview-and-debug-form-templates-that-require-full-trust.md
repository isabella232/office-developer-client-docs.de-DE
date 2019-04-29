---
title: Vorschau und Debuggen von Formularvorlagen, die volle Vertrauenswürdigkeit erfordern
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- Debuggen [InfoPath 2007], InfoPath 2003-kompatible Formularvorlagen, Vorschau der InfoPath 2003-kompatiblen Formularvorlagen, Formularvorlagen [InfoPath 2007], Vorschau auf 2003-kompatible Formularvorlagen [InfoPath 2007], Debuggen von 2003-kompatibel, Debuggen InfoPath 2003-kompatible Formularvorlagen
localization_priority: Normal
ms.assetid: 5c491666-06f0-42ec-967e-1c70cd5e03a0
description: Wenn Sie versuchen, ein Projekt mit verwaltetem Code zu debuggen oder in der Vorschau anzuzeigen, das Code enthält, der ein Objektmodellelement aufruft, das volle Vertrauenswürdigkeit erfordert, wie beispielsweise die LoginName-Eigenschaft, die Zugriff auf Informationen zur Anmeldedomäne des Benutzers benötigt, Microsoft In InfoPath werden die folgenden Fehlermeldungen angezeigt.
ms.openlocfilehash: 0780db286e2ca9cef381c2d24cb621c7c243dcb7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411260"
---
# <a name="preview-and-debug-form-templates-that-require-full-trust"></a><span data-ttu-id="d2de8-104">Vorschau und Debuggen von Formularvorlagen, die volle Vertrauenswürdigkeit erfordern</span><span class="sxs-lookup"><span data-stu-id="d2de8-104">Preview and Debug Form Templates that Require Full Trust</span></span>

<span data-ttu-id="d2de8-105">Wenn Sie versuchen, ein Projekt mit verwaltetem Code zu debuggen oder in der Vorschau anzuzeigen, das Code enthält, der ein Objektmodellelement aufruft, das volle Vertrauenswürdigkeit erfordert, wie beispielsweise die **LoginName** -Eigenschaft, die Zugriff auf Informationen zur Anmeldedomäne des Benutzers benötigt, In Microsoft InfoPath werden die folgenden Fehlermeldungen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d2de8-105">By default, if you attempt to debug or preview a managed-code project that contains code that invokes an object model member that requires full trust, such as the **LoginName** property which requires access to information about the user's login domain, Microsoft InfoPath will display the following error messages.</span></span> 
  
<span data-ttu-id="d2de8-106">Beim Anzeigen der Vorschau:</span><span class="sxs-lookup"><span data-stu-id="d2de8-106">When previewing:</span></span>
  
<span data-ttu-id="d2de8-p101">"Eine unbekannte Ausnahme ist im Formularcode aufgetreten." Gefolgt von: "Fehler im Formularcode beim Abschließen dieser Aktion von InfoPath."</span><span class="sxs-lookup"><span data-stu-id="d2de8-p101">"An unhandled exception has occurred in the form's code." Followed by, "InfoPath cannot complete this action, because of an error in the form's code."</span></span>
  
<span data-ttu-id="d2de8-109">Beim Debuggen:</span><span class="sxs-lookup"><span data-stu-id="d2de8-109">When debugging:</span></span>
  
<span data-ttu-id="d2de8-110">Der Fokus wird auf die Codezeile im Code-Editor verschoben, der das Mitglied anruft, das volle Vertrauenswürdigkeit erfordert, und die folgende Meldung wird angezeigt \*\*\*\* : "SecurityException wurde von der Benutzercode Anforderung nicht verarbeitet".</span><span class="sxs-lookup"><span data-stu-id="d2de8-110">Focus will move to the line of code in the code editor that is calling the member that requires full trust, and the following message will be displayed: " **SecurityException** was unhandled by user code - Request failed".</span></span> 
  
<span data-ttu-id="d2de8-111">Sie müssen für die Sicherheitsebene der Formularvorlage **Voll vertrauenswürdig** festlegen, wie im folgenden Verfahren beschrieben, um das Aufrufen dieses Members beim Debuggen oder Anzeigen einer Vorschau durch die Geschäftslogik der Formularvorlage zuzulassen.</span><span class="sxs-lookup"><span data-stu-id="d2de8-111">To allow the form template's business logic to call this member when it is being debugged or previewed, you must set your form template's security level to **Full Trust** as described in the following procedure.</span></span> 
  
## <a name="configuring-a-managed-code-form-template-that-requires-full-trust"></a><span data-ttu-id="d2de8-112">Konfigurieren einer Formularvorlage mit verwaltetem Code, die vollständig vertrauenswürdig sein muss</span><span class="sxs-lookup"><span data-stu-id="d2de8-112">Configuring a Managed Code Form Template that Requires Full Trust</span></span>

### <a name="set-your-forms-security-level-to-full-trust"></a><span data-ttu-id="d2de8-113">Festlegen der Sicherheitsebene "Voll vertrauenswürdig" für ein Formular</span><span class="sxs-lookup"><span data-stu-id="d2de8-113">Set your form's security level to Full Trust</span></span>

1. <span data-ttu-id="d2de8-114">Öffnen Sie in InfoPath die Formularvorlage im Entwurfsmodus.</span><span class="sxs-lookup"><span data-stu-id="d2de8-114">In InfoPath, open the form template in design mode.</span></span>
    
2. <span data-ttu-id="d2de8-115">Klicken Sie auf die Registerkarte **Datei**, und klicken Sie dann auf der Registerkarte **Info** auf **Formularoptionen**.</span><span class="sxs-lookup"><span data-stu-id="d2de8-115">Click the **File** tab, and then click **Form Options** on the **Info** tab.</span></span> 
    
3. <span data-ttu-id="d2de8-116">Klicken Sie in der Liste **Kategorie** auf **Sicherheit und Vertrauensstellung**.</span><span class="sxs-lookup"><span data-stu-id="d2de8-116">In the **Category** list, click **Security and Trust.**</span></span>
    
4. <span data-ttu-id="d2de8-117">Deaktivieren Sie im Bereich **Sicherheitsstufe** das Kontrollkästchen **Sicherheitsstufe automatisch ermitteln**.</span><span class="sxs-lookup"><span data-stu-id="d2de8-117">Under **Security Level**, clear **Automatically determine security level**.</span></span>
    
5. <span data-ttu-id="d2de8-118">Wählen Sie **Voll vertrauenswürdig** aus, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="d2de8-118">Select **Full Trust**, and then click **OK**.</span></span>
    
<span data-ttu-id="d2de8-119">Nachdem Sie dieses Verfahren ausgeführt haben, können Sie das Projekt Debuggen, wie in [Vorschau und Debuggen von InfoPath-Formularvorlagen mit Code](how-to-preview-and-debug-infopath-form-templates-with-code.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="d2de8-119">After this procedure is performed, you can debug your project as described in [Preview and Debug InfoPath Form Templates with Code](how-to-preview-and-debug-infopath-form-templates-with-code.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="d2de8-120">Für die erfolgreiche Bereitstellung von Formularvorlagen mit verwaltetem Code, die vollständig vertrauenswürdig sein müssen, sind zusätzliche Schritte erforderlich, z. B. das digitale Signieren oder Installieren und Registrieren der Formularvorlage.</span><span class="sxs-lookup"><span data-stu-id="d2de8-120">Successfully deploying a managed code form template that requires full trust requires additional steps, such as digitally signing, or installing and registering the form template.</span></span> <span data-ttu-id="d2de8-121">Informationen zur Bereitstellung einer Formularvorlage mit verwaltetem Code, nachdem Sie gedebuggt wurde, finden Sie unter [Bereitstellen von InfoPath-Formularvorlagen mit Code](how-to-deploy-infopath-form-templates-with-code.md).</span><span class="sxs-lookup"><span data-stu-id="d2de8-121">For information on deploying a managed code form template after it is debugged see, [Deploy InfoPath Form Templates with Code](how-to-deploy-infopath-form-templates-with-code.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d2de8-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d2de8-122">See also</span></span>



[<span data-ttu-id="d2de8-123">Anzeigen und Debuggen von InfoPath-Formularvorlagen mit Code</span><span class="sxs-lookup"><span data-stu-id="d2de8-123">Preview and Debug InfoPath Form Templates with Code</span></span>](how-to-preview-and-debug-infopath-form-templates-with-code.md)
  
[<span data-ttu-id="d2de8-124">Bereitstellen von InfoPath-Formularvorlagen mit Code</span><span class="sxs-lookup"><span data-stu-id="d2de8-124">Deploy InfoPath Form Templates with Code</span></span>](how-to-deploy-infopath-form-templates-with-code.md)

