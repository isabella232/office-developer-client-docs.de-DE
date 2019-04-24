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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: fc8615fcd984623ae9c17c45fb7b51a4498a723b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348832"
---
# <a name="iablogon--iunknown"></a><span data-ttu-id="69fb8-103">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="69fb8-103">IABLogon : IUnknown</span></span>

  
  
<span data-ttu-id="69fb8-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="69fb8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="69fb8-105">Greift auf Ressourcen in einem Adressbuchanbieter zu.</span><span class="sxs-lookup"><span data-stu-id="69fb8-105">Accesses resources in an address book provider.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="69fb8-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="69fb8-106">Header file:</span></span>  <br/> |<span data-ttu-id="69fb8-107">Mapispi. h</span><span class="sxs-lookup"><span data-stu-id="69fb8-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="69fb8-108">Verf�gbar gemacht von:</span><span class="sxs-lookup"><span data-stu-id="69fb8-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="69fb8-109">Adressbuch-Anmeldeobjekte</span><span class="sxs-lookup"><span data-stu-id="69fb8-109">Address book logon objects</span></span>  <br/> |
|<span data-ttu-id="69fb8-110">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="69fb8-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="69fb8-111">Adressbuchanbieter</span><span class="sxs-lookup"><span data-stu-id="69fb8-111">Address book providers</span></span>  <br/> |
|<span data-ttu-id="69fb8-112">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="69fb8-112">Called by:</span></span>  <br/> |<span data-ttu-id="69fb8-113">MAPI</span><span class="sxs-lookup"><span data-stu-id="69fb8-113">MAPI</span></span>  <br/> |
|<span data-ttu-id="69fb8-114">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="69fb8-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="69fb8-115">IID_IABLogon</span><span class="sxs-lookup"><span data-stu-id="69fb8-115">IID_IABLogon</span></span>  <br/> |
|<span data-ttu-id="69fb8-116">Zeigertyp:</span><span class="sxs-lookup"><span data-stu-id="69fb8-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="69fb8-117">LPABLOGON</span><span class="sxs-lookup"><span data-stu-id="69fb8-117">LPABLOGON</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="69fb8-118">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="69fb8-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="69fb8-119">Getlasterroraufzurufen</span><span class="sxs-lookup"><span data-stu-id="69fb8-119">GetLastError</span></span>](iablogon-getlasterror.md) <br/> |<span data-ttu-id="69fb8-120">Gibt eine [MAPIERROR](mapierror.md) -Struktur zurück, die Informationen zum vorherigen Fehler des Adressbuch Anbieters enthält.</span><span class="sxs-lookup"><span data-stu-id="69fb8-120">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous address book provider error.</span></span>  <br/> |
|[<span data-ttu-id="69fb8-121">Logoff</span><span class="sxs-lookup"><span data-stu-id="69fb8-121">Logoff</span></span>](iablogon-logoff.md) <br/> |<span data-ttu-id="69fb8-122">Initiiert den ABMELDEPROZESS.</span><span class="sxs-lookup"><span data-stu-id="69fb8-122">Initiates the logoff process.</span></span>  <br/> |
|[<span data-ttu-id="69fb8-123">OpenEntry</span><span class="sxs-lookup"><span data-stu-id="69fb8-123">OpenEntry</span></span>](iablogon-openentry.md) <br/> |<span data-ttu-id="69fb8-124">Öffnet einen Container, einen Messagingbenutzer oder eine Verteilerliste und gibt einen Zeiger auf eine Schnittstellenimplementierung zurück, um weiteren Zugriff zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="69fb8-124">Opens a container, messaging user, or distribution list, and returns a pointer to an interface implementation to provide further access.</span></span>  <br/> |
|[<span data-ttu-id="69fb8-125">CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="69fb8-125">CompareEntryIDs</span></span>](iablogon-compareentryids.md) <br/> |<span data-ttu-id="69fb8-126">Vergleicht zwei Eintragsbezeichner, um zu bestimmen, ob Sie auf dasselbe Objekt verweisen.</span><span class="sxs-lookup"><span data-stu-id="69fb8-126">Compares two entry identifiers to determine whether they refer to the same object.</span></span>  <br/> |
|[<span data-ttu-id="69fb8-127">Beraten</span><span class="sxs-lookup"><span data-stu-id="69fb8-127">Advise</span></span>](iablogon-advise.md) <br/> |<span data-ttu-id="69fb8-128">Registriert den Anrufer so, dass er Benachrichtigungen über angegebene Ereignisse erhält, die sich auf einen Container, einen Messagingbenutzer oder eine Verteilerliste auswirken.</span><span class="sxs-lookup"><span data-stu-id="69fb8-128">Registers the caller to receive notification of specified events that affect a container, messaging user, or distribution list.</span></span>  <br/> |
|[<span data-ttu-id="69fb8-129">Unadvise</span><span class="sxs-lookup"><span data-stu-id="69fb8-129">Unadvise</span></span>](iablogon-unadvise.md) <br/> |<span data-ttu-id="69fb8-130">Bricht Benachrichtigungen ab, die zuvor mit einem Aufruf der **Advise** -Methode eingerichtet wurden.</span><span class="sxs-lookup"><span data-stu-id="69fb8-130">Cancels notifications that were previously set up with a call to the **Advise** method.</span></span>  <br/> |
|[<span data-ttu-id="69fb8-131">OpenStatusEntry</span><span class="sxs-lookup"><span data-stu-id="69fb8-131">OpenStatusEntry</span></span>](iablogon-openstatusentry.md) <br/> |<span data-ttu-id="69fb8-132">Öffnet das Status-Objekt des Anbieters.</span><span class="sxs-lookup"><span data-stu-id="69fb8-132">Opens the provider's status object.</span></span>  <br/> |
|[<span data-ttu-id="69fb8-133">OpenTemplate-Nr.</span><span class="sxs-lookup"><span data-stu-id="69fb8-133">OpenTemplateID</span></span>](iablogon-opentemplateid.md) <br/> |<span data-ttu-id="69fb8-134">Öffnet einen Empfängereintrag mit Daten, die sich in einem Host-Adressbuchanbieter befinden.</span><span class="sxs-lookup"><span data-stu-id="69fb8-134">Opens a recipient entry that has data residing in a host address book provider.</span></span>  <br/> |
|[<span data-ttu-id="69fb8-135">GetOneOffTable</span><span class="sxs-lookup"><span data-stu-id="69fb8-135">GetOneOffTable</span></span>](iablogon-getoneofftable.md) <br/> |<span data-ttu-id="69fb8-136">Gibt eine Tabelle mit einmaligen Vorlagen zum Erstellen von Empfängern zurück, die der Empfängerliste einer ausgehenden Nachricht hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="69fb8-136">Returns a table of one-off templates for creating recipients to be added to the recipient list of an outgoing message.</span></span>  <br/> |
|[<span data-ttu-id="69fb8-137">PrepareRecips</span><span class="sxs-lookup"><span data-stu-id="69fb8-137">PrepareRecips</span></span>](iablogon-preparerecips.md) <br/> |<span data-ttu-id="69fb8-138">Bereitet eine Empfängerliste für die spätere Verwendung durch das Messagingsystem vor.</span><span class="sxs-lookup"><span data-stu-id="69fb8-138">Prepares a recipient list for later use by the messaging system.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="69fb8-139">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="69fb8-139">Remarks</span></span>

<span data-ttu-id="69fb8-140">Allgemeine Informationen zu den Methoden der **IABLogon** -Schnittstelle finden Sie unter [Implementieren der Dienstanbieter Anmeldung](implementing-service-provider-logon.md).</span><span class="sxs-lookup"><span data-stu-id="69fb8-140">For general information about the methods of the **IABLogon** interface, see [Implementing Service Provider Logon](implementing-service-provider-logon.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="69fb8-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="69fb8-141">See also</span></span>



[<span data-ttu-id="69fb8-142">MAPI-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="69fb8-142">MAPI Interfaces</span></span>](mapi-interfaces.md)

