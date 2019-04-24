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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357211"
---
# <a name="ixplogonaddresstypes"></a><span data-ttu-id="d945d-103">IXPLogon::AddressTypes</span><span class="sxs-lookup"><span data-stu-id="d945d-103">IXPLogon::AddressTypes</span></span>

  
  
<span data-ttu-id="d945d-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d945d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d945d-105">Gibt die Empfängertypen zurück, die vom Transportanbieter verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="d945d-105">Returns the types of recipients that the transport provider handles.</span></span>
  
```cpp
HRESULT AddressTypes(
  ULONG FAR * lpulFlags,
  ULONG FAR * lpcAdrType,
  LPSTR FAR * FAR * lpppszAdrTypeArray,
  ULONG FAR * lpcMAPIUID,
  LPUID FAR * FAR * lpppUIDArray
);
```

## <a name="parameters"></a><span data-ttu-id="d945d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d945d-106">Parameters</span></span>

 <span data-ttu-id="d945d-107">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="d945d-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="d945d-108">Out Eine Bitmaske von Flags, die den Typ der zurückgegebenen Zeichenfolgen steuert.</span><span class="sxs-lookup"><span data-stu-id="d945d-108">[out] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="d945d-109">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="d945d-109">The following flag can be set:</span></span>
    
<span data-ttu-id="d945d-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="d945d-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="d945d-111">Die zurückgegebenen Zeichenfolgen sind im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="d945d-111">The returned strings are in Unicode format.</span></span> <span data-ttu-id="d945d-112">Wenn das MAPI_UNICODE-Flag nicht festgelegt ist, werden die Zeichenfolgen im ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="d945d-112">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="d945d-113">_lpcAdrType_</span><span class="sxs-lookup"><span data-stu-id="d945d-113">_lpcAdrType_</span></span>
  
> <span data-ttu-id="d945d-114">Out Ein Zeiger auf die Anzahl der Einträge im Array, auf die durch den _lpppszAdrTypeArray_ -Parameter verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="d945d-114">[out] A pointer to the count of entries in the array pointed to by the  _lpppszAdrTypeArray_ parameter.</span></span> 
    
 <span data-ttu-id="d945d-115">_lpppszAdrTypeArray_</span><span class="sxs-lookup"><span data-stu-id="d945d-115">_lpppszAdrTypeArray_</span></span>
  
> <span data-ttu-id="d945d-116">Out Ein Zeiger auf einen Zeiger auf ein Array von Zeichenfolgen, die Empfängertypen identifizieren.</span><span class="sxs-lookup"><span data-stu-id="d945d-116">[out] A pointer to a pointer to an array of strings that identify recipient types.</span></span>
    
 <span data-ttu-id="d945d-117">_lpcMAPIUID_</span><span class="sxs-lookup"><span data-stu-id="d945d-117">_lpcMAPIUID_</span></span>
  
> <span data-ttu-id="d945d-118">Out Ein Zeiger auf die Anzahl der Einträge im Array, auf die durch den _lpppUIDArray_ -Parameter verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="d945d-118">[out] A pointer to the count of entries in the array pointed to by the  _lpppUIDArray_ parameter.</span></span> 
    
 <span data-ttu-id="d945d-119">_lpppUIDArray_</span><span class="sxs-lookup"><span data-stu-id="d945d-119">_lpppUIDArray_</span></span>
  
> <span data-ttu-id="d945d-120">Out Ein Zeiger auf einen Zeiger auf ein Array von Zeigern auf [MAPIUID](mapiuid.md) -Strukturen, die Empfängertypen identifizieren.</span><span class="sxs-lookup"><span data-stu-id="d945d-120">[out] A pointer to a pointer to an array of pointers to [MAPIUID](mapiuid.md) structures that identify recipient types.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="d945d-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d945d-121">Return value</span></span>

<span data-ttu-id="d945d-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="d945d-122">S_OK</span></span> 
  
> <span data-ttu-id="d945d-123">Der Transportanbieter hat erfolgreich die Empfängertypen angegeben, die er verarbeiten kann.</span><span class="sxs-lookup"><span data-stu-id="d945d-123">The transport provider successfully indicated the types of recipients that it can handle.</span></span>
    
## <a name="notes-to-implementers"></a><span data-ttu-id="d945d-124">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="d945d-124">Notes to implementers</span></span>

<span data-ttu-id="d945d-125">Der MAPI-Spooler Ruft die **IXPLogon:: AddressTypes** -Methode unmittelbar auf, nachdem ein Transportanbieter von einem Aufruf der [IXPProvider:: TransportLogon](ixpprovider-transportlogon.md) -Methode zurückgegeben hat, sodass der Transportanbieter anzeigen kann, welche Empfängertypen er verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="d945d-125">The MAPI spooler calls the **IXPLogon::AddressTypes** method immediately after a transport provider returns from a call to the [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) method so the transport provider can indicate what types of recipients it handles.</span></span> <span data-ttu-id="d945d-126">Um dies anzugeben, sollte der Transportanbieter zurückgeben, in der _lpppszAdrTypeArray_ -Parameter einen Zeiger auf ein Array von Zeigern auf Zeichenfolgen oder zurückgeben Sie den _lpppUIDArray_ -Parameter einen Zeiger auf ein Array von Zeigern auf **MAPIUID** Strukturen oder übergeben Sie Werte in beiden Parametern.</span><span class="sxs-lookup"><span data-stu-id="d945d-126">To indicate this, the transport provider should pass back in the  _lpppszAdrTypeArray_ parameter a pointer to an array of pointers to strings, or pass back in the  _lpppUIDArray_ parameter a pointer to an array of pointers to **MAPIUID** structures, or pass values in both parameters.</span></span> 
  
<span data-ttu-id="d945d-127">Diese beiden Arrays werden für verschiedene identifizierungsprozesse verwendet.</span><span class="sxs-lookup"><span data-stu-id="d945d-127">These two arrays are used for different identification processes.</span></span> <span data-ttu-id="d945d-128">MAPI und der MAPI-Spooler verwenden die [MAPIUID](mapiuid.md) -Strukturen im _lpppUIDArray_ -Array, um die Empfänger Eintrags-IDs zu identifizieren, die direkt vom Transportanbieter oder vom Messagingsystem verarbeitet werden, mit dem der Transportanbieter eine Verbindung herstellt. .</span><span class="sxs-lookup"><span data-stu-id="d945d-128">MAPI and the MAPI spooler use the [MAPIUID](mapiuid.md) structures in the  _lpppUIDArray_ array to identify those recipient entry identifiers that are directly handled by the transport provider or by the messaging system to which the transport provider connects.</span></span> <span data-ttu-id="d945d-129">Weder MAPI noch der MAPI-Spooler erweitern Adressen mithilfe von Eintrags-IDs, die in einer dieser **MAPIUID** -Strukturen enthalten sind; Diese Strukturen werden nur zur Identifizierung von Empfängertypen verwendet.</span><span class="sxs-lookup"><span data-stu-id="d945d-129">Neither MAPI nor the MAPI spooler expands addresses by using entry identifiers contained in any of these **MAPIUID** structures; these structures are used only for recipient type identification.</span></span> 
  
<span data-ttu-id="d945d-130">Der MAPI-Spooler verwendet jede der Zeichenfolgen im _lpppszAdrTypeArray_ -Parameter für einen Vergleichstest, wenn er entscheidet, welcher Transportanbieter welche Empfänger für eine ausgehende Nachricht behandeln soll.</span><span class="sxs-lookup"><span data-stu-id="d945d-130">The MAPI spooler uses each of the strings in the  _lpppszAdrTypeArray_ parameter for a comparison test when it decides which transport provider should handle which recipients for an outbound message.</span></span> <span data-ttu-id="d945d-131">Wenn die **PR_ADDRTYPE** ([pidtagaddresstype (](pidtagaddresstype-canonical-property.md))-Eigenschaft eines Nachrichtenempfängers genau mit einer Zeichenfolge übereinstimmt, die einen der vom Transportanbieter bereitgestellten Messaging Adresstypen identifiziert, kann der Anbieter die Nachricht an diesen Empfänger übermitteln.</span><span class="sxs-lookup"><span data-stu-id="d945d-131">If a message recipient's **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) property exactly matches a string that identifies one of the messaging address types that the transport provider supplies, the provider can deliver the message to that recipient.</span></span>
  
<span data-ttu-id="d945d-132">Wenn mehrere Transportanbieter denselben Empfängertyp verarbeiten können, wählt MAPI einen Transportanbieter basierend auf der im Profil der Clientanwendung angegebenen Transport Prioritätsreihenfolge aus.</span><span class="sxs-lookup"><span data-stu-id="d945d-132">If multiple transport providers can handle the same type of recipient, MAPI selects a transport provider based on the transport priority order indicated in the client application's profile.</span></span> <span data-ttu-id="d945d-133">Um zu bestimmen, welcher Transportanbieter verwendet werden soll, scannt der MAPI-Spooler alle vom Anbieter angegebenen **MAPIUID** -Strukturen in der Prioritätsreihenfolge und dann alle vom Anbieter angegebenen Adresstyp Werte in der Prioritätsreihenfolge.</span><span class="sxs-lookup"><span data-stu-id="d945d-133">To determine which transport provider to use, the MAPI spooler scans all provider-specified **MAPIUID** structures in priority order, and then all provider-specified address type values in priority order.</span></span> <span data-ttu-id="d945d-134">Der erste Transportanbieter, der einem bestimmten Empfänger bei dieser Überprüfung entspricht, erhält die erste Gelegenheit, diesen Empfänger zu behandeln.</span><span class="sxs-lookup"><span data-stu-id="d945d-134">The first transport provider to match a particular recipient in this scan gets the first opportunity to handle this recipient.</span></span> <span data-ttu-id="d945d-135">Wenn dieser Anbieter den Empfänger nicht verarbeitet, setzt der MAPI-Spooler die Überprüfung fort, um einen Transportanbieter für einen Empfänger zu finden, der noch nicht behandelt wurde.</span><span class="sxs-lookup"><span data-stu-id="d945d-135">If that provider does not handle the recipient, the MAPI spooler continues the scan to find a transport provider for any recipient not yet handled.</span></span> <span data-ttu-id="d945d-136">Die Überprüfung wird fortgesetzt, bis keine weiteren Übereinstimmungen gefunden werden, an welcher Stelle ein Unzustellbarkeitsbericht für einen Empfänger generiert wird, der nicht behandelt wurde.</span><span class="sxs-lookup"><span data-stu-id="d945d-136">The scan continues until no further matches are found, at which point a nondelivery report is generated for any recipient that was not handled.</span></span> 
  
<span data-ttu-id="d945d-137">Wenn der Anbieter eine bestimmte Gruppe von Empfängertypen immer unterstützt, können der Adresstyp und die **MAPIUID** -Arrays, die der Transportanbieter übergeben hat, statisch sein.</span><span class="sxs-lookup"><span data-stu-id="d945d-137">If the provider always supports a particular set of recipient types, the address type and **MAPIUID** arrays that the transport provider passed can be static.</span></span> <span data-ttu-id="d945d-138">Wenn der Transportanbieter diese Arrays dynamisch erstellt, kann er Arbeitsspeicher mithilfe des Support-Objekts zuweisen, das zuvor im Aufruf an **TransportLogon**übergeben wurde, obwohl dies nicht erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="d945d-138">If the transport provider dynamically constructs these arrays, it can allocate memory by using the support object that was previously passed in the call to **TransportLogon**, although this is not necessary.</span></span>
  
<span data-ttu-id="d945d-139">Der für den Adresstyp und **MAPIUID** -Arrays verwendete Speicher sollte bis zum letzten Aufruf der [IXPLogon:: TransportLogoff](ixplogon-transportlogoff.md) -Methode reserviert werden, zu der Zeit, zu der der Transportanbieter den Arbeitsspeicher freigeben kann, falls erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d945d-139">The memory used for the address type and **MAPIUID** arrays should remain allocated until the final call to the [IXPLogon::TransportLogoff](ixplogon-transportlogoff.md) method, at which time the transport provider can free the memory, if necessary.</span></span> <span data-ttu-id="d945d-140">Der Transportanbieter sollte den Inhalt dieser Arrays nicht ändern, nachdem er vom **TransportLogoff** -Aufruf zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="d945d-140">The transport provider should not alter the contents of these arrays after it returns from the **TransportLogoff** call.</span></span> 
  
<span data-ttu-id="d945d-141">Ein Transportanbieter, der einen beliebigen Empfängertyp verarbeiten kann, kann im _lpppszAdrTypeArray_ -Parameter NULL zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="d945d-141">A transport provider that can handle any type of recipient can return NULL in the  _lpppszAdrTypeArray_ parameter.</span></span> <span data-ttu-id="d945d-142">Transport Anbieter für LAN-basierte Messagingsysteme, die einen zentralen Server verwenden, um ausgehende Nachrichten an verschiedene fremd Nachrichtensysteme zuzustellen, tun dies häufig.</span><span class="sxs-lookup"><span data-stu-id="d945d-142">Transport providers for LAN-based messaging systems that use a central server to deliver outgoing messages to various foreign message systems commonly do this.</span></span> <span data-ttu-id="d945d-143">Dieser Transport Anbietertyp sollte zuletzt in der MAPI-und MAPI-Spooler-Prioritätsreihenfolge der Transportanbieter im Profil installiert werden.</span><span class="sxs-lookup"><span data-stu-id="d945d-143">This type of transport provider should be installed last in the MAPI and MAPI spooler priority order of transport providers in the profile.</span></span> 
  
<span data-ttu-id="d945d-144">Ein Transportanbieter, der ausgehende Nachrichten, die basierend auf dem Adresstyp an ihn gesendet werden, nicht unterstützt, sollte eine einzelne leere Zeichenfolge in _lpppszAdrTypeArray_zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="d945d-144">A transport provider that does not support outbound messages that are dispatched to it based on address type should return a single zero-length string in  _lpppszAdrTypeArray_.</span></span> <span data-ttu-id="d945d-145">Wenn ein Transportanbieter keine Empfängertypen unterstützt, sollte er NULL für die **MAPIUID** -Struktur und eine leere Zeichenfolge für den Adresstyp überschreiten.</span><span class="sxs-lookup"><span data-stu-id="d945d-145">If a transport provider supports no recipient types, it should pass NULL for the **MAPIUID** structure and an empty string for the address type.</span></span> <span data-ttu-id="d945d-146">Transport Anbieter dieses Typs werden am häufigsten für die Installation eines nachrichtenpräprozessors verwendet.</span><span class="sxs-lookup"><span data-stu-id="d945d-146">Transport providers of this type are most commonly used to install a message preprocessor.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d945d-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d945d-147">See also</span></span>



[<span data-ttu-id="d945d-148">IXPLogon::TransportLogoff</span><span class="sxs-lookup"><span data-stu-id="d945d-148">IXPLogon::TransportLogoff</span></span>](ixplogon-transportlogoff.md)
  
[<span data-ttu-id="d945d-149">IXPProvider::TransportLogon</span><span class="sxs-lookup"><span data-stu-id="d945d-149">IXPProvider::TransportLogon</span></span>](ixpprovider-transportlogon.md)
  
[<span data-ttu-id="d945d-150">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="d945d-150">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="d945d-151">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d945d-151">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

