---
title: Implementieren einer Formularanzeige
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a567185c-bd72-4307-928c-08cac5494c1a
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: bbd0792b0e3e3f274797fabd7f5d5eb49cfc73fd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435817"
---
# <a name="implementing-a-form-viewer"></a><span data-ttu-id="ed897-103">Implementieren einer Formularanzeige</span><span class="sxs-lookup"><span data-stu-id="ed897-103">Implementing a Form Viewer</span></span>

  
  
<span data-ttu-id="ed897-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ed897-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ed897-105">Eine Formularanzeige umfasst drei Objekte: eine Nachrichtenwebsite, eine Ansichtssenke und einen Ansichtskontext.</span><span class="sxs-lookup"><span data-stu-id="ed897-105">A form viewer includes three objects: a message site, a view advise sink, and a view context.</span></span> <span data-ttu-id="ed897-106">Mit jedem dieser Objekte können Sie mit einem Formularserver und dessen Formularen interagieren.</span><span class="sxs-lookup"><span data-stu-id="ed897-106">Each of these objects allows you to interact with a form server and its forms.</span></span>
  
<span data-ttu-id="ed897-107">Eine Nachrichtenwebsite ist ein Objekt, das die [IMAPIMessageSite : IUnknown-Schnittstelle](imapimessagesiteiunknown.md) implementiert und Formularserver bei Aufgaben wie dem Verschieben, Speichern oder Löschen von Nachrichten, dem Erstellen neuer Nachrichten oder dem Starten neuer Formularserver unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ed897-107">A message site is an object that implements the [IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md) interface and assists form servers with tasks such as moving, saving, or deleting messages, creating new messages, or launching new form servers.</span></span> <span data-ttu-id="ed897-108">Nachrichtenwebsites werden von Formularen verwendet, um Informationen über den Status Ihres Clients in Bezug auf verschiedene Dienstanbieter zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="ed897-108">Message sites are used by forms to get information about your client's status with respect to various service providers.</span></span> <span data-ttu-id="ed897-109">Beispielsweise kann ein Formular Ihre Nachrichtenwebsite verwenden, um einen Zeiger auf Den aktuellen Nachrichtenspeicher, eine Nachricht oder einen Ordner zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="ed897-109">For example, a form can use your message site to get a pointer to your current message store, a message, or a folder.</span></span> 
  
<span data-ttu-id="ed897-110">Die **IMAPIMessageSite-Schnittstelle** bietet zwei Methodentypen:</span><span class="sxs-lookup"><span data-stu-id="ed897-110">There are two types of methods in the **IMAPIMessageSite** interface:</span></span> 
  
- <span data-ttu-id="ed897-111">Methoden, die Informationen zu Formularobjekten bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="ed897-111">Methods that provide information to form objects.</span></span>
    
- <span data-ttu-id="ed897-112">Methoden zum Bearbeiten von Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="ed897-112">Methods that manipulate messages.</span></span>
    
<span data-ttu-id="ed897-113">Die Methoden, die Informationen zu Formularobjekten bereitstellen, sind einfach zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="ed897-113">The methods that provide information to form objects are straightforward to implement.</span></span> <span data-ttu-id="ed897-114">In allen Fällen außer [IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md)sollten Sie bereits über die für jede Methode erforderlichen Informationen verfügen.</span><span class="sxs-lookup"><span data-stu-id="ed897-114">In all cases except [IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md), you should already have available the information required by each method.</span></span>
  
<span data-ttu-id="ed897-115">Die Methoden zum Bearbeiten von Nachrichten sollten so tun, als wären sie über Ihre reguläre Benutzeroberfläche ausgelöst worden.</span><span class="sxs-lookup"><span data-stu-id="ed897-115">The methods that manipulate messages should act as if they had been triggered through your regular user interface.</span></span> <span data-ttu-id="ed897-116">Wenn z. B. ein Formularobjekt Ihre [IMAPIMessageSite::NewMessage-Methode](imapimessagesite-newmessage.md) aufruft, verhalten Sie sich so, als hätte der Benutzer eine neue benutzerdefinierte Nachricht mit der regulären Benutzeroberfläche erstellt.</span><span class="sxs-lookup"><span data-stu-id="ed897-116">For example, if a form object calls your [IMAPIMessageSite::NewMessage](imapimessagesite-newmessage.md) method, behave as if the user had chosen to compose a new custom message with your regular user interface.</span></span> <span data-ttu-id="ed897-117">Befehle, die in der Regel dieses Verhalten generieren, sind **Compose**, **Open**, **Reply**, Reply to **All Recipients** und **Forward**.</span><span class="sxs-lookup"><span data-stu-id="ed897-117">Commands which typically generate this behavior are **Compose**, **Open**, **Reply**, **Reply to All Recipients**, and **Forward**.</span></span> 
  
<span data-ttu-id="ed897-118">Ein Ansichtskontext ist ein Objekt, das die [IMAPIViewContext : IUnknown-Schnittstelle](imapiviewcontextiunknown.md) implementiert und Formularservern einen Kontext für die aktuelle Nachricht bietet, sodass Server problemlos zur nächsten oder vorherigen Nachricht im Ordner wechseln können.</span><span class="sxs-lookup"><span data-stu-id="ed897-118">A view context is an object that implements the [IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md) interface and provides form servers with a context for the current message, allowing servers to easily switch to the next or previous message in the folder.</span></span> <span data-ttu-id="ed897-119">Ein Formular verwendet einen Ansichtskontext für die Freigabe von Informationen.</span><span class="sxs-lookup"><span data-stu-id="ed897-119">A form uses a view context for sharing information.</span></span> <span data-ttu-id="ed897-120">Mit einem Ansichtskontextobjekt kann ein Formular:</span><span class="sxs-lookup"><span data-stu-id="ed897-120">With a view context object, a form can:</span></span> 
  
- <span data-ttu-id="ed897-121">Registrieren Sie sich bei Ihrem Client für Benachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="ed897-121">Register with your client for notifications.</span></span>
    
- <span data-ttu-id="ed897-122">Aktivieren Sie die nächste oder vorherige Nachricht im Ordner.</span><span class="sxs-lookup"><span data-stu-id="ed897-122">Activate the next or previous message in the folder.</span></span>
    
- <span data-ttu-id="ed897-123">Hier finden Sie Druckinformationen.</span><span class="sxs-lookup"><span data-stu-id="ed897-123">Get printing information.</span></span>
    
- <span data-ttu-id="ed897-124">Erhalten Sie den Status Ihres Clients.</span><span class="sxs-lookup"><span data-stu-id="ed897-124">Get your client's status.</span></span>
    
- <span data-ttu-id="ed897-125">Dient zum Anzeigen eines Datenstroms, der zum Speichern der Textversion einer Nachricht verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="ed897-125">Get a stream that can be used to save the text version of a message.</span></span>
    
<span data-ttu-id="ed897-126">Ähnlich wie die Methoden in der [IMAPIMessageSite : IUnknown-Schnittstelle](imapimessagesiteiunknown.md) korrelieren die Methoden in **IMAPIViewContext** mit Benutzeraktionen und Clientfeatures, die sich auf den Ansichtskontext beziehen.</span><span class="sxs-lookup"><span data-stu-id="ed897-126">Similar to the methods in the [IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md) interface, the methods in **IMAPIViewContext** correlate with user actions and client features that relate to the view context.</span></span> <span data-ttu-id="ed897-127">Beispielsweise ist ein Ansichtskontext mit der Aktivierung der nächsten oder vorherigen Nachricht, dem Sortieren des Ordnerinhalts und dem Filtern des Ordnerinhalts beteiligt.</span><span class="sxs-lookup"><span data-stu-id="ed897-127">For example, a view context is involved with activating the next or previous message, sorting the contents of the folder, and filtering the contents of the folder.</span></span> 
  
<span data-ttu-id="ed897-128">Es ist nicht wichtig, welchen Mechanismus Sie für Benutzer bereitstellen, um diese Features zu aktivieren. Es ist nur wichtig, dass die Semantik dieser Features den Methoden in der **IMAPIViewContext-Schnittstelle** gut zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="ed897-128">It is not important what mechanism you provide for users to activate these features, it is only important that the semantics of those features map well to the methods in the **IMAPIViewContext** interface.</span></span> 
  
<span data-ttu-id="ed897-129">Eine Ansichtssenke ist ein Objekt, das die [IMAPIViewAdviseSink : IUnknown-Schnittstelle](imapiviewadvisesinkiunknown.md) implementiert und Benachrichtigungen von Formularservern verarbeitet, die sich auf Ihren Viewer auswirken und Formular- und Formularanzeigen bei der Zusammenarbeit unterstützen.</span><span class="sxs-lookup"><span data-stu-id="ed897-129">A view advise sink is an object that implements the [IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md) interface and handles notifications from form servers that affect your viewer and help forms and form viewers to work together.</span></span> <span data-ttu-id="ed897-130">Weitere Informationen finden Sie unter [Senden und Empfangen von Formularbenachrichtigungen](sending-and-receiving-form-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="ed897-130">For more information, see [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).</span></span> 
  

