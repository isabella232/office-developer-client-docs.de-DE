---
title: IABLogon IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon
api_type:
- COM
ms.assetid: fe340182-f41e-42e7-b8e8-cc005b1e9a5f
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 784430f1286c9a017337a0fae4b269757a56a3e8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791991"
---
# <a name="iablogon--iunknown"></a><span data-ttu-id="08bb9-103">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="08bb9-103">IABLogon : IUnknown</span></span>

  
  
<span data-ttu-id="08bb9-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="08bb9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="08bb9-105">Greift auf Ressourcen in einer Adressbuchanbieter.</span><span class="sxs-lookup"><span data-stu-id="08bb9-105">Accesses resources in an address book provider.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="08bb9-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="08bb9-106">Header file:</span></span>  <br/> |<span data-ttu-id="08bb9-107">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="08bb9-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="08bb9-108">Verfügbar gemacht von:</span><span class="sxs-lookup"><span data-stu-id="08bb9-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="08bb9-109">Address Book Logon-Objekten</span><span class="sxs-lookup"><span data-stu-id="08bb9-109">Address book logon objects</span></span>  <br/> |
|<span data-ttu-id="08bb9-110">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="08bb9-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="08bb9-111">Von adressbuchanbietern implementierte</span><span class="sxs-lookup"><span data-stu-id="08bb9-111">Address book providers</span></span>  <br/> |
|<span data-ttu-id="08bb9-112">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="08bb9-112">Called by:</span></span>  <br/> |<span data-ttu-id="08bb9-113">MAPI</span><span class="sxs-lookup"><span data-stu-id="08bb9-113">MAPI</span></span>  <br/> |
|<span data-ttu-id="08bb9-114">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="08bb9-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="08bb9-115">IID_IABLogon</span><span class="sxs-lookup"><span data-stu-id="08bb9-115">IID_IABLogon</span></span>  <br/> |
|<span data-ttu-id="08bb9-116">Zeigertyp:</span><span class="sxs-lookup"><span data-stu-id="08bb9-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="08bb9-117">LPABLOGON</span><span class="sxs-lookup"><span data-stu-id="08bb9-117">LPABLOGON</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="08bb9-118">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="08bb9-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="08bb9-119">GetLastError</span><span class="sxs-lookup"><span data-stu-id="08bb9-119">GetLastError</span></span>](iablogon-getlasterror.md) <br/> |<span data-ttu-id="08bb9-120">Gibt eine [MAPIERROR](mapierror.md) -Struktur, die Informationen über den vorherigen Address Book Anbieterfehler enthält.</span><span class="sxs-lookup"><span data-stu-id="08bb9-120">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous address book provider error.</span></span>  <br/> |
|[<span data-ttu-id="08bb9-121">Logoff</span><span class="sxs-lookup"><span data-stu-id="08bb9-121">Logoff</span></span>](iablogon-logoff.md) <br/> |<span data-ttu-id="08bb9-122">Initiiert den Prozess abmelden.</span><span class="sxs-lookup"><span data-stu-id="08bb9-122">Initiates the logoff process.</span></span>  <br/> |
|[<span data-ttu-id="08bb9-123">OpenEntry</span><span class="sxs-lookup"><span data-stu-id="08bb9-123">OpenEntry</span></span>](iablogon-openentry.md) <br/> |<span data-ttu-id="08bb9-124">Öffnet einen Container, messaging-Benutzer oder eine Verteilerliste, und gibt einen Zeiger auf eine Implementierung Zugriff zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="08bb9-124">Opens a container, messaging user, or distribution list, and returns a pointer to an interface implementation to provide further access.</span></span>  <br/> |
|[<span data-ttu-id="08bb9-125">CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="08bb9-125">CompareEntryIDs</span></span>](iablogon-compareentryids.md) <br/> |<span data-ttu-id="08bb9-126">Vergleicht zwei Eintragsbezeichner, um zu bestimmen, ob sie sich auf dasselbe Objekt verweisen.</span><span class="sxs-lookup"><span data-stu-id="08bb9-126">Compares two entry identifiers to determine whether they refer to the same object.</span></span>  <br/> |
|[<span data-ttu-id="08bb9-127">Beraten</span><span class="sxs-lookup"><span data-stu-id="08bb9-127">Advise</span></span>](iablogon-advise.md) <br/> |<span data-ttu-id="08bb9-128">Den Anrufer, um die Benachrichtigung der angegebenen Ereignisse, die einen Container, messaging-Benutzer oder Verteilerliste betreffen registriert.</span><span class="sxs-lookup"><span data-stu-id="08bb9-128">Registers the caller to receive notification of specified events that affect a container, messaging user, or distribution list.</span></span>  <br/> |
|[<span data-ttu-id="08bb9-129">Heben Sie diesen Vorgang</span><span class="sxs-lookup"><span data-stu-id="08bb9-129">Unadvise</span></span>](iablogon-unadvise.md) <br/> |<span data-ttu-id="08bb9-130">Benachrichtigungen, die zuvor mit einem Aufruf der **Advise** -Methode eingerichtet wurden, werden abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="08bb9-130">Cancels notifications that were previously set up with a call to the **Advise** method.</span></span>  <br/> |
|[<span data-ttu-id="08bb9-131">OpenStatusEntry</span><span class="sxs-lookup"><span data-stu-id="08bb9-131">OpenStatusEntry</span></span>](iablogon-openstatusentry.md) <br/> |<span data-ttu-id="08bb9-132">Öffnet den Anbieter Status-Objekt.</span><span class="sxs-lookup"><span data-stu-id="08bb9-132">Opens the provider's status object.</span></span>  <br/> |
|[<span data-ttu-id="08bb9-133">OpenTemplateID</span><span class="sxs-lookup"><span data-stu-id="08bb9-133">OpenTemplateID</span></span>](iablogon-opentemplateid.md) <br/> |<span data-ttu-id="08bb9-134">Öffnet einen Empfänger-Eintrag, der Daten in einer Host-Adressbuchanbieter hat.</span><span class="sxs-lookup"><span data-stu-id="08bb9-134">Opens a recipient entry that has data residing in a host address book provider.</span></span>  <br/> |
|[<span data-ttu-id="08bb9-135">GetOneOffTable</span><span class="sxs-lookup"><span data-stu-id="08bb9-135">GetOneOffTable</span></span>](iablogon-getoneofftable.md) <br/> |<span data-ttu-id="08bb9-136">Gibt eine Tabelle mit einmaligen Vorlagen zum Erstellen von Empfängern, die Empfängerliste von ausgehenden Nachrichten hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="08bb9-136">Returns a table of one-off templates for creating recipients to be added to the recipient list of an outgoing message.</span></span>  <br/> |
|[<span data-ttu-id="08bb9-137">PrepareRecips</span><span class="sxs-lookup"><span data-stu-id="08bb9-137">PrepareRecips</span></span>](iablogon-preparerecips.md) <br/> |<span data-ttu-id="08bb9-138">Bereitet eine Empfängerliste zur späteren Verwendung von messaging-System.</span><span class="sxs-lookup"><span data-stu-id="08bb9-138">Prepares a recipient list for later use by the messaging system.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="08bb9-139">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="08bb9-139">Remarks</span></span>

<span data-ttu-id="08bb9-140">Allgemeine Informationen zu den Methoden der **IABLogon** -Schnittstelle finden Sie unter [Implementieren Service Provider Anmeldung](implementing-service-provider-logon.md).</span><span class="sxs-lookup"><span data-stu-id="08bb9-140">For general information about the methods of the **IABLogon** interface, see [Implementing Service Provider Logon](implementing-service-provider-logon.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="08bb9-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="08bb9-141">See also</span></span>



[<span data-ttu-id="08bb9-142">MAPI-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="08bb9-142">MAPI Interfaces</span></span>](mapi-interfaces.md)

