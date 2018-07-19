---
title: Starten eines Formularservers
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a439e75a-92b3-4830-9dfc-e723d046be7b
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: c70fd9eb771268db4030cefdf2f27b75ae5963b7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792896"
---
# <a name="launching-a-form-server"></a><span data-ttu-id="58b7a-103">Starten eines Formularservers</span><span class="sxs-lookup"><span data-stu-id="58b7a-103">Launching a Form Server</span></span>

  
  
<span data-ttu-id="58b7a-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="58b7a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="58b7a-105">Die Reihe von Interaktionen, das auftritt, wenn ein Formular aus dem permanenten Speicher geladen wird (d. h., aus einer Formularbibliothek) zum Anzeigen einer Meldung lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="58b7a-105">The series of interactions that occurs when a form is loaded from persistent storage (that is, from a form library) to display a message is as follows:</span></span>
  
1. <span data-ttu-id="58b7a-106">Der messaging-Client Ruft die Nachrichtenklasse, Nachrichtenflags und Nachricht den Status der Nachricht ab.</span><span class="sxs-lookup"><span data-stu-id="58b7a-106">The messaging client gets the message's message class, message flags, and message status.</span></span> <span data-ttu-id="58b7a-107">Dieser Schritt ist optional. Wenn dieser Datenelemente nicht in Schritt 2 angegeben werden, wird der Formular-Manager diese abzurufen.</span><span class="sxs-lookup"><span data-stu-id="58b7a-107">This step is optional; if these pieces of data are not provided in step 2, the form manager will retrieve them.</span></span>
    
2. <span data-ttu-id="58b7a-108">Der messaging-Client ruft [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) mit der Nachrichten-Ziel.</span><span class="sxs-lookup"><span data-stu-id="58b7a-108">The messaging client calls [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) with the target message.</span></span> 
    
3. <span data-ttu-id="58b7a-109">Der Formular-Manager lädt der Formular-Server aus der entsprechenden Formularbibliothek.</span><span class="sxs-lookup"><span data-stu-id="58b7a-109">The form manager loads the form server from the appropriate form library.</span></span> <span data-ttu-id="58b7a-110">Wenn der Formular Server für die Zielnachricht nicht installiert ist, wird der Formular-Manager des Formulars ausführbare Dateien als auch installiert.</span><span class="sxs-lookup"><span data-stu-id="58b7a-110">If the form server for the target message is not installed, the form manager installs the form's executable files, as well.</span></span>
    
4. <span data-ttu-id="58b7a-111">Der Formular-Manager ruft [QueryInterface](http://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) für das Formularobjekt, des Form-Objekts abgerufen [IMAPIForm: IUnknown](imapiformiunknown.md) und [IPersistMessage: IUnknown](ipersistmessageiunknown.md) Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="58b7a-111">The form manager calls [IUnknown::QueryInterface](http://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) on the form object to obtain the form object's [IMAPIForm : IUnknown](imapiformiunknown.md) and [IPersistMessage : IUnknown](ipersistmessageiunknown.md) interfaces.</span></span> 
    
5. <span data-ttu-id="58b7a-112">Der Formular-Manager ruft [IPersistMessage::Load](ipersistmessage-load.md) mit der Nachrichten-Website und die Nachricht Schnittstellen aus dem Viewer-Objekt.</span><span class="sxs-lookup"><span data-stu-id="58b7a-112">The form manager calls [IPersistMessage::Load](ipersistmessage-load.md) with the message site and message interfaces from the viewer object.</span></span> 
    
6. <span data-ttu-id="58b7a-113">Das Form-Objekt einen Rückruf an die messaging-Client [IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="58b7a-113">The form object calls back to the messaging client's [IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md) method.</span></span> 
    
7. <span data-ttu-id="58b7a-114">Der Formular-Manager Ruft das Formularobjekt [IMAPIForm::SetViewContext](imapiform-setviewcontext.md) -Methode mit der Ansicht Kontext-Schnittstelle von der messaging-Client.</span><span class="sxs-lookup"><span data-stu-id="58b7a-114">The form manager calls the form object's [IMAPIForm::SetViewContext](imapiform-setviewcontext.md) method with the view context interface from the messaging client.</span></span> 
    
8. <span data-ttu-id="58b7a-115">Das Form-Objekt einen Rückruf an die messaging-Client [IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="58b7a-115">The form object calls back to the messaging client's [IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) method.</span></span> 
    
9. <span data-ttu-id="58b7a-116">Das Form-Objekt einen Rückruf an die messaging-Client [IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="58b7a-116">The form object calls back to the messaging client's [IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md) method.</span></span> 
    
10. <span data-ttu-id="58b7a-117">Der messaging-Client Ruft das Formularobjekt [IMAPIForm::Advise](imapiform-advise.md) -Methode mit der Ansicht Kontext Schnittstellen aus dem Viewer-Objekt und das Objekt "Message" Website.</span><span class="sxs-lookup"><span data-stu-id="58b7a-117">The messaging client calls the form object's [IMAPIForm::Advise](imapiform-advise.md) method with the view context interfaces from the viewer object and the message site object.</span></span> 
    
11. <span data-ttu-id="58b7a-118">Der messaging-Client Ruft das Formularobjekt [IMAPIForm::DoVerb](imapiform-doverb.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="58b7a-118">The messaging client calls the form object's [IMAPIForm::DoVerb](imapiform-doverb.md) method.</span></span> 
    
12. <span data-ttu-id="58b7a-119">Das Form-Objekt die Benutzeroberfläche erstellt, bei Bedarf, und interagiert mit dem Benutzer.</span><span class="sxs-lookup"><span data-stu-id="58b7a-119">The form object creates its user interface, if necessary, and interacts with the user.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="58b7a-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="58b7a-120">See also</span></span>



[<span data-ttu-id="58b7a-121">Formularserverinteraktionen</span><span class="sxs-lookup"><span data-stu-id="58b7a-121">Form Server Interactions</span></span>](form-server-interactions.md)

