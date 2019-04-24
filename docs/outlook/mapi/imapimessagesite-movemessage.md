---
title: IMAPIMessageSiteMoveMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.MoveMessage
api_type:
- COM
ms.assetid: cd4d7b11-fad0-4f05-a99e-9567abcab45c
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: c68e4fbda661a119416918a2c35d1780f1deccda
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321365"
---
# <a name="imapimessagesitemovemessage"></a><span data-ttu-id="b3d0b-103">IMAPIMessageSite::MoveMessage</span><span class="sxs-lookup"><span data-stu-id="b3d0b-103">IMAPIMessageSite::MoveMessage</span></span>

  
  
<span data-ttu-id="b3d0b-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b3d0b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b3d0b-105">Verschiebt die aktuelle Nachricht in einen Ordner.</span><span class="sxs-lookup"><span data-stu-id="b3d0b-105">Moves the current message to a folder.</span></span>
  
```cpp
HRESULT MoveMessage(
  LPFOLDER pFolderDestination,
  LPMAPIVIEWCONTEXT pViewContext,
  LPCRECT prcPosRect
);
```

## <a name="parameters"></a><span data-ttu-id="b3d0b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b3d0b-106">Parameters</span></span>

 <span data-ttu-id="b3d0b-107">_pFolderDestination_</span><span class="sxs-lookup"><span data-stu-id="b3d0b-107">_pFolderDestination_</span></span>
  
> <span data-ttu-id="b3d0b-108">in Ein Zeiger auf den Ordner, in den die Nachricht verschoben werden soll.</span><span class="sxs-lookup"><span data-stu-id="b3d0b-108">[in] A pointer to the folder where the message is to be moved.</span></span>
    
 <span data-ttu-id="b3d0b-109">_pViewContext_</span><span class="sxs-lookup"><span data-stu-id="b3d0b-109">_pViewContext_</span></span>
  
> <span data-ttu-id="b3d0b-110">in Ein Zeiger auf ein View-Kontextobjekt.</span><span class="sxs-lookup"><span data-stu-id="b3d0b-110">[in] A pointer to a view context object.</span></span>
    
 <span data-ttu-id="b3d0b-111">_prcPosRect_</span><span class="sxs-lookup"><span data-stu-id="b3d0b-111">_prcPosRect_</span></span>
  
> <span data-ttu-id="b3d0b-112">in Ein Zeiger auf eine [Rect](https://msdn.microsoft.com/library/dd162897%28VS.85%29.aspx) -Struktur, die die Größe und Position des aktuellen Formulars enthält.</span><span class="sxs-lookup"><span data-stu-id="b3d0b-112">[in] A pointer to a [RECT](https://msdn.microsoft.com/library/dd162897%28VS.85%29.aspx) structure that contains the current form's window size and position.</span></span> <span data-ttu-id="b3d0b-113">Das nächste Formular wird auch dieses Fensterrechteck verwendet.</span><span class="sxs-lookup"><span data-stu-id="b3d0b-113">The next form displayed also uses this window rectangle.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="b3d0b-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b3d0b-114">Return value</span></span>

<span data-ttu-id="b3d0b-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="b3d0b-115">S_OK</span></span> 
  
> <span data-ttu-id="b3d0b-116">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="b3d0b-116">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="b3d0b-117">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="b3d0b-117">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="b3d0b-118">Der Vorgang wird von dieser Nachrichtenwebsite nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b3d0b-118">The operation is not supported by this message site.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b3d0b-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b3d0b-119">Remarks</span></span>

<span data-ttu-id="b3d0b-120">Formularobjekte rufen die **IMAPIMessageSite:: MoveMessage** -Methode auf, um die aktuelle Nachricht in einen neuen Ordner zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="b3d0b-120">Form objects call the **IMAPIMessageSite::MoveMessage** method to move the current message to a new folder.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="b3d0b-121">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="b3d0b-121">Notes to implementers</span></span>

<span data-ttu-id="b3d0b-122">Die Implementierung von **MoveMessage** durch einen Formular Betrachter muss die [IMAPIViewContext:: ActivateNext](imapiviewcontext-activatenext.md) -Methode aufrufen und das VCDIR_MOVE-Flag übergeben, bevor die Nachricht tatsächlich in einen neuen Ordner bewegt wird.</span><span class="sxs-lookup"><span data-stu-id="b3d0b-122">A form viewer's implementation of **MoveMessage** must call the [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md) method, passing the VCDIR_MOVE flag, before actually moving the message to a new folder.</span></span> <span data-ttu-id="b3d0b-123">Rufen Sie die Windows- [GetWindowRect](https://msdn.microsoft.com/library/ms633519) -Funktion auf, um die vom Fenster eines Formulars verwendete **Rect** -Struktur abzurufen.</span><span class="sxs-lookup"><span data-stu-id="b3d0b-123">To obtain the **RECT** structure used by a form's window, call the Windows [GetWindowRect](https://msdn.microsoft.com/library/ms633519) function.</span></span> 
  
<span data-ttu-id="b3d0b-124">Eine Liste der Schnittstellen im Zusammenhang mit Formular Servern finden Sie unter [MAPI-Formular Schnittstellen](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="b3d0b-124">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="b3d0b-125">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="b3d0b-125">Notes to callers</span></span>

<span data-ttu-id="b3d0b-126">Nach der Rückgabe von **MoveMessage**müssen Formulare nach einer aktuellen Nachricht suchen und sich dann selbst entlassen, wenn keine vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="b3d0b-126">Following the return of **MoveMessage**, forms must check for a current message and then dismiss themselves if none exists.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="b3d0b-127">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="b3d0b-127">MFCMAPI reference</span></span>

<span data-ttu-id="b3d0b-128">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="b3d0b-128">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="b3d0b-129">**Datei**</span><span class="sxs-lookup"><span data-stu-id="b3d0b-129">**File**</span></span>|<span data-ttu-id="b3d0b-130">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="b3d0b-130">**Function**</span></span>|<span data-ttu-id="b3d0b-131">**Comment**</span><span class="sxs-lookup"><span data-stu-id="b3d0b-131">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b3d0b-132">MyMAPIFormViewer. cpp</span><span class="sxs-lookup"><span data-stu-id="b3d0b-132">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="b3d0b-133">CMyMAPIFormViewer:: MoveMessage</span><span class="sxs-lookup"><span data-stu-id="b3d0b-133">CMyMAPIFormViewer::MoveMessage</span></span>  <br/> |<span data-ttu-id="b3d0b-134">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="b3d0b-134">Not implemented.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b3d0b-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b3d0b-135">See also</span></span>



[<span data-ttu-id="b3d0b-136">IMAPIViewContext::ActivateNext</span><span class="sxs-lookup"><span data-stu-id="b3d0b-136">IMAPIViewContext::ActivateNext</span></span>](imapiviewcontext-activatenext.md)
  
[<span data-ttu-id="b3d0b-137">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b3d0b-137">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="b3d0b-138">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="b3d0b-138">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="b3d0b-139">MAPI-Formular Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="b3d0b-139">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

