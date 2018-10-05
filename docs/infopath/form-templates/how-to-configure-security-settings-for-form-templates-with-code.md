---
title: Konfigurieren von Sicherheitseinstellungen für Formularvorlagen mit verwaltetem Code
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- die Bereitstellung von Gruppenrichtlinien [Infopath 2007] URLs [InfoPath 2007], Zuweisen von FullTrust zu packen, Codezugriffssicherheit [InfoPath 2007], UNCs [InfoPath 2007], "voll vertrauenswürdig", CAS [InfoPath 2007], [InfoPath 2007] Sicherheit, konfigurieren, Code Gruppen [zuweisen InfoPath 2007] FullTrust [InfoPath 2007], zuweisen zu UNCs FullTrust [InfoPath 2007], zuweisen zu URLs
localization_priority: Normal
ms.assetid: 24d1a322-581f-497e-b97b-bd02c4516551
description: Sie können den Berechtigungssatz anpassen, der mit dem .NET Configuration-Snap-in auf einer InfoPath-Formularvorlage verwaltetem Code angewendet wird.
ms.openlocfilehash: 77f3546d976bb5ea353aa3fbe58ba7af6cd92a6d
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25391416"
---
# <a name="configure-security-settings-for-form-templates-with-code"></a>Konfigurieren von Sicherheitseinstellungen für Formularvorlagen mit verwaltetem Code

Sie können den Berechtigungssatz anpassen, der mit dem .NET Configuration-Snap-in auf einer InfoPath-Formularvorlage verwaltetem Code angewendet wird.
  
Die von InfoPath gehosteten common Language Runtime (CLR) sucht nach einer vordefinierten Codegruppe mit dem Namen *InfoPath-Formularvorlagen* auf Computerebene Richtlinie unter der Gruppe All_Code. Die CLR gelten die Berechtigungssätze, die unter dieser Gruppe sein, um die Anwendungsdomäne (AppDomain) definiert sind, wo die Formularcode ausgeführt wird. So können Sie die Berechtigungssätze anpassen, die verwalteten InfoPath-Formularvorlagen Code erteilt werden. Sie können beispielsweise eine Formularvorlage heruntergeladen erteilen https://MySite Berechtigung, um das Active Directory zugreifen. 
  
Zur Anwendung benutzerdefinierter Sicherheitsrichtlinien, die mithilfe des Snap-Ins .NET-Konfiguration definiert wurden, müssen diese auf allen Clientcomputern bereitgestellt werden, auf denen die Formularvorlage ausgeführt werden soll.
  
Weitere Informationen zum Sicherheitsmodell für InfoPath verwaltete code Formularvorlagen finden Sie [Informationen zum Sicherheitsmodell für Formularvorlagen mit Code](about-the-security-model-for-form-templates-with-code.md)
  
## <a name="creating-a-code-group-for-infopath-form-templates"></a>Erstellen einer Codegruppe für InfoPath-Formularvorlagen

Das folgende Verfahren wird eine Codegruppe, dass gewährt keine Berechtigungen in InfoPath managed code Formularvorlagen (ausgenommen solche, die installiert oder auf dem lokalen Computer registriert sind) erstellen, unter dem Sie zuweisen können Berechtigungssätze InfoPath-Formularvorlagen gefunden auf bestimmte URLs oder UNCs. Für Informationen zum Erstellen und Zuweisen von Berechtigungen auf Codegruppen innerhalb setzt die `InfoPath Form Templates` Codegruppe, finden Sie unter die folgenden Schritte aus. 
  
> [!NOTE]
> Im Gegensatz zu den **Microsoft .NET Framework 1.1-Konfiguration** -Tool, das mit dem Microsoft .NET Framework 1.1 Redistributable Package installiert wird, wird die **Microsoft .NET Framework 2.0-Konfiguration** nur mit Microsoft .NET Framework installiert. 2.0-Software Development Kit (SDK). 
  
### <a name="to-create-a-custom-security-code-group-for-infopath-managed-code-forms"></a>So erstellen Sie eine benutzerdefinierte Sicherheitscodegruppe für InfoPath-Formulare mit verwaltetem Code

1. Zeigen Sie im Menü **Start** auf **Verwaltung**, und klicken Sie dann auf **Microsoft .NET Framework 2.0-Konfiguration**.
    
    Wenn Sie im **Startmenü** auf **Verwaltung** nicht verfügen, aus der **Control Panel** öffnen Sie **Verwaltung**, und doppelklicken Sie dann auf **Microsoft .NET Framework 2.0-Konfiguration**.
    
2. Unter **Arbeitsplatz**erweitern Sie den Knoten **Laufzeitsicherheitsrichtlinie** , den Knoten **Computer** , Knoten **Codegruppen** , den Knoten **All_Code** , und klicken Sie dann mit der rechten Maustaste in des Knotens **All_Code** und klicken Sie auf **neu** , um die **erstellen zu öffnen Codegruppe** im Dialogfeld. 
    
3. Nennen Sie die neue Codegruppe `InfoPath Form Templates` (dieser Text muss genauen), und klicken Sie dann auf **Weiter**.
    
4. Legen Sie den Bedingungstyp für die Codegruppe **Gesamter Code** fest, und klicken Sie dann auf **Weiter**.
    
5. Klicken Sie auf **Vorhandenen Berechtigungssatz verwenden**, weisen Sie den Berechtigungssatz **Nothing** der Codegruppe zu, klicken Sie auf **Weiter** und anschließend auf **Fertig stellen**.
    
6. Um die neuen Einstellungen anzuwenden, schließen Sie, und starten Sie InfoPath.
    
Wenn Sie es vorziehen, können Sie den Berechtigungssatz für alle Formularvorlagen für InfoPath managed Code durch Zuweisen von einem Berechtigungssatz als den Berechtigungssatz **Nothing** der Codegruppe **InfoPath-Formularvorlagen** verwalten. 
> [!NOTE]
> Sie können den Berechtigungssatz für eine Sicherheitsgruppe Code können Sie jederzeit mit der rechten Maustaste in die Gruppe ändern der. **NET Configuration 2.0** -Snap-in, indem Sie auf **Eigenschaften**klicken und dann auf die Registerkarte **Berechtigungssatz** . 
  
## <a name="assigning-fulltrust-to-forms-at-a-specific-url-or-unc"></a>Zuweisen von "Voll vertrauenswürdig" an Formulare unter einem bestimmten URL oder UNC

Sie können Codegruppen unter der Gruppe InfoPath-Formularvorlagen erstellen, die Formularvorlagen unter einer bestimmten URL- oder UNC-Adresse den Berechtigungssatz Voll vertrauenswürdig erteilen. Jede unter der angegebenen Adresse veröffentlichte Formularvorlage wird dann als voll vertrauenswürdig ausgeführt. 
  
> [!NOTE]
> Eine Formularvorlage, die aus dem lokalen Computer (Mein Computer Zone Codegruppe) geladen wird, wird von InfoPath mithilfe einer zufällig ausgewählten URL geladen. Aus diesem Grund können Sie das folgende Verfahren zum Erteilen Sie der Berechtigungssatzes "voll vertrauenswürdig" zu einer solchen Formularvorlage verwenden. Erteilen einer lokal installierte Formularvorlage die Berechtigung "voll vertrauenswürdig" festgelegt ist, verwenden Sie eine der der beschriebenen Verfahren im Abschnitt "Bereitstellen von Formularvorlagen, die erfordern voll vertrauenswürdig" neben dem Thema [Bereitstellen von InfoPath-Formularvorlagen mit Code](how-to-deploy-infopath-form-templates-with-code.md) . 
  
### <a name="to-assign-fulltrust-to-infopath-forms-at-a-specific-url-or-unc-location"></a>So weisen Sie InfoPath-Formularen unter einer bestimmten URL oder UNC die Berechtigung "Voll vertrauenswürdig" zu

1. Zeigen Sie im Menü **Start** auf **Verwaltung**, und klicken Sie dann auf **Microsoft .NET Framework 2.0-Konfiguration**.
    
    Wenn Sie im **Startmenü** auf **Verwaltung** nicht verfügen, aus der **Control Panel** öffnen Sie **Verwaltung**, und doppelklicken Sie dann auf **Microsoft .NET Framework 2.0-Konfiguration**.
    
2. Klicken Sie unter **Arbeitsplatz**erweitern Sie den Knoten **Laufzeitsicherheitsrichtlinie** , den Knoten **Computer** , Knoten **Codegruppen** , den Knoten **All_Code** , und klicken Sie dann auf den Knoten **InfoPath-Formularvorlagen** . 
    
3. Klicken Sie in der Liste **Aufgaben** im rechten Bereich auf **Untergeordnete Codegruppe hinzufügen**, benennen Sie die Codegruppe, und klicken Sie dann auf **Weiter**.
    
4. Wählen Sie in der Liste **Wählen Sie den Bedingungstyp für die Codegruppe aus** **URL**aus, und geben Sie die URL oder UNC für den Speicherort der InfoPath managed Code Form Templates, die Sie den Berechtigungssatz **voll vertrauenswürdig** gewähren möchten. 
    
    Zum Einschränken des Berechtigungssatzes auf eine einzelne Formularvorlage geben Sie den vollständigen Pfad für die jeweilige Formularvorlage ein. Beispiel:
    
     `\\MyServer\MyShare\MyFormTemplate.xsn`
    
     `https://MySite/MySubsite/MyFormTempate.xsn`
    
    Wenn der Berechtigungssatz allen Formularvorlagen unter dieser URL oder UNC erteilt werden soll, lassen Sie den Namen der Vorlage weg, und fügen Sie ein Sternchen am Ende der URL oder UNC hinzu. Beispiel:
    
     `\\MyServer\MyShare\*`
    
     `https://MySite/MySubsite/*`
    
5. Klicken Sie auf **Weiter**, dann auf **Vorhandenen Berechtigungssatz verwenden**, und weisen Sie der Codegruppe den Berechtigungssatz **Voll vertrauenswürdig** zu. 
    
6. Klicken Sie auf  **Weiter ** und anschließend auf  **Fertig stellen **.
    
7. Um die neuen Einstellungen anzuwenden, schließen Sie, und starten Sie InfoPath.
    
> [!NOTE]
> Wenn Sie einen restriktiveren oder benutzerdefinierten Berechtigungssatz anwenden möchten, wählen Sie anstelle von **Voll vertrauenswürdig** in Schritt 4 die geeignete Option aus. 
  
## <a name="creating-a-deployment-package-for-infopath-security-policy"></a>Erstellen eines Bereitstellungspakets für InfoPath-Sicherheitsrichtlinien

Nach dem Definieren benutzerdefinierter Sicherheitsrichtlinien für InfoPath managed-Formularvorlagen, können Sie eine Windows Installer-Paket (MSI-Datei) zum Bereitstellen von dieser Codezugriffssicherheits-Richtlinie auf den Computern der Benutzer mithilfe von Gruppenrichtlinien oder Microsoft Systems Management Server erstellen.
  
### <a name="to-create-a-deployment-package-for-custom-infopath-security-policy"></a>So erstellen Sie ein Bereitstellungspaket für benutzerdefinierte InfoPath-Sicherheitsrichtlinien

1. Zeigen Sie im Menü **Start** auf **Verwaltung**, und klicken Sie dann auf **Microsoft .NET Framework 2.0-Konfiguration**.
    
    Wenn Sie im **Startmenü** auf **Verwaltung** nicht verfügen, aus der **Control Panel** öffnen Sie **Verwaltung**, und doppelklicken Sie dann auf **Microsoft .NET Framework 2.0-Konfiguration**.
    
2. Klicken Sie mit der rechten Maustaste auf **Laufzeitsicherheitsrichtlinie**, und klicken Sie dann auf **Bereitstellungspaket erstellen**.
    
3. Klicken Sie unter **Wählen Sie die weiterzugebende Sicherheitsrichtlinienebene aus** auf **Computer**, geben Sie den Ordner und den Dateinamen für das Windows Installer-Paket an, und klicken Sie dann auf **Weiter**.
    
4. Klicken Sie auf **Fertig stellen**, um das Bereitstellungspaket zu erstellen. 
    
5. Informationen zur Verwendung von .NET Framework-Konfigurationstools suchen Sie Hilfe zu Visual Studio oder der MSDN-Website nach ".NET Framework Configuration Tool (Mscorcfg.msc)".
    
## <a name="see-also"></a>Siehe auch



[Informationen zum Sicherheitsmodell für Formularvorlagen mit Code](about-the-security-model-for-form-templates-with-code.md)

