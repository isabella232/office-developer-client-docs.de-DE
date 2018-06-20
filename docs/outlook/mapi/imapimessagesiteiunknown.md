---
title: IMAPIMessageSite IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite
api_type:
- COM
ms.assetid: 883448f5-0d3f-486d-80a3-7b961c209cd0
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 75ef8d6f2134e0269745f92dab1f790228692853
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792238"
---
# <a name="imapimessagesite--iunknown"></a><span data-ttu-id="5a0cd-103">IMAPIMessageSite: IUnknown</span><span class="sxs-lookup"><span data-stu-id="5a0cd-103">IMAPIMessageSite : IUnknown</span></span>

  
  
<span data-ttu-id="5a0cd-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5a0cd-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5a0cd-105">Nachrichten bearbeitet und wird durch die Viewer Formularcode (normalerweise eine Clientanwendung), die auf eine solche Bearbeitung reagiert implementiert.</span><span class="sxs-lookup"><span data-stu-id="5a0cd-105">Manipulates messages and is implemented by the form viewer code (typically a client application) that responds to such manipulation.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5a0cd-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="5a0cd-106">Header file:</span></span>  <br/> |<span data-ttu-id="5a0cd-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="5a0cd-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="5a0cd-108">Verf�gbar gemacht von:</span><span class="sxs-lookup"><span data-stu-id="5a0cd-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="5a0cd-109">Nachricht Websiteobjekten</span><span class="sxs-lookup"><span data-stu-id="5a0cd-109">Message site objects</span></span>  <br/> |
|<span data-ttu-id="5a0cd-110">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="5a0cd-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="5a0cd-111">Formular-Viewer</span><span class="sxs-lookup"><span data-stu-id="5a0cd-111">Form viewers</span></span>  <br/> |
|<span data-ttu-id="5a0cd-112">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="5a0cd-112">Called by:</span></span>  <br/> |<span data-ttu-id="5a0cd-113">Formular-Objekte</span><span class="sxs-lookup"><span data-stu-id="5a0cd-113">Form objects</span></span>  <br/> |
|<span data-ttu-id="5a0cd-114">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="5a0cd-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="5a0cd-115">IID_IMAPIMessageSite</span><span class="sxs-lookup"><span data-stu-id="5a0cd-115">IID_IMAPIMessageSite</span></span>  <br/> |
|<span data-ttu-id="5a0cd-116">Zeigertyp:</span><span class="sxs-lookup"><span data-stu-id="5a0cd-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="5a0cd-117">LPMAPIMESSAGESITE</span><span class="sxs-lookup"><span data-stu-id="5a0cd-117">LPMAPIMESSAGESITE</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="5a0cd-118">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="5a0cd-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="5a0cd-119">GetSession</span><span class="sxs-lookup"><span data-stu-id="5a0cd-119">GetSession</span></span>](imapimessagesite-getsession.md) <br/> |<span data-ttu-id="5a0cd-120">Gibt die MAPI-Sitzung, in der die aktuelle Nachricht erstellt oder geöffnet wurde.</span><span class="sxs-lookup"><span data-stu-id="5a0cd-120">Returns the MAPI session in which the current message was created or opened.</span></span>  <br/> |
|[<span data-ttu-id="5a0cd-121">GetStore</span><span class="sxs-lookup"><span data-stu-id="5a0cd-121">GetStore</span></span>](imapimessagesite-getstore.md) <br/> |<span data-ttu-id="5a0cd-122">Gibt den Nachrichtenspeicher, der die aktuelle Nachricht enthält zurück, wenn eine solche ein Speicher vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="5a0cd-122">Returns the message store that contains the current message, if such a store exists.</span></span>  <br/> |
|[<span data-ttu-id="5a0cd-123">GetFolder</span><span class="sxs-lookup"><span data-stu-id="5a0cd-123">GetFolder</span></span>](imapimessagesite-getfolder.md) <br/> |<span data-ttu-id="5a0cd-124">Der Ordner, in dem die aktuelle Nachricht geöffnet oder erstellt wurde, zurückgegeben, wenn solche ein Ordner vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="5a0cd-124">Returns the folder in which the current message was created or opened, if such a folder exists.</span></span>  <br/> |
|[<span data-ttu-id="5a0cd-125">GetMessage</span><span class="sxs-lookup"><span data-stu-id="5a0cd-125">GetMessage</span></span>](imapimessagesite-getmessage.md) <br/> |<span data-ttu-id="5a0cd-126">Gibt die aktuelle Nachricht zurück.</span><span class="sxs-lookup"><span data-stu-id="5a0cd-126">Returns the current message.</span></span>  <br/> |
|[<span data-ttu-id="5a0cd-127">GetFormManager</span><span class="sxs-lookup"><span data-stu-id="5a0cd-127">GetFormManager</span></span>](imapimessagesite-getformmanager.md) <br/> |<span data-ttu-id="5a0cd-128">Gibt eine Formular-Manager-Schnittstelle, die ein Formular Server verwenden kann, um ein anderes Formular Server zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="5a0cd-128">Returns a form manager interface, which a form server can use to open another form server.</span></span>  <br/> |
|[<span data-ttu-id="5a0cd-129">NewMessage</span><span class="sxs-lookup"><span data-stu-id="5a0cd-129">NewMessage</span></span>](imapimessagesite-newmessage.md) <br/> |<span data-ttu-id="5a0cd-130">Erstellt eine neue Nachricht an.</span><span class="sxs-lookup"><span data-stu-id="5a0cd-130">Creates a new message.</span></span>  <br/> |
|[<span data-ttu-id="5a0cd-131">CopyMessage</span><span class="sxs-lookup"><span data-stu-id="5a0cd-131">CopyMessage</span></span>](imapimessagesite-copymessage.md) <br/> |<span data-ttu-id="5a0cd-132">Kopiert die aktuelle Nachricht in einen Ordner.</span><span class="sxs-lookup"><span data-stu-id="5a0cd-132">Copies the current message to a folder.</span></span>  <br/> |
|[<span data-ttu-id="5a0cd-133">MoveMessage</span><span class="sxs-lookup"><span data-stu-id="5a0cd-133">MoveMessage</span></span>](imapimessagesite-movemessage.md) <br/> |<span data-ttu-id="5a0cd-134">Verschiebt die aktuelle Nachricht in einen Ordner.</span><span class="sxs-lookup"><span data-stu-id="5a0cd-134">Moves the current message to a folder.</span></span>  <br/> |
|[<span data-ttu-id="5a0cd-135">DeleteMessage</span><span class="sxs-lookup"><span data-stu-id="5a0cd-135">DeleteMessage</span></span>](imapimessagesite-deletemessage.md) <br/> |<span data-ttu-id="5a0cd-136">Löscht die aktuelle Nachricht.</span><span class="sxs-lookup"><span data-stu-id="5a0cd-136">Deletes the current message.</span></span>  <br/> |
|[<span data-ttu-id="5a0cd-137">SaveMessage</span><span class="sxs-lookup"><span data-stu-id="5a0cd-137">SaveMessage</span></span>](imapimessagesite-savemessage.md) <br/> |<span data-ttu-id="5a0cd-138">Anforderungen, die die aktuelle Nachricht gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="5a0cd-138">Requests that the current message be saved.</span></span>  <br/> |
|[<span data-ttu-id="5a0cd-139">SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="5a0cd-139">SubmitMessage</span></span>](imapimessagesite-submitmessage.md) <br/> |<span data-ttu-id="5a0cd-140">Fordert, dass die aktuelle Nachricht für die Übermittlung in die Warteschlange gestellt werden.</span><span class="sxs-lookup"><span data-stu-id="5a0cd-140">Requests that the current message be queued for delivery.</span></span>  <br/> |
|[<span data-ttu-id="5a0cd-141">GetSiteStatus</span><span class="sxs-lookup"><span data-stu-id="5a0cd-141">GetSiteStatus</span></span>](imapimessagesite-getsitestatus.md) <br/> |<span data-ttu-id="5a0cd-142">Gibt Informationen aus einem Objekt "Message" Website zur Nachricht der Website Funktionen für die aktuelle Nachricht zurück.</span><span class="sxs-lookup"><span data-stu-id="5a0cd-142">Returns information from a message site object about the message site's capabilities for the current message.</span></span>  <br/> |
|[<span data-ttu-id="5a0cd-143">GetLastError</span><span class="sxs-lookup"><span data-stu-id="5a0cd-143">GetLastError</span></span>](imapimessagesite-getlasterror.md) <br/> |<span data-ttu-id="5a0cd-144">Gibt eine [MAPIERROR](mapierror.md) -Struktur, die Informationen über den vorherigen Fehler auftreten, um das Objekt "Message" Website enthält.</span><span class="sxs-lookup"><span data-stu-id="5a0cd-144">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error occurring to the message site object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5a0cd-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5a0cd-145">See also</span></span>



[<span data-ttu-id="5a0cd-146">MAPI-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="5a0cd-146">MAPI Interfaces</span></span>](mapi-interfaces.md)

