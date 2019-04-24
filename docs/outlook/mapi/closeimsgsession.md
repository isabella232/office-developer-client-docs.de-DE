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
ms.openlocfilehash: 877bebf0a156c99907505d815ca8d36a4b398678
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334937"
---
# <a name="closeimsgsession"></a><span data-ttu-id="98308-103">CloseIMsgSession</span><span class="sxs-lookup"><span data-stu-id="98308-103">CloseIMsgSession</span></span>

  
  
<span data-ttu-id="98308-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="98308-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="98308-105">Schließt eine nachrichtensitzung und alle innerhalb dieser Sitzung erstellten Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="98308-105">Closes a message session and all the messages created within that session.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="98308-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="98308-106">Header file:</span></span>  <br/> |<span data-ttu-id="98308-107">IMessage. h</span><span class="sxs-lookup"><span data-stu-id="98308-107">Imessage.h</span></span>  <br/> |
|<span data-ttu-id="98308-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="98308-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="98308-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="98308-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="98308-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="98308-110">Called by:</span></span>  <br/> |<span data-ttu-id="98308-111">Client Anwendungen und Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="98308-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
VOID CloseIMsgSession(
  LPMSGSESS lpMsgSess
);
```

## <a name="parameters"></a><span data-ttu-id="98308-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="98308-112">Parameters</span></span>

 <span data-ttu-id="98308-113">_lpMsgSess_</span><span class="sxs-lookup"><span data-stu-id="98308-113">_lpMsgSess_</span></span>
  
> <span data-ttu-id="98308-114">in Zeiger auf das Nachrichten Sitzungsobjekt, das mit der [OpenIMsgSession](openimsgsession.md) -Funktion zu Beginn der nachrichtensitzung abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="98308-114">[in] Pointer to the message session object obtained using the [OpenIMsgSession](openimsgsession.md) function at the start of the message session.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="98308-115">Return value</span><span class="sxs-lookup"><span data-stu-id="98308-115">Return value</span></span>

<span data-ttu-id="98308-116">Keine.</span><span class="sxs-lookup"><span data-stu-id="98308-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="98308-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="98308-117">Remarks</span></span>

<span data-ttu-id="98308-118">Eine nachrichtensitzung wird von Clientanwendungen und Dienstanbietern verwendet, die mit mehreren verwandten MAPI- **IMessage** -Objekten umgehen möchten, die auf zugrunde liegenden OLE- **IStorage** -Objekten basieren.</span><span class="sxs-lookup"><span data-stu-id="98308-118">A message session is used by client applications and service providers that want to deal with several related MAPI **IMessage** objects built on top of underlying OLE **IStorage** objects.</span></span> <span data-ttu-id="98308-119">Der Client oder Anbieter verwendet die [OpenIMsgSession](openimsgsession.md) -und **CloseIMsgSession** -Funktionen, um die Erstellung solcher Nachrichten innerhalb einer nachrichtensitzung umzubrechen.</span><span class="sxs-lookup"><span data-stu-id="98308-119">The client or provider uses the [OpenIMsgSession](openimsgsession.md) and **CloseIMsgSession** functions to wrap the creation of such messages inside a message session.</span></span> <span data-ttu-id="98308-120">Nach dem Öffnen der nachrichtensitzung übergibt der Client oder Anbieter einen Zeiger an diesen in einem Aufruf an [OpenIMsgOnIStg](openimsgonistg.md) , um ein neues **IMessage**-on- **IStorage** -Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="98308-120">Once the message session is opened, the client or provider passes a pointer to it in a call to [OpenIMsgOnIStg](openimsgonistg.md) to create a new **IMessage**-on- **IStorage** object.</span></span> 
  
<span data-ttu-id="98308-121">Eine nachrichtensitzung verfolgt alle **IMessage**-on- **IStorage** -Objekte, die während der Dauer der Sitzung geöffnet werden, zusätzlich zu allen Anlagen und anderen Eigenschaften der Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="98308-121">A message session keeps track of all **IMessage**-on- **IStorage** objects opened during the duration of the session, in addition to all the attachments and other properties of the messages.</span></span> <span data-ttu-id="98308-122">Wenn ein Client oder Anbieter **CloseIMsgSession**aufruft, werden alle diese Objekte geschlossen.</span><span class="sxs-lookup"><span data-stu-id="98308-122">When a client or provider calls **CloseIMsgSession**, it closes all these objects.</span></span> <span data-ttu-id="98308-123">Das Aufrufen von **CloseIMsgSession** ist die einzige Möglichkeit zum Beenden von **IMessage**-on- **IStorage** -Objekten.</span><span class="sxs-lookup"><span data-stu-id="98308-123">Calling **CloseIMsgSession** is the only way to close **IMessage**-on- **IStorage** objects.</span></span> 
  

