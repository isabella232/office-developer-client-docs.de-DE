---
title: Konfigurieren von Einstellungen für Formularvorlagen mit Code
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- Bereitstellungspaket für Sicherheitsrichtlinien [infopath 2007],URLs [InfoPath 2007], Zuweisen von FullTrust,Codezugriffssicherheit [InfoPath 2007],UNCs [InfoPath 2007], Zuweisen von FullTrust, CAS [InfoPath 2007],Sicherheit [InfoPath 2007], Konfigurieren,Codegruppen [InfoPath 2007],FullTrust [InfoPath 2007], Zuweisen zu UNCs,FullTrust [InfoPath 2007], Zuweisen zu URLs
localization_priority: Normal
ms.assetid: 24d1a322-581f-497e-b97b-bd02c4516551
description: Sie können den Berechtigungssatz, der auf eine Formularvorlage für verwalteten InfoPath-Code angewendet wird, mithilfe des .NET Configuration-Snap-Ins anpassen.
ms.openlocfilehash: 77f3546d976bb5ea353aa3fbe58ba7af6cd92a6d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300160"
---
# <a name="configure-security-settings-for-form-templates-with-code"></a>Konfigurieren von Einstellungen für Formularvorlagen mit Code

Sie können den Berechtigungssatz, der auf eine Formularvorlage für verwalteten InfoPath-Code angewendet wird, mithilfe des .NET Configuration-Snap-Ins anpassen.
  
Die von InfoPath gehostete Common Language Runtime (CLR)  sucht auf der Computerrichtlinienebene unter der Gruppe All_Code nach einer vordefinierten Codegruppe namens InfoPath-Formularvorlagen. Die CLR wenden die Berechtigungssätze, die unter dieser Gruppe definiert sind, auf die Anwendungsdomäne (AppDomain) an, in der der Formularcode ausgeführt wird. Auf diese Weise können Sie die Berechtigungssätze anpassen, die Formularvorlagen mit verwalteten Code von InfoPath gewährt werden. Sie können z. B. eine Formularvorlage erteilen, die aus der Berechtigung https://MySite für den Zugriff auf Active Directory heruntergeladen wurde. 
  
Zur Anwendung benutzerdefinierter Sicherheitsrichtlinien, die mithilfe des Snap-Ins .NET-Konfiguration definiert wurden, müssen diese auf allen Clientcomputern bereitgestellt werden, auf denen die Formularvorlage ausgeführt werden soll.
  
Weitere Informationen zum Sicherheitsmodell für Formularvorlagen mit verwalteten Code in InfoPath finden Sie unter Informationen zum Sicherheitsmodell für [Formularvorlagen mit Code](about-the-security-model-for-form-templates-with-code.md)
  
## <a name="creating-a-code-group-for-infopath-form-templates"></a>Erstellen einer Codegruppe für InfoPath-Formularvorlagen

Mit dem folgenden Verfahren wird eine Codegruppe erstellt, die keine Berechtigungen für Formularvorlagen mit verwaltetem Code von InfoPath erteilt (mit Ausnahme der auf Ihrem lokalen Computer installierten oder registrierten), unter der Sie InfoPath-Formularvorlagen, die sich in bestimmten URLs oder UNCs befinden, Berechtigungssätze zuweisen können. Informationen zum Erstellen und Zuweisen von Berechtigungssätzen zu Codegruppen innerhalb der Codegruppe finden Sie  `InfoPath Form Templates` im folgenden Verfahren. 
  
> [!NOTE]
> Im Gegensatz zum **Microsoft .NET Framework 1.1-Konfigurationstool,** das mit dem Microsoft .NET Framework 1.1 Redistributable Package installiert ist, wird **die Microsoft .NET Framework 2.0-Konfiguration** nur mit dem Microsoft .NET Framework 2.0 Software Development Kit (SDK) installiert. 
  
### <a name="to-create-a-custom-security-code-group-for-infopath-managed-code-forms"></a>So erstellen Sie eine benutzerdefinierte Sicherheitscodegruppe für InfoPath-Formulare mit verwaltetem Code

1. Zeigen Sie im Menü **Start** auf **Verwaltung**, und klicken Sie dann auf **Microsoft .NET Framework 2.0-Konfiguration**.
    
    Wenn Sie nicht über Administrative **Tools** im  Menü **Start** verfügen, öffnen Sie in der Systemsteuerung administrative **Tools,** und doppelklicken Sie dann auf Microsoft **.NET Framework 2.0-Konfiguration**.
    
2. Erweitern Sie unter Mein **Computer** den  Knoten  Laufzeitsicherheitsrichtlinie, den Knoten **Computer,** Codegruppen, den Knoten **All_Code,** und klicken Sie dann mit der rechten Maustaste auf den Knoten  **All_Code,** und klicken Sie auf **Neu,** um das Dialogfeld Codegruppe erstellen zu öffnen. 
    
3. Nennen Sie die neue Codegruppe  `InfoPath Form Templates` (dieser Text muss exakt sein), und klicken Sie dann auf **Weiter**.
    
4. Legen Sie den Bedingungstyp für die Codegruppe **Gesamter Code** fest, und klicken Sie dann auf **Weiter**.
    
5. Klicken Sie auf **Vorhandenen Berechtigungssatz verwenden**, weisen Sie den Berechtigungssatz **Nothing** der Codegruppe zu, klicken Sie auf **Weiter** und anschließend auf **Fertig stellen**.
    
6. Um die neuen Einstellungen anzuwenden, schließen und starten Sie InfoPath neu.
    
Wenn es Ihnen lieber ist, können Sie den Berechtigungssatz für alle Formularvorlagen  mit verwalteten Code in InfoPath verwalten, indem Sie der Codegruppe **InfoPath-Formularvorlagen** einen anderen Berechtigungssatz als den Berechtigungssatz Nothing zuweisen. 
> [!NOTE]
> Sie können den Berechtigungssatz für eine Sicherheitscodegruppe jederzeit ändern, indem Sie mit der rechten Maustaste auf die Gruppe in klicken. **NET Configuration 2.0** Snap-In, klicken Sie auf **Eigenschaften** und dann auf die Registerkarte **Berechtigungssatz.** 
  
## <a name="assigning-fulltrust-to-forms-at-a-specific-url-or-unc"></a>Zuweisen von "Voll vertrauenswürdig" an Formulare unter einem bestimmten URL oder UNC

Sie können Codegruppen unter der **Gruppe InfoPath-Formularvorlagen** erstellen, um formularvorlagen von einer bestimmten URL oder einem bestimmten UNC-Speicherort den voll vertrauenswürdigen Berechtigungssatz zu erteilen. Danach wird jede am angegebenen Speicherort veröffentlichte Formularvorlage vollständig vertrauenswürdig ausgeführt. 
  
> [!NOTE]
> Eine Formularvorlage, die vom lokalen Computer geladen wird (Codegruppe Meine Computerzone), wird von InfoPath mithilfe einer zufälligen URL geladen. Aus diesem Grund können Sie das folgende Verfahren nicht verwenden, um den Berechtigungssatz FullTrust für eine solche Formularvorlage zu erteilen. Um einer lokal installierten Formularvorlage den Berechtigungssatz FullTrust zu erteilen, verwenden Sie eines der Verfahren, die im Abschnitt "Bereitstellen von Formularvorlagen, die voll vertrauenswürdig sind" im Thema Bereitstellen von [InfoPath-Formularvorlagen](how-to-deploy-infopath-form-templates-with-code.md) mit Code beschrieben werden. 
  
### <a name="to-assign-fulltrust-to-infopath-forms-at-a-specific-url-or-unc-location"></a>So weisen Sie InfoPath-Formularen unter einer bestimmten URL oder UNC die Berechtigung "Voll vertrauenswürdig" zu

1. Zeigen Sie im Menü **Start** auf **Verwaltung**, und klicken Sie dann auf **Microsoft .NET Framework 2.0-Konfiguration**.
    
    Wenn Sie nicht über Administrative **Tools** im  Menü **Start** verfügen, öffnen Sie in der Systemsteuerung administrative **Tools,** und doppelklicken Sie dann auf Microsoft **.NET Framework 2.0-Konfiguration**.
    
2. Erweitern **Sie unter** Mein Computer den Knoten **Laufzeitsicherheitsrichtlinie,** den Knoten **Computer,** Codegruppen, den Knoten **All_Code,** und klicken Sie dann auf den Knoten **InfoPath-Formularvorlagen.**  
    
3. Klicken Sie in der Liste **Aufgaben** im rechten Bereich auf **Untergeordnete Codegruppe hinzufügen**, benennen Sie die Codegruppe, und klicken Sie dann auf **Weiter**.
    
4. Wählen  Sie in der Liste Bedingungstyp für diese Codegruppe auswählen **DIE URL** aus, und geben Sie dann die URL oder UNC für den Speicherort der Formularvorlagen mit verwaltetem Code von InfoPath ein, die Sie dem Berechtigungssatz **FullTrust** erteilen möchten. 
    
    Zum Einschränken des Berechtigungssatzes auf eine einzelne Formularvorlage geben Sie den vollständigen Pfad für die jeweilige Formularvorlage ein. Beispiel:
    
     `\\MyServer\MyShare\MyFormTemplate.xsn`
    
     `https://MySite/MySubsite/MyFormTempate.xsn`
    
    Wenn der Berechtigungssatz allen Formularvorlagen unter dieser URL oder UNC erteilt werden soll, lassen Sie den Namen der Vorlage weg, und fügen Sie ein Sternchen am Ende der URL oder UNC hinzu. Beispiel:
    
     `\\MyServer\MyShare\*`
    
     `https://MySite/MySubsite/*`
    
5. Klicken Sie auf **Weiter**, dann auf **Vorhandenen Berechtigungssatz verwenden**, und weisen Sie der Codegruppe den Berechtigungssatz **Voll vertrauenswürdig** zu. 
    
6. Klicken Sie auf **Weiter** und dann auf **Fertig stellen**.
    
7. Um die neuen Einstellungen anzuwenden, schließen und starten Sie InfoPath neu.
    
> [!NOTE]
> Wenn Sie einen restriktiveren oder benutzerdefinierten Berechtigungssatz anwenden möchten, wählen Sie anstelle von **Voll vertrauenswürdig** in Schritt 4 die geeignete Option aus. 
  
## <a name="creating-a-deployment-package-for-infopath-security-policy"></a>Erstellen eines Bereitstellungspakets für InfoPath-Sicherheitsrichtlinien

Nachdem Sie benutzerdefinierte Sicherheitsrichtlinien für verwaltete Formularvorlagen von InfoPath definiert haben, können Sie ein Windows Installer Package (.msi) erstellen, um diese Sicherheitsrichtlinie mithilfe von Gruppenrichtlinien oder Microsoft Systems Management Server auf den Computern der Benutzer zu bereitstellen.
  
### <a name="to-create-a-deployment-package-for-custom-infopath-security-policy"></a>So erstellen Sie ein Bereitstellungspaket für benutzerdefinierte InfoPath-Sicherheitsrichtlinien

1. Zeigen Sie im Menü **Start** auf **Verwaltung**, und klicken Sie dann auf **Microsoft .NET Framework 2.0-Konfiguration**.
    
    Wenn Sie nicht über Administrative **Tools** im  Menü **Start** verfügen, öffnen Sie in der Systemsteuerung administrative **Tools,** und doppelklicken Sie dann auf Microsoft **.NET Framework 2.0-Konfiguration**.
    
2. Klicken Sie mit der rechten Maustaste auf **Laufzeitsicherheitsrichtlinie**, und klicken Sie dann auf **Bereitstellungspaket erstellen**.
    
3. Klicken Sie unter **Wählen Sie die weiterzugebende Sicherheitsrichtlinienebene aus** auf **Computer**, geben Sie den Ordner und den Dateinamen für das Windows Installer-Paket an, und klicken Sie dann auf **Weiter**.
    
4. Klicken Sie auf **Fertig stellen**, um das Bereitstellungspaket zu erstellen. 
    
5. Weitere Informationen zur Verwendung des .NET Framework-Konfigurationstools finden Sie Visual Studio Hilfe oder auf der MSDN-Website nach ".NET Framework Configuration Tool (Mscorcfg.msc)".
    
## <a name="see-also"></a>Siehe auch



[Informationen zum Sicherheitsmodell für Formularvorlagen mit Code](about-the-security-model-for-form-templates-with-code.md)

