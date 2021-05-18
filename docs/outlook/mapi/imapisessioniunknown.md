---
title: IMAPISession IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession
api_type:
- COM
ms.assetid: 5650fa2a-6e62-451c-964e-363f7bee2344
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 1c1a66f61fe1533e436f4e35a542f53d938b4d01
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413381"
---
# <a name="imapisession--iunknown"></a><span data-ttu-id="123f2-103">IMAPISession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="123f2-103">IMAPISession : IUnknown</span></span>

  
  
<span data-ttu-id="123f2-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="123f2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="123f2-105">Verwaltet Objekte, die einer MAPI-Anmeldesitzung zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="123f2-105">Manages objects associated with a MAPI logon session.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="123f2-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="123f2-106">Header file:</span></span>  <br/> |<span data-ttu-id="123f2-107">Mapix.h</span><span class="sxs-lookup"><span data-stu-id="123f2-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="123f2-108">Verf�gbar gemacht von:</span><span class="sxs-lookup"><span data-stu-id="123f2-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="123f2-109">Sitzungsobjekte</span><span class="sxs-lookup"><span data-stu-id="123f2-109">Session objects</span></span>  <br/> |
|<span data-ttu-id="123f2-110">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="123f2-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="123f2-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="123f2-111">MAPI</span></span>  <br/> |
|<span data-ttu-id="123f2-112">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="123f2-112">Called by:</span></span>  <br/> |<span data-ttu-id="123f2-113">Clientanwendungen und MAPI</span><span class="sxs-lookup"><span data-stu-id="123f2-113">Client applications and MAPI</span></span>  <br/> |
|<span data-ttu-id="123f2-114">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="123f2-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="123f2-115">IID_IMAPISession</span><span class="sxs-lookup"><span data-stu-id="123f2-115">IID_IMAPISession</span></span>  <br/> |
|<span data-ttu-id="123f2-116">Zeigertyp:</span><span class="sxs-lookup"><span data-stu-id="123f2-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="123f2-117">LPMAPISESSION</span><span class="sxs-lookup"><span data-stu-id="123f2-117">LPMAPISESSION</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="123f2-118">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="123f2-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="123f2-119">GetLastError</span><span class="sxs-lookup"><span data-stu-id="123f2-119">GetLastError</span></span>](imapisession-getlasterror.md) <br/> |<span data-ttu-id="123f2-120">Gibt eine [MAPIERROR-Struktur](mapierror.md) zurück, die Informationen zum vorherigen Sitzungsfehler enthält.</span><span class="sxs-lookup"><span data-stu-id="123f2-120">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous session error.</span></span>  <br/> |
|[<span data-ttu-id="123f2-121">GetMsgStoresTable</span><span class="sxs-lookup"><span data-stu-id="123f2-121">GetMsgStoresTable</span></span>](imapisession-getmsgstorestable.md) <br/> |<span data-ttu-id="123f2-122">Bietet Zugriff auf die Nachrichtenspeichertabelle, die Informationen zu allen Nachrichtenspeichern im Sitzungsprofil enthält.</span><span class="sxs-lookup"><span data-stu-id="123f2-122">Provides access to the message store table that contains information about all the message stores in the session profile.</span></span>  <br/> |
|[<span data-ttu-id="123f2-123">OpenMsgStore</span><span class="sxs-lookup"><span data-stu-id="123f2-123">OpenMsgStore</span></span>](imapisession-openmsgstore.md) <br/> |<span data-ttu-id="123f2-124">Öffnet einen Nachrichtenspeicher und gibt einen [IMsgStore-Zeiger](imsgstoreimapiprop.md) für weiteren Zugriff zurück.</span><span class="sxs-lookup"><span data-stu-id="123f2-124">Opens a message store and returns an [IMsgStore](imsgstoreimapiprop.md) pointer for further access.</span></span>  <br/> |
|[<span data-ttu-id="123f2-125">OpenAddressBook</span><span class="sxs-lookup"><span data-stu-id="123f2-125">OpenAddressBook</span></span>](imapisession-openaddressbook.md) <br/> |<span data-ttu-id="123f2-126">Öffnet das integrierte MAPI-Adressbuch und gibt einen [IAddrBook-Zeiger für](iaddrbookimapiprop.md) weiteren Zugriff zurück.</span><span class="sxs-lookup"><span data-stu-id="123f2-126">Opens the MAPI integrated address book, returning an [IAddrBook](iaddrbookimapiprop.md) pointer for further access.</span></span>  <br/> |
|[<span data-ttu-id="123f2-127">OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="123f2-127">OpenProfileSection</span></span>](imapisession-openprofilesection.md) <br/> |<span data-ttu-id="123f2-128">Öffnet einen Abschnitt des aktuellen Profils und gibt einen [IProfSect-Zeiger](iprofsectimapiprop.md) für weiteren Zugriff zurück.</span><span class="sxs-lookup"><span data-stu-id="123f2-128">Opens a section of the current profile and returns an [IProfSect](iprofsectimapiprop.md) pointer for further access.</span></span>  <br/> |
|[<span data-ttu-id="123f2-129">GetStatusTable</span><span class="sxs-lookup"><span data-stu-id="123f2-129">GetStatusTable</span></span>](imapisession-getstatustable.md) <br/> |<span data-ttu-id="123f2-130">Bietet Zugriff auf die Statustabelle, eine Tabelle, die Informationen zu allen MAPI-Ressourcen in der Sitzung enthält.</span><span class="sxs-lookup"><span data-stu-id="123f2-130">Provides access to the status table, a table that contains information about all the MAPI resources in the session.</span></span>  <br/> |
|[<span data-ttu-id="123f2-131">OpenEntry</span><span class="sxs-lookup"><span data-stu-id="123f2-131">OpenEntry</span></span>](imapisession-openentry.md) <br/> |<span data-ttu-id="123f2-132">Öffnet ein Objekt und gibt einen Schnittstellenzeiger für weiteren Zugriff zurück.</span><span class="sxs-lookup"><span data-stu-id="123f2-132">Opens an object and returns an interface pointer for further access.</span></span>  <br/> |
|[<span data-ttu-id="123f2-133">CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="123f2-133">CompareEntryIDs</span></span>](imapisession-compareentryids.md) <br/> |<span data-ttu-id="123f2-134">Vergleicht zwei Eintragsbezeichner, um zu bestimmen, ob sie auf dasselbe Objekt verweisen.</span><span class="sxs-lookup"><span data-stu-id="123f2-134">Compares two entry identifiers to determine whether they refer to the same object.</span></span>  <br/> |
|[<span data-ttu-id="123f2-135">Raten</span><span class="sxs-lookup"><span data-stu-id="123f2-135">Advise</span></span>](imapisession-advise.md) <br/> |<span data-ttu-id="123f2-136">Registriert, um Benachrichtigungen über angegebene Ereignisse zu erhalten, die sich auf die Sitzung auswirken.</span><span class="sxs-lookup"><span data-stu-id="123f2-136">Registers to receive notification of specified events that affect the session.</span></span>  <br/> |
|[<span data-ttu-id="123f2-137">Unadvise</span><span class="sxs-lookup"><span data-stu-id="123f2-137">Unadvise</span></span>](imapisession-unadvise.md) <br/> |<span data-ttu-id="123f2-138">Bricht das Senden von Benachrichtigungen ab, die zuvor mit einem Aufruf der **Advise-Methode eingerichtet** wurden.</span><span class="sxs-lookup"><span data-stu-id="123f2-138">Cancels the sending of notifications previously set up with a call to the **Advise** method.</span></span>  <br/> |
|<span data-ttu-id="123f2-139">**MessageOptions**</span><span class="sxs-lookup"><span data-stu-id="123f2-139">**MessageOptions**</span></span> <br/> | <span data-ttu-id="123f2-140">*Nicht unterstützt oder dokumentiert.*</span><span class="sxs-lookup"><span data-stu-id="123f2-140">*Not supported or documented.*</span></span>  <br/> |
|<span data-ttu-id="123f2-141">**QueryDefaultMessageOpt**</span><span class="sxs-lookup"><span data-stu-id="123f2-141">**QueryDefaultMessageOpt**</span></span> <br/> | <span data-ttu-id="123f2-142">*Nicht unterstützt oder dokumentiert.*</span><span class="sxs-lookup"><span data-stu-id="123f2-142">*Not supported or documented.*</span></span>  <br/> |
|[<span data-ttu-id="123f2-143">EnumAdrTypes</span><span class="sxs-lookup"><span data-stu-id="123f2-143">EnumAdrTypes</span></span>](imapisession-enumadrtypes.md) <br/> |<span data-ttu-id="123f2-144">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="123f2-144">Deprecated.</span></span> <span data-ttu-id="123f2-145">Gibt die Adresstypen zurück, die von allen Transportanbietern in der Sitzung verarbeitet werden können.</span><span class="sxs-lookup"><span data-stu-id="123f2-145">Returns the address types that can be handled by all of the transport providers in the session.</span></span>  <br/> |
|[<span data-ttu-id="123f2-146">QueryIdentity</span><span class="sxs-lookup"><span data-stu-id="123f2-146">QueryIdentity</span></span>](imapisession-queryidentity.md) <br/> |<span data-ttu-id="123f2-147">Gibt den Eintragsbezeichner des Objekts zurück, das die primäre Identität für die Sitzung enthält.</span><span class="sxs-lookup"><span data-stu-id="123f2-147">Returns the entry identifier of the object that provides the primary identity for the session.</span></span>  <br/> |
|[<span data-ttu-id="123f2-148">Logoff</span><span class="sxs-lookup"><span data-stu-id="123f2-148">Logoff</span></span>](imapisession-logoff.md) <br/> |<span data-ttu-id="123f2-149">Beendet eine MAPI-Sitzung.</span><span class="sxs-lookup"><span data-stu-id="123f2-149">Ends a MAPI session.</span></span>  <br/> |
|[<span data-ttu-id="123f2-150">SetDefaultStore</span><span class="sxs-lookup"><span data-stu-id="123f2-150">SetDefaultStore</span></span>](imapisession-setdefaultstore.md) <br/> |<span data-ttu-id="123f2-151">Richtet einen Nachrichtenspeicher als Standardnachrichtenspeicher für die Sitzung ein.</span><span class="sxs-lookup"><span data-stu-id="123f2-151">Establishes a message store as the default message store for the session.</span></span>  <br/> |
|[<span data-ttu-id="123f2-152">AdminServices</span><span class="sxs-lookup"><span data-stu-id="123f2-152">AdminServices</span></span>](imapisession-adminservices.md) <br/> |<span data-ttu-id="123f2-153">Gibt einen [IMsgServiceAdmin-Zeiger zum](imsgserviceadminiunknown.md) Vornehmen von Änderungen an Nachrichtendiensten zurück.</span><span class="sxs-lookup"><span data-stu-id="123f2-153">Returns an [IMsgServiceAdmin](imsgserviceadminiunknown.md) pointer for making changes to message services.</span></span>  <br/> |
|[<span data-ttu-id="123f2-154">ShowForm</span><span class="sxs-lookup"><span data-stu-id="123f2-154">ShowForm</span></span>](imapisession-showform.md) <br/> |<span data-ttu-id="123f2-155">Zeigt ein Formular an.</span><span class="sxs-lookup"><span data-stu-id="123f2-155">Displays a form.</span></span>  <br/> |
|[<span data-ttu-id="123f2-156">PrepareForm</span><span class="sxs-lookup"><span data-stu-id="123f2-156">PrepareForm</span></span>](imapisession-prepareform.md) <br/> |<span data-ttu-id="123f2-157">Erstellt ein numerisches Token, das von der **ShowForm-Methode** für den Zugriff auf eine Nachricht verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="123f2-157">Creates a numeric token that the **ShowForm** method uses to access a message.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="123f2-158">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="123f2-158">See also</span></span>



[<span data-ttu-id="123f2-159">MAPI-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="123f2-159">MAPI Interfaces</span></span>](mapi-interfaces.md)

