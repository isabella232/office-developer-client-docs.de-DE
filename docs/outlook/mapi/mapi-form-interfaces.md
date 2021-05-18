---
title: MAPI-Formularschnittstellen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 611213c9-e758-4366-b193-fc62181d3d1f
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: f207f9550c61ad69fd1fc560cdb2084b7bb56c6f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412345"
---
# <a name="mapi-form-interfaces"></a><span data-ttu-id="7f2b1-103">MAPI-Formularschnittstellen</span><span class="sxs-lookup"><span data-stu-id="7f2b1-103">MAPI Form Interfaces</span></span>

  
  
<span data-ttu-id="7f2b1-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7f2b1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7f2b1-105">MAPI definiert die folgenden Schnittstellen in Bezug auf Formulare.</span><span class="sxs-lookup"><span data-stu-id="7f2b1-105">MAPI defines the following interfaces relating to forms.</span></span>
  
|<span data-ttu-id="7f2b1-106">**Schnittstellenname**</span><span class="sxs-lookup"><span data-stu-id="7f2b1-106">**Interface name**</span></span>|<span data-ttu-id="7f2b1-107">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7f2b1-107">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7f2b1-108">IMAPIForm</span><span class="sxs-lookup"><span data-stu-id="7f2b1-108">IMAPIForm</span></span>](imapiformiunknown.md) <br/> |<span data-ttu-id="7f2b1-109">Bearbeitet Formularobjekte und verarbeitet Formularobjektbefehle.</span><span class="sxs-lookup"><span data-stu-id="7f2b1-109">Manipulates form objects and handles form object commands.</span></span>  <br/> |
|[<span data-ttu-id="7f2b1-110">IMAPIFormAdviseSink</span><span class="sxs-lookup"><span data-stu-id="7f2b1-110">IMAPIFormAdviseSink</span></span>](imapiformadvisesinkiunknown.md) <br/> |<span data-ttu-id="7f2b1-111">Bestimmt, ob das Formularobjekt die nächste Nachricht verarbeiten kann, und ändert den nächsten oder vorherigen Status des Formularobjekts.</span><span class="sxs-lookup"><span data-stu-id="7f2b1-111">Determines if the form object can handle the next message and changes the next or previous state of the form object.</span></span>  <br/> |
|[<span data-ttu-id="7f2b1-112">IMAPIFormContainer</span><span class="sxs-lookup"><span data-stu-id="7f2b1-112">IMAPIFormContainer</span></span>](imapiformcontaineriunknown.md) <br/> |<span data-ttu-id="7f2b1-113">Unterstützt die Installation, Deinstallation und Auflösung von Formularservern für einen bestimmten Formularcontainer.</span><span class="sxs-lookup"><span data-stu-id="7f2b1-113">Supports installation, deinstallation, and resolution of form servers against a specific form container.</span></span>  <br/> |
|[<span data-ttu-id="7f2b1-114">IMAPIFormFactory</span><span class="sxs-lookup"><span data-stu-id="7f2b1-114">IMAPIFormFactory</span></span>](imapiformfactoryiunknown.md) <br/> |<span data-ttu-id="7f2b1-115">Unterstützt die Verwendung konfigurierbarer Laufzeitformularserver.</span><span class="sxs-lookup"><span data-stu-id="7f2b1-115">Supports the use of configurable run-time form servers.</span></span>  <br/> |
|[<span data-ttu-id="7f2b1-116">IMAPIFormInfo</span><span class="sxs-lookup"><span data-stu-id="7f2b1-116">IMAPIFormInfo</span></span>](imapiforminfoimapiprop.md) <br/> |<span data-ttu-id="7f2b1-117">Ermöglicht Clientanwendungen die Arbeit mit Eigenschaften, die für eine Nachrichtenklasse spezifisch sind.</span><span class="sxs-lookup"><span data-stu-id="7f2b1-117">Enables client applications to work with properties that are specific to a message class.</span></span>  <br/> |
|[<span data-ttu-id="7f2b1-118">IMAPIFormMgr</span><span class="sxs-lookup"><span data-stu-id="7f2b1-118">IMAPIFormMgr</span></span>](imapiformmgriunknown.md) <br/> |<span data-ttu-id="7f2b1-119">Ermöglicht Clientanwendungen, Informationen zu Formularservern zu erhalten, Formularserver zu aktivieren und Formularserver im Messagingsystem zu installieren.</span><span class="sxs-lookup"><span data-stu-id="7f2b1-119">Enables client applications to get information about form servers, activates form servers, and installs form servers in the messaging system.</span></span>  <br/> |
|[<span data-ttu-id="7f2b1-120">IMAPIMessageSite</span><span class="sxs-lookup"><span data-stu-id="7f2b1-120">IMAPIMessageSite</span></span>](imapimessagesiteiunknown.md) <br/> |<span data-ttu-id="7f2b1-121">Wird verwendet, um Nachrichten zu bearbeiten, die Formularobjekten zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="7f2b1-121">Used to manipulate messages associated with form objects.</span></span>  <br/> |
|[<span data-ttu-id="7f2b1-122">IMAPIViewAdviseSink</span><span class="sxs-lookup"><span data-stu-id="7f2b1-122">IMAPIViewAdviseSink</span></span>](imapiviewadvisesinkiunknown.md) <br/> |<span data-ttu-id="7f2b1-123">Benachrichtigt Clientanwendungen, dass ein Ereignis im Formularobjekt aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="7f2b1-123">Notifies client applications that an event has occurred in the form object.</span></span>  <br/> |
|[<span data-ttu-id="7f2b1-124">IMAPIViewContext</span><span class="sxs-lookup"><span data-stu-id="7f2b1-124">IMAPIViewContext</span></span>](imapiviewcontextiunknown.md) <br/> |<span data-ttu-id="7f2b1-125">Wird verwendet, um auf die Befehle Next, Previous und Delete im Formularobjekt zu reagieren.</span><span class="sxs-lookup"><span data-stu-id="7f2b1-125">Used to respond to Next, Previous, and Delete commands in the form object.</span></span>  <br/> |
|[<span data-ttu-id="7f2b1-126">IPersistMessage</span><span class="sxs-lookup"><span data-stu-id="7f2b1-126">IPersistMessage</span></span>](ipersistmessageiunknown.md) <br/> |<span data-ttu-id="7f2b1-127">Wird zum Speichern, Initialisieren und Laden von Formularobjekten in und aus dem Nachrichtenspeicher verwendet.</span><span class="sxs-lookup"><span data-stu-id="7f2b1-127">Used to save, initialize, and load form objects to and from message storage.</span></span>  <br/> |
   
<span data-ttu-id="7f2b1-128">Weitere Informationen zu den Methoden der MAPI-Formularschnittstellen finden Sie in der Dokumentation zu diesen Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="7f2b1-128">For more information about the methods of the MAPI form interfaces, see the documentation for these interfaces.</span></span> <span data-ttu-id="7f2b1-129">Sie müssen nicht alle MAPI-Formularschnittstellen implementieren, um ein benutzerdefiniertes Formular zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="7f2b1-129">You do not have to implement all of the MAPI form interfaces in order to create a custom form.</span></span> <span data-ttu-id="7f2b1-130">Ein Formular selbst erfordert nur, dass Sie die **Schnittstellen IPersistMessage,** **IMAPIForm** und **IMAPIFormAdviseSink** implementieren.</span><span class="sxs-lookup"><span data-stu-id="7f2b1-130">A form itself requires only that you implement the **IPersistMessage**, **IMAPIForm**, and **IMAPIFormAdviseSink** interfaces.</span></span> <span data-ttu-id="7f2b1-131">Darüber hinaus ist es auch eine gute Idee, **IMAPIFormFactory** und **IMAPIFormInfo zu implementieren.**</span><span class="sxs-lookup"><span data-stu-id="7f2b1-131">Additionally, it is also a good idea to implement **IMAPIFormFactory** and **IMAPIFormInfo**.</span></span> <span data-ttu-id="7f2b1-132">**IMAPIFormFactory ist** nützlich für die OLE-Compliance, und **IMAPIFormInfo** ermöglicht gut geschriebenen Clientanwendungen eine bessere Nutzung Ihrer Formulare.</span><span class="sxs-lookup"><span data-stu-id="7f2b1-132">**IMAPIFormFactory** is useful for OLE compliance, and **IMAPIFormInfo** enables well-written client applications to make better use of your forms.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="7f2b1-133">Genau genommen ist **IMAPIFormAdviseSink** eine optionale Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="7f2b1-133">Strictly speaking, **IMAPIFormAdviseSink** is an optional interface.</span></span> <span data-ttu-id="7f2b1-134">Es wird jedoch dringend empfohlen, sie auf Ihren Formularservern zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="7f2b1-134">However, it is strongly recommended that you implement it in your form servers.</span></span> <span data-ttu-id="7f2b1-135">Diese Schnittstelle ist entscheidend für die effiziente Interaktion zwischen Messagingclients und Formularservern, insbesondere wenn mehrere Nachrichten der Nachrichtenklasse des Formularservers behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="7f2b1-135">This interface is critical to efficient interaction between messaging clients and form servers, especially when several messages of your form server's message class are being dealt with.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7f2b1-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7f2b1-136">See also</span></span>



[<span data-ttu-id="7f2b1-137">MAPI-Formulare</span><span class="sxs-lookup"><span data-stu-id="7f2b1-137">MAPI Forms</span></span>](mapi-forms.md)

