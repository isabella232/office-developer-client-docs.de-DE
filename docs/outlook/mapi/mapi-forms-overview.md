---
title: MAPI-Workflowformulare (Übersicht)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1b3afeaa-4ede-41eb-a3c1-b8947a46ef97
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 91bc0641723a92d8dc86bf3d1037d8e9936930ce
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793001"
---
# <a name="mapi-forms-overview"></a><span data-ttu-id="05ab1-103">MAPI-Workflowformulare (Übersicht)</span><span class="sxs-lookup"><span data-stu-id="05ab1-103">MAPI forms overview</span></span>
  
<span data-ttu-id="05ab1-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="05ab1-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="05ab1-105">Ein MAPI-Formular ist ein Viewer für eine Nachricht.</span><span class="sxs-lookup"><span data-stu-id="05ab1-105">A MAPI form is a viewer for a message.</span></span> <span data-ttu-id="05ab1-106">Jede Nachricht weist eine Nachrichtenklasse, die bestimmte Form durch die bestimmt, die als Viewer verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="05ab1-106">Every message has a message class that dictates the particular form that is used as its viewer.</span></span> <span data-ttu-id="05ab1-107">MAPI definiert verschiedene Nachrichtenklassen und die Formulare für die Anzeige von Nachrichten dieser Klassen wurde implementiert.</span><span class="sxs-lookup"><span data-stu-id="05ab1-107">MAPI defines several message classes and has implemented the forms for viewing messages of these classes.</span></span> <span data-ttu-id="05ab1-108">Client-Software-Entwicklern können neue Nachrichtenklassen und benutzerdefinierte Formulare für die Anzeige von Nachrichten mithilfe der neuen Klassen erstellt erstellen.</span><span class="sxs-lookup"><span data-stu-id="05ab1-108">Client software developers can create new message classes and custom forms for viewing messages created by using the new classes.</span></span>
  
<span data-ttu-id="05ab1-109">Jedes benutzerdefiniertes Formular implementiert eine Reihe von standard Menübefehle, z. B. **Open**, **Erstellen**, **Löschen**und **Antwort**, und eine Reihe von Befehlen, die auf das Formular spezifisch sind.</span><span class="sxs-lookup"><span data-stu-id="05ab1-109">Every custom form implements a set of standard menu commands, such as **Open**, **Create**, **Delete**, and **Reply**, and a set of commands that are specific to the particular form.</span></span> <span data-ttu-id="05ab1-110">Einige der Formularbefehle sind mit der Benutzeroberfläche der Client-Anwendung integriert, wenn das Formular aktiv ist. andere Formularbefehle ersetzt vollständig die Clientbefehle.</span><span class="sxs-lookup"><span data-stu-id="05ab1-110">Some of the form commands are integrated with the user interface of the client application when the form is active; other form commands completely replace the client commands.</span></span> 
  
<span data-ttu-id="05ab1-111">Die folgende Abbildung zeigt die Beziehung zwischen den MAPI-Komponenten für die Verwendung von Formularen.</span><span class="sxs-lookup"><span data-stu-id="05ab1-111">The following illustration shows the relationship between the MAPI components involved in using forms.</span></span> 
  
<span data-ttu-id="05ab1-112">**Architektur des MAPI-Formulars**</span><span class="sxs-lookup"><span data-stu-id="05ab1-112">**MAPI form architecture**</span></span>
  
<span data-ttu-id="05ab1-113">![MAPI-Formular-Architektur] (media/forms01.gif "MAPI-Formular-Architektur")</span><span class="sxs-lookup"><span data-stu-id="05ab1-113">![MAPI form architecture](media/forms01.gif "MAPI form architecture")</span></span>
  
<span data-ttu-id="05ab1-114">Beachten Sie, dass der Formular-Manager eine Rolle, die andere MAPI-Dienstanbieter ähnlich ist spielt, obwohl es keinem Dienstanbieter selbst ist, in das Diagramm.</span><span class="sxs-lookup"><span data-stu-id="05ab1-114">In the diagram, notice that the form manager plays a role that is similar to other MAPI service providers, although it is not a service provider itself.</span></span> <span data-ttu-id="05ab1-115">Der Formular-Manager ist eine austauschbare DLL, die einige MAPI-Schnittstellen implementiert.</span><span class="sxs-lookup"><span data-stu-id="05ab1-115">The form manager is a replaceable DLL that implements some of the MAPI interfaces.</span></span> <span data-ttu-id="05ab1-116">Obwohl Entwickler ihre eigenen Formular-Manager implementieren können, werden die meisten Umgebungen aufgrund der Komplexität der Formular-Manager von Microsoft bereitgestellten Formular-Manager verwenden.</span><span class="sxs-lookup"><span data-stu-id="05ab1-116">Although developers can implement their own form manager, most environments will use the form manager provided by Microsoft due to the form manager's complexity.</span></span>
  
<span data-ttu-id="05ab1-117">Die folgende Liste beschreibt die Komponenten im Diagramm und deren Beziehung zu anderen Komponenten:</span><span class="sxs-lookup"><span data-stu-id="05ab1-117">The following list describes the components in the diagram and their relationship to other components:</span></span>
  
- <span data-ttu-id="05ab1-118">Messaging-Client: eine Anwendung, die Formular-Objekte verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="05ab1-118">Messaging client: An application that can use form objects.</span></span> <span data-ttu-id="05ab1-119">Der messaging-Client verwendet die MAPI-Formular-Schnittstellen zur Kommunikation mit der Formular-Manager Nachrichten in Formularobjekte zu laden.</span><span class="sxs-lookup"><span data-stu-id="05ab1-119">The messaging client uses the MAPI form interfaces to communicate with the form manager to load messages into form objects.</span></span>
    
- <span data-ttu-id="05ab1-120">MAPI-Formulars Schnittstellen: ein definierter Standard für die Kommunikation zwischen MAPI-Komponenten, die im Zusammenhang mit Formularen.</span><span class="sxs-lookup"><span data-stu-id="05ab1-120">MAPI form interfaces: A defined standard for communication between MAPI components that are related to forms.</span></span>
    
- <span data-ttu-id="05ab1-121">Formular-Manager: der DLL, die messaging-Clients verwenden, um die Installation von Formularen in Formularbibliotheken, Laden des Formulars Servern und erste Kommunikation zwischen messaging-Clients und Servern Formular zu behandeln.</span><span class="sxs-lookup"><span data-stu-id="05ab1-121">Form manager: The DLL that messaging clients use to handle installation of forms in form libraries, loading of form servers, and initial communication between messaging clients and form servers.</span></span>
    
- <span data-ttu-id="05ab1-122">Formular Bibliotheken: permanenten Speicher für die ausführbaren Dateien Formular Server zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="05ab1-122">Form libraries: Permanent storage for the executable files associated with form servers.</span></span>
    
- <span data-ttu-id="05ab1-123">Server bilden: ausführbare Dateien, die einem Formular zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="05ab1-123">Form servers: Executable files that implement a form.</span></span> <span data-ttu-id="05ab1-124">Formular Servern Formular-Objekte und -Benutzeroberflächen für den Umgang mit bestimmter Nachrichten erstellen.</span><span class="sxs-lookup"><span data-stu-id="05ab1-124">Form servers create form objects and user interfaces to deal with specific messages.</span></span> <span data-ttu-id="05ab1-125">Diese ausführbare Datei ist auch ein OLE-Server und den üblichen OLE-Konventionen befolgt.</span><span class="sxs-lookup"><span data-stu-id="05ab1-125">This executable is also an OLE server and adheres to the usual OLE conventions.</span></span>
    
- <span data-ttu-id="05ab1-126">Objekte bilden: Laufzeitobjekte erstelltes Formular Server, die bestimmte Nachrichten entsprechen.</span><span class="sxs-lookup"><span data-stu-id="05ab1-126">Form objects: Run-time objects created by form servers that correspond to specific messages.</span></span> <span data-ttu-id="05ab1-127">Formular-Objekte werden in demselben Prozesskontext als Formular Server ausführen.</span><span class="sxs-lookup"><span data-stu-id="05ab1-127">Form objects run in the same process context as their form server.</span></span>
    
<span data-ttu-id="05ab1-128">Weitere Informationen zu MAPI-Formularkomponenten finden Sie unter [MAPI-Formulare](mapi-forms.md).</span><span class="sxs-lookup"><span data-stu-id="05ab1-128">For more information about MAPI form components, see [MAPI Forms](mapi-forms.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="05ab1-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="05ab1-129">See also</span></span>

- [<span data-ttu-id="05ab1-130">MAPI-Features und die Architektur</span><span class="sxs-lookup"><span data-stu-id="05ab1-130">MAPI Features and Architecture</span></span>](mapi-features-and-architecture.md)

