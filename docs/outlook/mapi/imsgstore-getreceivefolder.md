---
title: IMsgStoreGetReceiveFolder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.GetReceiveFolder
api_type:
- COM
ms.assetid: ccd9d623-a3cb-4e66-9649-78c3887cb726
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: f58bd8499b63bcd526906f78143b76092f194cb4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792619"
---
# <a name="imsgstoregetreceivefolder"></a><span data-ttu-id="39de1-103">IMsgStore::GetReceiveFolder</span><span class="sxs-lookup"><span data-stu-id="39de1-103">IMsgStore::GetReceiveFolder</span></span>

  
  
<span data-ttu-id="39de1-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="39de1-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="39de1-105">Ruft den Ordner, der als Ziel für eingehende Nachrichten von einer angegebenen Nachrichtenklasse oder als Standard Empfangsordner für den Nachrichtenspeicher eingerichtet wurde.</span><span class="sxs-lookup"><span data-stu-id="39de1-105">Obtains the folder that was established as the destination for incoming messages of a specified message class or as the default receive folder for the message store.</span></span>
  
```cpp
HRESULT GetReceiveFolder(
  LPSTR lpszMessageClass,
  ULONG ulFlags,
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID,
  LPSTR FAR * lppszExplicitClass
);
```

## <a name="parameters"></a><span data-ttu-id="39de1-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="39de1-106">Parameters</span></span>

 <span data-ttu-id="39de1-107">_lpszMessageClass_</span><span class="sxs-lookup"><span data-stu-id="39de1-107">_lpszMessageClass_</span></span>
  
> <span data-ttu-id="39de1-108">[in] Ein Zeiger auf eine Nachrichtenklasse, die ein Empfangsordner zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="39de1-108">[in] A pointer to a message class that is associated with a receive folder.</span></span> <span data-ttu-id="39de1-109">Wenn der Parameter _LpszMessageClass_ gibt NULL oder eine leere Zeichenfolge, **GetReceiveFolder** festgelegt ist die Standardeinstellung Ordner für den Nachrichtenspeicher empfangen.</span><span class="sxs-lookup"><span data-stu-id="39de1-109">If the  _lpszMessageClass_ parameter is set to NULL or an empty string, **GetReceiveFolder** returns the default receive folder for the message store.</span></span> 
    
 <span data-ttu-id="39de1-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="39de1-110">_ulFlags_</span></span>
  
> <span data-ttu-id="39de1-111">[in] Eine Bitmaske aus Flags, die den Typ der übergebenen und zurückgegebenen Zeichenfolgen steuert.</span><span class="sxs-lookup"><span data-stu-id="39de1-111">[in] A bitmask of flags that controls the type of the passed-in and returned strings.</span></span> <span data-ttu-id="39de1-112">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="39de1-112">The following flag can be set:</span></span>
    
<span data-ttu-id="39de1-113">PARAMETER MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="39de1-113">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="39de1-114">Die Klasse Meldungszeichenfolge ist im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="39de1-114">The message class string is in Unicode format.</span></span> <span data-ttu-id="39de1-115">Wenn die Option MAPI_UNICODE nicht festgelegt ist, wird die Zeichenfolge der Klasse im ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="39de1-115">If the MAPI_UNICODE flag is not set, the message class string is in ANSI format.</span></span>
    
 <span data-ttu-id="39de1-116">_lpcbEntryID_</span><span class="sxs-lookup"><span data-stu-id="39de1-116">_lpcbEntryID_</span></span>
  
> <span data-ttu-id="39de1-117">[out] Ein Zeiger auf die Byteanzahl von in die Eintrags-ID auf den durch den Parameter _LppEntryID_ verwiesen.</span><span class="sxs-lookup"><span data-stu-id="39de1-117">[out] A pointer to the byte count in the entry identifier pointed to by the  _lppEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="39de1-118">_lppEntryID_</span><span class="sxs-lookup"><span data-stu-id="39de1-118">_lppEntryID_</span></span>
  
> <span data-ttu-id="39de1-119">[out] Ein Zeiger auf einen Zeiger auf die Eintrags-ID für die angeforderte Empfangsordner.</span><span class="sxs-lookup"><span data-stu-id="39de1-119">[out] A pointer to a pointer to the entry identifier for the requested receive folder.</span></span>
    
 <span data-ttu-id="39de1-120">_lppszExplicitClass_</span><span class="sxs-lookup"><span data-stu-id="39de1-120">_lppszExplicitClass_</span></span>
  
> <span data-ttu-id="39de1-121">[out] Ein Zeiger auf einen Zeiger auf die Nachrichtenklasse, die explizit als festlegt seine Empfangsordner im Ordner, die auf die _LppEntryID_zeigt.</span><span class="sxs-lookup"><span data-stu-id="39de1-121">[out] A pointer to a pointer to the message class that explicitly sets as its receive folder the folder pointed to by  _lppEntryID_.</span></span> <span data-ttu-id="39de1-122">Diese Nachrichtenklasse sollte entweder der Klasse in der _LpszMessageClass_ -Parameter oder dieser Klasse eine Basisklasse identisch sein.</span><span class="sxs-lookup"><span data-stu-id="39de1-122">This message class should either be the same as the class in the  _lpszMessageClass_ parameter, or a base class of that class.</span></span> <span data-ttu-id="39de1-123">Übergeben von NULL gibt an, dass der Ordner, auf die _LppEntryID_ zeigt den standardmäßigen Ordner für den Nachrichtenspeicher empfangen.</span><span class="sxs-lookup"><span data-stu-id="39de1-123">Passing NULL indicates that the folder pointed to by  _lppEntryID_ is the default receive folder for the message store.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="39de1-124">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="39de1-124">Return value</span></span>

<span data-ttu-id="39de1-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="39de1-125">S_OK</span></span> 
  
> <span data-ttu-id="39de1-126">Der Empfangsordner wurde erfolgreich zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="39de1-126">The receive folder was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="39de1-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="39de1-127">Remarks</span></span>

<span data-ttu-id="39de1-128">Die **IMsgStore::GetReceiveFolder** -Methode ruft die Eintrags-ID eines Ordners empfangen, einen Ordner, der zum Empfangen eingehender Nachrichten von einer bestimmten Nachrichtenklasse festgelegt.</span><span class="sxs-lookup"><span data-stu-id="39de1-128">The **IMsgStore::GetReceiveFolder** method obtains the entry identifier of a receive folder, a folder designated to receive incoming messages of a particular message class.</span></span> <span data-ttu-id="39de1-129">Anrufer können eine Nachrichtenklasse oder NULL in der _LpszMessageClass_ -Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="39de1-129">Callers can specify a message class or NULL in the  _lpszMessageClass_ parameter.</span></span> <span data-ttu-id="39de1-130">Wenn _LpszMessageClass_ NULL ist, gibt **GetReceiveFolder** die folgenden Werte zurück:</span><span class="sxs-lookup"><span data-stu-id="39de1-130">If  _lpszMessageClass_ is NULL, **GetReceiveFolder** returns the following values:</span></span> 
  
- <span data-ttu-id="39de1-131">In _LppszExplicitClass_auf die der Name des ersten-Basisklasse der Nachrichtenklasse _LpszMessageClass_ , die explizit eine Empfangsordner festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="39de1-131">In  _lppszExplicitClass_, the name of the first base class of the message class pointed to by  _lpszMessageClass_ that does explicitly set a receive folder.</span></span> 
    
- <span data-ttu-id="39de1-132">In _LppEntryID_auf das die Eintrags-ID des Ordners empfangen der Basisklasse durch den Parameter _LppszExplicitClass_ .</span><span class="sxs-lookup"><span data-stu-id="39de1-132">In  _lppEntryID_, the entry identifier of the receive folder for the base class pointed to by the  _lppszExplicitClass_ parameter.</span></span> 
    
<span data-ttu-id="39de1-133">Nehmen wir beispielsweise bei den Empfangsordner der Nachrichtenklasse IPM **. Hinweis** festgelegt wurde dem Eintrag Bezeichner der Posteingang und **GetReceiveFolder** aufgerufen, mit dem Inhalt des _LpszMessageClass_ auf **IPM festgelegt. Note.Phone**.</span><span class="sxs-lookup"><span data-stu-id="39de1-133">For example, suppose the receive folder of the message class **IPM.Note** has been set to the entry identifier of the Inbox and **GetReceiveFolder** is called with the contents of  _lpszMessageClass_ set to **IPM.Note.Phone**.</span></span> <span data-ttu-id="39de1-134">Wenn **IPM. Note.Phone** haben eine explizite erhält keine Ordner Set, **GetReceiveFolder** gibt die Eintrags-ID des Posteingangs in _LppEntryID_ und **IPM. Hinweis** in _LppszExplicitClass_.</span><span class="sxs-lookup"><span data-stu-id="39de1-134">If **IPM.Note.Phone** does not have an explicit receive folder set, **GetReceiveFolder** returns the entry identifier of the Inbox in  _lppEntryID_ and **IPM.Note** in  _lppszExplicitClass_.</span></span>
  
<span data-ttu-id="39de1-135">Wenn der Client **GetReceiveFolder** für eine Nachrichtenklasse ruft und eine Empfangsordner für die Nachrichtenklasse nicht festgelegt wurde, _LppszExplicitClass_ ist entweder eine leere Zeichenfolge, eine Zeichenfolge im Unicode-Format oder eine Zeichenfolge im ANSI-Format, je nachdem, ob die Client legen Sie die Option MAPI_UNICODE im _UlFlags_ -Parameter.</span><span class="sxs-lookup"><span data-stu-id="39de1-135">If the client calls **GetReceiveFolder** for a message class and has not set a receive folder for that message class,  _lppszExplicitClass_ is either a zero-length string, a string in Unicode format, or a string in ANSI format depending on whether the client set the MAPI_UNICODE flag in the  _ulFlags_ parameter.</span></span> 
  
<span data-ttu-id="39de1-136">Ein standardmäßiges Empfangsordner abgerufen, indem Sie NULL im _LpszMessageClass_ -Parameter übergeben, ist für jedes Nachrichtenspeicher immer vorhanden.</span><span class="sxs-lookup"><span data-stu-id="39de1-136">A default receive folder, obtained by passing NULL in the  _lpszMessageClass_ parameter, always exists for every message store.</span></span> 
  
<span data-ttu-id="39de1-137">Ein Client sollte die Funktion [MAPIFreeBuffer](mapifreebuffer.md) aufrufen, wenn er, mit der Eintrags-ID, die in _LppEntryID abgeschlossen ist_ , um den Arbeitsspeicher freizugeben, der die Eintrags-ID zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="39de1-137">A client should call the [MAPIFreeBuffer](mapifreebuffer.md) function when it is done with the entry identifier returned in  _lppEntryID_ to free the memory that holds that entry identifier.</span></span> <span data-ttu-id="39de1-138">Sie sollten auch **MAPIFreeBuffer** aufrufen, wenn er, mit der Klassenzeichenfolge zurückgegeben, die in _LppszExplicitClass abgeschlossen ist_ , um den Arbeitsspeicher freizugeben, der die Zeichenfolge enthält.</span><span class="sxs-lookup"><span data-stu-id="39de1-138">It should also call **MAPIFreeBuffer** when it is done with the message class string returned in  _lppszExplicitClass_ to free the memory that holds that string.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="39de1-139">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="39de1-139">MFCMAPI reference</span></span>

<span data-ttu-id="39de1-140">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="39de1-140">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="39de1-141">**Datei**</span><span class="sxs-lookup"><span data-stu-id="39de1-141">**File**</span></span>|<span data-ttu-id="39de1-142">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="39de1-142">**Function**</span></span>|<span data-ttu-id="39de1-143">**Comment**</span><span class="sxs-lookup"><span data-stu-id="39de1-143">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="39de1-144">MAPIFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="39de1-144">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="39de1-145">GetInbox</span><span class="sxs-lookup"><span data-stu-id="39de1-145">GetInbox</span></span>  <br/> |<span data-ttu-id="39de1-146">MFCMAPI (engl.) verwendet die **IMsgStore::GetReceiveFolder** -Methode, um den Ordner Posteingang zu suchen.</span><span class="sxs-lookup"><span data-stu-id="39de1-146">MFCMAPI uses the **IMsgStore::GetReceiveFolder** method to locate the Inbox folder.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="39de1-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="39de1-147">See also</span></span>



[<span data-ttu-id="39de1-148">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="39de1-148">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="39de1-149">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="39de1-149">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)


[<span data-ttu-id="39de1-150">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="39de1-150">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

