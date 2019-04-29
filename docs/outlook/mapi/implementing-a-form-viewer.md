---
title: Implementieren eines Formular-Viewers
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
# <a name="implementing-a-form-viewer"></a><span data-ttu-id="2c7a9-103">Implementieren eines Formular-Viewers</span><span class="sxs-lookup"><span data-stu-id="2c7a9-103">Implementing a Form Viewer</span></span>

  
  
<span data-ttu-id="2c7a9-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2c7a9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2c7a9-105">Ein Formular Betrachter umfasst drei Objekte: eine Nachrichtenwebsite, eine Ansicht Advise-Senke und einen Ansichtskontext.</span><span class="sxs-lookup"><span data-stu-id="2c7a9-105">A form viewer includes three objects: a message site, a view advise sink, and a view context.</span></span> <span data-ttu-id="2c7a9-106">Jedes dieser Objekte ermöglicht die Interaktion mit einem Formularserver und seinen Formularen.</span><span class="sxs-lookup"><span data-stu-id="2c7a9-106">Each of these objects allows you to interact with a form server and its forms.</span></span>
  
<span data-ttu-id="2c7a9-107">Bei einer Nachrichtenwebsite handelt es sich um ein Objekt, das die [IMAPIMessageSite: IUnknown](imapimessagesiteiunknown.md) -Schnittstelle implementiert und Formularserver bei Aufgaben wie dem bewegen, speichern oder Löschen von Nachrichten, beim Erstellen neuer Nachrichten oder beim Starten neuer Formularserver unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2c7a9-107">A message site is an object that implements the [IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md) interface and assists form servers with tasks such as moving, saving, or deleting messages, creating new messages, or launching new form servers.</span></span> <span data-ttu-id="2c7a9-108">Nachrichtenwebsites werden von Formularen verwendet, um Informationen zum Status des Clients in Bezug auf verschiedene Dienstanbieter abzurufen.</span><span class="sxs-lookup"><span data-stu-id="2c7a9-108">Message sites are used by forms to get information about your client's status with respect to various service providers.</span></span> <span data-ttu-id="2c7a9-109">Ein Formular kann beispielsweise Ihre Nachrichtenwebsite verwenden, um einen Zeiger auf den aktuellen Nachrichtenspeicher, eine Nachricht oder einen Ordner zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="2c7a9-109">For example, a form can use your message site to get a pointer to your current message store, a message, or a folder.</span></span> 
  
<span data-ttu-id="2c7a9-110">Es gibt zwei Arten von Methoden in der **IMAPIMessageSite** -Schnittstelle:</span><span class="sxs-lookup"><span data-stu-id="2c7a9-110">There are two types of methods in the **IMAPIMessageSite** interface:</span></span> 
  
- <span data-ttu-id="2c7a9-111">Methoden, die Informationen für Formularobjekte bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="2c7a9-111">Methods that provide information to form objects.</span></span>
    
- <span data-ttu-id="2c7a9-112">Methoden zum Bearbeiten von Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="2c7a9-112">Methods that manipulate messages.</span></span>
    
<span data-ttu-id="2c7a9-113">Die Methoden, die Informationen für Formularobjekte bereitstellen, sind einfach zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="2c7a9-113">The methods that provide information to form objects are straightforward to implement.</span></span> <span data-ttu-id="2c7a9-114">In allen Fällen, außer [IMAPIMessageSite:: GetSiteStatus](imapimessagesite-getsitestatus.md), sollten die für jede Methode erforderlichen Informationen bereits verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="2c7a9-114">In all cases except [IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md), you should already have available the information required by each method.</span></span>
  
<span data-ttu-id="2c7a9-115">Die Methoden zum Bearbeiten von Nachrichten sollten so agieren, als ob Sie über Ihre reguläre Benutzeroberfläche ausgelöst wurden.</span><span class="sxs-lookup"><span data-stu-id="2c7a9-115">The methods that manipulate messages should act as if they had been triggered through your regular user interface.</span></span> <span data-ttu-id="2c7a9-116">Wenn beispielsweise ein Form-Objekt ihre [IMAPIMessageSite:: PostMessage](imapimessagesite-newmessage.md) -Methode aufruft, Verhalten Sie sich, als ob der Benutzer eine neue benutzerdefinierte Nachricht mit ihrer regulären Benutzeroberfläche erstellt hätte.</span><span class="sxs-lookup"><span data-stu-id="2c7a9-116">For example, if a form object calls your [IMAPIMessageSite::NewMessage](imapimessagesite-newmessage.md) method, behave as if the user had chosen to compose a new custom message with your regular user interface.</span></span> <span data-ttu-id="2c7a9-117">Befehle, die dieses Verhalten in der \*\*\*\* Regel generieren, sind verfassen, **Öffnen**, **Antworten**, **allen Empfängern antworten**und **weiterleiten**.</span><span class="sxs-lookup"><span data-stu-id="2c7a9-117">Commands which typically generate this behavior are **Compose**, **Open**, **Reply**, **Reply to All Recipients**, and **Forward**.</span></span> 
  
<span data-ttu-id="2c7a9-118">Ein Ansichtskontext ist ein Objekt, das die [IMAPIViewContext: IUnknown](imapiviewcontextiunknown.md) -Schnittstelle implementiert und Formularserver mit einem Kontext für die aktuelle Nachricht bereitstellt, sodass Server problemlos zur nächsten oder vorherigen Nachricht im Ordner wechseln können.</span><span class="sxs-lookup"><span data-stu-id="2c7a9-118">A view context is an object that implements the [IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md) interface and provides form servers with a context for the current message, allowing servers to easily switch to the next or previous message in the folder.</span></span> <span data-ttu-id="2c7a9-119">Ein Formular verwendet einen Ansichtskontext für die Freigabe von Informationen.</span><span class="sxs-lookup"><span data-stu-id="2c7a9-119">A form uses a view context for sharing information.</span></span> <span data-ttu-id="2c7a9-120">Bei einem View-Kontextobjekt kann ein Formular Folgendes:</span><span class="sxs-lookup"><span data-stu-id="2c7a9-120">With a view context object, a form can:</span></span> 
  
- <span data-ttu-id="2c7a9-121">Registrieren Sie sich bei Ihrem Client für Benachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="2c7a9-121">Register with your client for notifications.</span></span>
    
- <span data-ttu-id="2c7a9-122">Die nächste oder vorherige Nachricht im Ordner aktivieren.</span><span class="sxs-lookup"><span data-stu-id="2c7a9-122">Activate the next or previous message in the folder.</span></span>
    
- <span data-ttu-id="2c7a9-123">Druckinformationen abrufen.</span><span class="sxs-lookup"><span data-stu-id="2c7a9-123">Get printing information.</span></span>
    
- <span data-ttu-id="2c7a9-124">Rufen Sie den Status Ihres Clients ab.</span><span class="sxs-lookup"><span data-stu-id="2c7a9-124">Get your client's status.</span></span>
    
- <span data-ttu-id="2c7a9-125">Dient zum Abrufen eines Streams, der zum Speichern der Textversion einer Nachricht verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="2c7a9-125">Get a stream that can be used to save the text version of a message.</span></span>
    
<span data-ttu-id="2c7a9-126">Ähnlich wie bei den Methoden in der [IMAPIMessageSite: IUnknown](imapimessagesiteiunknown.md) -Schnittstelle korrelieren die Methoden in **IMAPIViewContext** mit Benutzeraktionen und Clientfeatures, die sich auf den Ansichtskontext beziehen.</span><span class="sxs-lookup"><span data-stu-id="2c7a9-126">Similar to the methods in the [IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md) interface, the methods in **IMAPIViewContext** correlate with user actions and client features that relate to the view context.</span></span> <span data-ttu-id="2c7a9-127">Beispielsweise ist ein Ansichtskontext an der Aktivierung der nächsten oder der vorherigen Nachricht beteiligt, wobei der Inhalt des Ordners sortiert und der Inhalt des Ordners gefiltert wird.</span><span class="sxs-lookup"><span data-stu-id="2c7a9-127">For example, a view context is involved with activating the next or previous message, sorting the contents of the folder, and filtering the contents of the folder.</span></span> 
  
<span data-ttu-id="2c7a9-128">Es ist nicht wichtig, welchen Mechanismus Sie Benutzern zur Aktivierung dieser Funktionen zur Verfügung stellen, es ist nur wichtig, dass die Semantik dieser Features den Methoden in der **IMAPIViewContext** -Schnittstelle gut zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="2c7a9-128">It is not important what mechanism you provide for users to activate these features, it is only important that the semantics of those features map well to the methods in the **IMAPIViewContext** interface.</span></span> 
  
<span data-ttu-id="2c7a9-129">Eine View Advise-Senke ist ein Objekt, das die [IMAPIViewAdviseSink: IUnknown](imapiviewadvisesinkiunknown.md) -Schnittstelle implementiert und Benachrichtigungen von Formular Servern verarbeitet, die sich auf den Betrachter auswirken, und Formulare und Formular Betrachter bei der Zusammenarbeit unterstützen.</span><span class="sxs-lookup"><span data-stu-id="2c7a9-129">A view advise sink is an object that implements the [IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md) interface and handles notifications from form servers that affect your viewer and help forms and form viewers to work together.</span></span> <span data-ttu-id="2c7a9-130">Weitere Informationen finden Sie unter [senden und empfangen von Formular Benachrichtigungen](sending-and-receiving-form-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="2c7a9-130">For more information, see [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).</span></span> 
  

