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
ms.openlocfilehash: 7e67d84320b57fe6e510b70a68088f289ef6030d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406024"
---
# <a name="openstreamonfilew"></a><span data-ttu-id="77256-103">OpenStreamOnFileW</span><span class="sxs-lookup"><span data-stu-id="77256-103">OpenStreamOnFileW</span></span>

  
  
<span data-ttu-id="77256-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="77256-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="77256-105">Weist ein OLE **IStream-Objekt** zu und initialisiert es, um auf den Inhalt einer Datei zu zugreifen.</span><span class="sxs-lookup"><span data-stu-id="77256-105">Allocates and initializes an OLE **IStream** object to access the contents of a file.</span></span> <span data-ttu-id="77256-106">Diese Funktion verwendet UNICODE-Zeichenfolgen als Argumente, im Gegensatz zur ANSI-Version dieser Funktion [OpenStreamOnFile](openstreamonfile.md), und ermöglicht somit beliebige Zeichen im Dateinamen, einschließlich des Pfads und der Dateierweiterung.</span><span class="sxs-lookup"><span data-stu-id="77256-106">This function takes UNICODE strings as arguments, unlike the ANSI version of this function [OpenStreamOnFile](openstreamonfile.md), and thus allows for arbitrary characters in the file name including the path and file extension.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="77256-107">Exportiert von:</span><span class="sxs-lookup"><span data-stu-id="77256-107">Exported by:</span></span>  <br/> |<span data-ttu-id="77256-108">olmapi32.dll</span><span class="sxs-lookup"><span data-stu-id="77256-108">olmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="77256-109">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="77256-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="77256-110">Outlook</span><span class="sxs-lookup"><span data-stu-id="77256-110">Outlook</span></span>  <br/> |
|<span data-ttu-id="77256-111">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="77256-111">Called by:</span></span>  <br/> |<span data-ttu-id="77256-112">Clientanwendungen und Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="77256-112">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="77256-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="77256-113">Parameters</span></span>

 <span data-ttu-id="77256-114">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="77256-114">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="77256-115">[in] Zeiger auf die [MAPIAllocateBuffer-Funktion,](mapiallocatebuffer.md) die zum Zuordnen von Arbeitsspeicher verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="77256-115">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
 <span data-ttu-id="77256-116">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="77256-116">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="77256-117">[in] Zeiger auf die [MAPIFreeBuffer-Funktion,](mapifreebuffer.md) die zum Freispeichern verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="77256-117">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
 <span data-ttu-id="77256-118">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="77256-118">_ulFlags_</span></span>
  
> <span data-ttu-id="77256-119">[in] Bitmaske von Flags, die zum Steuern des Erstellens oder Öffnens der Datei verwendet werden, auf die über das OLE **IStream-Objekt zugegriffen werden** soll.</span><span class="sxs-lookup"><span data-stu-id="77256-119">[in] Bitmask of flags used to control the creation or opening of the file to be accessed through the OLE **IStream** object.</span></span> <span data-ttu-id="77256-120">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="77256-120">The following flags can be set:</span></span> 
    
<span data-ttu-id="77256-121">SOF_UNIQUEFILENAME</span><span class="sxs-lookup"><span data-stu-id="77256-121">SOF_UNIQUEFILENAME</span></span>
  
> <span data-ttu-id="77256-122">Für das **IStream-Objekt** soll eine temporäre Datei erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="77256-122">A temporary file is to be created for the **IStream** object.</span></span> <span data-ttu-id="77256-123">Wenn dieses Flag festgelegt ist, sollten auch die STGM_CREATE und STGM_READWRITE festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="77256-123">If this flag is set, the STGM_CREATE and STGM_READWRITE flags should also be set.</span></span> 
    
<span data-ttu-id="77256-124">STGM_CREATE</span><span class="sxs-lookup"><span data-stu-id="77256-124">STGM_CREATE</span></span>
  
> <span data-ttu-id="77256-125">Die Datei soll auch dann erstellt werden, wenn bereits eine vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="77256-125">The file is to be created even if one already exists.</span></span> <span data-ttu-id="77256-126">Wenn der  _lpszFileName-Parameter_ nicht festgelegt ist, müssen sowohl dieses Flag als auch STGM_DELETEONRELEASE festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="77256-126">If the  _lpszFileName_ parameter is not set, both this flag and STGM_DELETEONRELEASE must be set.</span></span> <span data-ttu-id="77256-127">Wenn STGM_CREATE festgelegt ist, muss auch das STGM_READWRITE festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="77256-127">If STGM_CREATE is set, the STGM_READWRITE flag must also be set.</span></span> 
    
<span data-ttu-id="77256-128">STGM_DELETEONRELEASE</span><span class="sxs-lookup"><span data-stu-id="77256-128">STGM_DELETEONRELEASE</span></span>
  
> <span data-ttu-id="77256-129">Die Datei soll gelöscht werden, wenn das **IStream-Objekt** freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="77256-129">The file is to be deleted when the **IStream** object is released.</span></span> <span data-ttu-id="77256-130">Wenn der  _lpszFileName-Parameter_ nicht festgelegt ist, müssen sowohl dieses Flag als auch STGM_CREATE festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="77256-130">If the  _lpszFileName_ parameter is not set, both this flag and STGM_CREATE must be set.</span></span> 
    
<span data-ttu-id="77256-131">STGM_READ</span><span class="sxs-lookup"><span data-stu-id="77256-131">STGM_READ</span></span>
  
> <span data-ttu-id="77256-132">Die Datei soll mit schreibgeschützten Zugriff erstellt oder geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="77256-132">The file is to be created or opened with read-only access.</span></span>
    
<span data-ttu-id="77256-133">STGM_READWRITE</span><span class="sxs-lookup"><span data-stu-id="77256-133">STGM_READWRITE</span></span>
  
> <span data-ttu-id="77256-134">Die Datei soll mit Lese-/Schreibberechtigung erstellt oder geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="77256-134">The file is to be created or opened with read/write permission.</span></span> <span data-ttu-id="77256-135">Wenn dieses Flag nicht festgelegt ist, darf STGM_CREATE auch nicht festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="77256-135">If this flag is not set, the STGM_CREATE flag must not be set either.</span></span>
    
 <span data-ttu-id="77256-136">_lpszFileName_</span><span class="sxs-lookup"><span data-stu-id="77256-136">_lpszFileName_</span></span>
  
> <span data-ttu-id="77256-137">[in] Der Dateiname, einschließlich Pfad und Erweiterung, der benannten Unicode-Datei, für die **OpenStreamOnFileW** das **IStream-Objekt initialisiert.**</span><span class="sxs-lookup"><span data-stu-id="77256-137">[in] The filename, including path and extension, of the Unicode named file for which **OpenStreamOnFileW** initializes the **IStream** object.</span></span> <span data-ttu-id="77256-138">Wenn das SOF_UNIQUEFILENAME festgelegt ist, enthält  _lpszFileName_ den Pfad zum Verzeichnis, in dem eine temporäre Datei erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="77256-138">If the SOF_UNIQUEFILENAME flag is set,  _lpszFileName_ contains the path to the directory in which to create a temporary file.</span></span> <span data-ttu-id="77256-139">Wenn  _lpszFileName_ null ist, **ruft OpenStreamOnFileW** einen entsprechenden Pfad vom System ab, und sowohl die STGM_CREATE als auch STGM_DELETEONRELEASE müssen festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="77256-139">If  _lpszFileName_ is NULL, **OpenStreamOnFileW** obtains an appropriate path from the system, and both the STGM_CREATE and STGM_DELETEONRELEASE flags must be set.</span></span> 
    
 <span data-ttu-id="77256-140">_lpszPrefix_</span><span class="sxs-lookup"><span data-stu-id="77256-140">_lpszPrefix_</span></span>
  
> <span data-ttu-id="77256-141">[in] Das Präfix für den Unicode-Dateinamen, für den **OpenStreamOnFileW** das **IStream-Objekt initialisiert.**</span><span class="sxs-lookup"><span data-stu-id="77256-141">[in] The prefix for the Unicode filename on which **OpenStreamOnFileW** initializes the **IStream** object.</span></span> <span data-ttu-id="77256-142">Wenn festgelegt, darf das Präfix nicht mehr als drei Zeichen enthalten.</span><span class="sxs-lookup"><span data-stu-id="77256-142">If set, the prefix must contain not more than three characters.</span></span> <span data-ttu-id="77256-143">Wenn  _lpszPrefix_ NULL ist, wird das Präfix "SOF" verwendet.</span><span class="sxs-lookup"><span data-stu-id="77256-143">If  _lpszPrefix_ is NULL, a prefix of "SOF" is used.</span></span> 
    
 <span data-ttu-id="77256-144">_lppStream_</span><span class="sxs-lookup"><span data-stu-id="77256-144">_lppStream_</span></span>
  
> <span data-ttu-id="77256-145">[out] Zeiger auf einen Zeiger auf ein Objekt, das die **IStream-Schnittstelle verfügbar** machen soll.</span><span class="sxs-lookup"><span data-stu-id="77256-145">[out] Pointer to a pointer to an object exposing the **IStream** interface.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="77256-146">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="77256-146">Return value</span></span>

<span data-ttu-id="77256-147">S_OK</span><span class="sxs-lookup"><span data-stu-id="77256-147">S_OK</span></span>
  
> <span data-ttu-id="77256-148">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="77256-148">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="77256-149">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="77256-149">MAPI_E_NO_ACCESS</span></span>
  
> <span data-ttu-id="77256-150">Der Zugriff auf die Datei konnte aufgrund unzureichender Benutzerberechtigungen oder aufgrund von schreibgeschützten Dateien nicht möglich sein.</span><span class="sxs-lookup"><span data-stu-id="77256-150">The file could not be accessed due to insufficient user permissions or because read-only files cannot be modified.</span></span>
    
<span data-ttu-id="77256-151">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="77256-151">MAPI_E_NOT_FOUND</span></span>
  
> <span data-ttu-id="77256-152">Die festgelegte Datei ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="77256-152">The designated file does not exist.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="77256-153">Hinweise</span><span class="sxs-lookup"><span data-stu-id="77256-153">Remarks</span></span>

<span data-ttu-id="77256-154">Die **OpenStreamOnFileW-Funktion** hat neben der Verarbeitung einer Datei mit einem Unicode-Namen zwei wichtige Verwendungsmöglichkeiten, die sich durch die Einstellung des SOF_UNIQUEFILENAME unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="77256-154">The **OpenStreamOnFileW** function has two important uses in addition to handling a file with a Unicode name, distinguished by the setting of the SOF_UNIQUEFILENAME flag.</span></span> <span data-ttu-id="77256-155">Wenn dieses Flag nicht festgelegt ist, öffnet **OpenStreamOnFileW** ein **IStream-Objekt** in einer vorhandenen Datei, z. B. um den Inhalt in die **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md))-Eigenschaft einer Anlage mithilfe der **IStream::CopyTo-Methode** zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="77256-155">When this flag is not set, **OpenStreamOnFileW** opens an **IStream** object on an existing file, for example to copy its contents to the **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) property of an attachment using the **IStream::CopyTo** method.</span></span> <span data-ttu-id="77256-156">In diesem Fall gibt  _der lpszFileName-Parameter_ den Pfad und Dateinamen der Datei an.</span><span class="sxs-lookup"><span data-stu-id="77256-156">In this case the  _lpszFileName_ parameter specifies the path and filename of the file.</span></span> 
  
<span data-ttu-id="77256-157">Wenn SOF_UNIQUEFILENAME festgelegt ist, **erstellt OpenStreamOnFileW** eine temporäre Datei zum Speichern von Daten für ein **IStream-Objekt.**</span><span class="sxs-lookup"><span data-stu-id="77256-157">When SOF_UNIQUEFILENAME is set, **OpenStreamOnFileW** creates a temporary file to hold data for an **IStream** object.</span></span> <span data-ttu-id="77256-158">Für diese Verwendung kann der  _lpszFileName-Parameter_ optional den Pfad zum Verzeichnis festlegen, in dem die Datei erstellt werden soll, und der  _lpszPrefix-Parameter_ kann optional ein Präfix für den Dateinamen angeben.</span><span class="sxs-lookup"><span data-stu-id="77256-158">For this usage, the  _lpszFileName_ parameter can optionally designate the path to the directory where the file is to be created, and the  _lpszPrefix_ parameter can optionally specify a prefix for the filename.</span></span> 
  
<span data-ttu-id="77256-159">Wenn die aufrufende Clientanwendung oder der aufrufende Dienstanbieter mit dem **IStream-Objekt** fertig ist, sollte es durch Aufrufen der OLE **IStream::Release-Methode freigegeben** werden.</span><span class="sxs-lookup"><span data-stu-id="77256-159">When the calling client application or service provider is finished with the **IStream** object, it should free it by calling the OLE **IStream::Release** method.</span></span> 
  
<span data-ttu-id="77256-160">MAPI verwendet die Funktionen, auf die  _von lpAllocateBuffer_ und  _lpFreeBuffer_ verwiesen wird, für die meisten Speicherzuweisungen und Deallocation, insbesondere zum Zuordnen von Arbeitsspeicher zur Verwendung durch Clientanwendungen beim Aufrufen von Objektschnittstellen wie [IMAPIProp::GetProps](imapiprop-getprops.md) und [IMAPITable::QueryRows](imapitable-queryrows.md).</span><span class="sxs-lookup"><span data-stu-id="77256-160">MAPI uses the functions pointed to by  _lpAllocateBuffer_ and  _lpFreeBuffer_ for most memory allocation and deallocation, in particular to allocate memory for use by client applications when calling object interfaces such as [IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="77256-161">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="77256-161">Notes to callers</span></span>

<span data-ttu-id="77256-162">Das SOF_UNIQUEFILENAME wird verwendet, um eine temporäre Datei mit einem für das Messagingsystem eindeutigen Namen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="77256-162">The SOF_UNIQUEFILENAME flag is used to create a temporary file with a name unique to the messaging system.</span></span> <span data-ttu-id="77256-163">Wenn dieses Flag festgelegt ist, gibt der  _lpszFileName-Parameter_ den Pfad für die temporäre Datei an, und der  _lpszPrefix-Parameter_ enthält die Präfixzeichen des Dateinamens.</span><span class="sxs-lookup"><span data-stu-id="77256-163">If this flag is set, the  _lpszFileName_ parameter specifes the path for the temporary file, and the  _lpszPrefix_ parameter contains the prefix characters of the filename.</span></span> <span data-ttu-id="77256-164">Der konstruierte Dateiname ist <prefix> HHHH. TMP, wobei HHHH eine Hexadezimalzahl ist.</span><span class="sxs-lookup"><span data-stu-id="77256-164">The constructed filename is <prefix>HHHH.TMP, where HHHH is a hexadecimal number.</span></span> <span data-ttu-id="77256-165">Wenn  _lpszFileName_ NULL ist, wird die Datei im temporären Dateiverzeichnis erstellt, das von der Windows-Funktion **GetTempPath** oder dem aktuellen Verzeichnis zurückgegeben wird, wenn kein temporäres Dateiverzeichnis angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="77256-165">If  _lpszFileName_ is NULL, the file will be created in the temporary file directory that is returned from the Windows function **GetTempPath**, or the current directory if no temporary file directory has been designated.</span></span>
  
<span data-ttu-id="77256-166">Wenn das SOF_UNIQUEFILENAME nicht festgelegt ist,  _wird lpszPrefix_ ignoriert, und  _lpszFileName_ sollte den vollqualifizierten Pfad und Dateinamen der datei enthalten, die geöffnet oder erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="77256-166">If the SOF_UNIQUEFILENAME flag is not set,  _lpszPrefix_ is ignored, and  _lpszFileName_ should contain the fully qualified path and filename of the file to be opened or created.</span></span> <span data-ttu-id="77256-167">Die Datei wird basierend auf den anderen Flags geöffnet oder erstellt, die in _ulFlags festgelegt sind._</span><span class="sxs-lookup"><span data-stu-id="77256-167">The file will be opened or created based on the other flags that are set in  _ulFlags_.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="77256-168">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="77256-168">See also</span></span>



[<span data-ttu-id="77256-169">OpenStreamOnFile</span><span class="sxs-lookup"><span data-stu-id="77256-169">OpenStreamOnFile</span></span>](openstreamonfile.md)

