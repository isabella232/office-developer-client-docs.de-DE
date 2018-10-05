---
title: Integrieren von MAPI-Formularservercode mit Windows-Code
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 47ec3e97-ad2b-43ea-842a-b2a0675eef48
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 33b205c0ac5caf5fc049a0732cd219aa2c321326
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397863"
---
# <a name="integrating-mapi-form-server-code-with-windows-code"></a><span data-ttu-id="cff32-103">Integrieren von MAPI-Formularservercode mit Windows-Code</span><span class="sxs-lookup"><span data-stu-id="cff32-103">Integrating MAPI Form Server Code with Windows Code</span></span>

  
  
<span data-ttu-id="cff32-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cff32-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cff32-105">Denken Sie daran, dass Ihr Formular Server eine Win32-Anwendung ist.</span><span class="sxs-lookup"><span data-stu-id="cff32-105">Recall that your form server is a Win32 application.</span></span> <span data-ttu-id="cff32-106">Es sind einige Aufgaben im Zusammenhang mit Ihrem Formular Server in den Arbeitsspeicher geladen und ordnungsgemäß beendet.</span><span class="sxs-lookup"><span data-stu-id="cff32-106">As such, there are some tasks related to loading your form server into memory and exiting cleanly.</span></span> <span data-ttu-id="cff32-107">Wie alle Windows-Anwendungen ist der Einstiegspunkt für Ihren Server Formular **WinMain** -Funktion.</span><span class="sxs-lookup"><span data-stu-id="cff32-107">Like all Windows applications, the entry point for your form server is the **WinMain** function.</span></span> <span data-ttu-id="cff32-108">Diese Funktion ist der entsprechenden Stelle die folgenden Aufgaben ausführen:</span><span class="sxs-lookup"><span data-stu-id="cff32-108">This function is the appropriate place to perform the following tasks:</span></span> 
  
- <span data-ttu-id="cff32-109">Erstellen und Registrieren einer Fensterklasse, damit Ihr Formular Server mit anderen OLE-Komponenten interagieren kann.</span><span class="sxs-lookup"><span data-stu-id="cff32-109">Creating and registering a window class so that your form server can interact with other OLE components.</span></span>
    
- <span data-ttu-id="cff32-110">Erstellen und Registrieren einer Fensterklasse oder Klassen für Ihr Formular-Objekte von Benutzeroberflächen.</span><span class="sxs-lookup"><span data-stu-id="cff32-110">Creating and registering a window class or classes for your form objects' user interfaces.</span></span>
    
- <span data-ttu-id="cff32-111">Aufrufen der Funktion ["MAPIInitialize"](mapiinitialize.md) .</span><span class="sxs-lookup"><span data-stu-id="cff32-111">Calling the [MAPIInitialize](mapiinitialize.md) function.</span></span> <span data-ttu-id="cff32-112">**"MAPIInitialize"** verarbeitet die erforderliche OLE Initialisierung für Sie ebenfalls.</span><span class="sxs-lookup"><span data-stu-id="cff32-112">**MAPIInitialize** handles the required OLE initialization for you, as well.</span></span> <span data-ttu-id="cff32-113">Dies muss einmal pro Instanz des Servers Formular erfolgen.</span><span class="sxs-lookup"><span data-stu-id="cff32-113">This must be done once per instance of your form server.</span></span> 
    
- <span data-ttu-id="cff32-114">Registrieren eine globale Atom mit zeichenfolgendendarstellung des dem Formular Server Klassen-ID (CLSID).</span><span class="sxs-lookup"><span data-stu-id="cff32-114">Registering a global atom with a string representation of the form server's class identifier (CLSID).</span></span> <span data-ttu-id="cff32-115">Diese Atom sollte für die Lebensdauer des dem Formular Server vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="cff32-115">This atom should exist for the lifetime of the form server.</span></span>
    
- <span data-ttu-id="cff32-116">Aufrufen der OLE-Funktion [CoRegisterClassObject](https://msdn.microsoft.com/library/ms693407.aspx) Ihr Formular Konferenzserver Klasse mit OLE registriert.</span><span class="sxs-lookup"><span data-stu-id="cff32-116">Calling the OLE function [CoRegisterClassObject](https://msdn.microsoft.com/library/ms693407.aspx) to register your form server's class factory with OLE.</span></span> 
    
- <span data-ttu-id="cff32-117">Erstellen ein Hauptfenster Empfang von Nachrichten an.</span><span class="sxs-lookup"><span data-stu-id="cff32-117">Creating a main window to receive messages.</span></span> <span data-ttu-id="cff32-118">In diesem Fenster muss wahrscheinlich nicht sichtbar sein, da die spezifischen Fenster einzelne Formularobjekten zugeordnet der Benutzer interagiert werden.</span><span class="sxs-lookup"><span data-stu-id="cff32-118">This window probably does not need to be visible because the user will be interacting with the specific windows associated with individual form objects.</span></span> <span data-ttu-id="cff32-119">Klicken Sie im Hauptfenster während der Entwicklung, kann jedoch eine bequeme Möglichkeit für das debugging Ausgabe oder Kontrolle über Ihre Server Formular sein.</span><span class="sxs-lookup"><span data-stu-id="cff32-119">However, during development, the main window can be a convenient place for debugging output or control of your form server.</span></span>
    
- <span data-ttu-id="cff32-120">Erstellen eine Nachrichtenschleife, die für die Lebensdauer des Servers Formular ausgeführt wird, übersetzen und Verteilung von Windows-Nachrichten zum aktiven Formular-Objekte.</span><span class="sxs-lookup"><span data-stu-id="cff32-120">Creating a message loop that runs for the lifetime of the form server, translating and dispatching windows messages to active form objects.</span></span>
    
<span data-ttu-id="cff32-121">Wenn Ihr Formular Server beendet wird, sollten sie die folgenden Aufgaben ausführen:</span><span class="sxs-lookup"><span data-stu-id="cff32-121">When your form server exits, it should perform the following tasks:</span></span>
  
- <span data-ttu-id="cff32-122">Rufen Sie die OLE-Funktion [CoRevokeClassObject für die Abmeldung](https://msdn.microsoft.com/library/ms688650%28VS.85%29.aspx) der Nachrichtenklasse OLE-Registrierung widerrufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="cff32-122">Call the OLE function [CoRevokeClassObject](https://msdn.microsoft.com/library/ms688650%28VS.85%29.aspx) to revoke your message class's OLE registration.</span></span> 
    
- <span data-ttu-id="cff32-123">Rufen Sie **MAPIUninitialize** , um den Formular-Server-Verbindung MAPI ordnungsgemäß zu schließen.</span><span class="sxs-lookup"><span data-stu-id="cff32-123">Call **MAPIUninitialize** to properly close the form server's connection to MAPI.</span></span> 
    
- <span data-ttu-id="cff32-124">Löschen Sie das globale Atom, das die Zeichenfolgendarstellung der Klassenbezeichner enthält.</span><span class="sxs-lookup"><span data-stu-id="cff32-124">Delete the global atom that contains the string representation of the class identifier.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="cff32-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cff32-125">See also</span></span>



[<span data-ttu-id="cff32-126">Schreiben von Formularservercode</span><span class="sxs-lookup"><span data-stu-id="cff32-126">Writing Form Server Code</span></span>](writing-form-server-code.md)

