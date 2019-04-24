---
title: Starten eines Formular Servers
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a439e75a-92b3-4830-9dfc-e723d046be7b
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: dec8706ba00356660ec82c25e0213ef3e638691d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32270049"
---
# <a name="launching-a-form-server"></a><span data-ttu-id="b4602-103">Starten eines Formular Servers</span><span class="sxs-lookup"><span data-stu-id="b4602-103">Launching a Form Server</span></span>

  
  
<span data-ttu-id="b4602-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b4602-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b4602-105">Die Reihe von Interaktionen, die auftreten, wenn ein Formular aus einem persistenten Speicher (also aus einer Formularbibliothek) geladen wird, um eine Meldung anzuzeigen, lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="b4602-105">The series of interactions that occurs when a form is loaded from persistent storage (that is, from a form library) to display a message is as follows:</span></span>
  
1. <span data-ttu-id="b4602-106">Der Messaging-Client ruft Nachrichtenklasse, Nachrichtenkennzeichen und Nachrichtenstatus der Nachricht ab.</span><span class="sxs-lookup"><span data-stu-id="b4602-106">The messaging client gets the message's message class, message flags, and message status.</span></span> <span data-ttu-id="b4602-107">Dieser Schritt ist optional; Wenn diese Datenteile in Schritt 2 nicht bereitgestellt werden, werden Sie vom Formular-Manager abgerufen.</span><span class="sxs-lookup"><span data-stu-id="b4602-107">This step is optional; if these pieces of data are not provided in step 2, the form manager will retrieve them.</span></span>
    
2. <span data-ttu-id="b4602-108">Der Messaging Client ruft [IMAPIFormMgr:: LoadForm](imapiformmgr-loadform.md) mit der Zielnachricht auf.</span><span class="sxs-lookup"><span data-stu-id="b4602-108">The messaging client calls [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) with the target message.</span></span> 
    
3. <span data-ttu-id="b4602-109">Der Formular-Manager lädt den Formularserver aus der entsprechenden Formularbibliothek.</span><span class="sxs-lookup"><span data-stu-id="b4602-109">The form manager loads the form server from the appropriate form library.</span></span> <span data-ttu-id="b4602-110">Wenn der Formularserver für die Zielnachricht nicht installiert ist, werden auch die ausführbaren Dateien des Formulars vom Formular-Manager installiert.</span><span class="sxs-lookup"><span data-stu-id="b4602-110">If the form server for the target message is not installed, the form manager installs the form's executable files, as well.</span></span>
    
4. <span data-ttu-id="b4602-111">Der Formular-Manager ruft [IUnknown:: QueryInterface](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) für das Form-Objekt auf, um die Schnittstellen [IMAPIForm: IUnknown](imapiformiunknown.md) und [IPersistMessage: IUnknown](ipersistmessageiunknown.md) des Form-Objekts abzurufen.</span><span class="sxs-lookup"><span data-stu-id="b4602-111">The form manager calls [IUnknown::QueryInterface](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) on the form object to obtain the form object's [IMAPIForm : IUnknown](imapiformiunknown.md) and [IPersistMessage : IUnknown](ipersistmessageiunknown.md) interfaces.</span></span> 
    
5. <span data-ttu-id="b4602-112">Der Formular-Manager ruft [IPersistMessage:: Laden](ipersistmessage-load.md) mit dem Nachrichten Standort und den Nachrichten Schnittstellen vom Viewer-Objekt auf.</span><span class="sxs-lookup"><span data-stu-id="b4602-112">The form manager calls [IPersistMessage::Load](ipersistmessage-load.md) with the message site and message interfaces from the viewer object.</span></span> 
    
6. <span data-ttu-id="b4602-113">Das Form-Objekt ruft zurück zur [IMAPIMessageSite:: GetSiteStatus](imapimessagesite-getsitestatus.md) -Methode des Messagingclients auf.</span><span class="sxs-lookup"><span data-stu-id="b4602-113">The form object calls back to the messaging client's [IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md) method.</span></span> 
    
7. <span data-ttu-id="b4602-114">Der Formular-Manager ruft die [IMAPIForm::](imapiform-setviewcontext.md) setviewcontext-Methode des Form-Objekts mit der Kontext Schnittstelle View des Messagingclients auf.</span><span class="sxs-lookup"><span data-stu-id="b4602-114">The form manager calls the form object's [IMAPIForm::SetViewContext](imapiform-setviewcontext.md) method with the view context interface from the messaging client.</span></span> 
    
8. <span data-ttu-id="b4602-115">Das Form-Objekt ruft zurück zur [IMAPIViewContext:: SetAdviseSink](imapiviewcontext-setadvisesink.md) -Methode des Messagingclients auf.</span><span class="sxs-lookup"><span data-stu-id="b4602-115">The form object calls back to the messaging client's [IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) method.</span></span> 
    
9. <span data-ttu-id="b4602-116">Das Form-Objekt ruft zurück zur [IMAPIViewContext:: GetViewStatus](imapiviewcontext-getviewstatus.md) -Methode des Messagingclients auf.</span><span class="sxs-lookup"><span data-stu-id="b4602-116">The form object calls back to the messaging client's [IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md) method.</span></span> 
    
10. <span data-ttu-id="b4602-117">Der Messaging-Client ruft die [IMAPIForm:: Advise](imapiform-advise.md) -Methode des Form-Objekts mit den Ansichtskontext Schnittstellen des Viewer-Objekts und des Message-websiteobjekts auf.</span><span class="sxs-lookup"><span data-stu-id="b4602-117">The messaging client calls the form object's [IMAPIForm::Advise](imapiform-advise.md) method with the view context interfaces from the viewer object and the message site object.</span></span> 
    
11. <span data-ttu-id="b4602-118">Der Messaging Client ruft die [IMAPIForm::D overb](imapiform-doverb.md) -Methode des Form-Objekts auf.</span><span class="sxs-lookup"><span data-stu-id="b4602-118">The messaging client calls the form object's [IMAPIForm::DoVerb](imapiform-doverb.md) method.</span></span> 
    
12. <span data-ttu-id="b4602-119">Das Form-Objekt erstellt die Benutzeroberfläche, falls erforderlich, und interagiert mit dem Benutzer.</span><span class="sxs-lookup"><span data-stu-id="b4602-119">The form object creates its user interface, if necessary, and interacts with the user.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b4602-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b4602-120">See also</span></span>



[<span data-ttu-id="b4602-121">Formular Server interAktionen</span><span class="sxs-lookup"><span data-stu-id="b4602-121">Form Server Interactions</span></span>](form-server-interactions.md)

