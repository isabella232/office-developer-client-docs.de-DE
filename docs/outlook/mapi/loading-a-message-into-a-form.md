---
title: Laden einer Nachricht in ein Formular
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4bdbe021-d694-4967-a105-4b24f1eebc44
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: afecd3b334dd2cf7b2953916872982e6459a8434
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412415"
---
# <a name="loading-a-message-into-a-form"></a><span data-ttu-id="253cd-103">Laden einer Nachricht in ein Formular</span><span class="sxs-lookup"><span data-stu-id="253cd-103">Loading a Message Into a Form</span></span>

  
  
<span data-ttu-id="253cd-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="253cd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="253cd-105">Wenn Sie eine vorhandene Nachricht mithilfe eines Formular Servers in ein Formular laden möchten, verwenden Sie eine der folgenden Strategien.</span><span class="sxs-lookup"><span data-stu-id="253cd-105">To load an existing message into a form using a form server, use one of the following strategies.</span></span>
  
- <span data-ttu-id="253cd-106">Rufen Sie [IMAPISession::P repareform](imapisession-prepareform.md) , um ein Token zu erstellen, und klicken Sie dann auf [IMAPISession:: ShowForm](imapisession-showform.md) , um das Formular anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="253cd-106">Call [IMAPISession::PrepareForm](imapisession-prepareform.md) to create a token and then [IMAPISession::ShowForm](imapisession-showform.md) to display the form.</span></span> 
    
- <span data-ttu-id="253cd-107">Rufen Sie [IMAPIFormMgr:: LoadForm](imapiformmgr-loadform.md)auf.</span><span class="sxs-lookup"><span data-stu-id="253cd-107">Call [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md).</span></span> 
    
<span data-ttu-id="253cd-108">Die Verwendung der **PrepareForm** -und **ShowForm** -Strategie ist vergleichsweise einfach, führt jedoch zu Formularen, die in Bezug auf Ihren Client Modal sind.</span><span class="sxs-lookup"><span data-stu-id="253cd-108">Using the **PrepareForm** and **ShowForm** strategy is comparatively easy, but it results in forms that are modal with respect to your client.</span></span> <span data-ttu-id="253cd-109">Der Grund ist, dass der Aufruf von **ShowForm** erst zurückgegeben wird, wenn das Formular beendet wurde.</span><span class="sxs-lookup"><span data-stu-id="253cd-109">This is because the call to **ShowForm** does not return until the form has exited.</span></span> <span data-ttu-id="253cd-110">Wenn Sie Formulare asynchron behandeln müssen, verwenden Sie diese Strategie nicht.</span><span class="sxs-lookup"><span data-stu-id="253cd-110">If you need to handle forms asynchronously, do not use this strategy.</span></span> 
  
<span data-ttu-id="253cd-111">Die Verwendung der **LoadForm** -Strategie ist schwieriger, da die Methode mehrere Parameter erfordert.</span><span class="sxs-lookup"><span data-stu-id="253cd-111">Using the **LoadForm** strategy is more difficult because the method requires several parameters.</span></span> <span data-ttu-id="253cd-112">Diese Parameter weisen den Formular-Manager an, den richtigen Formularserver im richtigen Kontext zu starten und die entsprechende Meldung anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="253cd-112">These parameters instruct the form manager to launch the proper form server in the proper context and display the proper message.</span></span> <span data-ttu-id="253cd-113">Wenn der Formularserver bereits aktiv ist, wird die Nachricht vom Formular-Manager in den Formularserver geladen, ohne eine neue Instanz des Formular Servers zu starten.</span><span class="sxs-lookup"><span data-stu-id="253cd-113">If the form server is already running, the form manager loads the message into the form server without launching a new instance of the form server.</span></span> 
  
<span data-ttu-id="253cd-114">Um anzugeben, welcher Formularserver gestartet werden soll, übergeben Sie die vom Zielserver verarbeitete Nachrichtenklasse im Inhalt des _lpszMessageClass_ -Parameters.</span><span class="sxs-lookup"><span data-stu-id="253cd-114">To specify which form server to launch, pass the message class handled by the target server in the contents of the  _lpszMessageClass_ parameter.</span></span> <span data-ttu-id="253cd-115">Die entsprechende Nachrichtenklasse kann ermittelt werden, indem die **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))-Eigenschaft der zu ladenden Nachricht abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="253cd-115">The appropriate message class can be determined by retrieving the **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property of the message to be loaded.</span></span> <span data-ttu-id="253cd-116">Manchmal gibt es keinen Formularserver für die angegebene Nachrichtenklasse, sondern nur einen Formularserver, der Nachrichten verarbeitet, die zur Oberklasse der Nachricht gehören.</span><span class="sxs-lookup"><span data-stu-id="253cd-116">Sometimes there is no form server for the specified message class, only a form server that handles messages belonging to the message's superclass.</span></span> <span data-ttu-id="253cd-117">Wenn Sie es vorziehen, die Nachricht nur von einem Formularserver zu laden, der speziell für die Verarbeitung von Nachrichten dieser Klasse vorgesehen ist, legen Sie das MAPIFORM_EXACTMATCH-Flag im **LoadForm** -Aufruf fest.</span><span class="sxs-lookup"><span data-stu-id="253cd-117">If you prefer that the message be loaded only by a form server specifically meant to handle messages of that class, set the MAPIFORM_EXACTMATCH flag in the **LoadForm** call.</span></span> <span data-ttu-id="253cd-118">Weitere Informationen finden Sie unter [MAPI Message Classes](mapi-message-classes.md).</span><span class="sxs-lookup"><span data-stu-id="253cd-118">For more information, see [MAPI Message Classes](mapi-message-classes.md).</span></span>
  
 <span data-ttu-id="253cd-119">**LoadForm** erfordert auch einen Zeiger auf die Nachrichtenwebsite und den Ansichtskontext des Viewers und den Wert für die **PR_MSG_STATUS** ([pidtagmessagestatus (](pidtagmessagestatus-canonical-property.md)) und **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) der Zielnachricht. Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="253cd-119">**LoadForm** also requires a pointer to your viewer's message site and view context and the value for the target message's **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) and **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) properties.</span></span>
  

