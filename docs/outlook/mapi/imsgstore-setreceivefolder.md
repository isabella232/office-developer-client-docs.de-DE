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
ms.openlocfilehash: efa5d60098fd5f16328669249a8445a124d9878b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434088"
---
# <a name="imsgstoresetreceivefolder"></a><span data-ttu-id="0e615-103">IMsgStore::SetReceiveFolder</span><span class="sxs-lookup"><span data-stu-id="0e615-103">IMsgStore::SetReceiveFolder</span></span>

  
  
<span data-ttu-id="0e615-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0e615-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0e615-105">Richtet einen Ordner als Ziel für eingehende Nachrichten einer bestimmten Nachrichtenklasse ein.</span><span class="sxs-lookup"><span data-stu-id="0e615-105">Establishes a folder as the destination for incoming messages of a particular message class.</span></span>
  
```cpp
HRESULT SetReceiveFolder(
  LPSTR lpszMessageClass,
  ULONG ulFlags,
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="0e615-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0e615-106">Parameters</span></span>

 <span data-ttu-id="0e615-107">_lpszMessageClass_</span><span class="sxs-lookup"><span data-stu-id="0e615-107">_lpszMessageClass_</span></span>
  
> <span data-ttu-id="0e615-108">in Ein Zeiger auf die Nachrichtenklasse, die dem neuen Empfänger Ordner zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="0e615-108">[in] A pointer to the message class that is to be associated with the new receive folder.</span></span> <span data-ttu-id="0e615-109">Wenn der Parameter _lpszMessageClass_ auf NULL oder eine leere Zeichenfolge festgelegt ist, legt **SetReceiveFolder** den standardmäßigen Empfangsordner für den Nachrichtenspeicher fest.</span><span class="sxs-lookup"><span data-stu-id="0e615-109">If the  _lpszMessageClass_ parameter is set to NULL or an empty string, **SetReceiveFolder** sets the default receive folder for the message store.</span></span> 
    
 <span data-ttu-id="0e615-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="0e615-110">_ulFlags_</span></span>
  
> <span data-ttu-id="0e615-111">in Eine Bitmaske von Flags, die den Texttyp in den übergebenen Zeichenfolgen steuert.</span><span class="sxs-lookup"><span data-stu-id="0e615-111">[in] A bitmask of flags that controls the type of the text in the passed-in strings.</span></span> <span data-ttu-id="0e615-112">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="0e615-112">The following flag can be set:</span></span>
    
<span data-ttu-id="0e615-113">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="0e615-113">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="0e615-114">Die Zeichenfolge der Nachrichtenklasse ist im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="0e615-114">The message class string is in Unicode format.</span></span> <span data-ttu-id="0e615-115">Wenn das MAPI_UNICODE-Flag nicht festgelegt ist, ist die Zeichenfolge der Nachrichtenklasse im ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="0e615-115">If the MAPI_UNICODE flag is not set, the message class string is in ANSI format.</span></span>
    
 <span data-ttu-id="0e615-116">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="0e615-116">_cbEntryID_</span></span>
  
> <span data-ttu-id="0e615-117">in Die Anzahl der Bytes in der Eintrags-ID, auf die durch den _lpEntryID_ -Parameter verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="0e615-117">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="0e615-118">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="0e615-118">_lpEntryID_</span></span>
  
> <span data-ttu-id="0e615-119">in Ein Zeiger auf die Eintrags-ID des Ordners, der als Empfänger Ordner eingerichtet werden soll.</span><span class="sxs-lookup"><span data-stu-id="0e615-119">[in] A pointer to the entry identifier of the folder to establish as the receive folder.</span></span> <span data-ttu-id="0e615-120">Wenn der Parameter _lpEntryID_ auf NULL festgelegt ist, ersetzt **SetReceiveFolder** den aktuellen Empfänger Ordner durch den Standardwert des Nachrichtenspeichers.</span><span class="sxs-lookup"><span data-stu-id="0e615-120">If the  _lpEntryID_ parameter is set to NULL, **SetReceiveFolder** replaces the current receive folder with the message store's default.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="0e615-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0e615-121">Return value</span></span>

<span data-ttu-id="0e615-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="0e615-122">S_OK</span></span> 
  
> <span data-ttu-id="0e615-123">Ein Empfangsordner wurde erfolgreich eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="0e615-123">A receive folder was successfully established.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0e615-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0e615-124">Remarks</span></span>

<span data-ttu-id="0e615-125">Mit der **IMsgStore:: SetReceiveFolder** -Methode wird der Empfangsordner für eine bestimmte Nachrichtenklasse festgelegt oder geändert.</span><span class="sxs-lookup"><span data-stu-id="0e615-125">The **IMsgStore::SetReceiveFolder** method sets or changes the receive folder for a particular message class.</span></span> <span data-ttu-id="0e615-126">Mit **SetReceiveFolder**kann ein Client mithilfe aufeinanderfolgender Aufrufe einen anderen Empfangsordner für jede definierte Nachrichtenklasse angeben oder angeben, dass eingehende Nachrichten für mehrere Nachrichtenklassen in denselben Ordner gelangen.</span><span class="sxs-lookup"><span data-stu-id="0e615-126">With **SetReceiveFolder**, a client can, by using successive calls, specify a different receive folder for each defined message class or specify that incoming messages for multiple message classes all go to the same folder.</span></span> <span data-ttu-id="0e615-127">Beispielsweise kann ein Client eine eigene Klasse von Nachrichten in seinem eigenen Ordner eingehen lassen.</span><span class="sxs-lookup"><span data-stu-id="0e615-127">For example, a client can have its own class of messages arrive in its own folder.</span></span> <span data-ttu-id="0e615-128">Eine Fax-Anwendung kann einen Ordner festlegen, in dem der Informationsspeicher Anbieter eingehende Faxe eingibt, und einen anderen Ordner, in dem der Anbieter ausgehende Faxe platziert.</span><span class="sxs-lookup"><span data-stu-id="0e615-128">A fax application can designate one folder in which the store provider puts incoming faxes and another folder in which the provider puts outgoing faxes.</span></span>
  
<span data-ttu-id="0e615-129">Wenn während des Anrufs an **SetReceiveFolder**ein Fehler auftritt, bleibt die Einstellung für den Empfangsordner unverändert.</span><span class="sxs-lookup"><span data-stu-id="0e615-129">If an error occurs during the call to **SetReceiveFolder**, the receive folder setting remains unchanged.</span></span> 
  
<span data-ttu-id="0e615-130">Wenn **SetReceiveFolder** die Einstellung für den Empfänger Ordner mit _lpEntryID_ auf NULL festgelegt ändert, was darauf hinweist, dass der standardmäßige Empfangsordner festgelegt werden soll, gibt **SetReceiveFolder** S_OK zurück, auch wenn keine Einstellung für die angegebene Nachrichtenklasse.</span><span class="sxs-lookup"><span data-stu-id="0e615-130">If **SetReceiveFolder** changes the receive folder setting with  _lpEntryID_ set to NULL, indicating that the default receive folder should be set, **SetReceiveFolder** returns S_OK even if there was no existing setting for the indicated message class.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="0e615-131">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="0e615-131">MFCMAPI reference</span></span>

<span data-ttu-id="0e615-132">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="0e615-132">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="0e615-133">**Datei**</span><span class="sxs-lookup"><span data-stu-id="0e615-133">**File**</span></span>|<span data-ttu-id="0e615-134">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="0e615-134">**Function**</span></span>|<span data-ttu-id="0e615-135">**Comment**</span><span class="sxs-lookup"><span data-stu-id="0e615-135">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="0e615-136">MsgStoreDlg. cpp</span><span class="sxs-lookup"><span data-stu-id="0e615-136">MsgStoreDlg.cpp</span></span>  <br/> |<span data-ttu-id="0e615-137">CMsgStoreDlg:: OnSetReceiveFolder</span><span class="sxs-lookup"><span data-stu-id="0e615-137">CMsgStoreDlg::OnSetReceiveFolder</span></span>  <br/> |<span data-ttu-id="0e615-138">MFCMAPI verwendet die **IMsgStore:: SetReceiveFolder** -Methode, um einen Ordner als Empfangsordner für eine bestimmte Nachrichtenklasse festzulegen.</span><span class="sxs-lookup"><span data-stu-id="0e615-138">MFCMAPI uses the **IMsgStore::SetReceiveFolder** method to set a folder as the receive folder for a particular message class.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0e615-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0e615-139">See also</span></span>



[<span data-ttu-id="0e615-140">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="0e615-140">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)


[<span data-ttu-id="0e615-141">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="0e615-141">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

