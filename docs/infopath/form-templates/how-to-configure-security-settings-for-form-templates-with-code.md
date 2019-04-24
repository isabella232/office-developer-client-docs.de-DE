---
title: Konfigurieren von Sicherheitseinstellungen für Formularvorlagen mit Code
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- Sicherheitsrichtlinien-Bereitstellungspaket [InfoPath 2007], URLs [InfoPath 2007], Zuweisen von FullTrust, Codezugriffssicherheit [InfoPath 2007], UNCs [InfoPath 2007], Zuweisen von FullTrust, CAS [InfoPath 2007], Sicherheit [InfoPath 2007], konfigurieren, Codegruppen [ InfoPath 2007], FullTrust [InfoPath 2007], zuweisen zu UNCs, FullTrust [InfoPath 2007], zuweisen zu URLs
localization_priority: Normal
ms.assetid: 24d1a322-581f-497e-b97b-bd02c4516551
description: Sie können den Berechtigungssatz anpassen, der auf eine InfoPath-Formularvorlage mit verwaltetem Code angewendet wird, indem Sie das .NET-Konfigurations-Snap-in verwenden.
ms.openlocfilehash: 77f3546d976bb5ea353aa3fbe58ba7af6cd92a6d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300160"
---
# <a name="configure-security-settings-for-form-templates-with-code"></a>Konfigurieren von Sicherheitseinstellungen für Formularvorlagen mit Code

Sie können den Berechtigungssatz anpassen, der auf eine InfoPath-Formularvorlage mit verwaltetem Code angewendet wird, indem Sie das .NET-Konfigurations-Snap-in verwenden.
  
Die Common Language Runtime (CLR), die von InfoPath gehostet wird, sucht nach einer vordefinierten Codegruppe mit dem Namen *InfoPath-Formularvorlagen* auf der Ebene der Computerrichtlinien unter der Gruppe All_Code. Die CLR wendet die Berechtigungssätze, die unter dieser Gruppe definiert sind, auf die Anwendungsdomäne (AppDomain) an, in der der Formularcode ausgeführt wird. Auf diese Weise können Sie die Berechtigungssätze anpassen, die InfoPath-Formularvorlagen mit verwaltetem Code erteilt werden. Sie können beispielsweise einer Formularvorlage, die von https://MySite der Berechtigung für den Zugriff auf Active Directory heruntergeladen wurde, erteilen. 
  
Zur Anwendung benutzerdefinierter Sicherheitsrichtlinien, die mithilfe des Snap-Ins .NET-Konfiguration definiert wurden, müssen diese auf allen Clientcomputern bereitgestellt werden, auf denen die Formularvorlage ausgeführt werden soll.
  
Weitere Informationen zum Sicherheitsmodell für InfoPath-Formularvorlagen mit verwaltetem Code finden Sie unter [Informationen zum Sicherheitsmodell für Formularvorlagen mit Code](about-the-security-model-for-form-templates-with-code.md)
  
## <a name="creating-a-code-group-for-infopath-form-templates"></a>Erstellen einer Codegruppe für InfoPath-Formularvorlagen

Mit dem folgenden Verfahren wird eine Codegruppe erstellt, die keine Berechtigungen für InfoPath-Formularvorlagen mit verwaltetem Code gewährt (mit Ausnahme derjenigen, die auf dem lokalen Computer installiert oder registriert sind), unter der Sie Berechtigungssätze zu InfoPath-Formularvorlagen zuweisen können. bei bestimmten URLs oder UNCs. Weitere Informationen zum Erstellen und Zuweisen von Berechtigungssätzen zu Codegruppen innerhalb der `InfoPath Form Templates` Codegruppe finden Sie im folgenden Verfahren. 
  
> [!NOTE]
> Im Gegensatz zum **Microsoft .NET framework 1,1-Konfigurations** Tool, das mit dem Redistributable-Paket von Microsoft .net Framework 1,1 installiert wird, wird die **microsoft .NET Framework 2,0-Konfiguration** nur mit Microsoft .NET Framework installiert. 2,0 Software Development Kit (SDK). 
  
### <a name="to-create-a-custom-security-code-group-for-infopath-managed-code-forms"></a>So erstellen Sie eine benutzerdefinierte Sicherheitscodegruppe für InfoPath-Formulare mit verwaltetem Code

1. Zeigen Sie im Menü **Start** auf **Verwaltung**, und klicken Sie dann auf **Microsoft .NET Framework 2.0-Konfiguration**.
    
    Wenn Sie im **Startmenü** nicht über **Verwaltungstools** verfügen, öffnen Sie in der **System** Steuerung die Option **Verwaltung**, und doppelklicken Sie dann auf **Microsoft .NET Framework 2,0-Konfiguration**.
    
2. Erweitern Sie unter **Arbeitsplatz**den Knoten **Laufzeitsicherheitsrichtlinie** , den Knoten **Computer** , **Code Gruppen** , den Knoten **All_Code** , klicken Sie dann mit der rechten Maustaste auf den Knoten **All_Code** , und klicken Sie dann auf **neu** , um das **Create Dialogfeld Code Gruppe** . 
    
3. Benennen Sie die neue Code `InfoPath Form Templates` Gruppe (dieser Text muss genau sein), und klicken Sie dann auf **weiter**.
    
4. Legen Sie den Bedingungstyp für die Codegruppe **Gesamter Code** fest, und klicken Sie dann auf **Weiter**.
    
5. Klicken Sie auf **Vorhandenen Berechtigungssatz verwenden**, weisen Sie den Berechtigungssatz **Nothing** der Codegruppe zu, klicken Sie auf **Weiter** und anschließend auf **Fertig stellen**.
    
6. Zum Anwenden der neuen Einstellungen müssen Sie InfoPath beenden und neu starten.
    
Wenn Sie es vorziehen, können Sie den Berechtigungssatz für alle InfoPath-Formularvorlagen mit verwaltetem Code verwalten, indem Sie der Codegruppe InfoPath- **Formularvorlagen** einen anderen Berechtigungssatz als **Nothing** zuweisen. 
> [!NOTE]
> Sie können den Berechtigungssatz für eine Sicherheitscodegruppe jederzeit ändern, indem Sie mit der rechten Maustaste auf die Gruppe in der klicken. **Net-konfiguration 2,0** -Snap-in, klicken Sie auf **Eigenschaften**, und klicken Sie dann auf die Registerkarte **Berechtigungssatz** . 
  
## <a name="assigning-fulltrust-to-forms-at-a-specific-url-or-unc"></a>Zuweisen von "Voll vertrauenswürdig" an Formulare unter einem bestimmten URL oder UNC

Sie können Codegruppen unter der Gruppe **InfoPath-Formularvorlagen** erstellen, um den Berechtigungssatz voll vertrauenswürdig auf Formularvorlagen von einer bestimmten URL oder UNC-Speicherort zu gewähren. Danach wird jede Formularvorlage, die am angegebenen Speicherort veröffentlicht wurde, voll vertrauenswürdig ausgeführt. 
  
> [!NOTE]
> Eine Formularvorlage, die auf dem lokalen Computer (Computer Zonen Codegruppe) geladen wird, wird von InfoPath mithilfe einer zufälligen URL geladen. Aus diesem Grund können Sie das folgende Verfahren nicht verwenden, um dem Berechtigungssatz FullTrust eine solche Formularvorlage zuzuweisen. Wenn Sie eine lokal installierte Formularvorlage mit dem Berechtigungssatz FullTrust erteilen möchten, verwenden Sie eines der Verfahren, die im Thema bereitStellen von Formularvorlagen, die die vollständige Vertrauenswürdigkeit erfordern, des Abschnitts [InfoPath-Formularvorlagen mit Code](how-to-deploy-infopath-form-templates-with-code.md) ausführen beschrieben werden. 
  
### <a name="to-assign-fulltrust-to-infopath-forms-at-a-specific-url-or-unc-location"></a>So weisen Sie InfoPath-Formularen unter einer bestimmten URL oder UNC die Berechtigung "Voll vertrauenswürdig" zu

1. Zeigen Sie im Menü **Start** auf **Verwaltung**, und klicken Sie dann auf **Microsoft .NET Framework 2.0-Konfiguration**.
    
    Wenn Sie im **Startmenü** nicht über **Verwaltungstools** verfügen, öffnen Sie in der **System** Steuerung die Option **Verwaltung**, und doppelklicken Sie dann auf **Microsoft .NET Framework 2,0-Konfiguration**.
    
2. Erweitern Sie unter **Arbeitsplatz**den Knoten **Laufzeitsicherheitsrichtlinie** , den Knoten **Computer** , **Code Gruppen** und den Knoten **All_Code** , und klicken Sie dann auf den Knoten **InfoPath-Formularvorlagen** . 
    
3. Klicken Sie in der Liste **Aufgaben** im rechten Bereich auf **Untergeordnete Codegruppe hinzufügen**, benennen Sie die Codegruppe, und klicken Sie dann auf **Weiter**.
    
4. Wählen Sie in der Liste **Wählen Sie die Konditionsart für diese Codegruppe** aus die Option **URL**aus, und geben Sie dann die URL oder UNC für den Speicherort der InfoPath-Formularvorlagen mit verwaltetem Code ein, denen Sie den **FullTrust** -Berechtigungssatz erteilen möchten. 
    
    Zum Einschränken des Berechtigungssatzes auf eine einzelne Formularvorlage geben Sie den vollständigen Pfad für die jeweilige Formularvorlage ein. Beispiel:
    
     `\\MyServer\MyShare\MyFormTemplate.xsn`
    
     `https://MySite/MySubsite/MyFormTempate.xsn`
    
    Wenn der Berechtigungssatz allen Formularvorlagen unter dieser URL oder UNC erteilt werden soll, lassen Sie den Namen der Vorlage weg, und fügen Sie ein Sternchen am Ende der URL oder UNC hinzu. Beispiel:
    
     `\\MyServer\MyShare\*`
    
     `https://MySite/MySubsite/*`
    
5. Klicken Sie auf **Weiter**, dann auf **Vorhandenen Berechtigungssatz verwenden**, und weisen Sie der Codegruppe den Berechtigungssatz **Voll vertrauenswürdig** zu. 
    
6. Klicken Sie auf **Weiter** und dann auf **Fertig stellen**.
    
7. Zum Anwenden der neuen Einstellungen müssen Sie InfoPath beenden und neu starten.
    
> [!NOTE]
> Wenn Sie einen restriktiveren oder benutzerdefinierten Berechtigungssatz anwenden möchten, wählen Sie anstelle von **Voll vertrauenswürdig** in Schritt 4 die geeignete Option aus. 
  
## <a name="creating-a-deployment-package-for-infopath-security-policy"></a>Erstellen eines Bereitstellungspakets für InfoPath-Sicherheitsrichtlinien

Nachdem Sie benutzerdefinierte Sicherheitsrichtlinien für InfoPath-Formularvorlagen definiert haben, können Sie ein Windows Installer-Paket (MSI) erstellen, um diese Sicherheitsrichtlinie auf Benutzercomputern mithilfe von Gruppenrichtlinien oder Microsoft Systems Management Server bereitzustellen.
  
### <a name="to-create-a-deployment-package-for-custom-infopath-security-policy"></a>So erstellen Sie ein Bereitstellungspaket für benutzerdefinierte InfoPath-Sicherheitsrichtlinien

1. Zeigen Sie im Menü **Start** auf **Verwaltung**, und klicken Sie dann auf **Microsoft .NET Framework 2.0-Konfiguration**.
    
    Wenn Sie im **Startmenü** nicht über **Verwaltungstools** verfügen, öffnen Sie in der **System** Steuerung die Option **Verwaltung**, und doppelklicken Sie dann auf **Microsoft .NET Framework 2,0-Konfiguration**.
    
2. Klicken Sie mit der rechten Maustaste auf **Laufzeitsicherheitsrichtlinie**, und klicken Sie dann auf **Bereitstellungspaket erstellen**.
    
3. Klicken Sie unter **Wählen Sie die weiterzugebende Sicherheitsrichtlinienebene aus** auf **Computer**, geben Sie den Ordner und den Dateinamen für das Windows Installer-Paket an, und klicken Sie dann auf **Weiter**.
    
4. Klicken Sie auf **Fertig stellen**, um das Bereitstellungspaket zu erstellen. 
    
5. Informationen zur Verwendung des .NET Framework-Konfigurationstools finden Sie in der Visual Studio-Hilfe oder auf der MSDN-Website für ".NET Framework Configuration Tool (Mscorcfg. msc)".
    
## <a name="see-also"></a>Siehe auch



[Informationen zum Sicherheitsmodell für Formularvorlagen mit Code](about-the-security-model-for-form-templates-with-code.md)

