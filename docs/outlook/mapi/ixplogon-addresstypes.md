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
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: ca68c604152a7a28fb6a5357aa9c012ec7466b5a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435376"
---
# <a name="ixplogonaddresstypes"></a><span data-ttu-id="869b9-103">IXPLogon::AddressTypes</span><span class="sxs-lookup"><span data-stu-id="869b9-103">IXPLogon::AddressTypes</span></span>

  
  
<span data-ttu-id="869b9-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="869b9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="869b9-105">Gibt die Empfängertypen zurück, die vom Transportanbieter verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="869b9-105">Returns the types of recipients that the transport provider handles.</span></span>
  
```cpp
HRESULT AddressTypes(
  ULONG FAR * lpulFlags,
  ULONG FAR * lpcAdrType,
  LPSTR FAR * FAR * lpppszAdrTypeArray,
  ULONG FAR * lpcMAPIUID,
  LPUID FAR * FAR * lpppUIDArray
);
```

## <a name="parameters"></a><span data-ttu-id="869b9-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="869b9-106">Parameters</span></span>

 <span data-ttu-id="869b9-107">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="869b9-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="869b9-108">[out] Eine Bitmaske mit Flags, die den Typ der zurückgegebenen Zeichenfolgen steuert.</span><span class="sxs-lookup"><span data-stu-id="869b9-108">[out] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="869b9-109">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="869b9-109">The following flag can be set:</span></span>
    
<span data-ttu-id="869b9-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="869b9-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="869b9-111">Die zurückgegebenen Zeichenfolgen sind im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="869b9-111">The returned strings are in Unicode format.</span></span> <span data-ttu-id="869b9-112">Wenn das MAPI_UNICODE nicht festgelegt ist, befinden sich die Zeichenfolgen im ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="869b9-112">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="869b9-113">_lpcAdrType_</span><span class="sxs-lookup"><span data-stu-id="869b9-113">_lpcAdrType_</span></span>
  
> <span data-ttu-id="869b9-114">[out] Ein Zeiger auf die Anzahl der Einträge im Array, auf die der  _lpppszAdrTypeArray-Parameter_ verweist.</span><span class="sxs-lookup"><span data-stu-id="869b9-114">[out] A pointer to the count of entries in the array pointed to by the  _lpppszAdrTypeArray_ parameter.</span></span> 
    
 <span data-ttu-id="869b9-115">_lpppszAdrTypeArray_</span><span class="sxs-lookup"><span data-stu-id="869b9-115">_lpppszAdrTypeArray_</span></span>
  
> <span data-ttu-id="869b9-116">[out] Ein Zeiger auf einen Zeiger auf ein Array von Zeichenfolgen, die Empfängertypen identifizieren.</span><span class="sxs-lookup"><span data-stu-id="869b9-116">[out] A pointer to a pointer to an array of strings that identify recipient types.</span></span>
    
 <span data-ttu-id="869b9-117">_lpcMAPIUID_</span><span class="sxs-lookup"><span data-stu-id="869b9-117">_lpcMAPIUID_</span></span>
  
> <span data-ttu-id="869b9-118">[out] Ein Zeiger auf die Anzahl der Einträge im Array, auf die der  _lpppUIDArray-Parameter_ verweist.</span><span class="sxs-lookup"><span data-stu-id="869b9-118">[out] A pointer to the count of entries in the array pointed to by the  _lpppUIDArray_ parameter.</span></span> 
    
 <span data-ttu-id="869b9-119">_lpppUIDArray_</span><span class="sxs-lookup"><span data-stu-id="869b9-119">_lpppUIDArray_</span></span>
  
> <span data-ttu-id="869b9-120">[out] Ein Zeiger auf einen Zeiger auf ein Array von Zeigern auf [MAPIUID-Strukturen,](mapiuid.md) die Empfängertypen identifizieren.</span><span class="sxs-lookup"><span data-stu-id="869b9-120">[out] A pointer to a pointer to an array of pointers to [MAPIUID](mapiuid.md) structures that identify recipient types.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="869b9-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="869b9-121">Return value</span></span>

<span data-ttu-id="869b9-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="869b9-122">S_OK</span></span> 
  
> <span data-ttu-id="869b9-123">Der Transportanbieter hat die Empfängertypen, die er verarbeiten kann, erfolgreich angegeben.</span><span class="sxs-lookup"><span data-stu-id="869b9-123">The transport provider successfully indicated the types of recipients that it can handle.</span></span>
    
## <a name="notes-to-implementers"></a><span data-ttu-id="869b9-124">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="869b9-124">Notes to implementers</span></span>

<span data-ttu-id="869b9-125">Der MAPI-Spooler ruft die **IXPLogon::AddressTypes-Methode** unmittelbar nach der Rückgabe eines Transportanbieters von einem Aufruf der [IXPProvider::TransportLogon-Methode](ixpprovider-transportlogon.md) auf, damit der Transportanbieter angeben kann, welche Empfängertypen er verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="869b9-125">The MAPI spooler calls the **IXPLogon::AddressTypes** method immediately after a transport provider returns from a call to the [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) method so the transport provider can indicate what types of recipients it handles.</span></span> <span data-ttu-id="869b9-126">Um dies anzugeben, sollte der Transportanbieter im  _lpppszAdrTypeArray-Parameter_ einen Zeiger auf ein Array von Zeigern auf Zeichenfolgen übergeben oder im  _lpppUIDArray-Parameter_ einen Zeiger an ein Array von Zeigern an **MAPIUID-Strukturen** übergeben oder Werte in beiden Parametern übergeben.</span><span class="sxs-lookup"><span data-stu-id="869b9-126">To indicate this, the transport provider should pass back in the  _lpppszAdrTypeArray_ parameter a pointer to an array of pointers to strings, or pass back in the  _lpppUIDArray_ parameter a pointer to an array of pointers to **MAPIUID** structures, or pass values in both parameters.</span></span> 
  
<span data-ttu-id="869b9-127">Diese beiden Arrays werden für verschiedene Identifikationsprozesse verwendet.</span><span class="sxs-lookup"><span data-stu-id="869b9-127">These two arrays are used for different identification processes.</span></span> <span data-ttu-id="869b9-128">MAPI und der MAPI-Spooler verwenden die [MAPIUID-Strukturen](mapiuid.md) im  _lpppUIDArray-Array,_ um die Empfängereintragsbezeichner zu identifizieren, die direkt vom Transportanbieter oder vom Messagingsystem verarbeitet werden, mit dem der Transportanbieter eine Verbindung herstellt.</span><span class="sxs-lookup"><span data-stu-id="869b9-128">MAPI and the MAPI spooler use the [MAPIUID](mapiuid.md) structures in the  _lpppUIDArray_ array to identify those recipient entry identifiers that are directly handled by the transport provider or by the messaging system to which the transport provider connects.</span></span> <span data-ttu-id="869b9-129">Weder MAPI noch der #A0 erweitern Adressen mithilfe von Eintragsbezeichnern, die in diesen **MAPIUID-Strukturen enthalten** sind. Diese Strukturen werden nur für die Empfängertypidentifikation verwendet.</span><span class="sxs-lookup"><span data-stu-id="869b9-129">Neither MAPI nor the MAPI spooler expands addresses by using entry identifiers contained in any of these **MAPIUID** structures; these structures are used only for recipient type identification.</span></span> 
  
<span data-ttu-id="869b9-130">Der MAPI-Spooler verwendet jede zeichenfolge im  _lpppszAdrTypeArray-Parameter_ für einen Vergleichstest, wenn er entscheidet, welcher Transportanbieter welche Empfänger für eine ausgehende Nachricht verarbeiten soll.</span><span class="sxs-lookup"><span data-stu-id="869b9-130">The MAPI spooler uses each of the strings in the  _lpppszAdrTypeArray_ parameter for a comparison test when it decides which transport provider should handle which recipients for an outbound message.</span></span> <span data-ttu-id="869b9-131">Wenn die PR_ADDRTYPE **(** [PidTagAddressType](pidtagaddresstype-canonical-property.md))-Eigenschaft eines Nachrichtenempfängers exakt mit einer Zeichenfolge entspricht, die einen der vom Transportanbieter zur Verfügung stellten Messagingadressentypen identifiziert, kann der Anbieter die Nachricht an diesen Empfänger senden.</span><span class="sxs-lookup"><span data-stu-id="869b9-131">If a message recipient's **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) property exactly matches a string that identifies one of the messaging address types that the transport provider supplies, the provider can deliver the message to that recipient.</span></span>
  
<span data-ttu-id="869b9-132">Wenn mehrere Transportanbieter denselben Empfängertyp verarbeiten können, wählt MAPI einen Transportanbieter basierend auf der Transportprioritätsreihenfolge aus, die im Profil der Clientanwendung angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="869b9-132">If multiple transport providers can handle the same type of recipient, MAPI selects a transport provider based on the transport priority order indicated in the client application's profile.</span></span> <span data-ttu-id="869b9-133">Um zu bestimmen, welcher Transportanbieter verwendet werden soll, überprüft der MAPI-Spooler alle vom Anbieter angegebenen **MAPIUID-Strukturen** in Prioritätsreihenfolge und anschließend alle vom Anbieter angegebenen Adresstypwerte in Prioritätsreihenfolge.</span><span class="sxs-lookup"><span data-stu-id="869b9-133">To determine which transport provider to use, the MAPI spooler scans all provider-specified **MAPIUID** structures in priority order, and then all provider-specified address type values in priority order.</span></span> <span data-ttu-id="869b9-134">Der erste Transportanbieter, der bei dieser Überprüfung mit einem bestimmten Empfänger übereinstimmen soll, erhält die erste Möglichkeit, diesen Empfänger zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="869b9-134">The first transport provider to match a particular recipient in this scan gets the first opportunity to handle this recipient.</span></span> <span data-ttu-id="869b9-135">Wenn dieser Anbieter den Empfänger nicht verarbeitet, setzt der MAPI-Spooler die Überprüfung fort, um einen Transportanbieter für einen Empfänger zu finden, der noch nicht verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="869b9-135">If that provider does not handle the recipient, the MAPI spooler continues the scan to find a transport provider for any recipient not yet handled.</span></span> <span data-ttu-id="869b9-136">Die Überprüfung wird fortgesetzt, bis keine weiteren Übereinstimmungen gefunden wurden. An diesem Punkt wird für empfänger, die nicht verarbeitet wurden, ein Unauslöschungsbericht generiert.</span><span class="sxs-lookup"><span data-stu-id="869b9-136">The scan continues until no further matches are found, at which point a nondelivery report is generated for any recipient that was not handled.</span></span> 
  
<span data-ttu-id="869b9-137">Wenn der Anbieter immer einen bestimmten Satz von Empfängertypen unterstützt, können der Adresstyp und **die MAPIUID-Arrays,** die der Transportanbieter übergeben hat, statisch sein.</span><span class="sxs-lookup"><span data-stu-id="869b9-137">If the provider always supports a particular set of recipient types, the address type and **MAPIUID** arrays that the transport provider passed can be static.</span></span> <span data-ttu-id="869b9-138">Wenn der Transportanbieter diese Arrays dynamisch erstellt, kann er Arbeitsspeicher mithilfe des Supportobjekts zuweisen, das zuvor im Aufruf von **TransportLogon** übergeben wurde, obwohl dies nicht erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="869b9-138">If the transport provider dynamically constructs these arrays, it can allocate memory by using the support object that was previously passed in the call to **TransportLogon**, although this is not necessary.</span></span>
  
<span data-ttu-id="869b9-139">Der für den Adresstyp und die **MAPIUID-Arrays** verwendete Arbeitsspeicher sollte bis zum letzten Aufruf der [IXPLogon::TransportLogoff-Methode](ixplogon-transportlogoff.md) zugewiesen bleiben, zu dem der Transportanbieter den Arbeitsspeicher bei Bedarf frei geben kann.</span><span class="sxs-lookup"><span data-stu-id="869b9-139">The memory used for the address type and **MAPIUID** arrays should remain allocated until the final call to the [IXPLogon::TransportLogoff](ixplogon-transportlogoff.md) method, at which time the transport provider can free the memory, if necessary.</span></span> <span data-ttu-id="869b9-140">Der Transportanbieter sollte den Inhalt dieser Arrays nicht ändern, nachdem er vom **TransportLogoff-Aufruf zurückgegeben** wurde.</span><span class="sxs-lookup"><span data-stu-id="869b9-140">The transport provider should not alter the contents of these arrays after it returns from the **TransportLogoff** call.</span></span> 
  
<span data-ttu-id="869b9-141">Ein Transportanbieter, der jeden Empfängertyp verarbeiten kann, kann NULL im  _lpppszAdrTypeArray-Parameter_ zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="869b9-141">A transport provider that can handle any type of recipient can return NULL in the  _lpppszAdrTypeArray_ parameter.</span></span> <span data-ttu-id="869b9-142">Transportanbieter für LAN-basierte Messagingsysteme, die einen zentralen Server verwenden, um ausgehende Nachrichten an verschiedene fremde Nachrichtensysteme zu senden, tun dies in der Regel.</span><span class="sxs-lookup"><span data-stu-id="869b9-142">Transport providers for LAN-based messaging systems that use a central server to deliver outgoing messages to various foreign message systems commonly do this.</span></span> <span data-ttu-id="869b9-143">Dieser Transportanbietertyp sollte zuletzt in der Prioritätsreihenfolge der Transportanbieter im Profil der MAPI- und MAPI-Spooler installiert werden.</span><span class="sxs-lookup"><span data-stu-id="869b9-143">This type of transport provider should be installed last in the MAPI and MAPI spooler priority order of transport providers in the profile.</span></span> 
  
<span data-ttu-id="869b9-144">Ein Transportanbieter, der ausgehende Nachrichten, die basierend auf dem Adresstyp an ihn gesendet werden, nicht unterstützt, sollte eine einzelne zeichenfolge ohne Länge in _lpppszAdrTypeArray zurückgeben._</span><span class="sxs-lookup"><span data-stu-id="869b9-144">A transport provider that does not support outbound messages that are dispatched to it based on address type should return a single zero-length string in  _lpppszAdrTypeArray_.</span></span> <span data-ttu-id="869b9-145">Wenn ein Transportanbieter keine Empfängertypen unterstützt, sollte er NULL für die **MAPIUID-Struktur** und eine leere Zeichenfolge für den Adresstyp übergeben.</span><span class="sxs-lookup"><span data-stu-id="869b9-145">If a transport provider supports no recipient types, it should pass NULL for the **MAPIUID** structure and an empty string for the address type.</span></span> <span data-ttu-id="869b9-146">Transportanbieter dieses Typs werden am häufigsten zum Installieren eines Nachrichtenvorprozessors verwendet.</span><span class="sxs-lookup"><span data-stu-id="869b9-146">Transport providers of this type are most commonly used to install a message preprocessor.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="869b9-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="869b9-147">See also</span></span>



[<span data-ttu-id="869b9-148">IXPLogon::TransportLogoff</span><span class="sxs-lookup"><span data-stu-id="869b9-148">IXPLogon::TransportLogoff</span></span>](ixplogon-transportlogoff.md)
  
[<span data-ttu-id="869b9-149">IXPProvider::TransportLogon</span><span class="sxs-lookup"><span data-stu-id="869b9-149">IXPProvider::TransportLogon</span></span>](ixpprovider-transportlogon.md)
  
[<span data-ttu-id="869b9-150">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="869b9-150">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="869b9-151">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="869b9-151">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

