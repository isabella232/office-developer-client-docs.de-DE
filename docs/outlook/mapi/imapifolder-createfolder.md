---
title: IMAPIFolderCreateFolder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.CreateFolder
api_type:
- COM
ms.assetid: 39d07fc8-09aa-4122-af32-b02f2c893d29
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 36fd729b1ca3e5d877d03358d581b83fc6d4782c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792107"
---
# <a name="imapifoldercreatefolder"></a><span data-ttu-id="0e0fe-103">IMAPIFolder::CreateFolder</span><span class="sxs-lookup"><span data-stu-id="0e0fe-103">IMAPIFolder::CreateFolder</span></span>

  
  
<span data-ttu-id="0e0fe-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0e0fe-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0e0fe-105">Erstellt einen neuen Unterordner.</span><span class="sxs-lookup"><span data-stu-id="0e0fe-105">Creates a new subfolder.</span></span>
  
```cpp
HRESULT CreateFolder(
  ULONG ulFolderType,
  LPSTR lpszFolderName,
  LPSTR lpszFolderComment,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPMAPIFOLDER FAR * lppFolder
);
```

## <a name="parameters"></a><span data-ttu-id="0e0fe-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0e0fe-106">Parameters</span></span>

 <span data-ttu-id="0e0fe-107">_ulFolderType_</span><span class="sxs-lookup"><span data-stu-id="0e0fe-107">_ulFolderType_</span></span>
  
> <span data-ttu-id="0e0fe-108">[in] Der Typ des zu erstellenden Ordners.</span><span class="sxs-lookup"><span data-stu-id="0e0fe-108">[in] The type of folder to create.</span></span> <span data-ttu-id="0e0fe-109">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="0e0fe-109">The following flags can be set:</span></span>
    
<span data-ttu-id="0e0fe-110">FOLDER_GENERIC</span><span class="sxs-lookup"><span data-stu-id="0e0fe-110">FOLDER_GENERIC</span></span> 
  
> <span data-ttu-id="0e0fe-111">Ein generischer Ordner sollte erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="0e0fe-111">A generic folder should be created.</span></span>
    
<span data-ttu-id="0e0fe-112">FOLDER_SEARCH</span><span class="sxs-lookup"><span data-stu-id="0e0fe-112">FOLDER_SEARCH</span></span> 
  
> <span data-ttu-id="0e0fe-113">Ein Suchergebnisse Ordner sollte erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="0e0fe-113">A search-results folder should be created.</span></span>
    
 <span data-ttu-id="0e0fe-114">_lpszFolderName_</span><span class="sxs-lookup"><span data-stu-id="0e0fe-114">_lpszFolderName_</span></span>
  
> <span data-ttu-id="0e0fe-115">[in] Ein Zeiger auf eine Zeichenfolge, die den Namen für den neuen Ordner enthält.</span><span class="sxs-lookup"><span data-stu-id="0e0fe-115">[in] A pointer to a string that contains the name for the new folder.</span></span> <span data-ttu-id="0e0fe-116">Dieser Name ist die Grundlage für den neuen Ordner **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="0e0fe-116">This name is the basis for the new folder's **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property.</span></span>
    
 <span data-ttu-id="0e0fe-117">_lpszFolderComment_</span><span class="sxs-lookup"><span data-stu-id="0e0fe-117">_lpszFolderComment_</span></span>
  
> <span data-ttu-id="0e0fe-118">[in] Ein Zeiger auf eine Zeichenfolge, die einen Kommentar Zusammenhang mit den neuen Ordner enthält.</span><span class="sxs-lookup"><span data-stu-id="0e0fe-118">[in] A pointer to a string that contains a comment associated with the new folder.</span></span> <span data-ttu-id="0e0fe-119">Diese Zeichenfolge wird der Wert der Eigenschaft für den neuen Ordner **PR_COMMENT** ([PidTagComment](pidtagcomment-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="0e0fe-119">This string becomes the value of the new folder's **PR_COMMENT** ([PidTagComment](pidtagcomment-canonical-property.md)) property.</span></span> <span data-ttu-id="0e0fe-120">Wenn NULL übergeben wird, hat der Ordner keine Kommentar.</span><span class="sxs-lookup"><span data-stu-id="0e0fe-120">If NULL is passed, the folder has no initial comment.</span></span>
    
 <span data-ttu-id="0e0fe-121">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="0e0fe-121">_lpInterface_</span></span>
  
> <span data-ttu-id="0e0fe-122">[in] Ein Zeiger auf die Schnittstelle-ID (IID), die die Schnittstelle verwendet werden, Zugriff auf den neuen Ordner darstellt.</span><span class="sxs-lookup"><span data-stu-id="0e0fe-122">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the new folder.</span></span> <span data-ttu-id="0e0fe-123">Übergeben von NULL wird eine Nachricht an die Standardordner-Schnittstelle zurück, die [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="0e0fe-123">Passing NULL causes the message store provider to return the standard folder interface, [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md).</span></span> <span data-ttu-id="0e0fe-124">Clients müssen NULL übergeben.</span><span class="sxs-lookup"><span data-stu-id="0e0fe-124">Clients must pass NULL.</span></span> <span data-ttu-id="0e0fe-125">Andere Aufrufer können den Parameter _LpInterface_ auf IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer oder IID_IMAPIFolder festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0e0fe-125">Other callers can set the  _lpInterface_ parameter to IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer, or IID_IMAPIFolder.</span></span> 
    
 <span data-ttu-id="0e0fe-126">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="0e0fe-126">_ulFlags_</span></span>
  
> <span data-ttu-id="0e0fe-127">[in] Eine Bitmaske aus Flags, die steuert, wie der Ordner erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="0e0fe-127">[in] A bitmask of flags that controls how the folder is created.</span></span> <span data-ttu-id="0e0fe-128">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="0e0fe-128">The following flags can be set:</span></span>
    
<span data-ttu-id="0e0fe-129">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="0e0fe-129">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="0e0fe-130">Ermöglicht die **CreateFolder** erfolgreich, möglicherweise beendet, bevor Sie der neue Ordner vollständig an den aufrufenden Client verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="0e0fe-130">Allows **CreateFolder** to return successfully, possibly before the new folder is fully available to the calling client.</span></span> <span data-ttu-id="0e0fe-131">Wenn Sie der neue Ordner nicht verfügbar ist, kann nachfolgende anrufen darauf verursacht einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="0e0fe-131">If the new folder is not available, making a subsequent call to it can cause an error.</span></span> 
    
<span data-ttu-id="0e0fe-132">PARAMETER MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="0e0fe-132">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="0e0fe-133">Der Name des Ordners ist im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="0e0fe-133">The name of the folder is in Unicode format.</span></span> <span data-ttu-id="0e0fe-134">Wenn die Option MAPI_UNICODE nicht festgelegt ist, ist der Name des Ordners im ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="0e0fe-134">If the MAPI_UNICODE flag is not set, the folder name is in ANSI format.</span></span>
    
<span data-ttu-id="0e0fe-135">OPEN_IF_EXISTS</span><span class="sxs-lookup"><span data-stu-id="0e0fe-135">OPEN_IF_EXISTS</span></span> 
  
> <span data-ttu-id="0e0fe-136">Die Methode erfolgreich ausgeführt, auch wenn Sie der Ordner mit dem Namen im Parameter _LpszFolderName_ bereits vorhanden ist, indem Sie den vorhandenen Ordner mit diesem Namen öffnen können.</span><span class="sxs-lookup"><span data-stu-id="0e0fe-136">Allows the method to succeed even if the folder named in the  _lpszFolderName_ parameter already exists by opening the existing folder that has that name.</span></span> <span data-ttu-id="0e0fe-137">Beachten Sie, dass Nachricht-Anbieter, mit die gleichgeordneten Knoten Ordner, die denselben Namen aufweisen können keinen bestehenden Ordner öffnen möglicherweise, wenn mehr als eine mit dem angegebenen Namen vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="0e0fe-137">Note that message store providers that allow sibling folders to have the same name might not open an existing folder if more than one exists with the supplied name.</span></span> 
    
 <span data-ttu-id="0e0fe-138">_lppFolder_</span><span class="sxs-lookup"><span data-stu-id="0e0fe-138">_lppFolder_</span></span>
  
> <span data-ttu-id="0e0fe-139">[out] Ein Zeiger auf einen Zeiger auf den neu erstellten Ordner.</span><span class="sxs-lookup"><span data-stu-id="0e0fe-139">[out] A pointer to a pointer to the newly created folder.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0e0fe-140">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="0e0fe-140">Return value</span></span>

<span data-ttu-id="0e0fe-141">S_OK</span><span class="sxs-lookup"><span data-stu-id="0e0fe-141">S_OK</span></span> 
  
> <span data-ttu-id="0e0fe-142">Neue Ordner wurde erfolgreich erstellt oder geöffnet, wenn das Flag OPEN_IF_EXISTS festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="0e0fe-142">The new folder has been successfully created or opened, if the OPEN_IF_EXISTS flag is set.</span></span>
    
<span data-ttu-id="0e0fe-143">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="0e0fe-143">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="0e0fe-144">Entweder die Option MAPI_UNICODE festgelegt wurde und die Implementierung unterstützt keine Unicode oder Parameter MAPI_UNICODE nicht festgelegt wurde und die Implementierung unterstützt nur Unicode.</span><span class="sxs-lookup"><span data-stu-id="0e0fe-144">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
<span data-ttu-id="0e0fe-145">MAPI_E_COLLISION</span><span class="sxs-lookup"><span data-stu-id="0e0fe-145">MAPI_E_COLLISION</span></span> 
  
> <span data-ttu-id="0e0fe-146">Ein Ordner mit dem Namen bereits in der _LpszFolderName_ -Parameter angegebenen vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="0e0fe-146">A folder that has the name given in the  _lpszFolderName_ parameter already exists.</span></span> <span data-ttu-id="0e0fe-147">Ordnernamen müssen eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="0e0fe-147">Folder names must be unique.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="0e0fe-148">Hinweise</span><span class="sxs-lookup"><span data-stu-id="0e0fe-148">Remarks</span></span>

<span data-ttu-id="0e0fe-149">Die **IMAPIFolder::CreateFolder** -Methode erstellt einen Unterordner im aktuellen Ordner und den neuen Ordner eine Eintrags-ID zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="0e0fe-149">The **IMAPIFolder::CreateFolder** method creates a subfolder in the current folder and assigns an entry identifier to the new folder.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="0e0fe-150">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="0e0fe-150">Notes to callers</span></span>

<span data-ttu-id="0e0fe-151">Wenn **CreateFolder** zurückgegeben wird, achten Sie darauf, dass die Eintrags-ID für den neuen Ordner möglicherweise nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="0e0fe-151">When **CreateFolder** returns, be aware that the entry identifier for the new folder might not be available.</span></span> <span data-ttu-id="0e0fe-152">Einige Anbieter Nachricht machen nicht Eintragsbezeichner erst verfügbar, nachdem Sie den neuen Ordner [IMAPIProp::SaveChanges](imapiprop-savechanges.md) -Methode, um sie dauerhaft zu speichern aufgerufen haben.</span><span class="sxs-lookup"><span data-stu-id="0e0fe-152">Some message store providers do not make entry identifiers available until after you have called the new folder's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to permanently save it.</span></span> <span data-ttu-id="0e0fe-153">Dies ist insbesondere dann, wenn Sie die Kennzeichen MAPI_DEFERRED_ERRORS eingerichtet haben.</span><span class="sxs-lookup"><span data-stu-id="0e0fe-153">This is especially true if you have set the MAPI_DEFERRED_ERRORS flag.</span></span> 
  
<span data-ttu-id="0e0fe-154">Beachten Sie, dass einige Anbieter Nachricht immer den _LppFolder_ -Parameter auf den Ordner Standardschnittstelle ungeachtet des Werts verweisen, die Sie für den _LpInterface_ -Parameter übergeben.</span><span class="sxs-lookup"><span data-stu-id="0e0fe-154">Be aware that some message store providers always point the  _lppFolder_ parameter to the folder's standard interface, regardless of the value that you pass in for the  _lpInterface_ parameter.</span></span> <span data-ttu-id="0e0fe-155">Da Zeiger der Schnittstelle, der zurückgegeben wird nicht vom Typ, die Sie erwarten sein kann, rufen Sie den neuen Ordner [IMAPIProp::GetProps](imapiprop-getprops.md) -Methode zum Abrufen der Eigenschaft **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="0e0fe-155">Because the interface pointer that is returned might not be of the type that you expect, call the new folder's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) property.</span></span> <span data-ttu-id="0e0fe-156">Falls erforderlich, wandeln Sie den Zeiger auf ein anderes besser geeignet, bevor Sie andere Anrufe tätigen.</span><span class="sxs-lookup"><span data-stu-id="0e0fe-156">If necessary, cast the pointer to a more appropriate type before you make other calls.</span></span>
  
<span data-ttu-id="0e0fe-157">Die meisten Anbieter Nachricht erfordern den Namen des neuen Ordners in Bezug auf die Namen der zugehörigen gleichgeordneten Knoten Ordner eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="0e0fe-157">Most message store providers require the name of the new folder to be unique with respect to the names of its sibling folders.</span></span> <span data-ttu-id="0e0fe-158">Möglicherweise den Fehlerwert MAPI_E_COLLISION verarbeitet werden, die zurückgegeben wird, wenn diese Regel nicht befolgt wird.</span><span class="sxs-lookup"><span data-stu-id="0e0fe-158">Be able to handle the MAPI_E_COLLISION error value, which is returned if this rule is not followed.</span></span> 
  
<span data-ttu-id="0e0fe-159">Um die Eintrags-ID des neu erstellten Ordners zu bestimmen, rufen Sie den neuen Ordner **IMAPIProp::GetProps** -Methode zum Abrufen der Eigenschaft **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="0e0fe-159">To determine the entry identifier of the newly created folder, call the new folder's **IMAPIProp::GetProps** method to retrieve its **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="0e0fe-160">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="0e0fe-160">MFCMAPI reference</span></span>

<span data-ttu-id="0e0fe-161">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="0e0fe-161">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="0e0fe-162">**Datei**</span><span class="sxs-lookup"><span data-stu-id="0e0fe-162">**File**</span></span>|<span data-ttu-id="0e0fe-163">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="0e0fe-163">**Function**</span></span>|<span data-ttu-id="0e0fe-164">**Comment**</span><span class="sxs-lookup"><span data-stu-id="0e0fe-164">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="0e0fe-165">MsgStoreDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="0e0fe-165">MsgStoreDlg.cpp</span></span>  <br/> |<span data-ttu-id="0e0fe-166">CMsgStoreDlg::OnCreateSubFolder</span><span class="sxs-lookup"><span data-stu-id="0e0fe-166">CMsgStoreDlg::OnCreateSubFolder</span></span>  <br/> |<span data-ttu-id="0e0fe-167">MFCMAPI (engl.) verwendet die **CMsgStoreDlg::OnCreateSubFolder** -Methode zum Erstellen von neuer Ordnern in MFCMAPI (engl.).</span><span class="sxs-lookup"><span data-stu-id="0e0fe-167">MFCMAPI uses the **CMsgStoreDlg::OnCreateSubFolder** method to create new folders in MFCMAPI.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0e0fe-168">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0e0fe-168">See also</span></span>



[<span data-ttu-id="0e0fe-169">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="0e0fe-169">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="0e0fe-170">IMAPIFolder: IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="0e0fe-170">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)


[<span data-ttu-id="0e0fe-171">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="0e0fe-171">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

