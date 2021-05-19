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
ms.openlocfilehash: def51a752abcb79a35980ed12eb73011c26d2597
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356588"
---
# <a name="transport-provider-sample"></a><span data-ttu-id="f2837-103">Beispiel für einen Transportanbieter</span><span class="sxs-lookup"><span data-stu-id="f2837-103">Transport Provider Sample</span></span>

  
  
<span data-ttu-id="f2837-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f2837-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f2837-105">In diesem Beispiel werden Dateien und Verzeichnisse zum Übertragen und Empfangen von Nachrichten verwendet.</span><span class="sxs-lookup"><span data-stu-id="f2837-105">This sample uses files and directories to transmit and receive messages.</span></span> <span data-ttu-id="f2837-106">Es implementiert und registriert einen sehr einfachen Präprozessor, der jeder ausgehenden Nachricht eine Textzeile anfügen kann.</span><span class="sxs-lookup"><span data-stu-id="f2837-106">It implements and registers a very simple preprocessor that appends a line of text to each outbound message.</span></span> <span data-ttu-id="f2837-107">Das Beispiel veranschaulicht, wie Nachrichteninhalte zwischen TNEF (Transport Neutral Encapsulation Format) und Text aufgeteilt werden.</span><span class="sxs-lookup"><span data-stu-id="f2837-107">The sample illustrates how to split message content between Transport Neutral Encapsulation Format (TNEF) and text.</span></span> <span data-ttu-id="f2837-108">Außerdem werden alle Konfigurationsoptionen (Eigenschaftenblätter, Assistenten und programmgesteuerte Konfiguration) und Nachrichtenoptionen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f2837-108">It also supports all configuration options (property sheets, wizards, and programmatic configuration) and message options.</span></span> <span data-ttu-id="f2837-109">Die Remote-Transportschnittstellen werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f2837-109">It does not support the remote transport interfaces.</span></span> 
  
<span data-ttu-id="f2837-110">Sie können dieses Beispiel aus Outlook [Messaging-API (MAPI)-Codebeispiele herunterladen.](https://go.microsoft.com/fwlink/?LinkId=129740)</span><span class="sxs-lookup"><span data-stu-id="f2837-110">You can download this sample from [Outlook Messaging API (MAPI) Code Samples](https://go.microsoft.com/fwlink/?LinkId=129740).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f2837-111">Ausführbare Datei:</span><span class="sxs-lookup"><span data-stu-id="f2837-111">Executable:</span></span>  <br/> |<span data-ttu-id="f2837-112">mrxp32.dll</span><span class="sxs-lookup"><span data-stu-id="f2837-112">mrxp32.dll</span></span>  <br/> |
|<span data-ttu-id="f2837-113">Quellcodeverzeichnis:</span><span class="sxs-lookup"><span data-stu-id="f2837-113">Source code directory:</span></span>  <br/> |<span data-ttu-id="f2837-114">SampleTransportProvider\MRXP</span><span class="sxs-lookup"><span data-stu-id="f2837-114">SampleTransportProvider\MRXP</span></span>  <br/> |
|<span data-ttu-id="f2837-115">Sprache:</span><span class="sxs-lookup"><span data-stu-id="f2837-115">Language:</span></span>  <br/> |<span data-ttu-id="f2837-116">C++</span><span class="sxs-lookup"><span data-stu-id="f2837-116">C++</span></span>  <br/> |
|<span data-ttu-id="f2837-117">Plattformen:</span><span class="sxs-lookup"><span data-stu-id="f2837-117">Platforms:</span></span>  <br/> |<span data-ttu-id="f2837-118">Visual Studio 2008 zum Kompilieren für Windows Vista, Windows Server 2008, Windows XP SP2 und Windows Server 2003 SP1</span><span class="sxs-lookup"><span data-stu-id="f2837-118">Visual Studio 2008 to compile for Windows Vista, Windows Server 2008, Windows XP SP2, and Windows Server 2003 SP1</span></span>  <br/> |
   
## <a name="supported-features"></a><span data-ttu-id="f2837-119">Unterstützte Features</span><span class="sxs-lookup"><span data-stu-id="f2837-119">Supported Features</span></span>

<span data-ttu-id="f2837-120">Dieses Beispiel unterstützt die folgenden Features:</span><span class="sxs-lookup"><span data-stu-id="f2837-120">This sample supports the following features:</span></span>
  
- <span data-ttu-id="f2837-121">Grundlegende Features wie das Senden, Empfangen und Abrufen neuer Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="f2837-121">Basic features such as sending, receiving, and polling for new messages.</span></span>
    
- <span data-ttu-id="f2837-122">Interaktive und programmgesteuerte Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="f2837-122">Interactive and programmatic configuration.</span></span>
    
- <span data-ttu-id="f2837-123">Die **IMAPIStatus-Schnittstelle,** mit Ausnahme der Eigenschafteneinstellung.</span><span class="sxs-lookup"><span data-stu-id="f2837-123">The **IMAPIStatus** interface, except for property setting.</span></span> <span data-ttu-id="f2837-124">Weitere Informationen finden Sie unter [IMAPIStatus : IMAPIProp-Schnittstelle.](imapistatusimapiprop.md)</span><span class="sxs-lookup"><span data-stu-id="f2837-124">For more information, see the [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) interface.</span></span> 
    
- <span data-ttu-id="f2837-125">Threadsicherheit.</span><span class="sxs-lookup"><span data-stu-id="f2837-125">Thread safety.</span></span>
    
- <span data-ttu-id="f2837-126">Ereignisprotokollierung bei einer Textdatei.</span><span class="sxs-lookup"><span data-stu-id="f2837-126">Event logging to a text file.</span></span> <span data-ttu-id="f2837-127">Die Datei ist automatisch auf eine angegebene Größe beschränkt.</span><span class="sxs-lookup"><span data-stu-id="f2837-127">The file is automatically limited to a specified size.</span></span> <span data-ttu-id="f2837-128">Alle Transportsitzungen verwenden dieselbe Datei.</span><span class="sxs-lookup"><span data-stu-id="f2837-128">All transport sessions use the same file.</span></span>
    
## <a name="unsupported-features"></a><span data-ttu-id="f2837-129">Nicht unterstützte Features</span><span class="sxs-lookup"><span data-stu-id="f2837-129">Unsupported Features</span></span>

<span data-ttu-id="f2837-130">Dieses Beispiel unterstützt keine asynchrone Erkennung eingehender Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="f2837-130">This sample does not support asynchronous detection of incoming messages.</span></span>
  
 <span data-ttu-id="f2837-131">**So installieren Sie den Beispieltransportanbieter**</span><span class="sxs-lookup"><span data-stu-id="f2837-131">**To install the Sample Transport Provider**</span></span>
  
1. <span data-ttu-id="f2837-132">Informationen zum Herunterladen des Beispieltransportanbieters finden Sie unter [Herunterladen der Outlook MAPI-Beispiele](downloading-the-outlook-mapi-samples.md).</span><span class="sxs-lookup"><span data-stu-id="f2837-132">To download the Sample Transport Provider, see [Downloading the Outlook MAPI Samples](downloading-the-outlook-mapi-samples.md).</span></span>
    
2. <span data-ttu-id="f2837-133">Suchen Sie den Ordner, in dem Sie die Outlook gespeichert haben.</span><span class="sxs-lookup"><span data-stu-id="f2837-133">Locate the folder where you saved the Outlook MAPI samples.</span></span> <span data-ttu-id="f2837-134">Klicken Sie mit der rechten Maustaste auf den **Ordner OutlookMAPISamples- \< version number \>** zip, und klicken Sie auf Alle **extrahieren.**</span><span class="sxs-lookup"><span data-stu-id="f2837-134">Right-click the **OutlookMAPISamples-\<version number\>** zip folder and click **Extract All**.</span></span>
    
3. <span data-ttu-id="f2837-135">Klicken **Sie auf Durchsuchen,** wählen Sie den Speicherort aus, an dem Sie das Beispiel speichern möchten, und klicken Sie auf **Extrahieren**.</span><span class="sxs-lookup"><span data-stu-id="f2837-135">Click **Browse**, select the location where you want to save the sample, and click **Extract**.</span></span>
    
4. <span data-ttu-id="f2837-136">Führen Visual Studio 2008 aus.</span><span class="sxs-lookup"><span data-stu-id="f2837-136">Run Visual Studio 2008.</span></span>
    
5. <span data-ttu-id="f2837-137">Klicken Visual Studio 2008 auf **Datei,** wählen Sie **Öffnen** aus, und klicken Sie **dann auf Project/Lösung**.</span><span class="sxs-lookup"><span data-stu-id="f2837-137">In Visual Studio 2008, click **File**, select **Open**, and then click **Project/Solution**.</span></span>
    
6. <span data-ttu-id="f2837-138">Navigieren Sie zu dem Speicherort, an dem Sie das Beispiel gespeichert haben, klicken Sie **auf mrxp32.vcproj,** und klicken Sie dann auf **Öffnen**.</span><span class="sxs-lookup"><span data-stu-id="f2837-138">Browse to the location where you saved the sample, click **mrxp32.vcproj**, and then click **Open**.</span></span>
    
7. <span data-ttu-id="f2837-139">Klicken Sie **im Menü** Erstellen auf **Configuration Manager**.</span><span class="sxs-lookup"><span data-stu-id="f2837-139">On the **Build** menu, click **Configuration Manager**.</span></span>
    
8. <span data-ttu-id="f2837-140">Wechseln Sie im Dialogfeld **Configuration Manager** zur **Zeile mrxp32,** und wählen Sie in der Spalte **Konfiguration** die Option **Release** aus, und klicken Sie dann auf **Schließen**.</span><span class="sxs-lookup"><span data-stu-id="f2837-140">In the **Configuration Manager** dialog box, go to the **mrxp32** row, and in the **Configuration** column select **Release**, and then click **Close**.</span></span>
    
9. <span data-ttu-id="f2837-141">On the **Build** menu, click **Build Solution**.</span><span class="sxs-lookup"><span data-stu-id="f2837-141">On the **Build** menu, click **Build Solution**.</span></span>
    
10. <span data-ttu-id="f2837-142">Klicken Sie im Dialogfeld Datei speichern **unter** auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="f2837-142">In the **Save File As** dialog box, click **Save**.</span></span>
    
11. <span data-ttu-id="f2837-143">Klicken Sie im Ordner, in dem Sie das Beispiel gespeichert haben, mit der rechten Maustaste auf die Installationsbatchdatei, und klicken Sie **auf Als Administrator ausführen**.</span><span class="sxs-lookup"><span data-stu-id="f2837-143">In the folder where you saved the sample, right-click the installation batch file and click **Run as administrator**.</span></span>
    
12. <span data-ttu-id="f2837-144">Klicken Sie im Dialogfeld **Benutzerkontensteuerung** auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="f2837-144">In the **User Account Control** dialog box, click **Continue**.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="f2837-145">**install.bat** kopiert die .dll in den Standardinstallationsordner Microsoft Office C:\Program Files\Microsoft Office\Office12\.</span><span class="sxs-lookup"><span data-stu-id="f2837-145">**install.bat** copies the .dll to the default Microsoft Office installation folder, C:\Program Files\Microsoft Office\Office12\.</span></span> <span data-ttu-id="f2837-146">Wenn Sie die Office an einem anderen Speicherort installiert haben, klicken Sie mit der rechten Maustaste **aufinstall.bat** und klicken Sie auf **Bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="f2837-146">If you have installed Office products in a different location, right-click **install.bat** and click **Edit**.</span></span> <span data-ttu-id="f2837-147">Die Datei wird in Editor.</span><span class="sxs-lookup"><span data-stu-id="f2837-147">The file opens in Notepad.</span></span> <span data-ttu-id="f2837-148">Ersetzen Sie den Standardinstallationspfad durch den Installationspfad, der auf Ihrem Computer verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f2837-148">Replace the default installation path with the installation path used on your computer.</span></span> 
  
 <span data-ttu-id="f2837-149">**So richten Sie den Transportanbieter in Outlook**</span><span class="sxs-lookup"><span data-stu-id="f2837-149">**To set up the Transport Provider in Outlook**</span></span>
  
1. <span data-ttu-id="f2837-150">Klicken Sie **im** Menü Extras Outlook auf **Konto Einstellungen**.</span><span class="sxs-lookup"><span data-stu-id="f2837-150">On the **Tools** menu of Outlook, click **Account Settings**.</span></span>
    
2. <span data-ttu-id="f2837-151">Klicken Sie **im Einstellungen** Auf **der** Registerkarte E-Mail auf **Neu**.</span><span class="sxs-lookup"><span data-stu-id="f2837-151">In the **Account Settings** dialog box, on the **Email** tab, click **New**.</span></span>
    
3. <span data-ttu-id="f2837-152">Klicken **Sie unter E-Mail-Dienst** auswählen **auf Andere,** wählen **Sie MRXP-Beispieltransport** aus, und klicken Sie dann auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="f2837-152">Under **Choose Email Service** click **Other**, select **MRXP Sample Transport**, and then click **Next**.</span></span>
    
4. <span data-ttu-id="f2837-153">Geben Sie **im Dialogfeld MRXP-Transportkonfiguration** einen **Benutzeranzeigenamen ein.**</span><span class="sxs-lookup"><span data-stu-id="f2837-153">In the **MRXP Transport Configuration** dialog box type a **User Display Name**.</span></span>
    
5. <span data-ttu-id="f2837-154">Geben **Sie unter Pfad zum Posteingang (UNC Share)** einen Ordnerpfad ein.</span><span class="sxs-lookup"><span data-stu-id="f2837-154">Under **Path to Inbox (UNC Share)** enter a folder path.</span></span> <span data-ttu-id="f2837-155">Dies kann auch ein Pfad zu einem lokalen Ordner sein.</span><span class="sxs-lookup"><span data-stu-id="f2837-155">This can also be a path to a local folder.</span></span> 
    
    > [!IMPORTANT]
    > <span data-ttu-id="f2837-156">Dieser Pfad muss vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="f2837-156">This path must exist.</span></span> 
  
6. <span data-ttu-id="f2837-157">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="f2837-157">Click **OK**.</span></span>
    
7. <span data-ttu-id="f2837-158">Klicken Sie **im Dialogfeld E-Mail-Konto** hinzufügen auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="f2837-158">In the **Add Email Account** dialog box click **OK**.</span></span> <span data-ttu-id="f2837-159">Klicken Sie **auf Fertig** stellen, und klicken Sie dann auf **Schließen**.</span><span class="sxs-lookup"><span data-stu-id="f2837-159">Click **Finish** and then click **Close**.</span></span>
    
8. <span data-ttu-id="f2837-160">Um mit der Verwendung des MRXP-Kontos zu beginnen, beenden und starten Sie Outlook.</span><span class="sxs-lookup"><span data-stu-id="f2837-160">To start using the MRXP account, exit and restart Outlook.</span></span>
    
 <span data-ttu-id="f2837-161">**So verwenden Sie das Beispiel des Transportanbieters zum Senden einer Nachricht in Outlook**</span><span class="sxs-lookup"><span data-stu-id="f2837-161">**To use the Transport Provider Sample to send a message in Outlook**</span></span>
  
1. <span data-ttu-id="f2837-162">Klicken Sie **im** Menü Datei auf **Neu,** und klicken Sie dann auf **E-Mail-Nachricht**.</span><span class="sxs-lookup"><span data-stu-id="f2837-162">On the **File** menu, click **New**, and then click **Mail Message**.</span></span>
    
2. <span data-ttu-id="f2837-163">Geben Sie **im Feld An** den Namen des Empfängers im Format **[MRXP: \< ADDRESS ] \> ein.**</span><span class="sxs-lookup"><span data-stu-id="f2837-163">In the **To** box type the name of the recipient using the format **[MRXP:\<ADDRESS\>]**.</span></span> <span data-ttu-id="f2837-164">Die Adresse ist der UNC-Freigabe- oder lokaler Ordnerpfad zum Posteingang des Empfängers.</span><span class="sxs-lookup"><span data-stu-id="f2837-164">The address is the UNC share or local folder path to the recipient's inbox.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="f2837-165">Wenn die Adresse Doppelpunkte oder umgekehrte Schrägstriche hat, müssen Sie vor jedem Doppelpunkt oder umgekehrten Schrägstrich einen umgekehrten Schrägstrich einfügen.</span><span class="sxs-lookup"><span data-stu-id="f2837-165">If there are colons or backslashes in the address, you must insert a backslash before each colon or backslash.</span></span> <span data-ttu-id="f2837-166">Zum Senden von E-Mails an [MRXP:C:\Mail\myDir] müssen Sie z. B.  `[MRXP:C\:\\Mail\\myDir]` eingeben.</span><span class="sxs-lookup"><span data-stu-id="f2837-166">For example, to send mail to [MRXP:C:\Mail\myDir] you must type  `[MRXP:C\:\\Mail\\myDir]`.</span></span> 
  
    > [!IMPORTANT]
    > <span data-ttu-id="f2837-167">Die Empfängeradresse muss vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="f2837-167">The recipient address must exist.</span></span> 
  
3. <span data-ttu-id="f2837-168">Klicken Sie **auf Konto,** und klicken Sie dann **auf MRXP-Beispieltransport**.</span><span class="sxs-lookup"><span data-stu-id="f2837-168">Click **Account** and then click **MRXP Sample Transport**.</span></span>
    
4. <span data-ttu-id="f2837-169">Geben Sie Ihre Nachricht ein, und klicken Sie auf **Senden**.</span><span class="sxs-lookup"><span data-stu-id="f2837-169">Type your message and click **Send**.</span></span> <span data-ttu-id="f2837-170">Die Nachricht wird über den MRXP-Transportanbieter gesendet.</span><span class="sxs-lookup"><span data-stu-id="f2837-170">The message is sent using the MRXP transport provider.</span></span>
    
 <span data-ttu-id="f2837-171">**So verwenden Sie das Beispiel des Transportanbieters zum Empfangen einer Nachricht in Outlook**</span><span class="sxs-lookup"><span data-stu-id="f2837-171">**To use the Transport Provider Sample to receive a message in Outlook**</span></span>
  
1. <span data-ttu-id="f2837-172">Klicken Sie **im** Menü Datei auf **Neu,** und klicken Sie dann auf **E-Mail-Nachricht**.</span><span class="sxs-lookup"><span data-stu-id="f2837-172">On the **File** menu, click **New**, and then click **Mail Message**.</span></span>
    
2. <span data-ttu-id="f2837-173">Geben Sie Ihre Nachricht ein.</span><span class="sxs-lookup"><span data-stu-id="f2837-173">Type your message.</span></span>
    
3. <span data-ttu-id="f2837-174">Klicken Sie **Microsoft Office Schaltfläche,** klicken Sie auf **Speichern unter**, und klicken Sie dann auf **Speichern unter,** um die Datei im Posteingangsordner zu speichern, den Sie während des Setups angegeben haben.</span><span class="sxs-lookup"><span data-stu-id="f2837-174">Click the **Microsoft Office Button**, click **Save As**, and then click **Save As** to save the file to the inbox folder you specified during setup.</span></span> 
    
4. <span data-ttu-id="f2837-175">Navigieren Sie **im** Dialogfeld Speichern unter zu der UNC-Freigabe oder dem lokalen Ordner, den Sie als Posteingang festlegen.</span><span class="sxs-lookup"><span data-stu-id="f2837-175">In the **Save As** dialog box, browse to the UNC share or local folder that you set as your inbox.</span></span> 
    
5. <span data-ttu-id="f2837-176">Klicken Sie **in der Dropdownliste** Unter Typ speichern **auf Outlook Nachrichtenformat**.</span><span class="sxs-lookup"><span data-stu-id="f2837-176">In the **Save as type** drop down, click **Outlook Message Format**.</span></span>
    
6. <span data-ttu-id="f2837-177">Geben Sie einen Namen für die Datei ein, und klicken Sie auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="f2837-177">Type a name for the file and click **Save**.</span></span>
    
7. <span data-ttu-id="f2837-178">Die Datei wird im freigegebenen Ordner gespeichert.</span><span class="sxs-lookup"><span data-stu-id="f2837-178">The file is saved to the shared folder.</span></span> <span data-ttu-id="f2837-179">Der MRXP-Transportanbieter übermittelt die Nachricht an Ihren Posteingang in Outlook.</span><span class="sxs-lookup"><span data-stu-id="f2837-179">The MRXP transport provider delivers the message to your Inbox in Outlook.</span></span>
    

