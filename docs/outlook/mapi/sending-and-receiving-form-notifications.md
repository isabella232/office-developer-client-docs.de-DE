---
title: Senden und empfangen von Formular Benachrichtigungen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a4374728-e2bc-47d9-8b03-ba09545a38d8
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 4ee47b51a98cf732f4e9af2a87fa1734a7250208
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431855"
---
# <a name="sending-and-receiving-form-notifications"></a><span data-ttu-id="63180-103">Senden und empfangen von Formular Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="63180-103">Sending and Receiving Form Notifications</span></span>

  
  
<span data-ttu-id="63180-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="63180-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="63180-105">Formular Benachrichtigungen werden in MAPI verwendet, um die Kommunikation sowohl vom Formular zum Betrachter als auch von Ihrem Betrachter zum Formular zu erleichtern.</span><span class="sxs-lookup"><span data-stu-id="63180-105">Form notifications are used in MAPI to facilitate communication both from the form to your viewer as well as from your viewer to the form.</span></span>
  
<span data-ttu-id="63180-106">Formulare senden Benachrichtigungen an den Betrachter, wenn eines der folgenden Ereignisse eintritt:</span><span class="sxs-lookup"><span data-stu-id="63180-106">Forms send notifications to your viewer when one of the following events occur:</span></span>
  
- <span data-ttu-id="63180-107">Das Formular ist geschlossen.</span><span class="sxs-lookup"><span data-stu-id="63180-107">The form is closed.</span></span>
    
- <span data-ttu-id="63180-108">Eine neue Nachricht wird in das Formular geladen.</span><span class="sxs-lookup"><span data-stu-id="63180-108">A new message is loaded in the form.</span></span>
    
- <span data-ttu-id="63180-109">Ein Speichervorgang ist abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="63180-109">A save operation is completed.</span></span>
    
- <span data-ttu-id="63180-110">Eine Nachricht wird gesendet.</span><span class="sxs-lookup"><span data-stu-id="63180-110">A message is sent.</span></span>
    
<span data-ttu-id="63180-111">Jeder dieser Ereignistypen entspricht einer bestimmten Methode in [IMAPIViewAdviseSink: IUnknown](imapiviewadvisesinkiunknown.md), eine der Schnittstellen, die der Formular Betrachter implementieren muss.</span><span class="sxs-lookup"><span data-stu-id="63180-111">Each of these event types correspond to a particular method in [IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md), one of the interfaces that your form viewer must implement.</span></span> <span data-ttu-id="63180-112">Wenn ein Ereignis auftritt, ruft das Formular die entsprechende **IMAPIViewAdviseSink** -Methode in der Advise-Senke des Viewers auf.</span><span class="sxs-lookup"><span data-stu-id="63180-112">When an event occurs, the form calls the corresponding **IMAPIViewAdviseSink** method in your viewer's advise sink.</span></span> <span data-ttu-id="63180-113">Wenn beispielsweise eine neue Nachricht eingeht, die Ihr Viewer in die Anzeige aufnehmen soll, ruft das Formular die [IMAPIViewAdviseSink:: OnNewMessage](imapiviewadvisesink-onnewmessage.md) -Methode auf.</span><span class="sxs-lookup"><span data-stu-id="63180-113">For example, when a new message arrives that your viewer should include in its display, the form calls your [IMAPIViewAdviseSink::OnNewMessage](imapiviewadvisesink-onnewmessage.md) method.</span></span> 
  
<span data-ttu-id="63180-114">Implementieren Sie Ihre Ansicht Advise-Senke auf eine Weise, die für Ihren Betrachter sinnvoll ist. Es gibt keine Standardimplementierung.</span><span class="sxs-lookup"><span data-stu-id="63180-114">Implement your view advise sink in a way that makes sense for your viewer; there is no standard implementation.</span></span> <span data-ttu-id="63180-115">In **OnNewMessage** können Sie beispielsweise die Ansicht der Inhaltstabelle des aktuellen Ordners aktualisieren, um die neu eingetroffene Nachricht einzuschließen.</span><span class="sxs-lookup"><span data-stu-id="63180-115">For example, in **OnNewMessage** you can update the view of the current folder's contents table to include the newly arrived message.</span></span> <span data-ttu-id="63180-116">In [IMAPIViewAdviseSink:: onsubmitted](imapiviewadvisesink-onsubmitted.md), die Methode, die aufgerufen wird, wenn Sie ein gesendetes Nachrichtenereignis empfangen, können Sie die übermittelte Nachricht in einen Ordner "Gesendete Elemente" kopieren.</span><span class="sxs-lookup"><span data-stu-id="63180-116">In [IMAPIViewAdviseSink::OnSubmitted](imapiviewadvisesink-onsubmitted.md), the method that is called when you receive a submitted message event, you can copy the submitted message to a Sent Items folder.</span></span>
  
<span data-ttu-id="63180-117">Formulare erhalten eine Benachrichtigung von Ihrem Betrachter, wenn eine Änderung auftritt, die sich auf das Formular auswirkt und wenn Sie eine neue Nachricht laden.</span><span class="sxs-lookup"><span data-stu-id="63180-117">Forms receive notification from your viewer when a change occurs that affects the form and when you are loading a new message.</span></span> <span data-ttu-id="63180-118">Wenn Sie ein Formular benachrichtigen möchten, rufen Sie eine der Methoden von **IMAPIFormAdviseSink**: [IMAPIFormAdviseSink:: OnChange](imapiformadvisesink-onchange.md) oder [IMAPIFormAdviseSink:: OnActivateNext](imapiformadvisesink-onactivatenext.md)auf.</span><span class="sxs-lookup"><span data-stu-id="63180-118">To notify a form, call one of the methods of **IMAPIFormAdviseSink**: [IMAPIFormAdviseSink::OnChange](imapiformadvisesink-onchange.md) or [IMAPIFormAdviseSink::OnActivateNext](imapiformadvisesink-onactivatenext.md).</span></span> <span data-ttu-id="63180-119">Rufen \*\*\*\* Sie OnChange auf, um den Status zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="63180-119">Call **OnChange** to communicate status.</span></span> <span data-ttu-id="63180-120">Wenn beispielsweise das Formular das letzte Element in einem Ordner anzeigt, wenn eine neue Nachricht eingeht, rufen \*\*\*\* Sie OnChange mit dem VCSTATUS_NEXT-Flag auf, um dem Formular mitzuteilen, dass es jetzt ein nächstes Element gibt.</span><span class="sxs-lookup"><span data-stu-id="63180-120">For example, if the form is displaying the last item in a folder when a new message arrives, call **OnChange** with the VCSTATUS_NEXT flag set to tell the form that there is now a next item.</span></span> 
  
<span data-ttu-id="63180-121">Rufen Sie **OnActivateNext** auf, um das Formular an den Eingang einer neuen Nachricht zu benachrichtigen, die möglicherweise nicht angezeigt werden kann oder nicht.</span><span class="sxs-lookup"><span data-stu-id="63180-121">Call **OnActivateNext** to alert the form to the arrival of a new message that it may or may not be able to display.</span></span> <span data-ttu-id="63180-122">Führen Sie die Nachrichtenklasse der Nachricht an **OnActivateNext**.</span><span class="sxs-lookup"><span data-stu-id="63180-122">Pass the message class of the message to **OnActivateNext**.</span></span> 
  
<span data-ttu-id="63180-123">Benachrichtigungen durch ein Form-Objekt an die Clientanwendung werden von der **IMAPIViewAdviseSink** -Schnittstelle der Clientanwendung verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="63180-123">Notifications by a form object to the client application are handled by the client application's **IMAPIViewAdviseSink** interface.</span></span> <span data-ttu-id="63180-124">Weitere Informationen finden Sie unter [IMAPIViewAdviseSink: IUnknown](imapiviewadvisesinkiunknown.md).</span><span class="sxs-lookup"><span data-stu-id="63180-124">For more information, see [IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md).</span></span>
  

