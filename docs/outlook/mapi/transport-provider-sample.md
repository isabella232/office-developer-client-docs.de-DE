---
title: Beispiel für einen Transportanbieter
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ec6eb6c0-bfe3-4989-9071-89a14c0e7bdd
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 3b3ae4170cab109ae96a51eae6e70c674895eeae
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575784"
---
# <a name="transport-provider-sample"></a><span data-ttu-id="e7b4e-103">Beispiel für einen Transportanbieter</span><span class="sxs-lookup"><span data-stu-id="e7b4e-103">Transport Provider Sample</span></span>

  
  
<span data-ttu-id="e7b4e-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e7b4e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e7b4e-105">In diesem Beispiel werden Dateien und Verzeichnisse senden und Empfangen von Nachrichten verwendet.</span><span class="sxs-lookup"><span data-stu-id="e7b4e-105">This sample uses files and directories to transmit and receive messages.</span></span> <span data-ttu-id="e7b4e-106">Es implementiert und einen sehr einfachen Präprozessor, der eine Textzeile auf jede ausgehende Nachricht anfügt registriert.</span><span class="sxs-lookup"><span data-stu-id="e7b4e-106">It implements and registers a very simple preprocessor that appends a line of text to each outbound message.</span></span> <span data-ttu-id="e7b4e-107">Im Beispiel veranschaulicht, wie Nachrichteninhalt zwischen Transport Neutral Encapsulation Format (TNEF) und Text teilen.</span><span class="sxs-lookup"><span data-stu-id="e7b4e-107">The sample illustrates how to split message content between Transport Neutral Encapsulation Format (TNEF) and text.</span></span> <span data-ttu-id="e7b4e-108">Außerdem werden alle Konfigurationsoptionen (Eigenschaftenseiten, Assistenten und programmgesteuerte Konfiguration) und Nachrichtenoptionen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e7b4e-108">It also supports all configuration options (property sheets, wizards, and programmatic configuration) and message options.</span></span> <span data-ttu-id="e7b4e-109">Es wird nicht die remote-Transport-Schnittstellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e7b4e-109">It does not support the remote transport interfaces.</span></span> 
  
<span data-ttu-id="e7b4e-110">Sie können dieses Beispiel aus [Outlook Messaging-API (MAPI)-Codebeispiele](http://go.microsoft.com/fwlink/?LinkId=129740)herunterladen.</span><span class="sxs-lookup"><span data-stu-id="e7b4e-110">You can download this sample from [Outlook Messaging API (MAPI) Code Samples](http://go.microsoft.com/fwlink/?LinkId=129740).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e7b4e-111">Ausführbare Datei:</span><span class="sxs-lookup"><span data-stu-id="e7b4e-111">Executable:</span></span>  <br/> |<span data-ttu-id="e7b4e-112">mrxp32.dll</span><span class="sxs-lookup"><span data-stu-id="e7b4e-112">mrxp32.dll</span></span>  <br/> |
|<span data-ttu-id="e7b4e-113">Code Quellverzeichnis:</span><span class="sxs-lookup"><span data-stu-id="e7b4e-113">Source code directory:</span></span>  <br/> |<span data-ttu-id="e7b4e-114">SampleTransportProvider\MRXP</span><span class="sxs-lookup"><span data-stu-id="e7b4e-114">SampleTransportProvider\MRXP</span></span>  <br/> |
|<span data-ttu-id="e7b4e-115">Sprache:</span><span class="sxs-lookup"><span data-stu-id="e7b4e-115">Language:</span></span>  <br/> |<span data-ttu-id="e7b4e-116">C++</span><span class="sxs-lookup"><span data-stu-id="e7b4e-116">C++</span></span>  <br/> |
|<span data-ttu-id="e7b4e-117">Plattformen:</span><span class="sxs-lookup"><span data-stu-id="e7b4e-117">Platforms:</span></span>  <br/> |<span data-ttu-id="e7b4e-118">Visual Studio 2008 zum Kompilieren für Windows Vista, Windows Server 2008, Windows XP SP2 und Windows Server 2003 SP1</span><span class="sxs-lookup"><span data-stu-id="e7b4e-118">Visual Studio 2008 to compile for Windows Vista, Windows Server 2008, Windows XP SP2, and Windows Server 2003 SP1</span></span>  <br/> |
   
## <a name="supported-features"></a><span data-ttu-id="e7b4e-119">Unterstützte Features</span><span class="sxs-lookup"><span data-stu-id="e7b4e-119">Supported Features</span></span>

<span data-ttu-id="e7b4e-120">In diesem Beispiel werden die folgenden Features unterstützt:</span><span class="sxs-lookup"><span data-stu-id="e7b4e-120">This sample supports the following features:</span></span>
  
- <span data-ttu-id="e7b4e-121">Grundlegende Features wie senden, empfangen und neue Nachrichten abrufen.</span><span class="sxs-lookup"><span data-stu-id="e7b4e-121">Basic features such as sending, receiving, and polling for new messages.</span></span>
    
- <span data-ttu-id="e7b4e-122">Interaktive und programmgesteuerte Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="e7b4e-122">Interactive and programmatic configuration.</span></span>
    
- <span data-ttu-id="e7b4e-123">Die **IMAPIStatus** -Schnittstelle, mit Ausnahme der Einstellung-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="e7b4e-123">The **IMAPIStatus** interface, except for property setting.</span></span> <span data-ttu-id="e7b4e-124">Weitere Informationen finden Sie unter der [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md) Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="e7b4e-124">For more information, see the [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) interface.</span></span> 
    
- <span data-ttu-id="e7b4e-125">Threadsicherheit.</span><span class="sxs-lookup"><span data-stu-id="e7b4e-125">Thread safety.</span></span>
    
- <span data-ttu-id="e7b4e-126">Protokollierung in eine Textdatei.</span><span class="sxs-lookup"><span data-stu-id="e7b4e-126">Event logging to a text file.</span></span> <span data-ttu-id="e7b4e-127">Die Datei wird automatisch auf eine bestimmte Größe beschränkt.</span><span class="sxs-lookup"><span data-stu-id="e7b4e-127">The file is automatically limited to a specified size.</span></span> <span data-ttu-id="e7b4e-128">Alle Transport-Sitzungen verwenden dieselbe Datei.</span><span class="sxs-lookup"><span data-stu-id="e7b4e-128">All transport sessions use the same file.</span></span>
    
## <a name="unsupported-features"></a><span data-ttu-id="e7b4e-129">Nicht unterstützte Features</span><span class="sxs-lookup"><span data-stu-id="e7b4e-129">Unsupported Features</span></span>

<span data-ttu-id="e7b4e-130">In diesem Beispiel unterstützt keine asynchronen Erkennung von eingehenden Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="e7b4e-130">This sample does not support asynchronous detection of incoming messages.</span></span>
  
 <span data-ttu-id="e7b4e-131">**So installieren Sie den Beispielanbieter Transport**</span><span class="sxs-lookup"><span data-stu-id="e7b4e-131">**To install the Sample Transport Provider**</span></span>
  
1. <span data-ttu-id="e7b4e-132">Zum Herunterladen der Adressbuchhierarchie Beispiel finden Sie unter [Herunterladen der MAPI-Beispiele für Outlook](downloading-the-outlook-mapi-samples.md).</span><span class="sxs-lookup"><span data-stu-id="e7b4e-132">To download the Sample Transport Provider, see [Downloading the Outlook MAPI Samples](downloading-the-outlook-mapi-samples.md).</span></span>
    
2. <span data-ttu-id="e7b4e-133">Suchen Sie den Ordner, in dem Sie die Outlook-MAPI-Beispiele gespeichert haben.</span><span class="sxs-lookup"><span data-stu-id="e7b4e-133">Locate the folder where you saved the Outlook MAPI samples.</span></span> <span data-ttu-id="e7b4e-134">Mit der rechten Maustaste die **OutlookMAPISamples -\<Versionsnummer\> ** zip-Ordner, und klicken Sie auf **Alle extrahieren**.</span><span class="sxs-lookup"><span data-stu-id="e7b4e-134">Right-click the **OutlookMAPISamples-\<version number\>** zip folder and click **Extract All**.</span></span>
    
3. <span data-ttu-id="e7b4e-135">Klicken Sie auf **Durchsuchen**, markieren Sie den Speicherort, in dem Sie das Beispiel zu speichern möchten, und klicken Sie auf **extrahieren**.</span><span class="sxs-lookup"><span data-stu-id="e7b4e-135">Click **Browse**, select the location where you want to save the sample, and click **Extract**.</span></span>
    
4. <span data-ttu-id="e7b4e-136">Führen Sie Visual Studio 2008.</span><span class="sxs-lookup"><span data-stu-id="e7b4e-136">Run Visual Studio 2008.</span></span>
    
5. <span data-ttu-id="e7b4e-137">Klicken Sie in Visual Studio 2008 auf **Datei**, klicken Sie auf **Öffnen**, und klicken Sie dann auf **Projekt/Projektmappe**.</span><span class="sxs-lookup"><span data-stu-id="e7b4e-137">In Visual Studio 2008, click **File**, select **Open**, and then click **Project/Solution**.</span></span>
    
6. <span data-ttu-id="e7b4e-138">Navigieren Sie zum Speicherort, in dem Sie das Beispiel gespeichert haben, klicken Sie auf **mrxp32.vcproj**und klicken Sie dann auf **Öffnen**.</span><span class="sxs-lookup"><span data-stu-id="e7b4e-138">Browse to the location where you saved the sample, click **mrxp32.vcproj**, and then click **Open**.</span></span>
    
7. <span data-ttu-id="e7b4e-139">Klicken Sie im Menü **Erstellen** auf **Konfigurations-Manager**.</span><span class="sxs-lookup"><span data-stu-id="e7b4e-139">On the **Build** menu, click **Configuration Manager**.</span></span>
    
8. <span data-ttu-id="e7b4e-140">Klicken Sie im Dialogfeld **Konfigurations-Manager** wechseln Sie in der Zeile **mrxp32** in der Spalte **Konfiguration** wählen Sie **Release aus**und klicken Sie dann auf **Schließen**.</span><span class="sxs-lookup"><span data-stu-id="e7b4e-140">In the **Configuration Manager** dialog box, go to the **mrxp32** row, and in the **Configuration** column select **Release**, and then click **Close**.</span></span>
    
9. <span data-ttu-id="e7b4e-141">On the **Build** menu, click **Build Solution**.</span><span class="sxs-lookup"><span data-stu-id="e7b4e-141">On the **Build** menu, click **Build Solution**.</span></span>
    
10. <span data-ttu-id="e7b4e-142">Klicken Sie im Dialogfeld **Datei speichern unter** auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="e7b4e-142">In the **Save File As** dialog box, click **Save**.</span></span>
    
11. <span data-ttu-id="e7b4e-143">In den Ordner, in dem Sie das Beispiel gespeichert haben, mit der rechten Maustaste der Installations-Batchdatei, und klicken Sie auf **als Administrator ausführen**.</span><span class="sxs-lookup"><span data-stu-id="e7b4e-143">In the folder where you saved the sample, right-click the installation batch file and click **Run as administrator**.</span></span>
    
12. <span data-ttu-id="e7b4e-144">Klicken Sie im Dialogfeld **Benutzerkontensteuerung** auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="e7b4e-144">In the **User Account Control** dialog box, click **Continue**.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="e7b4e-145">**Install.bat** kopiert die DLL-Datei in den standardmäßigen Microsoft Office-Installationsordner C:\Program Files\Microsoft Office\Office12\.</span><span class="sxs-lookup"><span data-stu-id="e7b4e-145">**install.bat** copies the .dll to the default Microsoft Office installation folder, C:\Program Files\Microsoft Office\Office12\.</span></span> <span data-ttu-id="e7b4e-146">Wenn Sie Office-Produkte an einem anderen Speicherort installiert haben, mit der rechten Maustaste **Install.bat aus** , und klicken Sie auf **Bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="e7b4e-146">If you have installed Office products in a different location, right-click **install.bat** and click **Edit**.</span></span> <span data-ttu-id="e7b4e-147">Die Datei wird im Editor geöffnet.</span><span class="sxs-lookup"><span data-stu-id="e7b4e-147">The file opens in Notepad.</span></span> <span data-ttu-id="e7b4e-148">Ersetzen Sie den Standardpfad für die Installation durch den Installationspfad auf Ihrem Computer verwendet.</span><span class="sxs-lookup"><span data-stu-id="e7b4e-148">Replace the default installation path with the installation path used on your computer.</span></span> 
  
 <span data-ttu-id="e7b4e-149">**Einrichten der Adressbuchhierarchie in Outlook**</span><span class="sxs-lookup"><span data-stu-id="e7b4e-149">**To set up the Transport Provider in Outlook**</span></span>
  
1. <span data-ttu-id="e7b4e-150">Klicken Sie auf von Outlook im Menü **Extras** auf **Konten-Einstellungen**.</span><span class="sxs-lookup"><span data-stu-id="e7b4e-150">On the **Tools** menu of Outlook, click **Account Settings**.</span></span>
    
2. <span data-ttu-id="e7b4e-151">Klicken Sie im Dialogfeld **Kontoeinstellungen** auf der Registerkarte **E-Mail** auf **neu**.</span><span class="sxs-lookup"><span data-stu-id="e7b4e-151">In the **Account Settings** dialog box, on the **Email** tab, click **New**.</span></span>
    
3. <span data-ttu-id="e7b4e-152">Klicken Sie unter **E-Mail-Dienst auswählen** auf **andere**, wählen Sie **MRXP Beispiel Transport aus**, und klicken Sie dann auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="e7b4e-152">Under **Choose Email Service** click **Other**, select **MRXP Sample Transport**, and then click **Next**.</span></span>
    
4. <span data-ttu-id="e7b4e-153">Geben Sie im Dialogfeld **MRXP Transportkonfiguration** einen **Anzeigenamen des Benutzers ein**.</span><span class="sxs-lookup"><span data-stu-id="e7b4e-153">In the **MRXP Transport Configuration** dialog box type a **User Display Name**.</span></span>
    
5. <span data-ttu-id="e7b4e-154">Geben Sie unter **Pfad zur Posteingang (UNC-Freigabe)** einen Ordnerpfad aus.</span><span class="sxs-lookup"><span data-stu-id="e7b4e-154">Under **Path to Inbox (UNC Share)** enter a folder path.</span></span> <span data-ttu-id="e7b4e-155">Dies kann auch ein Pfad zu einem lokalen Ordner sein.</span><span class="sxs-lookup"><span data-stu-id="e7b4e-155">This can also be a path to a local folder.</span></span> 
    
    > [!IMPORTANT]
    > <span data-ttu-id="e7b4e-156">In diesem Pfad muss vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="e7b4e-156">This path must exist.</span></span> 
  
6. <span data-ttu-id="e7b4e-157">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="e7b4e-157">Click **OK**.</span></span>
    
7. <span data-ttu-id="e7b4e-158">Klicken Sie im Dialogfeld **E-Mail-Konto hinzufügen** auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="e7b4e-158">In the **Add Email Account** dialog box click **OK**.</span></span> <span data-ttu-id="e7b4e-159">Klicken Sie auf **Fertig stellen** , und klicken Sie dann auf **Schließen**.</span><span class="sxs-lookup"><span data-stu-id="e7b4e-159">Click **Finish** and then click **Close**.</span></span>
    
8. <span data-ttu-id="e7b4e-160">Um mit dem Konto MRXP zu starten, beenden und starten Sie Outlook neu.</span><span class="sxs-lookup"><span data-stu-id="e7b4e-160">To start using the MRXP account, exit and restart Outlook.</span></span>
    
 <span data-ttu-id="e7b4e-161">**So verwenden Sie Sample Anbieter Transport zum Senden einer Nachricht in Outlook**</span><span class="sxs-lookup"><span data-stu-id="e7b4e-161">**To use the Transport Provider Sample to send a message in Outlook**</span></span>
  
1. <span data-ttu-id="e7b4e-162">Klicken Sie im Menü **Datei** auf **neu**und klicken Sie dann auf **E-Mail-Nachricht**.</span><span class="sxs-lookup"><span data-stu-id="e7b4e-162">On the **File** menu, click **New**, and then click **Mail Message**.</span></span>
    
2. <span data-ttu-id="e7b4e-163">Geben Sie in das Feld **an** den Namen des Empfängers mit dem Format **[MRXP:\<Adresse\>]**.</span><span class="sxs-lookup"><span data-stu-id="e7b4e-163">In the **To** box type the name of the recipient using the format **[MRXP:\<ADDRESS\>]**.</span></span> <span data-ttu-id="e7b4e-164">Die Adresse ist der UNC-Freigabe oder lokalen Ordnerpfad an den Posteingang des Empfängers.</span><span class="sxs-lookup"><span data-stu-id="e7b4e-164">The address is the UNC share or local folder path to the recipient's inbox.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="e7b4e-165">Doppelpunkte oder umgekehrte Schrägstriche in der Adresse vorhanden sind, müssen Sie einen umgekehrten Schrägstrich vor jeder Doppelpunkt oder umgekehrten Schrägstrich einfügen.</span><span class="sxs-lookup"><span data-stu-id="e7b4e-165">If there are colons or backslashes in the address, you must insert a backslash before each colon or backslash.</span></span> <span data-ttu-id="e7b4e-166">Beispielsweise zum Senden von e-Mails an [MRXP:C:\Mail\myDir] Geben Sie `[MRXP:C\:\\Mail\\myDir]`.</span><span class="sxs-lookup"><span data-stu-id="e7b4e-166">For example, to send mail to [MRXP:C:\Mail\myDir] you must type  `[MRXP:C\:\\Mail\\myDir]`.</span></span> 
  
    > [!IMPORTANT]
    > <span data-ttu-id="e7b4e-167">Die Adresse des Empfängers muss vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="e7b4e-167">The recipient address must exist.</span></span> 
  
3. <span data-ttu-id="e7b4e-168">Klicken Sie auf **Konto** , und klicken Sie dann auf **MRXP Beispiel Transport**.</span><span class="sxs-lookup"><span data-stu-id="e7b4e-168">Click **Account** and then click **MRXP Sample Transport**.</span></span>
    
4. <span data-ttu-id="e7b4e-169">Geben Sie Ihre Nachricht ein, und klicken Sie auf **Senden**.</span><span class="sxs-lookup"><span data-stu-id="e7b4e-169">Type your message and click **Send**.</span></span> <span data-ttu-id="e7b4e-170">Die Nachricht wird mithilfe der Adressbuchhierarchie MRXP gesendet.</span><span class="sxs-lookup"><span data-stu-id="e7b4e-170">The message is sent using the MRXP transport provider.</span></span>
    
 <span data-ttu-id="e7b4e-171">**Zum Verwenden des Transport-Anbieter-Beispiels zum Empfangen einer Nachricht in Outlook**</span><span class="sxs-lookup"><span data-stu-id="e7b4e-171">**To use the Transport Provider Sample to receive a message in Outlook**</span></span>
  
1. <span data-ttu-id="e7b4e-172">Klicken Sie im Menü **Datei** auf **neu**und klicken Sie dann auf **E-Mail-Nachricht**.</span><span class="sxs-lookup"><span data-stu-id="e7b4e-172">On the **File** menu, click **New**, and then click **Mail Message**.</span></span>
    
2. <span data-ttu-id="e7b4e-173">Geben Sie Ihre Nachricht ein.</span><span class="sxs-lookup"><span data-stu-id="e7b4e-173">Type your message.</span></span>
    
3. <span data-ttu-id="e7b4e-174">Klicken Sie auf der **Microsoft Office-Schaltfläche**, klicken Sie auf **Speichern unter**, und klicken Sie dann auf **Speichern unter,** um die Datei in den Posteingangsordner zu speichern, die Sie während der Installation angegeben.</span><span class="sxs-lookup"><span data-stu-id="e7b4e-174">Click the **Microsoft Office Button**, click **Save As**, and then click **Save As** to save the file to the inbox folder you specified during setup.</span></span> 
    
4. <span data-ttu-id="e7b4e-175">Klicken Sie im Dialogfeld **Speichern unter,** wechseln Sie zu den UNC-Freigabe oder einem lokalen Ordner, den im Posteingang festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e7b4e-175">In the **Save As** dialog box, browse to the UNC share or local folder that you set as your inbox.</span></span> 
    
5. <span data-ttu-id="e7b4e-176">Klicken Sie im Dropdown **Dateityp** - **Outlook-Nachrichtenformat**auf.</span><span class="sxs-lookup"><span data-stu-id="e7b4e-176">In the **Save as type** drop down, click **Outlook Message Format**.</span></span>
    
6. <span data-ttu-id="e7b4e-177">Geben Sie einen Namen für die Datei, und klicken Sie auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="e7b4e-177">Type a name for the file and click **Save**.</span></span>
    
7. <span data-ttu-id="e7b4e-178">Die Datei wird in den freigegebenen Ordner gespeichert.</span><span class="sxs-lookup"><span data-stu-id="e7b4e-178">The file is saved to the shared folder.</span></span> <span data-ttu-id="e7b4e-179">Der Transportdienst MRXP übermittelt die Nachricht an Ihren Posteingang in Outlook.</span><span class="sxs-lookup"><span data-stu-id="e7b4e-179">The MRXP transport provider delivers the message to your Inbox in Outlook.</span></span>
    

