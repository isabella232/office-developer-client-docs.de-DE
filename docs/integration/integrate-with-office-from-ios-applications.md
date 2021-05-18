---
title: Integration in Office von iOS-Anwendungen aus
manager: soliver
ms.date: 06/04/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: f3a277ba-7ba1-4eea-83b5-915b409f3093
description: Office für iOS bietet eine erweiterbare Lösung, die die Integration in Drittanbieteranwendungen ermöglicht. Dieser Artikel beschreibt, wie Sie eine Integration in Office von Ihrer iOS-Anwendung ausführen können, indem Sie Benutzer von Ihrer Anwendung in Office übergeben und sie dann an die Anwendung zurückgeben.
ms.openlocfilehash: d17a096c17eadab0cd94ee1dce18e979e80fa65d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413850"
---
# <a name="integrate-with-office-from-ios-applications"></a><span data-ttu-id="dcb85-104">Integration in Office von iOS-Anwendungen aus</span><span class="sxs-lookup"><span data-stu-id="dcb85-104">Integrate with Office from iOS applications</span></span>

<span data-ttu-id="dcb85-p102">Office für iOS bietet eine erweiterbare Lösung, die die Integration in Drittanbieteranwendungen ermöglicht. Dieser Artikel beschreibt, wie Sie eine Integration in Office von Ihrer iOS-Anwendung ausführen können, indem Sie Benutzer von Ihrer Anwendung in Office übergeben und sie dann an die Anwendung zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="dcb85-p102">Office for iOS provides an extensible solution that enables integration with third-party applications. This article describes how you can integrate with Office from your iOS application by passing users from your application to Office, and then returning them to your application.</span></span>
  
<span data-ttu-id="dcb85-p103">Sie können Benutzern, die Office auf einem iOS-Gerät ausführen, ermöglichen, Dateien, die in SharePoint oder OneDrive gespeichert sind, von einer beliebigen Anwendung aus zu öffnen und zu bearbeiten und sie dann schnell in die ursprüngliche Anwendung zurückzugeben, wenn sie das Bearbeiten der Datei abgeschlossen haben. Hierfür übergeben Sie Dateien über Protokollhandler an Office und stellen sicher, dass Office so aufgerufen wird, dass Office dies versteht.</span><span class="sxs-lookup"><span data-stu-id="dcb85-p103">You can enable users who are running Office on an iOS device to open and edit files stored in SharePoint or OneDrive from any application, and then quickly return them to the original application when they're done editing the file. To do this, you pass files to Office via protocol handlers, and you make sure that Office is invoked in a way that Office can understand.</span></span>
  
<span data-ttu-id="dcb85-109">Wenn ein Benutzer mit der Bearbeitung einer Datei fertig ist, kann er auf den Pfeil "Zurück" in der Office-Anwendung klicken, um das Dokument zu schließen und es an die ursprüngliche Speicheranwendung zurückzugeben, vorausgesetzt, Sie übergeben bestimmte Informationen an die Office-Anwendung, wenn diese gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="dcb85-109">When a user is done editing a file, they can choose the back arrow in the Office application to close the document and return to the original storage application, provided you pass specific information to the Office application when it launches.</span></span>
  
## <a name="verify-that-office-has-been-installed"></a><span data-ttu-id="dcb85-110">Überprüfen, dass Office installiert wurde</span><span class="sxs-lookup"><span data-stu-id="dcb85-110">Verify that Office has been installed</span></span>

<span data-ttu-id="dcb85-p104">Die verweisende Anwendung muss zunächst überprüfen, dass eine bestimmte Office-Anwendung installiert ist. Die folgenden Office-Anwendungen können auf iOS-Geräten zum Anzeigen und Bearbeiten von Dokumenten installiert werden:</span><span class="sxs-lookup"><span data-stu-id="dcb85-p104">Your referring application will first need to verify that a particular Office application is installed. The following Office applications can be installed on iOS devices for document viewing and editing:</span></span>
  
- <span data-ttu-id="dcb85-113">Excel</span><span class="sxs-lookup"><span data-stu-id="dcb85-113">Excel</span></span>
    
- <span data-ttu-id="dcb85-114">OneNote</span><span class="sxs-lookup"><span data-stu-id="dcb85-114">OneNote</span></span>
    
- <span data-ttu-id="dcb85-115">PowerPoint</span><span class="sxs-lookup"><span data-stu-id="dcb85-115">PowerPoint</span></span>
    
- <span data-ttu-id="dcb85-116">Word</span><span class="sxs-lookup"><span data-stu-id="dcb85-116">Word</span></span>
    
<span data-ttu-id="dcb85-p105">Verwenden Sie die [canOpenURL](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIApplication_Class/index.html)-Methode, um zu bestimmen, ob die Anwendung die Ressourcen öffnen kann. Diese Methode verwendet die URL für die Ressource als Parameter und gibt **No** zurück, wenn die Anwendung, die die URL akzeptiert, nicht verfügbar ist. Wenn **canOpenURL** den Text **No** zurückgibt, müssen Sie den Benutzer auffordern, Office zu installieren.</span><span class="sxs-lookup"><span data-stu-id="dcb85-p105">Use the [canOpenURL](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIApplication_Class/index.html) method to determine whether your application can open the resource. This method takes the URL for the resource as a parameter, and returns **No** if the application that accepts the URL is not available. If **canOpenURL** returns **No**, you'll need to prompt the user to install Office.</span></span>
  
### <a name="prompt-the-user-to-install-office"></a><span data-ttu-id="dcb85-120">Auffordern des Benutzers zur Installation von Office</span><span class="sxs-lookup"><span data-stu-id="dcb85-120">Prompt the user to install Office</span></span>

 <span data-ttu-id="dcb85-p106">Wenn eine bestimmte Office-Anwendung nicht installiert ist, können Sie ein [SKProductViewController](https://developer.apple.com/library/ios/documentation/StoreKit/Reference/SKITunesProductViewController_Ref/index.html)-Objekt verwenden, um den iTunes App Store in Ihrer Anwendung zu rendern und dem Benutzer die zu installierende Office-Anwendung anzuzeigen. In der folgenden Tabelle sind die jeweiligen iTunes-IDs aufgeführt, die für das Aufrufen der einzelnen Office-Anwendungen im Store Kit Product View Controller verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="dcb85-p106">If a particular Office application is not installed, you can use an [SKProductViewController](https://developer.apple.com/library/ios/documentation/StoreKit/Reference/SKITunesProductViewController_Ref/index.html) object to render the iTunes app store in your application and show the user the Office application to install. The following table lists the iTunes identifier to use to invoke each Office application in the Store Kit Product View Controller.</span></span> 
  
|<span data-ttu-id="dcb85-123">**Office-Anwendung**</span><span class="sxs-lookup"><span data-stu-id="dcb85-123">**Office application**</span></span>|<span data-ttu-id="dcb85-124">**iTunes-ID**</span><span class="sxs-lookup"><span data-stu-id="dcb85-124">**iTunes identifier**</span></span>|
|:-----|:-----|
|<span data-ttu-id="dcb85-125">Excel</span><span class="sxs-lookup"><span data-stu-id="dcb85-125">Excel</span></span>  <br/> |[<span data-ttu-id="dcb85-126"> https://itunes.apple.com/us/app/microsoft-excel/id586683407?mt=8&amp;uo=4</span><span class="sxs-lookup"><span data-stu-id="dcb85-126">https://itunes.apple.com/us/app/microsoft-excel/id586683407?mt=8&amp;uo=4</span></span>](https://itunes.apple.com/us/app/microsoft-excel/id586683407?mt=8&amp;uo=4) <br/> |
|<span data-ttu-id="dcb85-127">OneNote (iPhone)</span><span class="sxs-lookup"><span data-stu-id="dcb85-127">OneNote (iPhone)</span></span>  <br/> |[<span data-ttu-id="dcb85-128"> https://itunes.apple.com/us/app/microsoft-onenote-for-iphone/id410395246?mt=8&amp;uo=4</span><span class="sxs-lookup"><span data-stu-id="dcb85-128">https://itunes.apple.com/us/app/microsoft-onenote-for-iphone/id410395246?mt=8&amp;uo=4</span></span>](https://itunes.apple.com/us/app/microsoft-onenote-for-iphone/id410395246?mt=8&amp;uo=4) <br/> |
|<span data-ttu-id="dcb85-129">PowerPoint</span><span class="sxs-lookup"><span data-stu-id="dcb85-129">PowerPoint</span></span>  <br/> |[<span data-ttu-id="dcb85-130"> https://itunes.apple.com/us/app/microsoft-powerpoint/id586449534?mt=8&amp;uo=4</span><span class="sxs-lookup"><span data-stu-id="dcb85-130">https://itunes.apple.com/us/app/microsoft-powerpoint/id586449534?mt=8&amp;uo=4</span></span>](https://itunes.apple.com/us/app/microsoft-powerpoint/id586449534?mt=8&amp;uo=4) <br/> |
|<span data-ttu-id="dcb85-131">Word</span><span class="sxs-lookup"><span data-stu-id="dcb85-131">Word</span></span>  <br/> |[<span data-ttu-id="dcb85-132"> https://itunes.apple.com/us/app/microsoft-word/id586447913?mt=8&amp;uo=4</span><span class="sxs-lookup"><span data-stu-id="dcb85-132">https://itunes.apple.com/us/app/microsoft-word/id586447913?mt=8&amp;uo=4</span></span>](https://itunes.apple.com/us/app/microsoft-word/id586447913?mt=8&amp;uo=4) <br/> |
   
## <a name="invoke-office"></a><span data-ttu-id="dcb85-133">Aufrufen von Office</span><span class="sxs-lookup"><span data-stu-id="dcb85-133">Invoke Office</span></span>

<span data-ttu-id="dcb85-134">Wenn die Office-Anwendung installiert ist, kann die verweisende Anwendung Office durch Übergeben der folgenen Details aufrufen:</span><span class="sxs-lookup"><span data-stu-id="dcb85-134">When the Office application is installed, your referring application can invoke Office by passing the following details:</span></span> 
  
- <span data-ttu-id="dcb85-135">Office-Protokoll</span><span class="sxs-lookup"><span data-stu-id="dcb85-135">Office protocol</span></span>
    
- <span data-ttu-id="dcb85-136">Open-Modus</span><span class="sxs-lookup"><span data-stu-id="dcb85-136">Open mode</span></span>
    
- <span data-ttu-id="dcb85-137">URL</span><span class="sxs-lookup"><span data-stu-id="dcb85-137">URL</span></span>
    
- <span data-ttu-id="dcb85-138">Passback-Protokoll</span><span class="sxs-lookup"><span data-stu-id="dcb85-138">Passback protocol</span></span>
    
- <span data-ttu-id="dcb85-139">Dokumentenkontext</span><span class="sxs-lookup"><span data-stu-id="dcb85-139">Document context</span></span>
    
<span data-ttu-id="dcb85-140">Schemaformat:</span><span class="sxs-lookup"><span data-stu-id="dcb85-140">Schema format:</span></span>
  
 `<Office protocol><open mode>|u|<URL>|p|<passback protocol>|c|<document context>`
  
<span data-ttu-id="dcb85-141">Das folgende Beispiel zeigt eine Anforderung zum Aufrufen einer Word-Datei zur Bearbeitung:</span><span class="sxs-lookup"><span data-stu-id="dcb85-141">The following example shows a request to invoke a Word file for editing:</span></span>
  
 `ms-word:ofe|u|https://contoso/Q4/budget.docx|p|clouddrive|c|folderviewQ4`
  
### <a name="office-protocols"></a><span data-ttu-id="dcb85-142">Office-Protokolle</span><span class="sxs-lookup"><span data-stu-id="dcb85-142">Office protocols</span></span>

<span data-ttu-id="dcb85-143">Die folgende Tabelle enthält die Protokolle für jede Office-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="dcb85-143">The following table lists the protocols for each Office application.</span></span> 
  
|<span data-ttu-id="dcb85-144">**Anwendung**</span><span class="sxs-lookup"><span data-stu-id="dcb85-144">**Application**</span></span>|<span data-ttu-id="dcb85-145">**Protokoll**</span><span class="sxs-lookup"><span data-stu-id="dcb85-145">**Protocol**</span></span>|
|:-----|:-----|
|<span data-ttu-id="dcb85-146">Excel</span><span class="sxs-lookup"><span data-stu-id="dcb85-146">Excel</span></span>  <br/> |<span data-ttu-id="dcb85-147">ms-excel:</span><span class="sxs-lookup"><span data-stu-id="dcb85-147">ms-excel:</span></span>  <br/> |
|<span data-ttu-id="dcb85-148">OneNote</span><span class="sxs-lookup"><span data-stu-id="dcb85-148">OneNote</span></span>  <br/> |<span data-ttu-id="dcb85-149">onenote:</span><span class="sxs-lookup"><span data-stu-id="dcb85-149">onenote:</span></span>  <br/> |
|<span data-ttu-id="dcb85-150">PowerPoint</span><span class="sxs-lookup"><span data-stu-id="dcb85-150">PowerPoint</span></span>  <br/> |<span data-ttu-id="dcb85-151">ms-powerpoint:</span><span class="sxs-lookup"><span data-stu-id="dcb85-151">ms-powerpoint:</span></span>  <br/> |
|<span data-ttu-id="dcb85-152">Word</span><span class="sxs-lookup"><span data-stu-id="dcb85-152">Word</span></span>  <br/> |<span data-ttu-id="dcb85-153">ms-word:</span><span class="sxs-lookup"><span data-stu-id="dcb85-153">ms-word:</span></span>  <br/> |
   
### <a name="open-mode"></a><span data-ttu-id="dcb85-154">Open-Modus</span><span class="sxs-lookup"><span data-stu-id="dcb85-154">Open mode</span></span>

<span data-ttu-id="dcb85-p107">Office-Anwendungen können Dateien direkt im Ansichtsmodus (ofv) oder im Bearbeitungsmodus (ofe) öffnen. Der Bearbeitungsmodus ist Standard.</span><span class="sxs-lookup"><span data-stu-id="dcb85-p107">Office applications can open files directly into view (ofv) or edit (ofe) mode. Edit mode is the default.</span></span> 
  
<span data-ttu-id="dcb85-157">Schemaformat:</span><span class="sxs-lookup"><span data-stu-id="dcb85-157">Schema format:</span></span>
  
 `<ofv or ofe>`
  
### <a name="url"></a><span data-ttu-id="dcb85-158">URL</span><span class="sxs-lookup"><span data-stu-id="dcb85-158">URL</span></span>

<span data-ttu-id="dcb85-159">Die URL besteht aus drei Teilen:</span><span class="sxs-lookup"><span data-stu-id="dcb85-159">The URL includes three parts:</span></span> 
  
- <span data-ttu-id="dcb85-160">Der Deklaration, dass die Datei zum Bearbeiten geöffnet wird (ofe)</span><span class="sxs-lookup"><span data-stu-id="dcb85-160">The declaration that the file will be opened for edit (ofe)</span></span>
    
- <span data-ttu-id="dcb85-161">Dem URL-Deskriptor (|u|)</span><span class="sxs-lookup"><span data-stu-id="dcb85-161">The URL descriptor (|u|)</span></span>
    
- <span data-ttu-id="dcb85-162">Der URL</span><span class="sxs-lookup"><span data-stu-id="dcb85-162">The URL</span></span>
    
<span data-ttu-id="dcb85-p108">Die URL muss codiert sein und muss eine direkte Verbindung zu der Datei (keine Umleitung) sein. Wenn die URL ein Format aufweist, das Office nicht verarbeiten kann, oder einfach ein Downloadfehler auftritt, gibt Office den Benutzer nicht an die aufrufende Anwendung zurück.</span><span class="sxs-lookup"><span data-stu-id="dcb85-p108">The URL has to be encoded and must be a direct link to the file (not a redirect). If the URL is in a format that Office cannot handle, or the download simply fails, Office will not return the user to the invoking application.</span></span> 
  
<span data-ttu-id="dcb85-165">Schemaformat:</span><span class="sxs-lookup"><span data-stu-id="dcb85-165">Schema format:</span></span>
  
 `|u|<document URL>`
  
### <a name="passback-protocol-optional"></a><span data-ttu-id="dcb85-166">Passback-Protokoll (optional)</span><span class="sxs-lookup"><span data-stu-id="dcb85-166">Passback protocol (optional)</span></span>

<span data-ttu-id="dcb85-p109">Wenn Sie möchten, dass Office Benutzer an Ihre iOS-Anwendung zurückgibt, wenn diese auf den Pfeil "Zurück" klicken, muss die aufrufende Anwendung das Passback-Protokoll verwenden, das den Deskriptor '|p|' gefolgt vom App-Protokoll (ohne Doppelpunkt) umfasst. Sie müssen sicherstellen, dass die Anwendung die Antwort von Office korrekt verarbeiten kann.</span><span class="sxs-lookup"><span data-stu-id="dcb85-p109">If you want Office to return users to your iOS application when they choose the back arrow, the invoking application will need to use the passback protocol, which includes the descriptor '|p|' followed by the app protocol (without a colon). You'll need to ensure that your application can properly handle the response from Office.</span></span>
  
<span data-ttu-id="dcb85-169">Schemaformat:</span><span class="sxs-lookup"><span data-stu-id="dcb85-169">Schema format:</span></span>
  
 `|p|<passback protocol>`
  
### <a name="document-context-optional"></a><span data-ttu-id="dcb85-170">Dokumentenkontext (optional)</span><span class="sxs-lookup"><span data-stu-id="dcb85-170">Document context (optional)</span></span>

<span data-ttu-id="dcb85-p110">Office verwendet den Dokumentkontext nicht, die verweisende Anwendung benötigt diesen jedoch möglicherweise, wenn Office einen Benutzer zurückgibt. Wenn Sie möchten, dass der Dokumentkontext an Ihre Anwendung zurückgegeben wird, verwenden Sie den Deskriptor '|c|' gefolgt von dem gewünschten Kontext als Zeichenfolge. In Office gibt es (abgesehen von den Beschränkungen des Betriebssystems ) keine Längenbeschränkung für die Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="dcb85-p110">Office doesn't use the document context, but the referring application might need it when Office passes a user back. If you want the document context to be returned to your application, use the descriptor '|c|' followed by the context that you want as a string. Office does not limit the length of the string, beyond any limits imposed by the operating system.</span></span>
  
<span data-ttu-id="dcb85-174">Schemaformat:</span><span class="sxs-lookup"><span data-stu-id="dcb85-174">Schema format:</span></span>
  
 `|c|<document context>`
  
## <a name="return-users-to-the-referring-application"></a><span data-ttu-id="dcb85-175">Zurückgeben von Benutzern an die verweisende Anwendung</span><span class="sxs-lookup"><span data-stu-id="dcb85-175">Return users to the referring application</span></span>

<span data-ttu-id="dcb85-p111">Aus Sicherheitsgründen gibt Office nur Benutzer an die verweisende Andwendung zurück, wenn die Datei erfolgreich geöffnet wurde. Wenn der Benutzer den Pfeil "Zurück" auswählt, antwortet Office der aufrufenden Anwendung mit dem Passback-Protokoll, dem Open-Modus, der URL, dem ausstehenden Uploadstatus und dem Dokumentkontext. Der ausstehende Uploadstatus verwendet den Deskriptor |z| und ist entweder "ja" oder "nein".</span><span class="sxs-lookup"><span data-stu-id="dcb85-p111">For security reasons, Office only returns users to the referring application if the file opened successfully. When the user chooses the back arrow, Office responds to the invoking application with the passback protocol, open mode, URL, upload pending status, and document context. The upload pending status uses the descriptor |z|, and is either yes or no.</span></span>
  
<span data-ttu-id="dcb85-179">Schemaformat:</span><span class="sxs-lookup"><span data-stu-id="dcb85-179">Schema format:</span></span>
  
 `<app protocol>:ofe|u|<URL>|z|<yes or no>|c|<doc context> Example: clouddrive:ofe|u|https://contoso/Q4/budget.docx|z|no|c|folderviewQ4`
  
## <a name="see-also"></a><span data-ttu-id="dcb85-180">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dcb85-180">See also</span></span>
<span data-ttu-id="dcb85-181"><a name="bk_addresources"> </a></span><span class="sxs-lookup"><span data-stu-id="dcb85-181"><a name="bk_addresources"> </a></span></span>

- [<span data-ttu-id="dcb85-182">canOpenURL-Methode</span><span class="sxs-lookup"><span data-stu-id="dcb85-182">canOpenURL method</span></span>](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIApplication_Class/index.html)
    
- [<span data-ttu-id="dcb85-183">UIApplication-Klasse</span><span class="sxs-lookup"><span data-stu-id="dcb85-183">UIApplication class</span></span>](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIApplication_Class/index.html)
    
- [<span data-ttu-id="dcb85-184">SKProductViewController-Objekt</span><span class="sxs-lookup"><span data-stu-id="dcb85-184">SKProductViewController object</span></span>](https://developer.apple.com/library/ios/documentation/StoreKit/Reference/SKITunesProductViewController_Ref/index.html)
    

