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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 606d780aa59e363c30ddc7a5b562db64d845ccb0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436762"
---
# <a name="imapifoldercreatefolder"></a><span data-ttu-id="ccb7e-103">IMAPIFolder::CreateFolder</span><span class="sxs-lookup"><span data-stu-id="ccb7e-103">IMAPIFolder::CreateFolder</span></span>

  
  
<span data-ttu-id="ccb7e-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ccb7e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ccb7e-105">Erstellt einen neuen Unterordner.</span><span class="sxs-lookup"><span data-stu-id="ccb7e-105">Creates a new subfolder.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="ccb7e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ccb7e-106">Parameters</span></span>

 <span data-ttu-id="ccb7e-107">_ulFolderType_</span><span class="sxs-lookup"><span data-stu-id="ccb7e-107">_ulFolderType_</span></span>
  
> <span data-ttu-id="ccb7e-108">in Der Typ des zu erstellende Ordners.</span><span class="sxs-lookup"><span data-stu-id="ccb7e-108">[in] The type of folder to create.</span></span> <span data-ttu-id="ccb7e-109">Die folgenden Flags können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="ccb7e-109">The following flags can be set:</span></span>
    
<span data-ttu-id="ccb7e-110">FOLDER_GENERIC</span><span class="sxs-lookup"><span data-stu-id="ccb7e-110">FOLDER_GENERIC</span></span> 
  
> <span data-ttu-id="ccb7e-111">Es sollte ein generischer Ordner erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="ccb7e-111">A generic folder should be created.</span></span>
    
<span data-ttu-id="ccb7e-112">FOLDER_SEARCH</span><span class="sxs-lookup"><span data-stu-id="ccb7e-112">FOLDER_SEARCH</span></span> 
  
> <span data-ttu-id="ccb7e-113">Es sollte ein Ordner mit Suchergebnissen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="ccb7e-113">A search-results folder should be created.</span></span>
    
 <span data-ttu-id="ccb7e-114">_lpszFolderName_</span><span class="sxs-lookup"><span data-stu-id="ccb7e-114">_lpszFolderName_</span></span>
  
> <span data-ttu-id="ccb7e-115">in Ein Zeiger auf eine Zeichenfolge, die den Namen für den neuen Ordner enthält.</span><span class="sxs-lookup"><span data-stu-id="ccb7e-115">[in] A pointer to a string that contains the name for the new folder.</span></span> <span data-ttu-id="ccb7e-116">Dieser Name ist die Basis für die **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))-Eigenschaft des neuen Ordners.</span><span class="sxs-lookup"><span data-stu-id="ccb7e-116">This name is the basis for the new folder's **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property.</span></span>
    
 <span data-ttu-id="ccb7e-117">_lpszFolderComment_</span><span class="sxs-lookup"><span data-stu-id="ccb7e-117">_lpszFolderComment_</span></span>
  
> <span data-ttu-id="ccb7e-118">in Ein Zeiger auf eine Zeichenfolge, die einen Kommentar enthält, der dem neuen Ordner zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="ccb7e-118">[in] A pointer to a string that contains a comment associated with the new folder.</span></span> <span data-ttu-id="ccb7e-119">Diese Zeichenfolge wird zum Wert der **PR_COMMENT** ([PidTagComment](pidtagcomment-canonical-property.md))-Eigenschaft des neuen Ordners.</span><span class="sxs-lookup"><span data-stu-id="ccb7e-119">This string becomes the value of the new folder's **PR_COMMENT** ([PidTagComment](pidtagcomment-canonical-property.md)) property.</span></span> <span data-ttu-id="ccb7e-120">Wenn NULL übergeben wird, hat der Ordner keinen anfänglichen Kommentar.</span><span class="sxs-lookup"><span data-stu-id="ccb7e-120">If NULL is passed, the folder has no initial comment.</span></span>
    
 <span data-ttu-id="ccb7e-121">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="ccb7e-121">_lpInterface_</span></span>
  
> <span data-ttu-id="ccb7e-122">in Ein Zeiger auf die Schnittstellen-ID (IID), die die Schnittstelle darstellt, die für den Zugriff auf den neuen Ordner verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="ccb7e-122">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the new folder.</span></span> <span data-ttu-id="ccb7e-123">Die Übergabe von NULL bewirkt, dass der Nachrichtenspeicher Anbieter die Standardordner Schnittstelle [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md)zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="ccb7e-123">Passing NULL causes the message store provider to return the standard folder interface, [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md).</span></span> <span data-ttu-id="ccb7e-124">Clients müssen NULL überschreiten.</span><span class="sxs-lookup"><span data-stu-id="ccb7e-124">Clients must pass NULL.</span></span> <span data-ttu-id="ccb7e-125">Andere Aufrufer können den _lpInterface_ -Parameter auf IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer oder IID_IMAPIFolder festlegen.</span><span class="sxs-lookup"><span data-stu-id="ccb7e-125">Other callers can set the  _lpInterface_ parameter to IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer, or IID_IMAPIFolder.</span></span> 
    
 <span data-ttu-id="ccb7e-126">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ccb7e-126">_ulFlags_</span></span>
  
> <span data-ttu-id="ccb7e-127">in Eine Bitmaske von Flags, die die Erstellung des Ordners steuert.</span><span class="sxs-lookup"><span data-stu-id="ccb7e-127">[in] A bitmask of flags that controls how the folder is created.</span></span> <span data-ttu-id="ccb7e-128">Die folgenden Flags können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="ccb7e-128">The following flags can be set:</span></span>
    
<span data-ttu-id="ccb7e-129">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="ccb7e-129">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="ccb7e-130">Ermöglicht \*\*\*\* , dass CreateFolder erfolgreich zurückgegeben wird, möglicherweise bevor der neue Ordner vollständig für den aufrufenden Client verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="ccb7e-130">Allows **CreateFolder** to return successfully, possibly before the new folder is fully available to the calling client.</span></span> <span data-ttu-id="ccb7e-131">Wenn der neue Ordner nicht verfügbar ist, kann der nachfolgende Aufruf zu einem Fehler führen.</span><span class="sxs-lookup"><span data-stu-id="ccb7e-131">If the new folder is not available, making a subsequent call to it can cause an error.</span></span> 
    
<span data-ttu-id="ccb7e-132">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="ccb7e-132">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="ccb7e-133">Der Name des Ordners ist im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="ccb7e-133">The name of the folder is in Unicode format.</span></span> <span data-ttu-id="ccb7e-134">Wenn das MAPI_UNICODE-Flag nicht festgelegt ist, ist der Ordnername im ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="ccb7e-134">If the MAPI_UNICODE flag is not set, the folder name is in ANSI format.</span></span>
    
<span data-ttu-id="ccb7e-135">OPEN_IF_EXISTS</span><span class="sxs-lookup"><span data-stu-id="ccb7e-135">OPEN_IF_EXISTS</span></span> 
  
> <span data-ttu-id="ccb7e-136">Die Methode kann auch dann erfolgreich ausgeführt werden, wenn der im _lpszFolderName_ -Parameter genannte Ordner bereits vorhanden ist, indem der vorhandene Ordner mit diesem Namen geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="ccb7e-136">Allows the method to succeed even if the folder named in the  _lpszFolderName_ parameter already exists by opening the existing folder that has that name.</span></span> <span data-ttu-id="ccb7e-137">Beachten Sie, dass Nachrichtenspeicher Anbieter, die gleichgeordnete Ordner mit demselben Namen zulassen, möglicherweise keinen vorhandenen Ordner öffnen, wenn mehrere mit dem angegebenen Namen vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="ccb7e-137">Note that message store providers that allow sibling folders to have the same name might not open an existing folder if more than one exists with the supplied name.</span></span> 
    
 <span data-ttu-id="ccb7e-138">_lppFolder_</span><span class="sxs-lookup"><span data-stu-id="ccb7e-138">_lppFolder_</span></span>
  
> <span data-ttu-id="ccb7e-139">Out Ein Zeiger auf einen Zeiger auf den neu erstellten Ordner.</span><span class="sxs-lookup"><span data-stu-id="ccb7e-139">[out] A pointer to a pointer to the newly created folder.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ccb7e-140">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ccb7e-140">Return value</span></span>

<span data-ttu-id="ccb7e-141">S_OK</span><span class="sxs-lookup"><span data-stu-id="ccb7e-141">S_OK</span></span> 
  
> <span data-ttu-id="ccb7e-142">Der neue Ordner wurde erfolgreich erstellt oder geöffnet, wenn das OPEN_IF_EXISTS-Flag festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="ccb7e-142">The new folder has been successfully created or opened, if the OPEN_IF_EXISTS flag is set.</span></span>
    
<span data-ttu-id="ccb7e-143">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="ccb7e-143">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="ccb7e-144">Entweder wurde das MAPI_UNICODE-Flag festgelegt, und die Implementierung unterstützt Unicode nicht, oder MAPI_UNICODE wurde nicht festgelegt, und die Implementierung unterstützt nur Unicode.</span><span class="sxs-lookup"><span data-stu-id="ccb7e-144">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
<span data-ttu-id="ccb7e-145">MAPI_E_COLLISION</span><span class="sxs-lookup"><span data-stu-id="ccb7e-145">MAPI_E_COLLISION</span></span> 
  
> <span data-ttu-id="ccb7e-146">Ein Ordner mit dem im _lpszFolderName_ -Parameter angegebenen Namen ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="ccb7e-146">A folder that has the name given in the  _lpszFolderName_ parameter already exists.</span></span> <span data-ttu-id="ccb7e-147">Ordnernamen müssen eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="ccb7e-147">Folder names must be unique.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="ccb7e-148">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ccb7e-148">Remarks</span></span>

<span data-ttu-id="ccb7e-149">Die **IMAPIFolder:: CreateFolder** -Methode erstellt einen Unterordner im aktuellen Ordner und weist dem neuen Ordner eine Eintrags-ID zu.</span><span class="sxs-lookup"><span data-stu-id="ccb7e-149">The **IMAPIFolder::CreateFolder** method creates a subfolder in the current folder and assigns an entry identifier to the new folder.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="ccb7e-150">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="ccb7e-150">Notes to callers</span></span>

<span data-ttu-id="ccb7e-151">Wenn **CreateFolder** zurückgegeben wird, müssen Sie beachten, dass die Eintrags-ID für den neuen Ordner möglicherweise nicht verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="ccb7e-151">When **CreateFolder** returns, be aware that the entry identifier for the new folder might not be available.</span></span> <span data-ttu-id="ccb7e-152">Einige Nachrichtenspeicher Anbieter stellen keine Eingabe-IDs zur Verfügung, bis Sie die [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) -Methode des neuen Ordners aufgerufen haben, um Sie dauerhaft zu speichern.</span><span class="sxs-lookup"><span data-stu-id="ccb7e-152">Some message store providers do not make entry identifiers available until after you have called the new folder's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to permanently save it.</span></span> <span data-ttu-id="ccb7e-153">Dies gilt insbesondere, wenn Sie das MAPI_DEFERRED_ERRORS-Flag festgelegt haben.</span><span class="sxs-lookup"><span data-stu-id="ccb7e-153">This is especially true if you have set the MAPI_DEFERRED_ERRORS flag.</span></span> 
  
<span data-ttu-id="ccb7e-154">Beachten Sie, dass einige Nachrichtenspeicher Anbieter den Parameter _lppFolder_ immer auf die Standardschnittstelle des Ordners verweisen, unabhängig davon, welcher Wert für den _lpInterface_ -Parameter übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="ccb7e-154">Be aware that some message store providers always point the  _lppFolder_ parameter to the folder's standard interface, regardless of the value that you pass in for the  _lpInterface_ parameter.</span></span> <span data-ttu-id="ccb7e-155">Da der zurückgegebene Schnittstellenzeiger möglicherweise nicht vom erwarteten Typ ist, rufen Sie die [IMAPIProp::](imapiprop-getprops.md) GetProps-Methode des neuen Ordners auf, um die **PR_OBJECT_TYPE** ([pidtagobjecttype (](pidtagobjecttype-canonical-property.md))-Eigenschaft abzurufen.</span><span class="sxs-lookup"><span data-stu-id="ccb7e-155">Because the interface pointer that is returned might not be of the type that you expect, call the new folder's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) property.</span></span> <span data-ttu-id="ccb7e-156">Falls erforderlich, werfen Sie den Zeiger in einen besser geeigneten Typ, bevor Sie andere Aufrufe ausführen.</span><span class="sxs-lookup"><span data-stu-id="ccb7e-156">If necessary, cast the pointer to a more appropriate type before you make other calls.</span></span>
  
<span data-ttu-id="ccb7e-157">Für die meisten Nachrichtenspeicher Anbieter muss der Name des neuen Ordners im Hinblick auf die Namen seiner nebengeordneten Ordner eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="ccb7e-157">Most message store providers require the name of the new folder to be unique with respect to the names of its sibling folders.</span></span> <span data-ttu-id="ccb7e-158">Sie können den MAPI_E_COLLISION-Fehlerwert behandeln, der zurückgegeben wird, wenn diese Regel nicht befolgt wird.</span><span class="sxs-lookup"><span data-stu-id="ccb7e-158">Be able to handle the MAPI_E_COLLISION error value, which is returned if this rule is not followed.</span></span> 
  
<span data-ttu-id="ccb7e-159">Um die Eintrags-ID des neu erstellten Ordners zu bestimmen, rufen Sie die **IMAPIProp::** GetProps-Methode des neuen Ordners auf, um die **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))-Eigenschaft abzurufen.</span><span class="sxs-lookup"><span data-stu-id="ccb7e-159">To determine the entry identifier of the newly created folder, call the new folder's **IMAPIProp::GetProps** method to retrieve its **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="ccb7e-160">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="ccb7e-160">MFCMAPI reference</span></span>

<span data-ttu-id="ccb7e-161">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="ccb7e-161">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="ccb7e-162">**Datei**</span><span class="sxs-lookup"><span data-stu-id="ccb7e-162">**File**</span></span>|<span data-ttu-id="ccb7e-163">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="ccb7e-163">**Function**</span></span>|<span data-ttu-id="ccb7e-164">**Comment**</span><span class="sxs-lookup"><span data-stu-id="ccb7e-164">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ccb7e-165">MsgStoreDlg. cpp</span><span class="sxs-lookup"><span data-stu-id="ccb7e-165">MsgStoreDlg.cpp</span></span>  <br/> |<span data-ttu-id="ccb7e-166">CMsgStoreDlg:: OnCreateSubFolder</span><span class="sxs-lookup"><span data-stu-id="ccb7e-166">CMsgStoreDlg::OnCreateSubFolder</span></span>  <br/> |<span data-ttu-id="ccb7e-167">MFCMAPI verwendet die **CMsgStoreDlg:: OnCreateSubFolder** -Methode, um neue Ordner in MfcMapi zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="ccb7e-167">MFCMAPI uses the **CMsgStoreDlg::OnCreateSubFolder** method to create new folders in MFCMAPI.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ccb7e-168">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ccb7e-168">See also</span></span>



[<span data-ttu-id="ccb7e-169">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="ccb7e-169">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="ccb7e-170">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="ccb7e-170">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)


[<span data-ttu-id="ccb7e-171">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="ccb7e-171">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

