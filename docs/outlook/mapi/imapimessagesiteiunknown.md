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
ms.openlocfilehash: bf21ed1d41a61f600cfded777b699cf620c2e00f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321350"
---
# <a name="imapimessagesite--iunknown"></a><span data-ttu-id="1b071-103">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1b071-103">IMAPIMessageSite : IUnknown</span></span>

  
  
<span data-ttu-id="1b071-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1b071-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1b071-105">Bearbeitet Nachrichten und wird vom Formularanzeige Code (in der Regel eine Clientanwendung) implementiert, der auf eine solche Manipulation reagiert.</span><span class="sxs-lookup"><span data-stu-id="1b071-105">Manipulates messages and is implemented by the form viewer code (typically a client application) that responds to such manipulation.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1b071-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="1b071-106">Header file:</span></span>  <br/> |<span data-ttu-id="1b071-107">Mapiform. h</span><span class="sxs-lookup"><span data-stu-id="1b071-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="1b071-108">Verf�gbar gemacht von:</span><span class="sxs-lookup"><span data-stu-id="1b071-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="1b071-109">Nachrichtenwebsite Objekte</span><span class="sxs-lookup"><span data-stu-id="1b071-109">Message site objects</span></span>  <br/> |
|<span data-ttu-id="1b071-110">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="1b071-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="1b071-111">Formular Betrachter</span><span class="sxs-lookup"><span data-stu-id="1b071-111">Form viewers</span></span>  <br/> |
|<span data-ttu-id="1b071-112">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="1b071-112">Called by:</span></span>  <br/> |<span data-ttu-id="1b071-113">Formularobjekte</span><span class="sxs-lookup"><span data-stu-id="1b071-113">Form objects</span></span>  <br/> |
|<span data-ttu-id="1b071-114">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="1b071-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="1b071-115">IID_IMAPIMessageSite</span><span class="sxs-lookup"><span data-stu-id="1b071-115">IID_IMAPIMessageSite</span></span>  <br/> |
|<span data-ttu-id="1b071-116">Zeigertyp:</span><span class="sxs-lookup"><span data-stu-id="1b071-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="1b071-117">LPMAPIMESSAGESITE</span><span class="sxs-lookup"><span data-stu-id="1b071-117">LPMAPIMESSAGESITE</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="1b071-118">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="1b071-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="1b071-119">GetSession "</span><span class="sxs-lookup"><span data-stu-id="1b071-119">GetSession</span></span>](imapimessagesite-getsession.md) <br/> |<span data-ttu-id="1b071-120">Gibt die MAPI-Sitzung zurück, in der die aktuelle Nachricht erstellt oder geöffnet wurde.</span><span class="sxs-lookup"><span data-stu-id="1b071-120">Returns the MAPI session in which the current message was created or opened.</span></span>  <br/> |
|[<span data-ttu-id="1b071-121">GetStore</span><span class="sxs-lookup"><span data-stu-id="1b071-121">GetStore</span></span>](imapimessagesite-getstore.md) <br/> |<span data-ttu-id="1b071-122">Gibt den Nachrichtenspeicher zurück, der die aktuelle Nachricht enthält, wenn ein solcher Speicher vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="1b071-122">Returns the message store that contains the current message, if such a store exists.</span></span>  <br/> |
|[<span data-ttu-id="1b071-123">GetFolder</span><span class="sxs-lookup"><span data-stu-id="1b071-123">GetFolder</span></span>](imapimessagesite-getfolder.md) <br/> |<span data-ttu-id="1b071-124">Gibt den Ordner zurück, in dem die aktuelle Nachricht erstellt oder geöffnet wurde, wenn ein solcher Ordner vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="1b071-124">Returns the folder in which the current message was created or opened, if such a folder exists.</span></span>  <br/> |
|[<span data-ttu-id="1b071-125">GetMessage</span><span class="sxs-lookup"><span data-stu-id="1b071-125">GetMessage</span></span>](imapimessagesite-getmessage.md) <br/> |<span data-ttu-id="1b071-126">Gibt die aktuelle Nachricht zurück.</span><span class="sxs-lookup"><span data-stu-id="1b071-126">Returns the current message.</span></span>  <br/> |
|[<span data-ttu-id="1b071-127">GetFormmanager</span><span class="sxs-lookup"><span data-stu-id="1b071-127">GetFormManager</span></span>](imapimessagesite-getformmanager.md) <br/> |<span data-ttu-id="1b071-128">Gibt eine Formular-Manager-Schnittstelle zurück, die ein Formularserver zum Öffnen eines anderen Formular Servers verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="1b071-128">Returns a form manager interface, which a form server can use to open another form server.</span></span>  <br/> |
|[<span data-ttu-id="1b071-129">NewMessage</span><span class="sxs-lookup"><span data-stu-id="1b071-129">NewMessage</span></span>](imapimessagesite-newmessage.md) <br/> |<span data-ttu-id="1b071-130">Erstellt eine neue Nachricht.</span><span class="sxs-lookup"><span data-stu-id="1b071-130">Creates a new message.</span></span>  <br/> |
|[<span data-ttu-id="1b071-131">CopyMessage</span><span class="sxs-lookup"><span data-stu-id="1b071-131">CopyMessage</span></span>](imapimessagesite-copymessage.md) <br/> |<span data-ttu-id="1b071-132">Kopiert die aktuelle Nachricht in einen Ordner.</span><span class="sxs-lookup"><span data-stu-id="1b071-132">Copies the current message to a folder.</span></span>  <br/> |
|[<span data-ttu-id="1b071-133">MoveMessage</span><span class="sxs-lookup"><span data-stu-id="1b071-133">MoveMessage</span></span>](imapimessagesite-movemessage.md) <br/> |<span data-ttu-id="1b071-134">Verschiebt die aktuelle Nachricht in einen Ordner.</span><span class="sxs-lookup"><span data-stu-id="1b071-134">Moves the current message to a folder.</span></span>  <br/> |
|[<span data-ttu-id="1b071-135">DeleteMessage</span><span class="sxs-lookup"><span data-stu-id="1b071-135">DeleteMessage</span></span>](imapimessagesite-deletemessage.md) <br/> |<span data-ttu-id="1b071-136">Löscht die aktuelle Nachricht.</span><span class="sxs-lookup"><span data-stu-id="1b071-136">Deletes the current message.</span></span>  <br/> |
|[<span data-ttu-id="1b071-137">SaveMessage</span><span class="sxs-lookup"><span data-stu-id="1b071-137">SaveMessage</span></span>](imapimessagesite-savemessage.md) <br/> |<span data-ttu-id="1b071-138">Fordert, dass die aktuelle Nachricht gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="1b071-138">Requests that the current message be saved.</span></span>  <br/> |
|[<span data-ttu-id="1b071-139">SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="1b071-139">SubmitMessage</span></span>](imapimessagesite-submitmessage.md) <br/> |<span data-ttu-id="1b071-140">Fordert an, dass die aktuelle Nachricht für die Übermittlung in die Warteschlange gestellt wird.</span><span class="sxs-lookup"><span data-stu-id="1b071-140">Requests that the current message be queued for delivery.</span></span>  <br/> |
|[<span data-ttu-id="1b071-141">GetSiteStatus</span><span class="sxs-lookup"><span data-stu-id="1b071-141">GetSiteStatus</span></span>](imapimessagesite-getsitestatus.md) <br/> |<span data-ttu-id="1b071-142">Gibt Informationen aus einem Nachrichtenwebsite Objekt über die Funktionen der Nachrichtenwebsite für die aktuelle Nachricht zurück.</span><span class="sxs-lookup"><span data-stu-id="1b071-142">Returns information from a message site object about the message site's capabilities for the current message.</span></span>  <br/> |
|[<span data-ttu-id="1b071-143">Getlasterroraufzurufen</span><span class="sxs-lookup"><span data-stu-id="1b071-143">GetLastError</span></span>](imapimessagesite-getlasterror.md) <br/> |<span data-ttu-id="1b071-144">Gibt eine [MAPIERROR](mapierror.md) -Struktur zurück, die Informationen zum vorherigen Fehler enthält, der für das Nachrichtenwebsite Objekt auftritt.</span><span class="sxs-lookup"><span data-stu-id="1b071-144">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error occurring to the message site object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1b071-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1b071-145">See also</span></span>



[<span data-ttu-id="1b071-146">MAPI-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="1b071-146">MAPI Interfaces</span></span>](mapi-interfaces.md)

