---
title: IMAPIMessageSiteGetFolder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.GetFolder
api_type:
- COM
ms.assetid: 9f4b4147-ed98-47cb-a799-ddf028f8e826
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 78fb610c5afc3cac4f6de84240f734e5ae196110
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565543"
---
# <a name="imapimessagesitegetfolder"></a><span data-ttu-id="9e115-103">IMAPIMessageSite::GetFolder</span><span class="sxs-lookup"><span data-stu-id="9e115-103">IMAPIMessageSite::GetFolder</span></span>

  
  
<span data-ttu-id="9e115-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9e115-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9e115-105">Der Ordner, in dem die aktuelle Nachricht geöffnet oder erstellt wurde, zurückgegeben, wenn solche ein Ordner vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="9e115-105">Returns the folder in which the current message was created or opened, if such a folder exists.</span></span> <span data-ttu-id="9e115-106">Diese Methode gibt NULL zurück, in der _PpFolder_ -Parameter für eingebettete Nachrichten, die nicht direkt in einem Ordner gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="9e115-106">This method returns NULL in the  _ppFolder_ parameter for embedded messages, which are not stored directly in a folder.</span></span> 
  
```cpp
HRESULT GetFolder(
  LPMAPIFOLDER FAR * ppFolder
);
```

## <a name="parameters"></a><span data-ttu-id="9e115-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="9e115-107">Parameters</span></span>

 <span data-ttu-id="9e115-108">_ppFolder_</span><span class="sxs-lookup"><span data-stu-id="9e115-108">_ppFolder_</span></span>
  
> <span data-ttu-id="9e115-109">[out] Ein Zeiger auf einen Zeiger auf den zurückgegebenen Ordner.</span><span class="sxs-lookup"><span data-stu-id="9e115-109">[out] A pointer to a pointer to the returned folder.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="9e115-110">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="9e115-110">Return value</span></span>

<span data-ttu-id="9e115-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="9e115-111">S_OK</span></span> 
  
> <span data-ttu-id="9e115-112">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="9e115-112">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="9e115-113">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="9e115-113">S_FALSE</span></span> 
  
> <span data-ttu-id="9e115-114">Kein Ordner für die Nachricht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="9e115-114">No folder exists for the message.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9e115-115">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="9e115-115">Remarks</span></span>

<span data-ttu-id="9e115-116">Eine Liste der Schnittstellen im Zusammenhang mit Formular Servern, finden Sie unter [MAPI-Formulars Schnittstellen](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="9e115-116">For a list of interfaces that are related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="9e115-117">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="9e115-117">MFCMAPI reference</span></span>

<span data-ttu-id="9e115-118">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="9e115-118">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="9e115-119">**Datei**</span><span class="sxs-lookup"><span data-stu-id="9e115-119">**File**</span></span>|<span data-ttu-id="9e115-120">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="9e115-120">**Function**</span></span>|<span data-ttu-id="9e115-121">**Comment**</span><span class="sxs-lookup"><span data-stu-id="9e115-121">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="9e115-122">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="9e115-122">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="9e115-123">CMyMAPIFormViewer::GetFolder</span><span class="sxs-lookup"><span data-stu-id="9e115-123">CMyMAPIFormViewer::GetFolder</span></span>  <br/> |<span data-ttu-id="9e115-124">MFCMAPI (engl.) wird die **IMAPIMessageSite::GetFolder** -Methode verwendet, um die aktuell zwischengespeicherten Zeiger auf den angegebenen Ordner zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="9e115-124">MFCMAPI uses the **IMAPIMessageSite::GetFolder** method to return the currently cached pointer to the specified folder.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9e115-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9e115-125">See also</span></span>



[<span data-ttu-id="9e115-126">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9e115-126">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="9e115-127">MFCMAPI als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="9e115-127">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="9e115-128">MAPI-Formularoberflächen</span><span class="sxs-lookup"><span data-stu-id="9e115-128">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

