---
title: Anzeigen der Vorschau und Debuggen von Formularvorlagen, die volle Vertrauenswürdigkeit erfordern
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- debugging [infopath 2007], infopath 2003-kompatible Formularvorlagen, Vorschau von InfoPath 2003-kompatiblen Formularvorlagen,Formularvorlagen [InfoPath 2007], Vorschau auf 2003-kompatible,Formularvorlagen [InfoPath 2007], Debuggen 2003-kompatibel,Debuggen von InfoPath 2003-kompatiblen Formularvorlagen
ms.localizationpriority: medium
ms.assetid: 5c491666-06f0-42ec-967e-1c70cd5e03a0
description: Wenn Sie versuchen, ein Projekt mit verwaltetem Code zu debuggen oder eine Vorschau anzuzeigen, das Code enthält, der ein Objektmodellmitglied aufruft, das volle Vertrauenswürdigkeit erfordert, z. B. die LoginName-Eigenschaft, die Zugriff auf Informationen über die Anmeldedomäne des Benutzers erfordert, zeigt Microsoft InfoPath standardmäßig die folgenden Fehlermeldungen an.
ms.openlocfilehash: 8fef3f0fceb1c9637cc4fbeb59bc8d716db442d2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59605568"
---
# <a name="preview-and-debug-form-templates-that-require-full-trust"></a>Anzeigen der Vorschau und Debuggen von Formularvorlagen, die volle Vertrauenswürdigkeit erfordern

Wenn Sie versuchen, ein Projekt mit verwaltetem Code zu debuggen oder eine Vorschau anzuzeigen, das Code enthält, der ein Objektmodellmitglied aufruft, das volle Vertrauenswürdigkeit erfordert, z. B. die **LoginName-Eigenschaft,** die Zugriff auf Informationen über die Anmeldedomäne des Benutzers erfordert, zeigt Microsoft InfoPath standardmäßig die folgenden Fehlermeldungen an. 
  
Beim Anzeigen der Vorschau:
  
"Eine unbekannte Ausnahme ist im Formularcode aufgetreten." Gefolgt von: "Fehler im Formularcode beim Abschließen dieser Aktion von InfoPath."
  
Beim Debuggen:
  
Der Fokus wird auf die Codezeile im Code-Editor verschoben, die das Element aufruft, das volle Vertrauenswürdigkeit erfordert, und die folgende Meldung wird angezeigt: **"SecurityException** wurde vom Benutzercode nicht behandelt – Anforderung fehlgeschlagen". 
  
Sie müssen für die Sicherheitsebene der Formularvorlage **Voll vertrauenswürdig** festlegen, wie im folgenden Verfahren beschrieben, um das Aufrufen dieses Members beim Debuggen oder Anzeigen einer Vorschau durch die Geschäftslogik der Formularvorlage zuzulassen. 
  
## <a name="configuring-a-managed-code-form-template-that-requires-full-trust"></a>Konfigurieren einer Formularvorlage mit verwaltetem Code, die vollständig vertrauenswürdig sein muss

### <a name="set-your-forms-security-level-to-full-trust"></a>Festlegen der Sicherheitsebene "Voll vertrauenswürdig" für ein Formular

1. Öffnen Sie in InfoPath die Formularvorlage im Entwurfsmodus.
    
2. Klicken Sie auf die Registerkarte **Datei**, und klicken Sie dann auf der Registerkarte **Info** auf **Formularoptionen**. 
    
3. Klicken Sie in der Liste **Kategorie** auf **Sicherheit und Vertrauensstellung**.
    
4. Deaktivieren Sie im Bereich **Sicherheitsstufe** das Kontrollkästchen **Sicherheitsstufe automatisch ermitteln**.
    
5. Wählen Sie **Voll vertrauenswürdig** aus, und klicken Sie dann auf **OK**.
    
Nachdem dieses Verfahren ausgeführt wurde, können Sie das Projekt wie unter Vorschau und Debuggen von [InfoPath-Formularvorlagen mit Code](how-to-preview-and-debug-infopath-form-templates-with-code.md)beschrieben debuggen.
  
> [!NOTE]
> Für die erfolgreiche Bereitstellung von Formularvorlagen mit verwaltetem Code, die vollständig vertrauenswürdig sein müssen, sind zusätzliche Schritte erforderlich, z. B. das digitale Signieren oder Installieren und Registrieren der Formularvorlage. Informationen zum Bereitstellen einer Formularvorlage mit verwaltetem Code nach dem Debuggen finden Sie unter [Bereitstellen von InfoPath-Formularvorlagen mit Code.](how-to-deploy-infopath-form-templates-with-code.md) 
  
## <a name="see-also"></a>Siehe auch



[Anzeigen und Debuggen von InfoPath-Formularvorlagen mit Code](how-to-preview-and-debug-infopath-form-templates-with-code.md)
  
[Bereitstellen von InfoPath-Formularvorlagen mit Code](how-to-deploy-infopath-form-templates-with-code.md)

