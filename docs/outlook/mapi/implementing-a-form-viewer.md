---
title: Implementieren eines Formular-Viewers
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a567185c-bd72-4307-928c-08cac5494c1a
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 645f98342b4b3ec2bebf3f233f719bd5cae69da9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792528"
---
# <a name="implementing-a-form-viewer"></a><span data-ttu-id="c0e45-103">Implementieren eines Formular-Viewers</span><span class="sxs-lookup"><span data-stu-id="c0e45-103">Implementing a Form Viewer</span></span>

  
  
<span data-ttu-id="c0e45-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c0e45-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c0e45-105">Ein Formular Viewer umfasst drei Objekte: eine Nachricht-Website eine Ansicht advise-Empfänger, und ein Ansichtskontext.</span><span class="sxs-lookup"><span data-stu-id="c0e45-105">A form viewer includes three objects: a message site, a view advise sink, and a view context.</span></span> <span data-ttu-id="c0e45-106">Jedes dieser Objekte können Sie mit einem Formular Server und den Formularen interagieren.</span><span class="sxs-lookup"><span data-stu-id="c0e45-106">Each of these objects allows you to interact with a form server and its forms.</span></span>
  
<span data-ttu-id="c0e45-107">Eine Website für die Nachricht wird ein Objekt, das implementiert die [IMAPIMessageSite: IUnknown](imapimessagesiteiunknown.md) -Schnittstelle und hilft beim Formular Servern mit Aufgaben wie das Verschieben, speichern, oder Löschen von Nachrichten, Erstellen von neuen Nachrichten oder neuen Formular Servern starten.</span><span class="sxs-lookup"><span data-stu-id="c0e45-107">A message site is an object that implements the [IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md) interface and assists form servers with tasks such as moving, saving, or deleting messages, creating new messages, or launching new form servers.</span></span> <span data-ttu-id="c0e45-108">Nachricht Websites werden durch Formulare zum Abrufen von Informationen zu Ihrer Client-Status in Bezug auf verschiedenen-Dienstanbieter verwendet.</span><span class="sxs-lookup"><span data-stu-id="c0e45-108">Message sites are used by forms to get information about your client's status with respect to various service providers.</span></span> <span data-ttu-id="c0e45-109">Angenommen, können ein Formular Ihrer Website Nachricht Sie einen Zeiger auf den aktuellen Nachrichtenspeicher, eine Nachricht oder einen Ordner abzurufen.</span><span class="sxs-lookup"><span data-stu-id="c0e45-109">For example, a form can use your message site to get a pointer to your current message store, a message, or a folder.</span></span> 
  
<span data-ttu-id="c0e45-110">Es gibt zwei Arten von Methoden in der **IMAPIMessageSite** -Schnittstelle:</span><span class="sxs-lookup"><span data-stu-id="c0e45-110">There are two types of methods in the **IMAPIMessageSite** interface:</span></span> 
  
- <span data-ttu-id="c0e45-111">Methoden, die Informationen für Formularobjekte enthalten.</span><span class="sxs-lookup"><span data-stu-id="c0e45-111">Methods that provide information to form objects.</span></span>
    
- <span data-ttu-id="c0e45-112">Methoden, die Nachrichten zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="c0e45-112">Methods that manipulate messages.</span></span>
    
<span data-ttu-id="c0e45-113">Die Methoden, die Informationen für Formularobjekte enthalten sind einfach implementieren.</span><span class="sxs-lookup"><span data-stu-id="c0e45-113">The methods that provide information to form objects are straightforward to implement.</span></span> <span data-ttu-id="c0e45-114">In allen Fällen außer [IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md)sollte bereits Ihnen zur Verfügung stehen die Informationen, die von jeder Methode erforderlich.</span><span class="sxs-lookup"><span data-stu-id="c0e45-114">In all cases except [IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md), you should already have available the information required by each method.</span></span>
  
<span data-ttu-id="c0e45-115">Die Methoden, die Nachrichten bearbeiten sollte fungieren, als ob sie über die normale Benutzeroberfläche ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="c0e45-115">The methods that manipulate messages should act as if they had been triggered through your regular user interface.</span></span> <span data-ttu-id="c0e45-116">Beispielsweise, wenn ein Form-Objekt die [IMAPIMessageSite::NewMessage](imapimessagesite-newmessage.md) -Methode aufruft, Verhalten Sie, als ob der Benutzer sich, zum Erstellen einer neuen benutzerdefinierten Nachricht mit der normale Benutzeroberfläche entschieden hat.</span><span class="sxs-lookup"><span data-stu-id="c0e45-116">For example, if a form object calls your [IMAPIMessageSite::NewMessage](imapimessagesite-newmessage.md) method, behave as if the user had chosen to compose a new custom message with your regular user interface.</span></span> <span data-ttu-id="c0e45-117">Befehle, die dieses Verhalten in der Regel generieren sind **zum Verfassen**, **Öffnen**, **Antworten**, **Antwort an alle Empfänger**und **Weiterleiten**.</span><span class="sxs-lookup"><span data-stu-id="c0e45-117">Commands which typically generate this behavior are **Compose**, **Open**, **Reply**, **Reply to All Recipients**, and **Forward**.</span></span> 
  
<span data-ttu-id="c0e45-118">Ein Ansichtskontext ist ein Objekt, das implementiert die [IMAPIViewContext: IUnknown](imapiviewcontextiunknown.md) -Schnittstelle und bietet Formular Servern mit einem Kontext für die aktuelle Nachricht, Servern und einfach zu der nächsten oder der vorherigen Nachricht im Ordner wechseln.</span><span class="sxs-lookup"><span data-stu-id="c0e45-118">A view context is an object that implements the [IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md) interface and provides form servers with a context for the current message, allowing servers to easily switch to the next or previous message in the folder.</span></span> <span data-ttu-id="c0e45-119">Ein Formular verwendet ein Ansichtskontext für die Freigabe von Informationen.</span><span class="sxs-lookup"><span data-stu-id="c0e45-119">A form uses a view context for sharing information.</span></span> <span data-ttu-id="c0e45-120">Mit einer Ansicht Context-Objekt können ein Formular:</span><span class="sxs-lookup"><span data-stu-id="c0e45-120">With a view context object, a form can:</span></span> 
  
- <span data-ttu-id="c0e45-121">Registrieren Sie Ihre Client für Benachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="c0e45-121">Register with your client for notifications.</span></span>
    
- <span data-ttu-id="c0e45-122">Aktivieren der nächsten oder der vorherigen Nachricht im Ordner.</span><span class="sxs-lookup"><span data-stu-id="c0e45-122">Activate the next or previous message in the folder.</span></span>
    
- <span data-ttu-id="c0e45-123">Möchten Sie Drucken von Informationen erhalten.</span><span class="sxs-lookup"><span data-stu-id="c0e45-123">Get printing information.</span></span>
    
- <span data-ttu-id="c0e45-124">Abrufen des Status des Clients.</span><span class="sxs-lookup"><span data-stu-id="c0e45-124">Get your client's status.</span></span>
    
- <span data-ttu-id="c0e45-125">Rufen Sie einen Datenstrom, der zum Speichern der Textversion einer Nachricht verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="c0e45-125">Get a stream that can be used to save the text version of a message.</span></span>
    
<span data-ttu-id="c0e45-126">Ähnlich wie die Methoden in der [IMAPIMessageSite: IUnknown](imapimessagesiteiunknown.md) -Schnittstelle, die Methoden in **IMAPIViewContext** Korrelation mit Benutzeraktionen und Clientfeatures, die mit dem Ansichtskontext verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="c0e45-126">Similar to the methods in the [IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md) interface, the methods in **IMAPIViewContext** correlate with user actions and client features that relate to the view context.</span></span> <span data-ttu-id="c0e45-127">Beispielsweise ist ein Ansichtskontext beteiligt, mit die nächste oder der vorherige Nachricht aktivieren, den Inhalt des Ordners sortieren und Filtern von den Inhalt des Ordners.</span><span class="sxs-lookup"><span data-stu-id="c0e45-127">For example, a view context is involved with activating the next or previous message, sorting the contents of the folder, and filtering the contents of the folder.</span></span> 
  
<span data-ttu-id="c0e45-128">Es ist nicht wichtig sind, welche Mechanismus, die Sie für Benutzer bereitstellen, um diese Features zu aktivieren, es ist nur wichtig, dass die Semantik dieser Features sowie die Methoden in der **IMAPIViewContext** -Schnittstelle zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="c0e45-128">It is not important what mechanism you provide for users to activate these features, it is only important that the semantics of those features map well to the methods in the **IMAPIViewContext** interface.</span></span> 
  
<span data-ttu-id="c0e45-129">Eine Ansicht advise-Empfänger ist ein Objekt, das implementiert die [IMAPIViewAdviseSink: IUnknown](imapiviewadvisesinkiunknown.md) -Schnittstelle und Handles Benachrichtigungen von Formular-Servern, die Einfluss auf Viewer und Hilfe-Formularen und Formular Viewer zusammenarbeiten.</span><span class="sxs-lookup"><span data-stu-id="c0e45-129">A view advise sink is an object that implements the [IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md) interface and handles notifications from form servers that affect your viewer and help forms and form viewers to work together.</span></span> <span data-ttu-id="c0e45-130">Weitere Informationen finden Sie unter [Senden und Empfangen von Formular Benachrichtigungen](sending-and-receiving-form-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="c0e45-130">For more information, see [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).</span></span> 
  

