---
title: Adressbuchanbieter-Beispiel
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2ccf1643-5604-4fee-92cc-3d6af00e7f98
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: ebbed00fb920994f40b7ae139c7eddd658984b95
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566859"
---
# <a name="address-book-provider-sample"></a><span data-ttu-id="fe752-103">Adressbuchanbieter-Beispiel</span><span class="sxs-lookup"><span data-stu-id="fe752-103">Address Book Provider Sample</span></span>

  
  
<span data-ttu-id="fe752-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fe752-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fe752-105">In diesem Beispiel unterstützt einen einzelnen schreibgeschützten Container für Anzeigenamen und e-Mail-Adressen, die aus einer flachen Binärdatei gelesen werden.</span><span class="sxs-lookup"><span data-stu-id="fe752-105">This sample supports a single read-only container for display names and email addresses, which are read from a flat binary file.</span></span> <span data-ttu-id="fe752-106">Im Beispiel werden einmal-Vorlagen und alle Konfigurationsoptionen, mit Ausnahme der Profil-Assistent unterstützt.</span><span class="sxs-lookup"><span data-stu-id="fe752-106">The sample supports one-off templates and all configuration options except the Profile Wizard.</span></span>
  
<span data-ttu-id="fe752-107">Sie können dieses Beispiel aus [Outlook Messaging-API (MAPI)-Codebeispiele](http://go.microsoft.com/fwlink/?LinkId=129740
)herunterladen.</span><span class="sxs-lookup"><span data-stu-id="fe752-107">You can download this sample from [Outlook Messaging API (MAPI) Code Samples](http://go.microsoft.com/fwlink/?LinkId=129740
).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="fe752-108">Ausführbare Datei:</span><span class="sxs-lookup"><span data-stu-id="fe752-108">Executable:</span></span>  <br/> |<span data-ttu-id="fe752-109">SABP32.dll</span><span class="sxs-lookup"><span data-stu-id="fe752-109">SABP32.dll</span></span>  <br/> |
| <span data-ttu-id="fe752-110">Code Quellverzeichnis:</span><span class="sxs-lookup"><span data-stu-id="fe752-110">Source code directory:</span></span>  <br/> |<span data-ttu-id="fe752-111">SampleAddressBookProvider\SABP</span><span class="sxs-lookup"><span data-stu-id="fe752-111">SampleAddressBookProvider\SABP</span></span>  <br/> |
|<span data-ttu-id="fe752-112">Sprache:</span><span class="sxs-lookup"><span data-stu-id="fe752-112">Language:</span></span>  <br/> |<span data-ttu-id="fe752-113">C++</span><span class="sxs-lookup"><span data-stu-id="fe752-113">C++</span></span>  <br/> |
|<span data-ttu-id="fe752-114">Plattformen:</span><span class="sxs-lookup"><span data-stu-id="fe752-114">Platforms:</span></span>  <br/> |<span data-ttu-id="fe752-115">Microsoft Visual Studio 2008 zum Kompilieren für Windows Vista, Windows Server 2008, Windows XP SP2 und Windows Server 2003 SP1</span><span class="sxs-lookup"><span data-stu-id="fe752-115">Microsoft Visual Studio 2008 to compile for Windows Vista, Windows Server 2008, Windows XP SP2, and Windows Server 2003 SP1</span></span>  <br/> |
   
## <a name="supported-features"></a><span data-ttu-id="fe752-116">Unterstützte Features</span><span class="sxs-lookup"><span data-stu-id="fe752-116">Supported Features</span></span>

<span data-ttu-id="fe752-117">In diesem Beispiel werden die folgenden Features unterstützt:</span><span class="sxs-lookup"><span data-stu-id="fe752-117">This sample supports the following features:</span></span>
  
- <span data-ttu-id="fe752-118">Tabelle Einschränkungen.</span><span class="sxs-lookup"><span data-stu-id="fe752-118">Table restrictions.</span></span> <span data-ttu-id="fe752-119">Im Beispiel wird die präfixübereinstimmung und mehrdeutiger Name Resolution implementiert.</span><span class="sxs-lookup"><span data-stu-id="fe752-119">The sample implements prefix-match and ambiguous-name resolution.</span></span> <span data-ttu-id="fe752-120">Die vollständige MAPI-Einschränkung Sprache wird nicht implementiert, und Einschränkungen sind nur für den Anzeigenamen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="fe752-120">It does not implement the full MAPI restriction language, and restrictions are supported only on the display name.</span></span>
    
- <span data-ttu-id="fe752-121">Eine Tabelle, für Benutzer messaging Details anzeigen.</span><span class="sxs-lookup"><span data-stu-id="fe752-121">A details display table for messaging users.</span></span> 
    
- <span data-ttu-id="fe752-122">Einmal-Adressen.</span><span class="sxs-lookup"><span data-stu-id="fe752-122">One-off addresses.</span></span>
    
- <span data-ttu-id="fe752-123">Ein Dialogfeld Erweiterte Suche.</span><span class="sxs-lookup"><span data-stu-id="fe752-123">An advanced search dialog box.</span></span>
    
- <span data-ttu-id="fe752-124">Ein [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md) Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="fe752-124">An [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) interface.</span></span> <span data-ttu-id="fe752-125">Diese Schnittstelle ist teilweise unterstützt. seine **IMAPIProp** Methoden werden an die Schnittstelle **IPropData** delegiert.</span><span class="sxs-lookup"><span data-stu-id="fe752-125">This interface is partially supported; its **IMAPIProp** methods are delegated to the **IPropData** interface.</span></span> <span data-ttu-id="fe752-126">Weitere Informationen finden Sie unter der [IPropData: IMAPIProp](ipropdataimapiprop.md) Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="fe752-126">For more information, see the [IPropData : IMAPIProp](ipropdataimapiprop.md) interface.</span></span> 
    
- <span data-ttu-id="fe752-127">Interaktive und programmgesteuerte Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="fe752-127">Interactive and programmatic configuration.</span></span>
    
## <a name="unsupported-features"></a><span data-ttu-id="fe752-128">Nicht unterstützte Features</span><span class="sxs-lookup"><span data-stu-id="fe752-128">Unsupported Features</span></span>

<span data-ttu-id="fe752-129">In diesem Beispiel wird die folgenden Features nicht unterstützt:</span><span class="sxs-lookup"><span data-stu-id="fe752-129">This sample does not support the following features:</span></span>
  
- <span data-ttu-id="fe752-130">Sortieren.</span><span class="sxs-lookup"><span data-stu-id="fe752-130">Sorting.</span></span>
    
- <span data-ttu-id="fe752-131">Verteilerlisten.</span><span class="sxs-lookup"><span data-stu-id="fe752-131">Distribution lists.</span></span>
    
- <span data-ttu-id="fe752-132">Erstellen, löschen und Ändern von Einträgen.</span><span class="sxs-lookup"><span data-stu-id="fe752-132">Creating, deleting, and modifying entries.</span></span>
    
- <span data-ttu-id="fe752-133">Eigenschaften mit mehreren Werten.</span><span class="sxs-lookup"><span data-stu-id="fe752-133">Properties with multiple values.</span></span>
    
- <span data-ttu-id="fe752-134">Benannte Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="fe752-134">Named properties.</span></span>
    
- <span data-ttu-id="fe752-135">Unterscheidung zwischen vor- und Nachnamen Namen im Anzeigenamen.</span><span class="sxs-lookup"><span data-stu-id="fe752-135">Distinguishing between first and last names in display names.</span></span>
    
 <span data-ttu-id="fe752-136">**So installieren Sie die Beispiel-Adressbuchanbieter**</span><span class="sxs-lookup"><span data-stu-id="fe752-136">**To install the Sample Address Book Provider**</span></span>
  
1. <span data-ttu-id="fe752-137">Wenn die Beispiel-Adressbuchanbieter herunterladen möchten, finden Sie unter [Herunterladen der MAPI-Beispiele für Outlook](downloading-the-outlook-mapi-samples.md).</span><span class="sxs-lookup"><span data-stu-id="fe752-137">To download the Sample Address Book Provider, see [Downloading the Outlook MAPI Samples](downloading-the-outlook-mapi-samples.md).</span></span>
    
2. <span data-ttu-id="fe752-138">Suchen Sie den Ordner, in dem Sie die MAPI-Beispiele für Outlook gespeichert.</span><span class="sxs-lookup"><span data-stu-id="fe752-138">Locate the folder where you saved the Outlook MAPI Samples.</span></span> <span data-ttu-id="fe752-139">Mit der rechten Maustaste die **OutlookMAPISamples -\<Versionsnummer\> ** zip-Ordner, und klicken Sie auf **Alle extrahieren**.</span><span class="sxs-lookup"><span data-stu-id="fe752-139">Right-click the **OutlookMAPISamples-\<version number\>** zip folder and click **Extract All**.</span></span>
    
3. <span data-ttu-id="fe752-140">Klicken Sie auf **Durchsuchen**, markieren Sie den Speicherort, in dem Sie das Beispiel zu speichern möchten, und klicken Sie auf **extrahieren**.</span><span class="sxs-lookup"><span data-stu-id="fe752-140">Click **Browse**, select the location where you want to save the sample, and click **Extract**.</span></span>
    
4. <span data-ttu-id="fe752-141">Führen Sie Visual Studio 2008.</span><span class="sxs-lookup"><span data-stu-id="fe752-141">Run Visual Studio 2008.</span></span>
    
5. <span data-ttu-id="fe752-142">Klicken Sie in Visual Studio 2008 auf **Datei**, klicken Sie auf **Öffnen**, und klicken Sie dann auf **Projekt/Projektmappe**.</span><span class="sxs-lookup"><span data-stu-id="fe752-142">In Visual Studio 2008, click **File**, select **Open**, and then click **Project/Solution**.</span></span>
    
6. <span data-ttu-id="fe752-143">Navigieren Sie zum Speicherort, in dem Sie das Beispiel gespeichert haben, klicken Sie auf **SABP.vcproj**und klicken Sie dann auf **Öffnen**.</span><span class="sxs-lookup"><span data-stu-id="fe752-143">Browse to the location where you saved the sample, click **SABP.vcproj**, and then click **Open**.</span></span>
    
7. <span data-ttu-id="fe752-144">On the **Build** menu, click **Build Solution**.</span><span class="sxs-lookup"><span data-stu-id="fe752-144">On the **Build** menu, click **Build Solution**.</span></span>
    
8. <span data-ttu-id="fe752-145">Klicken Sie im Dialogfeld **Datei speichern unter** auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="fe752-145">In the **Save File As** dialog box, click **Save**.</span></span>
    
9. <span data-ttu-id="fe752-146">In den Ordner, in dem Sie das Beispiel gespeichert haben, mit der rechten Maustaste in der Datei **Install.bat aus** , und klicken Sie auf **als Administrator ausführen**.</span><span class="sxs-lookup"><span data-stu-id="fe752-146">In the folder where you saved the sample, right-click the **install.bat** file and click **Run as administrator**.</span></span>
    
10. <span data-ttu-id="fe752-147">Klicken Sie im Dialogfeld **Benutzerkontensteuerung** auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="fe752-147">In the **User Account Control** dialog box, click **Continue**.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="fe752-148">**Install.bat** kopiert die DLL-Datei in den standardmäßigen Microsoft Office-Installationsordner C:\Program Files\Microsoft Office\Office12\.</span><span class="sxs-lookup"><span data-stu-id="fe752-148">**Install.bat** copies the .dll to the default Microsoft Office installation folder, C:\Program Files\Microsoft Office\Office12\.</span></span> <span data-ttu-id="fe752-149">Wenn Sie Office-Produkte an einem anderen Speicherort installiert haben, mit der rechten Maustaste **Install.bat aus** , und klicken Sie auf **Bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="fe752-149">If you have installed Office products in a different location, right-click **Install.bat** and click **Edit**.</span></span> <span data-ttu-id="fe752-150">Die Datei wird im Editor geöffnet.</span><span class="sxs-lookup"><span data-stu-id="fe752-150">The file opens in Notepad.</span></span> <span data-ttu-id="fe752-151">Ersetzen Sie den Standardpfad für die Installation durch den Installationspfad auf Ihrem Computer verwendet.</span><span class="sxs-lookup"><span data-stu-id="fe752-151">Replace the default installation path with the installation path used on your computer.</span></span> 
  

