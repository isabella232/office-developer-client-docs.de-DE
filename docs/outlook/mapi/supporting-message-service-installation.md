---
title: Unterstützen der Installation des Nachrichtendiensts
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
# <a name="supporting-message-service-installation"></a><span data-ttu-id="123b7-103">Unterstützen der Installation des Nachrichtendiensts</span><span class="sxs-lookup"><span data-stu-id="123b7-103">Supporting Message Service Installation</span></span>

  
  
<span data-ttu-id="123b7-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="123b7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="123b7-105">Das Setupprogramm für die Installation des Nachrichtendiensts sollte die folgenden Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="123b7-105">The setup program for installing your message service should do the following:</span></span>
  
1. <span data-ttu-id="123b7-106">Kopieren Sie Nachrichtendienstdateien, z. B. den Nachrichtendienst und die Dienstanbieter-DLLs, von einer CD oder einem Datenträger auf ein lokales Laufwerk auf der Arbeitsstation.</span><span class="sxs-lookup"><span data-stu-id="123b7-106">Copy message service files, such as the message service and service provider DLLs, from a CD or disk, to a local drive on the workstation.</span></span> <span data-ttu-id="123b7-107">Die Dateien, die kopiert werden müssen, hängen vom Nachrichtendienst ab.</span><span class="sxs-lookup"><span data-stu-id="123b7-107">The files that need to be copied depend on your message service.</span></span> <span data-ttu-id="123b7-108">In der Regel kopieren Sie mindestens eine DLL.</span><span class="sxs-lookup"><span data-stu-id="123b7-108">Typically you will copy at least one DLL.</span></span>
    
2. <span data-ttu-id="123b7-109">Fügen Sie der Konfigurationsdatei Mapisvc.inf Einträge hinzu.</span><span class="sxs-lookup"><span data-stu-id="123b7-109">Add entries to the Mapisvc.inf configuration file.</span></span> <span data-ttu-id="123b7-110">Weitere Informationen zum Ändern dieser Datei zur Unterstützung der Dienstanbieter in Ihrem Nachrichtendienst finden Sie unter [File Format of MapiSvc.inf](file-format-of-mapisvc-inf.md).</span><span class="sxs-lookup"><span data-stu-id="123b7-110">For more information about how to modify this file to support the service providers in your message service, see [File Format of MapiSvc.inf](file-format-of-mapisvc-inf.md).</span></span>
    
3. <span data-ttu-id="123b7-111">Fügen Sie der Systemregistrierung für Nachrichtendienste gegebenenfalls Einträge hinzu.</span><span class="sxs-lookup"><span data-stu-id="123b7-111">Add entries, as appropriate, to the system registry for message services.</span></span> <span data-ttu-id="123b7-112">Weitere Informationen dazu, wie die Einträge in der Systemregistrierung angezeigt werden sollen, finden Sie unter [Installing the MAPI Subsystem](installing-the-mapi-subsystem.md).</span><span class="sxs-lookup"><span data-stu-id="123b7-112">For more information about how the entries should appear in the system registry, see [Installing the MAPI Subsystem](installing-the-mapi-subsystem.md).</span></span>
    
4. <span data-ttu-id="123b7-113">Erstellen Sie ein Standardprofil, wenn eines noch nicht vorhanden ist, indem Sie eines der folgenden Elemente verwenden:</span><span class="sxs-lookup"><span data-stu-id="123b7-113">Create a default profile if one does not yet exist by using one of the following items:</span></span>
    
  - <span data-ttu-id="123b7-114">Der Profil-Assistent zum Erstellen eines Profils mithilfe der Benutzerinteraktion über eine Reihe von Dialogfelder.</span><span class="sxs-lookup"><span data-stu-id="123b7-114">The Profile Wizard to create a profile by using user interaction through a series of dialog boxes.</span></span> <span data-ttu-id="123b7-115">Weitere Informationen zur Verwendung des Profil-Assistenten finden Sie unter [Creating a Profile by Using the Profile Wizard](creating-a-profile-by-using-the-profile-wizard.md).</span><span class="sxs-lookup"><span data-stu-id="123b7-115">For more information about using the Profile Wizard, see [Creating a Profile by Using the Profile Wizard](creating-a-profile-by-using-the-profile-wizard.md).</span></span>
    
  - <span data-ttu-id="123b7-116">Die Systemsteuerung zum Erstellen eines Profils mithilfe der Benutzerinteraktion.</span><span class="sxs-lookup"><span data-stu-id="123b7-116">The Control Panel to create a profile by using user interaction.</span></span> <span data-ttu-id="123b7-117">Die Systemsteuerung bietet dem Benutzer mehr Flexibilität als der Profil-Assistent zum Konfigurieren der Nachrichtendienste und Festlegen von Profileigenschaften.</span><span class="sxs-lookup"><span data-stu-id="123b7-117">The Control Panel offers the user more flexibility than the Profile Wizard for configuring the message services and setting profile properties.</span></span> 
    
<span data-ttu-id="123b7-118">Platzieren Sie das Setupprogramm in einem festgelegten öffentlichen Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="123b7-118">Place the setup program in a designated public directory.</span></span> <span data-ttu-id="123b7-119">Dies ist wichtig, da die meisten Konfigurationsclients, z. B. die Systemsteuerung, den Namen des Verzeichnisses eingeben müssen.</span><span class="sxs-lookup"><span data-stu-id="123b7-119">This is important because most configuration clients, such as the Control Panel, require that users enter the name of the directory.</span></span> <span data-ttu-id="123b7-120">Die Systemsteuerung ruft ein Setupprogramm auf,  wenn ein Benutzer  auf die Schaltfläche Hinzufügen klickt, das Dialogfeld Datenträger haben aufruft und den Pfad zum Programm angibt.</span><span class="sxs-lookup"><span data-stu-id="123b7-120">The Control Panel invokes a setup program when a user clicks the **Add** button, invokes the **Have Disk** dialog box, and specifies the path to the program.</span></span> <span data-ttu-id="123b7-121">Die Systemsteuerung führt das Programm aus und ruft die Einstiegspunktfunktion Ihres Nachrichtendiensts auf, der  _ulContext-Parameter_ ist auf MSG_SERVICE_INSTALL.</span><span class="sxs-lookup"><span data-stu-id="123b7-121">The Control Panel runs the program and calls your message service's entry point function with the  _ulContext_ parameter set to MSG_SERVICE_INSTALL.</span></span> 
  
> [!CAUTION]
> <span data-ttu-id="123b7-122">Da Profile ein ernennbarer Bestandteil der MAPI-Architektur sind, müssen Sie sicherstellen, dass in Ihrem Installationsprogramm nichts im Standardprofil gespeichert wird, das nur schwer neu erstellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="123b7-122">Because profiles are an expendable part of the MAPI architecture, be sure that your installation program does not store anything in the default profile that would be difficult to recreate.</span></span> <span data-ttu-id="123b7-123">Es gibt keine Dienstprogramme für die Profilwiederherstellung, für das Verschieben von Profilen von einem Computer auf einen anderen, für die off-line-Sicherung oder für die individuelle oder globale Wiederherstellung von Sicherungskopien.</span><span class="sxs-lookup"><span data-stu-id="123b7-123">There are no utilities for profile recovery, for moving profiles from one computer to another, for off-line backup, or for individual or global restoration from backup copies.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="123b7-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="123b7-124">See also</span></span>



[<span data-ttu-id="123b7-125">Implementierung des Nachrichtendiensts</span><span class="sxs-lookup"><span data-stu-id="123b7-125">Message Service Implementation</span></span>](message-service-implementation.md)

