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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: c190691c8cfcb9b049bcf9ee4f21436e20955def
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791413"
---
# <a name="closeimsgsession"></a><span data-ttu-id="5ae0e-103">CloseIMsgSession</span><span class="sxs-lookup"><span data-stu-id="5ae0e-103">CloseIMsgSession</span></span>

  
  
<span data-ttu-id="5ae0e-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5ae0e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5ae0e-105">Schließt eine Sofortnachrichtensitzung und alle Nachrichten, die in dieser Sitzung erstellt.</span><span class="sxs-lookup"><span data-stu-id="5ae0e-105">Closes a message session and all the messages created within that session.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5ae0e-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="5ae0e-106">Header file:</span></span>  <br/> |<span data-ttu-id="5ae0e-107">IMessage.h</span><span class="sxs-lookup"><span data-stu-id="5ae0e-107">Imessage.h</span></span>  <br/> |
|<span data-ttu-id="5ae0e-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="5ae0e-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="5ae0e-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="5ae0e-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="5ae0e-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="5ae0e-110">Called by:</span></span>  <br/> |<span data-ttu-id="5ae0e-111">Clientanwendungen und -Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="5ae0e-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
VOID CloseIMsgSession(
  LPMSGSESS lpMsgSess
);
```

## <a name="parameters"></a><span data-ttu-id="5ae0e-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="5ae0e-112">Parameters</span></span>

 <span data-ttu-id="5ae0e-113">_lpMsgSess_</span><span class="sxs-lookup"><span data-stu-id="5ae0e-113">_lpMsgSess_</span></span>
  
> <span data-ttu-id="5ae0e-114">[in] Zeiger auf das Objekt "Message" Sitzung mithilfe der Funktion [OpenIMsgSession](openimsgsession.md) am Anfang der Nachricht Sitzung abgerufen.</span><span class="sxs-lookup"><span data-stu-id="5ae0e-114">[in] Pointer to the message session object obtained using the [OpenIMsgSession](openimsgsession.md) function at the start of the message session.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="5ae0e-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5ae0e-115">Return value</span></span>

<span data-ttu-id="5ae0e-116">None.</span><span class="sxs-lookup"><span data-stu-id="5ae0e-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5ae0e-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5ae0e-117">Remarks</span></span>

<span data-ttu-id="5ae0e-118">Eine Sofortnachrichtensitzung wird von Clientanwendungen und Dienstanbieter, die für den Umgang mit mehrere verwandte MAPI- **IMessage** -Objekte auf der Basis zugrunde liegenden OLE **IStorage** -Objekte werden soll.</span><span class="sxs-lookup"><span data-stu-id="5ae0e-118">A message session is used by client applications and service providers that want to deal with several related MAPI **IMessage** objects built on top of underlying OLE **IStorage** objects.</span></span> <span data-ttu-id="5ae0e-119">Der Client oder Anbieter verwendet die Funktionen [OpenIMsgSession](openimsgsession.md) und **CloseIMsgSession** um die Erstellung solcher Nachrichten innerhalb einer Sofortnachrichtensitzung zu umschließen.</span><span class="sxs-lookup"><span data-stu-id="5ae0e-119">The client or provider uses the [OpenIMsgSession](openimsgsession.md) and **CloseIMsgSession** functions to wrap the creation of such messages inside a message session.</span></span> <span data-ttu-id="5ae0e-120">Sobald die Nachricht Sitzung geöffnet ist, übergibt der Client oder der Anbieter einen Zeiger auf es in einem Aufruf von [OpenIMsgOnIStg](openimsgonistg.md) zum Erstellen einer neuen **IMessage**- auf - **IStorage** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="5ae0e-120">Once the message session is opened, the client or provider passes a pointer to it in a call to [OpenIMsgOnIStg](openimsgonistg.md) to create a new **IMessage**-on- **IStorage** object.</span></span> 
  
<span data-ttu-id="5ae0e-121">Eine Sofortnachrichtensitzung werden von nachverfolgt alle **IMessage**- auf - **IStorage** -Objekte, die während der Dauer der Sitzung, zusätzlich zu aller Anlagen und andere Eigenschaften der Nachrichten geöffnet.</span><span class="sxs-lookup"><span data-stu-id="5ae0e-121">A message session keeps track of all **IMessage**-on- **IStorage** objects opened during the duration of the session, in addition to all the attachments and other properties of the messages.</span></span> <span data-ttu-id="5ae0e-122">Wenn ein Client oder Anbieter **CloseIMsgSession**aufruft, wird dieser Objekte geschlossen.</span><span class="sxs-lookup"><span data-stu-id="5ae0e-122">When a client or provider calls **CloseIMsgSession**, it closes all these objects.</span></span> <span data-ttu-id="5ae0e-123">**CloseIMsgSession** aufrufen, ist die einzige Möglichkeit **IMessage**- auf - **IStorage** -Objekte zu schließen.</span><span class="sxs-lookup"><span data-stu-id="5ae0e-123">Calling **CloseIMsgSession** is the only way to close **IMessage**-on- **IStorage** objects.</span></span> 
  

