---
title: CloseIMsgSession
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.CloseIMsgSession
api_type:
- COM
ms.assetid: a0a17309-fc59-4822-be9b-b6f623b68bb1
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 877bebf0a156c99907505d815ca8d36a4b398678
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412037"
---
# <a name="closeimsgsession"></a><span data-ttu-id="4920b-103">CloseIMsgSession</span><span class="sxs-lookup"><span data-stu-id="4920b-103">CloseIMsgSession</span></span>

  
  
<span data-ttu-id="4920b-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4920b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4920b-105">Schließt eine Nachrichtensitzung und alle in dieser Sitzung erstellten Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="4920b-105">Closes a message session and all the messages created within that session.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4920b-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="4920b-106">Header file:</span></span>  <br/> |<span data-ttu-id="4920b-107">Imessage.h</span><span class="sxs-lookup"><span data-stu-id="4920b-107">Imessage.h</span></span>  <br/> |
|<span data-ttu-id="4920b-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="4920b-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="4920b-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="4920b-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="4920b-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="4920b-110">Called by:</span></span>  <br/> |<span data-ttu-id="4920b-111">Clientanwendungen und Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="4920b-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
VOID CloseIMsgSession(
  LPMSGSESS lpMsgSess
);
```

## <a name="parameters"></a><span data-ttu-id="4920b-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="4920b-112">Parameters</span></span>

 <span data-ttu-id="4920b-113">_lpMsgSess_</span><span class="sxs-lookup"><span data-stu-id="4920b-113">_lpMsgSess_</span></span>
  
> <span data-ttu-id="4920b-114">[in] Zeiger auf das Nachrichtensitzungsobjekt, das mit der [OpenIMsgSession-Funktion](openimsgsession.md) zu Beginn der Nachrichtensitzung erhalten wurde.</span><span class="sxs-lookup"><span data-stu-id="4920b-114">[in] Pointer to the message session object obtained using the [OpenIMsgSession](openimsgsession.md) function at the start of the message session.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="4920b-115">Return value</span><span class="sxs-lookup"><span data-stu-id="4920b-115">Return value</span></span>

<span data-ttu-id="4920b-116">Keine.</span><span class="sxs-lookup"><span data-stu-id="4920b-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4920b-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="4920b-117">Remarks</span></span>

<span data-ttu-id="4920b-118">Eine Nachrichtensitzung wird von Clientanwendungen und Dienstanbietern verwendet, die sich mit mehreren verwandten **MAPI-IMessage-Objekten** befassen möchten, die auf zugrunde liegenden OLE **IStorage-Objekten** aufgebaut sind.</span><span class="sxs-lookup"><span data-stu-id="4920b-118">A message session is used by client applications and service providers that want to deal with several related MAPI **IMessage** objects built on top of underlying OLE **IStorage** objects.</span></span> <span data-ttu-id="4920b-119">Der Client oder Anbieter verwendet die [Funktionen OpenIMsgSession](openimsgsession.md) und **CloseIMsgSession,** um die Erstellung solcher Nachrichten in einer Nachrichtensitzung zu umschließen.</span><span class="sxs-lookup"><span data-stu-id="4920b-119">The client or provider uses the [OpenIMsgSession](openimsgsession.md) and **CloseIMsgSession** functions to wrap the creation of such messages inside a message session.</span></span> <span data-ttu-id="4920b-120">Nachdem die Nachrichtensitzung geöffnet wurde, übergibt der Client oder Anbieter einen Zeiger an [openIMsgOnIStg,](openimsgonistg.md) um ein neues **IMessage**-on-IStorage-Objekt zu erstellen. </span><span class="sxs-lookup"><span data-stu-id="4920b-120">Once the message session is opened, the client or provider passes a pointer to it in a call to [OpenIMsgOnIStg](openimsgonistg.md) to create a new **IMessage**-on- **IStorage** object.</span></span> 
  
<span data-ttu-id="4920b-121">Eine Nachrichtensitzung verfolgt alle **IMessage** **-on-IStorage-Objekte,** die während der Sitzung geöffnet wurden, zusätzlich zu allen Anlagen und anderen Eigenschaften der Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="4920b-121">A message session keeps track of all **IMessage**-on- **IStorage** objects opened during the duration of the session, in addition to all the attachments and other properties of the messages.</span></span> <span data-ttu-id="4920b-122">Wenn ein Client oder Anbieter **CloseIMsgSession aufruft,** werden alle diese Objekte geschlossen.</span><span class="sxs-lookup"><span data-stu-id="4920b-122">When a client or provider calls **CloseIMsgSession**, it closes all these objects.</span></span> <span data-ttu-id="4920b-123">Das **Aufrufen von CloseIMsgSession** ist die einzige Möglichkeit, **IMessage**-on-IStorage-Objekte **zu** schließen.</span><span class="sxs-lookup"><span data-stu-id="4920b-123">Calling **CloseIMsgSession** is the only way to close **IMessage**-on- **IStorage** objects.</span></span> 
  

