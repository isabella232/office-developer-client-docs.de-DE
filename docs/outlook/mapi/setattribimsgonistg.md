---
title: SetAttribIMsgOnIStg
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SetAttribIMsgOnIStg
api_type:
- COM
ms.assetid: 683d0d00-1b93-445d-86ff-180a3e6d2323
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 852ce31ba5ab02ff8f05dee25c9b32acb73130ec
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428830"
---
# <a name="setattribimsgonistg"></a><span data-ttu-id="0e050-103">SetAttribIMsgOnIStg</span><span class="sxs-lookup"><span data-stu-id="0e050-103">SetAttribIMsgOnIStg</span></span>

  
  
<span data-ttu-id="0e050-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0e050-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0e050-105">Legt Attribute von Eigenschaften für ein [IMessage-Objekt](imessageimapiprop.md) fest, das von der [OpenIMsgOnIStg-Funktion bereitgestellt](openimsgonistg.md) wird, oder ändert sie.</span><span class="sxs-lookup"><span data-stu-id="0e050-105">Sets or alters attributes of properties on an [IMessage](imessageimapiprop.md) object supplied by the [OpenIMsgOnIStg](openimsgonistg.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0e050-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="0e050-106">Header file:</span></span>  <br/> |<span data-ttu-id="0e050-107">Imessage.h</span><span class="sxs-lookup"><span data-stu-id="0e050-107">Imessage.h</span></span>  <br/> |
|<span data-ttu-id="0e050-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="0e050-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="0e050-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="0e050-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="0e050-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="0e050-110">Called by:</span></span>  <br/> |<span data-ttu-id="0e050-111">Clientanwendungen und Nachrichtenspeicheranbieter</span><span class="sxs-lookup"><span data-stu-id="0e050-111">Client applications and message store providers</span></span>  <br/> |
   
```cpp
HRESULT SetAttribIMsgOnIStg(
  LPVOID lpObject,
  LPSPropTagArray lpPropTags,
  LPSPropAttrArray lpPropAttrs,
  LPSPropProblemArray FAR * lppPropProblems
);
```

## <a name="parameters"></a><span data-ttu-id="0e050-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="0e050-112">Parameters</span></span>

 <span data-ttu-id="0e050-113">_lpObject_</span><span class="sxs-lookup"><span data-stu-id="0e050-113">_lpObject_</span></span>
  
> <span data-ttu-id="0e050-114">[in] Zeiger auf das Objekt, für das Eigenschaftenattribute festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="0e050-114">[in] Pointer to the object for which property attributes are being set.</span></span> 
    
 <span data-ttu-id="0e050-115">_lpPropTags_</span><span class="sxs-lookup"><span data-stu-id="0e050-115">_lpPropTags_</span></span>
  
> <span data-ttu-id="0e050-116">[in] Zeiger auf eine [SPropTagArray-Struktur,](sproptagarray.md) die ein Array von Eigenschaftstags enthält, die die Eigenschaften angeben, für die Eigenschaftenattribute festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="0e050-116">[in] Pointer to an [SPropTagArray](sproptagarray.md) structure containing an array of property tags indicating the properties for which property attributes are being set.</span></span> 
    
 <span data-ttu-id="0e050-117">_lpPropAttrs_</span><span class="sxs-lookup"><span data-stu-id="0e050-117">_lpPropAttrs_</span></span>
  
> <span data-ttu-id="0e050-118">[in] Zeiger auf eine [SPropAttrArray-Struktur,](spropattrarray.md) die die festgelegten Eigenschaftenattribute auflistet.</span><span class="sxs-lookup"><span data-stu-id="0e050-118">[in] Pointer to an [SPropAttrArray](spropattrarray.md) structure listing the property attributes to set.</span></span> 
    
 <span data-ttu-id="0e050-119">_lppPropProblems_</span><span class="sxs-lookup"><span data-stu-id="0e050-119">_lppPropProblems_</span></span>
  
> <span data-ttu-id="0e050-120">[out] Zeiger auf die zurückgegebene [SPropProblemArray-Struktur](spropproblemarray.md) mit einer Reihe von Eigenschaftsproblemen.</span><span class="sxs-lookup"><span data-stu-id="0e050-120">[out] Pointer to the returned [SPropProblemArray](spropproblemarray.md) structure containing a set of property problems.</span></span> <span data-ttu-id="0e050-121">Diese Struktur identifiziert Probleme, die **auftreten, wenn SetAttribIMsgOnIStg** einige Eigenschaften festlegen konnte, aber nicht alle.</span><span class="sxs-lookup"><span data-stu-id="0e050-121">This structure identifies problems encountered if **SetAttribIMsgOnIStg** has been able to set some properties, but not all.</span></span> <span data-ttu-id="0e050-122">Wenn ein Zeiger auf NULL im  _lppPropProblems-Parameter_ übergeben wird, wird kein Eigenschaftsproblemarray zurückgegeben, auch wenn einige Eigenschaften nicht festgelegt wurden.</span><span class="sxs-lookup"><span data-stu-id="0e050-122">If a pointer to NULL is passed in the  _lppPropProblems_ parameter, no property problem array is returned even if some properties were not set.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="0e050-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0e050-123">Return value</span></span>

<span data-ttu-id="0e050-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="0e050-124">S_OK</span></span> 
  
> <span data-ttu-id="0e050-125">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="0e050-125">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="0e050-126">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="0e050-126">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="0e050-127">Der Aufruf war insgesamt erfolgreich, aber auf eine oder mehrere Eigenschaften konnte nicht zugegriffen werden und wurde mit dem Eigenschaftstyp PT_ERROR.</span><span class="sxs-lookup"><span data-stu-id="0e050-127">The call succeeded overall, but one or more properties could not be accessed and were returned with a property type of PT_ERROR.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0e050-128">Hinweise</span><span class="sxs-lookup"><span data-stu-id="0e050-128">Remarks</span></span>

<span data-ttu-id="0e050-129">Auf Eigenschaftsattribute kann nur auf Eigenschaftsobjekte zugegriffen werden, d. h. auf Objekte, die die [IMAPIProp : IUnknown-Schnittstelle](imapipropiunknown.md) implementieren.</span><span class="sxs-lookup"><span data-stu-id="0e050-129">Property attributes can only be accessed on property objects, that is, objects implementing the [IMAPIProp : IUnknown](imapipropiunknown.md) interface.</span></span> <span data-ttu-id="0e050-130">Um MAPI-Eigenschaften für ein strukturiertes OLE-Speicherobjekt verfügbar zu machen, erstellt [OpenIMsgOnIStg](openimsgonistg.md) ein [IMessage : IMAPIProp-Objekt](imessageimapiprop.md) über dem OLE **IStorage-Objekt.**</span><span class="sxs-lookup"><span data-stu-id="0e050-130">To make MAPI properties available on an OLE structured storage object, [OpenIMsgOnIStg](openimsgonistg.md) builds an [IMessage : IMAPIProp](imessageimapiprop.md) object on top of the OLE **IStorage** object.</span></span> <span data-ttu-id="0e050-131">Die Eigenschaftenattribute für solche Objekte können mit **SetAttribIMsgOnIStg** festgelegt oder geändert und mit [GetAttribIMsgOnIStg abgerufen werden.](getattribimsgonistg.md)</span><span class="sxs-lookup"><span data-stu-id="0e050-131">The property attributes on such objects can be set or altered with **SetAttribIMsgOnIStg** and retrieved with [GetAttribIMsgOnIStg](getattribimsgonistg.md).</span></span> 
  
 <span data-ttu-id="0e050-132">**Hinweis** **GetAttribIMsgOnIStg** und **SetAttribIMsgOnIStg** funktionieren nicht für alle **IMessage-Objekte.**</span><span class="sxs-lookup"><span data-stu-id="0e050-132">**Note** **GetAttribIMsgOnIStg** and **SetAttribIMsgOnIStg** do not operate on all **IMessage** objects.</span></span> <span data-ttu-id="0e050-133">Sie sind nur gültig für **IMessage** **-on-IStorage-Objekte,** die von **OpenIMsgOnIStg zurückgegeben werden.**</span><span class="sxs-lookup"><span data-stu-id="0e050-133">They are only valid for **IMessage**-on- **IStorage** objects returned by **OpenIMsgOnIStg**.</span></span> 
  
<span data-ttu-id="0e050-134">Im  _lpPropAttrs-Parameter_ müssen Anzahl und Position der Attribute mit der Anzahl und Position der Eigenschaftstags übereinstimmen, die im  _lpPropTags-Parameter übergeben_ werden.</span><span class="sxs-lookup"><span data-stu-id="0e050-134">In the  _lpPropAttrs_ parameter, the number and position of the attributes must match the number and position of the property tags passed in the  _lpPropTags_ parameter.</span></span> 
  
<span data-ttu-id="0e050-135">Die **SetAttribIMsgOnIStg-Funktion** wird verwendet, um Nachrichteneigenschaften schreibgeschützt zu machen, wenn dies im **IMessage-Schema erforderlich** ist.</span><span class="sxs-lookup"><span data-stu-id="0e050-135">The **SetAttribIMsgOnIStg** function is used to make message properties read-only when required by the **IMessage** schema.</span></span> <span data-ttu-id="0e050-136">Der Beispielnachrichtenspeicheranbieter verwendet ihn zu diesem Zweck.</span><span class="sxs-lookup"><span data-stu-id="0e050-136">The sample message store provider uses it for this purpose.</span></span> <span data-ttu-id="0e050-137">Weitere Informationen finden Sie unter [Nachrichten](mapi-messages.md).</span><span class="sxs-lookup"><span data-stu-id="0e050-137">For more information, see [Messages](mapi-messages.md).</span></span> 
  

