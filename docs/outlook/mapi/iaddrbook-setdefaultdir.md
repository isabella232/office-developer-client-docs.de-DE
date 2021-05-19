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
ms.openlocfilehash: 3ab01f189734ac30b4c027f4e5596c88031b5f99
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341699"
---
# <a name="iaddrbooksetdefaultdir"></a><span data-ttu-id="ebe33-103">IAddrBook::SetDefaultDir</span><span class="sxs-lookup"><span data-stu-id="ebe33-103">IAddrBook::SetDefaultDir</span></span>

  
  
<span data-ttu-id="ebe33-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ebe33-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ebe33-105">Richtet den angegebenen Container als Standard-Adressbuchcontainer ein.</span><span class="sxs-lookup"><span data-stu-id="ebe33-105">Establishes the specified container as the default address book container.</span></span>
  
```cpp
HRESULT SetDefaultDir(
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="ebe33-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ebe33-106">Parameters</span></span>

 <span data-ttu-id="ebe33-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="ebe33-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="ebe33-108">[in] Die Byteanzahl im Eintragsbezeichner, auf den der  _lpEntryID-Parameter_ verweist.</span><span class="sxs-lookup"><span data-stu-id="ebe33-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="ebe33-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="ebe33-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="ebe33-110">[in] Ein Zeiger auf die Eintrags-ID des Standard-Adressbuchcontainers.</span><span class="sxs-lookup"><span data-stu-id="ebe33-110">[in] A pointer to the entry identifier of the default address book container.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ebe33-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ebe33-111">Return value</span></span>

<span data-ttu-id="ebe33-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="ebe33-112">S_OK</span></span> 
  
> <span data-ttu-id="ebe33-113">Der Standard-Adressbuchcontainer wurde erfolgreich festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ebe33-113">The default address book container was successfully set.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ebe33-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ebe33-114">Remarks</span></span>

<span data-ttu-id="ebe33-115">Clients und Dienstanbieter rufen die **SetDefaultDir-Methode** auf, um einen neuen Standard-Adressbuchcontainer zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="ebe33-115">Clients and service providers call the **SetDefaultDir** method to establish a new default address book container.</span></span> <span data-ttu-id="ebe33-116">Der Standardcontainer ist der Container, den der Benutzer beim ersten Öffnen des Adressbuchs im Adressbuch angezeigt sieht.</span><span class="sxs-lookup"><span data-stu-id="ebe33-116">The default container is the container that the user sees displayed in the address book when the address book is first opened.</span></span> <span data-ttu-id="ebe33-117">**SetDefaultDir** speichert den Standardcontainer als Eintrag im Profil.</span><span class="sxs-lookup"><span data-stu-id="ebe33-117">**SetDefaultDir** saves the default container as an entry in the profile.</span></span> <span data-ttu-id="ebe33-118">Der Container bleibt die Standardeinstellung, bis ein anderer Aufruf von **SetDefaultDir** in derselben Sitzung oder in einer anderen Sitzung erfolgt oder der Container entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="ebe33-118">The container remains as the default until either another call to **SetDefaultDir** is made in the same session or in another session, or the container is removed.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="ebe33-119">Die [PR_AB_CHOOSE_DIRECTORY_AUTOMATICALLY](pidtagaddressbookchoosedirectoryautomatically-canonical-property.md) entspricht der Einstellung **Automatisch** auswählen im Dialogfeld Adressbuchoptionen.</span><span class="sxs-lookup"><span data-stu-id="ebe33-119">The [PR_AB_CHOOSE_DIRECTORY_AUTOMATICALLY](pidtagaddressbookchoosedirectoryautomatically-canonical-property.md) property corresponds to the **Choose automatically** setting in the Address Book Options dialog.</span></span> <span data-ttu-id="ebe33-120">Wenn diese Eigenschaft im Abschnitt [IID_CAPONE_PROF-Profil](https://msdn.microsoft.com/library/281aabc3-9656-299c-4c78-7733dc71050a%28Office.15%29.aspx) vorhanden ist und auf **true** festgelegt ist, wird im Adressbuchdialogfeld nicht mehr standardmäßig der von **SetDefaultDir** angegebene Container verwendet, sondern ein Adressbuch ausgewählt, das von Microsoft Outlook für den Kontext geeignet erachtet wird, in dem das Dialogfeld angezeigt wurde.</span><span class="sxs-lookup"><span data-stu-id="ebe33-120">When this property exists in the [IID_CAPONE_PROF](https://msdn.microsoft.com/library/281aabc3-9656-299c-4c78-7733dc71050a%28Office.15%29.aspx) profile section and is set to **true**, the Address Book dialog no longer defaults to the container specified by **SetDefaultDir**, but chooses an address book that Microsoft Outlook considers appropriate for the context in which the dialog was displayed.</span></span> <span data-ttu-id="ebe33-121">Beachten Sie, dass dies zu einer schlechten Erfahrung für Adressbuchanbieter von Drittanbietern führen kann.</span><span class="sxs-lookup"><span data-stu-id="ebe33-121">Note that this may result in a poor experience for third-party address book providers.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="ebe33-122">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="ebe33-122">MFCMAPI reference</span></span>

<span data-ttu-id="ebe33-123">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="ebe33-123">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="ebe33-124">**Datei**</span><span class="sxs-lookup"><span data-stu-id="ebe33-124">**File**</span></span>|<span data-ttu-id="ebe33-125">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="ebe33-125">**Function**</span></span>|<span data-ttu-id="ebe33-126">**Comment**</span><span class="sxs-lookup"><span data-stu-id="ebe33-126">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ebe33-127">Abcontdlg.cpp</span><span class="sxs-lookup"><span data-stu-id="ebe33-127">Abcontdlg.cpp</span></span>  <br/> |<span data-ttu-id="ebe33-128">CAbContDlg::OnSetDefaultDir</span><span class="sxs-lookup"><span data-stu-id="ebe33-128">CAbContDlg::OnSetDefaultDir</span></span>  <br/> |<span data-ttu-id="ebe33-129">MFCMAPI verwendet die **SetDefaultDir-Methode,** um den angegebenen Adressbuchcontainer zum Standardcontainer zu machen.</span><span class="sxs-lookup"><span data-stu-id="ebe33-129">MFCMAPI uses the **SetDefaultDir** method to make the specified address book container the default one.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ebe33-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ebe33-130">See also</span></span>



[<span data-ttu-id="ebe33-131">IAddrBook::GetDefaultDir</span><span class="sxs-lookup"><span data-stu-id="ebe33-131">IAddrBook::GetDefaultDir</span></span>](iaddrbook-getdefaultdir.md)
  
[<span data-ttu-id="ebe33-132">IAddrBook::GetSearchPath</span><span class="sxs-lookup"><span data-stu-id="ebe33-132">IAddrBook::GetSearchPath</span></span>](iaddrbook-getsearchpath.md)
  
[<span data-ttu-id="ebe33-133">IMAPISession::Logoff</span><span class="sxs-lookup"><span data-stu-id="ebe33-133">IMAPISession::Logoff</span></span>](imapisession-logoff.md)
  
[<span data-ttu-id="ebe33-134">MAPILogonEx</span><span class="sxs-lookup"><span data-stu-id="ebe33-134">MAPILogonEx</span></span>](mapilogonex.md)
  
[<span data-ttu-id="ebe33-135">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="ebe33-135">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)


[<span data-ttu-id="ebe33-136">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="ebe33-136">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

