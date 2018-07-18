---
title: Unterstützen der Nachrichtendienstinstallation
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 822e07bc-0bca-4485-8938-2264315161e2
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: bf3e79ad32801a659df2c68016167d3b547ddc6f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795668"
---
# <a name="supporting-message-service-installation"></a><span data-ttu-id="504a8-103">Unterstützen der Nachrichtendienstinstallation</span><span class="sxs-lookup"><span data-stu-id="504a8-103">Supporting Message Service Installation</span></span>

  
  
<span data-ttu-id="504a8-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="504a8-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="504a8-105">Das Setup-Programm für die Installation von Ihrer Messagingdiensts sollten folgendermaßen vorgehen:</span><span class="sxs-lookup"><span data-stu-id="504a8-105">The setup program for installing your message service should do the following:</span></span>
  
1. <span data-ttu-id="504a8-106">Kopieren Sie Service Nachrichtendateien, wie die Messagingdiensts und Service Provider-DLLs, von einer CD oder Diskette, einem lokalen Laufwerk auf der Arbeitsstation.</span><span class="sxs-lookup"><span data-stu-id="504a8-106">Copy message service files, such as the message service and service provider DLLs, from a CD or disk, to a local drive on the workstation.</span></span> <span data-ttu-id="504a8-107">Die Dateien, die kopiert werden müssen, abhängig von Ihrer Messagingdiensts ab.</span><span class="sxs-lookup"><span data-stu-id="504a8-107">The files that need to be copied depend on your message service.</span></span> <span data-ttu-id="504a8-108">Kopieren Sie in der Regel mindestens eine DLL-Datei.</span><span class="sxs-lookup"><span data-stu-id="504a8-108">Typically you will copy at least one DLL.</span></span>
    
2. <span data-ttu-id="504a8-109">Die Datei "Mapisvc.inf" Konfiguration Einträge hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="504a8-109">Add entries to the Mapisvc.inf configuration file.</span></span> <span data-ttu-id="504a8-110">Weitere Informationen zum Ändern der Datei, um die-Dienstanbieter in Ihrer Messagingdiensts zu unterstützen finden Sie unter [File Format der MapiSvc.inf](file-format-of-mapisvc-inf.md).</span><span class="sxs-lookup"><span data-stu-id="504a8-110">For more information about how to modify this file to support the service providers in your message service, see [File Format of MapiSvc.inf](file-format-of-mapisvc-inf.md).</span></span>
    
3. <span data-ttu-id="504a8-111">Fügen Sie Einträge, je nach der Registrierung des Systems für die Message-Dienste.</span><span class="sxs-lookup"><span data-stu-id="504a8-111">Add entries, as appropriate, to the system registry for message services.</span></span> <span data-ttu-id="504a8-112">Weitere Informationen dazu, wie die Einträge in der Registrierung angezeigt werden soll finden Sie unter [Installieren des MAPI-Subsystems](installing-the-mapi-subsystem.md).</span><span class="sxs-lookup"><span data-stu-id="504a8-112">For more information about how the entries should appear in the system registry, see [Installing the MAPI Subsystem](installing-the-mapi-subsystem.md).</span></span>
    
4. <span data-ttu-id="504a8-113">Erstellen Sie ein Standardprofil aus, wenn eine noch nicht vorhanden ist mit einer der folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="504a8-113">Create a default profile if one does not yet exist by using one of the following items:</span></span>
    
  - <span data-ttu-id="504a8-114">Der Profil-Assistent zum Erstellen eines Profils mithilfe der Benutzerinteraktion durch eine Reihe von Dialogfeldern.</span><span class="sxs-lookup"><span data-stu-id="504a8-114">The Profile Wizard to create a profile by using user interaction through a series of dialog boxes.</span></span> <span data-ttu-id="504a8-115">Weitere Informationen zur Verwendung des Profil-Assistenten finden Sie unter [Erstellen eines Profils mithilfe der Profil-Assistent](creating-a-profile-by-using-the-profile-wizard.md).</span><span class="sxs-lookup"><span data-stu-id="504a8-115">For more information about using the Profile Wizard, see [Creating a Profile by Using the Profile Wizard](creating-a-profile-by-using-the-profile-wizard.md).</span></span>
    
  - <span data-ttu-id="504a8-116">Die Systemsteuerung zum Erstellen eines Profils mithilfe der Benutzerinteraktion.</span><span class="sxs-lookup"><span data-stu-id="504a8-116">The Control Panel to create a profile by using user interaction.</span></span> <span data-ttu-id="504a8-117">Die Systemsteuerung bietet dem Benutzer mehr Flexibilität als die-Profil-Assistent zum Konfigurieren der Nachrichtendienste und Festlegen von Profileigenschaften.</span><span class="sxs-lookup"><span data-stu-id="504a8-117">The Control Panel offers the user more flexibility than the Profile Wizard for configuring the message services and setting profile properties.</span></span> 
    
<span data-ttu-id="504a8-118">Platzieren Sie das Setup-Programm in einem öffentlichen Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="504a8-118">Place the setup program in a designated public directory.</span></span> <span data-ttu-id="504a8-119">Dies ist wichtig, da die meisten Konfiguration Clients wie beispielsweise die Systemsteuerung erfordert, dass Benutzer auf den Namen des Verzeichnisses eingeben.</span><span class="sxs-lookup"><span data-stu-id="504a8-119">This is important because most configuration clients, such as the Control Panel, require that users enter the name of the directory.</span></span> <span data-ttu-id="504a8-120">Die Systemsteuerung Ruft ein Setup-Programm aus, wenn ein Benutzer klickt auf die Schaltfläche **Hinzufügen** , das Dialogfeld **Datenträger ruft** und den Pfad zu dem Programm gibt.</span><span class="sxs-lookup"><span data-stu-id="504a8-120">The Control Panel invokes a setup program when a user clicks the **Add** button, invokes the **Have Disk** dialog box, and specifies the path to the program.</span></span> <span data-ttu-id="504a8-121">Der Systemsteuerung das Programm ausgeführt wird und Ihre Messagingdiensts Eintrag Point-Funktion aufruft, mit dem _UlContext_ -Parameter auf MSG_SERVICE_INSTALL festgelegt.</span><span class="sxs-lookup"><span data-stu-id="504a8-121">The Control Panel runs the program and calls your message service's entry point function with the  _ulContext_ parameter set to MSG_SERVICE_INSTALL.</span></span> 
  
> [!CAUTION]
> <span data-ttu-id="504a8-122">Da Profile einer geeigneten Bestandteil der MAPI-Architektur sind, werden Sie sicher, dass das Installationsprogramm nicht alles im Standardprofil speichert, die zum erneuten Erstellen schwierig wäre.</span><span class="sxs-lookup"><span data-stu-id="504a8-122">Because profiles are an expendable part of the MAPI architecture, be sure that your installation program does not store anything in the default profile that would be difficult to recreate.</span></span> <span data-ttu-id="504a8-123">Es gibt keine Dienstprogramme für die Benutzerprofildienst-Wiederherstellung, zum Verschieben von Profilen von einem Computer an eine andere, für Offline-Sicherung oder für einzelne oder globale Wiederherstellung von Sicherungskopien.</span><span class="sxs-lookup"><span data-stu-id="504a8-123">There are no utilities for profile recovery, for moving profiles from one computer to another, for off-line backup, or for individual or global restoration from backup copies.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="504a8-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="504a8-124">See also</span></span>



[<span data-ttu-id="504a8-125">Nachrichtendienstimplementierung</span><span class="sxs-lookup"><span data-stu-id="504a8-125">Message Service Implementation</span></span>](message-service-implementation.md)

