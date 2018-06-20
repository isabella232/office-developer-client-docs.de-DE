---
title: OpenTnefStreamEx
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.OpenTnefStreamEx
api_type:
- COM
ms.assetid: eb84c408-2d8b-453b-92f4-5fd8851b84ca
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 52fd844954f41d5d09b5e78f7c23ff6f7469bb43
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793327"
---
# <a name="opentnefstreamex"></a><span data-ttu-id="36f10-103">OpenTnefStreamEx</span><span class="sxs-lookup"><span data-stu-id="36f10-103">OpenTnefStreamEx</span></span>

<span data-ttu-id="36f10-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="36f10-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="36f10-105">Erstellt einen Transport-Neutral Encapsulation Format (TNEF)-Objekt, das zum Ver- oder Entschlüsseln ein Meldungsobjekt in einen Datenstrom von TNEF für die Verwendung von Transporten oder Gateways und Nachrichtenspeicher verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="36f10-105">Creates a Transport-Neutral Encapsulation Format (TNEF) object that can be used to encode or decode a message object into a TNEF data stream for use by transports or gateways and message stores.</span></span> <span data-ttu-id="36f10-106">Dies ist der Einstiegspunkt für TNEF-Zugriff.</span><span class="sxs-lookup"><span data-stu-id="36f10-106">This is the entry point for TNEF access.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="36f10-107">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="36f10-107">Header file:</span></span>  <br/> |<span data-ttu-id="36f10-108">TNEF.h</span><span class="sxs-lookup"><span data-stu-id="36f10-108">Tnef.h</span></span>  <br/> |
|<span data-ttu-id="36f10-109">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="36f10-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="36f10-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="36f10-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="36f10-111">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="36f10-111">Called by:</span></span>  <br/> |<span data-ttu-id="36f10-112">Transportanbieter</span><span class="sxs-lookup"><span data-stu-id="36f10-112">Transport providers</span></span>  <br/> |
   
```cpp
HRESULT OpenTnefStreamEx(
  LPVOID lpvSupport,
  LPSTREAM lpStream,
  LPSTR lpszStreamName,
  ULONG ulFlags,
  LPMESSAGE lpMessage,
  WORD wKeyVal,
  LPADDRESSBOOK lpAddressBook,
  LPITNEF FAR * lppTNEF
);
```

## <a name="parameters"></a><span data-ttu-id="36f10-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="36f10-113">Parameters</span></span>

<span data-ttu-id="36f10-114">_lpvSupport_</span><span class="sxs-lookup"><span data-stu-id="36f10-114">_lpvSupport_</span></span>
  
> <span data-ttu-id="36f10-115">[in] Übergibt ein Support-Objekt oder NULL übergibt.</span><span class="sxs-lookup"><span data-stu-id="36f10-115">[in] Passes a support object, or passes in NULL.</span></span> <span data-ttu-id="36f10-116">Wenn NULL ist, sollte der Parameter _LpAddressBook_ ungleich Null sein.</span><span class="sxs-lookup"><span data-stu-id="36f10-116">If NULL, the  _lpAddressBook_ parameter should be non-null.</span></span> 
    
<span data-ttu-id="36f10-117">_lpStream_</span><span class="sxs-lookup"><span data-stu-id="36f10-117">_lpStream_</span></span>
  
> <span data-ttu-id="36f10-118">[in] Zeiger auf ein Storage Stream-Objekt, wie etwa eine OLE- **IStream** -Schnittstelle, Quelle oder Ziel für eine TNEF-Nachricht Stream bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="36f10-118">[in] Pointer to a storage stream object, such as an OLE **IStream** interface, providing a source or destination for a TNEF stream message.</span></span> 
    
<span data-ttu-id="36f10-119">_lpszStreamName_</span><span class="sxs-lookup"><span data-stu-id="36f10-119">_lpszStreamName_</span></span>
  
> <span data-ttu-id="36f10-120">[in] Zeiger auf den Namen des Datenstroms, die das TNEF-Objekt verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="36f10-120">[in] Pointer to the name of the data stream that the TNEF object uses.</span></span> <span data-ttu-id="36f10-121">Wenn der Aufrufer das Flag TNEF_ENCODE ( _UlFlags_ -Parameter) in dem Aufruf von **OpenTNEFStream nicht ausgeführt werden**festgelegt, muss den _Wert_ -Parameter einen nicht-Null Zeiger auf eine beliebige Zeichen gültig für eine Datei bestehend ungleich Null-Zeichenfolge angeben.</span><span class="sxs-lookup"><span data-stu-id="36f10-121">If the caller has set the TNEF_ENCODE flag ( _ulFlags_ parameter) in its call to **OpenTnefStream**, the  _lpszName_ parameter must specify a non-null pointer to a non-null string consisting of any characters considered valid for naming a file.</span></span> <span data-ttu-id="36f10-122">MAPI lässt nicht Zeichenfolgennamen, einschließlich der Zeichen "[", "]", oder ":", auch wenn das Dateisystem ihre Verwendung ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="36f10-122">MAPI does not allow string names including the characters "[", "]", or ":", even if the file system permits their use.</span></span> <span data-ttu-id="36f10-123">Die Größe der für den _Wert_ -Parameter übergebene Zeichenfolge muss den Wert der MAX_PATH, die maximale Länge einer Zeichenfolge, die ein Pfadname enthält, nicht überschreiten.</span><span class="sxs-lookup"><span data-stu-id="36f10-123">The size of the string passed for the  _lpszName_ parameter must not exceed the value of MAX_PATH, the maximum length of a string that contains a path name.</span></span> 
    
<span data-ttu-id="36f10-124">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="36f10-124">_ulFlags_</span></span>
  
> <span data-ttu-id="36f10-125">[in] Bitmaske aus Flags verwendet, um den Modus der Funktion anzugeben.</span><span class="sxs-lookup"><span data-stu-id="36f10-125">[in] Bitmask of flags used to indicate the mode of the function.</span></span> <span data-ttu-id="36f10-126">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="36f10-126">The following flags can be set:</span></span>
    
<span data-ttu-id="36f10-127">TNEF_BEST_DATA</span><span class="sxs-lookup"><span data-stu-id="36f10-127">TNEF_BEST_DATA</span></span> 
  
> <span data-ttu-id="36f10-128">Alle mögliche Eigenschaften in ihre kompatible Attribute zugeordnet sind, aber bei ein möglichen Datenverlust aufgrund der Konvertierung einer kompatiblen-Attribut vorhanden ist, wird die Eigenschaft auch in der Encapsulations codiert.</span><span class="sxs-lookup"><span data-stu-id="36f10-128">All possible properties are mapped into their down-level attributes, but when there is a possible data loss due to the conversion to a down-level attribute, the property is also encoded in the encapsulations.</span></span> <span data-ttu-id="36f10-129">Beachten Sie, dass dies die Duplizierung von Informationen in der TNEF-Stream verursacht.</span><span class="sxs-lookup"><span data-stu-id="36f10-129">Note that this will cause the duplication of information in the TNEF stream.</span></span> <span data-ttu-id="36f10-130">TNEF_BEST_DATA ist der Standardwert, wenn keine anderen Modi angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="36f10-130">TNEF_BEST_DATA is the default if no other modes are specified.</span></span> 
    
<span data-ttu-id="36f10-131">TNEF_COMPATIBILITY</span><span class="sxs-lookup"><span data-stu-id="36f10-131">TNEF_COMPATIBILITY</span></span> 
  
> <span data-ttu-id="36f10-132">Stellt die Abwärtskompatibilität mit älteren Clientanwendungen bereit.</span><span class="sxs-lookup"><span data-stu-id="36f10-132">Provides backward compatibility with older client applications.</span></span> <span data-ttu-id="36f10-133">TNEF-Streams dieses Flag codiert werden alle mögliche Eigenschaften in die entsprechende kompatible Attribut zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="36f10-133">TNEF streams encoded with this flag will map all possible properties into their corresponding down-level attribute.</span></span> <span data-ttu-id="36f10-134">Dieser Modus wird auch die Standardwerte einiger Eigenschaften, die durch kompatible Clients erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="36f10-134">This mode also causes the defaulting of some properties that are required by down-level clients.</span></span> 
    
  > [!CAUTION]
  > <span data-ttu-id="36f10-135">Dieses Kennzeichen ist veraltet und sollte nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="36f10-135">This flag is obsolete and should not be used.</span></span> 
  
<span data-ttu-id="36f10-136">TNEF_DECODE</span><span class="sxs-lookup"><span data-stu-id="36f10-136">TNEF_DECODE</span></span> 
  
> <span data-ttu-id="36f10-137">Das TNEF-Objekt im angegebenen Stream wird mit schreibgeschützten Zugriff geöffnet.</span><span class="sxs-lookup"><span data-stu-id="36f10-137">The TNEF object on the indicated stream is opened with read-only access.</span></span> <span data-ttu-id="36f10-138">Der Transportdienst muss dieses Flag festgelegt, wenn die Funktion ist das Objekt für die nachfolgende Decodierung nicht initialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="36f10-138">The transport provider must set this flag if the function is to initialize the object for subsequent decoding.</span></span>
    
<span data-ttu-id="36f10-139">TNEF_ENCODE</span><span class="sxs-lookup"><span data-stu-id="36f10-139">TNEF_ENCODE</span></span> 
  
> <span data-ttu-id="36f10-140">Das TNEF-Objekt im angegebenen Stream wird Lese-/Schreibzugriff geöffnet.</span><span class="sxs-lookup"><span data-stu-id="36f10-140">The TNEF object on the indicated stream is opened for read/write permission.</span></span> <span data-ttu-id="36f10-141">Der Transportdienst muss dieses Flag festgelegt, wenn die Funktion zum Initialisieren des Objekts für die nachfolgende Codierung ist.</span><span class="sxs-lookup"><span data-stu-id="36f10-141">The transport provider must set this flag if the function is to initialize the object for subsequent encoding.</span></span>
    
<span data-ttu-id="36f10-142">TNEF_PURE</span><span class="sxs-lookup"><span data-stu-id="36f10-142">TNEF_PURE</span></span> 
  
> <span data-ttu-id="36f10-143">Alle Eigenschaften codiert in die MAPI-Kapselung Blöcke.</span><span class="sxs-lookup"><span data-stu-id="36f10-143">Encodes all properties into the MAPI encapsulation blocks.</span></span> <span data-ttu-id="36f10-144">Aus diesem Grund "reine" TNEF-Datei besteht, höchstens, die Attribute AttMAPIProps, AttAttachment, AttRenddata und AttRecipTable.</span><span class="sxs-lookup"><span data-stu-id="36f10-144">Therefore, a "pure" TNEF file will consist of, at most, the attributes attMAPIProps, attAttachment, attRenddata, and attRecipTable.</span></span> <span data-ttu-id="36f10-145">Dieser Modus ist ideal für die Verwendung, wenn keine Abwärtskompatibilität erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="36f10-145">This mode is ideal for use when no backward compatibility is required.</span></span>
    
<span data-ttu-id="36f10-146">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="36f10-146">_lpMessage_</span></span>
  
> <span data-ttu-id="36f10-147">[in] Zeiger auf ein Objekt "Message" als Ziel für eine entschlüsselte Nachricht mit Anlagen oder eine Quelle für eine codierte Nachricht mit Anlagen.</span><span class="sxs-lookup"><span data-stu-id="36f10-147">[in] Pointer to a message object as a destination for a decoded message with attachments or a source for an encoded message with attachments.</span></span> <span data-ttu-id="36f10-148">Alle Eigenschaften einer Nachricht Ziel können durch die Eigenschaften einer verschlüsselten Nachricht überschrieben werden soll.</span><span class="sxs-lookup"><span data-stu-id="36f10-148">Any properties of a destination message can be overwritten by the properties of an encoded message.</span></span>
    
<span data-ttu-id="36f10-149">_wKeyVal_</span><span class="sxs-lookup"><span data-stu-id="36f10-149">_wKeyVal_</span></span>
  
> <span data-ttu-id="36f10-150">[in] Ein Search-Schlüssel, den das TNEF-Objekt wird verwendet, um Anlagen, die Text-Tags in den Nachrichtentext eingefügt übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="36f10-150">[in] A search key that the TNEF object uses to match attachments to the text tags inserted in the message text.</span></span> <span data-ttu-id="36f10-151">Dieser Wert sollte über Nachrichten relativ eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="36f10-151">This value should be relatively unique across messages.</span></span> 
    
<span data-ttu-id="36f10-152">_lpAddressBook_</span><span class="sxs-lookup"><span data-stu-id="36f10-152">_lpAddressBook_</span></span>
  
> <span data-ttu-id="36f10-153">[in] Zeiger auf eine Adresse Adressbuch-Objekt verwendet, um die Informationen für Eintragsbezeichner Adressierung abrufen.</span><span class="sxs-lookup"><span data-stu-id="36f10-153">[in] Pointer to an address book object used to get addressing information for entry identifiers.</span></span> 
    
<span data-ttu-id="36f10-154">_lppTNEF_</span><span class="sxs-lookup"><span data-stu-id="36f10-154">_lppTNEF_</span></span>
  
> <span data-ttu-id="36f10-155">[out] Zeiger auf das neue TNEF-Objekt.</span><span class="sxs-lookup"><span data-stu-id="36f10-155">[out] Pointer to the new TNEF object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="36f10-156">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="36f10-156">Return value</span></span>

<span data-ttu-id="36f10-157">S_OK</span><span class="sxs-lookup"><span data-stu-id="36f10-157">S_OK</span></span> 
  
> <span data-ttu-id="36f10-158">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="36f10-158">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="36f10-159">Hinweise</span><span class="sxs-lookup"><span data-stu-id="36f10-159">Remarks</span></span>

<span data-ttu-id="36f10-160">Die **OpenTnefStreamEx** -Funktion ist die empfohlene Ersatz für [OpenTNEFStream nicht ausgeführt werden](opentnefstream.md), den ursprünglichen Einstiegspunkt für TNEF-Zugriff.</span><span class="sxs-lookup"><span data-stu-id="36f10-160">The **OpenTnefStreamEx** function is the recommended replacement for [OpenTnefStream](opentnefstream.md), the original entry point for TNEF access.</span></span> 
  
<span data-ttu-id="36f10-161">Ein TNEF-Objekt, das später durch die Funktion **OpenTnefStreamEx** erstellt Ruft die OLE-Methode **IUnknown:: AddRef** Hinzufügen von Verweisen für den Support-Objekt, das Stream-Objekt und Message-Objekts.</span><span class="sxs-lookup"><span data-stu-id="36f10-161">A TNEF object created by the **OpenTnefStreamEx** function later calls the OLE method **IUnknown::AddRef** to add references for the support object, the stream object, and the message object.</span></span> <span data-ttu-id="36f10-162">Der Transportdienst kann die Verweise für alle drei Objekte mit einem einzigen Aufruf der OLE-Methode **IUnknown** für die TNEF-Objekt freigeben.</span><span class="sxs-lookup"><span data-stu-id="36f10-162">The transport provider can release the references for all three objects with a single call to the OLE method **IUnknown::Release** on the TNEF object.</span></span> 
  
<span data-ttu-id="36f10-163">**OpenTnefStreamEx** reserviert und initialisiert ein TNEF-Objekt für den Anbieter in eine MAPI-Nachricht in ein Stream-Nachricht TNEF-Codierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="36f10-163">**OpenTnefStreamEx** allocates and initializes a TNEF object for the provider to use in encoding a MAPI message into a TNEF stream message.</span></span> <span data-ttu-id="36f10-164">Alternativ kann diese Funktion das Objekt für den Anbieter im nachfolgende Aufrufe von [ITnef::ExtractProps](itnef-extractprops.md) zum Decodieren einer TNEF-Stream-Nachricht in einem MAPI-Nachricht verwenden einrichten.</span><span class="sxs-lookup"><span data-stu-id="36f10-164">Alternatively, this function can set up the object for the provider to use in subsequent calls to [ITnef::ExtractProps](itnef-extractprops.md) to decode a TNEF stream message into a MAPI message.</span></span> <span data-ttu-id="36f10-165">Um die TNEF-Objekts frei, und schließen die Sitzung, muss der Adressbuchhierarchie die geerbte **IUnknown** -Methode für das Objekt aufrufen.</span><span class="sxs-lookup"><span data-stu-id="36f10-165">To free the TNEF object and close the session, the transport provider must call the inherited **IUnknown::Release** method on the object.</span></span> 
  
<span data-ttu-id="36f10-166">Der Basiswert für den Parameter _wKeyVal_ darf nicht NULL sein und sollte nicht für jeden Aufruf von **OpenTnefStreamEx**identisch sein.</span><span class="sxs-lookup"><span data-stu-id="36f10-166">The base value for the  _wKeyVal_ parameter must not be zero and should not be the same for every call to **OpenTnefStreamEx**.</span></span> <span data-ttu-id="36f10-167">Verwenden Sie stattdessen Zufallszahlen basierend auf der Systemzeit aus der Laufzeitbibliothek Zufallszahlengenerator.</span><span class="sxs-lookup"><span data-stu-id="36f10-167">Instead, use random numbers based on the system time from the run-time library's random number generator.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="36f10-168">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="36f10-168">MFCMAPI reference</span></span>

<span data-ttu-id="36f10-169">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="36f10-169">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="36f10-170">**Datei**</span><span class="sxs-lookup"><span data-stu-id="36f10-170">**File**</span></span>|<span data-ttu-id="36f10-171">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="36f10-171">**Function**</span></span>|<span data-ttu-id="36f10-172">**Comment**</span><span class="sxs-lookup"><span data-stu-id="36f10-172">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="36f10-173">File.cpp</span><span class="sxs-lookup"><span data-stu-id="36f10-173">File.cpp</span></span>  <br/> |<span data-ttu-id="36f10-174">LoadFromTNEF</span><span class="sxs-lookup"><span data-stu-id="36f10-174">LoadFromTNEF</span></span>  <br/> |<span data-ttu-id="36f10-175">MFCMAPI (engl.) verwendet die **OpenTnefStreamEx** -Methode, um einen Datenstrom für die TNEF-Datei öffnen, damit Eigenschaften extrahiert werden können.</span><span class="sxs-lookup"><span data-stu-id="36f10-175">MFCMAPI uses the **OpenTnefStreamEx** method to open a stream on the TNEF file so properties may be extracted.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="36f10-176">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="36f10-176">See also</span></span>

- [<span data-ttu-id="36f10-177">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="36f10-177">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)
- [<span data-ttu-id="36f10-178">IXPProvider::TransportLogon</span><span class="sxs-lookup"><span data-stu-id="36f10-178">IXPProvider::TransportLogon</span></span>](ixpprovider-transportlogon.md)
- [<span data-ttu-id="36f10-179">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="36f10-179">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

