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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 178ab67875d8fb442500dd412dbafe4403deee16
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406241"
---
# <a name="opentnefstreamex"></a><span data-ttu-id="72567-103">OpenTnefStreamEx</span><span class="sxs-lookup"><span data-stu-id="72567-103">OpenTnefStreamEx</span></span>

<span data-ttu-id="72567-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="72567-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="72567-105">Erstellt ein Transport-Neutral -Objekt (Encapsulation Format, TNEF), das zum Codieren oder Decodieren eines Nachrichtenobjekts in einen TNEF-Datenstrom zur Verwendung durch Transporte oder Gateways und Nachrichtenspeicher verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="72567-105">Creates a Transport-Neutral Encapsulation Format (TNEF) object that can be used to encode or decode a message object into a TNEF data stream for use by transports or gateways and message stores.</span></span> <span data-ttu-id="72567-106">Dies ist der Einstiegspunkt für den TNEF-Zugriff.</span><span class="sxs-lookup"><span data-stu-id="72567-106">This is the entry point for TNEF access.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="72567-107">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="72567-107">Header file:</span></span>  <br/> |<span data-ttu-id="72567-108">Tnef.h</span><span class="sxs-lookup"><span data-stu-id="72567-108">Tnef.h</span></span>  <br/> |
|<span data-ttu-id="72567-109">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="72567-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="72567-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="72567-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="72567-111">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="72567-111">Called by:</span></span>  <br/> |<span data-ttu-id="72567-112">Transportanbieter</span><span class="sxs-lookup"><span data-stu-id="72567-112">Transport providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="72567-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="72567-113">Parameters</span></span>

<span data-ttu-id="72567-114">_lpvSupport_</span><span class="sxs-lookup"><span data-stu-id="72567-114">_lpvSupport_</span></span>
  
> <span data-ttu-id="72567-115">[in] Übergibt ein Supportobjekt oder null.</span><span class="sxs-lookup"><span data-stu-id="72567-115">[in] Passes a support object, or passes in NULL.</span></span> <span data-ttu-id="72567-116">Wenn NULL, sollte  _der lpAddressBook-Parameter_ nicht null sein.</span><span class="sxs-lookup"><span data-stu-id="72567-116">If NULL, the  _lpAddressBook_ parameter should be non-null.</span></span> 
    
<span data-ttu-id="72567-117">_lpStream_</span><span class="sxs-lookup"><span data-stu-id="72567-117">_lpStream_</span></span>
  
> <span data-ttu-id="72567-118">[in] Zeiger auf ein Speicherdatenstromobjekt, z. B. eine OLE **IStream-Schnittstelle,** die eine Quelle oder ein Ziel für eine TNEF-Streamnachricht bietet.</span><span class="sxs-lookup"><span data-stu-id="72567-118">[in] Pointer to a storage stream object, such as an OLE **IStream** interface, providing a source or destination for a TNEF stream message.</span></span> 
    
<span data-ttu-id="72567-119">_lpszStreamName_</span><span class="sxs-lookup"><span data-stu-id="72567-119">_lpszStreamName_</span></span>
  
> <span data-ttu-id="72567-120">[in] Zeiger auf den Namen des Datenstroms, den das TNEF-Objekt verwendet.</span><span class="sxs-lookup"><span data-stu-id="72567-120">[in] Pointer to the name of the data stream that the TNEF object uses.</span></span> <span data-ttu-id="72567-121">Wenn der Aufrufer das TNEF_ENCODE-Flag ( _ulFlags-Parameter)_ in seinem Aufruf von **OpenTnefStream** festgelegt hat, muss der  _lpszName-Parameter_ einen Nicht-Null-Zeiger auf eine Nicht-Null-Zeichenfolge angeben, die aus allen Zeichen besteht, die für die Benennung einer Datei als gültig gelten.</span><span class="sxs-lookup"><span data-stu-id="72567-121">If the caller has set the TNEF_ENCODE flag ( _ulFlags_ parameter) in its call to **OpenTnefStream**, the  _lpszName_ parameter must specify a non-null pointer to a non-null string consisting of any characters considered valid for naming a file.</span></span> <span data-ttu-id="72567-122">MAPI lässt keine Zeichenfolgennamen zu, einschließlich der Zeichen "[", "]" oder ":", auch wenn das Dateisystem die Verwendung zulässt.</span><span class="sxs-lookup"><span data-stu-id="72567-122">MAPI does not allow string names including the characters "[", "]", or ":", even if the file system permits their use.</span></span> <span data-ttu-id="72567-123">Die Größe der zeichenfolge, die für den  _lpszName-Parameter_ übergeben wird, darf den Wert von MAX_PATH, die maximale Länge einer Zeichenfolge, die einen Pfadnamen enthält, nicht überschreiten.</span><span class="sxs-lookup"><span data-stu-id="72567-123">The size of the string passed for the  _lpszName_ parameter must not exceed the value of MAX_PATH, the maximum length of a string that contains a path name.</span></span> 
    
<span data-ttu-id="72567-124">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="72567-124">_ulFlags_</span></span>
  
> <span data-ttu-id="72567-125">[in] Bitmaske von Flags, die verwendet werden, um den Modus der Funktion anzugeben.</span><span class="sxs-lookup"><span data-stu-id="72567-125">[in] Bitmask of flags used to indicate the mode of the function.</span></span> <span data-ttu-id="72567-126">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="72567-126">The following flags can be set:</span></span>
    
<span data-ttu-id="72567-127">TNEF_BEST_DATA</span><span class="sxs-lookup"><span data-stu-id="72567-127">TNEF_BEST_DATA</span></span> 
  
> <span data-ttu-id="72567-128">Alle möglichen Eigenschaften werden ihren Attributen auf der ebeneren Ebene zugeordnet, aber wenn aufgrund der Konvertierung in ein Down-Level-Attribut ein möglicher Datenverlust besteht, wird die Eigenschaft auch in den Kapselungen codiert.</span><span class="sxs-lookup"><span data-stu-id="72567-128">All possible properties are mapped into their down-level attributes, but when there is a possible data loss due to the conversion to a down-level attribute, the property is also encoded in the encapsulations.</span></span> <span data-ttu-id="72567-129">Beachten Sie, dass dadurch die Duplizierung von Informationen im TNEF-Stream verursacht wird.</span><span class="sxs-lookup"><span data-stu-id="72567-129">Note that this will cause the duplication of information in the TNEF stream.</span></span> <span data-ttu-id="72567-130">TNEF_BEST_DATA ist die Standardeinstellung, wenn keine anderen Modi angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="72567-130">TNEF_BEST_DATA is the default if no other modes are specified.</span></span> 
    
<span data-ttu-id="72567-131">TNEF_COMPATIBILITY</span><span class="sxs-lookup"><span data-stu-id="72567-131">TNEF_COMPATIBILITY</span></span> 
  
> <span data-ttu-id="72567-132">Bietet Abwärtskompatibilität mit älteren Clientanwendungen.</span><span class="sxs-lookup"><span data-stu-id="72567-132">Provides backward compatibility with older client applications.</span></span> <span data-ttu-id="72567-133">Mit diesem Flag codierte TNEF-Datenströme ordnen alle möglichen Eigenschaften ihrem entsprechenden Attribut auf unterer Ebene zu.</span><span class="sxs-lookup"><span data-stu-id="72567-133">TNEF streams encoded with this flag will map all possible properties into their corresponding down-level attribute.</span></span> <span data-ttu-id="72567-134">Dieser Modus bewirkt auch die Standardeinstellung einiger Eigenschaften, die für Clients auf ebener Ebene erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="72567-134">This mode also causes the defaulting of some properties that are required by down-level clients.</span></span> 
    
  > [!CAUTION]
  > <span data-ttu-id="72567-135">Dieses Flag ist veraltet und sollte nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="72567-135">This flag is obsolete and should not be used.</span></span> 
  
<span data-ttu-id="72567-136">TNEF_DECODE</span><span class="sxs-lookup"><span data-stu-id="72567-136">TNEF_DECODE</span></span> 
  
> <span data-ttu-id="72567-137">Das TNEF-Objekt im angegebenen Datenstrom wird mit schreibgeschützten Zugriff geöffnet.</span><span class="sxs-lookup"><span data-stu-id="72567-137">The TNEF object on the indicated stream is opened with read-only access.</span></span> <span data-ttu-id="72567-138">Der Transportanbieter muss dieses Flag festlegen, wenn die Funktion das Objekt für die nachfolgende Decodierung initialisieren soll.</span><span class="sxs-lookup"><span data-stu-id="72567-138">The transport provider must set this flag if the function is to initialize the object for subsequent decoding.</span></span>
    
<span data-ttu-id="72567-139">TNEF_ENCODE</span><span class="sxs-lookup"><span data-stu-id="72567-139">TNEF_ENCODE</span></span> 
  
> <span data-ttu-id="72567-140">Das TNEF-Objekt im angegebenen Datenstrom wird für Lese-/Schreibberechtigungen geöffnet.</span><span class="sxs-lookup"><span data-stu-id="72567-140">The TNEF object on the indicated stream is opened for read/write permission.</span></span> <span data-ttu-id="72567-141">Der Transportanbieter muss dieses Flag festlegen, wenn die Funktion das Objekt für die nachfolgende Codierung initialisieren soll.</span><span class="sxs-lookup"><span data-stu-id="72567-141">The transport provider must set this flag if the function is to initialize the object for subsequent encoding.</span></span>
    
<span data-ttu-id="72567-142">TNEF_PURE</span><span class="sxs-lookup"><span data-stu-id="72567-142">TNEF_PURE</span></span> 
  
> <span data-ttu-id="72567-143">Codiert alle Eigenschaften in die MAPI-Kapselungsblöcke.</span><span class="sxs-lookup"><span data-stu-id="72567-143">Encodes all properties into the MAPI encapsulation blocks.</span></span> <span data-ttu-id="72567-144">Daher besteht eine "reine" TNEF-Datei aus den Attributen attMAPIProps, attAttachment, attRenddata und attRecipTable.</span><span class="sxs-lookup"><span data-stu-id="72567-144">Therefore, a "pure" TNEF file will consist of, at most, the attributes attMAPIProps, attAttachment, attRenddata, and attRecipTable.</span></span> <span data-ttu-id="72567-145">Dieser Modus eignet sich ideal, wenn keine Abwärtskompatibilität erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="72567-145">This mode is ideal for use when no backward compatibility is required.</span></span>
    
<span data-ttu-id="72567-146">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="72567-146">_lpMessage_</span></span>
  
> <span data-ttu-id="72567-147">[in] Zeiger auf ein Nachrichtenobjekt als Ziel für eine decodierte Nachricht mit Anlagen oder eine Quelle für eine codierte Nachricht mit Anlagen.</span><span class="sxs-lookup"><span data-stu-id="72567-147">[in] Pointer to a message object as a destination for a decoded message with attachments or a source for an encoded message with attachments.</span></span> <span data-ttu-id="72567-148">Alle Eigenschaften einer Zielnachricht können von den Eigenschaften einer codierten Nachricht überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="72567-148">Any properties of a destination message can be overwritten by the properties of an encoded message.</span></span>
    
<span data-ttu-id="72567-149">_wKeyVal_</span><span class="sxs-lookup"><span data-stu-id="72567-149">_wKeyVal_</span></span>
  
> <span data-ttu-id="72567-150">[in] Ein Suchschlüssel, den das TNEF-Objekt verwendet, um Anlagen mit den im Nachrichtentext eingefügten Texttags zu versehen.</span><span class="sxs-lookup"><span data-stu-id="72567-150">[in] A search key that the TNEF object uses to match attachments to the text tags inserted in the message text.</span></span> <span data-ttu-id="72567-151">Dieser Wert sollte nachrichtenübergreifend relativ eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="72567-151">This value should be relatively unique across messages.</span></span> 
    
<span data-ttu-id="72567-152">_lpAddressBook_</span><span class="sxs-lookup"><span data-stu-id="72567-152">_lpAddressBook_</span></span>
  
> <span data-ttu-id="72567-153">[in] Zeiger auf ein Adressbuchobjekt, das zum Erhalten von Adressierungsinformationen für Eintragsbezeichner verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="72567-153">[in] Pointer to an address book object used to get addressing information for entry identifiers.</span></span> 
    
<span data-ttu-id="72567-154">_lppTNEF_</span><span class="sxs-lookup"><span data-stu-id="72567-154">_lppTNEF_</span></span>
  
> <span data-ttu-id="72567-155">[out] Zeiger auf das neue TNEF-Objekt.</span><span class="sxs-lookup"><span data-stu-id="72567-155">[out] Pointer to the new TNEF object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="72567-156">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="72567-156">Return value</span></span>

<span data-ttu-id="72567-157">S_OK</span><span class="sxs-lookup"><span data-stu-id="72567-157">S_OK</span></span> 
  
> <span data-ttu-id="72567-158">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="72567-158">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="72567-159">Hinweise</span><span class="sxs-lookup"><span data-stu-id="72567-159">Remarks</span></span>

<span data-ttu-id="72567-160">Die **OpenTnefStreamEx-Funktion** ist der empfohlene Ersatz für [OpenTnefStream](opentnefstream.md), den ursprünglichen Einstiegspunkt für den TNEF-Zugriff.</span><span class="sxs-lookup"><span data-stu-id="72567-160">The **OpenTnefStreamEx** function is the recommended replacement for [OpenTnefStream](opentnefstream.md), the original entry point for TNEF access.</span></span> 
  
<span data-ttu-id="72567-161">Ein von der **OpenTnefStreamEx-Funktion** erstelltes TNEF-Objekt ruft später die OLE-Methode **IUnknown::AddRef** auf, um Verweise für das Supportobjekt, das Stream-Objekt und das Message-Objekt hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="72567-161">A TNEF object created by the **OpenTnefStreamEx** function later calls the OLE method **IUnknown::AddRef** to add references for the support object, the stream object, and the message object.</span></span> <span data-ttu-id="72567-162">Der Transportanbieter kann die Verweise für alle drei Objekte mit einem einzigen Aufruf der OLE-Methode **IUnknown::Release für** das TNEF-Objekt los.</span><span class="sxs-lookup"><span data-stu-id="72567-162">The transport provider can release the references for all three objects with a single call to the OLE method **IUnknown::Release** on the TNEF object.</span></span> 
  
<span data-ttu-id="72567-163">**OpenTnefStreamEx** weist ein TNEF-Objekt zu, das der Anbieter beim Codieren einer MAPI-Nachricht in eine TNEF-Streamnachricht verwenden soll, und initialisiert es.</span><span class="sxs-lookup"><span data-stu-id="72567-163">**OpenTnefStreamEx** allocates and initializes a TNEF object for the provider to use in encoding a MAPI message into a TNEF stream message.</span></span> <span data-ttu-id="72567-164">Alternativ kann diese Funktion das Objekt für den Anbieter einrichten, das in nachfolgenden Aufrufen von [ITnef::ExtractProps](itnef-extractprops.md) verwendet werden soll, um eine TNEF-Streamnachricht in eine MAPI-Nachricht zu decodieren.</span><span class="sxs-lookup"><span data-stu-id="72567-164">Alternatively, this function can set up the object for the provider to use in subsequent calls to [ITnef::ExtractProps](itnef-extractprops.md) to decode a TNEF stream message into a MAPI message.</span></span> <span data-ttu-id="72567-165">Um das TNEF-Objekt frei zu geben und die Sitzung zu schließen, muss der Transportanbieter die geerbte **IUnknown::Release-Methode** für das Objekt aufrufen.</span><span class="sxs-lookup"><span data-stu-id="72567-165">To free the TNEF object and close the session, the transport provider must call the inherited **IUnknown::Release** method on the object.</span></span> 
  
<span data-ttu-id="72567-166">Der Basiswert für den _wKeyVal-Parameter_ darf nicht null sein und sollte nicht für jeden Aufruf von **OpenTnefStreamEx gleich sein.**</span><span class="sxs-lookup"><span data-stu-id="72567-166">The base value for the  _wKeyVal_ parameter must not be zero and should not be the same for every call to **OpenTnefStreamEx**.</span></span> <span data-ttu-id="72567-167">Verwenden Sie stattdessen Zufallszahlen basierend auf der Systemzeit aus dem Zufallszahlengenerator der Laufzeitbibliothek.</span><span class="sxs-lookup"><span data-stu-id="72567-167">Instead, use random numbers based on the system time from the run-time library's random number generator.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="72567-168">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="72567-168">MFCMAPI reference</span></span>

<span data-ttu-id="72567-169">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="72567-169">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="72567-170">**Datei**</span><span class="sxs-lookup"><span data-stu-id="72567-170">**File**</span></span>|<span data-ttu-id="72567-171">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="72567-171">**Function**</span></span>|<span data-ttu-id="72567-172">**Comment**</span><span class="sxs-lookup"><span data-stu-id="72567-172">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="72567-173">File.cpp</span><span class="sxs-lookup"><span data-stu-id="72567-173">File.cpp</span></span>  <br/> |<span data-ttu-id="72567-174">LoadFromTNEF</span><span class="sxs-lookup"><span data-stu-id="72567-174">LoadFromTNEF</span></span>  <br/> |<span data-ttu-id="72567-175">MFCMAPI verwendet die **OpenTnefStreamEx-Methode,** um einen Datenstrom in der TNEF-Datei zu öffnen, damit Eigenschaften extrahiert werden können.</span><span class="sxs-lookup"><span data-stu-id="72567-175">MFCMAPI uses the **OpenTnefStreamEx** method to open a stream on the TNEF file so properties may be extracted.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="72567-176">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="72567-176">See also</span></span>

- [<span data-ttu-id="72567-177">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="72567-177">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)
- [<span data-ttu-id="72567-178">IXPProvider::TransportLogon</span><span class="sxs-lookup"><span data-stu-id="72567-178">IXPProvider::TransportLogon</span></span>](ixpprovider-transportlogon.md)
- [<span data-ttu-id="72567-179">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="72567-179">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

