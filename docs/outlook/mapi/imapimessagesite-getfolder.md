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
ms.openlocfilehash: 24461099877af683109c8627eacd22a657d6e156
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430567"
---
# <a name="imapimessagesitegetfolder"></a><span data-ttu-id="a00cf-103">IMAPIMessageSite::GetFolder</span><span class="sxs-lookup"><span data-stu-id="a00cf-103">IMAPIMessageSite::GetFolder</span></span>

  
  
<span data-ttu-id="a00cf-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a00cf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a00cf-105">Gibt den Ordner zurück, in dem die aktuelle Nachricht erstellt oder geöffnet wurde, wenn ein solcher Ordner vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="a00cf-105">Returns the folder in which the current message was created or opened, if such a folder exists.</span></span> <span data-ttu-id="a00cf-106">Diese Methode gibt NULL im  _ppFolder-Parameter_ für eingebettete Nachrichten zurück, die nicht direkt in einem Ordner gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="a00cf-106">This method returns NULL in the  _ppFolder_ parameter for embedded messages, which are not stored directly in a folder.</span></span> 
  
```cpp
HRESULT GetFolder(
  LPMAPIFOLDER FAR * ppFolder
);
```

## <a name="parameters"></a><span data-ttu-id="a00cf-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="a00cf-107">Parameters</span></span>

 <span data-ttu-id="a00cf-108">_ppFolder_</span><span class="sxs-lookup"><span data-stu-id="a00cf-108">_ppFolder_</span></span>
  
> <span data-ttu-id="a00cf-109">[out] Ein Zeiger auf einen Zeiger auf den zurückgegebenen Ordner.</span><span class="sxs-lookup"><span data-stu-id="a00cf-109">[out] A pointer to a pointer to the returned folder.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a00cf-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a00cf-110">Return value</span></span>

<span data-ttu-id="a00cf-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="a00cf-111">S_OK</span></span> 
  
> <span data-ttu-id="a00cf-112">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="a00cf-112">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="a00cf-113">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="a00cf-113">S_FALSE</span></span> 
  
> <span data-ttu-id="a00cf-114">Für die Nachricht ist kein Ordner vorhanden.</span><span class="sxs-lookup"><span data-stu-id="a00cf-114">No folder exists for the message.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a00cf-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a00cf-115">Remarks</span></span>

<span data-ttu-id="a00cf-116">Eine Liste der Schnittstellen im Zusammenhang mit Formularservern finden Sie unter [MAPI Form Interfaces](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="a00cf-116">For a list of interfaces that are related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="a00cf-117">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="a00cf-117">MFCMAPI reference</span></span>

<span data-ttu-id="a00cf-118">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="a00cf-118">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="a00cf-119">**Datei**</span><span class="sxs-lookup"><span data-stu-id="a00cf-119">**File**</span></span>|<span data-ttu-id="a00cf-120">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="a00cf-120">**Function**</span></span>|<span data-ttu-id="a00cf-121">**Comment**</span><span class="sxs-lookup"><span data-stu-id="a00cf-121">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a00cf-122">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="a00cf-122">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="a00cf-123">CMyMAPIFormViewer::GetFolder</span><span class="sxs-lookup"><span data-stu-id="a00cf-123">CMyMAPIFormViewer::GetFolder</span></span>  <br/> |<span data-ttu-id="a00cf-124">MFCMAPI verwendet die **IMAPIMessageSite::GetFolder-Methode,** um den aktuell zwischengespeicherten Zeiger auf den angegebenen Ordner zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="a00cf-124">MFCMAPI uses the **IMAPIMessageSite::GetFolder** method to return the currently cached pointer to the specified folder.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a00cf-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a00cf-125">See also</span></span>



[<span data-ttu-id="a00cf-126">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a00cf-126">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="a00cf-127">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="a00cf-127">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="a00cf-128">MAPI-Formularschnittstellen</span><span class="sxs-lookup"><span data-stu-id="a00cf-128">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

