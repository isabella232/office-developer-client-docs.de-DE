---
title: IMAPIFormMgrResolveMessageClass
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr.ResolveMessageClass
api_type:
- COM
ms.assetid: c2af7516-3a97-4422-874d-b1e3a0d4f316
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: e99cff77fe872018722395c53c605e4d8fabfdde
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321609"
---
# <a name="imapiformmgrresolvemessageclass"></a><span data-ttu-id="d228f-103">IMAPIFormMgr::ResolveMessageClass</span><span class="sxs-lookup"><span data-stu-id="d228f-103">IMAPIFormMgr::ResolveMessageClass</span></span>

  
  
<span data-ttu-id="d228f-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d228f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d228f-105">Löst eine Nachrichtenklasse in Ihrem Formular innerhalb eines Formular Containers auf und gibt ein Formular Informationsobjekt für dieses Formular zurück.</span><span class="sxs-lookup"><span data-stu-id="d228f-105">Resolves a message class to its form within a form container, and returns a form information object for that form.</span></span>
  
```cpp
HRESULT ResolveMessageClass(
  LPCSTR szMsgClass,
  ULONG ulFlags,
  LPMAPIFOLDER pFolderFocus,
  LPMAPIFORMINFO FAR * ppResult
);
```

## <a name="parameters"></a><span data-ttu-id="d228f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d228f-106">Parameters</span></span>

 <span data-ttu-id="d228f-107">_szMsgClass_</span><span class="sxs-lookup"><span data-stu-id="d228f-107">_szMsgClass_</span></span>
  
> <span data-ttu-id="d228f-108">in Eine Zeichenfolge, die die zu lösende Nachrichtenklasse benennt.</span><span class="sxs-lookup"><span data-stu-id="d228f-108">[in] A string that names the message class being resolved.</span></span>
    
 <span data-ttu-id="d228f-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d228f-109">_ulFlags_</span></span>
  
> <span data-ttu-id="d228f-110">in Eine Bitmaske von Flags, die die Auflösung der Nachrichtenklasse steuert.</span><span class="sxs-lookup"><span data-stu-id="d228f-110">[in] A bitmask of flags that controls how the message class is resolved.</span></span> <span data-ttu-id="d228f-111">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="d228f-111">The following flag can be set:</span></span>
    
<span data-ttu-id="d228f-112">MAPIFORM_EXACTMATCH</span><span class="sxs-lookup"><span data-stu-id="d228f-112">MAPIFORM_EXACTMATCH</span></span> 
  
> <span data-ttu-id="d228f-113">Nur Nachrichtenklassen Zeichenfolgen, die exakt übereinstimmen, sollten aufgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="d228f-113">Only message class strings that are an exact match should be resolved.</span></span>
    
 <span data-ttu-id="d228f-114">_pFolderFocus_</span><span class="sxs-lookup"><span data-stu-id="d228f-114">_pFolderFocus_</span></span>
  
> <span data-ttu-id="d228f-115">in Ein Zeiger auf den Ordner, der die zu bearbeitende Nachricht enthält.</span><span class="sxs-lookup"><span data-stu-id="d228f-115">[in] A pointer to the folder that contains the message being resolved.</span></span> <span data-ttu-id="d228f-116">Der _pFolderFocus_ -Parameter kann NULL sein.</span><span class="sxs-lookup"><span data-stu-id="d228f-116">The  _pFolderFocus_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="d228f-117">_ppResult_</span><span class="sxs-lookup"><span data-stu-id="d228f-117">_ppResult_</span></span>
  
> <span data-ttu-id="d228f-118">Out Ein Zeiger auf einen Zeiger auf ein zurückgegebenes Formular Informationsobjekt.</span><span class="sxs-lookup"><span data-stu-id="d228f-118">[out] A pointer to a pointer to a returned form information object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d228f-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d228f-119">Return value</span></span>

<span data-ttu-id="d228f-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="d228f-120">S_OK</span></span> 
  
> <span data-ttu-id="d228f-121">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="d228f-121">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="d228f-122">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="d228f-122">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="d228f-123">Die Nachrichtenklasse, die im _szMsgClass_ -Parameter übergeben wird, stimmt nicht mit der Nachrichtenklasse für ein Formular in der Formularbibliothek überein.</span><span class="sxs-lookup"><span data-stu-id="d228f-123">The message class passed in the  _szMsgClass_ parameter does not match the message class for any form in the form library.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="d228f-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d228f-124">Remarks</span></span>

<span data-ttu-id="d228f-125">Formular Betrachter rufen die **IMAPIFormMgr:: ResolveMessageClass** -Methode auf, um eine Nachrichtenklasse in Ihr Formular innerhalb eines Formular Containers aufzulösen.</span><span class="sxs-lookup"><span data-stu-id="d228f-125">Form viewers call the **IMAPIFormMgr::ResolveMessageClass** method to resolve a message class to its form within a form container.</span></span> <span data-ttu-id="d228f-126">Das im _ppResult_ -Parameter zurückgegebene Formular Informationsobjekt bietet weiteren Zugriff auf die Eigenschaften des Formulars, das über die angegebene Nachrichtenklasse verfügt.</span><span class="sxs-lookup"><span data-stu-id="d228f-126">The form information object returned in the  _ppResult_ parameter provides further access to the properties of the form that has the given message class.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="d228f-127">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="d228f-127">Notes to callers</span></span>

<span data-ttu-id="d228f-128">Um eine Nachrichtenklasse in ein Formular aufzulösen, übergibt ein Formular Betrachter den Namen der zu lösenden Nachrichtenklasse, beispielsweise " `IPM.HelpDesk.Software`".</span><span class="sxs-lookup"><span data-stu-id="d228f-128">To resolve a message class to a form, a form viewer passes in the name of the message class to be resolved, such as " `IPM.HelpDesk.Software`".</span></span> <span data-ttu-id="d228f-129">Um die Auflösung genau zu erzwingen (das heißt, um die Auflösung einer Basisklasse der Nachrichtenklasse zu verhindern, wenn ein genau übereinstimmender Formularserver nicht verfügbar ist), kann das MAPIFORM_EXACTMATCH-Flag im _ulFlags_ -Parameter übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="d228f-129">To force the resolution to be exact (that is, to prevent resolution to a base class of the message class when an exactly matching form server is not available), the MAPIFORM_EXACTMATCH flag can be passed in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="d228f-130">Wenn der _pFolderFocus_ -Parameter NULL ist, durchsucht der Prozess der Nachrichtenklassen Auflösung keinen Ordner Container.</span><span class="sxs-lookup"><span data-stu-id="d228f-130">If the  _pFolderFocus_ parameter is NULL, the message-class resolution process does not search a folder container.</span></span> 
  
<span data-ttu-id="d228f-131">Die Reihenfolge der gesuchten Container hängt von der Implementierung des Formularbibliothek Anbieters ab.</span><span class="sxs-lookup"><span data-stu-id="d228f-131">The order of the containers searched depends on the implementation of the form library provider.</span></span> <span data-ttu-id="d228f-132">Der Standardanbieter für Formularbibliotheken durchsucht zuerst den lokalen Container, dann den Ordner Container für den übergebenen Ordner, den persönlichen Formular Container und schließlich den Organisationscontainer.</span><span class="sxs-lookup"><span data-stu-id="d228f-132">The default form library provider searches first the local container, then the folder container for the passed-in folder, the personal form container and, finally, the organization container.</span></span>
  
<span data-ttu-id="d228f-133">Nachrichtenklassennamen sind immer ANSI-Zeichenfolgen, nie Unicode.</span><span class="sxs-lookup"><span data-stu-id="d228f-133">Message class names are always ANSI strings, never Unicode.</span></span>
  
<span data-ttu-id="d228f-134">Der Klassenbezeichner für die aufgelöste Nachrichtenklasse wird als Teil des Form Information-Objekts zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d228f-134">The class identifier for the resolved message class is returned as part of the form information object.</span></span> <span data-ttu-id="d228f-135">Ein Formular Betrachter sollte nicht davon ausgehen, dass der Klassenbezeichner in der OLE-Bibliothek vorhanden ist, bis die [IMAPIFormMgr::P repareform](imapiformmgr-prepareform.md) -Methode oder die [IMAPIFormMgr:: CreateForm](imapiformmgr-createform.md) -Methode aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="d228f-135">A form viewer should not work on the assumption that the class identifier exists in the OLE library until after the form viewer has called either the [IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md) method or the [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d228f-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d228f-136">See also</span></span>



[<span data-ttu-id="d228f-137">IMAPIFormInfo : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="d228f-137">IMAPIFormInfo : IMAPIProp</span></span>](imapiforminfoimapiprop.md)
  
[<span data-ttu-id="d228f-138">IMAPIFormMgr::CreateForm</span><span class="sxs-lookup"><span data-stu-id="d228f-138">IMAPIFormMgr::CreateForm</span></span>](imapiformmgr-createform.md)
  
[<span data-ttu-id="d228f-139">IMAPIFormMgr::PrepareForm</span><span class="sxs-lookup"><span data-stu-id="d228f-139">IMAPIFormMgr::PrepareForm</span></span>](imapiformmgr-prepareform.md)
  
[<span data-ttu-id="d228f-140">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d228f-140">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)

