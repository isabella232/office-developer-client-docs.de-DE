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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 24461099877af683109c8627eacd22a657d6e156
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321385"
---
# <a name="imapimessagesitegetfolder"></a><span data-ttu-id="fed0d-103">IMAPIMessageSite::GetFolder</span><span class="sxs-lookup"><span data-stu-id="fed0d-103">IMAPIMessageSite::GetFolder</span></span>

  
  
<span data-ttu-id="fed0d-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fed0d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fed0d-105">Gibt den Ordner zurück, in dem die aktuelle Nachricht erstellt oder geöffnet wurde, wenn ein solcher Ordner vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="fed0d-105">Returns the folder in which the current message was created or opened, if such a folder exists.</span></span> <span data-ttu-id="fed0d-106">Diese Methode gibt NULL im _ppFolder_ -Parameter für eingebettete Nachrichten zurück, die nicht direkt in einem Ordner gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="fed0d-106">This method returns NULL in the  _ppFolder_ parameter for embedded messages, which are not stored directly in a folder.</span></span> 
  
```cpp
HRESULT GetFolder(
  LPMAPIFOLDER FAR * ppFolder
);
```

## <a name="parameters"></a><span data-ttu-id="fed0d-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="fed0d-107">Parameters</span></span>

 <span data-ttu-id="fed0d-108">_ppFolder_</span><span class="sxs-lookup"><span data-stu-id="fed0d-108">_ppFolder_</span></span>
  
> <span data-ttu-id="fed0d-109">Out Ein Zeiger auf einen Zeiger auf den zurückgegebenen Ordner.</span><span class="sxs-lookup"><span data-stu-id="fed0d-109">[out] A pointer to a pointer to the returned folder.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="fed0d-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fed0d-110">Return value</span></span>

<span data-ttu-id="fed0d-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="fed0d-111">S_OK</span></span> 
  
> <span data-ttu-id="fed0d-112">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="fed0d-112">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="fed0d-113">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="fed0d-113">S_FALSE</span></span> 
  
> <span data-ttu-id="fed0d-114">Für die Nachricht ist kein Ordner vorhanden.</span><span class="sxs-lookup"><span data-stu-id="fed0d-114">No folder exists for the message.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="fed0d-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fed0d-115">Remarks</span></span>

<span data-ttu-id="fed0d-116">Eine Liste der Schnittstellen im Zusammenhang mit Formular Servern finden Sie unter [MAPI-Formular Schnittstellen](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="fed0d-116">For a list of interfaces that are related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="fed0d-117">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="fed0d-117">MFCMAPI reference</span></span>

<span data-ttu-id="fed0d-118">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="fed0d-118">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="fed0d-119">**Datei**</span><span class="sxs-lookup"><span data-stu-id="fed0d-119">**File**</span></span>|<span data-ttu-id="fed0d-120">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="fed0d-120">**Function**</span></span>|<span data-ttu-id="fed0d-121">**Comment**</span><span class="sxs-lookup"><span data-stu-id="fed0d-121">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="fed0d-122">MyMAPIFormViewer. cpp</span><span class="sxs-lookup"><span data-stu-id="fed0d-122">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="fed0d-123">CMyMAPIFormViewer:: getFolder</span><span class="sxs-lookup"><span data-stu-id="fed0d-123">CMyMAPIFormViewer::GetFolder</span></span>  <br/> |<span data-ttu-id="fed0d-124">MFCMAPI verwendet die **IMAPIMessageSite:: GetFolder** -Methode, um den aktuell zwischengespeicherten Zeiger auf den angegebenen Ordner zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="fed0d-124">MFCMAPI uses the **IMAPIMessageSite::GetFolder** method to return the currently cached pointer to the specified folder.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fed0d-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fed0d-125">See also</span></span>



[<span data-ttu-id="fed0d-126">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="fed0d-126">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="fed0d-127">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="fed0d-127">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="fed0d-128">MAPI-Formular Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="fed0d-128">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

