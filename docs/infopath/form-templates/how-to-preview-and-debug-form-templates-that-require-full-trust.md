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
# <a name="preview-and-debug-form-templates-that-require-full-trust"></a>Anzeigen der Vorschau und Debuggen von Formularvorlagen, die volle Vertrauenswürdigkeit erfordern

Standardmäßig, wenn Sie versuchen, Debuggen oder Vorschau einer verwalteten Code-Projekt, das Code enthält, der ein Objektmodellelement aufruft, die volle Vertrauenswürdigkeit erfordert, wie beispielsweise die **LoginName** -Eigenschaft der Zugriff auf Informationen über die Anmelde-Domäne des Benutzers erfordert, Microsoft InfoPath wird die folgenden Fehlermeldungen angezeigt. 
  
Beim Anzeigen der Vorschau:
  
"Eine unbekannte Ausnahme ist im Formularcode aufgetreten." Gefolgt von: "Fehler im Formularcode beim Abschließen dieser Aktion von InfoPath."
  
Beim Debuggen:
  
Wird der Fokus auf die Codezeile im Code-Editor, der das Element aufruft, die volle Vertrauenswürdigkeit erfordert, und die folgende Meldung angezeigt: **"SecurityException** wurde nicht von Benutzercode behandelt – Fehler bei Anforderung". 
  
Ermöglichen Sie die Formularvorlage von Geschäftslogik in diesen Member aufzurufen, wenn es gerade gedebuggt oder angezeigt werden, müssen Sie die Formularvorlage Sicherheitsstufe auf **Voll vertrauenswürdig** festlegen, wie im folgenden Verfahren beschrieben. 
  
## <a name="configuring-a-managed-code-form-template-that-requires-full-trust"></a>Konfigurieren einer Formularvorlage mit verwaltetem Code, die vollständig vertrauenswürdig sein muss

### <a name="set-your-forms-security-level-to-full-trust"></a>Festlegen der Sicherheitsebene "Voll vertrauenswürdig" für ein Formular

1. Öffnen Sie in InfoPath die Formularvorlage im Entwurfsmodus.
    
2. Klicken Sie auf der Registerkarte **Datei** , und klicken Sie dann auf der Registerkarte **Info** auf **Formularoptionen** . 
    
3. Klicken Sie in der Liste **Kategorie** auf **Sicherheit und Vertrauensstellung.**
    
4. Deaktivieren Sie unter **Sicherheitsstufe** **Sicherheitsstufe automatisch ermitteln**.
    
5. Wählen Sie **Voll vertrauenswürdig**aus, und klicken Sie dann auf **OK**.
    
Nachdem Sie dieses Verfahren durchgeführt wird, können Sie das Projekt debuggen, wie in der [Vorschau und Debuggen von InfoPath-Formularvorlagen mit Code](how-to-preview-and-debug-infopath-form-templates-with-code.md)beschrieben.
  
> [!NOTE]
> Erfolgreiche Bereitstellung von einer Formularvorlage für verwalteten Code, die volle Vertrauenswürdigkeit erfordert erfordert zusätzliche Schritte, wie digital signieren, oder installieren und registrieren die Formularvorlage. Informationen zur Bereitstellung von verwaltetem Code, um eine Formularvorlage nach dem Debuggen es finden Sie unter [Bereitstellen von InfoPath-Formularvorlagen mit Code](how-to-deploy-infopath-form-templates-with-code.md). 
  
## <a name="see-also"></a>Siehe auch



[Anzeigen der Vorschau und Debuggen von InfoPath-Formularvorlagen mit Code](how-to-preview-and-debug-infopath-form-templates-with-code.md)
  
[Bereitstellen von InfoPath-Formularvorlagen mit Code](how-to-deploy-infopath-form-templates-with-code.md)

