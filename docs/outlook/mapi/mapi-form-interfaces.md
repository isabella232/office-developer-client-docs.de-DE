---
title: MAPI-Formularoberflächen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 611213c9-e758-4366-b193-fc62181d3d1f
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: f37d398167e8210a2fd67ff08e63572eb6c9db9c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585724"
---
# <a name="mapi-form-interfaces"></a><span data-ttu-id="2dcd4-103">MAPI-Formularoberflächen</span><span class="sxs-lookup"><span data-stu-id="2dcd4-103">MAPI Form Interfaces</span></span>

  
  
<span data-ttu-id="2dcd4-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2dcd4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2dcd4-105">MAPI definiert die folgenden Schnittstellen, die sich auf die Formulare beziehen.</span><span class="sxs-lookup"><span data-stu-id="2dcd4-105">MAPI defines the following interfaces relating to forms.</span></span>
  
|<span data-ttu-id="2dcd4-106">**Name der Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="2dcd4-106">**Interface name**</span></span>|<span data-ttu-id="2dcd4-107">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2dcd4-107">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2dcd4-108">IMAPIForm</span><span class="sxs-lookup"><span data-stu-id="2dcd4-108">IMAPIForm</span></span>](imapiformiunknown.md) <br/> |<span data-ttu-id="2dcd4-109">Bearbeiten der Formular-Objekte und Form-Objektbefehle behandelt.</span><span class="sxs-lookup"><span data-stu-id="2dcd4-109">Manipulates form objects and handles form object commands.</span></span>  <br/> |
|[<span data-ttu-id="2dcd4-110">IMAPIFormAdviseSink</span><span class="sxs-lookup"><span data-stu-id="2dcd4-110">IMAPIFormAdviseSink</span></span>](imapiformadvisesinkiunknown.md) <br/> |<span data-ttu-id="2dcd4-111">Bestimmt, ob das Form-Objekt die nächste Nachricht verarbeiten kann und den nächsten oder vorherigen Zustand des Form-Objekts ändert.</span><span class="sxs-lookup"><span data-stu-id="2dcd4-111">Determines if the form object can handle the next message and changes the next or previous state of the form object.</span></span>  <br/> |
|[<span data-ttu-id="2dcd4-112">IMAPIFormContainer</span><span class="sxs-lookup"><span data-stu-id="2dcd4-112">IMAPIFormContainer</span></span>](imapiformcontaineriunknown.md) <br/> |<span data-ttu-id="2dcd4-113">Unterstützt die Installation, Deinstallation und Auflösung von Servern für ein bestimmtes Formular Container Formular.</span><span class="sxs-lookup"><span data-stu-id="2dcd4-113">Supports installation, deinstallation, and resolution of form servers against a specific form container.</span></span>  <br/> |
|[<span data-ttu-id="2dcd4-114">IMAPIFormFactory</span><span class="sxs-lookup"><span data-stu-id="2dcd4-114">IMAPIFormFactory</span></span>](imapiformfactoryiunknown.md) <br/> |<span data-ttu-id="2dcd4-115">Unterstützt die Verwendung von Servern konfigurierbar Laufzeit-Formular.</span><span class="sxs-lookup"><span data-stu-id="2dcd4-115">Supports the use of configurable run-time form servers.</span></span>  <br/> |
|[<span data-ttu-id="2dcd4-116">IMAPIFormInfo</span><span class="sxs-lookup"><span data-stu-id="2dcd4-116">IMAPIFormInfo</span></span>](imapiforminfoimapiprop.md) <br/> |<span data-ttu-id="2dcd4-117">Ermöglicht Clientanwendungen zum Arbeiten mit Eigenschaften, die für eine Nachrichtenklasse spezifisch sind.</span><span class="sxs-lookup"><span data-stu-id="2dcd4-117">Enables client applications to work with properties that are specific to a message class.</span></span>  <br/> |
|[<span data-ttu-id="2dcd4-118">IMAPIFormMgr</span><span class="sxs-lookup"><span data-stu-id="2dcd4-118">IMAPIFormMgr</span></span>](imapiformmgriunknown.md) <br/> |<span data-ttu-id="2dcd4-119">Ermöglicht Clientanwendungen zum Abrufen von Informationen zu Servern Formular, Formular Server aktiviert und Formular Servern im Nachrichtensystem installiert.</span><span class="sxs-lookup"><span data-stu-id="2dcd4-119">Enables client applications to get information about form servers, activates form servers, and installs form servers in the messaging system.</span></span>  <br/> |
|[<span data-ttu-id="2dcd4-120">IMAPIMessageSite</span><span class="sxs-lookup"><span data-stu-id="2dcd4-120">IMAPIMessageSite</span></span>](imapimessagesiteiunknown.md) <br/> |<span data-ttu-id="2dcd4-121">Zum Bearbeiten von Formularobjekten zugeordneten Nachrichten verwendet.</span><span class="sxs-lookup"><span data-stu-id="2dcd4-121">Used to manipulate messages associated with form objects.</span></span>  <br/> |
|[<span data-ttu-id="2dcd4-122">IMAPIViewAdviseSink</span><span class="sxs-lookup"><span data-stu-id="2dcd4-122">IMAPIViewAdviseSink</span></span>](imapiviewadvisesinkiunknown.md) <br/> |<span data-ttu-id="2dcd4-123">Benachrichtigt die Clientanwendungen, die in das Form-Objekt ein Ereignis aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="2dcd4-123">Notifies client applications that an event has occurred in the form object.</span></span>  <br/> |
|[<span data-ttu-id="2dcd4-124">IMAPIViewContext</span><span class="sxs-lookup"><span data-stu-id="2dcd4-124">IMAPIViewContext</span></span>](imapiviewcontextiunknown.md) <br/> |<span data-ttu-id="2dcd4-125">Zum Reagieren auf Next, Previous und Delete-Befehle in das Form-Objekt verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="2dcd4-125">Used to respond to Next, Previous, and Delete commands in the form object.</span></span>  <br/> |
|[<span data-ttu-id="2dcd4-126">IPersistMessage</span><span class="sxs-lookup"><span data-stu-id="2dcd4-126">IPersistMessage</span></span>](ipersistmessageiunknown.md) <br/> |<span data-ttu-id="2dcd4-127">Verwendet, um speichern, initialisieren, und Laden Formularobjekte von und zu speichern.</span><span class="sxs-lookup"><span data-stu-id="2dcd4-127">Used to save, initialize, and load form objects to and from message storage.</span></span>  <br/> |
   
<span data-ttu-id="2dcd4-128">Weitere Informationen zu den Methoden der MAPI-Formulars Schnittstellen finden Sie unter Dokumentation für diese Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="2dcd4-128">For more information about the methods of the MAPI form interfaces, see the documentation for these interfaces.</span></span> <span data-ttu-id="2dcd4-129">Sie müssen nicht alle MAPI-Formulars Schnittstellen implementieren, um ein benutzerdefiniertes Formular erstellen.</span><span class="sxs-lookup"><span data-stu-id="2dcd4-129">You do not have to implement all of the MAPI form interfaces in order to create a custom form.</span></span> <span data-ttu-id="2dcd4-130">Ein Formular selbst erfordert nur, dass Sie die **IPersistMessage**, **IMAPIForm**, implementieren und **IMAPIFormAdviseSink** Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="2dcd4-130">A form itself requires only that you implement the **IPersistMessage**, **IMAPIForm**, and **IMAPIFormAdviseSink** interfaces.</span></span> <span data-ttu-id="2dcd4-131">Darüber hinaus ist es ratsam, **IMAPIFormFactory** und **IMAPIFormInfo**implementieren.</span><span class="sxs-lookup"><span data-stu-id="2dcd4-131">Additionally, it is also a good idea to implement **IMAPIFormFactory** and **IMAPIFormInfo**.</span></span> <span data-ttu-id="2dcd4-132">**IMAPIFormFactory** eignet sich für die Einhaltung der OLE und **IMAPIFormInfo** ermöglicht gut geschriebenem Clientanwendungen von Formularen besser zu nutzen.</span><span class="sxs-lookup"><span data-stu-id="2dcd4-132">**IMAPIFormFactory** is useful for OLE compliance, and **IMAPIFormInfo** enables well-written client applications to make better use of your forms.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="2dcd4-133">Eigentlich ist **IMAPIFormAdviseSink** eine optionale Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="2dcd4-133">Strictly speaking, **IMAPIFormAdviseSink** is an optional interface.</span></span> <span data-ttu-id="2dcd4-134">Jedoch wird dringend empfohlen, dass Sie es in Ihren Servern Formular implementieren.</span><span class="sxs-lookup"><span data-stu-id="2dcd4-134">However, it is strongly recommended that you implement it in your form servers.</span></span> <span data-ttu-id="2dcd4-135">Diese Schnittstelle ist entscheidend für effiziente Interaktion zwischen messaging-Clients und Servern Formular, insbesondere wenn mehrere Nachrichten Ihres Formulars Servers Klasse die Nachricht wird behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="2dcd4-135">This interface is critical to efficient interaction between messaging clients and form servers, especially when several messages of your form server's message class are being dealt with.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2dcd4-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2dcd4-136">See also</span></span>



[<span data-ttu-id="2dcd4-137">MAPI-Formulare</span><span class="sxs-lookup"><span data-stu-id="2dcd4-137">MAPI Forms</span></span>](mapi-forms.md)

