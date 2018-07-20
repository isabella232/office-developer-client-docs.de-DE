---
title: OpenStreamOnFileW
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- OpenStreamOnFileW
api_type:
- COM
ms.assetid: 263b9f24-eac8-4d34-8f66-dc87024b94b9
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 127c4a77b9184d8bb62925c5237c1aedec643992
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793322"
---
# <a name="openstreamonfilew"></a><span data-ttu-id="e9d83-103">OpenStreamOnFileW</span><span class="sxs-lookup"><span data-stu-id="e9d83-103">OpenStreamOnFileW</span></span>

  
  
<span data-ttu-id="e9d83-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e9d83-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e9d83-105">Reserviert und initialisiert ein OLE- **IStream** -Objekt Zugriff auf den Inhalt einer Datei.</span><span class="sxs-lookup"><span data-stu-id="e9d83-105">Allocates and initializes an OLE **IStream** object to access the contents of a file.</span></span> <span data-ttu-id="e9d83-106">Diese Funktion akzeptiert Unicode-Zeichenfolgen als Argumente, im Gegensatz zu ANSI-Version dieser Funktion [OpenStreamOnFile nicht ausgeführt werden](openstreamonfile.md), und daher kann für beliebige Zeichen in den Dateinamen einschließlich der Erweiterungs Pfad und den Dateinamen.</span><span class="sxs-lookup"><span data-stu-id="e9d83-106">This function takes UNICODE strings as arguments, unlike the ANSI version of this function [OpenStreamOnFile](openstreamonfile.md), and thus allows for arbitrary characters in the file name including the path and file extension.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e9d83-107">Vom exportiert werden:</span><span class="sxs-lookup"><span data-stu-id="e9d83-107">Exported by:</span></span>  <br/> |<span data-ttu-id="e9d83-108">olmapi32.dll</span><span class="sxs-lookup"><span data-stu-id="e9d83-108">olmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="e9d83-109">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="e9d83-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="e9d83-110">Outlook</span><span class="sxs-lookup"><span data-stu-id="e9d83-110">Outlook</span></span>  <br/> |
|<span data-ttu-id="e9d83-111">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="e9d83-111">Called by:</span></span>  <br/> |<span data-ttu-id="e9d83-112">Clientanwendungen und -Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="e9d83-112">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT STDMETHODCALLTYPE OpenStreamOnFileW(
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPFREEBUFFER lpFreeBuffer,
  ULONG ulFlags,
  LPWSTR lpszFileName,
  LPWSTR lpszPrefix,
  LPSTREAM FAR * lppStream
);
```

## <a name="parameters"></a><span data-ttu-id="e9d83-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="e9d83-113">Parameters</span></span>

 <span data-ttu-id="e9d83-114">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="e9d83-114">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="e9d83-115">[in] Zeiger auf die Funktion [MAPIAllocateBuffer](mapiallocatebuffer.md) , Speicher verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="e9d83-115">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
 <span data-ttu-id="e9d83-116">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="e9d83-116">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="e9d83-117">[in] Zeiger auf die [MAPIFreeBuffer](mapifreebuffer.md) -Funktion verwendet werden, um Arbeitsspeicher freizugeben.</span><span class="sxs-lookup"><span data-stu-id="e9d83-117">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
 <span data-ttu-id="e9d83-118">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e9d83-118">_ulFlags_</span></span>
  
> <span data-ttu-id="e9d83-119">[in] Bitmaske der Flags verwendet, um das Erstellen oder Öffnen der Datei steuern über das OLE- **IStream** -Objekt zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="e9d83-119">[in] Bitmask of flags used to control the creation or opening of the file to be accessed through the OLE **IStream** object.</span></span> <span data-ttu-id="e9d83-120">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="e9d83-120">The following flags can be set:</span></span> 
    
<span data-ttu-id="e9d83-121">SOF_UNIQUEFILENAME</span><span class="sxs-lookup"><span data-stu-id="e9d83-121">SOF_UNIQUEFILENAME</span></span>
  
> <span data-ttu-id="e9d83-122">Eine temporäre Datei ist für das **IStream** -Objekt erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="e9d83-122">A temporary file is to be created for the **IStream** object.</span></span> <span data-ttu-id="e9d83-123">Wenn dieses Flag festgelegt ist, sollte die Flags STGM_CREATE und Accessor auch festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="e9d83-123">If this flag is set, the STGM_CREATE and STGM_READWRITE flags should also be set.</span></span> 
    
<span data-ttu-id="e9d83-124">STGM_CREATE</span><span class="sxs-lookup"><span data-stu-id="e9d83-124">STGM_CREATE</span></span>
  
> <span data-ttu-id="e9d83-125">Die Datei ist erstellt werden soll, auch wenn Sie bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="e9d83-125">The file is to be created even if one already exists.</span></span> <span data-ttu-id="e9d83-126">Wenn der Parameter _LpszFileName_ nicht festgelegt ist, muss dieses Flag und die STGM_DELETEONRELEASE festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="e9d83-126">If the  _lpszFileName_ parameter is not set, both this flag and STGM_DELETEONRELEASE must be set.</span></span> <span data-ttu-id="e9d83-127">Wenn STGM_CREATE festgelegt ist, muss auch die Accessor-Flag festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="e9d83-127">If STGM_CREATE is set, the STGM_READWRITE flag must also be set.</span></span> 
    
<span data-ttu-id="e9d83-128">STGM_DELETEONRELEASE</span><span class="sxs-lookup"><span data-stu-id="e9d83-128">STGM_DELETEONRELEASE</span></span>
  
> <span data-ttu-id="e9d83-129">Die Datei wird gelöscht, wenn das Objekt **IStream** freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="e9d83-129">The file is to be deleted when the **IStream** object is released.</span></span> <span data-ttu-id="e9d83-130">Wenn der Parameter _LpszFileName_ nicht festgelegt ist, muss dieses Flag und die STGM_CREATE festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="e9d83-130">If the  _lpszFileName_ parameter is not set, both this flag and STGM_CREATE must be set.</span></span> 
    
<span data-ttu-id="e9d83-131">BEISPIELCODEZEILEN</span><span class="sxs-lookup"><span data-stu-id="e9d83-131">STGM_READ</span></span>
  
> <span data-ttu-id="e9d83-132">Die Datei wird mit schreibgeschützten Zugriff geöffnet oder erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="e9d83-132">The file is to be created or opened with read-only access.</span></span>
    
<span data-ttu-id="e9d83-133">ACCESSOR</span><span class="sxs-lookup"><span data-stu-id="e9d83-133">STGM_READWRITE</span></span>
  
> <span data-ttu-id="e9d83-134">Die Datei wird erstellt oder mit Lese-/Schreibzugriff geöffnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="e9d83-134">The file is to be created or opened with read/write permission.</span></span> <span data-ttu-id="e9d83-135">Wenn dieses Flag nicht festgelegt ist, muss das Flag STGM_CREATE nicht festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="e9d83-135">If this flag is not set, the STGM_CREATE flag must not be set either.</span></span>
    
 <span data-ttu-id="e9d83-136">_lpszFileName_</span><span class="sxs-lookup"><span data-stu-id="e9d83-136">_lpszFileName_</span></span>
  
> <span data-ttu-id="e9d83-137">[in] Der Dateiname mit dem Namen einschließlich Pfad und Erweiterung des Unicode-Datei für die **OpenStreamOnFileW** **IStream** -Objekt initialisiert.</span><span class="sxs-lookup"><span data-stu-id="e9d83-137">[in] The filename, including path and extension, of the Unicode named file for which **OpenStreamOnFileW** initializes the **IStream** object.</span></span> <span data-ttu-id="e9d83-138">Wenn das Flag SOF_UNIQUEFILENAME festgelegt ist, enthält _LpszFileName_ den Pfad zu dem Verzeichnis, in dem Sie eine temporäre Datei zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="e9d83-138">If the SOF_UNIQUEFILENAME flag is set,  _lpszFileName_ contains the path to the directory in which to create a temporary file.</span></span> <span data-ttu-id="e9d83-139">Wenn _LpszFileName_ NULL ist, **OpenStreamOnFileW** ruft geeigneten Pfad aus dem System und die STGM_CREATE und die STGM_DELETEONRELEASE Flags müssen festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="e9d83-139">If  _lpszFileName_ is NULL, **OpenStreamOnFileW** obtains an appropriate path from the system, and both the STGM_CREATE and STGM_DELETEONRELEASE flags must be set.</span></span> 
    
 <span data-ttu-id="e9d83-140">_lpszPrefix_</span><span class="sxs-lookup"><span data-stu-id="e9d83-140">_lpszPrefix_</span></span>
  
> <span data-ttu-id="e9d83-141">[in] Das Präfix für den Unicode-Dateinamen auf dem **OpenStreamOnFileW** **IStream** -Objekt initialisiert.</span><span class="sxs-lookup"><span data-stu-id="e9d83-141">[in] The prefix for the Unicode filename on which **OpenStreamOnFileW** initializes the **IStream** object.</span></span> <span data-ttu-id="e9d83-142">Wenn festgelegt, das Präfix nicht mehr als drei Zeichen enthalten muss.</span><span class="sxs-lookup"><span data-stu-id="e9d83-142">If set, the prefix must contain not more than three characters.</span></span> <span data-ttu-id="e9d83-143">Wenn _LpszPrefix_ NULL ist, wird das Präfix "SOF" verwendet.</span><span class="sxs-lookup"><span data-stu-id="e9d83-143">If  _lpszPrefix_ is NULL, a prefix of "SOF" is used.</span></span> 
    
 <span data-ttu-id="e9d83-144">_lppStream_</span><span class="sxs-lookup"><span data-stu-id="e9d83-144">_lppStream_</span></span>
  
> <span data-ttu-id="e9d83-145">[out] Zeiger auf einen Zeiger auf ein Objekt, das die **IStream** -Schnittstelle verfügbar macht.</span><span class="sxs-lookup"><span data-stu-id="e9d83-145">[out] Pointer to a pointer to an object exposing the **IStream** interface.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="e9d83-146">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e9d83-146">Return value</span></span>

<span data-ttu-id="e9d83-147">S_OK</span><span class="sxs-lookup"><span data-stu-id="e9d83-147">S_OK</span></span>
  
> <span data-ttu-id="e9d83-148">Der Aufruf erfolgreich ausgeführt und der erwartete Wert oder Werte zurückgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="e9d83-148">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="e9d83-149">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="e9d83-149">MAPI_E_NO_ACCESS</span></span>
  
> <span data-ttu-id="e9d83-150">Die Datei konnte nicht zugegriffen werden, aufgrund der nicht über ausreichende Benutzerberechtigungen oder da schreibgeschützte Dateien nicht geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="e9d83-150">The file could not be accessed due to insufficient user permissions or because read-only files cannot be modified.</span></span>
    
<span data-ttu-id="e9d83-151">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="e9d83-151">MAPI_E_NOT_FOUND</span></span>
  
> <span data-ttu-id="e9d83-152">Die angegebene Datei ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="e9d83-152">The designated file does not exist.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e9d83-153">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e9d83-153">Remarks</span></span>

<span data-ttu-id="e9d83-154">Die **OpenStreamOnFileW** -Funktion besitzt zwei wichtige Verwendungen neben der Behandlung von einer Datei mit einem Unicode-Namen, durch die Einstellung des Flags SOF_UNIQUEFILENAME unterschieden.</span><span class="sxs-lookup"><span data-stu-id="e9d83-154">The **OpenStreamOnFileW** function has two important uses in addition to handling a file with a Unicode name, distinguished by the setting of the SOF_UNIQUEFILENAME flag.</span></span> <span data-ttu-id="e9d83-155">Wenn dieses Flag nicht festgelegt ist, wird **OpenStreamOnFileW** **IStream** -Objekts auf eine vorhandene Datei, zum Beispiel zum Kopieren von seinen Inhalt der **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md))-Eigenschaft einer Anlage, die mit der **geöffnet. :: CopyTo** Methode.</span><span class="sxs-lookup"><span data-stu-id="e9d83-155">When this flag is not set, **OpenStreamOnFileW** opens an **IStream** object on an existing file, for example to copy its contents to the **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) property of an attachment using the **IStream::CopyTo** method.</span></span> <span data-ttu-id="e9d83-156">In diesem Fall gibt der Parameter _LpszFileName_ den Pfad und Dateinamen der Datei an.</span><span class="sxs-lookup"><span data-stu-id="e9d83-156">In this case the  _lpszFileName_ parameter specifies the path and filename of the file.</span></span> 
  
<span data-ttu-id="e9d83-157">Wenn SOF_UNIQUEFILENAME festgelegt ist, erstellt **OpenStreamOnFileW** eine temporäre Datei zum Speichern von Daten für **IStream** -Objekts.</span><span class="sxs-lookup"><span data-stu-id="e9d83-157">When SOF_UNIQUEFILENAME is set, **OpenStreamOnFileW** creates a temporary file to hold data for an **IStream** object.</span></span> <span data-ttu-id="e9d83-158">Für diese Verwendung kann der Parameter _LpszFileName_ optional bestimmen den Pfad zu dem Verzeichnis, in dem die Datei erstellt werden soll, und der Parameter _LpszPrefix_ kann optional ein Präfix für den Dateinamen angeben.</span><span class="sxs-lookup"><span data-stu-id="e9d83-158">For this usage, the  _lpszFileName_ parameter can optionally designate the path to the directory where the file is to be created, and the  _lpszPrefix_ parameter can optionally specify a prefix for the filename.</span></span> 
  
<span data-ttu-id="e9d83-159">Wenn mit dem **IStream** -Objekt den aufrufenden Clientanwendung oder den Dienstanbieter abgeschlossen ist, sollten sie es durch Aufrufen der Methode OLE **Streamkomponente IStream::** frei.</span><span class="sxs-lookup"><span data-stu-id="e9d83-159">When the calling client application or service provider is finished with the **IStream** object, it should free it by calling the OLE **IStream::Release** method.</span></span> 
  
<span data-ttu-id="e9d83-160">MAPI verwendet die Funktionen, auf die _LpAllocateBuffer_ und _LpFreeBuffer_ für die meisten Zuweisung von virtuellem Speicher und zur Freigabe, insbesondere, um für die Verwendung von Clientanwendungen Speicher beim Aufruf von Schnittstellen für Objekte wie [IMAPIProp:: GetProps](imapiprop-getprops.md) und [IMAPITable::QueryRows](imapitable-queryrows.md).</span><span class="sxs-lookup"><span data-stu-id="e9d83-160">MAPI uses the functions pointed to by  _lpAllocateBuffer_ and  _lpFreeBuffer_ for most memory allocation and deallocation, in particular to allocate memory for use by client applications when calling object interfaces such as [IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="e9d83-161">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="e9d83-161">Notes to callers</span></span>

<span data-ttu-id="e9d83-162">Das Flag SOF_UNIQUEFILENAME wird verwendet, um eine temporäre Datei durch einen Namen für die messaging-System eindeutig zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="e9d83-162">The SOF_UNIQUEFILENAME flag is used to create a temporary file with a name unique to the messaging system.</span></span> <span data-ttu-id="e9d83-163">Wenn dieses Flag festgelegt ist, enthält die _LpszFileName_ -Parameter gibt den Pfad für die temporäre Datei und der _LpszPrefix_ -Parameter die Anfangszeichen des Dateinamens.</span><span class="sxs-lookup"><span data-stu-id="e9d83-163">If this flag is set, the  _lpszFileName_ parameter specifes the path for the temporary file, and the  _lpszPrefix_ parameter contains the prefix characters of the filename.</span></span> <span data-ttu-id="e9d83-164">Der erstellte Dateiname ist <prefix>HHHH. TMP, wobei HHHH eine hexadezimale Zahl ist.</span><span class="sxs-lookup"><span data-stu-id="e9d83-164">The constructed filename is <prefix>HHHH.TMP, where HHHH is a hexadecimal number.</span></span> <span data-ttu-id="e9d83-165">Wenn _LpszFileName_ NULL ist, wird die Datei im Verzeichnis temporäre Datei, das von der Windows-Funktion **GetTempPath**zurückgegeben wird, oder das aktuelle Verzeichnis erstellt, wenn kein Verzeichnis temporäre Datei vorgesehen ist.</span><span class="sxs-lookup"><span data-stu-id="e9d83-165">If  _lpszFileName_ is NULL, the file will be created in the temporary file directory that is returned from the Windows function **GetTempPath**, or the current directory if no temporary file directory has been designated.</span></span>
  
<span data-ttu-id="e9d83-166">Wenn das Flag SOF_UNIQUEFILENAME nicht festgelegt ist, _LpszPrefix_ wird ignoriert, und der vollständig qualifizierte Pfad und Dateiname der Datei geöffnet oder erstellt werden, sollte _LpszFileName_ enthalten.</span><span class="sxs-lookup"><span data-stu-id="e9d83-166">If the SOF_UNIQUEFILENAME flag is not set,  _lpszPrefix_ is ignored, and  _lpszFileName_ should contain the fully qualified path and filename of the file to be opened or created.</span></span> <span data-ttu-id="e9d83-167">Die Datei wird geöffnet oder erstellt basierend auf den anderen Flags, die in _UlFlags_festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="e9d83-167">The file will be opened or created based on the other flags that are set in  _ulFlags_.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e9d83-168">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e9d83-168">See also</span></span>



[<span data-ttu-id="e9d83-169">OpenStreamOnFile</span><span class="sxs-lookup"><span data-stu-id="e9d83-169">OpenStreamOnFile</span></span>](openstreamonfile.md)

