---
title: OpenTnefStream
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.OpenTnefStream
api_type:
- COM
ms.assetid: 912d7799-53ce-42a7-9fbd-f9a6a3a56047
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 866d3be5e1c7a4375db84d1f15802e01f8d10f23
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793319"
---
# <a name="opentnefstream"></a><span data-ttu-id="63210-103">OpenTnefStream</span><span class="sxs-lookup"><span data-stu-id="63210-103">OpenTnefStream</span></span>

<span data-ttu-id="63210-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="63210-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="63210-105">Aufgerufen von eines Transportdienstes So initiieren Sie eine Sitzung MAPI Transport Neutral Encapsulation Format (TNEF).</span><span class="sxs-lookup"><span data-stu-id="63210-105">Called by a transport provider to initiate a MAPI Transport Neutral Encapsulation Format (TNEF) session.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="63210-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="63210-106">Header file:</span></span>  <br/> |<span data-ttu-id="63210-107">TNEF.h</span><span class="sxs-lookup"><span data-stu-id="63210-107">Tnef.h</span></span>  <br/> |
|<span data-ttu-id="63210-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="63210-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="63210-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="63210-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="63210-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="63210-110">Called by:</span></span>  <br/> |<span data-ttu-id="63210-111">Transportanbieter</span><span class="sxs-lookup"><span data-stu-id="63210-111">Transport providers</span></span>  <br/> |
   
```cpp
HRESULT OpenTnefStream(
  LPVOID lpvSupport,
  LPSTREAM lpStream,
  LPSTR lpszStreamName, 
  ULONG ulFlags,
  LPMESSAGE lpMessage,
  WORD wKey,
  LPITNEF FAR * lppTNEF
);
```

## <a name="parameters"></a><span data-ttu-id="63210-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="63210-112">Parameters</span></span>

<span data-ttu-id="63210-113">_lpvSupport_</span><span class="sxs-lookup"><span data-stu-id="63210-113">_lpvSupport_</span></span>
  
> <span data-ttu-id="63210-114">[in] Übergibt ein Support-Objekt oder NULL übergibt.</span><span class="sxs-lookup"><span data-stu-id="63210-114">[in] Passes a support object, or passes in NULL.</span></span> 
    
<span data-ttu-id="63210-115">_lpStream_</span><span class="sxs-lookup"><span data-stu-id="63210-115">_lpStream_</span></span>
  
> <span data-ttu-id="63210-116">[in] Zeiger auf einen Speicher Stream-Objekt OLE **IStream** Schnittstelle Bereitstellen von Quelle oder Ziel für eine Nachricht der TNEF-Stream.</span><span class="sxs-lookup"><span data-stu-id="63210-116">[in] Pointer to a storage stream object OLE **IStream** interface providing a source or destination for a TNEF stream message.</span></span> 
    
<span data-ttu-id="63210-117">_lpszStreamName_</span><span class="sxs-lookup"><span data-stu-id="63210-117">_lpszStreamName_</span></span>
  
> <span data-ttu-id="63210-118">[in] Zeiger auf den Namen des Datenstroms, die das TNEF-Objekt verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="63210-118">[in] Pointer to the name of the data stream that the TNEF object uses.</span></span> <span data-ttu-id="63210-119">Wenn der Aufrufer das Flag TNEF_ENCODE ( _UlFlags_ -Parameter) in dem Aufruf von **OpenTNEFStream nicht ausgeführt werden**festgelegt, muss den _Wert_ -Parameter einen nicht-Null Zeiger auf eine beliebige Zeichen gültig für eine Datei bestehend ungleich Null-Zeichenfolge angeben.</span><span class="sxs-lookup"><span data-stu-id="63210-119">If the caller has set the TNEF_ENCODE flag ( _ulFlags_ parameter) in its call to **OpenTnefStream**, the  _lpszName_ parameter must specify a non-null pointer to a non-null string consisting of any characters considered valid for naming a file.</span></span> <span data-ttu-id="63210-120">MAPI lässt nicht Zeichenfolgennamen, einschließlich der Zeichen "[", "]", oder ":", auch wenn das Dateisystem ihre Verwendung ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="63210-120">MAPI does not allow string names including the characters "[", "]", or ":", even if the file system permits their use.</span></span> <span data-ttu-id="63210-121">Die Größe der für _Wert_ übergebene Zeichenfolge muss den Wert der MAX_PATH, die maximale Länge einer Zeichenfolge, die ein Pfadname enthält, nicht überschreiten.</span><span class="sxs-lookup"><span data-stu-id="63210-121">The size of the string passed for  _lpszName_ must not exceed the value of MAX_PATH, the maximum length of a string that contains a path name.</span></span> 
    
<span data-ttu-id="63210-122">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="63210-122">_ulFlags_</span></span>
  
> <span data-ttu-id="63210-123">[in] Bitmaske aus Flags verwendet, um den Modus der Funktion anzugeben.</span><span class="sxs-lookup"><span data-stu-id="63210-123">[in] Bitmask of flags used to indicate the mode of the function.</span></span> <span data-ttu-id="63210-124">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="63210-124">The following flags can be set:</span></span>
    
<span data-ttu-id="63210-125">TNEF_BEST_DATA</span><span class="sxs-lookup"><span data-stu-id="63210-125">TNEF_BEST_DATA</span></span> 
  
> <span data-ttu-id="63210-126">Alle mögliche Eigenschaften in ihre kompatible Attribute zugeordnet sind, aber bei ein möglichen Datenverlust aufgrund der Konvertierung einer kompatiblen-Attribut vorhanden ist, wird die Eigenschaft auch in der Encapsulations codiert.</span><span class="sxs-lookup"><span data-stu-id="63210-126">All possible properties are mapped into their down-level attributes, but when there is a possible data loss due to the conversion to a down-level attribute, the property is also encoded in the encapsulations.</span></span> <span data-ttu-id="63210-127">Beachten Sie, dass dies die Duplizierung von Informationen in der TNEF-Stream verursacht.</span><span class="sxs-lookup"><span data-stu-id="63210-127">Note that this will cause the duplication of information in the TNEF stream.</span></span> <span data-ttu-id="63210-128">TNEF_BEST_DATA ist der Standardwert, wenn keine anderen Modi angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="63210-128">TNEF_BEST_DATA is the default if no other modes are specified.</span></span> 
    
<span data-ttu-id="63210-129">TNEF_COMPATIBILITY</span><span class="sxs-lookup"><span data-stu-id="63210-129">TNEF_COMPATIBILITY</span></span> 
  
> <span data-ttu-id="63210-130">Stellt die Abwärtskompatibilität mit älteren Client Clientanwendungen bereit.</span><span class="sxs-lookup"><span data-stu-id="63210-130">Provides backward compatibility with the older client applications.</span></span> <span data-ttu-id="63210-131">TNEF-Streams dieses Flag codiert werden alle mögliche Eigenschaften in die entsprechende kompatible Attribut zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="63210-131">TNEF streams encoded with this flag will map all possible properties into their corresponding down-level attribute.</span></span> <span data-ttu-id="63210-132">Dieser Modus wird auch die Standardwerte einiger Eigenschaften, die durch kompatible Clients erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="63210-132">This mode also causes the defaulting of some properties that are required by down-level clients.</span></span> 
    
  > [!CAUTION]
  > <span data-ttu-id="63210-133">Dieses Kennzeichen ist veraltet und sollte nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="63210-133">This flag is obsolete and should not be used.</span></span> 
  
<span data-ttu-id="63210-134">TNEF_DECODE</span><span class="sxs-lookup"><span data-stu-id="63210-134">TNEF_DECODE</span></span> 
  
> <span data-ttu-id="63210-135">Das TNEF-Objekt im angegebenen Stream wird mit schreibgeschützten Zugriff geöffnet.</span><span class="sxs-lookup"><span data-stu-id="63210-135">The TNEF object on the indicated stream is opened with read-only access.</span></span> <span data-ttu-id="63210-136">Der Transportdienst muss dieses Flag festgelegt, wenn sie die Funktion zum Initialisieren des Objekts für die nachfolgende Decodierung möchte.</span><span class="sxs-lookup"><span data-stu-id="63210-136">The transport provider must set this flag if it wants the function to initialize the object for subsequent decoding.</span></span>
    
<span data-ttu-id="63210-137">TNEF_ENCODE</span><span class="sxs-lookup"><span data-stu-id="63210-137">TNEF_ENCODE</span></span> 
  
> <span data-ttu-id="63210-138">Das TNEF-Objekt im angegebenen Stream wird Lese-/Schreibzugriff geöffnet.</span><span class="sxs-lookup"><span data-stu-id="63210-138">The TNEF object on the indicated stream is opened for read/write permission.</span></span> <span data-ttu-id="63210-139">Der Transportdienst muss dieses Flag festgelegt, wenn sie die Funktion zum Initialisieren des Objekts für die nachfolgende Codierung möchte.</span><span class="sxs-lookup"><span data-stu-id="63210-139">The transport provider must set this flag if it wants the function to initialize the object for subsequent encoding.</span></span>
    
<span data-ttu-id="63210-140">TNEF_PURE</span><span class="sxs-lookup"><span data-stu-id="63210-140">TNEF_PURE</span></span> 
  
> <span data-ttu-id="63210-141">Alle Eigenschaften codiert in die MAPI-Kapselung Blöcke.</span><span class="sxs-lookup"><span data-stu-id="63210-141">Encodes all properties into the MAPI encapsulation blocks.</span></span> <span data-ttu-id="63210-142">Aus diesem Grund "reine" TNEF-Datei besteht aus, an die meisten, AttMAPIProps AttAttachment, AttRenddata, und AttRecipTable.</span><span class="sxs-lookup"><span data-stu-id="63210-142">Therefore, a "pure" TNEF file will consist of, at most, attMAPIProps, attAttachment, attRenddata, and attRecipTable.</span></span> <span data-ttu-id="63210-143">Dieser Modus ist ideal für die Verwendung, wenn keine Abwärtskompatibilität erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="63210-143">This mode is ideal for use when no backward compatibility is required.</span></span>
    
<span data-ttu-id="63210-144">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="63210-144">_lpMessage_</span></span>
  
> <span data-ttu-id="63210-145">[in] Zeiger auf ein Objekt "Message" als Ziel für eine entschlüsselte Nachricht mit Anlagen oder eine Quelle für eine codierte Nachricht mit Anlagen.</span><span class="sxs-lookup"><span data-stu-id="63210-145">[in] Pointer to a message object as a destination for a decoded message with attachments or a source for an encoded message with attachments.</span></span> <span data-ttu-id="63210-146">Alle Eigenschaften einer Nachricht Ziel möglicherweise durch die Eigenschaften einer verschlüsselten Nachricht überschrieben werden soll.</span><span class="sxs-lookup"><span data-stu-id="63210-146">Any properties of a destination message might be overwritten by the properties of an encoded message.</span></span>
    
<span data-ttu-id="63210-147">_wKey_</span><span class="sxs-lookup"><span data-stu-id="63210-147">_wKey_</span></span>
  
> <span data-ttu-id="63210-148">[in] Ein Search-Schlüssel, den das TNEF-Objekt wird verwendet, um Anlagen, die Text-Tags in den Nachrichtentext eingefügt übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="63210-148">[in] A search key that the TNEF object uses to match attachments to the text tags inserted in the message text.</span></span> <span data-ttu-id="63210-149">Dieser Wert sollte über Nachrichten relativ eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="63210-149">This value should be relatively unique across messages.</span></span>
    
<span data-ttu-id="63210-150">_lppTNEF_</span><span class="sxs-lookup"><span data-stu-id="63210-150">_lppTNEF_</span></span>
  
> <span data-ttu-id="63210-151">[out] Zeiger auf das neue TNEF-Objekt.</span><span class="sxs-lookup"><span data-stu-id="63210-151">[out] Pointer to the new TNEF object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="63210-152">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="63210-152">Return value</span></span>

<span data-ttu-id="63210-153">S_OK</span><span class="sxs-lookup"><span data-stu-id="63210-153">S_OK</span></span> 
  
> <span data-ttu-id="63210-154">Der Aufruf erfolgreich ausgeführt und der erwartete Wert oder Werte zurückgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="63210-154">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="63210-155">Hinweise</span><span class="sxs-lookup"><span data-stu-id="63210-155">Remarks</span></span>

<span data-ttu-id="63210-156">Ein TNEF-Objekt von der Funktion **OpenTNEFStream nicht ausgeführt werden** später erstellt Ruft die OLE-Methode **IUnknown:: AddRef** Hinzufügen von Verweisen für den Support-Objekt, das Stream-Objekt und Message-Objekts.</span><span class="sxs-lookup"><span data-stu-id="63210-156">A TNEF object created by the **OpenTnefStream** function later calls the OLE method **IUnknown::AddRef** to add references for the support object, the stream object, and the message object.</span></span> <span data-ttu-id="63210-157">Der Transportdienst kann die Verweise für alle drei Objekte mit einem einzigen Aufruf der OLE-Methode **IUnknown** für die TNEF-Objekt freigeben.</span><span class="sxs-lookup"><span data-stu-id="63210-157">The transport provider can release the references for all three objects with a single call to the OLE method **IUnknown::Release** on the TNEF object.</span></span> 
  
<span data-ttu-id="63210-158">**OpenTNEFStream nicht ausgeführt werden** reserviert und initialisiert TNEF-Objektschnittstelle **ITnef** für den Anbieter in einer MAPI-Nachricht **IMessage** -Schnittstelle in einem Stream TNEF-Nachricht-Codierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="63210-158">**OpenTnefStream** allocates and initializes a TNEF object **ITnef** interface for the provider to use in encoding a MAPI message **IMessage** interface into a TNEF stream message.</span></span> <span data-ttu-id="63210-159">Alternativ kann das Objekt für den Anbieter im nachfolgende Aufrufe von [ITnef::ExtractProps](itnef-extractprops.md) zum Decodieren einer TNEF-Stream-Nachricht in einem MAPI-Nachricht verwenden die Funktion einrichten.</span><span class="sxs-lookup"><span data-stu-id="63210-159">Alternatively, the function can set up the object for the provider to use in subsequent calls to [ITnef::ExtractProps](itnef-extractprops.md) to decode a TNEF stream message into a MAPI message.</span></span> <span data-ttu-id="63210-160">Um die TNEF-Objekts frei, und schließen die Sitzung, muss der Adressbuchhierarchie die geerbte **IUnknown** -Methode für das Objekt aufrufen.</span><span class="sxs-lookup"><span data-stu-id="63210-160">To free the TNEF object and close the session, the transport provider must call the inherited **IUnknown::Release** method on the object.</span></span> 
  
<span data-ttu-id="63210-161">Diese Funktion ist der ursprüngliche Einstiegspunkt für den Zugriff von TNEF und wurde ersetzt durch [OpenTnefStreamEx](opentnefstreamex.md) aber weiterhin für die Kompatibilität für die Verwendung von TNEF bereits verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="63210-161">This function is the original entry point for TNEF access and has been replaced by [OpenTnefStreamEx](opentnefstreamex.md) but is still used for compatibility for those already using TNEF.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="63210-162">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="63210-162">See also</span></span>

- [<span data-ttu-id="63210-163">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="63210-163">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)
- [<span data-ttu-id="63210-164">IXPProvider::TransportLogon</span><span class="sxs-lookup"><span data-stu-id="63210-164">IXPProvider::TransportLogon</span></span>](ixpprovider-transportlogon.md)

