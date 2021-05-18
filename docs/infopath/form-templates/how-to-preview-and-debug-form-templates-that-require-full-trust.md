---
title: Vorschau und Debuggen von Formularvorlagen, die eine vollständige Vertrauenswürdigkeit erfordern
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- Debugging [infopath 2007], infopath 2003-kompatible Formularvorlagen,Vorschau von InfoPath 2003-kompatiblen Formularvorlagen,Formularvorlagen [InfoPath 2007], Vorschau von 2003-kompatiblen Formularvorlagen [InfoPath 2007], Debuggen von 2003-kompatiblen,Debuggen von InfoPath 2003-kompatiblen Formularvorlagen
localization_priority: Normal
ms.assetid: 5c491666-06f0-42ec-967e-1c70cd5e03a0
description: Wenn Sie versuchen, ein Projekt mit verwalteten Code zu debuggen oder in der Vorschau anzuzeigen, das Code enthält, der ein Objektmodellmmitglied aufruft, das volle Vertrauenswürdigkeit erfordert, z. B. die LoginName-Eigenschaft, die Zugriff auf Informationen zur Anmeldedomäne des Benutzers erfordert, zeigt Microsoft InfoPath die folgenden Fehlermeldungen an.
ms.openlocfilehash: 0780db286e2ca9cef381c2d24cb621c7c243dcb7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411260"
---
# <a name="preview-and-debug-form-templates-that-require-full-trust"></a>Vorschau und Debuggen von Formularvorlagen, die eine vollständige Vertrauenswürdigkeit erfordern

Wenn Sie versuchen, ein Projekt mit verwalteten Code zu debuggen oder in der Vorschau anzuzeigen, das Code enthält, der ein Objektmodellmmitglied aufruft, das volle Vertrauenswürdigkeit erfordert, z. B. die **LoginName-Eigenschaft,** die Zugriff auf Informationen zur Anmeldedomäne des Benutzers erfordert, zeigt Microsoft InfoPath die folgenden Fehlermeldungen an. 
  
Beim Anzeigen der Vorschau:
  
"Eine unbekannte Ausnahme ist im Formularcode aufgetreten." Gefolgt von: "Fehler im Formularcode beim Abschließen dieser Aktion von InfoPath."
  
Beim Debuggen:
  
Der Fokus wird zur Codezeile im Code-Editor wechseln, der das Mitglied aufruft, das volle Vertrauenswürdigkeit erfordert, und die folgende Meldung wird angezeigt: **"SecurityException** was unhandled by user code - Request failed". 
  
Sie müssen für die Sicherheitsebene der Formularvorlage **Voll vertrauenswürdig** festlegen, wie im folgenden Verfahren beschrieben, um das Aufrufen dieses Members beim Debuggen oder Anzeigen einer Vorschau durch die Geschäftslogik der Formularvorlage zuzulassen. 
  
## <a name="configuring-a-managed-code-form-template-that-requires-full-trust"></a>Konfigurieren einer Formularvorlage mit verwaltetem Code, die vollständig vertrauenswürdig sein muss

### <a name="set-your-forms-security-level-to-full-trust"></a>Festlegen der Sicherheitsebene "Voll vertrauenswürdig" für ein Formular

1. Öffnen Sie in InfoPath die Formularvorlage im Entwurfsmodus.
    
2. Klicken Sie auf die Registerkarte **Datei**, und klicken Sie dann auf der Registerkarte **Info** auf **Formularoptionen**. 
    
3. Klicken Sie in der Liste **Kategorie** auf **Sicherheit und Vertrauensstellung**.
    
4. Deaktivieren Sie im Bereich **Sicherheitsstufe** das Kontrollkästchen **Sicherheitsstufe automatisch ermitteln**.
    
5. Wählen Sie **Voll vertrauenswürdig** aus, und klicken Sie dann auf **OK**.
    
Nachdem dieses Verfahren ausgeführt wurde, können Sie Das Projekt wie unter Vorschau und Debuggen von [InfoPath-Formularvorlagen mit Code beschrieben debuggen.](how-to-preview-and-debug-infopath-form-templates-with-code.md)
  
> [!NOTE]
> Für die erfolgreiche Bereitstellung von Formularvorlagen mit verwaltetem Code, die vollständig vertrauenswürdig sein müssen, sind zusätzliche Schritte erforderlich, z. B. das digitale Signieren oder Installieren und Registrieren der Formularvorlage. Informationen zum Bereitstellen einer Formularvorlage für verwalteten Code nach dem Debuggen finden Sie unter [Deploy InfoPath Form Templates with Code](how-to-deploy-infopath-form-templates-with-code.md). 
  
## <a name="see-also"></a>Siehe auch



[Anzeigen und Debuggen von InfoPath-Formularvorlagen mit Code](how-to-preview-and-debug-infopath-form-templates-with-code.md)
  
[Bereitstellen von InfoPath-Formularvorlagen mit Code](how-to-deploy-infopath-form-templates-with-code.md)

