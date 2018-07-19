---
title: IAddrBookSetDefaultDir
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.SetDefaultDir
api_type:
- COM
ms.assetid: d5d60150-15e4-41ff-bfb0-0c67e2abcacc
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 00d5b2bfc6b0c024f0ef12ce19fed90ef0af6721
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792002"
---
# <a name="iaddrbooksetdefaultdir"></a><span data-ttu-id="feb50-103">IAddrBook::SetDefaultDir</span><span class="sxs-lookup"><span data-stu-id="feb50-103">IAddrBook::SetDefaultDir</span></span>

  
  
<span data-ttu-id="feb50-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="feb50-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="feb50-105">Stellt den angegebenen Container als Standard Adressbuchcontainer her.</span><span class="sxs-lookup"><span data-stu-id="feb50-105">Establishes the specified container as the default address book container.</span></span>
  
```cpp
HRESULT SetDefaultDir(
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="feb50-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="feb50-106">Parameters</span></span>

 <span data-ttu-id="feb50-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="feb50-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="feb50-108">[in] Die Byteanzahl von in die Eintrags-ID auf den durch den Parameter _LpEntryID_ verwiesen.</span><span class="sxs-lookup"><span data-stu-id="feb50-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="feb50-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="feb50-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="feb50-110">[in] Ein Zeiger auf die Eintrags-ID der Standard-Adressbuchcontainer.</span><span class="sxs-lookup"><span data-stu-id="feb50-110">[in] A pointer to the entry identifier of the default address book container.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="feb50-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="feb50-111">Return value</span></span>

<span data-ttu-id="feb50-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="feb50-112">S_OK</span></span> 
  
> <span data-ttu-id="feb50-113">Die Standard-Adressbuchcontainer wurde erfolgreich festgelegt.</span><span class="sxs-lookup"><span data-stu-id="feb50-113">The default address book container was successfully set.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="feb50-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="feb50-114">Remarks</span></span>

<span data-ttu-id="feb50-115">Clients und Dienstanbieter rufen Sie die **SetDefaultDir** -Methode, um eine neue Standard Adressbuchcontainer herzustellen.</span><span class="sxs-lookup"><span data-stu-id="feb50-115">Clients and service providers call the **SetDefaultDir** method to establish a new default address book container.</span></span> <span data-ttu-id="feb50-116">Der standardmäßige Container ist der Container, den der Benutzer erhält im Adressbuch angezeigt wird, wenn das Adressbuch zum ersten Mal geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="feb50-116">The default container is the container that the user sees displayed in the address book when the address book is first opened.</span></span> <span data-ttu-id="feb50-117">**SetDefaultDir** speichert den Standardcontainer als Eintrag im Profil.</span><span class="sxs-lookup"><span data-stu-id="feb50-117">**SetDefaultDir** saves the default container as an entry in the profile.</span></span> <span data-ttu-id="feb50-118">Der Container bleibt unverändert bis einen weiteren Anruf zu **SetDefaultDir** in der gleichen Sitzung oder in einer anderen Sitzung erfolgt oder der Container wird entfernt.</span><span class="sxs-lookup"><span data-stu-id="feb50-118">The container remains as the default until either another call to **SetDefaultDir** is made in the same session or in another session, or the container is removed.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="feb50-119">Die [PR_AB_CHOOSE_DIRECTORY_AUTOMATICALLY](pidtagaddressbookchoosedirectoryautomatically-canonical-property.md) -Eigenschaft entspricht der Einstellung **automatisch wählen Sie** im Dialogfeld Optionen für das Adressbuch.</span><span class="sxs-lookup"><span data-stu-id="feb50-119">The [PR_AB_CHOOSE_DIRECTORY_AUTOMATICALLY](pidtagaddressbookchoosedirectoryautomatically-canonical-property.md) property corresponds to the **Choose automatically** setting in the Address Book Options dialog.</span></span> <span data-ttu-id="feb50-120">Wenn diese Eigenschaft im Abschnitt [IID_CAPONE_PROF](http://msdn.microsoft.com/library/281aabc3-9656-299c-4c78-7733dc71050a%28Office.15%29.aspx) Profile vorhanden ist und auf **true**festgelegt ist, im Adressbuch-Dialogfeld nicht mehr standardmäßig durch **SetDefaultDir**angegebene Container, jedoch wählt ein Adressbuch, von denen Microsoft Outlook annimmt. geeignet für den Kontext, in dem das Dialogfeld angezeigt wurde.</span><span class="sxs-lookup"><span data-stu-id="feb50-120">When this property exists in the [IID_CAPONE_PROF](http://msdn.microsoft.com/library/281aabc3-9656-299c-4c78-7733dc71050a%28Office.15%29.aspx) profile section and is set to **true**, the Address Book dialog no longer defaults to the container specified by **SetDefaultDir**, but chooses an address book that Microsoft Outlook considers appropriate for the context in which the dialog was displayed.</span></span> <span data-ttu-id="feb50-121">Beachten Sie, dass dies eine schlechte Erfahrung für Drittanbieter-adressbuchanbietern implementierte führen kann.</span><span class="sxs-lookup"><span data-stu-id="feb50-121">Note that this may result in a poor experience for third-party address book providers.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="feb50-122">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="feb50-122">MFCMAPI reference</span></span>

<span data-ttu-id="feb50-123">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="feb50-123">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="feb50-124">**Datei**</span><span class="sxs-lookup"><span data-stu-id="feb50-124">**File**</span></span>|<span data-ttu-id="feb50-125">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="feb50-125">**Function**</span></span>|<span data-ttu-id="feb50-126">**Comment**</span><span class="sxs-lookup"><span data-stu-id="feb50-126">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="feb50-127">Abcontdlg.cpp</span><span class="sxs-lookup"><span data-stu-id="feb50-127">Abcontdlg.cpp</span></span>  <br/> |<span data-ttu-id="feb50-128">CAbContDlg::OnSetDefaultDir</span><span class="sxs-lookup"><span data-stu-id="feb50-128">CAbContDlg::OnSetDefaultDir</span></span>  <br/> |<span data-ttu-id="feb50-129">MFCMAPI (engl.) verwendet die **SetDefaultDir** -Methode zum angegebenen Adressbuchcontainer eines machen.</span><span class="sxs-lookup"><span data-stu-id="feb50-129">MFCMAPI uses the **SetDefaultDir** method to make the specified address book container the default one.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="feb50-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="feb50-130">See also</span></span>



[<span data-ttu-id="feb50-131">IAddrBook::GetDefaultDir</span><span class="sxs-lookup"><span data-stu-id="feb50-131">IAddrBook::GetDefaultDir</span></span>](iaddrbook-getdefaultdir.md)
  
[<span data-ttu-id="feb50-132">IAddrBook::GetSearchPath</span><span class="sxs-lookup"><span data-stu-id="feb50-132">IAddrBook::GetSearchPath</span></span>](iaddrbook-getsearchpath.md)
  
[<span data-ttu-id="feb50-133">IMAPISession::Logoff</span><span class="sxs-lookup"><span data-stu-id="feb50-133">IMAPISession::Logoff</span></span>](imapisession-logoff.md)
  
[<span data-ttu-id="feb50-134">MAPILogonEx</span><span class="sxs-lookup"><span data-stu-id="feb50-134">MAPILogonEx</span></span>](mapilogonex.md)
  
[<span data-ttu-id="feb50-135">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="feb50-135">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)


[<span data-ttu-id="feb50-136">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="feb50-136">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

