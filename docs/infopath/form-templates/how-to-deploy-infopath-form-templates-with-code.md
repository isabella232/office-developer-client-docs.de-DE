---
title: Bereitstellen von InfoPath-Formularvorlagen mit Code
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- Bereitstellen von Formularvorlagen [InfoPath 2007], InfoPath 2007, Bereitstellen von Formularvorlagen, Formularvorlagen [InfoPath 2007], Deploying,. NET Framework-Sicherheitseinstellungen [InfoPath 2007], Bereitstellung [InfoPath 2007], Formularvorlagen
localization_priority: Normal
ms.assetid: ab66e26d-74ee-4211-b387-1385183a6803
description: Der Formularcode für eine InfoPath-Formularvorlage mit verwaltetem Code wird als Assembly kompiliert, die unter der Common Language Runtime (CLR) ausgeführt wird. Wenn Sie also Änderungen am Formularcode vornehmen müssen, müssen Sie das Projekt in Visual Studio 2012 öffnen, Änderungen im Code-Editor vornehmen, die Formularvorlage neu kompilieren und dann die Formularvorlage erneut bereitstellen. Da die private Assembly für eine Formularvorlage mit verwaltetem Code unter einer gehosteten CLR-Anwendungsdomäne ausgeführt wird, unterscheiden sich die Sicherheitseinstellungen für Formulare, die volle Vertrauenswürdigkeit erfordern, geringfügig von Formularvorlagen, für die keine volle Vertrauenswürdigkeit erforderlich ist.
ms.openlocfilehash: ba3629e786a224ea950e78bbec9a9fe94d4499de
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303626"
---
# <a name="deploy-infopath-form-templates-with-code"></a>Bereitstellen von InfoPath-Formularvorlagen mit Code

Der Formularcode für eine InfoPath-Formularvorlage mit verwaltetem Code wird als Assembly kompiliert, die unter der Common Language Runtime (CLR) ausgeführt wird. Wenn Sie also Änderungen am Formularcode vornehmen müssen, müssen Sie das Projekt in Visual Studio 2012 öffnen, Änderungen im Code-Editor vornehmen, die Formularvorlage neu kompilieren und dann die Formularvorlage erneut bereitstellen. Da die private Assembly für eine Formularvorlage mit verwaltetem Code unter einer gehosteten CLR-Anwendungsdomäne ausgeführt wird, unterscheiden sich die Sicherheitseinstellungen für Formulare, die volle Vertrauenswürdigkeit erfordern, geringfügig von Formularvorlagen, für die keine volle Vertrauenswürdigkeit erforderlich ist.
  
## <a name="deploying-form-templates-that-do-not-require-full-trust"></a>Bereitstellen von Formularvorlagen, die nicht volle Vertrauenswürdigkeit erfordern

Wenn im Formularcode für eine Formularvorlage keine InfoPath-Objektmodellmember verwendet werden, für die volle Vertrauenswürdigkeit erforderlich ist, und in der Formularvorlage keine Features verwendet werden, für die volle Vertrauenswürdigkeit erforderlich ist, können Sie die Formularvorlage direkt aus InfoPath heraus mit dem folgenden Verfahren veröffentlichen. Informationen zum InfoPath-Sicherheitsmodell finden Sie unter Informationen zum [Sicherheitsmodell für Formularvorlagen mit Code](about-the-security-model-for-form-templates-with-code.md).
  
### <a name="deploy-a-form-template-that-does-not-require-full-trust"></a>Bereitstellen einer Formularvorlage, die nicht volle Vertrauenswürdigkeit erfordert

1. Erstellen und Debuggen Sie Ihre Formularvorlage in Visual Studio 2012.
    
2. Wenn Sie im Code-Editor von Visual Studio 2012 arbeiten, wechseln Sie zu InfoPath, klicken Sie auf die Registerkarte **Datei** , und klicken Sie dann auf der Registerkarte **veröffentlichen** auf die Schaltfläche für den gewünschten Veröffentlichungsort. (wenn Sie die Formularvorlage zuvor veröffentlicht haben, können Sie auf die Registerkarte **Datei** , und klicken Sie dann auf **schnell veröffentlichen** , um die Formularvorlage erneut an demselben Speicherort zu veröffentlichen.) 
    
    Die Formularvorlage wird kompiliert und der Veröffentlichungs-Assistent gestartet. Folgen Sie den Schritten im Veröffentlichungs-Assistenten, um das Formular am gewünschten Speicherort bereitzustellen. Weitere Informationen zum Verwenden des Veröffentlichungs-Assistenten finden Sie in der InfoPath-Hilfe unter dem Suchbegriff "Veröffentlichen einer Formularvorlage".
    
## <a name="deploying-form-templates-that-require-full-trust"></a>Bereitstellen von Formularvorlagen, die volle Vertrauenswürdigkeit erfordern

Wenn im Formularcode für die Formularvorlage InfoPath-Objektmodellmember verwendet werden, für die volle Vertrauenswürdigkeit erforderlich ist, oder wenn in der Formularvorlage Features verwendet werden, für die volle Vertrauenswürdigkeit erforderlich ist, müssen Sie die Formularvorlagendatei (XSN) digital mit einem Codesignierungszertifikat von einem vertrauenswürdigen Herausgeber signieren. Beim Öffnen des Formulars werden die Benutzer gefragt, ob sie diesen Herausgeber als vertrauenswürdig einstufen möchten. Damit wird auch das Formular voll vertrauenswürdig, und dem Formularcode wird der FullTrust-Berechtigungssatz zugewiesen.
  
### <a name="compile-publish-and-digitally-sign-a-form-template"></a>Kompilieren, Veröffentlichen und digitales Signieren einer Formularvorlage

1. Erstellen und Debuggen Sie Ihre Formularvorlage in Visual Studio 2012.
    
2. Wenn Sie im Code-Editor von Visual Studio 2012 arbeiten, wechseln Sie zu InfoPath, klicken Sie auf die Registerkarte **Datei** , und klicken Sie dann auf **Formularoptionen**.
    
3. Klicken Sie auf die Kategorie **Sicherheit und Vertrauensstellung**. 
    
4. Deaktivieren Sie unter **Sicherheitsstufe** das Kontrollkästchen **Sicherheitsstufe automatisch ermitteln**, und wählen Sie dann **Voll vertrauenswürdig** aus.
    
5. Aktivieren Sie unter **Signatur der Formularvorlage** das Kontrollkästchen **Diese Formularvorlage signieren**, klicken Sie auf **Zertifikat auswählen**, und geben Sie dann das Codesignierungszertifikat an, mit dem die Formularvorlage signiert werden soll.
    
6. Klicken Sie zweimal auf **OK**, um das Dialogfeld **Formularoptionen** zu schließen, und speichern Sie dann die Änderungen. 
    
7. Klicken Sie auf die Registerkarte **Veröffentlichen** und dann auf die Schaltfläche für den gewünschten Veröffentlichungsort. 
    
8. Die Formularvorlage wird kompiliert und der**** Veröffentlichungs-Assistent gestartet. Befolgen Sie die Schritte im**** Veröffentlichungs-Assistenten, um die Formularvorlage bereitzustellen. Weitere Informationen zum Verwenden des**** Veröffentlichungs-Assistenten zum Bereitstellen einer Formularvorlage, die volle Vertrauenswürdigkeit erfordert, finden Sie in der InfoPath-Hilfe unter dem Suchbegriff "Veröffentlichen einer Formularvorlage mit voller Vertrauenswürdigkeit". 
    
 **Hinweise**
- Zum digitalen Signieren eines Formulars muss ein authentifiziertes Codesignierungszertifikat auf dem Computer installiert sein. Wenden Sie sich an eine Zertifizierungsstelle oder den Netzwerkadministrator, um ein solches Zertifikat zu erhalten.
    
- Wenn nach dem Veröffentlichen des Formulars Änderungen daran erforderlich sind, müssen Sie das Verfahren wiederholen und die Formularvorlage erneut signieren. Durch eine Änderung des Formulars wird die digitale Signatur ungültig. Während der Entwicklung eines Formulars, das die Berechtigung "voll vertrauenswürdig" erfordert, können Sie das in [Vorschau-und Debug-Formularvorlagen](how-to-preview-and-debug-form-templates-that-require-full-trust.md) beschriebene Verfahren verwenden, um die Formularvorlage auf dem lokalen Computer zu registrieren. 
    
## <a name="configuring-net-framework-security-settings"></a>Konfigurieren der .NET Framework-Sicherheitseinstellungen

Zur besseren Steuerung der Berechtigungen, die dem in einer InfoPath-Formularvorlage mit verwaltetem Code ausgeführten verwalteten Code erteilt werden, können Sie das Hilfsprogramm .NET Framework 2.0-Konfiguration verwenden, um dem Formularcode einen bestimmten Berechtigungssatz zuzuweisen.
  
> [!IMPORTANT]
> Das Konfigurieren der .NET Framework-Sicherheitseinstellungen für eine InfoPath-Formularvorlage mit verwaltetem Code wirkt sich nicht darauf aus, ob InfoPath-Objektmodellmember, die volle Vertrauenswürdigkeit erfordern, ausgeführt werden dürfen. Sie müssen eine Formularvorlage entsprechend der Beschreibung weiter oben in diesem Thema entweder digital signieren oder registrieren, um Aufrufe der InfoPath-Objektmodellmember zu ermöglichen, die volle Vertrauenswürdigkeit erfordern. Die .NET Framework-Sicherheitseinstellungen gelten nur für Aufrufe von Membern von .NET Framework-Klassen und anderen verwalteten Komponenten als dem InfoPath-Objektmodell. 
  
### <a name="compile-publish-and-configure-net-security-settings-for-a-form-template"></a>Kompilieren, Veröffentlichen und Konfigurieren der .NET-Sicherheitseinstellungen für eine Formularvorlage

1. Erstellen und Debuggen Sie Ihre Formularvorlage in Visual Studio 2012.
    
2. Wenn Sie im Code-Editor von Visual Studio 2012 arbeiten, wechseln Sie zu InfoPath, klicken Sie auf die Registerkarte **Datei** , klicken Sie auf **veröffentlichen**, und klicken Sie dann auf die Schaltfläche für den gewünschten Veröffentlichungsort.
    
    Die Formularvorlage wird kompiliert und der**** Veröffentlichungs-Assistent gestartet. Befolgen Sie die Schritte im**** Veröffentlichungs-Assistenten, um die Formularvorlage bereitzustellen. Weitere Informationen zum Verwenden des**** Veröffentlichungs-Assistenten finden Sie in der InfoPath-Hilfe unter dem Suchbegriff "Veröffentlichen einer Formularvorlage".
    
3. Führen Sie das im Abschnitt "Zuweisen von FullTrust zu Formularen in einer bestimmten URL oder UNC" beschriebene Verfahren unter [Konfigurieren von Sicherheitseinstellungen für Formularvorlagen mit Code](how-to-configure-security-settings-for-form-templates-with-code.md) aus.
    
## <a name="see-also"></a>Siehe auch

#### <a name="tasks"></a>Aufgaben

[Konfigurieren von Sicherheitseinstellungen für Formularvorlagen mit Code](how-to-configure-security-settings-for-form-templates-with-code.md)


[Informationen zum Sicherheitsmodell für Formularvorlagen mit Code](about-the-security-model-for-form-templates-with-code.md)
  
[Anzeigen einer Vorschau und Debuggen von Formularvorlagen, die vollständig vertrauenswürdig sein müssen](how-to-preview-and-debug-form-templates-that-require-full-trust.md)

