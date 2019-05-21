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
ms.openlocfilehash: fa2a447d0757e75c95d7dc3d9b1dd16b8c7a8084
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331108"
---
# <a name="address-book-provider-sample"></a><span data-ttu-id="28f9a-103">Adressbuchanbieter-Beispiel</span><span class="sxs-lookup"><span data-stu-id="28f9a-103">Address book provider sample</span></span>

  
  
<span data-ttu-id="28f9a-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="28f9a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="28f9a-105">Dieses Beispiel unterstützt einen einzelnen schreibgeschützten Container für Anzeigenamen und E-Mail-Adressen, die aus einer Flatfile-Binärdatei ausgelesen werden.</span><span class="sxs-lookup"><span data-stu-id="28f9a-105">This sample supports a single read-only container for display names and email addresses, which are read from a flat binary file.</span></span> <span data-ttu-id="28f9a-106">Das Beispiel unterstützt einmalige Vorlagen und alle Konfigurationsoptionen außer den Profil-Assistenten.</span><span class="sxs-lookup"><span data-stu-id="28f9a-106">The sample supports one-off templates and all configuration options except the Profile Wizard.</span></span>
  
<span data-ttu-id="28f9a-107">Sie können dieses Beispiel aus [Outlook-MAPI-Code-Beispiele (Messaging-API)](https://go.microsoft.com/fwlink/?LinkId=129740
) herunterladen.</span><span class="sxs-lookup"><span data-stu-id="28f9a-107">You can download this sample from [Outlook Messaging API (MAPI) Code Samples](https://go.microsoft.com/fwlink/?LinkId=129740
).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="28f9a-108">Ausführbar:</span><span class="sxs-lookup"><span data-stu-id="28f9a-108">Executable file</span></span>  <br/> |<span data-ttu-id="28f9a-109">SABP32.dll</span><span class="sxs-lookup"><span data-stu-id="28f9a-109">SABP32.dll</span></span>  <br/> |
| <span data-ttu-id="28f9a-110">Quellcode-Verzeichnis:</span><span class="sxs-lookup"><span data-stu-id="28f9a-110">Source code directory:</span></span>  <br/> |<span data-ttu-id="28f9a-111">SampleAddressBookProvider\SABP</span><span class="sxs-lookup"><span data-stu-id="28f9a-111">SampleAddressBookProvider\SABP</span></span>  <br/> |
|<span data-ttu-id="28f9a-112">Sprache:</span><span class="sxs-lookup"><span data-stu-id="28f9a-112">Language</span></span>  <br/> |<span data-ttu-id="28f9a-113">C++</span><span class="sxs-lookup"><span data-stu-id="28f9a-113">C#</span></span>  <br/> |
|<span data-ttu-id="28f9a-114">Plattformen:</span><span class="sxs-lookup"><span data-stu-id="28f9a-114">Platforms</span></span>  <br/> |<span data-ttu-id="28f9a-115">Microsoft Visual Studio 2008 zum Kompilieren für Windows Vista, Windows Server 2008, Windows XP SP2 und Windows Server 2003 SP1</span><span class="sxs-lookup"><span data-stu-id="28f9a-115">Microsoft Visual Studio 2008 to compile for Windows Vista, Windows Server 2008, Windows XP SP2, and Windows Server 2003 SP1</span></span>  <br/> |
   
## <a name="supported-features"></a><span data-ttu-id="28f9a-116">Unterstützte Features</span><span class="sxs-lookup"><span data-stu-id="28f9a-116">Supported features</span></span>

<span data-ttu-id="28f9a-117">In diesem Beispiel werden die folgenden Features unterstützt:</span><span class="sxs-lookup"><span data-stu-id="28f9a-117">This sample supports the following features:</span></span>
  
- <span data-ttu-id="28f9a-118">Tabelleneinschränkungen.</span><span class="sxs-lookup"><span data-stu-id="28f9a-118">Table restrictions.</span></span> <span data-ttu-id="28f9a-119">Im Beispiel wird eine Auflösung von Namen mit Präfixübereinstimmung und mehrdeutigen Namen implementiert.</span><span class="sxs-lookup"><span data-stu-id="28f9a-119">The sample implements prefix-match and ambiguous-name resolution.</span></span> <span data-ttu-id="28f9a-120">Es wird nicht die vollständige MAPI-Einschränkungssprache implementiert und Einschränkungen werden nur im Anzeigenamen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="28f9a-120">It does not implement the full MAPI restriction language, and restrictions are supported only on the display name.</span></span>
    
- <span data-ttu-id="28f9a-121">Eine Detail-Anzeigetabelle für Nachrichtenbenutzer.</span><span class="sxs-lookup"><span data-stu-id="28f9a-121">A details display table for messaging users.</span></span> 
    
- <span data-ttu-id="28f9a-122">Einmaladressen.</span><span class="sxs-lookup"><span data-stu-id="28f9a-122">One-off addresses</span></span>
    
- <span data-ttu-id="28f9a-123">Ein Dialogfeld für die erweiterte Suche.</span><span class="sxs-lookup"><span data-stu-id="28f9a-123">An advanced search dialog box.</span></span>
    
- <span data-ttu-id="28f9a-124">Eine [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md)-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="28f9a-124">An [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) interface.</span></span> <span data-ttu-id="28f9a-125">Diese Schnittstelle wird teilweise unterstützt; ihre **IMAPIProp**-Methoden werden an die **IPropData**-Schnittstelle delegiert.</span><span class="sxs-lookup"><span data-stu-id="28f9a-125">This interface is partially supported; its **IMAPIProp** methods are delegated to the **IPropData** interface.</span></span> <span data-ttu-id="28f9a-126">Weitere Informationen finden Sie unter der [IPropData : IMAPIProp](ipropdataimapiprop.md)-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="28f9a-126">For more information, see the [IPropData : IMAPIProp](ipropdataimapiprop.md) interface.</span></span> 
    
- <span data-ttu-id="28f9a-127">Interaktive und programmgesteuerte Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="28f9a-127">Interactive and programmatic configuration.</span></span>
    
## <a name="unsupported-features"></a><span data-ttu-id="28f9a-128">Nicht unterstützte Features</span><span class="sxs-lookup"><span data-stu-id="28f9a-128">Unsupported features</span></span>

<span data-ttu-id="28f9a-129">In diesem Beispiel werden die folgenden Features nicht unterstützt:</span><span class="sxs-lookup"><span data-stu-id="28f9a-129">This sample does not support the following features:</span></span>
  
- <span data-ttu-id="28f9a-130">Sortieren.</span><span class="sxs-lookup"><span data-stu-id="28f9a-130">Sorting</span></span>
    
- <span data-ttu-id="28f9a-131">Verteilerlisten.</span><span class="sxs-lookup"><span data-stu-id="28f9a-131">Distribution lists</span></span>
    
- <span data-ttu-id="28f9a-132">Erstellen, Löschen und Ändern von Einträgen.</span><span class="sxs-lookup"><span data-stu-id="28f9a-132">Creating, deleting, and modifying entries.</span></span>
    
- <span data-ttu-id="28f9a-133">Eigenschaften mit mehreren Werten.</span><span class="sxs-lookup"><span data-stu-id="28f9a-133">Properties with multiple values.</span></span>
    
- <span data-ttu-id="28f9a-134">Benannte Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="28f9a-134">Named properties</span></span>
    
- <span data-ttu-id="28f9a-135">Unterscheidung zwischen Vor- und Nachnamen in Anzeigenamen.</span><span class="sxs-lookup"><span data-stu-id="28f9a-135">Distinguishing between first and last names in display names.</span></span>
    
 <span data-ttu-id="28f9a-136">**So laden Sie das Beispiel für einen Adressbuchanbieter herunter**</span><span class="sxs-lookup"><span data-stu-id="28f9a-136">**To download the Sample Address Book Provider**</span></span>
  
1. <span data-ttu-id="28f9a-137">Informationen zum Herunterladen des Beispiels für einen Adressbuchanbieter finden Sie unter [Herunterladen der Outlook-MAPI-Beispiele](downloading-the-outlook-mapi-samples.md).</span><span class="sxs-lookup"><span data-stu-id="28f9a-137">To download the Sample Address Book Provider, see [Downloading the Outlook MAPI Samples](downloading-the-outlook-mapi-samples.md).</span></span>
    
2. <span data-ttu-id="28f9a-138">Suchen Sie den Ordner, in dem die Outlook-MAPI-Beispiele gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="28f9a-138">Locate the folder where you saved the Outlook MAPI Samples.</span></span> <span data-ttu-id="28f9a-139">Klicken Sie mit der rechten Maustaste auf den ZIP-Ordner **OutlookMAPISamples-\<Versionsnummer\>**, und klicken Sie auf **Alle extrahieren**.</span><span class="sxs-lookup"><span data-stu-id="28f9a-139">Right-click the **OutlookMAPISamples-\<version number\>** zip folder and click **Extract All**.</span></span>
    
3. <span data-ttu-id="28f9a-140">Klicken Sie auf **Durchsuchen**, wählen Sie den Speicherort aus, wo Sie das Beispiel speichern wollen und klicken Sie auf **Extrahieren**.</span><span class="sxs-lookup"><span data-stu-id="28f9a-140">Click **Browse**, select the location where you want to save the sample, and click **Extract**.</span></span>
    
4. <span data-ttu-id="28f9a-141">Führen Sie Visual Studio 2008 aus.</span><span class="sxs-lookup"><span data-stu-id="28f9a-141">Visual Studio 2008</span></span>
    
5. <span data-ttu-id="28f9a-142">Klicken Sie in Visual Studio 2008 auf **Datei**, wählen Sie **Öffnen** aus, und klicken Sie dann auf **Projekt/Lösung**.</span><span class="sxs-lookup"><span data-stu-id="28f9a-142">In Visual Studio 2008, click **File**, select **Open**, and then click **Project/Solution**.</span></span>
    
6. <span data-ttu-id="28f9a-143">Navigieren Sie zu dem Speicherort, wo Sie das Beispiel gespeichert haben, klicken Sie auf **SABP.vcproj**, und klicken Sie dann auf **Öffnen**.</span><span class="sxs-lookup"><span data-stu-id="28f9a-143">Browse to the location where you saved the sample, click **SABP.vcproj**, and then click **Open**.</span></span>
    
7. <span data-ttu-id="28f9a-144">Klicken Sie im Menü **Erstellen** auf **Projektmappe erstellen**.</span><span class="sxs-lookup"><span data-stu-id="28f9a-144">On the **Build** menu, click **Build Solution**.</span></span>
    
8. <span data-ttu-id="28f9a-145">Klicken Sie im Dialogfeld **Speichern unter** auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="28f9a-145">In the **Save File As** dialog box, click the down arrow on the **Save** button.</span></span>
    
9. <span data-ttu-id="28f9a-146">Klicken Sie in dem Ordner, wo Sie das Beispiel gespeichert haben, mit der rechten Maustaste auf die Datei **install.bat**, und klicken Sie auf **Als Administrator ausführen**.</span><span class="sxs-lookup"><span data-stu-id="28f9a-146">In the folder where you saved the sample, right-click the **install.bat** file and click **Run as administrator**.</span></span>
    
10. <span data-ttu-id="28f9a-147">Klicken Sie im Dialogfeld **Benutzerkontensteuerung** auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="28f9a-147">In the **User Account Control** dialog box, click **Continue**.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="28f9a-148">**Install.bat** kopiert die .dll in den Microsoft Office-Standardinstallationsordner, C:\Program Files\Microsoft Office\Office12\.</span><span class="sxs-lookup"><span data-stu-id="28f9a-148">**Install.bat** copies the .dll to the default Microsoft Office installation folder, C:\Program Files\Microsoft Office\Office12\.</span></span> <span data-ttu-id="28f9a-149">Wenn Sie Office-Produkte an einem anderen Speicherort installiert haben, klicken Sie mit der rechten Maustaste auf **Install.bat** und klicken Sie auf **Bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="28f9a-149">If you have installed Office products in a different location, right-click **Install.bat** and click **Edit**.</span></span> <span data-ttu-id="28f9a-150">Die Datei wird im Editor geöffnet.</span><span class="sxs-lookup"><span data-stu-id="28f9a-150">The file opens in Notepad.</span></span> <span data-ttu-id="28f9a-151">Ersetzen Sie den Standardinstallationspfad durch den auf dem Computer verwendeten Installationspfad.</span><span class="sxs-lookup"><span data-stu-id="28f9a-151">Replace the default installation path with the installation path used on your computer.</span></span> 
  

