---
title: OpenStreamOnFile
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.OpenStreamOnFile
api_type:
- COM
ms.assetid: 01fa459f-597d-4b16-b340-a79fb270cd71
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 9f37e57f997ead58b1ef0e9a27ccbdb0a810be06
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571955"
---
# <a name="openstreamonfile"></a><span data-ttu-id="f3eab-103">OpenStreamOnFile</span><span class="sxs-lookup"><span data-stu-id="f3eab-103">OpenStreamOnFile</span></span>

  
  
<span data-ttu-id="f3eab-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f3eab-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f3eab-105">Reserviert und initialisiert ein OLE- **IStream** -Objekt Zugriff auf den Inhalt einer Datei.</span><span class="sxs-lookup"><span data-stu-id="f3eab-105">Allocates and initializes an OLE **IStream** object to access the contents of a file.</span></span> <span data-ttu-id="f3eab-106">Diese Funktion übernimmt eine ANSI-Zeichenfolge als der Dateinamen einschließlich der Pfad und der Dateierweiterung, daher Verwendung der Unicode-Version dieser Funktion, [OpenStreamOnFileW](openstreamonfilew.md), wird empfohlen.</span><span class="sxs-lookup"><span data-stu-id="f3eab-106">This function takes an ANSI string as the file name including the path and the file extension, therefore, use of the Unicode version of this function, [OpenStreamOnFileW](openstreamonfilew.md), is recommended.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f3eab-107">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="f3eab-107">Header file:</span></span>  <br/> |<span data-ttu-id="f3eab-108">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="f3eab-108">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="f3eab-109">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="f3eab-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="f3eab-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="f3eab-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="f3eab-111">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="f3eab-111">Called by:</span></span>  <br/> |<span data-ttu-id="f3eab-112">Clientanwendungen und -Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="f3eab-112">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT STDMETHODCALLTYPE OpenStreamOnFile(
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPFREEBUFFER lpFreeBuffer,
  ULONG ulFlags,
  LPSTR lpszFileName,
  LPSTR lpszPrefix,
  LPSTREAM FAR * lppStream
);
```

## <a name="parameters"></a><span data-ttu-id="f3eab-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="f3eab-113">Parameters</span></span>

 <span data-ttu-id="f3eab-114">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="f3eab-114">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="f3eab-115">[in] Zeiger auf die Funktion [MAPIAllocateBuffer](mapiallocatebuffer.md) , Speicher verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="f3eab-115">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
 <span data-ttu-id="f3eab-116">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="f3eab-116">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="f3eab-117">[in] Zeiger auf die [MAPIFreeBuffer](mapifreebuffer.md) -Funktion verwendet werden, um Arbeitsspeicher freizugeben.</span><span class="sxs-lookup"><span data-stu-id="f3eab-117">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
 <span data-ttu-id="f3eab-118">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f3eab-118">_ulFlags_</span></span>
  
> <span data-ttu-id="f3eab-119">[in] Bitmaske der Flags verwendet, um das Erstellen oder Öffnen der Datei steuern über das OLE- **IStream** -Objekt zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="f3eab-119">[in] Bitmask of flags used to control the creation or opening of the file to be accessed through the OLE **IStream** object.</span></span> <span data-ttu-id="f3eab-120">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="f3eab-120">The following flags can be set:</span></span> 
    
<span data-ttu-id="f3eab-121">SOF_UNIQUEFILENAME</span><span class="sxs-lookup"><span data-stu-id="f3eab-121">SOF_UNIQUEFILENAME</span></span> 
  
> <span data-ttu-id="f3eab-122">Eine temporäre Datei ist für das **IStream** -Objekt erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f3eab-122">A temporary file is to be created for the **IStream** object.</span></span> <span data-ttu-id="f3eab-123">Wenn dieses Flag festgelegt ist, sollte die Flags STGM_CREATE und Accessor auch festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="f3eab-123">If this flag is set, the STGM_CREATE and STGM_READWRITE flags should also be set.</span></span> 
    
<span data-ttu-id="f3eab-124">STGM_CREATE</span><span class="sxs-lookup"><span data-stu-id="f3eab-124">STGM_CREATE</span></span> 
  
> <span data-ttu-id="f3eab-125">Die Datei ist erstellt werden soll, auch wenn Sie bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="f3eab-125">The file is to be created even if one already exists.</span></span> <span data-ttu-id="f3eab-126">Wenn der Parameter _LpszFileName_ nicht festgelegt ist, muss dieses Flag und die STGM_DELETEONRELEASE festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="f3eab-126">If the  _lpszFileName_ parameter is not set, both this flag and STGM_DELETEONRELEASE must be set.</span></span> <span data-ttu-id="f3eab-127">Wenn STGM_CREATE festgelegt ist, muss auch die Accessor-Flag festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="f3eab-127">If STGM_CREATE is set, the STGM_READWRITE flag must also be set.</span></span> 
    
<span data-ttu-id="f3eab-128">STGM_DELETEONRELEASE</span><span class="sxs-lookup"><span data-stu-id="f3eab-128">STGM_DELETEONRELEASE</span></span> 
  
> <span data-ttu-id="f3eab-129">Die Datei wird gelöscht, wenn das Objekt **IStream** freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="f3eab-129">The file is to be deleted when the **IStream** object is released.</span></span> <span data-ttu-id="f3eab-130">Wenn der Parameter _LpszFileName_ nicht festgelegt ist, muss dieses Flag und die STGM_CREATE festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="f3eab-130">If the  _lpszFileName_ parameter is not set, both this flag and STGM_CREATE must be set.</span></span> 
    
<span data-ttu-id="f3eab-131">BEISPIELCODEZEILEN</span><span class="sxs-lookup"><span data-stu-id="f3eab-131">STGM_READ</span></span> 
  
> <span data-ttu-id="f3eab-132">Die Datei wird mit schreibgeschützten Zugriff geöffnet oder erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="f3eab-132">The file is to be created or opened with read-only access.</span></span> 
    
<span data-ttu-id="f3eab-133">ACCESSOR</span><span class="sxs-lookup"><span data-stu-id="f3eab-133">STGM_READWRITE</span></span> 
  
> <span data-ttu-id="f3eab-134">Die Datei wird erstellt oder mit Lese-/Schreibzugriff geöffnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="f3eab-134">The file is to be created or opened with read/write permission.</span></span> <span data-ttu-id="f3eab-135">Wenn dieses Flag nicht festgelegt ist, muss das Flag STGM_CREATE nicht festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="f3eab-135">If this flag is not set, the STGM_CREATE flag must not be set either.</span></span> 
    
 <span data-ttu-id="f3eab-136">_lpszFileName_</span><span class="sxs-lookup"><span data-stu-id="f3eab-136">_lpszFileName_</span></span>
  
> <span data-ttu-id="f3eab-137">[in] Der Dateiname, einschließlich Pfad und Erweiterung, der die Datei für die **OpenStreamOnFile nicht ausgeführt werden** **IStream** -Objekt initialisiert.</span><span class="sxs-lookup"><span data-stu-id="f3eab-137">[in] The filename, including path and extension, of the file for which **OpenStreamOnFile** initializes the **IStream** object.</span></span> <span data-ttu-id="f3eab-138">Wenn das Flag SOF_UNIQUEFILENAME festgelegt ist, enthält _LpszFileName_ den Pfad zu dem Verzeichnis, in dem Sie eine temporäre Datei zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="f3eab-138">If the SOF_UNIQUEFILENAME flag is set,  _lpszFileName_ contains the path to the directory in which to create a temporary file.</span></span> <span data-ttu-id="f3eab-139">Wenn _LpszFileName_ NULL ist, **OpenStreamOnFile nicht ausgeführt werden** ruft geeigneten Pfad aus dem System und die STGM_CREATE und die STGM_DELETEONRELEASE Flags müssen festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="f3eab-139">If  _lpszFileName_ is NULL, **OpenStreamOnFile** obtains an appropriate path from the system, and both the STGM_CREATE and STGM_DELETEONRELEASE flags must be set.</span></span> 
    
 <span data-ttu-id="f3eab-140">_lpszPrefix_</span><span class="sxs-lookup"><span data-stu-id="f3eab-140">_lpszPrefix_</span></span>
  
> <span data-ttu-id="f3eab-141">[in] Das Präfix für den Dateinamen an, auf dem **OpenStreamOnFile nicht ausgeführt werden** **IStream** -Objekt initialisiert.</span><span class="sxs-lookup"><span data-stu-id="f3eab-141">[in] The prefix for the filename on which **OpenStreamOnFile** initializes the **IStream** object.</span></span> <span data-ttu-id="f3eab-142">Wenn festgelegt, das Präfix nicht mehr als drei Zeichen enthalten muss.</span><span class="sxs-lookup"><span data-stu-id="f3eab-142">If set, the prefix must contain not more than three characters.</span></span> <span data-ttu-id="f3eab-143">Wenn _LpszPrefix_ NULL ist, wird das Präfix "SOF" verwendet.</span><span class="sxs-lookup"><span data-stu-id="f3eab-143">If  _lpszPrefix_ is NULL, a prefix of "SOF" is used.</span></span> 
    
 <span data-ttu-id="f3eab-144">_lppStream_</span><span class="sxs-lookup"><span data-stu-id="f3eab-144">_lppStream_</span></span>
  
> <span data-ttu-id="f3eab-145">[out] Zeiger auf einen Zeiger auf ein Objekt, das die **IStream** -Schnittstelle verfügbar macht.</span><span class="sxs-lookup"><span data-stu-id="f3eab-145">[out] Pointer to a pointer to an object exposing the **IStream** interface.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="f3eab-146">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="f3eab-146">Return value</span></span>

<span data-ttu-id="f3eab-147">S_OK</span><span class="sxs-lookup"><span data-stu-id="f3eab-147">S_OK</span></span> 
  
> <span data-ttu-id="f3eab-148">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="f3eab-148">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="f3eab-149">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="f3eab-149">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="f3eab-150">Die Datei konnte nicht zugegriffen werden, aufgrund der nicht über ausreichende Benutzerberechtigungen oder da schreibgeschützte Dateien nicht geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="f3eab-150">The file could not be accessed due to insufficient user permissions or because read-only files cannot be modified.</span></span> 
    
<span data-ttu-id="f3eab-151">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="f3eab-151">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="f3eab-152">Die angegebene Datei ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="f3eab-152">The designated file does not exist.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f3eab-153">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="f3eab-153">Remarks</span></span>

<span data-ttu-id="f3eab-154">Die **OpenStreamOnFile nicht ausgeführt werden** -Funktion weist zwei wichtige verwendet, durch die Einstellung des Flags SOF_UNIQUEFILENAME unterschieden.</span><span class="sxs-lookup"><span data-stu-id="f3eab-154">The **OpenStreamOnFile** function has two important uses, distinguished by the setting of the SOF_UNIQUEFILENAME flag.</span></span> <span data-ttu-id="f3eab-155">Wenn dieses Flag nicht festgelegt ist, wird **OpenStreamOnFile nicht ausgeführt werden** **IStream** -Objekts auf eine vorhandene Datei, um den Inhalt der **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md))-Eigenschaft einer Anlage, die mit der **IStream kopieren beispielsweise geöffnet. :: CopyTo** Methode.</span><span class="sxs-lookup"><span data-stu-id="f3eab-155">When this flag is not set, **OpenStreamOnFile** opens an **IStream** object on an existing file, for example to copy its contents to the **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) property of an attachment using the **IStream::CopyTo** method.</span></span> <span data-ttu-id="f3eab-156">In diesem Fall gibt der Parameter _LpszFileName_ den Pfad und Dateinamen der Datei an.</span><span class="sxs-lookup"><span data-stu-id="f3eab-156">In this case the  _lpszFileName_ parameter specifies the path and filename of the file.</span></span> 
  
<span data-ttu-id="f3eab-157">Wenn SOF_UNIQUEFILENAME festgelegt ist, wird **OpenStreamOnFile nicht ausgeführt werden** eine temporäre Datei zum Speichern von Daten für ein **IStream** -Objekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="f3eab-157">When SOF_UNIQUEFILENAME is set, **OpenStreamOnFile** creates a temporary file to hold data for an **IStream** object.</span></span> <span data-ttu-id="f3eab-158">Für diese Verwendung kann der Parameter _LpszFileName_ optional bestimmen den Pfad zu dem Verzeichnis, in dem die Datei erstellt werden soll, und der Parameter _LpszPrefix_ kann optional ein Präfix für den Dateinamen angeben.</span><span class="sxs-lookup"><span data-stu-id="f3eab-158">For this usage, the  _lpszFileName_ parameter can optionally designate the path to the directory where the file is to be created, and the  _lpszPrefix_ parameter can optionally specify a prefix for the filename.</span></span> 
  
<span data-ttu-id="f3eab-159">Wenn mit dem **IStream** -Objekt den aufrufenden Clientanwendung oder den Dienstanbieter abgeschlossen ist, sollten sie es durch Aufrufen der Methode OLE **Streamkomponente IStream::** frei.</span><span class="sxs-lookup"><span data-stu-id="f3eab-159">When the calling client application or service provider is finished with the **IStream** object, it should free it by calling the OLE **IStream::Release** method.</span></span> 
  
<span data-ttu-id="f3eab-160">MAPI verwendet die Funktionen, auf die _LpAllocateBuffer_ und _LpFreeBuffer_ für die meisten Zuweisung von virtuellem Speicher und zur Freigabe, insbesondere, um für die Verwendung von Clientanwendungen Speicher beim Aufruf von Schnittstellen für Objekte wie [IMAPIProp:: GetProps](imapiprop-getprops.md) und [IMAPITable::QueryRows](imapitable-queryrows.md).</span><span class="sxs-lookup"><span data-stu-id="f3eab-160">MAPI uses the functions pointed to by  _lpAllocateBuffer_ and  _lpFreeBuffer_ for most memory allocation and deallocation, in particular to allocate memory for use by client applications when calling object interfaces such as [IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="f3eab-161">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="f3eab-161">Notes to callers</span></span>

<span data-ttu-id="f3eab-162">Das Flag SOF_UNIQUEFILENAME wird verwendet, um eine temporäre Datei durch einen Namen für die messaging-System eindeutig zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="f3eab-162">The SOF_UNIQUEFILENAME flag is used to create a temporary file with a name unique to the messaging system.</span></span> <span data-ttu-id="f3eab-163">Wenn dieses Flag festgelegt ist, enthält die _LpszFileName_ -Parameter gibt den Pfad für die temporäre Datei und der _LpszPrefix_ -Parameter die Anfangszeichen des Dateinamens.</span><span class="sxs-lookup"><span data-stu-id="f3eab-163">If this flag is set, the  _lpszFileName_ parameter specifes the path for the temporary file, and the  _lpszPrefix_ parameter contains the prefix characters of the filename.</span></span> <span data-ttu-id="f3eab-164">Der erstellte Dateiname ist <prefix>HHHH. TMP, wobei HHHH eine hexadezimale Zahl ist.</span><span class="sxs-lookup"><span data-stu-id="f3eab-164">The constructed filename is <prefix>HHHH.TMP, where HHHH is a hexadecimal number.</span></span> <span data-ttu-id="f3eab-165">Wenn _LpszFileName_ NULL ist, wird die Datei im Verzeichnis temporäre Datei, das von der Windows-Funktion **GetTempPath**zurückgegeben wird, oder das aktuelle Verzeichnis erstellt, wenn kein Verzeichnis temporäre Datei vorgesehen ist.</span><span class="sxs-lookup"><span data-stu-id="f3eab-165">If  _lpszFileName_ is NULL, the file will be created in the temporary file directory that is returned from the Windows function **GetTempPath**, or the current directory if no temporary file directory has been designated.</span></span> 
  
<span data-ttu-id="f3eab-166">Wenn das Flag SOF_UNIQUEFILENAME nicht festgelegt ist, _LpszPrefix_ wird ignoriert, und der vollständig qualifizierte Pfad und Dateiname der Datei geöffnet oder erstellt werden, sollte _LpszFileName_ enthalten.</span><span class="sxs-lookup"><span data-stu-id="f3eab-166">If the SOF_UNIQUEFILENAME flag is not set,  _lpszPrefix_ is ignored, and  _lpszFileName_ should contain the fully qualified path and filename of the file to be opened or created.</span></span> <span data-ttu-id="f3eab-167">Die Datei wird geöffnet oder erstellt basierend auf den anderen Flags, die in _UlFlags_festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="f3eab-167">The file will be opened or created based on the other flags that are set in  _ulFlags_.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="f3eab-168">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="f3eab-168">MFCMAPI reference</span></span>

<span data-ttu-id="f3eab-169">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="f3eab-169">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="f3eab-170">**Datei**</span><span class="sxs-lookup"><span data-stu-id="f3eab-170">**File**</span></span>|<span data-ttu-id="f3eab-171">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="f3eab-171">**Function**</span></span>|<span data-ttu-id="f3eab-172">**Comment**</span><span class="sxs-lookup"><span data-stu-id="f3eab-172">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f3eab-173">File.cpp</span><span class="sxs-lookup"><span data-stu-id="f3eab-173">File.cpp</span></span>  <br/> |<span data-ttu-id="f3eab-174">WriteAttachStreamToFile</span><span class="sxs-lookup"><span data-stu-id="f3eab-174">WriteAttachStreamToFile</span></span>  <br/> |<span data-ttu-id="f3eab-175">MFCMAPI (engl.) verwendet die Methode **OpenStreamOnFile nicht ausgeführt werden** , um einen Datenstrom für eine Datei zu öffnen, damit eine Anlage darauf geschrieben werden kann.</span><span class="sxs-lookup"><span data-stu-id="f3eab-175">MFCMAPI uses the **OpenStreamOnFile** method to open a stream on a file so an attachment can be written out to it.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f3eab-176">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f3eab-176">See also</span></span>



[<span data-ttu-id="f3eab-177">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="f3eab-177">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

