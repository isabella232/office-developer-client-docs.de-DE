---
title: Integration in Office von Android-Anwendungen aus
manager: soliver
ms.date: 06/18/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: a765fa49-a272-4047-9147-59cc68e5dd27
description: Office für Android bietet eine erweiterbare Lösung, die die Integration in Drittanbieteranwendungen ermöglicht. Von Ihrer Android-Anwendung aus ist eine Integration in Office möglich, indem Sie Ihre Anwendungsbenutzer an Office übergeben.
ms.openlocfilehash: 2fd60c7e86d3390bc5343f3e09fb2235f97e0b13
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790853"
---
# <a name="integrate-with-office-from-android-applications"></a><span data-ttu-id="27c82-104">Integration in Office von Android-Anwendungen aus</span><span class="sxs-lookup"><span data-stu-id="27c82-104">Integrate with Office from Android applications</span></span>

<span data-ttu-id="27c82-p102">Office für Android bietet eine erweiterbare Lösung, die die Integration in Drittanbieteranwendungen ermöglicht. Von Ihrer Android-Anwendung aus ist eine Integration in Office möglich, indem Sie Ihre Anwendungsbenutzer an Office übergeben.</span><span class="sxs-lookup"><span data-stu-id="27c82-p102">Office for Android provides an extensible solution that enables integration with third-party applications. You can integrate with Office from your Android application by passing users from your application to Office.</span></span>
  
<span data-ttu-id="27c82-p103">Sie können Benutzern, die Office auf Android-Geräten ausführen, das Öffnen und Bearbeiten von in SharePoint oder OneDrive gespeicherten Dateien von einer beliebigen Anwendung aus ermöglichen. Übergeben Sie dazu mit dem Protokollhandler die Dateien an Office, und stellen Sie sicher, dass Office so aufgerufen wird, dass Office dies versteht.</span><span class="sxs-lookup"><span data-stu-id="27c82-p103">You can enable users who are running Office on an Android device to open and edit files stored in SharePoint or OneDrive from any application. To do this, you pass files to Office via protocol handlers, and you make sure that Office is invoked in a way that Office can understand.</span></span>
  
<span data-ttu-id="27c82-109">Wenn ein Benutzer das Bearbeiten einer Datei abgeschlossen hat, kann er „ZURÜCK" wählen, um zur ursprünglichen Speicheranwendung zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="27c82-109">When a user is done editing a file, they can choose the back key on the device to return to the original storage application.</span></span>
  
## <a name="verify-that-office-has-been-installed"></a><span data-ttu-id="27c82-110">Sicherstellen, dass Office installiert wurde</span><span class="sxs-lookup"><span data-stu-id="27c82-110">Verify that Office has been installed</span></span>

<span data-ttu-id="27c82-p104">Die verweisende Anwendung muss zunächst überprüfen, dass eine bestimmte Office-Anwendung installiert ist. Die folgenden Office-Anwendungen können auf Android-Geräten zum Anzeigen und Bearbeiten von Dokumenten installiert werden:</span><span class="sxs-lookup"><span data-stu-id="27c82-p104">Your referring application will first need to verify that a particular Office application is installed. The following Office applications can be installed on Android devices for document viewing and editing:</span></span> 
  
- <span data-ttu-id="27c82-113">Excel</span><span class="sxs-lookup"><span data-stu-id="27c82-113">Excel</span></span>
    
- <span data-ttu-id="27c82-114">PowerPoint</span><span class="sxs-lookup"><span data-stu-id="27c82-114">PowerPoint</span></span>
    
- <span data-ttu-id="27c82-115">Word</span><span class="sxs-lookup"><span data-stu-id="27c82-115">Word</span></span>
    
<span data-ttu-id="27c82-p105">Verwenden Sie PackageManager von Android, um zu ermitteln, ob eine bestimmte Office-Anwendung auf dem Gerät installiert ist. In der folgenden Tabelle sind die Paketnamen für Office-Anwendungen aufgeführt, die Sie in diesem Prozess verwenden können.</span><span class="sxs-lookup"><span data-stu-id="27c82-p105">Use Android PackageManager to determine whether a particular Office application is installed on the device. The following table lists the package names for the Office applications that you can use in this process.</span></span>
  
|<span data-ttu-id="27c82-118">**Anwendung**</span><span class="sxs-lookup"><span data-stu-id="27c82-118">**Application**</span></span>|<span data-ttu-id="27c82-119">**Name des Pakets**</span><span class="sxs-lookup"><span data-stu-id="27c82-119">**Package name**</span></span>|
|:-----|:-----|
|<span data-ttu-id="27c82-120">Excel</span><span class="sxs-lookup"><span data-stu-id="27c82-120">Excel</span></span>  <br/> |<span data-ttu-id="27c82-121">com.microsoft.office.excel</span><span class="sxs-lookup"><span data-stu-id="27c82-121">com.microsoft.office.excel</span></span>  <br/> |
|<span data-ttu-id="27c82-122">PowerPoint</span><span class="sxs-lookup"><span data-stu-id="27c82-122">PowerPoint</span></span>  <br/> |<span data-ttu-id="27c82-123">com.microsoft.office.powerpoint</span><span class="sxs-lookup"><span data-stu-id="27c82-123">com.microsoft.office.powerpoint</span></span>  <br/> |
|<span data-ttu-id="27c82-124">Word</span><span class="sxs-lookup"><span data-stu-id="27c82-124">Word</span></span>  <br/> |<span data-ttu-id="27c82-125">com.microsoft.office.word</span><span class="sxs-lookup"><span data-stu-id="27c82-125">com.microsoft.office.word</span></span>  <br/> |
   
### <a name="prompt-the-user-to-install-office"></a><span data-ttu-id="27c82-126">Auffordern des Benutzers zur Installation von Office</span><span class="sxs-lookup"><span data-stu-id="27c82-126">Prompt the user to install Office</span></span>

<span data-ttu-id="27c82-p106">Wenn eine bestimmte Office-Anwendung nicht installiert ist, kann der Benutzer zum Installieren der Anwendung aufgefordert werden. In der folgenden Tabelle sind die verfügbaren Installationsorte für Office-Anwendungen aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="27c82-p106">If a particular Office application is not installed, you can prompt the user to install the application. The following table lists the available install locations for Office applications.</span></span>
  
|<span data-ttu-id="27c82-129">**Anwendung**</span><span class="sxs-lookup"><span data-stu-id="27c82-129">**Application**</span></span>|<span data-ttu-id="27c82-130">**Google Play Store**</span><span class="sxs-lookup"><span data-stu-id="27c82-130">**Google Play Store**</span></span>|
|:-----|:-----|
|<span data-ttu-id="27c82-131">Excel</span><span class="sxs-lookup"><span data-stu-id="27c82-131">Excel</span></span>  <br/> |[https://play.google.com/store/apps/details?id=com.microsoft.office.excel](https://play.google.com/store/apps/details?id=com.microsoft.office.excel) <br/> |
|<span data-ttu-id="27c82-132">PowerPoint</span><span class="sxs-lookup"><span data-stu-id="27c82-132">PowerPoint</span></span>  <br/> |[https://play.google.com/store/apps/details?id=com.microsoft.office.powerpoint](https://play.google.com/store/apps/details?id=com.microsoft.office.powerpoint) <br/> |
|<span data-ttu-id="27c82-133">Word</span><span class="sxs-lookup"><span data-stu-id="27c82-133">Word</span></span>  <br/> |[https://play.google.com/store/apps/details?id=com.microsoft.office.word](https://play.google.com/store/apps/details?id=com.microsoft.office.word) <br/> |
   
## <a name="invoke-office"></a><span data-ttu-id="27c82-134">Aufrufen von Office</span><span class="sxs-lookup"><span data-stu-id="27c82-134">Invoke Office</span></span>

<span data-ttu-id="27c82-135">Wenn die Office-Anwendung installiert ist, kann die verweisende Anwendung Office durch Übergeben der folgenen Details aufrufen:</span><span class="sxs-lookup"><span data-stu-id="27c82-135">When the Office application is installed, your referring application can invoke Office by passing the following details:</span></span>
  
- <span data-ttu-id="27c82-136">Office-Protokoll</span><span class="sxs-lookup"><span data-stu-id="27c82-136">Office protocol</span></span>
    
- <span data-ttu-id="27c82-137">Open-Modus</span><span class="sxs-lookup"><span data-stu-id="27c82-137">Open mode</span></span>
    
- <span data-ttu-id="27c82-138">URL</span><span class="sxs-lookup"><span data-stu-id="27c82-138">URL</span></span>
    
<span data-ttu-id="27c82-139">Schemaformat:</span><span class="sxs-lookup"><span data-stu-id="27c82-139">Schema format:</span></span>
  
 `<Office protocol><open mode>|u|<URL>`
  
<span data-ttu-id="27c82-140">Das folgende Beispiel zeigt eine Anforderung zum Aufrufen einer Word-Datei zur Bearbeitung:</span><span class="sxs-lookup"><span data-stu-id="27c82-140">The following example shows a request to invoke a Word file for editing.</span></span>
  
 `ms-word:ofe|u|https://contoso/Q4/budget.docx`
  
### <a name="office-protocols"></a><span data-ttu-id="27c82-141">Office-Protokolle</span><span class="sxs-lookup"><span data-stu-id="27c82-141">Office protocols</span></span>

<span data-ttu-id="27c82-142">Die folgende Tabelle enthält die Protokolle für jede Office-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="27c82-142">The following table lists the protocols for each Office application.</span></span>
  
|<span data-ttu-id="27c82-143">**Anwendung**</span><span class="sxs-lookup"><span data-stu-id="27c82-143">**Application**</span></span>|<span data-ttu-id="27c82-144">**Protocol**</span><span class="sxs-lookup"><span data-stu-id="27c82-144">**Protocol**</span></span>|
|:-----|:-----|
|<span data-ttu-id="27c82-145">Excel</span><span class="sxs-lookup"><span data-stu-id="27c82-145">Excel</span></span>  <br/> |<span data-ttu-id="27c82-146">ms-excel:</span><span class="sxs-lookup"><span data-stu-id="27c82-146">ms-excel:</span></span>  <br/> |
|<span data-ttu-id="27c82-147">PowerPoint</span><span class="sxs-lookup"><span data-stu-id="27c82-147">PowerPoint</span></span>  <br/> |<span data-ttu-id="27c82-148">ms-powerpoint:</span><span class="sxs-lookup"><span data-stu-id="27c82-148">ms-powerpoint:</span></span>  <br/> |
|<span data-ttu-id="27c82-149">Word</span><span class="sxs-lookup"><span data-stu-id="27c82-149">Word</span></span>  <br/> |<span data-ttu-id="27c82-150">ms-word:</span><span class="sxs-lookup"><span data-stu-id="27c82-150">ms-word:</span></span>  <br/> |
   
### <a name="open-mode"></a><span data-ttu-id="27c82-151">Open-Modus</span><span class="sxs-lookup"><span data-stu-id="27c82-151">Open mode</span></span>

<span data-ttu-id="27c82-p107">Office-Anwendungen können Dateien direkt im Ansichtsmodus (ofv) oder im Bearbeitungsmodus (ofe) öffnen. Der Bearbeitungsmodus ist Standard.</span><span class="sxs-lookup"><span data-stu-id="27c82-p107">Office applications can open files directly into view (ofv) or edit (ofe) mode. Edit mode is the default.</span></span>
  
<span data-ttu-id="27c82-154">Schemaformat:</span><span class="sxs-lookup"><span data-stu-id="27c82-154">Schema format:</span></span>
  
 `<ofv or ofe>`
  
### <a name="url"></a><span data-ttu-id="27c82-155">URL</span><span class="sxs-lookup"><span data-stu-id="27c82-155">URL</span></span>

<span data-ttu-id="27c82-156">Die URL besteht aus drei Teilen:</span><span class="sxs-lookup"><span data-stu-id="27c82-156">The URL includes three parts:</span></span>
  
- <span data-ttu-id="27c82-157">Der Deklaration, dass die Datei zum Bearbeiten geöffnet wird (ofe)</span><span class="sxs-lookup"><span data-stu-id="27c82-157">The declaration that the file will be opened for edit (ofe)</span></span>
    
- <span data-ttu-id="27c82-158">Dem URL-Deskriptor (|u|)</span><span class="sxs-lookup"><span data-stu-id="27c82-158">The URL descriptor (|u|)</span></span>
    
- <span data-ttu-id="27c82-159">Der URL</span><span class="sxs-lookup"><span data-stu-id="27c82-159">The URL</span></span>
    
<span data-ttu-id="27c82-p108">Die URL muss codiert sein und muss eine direkte Verbindung zu der Datei (keine Umleitung) sein. Wenn die URL ein Format aufweist, das Office nicht verarbeiten kann, oder einfach ein Downloadfehler auftritt, gibt Office den Benutzer nicht an die aufrufende Anwendung zurück.</span><span class="sxs-lookup"><span data-stu-id="27c82-p108">The URL has to be encoded and must be a direct link to the file (not a redirect). If the URL is in a format that Office cannot handle, or the download simply fails, Office will not return the user to the invoking application.</span></span>
  
<span data-ttu-id="27c82-162">Schemaformat:</span><span class="sxs-lookup"><span data-stu-id="27c82-162">Schema format:</span></span>
  
 `|u|<document URL>`
  
## <a name="see-also"></a><span data-ttu-id="27c82-163">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="27c82-163">See also</span></span>
<span data-ttu-id="27c82-164"><a name="bk_addresources"> </a></span><span class="sxs-lookup"><span data-stu-id="27c82-164"></span></span>

- [<span data-ttu-id="27c82-165">Integration in Office</span><span class="sxs-lookup"><span data-stu-id="27c82-165">Integrate with Office</span></span>](integrate-with-office.md)
    
- [<span data-ttu-id="27c82-166">PackageManager</span><span class="sxs-lookup"><span data-stu-id="27c82-166">PackageManager</span></span>](http://developer.android.com/reference/android/content/pm/PackageManager.html)
    
- [<span data-ttu-id="27c82-167">GetPackageManager()</span><span class="sxs-lookup"><span data-stu-id="27c82-167">GetPackageManager()</span></span>](http://developer.android.com/reference/android/content/Context.html)
    

