---
title: Problembehandlung bei Formularvorlagen, die das InfoPath-Objektmodell zur Laufzeit verwenden
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- Problembehandlung bei Formularvorlagen [InfoPath 2007], Laufzeit, InfoPath 2003-kompatible Formularvorlagen, Problembehandlung zur Laufzeit
localization_priority: Normal
ms.assetid: 65e7882e-6397-4375-9bb4-d993d700d749
description: In den folgenden Abschnitten werden häufige Problembehandlungsszenarien beschrieben, die beim Arbeiten mit InfoPath-Formularvorlagen mit verwaltetem Code auftreten können, die das InfoPath 2003-kompatible Objektmodell verwenden, das von Microsoft. Office. Interop. InfoPath. SemiTrust bereitgestellt wird. Namespace zur Laufzeit.
ms.openlocfilehash: c7b4b65cc722e72ef155529a0b2aa66c4f6cfcff
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299797"
---
# <a name="troubleshoot-form-templates-that-use-the-infopath-object-model-at-run-time"></a>Problembehandlung bei Formularvorlagen, die das InfoPath-Objektmodell zur Laufzeit verwenden

In den folgenden Abschnitten werden häufige Problembehandlungsszenarien beschrieben, die beim Arbeiten mit InfoPath-Formularvorlagen mit verwaltetem Code auftreten können, die das InfoPath 2003-kompatible Objektmodell verwenden, das von der ** Microsoft. Office. Interop. InfoPath. SemiTrust** -Namespace zur Laufzeit. 
  
## <a name="display-notifications-for-unhandled-managed-code-exceptions-at-run-time"></a>Anzeigen von Benachrichtigungen für unbehandelte Ausnahmen mit verwaltetem Code zur Laufzeit

Wenn Sie im Formularcode keine try-catch-Ausnahmebehandlung verwenden, zeigt InfoPath beim Debuggen und Anzeigen der Vorschau Informationen zu unbehandelten Ausnahmen im Dialogfeld für InfoPath-Fehler an. Allerdings werden unbehandelte Ausnahmen im Dialogfeld für InfoPath-Fehler zur Laufzeit standardmäßig nicht angezeigt, wenn Sie eine Formularvorlage mit verwaltetem Code bereitstellen. Wenn Ausnahmen mit verwaltetem Code zur Laufzeit angezeigt werden sollen, führen Sie die Schritte im Abschnitt "behandeln von Ausnahmen mit verwaltetem Code" von " [fehlerBehandlung mit dem InfoPath 2003-Objektmodell](how-to-handle-errors-using-the-infopath-2003-object-model.md)" aus.
  
## <a name="problems-with-managed-code-form-templates-after-deployment"></a>Probleme mit Formularvorlagen mit verwaltetem Code nach der Bereitstellung

Vergessen Sie nicht, die Formularvorlage mit verwaltetem Code an dem Ort zu testen, an dem sie bereitgestellt werden soll. Informationen zu Bereitstellungsverfahren finden Sie unter [Bereitstellen von InfoPath-Formularvorlagen mit Code](how-to-deploy-infopath-form-templates-with-code.md). Informationen zu Sicherheitsszenarien, die sich auf die Bereitstellung auswirken, finden Sie unter Informationen zum [Sicherheitsmodell für Formularvorlagen mit Code](about-the-security-model-for-form-templates-with-code.md).
  
Wenn Sie das .NET Framework 1,1-Konfigurationsdienstprogramm und die Codegruppe InfoPath-Formularvorlagen verwenden, um bestimmte Berechtigungen für eine Formularvorlage mit verwaltetem Code hinzuzufügen, stellen Sie sicher, dass auf allen Clientcomputern dieselbe Sicherheitsrichtlinie bereitgestellt wird. Wenn Sie **URLEvidence** angeben, das auf einen Speicherort auf dem lokalen Computer verweist, stellen Sie außerdem sicher, dass der angegebene Speicherort auf den Ordner verweist, in dem die Lösung schließlich bereitgestellt wird (nicht derselbe Speicherort, der während der Entwicklung verwendet wird). Informationen zum Konfigurieren von .NET Framework-Sicherheitseinstellungen für eine Formularvorlage mit verwaltetem Code finden Sie unter "Zuweisen von FullTrust zu Formularen unter einer bestimmten URL oder UNC" im Thema [Konfigurieren von Sicherheitseinstellungen für Formularvorlagen mit Code](how-to-configure-security-settings-for-form-templates-with-code.md) . 
  
## <a name="see-also"></a>Siehe auch

- [Informationen zum Sicherheitsmodell für Formularvorlagen mit Code](about-the-security-model-for-form-templates-with-code.md)
- [Bereitstellen von InfoPath-Formularvorlagen mit Code](how-to-deploy-infopath-form-templates-with-code.md)
- [Behandeln von Fehlern mithilfe des InfoPath-2003-Objektmodells](how-to-handle-errors-using-the-infopath-2003-object-model.md)
- [Debuggen von InfoPath-Projekten mit dem InfoPath-2003-Objektmodell](how-to-debug-infopath-projects-using-the-infopath-2003-object-model.md)

