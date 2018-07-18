---
title: IXPLogonAddressTypes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon.AddressTypes
api_type:
- COM
ms.assetid: 5add1f2b-d9e6-4d78-8739-c3848f6e32a3
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: a7bb1aca501e24843950114bb76b6a09b20f2467
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792873"
---
# <a name="ixplogonaddresstypes"></a><span data-ttu-id="f3647-103">IXPLogon::AddressTypes</span><span class="sxs-lookup"><span data-stu-id="f3647-103">IXPLogon::AddressTypes</span></span>

  
  
<span data-ttu-id="f3647-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f3647-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f3647-105">Gibt die Typen von Empfängern, die der Adressbuchhierarchie behandelt.</span><span class="sxs-lookup"><span data-stu-id="f3647-105">Returns the types of recipients that the transport provider handles.</span></span>
  
```cpp
HRESULT AddressTypes(
  ULONG FAR * lpulFlags,
  ULONG FAR * lpcAdrType,
  LPSTR FAR * FAR * lpppszAdrTypeArray,
  ULONG FAR * lpcMAPIUID,
  LPUID FAR * FAR * lpppUIDArray
);
```

## <a name="parameters"></a><span data-ttu-id="f3647-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f3647-106">Parameters</span></span>

 <span data-ttu-id="f3647-107">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="f3647-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="f3647-108">[out] Eine Bitmaske aus Flags, die den Typ des zurückgegebenen Zeichenfolgen steuert.</span><span class="sxs-lookup"><span data-stu-id="f3647-108">[out] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="f3647-109">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="f3647-109">The following flag can be set:</span></span>
    
<span data-ttu-id="f3647-110">PARAMETER MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="f3647-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="f3647-111">Die zurückgegebenen Zeichenfolgen sind im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="f3647-111">The returned strings are in Unicode format.</span></span> <span data-ttu-id="f3647-112">Wenn die Option MAPI_UNICODE nicht festgelegt ist, sind die Zeichenfolgen in ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="f3647-112">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="f3647-113">_lpcAdrType_</span><span class="sxs-lookup"><span data-stu-id="f3647-113">_lpcAdrType_</span></span>
  
> <span data-ttu-id="f3647-114">[out] Ein Zeiger auf die Anzahl der Einträge in der Matrix, durch den Parameter _LpppszAdrTypeArray_ auf zeigt.</span><span class="sxs-lookup"><span data-stu-id="f3647-114">[out] A pointer to the count of entries in the array pointed to by the  _lpppszAdrTypeArray_ parameter.</span></span> 
    
 <span data-ttu-id="f3647-115">_lpppszAdrTypeArray_</span><span class="sxs-lookup"><span data-stu-id="f3647-115">_lpppszAdrTypeArray_</span></span>
  
> <span data-ttu-id="f3647-116">[out] Ein Zeiger auf einen Zeiger auf ein Array von Zeichenfolgen, die Empfängertypen bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="f3647-116">[out] A pointer to a pointer to an array of strings that identify recipient types.</span></span>
    
 <span data-ttu-id="f3647-117">_lpcMAPIUID_</span><span class="sxs-lookup"><span data-stu-id="f3647-117">_lpcMAPIUID_</span></span>
  
> <span data-ttu-id="f3647-118">[out] Ein Zeiger auf die Anzahl der Einträge in der Matrix, durch den Parameter _LpppUIDArray_ auf zeigt.</span><span class="sxs-lookup"><span data-stu-id="f3647-118">[out] A pointer to the count of entries in the array pointed to by the  _lpppUIDArray_ parameter.</span></span> 
    
 <span data-ttu-id="f3647-119">_lpppUIDArray_</span><span class="sxs-lookup"><span data-stu-id="f3647-119">_lpppUIDArray_</span></span>
  
> <span data-ttu-id="f3647-120">[out] Ein Zeiger auf einen Zeiger auf ein Array von Zeigern für [MAPIUID](mapiuid.md) -Strukturen, die Empfängertypen zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="f3647-120">[out] A pointer to a pointer to an array of pointers to [MAPIUID](mapiuid.md) structures that identify recipient types.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="f3647-121">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="f3647-121">Return value</span></span>

<span data-ttu-id="f3647-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="f3647-122">S_OK</span></span> 
  
> <span data-ttu-id="f3647-123">Der Transportdienst angegeben erfolgreich die Typen von Empfängern, die es verarbeiten kann.</span><span class="sxs-lookup"><span data-stu-id="f3647-123">The transport provider successfully indicated the types of recipients that it can handle.</span></span>
    
## <a name="notes-to-implementers"></a><span data-ttu-id="f3647-124">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="f3647-124">Notes to implementers</span></span>

<span data-ttu-id="f3647-125">Die MAPI-Warteschlange Ruft die **IXPLogon::AddressTypes** -Methode auf, unmittelbar nachdem ein Transportdienstes aus einen Anruf an die [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) -Methode zurückgegeben, damit der Adressbuchhierarchie angeben kann, welche Arten von Empfängern verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="f3647-125">The MAPI spooler calls the **IXPLogon::AddressTypes** method immediately after a transport provider returns from a call to the [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) method so the transport provider can indicate what types of recipients it handles.</span></span> <span data-ttu-id="f3647-126">Um dies darauf hinzuweisen, sollte der Adressbuchhierarchie in der _LpppszAdrTypeArray_ -Parameter einen Zeiger auf ein Array von Zeigern auf Zeichenfolgen übergeben oder wieder in den _LpppUIDArray_ -Parameter einen Zeiger auf ein Array von Zeigern für **MAPIUID** übergeben Strukturen oder Werte in beiden Parametern übergeben.</span><span class="sxs-lookup"><span data-stu-id="f3647-126">To indicate this, the transport provider should pass back in the  _lpppszAdrTypeArray_ parameter a pointer to an array of pointers to strings, or pass back in the  _lpppUIDArray_ parameter a pointer to an array of pointers to **MAPIUID** structures, or pass values in both parameters.</span></span> 
  
<span data-ttu-id="f3647-127">Für verschiedene Identification Prozesse werden diese beiden Arrays verwendet.</span><span class="sxs-lookup"><span data-stu-id="f3647-127">These two arrays are used for different identification processes.</span></span> <span data-ttu-id="f3647-128">MAPI- und die MAPI-Warteschlange können Sie die Strukturen [MAPIUID](mapiuid.md) im Array _LpppUIDArray_ verwenden, um diese Empfänger-Eintragsbezeichner identifizieren, die direkt mit der Adressbuchhierarchie oder mit der messaging-System mit dem der Adressbuchhierarchie verbindet behandelt werden .</span><span class="sxs-lookup"><span data-stu-id="f3647-128">MAPI and the MAPI spooler use the [MAPIUID](mapiuid.md) structures in the  _lpppUIDArray_ array to identify those recipient entry identifiers that are directly handled by the transport provider or by the messaging system to which the transport provider connects.</span></span> <span data-ttu-id="f3647-129">MAPI- weder die MAPI-Warteschlange erweitert Adressen mithilfe von Eintragsbezeichner in keiner dieser **MAPIUID** Strukturen enthalten; Diese Strukturen dienen nur zur Identifizierung der Empfängertyp.</span><span class="sxs-lookup"><span data-stu-id="f3647-129">Neither MAPI nor the MAPI spooler expands addresses by using entry identifiers contained in any of these **MAPIUID** structures; these structures are used only for recipient type identification.</span></span> 
  
<span data-ttu-id="f3647-130">Die MAPI-Warteschlange verwendet jede der Zeichenfolgen in der _LpppszAdrTypeArray_ -Parameter für einen Vergleichstest bei der Festlegung, welche Adressbuchhierarchie welche Empfänger für eine ausgehende Nachricht behandelt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="f3647-130">The MAPI spooler uses each of the strings in the  _lpppszAdrTypeArray_ parameter for a comparison test when it decides which transport provider should handle which recipients for an outbound message.</span></span> <span data-ttu-id="f3647-131">Wenn der Empfänger einer Nachricht **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))-Eigenschaft eine Zeichenfolge übereinstimmt, die eines der messaging-Adresstypen identifiziert, die der Adressbuchhierarchie bereitstellt, kann der Anbieter die Nachricht an diesen Empfänger übermitteln.</span><span class="sxs-lookup"><span data-stu-id="f3647-131">If a message recipient's **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) property exactly matches a string that identifies one of the messaging address types that the transport provider supplies, the provider can deliver the message to that recipient.</span></span>
  
<span data-ttu-id="f3647-132">Wenn mehrere Transportanbieter den gleichen Typ des Empfängers verarbeitet werden können, wählt MAPI ein Transportdienstes basierend auf der Transport Prioritätsreihenfolge aus, die in der Clientanwendung Profil angegeben.</span><span class="sxs-lookup"><span data-stu-id="f3647-132">If multiple transport providers can handle the same type of recipient, MAPI selects a transport provider based on the transport priority order indicated in the client application's profile.</span></span> <span data-ttu-id="f3647-133">Um festzustellen, welche Adressbuchhierarchie verwenden, überprüft die MAPI-Warteschlange alle Anbieter angegeben **MAPIUID** Strukturen in Prioritätsreihenfolge aus, und klicken Sie dann alle Anbieter angegebene Adresse Geben Sie Werte in Prioritätsreihenfolge aus.</span><span class="sxs-lookup"><span data-stu-id="f3647-133">To determine which transport provider to use, the MAPI spooler scans all provider-specified **MAPIUID** structures in priority order, and then all provider-specified address type values in priority order.</span></span> <span data-ttu-id="f3647-134">Der erste Transportdienst auf einen bestimmten Empfänger in diese Überprüfung übereinstimmen Ruft die erste Möglichkeit, diesen Empfänger zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="f3647-134">The first transport provider to match a particular recipient in this scan gets the first opportunity to handle this recipient.</span></span> <span data-ttu-id="f3647-135">Wenn dieses Anbieters den Empfänger nicht behandelt wird, wird die MAPI-Warteschlange die Überprüfung ein Transportdienstes für jeden Empfänger noch nicht verarbeitet finden fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="f3647-135">If that provider does not handle the recipient, the MAPI spooler continues the scan to find a transport provider for any recipient not yet handled.</span></span> <span data-ttu-id="f3647-136">Die Überprüfung wird fortgesetzt, bis keine weiteren Treffer gefunden werden, an welcher Stelle ein Unzustellbarkeitsbericht für alle Empfänger generiert wird, die nicht bearbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="f3647-136">The scan continues until no further matches are found, at which point a nondelivery report is generated for any recipient that was not handled.</span></span> 
  
<span data-ttu-id="f3647-137">Wenn der Anbieter immer einen bestimmten Satz von Empfängertypen unterstützt, können der Adresstyp und **MAPIUID** Arrays, die der Adressbuchhierarchie übergeben statisch sein.</span><span class="sxs-lookup"><span data-stu-id="f3647-137">If the provider always supports a particular set of recipient types, the address type and **MAPIUID** arrays that the transport provider passed can be static.</span></span> <span data-ttu-id="f3647-138">Wenn der Adressbuchhierarchie diese Arrays dynamisch erstellt wurde, können sie Speicher mithilfe des Support-Objekts, das zuvor im Aufruf **TransportLogon**, übergeben wurde, obwohl dies nicht erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="f3647-138">If the transport provider dynamically constructs these arrays, it can allocate memory by using the support object that was previously passed in the call to **TransportLogon**, although this is not necessary.</span></span>
  
<span data-ttu-id="f3647-139">Der Speicher für den Adresstyp und **MAPIUID** Arrays verwendet sollte erst nach dem letzten Aufruf der [IXPLogon::TransportLogoff](ixplogon-transportlogoff.md) -Methode zugewiesenen bleiben bei der Adressbuchhierarchie den Arbeitsspeicher bei Bedarf freigegeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="f3647-139">The memory used for the address type and **MAPIUID** arrays should remain allocated until the final call to the [IXPLogon::TransportLogoff](ixplogon-transportlogoff.md) method, at which time the transport provider can free the memory, if necessary.</span></span> <span data-ttu-id="f3647-140">Der Transportdienst sollten nicht den Inhalt dieser Arrays ändern, nachdem ein Wert aus dem Aufruf **TransportLogoff** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f3647-140">The transport provider should not alter the contents of these arrays after it returns from the **TransportLogoff** call.</span></span> 
  
<span data-ttu-id="f3647-141">Ein Transportanbieter, der jeden Empfänger behandeln kann kann im Parameter _LpppszAdrTypeArray_ NULL zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f3647-141">A transport provider that can handle any type of recipient can return NULL in the  _lpppszAdrTypeArray_ parameter.</span></span> <span data-ttu-id="f3647-142">Transportanbieter für LAN-basierte messaging-Systemen, die einen zentralen Server ausgehende Nachrichten an verschiedenen foreign Nachrichtensysteme häufig übermitteln verwenden hierzu.</span><span class="sxs-lookup"><span data-stu-id="f3647-142">Transport providers for LAN-based messaging systems that use a central server to deliver outgoing messages to various foreign message systems commonly do this.</span></span> <span data-ttu-id="f3647-143">Diese Art der Adressbuchhierarchie zuletzt in den MAPI- und MAPI-installiert werden soll Warteschlange Prioritätsreihenfolge aus der Transportanbieter im Profil.</span><span class="sxs-lookup"><span data-stu-id="f3647-143">This type of transport provider should be installed last in the MAPI and MAPI spooler priority order of transport providers in the profile.</span></span> 
  
<span data-ttu-id="f3647-144">Ein Transportdienstes, das nicht unterstützt werden ausgehende Nachrichten, die versandt werden, basierend auf den Adresstyp sollte in _LpppszAdrTypeArray_eine einzelne Zeichenfolge der Länge Null zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f3647-144">A transport provider that does not support outbound messages that are dispatched to it based on address type should return a single zero-length string in  _lpppszAdrTypeArray_.</span></span> <span data-ttu-id="f3647-145">Wenn ein Transportdienstes keine Empfängertypen unterstützt, sollten sie NULL für die **MAPIUID** -Struktur und eine leere Zeichenfolge für den Adresstyp übergeben.</span><span class="sxs-lookup"><span data-stu-id="f3647-145">If a transport provider supports no recipient types, it should pass NULL for the **MAPIUID** structure and an empty string for the address type.</span></span> <span data-ttu-id="f3647-146">Transportanbieter dieses Typs werden am häufigsten verwendet, um eine Nachricht Präprozessor zu installieren.</span><span class="sxs-lookup"><span data-stu-id="f3647-146">Transport providers of this type are most commonly used to install a message preprocessor.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f3647-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f3647-147">See also</span></span>



[<span data-ttu-id="f3647-148">IXPLogon::TransportLogoff</span><span class="sxs-lookup"><span data-stu-id="f3647-148">IXPLogon::TransportLogoff</span></span>](ixplogon-transportlogoff.md)
  
[<span data-ttu-id="f3647-149">IXPProvider::TransportLogon</span><span class="sxs-lookup"><span data-stu-id="f3647-149">IXPProvider::TransportLogon</span></span>](ixpprovider-transportlogon.md)
  
[<span data-ttu-id="f3647-150">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="f3647-150">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="f3647-151">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f3647-151">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

