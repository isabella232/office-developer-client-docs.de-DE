---
title: Grundlegendes zu voll vertrauenswürdigen Formularen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 64d62990-6275-edef-c639-b6ba8d10c38c
description: InfoPath bietet die Möglichkeit, voll vertrauenswürdige Formulare zu erstellen, bei denen es sich um Formulare mit höheren Sicherheitsberechtigungen handelt, die auf Systemressourcen und andere Komponenten auf dem Computer eines Benutzers zugreifen können. In diesem Artikel wird beschrieben, was ein voll vertrauenswürdiges Formular ist und warum es verwendet wird, und ein voll vertrauenswürdiges Formular erstellen, indem Sie ein Standardformular manuell konvertieren und registrieren oder ein Standardformular digital signieren.
ms.openlocfilehash: 04560e0c844d6a6ff681fd366ca7da2e4db36ba1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430392"
---
# <a name="understanding-fully-trusted-forms"></a>Grundlegendes zu voll vertrauenswürdigen Formularen

InfoPath bietet die Möglichkeit, voll vertrauenswürdige Formulare zu erstellen, bei denen es sich um Formulare mit höheren Sicherheitsberechtigungen handelt, die auf Systemressourcen und andere Komponenten auf dem Computer eines Benutzers zugreifen können. In diesem Artikel wird beschrieben, was ein voll vertrauenswürdiges Formular ist und warum es verwendet wird, und ein voll vertrauenswürdiges Formular erstellen, indem Sie ein Standardformular manuell konvertieren und registrieren oder ein Standardformular digital signieren.

InfoPath-Formularvorlagen können mit unterschiedlichen Sicherheitsstufen bereitgestellt werden. Die verwendete Stufe wird durch die Art des Zugriffs auf externe Ressourcen bestimmt, über die ein Formular verfügen soll. Standardmäßig sind InfoPath-Formulare vom Zugriff auf Systemressourcen ausgeschlossen und können keine Softwarekomponenten verwenden, die nicht als sicher für die Verwendung von Skript gekennzeichnet sind. Dieses Verhalten kann jedoch außer Kraft gesetzt werden, sodass ein Formular Zugriff auf Systemressourcen und andere externe Ressourcen sowie auf Softwarekomponenten erhält, die nicht als sicher für die Verwendung von Skript gekennzeichnet sind.
  
Für die Verwendung eines Formulars benötigt InfoPath Zugriff auf die Formularvorlage, auf der das Formular basiert. Wenn Sie eine Formularvorlage erstellen, wird von InfoPath ein Eintrag in der Formulardefinitionsdatei (XSF-Datei) erstellt, der die URL des Speicherorts der Formularvorlage enthält. Ein URL-basiertes Formular wird als Formular *mit eingeschränkter Sicherheitsstufe* bezeichnet. Wenn ein Benutzer das Formular ausfüllt, wird es einem lokalen Cache hinzugefügt, und der Zugriff auf Systemressourcen wird ihm verweigert. Diese Art von Formularen erbt die Berechtigungen von der Domäne, in der die Formulare geöffnet werden. 
  
Sie können ein Formular jedoch so ändern, dass es stattdessen auf einem URN (Uniform Resource Name) basiert. Dadurch erhält es Zugriff auf Systemressourcen. Diese Art von Formularen wird als *voll vertrauenswürdig * bezeichnet. 
  
## <a name="why-use-a-fully-trusted-form"></a>Gründe für die Verwendung von voll vertrauenswürdigen Formularen

Voll vertrauenswürdige Formulare verfügen über umfassendere Berechtigungen als Formulare mit eingeschränkter Sicherheitsstufe. Sie können beispielsweise Programmiercode enthalten, in dem über externe Objekte auf Systemressourcen zugegriffen wird. Sie können Softwarekomponenten oder Microsoft ActiveX-Steuerelemente verwenden, die nicht als sicher für die Verwendung von Skript gekennzeichnet sind, und sie können in .NET-Assemblys bereitgestellte benutzerdefinierte Geschäftslogik verwenden.
  
Darüber hinaus ist für einige Member des InfoPath-Objektmodells die Sicherheitsstufe 3 festgelegt, sie können also nur in einem voll vertrauenswürdigen Formular verwendet werden. Um beispielsweise auf das Microsoft Office- **CommandBars** -Objekt zuzugreifen, verwenden Sie die [CommandBars](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.CommandBars.aspx) -Eigenschaft der InfoPath- [Fenster](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) Klasse, um einen Verweis darauf festzulegen. Da für diese Eigenschaft die Sicherheitsstufe 3 festgelegt ist, kann die Eigenschaft nur in einem voll vertrauenswürdigen Formular verwendet werden. 
  
> [!NOTE]
> Wenn Sie [](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.CommandBars.aspx) die CommandBars-Eigenschaft der [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) -Klasse oder ein anderes Objektmodellelement mit der Sicherheitsstufe 3 in einem Formular verwenden, das nicht vollständig vertrauenswürdig ist, wird der Fehler "Berechtigung verweigert" verursacht. 
  
## <a name="what-makes-a-form-fully-trusted"></a>Wodurch wird ein Formular voll vertrauenswürdig?

Zum Erstellen und Verwenden eines voll vertrauenswürdigen Formulars sind die folgenden Aktionen bezüglich der Benutzeroberfläche von InfoPath und der Formulardateien erforderlich:
  
- Aktivieren der Verwendung von voll vertrauenswürdigen Formularen in InfoPath in der Kategorie **Vertrauenswürdige Herausgeber** des Dialogfelds **Sicherheitscenter**. Diese Option muss aktiviert sein, damit Benutzer voll vertrauenswürdige Formulare öffnen können. 
    
- Registrieren des voll vertrauenswürdigen Formulars auf dem Zielcomputer mithilfe der **RegisterSolution**-Methode des InfoPath-Objekts **Application**. 
    
## <a name="creating-a-fully-trusted-form"></a>Erstellen eines voll vertrauenswürdigen Formulars

- Sie können das Formular manuell erstellen. Dazu müssen Sie einige Formulardateien direkt ändern.
    
- Sie können die Formularvorlage digital signieren.
    
### <a name="manually-creating-a-fully-trusted-form"></a>Manuelles Erstellen eines voll vertrauenswürdigen Formulars

#### <a name="to-manually-create-a-fully-trusted-form"></a>So erstellen Sie ein voll vertrauenswürdiges Formular manuell

1. Erstellen Sie eine Sicherungskopie der Formularvorlage, die Sie zu einer voll vertrauenswürdigen Formularvorlage machen möchten.
    
2. Öffnen Sie die Formularvorlage in InfoPath.
    
3. Speichern Sie die Quelldateien des Formulars in einem Ordner auf der Festplatte. Klicken Sie dazu auf die Registerkarte **Datei**, dann auf **Veröffentlichen** und anschließend auf **Quelldateien exportieren**.
    
4. Geben Sie den Ordner an, in dem die Quelldateien des Formulars gespeichert werden sollen, klicken Sie auf **OK**, und beenden Sie dann den InfoPath-Designer.
    
5. Öffnen Sie in dem Ordner, in den Sie die Formulardateien extrahiert haben, die Formulardefinitionsdatei (XSF `manifest.xsf` ), die standardmäßig in einem Text-Editor wie Microsoft Notepad benannt ist. 
    
6. Fügen Sie dem **xDocumentClass**-Element in der XSF-Datei die folgenden Attribute hinzu: 
   
   `requireFullTrust="yes"`<br/>
   `name="urn:MyForm:MyCompany`

   > [!NOTE]
   > Für den URN können beliebige Zeichenfolgenwerte verwendet werden, der gesamte Wert muss jedoch eindeutig sein. Es müssen mindestens zwei Werte nach dem `urn:` Präfix vorhanden sein, und diese Werte müssen durch einen Doppelpunkt getrennt werden. Zudem sollte der URN maximal 255 Zeichen lang sein. 
  
7. Speichern und schließen Sie die XSF-Datei, und öffnen Sie dann die XML-Vorlagendatei `Template.xml` (XML) standardmäßig in einem Text-Editor wie Editor. 
    
8. Entfernen Sie das Attribut **href** aus `mso-infoPathSolution` der Verarbeitungsanweisung, und ersetzen Sie es durch das gleiche **Name** -Attribut, das Sie in Schritt 6 für die XSF-Datei verwendet haben. 
    
   > [!NOTE]
   > Die URN-Werte, die für das **name**-Attribut verwendet werden, müssen in der XSF-Datei und in der XML-Vorlagendatei übereinstimmen. 
  
9. Speichern und schließen Sie die XML-Vorlagendatei.
    
10. Verpacken Sie die Dateien mit einem Tool wie makecab.exe neu im CAB-Format (XSN-Datei).
    
    > [!NOTE]
    > Der InfoPath-Formulardesigner unterstützt zwar das Neuverpacken der Formulardateien in einer XSN-Datei, das Formular wird jedoch dabei wieder zu einem URL-basierten Formular. Daher müssen Sie die Dateien manuell verpacken, um zu verhindern, dass Ihre Änderungen in den Formulardateien überschrieben werden. 
  
11. Erstellen Sie ein benutzerdefiniertes Installationsprogramm mithilfe der **RegisterSolution**-Methode des InfoPath-Objekts **Application**, um das voll vertrauenswürdige Formular zu installieren. Eine einfache Möglichkeit besteht darin, eine Skriptdatei mit den folgenden Codezeilen zu erstellen (in Microsoft JScript- oder VBScript-Syntax): 
    
    ```js
        objIPApp = new ActiveXObject("InfoPath.Application"); 
        objIPApp.RegisterSolution("C:\\MyForms\\MyTrustedForm.xsn"); 
        objIPApp.Quit(); 
        objIPApp = null;
    ```
   
    ```vb
        Public Sub InstallForm()
            Dim objIPApp As Object
            ' Create a reference to the Application object.
            Set objIPApp = CreateObject("InfoPath.Application")
            ' Register the InfoPath form template.
            objIPApp.RegisterSolution ("C:\\My Forms\\MyFormTemplate.xsn")
            MsgBox "The InfoPath form template has been registered."
            Set objIPApp = Nothing
        End Sub
        
    ```

> [!NOTE] 
> In diesem Beispiel wird zwar eine einfache Skriptdatei verwendet, Sie können aber auch einen robusteren Installationsmechanismus wie Microsoft Windows Installer-Dateien (MSI) verwenden. Stellen Sie jedoch sicher, dass Sie die **RegisterSolution** -Methode verwenden, um das voll vertrauenswürdige Formular auf dem Zielcomputer ordnungsgemäß zu installieren. Wenn Sie auf die **RegisterSolution** -Methode des InfoPath-Objekts **Application** von Visual Basic oder Visual Studio zugreifen möchten, legen Sie einen Verweis auf die Microsoft InfoPath 3,0-Typbibliothek fest, die von ipeditor. dll bereitgestellt wird, die in der C:\Program Ordner "Files\Microsoft Office\Office14". 
  
Wenn ein voll vertrauenswürdiges Formular entfernt werden muss, können Sie die **UnregisterSolution**-Methode des **Application**-Objekts verwenden, wie in den folgenden JScript- und VBScript-Beispielen gezeigt wird. 
    
```js
    objIPApp = new ActiveXObject("InfoPath.Application"); 
    objIPApp.UnregisterSolution("C:\\MyForms\\MyTrustedForm.xsn"); 
    objIPApp.Quit(); 
    objIPApp = null;
```

```vb
    Public Sub UninstallForm()
        Dim objIPApp As Object
        ' Create a reference to the Application object.
        Set objIPApp = CreateObject("InfoPath.Application")
        ' Unregister the InfoPath form template.
        objIPApp.UnregisterSolution ("C:\My Forms\MyFormTemplate.xsn")
        MsgBox ("The InfoPath form template has been unregistered.")
        Set objIPApp = Nothing
    End Sub
    
```

### <a name="digitally-signing-a-form-template-to-create-a-fully-trusted-form"></a>Digitales Signieren einer Formularvorlage zum Erstellen eines voll vertrauenswürdigen Formulars

Wenn Sie eine Formularvorlage digital signieren, können Sie eine voll vertrauenswürdige Formularvorlage per e-Mail oder auf einem Webserver bereitstellen, beispielsweise einem Server, auf dem Microsoft SharePoint Foundation läuft. Verwenden Sie die Schritte in den folgenden drei Verfahren, um ein Formular voll vertrauenswürdig zu machen: Geben Sie die volle Vertrauenswürdigkeit für das Formular an, signieren Sie es digital, und veröffentlichen Sie es dann.
  
#### <a name="to-digitally-sign-a-form-template"></a>So signieren Sie eine Formularvorlage digital

1. Öffnen Sie das Formular im InfoPath-Designer, klicken Sie auf die Registerkarte **Datei**, und klicken Sie dann auf der Registerkarte **Info** auf **Formularoptionen**. 
    
2. Klicken Sie im Dialogfeld **Formularoptionen** auf die Kategorie **Sicherheit und Vertrauensstellung**. 
    
3. Deaktivieren Sie die Option **Sicherheitsstufe automatisch ermitteln (empfohlen)**.
    
4. Aktivieren Sie **Voll vertrauenswürdig (das Formular kann auf Dateien und Einstellungen auf dem Computer zugreifen)**.
    
5. Aktivieren Sie unter **Signatur der Formularvorlage** die Option **Diese Formularvorlage signieren**.
    
6. Klicken Sie auf **Zertifikat auswählen**, um ein Zertifikat auszuwählen, das zuvor von einem vertrauenswürdigen Zertifikatanbieter heruntergeladen und installiert wurde. 
    
7. Klicken Sie zweimal auf OK, um den Vorgang vollständig zu beenden.
    
#### <a name="to-publish-the-form-template-to-a-sharepoint-document-library"></a>So veröffentlichen Sie die Formularvorlage in einer SharePoint-Dokumentbibliothek

1. Klicken Sie auf die Registerkarte **Datei**, dann auf **Veröffentlichen** und anschließend auf **SharePoint Server**.
    
2. Folgen Sie den Anweisungen des Veröffentlichungs-Assistenten****, um die Formularvorlage in einer neuen oder vorhandenen SharePoint-Dokumentbibliothek zu veröffentlichen. 
    
#### <a name="to-a-create-a-form-that-is-based-on-your-fully-trusted-digitally-signed-form-template"></a>So erstellen Sie ein Formular auf der Basis der voll vertrauenswürdigen, digital signierten Formularvorlage

1. Klicken Sie in der SharePoint-Dokumentbibliothek auf **Fill Out the Form**.
    
   > [!NOTE]
   > Nachdem die Formatvorlage mithilfe des Veröffentlichungs-Assistenten**** in einer SharePoint-Dokumentbibliothek veröffentlicht wurde, wird die Vorlage nicht als Element in der Formularbibliothek angezeigt. Wenn Sie in dieser Dokumentbibliothek ein Formular erstellen, wird die Vorlage standardmäßig als Vorlage für das neue Formular verwendet. 
  
2. Falls die Standardformularvorlage digital signiert ist, wird von InfoPath eine Sicherheitswarnung bezüglich der digital signierten Formularvorlage angezeigt. Wählen Sie **Dateien von dieser Quelle immer vertrauen und automatisch öffnen** aus, und klicken Sie dann auf **Öffnen**.
    
## <a name="using-a-fully-trusted-form"></a>Verwenden eines voll vertrauenswürdigen Formulars

Ein voll vertrauenswürdiges Formular wird ähnlich verwendet wie ein Standardformular. Der wesentliche Unterschied besteht darin, dass das Formular auf beschränkte Ressourcen zugreifen kann und keine Warnungen mehr angezeigt werden.
  
> [!NOTE]
> Damit ein voll vertrauenswürdiges Formular in InfoPath verwendet werden kann, müssen Benutzer sicherstellen, dass in der Kategorie **Vertrauenswürdige Herausgeber** des Dialogfelds **Sicherheitscenter** das Kontrollkästchen **Ausführung vollständig vertrauenswürdiger Formulare auf diesem Computer zulassen** aktiviert ist. Klicken Sie zum Öffnen des Dialogfelds **Vertrauensstellungscenter** auf die Registerkarte **Datei** , klicken Sie auf **Optionen** (unter der Registerkarte **InfoPath** ), klicken Sie auf **Vertrauensstellungs**Center und dann auf Einstellungen für das Trust **Center**. 
  
Ein voll vertrauenswürdiges Formular kann in InfoPath im Dialogfeld **Ein Formular ausfüllen** geöffnet werden. 
  
Das Dialogfeld **Ein Formular ausfüllen** wird geöffnet, wenn Sie im Aufgabenbereich **Ein Formular ausfüllen** auf **Weitere Formulare** klicken oder wenn Sie im Menü **Datei** auf **Ein Formular ausfüllen** klicken. 
  
### <a name="making-changes-to-a-fully-trusted-form"></a>Ändern eines voll vertrauenswürdigen Formulars

Wenn Sie nur die XSN-Datei ändern müssen, können Sie die Benutzer nach der Vornahme der Änderungen bitten, ihre vorhandenen XSN-Dateien durch die neue zu ersetzen. Die Benutzer müssen die Datei nicht mit einem benutzerdefinierten Installationsprogramm neu installieren.
  
Wenn Sie jedoch Änderungen an den in der XSN-Datei enthaltenen Formulardateien vornehmen, müssen Sie die Dateien wie oben erläutert neu verpacken. Anschließend müssen die Benutzer das voll vertrauenswürdige Formular neu installieren.
  
> [!NOTE]
> Die beste Methode ist es, die Formularvorlage im InfoPath-Designer erneut im XSN-Format zu speichern und dann mit den hier beschriebenen Schritten ein voll vertrauenswürdiges Formular zu erstellen. 
  
## <a name="conclusion"></a>Schlussbemerkung

Abhängig von Ihren Unternehmensanforderungen und den Bedürfnissen der Benutzer müssen Sie unter Umständen ein Formular erstellen, das über höhere Berechtigungen verfügt als das InfoPath-Standardformular. In InfoPath können Formulare so geändert werden, dass sie Zugriff auf Systemressourcen und andere externe Ressourcen haben, die nicht als sicher für die Verwendung von Skript gekennzeichnet sind. Dies kann manuell durch Ändern der Formulardateien einer Formularvorlage und Ausführen eines Installationsskripts erfolgen oder durch digitales Signieren der Formularvorlage.
  

