---
title: Integrieren von Chatanwendungen in Office
manager: soliver
ms.date: 07/25/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: beba316b-1dfe-4e1b-adae-42418906c177
description: In diesem Artikel wird beschrieben, wie Sie eine Clientanwendung für Sofortnachrichten konfigurieren, sodass Features für soziale Netzwerke in Office 2013 integriert sind,u. a. Anzeigen von Anwesenheitsinformationen und Senden von Sofortnachrichten von der Visitenkarte aus.
ms.openlocfilehash: 383aac24be347cf637d9e2f255623035eea8bc40
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796322"
---
# <a name="integrating-im-applications-with-office"></a><span data-ttu-id="f64cd-103">Integrieren von Chatanwendungen in Office</span><span class="sxs-lookup"><span data-stu-id="f64cd-103">Integrating IM applications with Office</span></span>

<span data-ttu-id="f64cd-104">In diesem Artikel wird beschrieben, wie Sie eine Clientanwendung für Sofortnachrichten konfigurieren, sodass Features für soziale Netzwerke in Office 2013 integriert sind,u. a. Anzeigen von Anwesenheitsinformationen und Senden von Sofortnachrichten von der Visitenkarte aus.</span><span class="sxs-lookup"><span data-stu-id="f64cd-104">This article describes how to configure an instant message (IM) client application so that it integrates with the social features in Office 2013, including displaying presence and sending instant messages from the contact card.</span></span>
  
<span data-ttu-id="f64cd-105">Wenn Sie Fragen oder Anmerkungen zu diesem technischen Artikel oder zu Prozessen haben, die hier beschrieben werden, können Sie sich direkt per E-Mail unter [docthis@microsoft.com](mailto:docthis@microsoft.com) an Microsoft wenden.</span><span class="sxs-lookup"><span data-stu-id="f64cd-105">If you have any questions or comments about this technical article or the processes that it describes, you can contact Microsoft directly by sending an email to [docthis@microsoft.com](mailto:docthis@microsoft.com).</span></span>
  
## <a name="introduction"></a><span data-ttu-id="f64cd-106">Einführung</span><span class="sxs-lookup"><span data-stu-id="f64cd-106">Introduction</span></span>
<span data-ttu-id="f64cd-107"><a name="off15_IMIntegration_Intro"> </a></span><span class="sxs-lookup"><span data-stu-id="f64cd-107"></span></span>

<span data-ttu-id="f64cd-p101">Office 2013 ermöglicht die umfassende Integration mit Clientanwendungen für Chatnachrichten, einschließlich Lync 2013. Diese Integration bietet Benutzern Chat-Funktionen innerhalb von Word 2013, Excel 2013, PowerPoint 2013, Outlook 2013, Visio 2013, Project 2013 und OneNote 2013 sowie ermöglicht die Anwesenheitsintegration auf SharePoint 2013-Seiten. Benutzer können Foto, Name, Anwesenheitsstatus und Kontaktdaten für Personen in ihrer Kontaktliste sehen. Sie können Chats, Videoanrufe oder Anrufe direkt von der Visitenkarte (das Benutzeroberflächen-Element inOffice 2013 mit Kontaktinformationen und Kommunikationsoptionen) aus durchführen. Office 2013 erleichtert es, mit Kontakten direkt innerhalb von E-Mails oder Dokumenten in Verbindung zu bleiben.</span><span class="sxs-lookup"><span data-stu-id="f64cd-p101">Office 2013 provides rich integration with IM client applications, including Lync 2013. This integration provides users with IM capabilities from within Word 2013, Excel 2013, PowerPoint 2013, Outlook 2013, Visio 2013, Project 2013, and OneNote 2013 as well as providing presence integration on SharePoint 2013 pages. Users can see the photo, name, presence status, and contact data for people in their contacts list. They can start an IM session, video call, or phone call directly from the contact card (the UI element in Office 2013 that surfaces contact information and communication options). Office 2013 makes it easy to stay connected to your contacts without taking you outside of your email or documents.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="f64cd-p102">In diesem Artikel wird der Begriff Clientanwendung für Chatnachrichten verwendet, mit dem speziell die auf dem Benutzercomputer installierte Anwendung gemeint ist, die mit dem Chatdienst kommuniziert. Lync 2013gilt z. B. als eine Clientanwendung für Chatnachrichten. Dieser Artikel enthält keine detaillierten Informationen zur Kommunikation der Clientanwendung für Chatnachrichten mit dem Chatdienst und dem Chatdienst an sich.</span><span class="sxs-lookup"><span data-stu-id="f64cd-p102">This article uses the term IM client application to refer specifically to the application installed on a user's computer that communicates to the IM service. For example, Lync 2013 is considered an IM client application. This article does not provide details about how the IM client application communicates to the IM service or about the IM service itself.</span></span> 
  
<span data-ttu-id="f64cd-p103">Sie können eine Clientanwendung für Chatnachrichten so anpassen, dass diese mit Office kommuniziert. Sie können insbesondere Ihre Chatanwendung zum Anzeigen der folgenden Informationen innerhalb der Office-Benutzeroberfläche anpassen:</span><span class="sxs-lookup"><span data-stu-id="f64cd-p103">You can customize an IM client application so that it communicates with Office. Specifically, you can modify your IM application so that it displays the following information within the Office UI:</span></span>
  
- <span data-ttu-id="f64cd-118">Foto des Kontakts</span><span class="sxs-lookup"><span data-stu-id="f64cd-118">Contact photo.</span></span>
    
- <span data-ttu-id="f64cd-119">Name des Kontakts</span><span class="sxs-lookup"><span data-stu-id="f64cd-119">Contact name.</span></span>
    
- <span data-ttu-id="f64cd-120">Persönlicher Statushinweis des Kontakts</span><span class="sxs-lookup"><span data-stu-id="f64cd-120">Contact personal status note.</span></span>
    
- <span data-ttu-id="f64cd-121">Anwesenheitsstatus des Kontakts</span><span class="sxs-lookup"><span data-stu-id="f64cd-121">Contact presence status.</span></span>
    
- <span data-ttu-id="f64cd-122">Zeichenfolge zur Verfügbarkeit des Kontakts (z. B. „Verfügbar“ oder „Abwesend“).</span><span class="sxs-lookup"><span data-stu-id="f64cd-122">Contact availability string (for example, "Available" or "Out of Office").</span></span>
    
- <span data-ttu-id="f64cd-123">Zeichenfolge zu unterstützten Chatfunktionen des Kontakts (z. B. „Videomodus möglich“).</span><span class="sxs-lookup"><span data-stu-id="f64cd-123">Contact capability string (for example, "Video Ready").</span></span>
    
- <span data-ttu-id="f64cd-124">Chat starten mit einem Klick</span><span class="sxs-lookup"><span data-stu-id="f64cd-124">One-click IM launch.</span></span>
    
- <span data-ttu-id="f64cd-125">Videoanruf starten mit einem Klick</span><span class="sxs-lookup"><span data-stu-id="f64cd-125">One-click video call launch.</span></span>
    
- <span data-ttu-id="f64cd-126">Anruf starten mit einem Klick (SIP, Telefonnummer, Voicemail und neue Anrufnummer)</span><span class="sxs-lookup"><span data-stu-id="f64cd-126">One-click phone call launch (including SIP, phone number, voice mail, and call new number).</span></span>
    
- <span data-ttu-id="f64cd-127">Kontaktverwaltung (zur Chatgruppe hinzufügen)</span><span class="sxs-lookup"><span data-stu-id="f64cd-127">Contact management (add to IM group).</span></span>
    
- <span data-ttu-id="f64cd-128">Standort und Zeitzone des Kontakts</span><span class="sxs-lookup"><span data-stu-id="f64cd-128">Contact location and time zone.</span></span>
    
- <span data-ttu-id="f64cd-129">Kontaktdaten, Telefonnummer, E-Mail-Adresse, Titel und Name des Unternehmens</span><span class="sxs-lookup"><span data-stu-id="f64cd-129">Contact data, phone number, email address, title, and company name.</span></span>
    
<span data-ttu-id="f64cd-130">**Abbildung 1. Visitenkarte in Office 2013**</span><span class="sxs-lookup"><span data-stu-id="f64cd-130">**Figure 1. Contact card in Office 2013**</span></span>

<span data-ttu-id="f64cd-131">![Personen-Karte in Office 2013](media/ocom15_peoplecard.png "Personen-Karte in Office 2013")</span><span class="sxs-lookup"><span data-stu-id="f64cd-131">![The People Card in Office 2013](media/ocom15_peoplecard.png "The People Card in Office 2013")</span></span>
  
<span data-ttu-id="f64cd-p104">Um diese Integration in Office zu ermöglichen, müssen in einer Clientanwendung für Chatnachrichten Schnittstellen implementiert werden, mit denen Office eine Verbindung mit dieser herstellen kann. Die APIs für diese Integration sind im [UCCollborationLib](http://msdn.microsoft.com/en-au/library/uccollaborationlib.aspx)-Namespace in der Datei „Microsoft.Office.UC.dll" enthalten, die mit Versionen von Office 2013 installiert wird, die Lync/Skype for Business umfassen. Der **UCCollaborationLib**-Namespace enthält die Schnittstellen, die Sie für die Integration in Office implementieren müssen.</span><span class="sxs-lookup"><span data-stu-id="f64cd-p104">To enable this integration with Office, an IM client application must implement a set of interfaces that Office provides to connect to it. The APIs for this integration are included in the [UCCollborationLib](http://msdn.microsoft.com/en-au/library/uccollaborationlib.aspx) namespace that is contained in the Microsoft.Office.UC.dll file, which is installed with versions of Office 2013 that include Lync / Skype for Business. The **UCCollaborationLib** namespace includes the interfaces that you must implement to integrate with Office.</span></span> 
  
> [!IMPORTANT] 
> <span data-ttu-id="f64cd-135">Die Typbibliothek für die erforderlichen Schnittstellen ist in Lync 2013/Skype for Business eingebettet.</span><span class="sxs-lookup"><span data-stu-id="f64cd-135">Important: The type library for the required interfaces is embedded in Lync 2013/Skype for Business.</span></span> <span data-ttu-id="f64cd-136">Für Drittanbieter-Systemintegratoren funktioniert dies nur, wenn sowohl Lync 2013 als auch Skype for Business auf dem Zielcomputer installiert sind.</span><span class="sxs-lookup"><span data-stu-id="f64cd-136">For third-party integrators, this works only when both Lync 2013 and Skype for Business are installed on the target machine.</span></span> <span data-ttu-id="f64cd-137">Wenn Sie die Integration mit Office Standard ausführen, müssen Sie die Typbibliothek extrahieren und auf dem Zielcomputer installieren.</span><span class="sxs-lookup"><span data-stu-id="f64cd-137">If you are integrating using Office Standard, you need to extract the type library and install it on the target machine.</span></span> <span data-ttu-id="f64cd-138">Das [Lync 2013 SDK](https://www.microsoft.com/en-us/download/details.aspx?id=36824) enthält die Datei Microsoft.Office.UC.dll.</span><span class="sxs-lookup"><span data-stu-id="f64cd-138">The [Lync 2013 SDK](https://www.microsoft.com/en-us/download/details.aspx?id=36824) includes the Microsoft.Office.UC.dll file.</span></span> 
  
> [!NOTE]
>  <span data-ttu-id="f64cd-139">Eine Handvoll von Office 2010-Anwendungen können auf ähnliche Weise in einer Drittanbieter-Chatanwendung integriert werden: Outlook 2010, Word 2010, Excel 2010, PowerPoint 2010 und SharePoint Server 2010 (unter Verwendung eines ActiveX-Steuerelements).</span><span class="sxs-lookup"><span data-stu-id="f64cd-139">A handful of Office 2010 applications can integrate similarly with a third-party IM provider application: Outlook 2010, Word 2010, Excel 2010, PowerPoint 2010, and SharePoint Server 2010 (using an ActiveX control).</span></span> <span data-ttu-id="f64cd-140">Viele der für die Integration in Office 2013 erforderlichen Schritte gelten auch für Office 2010.</span><span class="sxs-lookup"><span data-stu-id="f64cd-140">Many of the steps required for integration with Office 2013 apply to Office 2010 as well.</span></span> <span data-ttu-id="f64cd-141">Es gibt einige wichtige Unterschiede bei der Integration von Office 2010 in einer Chatanbieteranwendung:</span><span class="sxs-lookup"><span data-stu-id="f64cd-141">There are several key differences in how off14short integrates with an IM provider application:</span></span> 
>  - <span data-ttu-id="f64cd-142">In Office 2010 wird das Kontakt-Foto nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f64cd-142">off14short does not display the contact's photo.</span></span> 
>  - <span data-ttu-id="f64cd-143">Sie müssen die Datei Microsoft.Office.Uc.dll separat von Office 2010 herunterladen.</span><span class="sxs-lookup"><span data-stu-id="f64cd-143">>  You must download the Microsoft.Office.Uc.dll file separately from Office 2010.</span></span> <span data-ttu-id="f64cd-144">Das [Lync 2010 SDK ](http://www.microsoft.com/en-us/download/details.aspx?id=18898) enthält die Datei Microsoft.Office.UC.dll für Office 2010.</span><span class="sxs-lookup"><span data-stu-id="f64cd-144">The [Lync 2010 SDK](http://www.microsoft.com/en-us/download/details.aspx?id=18898) includes the Microsoft.Office.UC.dll file for Office 2010.</span></span> 
>  - <span data-ttu-id="f64cd-145">Wenn die Office-Anwendung die [IUCOfficeIntegration.GetAuthenticationInfo](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IUCOfficeIntegration)-Methode in einer Clientanwendung für Chatnachrichten aufruft, übergibt diese die Zeichenfolge „14.0.0.0“.</span><span class="sxs-lookup"><span data-stu-id="f64cd-145">When the Office application calls the [IUCOfficeIntegration.GetAuthenticationInfo](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IUCOfficeIntegration) method on the IM client application, it passes in the string "14.0.0.0".</span></span> 
>  - <span data-ttu-id="f64cd-146">Office 2010 listet alle Gruppen und Kontakte auf, sobald es eine Verbindung zu einer Clientanwendung für Chatnachrichten herstellt.</span><span class="sxs-lookup"><span data-stu-id="f64cd-146">>  Office 2010 enumerates all groups and contacts as soon as it connects to an IM client application.</span></span> 
  
## <a name="how-office-integrates-with-an-im-client-application"></a><span data-ttu-id="f64cd-147">Integration von Office in einer Clientanwendung für Chatnachrichten</span><span class="sxs-lookup"><span data-stu-id="f64cd-147">How Office integrates with an IM client application</span></span>
<span data-ttu-id="f64cd-148"><a name="off15_IMIntegration_How"> </a></span><span class="sxs-lookup"><span data-stu-id="f64cd-148"></span></span>

<span data-ttu-id="f64cd-149">Wenn ein Office 2013-Anwendung gestartet wird, durchläuft sie den folgenden Prozess bei der Integration in einer standardmäßigen Clientanwendung für Chatnachrichten:</span><span class="sxs-lookup"><span data-stu-id="f64cd-149">When an Office 2013 application starts, it goes through the following process to integrate with the default IM client application:</span></span>
  
1. <span data-ttu-id="f64cd-150">Sie prüft die Registrierung, um die standardmäßige Clientanwendung für Chatnachrichten zu ermitteln, und stellt dann eine Verbindung mit dieser her.</span><span class="sxs-lookup"><span data-stu-id="f64cd-150">It checks the registry to discover the default IM client application and then connects to it.</span></span>
    
2. <span data-ttu-id="f64cd-151">Sie authentifiziert die Clientanwendung für Chatnachrichten.</span><span class="sxs-lookup"><span data-stu-id="f64cd-151">It authenticates with the IM client application.</span></span>
    
3. <span data-ttu-id="f64cd-152">Sie stellt eine Verbindung mit bestimmten Schnittstellen her, die von der Clientanwendung für Chatnachrichten bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="f64cd-152">It connects to specific interfaces that are exposed by the IM client application.</span></span>
    
4. <span data-ttu-id="f64cd-153">Sie ermittelt die von dem aktuell angemeldeten (lokalen) Benutzer unterstützte Funktionen, u. a. Kontakte des Benutzers, Anwesenheitsinformationen und unterstützte Chatfunktionen (Chatnachrichten, Videoanrufe, VOIP usw.).</span><span class="sxs-lookup"><span data-stu-id="f64cd-153">It determines the capabilities of the currently signed-in user (local user), including getting the user's contacts, determining the user's presence, and determining the user's IM capabilities (instant messaging, video chat, VOIP, and so on).</span></span>
    
5. <span data-ttu-id="f64cd-154">Sie ruft Anwesenheitsinformationen für die Kontakte des lokalen Benutzers ab.</span><span class="sxs-lookup"><span data-stu-id="f64cd-154">It gets presence information for the local user's contacts.</span></span>
    
6. <span data-ttu-id="f64cd-155">Wenn die Clientanwendung für Chatnachrichten beendet wird, wird die Verbindung mit der Office 2013-Anwendung im Hintergrund getrennt.</span><span class="sxs-lookup"><span data-stu-id="f64cd-155">When the IM client application shuts down, the Office 2013 application silently disconnects.</span></span>
    
### <a name="discovering-the-im-application"></a><span data-ttu-id="f64cd-156">Ermitteln der Chatanwendung</span><span class="sxs-lookup"><span data-stu-id="f64cd-156">Discovering the IM application</span></span>

<span data-ttu-id="f64cd-p108">Die Office-Anwendung sucht nach bestimmten Schlüsseln und Einträge in der Registrierung, um die standardmäßige Clientanwendung für Chatnachrichten zu ermitteln. Wenn eine standardmäßigen Clientanwendung für Chatnachrichten festgestellt wird, versucht die Anwendung eine Verbindung mit dieser herzustellen.</span><span class="sxs-lookup"><span data-stu-id="f64cd-p108">The Office application looks for several specific keys and entries in the registry to discover the default IM client application. If it discovers a default IM client application, it then attempts to connect to it.</span></span>
  
<span data-ttu-id="f64cd-159">Der Prozess, den die Office-Anwendung durchläuft, um die standardmäßige Clientanwendung für Chatnachrichten zu ermitteln, ist der folgendende:</span><span class="sxs-lookup"><span data-stu-id="f64cd-159">The process that the Office application goes through to discover the default IM client application is as follows:</span></span>
  
1. <span data-ttu-id="f64cd-160">Die Office-Anwendung prüft, ob der Unterschlüssel „HKEY_CURRENT_USER\Software\IM Providers\DefaultIMApp“ in der Registrierung festgelegt ist, und liest den dort aufgeführten Anwendungsnamen.</span><span class="sxs-lookup"><span data-stu-id="f64cd-160">The Office application looks to see if the HKEY_CURRENT_USER\Software\IM Providers\DefaultIMApp subkey in the registry is set and reads the application name listed there.</span></span>
    
2. <span data-ttu-id="f64cd-161">Anschließend liest die Office-Anwendung den Schlüssel „HKEY_CURRENT_USER\Software\IM Providers\ _Application name_\UpAndRunning" Schlüssel und prüft den Wert auf Änderungen.</span><span class="sxs-lookup"><span data-stu-id="f64cd-161">The Office application then reads the HKEY_CURRENT_USER\Software\IM Providers\ _Application name_\UpAndRunning key and monitors the value for changes.</span></span>
    
3. <span data-ttu-id="f64cd-162">Als nächstes liest die Office-Anwendung den Registrierungsschlüssel „HKEY_LOCAL_MACHINE\Software\IM Providers\ _Application name_" und ruft die dort gespeicherten ProcessName- und Klassen-ID (CLSID)-Werte ab.</span><span class="sxs-lookup"><span data-stu-id="f64cd-162">The Office application next reads the HKEY_LOCAL_MACHINE\Software\IM Providers\ _Application name_ registry key and gets the ProcessName and class ID (CLSID) values stored there.</span></span> 
    
4. <span data-ttu-id="f64cd-163">Sobald die Clientanwendung für Chatnachrichten ihre Startsequenz erfolgreich abgeschlossen und alle Klassen für die Anwesenheitsintegration ordnungsgemäß registriert hat, legt sie den Schlüssel „HKEY_CURRENT_USER\Software\IM Providers\ _Application name_\UpAndRunning" auf den Wert „2" fest, der angibt, dass die Clientanwendung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f64cd-163">Once the IM client application has completed its start sequence successfully and registered all of the classes correctly for the presence integration, it sets the HKEY_CURRENT_USER\Software\IM Providers\ _Application name_\UpAndRunning key to "2", indicating that the client application is running.</span></span>
    
5. <span data-ttu-id="f64cd-164">Wenn die Office-Anwendung feststellt, dass der Schlüssel „HKEY_CURRENT_USER\Software\IM Providers\ _Application name_\UpAndRunning" auf den Wert „2" festgelegt wurde, prüft sie die Liste der ausgeführten Prozesse auf dem Computer auf den Prozessnamen der Clientanwendung für Chatnachrichten.</span><span class="sxs-lookup"><span data-stu-id="f64cd-164">When the Office application discovers that the HKEY_CURRENT_USER\Software\IM Providers\ _Application name_\UpAndRunning key has been set to "2", it checks the list of running processes on the computer for the process name of the IM client application.</span></span>
    
6. <span data-ttu-id="f64cd-165">Findet die Office-Anwendung den von der Clientanwendung für Chatnachrichten verwendeten Prozess, ruft die Office-Anwendung mit der CLSID **CoCreateInstance** auf, um eine Verbindung mit der Clientanwendung für Chatnachrichten als COM-Server ohne Prozesse herzustellen.</span><span class="sxs-lookup"><span data-stu-id="f64cd-165">Once the Office application finds the process that the IM client application uses, the Office application calls **CoCreateInstance** using the CLSID to establish a connection to the IM client application as an out-of-process COM server.</span></span> 
    
### <a name="authenticating-the-connection-to-the-im-application"></a><span data-ttu-id="f64cd-166">Authentifizieren der Verbindung mit der Chatanwendung</span><span class="sxs-lookup"><span data-stu-id="f64cd-166">Authenticating the connection to the IM application</span></span>

<span data-ttu-id="f64cd-167">Nachdem die Office-Anwendung eine Verbindung mit der Clientanwendung für Chatnachrichten hergestellt hat, führt sie die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="f64cd-167">After the Office application establishes a connection to the IM client application, it then does the following:</span></span>
  
1. <span data-ttu-id="f64cd-168">Die Office-Anwendung ruft die [IUnknown::QueryInterface](http://msdn.microsoft.com/de-DE/library/ms682521%28v=VS.85%29.aspx)-Methode auf, um nach der [IUCOfficeIntegration](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IUCOfficeIntegration)-Schnittstelle zu suchen.</span><span class="sxs-lookup"><span data-stu-id="f64cd-168">The Office application calls [IUnknown::QueryInterface](http://msdn.microsoft.com/de-DE/library/ms682521%28v=VS.85%29.aspx) method to check for the [IUCOfficeIntegration](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IUCOfficeIntegration) interface.</span></span> 
    
2. <span data-ttu-id="f64cd-169">Anschließend ruft die Office-Anwendung die **IUCOfficeIntegration.GetAuthenticationInfo**-Methode auf und übergibt die höchste unterstützte Integrationsversion (z. B. „15.0.0.0").</span><span class="sxs-lookup"><span data-stu-id="f64cd-169">The Office application then calls the **IUCOfficeIntegration.GetAuthenticationInfo** method, passing in the highest supported integration version (for example, "15.0.0.0").</span></span> 
    
3. <span data-ttu-id="f64cd-170">Wenn die als Parameter übergebene Office-Version von der Clientanwendung für Chatnachrichten unterstützt wird, gibt die Anwendung die folgende hartcodierte XML-Zeichenfolge an den aufrufenden Code zurück:</span><span class="sxs-lookup"><span data-stu-id="f64cd-170">If the IM client application supports the version of Office passed in as a parameter, the application returns the following hard-coded XML string to the calling code:</span></span>
    
    `<authenticationinfo>`
    
   > [!NOTE]
   > <span data-ttu-id="f64cd-171">Aufgrund der Kompatibilität mit Vorversionen muss die Clientanwendung für Chatnachrichten den exakten Wert „ `<authenticationinfo>`" für den Aufruf von **GetAuthenticationInfo** zurückgeben, wenn die als Parameter übergebene Office-Version von dieser Anwendung unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="f64cd-171">For legacy reasons, the IM client application must return the exact value  `<authenticationinfo>` to the call to **GetAuthenticationInfo** if it supports the version of Office passed in as a parameter.</span></span> 
  
4. <span data-ttu-id="f64cd-172">Tritt beim Zurückgeben eines Werts durch die Clientanwendung für Chatnachrichten ein Fehler auf, ruft die Office-Anwendung erneut die **GetAuthenticationInfo**-Methode mit der nächsten höchsten unterstützten Version von Office (z. B. „14.0.0.0") auf.</span><span class="sxs-lookup"><span data-stu-id="f64cd-172">If the IM client application fails to return a value, the Office application calls the **GetAuthenticationInfo** method again with the next highest supported version of Office (for example, "14.0.0.0").</span></span> 
    
5. <span data-ttu-id="f64cd-p109">Nachdem Office festgestellt hat, dass die Chat- und Anwesenheitsintegration von der Clientanwendung für Chatnachrichten unterstützt wird, stellt es eine Verbindung mit den erforderlichen Schnittstellen her, um die Initialisierung abzuschließen. (Weitere Informationen finden Sie unter [Herstellen einer Verbindung mit den erforderlichen Schnittstellen](#off15_IMIntegration_HowConnect).)</span><span class="sxs-lookup"><span data-stu-id="f64cd-p109">Once Office determines that the IM client application supports IM and presence integration, it connects to a required set of interfaces to finish initializing. (For more information, see [Connecting to required interfaces](#off15_IMIntegration_HowConnect).)</span></span>
    
<span data-ttu-id="f64cd-175">Stellt die Office-Anwendung in einem der oben genannten Schritte einen Fehler fest, zieht sie sich zurück, und die Anwensenheitsintegration wird während der Sitzung der Office-Anwendung nicht erneut eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="f64cd-175">If the Office application encounters an error on any of the steps above, it backs out and presence integration is not established again during the session of the Office application.</span></span> 
  
### <a name="connecting-to-required-interfaces"></a><span data-ttu-id="f64cd-176">Herstellen einer Verbindung mit den erforderlichen Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="f64cd-176">Connecting to required interfaces</span></span>
<span data-ttu-id="f64cd-177"><a name="off15_IMIntegration_HowConnect"> </a></span><span class="sxs-lookup"><span data-stu-id="f64cd-177"></span></span>

<span data-ttu-id="f64cd-p110">Die Office-Anwendung versucht nach der Authentifizierung der Verbindung mit der Clientanwendung für Chatnachrichten, eine Verbindung mit den erforderlichen Schnittstellen herzustellen, die von der Clientanwendung für Chatnachrichten offen gelegt werden müssen. Dazu führt die Office-Anwendung die folgenden Aktionen durch:</span><span class="sxs-lookup"><span data-stu-id="f64cd-p110">After authenticating the connection to the IM client application, the Office application attempts to connect to a set of required interfaces that the IM client application must expose. The Office application accomplishes this by doing the following:</span></span>
  
- <span data-ttu-id="f64cd-180">Die Office-Anwendung ruft ein [ILyncClient](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ILyncClient)-Objekt durch Aufrufen der **IUCOfficeIntegration.GetInterface**-Methode und Übergeben der **oiInterfaceLyncClient**-Konstante aus der [UCCollaborationLib.OIInterface](http://msdn.microsoft.com/library/UCCollaborationLib.OIInterface)-Enumeration.</span><span class="sxs-lookup"><span data-stu-id="f64cd-180">The Office application gets an [ILyncClient](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ILyncClient) object by calling the **IUCOfficeIntegration.GetInterface** method, passing in the **oiInterfaceLyncClient** constant from the [UCCollaborationLib.OIInterface](http://msdn.microsoft.com/library/UCCollaborationLib.OIInterface) enumeration.</span></span> 
    
- <span data-ttu-id="f64cd-181">Die Office-Anwendung ruft ein [IAutomation](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IAutomation)-Objekt durch Aufrufen der **IUCOfficeIntegration.GetInterface**-Methode und Übergeben der **oiInterfaceAutomation**-Konstante aus der **OIInterface**-Enumeration.</span><span class="sxs-lookup"><span data-stu-id="f64cd-181">The Office application gets an [IAutomation](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IAutomation) object by calling the **IUCOfficeIntegration.GetInterface** method, passing in the **oiInterfaceAutomation** constant from the **OIInterface** enumeration.</span></span> 
    
- <span data-ttu-id="f64cd-182">Die Office-Anwendung richtet den [_ILyncClientEvents](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ILyncClient)-Ereignislistener ein.</span><span class="sxs-lookup"><span data-stu-id="f64cd-182">The Office application sets up the [_ILyncClientEvents](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ILyncClient) event listener.</span></span> 
    
- <span data-ttu-id="f64cd-183">Die Office-Anwendung richtet den [_IUCOfficeIntegrationEvents](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IUCOfficeIntegration)-Ereignislistener ein.</span><span class="sxs-lookup"><span data-stu-id="f64cd-183">The Office application sets up the [_IUCOfficeIntegrationEvents](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IUCOfficeIntegration) event listener.</span></span> 
    
- <span data-ttu-id="f64cd-184">Die Office-Anwendung ruft den Anmeldestatus aus der Clientanwendung für Chatnachrichten ab, indem sie auf die **ILyncClient.State**-Eigenschaft zugreift.</span><span class="sxs-lookup"><span data-stu-id="f64cd-184">The Office application gets the sign-in state from the IM client application by accessing the **ILyncClient.State** property.</span></span> 
    
- <span data-ttu-id="f64cd-185">Die Office-Anwendung ruft die Funktionen der Clientanwendung für Chantnachrichten durch Aufrufen der **IUCOfficeIntegration.GetSupportedFeatures**-Methode auf, die eine Kennzeichnung aus der [UCCollaborationLib.OIFeature](http://msdn.microsoft.com/library/UCCollaborationLib.OIFeature)-Enumeration zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="f64cd-185">The Office application gets the capabilities of the IM client application by calling the **IUCOfficeIntegration.GetSupportedFeatures** method, which returns a flag from the [UCCollaborationLib.OIFeature](http://msdn.microsoft.com/library/UCCollaborationLib.OIFeature) enumeration.</span></span> 
    
- <span data-ttu-id="f64cd-186">Die Office-Anwendung greift auf die **ILyncClient.Self**-Eigenschaft zu, um einen Verweis auf ein [ISelf](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ISelf)-Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="f64cd-186">The Office application accesses the **ILyncClient.Self** property to get a reference to an [ISelf](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ISelf) object.</span></span> 
    
### <a name="retrieving-the-capabilities-of-the-local-user"></a><span data-ttu-id="f64cd-187">Abrufen der Funktionen des lokalen Benutzers</span><span class="sxs-lookup"><span data-stu-id="f64cd-187">Retrieving the capabilities of the local user</span></span>
<span data-ttu-id="f64cd-188"><a name="off15_IMIntegration_HowConnect"> </a></span><span class="sxs-lookup"><span data-stu-id="f64cd-188"></span></span>

<span data-ttu-id="f64cd-189">Die Office-Anwendung ruft mithilfe der folgenden Schritte die Funktionen des lokalen Benutzers ab:</span><span class="sxs-lookup"><span data-stu-id="f64cd-189">The Office application gets the capabilities of the local user by doing the following:</span></span>
  
1. <span data-ttu-id="f64cd-190">Wenn die Clientanwendung für Chatnachrichten die **IClient2**-Schnittstelle unterstützt, versucht Office ein [IContactManager](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactManager)-Objekt abzurufen, indem es auf die **IClient2.PrivateContactManager**-Eigenschaft zugreift.</span><span class="sxs-lookup"><span data-stu-id="f64cd-190">If the IM client application supports the **IClient2** interface, Office tries to get an [IContactManager](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactManager) object by accessing the **IClient2.PrivateContactManager** property.</span></span> 
    
2. <span data-ttu-id="f64cd-p111">Wird die **IClient2**-Schnittstelle von der Chatanwendung nicht unterstützt, ruft die Office-Anwendung ein **IContactManager**-Objekt ab, indem es auf die **ILyncClient.ContactManager**-Eigenschaft zugreift. Die Clientanwendung für Chatnachrichten muss erfolgreich ein **IContactManager**-Objekt zurückgeben, bevor andere Chatfunktionen eingerichtet werden können.</span><span class="sxs-lookup"><span data-stu-id="f64cd-p111">If the IM application does not support the **IClient2** interface, Office application gets an **IContactManager** object by accessing the **ILyncClient.ContactManager** property. The IM client application must successfully return an **IContactManager** object before any other IM capabilities can be established.</span></span> 
    
3. <span data-ttu-id="f64cd-193">Die Office-Anwendung greift auf die **ILyncClient.Uri**-Eigenschaft zu und ruft dann **IContactManager.GetContactByUri** auf, um das dem lokalen Benutzer zugewiesene [IContact](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContact)-Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="f64cd-193">The Office application accesses the **ILyncClient.Uri** property and then calls **IContactManager.GetContactByUri** to get the [IContact](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContact) object associated with the local user.</span></span> 
    
4. <span data-ttu-id="f64cd-194">Anschließend führt die Office-Anwendung mehrere Aufrufe von **IContact.CanStart** durch, um die Funktionen des lokalen Benutzers einzurichten, indem die Werte für **ModalityTypes.ucModalityInstantMessage** und **ModalityTypes.ucModalityAudioVideo** nacheinander übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="f64cd-194">The Office application then makes several calls to **IContact.CanStart** to establish the capabilities of the local user, passing in the values for **ModalityTypes.ucModalityInstantMessage** and **ModalityTypes.ucModalityAudioVideo** successively.</span></span> 
    
### <a name="retrieving-contact-presence"></a><span data-ttu-id="f64cd-195">Abrufen von Anwesenheitsinformationen des Kontakts</span><span class="sxs-lookup"><span data-stu-id="f64cd-195">Retrieving contact presence</span></span>
<span data-ttu-id="f64cd-196"><a name="off15_IMIntegration_HowConnect"> </a></span><span class="sxs-lookup"><span data-stu-id="f64cd-196"></span></span>

<span data-ttu-id="f64cd-197">Die Office-Anwendung ruft mithilfe der folgenden Schritte die Anwesenheitsinformationen des Kontakts ab, einschließlich des lokalen Benutzers:</span><span class="sxs-lookup"><span data-stu-id="f64cd-197">The Office application gets contact presence, including the local user, by doing the following:</span></span> 
  
1. <span data-ttu-id="f64cd-198">Die Office-Anwendung ruft **IContact.GetContactInformation** auf, um ein Anwesenheitselement des Kontakts abzurufen.</span><span class="sxs-lookup"><span data-stu-id="f64cd-198">The Office application calls **IContact.GetContactInformation** to get a presence item from the contact.</span></span> 
    
2. <span data-ttu-id="f64cd-p112">Anschließend abonniert die Office-Anwendung Änderungen des Anwesenheitsstatus des Kontakts. Sie ruft **IContactManager.CreateSubscription** auf, um ein [IContactSubscription](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactSubscription)-Objekt abzurufen. Als nächstes ruft sie **IContactSubscription.AddContact** zum Hinzufügen des Kontakts zum Abonnement auf und ruft dann **IContactSubscription.Subscribe** auf, um Statusänderungen des Kontakts abzurufen.</span><span class="sxs-lookup"><span data-stu-id="f64cd-p112">The Office application then subscribes to presence status changes from the contact. It calls **IContactManager.CreateSubscription** to get an [IContactSubscription](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactSubscription) object. It then calls **IContactSubscription.AddContact** to add the contact to the subscription and then calls **IContactSubscription.Subscribe** to get changes in the contact's status.</span></span> 
    
3. <span data-ttu-id="f64cd-202">Wenn die Chatanwendung **IContact2** unterstützt, versucht Office Anwesenheitsinformationen durch Aufrufen von **IContact2.BatchGetContactInformation2**abzurufen.</span><span class="sxs-lookup"><span data-stu-id="f64cd-202">If the IM application supports **IContact2**, Office attempts to get presence information by calling **IContact2.BatchGetContactInformation2**.</span></span>
    
4. <span data-ttu-id="f64cd-p113">Anschließend ruft die Office-Anwendung die Anwesenheitseigenschaften des Kontakts durch Aufrufen von **IContact.BatchGetContactInformation** ab. Die Office-Anwendung kann einen zweiten Satz Anwesenheitseigenschaften durch Zugriff auf die **IContact.Settings**-Eigenschaft abrufen.</span><span class="sxs-lookup"><span data-stu-id="f64cd-p113">The Office application then retrieves the presence properties for the contact by calling **IContact.BatchGetContactInformation**. The Office application can get a second set of presence properties by accessing the **IContact.Settings** property.</span></span> 
    
5. <span data-ttu-id="f64cd-p114">Abschließend ruft die Office-Anwendung die Gruppenmitgliedschaft des Kontakts ab, indem Sie auf die **IContact.CustomGroups**-Eigenschaft zugreift. Dabei wird eine [IGroupCollection](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IGroup)-Sammlung mit allen [IGroup](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IGroup)-Objekten zurückgegeben, bei denen der Kontakt Mitglied ist.</span><span class="sxs-lookup"><span data-stu-id="f64cd-p114">Finally, the Office application gets the contact's group membership by accessing the **IContact.CustomGroups** property. This returns an [IGroupCollection](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IGroup) collection that includes all of the [IGroup](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IGroup) objects that the contact belongs to.</span></span> 
    
### <a name="disconnecting-from-the-im-application"></a><span data-ttu-id="f64cd-207">Trennen der Verbindung mit einer Chatanwendung</span><span class="sxs-lookup"><span data-stu-id="f64cd-207">Disconnecting from the IM application</span></span>
<span data-ttu-id="f64cd-208"><a name="off15_IMIntegration_HowConnect"> </a></span><span class="sxs-lookup"><span data-stu-id="f64cd-208"></span></span>

<span data-ttu-id="f64cd-p115">Wenn die Office 2013-Anwendung das **OnShuttingDown**-Ereignis in der Chatanwendung feststellt, wird die Verbindung im Hintergrund getrennt. Wenn die Office-Anwendung vor der Chatanwendung beendet wird, kann die Office-Anwendung jedoch nicht gewährleisten, dass die Verbindung bereinigt wird. Die Chatanwendung muss Verluste der Clientverbindung verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="f64cd-p115">When the Office 2013 application detects the **OnShuttingDown** event from the IM application, it disconnects silently. However, if the Office application shuts down before the IM application, the Office application does not guarantee that the connection is cleaned up. The IM application must handle client connection leaks.</span></span> 
  
## <a name="setting-registry-keys-and-entries"></a><span data-ttu-id="f64cd-212">Festlegen der Registrierungsschlüssel und-Einträge</span><span class="sxs-lookup"><span data-stu-id="f64cd-212">Setting registry keys and entries</span></span>
<span data-ttu-id="f64cd-213"><a name="off15_IMIntegration_SetRegistry"> </a></span><span class="sxs-lookup"><span data-stu-id="f64cd-213"></span></span>

<span data-ttu-id="f64cd-p116">Wie bereits erwähnt, suchen Chat-fähige Office 2013-Anwendungen nach bestimmten Schlüsseln, Einträgen und Werten in der Registrierung, um die Clientanwendung für Chatnachrichten zu ermitteln, mit der eine Verbindung hergestellt werden soll. Diese Registrierungswerte stellen der Office-Anwendung den Prozessnamen und die CLSID der Klasse bereit, die als Einstiegspunkt des Objektmodells der Clientanwendung für Chatnachrichten dient (d. h. die Klasse, die die **IUCOfficeIntegration**-Schnittstelle implementiert). Die Office-Anwendung ist an der Erstellung dieser Klasse beteiligt und stellt als Client eine Verbindung mit dem COM-Server ohne Prozesse in der Clientanwendung für Chatnachrichten her.</span><span class="sxs-lookup"><span data-stu-id="f64cd-p116">As mentioned previously, the IM-capable Office 2013 applications look for specific keys, entries, and values in the registry to discover the IM client application to connect to. These registry values provide the Office application with the process name and CLSID of the class that acts as the entry point to the IM client application's object model (that is, the class that implements the **IUCOfficeIntegration** interface). The Office application co-creates that class and connects as a client to the out-of-process COM server in the IM client application.</span></span> 
  
<span data-ttu-id="f64cd-217">Anhand der Tabelle 1 können Sie Schlüssel, Einträge und Werte identifizieren, die in der Registrierung geschrieben werden müssen, um eine Clientanwendung für Chatnachrichten in Office zu integrieren.</span><span class="sxs-lookup"><span data-stu-id="f64cd-217">Use Table 1 to identify the keys, entries, and values that must be written in the registry to integrate an IM client application with Office.</span></span>
  
<span data-ttu-id="f64cd-218">**Tabelle 1. Registrierungsschlüssel zum Festlegen der standardmäßigen Clientanwendung für Chatnachrichten**</span><span class="sxs-lookup"><span data-stu-id="f64cd-218">**Table 1. Registry keys for setting the default IM client application**</span></span>

|<span data-ttu-id="f64cd-219">**Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="f64cd-219">**Key**</span></span>|<span data-ttu-id="f64cd-220">**Eintrag**</span><span class="sxs-lookup"><span data-stu-id="f64cd-220">**Entry**</span></span>|<span data-ttu-id="f64cd-221">**Typ**</span><span class="sxs-lookup"><span data-stu-id="f64cd-221">**Type**</span></span>|<span data-ttu-id="f64cd-222">**Wert**</span><span class="sxs-lookup"><span data-stu-id="f64cd-222">**Value**</span></span>|<span data-ttu-id="f64cd-223">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="f64cd-223">**Example**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="f64cd-224">HKEY_LOCAL_MACHINE\Software\IM Providers\\< Anwendungsname\></span><span class="sxs-lookup"><span data-stu-id="f64cd-224">HKEY_LOCAL_MACHINE\Software\IM Providers\\<Application name\></span></span>  <br/> |<span data-ttu-id="f64cd-225">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="f64cd-225">FriendlyName</span></span>  <br/> |<span data-ttu-id="f64cd-226">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="f64cd-226">REG_SZ</span></span>  <br/> |<span data-ttu-id="f64cd-227">Der Name der Drittanbieter-Clientanwendung für Chatnachrichten.</span><span class="sxs-lookup"><span data-stu-id="f64cd-227">The name of the third-party IM client application.</span></span>  <br/> |<span data-ttu-id="f64cd-228">Litware IM 2012</span><span class="sxs-lookup"><span data-stu-id="f64cd-228">Litware IM 2012</span></span>  <br/> |
||<span data-ttu-id="f64cd-229">ProcessName</span><span class="sxs-lookup"><span data-stu-id="f64cd-229">ProcessName</span></span>  <br/> |<span data-ttu-id="f64cd-230">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="f64cd-230">REG_SZ</span></span>  <br/> |<span data-ttu-id="f64cd-231">Der Prozessname der Drittanbieter-Clientanwendung für Chatnachrichten.</span><span class="sxs-lookup"><span data-stu-id="f64cd-231">The process name of the third-party IM client application.</span></span>  <br/> |<span data-ttu-id="f64cd-232">litware.exe</span><span class="sxs-lookup"><span data-stu-id="f64cd-232">litware.exe</span></span>  <br/> |
||<span data-ttu-id="f64cd-233">GUID</span><span class="sxs-lookup"><span data-stu-id="f64cd-233">GUID</span></span>  <br/> |<span data-ttu-id="f64cd-234">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="f64cd-234">REG_SZ</span></span>  <br/> |<span data-ttu-id="f64cd-235">Eine Klassen-ID (CLSID) für den Stamm, eine mizugestaltende Klasse in der Chatanwendung (Klasse, die die **IUCOfficeIntegration**-Schnittstelle implementiert).</span><span class="sxs-lookup"><span data-stu-id="f64cd-235">A class ID (CLSID) for the root, cocreatable class in the IM application (the class that implements the **IUCOfficeIntegration** interface).</span></span>  <br/> |<span data-ttu-id="f64cd-236">(Eine GUID)</span><span class="sxs-lookup"><span data-stu-id="f64cd-236">(A GUID)</span></span>  <br/> |
|<span data-ttu-id="f64cd-237">HKEY_CURRENT_USER\Software\IM Providers</span><span class="sxs-lookup"><span data-stu-id="f64cd-237">HKEY_CURRENT_USER\Software\IM Providers</span></span>  <br/> |<span data-ttu-id="f64cd-238">DefaultIMApp</span><span class="sxs-lookup"><span data-stu-id="f64cd-238">DefaultIMApp</span></span>  <br/> |<span data-ttu-id="f64cd-239">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="f64cd-239">REG_SZ</span></span>  <br/> |<span data-ttu-id="f64cd-p117">Der Name der Clientanwendung für Chatnachrichten. Dieser muss mit dem Namen auf oberster Ebene des Registrierungsschlüssels (Struktur) in HKEY_LOCAL_MACHINE übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="f64cd-p117">The name of the IM client application. This must be the same as the name at the top-level registry key (hive) in the HKEY_LOCAL_MACHINE.</span></span>  <br/> |<span data-ttu-id="f64cd-242">Litware</span><span class="sxs-lookup"><span data-stu-id="f64cd-242">Litware</span></span>  <br/> |
|<span data-ttu-id="f64cd-243">HKEY_CURRENT_USER\Software\IM Providers\\<Anwendungsname\></span><span class="sxs-lookup"><span data-stu-id="f64cd-243">HKEY_CURRENT_USER\Software\IM Providers\\<Application name\></span></span>  <br/> |<span data-ttu-id="f64cd-244">UpAndRunning</span><span class="sxs-lookup"><span data-stu-id="f64cd-244">UpAndRunning</span></span>  <br/> |<span data-ttu-id="f64cd-245">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="f64cd-245">REG_DWORD</span></span>  <br/> | <span data-ttu-id="f64cd-246">Ein ganzzahliger Wert zwischen 0 und 2:</span><span class="sxs-lookup"><span data-stu-id="f64cd-246">An integer value between 0 and 2:</span></span>  <br/>  <span data-ttu-id="f64cd-247">0 – Wird ausgeführt</span><span class="sxs-lookup"><span data-stu-id="f64cd-247">0—Not running</span></span>  <br/>  <span data-ttu-id="f64cd-248">1 – Wird gestartet</span><span class="sxs-lookup"><span data-stu-id="f64cd-248">1—Starting</span></span>  <br/>  <span data-ttu-id="f64cd-249">2 – Wird ausgeführt</span><span class="sxs-lookup"><span data-stu-id="f64cd-249">2—Running</span></span>  <br/> <br/><span data-ttu-id="f64cd-250">**Hinweis**: Der Registrierungsschlüssel des Anwendungsnamens muss mit dem Wert des DefaultIMApp-Eintrags übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="f64cd-250">The application name registry key must be the same as the value of the DefaultIMApp entry.</span></span>           ||
   
## <a name="implementing-the-required-interfaces-for-integration-with-office"></a><span data-ttu-id="f64cd-251">Implementieren der erforderlichen Schnittstellen für die Integration in Office</span><span class="sxs-lookup"><span data-stu-id="f64cd-251">Implementing the required interfaces for integration with Office</span></span>
<span data-ttu-id="f64cd-252"><a name="off15_IMIntegration_ImplementRequired"> </a></span><span class="sxs-lookup"><span data-stu-id="f64cd-252"></span></span>

<span data-ttu-id="f64cd-p118">Es gibt drei Schnittstellen aus dem **UCCollaborationLib**-Namespace, die vom ausführbaren Programm (oder COM-Server) einer Clientanwendung für Chatnachrichten für die Integration in Office implementiert werden müssen. Werden diese Schnittstellen nicht implementiert, zieht sich die Office-Anwendung während des Initialisierungsprozesses zurück, und es wird keine Verbindung mit der Clientanwendung für Chatnachrichten hergestellt.</span><span class="sxs-lookup"><span data-stu-id="f64cd-p118">There are three interfaces from the **UCCollaborationLib** namespace that the executable (or COM server) of an IM client application must implement so that it can integrate with Office. If these interfaces are not implemented, the Office application backs out during the initialization process and the connection with the IM client application is not established.</span></span> 
  
<span data-ttu-id="f64cd-255">Die erforderlichen Schnittstellen sind die folgenden:</span><span class="sxs-lookup"><span data-stu-id="f64cd-255">The required interfaces are as follows:</span></span>
  
- <span data-ttu-id="f64cd-256">[IUCOfficeIntegration](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IUCOfficeIntegration). Die **_IUCOfficeIntegrationEvents**-Schnittstelle sollte, auch wenn nicht erforderlich, auch in der gleichen abgeleiteten Klasse implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="f64cd-256">[IUCOfficeIntegration](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IUCOfficeIntegration)—Although not required, the **_IUCOfficeIntegrationEvents** interface should also be implemented in the same derived class.</span></span> 
    
- <span data-ttu-id="f64cd-257">[ILyncClient](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ILyncClient). Die **_ILyncClientEvents**-Schnittstelle sollte, auch wenn nicht erforderlich, auch in der gleichen abgeleiteten Klasse implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="f64cd-257">[ILyncClient](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ILyncClient)—Although not required, the **_ILyncClientEvents** interface should also be implemented in the same derived class.</span></span> 
    
- [<span data-ttu-id="f64cd-258">IAutomation</span><span class="sxs-lookup"><span data-stu-id="f64cd-258">IAutomation</span></span>](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IAutomation)
    
### <a name="iucofficeintegration-interface"></a><span data-ttu-id="f64cd-259">IUCOfficeIntegration-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="f64cd-259">IUCOfficeIntegration interface</span></span>
<span data-ttu-id="f64cd-260"><a name="off15_IMIntegration_ImplementRequired_IUCOfficeIntegration"> </a></span><span class="sxs-lookup"><span data-stu-id="f64cd-260"></span></span>

<span data-ttu-id="f64cd-p119">Die **IUCOfficeIntegration**-Schnittstelle stellt den Einstiegspunkt für eine Office-Anwendung bereit, um eine Verbindung mit der Clientanwendung für Chatnachrichten herzustellen. Die Schnittstelle definiert drei Methoden, die eine Office-Anwendung im Rahmen der Initialisierung einer Verbindung mit der Clientanwendung für Chatnachrichten aufruft. Die Klasse, die die **IUCOfficeIntegration**-Schnittstelle implementiert, muss eine gemeinsam zu erstellende Klasse sein, damit Office eine Instanz von dieser mitgestalten kann. Darüber hinaus muss sie die CLSID offen legen, die als Wert für den GUID-Eintrag im Registrierungsschlüssel „HKEY_LOCAL_MACHINE\Software\IM Providers\ eingegeben haben, ist _Application name_" eingegeben wird.</span><span class="sxs-lookup"><span data-stu-id="f64cd-p119">The **IUCOfficeIntegration** interface provides the entry-point for an Office application to connect to the IM client application. The interface defines three methods that an Office application calls as part of the process of initiating a connection with the IM client application. The class that implements the **IUCOfficeIntegration** interface must be co-creatable so that Office can co-create an instance of it. In addition, it must expose the CLSID that is entered as the value for the GUID entry in the HKEY_LOCAL_MACHINE\Software\IM Providers\  _Application name_ registry key.</span></span> 
  
<span data-ttu-id="f64cd-p120">Die Klasse, die von **IUCOfficeIntegration** erbt, sollte auch die **_IUCOfficeIntegrationEvents**-Schnittstelle implementieren. Die **_IUCOfficeIntegrationEvents**-Schnittstelle enthält die Elemente, die die Ereignishandler der **IUCOfficeIntegration**-Schnittstelle verfügbar macht.</span><span class="sxs-lookup"><span data-stu-id="f64cd-p120">The class that inherits from **IUCOfficeIntegration** should also implement the **_IUCOfficeIntegrationEvents** interface. The **_IUCOfficeIntegrationEvents** interface contains the members that expose the event handlers of the **IUCOfficeIntegration** interface.</span></span> 
  
<span data-ttu-id="f64cd-267">In Tabelle 2 werden die Elemente aufgeführt, die in der Klasse implementiert werden müssen, die von **IUCOfficeIntegration** und **_IUCOfficeIntegration** erbt.</span><span class="sxs-lookup"><span data-stu-id="f64cd-267">Table 2 shows the members that must be implemented in the class that inherits from **IUCOfficeIntegration** and **_IUCOfficeIntegration**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="f64cd-268">Weitere Informationen zu den **IUCOfficeIntegration**- und **_IUCOfficeIntegrationEvents**-Schnittstellen und den dazugehörigen Elemente finden Sie unter [UCCollaborationLib.IUCOfficeIntegration](http://msdn.microsoft.com/library/UCCollaborationLib.IUCOfficeIntegration) und [UCCollaborationLib._IUCOfficeIntegrationEvents](http://msdn.microsoft.com/library/UCCollaborationLib._IUCOfficeIntegrationEvents).</span><span class="sxs-lookup"><span data-stu-id="f64cd-268">For more information about the **IUCOfficeIntegration** and **_IUCOfficeIntegrationEvents** interfaces and their members, see [UCCollaborationLib.IUCOfficeIntegration](http://msdn.microsoft.com/library/UCCollaborationLib.IUCOfficeIntegration) and [UCCollaborationLib._IUCOfficeIntegrationEvents](http://msdn.microsoft.com/library/UCCollaborationLib._IUCOfficeIntegrationEvents).</span></span> 
  
<span data-ttu-id="f64cd-269">**Tabelle 2 Implementierung der IUCOfficeIntegration- und _IUCOfficeIntegrationEvents-Schnittstellen**</span><span class="sxs-lookup"><span data-stu-id="f64cd-269">**Table 2. Implementation of the IUCOfficeIntegration and _IUCOfficeIntegrationEvents interfaces**</span></span>

|<span data-ttu-id="f64cd-270">**Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="f64cd-270">**Interface**</span></span>|<span data-ttu-id="f64cd-271">**Element**</span><span class="sxs-lookup"><span data-stu-id="f64cd-271">**Member**</span></span>|<span data-ttu-id="f64cd-272">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f64cd-272">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f64cd-273">**IUCOfficeIntegration**</span><span class="sxs-lookup"><span data-stu-id="f64cd-273">**IUCOfficeIntegration**</span></span> <br/> |<span data-ttu-id="f64cd-274">**GetAuthenticationInfo**-Methode</span><span class="sxs-lookup"><span data-stu-id="f64cd-274">**GetAuthenticationInfo** method</span></span>  <br/> |<span data-ttu-id="f64cd-275">Ruft die Zeichenfolge mit den Authentifizierungsinformationen ab.</span><span class="sxs-lookup"><span data-stu-id="f64cd-275">Gets the authentication info string.</span></span>  <br/> |
||<span data-ttu-id="f64cd-276">**GetInterface**-Methode</span><span class="sxs-lookup"><span data-stu-id="f64cd-276">**GetInterface** method</span></span>  <br/> |<span data-ttu-id="f64cd-277">Ruft die Schnittstelle einer bestimmten Version ab.</span><span class="sxs-lookup"><span data-stu-id="f64cd-277">Gets the interface of a particular version.</span></span>  <br/> |
||<span data-ttu-id="f64cd-278">**GetSupportedFeatures**-Methode</span><span class="sxs-lookup"><span data-stu-id="f64cd-278">**GetSupportedFeatures** method</span></span>  <br/> |<span data-ttu-id="f64cd-279">Ruft die unterstützten Features der Office-Integration ab.</span><span class="sxs-lookup"><span data-stu-id="f64cd-279">Gets the supported Office integration features.</span></span>  <br/> |
|<span data-ttu-id="f64cd-280">**_IUCOfficeIntegrationEvents**</span><span class="sxs-lookup"><span data-stu-id="f64cd-280">**_IUCOfficeIntegrationEvents**</span></span> <br/> |<span data-ttu-id="f64cd-281">**OnShuttingDown**-Ereignis</span><span class="sxs-lookup"><span data-stu-id="f64cd-281">**OnShuttingDown** event</span></span>  <br/> |<span data-ttu-id="f64cd-282">Das Ereignis, das ausgelöst wird, wenn die Clientanwendung für Chatnachrichten beendet wird.</span><span class="sxs-lookup"><span data-stu-id="f64cd-282">The event raised when the IM client application is trying to shut down.</span></span>  <br/> |
   
<span data-ttu-id="f64cd-283">Verwenden Sie den folgenden Code zum Definieren einer Klasse, die von den **IUCOfficeIntegration**- und **_IUCOfficeIntegration**-Schnittstellen innerhalb einer Clientanwendung für Chatnachrichten erbt.</span><span class="sxs-lookup"><span data-stu-id="f64cd-283">Use the following code to define a class that inherits from the **IUCOfficeIntegration** and **_IUCOfficeIntegration** interfaces within an IM client application.</span></span> 
  
```cs
// An example of a class that can be co-created and can integrate
// with Office as an IM provider.
[ClassInterface(ClassInterfaceType.None)]
[ComSourceInterfaces(typeof(_IUCOfficeIntegrationEvents))]
[Guid("{CLSID value}"), ComVisible(true)]
public class LitwareClientAppObject : IUCOfficeIntegration
{
    // Implementation details omitted.
}

```

<span data-ttu-id="f64cd-284">Die **GetAuthenticationInfo** -Methode akzeptiert eine Zeichenfolge als Argument für die _Version_ Parameter.</span><span class="sxs-lookup"><span data-stu-id="f64cd-284">The **GetAuthenticationInfo** method takes a string as an argument for the  _version_ parameter.</span></span> <span data-ttu-id="f64cd-285">Wenn die Office-Anwendung diese Methode aufruft, wird je nach Office-Version eine der zwei Zeichenfolgen für das Argument übergeben.</span><span class="sxs-lookup"><span data-stu-id="f64cd-285">When the Office application calls this method, it passes in one of two strings for the argument, depending on the version of Office.</span></span> <span data-ttu-id="f64cd-286">Stellt die Office-Anwendung die Methode mit der Office-Version bereit, die von der Clientanwendung für Chatnachrichten unterstützt wird (d. h. die Funktionalität wird unterstützt), gibt die **GetAuthenticationInfo**-Methode eine hartcodierte XML-Zeichenfolge `<authenticationinfo>` zurück.</span><span class="sxs-lookup"><span data-stu-id="f64cd-286">The GetAuthenticationInfo method takes a string as an argument for the  version parameter. When the Office application calls this method, it passes in one of two strings for the argument, depending on the version of Office. When the Office application supplies the method with the version of Office that the IM client application supports (that is, supports the functionality), the **GetAuthenticationInfo** method returns a hard-coded XML string "`<authenticationinfo>`".</span></span> 
  
<span data-ttu-id="f64cd-287">Verwenden Sie den folgenden Code zum Implementieren der **GetAuthentication**-Methode innerhalb des Codes der Clientanwendung für Chatnachrichten.</span><span class="sxs-lookup"><span data-stu-id="f64cd-287">Use the following code to implement the **GetAuthentication** method within the IM client application code.</span></span> 
  
```cs
public string GetAuthenticationInfo(string _version)
{
    // Define the version of Office that the IM client application supports.
    string supportedOfficeVersion = "15.0.0.0";
    // Do a simple check for equivalency.
    if (supportedOfficeVersion == _version)
    {
        // If the version of Office is supported, this method must 
        // return the string literal "<authenticationinfo>" exactly.
        return "<authenticationinfo>";
    }
    else
    {
        return null;
    }
}

```

<span data-ttu-id="f64cd-p122">Die **GetInterface**-Methode übermittelt Verweise auf Klassen an den aufrufenden Code, je nachdem, was als Argument für den  _interface_-Parameter übergeben wird. Wenn eine Office-Anwendung die **GetInterface**-Methode aufruft, wird einer von zwei Werten für den Schnittstellenparameter übergeben: entweder die **oiInterfaceILyncClient**-Konstante (1) oder die **oiInterfaceIAutomation**-Konstante (2) der [UCCollaborationLib.OIInterface](http://msdn.microsoft.com/library/UCCollaborationLib.OIInterface)-Enumeration. Übergibt die Office-Anwendung die **oiInterfaceILyncClient**-Konstante, gibt die **GetInterface**-Methode einen Verweis auf eine Klasse zurück, die die **ILyncClient**-Schnittstelle implementiert. Übergibt die Office-Anwendung die **oiInterfaceIAutomation**-Konstante, gibt die **GetInterface**-Methode eine Klasse zurück, die die **IAutomation**-Schnittstelle implementiert.</span><span class="sxs-lookup"><span data-stu-id="f64cd-p122">The **GetInterface** method shuttles references to classes to the calling code, depending on what is passed in as an argument for the  _interface_ parameter. When an Office application calls the **GetInterface** method, it passes in one of two values for the interface parameter: either the **oiInterfaceILyncClient** constant (1) or the **oiInterfaceIAutomation** constant (2) of the [UCCollaborationLib.OIInterface](http://msdn.microsoft.com/library/UCCollaborationLib.OIInterface) enumeration. If the Office application passes in the **oiInterfaceILyncClient** constant, the **GetInterface** method returns a reference to a class that implements the **ILyncClient** interface. If the Office application passes in the **oiInterfaceIAutomation** constant, the **GetInterface** method returns a class that implements the **IAutomation** interface.</span></span> 
  
<span data-ttu-id="f64cd-292">Verwenden Sie das folgende Codebeispiel zum Implementieren der **GetInterface**-Methode innerhalb des Codes der Clientanwendung für Chatnachrichten.</span><span class="sxs-lookup"><span data-stu-id="f64cd-292">Use the following code example to implement the **GetInterface** method within the IM client application code.</span></span> 
  
```cs
public object GetInterface(string _version, OIInterface _interface)
{
    // These objects implement the ILyncClient or IAutomation 
    // interfaces respectively. There is no restriction on what these
    // classes are named.
    IMClient imClient = new IMClient();
    IMClientAutomation imAutomation = new IMClientAutomation();
    // Return different object references depending on the value passed in
    // for the _interface parameter.
    switch (_interface)
    {
        // The calling code is asking for an object that inherits
        // from ILyncClient, so it returns such an object.
        case OIInterface.oiInterfaceILyncClient:
        {
            return imClient;
        }
        // The calling code is asking for an object that inherits
        // from IAutomation, so it returns such an object.
        case OIInterface.oiInterfaceIAutomation:
        {
            return imAutomation;
        }
        default:
        {
            throw new NotImplementedException();
        }
    }
}

```

<span data-ttu-id="f64cd-p123">Die **GetSupportedFeatures**-Methode gibt Informationen zu den Chatfunktionen zurück, die von der Clientanwendung für Chatnachrichten unterstützt werden. Sie verwendet eine Zeichenfolge als einzigen Parameter,  _version_. Wenn die Office-Anwendung die **GetSupportFeatures**-Methode aufruft, gibt die Methode einen Wert aus der [UCCollaborationLib.OIFeature](http://msdn.microsoft.com/library/UCCollaborationLib.OIFeature)-Enumeration zurück. Der zurückgegebene Wert gibt die Funktionen des Chatclients an, wobei jede Funktion der Clientanwendung für Chatnachrichten mit einer Kennzeichnung des Werts für die Office-Anwendung versehen ist.</span><span class="sxs-lookup"><span data-stu-id="f64cd-p123">The **GetSupportedFeatures** method returns information about the IM features that the IM client application supports. It takes a string for its only parameter,  _version_. When the Office application calls the **GetSupportFeatures** method, the method returns a value from the [UCCollaborationLib.OIFeature](http://msdn.microsoft.com/library/UCCollaborationLib.OIFeature) enumeration. The returned value specifies the capabilities of the IM client, where each capability of the IM client application is indicated to the Office application by adding a flag to the value.</span></span> 
  
> [!NOTE]
>  <span data-ttu-id="f64cd-297">Office 2013-Anwendungen ignorieren die folgenden Konstanten in der **OIFeature**-Enumeration:</span><span class="sxs-lookup"><span data-stu-id="f64cd-297">Office 2013 applications ignore the following constants in the **OIFeature** enumeration: > oiFeaturePictures (2) > oiFeatureFreeBusyIntegrationoiFeaturePhoneNormalization</span></span> 
> - <span data-ttu-id="f64cd-298">**oiFeaturePictures** (2)</span><span class="sxs-lookup"><span data-stu-id="f64cd-298">**oiFeaturePictures** (2)</span></span> 
> - <span data-ttu-id="f64cd-299">**oiFeatureFreeBusyIntegration**</span><span class="sxs-lookup"><span data-stu-id="f64cd-299">**oiFeatureFreeBusyIntegration**</span></span>
> - <span data-ttu-id="f64cd-300">**oiFeaturePhoneNormalization**</span><span class="sxs-lookup"><span data-stu-id="f64cd-300">**oiFeaturePhoneNormalization**</span></span>
  
<span data-ttu-id="f64cd-301">Verwenden Sie das folgende Codebeispiel zum Implementieren der **GetSupportFeatures** -Methode innerhalb des Codes der Clientanwendung für Chatnachrichten.</span><span class="sxs-lookup"><span data-stu-id="f64cd-301">Use the following code example to implement the **GetSupportFeatures** method within the IM client application code.</span></span> 
  
```cs
public OIFeature GetSupportedFeatures(string _version)
{
    OIFeature supportedFeature1 = OIFeature.oiFeatureQuickContacts;
    OIFeature supportedFeature2 = OIFeature.oiFeatureFastSearch;
    return (supportedFeature1 | supportedFeature2);
}

```

### <a name="ilyncclient-interface"></a><span data-ttu-id="f64cd-302">ILyncClient-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="f64cd-302">ILyncClient interface</span></span>
<span data-ttu-id="f64cd-303"><a name="off15_IMIntegration_ImplementRequired_ILyncClient"> </a></span><span class="sxs-lookup"><span data-stu-id="f64cd-303"></span></span>

<span data-ttu-id="f64cd-p124">Die **ILyncClient**-Schnittstelle wird den Funktionen der Clientanwendung für Chatnachrichten zugeordnet. Sie legt die Eigenschaften offen, die auf die bei der Anwendung angemeldete Person (der durch die [UCCollaborationLib.ISelf](http://msdn.microsoft.com/library/UCCollaborationLib.ISelf)-Schnittstelle dargestellte lokale Benutzer), den Status der Anwendung, die Liste der Kontakte des lokalen Benutzers verweisen, und viele andere Einstellungen. Wenn versucht wird, eine Verbindung mit der Clientanwendung für Chatnachrichten herzustellen, ruft die Office-Anwendung einen Verweis auf ein Objekt ab, das die **ILyncClient**-Schnittstelle implementiert. Über diesen Verweis kann Office auf viele Funktionen der Clientanwendung für Chatnachrichten zugreifen.</span><span class="sxs-lookup"><span data-stu-id="f64cd-p124">The **ILyncClient** interface maps to the capabilities of the IM client application itself. It exposes properties that refer to the person who is signed into the application (the local user, represented by the [UCCollaborationLib.ISelf](http://msdn.microsoft.com/library/UCCollaborationLib.ISelf) interface), the state of the application, the list of contacts for the local user, and several other settings. When it's trying to connect to the IM client application, the Office application gets a reference to an object that implements the **ILyncClient** interface. From that reference, Office can access much of the functionality of the IM client application.</span></span> 
  
<span data-ttu-id="f64cd-p125">Darüber hinaus sollte die Klasse, die die **ILyncClient**-Schnittstelle Implementiert, auch die **_ILyncClientEvents**-Schnittstelle implementieren. Die **_ILyncClientEvents**-Schnittstelle legt eine Reihe von Ereignissen offen, die für die Überwachung des Status der Clientanwendung für Chatnachrichten erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="f64cd-p125">In addition, the class that implements the **ILyncClient** interface should also implement the **_ILyncClientEvents** interface. The **_ILyncClientEvents** interface exposes several of the events that are required for monitoring the state of the IM client application.</span></span> 
  
<span data-ttu-id="f64cd-310">In Tabelle 3 werden die Elemente aufgeführt, die in der Klasse implementiert werden müssen, die aus **ILyncClient** und **_ILyncClientEvents** besteht.</span><span class="sxs-lookup"><span data-stu-id="f64cd-310">Table 3 shows the members that must be implemented in the class that inherits from **ILyncClient** and **_ILyncClientEvents**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="f64cd-311">Jegliche Elemente der **ILyncClient** oder **\_ILyncClientEvents**-Schnittstelle, die nicht in der Tabelle aufgeführt sind, müssen zwar vorhanden sein, jedoch nicht implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="f64cd-311">Any member of the ILyncClient or _ILyncClientEvents interface not listed in the table must be present but does not need to be implemented.</span></span> <span data-ttu-id="f64cd-312">Elemente, die vorhanden sind, jedoch nicht implementiert werden, können einen **NotImplementedException** or **E\_NOTIMPL**-Fehler zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="f64cd-312">Members that are present but not implemented can throw a NotImplementedException or E_NOTIMPL error.</span></span> 
> 
> <span data-ttu-id="f64cd-313">Weitere Informationen zu den **ILyncClient**- und **_ILyncClientEvents**-Schnittstellen und den dazugehörigen Elementen finden Sie unter [UCCollaborationLib.ILyncClient](http://msdn.microsoft.com/library/UCCollaborationLib.ILyncClient) und [UCCollaborationLib._ILyncClientEvents](http://msdn.microsoft.com/library/UCCollaborationLib._ILyncClientEvents).</span><span class="sxs-lookup"><span data-stu-id="f64cd-313">> For more information about the **ILyncClient** and **_ILyncClientEvents** interfaces and their members, see [UCCollaborationLib.ILyncClient](http://msdn.microsoft.com/library/UCCollaborationLib.ILyncClient) and [UCCollaborationLib._ILyncClientEvents](http://msdn.microsoft.com/library/UCCollaborationLib._ILyncClientEvents).</span></span> 
  
<span data-ttu-id="f64cd-314">**Tabelle 3. Implementierung von ILyncClient- und ILyncClientEvents-Schnittstellen **</span><span class="sxs-lookup"><span data-stu-id="f64cd-314">**Table 3. Implementation of ILyncClient and ILyncClientEvents interfaces**</span></span>

|<span data-ttu-id="f64cd-315">**Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="f64cd-315">**Interface**</span></span>|<span data-ttu-id="f64cd-316">**Element**</span><span class="sxs-lookup"><span data-stu-id="f64cd-316">**Member**</span></span>|<span data-ttu-id="f64cd-317">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f64cd-317">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f64cd-318">**ILyncClient**</span><span class="sxs-lookup"><span data-stu-id="f64cd-318">**ILyncClient**</span></span> <br/> |<span data-ttu-id="f64cd-319">**ContactManager**-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="f64cd-319">**ContactManager** property</span></span>  <br/> |<span data-ttu-id="f64cd-320">Ruft den Kontaktgruppenmanager ab.</span><span class="sxs-lookup"><span data-stu-id="f64cd-320">Gets the contact group manager.</span></span>  <br/> |
||<span data-ttu-id="f64cd-321">**ConversationManager**-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="f64cd-321">**ConversationManager** property</span></span>  <br/> |<span data-ttu-id="f64cd-322">Ruft den Unterhaltungsmanager ab.</span><span class="sxs-lookup"><span data-stu-id="f64cd-322">Gets the conversations manager.</span></span>  <br/> |
||<span data-ttu-id="f64cd-323">**Self**-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="f64cd-323">**Self** property</span></span>  <br/> |<span data-ttu-id="f64cd-324">Ruft das **Self**-Objekt ab.</span><span class="sxs-lookup"><span data-stu-id="f64cd-324">Gets the **Self** object.</span></span>  <br/> |
||<span data-ttu-id="f64cd-325">**SignIn**-Methode</span><span class="sxs-lookup"><span data-stu-id="f64cd-325">**SignIn** method</span></span>  <br/> |<span data-ttu-id="f64cd-326">Startet den Anmeldeprozess der Clientanwendung für Chatnachrichten mit einer bestimmten Verfügbarkeit.</span><span class="sxs-lookup"><span data-stu-id="f64cd-326">Starts the IM client application sign-in process with a specific availability.</span></span>  <br/> |
||<span data-ttu-id="f64cd-327">**State**-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="f64cd-327">**State** property</span></span>  <br/> |<span data-ttu-id="f64cd-328">Ruft den aktuellen Plattformzustand ab.</span><span class="sxs-lookup"><span data-stu-id="f64cd-328">Gets the current platform state.</span></span>  <br/> |
||<span data-ttu-id="f64cd-329">**Uri**-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="f64cd-329">**Uri** property</span></span>  <br/> |<span data-ttu-id="f64cd-330">Ruft den URI der Clientanwendung für Chatnachrichten ab.</span><span class="sxs-lookup"><span data-stu-id="f64cd-330">Gets the URI of the IM client application.</span></span>  <br/> |
|<span data-ttu-id="f64cd-331">**_ILyncClientEvents**</span><span class="sxs-lookup"><span data-stu-id="f64cd-331">**_ILyncClientEvents**</span></span> <br/> |<span data-ttu-id="f64cd-332">**OnStateChanged**-Ereignis</span><span class="sxs-lookup"><span data-stu-id="f64cd-332">**OnStateChanged** event</span></span>  <br/> |<span data-ttu-id="f64cd-p127">Wird ausgelöst, wenn sich der Status der Clientanwendung für Chatnachrichten ändert. Dieses Ereignis sollte verarbeitet werden, und die **eventData.NewState**-Eigenschaft abgerufen werden. Das Ereignis wird für alle Prozesse ausgelöst, die an eine Instanz einer Clientanwendung für Chatnachrichten gebunden sind, wenn ein Subsystem in der Anwendung die Statusänderung auslöst.  </span><span class="sxs-lookup"><span data-stu-id="f64cd-p127">Raised when the IM client application state changes. You should handle this event and get the **eventData.NewState** property. The event is raised for all processes bound to an instance of an IM client application when any subsystem in the application causes the state change.  </span></span><br/> |
   
<span data-ttu-id="f64cd-p128">Während des Initialisierungsprozesses greift Office auf die **ILyncClient.State**-Eigenschaft zu. Diese Eigenschaft muss einen Wert aus der [UCCollaborationLib.ClientState](http://msdn.microsoft.com/library/UCCollaborationLib.ClientState)-Enumeration zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="f64cd-p128">During the initialization process, Office accesses the **ILyncClient.State** property. This property needs to return a value from the [UCCollaborationLib.ClientState](http://msdn.microsoft.com/library/UCCollaborationLib.ClientState) enumeration.</span></span> 
  
```cs
private ClientState _clientState;
public ClientState State
{
    get
    {
        return this._clientState;
    }
}

```

<span data-ttu-id="f64cd-p129">Die **State**-Eigenschaft speichert den aktuellen Status der Clientanwendung für Chatnachrichten. Sie muss durchgehend während der Clientanwendungssitzung für Chatnachrichten festgelegt und aktualisiert werden. Beim Anmelden, Abmelden oder Beenden der Clientanwendung für Chatnachrichten sollte die **State**-Eigenschaft festgelegt werden. Es empfiehlt sich, diese Eigenschaft in den **ILyncClient.SignIn**- und **ILyncClient.SignOut**-Methoden festzulegen, wie im folgenden Beispiel veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="f64cd-p129">The **State** property stores the current status of the IM client application. It must be set and updated throughout the IM client application session. When the IM client application signs in, signs out, or shuts down, it should set the **State** property. It is best to set this property within the **ILyncClient.SignIn** and **ILyncClient.SignOut** methods, as the following example demonstrates.</span></span> 
  
```cs
// This field is of a type that implements the 
// IAsynchronousOperation interface.
private IMClientAsyncOperation _asyncOperation = new IMClientAsyncOperation();
// This field is of a type that implements the ISelf interface.
private IMClientSelf _self;
public IMClientAsyncOperation SignIn(string _userUri, string _domainAndUser, 
    string _password, object _IMClientCallback, object _state)
{
    ClientState _previousClientState = this._clientState;
    this._clientState = ClientState.ucClientStateSignedIn;
    // The IMClientStateChangedEventData class implements the 
    // IClientStateChangedEventData interface.
    IMClientStateChangedEventData eventData = 
        new IMClientStateChangedEventData(_previousClientState, 
        this._clientState);
    if (_userUri != null)
    {
        // During the sign-in process, create a new contact with
        // the contact information of the currently signed-in user.
        this._self = new IMClientSelf(IMContact.BuildContact(_userUri));
    }
    // Raise the _ILyncClientEvents.OnStateChanged event.
    OnStateChanged(this, eventData as UC.ClientStateChangedEventData);
    
    return this._asyncOperation;
    }
}

```

<span data-ttu-id="f64cd-342">Das folgende Codebeisiel veranschaulicht die Einrichtung des Ereignislisteners mit den Schnittstellen _ **ILyncClientEvents** und _ **IUCOfficeIntegrationEvents**.</span><span class="sxs-lookup"><span data-stu-id="f64cd-342">The following code example demonstrates how to set up the event listener using the _ **ILyncClientEvents** and _ **IUCOfficeIntegrationEvents** interfaces.</span></span> 
  
```cs
using Microsoft.Office.Uc;
using System;
using System.Runtime.CompilerServices;
using System.Runtime.InteropServices;
namespace SampleImplementation
{
    // Note: UCOfficeIntegration inherits from both IUCOfficeIntegration and _IUCOfficeIntegrationEvents_Event
    [ClassInterface(ClassInterfaceType.None), Guid("13c41ef9-eb90-4e94-8a7c-1e9d686bc019"), ComVisible(true)]
    [ComSourceInterfaces(typeof(_IUCOfficeIntegrationEvents))]
    public class MyInstantMessengerOfficeIntegration : UCOfficeIntegration
    {
        #region IUCOfficeIntegration implementation
        public string GetAuthenticationInfo(string _version)
        {
            return "";
        }
        public object GetInterface(string _version, OIInterface _interface)
        {
            return null;
        }
        public OIFeature GetSupportedFeatures(string _version)
        {
            return OIFeature.oiFeatureAddOneNoteToConversation;
        }
        #endregion
        #region _IUCOfficeIntegrationEvents support
        // This event implements void _IUCOfficeIntegrationEvents.OnShuttingDown();
        public event _IUCOfficeIntegrationEvents_OnShuttingDownEventHandler OnShuttingDown;
        // This method is called by the IM application when it is beginning to shut down.
        // The method will raise the OnShuttingDown event which is translated by .NET COM interop layer
        // into a call to _IUCOfficeIntegrationEvents.OnShuttingDown.
        // This notifies Office applications that the IM application is going away.
        internal void RaiseOnShuttingDownEvent()
        {
            if (this.OnShuttingDown != null)
            {
                this.OnShuttingDown();
            }
        }
        #endregion
    }
    // Note: LyncClient inherits from both ILyncClient and _ILyncClientEvents_Event
    // You must implement LyncClient because the event handlers in _ILyncClientEvents expect you to pass a LyncClient interface.
    [ComVisible(true)]
    [ComSourceInterfaces(typeof(_ILyncClientEvents))]
    public class MyInstantMessengerOfficeIntegration2 :
        Client,
        Client2,
        LyncClient
    {
        #region Interfaces
        public LyncClientCapabilityTypes Capabilities
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public ConferenceScheduler ConferenceScheduler
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public ContactManager ContactManager
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public ConversationManager ConversationManager
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public DelegatorClient[] DelegatorClients
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public DeviceManager DeviceManager
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public bool InSuppressedMode
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public ContactManager PrivateContactManager
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public RoomManager RoomManager
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public Self Self
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public ClientSettings Settings
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public SignInConfiguration SignInConfiguration
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public ClientState State
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public ClientType Type
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public string Uri
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public Utilities Utilities
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public ApplicationRegistration CreateApplicationRegistration(string _appGuid, string _appName)
        {
            throw new NotImplementedException();
        }
        public AsynchronousOperation Initialize(string _clientName, string _version = "0", string _clientShortName = "0", string _clientNameAbbreviation = "0", string _clientLongName = "0", SupportedFeatures _supportedFeatures = SupportedFeatures.ucAllFeatures, [IUnknownConstant] object _CommunicatorClientCallback = null, object _state = null)
        {
            throw new NotImplementedException();
        }
        public AsynchronousOperation Shutdown([IUnknownConstant] object _CommunicatorClientCallback, object _state)
        {
            throw new NotImplementedException();
        }
        public AsynchronousOperation SignIn(string _userUri = "0", string _domainAndUsername = "0", string _password = "0", [IUnknownConstant] object _CommunicatorClientCallback = null, object _state = null)
        {
            throw new NotImplementedException();
        }
        public AsynchronousOperation SignOut([IUnknownConstant] object _CommunicatorClientCallback, object _state)
        {
            throw new NotImplementedException();
        }
        #endregion
        #region _ILyncClientEvents support
        public event _ILyncClientEvents_OnStateChangedEventHandler OnStateChanged;
        public event _ILyncClientEvents_OnNotificationReceivedEventHandler OnNotificationReceived;
        public event _ILyncClientEvents_OnCredentialRequestedEventHandler OnCredentialRequested;
        public event _ILyncClientEvents_OnSignInDelayedEventHandler OnSignInDelayed;
        public event _ILyncClientEvents_OnCapabilitiesChangedEventHandler OnCapabilitiesChanged;
        public event _ILyncClientEvents_OnDelegatorClientAddedEventHandler OnDelegatorClientAdded;
        public event _ILyncClientEvents_OnDelegatorClientRemovedEventHandler OnDelegatorClientRemoved;
        // Notifies Office apps that the IM client state (signed out, signing in, singed in, signing out, etc) has changed.
        internal void RaiseOnStateChangedEvent(ClientStateChangedEventData eventData)
        {
            if (this.OnStateChanged != null)
            {
                this.OnStateChanged(this, eventData);
            }
        }
        // Notifies Office apps that the IM client has received a notification event from MAPI (e.g. autodiscover has finished)
        internal void RaiseOnNotificationReceivedEvent(LyncClientNotificationReceivedEventData eventData)
        {
            if (this.OnNotificationReceived != null)
            {
                this.OnNotificationReceived(this, eventData);
            }
        }
        // Notifies Office apps that the IM client has received a request for credentials for some operation (e.g. sign in, web search)
        internal void RaiseOnCredentialRequestedEvent(CredentialRequestedEventData eventData)
        {
            if (this.OnCredentialRequested != null)
            {
                this.OnCredentialRequested(this, eventData);
            }
        }
        // Notifies Office apps that the IM client has been delayed from signing in and gives an estimated delay time.
        internal void RaiseOnSignInDelayedEvent(SignInDelayedEventData eventData)
        {
            if (this.OnSignInDelayed != null)
            {
                this.OnSignInDelayed(this, eventData);
            }
        }
        // Notifies Office apps that the capabilities of this IM client have changed.
        internal void RaiseOnCapabilitiesChangedEvent(PreferredCapabilitiesChangedEventData eventData)
        {
            if (this.OnCapabilitiesChanged != null)
            {
                this.OnCapabilitiesChanged(this, eventData);
            }
        }
        // Notifies Office apps that a DelegatorClient object has been added to the IM client object.
        internal void RaiseOnDelegatorClientAdded(DelegatorClientCollectionEventData eventData)
        {
            if (this.OnDelegatorClientAdded != null)
            {
                this.OnDelegatorClientAdded(this, eventData);
            }
        }
        // Notifies Office apps that a DelegatorClient object has been removed from the IM client object.
        internal void RaiseOnDelegatorClientRemoved(DelegatorClientCollectionEventData eventData)
        {
            if (this.OnDelegatorClientRemoved != null)
            {
                this.OnDelegatorClientRemoved(this, eventData);
            }
        }
        #endregion
    }
}
```

### <a name="iautomation-interface"></a><span data-ttu-id="f64cd-343">IAutomation-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="f64cd-343">IAutomation interface</span></span>
<span data-ttu-id="f64cd-344"><a name="off15_IMIntegration_ImplementRequired_IAutomation"> </a></span><span class="sxs-lookup"><span data-stu-id="f64cd-344"></span></span>

<span data-ttu-id="f64cd-p130">Die **IAutomation**-Schnittstelle automatisiert Funktionen der Clientanwendung für Chatnachrichten. Sie kann zum Starten von Unterhaltungen, Teilnehmen an Konferenzen und Bereitstellen von Erweiterungsfensterkontext verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f64cd-p130">The **IAutomation** interface automates features of the IM client application. It can be used to start conversations, join conferences, and provide extensibility window context.</span></span> 
  
<span data-ttu-id="f64cd-347">In Tabelle 4 werden die Elemente aufgeführt, die in der Klasse implementiert werden müssen, die von **IAutomation** erbt.</span><span class="sxs-lookup"><span data-stu-id="f64cd-347">Table 4 shows the members that must be implemented in the class that inherits from **IAutomation**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="f64cd-348">Elemente der **IAutomation**-Schnittstelle, die nicht in der Tabelle aufgeführt sind, müssen zwar vorhanden sein, jedoch nicht implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="f64cd-348">Any member of the **IAutomation** interface not listed in the table must be present but does not need to be implemented.</span></span> <span data-ttu-id="f64cd-349">Members, die vorhanden sind, jedoch nicht implementiert werden, können einen **NotImplementedException** oder **E_NOTIMPL**-Fehler zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="f64cd-349">Members that are present but not implemented can throw a **NotImplementedException** or **E_NOTIMPL** error.</span></span> 
> 
> <span data-ttu-id="f64cd-350">Weitere Informationen zu der **IAutomation**-Schnittstelle und den dazugehörigen Elementen finden Sie unter [UCCollaborationLib.IAutomation](http://msdn.microsoft.com/library/UCCollaborationLib.IAutomation).</span><span class="sxs-lookup"><span data-stu-id="f64cd-350">> For more information about the **IAutomation** interface and its members, see [UCCollaborationLib.IAutomation](http://msdn.microsoft.com/library/UCCollaborationLib.IAutomation).</span></span> 
  
<span data-ttu-id="f64cd-351">**Tabelle 4. Implementierung der IAutomation-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="f64cd-351">**Table 4. Implementation of IAutomation interface**</span></span>

|<span data-ttu-id="f64cd-352">**Element**</span><span class="sxs-lookup"><span data-stu-id="f64cd-352">**Member**</span></span>|<span data-ttu-id="f64cd-353">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f64cd-353">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f64cd-354">**StartConversation**-Methode</span><span class="sxs-lookup"><span data-stu-id="f64cd-354">**StartConversation** method</span></span>  <br/> |<span data-ttu-id="f64cd-p132">Startet eine Unterhaltung unter Verwendung der angegebenen Unterhaltungsmodalität. Es wird eine Instanz von **IConversationWindow** zurückgegeben.  </span><span class="sxs-lookup"><span data-stu-id="f64cd-p132">Starts a conversation using the specified conversation modality. An instance of **IConversationWindow** is returned.  </span></span><br/> |
   
## <a name="implementing-contact-presence-integration"></a><span data-ttu-id="f64cd-357">Implementieren der Kontaktanwesenheitsintegration</span><span class="sxs-lookup"><span data-stu-id="f64cd-357">Implementing contact presence integration</span></span>
<span data-ttu-id="f64cd-358"><a name="off15_IMIntegration_ImplementIMFeatures"> </a></span><span class="sxs-lookup"><span data-stu-id="f64cd-358"></span></span>

<span data-ttu-id="f64cd-p133">Neben den drei beschriebenen erforderlichen Schnittstellen gibt es weitere Schnittstellen, die zum Aktivieren der Kontaktanwesenheitsfunktionen in Office wichtig sind. Hierzu gehören die Folgenden:</span><span class="sxs-lookup"><span data-stu-id="f64cd-p133">In addition to the three required interfaces discussed previously, there are several other interfaces that are important for enabling contact presence functionality in Office. These include the following:</span></span>
  
- <span data-ttu-id="f64cd-361">Die [IContact](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContact)- oder **IContact2**-Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="f64cd-361">The [IContact](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContact) or **IContact2** interface.</span></span> 
    
- <span data-ttu-id="f64cd-362">Die [ISelf](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ISelf)-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="f64cd-362">The [ISelf](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ISelf) interface.</span></span> 
    
- <span data-ttu-id="f64cd-363">Die [IContactManager](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactManager)- und [_IContactManagerEvents](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactManager)-Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="f64cd-363">The [IContactManager](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactManager) and [_IContactManagerEvents](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactManager) interfaces.</span></span> 
    
- <span data-ttu-id="f64cd-364">Die [IGroup](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IGroup)- und [IGroupCollection](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IGroup)-Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="f64cd-364">The [IGroup](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IGroup) and [IGroupCollection](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IGroup) interfaces.</span></span> 
    
- <span data-ttu-id="f64cd-365">Die [IContactSubscription](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactSubscription)-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="f64cd-365">The [IContactSubscription](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactSubscription) interface.</span></span> 
    
- <span data-ttu-id="f64cd-366">Die [IContactEndPoint](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactEndPoint)-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="f64cd-366">The [IContactEndPoint](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactEndPoint) interface.</span></span> 
    
- <span data-ttu-id="f64cd-367">Die [ILocaleString](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ILocaleString)-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="f64cd-367">The [ILocaleString](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ILocaleString) interface</span></span> 
    
### <a name="icontact-interface"></a><span data-ttu-id="f64cd-368">IContact-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="f64cd-368">IContact interface</span></span>
<span data-ttu-id="f64cd-369"><a name="off15_IMIntegration_ImplementRequired_IContact"> </a></span><span class="sxs-lookup"><span data-stu-id="f64cd-369"></span></span>

<span data-ttu-id="f64cd-p134">Die **IContact**-Schnittstelle stellt einen Benutzer der Clientanwendung für Chatnachrichten dar. Die Schnittstelle legt Anwesenheitsinformationen, verfügbare Modalitäten, Gruppenmitgliedschaften und Kontakttypeigenschaften für einen Benutzer offen. Um eine Unterhaltung mit einem anderen Benutzer zu beginnen, müssen Sie diese Benutzerinstanz von **IContact** angeben.</span><span class="sxs-lookup"><span data-stu-id="f64cd-p134">The **IContact** interface represents an IM client application user. The interface exposes presence, available modalities, group membership, and contact type properties for a user. To start a conversation with another user, you must provide that user instance of **IContact**.</span></span>
  
<span data-ttu-id="f64cd-373">In Tabelle 5 werden die Elemente aufgeführt, die in der Klasse implementiert werden müssen, die von **IContact** erbt.</span><span class="sxs-lookup"><span data-stu-id="f64cd-373">Table 5 shows the members that must be implemented in the class that inherits from **IContact**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="f64cd-374">Elemente der **IContact**-Schnittstelle, die nicht in der Tabelle aufgeführt sind, müssen zwar vorhanden sein, jedoch nicht implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="f64cd-374">Any member of the **IContact** interface not listed in the table must be present but does not need to be implemented.</span></span> <span data-ttu-id="f64cd-375">Members, die vorhanden sind, jedoch nicht implementiert werden, können einen **NotImplementedException** oder **E_NOTIMPL**-Fehler zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="f64cd-375">Members that are present but not implemented can throw a **NotImplementedException** or **E_NOTIMPL** error.</span></span> 
>
> <span data-ttu-id="f64cd-376">Weitere Informationen zu der **IContact**-Schnittstelle und den dazugehörigen Elementen finden Sie unter [UCCollaborationLib.IContact](http://msdn.microsoft.com/library/UCCollaborationLib.IContact).</span><span class="sxs-lookup"><span data-stu-id="f64cd-376">> For more information about the **IContact** interface and its members, see [UCCollaborationLib.IContact](http://msdn.microsoft.com/library/UCCollaborationLib.IContact).</span></span> 
  
<span data-ttu-id="f64cd-377">**Tabelle 5. Implementierung der IContact-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="f64cd-377">**Table 5. Implementation of the IContact interface**</span></span>

|<span data-ttu-id="f64cd-378">**Element**</span><span class="sxs-lookup"><span data-stu-id="f64cd-378">**Member**</span></span>|<span data-ttu-id="f64cd-379">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f64cd-379">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f64cd-380">**CanStart**-Methode</span><span class="sxs-lookup"><span data-stu-id="f64cd-380">**CanStart** method</span></span>  <br/> |<span data-ttu-id="f64cd-381">Gibt **true** zurück, wenn ein bestimmter Typ Modalität für den Kontakt gestartet werden kann.</span><span class="sxs-lookup"><span data-stu-id="f64cd-381">Returns **true** if a given type of modality can be started on the contact.</span></span>  <br/> |
|<span data-ttu-id="f64cd-382">**GetContactInformation**-Methode</span><span class="sxs-lookup"><span data-stu-id="f64cd-382">**GetContactInformation** method</span></span>  <br/> |<span data-ttu-id="f64cd-383">Ruft ein Anwesenheitselement eines veröffentlichten Kontakts ab.</span><span class="sxs-lookup"><span data-stu-id="f64cd-383">Gets one presence item from a publishing contact.</span></span>  <br/> |
|<span data-ttu-id="f64cd-384">**BatchGetContactInformation**-Methode</span><span class="sxs-lookup"><span data-stu-id="f64cd-384">**BatchGetContactInformation** method</span></span>  <br/> |<span data-ttu-id="f64cd-385">Ruft mehrere Anwesenheitselemente eines veröffentlichten Kontakts ab.</span><span class="sxs-lookup"><span data-stu-id="f64cd-385">Gets multiple presence items from a publishing contact.</span></span>  <br/> |
|<span data-ttu-id="f64cd-386">**Settings**-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="f64cd-386">**Settings** property</span></span>  <br/> |<span data-ttu-id="f64cd-387">Ruft eine Sammlung von Kontakteigenschaften ab.</span><span class="sxs-lookup"><span data-stu-id="f64cd-387">Gets a collection of contact properties.</span></span>  <br/> |
|<span data-ttu-id="f64cd-388">**CustomGroups**-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="f64cd-388">**CustomGroups** property</span></span>  <br/> |<span data-ttu-id="f64cd-389">Ruft eine Sammlung von Gruppen auf, bei denen der Kontakt Mitglied ist.</span><span class="sxs-lookup"><span data-stu-id="f64cd-389">Gets a collection of groups that the contact is a member of.</span></span>  <br/> |
   
<span data-ttu-id="f64cd-p136">Während des Initialisierungsprozesses ruft die Office-Anwendung die **IContact.CanStart**-Methode auf, um die Chatfunktionen für den lokalen Benutzer zu ermitteln. Die **CanStart**-Methode verwendet eine Kennzeichnung aus der[UCCollaborationLib.ModalityTypes](http://msdn.microsoft.com/library/UCCollaborationLib.ModalityTypes)-Enumeration als Argument für den  __modalityTypes_-Parameter. Wenn der aktuelle Benutzer in der angeforderten Modalität einbezogen werden kann (d. h. der Benutzer verfügt über Chatfunktionen, Funktionen für Audio- und Videoanrufe oder Anwendungsfreigebe), gibt die **CanStart**-Methode **true** zurück.</span><span class="sxs-lookup"><span data-stu-id="f64cd-p136">During the initialization process, the Office application calls the **IContact.CanStart** method to determine the IM capabilities for the local user. The **CanStart** method takes a flag from the [UCCollaborationLib.ModalityTypes](http://msdn.microsoft.com/library/UCCollaborationLib.ModalityTypes) enumeration as an argument for the  __modalityTypes_ parameter. If the current user can engage in the requested modality (that is, the user is capable of instant messaging, audio and video messaging, or application sharing), the **CanStart** method returns **true**.</span></span>
  
```cs
public bool CanStart(ModalityTypes _modalityTypes)
{
    // Define the capabilities of the current IM client application
    // user by using flags from the ModalityTypes enumeration.
    ModalityTypes userCapabilities = 
        ModalityTypes.ucModalityInstantMessage | 
        ModalityTypes.ucModalityAudioVideo | 
        ModalityTypes.ucModalityAppSharing;
    // Perform a simple test for equivalency.
    if (_modalityType == userCapabilities) 
    {
        return true;
    }
    else 
    {
        return false;
    }
}

```

<span data-ttu-id="f64cd-p137">Die **GetContactInformation**-Methode ruft Informationen über den Kontakt aus dem **IContact**-Objekt ab. Der aufgerufene Code muss einen Wert aus der [UCCollaborationLib.ContactInformationType](http://msdn.microsoft.com/library/UCCollaborationLib.ContactInformationType)-Enumeration für den  __contactInformationType_-Parameter übergeben, der die abzurufenden Daten angibt.</span><span class="sxs-lookup"><span data-stu-id="f64cd-p137">The **GetContactInformation** method retrieves information about the contact from the **IContact** object. The calling code needs to pass in a value from the [UCCollaborationLib.ContactInformationType](http://msdn.microsoft.com/library/UCCollaborationLib.ContactInformationType) enumeration for the  __contactInformationType_ parameter, which indicates the data to be retrieved.</span></span> 
  
```cs
public object GetContactInformation(
    ContactInformationType _contactInformationType)
{
    // Determine the information to return from the contact's data based
    // on the value passed in for the _contactInformationType parameter.
    switch (_contactInformationType)
    {
        case ContactInformationType.ucPresenceEmailAddresses:
        {
            // Return the URI associated with the contact.
            string returnValue = this.Uri.ToLower().Replace("sip:", String.Empty);
            return returnValue;
        }
        case ContactInformationType.ucPresenceDisplayName:
        {
            // Return the display name associated with the contact.
            string returnValue = this._DisplayName;
            return returnValue;
        }
        default:
        {
            throw new NotImplementedException;
        }
        // Additional implementation details omitted.
    }
}
```

<span data-ttu-id="f64cd-p138">Ähnlich wie **GetContactInformation**ruft die **BatchGetContactInformation**-Methode mehrere Anwesenheitselemente des Kontakts aus dem **IContact**-Objekt ab. Der aufgerufene Code muss ein Array von Werten aus der **ContactInformationType**-Enumeration für den  __contactInformationTypes_-Parameter übergeben. Die Methode gibt ein [UCCollaborationLib.IContactInformationDictionary](http://msdn.microsoft.com/library/UCCollaborationLib.IContactInformationDictionary)-Objekt mit den angeforderten Daten zurück.</span><span class="sxs-lookup"><span data-stu-id="f64cd-p138">Similar to the **GetContactInformation**, the **BatchGetContactInformation** method retrieves multiple presence items about the contact from the **IContact** object. The calling code needs to pass in an array of values from the **ContactInformationType** enumeration for the  __contactInformationTypes_ parameter. The method returns an [UCCollaborationLib.IContactInformationDictionary](http://msdn.microsoft.com/library/UCCollaborationLib.IContactInformationDictionary) object that contains the requested data.</span></span> 
  
```cs
public IMClientContactInformationDictionary BatchGetContactInformation(
    ContactInformationType[] _contactInformationTypes)
{
    // The IMClientContactInformationDictionary class implements the
    // IContactInformationDictionary interface.
    IMClientContactInformationDictionary contactDictionary = 
        new IMClientContactInformationDictionary();
    foreach (ContactInformationType type in _contactInformationTypes)
    {
        // Call GetContactInformation for each type of contact 
        // information to retrieve. This code adds a new entry to
        // a Dictionary object exposed by the
        // ContactInformationDictionary property.
        contactDictionary.ContactInformationDictionary.Add(
            type, this.GetContactInformation(type));
    }
    return contactDictionary;
}
```

<span data-ttu-id="f64cd-398">Die **IContact.Settings**-Eigenschaft gibt ein **IContactSettingDictionary**-Objekt mit den benutzerdefinierte Eigenschaften des Kontakts zurück.</span><span class="sxs-lookup"><span data-stu-id="f64cd-398">The **IContact.Settings** property returns an **IContactSettingDictionary** object that contains custom properties about the contact.</span></span> 
  
```cs
public IMClientContactSettingDictionary Settings
{
    get
    {
       // The IMClientContactSettingDictionary class implements
       // the IContactSettingDictionary interface.
       return new IMClientContactSettingDictionary();
    }
}
```

<span data-ttu-id="f64cd-399">Die **IContact.CustomGroups**-Eigenschaft gibt ein **IGroupCollection**-Objekt mit allen Gruppen zurück, bei denen der Kontakt Mitglied ist.</span><span class="sxs-lookup"><span data-stu-id="f64cd-399">The **IContact.CustomGroups** property returns an **IGroupCollection** object that includes all of the groups of which the contact is a member.</span></span> 
  
```cs
public IMClientGroupCollection CustomGroups
{
    get {
       // The IMClientGroupCollection class implements
       // the IGroupCollection interface.
        return new IMClientGroupCollection();
    }
}
```

### <a name="iself-interface"></a><span data-ttu-id="f64cd-400">ISelf-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="f64cd-400">ISelf interface</span></span>
<span data-ttu-id="f64cd-401"><a name="off15_IMIntegration_ImplementRequired_ISelf"> </a></span><span class="sxs-lookup"><span data-stu-id="f64cd-401"></span></span>

<span data-ttu-id="f64cd-p139">Während des Initialisierungsprozesses ruft die Office-Anwendung die Daten für den aktuellen Benutzer durch Zugriff auf die **ILyncClient.Self**-Eigenschaft ab, die ein **ISelf**-Objekt zurückgeben muss. Die **ISelf**-Schnittstelle stellt den lokalen, bei der Clientanwendung für Chatnachrichten angemeldeten Benutzer dar.</span><span class="sxs-lookup"><span data-stu-id="f64cd-p139">During the initialization process, the Office application gets the data for the current user by accessing the **ILyncClient.Self** property, which must return an **ISelf** object. The **ISelf** interface represents the local, signed-in IM client application user.</span></span> 
  
<span data-ttu-id="f64cd-404">In Tabelle 6 werden die Elemente aufgeführt, die in der Klasse implementiert werden müssen, die von **ISelf** erbt.</span><span class="sxs-lookup"><span data-stu-id="f64cd-404">Table 6 shows the members that must be implemented in the class that inherits from **ISelf**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="f64cd-p140">Elemente der **ISelf**-Schnittstelle, die nicht in der Tabelle aufgeführt sind, müssen zwar vorhanden sein, jedoch nicht implementiert werden. Elemente, die vorhanden sind, jedoch nicht implementiert werden, können einen **NotImplementedException**- oder **E_NOTIMPL**-Fehler zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="f64cd-p140">Any member of the **ISelf** interface not listed in the table must be present but does not need to be implemented. Members that are present but not implemented can throw a **NotImplementedException** or **E_NOTIMPL** error.</span></span> 
  
<span data-ttu-id="f64cd-407">**Tabelle 6. Implementierung der ISelf-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="f64cd-407">**Table 6. Implementation of the ISelf interface**</span></span>

|<span data-ttu-id="f64cd-408">**Element**</span><span class="sxs-lookup"><span data-stu-id="f64cd-408">**Member**</span></span>|<span data-ttu-id="f64cd-409">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f64cd-409">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f64cd-410">**Contact**-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="f64cd-410">**Contact** property</span></span>  <br/> |<span data-ttu-id="f64cd-411">Ruft das **IContact**-Objekt ab, das mit dem lokalen Benutzer verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="f64cd-411">Gets the **IContact** object associated with the local user.</span></span>  <br/> |
   
<span data-ttu-id="f64cd-p141">Anwesenheitsinformationen, verfügbare Modalitäten, Gruppenmitgliedschaften und Kontakttypeigenschaften für den lokalen Benutzer werden über die **ISelf.Contact**-Eigenschaft verfügbar gemacht (gibt ein **IContact**-Objekt zurück). Während des Initialisierungsprozesses greift die Office-Anwendung auf die **ISelf.Contact**-Eigenschaft zu, um einen Verweis auf die Kontaktinformationen des lokalen Benutzers abzurufen.</span><span class="sxs-lookup"><span data-stu-id="f64cd-p141">Presence, available modalities, group membership, and contact type properties for the local user are exposed through the **ISelf.Contact** property (which returns an **IContact** object). During the initialization process, the Office application accesses the **ISelf.Contact** property to get a reference to the contact information for the local user.</span></span> 
  
<span data-ttu-id="f64cd-414">Verwenden Sie den folgenden Code zum Definieren einer Klasse, die von der **ISelf**-Schnittstellen erbt, die die **Contact**-Eigenschaft implementiert.</span><span class="sxs-lookup"><span data-stu-id="f64cd-414">Use the following code to define a class that inherits from the **ISelf** interface that implements the **Contact** property.</span></span> 
  
```cs
[ComVisible(true)]
public class IMClientSelf : ISelf
{
    // Declare a private field to store contact data for local user.
    private IMClientContact _contactData;
    // In the constructor for the ISelf object, the calling code 
    // must supply contact data.
    public IMClientSelf (IMClientContact _selfContactData)
    {
        this._contactData = _selfContactData;
    }
    // When accessed, the Contact property returns a reference
    // to the IContact object that represents the local user.
    public IMClientContact Contact
    {
        get
        {
            return this._contactData as IMClientContact;
        }
    }
    // Additional implementation details omitted.
}
```

### <a name="icontactmanager-and-icontactmanagerevents-interfaces"></a><span data-ttu-id="f64cd-415">IContactManager- und _IContactManagerEvents-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="f64cd-415">IContactManager and _IContactManagerEvents interfaces</span></span>
<span data-ttu-id="f64cd-416"><a name="off15_IMIntegration_ImplementRequired_IContactManager"> </a></span><span class="sxs-lookup"><span data-stu-id="f64cd-416"></span></span>

<span data-ttu-id="f64cd-p142">Das **IContactManager**-Objekt verwaltet die Kontakte für den lokalen Benutzer, einschließlich der Kontaktinformationen des lokalen Benutzers. Die Office-Anwendung verwendet ein **IContactManager**-Objekt für den Zugriff auf **IContact**-Objekte, die den Kontakten des lokalen Benutzers entsprechen.</span><span class="sxs-lookup"><span data-stu-id="f64cd-p142">The **IContactManager** object manages the contacts for the local user, including the local user's own contact information. The Office application uses an **IContactManager** object to access **IContact** objects that correspond to the local user's contacts.</span></span> 
  
<span data-ttu-id="f64cd-419">In Tabelle 7 werden die Elemente aufgeführt, die in der Klasse implementiert werden müssen, die von **IContactManager** und **_IContactManagerEvents** erbt.</span><span class="sxs-lookup"><span data-stu-id="f64cd-419">Table 7 shows the members that must be implemented in the class that inherits from **IContactManager** and **_IContactManagerEvents**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="f64cd-420">Jegliche Elemente der **IContactManager**-Schnittstelle, die nicht in der Tabelle aufgeführt sind, müssen zwar vorhanden sein, jedoch nicht implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="f64cd-420">Any member of the **IContactManager** interface not listed in the table must be present but does not need to be implemented.</span></span> <span data-ttu-id="f64cd-421">Elemente, die vorhanden sind, jedoch nicht implementiert werden, können einen **NotImplementedException** or **E\_NOTIMPL**-Fehler zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="f64cd-421">Members that are present but not implemented can throw a NotImplementedException or E_NOTIMPL error.</span></span> 
>
> <span data-ttu-id="f64cd-422">Weitere Informationen zu den **IContactManager**- und **_IContactManagerEvents**-Schnittstellen und den dazugehörigen Elementen finden Sie unter [UCCollaborationLib.IContactManager](http://msdn.microsoft.com/library/UCCollaborationLib.IContactManager) und [UCCollaborationLib._IContactManagerEvents](http://msdn.microsoft.com/library/UCCollaborationLib._IContactManagerEvents).</span><span class="sxs-lookup"><span data-stu-id="f64cd-422">> For more information about the **IContactManager** and **_IContactManagerEvents** interfaces and their members, see [UCCollaborationLib.IContactManager](http://msdn.microsoft.com/library/UCCollaborationLib.IContactManager) and [UCCollaborationLib._IContactManagerEvents](http://msdn.microsoft.com/library/UCCollaborationLib._IContactManagerEvents).</span></span> 
  
<span data-ttu-id="f64cd-423">**Tabelle 7. Implementierung der IContactManager- und _IContactManagerEvents-Schnittstellen**</span><span class="sxs-lookup"><span data-stu-id="f64cd-423">**Table 7. Implementation of the IContactManager and _IContactManagerEvents interfaces**</span></span>

|<span data-ttu-id="f64cd-424">**Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="f64cd-424">**Interface**</span></span>|<span data-ttu-id="f64cd-425">**Element**</span><span class="sxs-lookup"><span data-stu-id="f64cd-425">**Member**</span></span>|<span data-ttu-id="f64cd-426">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f64cd-426">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f64cd-427">**IContactManager**</span><span class="sxs-lookup"><span data-stu-id="f64cd-427">**IContactManager**</span></span> <br/> |<span data-ttu-id="f64cd-428">**GetContactByUri**-Methode</span><span class="sxs-lookup"><span data-stu-id="f64cd-428">**GetContactByUri** method</span></span>  <br/> |<span data-ttu-id="f64cd-429">Sucht oder erstellt eine Instanz des neuen Kontakts mit dem Kontakt-URI.</span><span class="sxs-lookup"><span data-stu-id="f64cd-429">Finds or creates a new contact instance by using the contact URI.</span></span>  <br/> |
||<span data-ttu-id="f64cd-430">**CreateSubscription**-Methode</span><span class="sxs-lookup"><span data-stu-id="f64cd-430">**CreateSubscription** method</span></span>  <br/> |<span data-ttu-id="f64cd-431">Erstellt ein **ISubscription**-Objekt, das für die Batchverarbeitung von Abonnements oder Abfragen verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="f64cd-431">Creates an **ISubscription** object that can be used for batching subscriptions or queries.</span></span>  <br/> |
||<span data-ttu-id="f64cd-432">**Lookup**-Methode</span><span class="sxs-lookup"><span data-stu-id="f64cd-432">**Lookup** method</span></span>  <br/> |<span data-ttu-id="f64cd-433">Sucht nach einer Kontakt- oder Verteilergruppe.</span><span class="sxs-lookup"><span data-stu-id="f64cd-433">Looks up a contact or distribution group.</span></span>  <br/> |
|<span data-ttu-id="f64cd-434">**_IContactManagerEvents**</span><span class="sxs-lookup"><span data-stu-id="f64cd-434">**_IContactManagerEvents**</span></span> <br/> |<span data-ttu-id="f64cd-435">**OnGroupAdded**-Ereignis</span><span class="sxs-lookup"><span data-stu-id="f64cd-435">**OnGroupAdded** event</span></span>  <br/> |<span data-ttu-id="f64cd-p144">Wird ausgelöst, wenn eine Gruppe zu einer Gruppensammlung hinzugefügt wird. Die aktualisierte Gruppensammlung kann aus der **IContactManager.Groups**-Eigenschaft abgerufen werden.  </span><span class="sxs-lookup"><span data-stu-id="f64cd-p144">Raised when a group is added to a group collection. The updated group collection can be obtained from the **IContactManager.Groups** property.  </span></span><br/> |
||<span data-ttu-id="f64cd-438">**OnGroupRemoved**-Ereignis</span><span class="sxs-lookup"><span data-stu-id="f64cd-438">**OnGroupRemoved** event</span></span>  <br/> |<span data-ttu-id="f64cd-p145">Wird ausgelöst, wenn eine Gruppe aus einer Gruppensammlung entfernt wird. Die aktualisierte Gruppensammlung kann aus der **IContactManager.Groups**-Eigenschaft abgerufen werden.  </span><span class="sxs-lookup"><span data-stu-id="f64cd-p145">Raised when a group is removed from a group collection. The updated group collection can be obtained from the **IContactManager.Groups** property.  </span></span><br/> |
||<span data-ttu-id="f64cd-441">**OnSearchProviderStateChanged**-Ereignis</span><span class="sxs-lookup"><span data-stu-id="f64cd-441">**OnSearchProviderStateChanged** event</span></span>  <br/> |<span data-ttu-id="f64cd-442">Wird bei Statusänderung des Suchanbieters ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="f64cd-442">Raised when a search provider's status changes.</span></span>  <br/> |
   
<span data-ttu-id="f64cd-p146">Office ruft **IContactManager.GetContactByUri** zum Abrufen von Anwesenheitsinformationen eines Kontakts unter Verwendung der SIP-Adresse des Kontakts auf. Wenn ein Kontakt für eine SIP-Adresse in Active Directory konfiguriert ist, bestimmt Office diese Adresse für einen Kontakt und ruft **GetContactByUri** auf und übergibt die SIP-Adresse des Kontakts für den  __contactUri_-Parameter.</span><span class="sxs-lookup"><span data-stu-id="f64cd-p146">Office calls **IContactManager.GetContactByUri** to get a contact's presence information, by using the SIP address of the contact. When a contact is configured for an SIP address in the Active Directory, Office determines this address for a contact and calls **GetContactByUri**, passing the SIP address of the contact in for the  __contactUri_ parameter.</span></span> 
  
<span data-ttu-id="f64cd-p147">Wenn Office die SIP-Adresse des Kontakts nicht bestimmen kann, ruft es die **IContactManager.Lookup**-Methode auf, um die SIP über den Chatdienst zu finden. In diesem Fall übergibt Office die besten verfügbaren Daten für den Kontakt (z. B. nur die E-Mail-Adresse für den Kontakt). Die **Lookup**-Methode gibt asynchron ein **AsynchronousOperation**-Objekt zurück. Beim Aufrufen des Rückrufs sollte die **Lookup**-Methode neben dem zurückgegebenen URI des Kontakts angeben, ob der Vorgang erfolgreich war oder dabei ein Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="f64cd-p147">When Office cannot determine the SIP address for the contact, it calls the **IContactManager.Lookup** method to find the SIP by using the IM service. Here Office passes in the best data that it can find for the contact (for example, just the email address for the contact). The **Lookup** method asynchronously returns an **AsynchronousOperation** object. When it invokes the callback, the **Lookup** method should return the success or failure of the operation in addition to the URI of the contact.</span></span> 
  
```cs
public IMClientContact GetContactByUri(string _contactUri)
{
    // Declare a Contact variable to contain information about the contact.
    IMClientContact tempContact = null;
    // The _groupCollections field is an IGroupCollection object. Iterate 
    // over each group in collection to see if the 
    // contact is a part of the group.
    foreach (IMClientGroup group in this._groupCollections)
    {
       if (group.TryGetContact(_contactUri, out tempContact))
       {
           break;
       }
    }
    // Check to see that the URI returned a valid contact. If it
    // did not, create a new contact.
    if (tempContact == null)
    {
        tempContact = IMClientContact.BuildContact(_contactUri);
    }
    // Return the contact to the calling code.
    return tempContact;
}
```

<span data-ttu-id="f64cd-p148">Die Office-Anwendung muss Anwesenheitsänderungen für einen bestimmten Kontakt abonnieren. Bei einer Änderung des Anwesenheitsstatus des Kontakts sendet der Chatserver eine Benachrichtigung an die Clientanwendung für Chatnachrichten, wodurch die Office-Anwendung ebenfalls benachrichtigt wird. Dazu ruft die Office-Anwendung die **IContactManager.CreateSubscription**-Methode zum Erstellen eines neuen **IContactSubscription**-Objekts für diese Anforderung auf.</span><span class="sxs-lookup"><span data-stu-id="f64cd-p148">The Office application needs to subscribe to presence changes for an individual contact. Thus, when a contact's presence status changes, the IM server alerts the IM client application—thereby alerting the Office application. To do this, the Office application calls the **IContactManager.CreateSubscription** method to create a new **IContactSubscription** object for this request.</span></span> 
  
```cs
// Declare a private field to contain an IContactSubscription object.
private IMClientContactSubscription _contactSubscription;
// Return the IContactSubscription object associated 
// with the IContactManager object.
public IMClientContactSubscription CreateSubscription()
{
    return this._contactSubscription;
}
```

### <a name="igroup-and-igroupcollection-interfaces"></a><span data-ttu-id="f64cd-452">IGroup- und IGroupCollection-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="f64cd-452">IGroup and IGroupCollection interfaces</span></span>
<span data-ttu-id="f64cd-453"><a name="off15_IMIntegration_ImplementRequired_IGroup"> </a></span><span class="sxs-lookup"><span data-stu-id="f64cd-453"></span></span>

<span data-ttu-id="f64cd-p149">Das **IGroup**-Objekt gibt eine Sammlung von Kontakten mit zusätzlichen Eigenschaften zum Identifizieren der Kontaktsammlung unter Verwendung eines kollektiven Gruppennamens an. Ein **IGroupCollection**-Objekt gibt eine Sammlung von **IGroup**-Objekten an, die durch einen lokalen Benutzer und die Clientanwendung für Chatnachrichten definiert werden. Die Office-Anwendung verwendet die **IGroupCollection**- und **IGroup**-Objekte zum Zugreifen auf die Kontakte des lokalen Benutzers.</span><span class="sxs-lookup"><span data-stu-id="f64cd-p149">The **IGroup** object represents a collection of contacts with additional properties for identifying the contact collection by a collective group name. An **IGroupCollection** object represents a collection of **IGroup** objects defined by a local user and the IM client application. The Office application uses the **IGroupCollection** and **IGroup** objects to access the local user's contacts.</span></span> 
  
<span data-ttu-id="f64cd-457">In Tabelle 9 werden die Elemente aufgeführt, die in den Klassen implementiert werden müssen, die von **IGroup** und **IGroupCollection** in der folgenden Tabelle erben.</span><span class="sxs-lookup"><span data-stu-id="f64cd-457">Table 9 shows the members that must be implemented in the classes that inherit from **IGroup** and **IGroupCollection** in the following table.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="f64cd-458">Elemente der **IGroup**-Schnittstelle, die nicht in der Tabelle aufgeführt sind, müssen zwar vorhanden sein, jedoch nicht implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="f64cd-458">Any member of the **IGroup** interface not listed in the table must be present but does not need to be implemented.</span></span> <span data-ttu-id="f64cd-459">Members, die vorhanden sind, jedoch nicht implementiert werden, können einen **NotImplementedException** oder **E_NOTIMPL**-Fehler zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="f64cd-459">Members that are present but not implemented can throw a **NotImplementedException** or **E_NOTIMPL** error.</span></span> 
>
> <span data-ttu-id="f64cd-460">Weitere Informationen zu den **IGroup**- und **IGroupCollection**-Schnittstellen und den dazugehörigen Elementen finden Sie unter [UCCollaborationLib.IGroup](http://msdn.microsoft.com/library/UCCollaborationLib.IGroup) und [UCCollaborationLib.IGroupCollection](http://msdn.microsoft.com/library/UCCollaborationLib.IGroupCollection).</span><span class="sxs-lookup"><span data-stu-id="f64cd-460">> For more information about the **IGroup** and **IGroupCollection** interfaces and their members, see [UCCollaborationLib.IGroup](http://msdn.microsoft.com/library/UCCollaborationLib.IGroup) and [UCCollaborationLib.IGroupCollection](http://msdn.microsoft.com/library/UCCollaborationLib.IGroupCollection).</span></span> 
  
<span data-ttu-id="f64cd-461">**Tabelle 9. Implementierung der IGroup- und IGroupCollection-Schnittstellen**</span><span class="sxs-lookup"><span data-stu-id="f64cd-461">**Table 9. Implementation of the IGroup and IGroupCollection interfaces**</span></span>

|<span data-ttu-id="f64cd-462">**Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="f64cd-462">**Interface**</span></span>|<span data-ttu-id="f64cd-463">**Element**</span><span class="sxs-lookup"><span data-stu-id="f64cd-463">**Member**</span></span>|<span data-ttu-id="f64cd-464">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f64cd-464">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f64cd-465">**IGroupCollection**</span><span class="sxs-lookup"><span data-stu-id="f64cd-465">**IGroupCollection**</span></span> <br/> |<span data-ttu-id="f64cd-466">**Count**-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="f64cd-466">**Count** property</span></span>  <br/> |<span data-ttu-id="f64cd-467">Gibt die Anzahl von **IGroup**-Objekten in der Sammlung zurück.</span><span class="sxs-lookup"><span data-stu-id="f64cd-467">Returns the count of **IGroup** objects in the collection</span></span>  <br/> |
||<span data-ttu-id="f64cd-468">**Item**-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="f64cd-468">**Item** property</span></span>  <br/> |<span data-ttu-id="f64cd-469">Gibt das **IGroup**-Objekt an der angegebenen Indexposition in der Sammlung zurück.</span><span class="sxs-lookup"><span data-stu-id="f64cd-469">Returns the **IGroup** object at the specified index in the collection.</span></span>  <br/> |
|<span data-ttu-id="f64cd-470">**IGroup**</span><span class="sxs-lookup"><span data-stu-id="f64cd-470">**IGroup**</span></span> <br/> |<span data-ttu-id="f64cd-471">**Id**-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="f64cd-471">**Id** property</span></span>  <br/> |<span data-ttu-id="f64cd-472">Gibt die ID der Gruppe zurück.</span><span class="sxs-lookup"><span data-stu-id="f64cd-472">Returns the ID of the group.</span></span>  <br/> |
   
<span data-ttu-id="f64cd-p151">Wenn die Office-Anwendung die Informationen für den lokalen Benutzer abruft, greift es auf die Gruppenmitgliedschaften des Kontakts (lokaler Benutzer) durch Aufrufen der **IContact.CustomGroups**-Eigenschaft zu, die ein **IGroupCollection**-Objekt zurückgibt. **IGroupCollection** muss ein Array (oder **List**) von **IGroup**-Objekten enthalten. Die Klasse, die von **IGroupCollection** abgeleitet wird, muss eine **Count**-Eigenschaft verfügbar machen, die die Anzahl der Elemente in der Sammlung und eine Indexermethode zurückgibt, **this(int)**, welche ein **IGroup**-Objekt aus der Sammlung zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="f64cd-p151">When the Office application gets the information for the local user, it accesses the group memberships of the contact (local user) by calling the **IContact.CustomGroups** property, which returns an **IGroupCollection** object. The **IGroupCollection** must contain an array (or **List**) of **IGroup** objects. The class that derives from **IGroupCollection** must expose a **Count** property, which returns the number of items in the collection, and an indexer method, **this(int)**, which returns an **IGroup** object from the collection.</span></span> 
  
### <a name="icontactsubscription-interface"></a><span data-ttu-id="f64cd-476">IContactSubscription-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="f64cd-476">IContactSubscription interface</span></span>
<span data-ttu-id="f64cd-477"><a name="off15_IMIntegration_ImplementRequired_IContactSubscription"> </a></span><span class="sxs-lookup"><span data-stu-id="f64cd-477"></span></span>

<span data-ttu-id="f64cd-p152">Mit der **IContactSubscription**-Schnittstelle können Sie die Kontakte angeben, die Änderungen an Anwesenheitsinformationen erhalten, und die Typen der Anwesenheitsinformationen, die eine Benachrichtigung auslösen. Office-Anwendungen verwenden ein **IContactSubscription**-Objekt zum Registrieren von Änderungen am Anwesenheitsstatus des Kontakts.</span><span class="sxs-lookup"><span data-stu-id="f64cd-p152">The **IContactSubscription** interface allows you to specify the contacts to receive presence information updates for and the types of presence information that trigger a notification. Office applications use an **IContactSubscription** object to register changes to contact's presence status.</span></span> 
  
<span data-ttu-id="f64cd-480">In Tabelle 10 werden die Elemente aufgeführt, die in den Klassen implementiert werden müssen, die von **IContactSubscription** erben.</span><span class="sxs-lookup"><span data-stu-id="f64cd-480">Table 10 shows the members that must be implemented in the classes that inherit from **IContactSubscription**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="f64cd-481">Elemente der **IContactSubscription**-Schnittstelle, die nicht in der Tabelle aufgeführt sind, müssen zwar vorhanden sein, jedoch nicht implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="f64cd-481">Any member of the **IContactSubscription** interface not listed in the table must be present but does not need to be implemented.</span></span> <span data-ttu-id="f64cd-482">Members, die vorhanden sind, jedoch nicht implementiert werden, können einen **NotImplementedException** oder **E_NOTIMPL**-Fehler zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="f64cd-482">Members that are present but not implemented can throw a **NotImplementedException** or **E_NOTIMPL** error.</span></span>
>
> <span data-ttu-id="f64cd-483">Weitere Informationen zu der **IContactSubscription**Schnittstelle und den dazugehörigen Elementen finden Sie unter [UCCollaborationLib.IContactSubscription](http://msdn.microsoft.com/library/UCCollaborationLib.IContactSubscription).</span><span class="sxs-lookup"><span data-stu-id="f64cd-483">> For more information about the **IContactSubscription** interface and its members, see [UCCollaborationLib.IContactSubscription](http://msdn.microsoft.com/library/UCCollaborationLib.IContactSubscription).</span></span> 
  
<span data-ttu-id="f64cd-484">**Tabelle 10. Implementierung der IContactSubscription-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="f64cd-484">**Table 10. Implementation of the IContactSubscription interface**</span></span>

|<span data-ttu-id="f64cd-485">**Element**</span><span class="sxs-lookup"><span data-stu-id="f64cd-485">**Member**</span></span>|<span data-ttu-id="f64cd-486">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f64cd-486">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f64cd-487">**AddContact**-Methode</span><span class="sxs-lookup"><span data-stu-id="f64cd-487">**AddContact** method</span></span>  <br/> |<span data-ttu-id="f64cd-488">Fügt einen Kontakt zum Abonnementobjekt hinzu.</span><span class="sxs-lookup"><span data-stu-id="f64cd-488">Adds a contact to the subscription object.</span></span>  <br/> |
|<span data-ttu-id="f64cd-489">**Subscribe**-Methode</span><span class="sxs-lookup"><span data-stu-id="f64cd-489">**Subscribe** method</span></span>  <br/> |<span data-ttu-id="f64cd-490">Hilft der Clientanwendung für Chatnachrichten bei der Überwachung der Anwesenheit eines Kontakts.</span><span class="sxs-lookup"><span data-stu-id="f64cd-490">Helps the IM client application to monitor presence for a contact.</span></span>  <br/> |
   
<span data-ttu-id="f64cd-p154">Die **IContactSubscription**-Schnittstelle muss einen Verweis auf alle überwachten **IContact**-Objekte unter Verwendung eines Arrays oder eines **List**-Objekts enthalten. Die **IContactSubscription.AddContact**-Methode fügt ein **IContact**-Objekt für die zugrunde liegende Datenstruktur des **IContactSubscription**-Objekts hinzu und fügt dabei einen neuen Kontakt hinzu, dessen Anwesenheitsänderungen überwacht werden sollen.</span><span class="sxs-lookup"><span data-stu-id="f64cd-p154">The **IContactSubscription** interface must contain a reference to all the **IContact** objects that it monitors, using an array or a **List**. The **IContactSubscription.AddContact** method adds an **IContact** object for the to the underlying data structure of the **IContactSubscription** object, thereby adding a new contact to monitor for presence changes.</span></span> 
  
```cs
// Store references to all of the IContact objects to subscribe to.
private List<IMClientContact> _subscribedContacts;
// Add a new IContact object to the collection of contacts.
public void AddContact(IMClientContact _contact)
{
    this._subscribedContacts.Add(_contact);
}
```

<span data-ttu-id="f64cd-p155">Mit der **IContactSubscription.Subscribe**-Methode kann eine Clientanwendung für Chatnachrichten auf Beobachter der Anwesenheitsinformationen eines Kontakts zugreifen. Sie können eine Abrufstrategie zum Abrufen der Anwesenheitsinformationen vom Server für die Kontakte verwenden, die die Clientanwendung für Chatnachrichten abonniert hat. Die **Subscribe**-Methode ist nützlich,wenn Anwesenheitsinformationen für Personen außerhalb der Kontaktliste eines Benutzers (z. B. von einem größeren öffentlichen Netzwerk) angefordert werden.</span><span class="sxs-lookup"><span data-stu-id="f64cd-p155">The **IContactSubscription.Subscribe** method allows an IM client application to access presence observers for the contact. It can use a polling strategy to get the presence from the server for the contacts for that the IM client application has subscribed to. The **Subscribe** method is helpful in situations where presence is requested for someone outside of a user's contact list (for example, from a larger public network).</span></span> 
  
### <a name="icontactendpoint-interface"></a><span data-ttu-id="f64cd-496">IContactEndPoint-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="f64cd-496">IContactEndPoint interface</span></span>
<span data-ttu-id="f64cd-497"><a name="off15_IMIntegration_ImplementRequired_IContactEndPoint"> </a></span><span class="sxs-lookup"><span data-stu-id="f64cd-497"></span></span>

<span data-ttu-id="f64cd-498">Das **IContactEndPoint**-Objekt gibt eine Telefonnummer aus der Sammlung von Telefonnummern eines Kontakts an.</span><span class="sxs-lookup"><span data-stu-id="f64cd-498">The **IContactEndPoint** represents a telephone number from a contact's collection of telephone numbers.</span></span> 
  
<span data-ttu-id="f64cd-499">In Tabelle 11 werden die Elemente aufgeführt, die in den Klassen implementiert werden müssen, die von **IContactEndPoint** erben.</span><span class="sxs-lookup"><span data-stu-id="f64cd-499">Table 11 shows the members that must be implemented in the classes that inherit from **IContactEndPoint**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="f64cd-500">Elemente der **IContactEndPoint**-Schnittstelle, die nicht in der Tabelle aufgeführt sind, müssen zwar vorhanden sein, jedoch nicht implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="f64cd-500">Any member of the **IContactEndPoint** interface not listed in the table must be present but does not need to be implemented.</span></span> <span data-ttu-id="f64cd-501">Members, die vorhanden sind, jedoch nicht implementiert werden, können einen **NotImplementedException** oder **E_NOTIMPL**-Fehler zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="f64cd-501">Members that are present but not implemented can throw a **NotImplementedException** or **E_NOTIMPL** error.</span></span>
>
> <span data-ttu-id="f64cd-502">Weitere Informationen zu der **IContactEndPoint**Schnittstelle und den dazugehörigen Elementen finden Sie unter [UCCollaborationLib.IContactEndpoint](http://msdn.microsoft.com/library/UCCollaborationLib.IContactEndpoint).</span><span class="sxs-lookup"><span data-stu-id="f64cd-502">> For more information about the **IContactEndPoint** interface and its members, see [UCCollaborationLib.IContactEndpoint](http://msdn.microsoft.com/library/UCCollaborationLib.IContactEndpoint).</span></span> 
  
<span data-ttu-id="f64cd-503">**Tabelle 11. Implementierung der IContactEndPoint-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="f64cd-503">**Table 11. Implementation of the IContactEndPoint interface**</span></span>

|<span data-ttu-id="f64cd-504">**Element**</span><span class="sxs-lookup"><span data-stu-id="f64cd-504">**Member**</span></span>|<span data-ttu-id="f64cd-505">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f64cd-505">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f64cd-506">**DisplayName**-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="f64cd-506">**DisplayName** property</span></span>  <br/> |<span data-ttu-id="f64cd-507">Ruft die angezeigte Zeichenfolge ab.</span><span class="sxs-lookup"><span data-stu-id="f64cd-507">Gets the display string.</span></span>  <br/> |
|<span data-ttu-id="f64cd-508">**Type**-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="f64cd-508">**Type** property</span></span>  <br/> |<span data-ttu-id="f64cd-509">Ruft den Kontaktendpunkttyp ab.</span><span class="sxs-lookup"><span data-stu-id="f64cd-509">Gets the contact endpoint type</span></span>  <br/> |
|<span data-ttu-id="f64cd-510">**Uri**-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="f64cd-510">**Uri** property</span></span>  <br/> |<span data-ttu-id="f64cd-511">Ruft den Kontakt-URI ab.</span><span class="sxs-lookup"><span data-stu-id="f64cd-511">Gets the contact URI.</span></span>  <br/> |
   
### <a name="ilocalestring-interface"></a><span data-ttu-id="f64cd-512">ILocaleString-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="f64cd-512">ILocaleString interface</span></span>
<span data-ttu-id="f64cd-513"><a name="off15_IMIntegration_ImplementRequired_ILocaleString"> </a></span><span class="sxs-lookup"><span data-stu-id="f64cd-513"></span></span>

<span data-ttu-id="f64cd-p157">**ILocaleString** ist eine lokalisierte Zeichenfolgenstruktur, die eine lokalisierte Zeichenfolge und die Gebietsschema-ID der Lokalisierung enthält. Die **ILocaleString**-Schnittstelle wird zum Formatieren der benutzerdefinierten Statuszeichenfolge auf der Visitenkarte verwendet.</span><span class="sxs-lookup"><span data-stu-id="f64cd-p157">The **ILocaleString** is a localized string structure that contains both a localized string and the locale ID of the localization. The **ILocaleString** interface is used to format the custom status string on the contact card.</span></span> 
  
<span data-ttu-id="f64cd-516">In Tabelle 12 werden die Elemente aufgeführt, die in den Klassen implementiert werden müssen, die von **ILocaleString** erben.</span><span class="sxs-lookup"><span data-stu-id="f64cd-516">Table 12 shows the members that must be implemented in the classes that inherit from **ILocaleString**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="f64cd-517">Elemente der **ILocaleString**-Schnittstelle, die nicht in der Tabelle aufgeführt sind, müssen zwar vorhanden sein, jedoch nicht implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="f64cd-517">Any member of the **ILocaleString** interface not listed in the table must be present but does not need to be implemented.</span></span> <span data-ttu-id="f64cd-518">Members, die vorhanden sind, jedoch nicht implementiert werden, können einen **NotImplementedException** oder **E_NOTIMPL**-Fehler zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="f64cd-518">Members that are present but not implemented can throw a **NotImplementedException** or **E_NOTIMPL** error.</span></span>
>
> <span data-ttu-id="f64cd-519">Weitere Informationen zu der **ILocalString**-Schnittstelle und den dazugehörigen Elementen finden Sie unter [UCCollaborationLib.ILocaleString](http://msdn.microsoft.com/library/UCCollaborationLib.ILocaleString).</span><span class="sxs-lookup"><span data-stu-id="f64cd-519">> For more information about the **ILocalString** interface and its members, see [UCCollaborationLib.ILocaleString](http://msdn.microsoft.com/library/UCCollaborationLib.ILocaleString).</span></span> 
  
<span data-ttu-id="f64cd-520">**Tabelle 12. Implementierung der ILocaleString-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="f64cd-520">**Table 12. Implementation of the ILocaleString interface**</span></span>

|<span data-ttu-id="f64cd-521">**Element**</span><span class="sxs-lookup"><span data-stu-id="f64cd-521">**Member**</span></span>|<span data-ttu-id="f64cd-522">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f64cd-522">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f64cd-523">**LocaleId**-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="f64cd-523">**LocaleId** property</span></span>  <br/> |<span data-ttu-id="f64cd-524">Ruft die Gebietsschema-ID ab.</span><span class="sxs-lookup"><span data-stu-id="f64cd-524">Gets the locale ID.</span></span>  <br/> |
|<span data-ttu-id="f64cd-525">**Value**-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="f64cd-525">**Value** property</span></span>  <br/> |<span data-ttu-id="f64cd-526">Ruft die Zeichenfolge ab.</span><span class="sxs-lookup"><span data-stu-id="f64cd-526">Gets the string.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f64cd-527">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f64cd-527">See also</span></span>

- <span data-ttu-id="f64cd-528">[UCCollaborationLib](http://msdn.microsoft.com/library/UCCollaborationLib)-Namespace</span><span class="sxs-lookup"><span data-stu-id="f64cd-528">[UCCollaborationLib](http://msdn.microsoft.com/library/UCCollaborationLib) namespace</span></span> 
    

