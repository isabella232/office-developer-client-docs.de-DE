---
title: IMSLogon IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSLogon
api_type:
- COM
ms.assetid: d87093dc-f705-465f-ab3c-944ca0cd3e54
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 991e48aa458a58ad2d7d688e81dbb357ef9bda5b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428879"
---
# <a name="imslogon--iunknown"></a><span data-ttu-id="35660-103">IMSLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="35660-103">IMSLogon : IUnknown</span></span>

  
  
<span data-ttu-id="35660-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="35660-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="35660-105">Accesses resources in a message store logon object.</span><span class="sxs-lookup"><span data-stu-id="35660-105">Accesses resources in a message store logon object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="35660-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="35660-106">Header file:</span></span>  <br/> |<span data-ttu-id="35660-107">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="35660-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="35660-108">Verf�gbar gemacht von:</span><span class="sxs-lookup"><span data-stu-id="35660-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="35660-109">Anmeldeobjekte des Nachrichtenspeichers</span><span class="sxs-lookup"><span data-stu-id="35660-109">Message store logon objects</span></span>  <br/> |
|<span data-ttu-id="35660-110">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="35660-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="35660-111">Anbieter von Nachrichtenspeichern</span><span class="sxs-lookup"><span data-stu-id="35660-111">Message store providers</span></span>  <br/> |
|<span data-ttu-id="35660-112">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="35660-112">Called by:</span></span>  <br/> |<span data-ttu-id="35660-113">MAPI</span><span class="sxs-lookup"><span data-stu-id="35660-113">MAPI</span></span>  <br/> |
|<span data-ttu-id="35660-114">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="35660-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="35660-115">IID_IMSLogon</span><span class="sxs-lookup"><span data-stu-id="35660-115">IID_IMSLogon</span></span>  <br/> |
|<span data-ttu-id="35660-116">Zeigertyp:</span><span class="sxs-lookup"><span data-stu-id="35660-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="35660-117">LPMSLOGON</span><span class="sxs-lookup"><span data-stu-id="35660-117">LPMSLOGON</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="35660-118">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="35660-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="35660-119">GetLastError</span><span class="sxs-lookup"><span data-stu-id="35660-119">GetLastError</span></span>](imslogon-getlasterror.md) <br/> |<span data-ttu-id="35660-120">Gibt eine [MAPIERROR-Struktur](mapierror.md) zurück, die Informationen zum letzten Fehler enthält, der für das Nachrichtenspeicherobjekt aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="35660-120">Returns a [MAPIERROR](mapierror.md) structure that contains information about the last error that occurred for the message store object.</span></span>  <br/> |
|[<span data-ttu-id="35660-121">Logoff</span><span class="sxs-lookup"><span data-stu-id="35660-121">Logoff</span></span>](imslogon-logoff.md) <br/> |<span data-ttu-id="35660-122">Protokolliert einen Nachrichtenspeicheranbieter.</span><span class="sxs-lookup"><span data-stu-id="35660-122">Logs off a message store provider.</span></span>  <br/> |
|[<span data-ttu-id="35660-123">OpenEntry</span><span class="sxs-lookup"><span data-stu-id="35660-123">OpenEntry</span></span>](imslogon-openentry.md) <br/> |<span data-ttu-id="35660-124">Öffnet einen Ordner oder ein Nachrichtenobjekt und gibt einen Zeiger auf das Objekt zurück, um weiteren Zugriff zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="35660-124">Opens a folder or message object and returns a pointer to the object to provide further access.</span></span>  <br/> |
|[<span data-ttu-id="35660-125">CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="35660-125">CompareEntryIDs</span></span>](imslogon-compareentryids.md) <br/> |<span data-ttu-id="35660-126">Vergleicht zwei Eintragsbezeichner, um zu bestimmen, ob sie auf dasselbe Objekt verweisen.</span><span class="sxs-lookup"><span data-stu-id="35660-126">Compares two entry identifiers to determine whether they refer to the same object.</span></span>  <br/> |
|[<span data-ttu-id="35660-127">Raten</span><span class="sxs-lookup"><span data-stu-id="35660-127">Advise</span></span>](imslogon-advise.md) <br/> |<span data-ttu-id="35660-128">Registriert ein Objekt bei einem Nachrichtenspeicheranbieter für Benachrichtigungen über Änderungen im Nachrichtenspeicher.</span><span class="sxs-lookup"><span data-stu-id="35660-128">Registers an object with a message store provider for notifications about changes in the message store.</span></span>  <br/> |
|[<span data-ttu-id="35660-129">Unadvise</span><span class="sxs-lookup"><span data-stu-id="35660-129">Unadvise</span></span>](imslogon-unadvise.md) <br/> |<span data-ttu-id="35660-130">Entfernt die Registrierung eines Objekts zur Benachrichtigung über Nachrichtenspeicheränderungen, die zuvor mithilfe eines Aufrufs der **IMSLogon::Advise-Methode erstellt** wurden.</span><span class="sxs-lookup"><span data-stu-id="35660-130">Removes an object's registration for notification of message store changes previously established by using a call to the **IMSLogon::Advise** method.</span></span>  <br/> |
|[<span data-ttu-id="35660-131">OpenStatusEntry</span><span class="sxs-lookup"><span data-stu-id="35660-131">OpenStatusEntry</span></span>](imslogon-openstatusentry.md) <br/> |<span data-ttu-id="35660-132">Öffnet ein Statusobjekt.</span><span class="sxs-lookup"><span data-stu-id="35660-132">Opens a status object.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="35660-133">Hinweise</span><span class="sxs-lookup"><span data-stu-id="35660-133">Remarks</span></span>

<span data-ttu-id="35660-134">Das Anmeldeobjekt des Nachrichtenspeichers ist Teil eines geöffneten Nachrichtenspeicheranbieters, den MAPI direkt aufruft.</span><span class="sxs-lookup"><span data-stu-id="35660-134">The message store logon object is the part of an open message store provider that MAPI calls directly.</span></span> <span data-ttu-id="35660-135">Es besteht eine 1:1-Entsprechung zwischen dem von MAPI aufruften Anmeldeobjekt des Nachrichtenspeichers und dem Nachrichtenspeicherobjekt, das Clientanwendungen aufrufen. Sie können sich die Anmeldung und das Speichern von Objekten als ein Objekt ausbilden, das zwei Schnittstellen verfügbar macht.</span><span class="sxs-lookup"><span data-stu-id="35660-135">There is a one-to-one correspondence between the message store logon object that MAPI calls and the message store object that client applications call; you can think of the logon and store objects as one object that exposes two interfaces.</span></span> <span data-ttu-id="35660-136">Die beiden Objekte werden zusammen erstellt und gemeinsam frei.</span><span class="sxs-lookup"><span data-stu-id="35660-136">The two objects are created together and freed together.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="35660-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="35660-137">See also</span></span>



[<span data-ttu-id="35660-138">MAPI-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="35660-138">MAPI Interfaces</span></span>](mapi-interfaces.md)

