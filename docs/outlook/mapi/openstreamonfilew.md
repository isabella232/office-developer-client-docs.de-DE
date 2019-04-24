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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 7e67d84320b57fe6e510b70a68088f289ef6030d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348867"
---
# <a name="openstreamonfilew"></a><span data-ttu-id="93375-103">OpenStreamOnFileW</span><span class="sxs-lookup"><span data-stu-id="93375-103">OpenStreamOnFileW</span></span>

  
  
<span data-ttu-id="93375-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="93375-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="93375-105">Reserviert und initialisiert ein OLE **IStream** -Objekt, um auf den Inhalt einer Datei zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="93375-105">Allocates and initializes an OLE **IStream** object to access the contents of a file.</span></span> <span data-ttu-id="93375-106">Diese Funktion verwendet UNICODE-Zeichenfolgen als Argumente, im Gegensatz zur ANSI-Version dieser Funktion [OpenStreamOnFile](openstreamonfile.md)und ermöglicht daher beliebige Zeichen im Dateinamen, einschließlich des Pfads und der Dateierweiterung.</span><span class="sxs-lookup"><span data-stu-id="93375-106">This function takes UNICODE strings as arguments, unlike the ANSI version of this function [OpenStreamOnFile](openstreamonfile.md), and thus allows for arbitrary characters in the file name including the path and file extension.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="93375-107">Exportiert von:</span><span class="sxs-lookup"><span data-stu-id="93375-107">Exported by:</span></span>  <br/> |<span data-ttu-id="93375-108">olmapi32. dll</span><span class="sxs-lookup"><span data-stu-id="93375-108">olmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="93375-109">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="93375-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="93375-110">Outlook</span><span class="sxs-lookup"><span data-stu-id="93375-110">Outlook</span></span>  <br/> |
|<span data-ttu-id="93375-111">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="93375-111">Called by:</span></span>  <br/> |<span data-ttu-id="93375-112">Client Anwendungen und Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="93375-112">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="93375-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="93375-113">Parameters</span></span>

 <span data-ttu-id="93375-114">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="93375-114">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="93375-115">in Zeiger auf die [MAPIAllocateBuffer](mapiallocatebuffer.md) -Funktion, die zum Reservieren von Arbeitsspeicher verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="93375-115">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
 <span data-ttu-id="93375-116">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="93375-116">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="93375-117">in Zeiger auf die [mapifreebufferfreigegeben](mapifreebuffer.md) -Funktion, die verwendet werden, um Arbeitsspeicher freizugeben.</span><span class="sxs-lookup"><span data-stu-id="93375-117">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
 <span data-ttu-id="93375-118">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="93375-118">_ulFlags_</span></span>
  
> <span data-ttu-id="93375-119">in Bitmaske der Flags, die zum Steuern des Erstellens oder Öffnens der Datei verwendet werden, auf die über das **IStream** -Objekt von OLE zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="93375-119">[in] Bitmask of flags used to control the creation or opening of the file to be accessed through the OLE **IStream** object.</span></span> <span data-ttu-id="93375-120">Die folgenden Flags können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="93375-120">The following flags can be set:</span></span> 
    
<span data-ttu-id="93375-121">SOF_UNIQUEFILENAME</span><span class="sxs-lookup"><span data-stu-id="93375-121">SOF_UNIQUEFILENAME</span></span>
  
> <span data-ttu-id="93375-122">Für das **IStream** -Objekt muss eine temporäre Datei erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="93375-122">A temporary file is to be created for the **IStream** object.</span></span> <span data-ttu-id="93375-123">Wenn dieses Flag festgelegt ist, sollten auch die STGM_CREATE-und STGM_READWRITE-Flags festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="93375-123">If this flag is set, the STGM_CREATE and STGM_READWRITE flags should also be set.</span></span> 
    
<span data-ttu-id="93375-124">STGM_CREATE</span><span class="sxs-lookup"><span data-stu-id="93375-124">STGM_CREATE</span></span>
  
> <span data-ttu-id="93375-125">Die Datei muss auch dann erstellt werden, wenn Sie bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="93375-125">The file is to be created even if one already exists.</span></span> <span data-ttu-id="93375-126">Wenn der _lpszFileName_ -Parameter nicht festgelegt ist, müssen sowohl dieses Flag als auch STGM_DELETEONRELEASE festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="93375-126">If the  _lpszFileName_ parameter is not set, both this flag and STGM_DELETEONRELEASE must be set.</span></span> <span data-ttu-id="93375-127">Wenn STGM_CREATE festgelegt ist, muss auch das STGM_READWRITE-Flag festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="93375-127">If STGM_CREATE is set, the STGM_READWRITE flag must also be set.</span></span> 
    
<span data-ttu-id="93375-128">STGM_DELETEONRELEASE</span><span class="sxs-lookup"><span data-stu-id="93375-128">STGM_DELETEONRELEASE</span></span>
  
> <span data-ttu-id="93375-129">Die Datei muss gelöscht werden, wenn das **IStream** -Objekt freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="93375-129">The file is to be deleted when the **IStream** object is released.</span></span> <span data-ttu-id="93375-130">Wenn der _lpszFileName_ -Parameter nicht festgelegt ist, müssen sowohl dieses Flag als auch STGM_CREATE festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="93375-130">If the  _lpszFileName_ parameter is not set, both this flag and STGM_CREATE must be set.</span></span> 
    
<span data-ttu-id="93375-131">STGM_READ</span><span class="sxs-lookup"><span data-stu-id="93375-131">STGM_READ</span></span>
  
> <span data-ttu-id="93375-132">Die Datei muss mit Schreibschutz erstellt oder geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="93375-132">The file is to be created or opened with read-only access.</span></span>
    
<span data-ttu-id="93375-133">STGM_READWRITE</span><span class="sxs-lookup"><span data-stu-id="93375-133">STGM_READWRITE</span></span>
  
> <span data-ttu-id="93375-134">Die Datei muss mit Lese-/Schreibzugriff erstellt oder geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="93375-134">The file is to be created or opened with read/write permission.</span></span> <span data-ttu-id="93375-135">Wenn dieses Flag nicht festgelegt ist, darf das STGM_CREATE-Flag nicht festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="93375-135">If this flag is not set, the STGM_CREATE flag must not be set either.</span></span>
    
 <span data-ttu-id="93375-136">_lpszFileName_</span><span class="sxs-lookup"><span data-stu-id="93375-136">_lpszFileName_</span></span>
  
> <span data-ttu-id="93375-137">in Der Dateiname, einschließlich Pfad und Erweiterung der Unicode-Datei, für die **OpenStreamOnFileW** das **IStream** -Objekt initialisiert.</span><span class="sxs-lookup"><span data-stu-id="93375-137">[in] The filename, including path and extension, of the Unicode named file for which **OpenStreamOnFileW** initializes the **IStream** object.</span></span> <span data-ttu-id="93375-138">Wenn das SOF_UNIQUEFILENAME-Flag festgelegt ist, enthält _lpszFileName_ den Pfad zu dem Verzeichnis, in dem eine temporäre Datei erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="93375-138">If the SOF_UNIQUEFILENAME flag is set,  _lpszFileName_ contains the path to the directory in which to create a temporary file.</span></span> <span data-ttu-id="93375-139">Wenn _lpszFileName_ ist, ruft **OpenStreamOnFileW** einen entsprechenden Pfad vom System ab, und sowohl die STGM_CREATE-als auch die STGM_DELETEONRELEASE-Flags müssen festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="93375-139">If  _lpszFileName_ is NULL, **OpenStreamOnFileW** obtains an appropriate path from the system, and both the STGM_CREATE and STGM_DELETEONRELEASE flags must be set.</span></span> 
    
 <span data-ttu-id="93375-140">_lpszPrefix_</span><span class="sxs-lookup"><span data-stu-id="93375-140">_lpszPrefix_</span></span>
  
> <span data-ttu-id="93375-141">in Das Präfix für den Unicode-Dateinamen, auf dem **OpenStreamOnFileW** das **IStream** -Objekt initialisiert.</span><span class="sxs-lookup"><span data-stu-id="93375-141">[in] The prefix for the Unicode filename on which **OpenStreamOnFileW** initializes the **IStream** object.</span></span> <span data-ttu-id="93375-142">Wenn diese Einstellung festgelegt ist, darf das Präfix nicht mehr als drei Zeichen enthalten.</span><span class="sxs-lookup"><span data-stu-id="93375-142">If set, the prefix must contain not more than three characters.</span></span> <span data-ttu-id="93375-143">Wenn _lpszPrefix_ ist, wird ein Präfix von "Sof" verwendet.</span><span class="sxs-lookup"><span data-stu-id="93375-143">If  _lpszPrefix_ is NULL, a prefix of "SOF" is used.</span></span> 
    
 <span data-ttu-id="93375-144">_lppStream_</span><span class="sxs-lookup"><span data-stu-id="93375-144">_lppStream_</span></span>
  
> <span data-ttu-id="93375-145">Out Zeiger auf einen Zeiger auf ein Objekt, das die **IStream** -Schnittstelle verfügbar macht.</span><span class="sxs-lookup"><span data-stu-id="93375-145">[out] Pointer to a pointer to an object exposing the **IStream** interface.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="93375-146">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="93375-146">Return value</span></span>

<span data-ttu-id="93375-147">S_OK</span><span class="sxs-lookup"><span data-stu-id="93375-147">S_OK</span></span>
  
> <span data-ttu-id="93375-148">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="93375-148">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="93375-149">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="93375-149">MAPI_E_NO_ACCESS</span></span>
  
> <span data-ttu-id="93375-150">Auf die Datei konnte aufgrund unzureichender Benutzerberechtigungen nicht zugegriffen werden, oder da schreibgeschützte Dateien nicht geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="93375-150">The file could not be accessed due to insufficient user permissions or because read-only files cannot be modified.</span></span>
    
<span data-ttu-id="93375-151">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="93375-151">MAPI_E_NOT_FOUND</span></span>
  
> <span data-ttu-id="93375-152">Die angegebene Datei ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="93375-152">The designated file does not exist.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="93375-153">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="93375-153">Remarks</span></span>

<span data-ttu-id="93375-154">Die **OpenStreamOnFileW** -Funktion hat neben der Verarbeitung einer Datei mit einem Unicode-Namen, die durch die Einstellung des SOF_UNIQUEFILENAME-Flags gekennzeichnet ist, zwei wichtige Verwendungsmöglichkeiten.</span><span class="sxs-lookup"><span data-stu-id="93375-154">The **OpenStreamOnFileW** function has two important uses in addition to handling a file with a Unicode name, distinguished by the setting of the SOF_UNIQUEFILENAME flag.</span></span> <span data-ttu-id="93375-155">Wenn dieses Flag nicht festgelegt ist, öffnet **OpenStreamOnFileW** ein **IStream** -Objekt in einer vorhandenen Datei, beispielsweise, um den Inhalt in die **PR_ATTACH_DATA_BIN** ([pidtagattachdatabinary (](pidtagattachdatabinary-canonical-property.md))-Eigenschaft einer Anlage mithilfe der \*\* IStream:: CopyTo\*\* -Methode.</span><span class="sxs-lookup"><span data-stu-id="93375-155">When this flag is not set, **OpenStreamOnFileW** opens an **IStream** object on an existing file, for example to copy its contents to the **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) property of an attachment using the **IStream::CopyTo** method.</span></span> <span data-ttu-id="93375-156">In diesem Fall gibt der Parameter _lpszFileName_ den Pfad und den Dateinamen der Datei an.</span><span class="sxs-lookup"><span data-stu-id="93375-156">In this case the  _lpszFileName_ parameter specifies the path and filename of the file.</span></span> 
  
<span data-ttu-id="93375-157">Wenn SOF_UNIQUEFILENAME festgelegt ist, erstellt **OpenStreamOnFileW** eine temporäre Datei zum Speichern von Daten für ein **IStream** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="93375-157">When SOF_UNIQUEFILENAME is set, **OpenStreamOnFileW** creates a temporary file to hold data for an **IStream** object.</span></span> <span data-ttu-id="93375-158">Für diese Verwendung kann der Parameter _lpszFileName_ optional den Pfad zu dem Verzeichnis festlegen, in dem die Datei erstellt werden soll, und der Parameter _lpszPrefix_ kann optional ein Präfix für den Dateinamen angeben.</span><span class="sxs-lookup"><span data-stu-id="93375-158">For this usage, the  _lpszFileName_ parameter can optionally designate the path to the directory where the file is to be created, and the  _lpszPrefix_ parameter can optionally specify a prefix for the filename.</span></span> 
  
<span data-ttu-id="93375-159">Wenn die aufrufende Clientanwendung oder der Dienstanbieter mit dem **IStream** -Objekt fertig ist, sollten Sie diese freigeben, indem Sie die OLE **IStream:: Release** -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="93375-159">When the calling client application or service provider is finished with the **IStream** object, it should free it by calling the OLE **IStream::Release** method.</span></span> 
  
<span data-ttu-id="93375-160">MAPI verwendet die Funktionen, auf die von _lpAllocateBuffer_ und _lpFreeBuffer_ verwiesen wird, für die meisten Speicherzuweisungen und-Aufhebungen, insbesondere für die Zuweisung von Arbeitsspeicher für Clientanwendungen beim Aufrufen von Objektschnittstellen wie [IMAPIProp:: ](imapiprop-getprops.md)GetProps und [IMAPITable:: QueryRows](imapitable-queryrows.md).</span><span class="sxs-lookup"><span data-stu-id="93375-160">MAPI uses the functions pointed to by  _lpAllocateBuffer_ and  _lpFreeBuffer_ for most memory allocation and deallocation, in particular to allocate memory for use by client applications when calling object interfaces such as [IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="93375-161">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="93375-161">Notes to callers</span></span>

<span data-ttu-id="93375-162">Das SOF_UNIQUEFILENAME-Flag wird verwendet, um eine temporäre Datei mit einem eindeutigen Namen für das Messagingsystem zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="93375-162">The SOF_UNIQUEFILENAME flag is used to create a temporary file with a name unique to the messaging system.</span></span> <span data-ttu-id="93375-163">Wenn dieses Flag festgelegt ist, angibt der _lpszFileName_ -Parameter den Pfad für die temporäre Datei, und der _lpszPrefix_ -Parameter enthält die Präfixzeichen des Datei namens.</span><span class="sxs-lookup"><span data-stu-id="93375-163">If this flag is set, the  _lpszFileName_ parameter specifes the path for the temporary file, and the  _lpszPrefix_ parameter contains the prefix characters of the filename.</span></span> <span data-ttu-id="93375-164">Der erstellte Dateiname lautet <prefix>HHHH. TMP, wobei HHHH eine Hexadezimalzahl ist.</span><span class="sxs-lookup"><span data-stu-id="93375-164">The constructed filename is <prefix>HHHH.TMP, where HHHH is a hexadecimal number.</span></span> <span data-ttu-id="93375-165">Wenn _lpszFileName_ ist, wird die Datei im temporären Dateiverzeichnis erstellt, das von der Windows-Funktion **GetTempPath**zurückgegeben wird, oder das aktuelle Verzeichnis, wenn kein temporäres Dateiverzeichnis festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="93375-165">If  _lpszFileName_ is NULL, the file will be created in the temporary file directory that is returned from the Windows function **GetTempPath**, or the current directory if no temporary file directory has been designated.</span></span>
  
<span data-ttu-id="93375-166">Wenn das SOF_UNIQUEFILENAME-Flag nicht festgelegt ist, wird _lpszPrefix_ ignoriert, und _lpszFileName_ sollte den vollqualifizierten Pfad und Dateinamen der zu öffnenden oder zu erstellenden Datei enthalten.</span><span class="sxs-lookup"><span data-stu-id="93375-166">If the SOF_UNIQUEFILENAME flag is not set,  _lpszPrefix_ is ignored, and  _lpszFileName_ should contain the fully qualified path and filename of the file to be opened or created.</span></span> <span data-ttu-id="93375-167">Die Datei wird basierend auf den anderen in _ulFlags_festgelegten Flags geöffnet oder erstellt.</span><span class="sxs-lookup"><span data-stu-id="93375-167">The file will be opened or created based on the other flags that are set in  _ulFlags_.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="93375-168">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="93375-168">See also</span></span>



[<span data-ttu-id="93375-169">OpenStreamOnFile</span><span class="sxs-lookup"><span data-stu-id="93375-169">OpenStreamOnFile</span></span>](openstreamonfile.md)

