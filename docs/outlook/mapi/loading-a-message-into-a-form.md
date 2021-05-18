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
# <a name="loading-a-message-into-a-form"></a><span data-ttu-id="7616c-103">Laden einer Nachricht in ein Formular</span><span class="sxs-lookup"><span data-stu-id="7616c-103">Loading a Message Into a Form</span></span>

  
  
<span data-ttu-id="7616c-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7616c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7616c-105">Verwenden Sie eine der folgenden Strategien, um eine vorhandene Nachricht mithilfe eines Formularservers in ein Formular zu laden.</span><span class="sxs-lookup"><span data-stu-id="7616c-105">To load an existing message into a form using a form server, use one of the following strategies.</span></span>
  
- <span data-ttu-id="7616c-106">Rufen [Sie IMAPISession::P repareForm](imapisession-prepareform.md) auf, um ein Token zu erstellen, und dann [IMAPISession::ShowForm](imapisession-showform.md) zum Anzeigen des Formulars.</span><span class="sxs-lookup"><span data-stu-id="7616c-106">Call [IMAPISession::PrepareForm](imapisession-prepareform.md) to create a token and then [IMAPISession::ShowForm](imapisession-showform.md) to display the form.</span></span> 
    
- <span data-ttu-id="7616c-107">Rufen [Sie IMAPIFormMgr::LoadForm auf.](imapiformmgr-loadform.md)</span><span class="sxs-lookup"><span data-stu-id="7616c-107">Call [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md).</span></span> 
    
<span data-ttu-id="7616c-108">Die **Verwendung der PrepareForm-** und **ShowForm-Strategie** ist vergleichsweise einfach, führt jedoch zu modalen Formularen im Hinblick auf Ihren Client.</span><span class="sxs-lookup"><span data-stu-id="7616c-108">Using the **PrepareForm** and **ShowForm** strategy is comparatively easy, but it results in forms that are modal with respect to your client.</span></span> <span data-ttu-id="7616c-109">Der Grund dafür ist, dass der Aufruf von **ShowForm** erst zurückt, wenn das Formular beendet wurde.</span><span class="sxs-lookup"><span data-stu-id="7616c-109">This is because the call to **ShowForm** does not return until the form has exited.</span></span> <span data-ttu-id="7616c-110">Wenn Sie Formulare asynchron behandeln müssen, verwenden Sie diese Strategie nicht.</span><span class="sxs-lookup"><span data-stu-id="7616c-110">If you need to handle forms asynchronously, do not use this strategy.</span></span> 
  
<span data-ttu-id="7616c-111">Die **Verwendung der LoadForm-Strategie** ist schwieriger, da die Methode mehrere Parameter erfordert.</span><span class="sxs-lookup"><span data-stu-id="7616c-111">Using the **LoadForm** strategy is more difficult because the method requires several parameters.</span></span> <span data-ttu-id="7616c-112">Mit diesen Parametern wird der Formular-Manager angewiesen, den richtigen Formularserver im richtigen Kontext zu starten und die richtige Nachricht anzeigen zu können.</span><span class="sxs-lookup"><span data-stu-id="7616c-112">These parameters instruct the form manager to launch the proper form server in the proper context and display the proper message.</span></span> <span data-ttu-id="7616c-113">Wenn der Formularserver bereits ausgeführt wird, lädt der Formular-Manager die Nachricht auf den Formularserver, ohne eine neue Instanz des Formularservers zu starten.</span><span class="sxs-lookup"><span data-stu-id="7616c-113">If the form server is already running, the form manager loads the message into the form server without launching a new instance of the form server.</span></span> 
  
<span data-ttu-id="7616c-114">Um anzugeben, welcher Formularserver gestartet werden soll, übergeben Sie die nachrichtenklasse, die vom Zielserver verarbeitet wird, im Inhalt des _lpszMessageClass-Parameters._</span><span class="sxs-lookup"><span data-stu-id="7616c-114">To specify which form server to launch, pass the message class handled by the target server in the contents of the  _lpszMessageClass_ parameter.</span></span> <span data-ttu-id="7616c-115">Die entsprechende Nachrichtenklasse kann durch Abrufen der **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) -Eigenschaft der zu ladenden Nachricht bestimmt werden.</span><span class="sxs-lookup"><span data-stu-id="7616c-115">The appropriate message class can be determined by retrieving the **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property of the message to be loaded.</span></span> <span data-ttu-id="7616c-116">Manchmal gibt es keinen Formularserver für die angegebene Nachrichtenklasse, sondern nur einen Formularserver, der Nachrichten verarbeitet, die zur Überklasse der Nachricht gehören.</span><span class="sxs-lookup"><span data-stu-id="7616c-116">Sometimes there is no form server for the specified message class, only a form server that handles messages belonging to the message's superclass.</span></span> <span data-ttu-id="7616c-117">Wenn Sie es vorziehen, dass die Nachricht nur von einem Formularserver geladen wird, der speziell für die Verarbeitung von Nachrichten dieser Klasse gedacht ist, legen Sie das MAPIFORM_EXACTMATCH im **LoadForm-Aufruf** fest.</span><span class="sxs-lookup"><span data-stu-id="7616c-117">If you prefer that the message be loaded only by a form server specifically meant to handle messages of that class, set the MAPIFORM_EXACTMATCH flag in the **LoadForm** call.</span></span> <span data-ttu-id="7616c-118">Weitere Informationen finden Sie unter [MAPI Message Classes](mapi-message-classes.md).</span><span class="sxs-lookup"><span data-stu-id="7616c-118">For more information, see [MAPI Message Classes](mapi-message-classes.md).</span></span>
  
 <span data-ttu-id="7616c-119">**LoadForm** erfordert außerdem einen Zeiger auf die Nachrichtenwebsite und den Ansichtskontext des Betrachters sowie den Wert für die **Eigenschaften PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) und **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) der Zielnachricht.</span><span class="sxs-lookup"><span data-stu-id="7616c-119">**LoadForm** also requires a pointer to your viewer's message site and view context and the value for the target message's **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) and **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) properties.</span></span>
  

