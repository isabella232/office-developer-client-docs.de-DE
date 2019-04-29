---
title: Unterstützen der Nachrichtendienst Installation
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 822e07bc-0bca-4485-8938-2264315161e2
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 328884e8758e679eb1c9d968547cba02c01d4d47
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404701"
---
# <a name="supporting-message-service-installation"></a><span data-ttu-id="33a9a-103">Unterstützen der Nachrichtendienst Installation</span><span class="sxs-lookup"><span data-stu-id="33a9a-103">Supporting Message Service Installation</span></span>

  
  
<span data-ttu-id="33a9a-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="33a9a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="33a9a-105">Das Setupprogramm für die Installation des Nachrichtendiensts sollte folgendermaßen vorgehen:</span><span class="sxs-lookup"><span data-stu-id="33a9a-105">The setup program for installing your message service should do the following:</span></span>
  
1. <span data-ttu-id="33a9a-106">Kopieren Sie Nachrichtendienst Dateien wie den Nachrichtendienst und die Dienstanbieter-DLLs von einer CD oder einem Datenträger auf ein lokales Laufwerk auf der Arbeitsstation.</span><span class="sxs-lookup"><span data-stu-id="33a9a-106">Copy message service files, such as the message service and service provider DLLs, from a CD or disk, to a local drive on the workstation.</span></span> <span data-ttu-id="33a9a-107">Die zu kopierenden Dateien hängen vom Nachrichtendienst ab.</span><span class="sxs-lookup"><span data-stu-id="33a9a-107">The files that need to be copied depend on your message service.</span></span> <span data-ttu-id="33a9a-108">In der Regel kopieren Sie mindestens eine DLL.</span><span class="sxs-lookup"><span data-stu-id="33a9a-108">Typically you will copy at least one DLL.</span></span>
    
2. <span data-ttu-id="33a9a-109">Fügen Sie der Konfigurationsdatei MAPISVC. inf Einträge hinzu.</span><span class="sxs-lookup"><span data-stu-id="33a9a-109">Add entries to the Mapisvc.inf configuration file.</span></span> <span data-ttu-id="33a9a-110">Weitere Informationen zum Ändern dieser Datei zur Unterstützung der Dienstanbieter im Nachrichtendienst finden Sie unter [Datei Format von MapiSvc. inf](file-format-of-mapisvc-inf.md).</span><span class="sxs-lookup"><span data-stu-id="33a9a-110">For more information about how to modify this file to support the service providers in your message service, see [File Format of MapiSvc.inf](file-format-of-mapisvc-inf.md).</span></span>
    
3. <span data-ttu-id="33a9a-111">Fügen Sie der Systemregistrierung für Nachrichtendienste entsprechende Einträge hinzu.</span><span class="sxs-lookup"><span data-stu-id="33a9a-111">Add entries, as appropriate, to the system registry for message services.</span></span> <span data-ttu-id="33a9a-112">Weitere Informationen dazu, wie die Einträge in der Systemregistrierung angezeigt werden sollen, finden Sie unter [Installieren des MAPI-Subsystems](installing-the-mapi-subsystem.md).</span><span class="sxs-lookup"><span data-stu-id="33a9a-112">For more information about how the entries should appear in the system registry, see [Installing the MAPI Subsystem](installing-the-mapi-subsystem.md).</span></span>
    
4. <span data-ttu-id="33a9a-113">Erstellen Sie ein Standardprofil, wenn es noch nicht vorhanden ist, indem Sie eines der folgenden Elemente verwenden:</span><span class="sxs-lookup"><span data-stu-id="33a9a-113">Create a default profile if one does not yet exist by using one of the following items:</span></span>
    
  - <span data-ttu-id="33a9a-114">Der Profil-Assistent zum Erstellen eines Profils mithilfe von Benutzerinteraktionen über eine Reihe von Dialogfeldern.</span><span class="sxs-lookup"><span data-stu-id="33a9a-114">The Profile Wizard to create a profile by using user interaction through a series of dialog boxes.</span></span> <span data-ttu-id="33a9a-115">Weitere Informationen zur Verwendung des Profil-Assistenten finden Sie unter [Erstellen eines Profils mithilfe des Profil-Assistenten](creating-a-profile-by-using-the-profile-wizard.md).</span><span class="sxs-lookup"><span data-stu-id="33a9a-115">For more information about using the Profile Wizard, see [Creating a Profile by Using the Profile Wizard](creating-a-profile-by-using-the-profile-wizard.md).</span></span>
    
  - <span data-ttu-id="33a9a-116">Die Systemsteuerung zum Erstellen eines Profils mithilfe der Benutzerinteraktion.</span><span class="sxs-lookup"><span data-stu-id="33a9a-116">The Control Panel to create a profile by using user interaction.</span></span> <span data-ttu-id="33a9a-117">Die Systemsteuerung bietet dem Benutzer mehr Flexibilität als der Profil-Assistent zum Konfigurieren der Nachrichtendienste und zum Festlegen von Profileigenschaften.</span><span class="sxs-lookup"><span data-stu-id="33a9a-117">The Control Panel offers the user more flexibility than the Profile Wizard for configuring the message services and setting profile properties.</span></span> 
    
<span data-ttu-id="33a9a-118">Platzieren Sie das Setupprogramm in einem bestimmten öffentlichen Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="33a9a-118">Place the setup program in a designated public directory.</span></span> <span data-ttu-id="33a9a-119">Dies ist wichtig, da bei den meisten Konfigurations Clients wie der Systemsteuerung Benutzer den Namen des Verzeichnisses eingeben müssen.</span><span class="sxs-lookup"><span data-stu-id="33a9a-119">This is important because most configuration clients, such as the Control Panel, require that users enter the name of the directory.</span></span> <span data-ttu-id="33a9a-120">Die Systemsteuerung Ruft ein Setupprogramm auf, wenn ein Benutzer auf die Schaltfläche **Hinzufügen** klickt, das Dialogfeld **Datenträger** aufruft und den Pfad zum Programm angibt.</span><span class="sxs-lookup"><span data-stu-id="33a9a-120">The Control Panel invokes a setup program when a user clicks the **Add** button, invokes the **Have Disk** dialog box, and specifies the path to the program.</span></span> <span data-ttu-id="33a9a-121">Die Systemsteuerung führt das Programm aus und ruft die Einstiegspunktfunktion des Nachrichtendiensts auf, wobei der Parameter _ulContext_ auf MSG_SERVICE_INSTALL festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="33a9a-121">The Control Panel runs the program and calls your message service's entry point function with the  _ulContext_ parameter set to MSG_SERVICE_INSTALL.</span></span> 
  
> [!CAUTION]
> <span data-ttu-id="33a9a-122">Da Profile ein entbehrlicher Teil der MAPI-Architektur sind, müssen Sie sicherstellen, dass das Installationsprogramm nichts im Standardprofil speichert, das nur schwer neu erstellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="33a9a-122">Because profiles are an expendable part of the MAPI architecture, be sure that your installation program does not store anything in the default profile that would be difficult to recreate.</span></span> <span data-ttu-id="33a9a-123">Es gibt keine Dienstprogramme für die Profil Wiederherstellung, um Profile von einem Computer auf einen anderen zu übertragen, für die Offlinesicherung oder für die individuelle oder globale Wiederherstellung von Sicherungskopien.</span><span class="sxs-lookup"><span data-stu-id="33a9a-123">There are no utilities for profile recovery, for moving profiles from one computer to another, for off-line backup, or for individual or global restoration from backup copies.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="33a9a-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="33a9a-124">See also</span></span>



[<span data-ttu-id="33a9a-125">Nachrichtendienst Implementierung</span><span class="sxs-lookup"><span data-stu-id="33a9a-125">Message Service Implementation</span></span>](message-service-implementation.md)

