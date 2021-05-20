---
title: Grundlegendes zu voll vertrauenswürdigen Formularen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 64d62990-6275-edef-c639-b6ba8d10c38c
description: InfoPath bietet die Möglichkeit, vollständig vertrauenswürdige Formulare zu erstellen, bei denen es sich um Formulare handelt, die über höhere Sicherheitsberechtigungen verfügen und auf Systemressourcen und andere Komponenten auf dem Computer eines Benutzers zugreifen können. In diesem Artikel wird beschrieben, was ein voll vertrauenswürdiges Formular ist und warum es verwendet wird, und ein voll vertrauenswürdiges Formular erstellen, indem Sie ein Standardformular manuell konvertieren und registrieren oder ein Standardformular digital signieren.
ms.openlocfilehash: 04560e0c844d6a6ff681fd366ca7da2e4db36ba1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430392"
---
# <a name="understanding-fully-trusted-forms"></a><span data-ttu-id="9ec0a-104">Grundlegendes zu voll vertrauenswürdigen Formularen</span><span class="sxs-lookup"><span data-stu-id="9ec0a-104">Understanding Fully Trusted Forms</span></span>

<span data-ttu-id="9ec0a-105">InfoPath bietet die Möglichkeit, vollständig vertrauenswürdige Formulare zu erstellen, bei denen es sich um Formulare handelt, die über höhere Sicherheitsberechtigungen verfügen und auf Systemressourcen und andere Komponenten auf dem Computer eines Benutzers zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="9ec0a-105">InfoPath provides the ability to create fully trusted forms, which are forms that have greater security permissions and can access system resources and other components on a user's computer.</span></span> <span data-ttu-id="9ec0a-106">In diesem Artikel wird beschrieben, was ein voll vertrauenswürdiges Formular ist und warum es verwendet wird, und ein voll vertrauenswürdiges Formular erstellen, indem Sie ein Standardformular manuell konvertieren und registrieren oder ein Standardformular digital signieren.</span><span class="sxs-lookup"><span data-stu-id="9ec0a-106">This article describes what a fully trusted form is, and why it is used, and create a fully trusted form by manually converting and registering a standard form, or by digitally signing a standard form.</span></span>

<span data-ttu-id="9ec0a-107">InfoPath-Formularvorlagen können mit unterschiedlichen Sicherheitsstufen bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="9ec0a-107">InfoPath form templates can be deployed with varying levels of security.</span></span> <span data-ttu-id="9ec0a-108">Die verwendete Stufe wird durch die Art des Zugriffs auf externe Ressourcen bestimmt, über die ein Formular verfügen soll.</span><span class="sxs-lookup"><span data-stu-id="9ec0a-108">The level you use is dictated by the level of access to external resources that you want a form to have.</span></span> <span data-ttu-id="9ec0a-109">Standardmäßig sind InfoPath-Formulare vom Zugriff auf Systemressourcen ausgeschlossen und können keine Softwarekomponenten verwenden, die nicht als sicher für die Verwendung von Skript gekennzeichnet sind.</span><span class="sxs-lookup"><span data-stu-id="9ec0a-109">By default, InfoPath form templates are restricted from accessing system resources and are not allowed to use any software components that are not marked as safe for scripting.</span></span> <span data-ttu-id="9ec0a-110">Dieses Verhalten kann jedoch außer Kraft gesetzt werden, sodass ein Formular Zugriff auf Systemressourcen und andere externe Ressourcen sowie auf Softwarekomponenten erhält, die nicht als sicher für die Verwendung von Skript gekennzeichnet sind.</span><span class="sxs-lookup"><span data-stu-id="9ec0a-110">However, this behavior can be overridden so that a form can access system resources and other external resources, including software components that are not marked as safe for scripting.</span></span>
  
<span data-ttu-id="9ec0a-p104">Für die Verwendung eines Formulars benötigt InfoPath Zugriff auf die Formularvorlage, auf der das Formular basiert. Wenn Sie eine Formularvorlage erstellen, wird von InfoPath ein Eintrag in der Formulardefinitionsdatei (XSF-Datei) erstellt, der die URL des Speicherorts der Formularvorlage enthält. Ein URL-basiertes Formular wird als Formular *mit eingeschränkter Sicherheitsstufe* bezeichnet. Wenn ein Benutzer das Formular ausfüllt, wird es einem lokalen Cache hinzugefügt, und der Zugriff auf Systemressourcen wird ihm verweigert. Diese Art von Formularen erbt die Berechtigungen von der Domäne, in der die Formulare geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="9ec0a-p104">For a form to be used, InfoPath must be able to access the form template that the form is based on. When you create a form template, InfoPath creates an entry in the form definition (.xsf) file that contains the URL of the location of the form template. A URL-based form is said to be *sandboxed*. When a user fills it out, the form is added in a local cache and denied access to system resources. This kind of form inherits its permissions from the domain in which it is opened.</span></span> 
  
<span data-ttu-id="9ec0a-p105">Sie können ein Formular jedoch so ändern, dass es stattdessen auf einem URN (Uniform Resource Name) basiert. Dadurch erhält es Zugriff auf Systemressourcen. Diese Art von Formularen wird als *voll vertrauenswürdig* bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="9ec0a-p105">However, you can modify a form so that it is based on a Uniform Resource Name (URN) instead, which allows access to system resources. Forms of this kind are said to be *fully trusted*.</span></span> 
  
## <a name="why-use-a-fully-trusted-form"></a><span data-ttu-id="9ec0a-118">Gründe für die Verwendung von voll vertrauenswürdigen Formularen</span><span class="sxs-lookup"><span data-stu-id="9ec0a-118">Why Use a Fully Trusted Form?</span></span>

<span data-ttu-id="9ec0a-p106">Voll vertrauenswürdige Formulare verfügen über umfassendere Berechtigungen als Formulare mit eingeschränkter Sicherheitsstufe. Sie können beispielsweise Programmiercode enthalten, in dem über externe Objekte auf Systemressourcen zugegriffen wird. Sie können Softwarekomponenten oder Microsoft ActiveX-Steuerelemente verwenden, die nicht als sicher für die Verwendung von Skript gekennzeichnet sind, und sie können in .NET-Assemblys bereitgestellte benutzerdefinierte Geschäftslogik verwenden.</span><span class="sxs-lookup"><span data-stu-id="9ec0a-p106">Fully trusted forms have a better set of permissions than sandboxed forms. For example, they can contain programming code that uses external objects for accessing system resources, they can use software components or Microsoft ActiveX controls that are not marked as safe for scripting, and they can use custom business logic provided by .NET assemblies.</span></span>
  
<span data-ttu-id="9ec0a-121">Darüber hinaus ist für einige Member des InfoPath-Objektmodells die Sicherheitsstufe 3 festgelegt, sie können also nur in einem voll vertrauenswürdigen Formular verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9ec0a-121">In addition, some members of the InfoPath object model are set to security level 3, which means that they can only be used in a fully trusted form.</span></span> <span data-ttu-id="9ec0a-122">Um beispielsweise auf das Microsoft Office **CommandBars-Objekt** zu zugreifen, verwenden Sie die [CommandBars-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.CommandBars.aspx) der InfoPath [Window-Klasse,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) um einen Verweis darauf zu setzen.</span><span class="sxs-lookup"><span data-stu-id="9ec0a-122">For example, to access the Microsoft Office **CommandBars** object, you use the [CommandBars](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.CommandBars.aspx) property of the InfoPath [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) class to set a reference to it.</span></span> <span data-ttu-id="9ec0a-123">Da für diese Eigenschaft die Sicherheitsstufe 3 festgelegt ist, kann die Eigenschaft nur in einem voll vertrauenswürdigen Formular verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9ec0a-123">Because this property is set to security level 3, it cannot be used in a form that is not fully trusted.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="9ec0a-124">Die Verwendung der [CommandBars-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.CommandBars.aspx) der [Window-Klasse](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) oder eines anderen Objektmodellmmitglieds mit der Sicherheitsstufe 3 in einem Nicht vollständig vertrauenswürdigen Formular führt zu einem Fehler "Berechtigung verweigert".</span><span class="sxs-lookup"><span data-stu-id="9ec0a-124">Using the [CommandBars](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.CommandBars.aspx) property of the [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) class, or any other object model member that has a security level of 3, in a form that is not fully trusted will result in a "permission denied" error.</span></span> 
  
## <a name="what-makes-a-form-fully-trusted"></a><span data-ttu-id="9ec0a-125">Wodurch wird ein Formular voll vertrauenswürdig?</span><span class="sxs-lookup"><span data-stu-id="9ec0a-125">What Makes a Form Fully Trusted?</span></span>

<span data-ttu-id="9ec0a-126">Zum Erstellen und Verwenden eines voll vertrauenswürdigen Formulars sind die folgenden Aktionen bezüglich der Benutzeroberfläche von InfoPath und der Formulardateien erforderlich:</span><span class="sxs-lookup"><span data-stu-id="9ec0a-126">The following actions, involving both the InfoPath user interface and the form files, are required to create and use a fully trusted form:</span></span>
  
- <span data-ttu-id="9ec0a-p108">Aktivieren der Verwendung von voll vertrauenswürdigen Formularen in InfoPath in der Kategorie **Vertrauenswürdige Herausgeber** des Dialogfelds **Sicherheitscenter**. Diese Option muss aktiviert sein, damit Benutzer voll vertrauenswürdige Formulare öffnen können.</span><span class="sxs-lookup"><span data-stu-id="9ec0a-p108">Enabling InfoPath to allow for the use of fully trusted forms on the **Trusted Publishers** category of the **Trust Center** dialog box. This option must be enabled for users to open fully trusted forms.</span></span> 
    
- <span data-ttu-id="9ec0a-129">Registrieren des voll vertrauenswürdigen Formulars auf dem Zielcomputer mithilfe der **RegisterSolution**-Methode des InfoPath-Objekts **Application**.</span><span class="sxs-lookup"><span data-stu-id="9ec0a-129">Registering the fully trusted form on the target computer by using the **RegisterSolution** method of the InfoPath **Application** object.</span></span> 
    
## <a name="creating-a-fully-trusted-form"></a><span data-ttu-id="9ec0a-130">Erstellen eines voll vertrauenswürdigen Formulars</span><span class="sxs-lookup"><span data-stu-id="9ec0a-130">Creating a Fully Trusted Form</span></span>

- <span data-ttu-id="9ec0a-131">Sie können das Formular manuell erstellen. Dazu müssen Sie einige Formulardateien direkt ändern.</span><span class="sxs-lookup"><span data-stu-id="9ec0a-131">You can create the form manually, which involves modifying some of the form files directly.</span></span>
    
- <span data-ttu-id="9ec0a-132">Sie können die Formularvorlage digital signieren.</span><span class="sxs-lookup"><span data-stu-id="9ec0a-132">You can digitally sign the form template.</span></span>
    
### <a name="manually-creating-a-fully-trusted-form"></a><span data-ttu-id="9ec0a-133">Manuelles Erstellen eines voll vertrauenswürdigen Formulars</span><span class="sxs-lookup"><span data-stu-id="9ec0a-133">Manually Creating a Fully Trusted Form</span></span>

#### <a name="to-manually-create-a-fully-trusted-form"></a><span data-ttu-id="9ec0a-134">So erstellen Sie ein voll vertrauenswürdiges Formular manuell</span><span class="sxs-lookup"><span data-stu-id="9ec0a-134">To manually create a fully trusted form</span></span>

1. <span data-ttu-id="9ec0a-135">Erstellen Sie eine Sicherungskopie der Formularvorlage, die Sie zu einer voll vertrauenswürdigen Formularvorlage machen möchten.</span><span class="sxs-lookup"><span data-stu-id="9ec0a-135">Make a backup copy of the form template that you want to make fully trusted.</span></span>
    
2. <span data-ttu-id="9ec0a-136">Öffnen Sie die Formularvorlage in InfoPath.</span><span class="sxs-lookup"><span data-stu-id="9ec0a-136">Open the form template in InfoPath.</span></span>
    
3. <span data-ttu-id="9ec0a-137">Speichern Sie die Quelldateien des Formulars in einem Ordner auf der Festplatte. Klicken Sie dazu auf die Registerkarte **Datei**, dann auf **Veröffentlichen** und anschließend auf **Quelldateien exportieren**.</span><span class="sxs-lookup"><span data-stu-id="9ec0a-137">Save the form source files to a folder on your hard disk by clicking the **File** tab, clicking **Publish**, and then clicking **Export Source Files**.</span></span>
    
4. <span data-ttu-id="9ec0a-138">Geben Sie den Ordner an, in dem die Quelldateien des Formulars gespeichert werden sollen, klicken Sie auf **OK**, und beenden Sie dann den InfoPath-Designer.</span><span class="sxs-lookup"><span data-stu-id="9ec0a-138">Specify the folder in which to save the form source files, click **OK**, and then exit the InfoPath designer.</span></span>
    
5. <span data-ttu-id="9ec0a-139">Öffnen Sie in dem Ordner, in dem Sie die Formulardateien extrahiert haben, die Standardmäßig benannte Formulardefinitionsdatei (XSF) in einem Texteditor wie `manifest.xsf` Microsoft Editor.</span><span class="sxs-lookup"><span data-stu-id="9ec0a-139">In the folder in which you extracted the form files, open the form definition (.xsf) file, named  `manifest.xsf` by default, in a text editor such as Microsoft Notepad.</span></span> 
    
6. <span data-ttu-id="9ec0a-140">Fügen Sie dem **xDocumentClass**-Element in der XSF-Datei die folgenden Attribute hinzu:</span><span class="sxs-lookup"><span data-stu-id="9ec0a-140">Add the following attributes to the **xDocumentClass** element in the .xsf file:</span></span> 
   
   `requireFullTrust="yes"`<br/>
   `name="urn:MyForm:MyCompany`

   > [!NOTE]
   > Für den URN können beliebige Zeichenfolgenwerte verwendet werden, der gesamte Wert muss jedoch eindeutig sein. Es müssen mindestens zwei Werte hinter dem Präfix stehen, und `urn:` diese Werte müssen durch einen Doppelpunkt getrennt werden. <span data-ttu-id="9ec0a-143">Zudem sollte der URN maximal 255 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="9ec0a-143">In addition, the URN should not exceed 255 characters.</span></span> 
  
7. <span data-ttu-id="9ec0a-144">Speichern und schließen Sie die XSF-Datei, und öffnen Sie dann die standardmäßig benannte XML-Vorlagendatei (.xml) in einem Texteditor wie `Template.xml` Editor.</span><span class="sxs-lookup"><span data-stu-id="9ec0a-144">Save and close the .xsf file, and then open the XML template (.xml) file that is named  `Template.xml` by default, in a text editor such as Notepad.</span></span> 
    
8. <span data-ttu-id="9ec0a-145">Entfernen Sie **das href-Attribut** aus der Verarbeitungsanweisung, und ersetzen Sie es durch das Attribut mit demselben Namen, das Sie in Schritt 6 für die `mso-infoPathSolution` XSF-Datei verwendet haben. </span><span class="sxs-lookup"><span data-stu-id="9ec0a-145">Remove the **href** attribute from the  `mso-infoPathSolution` processing instruction and replace it with the same **name** attribute that you used in step 6 for the .xsf file.</span></span> 
    
   > [!NOTE]
   > <span data-ttu-id="9ec0a-146">Die URN-Werte, die für das **name**-Attribut verwendet werden, müssen in der XSF-Datei und in der XML-Vorlagendatei übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="9ec0a-146">The URN values that are used for the **name** attribute must be the same in both the .xsf file and XML template file.</span></span> 
  
9. <span data-ttu-id="9ec0a-147">Speichern und schließen Sie die XML-Vorlagendatei.</span><span class="sxs-lookup"><span data-stu-id="9ec0a-147">Save and close the XML template file.</span></span>
    
10. <span data-ttu-id="9ec0a-148">Verpacken Sie die Dateien mit einem Tool wie makecab.exe neu im CAB-Format (XSN-Datei).</span><span class="sxs-lookup"><span data-stu-id="9ec0a-148">Repackage the files into the .xsn CAB format with a tool such as makecab.exe.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="9ec0a-p110">Der InfoPath-Formulardesigner unterstützt zwar das Neuverpacken der Formulardateien in einer XSN-Datei, das Formular wird jedoch dabei wieder zu einem URL-basierten Formular. Daher müssen Sie die Dateien manuell verpacken, um zu verhindern, dass Ihre Änderungen in den Formulardateien überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="9ec0a-p110">Although InfoPath form designer supports repackaging the form files into an .xsn file, doing this will revert the form to a URL-based form. For this reason, you must repackage the files manually to avoid overwriting your changes to the form files.</span></span> 
  
11. <span data-ttu-id="9ec0a-p111">Erstellen Sie ein benutzerdefiniertes Installationsprogramm mithilfe der **RegisterSolution**-Methode des InfoPath-Objekts **Application**, um das voll vertrauenswürdige Formular zu installieren. Eine einfache Möglichkeit besteht darin, eine Skriptdatei mit den folgenden Codezeilen zu erstellen (in Microsoft JScript- oder VBScript-Syntax):</span><span class="sxs-lookup"><span data-stu-id="9ec0a-p111">Create a custom installation program by using the **RegisterSolution** method of the InfoPath **Application** object to install the fully trusted form. A simple way to do this is to create a script file that uses the following lines of code (in either Microsoft JScript or VBScript syntax):</span></span> 
    
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
> <span data-ttu-id="9ec0a-153">Obwohl in diesem Beispiel eine einfache Skriptdatei verwendet wird, können Sie auch einen stabileren Installationsmechanismus wie Microsoft Windows Installer (.msi) verwenden.</span><span class="sxs-lookup"><span data-stu-id="9ec0a-153">Although this example uses a simple script file, you can also use a more robust installation mechanism such as Microsoft Windows Installer (.msi) files.</span></span> <span data-ttu-id="9ec0a-154">Achten Sie jedoch darauf, die **RegisterSolution-Methode** zu verwenden, um das vollständig vertrauenswürdige Formular auf dem Zielcomputer ordnungsgemäß zu installieren.</span><span class="sxs-lookup"><span data-stu-id="9ec0a-154">Be sure, however, to use the **RegisterSolution** method to correctly install the fully trusted form on the target computer.</span></span> <span data-ttu-id="9ec0a-155">Um auf die **RegisterSolution-Methode**  des InfoPath-Application-Objekts von Visual Basic oder Visual Studio zu zugreifen, legen Sie einen Verweis auf die Microsoft InfoPath 3.0-Typbibliothek fest, die von IPEDITOR.dll bereitgestellt wird, die im Ordner "C:\Programme\Microsoft Office\Office14" installiert ist.</span><span class="sxs-lookup"><span data-stu-id="9ec0a-155">To access the **RegisterSolution** method of the InfoPath the **Application** object from Visual Basic or Visual Studio, set a reference to the Microsoft InfoPath 3.0 Type Library, which is provided by IPEDITOR.dll that is installed in the C:\Program Files\Microsoft Office\Office14 folder.</span></span> 
  
<span data-ttu-id="9ec0a-156">Wenn ein voll vertrauenswürdiges Formular entfernt werden muss, können Sie die **UnregisterSolution**-Methode des **Application**-Objekts verwenden, wie in den folgenden JScript- und VBScript-Beispielen gezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="9ec0a-156">If you have to remove a fully trusted form, you can use the **UnregisterSolution** method of the **Application** object as shown in the following JScript and VBScript examples.</span></span> 
    
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

### <a name="digitally-signing-a-form-template-to-create-a-fully-trusted-form"></a><span data-ttu-id="9ec0a-157">Digitales Signieren einer Formularvorlage zum Erstellen eines voll vertrauenswürdigen Formulars</span><span class="sxs-lookup"><span data-stu-id="9ec0a-157">Digitally Signing a Form Template to Create a Fully Trusted Form</span></span>

<span data-ttu-id="9ec0a-158">Durch das digitale Signieren einer Formularvorlage können Sie eine voll vertrauenswürdige Formularvorlage per E-Mail oder auf einem Webserver bereitstellen, z. B. auf einem Server, auf dem Microsoft SharePoint Foundation ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9ec0a-158">Digitally signing a form template enables you to deploy a fully trusted form template by email or on a Web server, such as a server that is running Microsoft SharePoint Foundation.</span></span> <span data-ttu-id="9ec0a-159">Verwenden Sie die Schritte in den folgenden drei Verfahren, um ein Formular voll vertrauenswürdig zu machen: Geben Sie die volle Vertrauenswürdigkeit für das Formular an, signieren Sie es digital, und veröffentlichen Sie es dann.</span><span class="sxs-lookup"><span data-stu-id="9ec0a-159">Use the steps in the following three procedures to make a form fully trusted by specifying full trust for the form, signing it digitally, and then publishing it.</span></span>
  
#### <a name="to-digitally-sign-a-form-template"></a><span data-ttu-id="9ec0a-160">So signieren Sie eine Formularvorlage digital</span><span class="sxs-lookup"><span data-stu-id="9ec0a-160">To digitally sign a form template</span></span>

1. <span data-ttu-id="9ec0a-161">Öffnen Sie das Formular im InfoPath-Designer, klicken Sie auf die Registerkarte **Datei**, und klicken Sie dann auf der Registerkarte **Info** auf **Formularoptionen**.</span><span class="sxs-lookup"><span data-stu-id="9ec0a-161">Open the form in the InfoPath designer, click the **File** tab, and then click **Form Options** on the **Info** tab.</span></span> 
    
2. <span data-ttu-id="9ec0a-162">Klicken Sie im Dialogfeld **Formularoptionen** auf die Kategorie **Sicherheit und Vertrauensstellung**.</span><span class="sxs-lookup"><span data-stu-id="9ec0a-162">In the **Form Options** dialog box, click the **Security and Trust** category.</span></span> 
    
3. <span data-ttu-id="9ec0a-163">Deaktivieren Sie die Option **Sicherheitsstufe automatisch ermitteln (empfohlen)**.</span><span class="sxs-lookup"><span data-stu-id="9ec0a-163">Clear the selection for **Automatically determine security level (recommended)**.</span></span>
    
4. <span data-ttu-id="9ec0a-164">Aktivieren Sie **Voll vertrauenswürdig (das Formular kann auf Dateien und Einstellungen auf dem Computer zugreifen)**.</span><span class="sxs-lookup"><span data-stu-id="9ec0a-164">Select **Full Trust (the form has access to files and settings on the user's computer)**.</span></span>
    
5. <span data-ttu-id="9ec0a-165">Aktivieren Sie unter **Signatur der Formularvorlage** die Option **Diese Formularvorlage signieren**.</span><span class="sxs-lookup"><span data-stu-id="9ec0a-165">Under **Form Template Signature**, select **Sign this form template**.</span></span>
    
6. <span data-ttu-id="9ec0a-166">Klicken Sie auf **Zertifikat auswählen**, um ein Zertifikat auszuwählen, das zuvor von einem vertrauenswürdigen Zertifikatanbieter heruntergeladen und installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="9ec0a-166">Click **Select Certificate** to select a certificate that was previously downloaded and installed from a trusted certificate provider.</span></span> 
    
7. <span data-ttu-id="9ec0a-167">Klicken Sie zweimal auf OK, um den Vorgang vollständig zu beenden.</span><span class="sxs-lookup"><span data-stu-id="9ec0a-167">Click OK two times to exit completely.</span></span>
    
#### <a name="to-publish-the-form-template-to-a-sharepoint-document-library"></a><span data-ttu-id="9ec0a-168">So veröffentlichen Sie die Formularvorlage in einer SharePoint-Dokumentbibliothek</span><span class="sxs-lookup"><span data-stu-id="9ec0a-168">To publish the form template to a SharePoint Document Library</span></span>

1. <span data-ttu-id="9ec0a-169">Klicken Sie auf die Registerkarte **Datei**, dann auf **Veröffentlichen** und anschließend auf **SharePoint Server**.</span><span class="sxs-lookup"><span data-stu-id="9ec0a-169">Click the **File** tab, click **Publish**, and then click **SharePoint Server**.</span></span>
    
2. <span data-ttu-id="9ec0a-170">Folgen Sie den Anweisungen des Veröffentlichungs-Assistenten, um die Formularvorlage in einer neuen oder vorhandenen SharePoint-Dokumentbibliothek zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="9ec0a-170">Follow the instructions in the **Publishing Wizard** to publish the form template to a new or existing SharePoint document library.</span></span> 
    
#### <a name="to-a-create-a-form-that-is-based-on-your-fully-trusted-digitally-signed-form-template"></a><span data-ttu-id="9ec0a-171">So erstellen Sie ein Formular auf der Basis der voll vertrauenswürdigen, digital signierten Formularvorlage</span><span class="sxs-lookup"><span data-stu-id="9ec0a-171">To a create a form that is based on your fully trusted, digitally signed form template</span></span>

1. <span data-ttu-id="9ec0a-172">Klicken Sie in der SharePoint-Dokumentbibliothek auf **Fill Out the Form**.</span><span class="sxs-lookup"><span data-stu-id="9ec0a-172">In the SharePoint document library, click **Fill Out the Form**.</span></span>
    
   > [!NOTE]
   > <span data-ttu-id="9ec0a-p114">Nachdem die Formatvorlage mithilfe des Veröffentlichungs-Assistenten in einer SharePoint-Dokumentbibliothek veröffentlicht wurde, wird die Vorlage nicht als Element in der Formularbibliothek angezeigt. Wenn Sie in dieser Dokumentbibliothek ein Formular erstellen, wird die Vorlage standardmäßig als Vorlage für das neue Formular verwendet.</span><span class="sxs-lookup"><span data-stu-id="9ec0a-p114">After publishing the form template to a SharePoint document library using the **Publishing Wizard**, the template is not displayed as an item in the form library. When you create a form in that document library, the template will be used by default as the template for the new form.</span></span> 
  
2. <span data-ttu-id="9ec0a-p115">Falls die Standardformularvorlage digital signiert ist, wird von InfoPath eine Sicherheitswarnung bezüglich der digital signierten Formularvorlage angezeigt. Wählen Sie **Dateien von dieser Quelle immer vertrauen und automatisch öffnen** aus, und klicken Sie dann auf **Öffnen**.</span><span class="sxs-lookup"><span data-stu-id="9ec0a-p115">If the default form template was digitally signed, InfoPath displays a security warning about the digitally signed form template. Select **Always trust files from this publisher and open them automatically**, and then click **Open**.</span></span>
    
## <a name="using-a-fully-trusted-form"></a><span data-ttu-id="9ec0a-177">Verwenden eines voll vertrauenswürdigen Formulars</span><span class="sxs-lookup"><span data-stu-id="9ec0a-177">Using a Fully Trusted Form</span></span>

<span data-ttu-id="9ec0a-p116">Ein voll vertrauenswürdiges Formular wird ähnlich verwendet wie ein Standardformular. Der wesentliche Unterschied besteht darin, dass das Formular auf beschränkte Ressourcen zugreifen kann und keine Warnungen mehr angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="9ec0a-p116">Using a fully trusted form is very similar to using a standard form. The only significant differences are that the form can access restricted resources and warnings will no longer be displayed.</span></span>
  
> [!NOTE]
> <span data-ttu-id="9ec0a-180">Damit ein voll vertrauenswürdiges Formular in InfoPath verwendet werden kann, müssen Benutzer sicherstellen, dass in der Kategorie **Vertrauenswürdige Herausgeber** des Dialogfelds **Sicherheitscenter** das Kontrollkästchen **Ausführung vollständig vertrauenswürdiger Formulare auf diesem Computer zulassen** aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="9ec0a-180">To enable InfoPath to use a fully trusted form, users must ensure that the **Allow fully trusted forms to run on my computer** check box is selected on the **Trusted Publishers** category of the **Trust Center** dialog box.</span></span> <span data-ttu-id="9ec0a-181">Klicken Sie **zum** Öffnen des  Dialogfelds Vertrauensstellungscenter auf die Registerkarte Datei, klicken Sie auf Optionen **(unterhalb** der Registerkarte **InfoPath),** klicken Sie auf Vertrauensstellungscenter, und klicken Sie dann auf Einstellungen **.**</span><span class="sxs-lookup"><span data-stu-id="9ec0a-181">To open the **Trust Center** dialog box, click the **File** tab, click **Options** (below the **InfoPath** tab), click **Trust Center**, and then click **Trust Center Settings**.</span></span> 
  
<span data-ttu-id="9ec0a-182">Ein voll vertrauenswürdiges Formular kann in InfoPath im Dialogfeld **Ein Formular ausfüllen** geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="9ec0a-182">A fully trusted form can be opened in InfoPath from the **Fill Out a Form** dialog box.</span></span> 
  
<span data-ttu-id="9ec0a-183">Das Dialogfeld **Ein Formular ausfüllen** wird geöffnet, wenn Sie im Aufgabenbereich **Ein Formular ausfüllen** auf **Weitere Formulare** klicken oder wenn Sie im Menü **Datei** auf **Ein Formular ausfüllen** klicken.</span><span class="sxs-lookup"><span data-stu-id="9ec0a-183">The **Fill Out a Form** dialog box opens when you click **More Forms** in the **Fill Out a Form** task pane, or you click **Fill Out a Form** on the **File** menu.</span></span> 
  
### <a name="making-changes-to-a-fully-trusted-form"></a><span data-ttu-id="9ec0a-184">Ändern eines voll vertrauenswürdigen Formulars</span><span class="sxs-lookup"><span data-stu-id="9ec0a-184">Making Changes to a Fully Trusted Form</span></span>

<span data-ttu-id="9ec0a-p118">Wenn Sie nur die XSN-Datei ändern müssen, können Sie die Benutzer nach der Vornahme der Änderungen bitten, ihre vorhandenen XSN-Dateien durch die neue zu ersetzen. Die Benutzer müssen die Datei nicht mit einem benutzerdefinierten Installationsprogramm neu installieren.</span><span class="sxs-lookup"><span data-stu-id="9ec0a-p118">If you only have to make changes to the .xsn file, you can have users replace their existing .xsn file with the new one after the changes are made. They will not have to reinstall it by using a custom installation program.</span></span>
  
<span data-ttu-id="9ec0a-187">Wenn Sie jedoch Änderungen an den in der XSN-Datei enthaltenen Formulardateien vornehmen, müssen Sie die Dateien wie oben erläutert neu verpacken. Anschließend müssen die Benutzer das voll vertrauenswürdige Formular neu installieren.</span><span class="sxs-lookup"><span data-stu-id="9ec0a-187">However, if you are making changes to the form files that the .xsn file contains, you must repackage the files, as explained earlier, and then have users reinstall the fully trusted form.</span></span>
  
> [!NOTE]
> <span data-ttu-id="9ec0a-188">Die beste Methode ist es, die Formularvorlage im InfoPath-Designer erneut im XSN-Format zu speichern und dann mit den hier beschriebenen Schritten ein voll vertrauenswürdiges Formular zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="9ec0a-188">The best approach is to save the form template back to the .xsn format from the InfoPath designer, and then follow the steps in this article to create a fully trusted form.</span></span> 
  
## <a name="conclusion"></a><span data-ttu-id="9ec0a-189">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="9ec0a-189">Conclusion</span></span>

<span data-ttu-id="9ec0a-p119">Abhängig von Ihren Unternehmensanforderungen und den Bedürfnissen der Benutzer müssen Sie unter Umständen ein Formular erstellen, das über höhere Berechtigungen verfügt als das InfoPath-Standardformular. In InfoPath können Formulare so geändert werden, dass sie Zugriff auf Systemressourcen und andere externe Ressourcen haben, die nicht als sicher für die Verwendung von Skript gekennzeichnet sind. Dies kann manuell durch Ändern der Formulardateien einer Formularvorlage und Ausführen eines Installationsskripts erfolgen oder durch digitales Signieren der Formularvorlage.</span><span class="sxs-lookup"><span data-stu-id="9ec0a-p119">Depending on your business requirements and the needs of your users, you may have to create a form that has a higher set of permissions than the standard InfoPath form. InfoPath provides the ability to modify a form so that it can access system resources and other external resources that are not marked as safe for scripting. This can be done manually by making modifications to the form files that a form template contains and running an installation script, or by digitally signing the form template.</span></span>
  

