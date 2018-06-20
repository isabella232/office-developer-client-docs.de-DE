---
title: Bereitstellen von InfoPath-Formularvorlagen mit Code
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- Bereitstellen von Formularvorlagen [Infopath 2007] InfoPath 2007, Bereitstellen von Formularvorlagen, die Bereitstellung von .NET Framework-Sicherheitseinstellungen [InfoPath 2007], [InfoPath 2007]-Bereitstellung, Formularvorlagen Formularvorlagen [InfoPath 2007]
localization_priority: Normal
ms.assetid: ab66e26d-74ee-4211-b387-1385183a6803
description: Für eine InfoPath-Formularvorlage verwaltetem Code Formularcode wird als eine Assembly kompiliert, die unter der common Language Runtime (CLR) ausgeführt wird. Dies bedeutet, wenn Sie dem Formularcode ändern müssen, müssen Sie öffnen Sie das Projekt in Visual Studio 2012, ändern im Code-Editor, kompilieren Sie die Formularvorlage erneut, und klicken Sie dann erneut bereitstellen die Formularvorlage. Darüber hinaus, da die private Assembly für eine Formularvorlage verwalteten Code unter einem gehosteten CLR-Anwendungsdomäne ausgeführt wird, unterscheiden sich die Sicherheitseinstellungen für Formulare, die volle Vertrauenswürdigkeit erfordern von Formularvorlagen, die nicht volle Vertrauenswürdigkeit erfordern.
ms.openlocfilehash: 56af865a80df75c7e1d973767066a03310cdde1e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790735"
---
# <a name="deploy-infopath-form-templates-with-code"></a>Bereitstellen von InfoPath-Formularvorlagen mit Code

Für eine InfoPath-Formularvorlage verwaltetem Code Formularcode wird als eine Assembly kompiliert, die unter der common Language Runtime (CLR) ausgeführt wird. Dies bedeutet, wenn Sie dem Formularcode ändern müssen, müssen Sie öffnen Sie das Projekt in Visual Studio 2012, ändern im Code-Editor, kompilieren Sie die Formularvorlage erneut, und klicken Sie dann erneut bereitstellen die Formularvorlage. Darüber hinaus, da die private Assembly für eine Formularvorlage verwalteten Code unter einem gehosteten CLR-Anwendungsdomäne ausgeführt wird, unterscheiden sich die Sicherheitseinstellungen für Formulare, die volle Vertrauenswürdigkeit erfordern von Formularvorlagen, die nicht volle Vertrauenswürdigkeit erfordern.
  
## <a name="deploying-form-templates-that-do-not-require-full-trust"></a>Bereitstellen von Formularvorlagen, die nicht volle Vertrauenswürdigkeit erfordern

Wenn die Formularcode für die Formularvorlage wird nicht verwendet, InfoPath-Objektmodellmember, die volle Vertrauenswürdigkeit erfordern, und die Formularvorlage wird nicht verwendet, Features, die volle Vertrauenswürdigkeit erfordern, können Sie die Formularvorlage direkt in InfoPath mithilfe des folgenden Verfahrens veröffentlichen. Informationen zum Sicherheitsmodell von InfoPath finden Sie unter [Informationen zum Sicherheitsmodell für Formularvorlagen mit Code](about-the-security-model-for-form-templates-with-code.md).
  
### <a name="deploy-a-form-template-that-does-not-require-full-trust"></a>Bereitstellen einer Formularvorlage, die nicht volle Vertrauenswürdigkeit erfordert

1. Erstellen Sie und Debuggen Sie die Formularvorlage in Visual Studio 2012.
    
2. Wenn Sie im Code-Editor von Visual Studio 2012 arbeiten, wechseln Sie zu InfoPath, klicken Sie auf der Registerkarte **Datei** , und klicken Sie dann auf die Schaltfläche für den gewünschten Veröffentlichungsort auf der Registerkarte **Veröffentlichen** (Wenn Sie zuvor die Formularvorlage veröffentlicht haben, klicken Sie auf der **Datei** Registerkarte, und klicken Sie dann auf **Schnell veröffentlichen** , um die Formularvorlage an den gleichen Speicherort erneut.) 
    
    Die Formularvorlage wird kompiliert und der **Veröffentlichen-Assistent** wird gestartet. Führen Sie die Schritte im **Veröffentlichen-Assistenten** , um das Formular für den Speicherort Ihrer Wahl bereitzustellen. Weitere Informationen zur Verwendung des **Veröffentlichungs-Assistenten**suchen Sie InfoPath-Hilfe nach "Veröffentlichen einer Formularvorlage".
    
## <a name="deploying-form-templates-that-require-full-trust"></a>Bereitstellen von Formularvorlagen, die volle Vertrauenswürdigkeit erfordern

Wenn im Formularcode für die Formularvorlage InfoPath-Objektmodellmember verwendet werden, für die volle Vertrauenswürdigkeit erforderlich ist, oder wenn in der Formularvorlage Features verwendet werden, für die volle Vertrauenswürdigkeit erforderlich ist, müssen Sie die Formularvorlagendatei (XSN) digital mit einem Codesignierungszertifikat von einem vertrauenswürdigen Herausgeber signieren. Beim Öffnen des Formulars werden die Benutzer gefragt, ob sie diesen Herausgeber als vertrauenswürdig einstufen möchten. Damit wird auch das Formular voll vertrauenswürdig, und dem Formularcode wird der FullTrust-Berechtigungssatz zugewiesen.
  
### <a name="compile-publish-and-digitally-sign-a-form-template"></a>Kompilieren, Veröffentlichen und digitales Signieren einer Formularvorlage

1. Erstellen Sie und Debuggen Sie die Formularvorlage in Visual Studio 2012.
    
2. Wenn Sie im Code-Editor von Visual Studio 2012 arbeiten, wechseln Sie zu InfoPath, klicken Sie auf der Registerkarte **Datei** , und klicken Sie dann auf **Formularoptionen**.
    
3. Klicken Sie auf die Kategorie **Sicherheit und Vertrauensstellung** . 
    
4. Klicken Sie unter **Sicherheitsstufe**deaktivieren Sie das Kontrollkästchen **Sicherheitsstufe automatisch ermitteln** , und wählen Sie **Voll vertrauenswürdig**.
    
5. Klicken Sie unter **Signatur der Formularvorlage**wählen Sie **Diese Formularvorlage signieren**, klicken Sie auf **Zertifikat auswählen**, und geben Sie dann das Codesignierungszertifikat mit dem die Formularvorlage signiert.
    
6. Klicken Sie auf **OK** zweimal ein, um das Dialogfeld **Formularoptionen** zu schließen, und klicken Sie dann speichern Sie Ihre Änderungen zu. 
    
7. Klicken Sie auf der Registerkarte **Veröffentlichen** , und klicken Sie dann auf die Schaltfläche für den gewünschten Veröffentlichungsort. 
    
8. Die Formularvorlage wird kompiliert und der **Veröffentlichen-Assistent** wird gestartet. Führen Sie die Schritte des **Veröffentlichen-Assistenten** zum Bereitstellen der Formularvorlage ein. Weitere Informationen zur Verwendung Suchen des **Veröffentlichungs-Assistenten** zum Bereitstellen einer Formularvorlage, die volle Vertrauenswürdigkeit erfordert InfoPath-Hilfe nach "Veröffentlichen einer Formularvorlage mit vollständiger Vertrauenswürdigkeit". 
    
 **Anmerkungen**
- Zum digitalen Signieren eines Formulars muss ein authentifiziertes Codesignierungszertifikat auf dem Computer installiert sein. Wenden Sie sich an eine Zertifizierungsstelle oder den Netzwerkadministrator, um ein solches Zertifikat zu erhalten.
    
- Wenn Sie das Formular nach dem Veröffentlichen ändern müssen, müssen Sie wiederholen Sie das Verfahren und die Formularvorlage signiert. Dies ist, da das Formular ändern die digitale Signatur ungültig wird. Das in der [Vorschau und Debuggen von Formularvorlagen, erfordern volle Vertrauenswürdigkeit](how-to-preview-and-debug-form-templates-that-require-full-trust.md) beschriebene Verfahren können Sie während der Entwicklung eines Formulars, das volle Vertrauenswürdigkeit erfordert um die Formularvorlage auf dem lokalen Computer zu registrieren. 
    
## <a name="configuring-net-framework-security-settings"></a>Konfigurieren der .NET Framework-Sicherheitseinstellungen

Zur besseren Steuerung der Berechtigungen, die dem in einer InfoPath-Formularvorlage mit verwaltetem Code ausgeführten verwalteten Code erteilt werden, können Sie das Hilfsprogramm .NET Framework 2.0-Konfiguration verwenden, um dem Formularcode einen bestimmten Berechtigungssatz zuzuweisen.
  
> [!IMPORTANT]
> Das Konfigurieren der .NET Framework-Sicherheitseinstellungen für eine InfoPath-Formularvorlage mit verwaltetem Code wirkt sich nicht darauf aus, ob InfoPath-Objektmodellmember, die volle Vertrauenswürdigkeit erfordern, ausgeführt werden dürfen. Sie müssen eine Formularvorlage entsprechend der Beschreibung weiter oben in diesem Thema entweder digital signieren oder registrieren, um Aufrufe der InfoPath-Objektmodellmember zu ermöglichen, die volle Vertrauenswürdigkeit erfordern. Die .NET Framework-Sicherheitseinstellungen gelten nur für Aufrufe von Membern von .NET Framework-Klassen und anderen verwalteten Komponenten als dem InfoPath-Objektmodell. 
  
### <a name="compile-publish-and-configure-net-security-settings-for-a-form-template"></a>Kompilieren, Veröffentlichen und Konfigurieren der .NET-Sicherheitseinstellungen für eine Formularvorlage

1. Erstellen Sie und Debuggen Sie die Formularvorlage in Visual Studio 2012.
    
2. Wenn Sie im Code-Editor von Visual Studio 2012 arbeiten, wechseln Sie zu InfoPath, klicken Sie auf der Registerkarte **Datei** , klicken Sie auf **Veröffentlichen**, und klicken Sie dann auf die Schaltfläche für den gewünschten Veröffentlichungsort.
    
    Die Formularvorlage wird kompiliert und der **Veröffentlichen-Assistent** wird gestartet. Führen Sie die Schritte des **Veröffentlichen-Assistenten** zum Bereitstellen der Formularvorlage ein. Weitere Informationen zur Verwendung des **Veröffentlichungs-Assistenten**suchen Sie InfoPath-Hilfe nach "Veröffentlichen einer Formularvorlage".
    
3. Führen Sie die Schritte beschrieben, die im Abschnitt "Zuweisen von"voll vertrauenswürdig "an Formulare unter einer bestimmten URL oder UNC" [Konfigurieren von Sicherheitseinstellungen für Formularvorlagen mit Code](how-to-configure-security-settings-for-form-templates-with-code.md)
    
## <a name="see-also"></a>Siehe auch

#### <a name="tasks"></a>Aufgaben

[Konfigurieren von Sicherheitseinstellungen für Formularvorlagen mit Code](how-to-configure-security-settings-for-form-templates-with-code.md)


[Informationen zum Sicherheitsmodell für Formularvorlagen mit Code](about-the-security-model-for-form-templates-with-code.md)
  
[Anzeigen der Vorschau und Debuggen von Formularvorlagen, die volle Vertrauenswürdigkeit erfordern](how-to-preview-and-debug-form-templates-that-require-full-trust.md)

