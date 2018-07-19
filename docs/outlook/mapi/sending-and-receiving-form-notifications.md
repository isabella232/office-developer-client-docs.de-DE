---
title: Senden und Empfangen von Formularbenachrichtigungen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a4374728-e2bc-47d9-8b03-ba09545a38d8
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 4730fb04d530fce516fe1ca4fd572c58fc1f1ffa
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795483"
---
# <a name="sending-and-receiving-form-notifications"></a><span data-ttu-id="f517d-103">Senden und Empfangen von Formularbenachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="f517d-103">Sending and Receiving Form Notifications</span></span>

  
  
<span data-ttu-id="f517d-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f517d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f517d-105">Formular Benachrichtigungen werden in MAPI verwendet, um Kommunikation sowohl aus dem Formular an die Anzeige sowie aus Ihrer Viewer auf das Formular zu vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="f517d-105">Form notifications are used in MAPI to facilitate communication both from the form to your viewer as well as from your viewer to the form.</span></span>
  
<span data-ttu-id="f517d-106">Formulare senden Benachrichtigungen für Ihre Betrachter, wenn eines der folgenden Ereignisse auftreten:</span><span class="sxs-lookup"><span data-stu-id="f517d-106">Forms send notifications to your viewer when one of the following events occur:</span></span>
  
- <span data-ttu-id="f517d-107">Das Formular geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="f517d-107">The form is closed.</span></span>
    
- <span data-ttu-id="f517d-108">Eine neue Nachricht wird in das Formular geladen.</span><span class="sxs-lookup"><span data-stu-id="f517d-108">A new message is loaded in the form.</span></span>
    
- <span data-ttu-id="f517d-109">Ein Speichervorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="f517d-109">A save operation is completed.</span></span>
    
- <span data-ttu-id="f517d-110">Eine Nachricht wird gesendet.</span><span class="sxs-lookup"><span data-stu-id="f517d-110">A message is sent.</span></span>
    
<span data-ttu-id="f517d-111">Jede dieser Ereignistypen in eine bestimmte Methode entspricht [IMAPIViewAdviseSink: IUnknown](imapiviewadvisesinkiunknown.md), eine der Schnittstellen, die Ihr Formular Viewer implementiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="f517d-111">Each of these event types correspond to a particular method in [IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md), one of the interfaces that your form viewer must implement.</span></span> <span data-ttu-id="f517d-112">Bei Auftreten eines Ereignisses, das Formular Anrufe in der Warteschlangenanzeige die entsprechende **IMAPIViewAdviseSink** -Methode des advise-Empfänger.</span><span class="sxs-lookup"><span data-stu-id="f517d-112">When an event occurs, the form calls the corresponding **IMAPIViewAdviseSink** method in your viewer's advise sink.</span></span> <span data-ttu-id="f517d-113">Beispielsweise beim Eintreffen einer neuen Nachricht, dass Ihre Viewer in seiner Darstellung aufgenommen werden sollen, ruft das Formular zu Ihrer [IMAPIViewAdviseSink::OnNewMessage](imapiviewadvisesink-onnewmessage.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="f517d-113">For example, when a new message arrives that your viewer should include in its display, the form calls your [IMAPIViewAdviseSink::OnNewMessage](imapiviewadvisesink-onnewmessage.md) method.</span></span> 
  
<span data-ttu-id="f517d-114">Implementieren Sie Ihre Ansicht advise-Empfänger in eine Möglichkeit, dass Ihre Viewer sinnvoll; Es ist keine standard-Implementierung.</span><span class="sxs-lookup"><span data-stu-id="f517d-114">Implement your view advise sink in a way that makes sense for your viewer; there is no standard implementation.</span></span> <span data-ttu-id="f517d-115">Beispielsweise können Sie die Ansicht im aktuellen Ordner Inhaltstabelle Einbeziehung die neu empfangene Meldung in **OnNewMessage** aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="f517d-115">For example, in **OnNewMessage** you can update the view of the current folder's contents table to include the newly arrived message.</span></span> <span data-ttu-id="f517d-116">In [IMAPIViewAdviseSink::OnSubmitted](imapiviewadvisesink-onsubmitted.md), die Methode, die aufgerufen wird, wenn Sie ein Ereignis gesendete Nachricht erhalten, können Sie die gesendete Nachricht in einen Ordner Gesendete Objekte kopieren.</span><span class="sxs-lookup"><span data-stu-id="f517d-116">In [IMAPIViewAdviseSink::OnSubmitted](imapiviewadvisesink-onsubmitted.md), the method that is called when you receive a submitted message event, you can copy the submitted message to a Sent Items folder.</span></span>
  
<span data-ttu-id="f517d-117">Formulare erhalten eine Benachrichtigung über den Viewer eine Änderung auftritt, der das Formular wirkt sich auf, wenn Sie eine neue Nachricht geladen werden.</span><span class="sxs-lookup"><span data-stu-id="f517d-117">Forms receive notification from your viewer when a change occurs that affects the form and when you are loading a new message.</span></span> <span data-ttu-id="f517d-118">Um ein Formular zu benachrichtigen, rufen Sie eine der Methoden des **IMAPIFormAdviseSink**: [IMAPIFormAdviseSink::OnChange](imapiformadvisesink-onchange.md) oder [IMAPIFormAdviseSink::OnActivateNext](imapiformadvisesink-onactivatenext.md).</span><span class="sxs-lookup"><span data-stu-id="f517d-118">To notify a form, call one of the methods of **IMAPIFormAdviseSink**: [IMAPIFormAdviseSink::OnChange](imapiformadvisesink-onchange.md) or [IMAPIFormAdviseSink::OnActivateNext](imapiformadvisesink-onactivatenext.md).</span></span> <span data-ttu-id="f517d-119">Rufen Sie die **OnChange** Status für die Kommunikation.</span><span class="sxs-lookup"><span data-stu-id="f517d-119">Call **OnChange** to communicate status.</span></span> <span data-ttu-id="f517d-120">Wenn das Formular in einem Ordner das letzte Element angezeigt wird, wenn eine neue Nachricht eingeht, rufen Sie **OnChange** beispielsweise mit VCSTATUS_NEXT Flag des Formulars mitgeteilt wird, dass nun eine nächsten Element vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="f517d-120">For example, if the form is displaying the last item in a folder when a new message arrives, call **OnChange** with the VCSTATUS_NEXT flag set to tell the form that there is now a next item.</span></span> 
  
<span data-ttu-id="f517d-121">Rufen Sie **OnActivateNext** , um das Formular über den Eingang einer neuen Nachricht informiert, dass es eventuell oder auch nicht angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="f517d-121">Call **OnActivateNext** to alert the form to the arrival of a new message that it may or may not be able to display.</span></span> <span data-ttu-id="f517d-122">Übergeben Sie die Nachrichtenklasse der Nachricht an **OnActivateNext**.</span><span class="sxs-lookup"><span data-stu-id="f517d-122">Pass the message class of the message to **OnActivateNext**.</span></span> 
  
<span data-ttu-id="f517d-123">Benachrichtigungen durch ein Form-Objekt an die Clientanwendung werden von der Clientanwendung **IMAPIViewAdviseSink** Schnittstelle behandelt.</span><span class="sxs-lookup"><span data-stu-id="f517d-123">Notifications by a form object to the client application are handled by the client application's **IMAPIViewAdviseSink** interface.</span></span> <span data-ttu-id="f517d-124">Weitere Informationen finden Sie unter [IMAPIViewAdviseSink: IUnknown](imapiviewadvisesinkiunknown.md).</span><span class="sxs-lookup"><span data-stu-id="f517d-124">For more information, see [IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md).</span></span>
  

