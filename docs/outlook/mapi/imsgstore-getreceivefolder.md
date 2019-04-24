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
ms.openlocfilehash: ab21dcfb9011b675e3db4e4df29cb6ecafa6e7c6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348776"
---
# <a name="imsgstoregetreceivefolder"></a><span data-ttu-id="7cedf-103">IMsgStore::GetReceiveFolder</span><span class="sxs-lookup"><span data-stu-id="7cedf-103">IMsgStore::GetReceiveFolder</span></span>

  
  
<span data-ttu-id="7cedf-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7cedf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7cedf-105">Ruft den Ordner ab, der als Ziel für eingehende Nachrichten einer angegebenen Nachrichtenklasse oder als standardmäßiger Empfangsordner für den Nachrichtenspeicher eingerichtet wurde.</span><span class="sxs-lookup"><span data-stu-id="7cedf-105">Obtains the folder that was established as the destination for incoming messages of a specified message class or as the default receive folder for the message store.</span></span>
  
```cpp
HRESULT GetReceiveFolder(
  LPSTR lpszMessageClass,
  ULONG ulFlags,
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID,
  LPSTR FAR * lppszExplicitClass
);
```

## <a name="parameters"></a><span data-ttu-id="7cedf-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7cedf-106">Parameters</span></span>

 <span data-ttu-id="7cedf-107">_lpszMessageClass_</span><span class="sxs-lookup"><span data-stu-id="7cedf-107">_lpszMessageClass_</span></span>
  
> <span data-ttu-id="7cedf-108">in Ein Zeiger auf eine Nachrichtenklasse, die einem Empfangsordner zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="7cedf-108">[in] A pointer to a message class that is associated with a receive folder.</span></span> <span data-ttu-id="7cedf-109">Wenn der Parameter _lpszMessageClass_ auf NULL oder eine leere Zeichenfolge festgelegt ist, gibt **GetReceiveFolder** den standardmäßigen Empfangsordner für den Nachrichtenspeicher zurück.</span><span class="sxs-lookup"><span data-stu-id="7cedf-109">If the  _lpszMessageClass_ parameter is set to NULL or an empty string, **GetReceiveFolder** returns the default receive folder for the message store.</span></span> 
    
 <span data-ttu-id="7cedf-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="7cedf-110">_ulFlags_</span></span>
  
> <span data-ttu-id="7cedf-111">in Eine Bitmaske von Flags, die den Typ der übergebenen und zurückgegebenen Zeichenfolgen steuert.</span><span class="sxs-lookup"><span data-stu-id="7cedf-111">[in] A bitmask of flags that controls the type of the passed-in and returned strings.</span></span> <span data-ttu-id="7cedf-112">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="7cedf-112">The following flag can be set:</span></span>
    
<span data-ttu-id="7cedf-113">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="7cedf-113">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="7cedf-114">Die Zeichenfolge der Nachrichtenklasse ist im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="7cedf-114">The message class string is in Unicode format.</span></span> <span data-ttu-id="7cedf-115">Wenn das MAPI_UNICODE-Flag nicht festgelegt ist, ist die Zeichenfolge der Nachrichtenklasse im ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="7cedf-115">If the MAPI_UNICODE flag is not set, the message class string is in ANSI format.</span></span>
    
 <span data-ttu-id="7cedf-116">_lpcbEntryID_</span><span class="sxs-lookup"><span data-stu-id="7cedf-116">_lpcbEntryID_</span></span>
  
> <span data-ttu-id="7cedf-117">Out Ein Zeiger auf die Bytezahl in der Eintrags-ID, auf die durch den _lppEntryID_ -Parameter verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="7cedf-117">[out] A pointer to the byte count in the entry identifier pointed to by the  _lppEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="7cedf-118">_lppEntryID_</span><span class="sxs-lookup"><span data-stu-id="7cedf-118">_lppEntryID_</span></span>
  
> <span data-ttu-id="7cedf-119">Out Ein Zeiger auf einen Zeiger auf die Eintrags-ID für den angeforderten Empfänger Ordner.</span><span class="sxs-lookup"><span data-stu-id="7cedf-119">[out] A pointer to a pointer to the entry identifier for the requested receive folder.</span></span>
    
 <span data-ttu-id="7cedf-120">_lppszExplicitClass_</span><span class="sxs-lookup"><span data-stu-id="7cedf-120">_lppszExplicitClass_</span></span>
  
> <span data-ttu-id="7cedf-121">Out Ein Zeiger auf einen Zeiger auf die Nachrichtenklasse, die explizit als der Empfänger Ordner den Ordner, auf den durch _lppEntryID_festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="7cedf-121">[out] A pointer to a pointer to the message class that explicitly sets as its receive folder the folder pointed to by  _lppEntryID_.</span></span> <span data-ttu-id="7cedf-122">Diese Nachrichtenklasse sollte entweder mit der Klasse im _lpszMessageClass_ -Parameter oder mit einer Basisklasse dieser Klasse übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="7cedf-122">This message class should either be the same as the class in the  _lpszMessageClass_ parameter, or a base class of that class.</span></span> <span data-ttu-id="7cedf-123">Die Übergabe von NULL gibt an, dass der Ordner, auf den von _lppEntryID_ verwiesen wird, der standardmäßige Empfangsordner für den Nachrichtenspeicher ist.</span><span class="sxs-lookup"><span data-stu-id="7cedf-123">Passing NULL indicates that the folder pointed to by  _lppEntryID_ is the default receive folder for the message store.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="7cedf-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7cedf-124">Return value</span></span>

<span data-ttu-id="7cedf-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="7cedf-125">S_OK</span></span> 
  
> <span data-ttu-id="7cedf-126">Der Empfangsordner wurde erfolgreich zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7cedf-126">The receive folder was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7cedf-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7cedf-127">Remarks</span></span>

<span data-ttu-id="7cedf-128">Die **IMsgStore:: GetReceiveFolder** -Methode ruft die Eintrags-ID eines Empfangs Ordners ab, einen Ordner, der zum Empfangen eingehender Nachrichten einer bestimmten Nachrichtenklasse bestimmt ist.</span><span class="sxs-lookup"><span data-stu-id="7cedf-128">The **IMsgStore::GetReceiveFolder** method obtains the entry identifier of a receive folder, a folder designated to receive incoming messages of a particular message class.</span></span> <span data-ttu-id="7cedf-129">Anrufer können eine Nachrichtenklasse oder einen NULL-Wert im _lpszMessageClass_ -Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="7cedf-129">Callers can specify a message class or NULL in the  _lpszMessageClass_ parameter.</span></span> <span data-ttu-id="7cedf-130">Wenn _lpszMessageClass_ ist, gibt **GetReceiveFolder** die folgenden Werte zurück:</span><span class="sxs-lookup"><span data-stu-id="7cedf-130">If  _lpszMessageClass_ is NULL, **GetReceiveFolder** returns the following values:</span></span> 
  
- <span data-ttu-id="7cedf-131">In _lppszExplicitClass_der Name der ersten Basisklasse der Nachrichtenklasse, auf die durch _lpszMessageClass_ verwiesen wird, der explizit einen Empfangsordner festgelegt hat.</span><span class="sxs-lookup"><span data-stu-id="7cedf-131">In  _lppszExplicitClass_, the name of the first base class of the message class pointed to by  _lpszMessageClass_ that does explicitly set a receive folder.</span></span> 
    
- <span data-ttu-id="7cedf-132">In _lppEntryID_wird die Eintrags-ID des Empfänger Ordners für die Basisklasse, auf die durch den _lppszExplicitClass_ -Parameter verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="7cedf-132">In  _lppEntryID_, the entry identifier of the receive folder for the base class pointed to by the  _lppszExplicitClass_ parameter.</span></span> 
    
<span data-ttu-id="7cedf-133">Angenommen, der Empfangsordner der Nachrichtenklasse **IPM. Hinweis** wurde auf die Eintrags-ID des Posteingangs festgelegt, und **GetReceiveFolder** wird aufgerufen, wenn der Inhalt von _lpszMessageClass_ auf IPM festgelegt ist **. Hinweis. Phone**.</span><span class="sxs-lookup"><span data-stu-id="7cedf-133">For example, suppose the receive folder of the message class **IPM.Note** has been set to the entry identifier of the Inbox and **GetReceiveFolder** is called with the contents of  _lpszMessageClass_ set to **IPM.Note.Phone**.</span></span> <span data-ttu-id="7cedf-134">Wenn **IPM. Hinweis. das Telefon** verfügt nicht über einen expliziten Empfänger Ordner, **GetReceiveFolder** gibt den Eintragsbezeichner des Posteingangs in _lppEntryID_ und **IPM zurück. Hinweis** in _lppszExplicitClass_.</span><span class="sxs-lookup"><span data-stu-id="7cedf-134">If **IPM.Note.Phone** does not have an explicit receive folder set, **GetReceiveFolder** returns the entry identifier of the Inbox in  _lppEntryID_ and **IPM.Note** in  _lppszExplicitClass_.</span></span>
  
<span data-ttu-id="7cedf-135">Wenn der Client **GetReceiveFolder** für eine Nachrichtenklasse aufruft und keinen Empfangsordner für diese Nachrichtenklasse festgelegt hat, ist _lppszExplicitClass_ entweder eine leere Zeichenfolge, eine Zeichenfolge im Unicode-Format oder eine Zeichenfolge im ANSI-Format, je nachdem, ob die Client legen Sie das MAPI_UNICODE-Flag im _ulFlags_ -Parameter fest.</span><span class="sxs-lookup"><span data-stu-id="7cedf-135">If the client calls **GetReceiveFolder** for a message class and has not set a receive folder for that message class,  _lppszExplicitClass_ is either a zero-length string, a string in Unicode format, or a string in ANSI format depending on whether the client set the MAPI_UNICODE flag in the  _ulFlags_ parameter.</span></span> 
  
<span data-ttu-id="7cedf-136">Ein standardmäßiger Empfangsordner, der durch Übergeben von NULL im _lpszMessageClass_ -Parameter abgerufen wird, ist immer für jeden Nachrichtenspeicher vorhanden.</span><span class="sxs-lookup"><span data-stu-id="7cedf-136">A default receive folder, obtained by passing NULL in the  _lpszMessageClass_ parameter, always exists for every message store.</span></span> 
  
<span data-ttu-id="7cedf-137">Ein Client sollte die [mapifreebufferfreigegeben](mapifreebuffer.md) -Funktion aufrufen, wenn er mit der in _lppEntryID_ zurückgegebenen Eintrags-ID ausgeführt wird, um den Speicher freizugeben, der diese Eintrags-ID enthält.</span><span class="sxs-lookup"><span data-stu-id="7cedf-137">A client should call the [MAPIFreeBuffer](mapifreebuffer.md) function when it is done with the entry identifier returned in  _lppEntryID_ to free the memory that holds that entry identifier.</span></span> <span data-ttu-id="7cedf-138">Sie sollte auch **mapifreebufferfreigegeben** aufrufen, wenn Sie mit der in _lppszExplicitClass_ zurückgegebenen Nachrichtenklassen Zeichenfolge ausgeführt wird, um den Speicher freizugeben, der diese Zeichenfolge enthält.</span><span class="sxs-lookup"><span data-stu-id="7cedf-138">It should also call **MAPIFreeBuffer** when it is done with the message class string returned in  _lppszExplicitClass_ to free the memory that holds that string.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="7cedf-139">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="7cedf-139">MFCMAPI reference</span></span>

<span data-ttu-id="7cedf-140">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="7cedf-140">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="7cedf-141">**Datei**</span><span class="sxs-lookup"><span data-stu-id="7cedf-141">**File**</span></span>|<span data-ttu-id="7cedf-142">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="7cedf-142">**Function**</span></span>|<span data-ttu-id="7cedf-143">**Comment**</span><span class="sxs-lookup"><span data-stu-id="7cedf-143">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="7cedf-144">MAPIFunctions. cpp</span><span class="sxs-lookup"><span data-stu-id="7cedf-144">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="7cedf-145">GetInbox</span><span class="sxs-lookup"><span data-stu-id="7cedf-145">GetInbox</span></span>  <br/> |<span data-ttu-id="7cedf-146">MFCMAPI verwendet die **IMsgStore:: GetReceiveFolder** -Methode, um den Ordner Posteingang zu suchen.</span><span class="sxs-lookup"><span data-stu-id="7cedf-146">MFCMAPI uses the **IMsgStore::GetReceiveFolder** method to locate the Inbox folder.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7cedf-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7cedf-147">See also</span></span>



[<span data-ttu-id="7cedf-148">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="7cedf-148">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="7cedf-149">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="7cedf-149">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)


[<span data-ttu-id="7cedf-150">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="7cedf-150">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

