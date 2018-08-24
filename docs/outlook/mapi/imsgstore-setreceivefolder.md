---
title: IMsgStoreSetReceiveFolder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.SetReceiveFolder
api_type:
- COM
ms.assetid: 469f0412-1343-47ce-b6e8-e0d5e56c29bb
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 4e2d4f76fe436fd18b439bbbb558b1169094b438
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589462"
---
# <a name="imsgstoresetreceivefolder"></a><span data-ttu-id="e242a-103">IMsgStore::SetReceiveFolder</span><span class="sxs-lookup"><span data-stu-id="e242a-103">IMsgStore::SetReceiveFolder</span></span>

  
  
<span data-ttu-id="e242a-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e242a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e242a-105">Stellt einen Ordner als Ziel für eingehende Nachrichten von einer bestimmten Nachrichtenklasse her.</span><span class="sxs-lookup"><span data-stu-id="e242a-105">Establishes a folder as the destination for incoming messages of a particular message class.</span></span>
  
```cpp
HRESULT SetReceiveFolder(
  LPSTR lpszMessageClass,
  ULONG ulFlags,
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="e242a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e242a-106">Parameters</span></span>

 <span data-ttu-id="e242a-107">_lpszMessageClass_</span><span class="sxs-lookup"><span data-stu-id="e242a-107">_lpszMessageClass_</span></span>
  
> <span data-ttu-id="e242a-108">[in] Empfangsordner für ein Zeiger auf die Nachrichtenklasse, die mit dem neuen zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="e242a-108">[in] A pointer to the message class that is to be associated with the new receive folder.</span></span> <span data-ttu-id="e242a-109">Wenn der _LpszMessageClass_ -Parameter auf NULL oder eine leere Zeichenfolge, **SetReceiveFolder** festgelegt werden standardmäßig Ordner für den Nachrichtenspeicher empfangen.</span><span class="sxs-lookup"><span data-stu-id="e242a-109">If the  _lpszMessageClass_ parameter is set to NULL or an empty string, **SetReceiveFolder** sets the default receive folder for the message store.</span></span> 
    
 <span data-ttu-id="e242a-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e242a-110">_ulFlags_</span></span>
  
> <span data-ttu-id="e242a-111">[in] Eine Bitmaske aus Flags, die den Typ des Texts in den übergebenen Zeichenfolgen steuert.</span><span class="sxs-lookup"><span data-stu-id="e242a-111">[in] A bitmask of flags that controls the type of the text in the passed-in strings.</span></span> <span data-ttu-id="e242a-112">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="e242a-112">The following flag can be set:</span></span>
    
<span data-ttu-id="e242a-113">PARAMETER MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="e242a-113">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="e242a-114">Die Klasse Meldungszeichenfolge ist im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="e242a-114">The message class string is in Unicode format.</span></span> <span data-ttu-id="e242a-115">Wenn die Option MAPI_UNICODE nicht festgelegt ist, wird die Zeichenfolge der Klasse im ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="e242a-115">If the MAPI_UNICODE flag is not set, the message class string is in ANSI format.</span></span>
    
 <span data-ttu-id="e242a-116">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="e242a-116">_cbEntryID_</span></span>
  
> <span data-ttu-id="e242a-117">[in] Die Byteanzahl von in die Eintrags-ID auf den durch den Parameter _LpEntryID_ verwiesen.</span><span class="sxs-lookup"><span data-stu-id="e242a-117">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="e242a-118">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="e242a-118">_lpEntryID_</span></span>
  
> <span data-ttu-id="e242a-119">[in] Ein Zeiger auf die Eintrags-ID des Ordners, der als den Empfangsordner einzurichten.</span><span class="sxs-lookup"><span data-stu-id="e242a-119">[in] A pointer to the entry identifier of the folder to establish as the receive folder.</span></span> <span data-ttu-id="e242a-120">Der _LpEntryID_ -Parameter auf NULL **SetReceiveFolder** ersetzt festgelegt ist empfangen die aktuelle Ordner mit der Nachrichtenspeicher Standard.</span><span class="sxs-lookup"><span data-stu-id="e242a-120">If the  _lpEntryID_ parameter is set to NULL, **SetReceiveFolder** replaces the current receive folder with the message store's default.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="e242a-121">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="e242a-121">Return value</span></span>

<span data-ttu-id="e242a-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="e242a-122">S_OK</span></span> 
  
> <span data-ttu-id="e242a-123">Eine Empfangsordner wurde erfolgreich hergestellt.</span><span class="sxs-lookup"><span data-stu-id="e242a-123">A receive folder was successfully established.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e242a-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e242a-124">Remarks</span></span>

<span data-ttu-id="e242a-125">Die **IMsgStore::SetReceiveFolder** -Methode legt oder ändert den Empfangsordner für eine bestimmte Nachrichtenklasse.</span><span class="sxs-lookup"><span data-stu-id="e242a-125">The **IMsgStore::SetReceiveFolder** method sets or changes the receive folder for a particular message class.</span></span> <span data-ttu-id="e242a-126">Mit **SetReceiveFolder**kann einen Client mithilfe von aufeinander folgenden Aufrufen angeben, ein anderes Empfangsordner für jede definierte Nachrichtenklasse oder angeben, dass eingehende Nachrichten für mehrere Nachrichtenklassen alle im gleichen Ordner wechseln.</span><span class="sxs-lookup"><span data-stu-id="e242a-126">With **SetReceiveFolder**, a client can, by using successive calls, specify a different receive folder for each defined message class or specify that incoming messages for multiple message classes all go to the same folder.</span></span> <span data-ttu-id="e242a-127">Ein Client kann beispielsweise eine eigene Klasse von Nachrichten in einem eigenen Ordner eintreffen haben.</span><span class="sxs-lookup"><span data-stu-id="e242a-127">For example, a client can have its own class of messages arrive in its own folder.</span></span> <span data-ttu-id="e242a-128">Eine Anwendung Fax kann festlegen, einen Ordner, in dem Speicheranbieter eingehende Faxe versetzt, und einen anderen Ordner, in dem der Anbieter Ausgehende Faxnachrichten versetzt.</span><span class="sxs-lookup"><span data-stu-id="e242a-128">A fax application can designate one folder in which the store provider puts incoming faxes and another folder in which the provider puts outgoing faxes.</span></span>
  
<span data-ttu-id="e242a-129">Wenn ein Fehler während des Aufrufs von **SetReceiveFolder**auftritt, bleibt die Einstellung für den empfangen unverändert.</span><span class="sxs-lookup"><span data-stu-id="e242a-129">If an error occurs during the call to **SetReceiveFolder**, the receive folder setting remains unchanged.</span></span> 
  
<span data-ttu-id="e242a-130">Wenn **SetReceiveFolder** ändert festgelegt die Einstellung für den Empfang mit _LpEntryID_ auf NULL wurde, was bedeutet, dass im Standardordner empfangen festgelegt werden sollte, **SetReceiveFolder** gibt S_OK zurück, auch wenn es wurde keine Einstellung für die angegebene Message-Klasse.</span><span class="sxs-lookup"><span data-stu-id="e242a-130">If **SetReceiveFolder** changes the receive folder setting with  _lpEntryID_ set to NULL, indicating that the default receive folder should be set, **SetReceiveFolder** returns S_OK even if there was no existing setting for the indicated message class.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="e242a-131">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="e242a-131">MFCMAPI reference</span></span>

<span data-ttu-id="e242a-132">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="e242a-132">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="e242a-133">**Datei**</span><span class="sxs-lookup"><span data-stu-id="e242a-133">**File**</span></span>|<span data-ttu-id="e242a-134">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="e242a-134">**Function**</span></span>|<span data-ttu-id="e242a-135">**Comment**</span><span class="sxs-lookup"><span data-stu-id="e242a-135">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e242a-136">MsgStoreDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="e242a-136">MsgStoreDlg.cpp</span></span>  <br/> |<span data-ttu-id="e242a-137">CMsgStoreDlg::OnSetReceiveFolder</span><span class="sxs-lookup"><span data-stu-id="e242a-137">CMsgStoreDlg::OnSetReceiveFolder</span></span>  <br/> |<span data-ttu-id="e242a-138">MFCMAPI (engl.) verwendet die **IMsgStore::SetReceiveFolder** -Methode, um einen Ordner als den Empfangsordner für eine bestimmte Nachrichtenklasse festzulegen.</span><span class="sxs-lookup"><span data-stu-id="e242a-138">MFCMAPI uses the **IMsgStore::SetReceiveFolder** method to set a folder as the receive folder for a particular message class.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e242a-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e242a-139">See also</span></span>



[<span data-ttu-id="e242a-140">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="e242a-140">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)


[<span data-ttu-id="e242a-141">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="e242a-141">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

