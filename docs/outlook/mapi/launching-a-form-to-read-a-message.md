---
title: Starten eines Formulars zum Lesen einer Nachricht
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 54a4b805-2ab7-4fb7-b0ea-4a33ead27451
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: b9166090321aa24e35fe1c82908aec0c403095cd
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593739"
---
# <a name="launching-a-form-to-read-a-message"></a><span data-ttu-id="4a1dd-103">Starten eines Formulars zum Lesen einer Nachricht</span><span class="sxs-lookup"><span data-stu-id="4a1dd-103">Launching a Form to Read a Message</span></span>

  
  
<span data-ttu-id="4a1dd-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4a1dd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4a1dd-105">Formular Server Implementierer erwarten, die folgende Sequenz von Methode Anrufe an ihre Formular Server- und Formularobjekte beim Laden von einer Clientanwendung aus einer Nachricht:</span><span class="sxs-lookup"><span data-stu-id="4a1dd-105">Form server implementers should expect the following sequence of method calls to their form server and form objects when a client application loads a message:</span></span>
  
1. <span data-ttu-id="4a1dd-106">Die Clientanwendung wird den Formular-Manager mit einem Aufruf der Funktion [MAPIOpenFormMgr](mapiopenformmgr.md) geöffnet.</span><span class="sxs-lookup"><span data-stu-id="4a1dd-106">The client application opens the form manager with a call to the [MAPIOpenFormMgr](mapiopenformmgr.md) function.</span></span> 
    
2. <span data-ttu-id="4a1dd-107">Die Clientanwendung ruft die [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) -Methode, die ein [IMAPIForm](imapiformiunknown.md)-Objekt zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="4a1dd-107">The client application calls the [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) method, which returns an object with [IMAPIForm](imapiformiunknown.md).</span></span> <span data-ttu-id="4a1dd-108">Der Formular-Manager kann jetzt freigegeben werden muss, wenn es nicht für weitere Formular Aktivierungen verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="4a1dd-108">The form manager may be released now if it will not be used for further form activations.</span></span> <span data-ttu-id="4a1dd-109">Beachten Sie, dass ein Aufruf von **LoadForm** einige Zeit dauern, da der Formular-Manager möglicherweise zum Installieren des Servers, der das Formular ausführbare Dateien vor dem fortfahren.</span><span class="sxs-lookup"><span data-stu-id="4a1dd-109">Note that a call to **LoadForm** may take some time because the form manager may have to install the form server's executable files before proceeding.</span></span> 
    
3. <span data-ttu-id="4a1dd-110">Optional kann die Clientanwendung [IMAPIViewContext](imapiviewcontextiunknown.md) Steuerelement Schritten vorbereiten, die das Form-Objekt geladen werden die vorherige oder nächste Nachricht im Ordner führen kann.</span><span class="sxs-lookup"><span data-stu-id="4a1dd-110">Optionally, the client application can prepare [IMAPIViewContext](imapiviewcontextiunknown.md) to control operations that may cause the form object to load the previous or next message in the folder.</span></span> <span data-ttu-id="4a1dd-111">Die Client-Anwendung können die [IMAPIForm::SetViewContext](imapiform-setviewcontext.md) -Methode den Standard-Ansichtskontext ändern, die festgelegt wurde in den Anruf **LoadForm** .</span><span class="sxs-lookup"><span data-stu-id="4a1dd-111">The client application can use the [IMAPIForm::SetViewContext](imapiform-setviewcontext.md) method to change the default view context that was set in the **LoadForm** call.</span></span> 
    
4. <span data-ttu-id="4a1dd-112">Die Clientanwendung ruft die [IPersistMessage::Load](ipersistmessage-load.md) -Methode, um Meldungsdaten in das Form-Objekt zu laden.</span><span class="sxs-lookup"><span data-stu-id="4a1dd-112">The client application calls the [IPersistMessage::Load](ipersistmessage-load.md) method to load message data into the form object.</span></span> 
    
5. <span data-ttu-id="4a1dd-113">Die Clientanwendung ruft [IMAPIForm::DoVerb](imapiform-doverb.md) zum Aufrufen der open Verbs Zeiger der optionalen [IMAPIViewContext](imapiviewcontextiunknown.md) -Schnittstelle übergeben.</span><span class="sxs-lookup"><span data-stu-id="4a1dd-113">The client application calls [IMAPIForm::DoVerb](imapiform-doverb.md) to invoke the open verb, passing the optional [IMAPIViewContext](imapiviewcontextiunknown.md) interface pointer.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="4a1dd-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4a1dd-114">See also</span></span>



[<span data-ttu-id="4a1dd-115">Formularserverinteraktionen</span><span class="sxs-lookup"><span data-stu-id="4a1dd-115">Form Server Interactions</span></span>](form-server-interactions.md)

