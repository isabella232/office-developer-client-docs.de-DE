---
title: Beispiel für einen Adressbuchanbieter
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2ccf1643-5604-4fee-92cc-3d6af00e7f98
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: fa2a447d0757e75c95d7dc3d9b1dd16b8c7a8084
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331108"
---
# <a name="address-book-provider-sample"></a><span data-ttu-id="ed5d7-103">Beispiel für einen Adressbuchanbieter</span><span class="sxs-lookup"><span data-stu-id="ed5d7-103">Address Book Provider Sample</span></span>

  
  
<span data-ttu-id="ed5d7-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ed5d7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ed5d7-105">In diesem Beispiel wird ein einzelner schreibgeschützter Container für Anzeigenamen und e-Mail-Adressen unterstützt, die aus einer Flatfile-Binärdatei gelesen werden.</span><span class="sxs-lookup"><span data-stu-id="ed5d7-105">This sample supports a single read-only container for display names and email addresses, which are read from a flat binary file.</span></span> <span data-ttu-id="ed5d7-106">Das Beispiel unterstützt einmalige Vorlagen und alle Konfigurationsoptionen mit Ausnahme des Profil-Assistenten.</span><span class="sxs-lookup"><span data-stu-id="ed5d7-106">The sample supports one-off templates and all configuration options except the Profile Wizard.</span></span>
  
<span data-ttu-id="ed5d7-107">Sie können dieses Beispiel aus [MAPI-Code Beispielen (Outlook Messaging API)](https://go.microsoft.com/fwlink/?LinkId=129740
)herunterladen.</span><span class="sxs-lookup"><span data-stu-id="ed5d7-107">You can download this sample from [Outlook Messaging API (MAPI) Code Samples](https://go.microsoft.com/fwlink/?LinkId=129740
).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ed5d7-108">Executable</span><span class="sxs-lookup"><span data-stu-id="ed5d7-108">Executable:</span></span>  <br/> |<span data-ttu-id="ed5d7-109">SABP32. dll</span><span class="sxs-lookup"><span data-stu-id="ed5d7-109">SABP32.dll</span></span>  <br/> |
| <span data-ttu-id="ed5d7-110">Quellcodeverzeichnis:</span><span class="sxs-lookup"><span data-stu-id="ed5d7-110">Source code directory:</span></span>  <br/> |<span data-ttu-id="ed5d7-111">SampleAddressBookProvider\SABP</span><span class="sxs-lookup"><span data-stu-id="ed5d7-111">SampleAddressBookProvider\SABP</span></span>  <br/> |
|<span data-ttu-id="ed5d7-112">Sprache</span><span class="sxs-lookup"><span data-stu-id="ed5d7-112">Language:</span></span>  <br/> |<span data-ttu-id="ed5d7-113">C++</span><span class="sxs-lookup"><span data-stu-id="ed5d7-113">C++</span></span>  <br/> |
|<span data-ttu-id="ed5d7-114">Plattformen</span><span class="sxs-lookup"><span data-stu-id="ed5d7-114">Platforms:</span></span>  <br/> |<span data-ttu-id="ed5d7-115">Microsoft Visual Studio 2008 für die Kompilierung für Windows Vista, Windows Server 2008, Windows XP SP2 und Windows Server 2003 SP1</span><span class="sxs-lookup"><span data-stu-id="ed5d7-115">Microsoft Visual Studio 2008 to compile for Windows Vista, Windows Server 2008, Windows XP SP2, and Windows Server 2003 SP1</span></span>  <br/> |
   
## <a name="supported-features"></a><span data-ttu-id="ed5d7-116">Unterstützte Features</span><span class="sxs-lookup"><span data-stu-id="ed5d7-116">Supported Features</span></span>

<span data-ttu-id="ed5d7-117">In diesem Beispiel werden die folgenden Features unterstützt:</span><span class="sxs-lookup"><span data-stu-id="ed5d7-117">This sample supports the following features:</span></span>
  
- <span data-ttu-id="ed5d7-118">Tabellen Einschränkungen.</span><span class="sxs-lookup"><span data-stu-id="ed5d7-118">Table restrictions.</span></span> <span data-ttu-id="ed5d7-119">Im Beispiel wird die Auflösung von Präfixen und mehrdeutigen Namen implementiert.</span><span class="sxs-lookup"><span data-stu-id="ed5d7-119">The sample implements prefix-match and ambiguous-name resolution.</span></span> <span data-ttu-id="ed5d7-120">Die vollständige MAPI-Einschränkungs Sprache wird nicht implementiert, und Einschränkungen werden nur für den Anzeigenamen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ed5d7-120">It does not implement the full MAPI restriction language, and restrictions are supported only on the display name.</span></span>
    
- <span data-ttu-id="ed5d7-121">Eine Details-Anzeigetabelle für Messagingbenutzer.</span><span class="sxs-lookup"><span data-stu-id="ed5d7-121">A details display table for messaging users.</span></span> 
    
- <span data-ttu-id="ed5d7-122">Einmalige Adressen.</span><span class="sxs-lookup"><span data-stu-id="ed5d7-122">One-off addresses.</span></span>
    
- <span data-ttu-id="ed5d7-123">Dialogfeld Erweiterte Suche.</span><span class="sxs-lookup"><span data-stu-id="ed5d7-123">An advanced search dialog box.</span></span>
    
- <span data-ttu-id="ed5d7-124">Eine [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="ed5d7-124">An [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) interface.</span></span> <span data-ttu-id="ed5d7-125">Diese Schnittstelle wird teilweise unterstützt; die **IMAPIProp** -Methoden werden an die **IPropData** -Schnittstelle delegiert.</span><span class="sxs-lookup"><span data-stu-id="ed5d7-125">This interface is partially supported; its **IMAPIProp** methods are delegated to the **IPropData** interface.</span></span> <span data-ttu-id="ed5d7-126">Weitere Informationen finden Sie unter der [IPropData: IMAPIProp](ipropdataimapiprop.md) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="ed5d7-126">For more information, see the [IPropData : IMAPIProp](ipropdataimapiprop.md) interface.</span></span> 
    
- <span data-ttu-id="ed5d7-127">Interaktive und programmgesteuerte Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="ed5d7-127">Interactive and programmatic configuration.</span></span>
    
## <a name="unsupported-features"></a><span data-ttu-id="ed5d7-128">Nicht unterstützte Features</span><span class="sxs-lookup"><span data-stu-id="ed5d7-128">Unsupported Features</span></span>

<span data-ttu-id="ed5d7-129">In diesem Beispiel werden die folgenden Features nicht unterstützt:</span><span class="sxs-lookup"><span data-stu-id="ed5d7-129">This sample does not support the following features:</span></span>
  
- <span data-ttu-id="ed5d7-130">Sortierung.</span><span class="sxs-lookup"><span data-stu-id="ed5d7-130">Sorting.</span></span>
    
- <span data-ttu-id="ed5d7-131">Verteilerlisten.</span><span class="sxs-lookup"><span data-stu-id="ed5d7-131">Distribution lists.</span></span>
    
- <span data-ttu-id="ed5d7-132">Erstellen, löschen und Ändern von Einträgen.</span><span class="sxs-lookup"><span data-stu-id="ed5d7-132">Creating, deleting, and modifying entries.</span></span>
    
- <span data-ttu-id="ed5d7-133">Eigenschaften mit mehreren Werten.</span><span class="sxs-lookup"><span data-stu-id="ed5d7-133">Properties with multiple values.</span></span>
    
- <span data-ttu-id="ed5d7-134">Benannte Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="ed5d7-134">Named properties.</span></span>
    
- <span data-ttu-id="ed5d7-135">Unterscheidung zwischen vor-und Nachnamen in Anzeigenamen.</span><span class="sxs-lookup"><span data-stu-id="ed5d7-135">Distinguishing between first and last names in display names.</span></span>
    
 <span data-ttu-id="ed5d7-136">**So installieren Sie den Beispiel-Adressbuchanbieter**</span><span class="sxs-lookup"><span data-stu-id="ed5d7-136">**To install the Sample Address Book Provider**</span></span>
  
1. <span data-ttu-id="ed5d7-137">Informationen zum Herunterladen des Beispiel-Adressbuch Anbieters finden Sie unter [herunterladen der Outlook-MAPI-Beispiele](downloading-the-outlook-mapi-samples.md).</span><span class="sxs-lookup"><span data-stu-id="ed5d7-137">To download the Sample Address Book Provider, see [Downloading the Outlook MAPI Samples](downloading-the-outlook-mapi-samples.md).</span></span>
    
2. <span data-ttu-id="ed5d7-138">Suchen Sie den Ordner, in dem Sie die Outlook-MAPI-Beispiele gespeichert haben.</span><span class="sxs-lookup"><span data-stu-id="ed5d7-138">Locate the folder where you saved the Outlook MAPI Samples.</span></span> <span data-ttu-id="ed5d7-139">Klicken Sie mit der rechten Maustaste auf den Zip **-Ordner OutlookMAPISamples-\<Versions\> Nummer** , und klicken Sie auf **Alle extrahieren**.</span><span class="sxs-lookup"><span data-stu-id="ed5d7-139">Right-click the **OutlookMAPISamples-\<version number\>** zip folder and click **Extract All**.</span></span>
    
3. <span data-ttu-id="ed5d7-140">Klicken Sie auf **Durchsuchen**, wählen Sie den Speicherort aus, an dem Sie das Beispiel speichern möchten, und klicken Sie auf **extrahieren**.</span><span class="sxs-lookup"><span data-stu-id="ed5d7-140">Click **Browse**, select the location where you want to save the sample, and click **Extract**.</span></span>
    
4. <span data-ttu-id="ed5d7-141">Führen Sie Visual Studio 2008 aus.</span><span class="sxs-lookup"><span data-stu-id="ed5d7-141">Run Visual Studio 2008.</span></span>
    
5. <span data-ttu-id="ed5d7-142">Klicken Sie in Visual Studio 2008 auf **Datei**, wählen Sie **Öffnen**aus, und klicken Sie dann auf **Projekt/Lösung**.</span><span class="sxs-lookup"><span data-stu-id="ed5d7-142">In Visual Studio 2008, click **File**, select **Open**, and then click **Project/Solution**.</span></span>
    
6. <span data-ttu-id="ed5d7-143">Navigieren Sie zu dem Speicherort, an dem Sie das Beispiel gespeichert haben, klicken Sie auf **SABP. vcproj**, und klicken Sie dann auf **Öffnen**.</span><span class="sxs-lookup"><span data-stu-id="ed5d7-143">Browse to the location where you saved the sample, click **SABP.vcproj**, and then click **Open**.</span></span>
    
7. <span data-ttu-id="ed5d7-144">On the **Build** menu, click **Build Solution**.</span><span class="sxs-lookup"><span data-stu-id="ed5d7-144">On the **Build** menu, click **Build Solution**.</span></span>
    
8. <span data-ttu-id="ed5d7-145">Klicken Sie im Dialogfeld **Datei speichern** unter auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="ed5d7-145">In the **Save File As** dialog box, click **Save**.</span></span>
    
9. <span data-ttu-id="ed5d7-146">Klicken Sie in dem Ordner, in dem Sie das Beispiel gespeichert haben, mit der rechten Maustaste auf die Datei **install. bat** , und klicken Sie dann auf **als Administrator ausführen**.</span><span class="sxs-lookup"><span data-stu-id="ed5d7-146">In the folder where you saved the sample, right-click the **install.bat** file and click **Run as administrator**.</span></span>
    
10. <span data-ttu-id="ed5d7-147">Klicken Sie im Dialogfeld **Benutzerkontensteuerung** auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="ed5d7-147">In the **User Account Control** dialog box, click **Continue**.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="ed5d7-148">**Install. bat** kopiert die dll in den standardMäßigen Microsoft Office-Installationsordner, c:\Programme\Microsoft Office\Office12\.</span><span class="sxs-lookup"><span data-stu-id="ed5d7-148">**Install.bat** copies the .dll to the default Microsoft Office installation folder, C:\Program Files\Microsoft Office\Office12\.</span></span> <span data-ttu-id="ed5d7-149">Wenn Sie Office-Produkte an einem anderen Speicherort installiert haben, klicken Sie mit der rechten Maustaste auf **install. bat** , und klicken Sie auf **Bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="ed5d7-149">If you have installed Office products in a different location, right-click **Install.bat** and click **Edit**.</span></span> <span data-ttu-id="ed5d7-150">Die Datei wird im Editor geöffnet.</span><span class="sxs-lookup"><span data-stu-id="ed5d7-150">The file opens in Notepad.</span></span> <span data-ttu-id="ed5d7-151">Ersetzen Sie den Standardinstallationspfad durch den Installationspfad, der auf Ihrem Computer verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ed5d7-151">Replace the default installation path with the installation path used on your computer.</span></span> 
  

