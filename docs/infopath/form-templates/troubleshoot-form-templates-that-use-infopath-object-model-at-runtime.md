---
title: Problembehandlung von Formularvorlagen, die das InfoPath-Objektmodell zur Laufzeit verwenden
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- Formularvorlagen [Infopath 2007] führen Sie Zeit bei der Problembehandlung, Laufzeit InfoPath 2003-kompatible Formularvorlagen, Problembehandlung zur
localization_priority: Normal
ms.assetid: 65e7882e-6397-4375-9bb4-d993d700d749
description: Die folgenden Abschnitte beschreiben allgemeine Problembehandlungsszenarien, die beim Arbeiten mit verwaltetem Code Formular InfoPath-Formularvorlagen, die durch die Microsoft.Office.Interop.InfoPath.SemiTrust bereitgestellte InfoPath 2003-kompatible Objektmodell verwenden auftreten können Namespace zur Laufzeit.
ms.openlocfilehash: 8c83679a0cd61fae212b3143b6b0131da92ac7f9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790845"
---
# <a name="troubleshoot-form-templates-that-use-the-infopath-object-model-at-run-time"></a>Problembehandlung von Formularvorlagen, die das InfoPath-Objektmodell zur Laufzeit verwenden

Die folgenden Abschnitte beschreiben allgemeine Problembehandlungsszenarien, die beim Arbeiten mit verwaltetem Code Formular InfoPath-Formularvorlagen, die durch die **bereitgestellte InfoPath 2003-kompatible Objektmodell verwenden auftreten können Microsoft.Office.Interop.InfoPath.SemiTrust** Namespace zur Laufzeit. 
  
## <a name="display-notifications-for-unhandled-managed-code-exceptions-at-run-time"></a>Anzeigen von Benachrichtigungen für nicht behandelte Ausnahmen im verwalteten Code zur Laufzeit

Wenn Sie im Formularcode keine try-catch-Ausnahmebehandlung verwenden, zeigt InfoPath beim Debuggen und Anzeigen der Vorschau Informationen zu unbehandelten Ausnahmen im Dialogfeld für InfoPath-Fehler an.  Allerdings werden standardmäßig nicht behandelte Ausnahmen nicht im Dialogfeld InfoPath-Fehler während der Laufzeit angezeigt bei der Bereitstellung von Formularvorlage mit verwaltetem Code. Wenn Ausnahmen im verwalteten Code zur Laufzeit angezeigt werden soll, führen Sie das Verfahren im Abschnitt "Behandeln von verwaltetem Code Exceptions" [Behandeln Fehler mithilfe des InfoPath 2003-Objektmodells](how-to-handle-errors-using-the-infopath-2003-object-model.md).
  
## <a name="problems-with-managed-code-form-templates-after-deployment"></a>Probleme mit Formularvorlagen mit verwaltetem Code nach der Bereitstellung

Achten Sie darauf, dass Sie in den Speicherort die Formularvorlage mit verwaltetem Code testen, in dem sie schließlich bereitgestellt wird. Informationen zu Bereitstellungsverfahren finden Sie unter [Bereitstellen von InfoPath-Formularvorlagen mit Code](how-to-deploy-infopath-form-templates-with-code.md). Informationen zu Sicherheitsszenarien, die sich auf Bereitstellung auswirken, finden Sie unter [Informationen zum Sicherheitsmodell für Formularvorlagen mit Code](about-the-security-model-for-form-templates-with-code.md).
  
Wenn Sie das Konfigurationsprogramm für .NET Framework 1.1 und die Codegruppe InfoPath-Formularvorlagen zum Hinzufügen von bestimmter Berechtigungen für eine Formularvorlage mit verwaltetem Code verwenden, stellen Sie sicher, dass die gleichen Codezugriffssicherheits-Richtlinie auf allen Clientcomputern bereitgestellt wird. Wenn Sie **URLEvidence** , die an einem Speicherort auf dem lokalen Computer verweist angeben, stellen Sie außerdem sicher, dass die angegebene Position auf den Ordner verweist, in dem die Lösung werden, schließlich (nicht den gleichen Speicherort während der Entwicklung) bereitgestellt. Informationen zum Konfigurieren von .NET Framework-Sicherheitseinstellungen für eine Formularvorlage mit verwaltetem Code finden Sie im Abschnitt "Zuweisen von"voll vertrauenswürdig "an Formulare unter einer bestimmten URL oder UNC" im Thema [Konfigurieren von Sicherheitseinstellungen für Formularvorlagen mit Code](how-to-configure-security-settings-for-form-templates-with-code.md) . 
  
## <a name="see-also"></a>Siehe auch

- [Informationen zum Sicherheitsmodell für Formularvorlagen mit Code](about-the-security-model-for-form-templates-with-code.md)
- [Bereitstellen von InfoPath-Formularvorlagen mit Code](how-to-deploy-infopath-form-templates-with-code.md)
- [Behandeln von Fehlern mit dem InfoPath 2003-Objektmodell](how-to-handle-errors-using-the-infopath-2003-object-model.md)
- [Debuggen von InfoPath-Projekten mit dem InfoPath 2003-Objektmodell](how-to-debug-infopath-projects-using-the-infopath-2003-object-model.md)

