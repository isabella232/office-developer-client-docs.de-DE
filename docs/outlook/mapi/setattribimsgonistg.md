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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 852ce31ba5ab02ff8f05dee25c9b32acb73130ec
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337968"
---
# <a name="setattribimsgonistg"></a><span data-ttu-id="a97de-103">SetAttribIMsgOnIStg</span><span class="sxs-lookup"><span data-stu-id="a97de-103">SetAttribIMsgOnIStg</span></span>

  
  
<span data-ttu-id="a97de-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a97de-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a97de-105">Legt Attribute von Eigenschaften für ein [IMessage](imessageimapiprop.md) -Objekt fest, das von der [OpenIMsgOnIStg](openimsgonistg.md) -Funktion bereitgestellt wird, oder ändert Sie.</span><span class="sxs-lookup"><span data-stu-id="a97de-105">Sets or alters attributes of properties on an [IMessage](imessageimapiprop.md) object supplied by the [OpenIMsgOnIStg](openimsgonistg.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a97de-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="a97de-106">Header file:</span></span>  <br/> |<span data-ttu-id="a97de-107">IMessage. h</span><span class="sxs-lookup"><span data-stu-id="a97de-107">Imessage.h</span></span>  <br/> |
|<span data-ttu-id="a97de-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="a97de-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="a97de-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="a97de-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="a97de-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="a97de-110">Called by:</span></span>  <br/> |<span data-ttu-id="a97de-111">Client Anwendungen und Nachrichtenspeicher Anbieter</span><span class="sxs-lookup"><span data-stu-id="a97de-111">Client applications and message store providers</span></span>  <br/> |
   
```cpp
HRESULT SetAttribIMsgOnIStg(
  LPVOID lpObject,
  LPSPropTagArray lpPropTags,
  LPSPropAttrArray lpPropAttrs,
  LPSPropProblemArray FAR * lppPropProblems
);
```

## <a name="parameters"></a><span data-ttu-id="a97de-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="a97de-112">Parameters</span></span>

 <span data-ttu-id="a97de-113">_lpObject_</span><span class="sxs-lookup"><span data-stu-id="a97de-113">_lpObject_</span></span>
  
> <span data-ttu-id="a97de-114">in Zeiger auf das Objekt, für das Eigenschaftsattribute festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="a97de-114">[in] Pointer to the object for which property attributes are being set.</span></span> 
    
 <span data-ttu-id="a97de-115">_lpPropTags_</span><span class="sxs-lookup"><span data-stu-id="a97de-115">_lpPropTags_</span></span>
  
> <span data-ttu-id="a97de-116">in Zeiger auf eine [SPropTagArray](sproptagarray.md) -Struktur, die ein Array von Property-Tags angibt, die die Eigenschaften angeben, für die Eigenschaftsattribute festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="a97de-116">[in] Pointer to an [SPropTagArray](sproptagarray.md) structure containing an array of property tags indicating the properties for which property attributes are being set.</span></span> 
    
 <span data-ttu-id="a97de-117">_lpPropAttrs_</span><span class="sxs-lookup"><span data-stu-id="a97de-117">_lpPropAttrs_</span></span>
  
> <span data-ttu-id="a97de-118">in Zeiger auf eine [SPropAttrArray](spropattrarray.md) -Struktur, die die festzulegenden Eigenschaften Attribute auflistet.</span><span class="sxs-lookup"><span data-stu-id="a97de-118">[in] Pointer to an [SPropAttrArray](spropattrarray.md) structure listing the property attributes to set.</span></span> 
    
 <span data-ttu-id="a97de-119">_lppPropProblems_</span><span class="sxs-lookup"><span data-stu-id="a97de-119">_lppPropProblems_</span></span>
  
> <span data-ttu-id="a97de-120">Out Zeiger auf die zurückgegebene [SPropProblemArray](spropproblemarray.md) -Struktur mit einem Satz von Eigenschafts Problemen.</span><span class="sxs-lookup"><span data-stu-id="a97de-120">[out] Pointer to the returned [SPropProblemArray](spropproblemarray.md) structure containing a set of property problems.</span></span> <span data-ttu-id="a97de-121">Diese Struktur identifiziert Probleme, die auftreten, wenn **SetAttribIMsgOnIStg** einige Eigenschaften festlegen konnte, aber nicht alle.</span><span class="sxs-lookup"><span data-stu-id="a97de-121">This structure identifies problems encountered if **SetAttribIMsgOnIStg** has been able to set some properties, but not all.</span></span> <span data-ttu-id="a97de-122">Wenn ein Zeiger auf NULL im _lppPropProblems_ -Parameter übergeben wird, wird kein Eigenschaften Problem Array zurückgegeben, auch wenn einige Eigenschaften nicht festgelegt wurden.</span><span class="sxs-lookup"><span data-stu-id="a97de-122">If a pointer to NULL is passed in the  _lppPropProblems_ parameter, no property problem array is returned even if some properties were not set.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="a97de-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a97de-123">Return value</span></span>

<span data-ttu-id="a97de-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="a97de-124">S_OK</span></span> 
  
> <span data-ttu-id="a97de-125">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="a97de-125">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="a97de-126">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="a97de-126">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="a97de-127">Der Aufruf war insgesamt erfolgreich, aber auf eine oder mehrere Eigenschaften konnte nicht zugegriffen werden, und es wurde ein Eigenschaftentyp von PT_ERROR zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a97de-127">The call succeeded overall, but one or more properties could not be accessed and were returned with a property type of PT_ERROR.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a97de-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a97de-128">Remarks</span></span>

<span data-ttu-id="a97de-129">Auf Eigenschaftsattribute kann nur über Property-Objekte zugegriffen werden, also auf Objekte, die die [IMAPIProp: IUnknown](imapipropiunknown.md) -Schnittstelle implementieren.</span><span class="sxs-lookup"><span data-stu-id="a97de-129">Property attributes can only be accessed on property objects, that is, objects implementing the [IMAPIProp : IUnknown](imapipropiunknown.md) interface.</span></span> <span data-ttu-id="a97de-130">Um MAPI-Eigenschaften für ein OLE Structured Storage-Objekt verfügbar zu machen, erstellt [OpenIMsgOnIStg](openimsgonistg.md) ein [IMessage: IMAPIProp](imessageimapiprop.md) -Objekt über dem OLE- **IStorage** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="a97de-130">To make MAPI properties available on an OLE structured storage object, [OpenIMsgOnIStg](openimsgonistg.md) builds an [IMessage : IMAPIProp](imessageimapiprop.md) object on top of the OLE **IStorage** object.</span></span> <span data-ttu-id="a97de-131">Die Eigenschaftsattribute für solche Objekte können mit **SetAttribIMsgOnIStg** festgelegt oder geändert und mit [GetAttribIMsgOnIStg](getattribimsgonistg.md)abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="a97de-131">The property attributes on such objects can be set or altered with **SetAttribIMsgOnIStg** and retrieved with [GetAttribIMsgOnIStg](getattribimsgonistg.md).</span></span> 
  
 <span data-ttu-id="a97de-132">**Hinweis** **GetAttribIMsgOnIStg** und **SetAttribIMsgOnIStg** funktionieren nicht für alle **IMessage** -Objekte.</span><span class="sxs-lookup"><span data-stu-id="a97de-132">**Note** **GetAttribIMsgOnIStg** and **SetAttribIMsgOnIStg** do not operate on all **IMessage** objects.</span></span> <span data-ttu-id="a97de-133">Sie sind nur für **IMessage**-on- **IStorage** -Objekte gültig, die von **OpenIMsgOnIStg**zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="a97de-133">They are only valid for **IMessage**-on- **IStorage** objects returned by **OpenIMsgOnIStg**.</span></span> 
  
<span data-ttu-id="a97de-134">Im _lpPropAttrs_ -Parameter müssen die Anzahl und die Position der Attribute mit der Anzahl und Position der im _lpPropTags_ -Parameter übergebenen Property-Tags übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="a97de-134">In the  _lpPropAttrs_ parameter, the number and position of the attributes must match the number and position of the property tags passed in the  _lpPropTags_ parameter.</span></span> 
  
<span data-ttu-id="a97de-135">Die **SetAttribIMsgOnIStg** -Funktion wird verwendet, um Nachrichteneigenschaften schreibgeschützt zu machen, wenn Sie vom **IMessage** -Schema benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="a97de-135">The **SetAttribIMsgOnIStg** function is used to make message properties read-only when required by the **IMessage** schema.</span></span> <span data-ttu-id="a97de-136">Der Beispiel-Nachrichtenspeicher Anbieter verwendet diesen zu diesem Zweck.</span><span class="sxs-lookup"><span data-stu-id="a97de-136">The sample message store provider uses it for this purpose.</span></span> <span data-ttu-id="a97de-137">Weitere Informationen finden Sie unter [Nachrichten](mapi-messages.md).</span><span class="sxs-lookup"><span data-stu-id="a97de-137">For more information, see [Messages](mapi-messages.md).</span></span> 
  

