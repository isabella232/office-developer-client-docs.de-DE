---
title: Bereitstellen von InfoPath-Formularvorlagen mit Code
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- Bereitstellen von Formularvorlagen [infopath 2007],InfoPath 2007, Bereitstellen von Formularvorlagen,Formularvorlagen [InfoPath 2007], Bereitstellen,.NET Framework Sicherheitseinstellungen [InfoPath 2007],Bereitstellung [InfoPath 2007], Formularvorlagen
localization_priority: Normal
ms.assetid: ab66e26d-74ee-4211-b387-1385183a6803
description: Der Formularcode für eine InfoPath-Formularvorlage mit verwaltetem Code wird als Assembly kompiliert, die unter der Common Language Runtime (CLR) ausgeführt wird. Dies bedeutet, dass Sie jedes Mal, wenn Sie Änderungen am Formularcode vornehmen müssen, das Projekt in Visual Studio 2012 öffnen, Änderungen im Code-Editor vornehmen, die Formularvorlage neu kompilieren und dann die Formularvorlage erneut bereitstellen müssen. Da die private Assembly für eine Formularvorlage mit verwaltetem Code unter einer gehosteten CLR-Anwendungsdomäne ausgeführt wird, unterscheiden sich die Sicherheitseinstellungen für Formulare, die volle Vertrauenswürdigkeit erfordern, geringfügig von Formularvorlagen, für die keine volle Vertrauenswürdigkeit erforderlich ist.
ms.openlocfilehash: ba3629e786a224ea950e78bbec9a9fe94d4499de
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406899"
---
# <a name="deploy-infopath-form-templates-with-code"></a>Bereitstellen von InfoPath-Formularvorlagen mit Code

Der Formularcode für eine InfoPath-Formularvorlage mit verwaltetem Code wird als Assembly kompiliert, die unter der Common Language Runtime (CLR) ausgeführt wird. Dies bedeutet, dass Sie jedes Mal, wenn Sie Änderungen am Formularcode vornehmen müssen, das Projekt in Visual Studio 2012 öffnen, Änderungen im Code-Editor vornehmen, die Formularvorlage neu kompilieren und dann die Formularvorlage erneut bereitstellen müssen. Da die private Assembly für eine Formularvorlage mit verwaltetem Code unter einer gehosteten CLR-Anwendungsdomäne ausgeführt wird, unterscheiden sich die Sicherheitseinstellungen für Formulare, die volle Vertrauenswürdigkeit erfordern, geringfügig von Formularvorlagen, für die keine volle Vertrauenswürdigkeit erforderlich ist.
  
## <a name="deploying-form-templates-that-do-not-require-full-trust"></a>Bereitstellen von Formularvorlagen, die nicht volle Vertrauenswürdigkeit erfordern

Wenn im Formularcode für eine Formularvorlage keine InfoPath-Objektmodellmember verwendet werden, für die volle Vertrauenswürdigkeit erforderlich ist, und in der Formularvorlage keine Features verwendet werden, für die volle Vertrauenswürdigkeit erforderlich ist, können Sie die Formularvorlage direkt aus InfoPath heraus mit dem folgenden Verfahren veröffentlichen. Informationen zum InfoPath-Sicherheitsmodell finden Sie unter [Informationen zum Sicherheitsmodell für Formularvorlagen mit Code](about-the-security-model-for-form-templates-with-code.md).
  
### <a name="deploy-a-form-template-that-does-not-require-full-trust"></a>Bereitstellen einer Formularvorlage, die nicht volle Vertrauenswürdigkeit erfordert

1. Erstellen und Debuggen Der Formularvorlage in Visual Studio 2012.
    
2. Wenn Sie im Visual Studio 2012-Code-Editor arbeiten, wechseln Sie  zu InfoPath, klicken Sie auf die Registerkarte Datei, und klicken Sie dann auf der Registerkarte  Veröffentlichen auf die Schaltfläche  für den gewünschten Veröffentlichungsspeicherort. (Wenn Sie die Formularvorlage zuvor veröffentlicht haben, können Sie auf die Registerkarte Datei klicken und dann auf Schnell veröffentlichen klicken, um die Formularvorlage erneut an demselben Speicherort zu veröffentlichen.)  
    
    Die Formularvorlage wird kompiliert und der Veröffentlichungs-Assistent gestartet. Folgen Sie den Schritten im Veröffentlichungs-Assistenten, um das Formular am gewünschten Speicherort bereitzustellen. Weitere Informationen zum Verwenden des Veröffentlichungs-Assistenten finden Sie in der InfoPath-Hilfe unter dem Suchbegriff "Veröffentlichen einer Formularvorlage".
    
## <a name="deploying-form-templates-that-require-full-trust"></a>Bereitstellen von Formularvorlagen, die volle Vertrauenswürdigkeit erfordern

Wenn im Formularcode für die Formularvorlage InfoPath-Objektmodellmember verwendet werden, für die volle Vertrauenswürdigkeit erforderlich ist, oder wenn in der Formularvorlage Features verwendet werden, für die volle Vertrauenswürdigkeit erforderlich ist, müssen Sie die Formularvorlagendatei (XSN) digital mit einem Codesignierungszertifikat von einem vertrauenswürdigen Herausgeber signieren. Beim Öffnen des Formulars werden die Benutzer gefragt, ob sie diesen Herausgeber als vertrauenswürdig einstufen möchten. Damit wird auch das Formular voll vertrauenswürdig, und dem Formularcode wird der FullTrust-Berechtigungssatz zugewiesen.
  
### <a name="compile-publish-and-digitally-sign-a-form-template"></a>Kompilieren, Veröffentlichen und digitales Signieren einer Formularvorlage

1. Erstellen und Debuggen Der Formularvorlage in Visual Studio 2012.
    
2. Wenn Sie im Visual Studio 2012-Code-Editor arbeiten, wechseln Sie  zu InfoPath, klicken Sie auf die Registerkarte Datei, und klicken Sie dann auf **Formularoptionen**.
    
3. Klicken Sie auf die Kategorie **Sicherheit und Vertrauensstellung**. 
    
4. Deaktivieren Sie unter **Sicherheitsstufe** das Kontrollkästchen **Sicherheitsstufe automatisch ermitteln**, und wählen Sie dann **Voll vertrauenswürdig** aus.
    
5. Aktivieren Sie unter **Signatur der Formularvorlage** das Kontrollkästchen **Diese Formularvorlage signieren**, klicken Sie auf **Zertifikat auswählen**, und geben Sie dann das Codesignierungszertifikat an, mit dem die Formularvorlage signiert werden soll.
    
6. Klicken Sie zweimal auf **OK**, um das Dialogfeld **Formularoptionen** zu schließen, und speichern Sie dann die Änderungen. 
    
7. Klicken Sie auf die Registerkarte **Veröffentlichen** und dann auf die Schaltfläche für den gewünschten Veröffentlichungsort. 
    
8. Die Formularvorlage wird kompiliert und derVeröffentlichungs-Assistent gestartet. Befolgen Sie die Schritte imVeröffentlichungs-Assistenten, um die Formularvorlage bereitzustellen. Weitere Informationen zum Verwenden desVeröffentlichungs-Assistenten zum Bereitstellen einer Formularvorlage, die volle Vertrauenswürdigkeit erfordert, finden Sie in der InfoPath-Hilfe unter dem Suchbegriff "Veröffentlichen einer Formularvorlage mit voller Vertrauenswürdigkeit". 
    
 **Notizen**
- Zum digitalen Signieren eines Formulars muss ein authentifiziertes Codesignierungszertifikat auf dem Computer installiert sein. Wenden Sie sich an eine Zertifizierungsstelle oder den Netzwerkadministrator, um ein solches Zertifikat zu erhalten.
    
- Wenn nach dem Veröffentlichen des Formulars Änderungen daran erforderlich sind, müssen Sie das Verfahren wiederholen und die Formularvorlage erneut signieren. Durch eine Änderung des Formulars wird die digitale Signatur ungültig. Während der Entwicklung eines Formulars, das voll vertrauenswürdige Berechtigungen erfordert, können Sie das unter Vorschau und [Debuggen](how-to-preview-and-debug-form-templates-that-require-full-trust.md) von Formularvorlagen beschriebene Verfahren verwenden, für das eine vollständige Vertrauenswürdigkeit erforderlich ist, um die Formularvorlage auf dem lokalen Computer zu registrieren. 
    
## <a name="configuring-net-framework-security-settings"></a>Konfigurieren der .NET Framework-Sicherheitseinstellungen

Zur besseren Steuerung der Berechtigungen, die dem in einer InfoPath-Formularvorlage mit verwaltetem Code ausgeführten verwalteten Code erteilt werden, können Sie das Hilfsprogramm .NET Framework 2.0-Konfiguration verwenden, um dem Formularcode einen bestimmten Berechtigungssatz zuzuweisen.
  
> [!IMPORTANT]
> Das Konfigurieren der .NET Framework-Sicherheitseinstellungen für eine InfoPath-Formularvorlage mit verwaltetem Code wirkt sich nicht darauf aus, ob InfoPath-Objektmodellmember, die volle Vertrauenswürdigkeit erfordern, ausgeführt werden dürfen. Sie müssen eine Formularvorlage entsprechend der Beschreibung weiter oben in diesem Thema entweder digital signieren oder registrieren, um Aufrufe der InfoPath-Objektmodellmember zu ermöglichen, die volle Vertrauenswürdigkeit erfordern. Die .NET Framework-Sicherheitseinstellungen gelten nur für Aufrufe von Membern von .NET Framework-Klassen und anderen verwalteten Komponenten als dem InfoPath-Objektmodell. 
  
### <a name="compile-publish-and-configure-net-security-settings-for-a-form-template"></a>Kompilieren, Veröffentlichen und Konfigurieren der .NET-Sicherheitseinstellungen für eine Formularvorlage

1. Erstellen und Debuggen Der Formularvorlage in Visual Studio 2012.
    
2. Wenn Sie im Visual Studio 2012-Code-Editor arbeiten, wechseln Sie  zu InfoPath, klicken Sie auf die Registerkarte Datei, klicken Sie auf **Veröffentlichen,** und klicken Sie dann auf die Schaltfläche für den gewünschten Veröffentlichungsspeicherort.
    
    Die Formularvorlage wird kompiliert und derVeröffentlichungs-Assistent gestartet. Befolgen Sie die Schritte imVeröffentlichungs-Assistenten, um die Formularvorlage bereitzustellen. Weitere Informationen zum Verwenden desVeröffentlichungs-Assistenten finden Sie in der InfoPath-Hilfe unter dem Suchbegriff "Veröffentlichen einer Formularvorlage".
    
3. Führen Sie das im Abschnitt "Zuweisen von FullTrust zu Formularen unter einer bestimmten URL oder UNC" des Abschnitts Configure Security Einstellungen for Form Templates with Code beschriebene [Verfahren aus.](how-to-configure-security-settings-for-form-templates-with-code.md)
    
## <a name="see-also"></a>Siehe auch

#### <a name="tasks"></a>Aufgaben

[Konfigurieren von Einstellungen für Formularvorlagen mit Code](how-to-configure-security-settings-for-form-templates-with-code.md)


[Informationen zum Sicherheitsmodell für Formularvorlagen mit Code](about-the-security-model-for-form-templates-with-code.md)
  
[Anzeigen einer Vorschau und Debuggen von Formularvorlagen, die vollständig vertrauenswürdig sein müssen](how-to-preview-and-debug-form-templates-that-require-full-trust.md)

