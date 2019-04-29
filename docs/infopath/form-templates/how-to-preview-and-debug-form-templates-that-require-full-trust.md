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
# <a name="preview-and-debug-form-templates-that-require-full-trust"></a>Vorschau und Debuggen von Formularvorlagen, die volle Vertrauenswürdigkeit erfordern

Wenn Sie versuchen, ein Projekt mit verwaltetem Code zu debuggen oder in der Vorschau anzuzeigen, das Code enthält, der ein Objektmodellelement aufruft, das volle Vertrauenswürdigkeit erfordert, wie beispielsweise die **LoginName** -Eigenschaft, die Zugriff auf Informationen zur Anmeldedomäne des Benutzers benötigt, In Microsoft InfoPath werden die folgenden Fehlermeldungen angezeigt. 
  
Beim Anzeigen der Vorschau:
  
"Eine unbekannte Ausnahme ist im Formularcode aufgetreten." Gefolgt von: "Fehler im Formularcode beim Abschließen dieser Aktion von InfoPath."
  
Beim Debuggen:
  
Der Fokus wird auf die Codezeile im Code-Editor verschoben, der das Mitglied anruft, das volle Vertrauenswürdigkeit erfordert, und die folgende Meldung wird angezeigt **** : "SecurityException wurde von der Benutzercode Anforderung nicht verarbeitet". 
  
Sie müssen für die Sicherheitsebene der Formularvorlage **Voll vertrauenswürdig** festlegen, wie im folgenden Verfahren beschrieben, um das Aufrufen dieses Members beim Debuggen oder Anzeigen einer Vorschau durch die Geschäftslogik der Formularvorlage zuzulassen. 
  
## <a name="configuring-a-managed-code-form-template-that-requires-full-trust"></a>Konfigurieren einer Formularvorlage mit verwaltetem Code, die vollständig vertrauenswürdig sein muss

### <a name="set-your-forms-security-level-to-full-trust"></a>Festlegen der Sicherheitsebene "Voll vertrauenswürdig" für ein Formular

1. Öffnen Sie in InfoPath die Formularvorlage im Entwurfsmodus.
    
2. Klicken Sie auf die Registerkarte **Datei**, und klicken Sie dann auf der Registerkarte **Info** auf **Formularoptionen**. 
    
3. Klicken Sie in der Liste **Kategorie** auf **Sicherheit und Vertrauensstellung**.
    
4. Deaktivieren Sie im Bereich **Sicherheitsstufe** das Kontrollkästchen **Sicherheitsstufe automatisch ermitteln**.
    
5. Wählen Sie **Voll vertrauenswürdig** aus, und klicken Sie dann auf **OK**.
    
Nachdem Sie dieses Verfahren ausgeführt haben, können Sie das Projekt Debuggen, wie in [Vorschau und Debuggen von InfoPath-Formularvorlagen mit Code](how-to-preview-and-debug-infopath-form-templates-with-code.md)beschrieben.
  
> [!NOTE]
> Für die erfolgreiche Bereitstellung von Formularvorlagen mit verwaltetem Code, die vollständig vertrauenswürdig sein müssen, sind zusätzliche Schritte erforderlich, z. B. das digitale Signieren oder Installieren und Registrieren der Formularvorlage. Informationen zur Bereitstellung einer Formularvorlage mit verwaltetem Code, nachdem Sie gedebuggt wurde, finden Sie unter [Bereitstellen von InfoPath-Formularvorlagen mit Code](how-to-deploy-infopath-form-templates-with-code.md). 
  
## <a name="see-also"></a>Siehe auch



[Anzeigen und Debuggen von InfoPath-Formularvorlagen mit Code](how-to-preview-and-debug-infopath-form-templates-with-code.md)
  
[Bereitstellen von InfoPath-Formularvorlagen mit Code](how-to-deploy-infopath-form-templates-with-code.md)

