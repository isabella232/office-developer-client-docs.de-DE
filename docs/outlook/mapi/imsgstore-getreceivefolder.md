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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: ab21dcfb9011b675e3db4e4df29cb6ecafa6e7c6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435348"
---
# <a name="imsgstoregetreceivefolder"></a><span data-ttu-id="eb573-103">IMsgStore::GetReceiveFolder</span><span class="sxs-lookup"><span data-stu-id="eb573-103">IMsgStore::GetReceiveFolder</span></span>

  
  
<span data-ttu-id="eb573-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="eb573-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="eb573-105">Ruft den Ordner ab, der als Ziel für eingehende Nachrichten einer angegebenen Nachrichtenklasse oder als Standard-Empfangsordner für den Nachrichtenspeicher eingerichtet wurde.</span><span class="sxs-lookup"><span data-stu-id="eb573-105">Obtains the folder that was established as the destination for incoming messages of a specified message class or as the default receive folder for the message store.</span></span>
  
```cpp
HRESULT GetReceiveFolder(
  LPSTR lpszMessageClass,
  ULONG ulFlags,
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID,
  LPSTR FAR * lppszExplicitClass
);
```

## <a name="parameters"></a><span data-ttu-id="eb573-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="eb573-106">Parameters</span></span>

 <span data-ttu-id="eb573-107">_lpszMessageClass_</span><span class="sxs-lookup"><span data-stu-id="eb573-107">_lpszMessageClass_</span></span>
  
> <span data-ttu-id="eb573-108">[in] Ein Zeiger auf eine Nachrichtenklasse, die einem Empfangsordner zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="eb573-108">[in] A pointer to a message class that is associated with a receive folder.</span></span> <span data-ttu-id="eb573-109">Wenn der  _lpszMessageClass-Parameter_ auf NULL oder eine leere Zeichenfolge festgelegt ist, gibt **GetReceiveFolder** den Standard-Empfangsordner für den Nachrichtenspeicher zurück.</span><span class="sxs-lookup"><span data-stu-id="eb573-109">If the  _lpszMessageClass_ parameter is set to NULL or an empty string, **GetReceiveFolder** returns the default receive folder for the message store.</span></span> 
    
 <span data-ttu-id="eb573-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="eb573-110">_ulFlags_</span></span>
  
> <span data-ttu-id="eb573-111">[in] Eine Bitmaske von Flags, die den Typ der übergebenen und zurückgegebenen Zeichenfolgen steuert.</span><span class="sxs-lookup"><span data-stu-id="eb573-111">[in] A bitmask of flags that controls the type of the passed-in and returned strings.</span></span> <span data-ttu-id="eb573-112">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="eb573-112">The following flag can be set:</span></span>
    
<span data-ttu-id="eb573-113">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="eb573-113">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="eb573-114">Die Zeichenfolge der Nachrichtenklasse befindet sich im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="eb573-114">The message class string is in Unicode format.</span></span> <span data-ttu-id="eb573-115">Wenn das MAPI_UNICODE nicht festgelegt ist, befindet sich die Zeichenfolge der Nachrichtenklasse im ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="eb573-115">If the MAPI_UNICODE flag is not set, the message class string is in ANSI format.</span></span>
    
 <span data-ttu-id="eb573-116">_lpcbEntryID_</span><span class="sxs-lookup"><span data-stu-id="eb573-116">_lpcbEntryID_</span></span>
  
> <span data-ttu-id="eb573-117">[out] Ein Zeiger auf die Byteanzahl in der Eintrags-ID, auf die der  _lppEntryID-Parameter_ verweist.</span><span class="sxs-lookup"><span data-stu-id="eb573-117">[out] A pointer to the byte count in the entry identifier pointed to by the  _lppEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="eb573-118">_lppEntryID_</span><span class="sxs-lookup"><span data-stu-id="eb573-118">_lppEntryID_</span></span>
  
> <span data-ttu-id="eb573-119">[out] Ein Zeiger auf einen Zeiger auf die Eintrags-ID für den angeforderten Empfangsordner.</span><span class="sxs-lookup"><span data-stu-id="eb573-119">[out] A pointer to a pointer to the entry identifier for the requested receive folder.</span></span>
    
 <span data-ttu-id="eb573-120">_lppszExplicitClass_</span><span class="sxs-lookup"><span data-stu-id="eb573-120">_lppszExplicitClass_</span></span>
  
> <span data-ttu-id="eb573-121">[out] Ein Zeiger auf einen Zeiger auf die Nachrichtenklasse, die explizit als Empfangsordner festgelegt wird, auf den der Ordner durch _lppEntryID verweist._</span><span class="sxs-lookup"><span data-stu-id="eb573-121">[out] A pointer to a pointer to the message class that explicitly sets as its receive folder the folder pointed to by  _lppEntryID_.</span></span> <span data-ttu-id="eb573-122">Diese Nachrichtenklasse sollte entweder mit der Klasse im  _lpszMessageClass-Parameter_ oder einer Basisklasse dieser Klasse identisch sein.</span><span class="sxs-lookup"><span data-stu-id="eb573-122">This message class should either be the same as the class in the  _lpszMessageClass_ parameter, or a base class of that class.</span></span> <span data-ttu-id="eb573-123">Das Übergeben von NULL gibt an, dass der Ordner, auf den  _lppEntryID_ verweist, der Standard-Empfangsordner für den Nachrichtenspeicher ist.</span><span class="sxs-lookup"><span data-stu-id="eb573-123">Passing NULL indicates that the folder pointed to by  _lppEntryID_ is the default receive folder for the message store.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="eb573-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="eb573-124">Return value</span></span>

<span data-ttu-id="eb573-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="eb573-125">S_OK</span></span> 
  
> <span data-ttu-id="eb573-126">Der Empfangsordner wurde erfolgreich zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="eb573-126">The receive folder was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="eb573-127">Hinweise</span><span class="sxs-lookup"><span data-stu-id="eb573-127">Remarks</span></span>

<span data-ttu-id="eb573-128">Die **IMsgStore::GetReceiveFolder-Methode** ruft die Eintrags-ID eines Empfangsordners ab, einem Ordner, der für den Empfang eingehender Nachrichten einer bestimmten Nachrichtenklasse bestimmt ist.</span><span class="sxs-lookup"><span data-stu-id="eb573-128">The **IMsgStore::GetReceiveFolder** method obtains the entry identifier of a receive folder, a folder designated to receive incoming messages of a particular message class.</span></span> <span data-ttu-id="eb573-129">Anrufer können eine Nachrichtenklasse oder NULL im  _lpszMessageClass-Parameter_ angeben.</span><span class="sxs-lookup"><span data-stu-id="eb573-129">Callers can specify a message class or NULL in the  _lpszMessageClass_ parameter.</span></span> <span data-ttu-id="eb573-130">Wenn  _lpszMessageClass_ null ist, **gibt GetReceiveFolder** die folgenden Werte zurück:</span><span class="sxs-lookup"><span data-stu-id="eb573-130">If  _lpszMessageClass_ is NULL, **GetReceiveFolder** returns the following values:</span></span> 
  
- <span data-ttu-id="eb573-131">In  _lppszExplicitClass_ der Name der ersten Basisklasse der Nachrichtenklasse, auf die  _von lpszMessageClass_ verwiesen wird, die explizit einen Empfangsordner festgelegt hat.</span><span class="sxs-lookup"><span data-stu-id="eb573-131">In  _lppszExplicitClass_, the name of the first base class of the message class pointed to by  _lpszMessageClass_ that does explicitly set a receive folder.</span></span> 
    
- <span data-ttu-id="eb573-132">In  _lppEntryID_ der Eintragsbezeichner des Empfangsordners für die Basisklasse, auf die der  _lppszExplicitClass-Parameter_ verweist.</span><span class="sxs-lookup"><span data-stu-id="eb573-132">In  _lppEntryID_, the entry identifier of the receive folder for the base class pointed to by the  _lppszExplicitClass_ parameter.</span></span> 
    
<span data-ttu-id="eb573-133">Angenommen, der Empfangsordner der Nachrichtenklasse **IPM. Note** has been set to the entry identifier of the Inbox and **GetReceiveFolder** is called with the contents of _lpszMessageClass_ set to **IPM. Hinweis. Telefon**.</span><span class="sxs-lookup"><span data-stu-id="eb573-133">For example, suppose the receive folder of the message class **IPM.Note** has been set to the entry identifier of the Inbox and **GetReceiveFolder** is called with the contents of  _lpszMessageClass_ set to **IPM.Note.Phone**.</span></span> <span data-ttu-id="eb573-134">Wenn **IPM. Hinweis. Telefon** hat keinen expliziten Empfangsordnersatz, **gibt GetReceiveFolder** den Eintragsbezeichner des Posteingangs in _lppEntryID_ und **IPM zurück. Hinweis** in _lppszExplicitClass_.</span><span class="sxs-lookup"><span data-stu-id="eb573-134">If **IPM.Note.Phone** does not have an explicit receive folder set, **GetReceiveFolder** returns the entry identifier of the Inbox in  _lppEntryID_ and **IPM.Note** in  _lppszExplicitClass_.</span></span>
  
<span data-ttu-id="eb573-135">Wenn der Client **GetReceiveFolder** für eine Nachrichtenklasse aufruft und keinen Empfangsordner für diese Nachrichtenklasse festgelegt hat, ist  _lppszExplicitClass_ entweder eine Nulllängenzeichenfolge, eine Zeichenfolge im Unicode-Format oder eine Zeichenfolge im ANSI-Format, je nachdem, ob der Client das MAPI_UNICODE-Flag im  _ulFlags-Parameter_ festgelegt hat.</span><span class="sxs-lookup"><span data-stu-id="eb573-135">If the client calls **GetReceiveFolder** for a message class and has not set a receive folder for that message class,  _lppszExplicitClass_ is either a zero-length string, a string in Unicode format, or a string in ANSI format depending on whether the client set the MAPI_UNICODE flag in the  _ulFlags_ parameter.</span></span> 
  
<span data-ttu-id="eb573-136">Ein Standardmäßiger Empfangsordner, der durch Übergeben von NULL im  _lpszMessageClass-Parameter_ erhalten wird, ist immer für jeden Nachrichtenspeicher vorhanden.</span><span class="sxs-lookup"><span data-stu-id="eb573-136">A default receive folder, obtained by passing NULL in the  _lpszMessageClass_ parameter, always exists for every message store.</span></span> 
  
<span data-ttu-id="eb573-137">Ein Client sollte die [MAPIFreeBuffer-Funktion](mapifreebuffer.md) aufrufen, wenn dies mit dem in  _lppEntryID zurückgegebenen_ Eintragsbezeichner erfolgt, um den Speicher frei zu machen, der diese Eintrags-ID enthält.</span><span class="sxs-lookup"><span data-stu-id="eb573-137">A client should call the [MAPIFreeBuffer](mapifreebuffer.md) function when it is done with the entry identifier returned in  _lppEntryID_ to free the memory that holds that entry identifier.</span></span> <span data-ttu-id="eb573-138">Es sollte auch **MAPIFreeBuffer** aufrufen, wenn dies mit der in  _lppszExplicitClass_ zurückgegebenen Nachrichtenklassenzeichenfolge erfolgt, um den Speicher frei zu machen, der diese Zeichenfolge enthält.</span><span class="sxs-lookup"><span data-stu-id="eb573-138">It should also call **MAPIFreeBuffer** when it is done with the message class string returned in  _lppszExplicitClass_ to free the memory that holds that string.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="eb573-139">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="eb573-139">MFCMAPI reference</span></span>

<span data-ttu-id="eb573-140">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="eb573-140">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="eb573-141">**Datei**</span><span class="sxs-lookup"><span data-stu-id="eb573-141">**File**</span></span>|<span data-ttu-id="eb573-142">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="eb573-142">**Function**</span></span>|<span data-ttu-id="eb573-143">**Comment**</span><span class="sxs-lookup"><span data-stu-id="eb573-143">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="eb573-144">MAPIFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="eb573-144">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="eb573-145">GetInbox</span><span class="sxs-lookup"><span data-stu-id="eb573-145">GetInbox</span></span>  <br/> |<span data-ttu-id="eb573-146">MFCMAPI verwendet die **IMsgStore::GetReceiveFolder-Methode,** um den Posteingangsordner zu finden.</span><span class="sxs-lookup"><span data-stu-id="eb573-146">MFCMAPI uses the **IMsgStore::GetReceiveFolder** method to locate the Inbox folder.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="eb573-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eb573-147">See also</span></span>



[<span data-ttu-id="eb573-148">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="eb573-148">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="eb573-149">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="eb573-149">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)


[<span data-ttu-id="eb573-150">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="eb573-150">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

