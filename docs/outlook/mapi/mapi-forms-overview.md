---
title: Übersicht über MAPI-Formulare
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1b3afeaa-4ede-41eb-a3c1-b8947a46ef97
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 4e7d48f6f6a47ce28aa0e1291ccef209b998c18e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351513"
---
# <a name="mapi-forms-overview"></a><span data-ttu-id="5dd0c-103">Übersicht über MAPI-Formulare</span><span class="sxs-lookup"><span data-stu-id="5dd0c-103">MAPI forms overview</span></span>
  
<span data-ttu-id="5dd0c-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5dd0c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5dd0c-105">Ein MAPI-Formular ist ein Viewer für eine Nachricht.</span><span class="sxs-lookup"><span data-stu-id="5dd0c-105">A MAPI form is a viewer for a message.</span></span> <span data-ttu-id="5dd0c-106">Jede Nachricht verfügt über eine Nachrichtenklasse, die das jeweilige Formular bestimmt, das als Viewer verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5dd0c-106">Every message has a message class that dictates the particular form that is used as its viewer.</span></span> <span data-ttu-id="5dd0c-107">MAPI definiert mehrere Nachrichtenklassen und hat die Formulare zum Anzeigen von Nachrichten dieser Klassen implementiert.</span><span class="sxs-lookup"><span data-stu-id="5dd0c-107">MAPI defines several message classes and has implemented the forms for viewing messages of these classes.</span></span> <span data-ttu-id="5dd0c-108">Client Softwareentwickler können neue Nachrichtenklassen und benutzerdefinierte Formulare zum Anzeigen von Nachrichten erstellen, die mithilfe der neuen Klassen erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="5dd0c-108">Client software developers can create new message classes and custom forms for viewing messages created by using the new classes.</span></span>
  
<span data-ttu-id="5dd0c-109">Jedes benutzerdefinierte Formular implementiert eine Reihe von Standardmenü Befehlen wie **Open**, **Create**, **Delete**und **Reply**sowie eine Reihe von Befehlen, die spezifisch für das jeweilige Formular sind.</span><span class="sxs-lookup"><span data-stu-id="5dd0c-109">Every custom form implements a set of standard menu commands, such as **Open**, **Create**, **Delete**, and **Reply**, and a set of commands that are specific to the particular form.</span></span> <span data-ttu-id="5dd0c-110">Einige der Formularbefehle sind in die Benutzeroberfläche der Clientanwendung integriert, wenn das Formular aktiv ist. andere Formularbefehle ersetzen die Clientbefehle vollständig.</span><span class="sxs-lookup"><span data-stu-id="5dd0c-110">Some of the form commands are integrated with the user interface of the client application when the form is active; other form commands completely replace the client commands.</span></span> 
  
<span data-ttu-id="5dd0c-111">In der folgenden Abbildung wird die Beziehung zwischen den MAPI-Komponenten dargestellt, die mit Formularen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5dd0c-111">The following illustration shows the relationship between the MAPI components involved in using forms.</span></span> 
  
<span data-ttu-id="5dd0c-112">**Architektur des MAPI-Formulars**</span><span class="sxs-lookup"><span data-stu-id="5dd0c-112">**MAPI form architecture**</span></span>
  
<span data-ttu-id="5dd0c-113">![MAPI-Formulararchitektur] (media/forms01.gif "MAPI-Formulararchitektur")</span><span class="sxs-lookup"><span data-stu-id="5dd0c-113">![MAPI form architecture](media/forms01.gif "MAPI form architecture")</span></span>
  
<span data-ttu-id="5dd0c-114">Beachten Sie im Diagramm, dass der Formular-Manager eine Rolle spielt, die anderen MAPI-Dienstanbietern ähnelt, obwohl es sich nicht um einen Dienstanbieter handelt.</span><span class="sxs-lookup"><span data-stu-id="5dd0c-114">In the diagram, notice that the form manager plays a role that is similar to other MAPI service providers, although it is not a service provider itself.</span></span> <span data-ttu-id="5dd0c-115">Der Formular-Manager ist eine austauschbare DLL, die einige der MAPI-Schnittstellen implementiert.</span><span class="sxs-lookup"><span data-stu-id="5dd0c-115">The form manager is a replaceable DLL that implements some of the MAPI interfaces.</span></span> <span data-ttu-id="5dd0c-116">Obwohl Entwickler ihren eigenen Formular-Manager implementieren können, verwenden die meisten Umgebungen den von Microsoft bereitgestellten Formular-Manager aufgrund der Komplexität des Formular-Managers.</span><span class="sxs-lookup"><span data-stu-id="5dd0c-116">Although developers can implement their own form manager, most environments will use the form manager provided by Microsoft due to the form manager's complexity.</span></span>
  
<span data-ttu-id="5dd0c-117">In der folgenden Liste werden die Komponenten im Diagramm und ihre Beziehung zu anderen Komponenten beschrieben:</span><span class="sxs-lookup"><span data-stu-id="5dd0c-117">The following list describes the components in the diagram and their relationship to other components:</span></span>
  
- <span data-ttu-id="5dd0c-118">Messaging Client: eine Anwendung, die Formularobjekte verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="5dd0c-118">Messaging client: An application that can use form objects.</span></span> <span data-ttu-id="5dd0c-119">Der Messaging Client verwendet die MAPI-Formular Schnittstellen für die Kommunikation mit dem Formular-Manager, um Nachrichten in Formularobjekte zu laden.</span><span class="sxs-lookup"><span data-stu-id="5dd0c-119">The messaging client uses the MAPI form interfaces to communicate with the form manager to load messages into form objects.</span></span>
    
- <span data-ttu-id="5dd0c-120">MAPI-Formular Schnittstellen: ein definierter Standard für die Kommunikation zwischen MAPI-Komponenten, die sich auf Formulare beziehen.</span><span class="sxs-lookup"><span data-stu-id="5dd0c-120">MAPI form interfaces: A defined standard for communication between MAPI components that are related to forms.</span></span>
    
- <span data-ttu-id="5dd0c-121">Formular-Manager: die DLL, die Messaging-Clients verwenden, um die Installation von Formularen in Formularbibliotheken, das Laden von Formular Servern und die anfängliche Kommunikation zwischen Messagingclients und Formular Servern zu behandeln.</span><span class="sxs-lookup"><span data-stu-id="5dd0c-121">Form manager: The DLL that messaging clients use to handle installation of forms in form libraries, loading of form servers, and initial communication between messaging clients and form servers.</span></span>
    
- <span data-ttu-id="5dd0c-122">Formularbibliotheken: permanenter Speicher für die den Formular Servern zugeordneten ausführbaren Dateien.</span><span class="sxs-lookup"><span data-stu-id="5dd0c-122">Form libraries: Permanent storage for the executable files associated with form servers.</span></span>
    
- <span data-ttu-id="5dd0c-123">Formularserver: ausführbare Dateien, die ein Formular implementieren.</span><span class="sxs-lookup"><span data-stu-id="5dd0c-123">Form servers: Executable files that implement a form.</span></span> <span data-ttu-id="5dd0c-124">Formularserver erstellen Formularobjekte und Benutzeroberflächen für die Behandlung bestimmter Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="5dd0c-124">Form servers create form objects and user interfaces to deal with specific messages.</span></span> <span data-ttu-id="5dd0c-125">Diese ausführbare Datei ist auch ein OLE-Server und entspricht den üblichen OLE-Konventionen.</span><span class="sxs-lookup"><span data-stu-id="5dd0c-125">This executable is also an OLE server and adheres to the usual OLE conventions.</span></span>
    
- <span data-ttu-id="5dd0c-126">Formularobjekte: von Formular Servern erstellte Laufzeitobjekte, die bestimmten Nachrichten entsprechen.</span><span class="sxs-lookup"><span data-stu-id="5dd0c-126">Form objects: Run-time objects created by form servers that correspond to specific messages.</span></span> <span data-ttu-id="5dd0c-127">Formularobjekte werden im gleichen Prozesskontext wie der Formularserver ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5dd0c-127">Form objects run in the same process context as their form server.</span></span>
    
<span data-ttu-id="5dd0c-128">Weitere Informationen zu MAPI-Formularkomponenten finden Sie unter [MAPI Forms](mapi-forms.md).</span><span class="sxs-lookup"><span data-stu-id="5dd0c-128">For more information about MAPI form components, see [MAPI Forms](mapi-forms.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="5dd0c-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5dd0c-129">See also</span></span>

- [<span data-ttu-id="5dd0c-130">MAPI-Features und -Architektur</span><span class="sxs-lookup"><span data-stu-id="5dd0c-130">MAPI Features and Architecture</span></span>](mapi-features-and-architecture.md)

