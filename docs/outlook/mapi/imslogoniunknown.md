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
ms.openlocfilehash: 991e48aa458a58ad2d7d688e81dbb357ef9bda5b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348713"
---
# <a name="imslogon--iunknown"></a><span data-ttu-id="ce92b-103">IMSLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ce92b-103">IMSLogon : IUnknown</span></span>

  
  
<span data-ttu-id="ce92b-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ce92b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ce92b-105">Greift auf Ressourcen in einem Nachrichtenspeicher-Anmeldeobjekt zu.</span><span class="sxs-lookup"><span data-stu-id="ce92b-105">Accesses resources in a message store logon object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ce92b-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="ce92b-106">Header file:</span></span>  <br/> |<span data-ttu-id="ce92b-107">Mapispi. h</span><span class="sxs-lookup"><span data-stu-id="ce92b-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="ce92b-108">Verf�gbar gemacht von:</span><span class="sxs-lookup"><span data-stu-id="ce92b-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="ce92b-109">Nachrichtenspeicher-Anmeldeobjekte</span><span class="sxs-lookup"><span data-stu-id="ce92b-109">Message store logon objects</span></span>  <br/> |
|<span data-ttu-id="ce92b-110">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="ce92b-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="ce92b-111">Nachrichtenspeicher Anbieter</span><span class="sxs-lookup"><span data-stu-id="ce92b-111">Message store providers</span></span>  <br/> |
|<span data-ttu-id="ce92b-112">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="ce92b-112">Called by:</span></span>  <br/> |<span data-ttu-id="ce92b-113">MAPI</span><span class="sxs-lookup"><span data-stu-id="ce92b-113">MAPI</span></span>  <br/> |
|<span data-ttu-id="ce92b-114">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="ce92b-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="ce92b-115">IID_IMSLogon</span><span class="sxs-lookup"><span data-stu-id="ce92b-115">IID_IMSLogon</span></span>  <br/> |
|<span data-ttu-id="ce92b-116">Zeigertyp:</span><span class="sxs-lookup"><span data-stu-id="ce92b-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="ce92b-117">LPMSLOGON</span><span class="sxs-lookup"><span data-stu-id="ce92b-117">LPMSLOGON</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="ce92b-118">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="ce92b-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="ce92b-119">Getlasterroraufzurufen</span><span class="sxs-lookup"><span data-stu-id="ce92b-119">GetLastError</span></span>](imslogon-getlasterror.md) <br/> |<span data-ttu-id="ce92b-120">Gibt eine [MAPIERROR](mapierror.md) -Struktur zurück, die Informationen zum letzten Fehler enthält, der für das Nachrichtenspeicherobjekt aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="ce92b-120">Returns a [MAPIERROR](mapierror.md) structure that contains information about the last error that occurred for the message store object.</span></span>  <br/> |
|[<span data-ttu-id="ce92b-121">Logoff</span><span class="sxs-lookup"><span data-stu-id="ce92b-121">Logoff</span></span>](imslogon-logoff.md) <br/> |<span data-ttu-id="ce92b-122">Meldet einen Nachrichtenspeicher Anbieter ab.</span><span class="sxs-lookup"><span data-stu-id="ce92b-122">Logs off a message store provider.</span></span>  <br/> |
|[<span data-ttu-id="ce92b-123">OpenEntry</span><span class="sxs-lookup"><span data-stu-id="ce92b-123">OpenEntry</span></span>](imslogon-openentry.md) <br/> |<span data-ttu-id="ce92b-124">Öffnet ein Folder-oder Message-Objekt und gibt einen Zeiger auf das Objekt zurück, um weiteren Zugriff zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="ce92b-124">Opens a folder or message object and returns a pointer to the object to provide further access.</span></span>  <br/> |
|[<span data-ttu-id="ce92b-125">CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="ce92b-125">CompareEntryIDs</span></span>](imslogon-compareentryids.md) <br/> |<span data-ttu-id="ce92b-126">Vergleicht zwei Eintragsbezeichner, um zu bestimmen, ob Sie auf dasselbe Objekt verweisen.</span><span class="sxs-lookup"><span data-stu-id="ce92b-126">Compares two entry identifiers to determine whether they refer to the same object.</span></span>  <br/> |
|[<span data-ttu-id="ce92b-127">Beraten</span><span class="sxs-lookup"><span data-stu-id="ce92b-127">Advise</span></span>](imslogon-advise.md) <br/> |<span data-ttu-id="ce92b-128">Registriert ein Objekt bei einem Nachrichtenspeicher Anbieter für Benachrichtigungen zu Änderungen im Nachrichtenspeicher.</span><span class="sxs-lookup"><span data-stu-id="ce92b-128">Registers an object with a message store provider for notifications about changes in the message store.</span></span>  <br/> |
|[<span data-ttu-id="ce92b-129">Unadvise</span><span class="sxs-lookup"><span data-stu-id="ce92b-129">Unadvise</span></span>](imslogon-unadvise.md) <br/> |<span data-ttu-id="ce92b-130">Entfernt die Registrierung eines Objekts für die Benachrichtigung über Änderungen am Nachrichtenspeicher, die zuvor mithilfe eines Aufrufs der **IMSLogon:: Advise** -Methode festgelegt wurden.</span><span class="sxs-lookup"><span data-stu-id="ce92b-130">Removes an object's registration for notification of message store changes previously established by using a call to the **IMSLogon::Advise** method.</span></span>  <br/> |
|[<span data-ttu-id="ce92b-131">OpenStatusEntry</span><span class="sxs-lookup"><span data-stu-id="ce92b-131">OpenStatusEntry</span></span>](imslogon-openstatusentry.md) <br/> |<span data-ttu-id="ce92b-132">Öffnet ein Status-Objekt.</span><span class="sxs-lookup"><span data-stu-id="ce92b-132">Opens a status object.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ce92b-133">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ce92b-133">Remarks</span></span>

<span data-ttu-id="ce92b-134">Das Nachrichtenspeicher-Anmeldeobjekt ist der Teil eines geöffneten Nachrichtenspeicher Anbieters, der von MAPI direkt aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="ce92b-134">The message store logon object is the part of an open message store provider that MAPI calls directly.</span></span> <span data-ttu-id="ce92b-135">Es gibt eine 1:1-Entsprechung zwischen dem Nachrichtenspeicher-Anmeldeobjekt, das von MAPI aufgerufen wird, und dem Nachrichtenspeicherobjekt, das von Clientanwendungen aufgerufen wird; Sie können sich die Anmelde-und Speicherobjekte als ein Objekt vorstellen, das zwei Schnittstellen verfügbar macht.</span><span class="sxs-lookup"><span data-stu-id="ce92b-135">There is a one-to-one correspondence between the message store logon object that MAPI calls and the message store object that client applications call; you can think of the logon and store objects as one object that exposes two interfaces.</span></span> <span data-ttu-id="ce92b-136">Die beiden Objekte werden zusammen erstellt und gemeinsam freigegeben.</span><span class="sxs-lookup"><span data-stu-id="ce92b-136">The two objects are created together and freed together.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ce92b-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ce92b-137">See also</span></span>



[<span data-ttu-id="ce92b-138">MAPI-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="ce92b-138">MAPI Interfaces</span></span>](mapi-interfaces.md)

