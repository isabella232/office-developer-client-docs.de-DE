---
title: Problembehandlung bei Formularvorlagen, die das InfoPath-Objektmodell zur Laufzeit verwenden
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- Problembehandlung bei Formularvorlagen [infopath 2007], Laufzeit,InfoPath 2003-kompatible Formularvorlagen, Problembehandlung zur Laufzeit
localization_priority: Normal
ms.assetid: 65e7882e-6397-4375-9bb4-d993d700d749
description: In den folgenden Abschnitten werden allgemeine Problembehandlungsszenarien beschrieben, die beim Arbeiten mit InfoPath-Formularvorlagen mit verwalteten Code auftreten können, die das infoPath 2003-kompatible Objektmodell verwenden, das von Microsoft bereitgestellt wird. Office.Interop.InfoPath.SemiTrust-Namespace zur Laufzeit.
ms.openlocfilehash: c7b4b65cc722e72ef155529a0b2aa66c4f6cfcff
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414445"
---
# <a name="troubleshoot-form-templates-that-use-the-infopath-object-model-at-run-time"></a>Problembehandlung bei Formularvorlagen, die das InfoPath-Objektmodell zur Laufzeit verwenden

In den folgenden Abschnitten werden allgemeine Problembehandlungsszenarien beschrieben, die beim Arbeiten mit InfoPath-Formularvorlagen mit verwalteten Code auftreten können, die das InfoPath 2003-kompatible Objektmodell verwenden, das vom **Microsoft.Office.Interop.InfoPath.SemiTrust-Namespace** zur Laufzeit bereitgestellt wird. 
  
## <a name="display-notifications-for-unhandled-managed-code-exceptions-at-run-time"></a>Anzeigen von Benachrichtigungen für nicht behandelte Ausnahmen mit verwalteten Code zur Laufzeit

Wenn Sie im Formularcode keine try-catch-Ausnahmebehandlung verwenden, zeigt InfoPath beim Debuggen und Anzeigen der Vorschau Informationen zu unbehandelten Ausnahmen im Dialogfeld für InfoPath-Fehler an. Allerdings werden unbehandelte Ausnahmen im Dialogfeld für InfoPath-Fehler zur Laufzeit standardmäßig nicht angezeigt, wenn Sie eine Formularvorlage mit verwaltetem Code bereitstellen. Wenn Zur Laufzeit Ausnahmen mit verwalteten Code angezeigt werden sollen, führen Sie das Verfahren im Abschnitt "Behandeln von Ausnahmen für verwalteten Code" unter Behandeln von Fehlern mithilfe des [InfoPath 2003-Objektmodells aus.](how-to-handle-errors-using-the-infopath-2003-object-model.md)
  
## <a name="problems-with-managed-code-form-templates-after-deployment"></a>Probleme mit Formularvorlagen mit verwalteten Code nach der Bereitstellung

Vergessen Sie nicht, die Formularvorlage mit verwaltetem Code an dem Ort zu testen, an dem sie bereitgestellt werden soll. Informationen zu Bereitstellungsverfahren finden Sie unter [Deploy InfoPath Form Templates with Code](how-to-deploy-infopath-form-templates-with-code.md). Informationen zu Sicherheitsszenarien, die sich auf die Bereitstellung auswirken, finden Sie unter Informationen zum [Sicherheitsmodell für Formularvorlagen mit Code](about-the-security-model-for-form-templates-with-code.md).
  
Wenn Sie das .NET Framework 1.1-Konfigurationsprogramm und die Codegruppe InfoPath-Formularvorlagen verwenden, um bestimmte Berechtigungen für eine Formularvorlage mit verwalteten Code hinzuzufügen, stellen Sie sicher, dass dieselbe Sicherheitsrichtlinie auf allen Clientcomputern bereitgestellt wird. Wenn Sie außerdem **URLEvidence** angeben, die sich auf einen Speicherort auf dem lokalen Computer bezieht, stellen Sie sicher, dass sich der angegebene Speicherort auf den Ordner bezieht, in dem die Lösung schließlich bereitgestellt wird (nicht der gleiche Speicherort, der während der Entwicklung verwendet wird). Informationen zum Konfigurieren .NET Framework Sicherheitseinstellungen für eine Formularvorlage mit verwalteten Code finden Sie im Abschnitt "Zuweisen von Vollvertrauenswürdigkeit zu Formularen unter einer bestimmten URL oder UNC" im Thema [Configure Security Einstellungen for Form Templates with Code.](how-to-configure-security-settings-for-form-templates-with-code.md) 
  
## <a name="see-also"></a>Siehe auch

- [Informationen zum Sicherheitsmodell für Formularvorlagen mit Code](about-the-security-model-for-form-templates-with-code.md)
- [Bereitstellen von InfoPath-Formularvorlagen mit Code](how-to-deploy-infopath-form-templates-with-code.md)
- [Behandeln von Fehlern mithilfe des InfoPath 2003-Objektmodells](how-to-handle-errors-using-the-infopath-2003-object-model.md)
- [Debuggen von InfoPath-Projekten mithilfe des InfoPath 2003-Objektmodells](how-to-debug-infopath-projects-using-the-infopath-2003-object-model.md)

