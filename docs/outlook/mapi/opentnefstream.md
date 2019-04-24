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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 524b52026010b9a06d5822b48b7c04bbf90a113e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348923"
---
# <a name="opentnefstream"></a><span data-ttu-id="7888e-103">OpenTnefStream</span><span class="sxs-lookup"><span data-stu-id="7888e-103">OpenTnefStream</span></span>

<span data-ttu-id="7888e-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7888e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7888e-105">Wird von einem Transportanbieter aufgerufen, um eine TNEF-Sitzung (MAPI Transport Neutral Encapsulation Format) zu initiieren.</span><span class="sxs-lookup"><span data-stu-id="7888e-105">Called by a transport provider to initiate a MAPI Transport Neutral Encapsulation Format (TNEF) session.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7888e-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="7888e-106">Header file:</span></span>  <br/> |<span data-ttu-id="7888e-107">TNEF. h</span><span class="sxs-lookup"><span data-stu-id="7888e-107">Tnef.h</span></span>  <br/> |
|<span data-ttu-id="7888e-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="7888e-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="7888e-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="7888e-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="7888e-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="7888e-110">Called by:</span></span>  <br/> |<span data-ttu-id="7888e-111">Transport Anbieter</span><span class="sxs-lookup"><span data-stu-id="7888e-111">Transport providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="7888e-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="7888e-112">Parameters</span></span>

<span data-ttu-id="7888e-113">_lpvSupport_</span><span class="sxs-lookup"><span data-stu-id="7888e-113">_lpvSupport_</span></span>
  
> <span data-ttu-id="7888e-114">in Übergibt ein Support-Objekt oder übergibt NULL.</span><span class="sxs-lookup"><span data-stu-id="7888e-114">[in] Passes a support object, or passes in NULL.</span></span> 
    
<span data-ttu-id="7888e-115">_lpStream_</span><span class="sxs-lookup"><span data-stu-id="7888e-115">_lpStream_</span></span>
  
> <span data-ttu-id="7888e-116">in Zeiger auf ein Speicher Stream-Objekt OLE **IStream** -Schnittstelle, die eine Quelle oder ein Ziel für eine TNEF-Stream-Nachricht bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="7888e-116">[in] Pointer to a storage stream object OLE **IStream** interface providing a source or destination for a TNEF stream message.</span></span> 
    
<span data-ttu-id="7888e-117">_lpszStreamName_</span><span class="sxs-lookup"><span data-stu-id="7888e-117">_lpszStreamName_</span></span>
  
> <span data-ttu-id="7888e-118">in Zeiger auf den Namen des Datenstroms, den das TNEF-Objekt verwendet.</span><span class="sxs-lookup"><span data-stu-id="7888e-118">[in] Pointer to the name of the data stream that the TNEF object uses.</span></span> <span data-ttu-id="7888e-119">Wenn der Aufrufer das TNEF_ENCODE-Flag ( _ulFlags_ -Parameter) beim Aufruf von **OpenTnefStream**festgelegt hat, muss der Parameter _lpszName_ einen nicht-NULL-Zeiger auf eine nicht-NULL-Zeichenfolge angeben, die aus allen für die Benennung einer Datei gültigen Zeichen besteht.</span><span class="sxs-lookup"><span data-stu-id="7888e-119">If the caller has set the TNEF_ENCODE flag ( _ulFlags_ parameter) in its call to **OpenTnefStream**, the  _lpszName_ parameter must specify a non-null pointer to a non-null string consisting of any characters considered valid for naming a file.</span></span> <span data-ttu-id="7888e-120">MAPI erlaubt keine Zeichenfolgennamen, einschließlich der Zeichen "[", "]" oder ":", auch wenn das Dateisystem ihre Verwendung zulässt.</span><span class="sxs-lookup"><span data-stu-id="7888e-120">MAPI does not allow string names including the characters "[", "]", or ":", even if the file system permits their use.</span></span> <span data-ttu-id="7888e-121">Die Größe der für _lpszName_ übergebenen Zeichenfolge darf den Wert von MAX_PATH, die maximale Länge einer Zeichenfolge, die einen Pfadnamen enthält, nicht überschreiten.</span><span class="sxs-lookup"><span data-stu-id="7888e-121">The size of the string passed for  _lpszName_ must not exceed the value of MAX_PATH, the maximum length of a string that contains a path name.</span></span> 
    
<span data-ttu-id="7888e-122">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="7888e-122">_ulFlags_</span></span>
  
> <span data-ttu-id="7888e-123">in Bitmaske der Flags, die zum Anzeigen des Modus der Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7888e-123">[in] Bitmask of flags used to indicate the mode of the function.</span></span> <span data-ttu-id="7888e-124">Die folgenden Flags können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="7888e-124">The following flags can be set:</span></span>
    
<span data-ttu-id="7888e-125">TNEF_BEST_DATA</span><span class="sxs-lookup"><span data-stu-id="7888e-125">TNEF_BEST_DATA</span></span> 
  
> <span data-ttu-id="7888e-126">Alle möglichen Eigenschaften werden in ihre untergeordneten Attribute zugeordnet, aber wenn ein möglicher Datenverlust aufgrund der Konvertierung in ein Down-Level-Attribut vorhanden ist, wird die Eigenschaft auch in den Kapselungs codiert.</span><span class="sxs-lookup"><span data-stu-id="7888e-126">All possible properties are mapped into their down-level attributes, but when there is a possible data loss due to the conversion to a down-level attribute, the property is also encoded in the encapsulations.</span></span> <span data-ttu-id="7888e-127">Beachten Sie, dass dadurch die Duplizierung von Informationen im TNEF-Stream verursacht wird.</span><span class="sxs-lookup"><span data-stu-id="7888e-127">Note that this will cause the duplication of information in the TNEF stream.</span></span> <span data-ttu-id="7888e-128">TNEF_BEST_DATA ist der Standardwert, wenn keine anderen Modi angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="7888e-128">TNEF_BEST_DATA is the default if no other modes are specified.</span></span> 
    
<span data-ttu-id="7888e-129">TNEF_COMPATIBILITY</span><span class="sxs-lookup"><span data-stu-id="7888e-129">TNEF_COMPATIBILITY</span></span> 
  
> <span data-ttu-id="7888e-130">Bietet Abwärtskompatibilität mit älteren Clientanwendungen.</span><span class="sxs-lookup"><span data-stu-id="7888e-130">Provides backward compatibility with the older client applications.</span></span> <span data-ttu-id="7888e-131">Mit diesem Flag codierte TNEF-Streams ordnen alle möglichen Eigenschaften dem entsprechenden Down-Level-Attribut zu.</span><span class="sxs-lookup"><span data-stu-id="7888e-131">TNEF streams encoded with this flag will map all possible properties into their corresponding down-level attribute.</span></span> <span data-ttu-id="7888e-132">Dieser Modus bewirkt auch die Standardeinstellung einiger Eigenschaften, die von Clients der untergeordneten Ebene benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="7888e-132">This mode also causes the defaulting of some properties that are required by down-level clients.</span></span> 
    
  > [!CAUTION]
  > <span data-ttu-id="7888e-133">Dieses Flag ist veraltet und sollte nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7888e-133">This flag is obsolete and should not be used.</span></span> 
  
<span data-ttu-id="7888e-134">TNEF_DECODE</span><span class="sxs-lookup"><span data-stu-id="7888e-134">TNEF_DECODE</span></span> 
  
> <span data-ttu-id="7888e-135">Das TNEF-Objekt des angegebenen Streams wird mit schreibgeschütztem Zugriff geöffnet.</span><span class="sxs-lookup"><span data-stu-id="7888e-135">The TNEF object on the indicated stream is opened with read-only access.</span></span> <span data-ttu-id="7888e-136">Der Transportanbieter muss dieses Flag festlegen, wenn die Funktion das Objekt für die spätere Decodierung initialisieren soll.</span><span class="sxs-lookup"><span data-stu-id="7888e-136">The transport provider must set this flag if it wants the function to initialize the object for subsequent decoding.</span></span>
    
<span data-ttu-id="7888e-137">TNEF_ENCODE</span><span class="sxs-lookup"><span data-stu-id="7888e-137">TNEF_ENCODE</span></span> 
  
> <span data-ttu-id="7888e-138">Das TNEF-Objekt des angegebenen Streams wird für Lese-/Schreibzugriff geöffnet.</span><span class="sxs-lookup"><span data-stu-id="7888e-138">The TNEF object on the indicated stream is opened for read/write permission.</span></span> <span data-ttu-id="7888e-139">Der Transportanbieter muss dieses Flag festlegen, wenn die Funktion das Objekt für die nachfolgende Codierung initialisieren soll.</span><span class="sxs-lookup"><span data-stu-id="7888e-139">The transport provider must set this flag if it wants the function to initialize the object for subsequent encoding.</span></span>
    
<span data-ttu-id="7888e-140">TNEF_PURE</span><span class="sxs-lookup"><span data-stu-id="7888e-140">TNEF_PURE</span></span> 
  
> <span data-ttu-id="7888e-141">Codiert alle Eigenschaften in die MAPI-Kapselungs Blöcke.</span><span class="sxs-lookup"><span data-stu-id="7888e-141">Encodes all properties into the MAPI encapsulation blocks.</span></span> <span data-ttu-id="7888e-142">Daher besteht eine "reine" TNEF-Datei aus höchstens attMAPIProps, attAttachment, attRenddata und attRecipTable.</span><span class="sxs-lookup"><span data-stu-id="7888e-142">Therefore, a "pure" TNEF file will consist of, at most, attMAPIProps, attAttachment, attRenddata, and attRecipTable.</span></span> <span data-ttu-id="7888e-143">Dieser Modus eignet sich ideal für den Fall, dass keine Abwärtskompatibilität erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="7888e-143">This mode is ideal for use when no backward compatibility is required.</span></span>
    
<span data-ttu-id="7888e-144">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="7888e-144">_lpMessage_</span></span>
  
> <span data-ttu-id="7888e-145">in Zeiger auf ein Nachrichtenobjekt als Ziel für eine decodierte Nachricht mit Anlagen oder eine Quelle für eine codierte Nachricht mit Anlagen.</span><span class="sxs-lookup"><span data-stu-id="7888e-145">[in] Pointer to a message object as a destination for a decoded message with attachments or a source for an encoded message with attachments.</span></span> <span data-ttu-id="7888e-146">Alle Eigenschaften einer Zielnachricht werden möglicherweise durch die Eigenschaften einer codierten Nachricht überschrieben.</span><span class="sxs-lookup"><span data-stu-id="7888e-146">Any properties of a destination message might be overwritten by the properties of an encoded message.</span></span>
    
<span data-ttu-id="7888e-147">_wTaste_</span><span class="sxs-lookup"><span data-stu-id="7888e-147">_wKey_</span></span>
  
> <span data-ttu-id="7888e-148">in Ein Suchschlüssel, den das TNEF-Objekt verwendet, um Anlagen mit den im Nachrichtentext eingefügten Text Tags zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="7888e-148">[in] A search key that the TNEF object uses to match attachments to the text tags inserted in the message text.</span></span> <span data-ttu-id="7888e-149">Dieser Wert sollte für Nachrichten relativ eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="7888e-149">This value should be relatively unique across messages.</span></span>
    
<span data-ttu-id="7888e-150">_lppTNEF_</span><span class="sxs-lookup"><span data-stu-id="7888e-150">_lppTNEF_</span></span>
  
> <span data-ttu-id="7888e-151">Out Zeiger auf das neue TNEF-Objekt.</span><span class="sxs-lookup"><span data-stu-id="7888e-151">[out] Pointer to the new TNEF object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7888e-152">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7888e-152">Return value</span></span>

<span data-ttu-id="7888e-153">S_OK</span><span class="sxs-lookup"><span data-stu-id="7888e-153">S_OK</span></span> 
  
> <span data-ttu-id="7888e-154">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="7888e-154">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7888e-155">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7888e-155">Remarks</span></span>

<span data-ttu-id="7888e-156">Ein von der **OpenTnefStream** -Funktion erstelltes TNEF-Objekt ruft später die OLE-Methode **IUnknown:: AddRef** auf, um Verweise für das Support-Objekt, das Stream-Objekt und das Message-Objekt hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="7888e-156">A TNEF object created by the **OpenTnefStream** function later calls the OLE method **IUnknown::AddRef** to add references for the support object, the stream object, and the message object.</span></span> <span data-ttu-id="7888e-157">Der Transportanbieter kann die Verweise für alle drei Objekte mit einem einzigen Aufruf an die OLE-Methode **IUnknown:: Release** für das TNEF-Objekt freigeben.</span><span class="sxs-lookup"><span data-stu-id="7888e-157">The transport provider can release the references for all three objects with a single call to the OLE method **IUnknown::Release** on the TNEF object.</span></span> 
  
<span data-ttu-id="7888e-158">**OpenTnefStream** ordnet eine TNEF-Objekt **ITnef** -Schnittstelle für den Anbieter zu, die beim Codieren einer MAPI-Nachricht **IMessage** -Schnittstelle in eine TNEF-Stream-Nachricht verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="7888e-158">**OpenTnefStream** allocates and initializes a TNEF object **ITnef** interface for the provider to use in encoding a MAPI message **IMessage** interface into a TNEF stream message.</span></span> <span data-ttu-id="7888e-159">Alternativ kann die Funktion das Objekt für den Anbieter einrichten, der in nachfolgenden Aufrufen von [ITnef:: ExtractProps](itnef-extractprops.md) zum Decodieren einer TNEF-Stream-Nachricht in eine MAPI-Nachricht verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="7888e-159">Alternatively, the function can set up the object for the provider to use in subsequent calls to [ITnef::ExtractProps](itnef-extractprops.md) to decode a TNEF stream message into a MAPI message.</span></span> <span data-ttu-id="7888e-160">Wenn Sie das TNEF-Objekt freigeben und die Sitzung beenden möchten, muss der Transportanbieter die geerbte **IUnknown:: Release** -Methode für das Objekt aufrufen.</span><span class="sxs-lookup"><span data-stu-id="7888e-160">To free the TNEF object and close the session, the transport provider must call the inherited **IUnknown::Release** method on the object.</span></span> 
  
<span data-ttu-id="7888e-161">Diese Funktion ist der ursprüngliche Einstiegspunkt für den TNEF-Zugriff und wurde durch [OpenTnefStreamEx](opentnefstreamex.md) ersetzt, Sie wird jedoch weiterhin für die Kompatibilität mit TNEF verwendet.</span><span class="sxs-lookup"><span data-stu-id="7888e-161">This function is the original entry point for TNEF access and has been replaced by [OpenTnefStreamEx](opentnefstreamex.md) but is still used for compatibility for those already using TNEF.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7888e-162">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7888e-162">See also</span></span>

- [<span data-ttu-id="7888e-163">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="7888e-163">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)
- [<span data-ttu-id="7888e-164">IXPProvider::TransportLogon</span><span class="sxs-lookup"><span data-stu-id="7888e-164">IXPProvider::TransportLogon</span></span>](ixpprovider-transportlogon.md)

