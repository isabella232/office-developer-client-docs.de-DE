---
title: Laden eine Nachricht in ein Formular
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4bdbe021-d694-4967-a105-4b24f1eebc44
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: d677958b1a429201c05b5195c58bd7462d0f3d37
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792900"
---
# <a name="loading-a-message-into-a-form"></a><span data-ttu-id="40de3-103">Laden eine Nachricht in ein Formular</span><span class="sxs-lookup"><span data-stu-id="40de3-103">Loading a Message Into a Form</span></span>

  
  
<span data-ttu-id="40de3-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="40de3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="40de3-105">Um eine vorhandene Nachricht in einem Formular mit einem Formular Server zu laden, verwenden Sie eine der folgenden Strategien.</span><span class="sxs-lookup"><span data-stu-id="40de3-105">To load an existing message into a form using a form server, use one of the following strategies.</span></span>
  
- <span data-ttu-id="40de3-106">Rufen Sie [IMAPISession::PrepareForm](imapisession-prepareform.md) , um ein Token zu erstellen, und klicken Sie dann [IMAPISession::ShowForm](imapisession-showform.md) um das Formular anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="40de3-106">Call [IMAPISession::PrepareForm](imapisession-prepareform.md) to create a token and then [IMAPISession::ShowForm](imapisession-showform.md) to display the form.</span></span> 
    
- <span data-ttu-id="40de3-107">Rufen Sie [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md).</span><span class="sxs-lookup"><span data-stu-id="40de3-107">Call [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md).</span></span> 
    
<span data-ttu-id="40de3-108">Verwenden der Strategie **PrepareForm** und **ShowForm aus** relativ einfach ist, aber es führt zu Formularen, die in Bezug auf Ihrem Client modal sind.</span><span class="sxs-lookup"><span data-stu-id="40de3-108">Using the **PrepareForm** and **ShowForm** strategy is comparatively easy, but it results in forms that are modal with respect to your client.</span></span> <span data-ttu-id="40de3-109">Dies ist, da der Anruf an **ShowForm aus** , bis das Formular beendet wurde nicht zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="40de3-109">This is because the call to **ShowForm** does not return until the form has exited.</span></span> <span data-ttu-id="40de3-110">Wenn Sie Formulare asynchron verarbeiten müssen, verwenden Sie diese Strategie nicht.</span><span class="sxs-lookup"><span data-stu-id="40de3-110">If you need to handle forms asynchronously, do not use this strategy.</span></span> 
  
<span data-ttu-id="40de3-111">Verwenden der **LoadForm** Strategie ist schwieriger, da die Methode mehrere Parameter erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="40de3-111">Using the **LoadForm** strategy is more difficult because the method requires several parameters.</span></span> <span data-ttu-id="40de3-112">Diese Parameter weisen den Formular-Manager, starten Sie den Server ordnungsgemäße Formular im richtigen Kontext und die richtige Meldung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="40de3-112">These parameters instruct the form manager to launch the proper form server in the proper context and display the proper message.</span></span> <span data-ttu-id="40de3-113">Wenn der Formular Server bereits ausgeführt wird, lädt der Formular-Manager die Nachricht in dem Formular Server ohne eine neue Instanz des Formulars Servers starten.</span><span class="sxs-lookup"><span data-stu-id="40de3-113">If the form server is already running, the form manager loads the message into the form server without launching a new instance of the form server.</span></span> 
  
<span data-ttu-id="40de3-114">Welche Formular Server zu starten, und übergeben Sie die Nachrichtenklasse angeben, die von dem Zielserver in den Inhalt des Parameters _LpszMessageClass_ behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="40de3-114">To specify which form server to launch, pass the message class handled by the target server in the contents of the  _lpszMessageClass_ parameter.</span></span> <span data-ttu-id="40de3-115">Die entsprechende Nachrichtenklasse kann ermittelt werden, durch die Eigenschaft **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) der Nachricht zu ladenden abrufen.</span><span class="sxs-lookup"><span data-stu-id="40de3-115">The appropriate message class can be determined by retrieving the **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property of the message to be loaded.</span></span> <span data-ttu-id="40de3-116">In einigen Fällen ist kein Formular Server für die angegebene Nachrichtenklasse nur Formular von einem Server, die Nachrichten, die an die Nachricht zur übergeordneten Klasse gehören behandelt.</span><span class="sxs-lookup"><span data-stu-id="40de3-116">Sometimes there is no form server for the specified message class, only a form server that handles messages belonging to the message's superclass.</span></span> <span data-ttu-id="40de3-117">Wenn Sie, dass die Nachricht nur von einem Formular-Server zum Verarbeiten von Nachrichten dieser Klasse speziell dafür vorgesehen geladen werden möchten, legen Sie das MAPIFORM_EXACTMATCH-Flag in den Anruf **LoadForm** .</span><span class="sxs-lookup"><span data-stu-id="40de3-117">If you prefer that the message be loaded only by a form server specifically meant to handle messages of that class, set the MAPIFORM_EXACTMATCH flag in the **LoadForm** call.</span></span> <span data-ttu-id="40de3-118">Weitere Informationen finden Sie unter [MAPI Message Classes](mapi-message-classes.md).</span><span class="sxs-lookup"><span data-stu-id="40de3-118">For more information, see [MAPI Message Classes](mapi-message-classes.md).</span></span>
  
 <span data-ttu-id="40de3-119">**LoadForm** erfordert auch einen Zeiger auf Ihre Viewer Nachricht Website und Ansichtskontext und den Wert für die Zielnachricht **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) und **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="40de3-119">**LoadForm** also requires a pointer to your viewer's message site and view context and the value for the target message's **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) and **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) properties.</span></span>
  

