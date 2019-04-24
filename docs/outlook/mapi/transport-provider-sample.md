---
title: Beispiel für einen Transport Anbieter
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ec6eb6c0-bfe3-4989-9071-89a14c0e7bdd
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: def51a752abcb79a35980ed12eb73011c26d2597
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356588"
---
# <a name="transport-provider-sample"></a><span data-ttu-id="2a6f5-103">Beispiel für einen Transport Anbieter</span><span class="sxs-lookup"><span data-stu-id="2a6f5-103">Transport Provider Sample</span></span>

  
  
<span data-ttu-id="2a6f5-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2a6f5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2a6f5-105">In diesem Beispiel werden Dateien und Verzeichnisse zum Senden und empfangen von Nachrichten verwendet.</span><span class="sxs-lookup"><span data-stu-id="2a6f5-105">This sample uses files and directories to transmit and receive messages.</span></span> <span data-ttu-id="2a6f5-106">Es wird ein sehr einfacher Präprozessor implementiert und registriert, der jeder ausgehenden Nachricht eine Textzeile hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="2a6f5-106">It implements and registers a very simple preprocessor that appends a line of text to each outbound message.</span></span> <span data-ttu-id="2a6f5-107">Im Beispiel wird veranschaulicht, wie der Nachrichteninhalt zwischen dem Transport Neutral Encapsulation Format (TNEF) und dem Text geteilt wird.</span><span class="sxs-lookup"><span data-stu-id="2a6f5-107">The sample illustrates how to split message content between Transport Neutral Encapsulation Format (TNEF) and text.</span></span> <span data-ttu-id="2a6f5-108">Außerdem werden alle Konfigurationsoptionen (Eigenschaftenblätter, Assistenten und programmgesteuerte Konfiguration) und Nachrichtenoptionen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2a6f5-108">It also supports all configuration options (property sheets, wizards, and programmatic configuration) and message options.</span></span> <span data-ttu-id="2a6f5-109">Die Remote Transport Schnittstellen werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2a6f5-109">It does not support the remote transport interfaces.</span></span> 
  
<span data-ttu-id="2a6f5-110">Sie können dieses Beispiel aus [MAPI-Code Beispielen (Outlook Messaging API)](https://go.microsoft.com/fwlink/?LinkId=129740)herunterladen.</span><span class="sxs-lookup"><span data-stu-id="2a6f5-110">You can download this sample from [Outlook Messaging API (MAPI) Code Samples](https://go.microsoft.com/fwlink/?LinkId=129740).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2a6f5-111">Executable</span><span class="sxs-lookup"><span data-stu-id="2a6f5-111">Executable:</span></span>  <br/> |<span data-ttu-id="2a6f5-112">mrxp32. dll</span><span class="sxs-lookup"><span data-stu-id="2a6f5-112">mrxp32.dll</span></span>  <br/> |
|<span data-ttu-id="2a6f5-113">Quellcodeverzeichnis:</span><span class="sxs-lookup"><span data-stu-id="2a6f5-113">Source code directory:</span></span>  <br/> |<span data-ttu-id="2a6f5-114">SampleTransportProvider\MRXP</span><span class="sxs-lookup"><span data-stu-id="2a6f5-114">SampleTransportProvider\MRXP</span></span>  <br/> |
|<span data-ttu-id="2a6f5-115">Sprache</span><span class="sxs-lookup"><span data-stu-id="2a6f5-115">Language:</span></span>  <br/> |<span data-ttu-id="2a6f5-116">C++</span><span class="sxs-lookup"><span data-stu-id="2a6f5-116">C++</span></span>  <br/> |
|<span data-ttu-id="2a6f5-117">Plattformen</span><span class="sxs-lookup"><span data-stu-id="2a6f5-117">Platforms:</span></span>  <br/> |<span data-ttu-id="2a6f5-118">Visual Studio 2008 für die Kompilierung für Windows Vista, Windows Server 2008, Windows XP SP2 und Windows Server 2003 SP1</span><span class="sxs-lookup"><span data-stu-id="2a6f5-118">Visual Studio 2008 to compile for Windows Vista, Windows Server 2008, Windows XP SP2, and Windows Server 2003 SP1</span></span>  <br/> |
   
## <a name="supported-features"></a><span data-ttu-id="2a6f5-119">Unterstützte Features</span><span class="sxs-lookup"><span data-stu-id="2a6f5-119">Supported Features</span></span>

<span data-ttu-id="2a6f5-120">In diesem Beispiel werden die folgenden Features unterstützt:</span><span class="sxs-lookup"><span data-stu-id="2a6f5-120">This sample supports the following features:</span></span>
  
- <span data-ttu-id="2a6f5-121">Grundlegende Features wie senden, empfangen und Abrufen von neuen Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="2a6f5-121">Basic features such as sending, receiving, and polling for new messages.</span></span>
    
- <span data-ttu-id="2a6f5-122">Interaktive und programmgesteuerte Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="2a6f5-122">Interactive and programmatic configuration.</span></span>
    
- <span data-ttu-id="2a6f5-123">Die **IMAPIStatus** -Schnittstelle, mit Ausnahme der Eigenschaftseinstellung.</span><span class="sxs-lookup"><span data-stu-id="2a6f5-123">The **IMAPIStatus** interface, except for property setting.</span></span> <span data-ttu-id="2a6f5-124">Weitere Informationen finden Sie unter der [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="2a6f5-124">For more information, see the [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) interface.</span></span> 
    
- <span data-ttu-id="2a6f5-125">Thread Sicherheit.</span><span class="sxs-lookup"><span data-stu-id="2a6f5-125">Thread safety.</span></span>
    
- <span data-ttu-id="2a6f5-126">Ereignisprotokollierung in eine Textdatei.</span><span class="sxs-lookup"><span data-stu-id="2a6f5-126">Event logging to a text file.</span></span> <span data-ttu-id="2a6f5-127">Die Datei wird automatisch auf eine bestimmte Größe beschränkt.</span><span class="sxs-lookup"><span data-stu-id="2a6f5-127">The file is automatically limited to a specified size.</span></span> <span data-ttu-id="2a6f5-128">Alle Transportsitzungen verwenden dieselbe Datei.</span><span class="sxs-lookup"><span data-stu-id="2a6f5-128">All transport sessions use the same file.</span></span>
    
## <a name="unsupported-features"></a><span data-ttu-id="2a6f5-129">Nicht unterstützte Features</span><span class="sxs-lookup"><span data-stu-id="2a6f5-129">Unsupported Features</span></span>

<span data-ttu-id="2a6f5-130">In diesem Beispiel wird die asynchrone Erkennung eingehender Nachrichten nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2a6f5-130">This sample does not support asynchronous detection of incoming messages.</span></span>
  
 <span data-ttu-id="2a6f5-131">**So installieren Sie den Beispiel Transport Anbieter**</span><span class="sxs-lookup"><span data-stu-id="2a6f5-131">**To install the Sample Transport Provider**</span></span>
  
1. <span data-ttu-id="2a6f5-132">Informationen zum Herunterladen des Beispiel Transport Anbieters finden Sie unter [herunterladen der Outlook-MAPI-Beispiele](downloading-the-outlook-mapi-samples.md).</span><span class="sxs-lookup"><span data-stu-id="2a6f5-132">To download the Sample Transport Provider, see [Downloading the Outlook MAPI Samples](downloading-the-outlook-mapi-samples.md).</span></span>
    
2. <span data-ttu-id="2a6f5-133">Suchen Sie den Ordner, in dem Sie die Outlook-MAPI-Beispiele gespeichert haben.</span><span class="sxs-lookup"><span data-stu-id="2a6f5-133">Locate the folder where you saved the Outlook MAPI samples.</span></span> <span data-ttu-id="2a6f5-134">Klicken Sie mit der rechten Maustaste auf den Zip **-Ordner OutlookMAPISamples-\<Versions\> Nummer** , und klicken Sie auf **Alle extrahieren**.</span><span class="sxs-lookup"><span data-stu-id="2a6f5-134">Right-click the **OutlookMAPISamples-\<version number\>** zip folder and click **Extract All**.</span></span>
    
3. <span data-ttu-id="2a6f5-135">Klicken Sie auf **Durchsuchen**, wählen Sie den Speicherort aus, an dem Sie das Beispiel speichern möchten, und klicken Sie auf **extrahieren**.</span><span class="sxs-lookup"><span data-stu-id="2a6f5-135">Click **Browse**, select the location where you want to save the sample, and click **Extract**.</span></span>
    
4. <span data-ttu-id="2a6f5-136">Führen Sie Visual Studio 2008 aus.</span><span class="sxs-lookup"><span data-stu-id="2a6f5-136">Run Visual Studio 2008.</span></span>
    
5. <span data-ttu-id="2a6f5-137">Klicken Sie in Visual Studio 2008 auf **Datei**, wählen Sie **Öffnen**aus, und klicken Sie dann auf **Projekt/Lösung**.</span><span class="sxs-lookup"><span data-stu-id="2a6f5-137">In Visual Studio 2008, click **File**, select **Open**, and then click **Project/Solution**.</span></span>
    
6. <span data-ttu-id="2a6f5-138">Navigieren Sie zu dem Speicherort, an dem Sie das Beispiel gespeichert haben, klicken Sie auf **mrxp32. vcproj**, und klicken Sie dann auf **Öffnen**.</span><span class="sxs-lookup"><span data-stu-id="2a6f5-138">Browse to the location where you saved the sample, click **mrxp32.vcproj**, and then click **Open**.</span></span>
    
7. <span data-ttu-id="2a6f5-139">Klicken Sie im Menü **Erstellen** auf **Konfigurations-Manager**.</span><span class="sxs-lookup"><span data-stu-id="2a6f5-139">On the **Build** menu, click **Configuration Manager**.</span></span>
    
8. <span data-ttu-id="2a6f5-140">Wechseln Sie im Dialogfeld **Konfigurations-Manager** zur Zeile **mrxp32** , und wählen Sie in der Spalte **Konfiguration** die Option **Release**aus, und klicken Sie dann auf **Schließen**.</span><span class="sxs-lookup"><span data-stu-id="2a6f5-140">In the **Configuration Manager** dialog box, go to the **mrxp32** row, and in the **Configuration** column select **Release**, and then click **Close**.</span></span>
    
9. <span data-ttu-id="2a6f5-141">On the **Build** menu, click **Build Solution**.</span><span class="sxs-lookup"><span data-stu-id="2a6f5-141">On the **Build** menu, click **Build Solution**.</span></span>
    
10. <span data-ttu-id="2a6f5-142">Klicken Sie im Dialogfeld **Datei speichern** unter auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="2a6f5-142">In the **Save File As** dialog box, click **Save**.</span></span>
    
11. <span data-ttu-id="2a6f5-143">Klicken Sie in dem Ordner, in dem Sie das Beispiel gespeichert haben, mit der rechten Maustaste auf die Installationsbatchdatei, und klicken Sie dann auf **als Administrator ausführen**.</span><span class="sxs-lookup"><span data-stu-id="2a6f5-143">In the folder where you saved the sample, right-click the installation batch file and click **Run as administrator**.</span></span>
    
12. <span data-ttu-id="2a6f5-144">Klicken Sie im Dialogfeld **Benutzerkontensteuerung** auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="2a6f5-144">In the **User Account Control** dialog box, click **Continue**.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="2a6f5-145">**install. bat** kopiert die dll in den standardMäßigen Microsoft Office-Installationsordner, c:\Programme\Microsoft Office\Office12\.</span><span class="sxs-lookup"><span data-stu-id="2a6f5-145">**install.bat** copies the .dll to the default Microsoft Office installation folder, C:\Program Files\Microsoft Office\Office12\.</span></span> <span data-ttu-id="2a6f5-146">Wenn Sie Office-Produkte an einem anderen Speicherort installiert haben, klicken Sie mit der rechten Maustaste auf **install. bat** , und klicken Sie auf **Bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="2a6f5-146">If you have installed Office products in a different location, right-click **install.bat** and click **Edit**.</span></span> <span data-ttu-id="2a6f5-147">Die Datei wird im Editor geöffnet.</span><span class="sxs-lookup"><span data-stu-id="2a6f5-147">The file opens in Notepad.</span></span> <span data-ttu-id="2a6f5-148">Ersetzen Sie den Standardinstallationspfad durch den Installationspfad, der auf Ihrem Computer verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="2a6f5-148">Replace the default installation path with the installation path used on your computer.</span></span> 
  
 <span data-ttu-id="2a6f5-149">**So richten Sie den Transport Anbieter in Outlook ein**</span><span class="sxs-lookup"><span data-stu-id="2a6f5-149">**To set up the Transport Provider in Outlook**</span></span>
  
1. <span data-ttu-id="2a6f5-150">Klicken Sie im Menü **Extras** von Outlook auf **Kontoeinstellungen**.</span><span class="sxs-lookup"><span data-stu-id="2a6f5-150">On the **Tools** menu of Outlook, click **Account Settings**.</span></span>
    
2. <span data-ttu-id="2a6f5-151">Klicken Sie im Dialogfeld **Kontoeinstellungen** auf der Registerkarte **e-Mail** auf **neu**.</span><span class="sxs-lookup"><span data-stu-id="2a6f5-151">In the **Account Settings** dialog box, on the **Email** tab, click **New**.</span></span>
    
3. <span data-ttu-id="2a6f5-152">Klicken Sie unter **e-Mail-Dienst auswählen** auf **Sonstiges**, wählen Sie **MRXP-Beispiel Transport**aus, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="2a6f5-152">Under **Choose Email Service** click **Other**, select **MRXP Sample Transport**, and then click **Next**.</span></span>
    
4. <span data-ttu-id="2a6f5-153">Geben Sie im Dialogfeld **MRXP-Transport Konfiguration** einen **Benutzeranzeigenamen**ein.</span><span class="sxs-lookup"><span data-stu-id="2a6f5-153">In the **MRXP Transport Configuration** dialog box type a **User Display Name**.</span></span>
    
5. <span data-ttu-id="2a6f5-154">Geben Sie unter **Pfad zu Posteingang (UNC-Freigabe)** einen Ordnerpfad ein.</span><span class="sxs-lookup"><span data-stu-id="2a6f5-154">Under **Path to Inbox (UNC Share)** enter a folder path.</span></span> <span data-ttu-id="2a6f5-155">Dabei kann es sich auch um einen Pfad zu einem lokalen Ordner handeln.</span><span class="sxs-lookup"><span data-stu-id="2a6f5-155">This can also be a path to a local folder.</span></span> 
    
    > [!IMPORTANT]
    > <span data-ttu-id="2a6f5-156">Dieser Pfad muss vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="2a6f5-156">This path must exist.</span></span> 
  
6. <span data-ttu-id="2a6f5-157">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="2a6f5-157">Click **OK**.</span></span>
    
7. <span data-ttu-id="2a6f5-158">Klicken Sie im Dialogfeld **e-Mail-Konto hinzufügen** auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="2a6f5-158">In the **Add Email Account** dialog box click **OK**.</span></span> <span data-ttu-id="2a6f5-159">Klicken Sie auf **Fertig stellen** und dann auf **Schließen**.</span><span class="sxs-lookup"><span data-stu-id="2a6f5-159">Click **Finish** and then click **Close**.</span></span>
    
8. <span data-ttu-id="2a6f5-160">Beenden Sie Outlook, und starten Sie es neu, um das MRXP-Konto zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="2a6f5-160">To start using the MRXP account, exit and restart Outlook.</span></span>
    
 <span data-ttu-id="2a6f5-161">**So verwenden Sie das Transport Anbieterbeispiel zum Senden einer Nachricht in Outlook**</span><span class="sxs-lookup"><span data-stu-id="2a6f5-161">**To use the Transport Provider Sample to send a message in Outlook**</span></span>
  
1. <span data-ttu-id="2a6f5-162">Klicken Sie im Menü **Datei** auf **neu**, und klicken Sie dann auf **e-Mail-Nachricht**.</span><span class="sxs-lookup"><span data-stu-id="2a6f5-162">On the **File** menu, click **New**, and then click **Mail Message**.</span></span>
    
2. <span data-ttu-id="2a6f5-163">Geben Sie im Feld **an** den Namen des Empfängers mit dem Format **[MRXP:\<Address\>]** ein.</span><span class="sxs-lookup"><span data-stu-id="2a6f5-163">In the **To** box type the name of the recipient using the format **[MRXP:\<ADDRESS\>]**.</span></span> <span data-ttu-id="2a6f5-164">Die Adresse ist die UNC-Freigabe oder der lokale Ordnerpfad zum Posteingang des Empfängers.</span><span class="sxs-lookup"><span data-stu-id="2a6f5-164">The address is the UNC share or local folder path to the recipient's inbox.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="2a6f5-165">Wenn die Adresse Doppelpunkte oder umgekehrte Schrägstriche enthält, müssen Sie vor jedem Doppelpunkt oder Backslash einen umgekehrten Schrägstrich einfügen.</span><span class="sxs-lookup"><span data-stu-id="2a6f5-165">If there are colons or backslashes in the address, you must insert a backslash before each colon or backslash.</span></span> <span data-ttu-id="2a6f5-166">Wenn Sie beispielsweise eine e-Mail an [MRXP: C: \Mail\myDir] senden möchten, `[MRXP:C\:\\Mail\\myDir]`müssen Sie Folgendes eingeben.</span><span class="sxs-lookup"><span data-stu-id="2a6f5-166">For example, to send mail to [MRXP:C:\Mail\myDir] you must type  `[MRXP:C\:\\Mail\\myDir]`.</span></span> 
  
    > [!IMPORTANT]
    > <span data-ttu-id="2a6f5-167">Die Empfängeradresse muss vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="2a6f5-167">The recipient address must exist.</span></span> 
  
3. <span data-ttu-id="2a6f5-168">Klicken Sie auf **Konto** , und klicken Sie dann auf **MRXP-Beispiel Transport**.</span><span class="sxs-lookup"><span data-stu-id="2a6f5-168">Click **Account** and then click **MRXP Sample Transport**.</span></span>
    
4. <span data-ttu-id="2a6f5-169">Geben Sie Ihre Nachricht ein, und klicken Sie auf **senden**.</span><span class="sxs-lookup"><span data-stu-id="2a6f5-169">Type your message and click **Send**.</span></span> <span data-ttu-id="2a6f5-170">Die Nachricht wird mit dem MRXP-Transportanbieter gesendet.</span><span class="sxs-lookup"><span data-stu-id="2a6f5-170">The message is sent using the MRXP transport provider.</span></span>
    
 <span data-ttu-id="2a6f5-171">**So verwenden Sie das Transport Anbieterbeispiel zum Empfangen einer Nachricht in Outlook**</span><span class="sxs-lookup"><span data-stu-id="2a6f5-171">**To use the Transport Provider Sample to receive a message in Outlook**</span></span>
  
1. <span data-ttu-id="2a6f5-172">Klicken Sie im Menü **Datei** auf **neu**, und klicken Sie dann auf **e-Mail-Nachricht**.</span><span class="sxs-lookup"><span data-stu-id="2a6f5-172">On the **File** menu, click **New**, and then click **Mail Message**.</span></span>
    
2. <span data-ttu-id="2a6f5-173">Geben Sie Ihre Nachricht ein.</span><span class="sxs-lookup"><span data-stu-id="2a6f5-173">Type your message.</span></span>
    
3. <span data-ttu-id="2a6f5-174">Klicken Sie auf die **Microsoft Office-Schaltfläche**, klicken Sie auf **Speichern**unter, und klicken Sie dann auf **Speichern** unter, um die Datei im Posteingang-Ordner zu speichern, den Sie während der Installation angegeben haben</span><span class="sxs-lookup"><span data-stu-id="2a6f5-174">Click the **Microsoft Office Button**, click **Save As**, and then click **Save As** to save the file to the inbox folder you specified during setup.</span></span> 
    
4. <span data-ttu-id="2a6f5-175">Navigieren Sie im Dialogfeld **Speichern** unter zu der UNC-Freigabe oder dem lokalen Ordner, den Sie als Posteingang festgelegt haben.</span><span class="sxs-lookup"><span data-stu-id="2a6f5-175">In the **Save As** dialog box, browse to the UNC share or local folder that you set as your inbox.</span></span> 
    
5. <span data-ttu-id="2a6f5-176">Klicken Sie \*\*\*\* im Dropdownmenü Dateityp auf Outlook- **Nachrichten Format**.</span><span class="sxs-lookup"><span data-stu-id="2a6f5-176">In the **Save as type** drop down, click **Outlook Message Format**.</span></span>
    
6. <span data-ttu-id="2a6f5-177">Geben Sie einen Namen für die Datei ein, und klicken Sie auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="2a6f5-177">Type a name for the file and click **Save**.</span></span>
    
7. <span data-ttu-id="2a6f5-178">Die Datei wird im freigegebenen Ordner gespeichert.</span><span class="sxs-lookup"><span data-stu-id="2a6f5-178">The file is saved to the shared folder.</span></span> <span data-ttu-id="2a6f5-179">Der MRXP-Transportanbieter übermittelt die Nachricht in Outlook an Ihren Posteingang.</span><span class="sxs-lookup"><span data-stu-id="2a6f5-179">The MRXP transport provider delivers the message to your Inbox in Outlook.</span></span>
    

