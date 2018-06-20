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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 42e2633ac6d534be2c75c47b24c1da5ed9771e18
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792679"
---
# <a name="imslogon--iunknown"></a><span data-ttu-id="9f913-103">IMSLogon: IUnknown</span><span class="sxs-lookup"><span data-stu-id="9f913-103">IMSLogon : IUnknown</span></span>

  
  
<span data-ttu-id="9f913-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9f913-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9f913-105">Greift auf Ressourcen in einer Nachricht speichern Anmeldeobjekt.</span><span class="sxs-lookup"><span data-stu-id="9f913-105">Accesses resources in a message store logon object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9f913-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="9f913-106">Header file:</span></span>  <br/> |<span data-ttu-id="9f913-107">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="9f913-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="9f913-108">Verf�gbar gemacht von:</span><span class="sxs-lookup"><span data-stu-id="9f913-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="9f913-109">Nachricht Store Logon-Objekten</span><span class="sxs-lookup"><span data-stu-id="9f913-109">Message store logon objects</span></span>  <br/> |
|<span data-ttu-id="9f913-110">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="9f913-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="9f913-111">Nachricht-Anbieter</span><span class="sxs-lookup"><span data-stu-id="9f913-111">Message store providers</span></span>  <br/> |
|<span data-ttu-id="9f913-112">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="9f913-112">Called by:</span></span>  <br/> |<span data-ttu-id="9f913-113">MAPI</span><span class="sxs-lookup"><span data-stu-id="9f913-113">MAPI</span></span>  <br/> |
|<span data-ttu-id="9f913-114">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="9f913-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="9f913-115">IID_IMSLogon</span><span class="sxs-lookup"><span data-stu-id="9f913-115">IID_IMSLogon</span></span>  <br/> |
|<span data-ttu-id="9f913-116">Zeigertyp:</span><span class="sxs-lookup"><span data-stu-id="9f913-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="9f913-117">LPMSLOGON</span><span class="sxs-lookup"><span data-stu-id="9f913-117">LPMSLOGON</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="9f913-118">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="9f913-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="9f913-119">GetLastError</span><span class="sxs-lookup"><span data-stu-id="9f913-119">GetLastError</span></span>](imslogon-getlasterror.md) <br/> |<span data-ttu-id="9f913-120">Gibt eine [MAPIERROR](mapierror.md) -Struktur, die Informationen über den letzten Fehler enthält, die für das Store-Nachrichtenspeicherobjekt aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="9f913-120">Returns a [MAPIERROR](mapierror.md) structure that contains information about the last error that occurred for the message store object.</span></span>  <br/> |
|[<span data-ttu-id="9f913-121">Logoff</span><span class="sxs-lookup"><span data-stu-id="9f913-121">Logoff</span></span>](imslogon-logoff.md) <br/> |<span data-ttu-id="9f913-122">Eine Nachricht Abmeldung Speicheranbieter.</span><span class="sxs-lookup"><span data-stu-id="9f913-122">Logs off a message store provider.</span></span>  <br/> |
|[<span data-ttu-id="9f913-123">OpenEntry</span><span class="sxs-lookup"><span data-stu-id="9f913-123">OpenEntry</span></span>](imslogon-openentry.md) <br/> |<span data-ttu-id="9f913-124">Öffnet einen Ordner oder Message-Objekt und gibt einen Zeiger auf das Objekt, das Zugriff zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="9f913-124">Opens a folder or message object and returns a pointer to the object to provide further access.</span></span>  <br/> |
|[<span data-ttu-id="9f913-125">CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="9f913-125">CompareEntryIDs</span></span>](imslogon-compareentryids.md) <br/> |<span data-ttu-id="9f913-126">Vergleicht zwei Eintragsbezeichner, um zu bestimmen, ob sie sich auf dasselbe Objekt verweisen.</span><span class="sxs-lookup"><span data-stu-id="9f913-126">Compares two entry identifiers to determine whether they refer to the same object.</span></span>  <br/> |
|[<span data-ttu-id="9f913-127">Beraten</span><span class="sxs-lookup"><span data-stu-id="9f913-127">Advise</span></span>](imslogon-advise.md) <br/> |<span data-ttu-id="9f913-128">Registriert ein Objekt mit einem Anbieter für Benachrichtigungen zu Änderungen im Nachrichtenspeicher Nachricht.</span><span class="sxs-lookup"><span data-stu-id="9f913-128">Registers an object with a message store provider for notifications about changes in the message store.</span></span>  <br/> |
|[<span data-ttu-id="9f913-129">Heben Sie diesen Vorgang</span><span class="sxs-lookup"><span data-stu-id="9f913-129">Unadvise</span></span>](imslogon-unadvise.md) <br/> |<span data-ttu-id="9f913-130">Entfernt ein Objekt Anmeldungsseite für Benachrichtigung über Message Store Änderungen, die zuvor durch einen Aufruf an die **IMSLogon::Advise** -Methode festgelegt.</span><span class="sxs-lookup"><span data-stu-id="9f913-130">Removes an object's registration for notification of message store changes previously established by using a call to the **IMSLogon::Advise** method.</span></span>  <br/> |
|[<span data-ttu-id="9f913-131">OpenStatusEntry</span><span class="sxs-lookup"><span data-stu-id="9f913-131">OpenStatusEntry</span></span>](imslogon-openstatusentry.md) <br/> |<span data-ttu-id="9f913-132">Öffnet ein Statusobjekt.</span><span class="sxs-lookup"><span data-stu-id="9f913-132">Opens a status object.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9f913-133">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9f913-133">Remarks</span></span>

<span data-ttu-id="9f913-134">Message Store Anmeldung-Objekts ist der Teil einer geöffneten Nachricht Speicheranbieter, die MAPI direkt aufruft.</span><span class="sxs-lookup"><span data-stu-id="9f913-134">The message store logon object is the part of an open message store provider that MAPI calls directly.</span></span> <span data-ttu-id="9f913-135">Es gibt eine 1: 1-Beziehung zwischen Message Store Anmeldung-Objekts, die MAPI-Aufrufe und die Nachricht Objekt speichern, die Clientanwendungen aufrufen. Sie können vorstellen der Anmeldung und Speichern von Objekten als ein Objekt, das zwei Schnittstellen verfügbar macht.</span><span class="sxs-lookup"><span data-stu-id="9f913-135">There is a one-to-one correspondence between the message store logon object that MAPI calls and the message store object that client applications call; you can think of the logon and store objects as one object that exposes two interfaces.</span></span> <span data-ttu-id="9f913-136">Die zwei Objekte werden zusammen und freigegebenen zusammen erstellt.</span><span class="sxs-lookup"><span data-stu-id="9f913-136">The two objects are created together and freed together.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9f913-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9f913-137">See also</span></span>



[<span data-ttu-id="9f913-138">MAPI-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="9f913-138">MAPI Interfaces</span></span>](mapi-interfaces.md)

