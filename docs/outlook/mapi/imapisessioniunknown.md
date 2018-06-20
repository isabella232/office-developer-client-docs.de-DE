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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: a37d8138547c8c4e9308dbb0ebbc6750b152d795
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792338"
---
# <a name="imapisession--iunknown"></a><span data-ttu-id="c8c92-103">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="c8c92-103">IMAPISession : IUnknown</span></span>

  
  
<span data-ttu-id="c8c92-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c8c92-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c8c92-105">Verwaltet von Objekten einer MAPI-Sitzung zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="c8c92-105">Manages objects associated with a MAPI logon session.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c8c92-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="c8c92-106">Header file:</span></span>  <br/> |<span data-ttu-id="c8c92-107">Mapix.h</span><span class="sxs-lookup"><span data-stu-id="c8c92-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="c8c92-108">Verf�gbar gemacht von:</span><span class="sxs-lookup"><span data-stu-id="c8c92-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="c8c92-109">Session-Objekte</span><span class="sxs-lookup"><span data-stu-id="c8c92-109">Session objects</span></span>  <br/> |
|<span data-ttu-id="c8c92-110">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="c8c92-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="c8c92-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="c8c92-111">MAPI</span></span>  <br/> |
|<span data-ttu-id="c8c92-112">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="c8c92-112">Called by:</span></span>  <br/> |<span data-ttu-id="c8c92-113">Clientanwendungen und MAPI</span><span class="sxs-lookup"><span data-stu-id="c8c92-113">Client applications and MAPI</span></span>  <br/> |
|<span data-ttu-id="c8c92-114">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="c8c92-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="c8c92-115">IID_IMAPISession</span><span class="sxs-lookup"><span data-stu-id="c8c92-115">IID_IMAPISession</span></span>  <br/> |
|<span data-ttu-id="c8c92-116">Zeigertyp:</span><span class="sxs-lookup"><span data-stu-id="c8c92-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="c8c92-117">LPMAPISESSION</span><span class="sxs-lookup"><span data-stu-id="c8c92-117">LPMAPISESSION</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="c8c92-118">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="c8c92-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="c8c92-119">GetLastError</span><span class="sxs-lookup"><span data-stu-id="c8c92-119">GetLastError</span></span>](imapisession-getlasterror.md) <br/> |<span data-ttu-id="c8c92-120">Gibt eine [MAPIERROR](mapierror.md) -Struktur, die Informationen über den vorherigen Sitzungsfehler enthält.</span><span class="sxs-lookup"><span data-stu-id="c8c92-120">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous session error.</span></span>  <br/> |
|[<span data-ttu-id="c8c92-121">GetMsgStoresTable</span><span class="sxs-lookup"><span data-stu-id="c8c92-121">GetMsgStoresTable</span></span>](imapisession-getmsgstorestable.md) <br/> |<span data-ttu-id="c8c92-122">Bietet Zugriff auf die Nachricht Store Tabelle mit Informationen zu allen Nachrichtenspeichern im Profil der Sitzung.</span><span class="sxs-lookup"><span data-stu-id="c8c92-122">Provides access to the message store table that contains information about all the message stores in the session profile.</span></span>  <br/> |
|[<span data-ttu-id="c8c92-123">OpenMsgStore</span><span class="sxs-lookup"><span data-stu-id="c8c92-123">OpenMsgStore</span></span>](imapisession-openmsgstore.md) <br/> |<span data-ttu-id="c8c92-124">Öffnet einen Nachrichtenspeicher und gibt einen Zeiger [IMsgStore](imsgstoreimapiprop.md) für den weiteren Zugriff.</span><span class="sxs-lookup"><span data-stu-id="c8c92-124">Opens a message store and returns an [IMsgStore](imsgstoreimapiprop.md) pointer for further access.</span></span>  <br/> |
|[<span data-ttu-id="c8c92-125">OpenAddressBook</span><span class="sxs-lookup"><span data-stu-id="c8c92-125">OpenAddressBook</span></span>](imapisession-openaddressbook.md) <br/> |<span data-ttu-id="c8c92-126">Öffnet das MAPI-integrierte Adressbuch, einen [IAddrBook](iaddrbookimapiprop.md) Zeiger für den weiteren Zugriff zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="c8c92-126">Opens the MAPI integrated address book, returning an [IAddrBook](iaddrbookimapiprop.md) pointer for further access.</span></span>  <br/> |
|[<span data-ttu-id="c8c92-127">"OpenProfileSection"</span><span class="sxs-lookup"><span data-stu-id="c8c92-127">OpenProfileSection</span></span>](imapisession-openprofilesection.md) <br/> |<span data-ttu-id="c8c92-128">Öffnet einen Abschnitt des aktuellen Profils und gibt einen Zeiger [IProfSect](iprofsectimapiprop.md) für den weiteren Zugriff.</span><span class="sxs-lookup"><span data-stu-id="c8c92-128">Opens a section of the current profile and returns an [IProfSect](iprofsectimapiprop.md) pointer for further access.</span></span>  <br/> |
|[<span data-ttu-id="c8c92-129">GetStatusTable</span><span class="sxs-lookup"><span data-stu-id="c8c92-129">GetStatusTable</span></span>](imapisession-getstatustable.md) <br/> |<span data-ttu-id="c8c92-130">Bietet Zugriff auf die Statustabelle, einer Tabelle, Informationen zu allen MAPI-Ressourcen in der Sitzung enthält.</span><span class="sxs-lookup"><span data-stu-id="c8c92-130">Provides access to the status table, a table that contains information about all the MAPI resources in the session.</span></span>  <br/> |
|[<span data-ttu-id="c8c92-131">OpenEntry</span><span class="sxs-lookup"><span data-stu-id="c8c92-131">OpenEntry</span></span>](imapisession-openentry.md) <br/> |<span data-ttu-id="c8c92-132">Öffnet ein Objekt und gibt einen Schnittstellenzeiger für den weiteren Zugriff.</span><span class="sxs-lookup"><span data-stu-id="c8c92-132">Opens an object and returns an interface pointer for further access.</span></span>  <br/> |
|[<span data-ttu-id="c8c92-133">CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="c8c92-133">CompareEntryIDs</span></span>](imapisession-compareentryids.md) <br/> |<span data-ttu-id="c8c92-134">Vergleicht zwei Eintragsbezeichner, um zu bestimmen, ob sie sich auf dasselbe Objekt verweisen.</span><span class="sxs-lookup"><span data-stu-id="c8c92-134">Compares two entry identifiers to determine whether they refer to the same object.</span></span>  <br/> |
|[<span data-ttu-id="c8c92-135">Beraten</span><span class="sxs-lookup"><span data-stu-id="c8c92-135">Advise</span></span>](imapisession-advise.md) <br/> |<span data-ttu-id="c8c92-136">Um die Benachrichtigung der angegebenen Ereignisse, die Einfluss auf die Sitzung registriert.</span><span class="sxs-lookup"><span data-stu-id="c8c92-136">Registers to receive notification of specified events that affect the session.</span></span>  <br/> |
|[<span data-ttu-id="c8c92-137">Heben Sie diesen Vorgang</span><span class="sxs-lookup"><span data-stu-id="c8c92-137">Unadvise</span></span>](imapisession-unadvise.md) <br/> |<span data-ttu-id="c8c92-138">Bricht ab, das Senden von Benachrichtigungen, die zuvor mit einem Aufruf der **Advise** -Methode eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="c8c92-138">Cancels the sending of notifications previously set up with a call to the **Advise** method.</span></span>  <br/> |
|<span data-ttu-id="c8c92-139">**MessageOptions**</span><span class="sxs-lookup"><span data-stu-id="c8c92-139">**MessageOptions**</span></span> <br/> | <span data-ttu-id="c8c92-140">*Nicht unterstützte oder dokumentiert.*</span><span class="sxs-lookup"><span data-stu-id="c8c92-140">*Not supported or documented.*</span></span>  <br/> |
|<span data-ttu-id="c8c92-141">**QueryDefaultMessageOpt**</span><span class="sxs-lookup"><span data-stu-id="c8c92-141">**QueryDefaultMessageOpt**</span></span> <br/> | <span data-ttu-id="c8c92-142">*Nicht unterstützte oder dokumentiert.*</span><span class="sxs-lookup"><span data-stu-id="c8c92-142">*Not supported or documented.*</span></span>  <br/> |
|[<span data-ttu-id="c8c92-143">EnumAdrTypes</span><span class="sxs-lookup"><span data-stu-id="c8c92-143">EnumAdrTypes</span></span>](imapisession-enumadrtypes.md) <br/> |<span data-ttu-id="c8c92-144">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="c8c92-144">Deprecated.</span></span> <span data-ttu-id="c8c92-145">Gibt die behandelt werden können Adresstypen aller Anbieter für den Transport in der Sitzung zurück.</span><span class="sxs-lookup"><span data-stu-id="c8c92-145">Returns the address types that can be handled by all of the transport providers in the session.</span></span>  <br/> |
|[<span data-ttu-id="c8c92-146">QueryIdentity</span><span class="sxs-lookup"><span data-stu-id="c8c92-146">QueryIdentity</span></span>](imapisession-queryidentity.md) <br/> |<span data-ttu-id="c8c92-147">Gibt die Eintrags-ID des Objekts, das die primäre Identität für die Sitzung bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="c8c92-147">Returns the entry identifier of the object that provides the primary identity for the session.</span></span>  <br/> |
|[<span data-ttu-id="c8c92-148">Logoff</span><span class="sxs-lookup"><span data-stu-id="c8c92-148">Logoff</span></span>](imapisession-logoff.md) <br/> |<span data-ttu-id="c8c92-149">MAPI-Sitzung beendet.</span><span class="sxs-lookup"><span data-stu-id="c8c92-149">Ends a MAPI session.</span></span>  <br/> |
|[<span data-ttu-id="c8c92-150">SetDefaultStore</span><span class="sxs-lookup"><span data-stu-id="c8c92-150">SetDefaultStore</span></span>](imapisession-setdefaultstore.md) <br/> |<span data-ttu-id="c8c92-151">Stellt einen Nachrichtenspeicher als Standard-Informationsspeicher für die Sitzung her.</span><span class="sxs-lookup"><span data-stu-id="c8c92-151">Establishes a message store as the default message store for the session.</span></span>  <br/> |
|[<span data-ttu-id="c8c92-152">AdminServices</span><span class="sxs-lookup"><span data-stu-id="c8c92-152">AdminServices</span></span>](imapisession-adminservices.md) <br/> |<span data-ttu-id="c8c92-153">Gibt einen Zeiger [IMsgServiceAdmin](imsgserviceadminiunknown.md) für die Änderung Message-Dienste.</span><span class="sxs-lookup"><span data-stu-id="c8c92-153">Returns an [IMsgServiceAdmin](imsgserviceadminiunknown.md) pointer for making changes to message services.</span></span>  <br/> |
|[<span data-ttu-id="c8c92-154">ShowForm aus</span><span class="sxs-lookup"><span data-stu-id="c8c92-154">ShowForm</span></span>](imapisession-showform.md) <br/> |<span data-ttu-id="c8c92-155">Zeigt ein Formular an.</span><span class="sxs-lookup"><span data-stu-id="c8c92-155">Displays a form.</span></span>  <br/> |
|[<span data-ttu-id="c8c92-156">PrepareForm</span><span class="sxs-lookup"><span data-stu-id="c8c92-156">PrepareForm</span></span>](imapisession-prepareform.md) <br/> |<span data-ttu-id="c8c92-157">Erstellt eine numerische Token, das die **ShowForm aus** -Methode verwendet, um auf eine Nachricht zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="c8c92-157">Creates a numeric token that the **ShowForm** method uses to access a message.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c8c92-158">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c8c92-158">See also</span></span>



[<span data-ttu-id="c8c92-159">MAPI-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="c8c92-159">MAPI Interfaces</span></span>](mapi-interfaces.md)
