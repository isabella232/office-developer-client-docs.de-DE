---
title: Konfigurieren von Sicherheits-Einstellungen für Formularvorlagen mit Code
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- Security Policy deployment package [infopath 2007],URLs [InfoPath 2007], assigning FullTrust,code access security [InfoPath 2007],UNCs [InfoPath 2007], assigning FullTrust,CAS [InfoPath 2007],security [InfoPath 2007], configuring,code groups [InfoPath 2007],FullTrust [InfoPath 2007], assigning to UNCs,FullTrust [InfoPath 2007], assigning to URLs
ms.localizationpriority: medium
ms.assetid: 24d1a322-581f-497e-b97b-bd02c4516551
description: Sie können den Berechtigungssatz, der auf eine InfoPath-Formularvorlage mit verwaltetem Code angewendet wird, mithilfe des .NET-Konfigurations-Snap-Ins anpassen.
ms.openlocfilehash: c420a88f6c6c1d4e1821efe310722d0f4f6845db
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59621234"
---
# <a name="configure-security-settings-for-form-templates-with-code"></a>Konfigurieren von Sicherheits-Einstellungen für Formularvorlagen mit Code

Sie können den Berechtigungssatz, der auf eine InfoPath-Formularvorlage mit verwaltetem Code angewendet wird, mithilfe des .NET-Konfigurations-Snap-Ins anpassen.
  
Die von InfoPath gehostete Common Language Runtime (CLR) sucht nach einer vordefinierten Codegruppe namens  *InfoPath-Formularvorlagen*  auf Computerrichtlinienebene unter der gruppe All_Code. Die CLR wendet die Berechtigungssätze, die unter dieser Gruppe definiert sind, auf die Anwendungsdomäne (AppDomain) an, in der der Formularcode ausgeführt wird. Dadurch können Sie die Berechtigungssätze anpassen, die InfoPath-Formularvorlagen mit verwaltetem Code gewährt werden. Sie können z. B. eine Formularvorlage erteilen, die von der Berechtigung für den Zugriff auf Active Directory heruntergeladen https://MySite wurde. 
  
Zur Anwendung benutzerdefinierter Sicherheitsrichtlinien, die mithilfe des Snap-Ins .NET-Konfiguration definiert wurden, müssen diese auf allen Clientcomputern bereitgestellt werden, auf denen die Formularvorlage ausgeführt werden soll.
  
Weitere Informationen zum Sicherheitsmodell für InfoPath-Formularvorlagen mit verwaltetem Code finden Sie unter ["Informationen zum Sicherheitsmodell für Formularvorlagen mit Code"](about-the-security-model-for-form-templates-with-code.md)
  
## <a name="creating-a-code-group-for-infopath-form-templates"></a>Erstellen einer Codegruppe für InfoPath-Formularvorlagen

Mit dem folgenden Verfahren wird eine Codegruppe erstellt, die keine Berechtigungen für InfoPath-Formularvorlagen mit verwaltetem Code gewährt (mit Ausnahme derjenigen, die auf Ihrem lokalen Computer installiert oder registriert sind), unter der Sie InfoPath-Formularvorlagen, die sich an bestimmten URLs oder UNCs befinden, Berechtigungssätze zuweisen können. Informationen zum Erstellen und Zuweisen von Berechtigungssätzen zu Codegruppen innerhalb der  `InfoPath Form Templates` Codegruppe finden Sie im folgenden Verfahren. 
  
> [!NOTE]
> Im Gegensatz zum **Microsoft .NET Framework 1.1-Konfigurationstool,** das mit dem Microsoft .NET Framework 1.1 Redistributable Package installiert ist, wird die **Microsoft .NET Framework 2.0-Konfiguration** nur mit dem Microsoft .NET Framework 2.0 Software Development Kit (SDK) installiert. 
  
### <a name="to-create-a-custom-security-code-group-for-infopath-managed-code-forms"></a>So erstellen Sie eine benutzerdefinierte Sicherheitscodegruppe für InfoPath-Formulare mit verwaltetem Code

1. Zeigen Sie im Menü **Start** auf **Verwaltung**, und klicken Sie dann auf **Microsoft .NET Framework 2.0-Konfiguration**.
    
    Wenn Im **Startmenü** keine **Verwaltungstools** vorhanden sind, öffnen Sie in der **Systemsteuerung** **die Verwaltungstools,** und doppelklicken Sie dann auf **Microsoft .NET Framework 2.0-Konfiguration.**
    
2. Erweitern Sie unter **"Mein Computer"** den Knoten **"Laufzeitsicherheitsrichtlinie",** den Knoten **"Computer",** **"Codegruppen"** und den **Knoten "All_Code",** und klicken Sie dann mit der rechten Maustaste auf den Knoten **All_Code,** und klicken Sie auf **"Neu",** um das Dialogfeld **"Codegruppe erstellen"** zu öffnen. 
    
3. Benennen Sie die neue Codegruppe `InfoPath Form Templates` (dieser Text muss exakt sein), und klicken Sie dann auf **"Weiter".**
    
4. Legen Sie den Bedingungstyp für die Codegruppe **Gesamter Code** fest, und klicken Sie dann auf **Weiter**.
    
5. Klicken Sie auf **Vorhandenen Berechtigungssatz verwenden**, weisen Sie den Berechtigungssatz **Nothing** der Codegruppe zu, klicken Sie auf **Weiter** und anschließend auf **Fertig stellen**.
    
6. Um die neuen Einstellungen anzuwenden, schließen Sie InfoPath, und starten Sie es neu.
    
Wenn Sie möchten, können Sie den Berechtigungssatz für alle InfoPath-Formularvorlagen mit verwaltetem Code verwalten, indem Sie der Codegruppe **InfoPath-Formularvorlagen** einen anderen Berechtigungssatz als den Berechtigungssatz **Nothing** zuweisen. 
> [!NOTE]
> Sie können den Berechtigungssatz für eine Sicherheitscodegruppe jederzeit ändern, indem Sie mit der rechten Maustaste auf die Gruppe in der . **Snap-In für NET Configuration 2.0,** Klicken auf **Eigenschaften** und anschließendes Klicken auf die Registerkarte **"Berechtigungssatz".** 
  
## <a name="assigning-fulltrust-to-forms-at-a-specific-url-or-unc"></a>Zuweisen von "Voll vertrauenswürdig" an Formulare unter einem bestimmten URL oder UNC

Sie können Codegruppen unter der **InfoPath-Formularvorlagengruppe** erstellen, um Formularvorlagen von einer bestimmten URL oder einem UNC-Speicherort den Berechtigungssatz "Voll vertrauenswürdig" zu erteilen. Danach wird jede formularvorlage, die an dem angegebenen Speicherort veröffentlicht wurde, voll vertrauenswürdig ausgeführt. 
  
> [!NOTE]
> Eine Formularvorlage, die vom lokalen Computer (Codegruppe "Meine Computerzone") geladen wird, wird von InfoPath mithilfe einer zufälligen URL geladen. Aus diesem Grund können Sie das folgende Verfahren nicht verwenden, um einer solchen Formularvorlage den Berechtigungssatz "FullTrust" zu erteilen. Um einer lokal installierten Formularvorlage den Berechtigungssatz "FullTrust" zu gewähren, verwenden Sie eines der Verfahren, die im Abschnitt "Bereitstellen von Formularvorlagen, die voll vertrauenswürdig sein müssen" des Themas ["Bereitstellen von InfoPath-Formularvorlagen mit Code"](how-to-deploy-infopath-form-templates-with-code.md) beschrieben sind. 
  
### <a name="to-assign-fulltrust-to-infopath-forms-at-a-specific-url-or-unc-location"></a>So weisen Sie InfoPath-Formularen unter einer bestimmten URL oder UNC die Berechtigung "Voll vertrauenswürdig" zu

1. Zeigen Sie im Menü **Start** auf **Verwaltung**, und klicken Sie dann auf **Microsoft .NET Framework 2.0-Konfiguration**.
    
    Wenn Im **Startmenü** keine **Verwaltungstools** vorhanden sind, öffnen Sie in der **Systemsteuerung** **die Verwaltungstools,** und doppelklicken Sie dann auf **Microsoft .NET Framework 2.0-Konfiguration.**
    
2. Erweitern Sie unter **"Mein Computer"** den Knoten **"Laufzeitsicherheitsrichtlinie",** den Knoten **"Computer",** **"Codegruppen"** und den **Knoten "All_Code",** und klicken Sie dann auf den Knoten **"InfoPath-Formularvorlagen".** 
    
3. Klicken Sie in der Liste **Aufgaben** im rechten Bereich auf **Untergeordnete Codegruppe hinzufügen**, benennen Sie die Codegruppe, und klicken Sie dann auf **Weiter**.
    
4. Wählen Sie in der **Liste "Bedingungstyp für diese Codegruppenliste auswählen"** die **URL** aus, und geben Sie dann die URL oder UNC für den Speicherort der InfoPath-Formularvorlagen mit verwaltetem Code ein, die Sie dem **Berechtigungssatz "Voll vertrauenswürdig"** erteilen möchten. 
    
    Zum Einschränken des Berechtigungssatzes auf eine einzelne Formularvorlage geben Sie den vollständigen Pfad für die jeweilige Formularvorlage ein. Beispiel:
    
     `\\MyServer\MyShare\MyFormTemplate.xsn`
    
     `https://MySite/MySubsite/MyFormTempate.xsn`
    
    Wenn der Berechtigungssatz allen Formularvorlagen unter dieser URL oder UNC erteilt werden soll, lassen Sie den Namen der Vorlage weg, und fügen Sie ein Sternchen am Ende der URL oder UNC hinzu. Beispiel:
    
     `\\MyServer\MyShare\*`
    
     `https://MySite/MySubsite/*`
    
5. Klicken Sie auf **Weiter**, dann auf **Vorhandenen Berechtigungssatz verwenden**, und weisen Sie der Codegruppe den Berechtigungssatz **Voll vertrauenswürdig** zu. 
    
6. Klicken Sie auf **Weiter** und dann auf **Fertig stellen**.
    
7. Um die neuen Einstellungen anzuwenden, schließen Sie InfoPath, und starten Sie es neu.
    
> [!NOTE]
> Wenn Sie einen restriktiveren oder benutzerdefinierten Berechtigungssatz anwenden möchten, wählen Sie anstelle von **Voll vertrauenswürdig** in Schritt 4 die geeignete Option aus. 
  
## <a name="creating-a-deployment-package-for-infopath-security-policy"></a>Erstellen eines Bereitstellungspakets für InfoPath-Sicherheitsrichtlinien

Nachdem Sie benutzerdefinierte Sicherheitsrichtlinien für InfoPath-Vorlagen mit verwalteten Formularen definiert haben, können Sie ein Windows Installer-Paket (.msi) erstellen, um diese Sicherheitsrichtlinie mithilfe von Gruppenrichtlinien oder Microsoft Systems Management Server auf den Computern der Benutzer bereitzustellen.
  
### <a name="to-create-a-deployment-package-for-custom-infopath-security-policy"></a>So erstellen Sie ein Bereitstellungspaket für benutzerdefinierte InfoPath-Sicherheitsrichtlinien

1. Zeigen Sie im Menü **Start** auf **Verwaltung**, und klicken Sie dann auf **Microsoft .NET Framework 2.0-Konfiguration**.
    
    Wenn Im **Startmenü** keine **Verwaltungstools** vorhanden sind, öffnen Sie in der **Systemsteuerung** **die Verwaltungstools,** und doppelklicken Sie dann auf **Microsoft .NET Framework 2.0-Konfiguration.**
    
2. Klicken Sie mit der rechten Maustaste auf **Laufzeitsicherheitsrichtlinie**, und klicken Sie dann auf **Bereitstellungspaket erstellen**.
    
3. Klicken Sie unter **Wählen Sie die weiterzugebende Sicherheitsrichtlinienebene aus** auf **Computer**, geben Sie den Ordner und den Dateinamen für das Windows Installer-Paket an, und klicken Sie dann auf **Weiter**.
    
4. Klicken Sie auf **Fertig stellen**, um das Bereitstellungspaket zu erstellen. 
    
5. Informationen zur Verwendung des .NET Framework-Konfigurationstool finden Sie in Visual Studio Hilfe oder auf der MSDN-Website nach ".NET Framework Configuration Tool (Mscorcfg.msc)".
    
## <a name="see-also"></a>Siehe auch



[Informationen zum Sicherheitsmodell für Formularvorlagen mit Code](about-the-security-model-for-form-templates-with-code.md)

