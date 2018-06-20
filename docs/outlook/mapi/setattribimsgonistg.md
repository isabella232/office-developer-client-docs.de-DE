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
ms.openlocfilehash: e8a0daa2afe2397f39b7f37a31ef718ba65a3350
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795513"
---
# <a name="setattribimsgonistg"></a><span data-ttu-id="488b9-103">SetAttribIMsgOnIStg</span><span class="sxs-lookup"><span data-stu-id="488b9-103">SetAttribIMsgOnIStg</span></span>

  
  
<span data-ttu-id="488b9-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="488b9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="488b9-105">Ändert Attribute der Eigenschaften für ein [IMessage](imessageimapiprop.md) -Objekt, das von der Funktion [OpenIMsgOnIStg](openimsgonistg.md) bereitgestellt wird, oder legt diesen fest an.</span><span class="sxs-lookup"><span data-stu-id="488b9-105">Sets or alters attributes of properties on an [IMessage](imessageimapiprop.md) object supplied by the [OpenIMsgOnIStg](openimsgonistg.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="488b9-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="488b9-106">Header file:</span></span>  <br/> |<span data-ttu-id="488b9-107">IMessage.h</span><span class="sxs-lookup"><span data-stu-id="488b9-107">Imessage.h</span></span>  <br/> |
|<span data-ttu-id="488b9-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="488b9-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="488b9-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="488b9-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="488b9-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="488b9-110">Called by:</span></span>  <br/> |<span data-ttu-id="488b9-111">Clientanwendungen und Nachricht speichern-Anbieter</span><span class="sxs-lookup"><span data-stu-id="488b9-111">Client applications and message store providers</span></span>  <br/> |
   
```cpp
HRESULT SetAttribIMsgOnIStg(
  LPVOID lpObject,
  LPSPropTagArray lpPropTags,
  LPSPropAttrArray lpPropAttrs,
  LPSPropProblemArray FAR * lppPropProblems
);
```

## <a name="parameters"></a><span data-ttu-id="488b9-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="488b9-112">Parameters</span></span>

 <span data-ttu-id="488b9-113">_lpObject_</span><span class="sxs-lookup"><span data-stu-id="488b9-113">_lpObject_</span></span>
  
> <span data-ttu-id="488b9-114">[in] Zeiger auf das Objekt, für welche, das Eigenschaft Attribute festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="488b9-114">[in] Pointer to the object for which property attributes are being set.</span></span> 
    
 <span data-ttu-id="488b9-115">_lpPropTags_</span><span class="sxs-lookup"><span data-stu-id="488b9-115">_lpPropTags_</span></span>
  
> <span data-ttu-id="488b9-116">[in] Zeiger auf eine [SPropTagArray](sproptagarray.md) -Struktur, die mit einem Array von Eigenschaftentags, der angibt, der Eigenschaften für die Eigenschaft Attribute festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="488b9-116">[in] Pointer to an [SPropTagArray](sproptagarray.md) structure containing an array of property tags indicating the properties for which property attributes are being set.</span></span> 
    
 <span data-ttu-id="488b9-117">_lpPropAttrs_</span><span class="sxs-lookup"><span data-stu-id="488b9-117">_lpPropAttrs_</span></span>
  
> <span data-ttu-id="488b9-118">[in] Zeiger auf eine [SPropAttrArray](spropattrarray.md) -Struktur mit den Eigenschaftsattributen festlegen.</span><span class="sxs-lookup"><span data-stu-id="488b9-118">[in] Pointer to an [SPropAttrArray](spropattrarray.md) structure listing the property attributes to set.</span></span> 
    
 <span data-ttu-id="488b9-119">_lppPropProblems_</span><span class="sxs-lookup"><span data-stu-id="488b9-119">_lppPropProblems_</span></span>
  
> <span data-ttu-id="488b9-120">[out] Zeiger auf das zurückgegebene [SPropProblemArray](spropproblemarray.md) -Struktur mit einem Satz von Eigenschaft Probleme.</span><span class="sxs-lookup"><span data-stu-id="488b9-120">[out] Pointer to the returned [SPropProblemArray](spropproblemarray.md) structure containing a set of property problems.</span></span> <span data-ttu-id="488b9-121">Diese Struktur identifiziert Probleme, wenn **SetAttribIMsgOnIStg** einige Eigenschaften festlegen können, jedoch nicht alle wurde.</span><span class="sxs-lookup"><span data-stu-id="488b9-121">This structure identifies problems encountered if **SetAttribIMsgOnIStg** has been able to set some properties, but not all.</span></span> <span data-ttu-id="488b9-122">Wenn ein Zeiger auf NULL in der _LppPropProblems_ -Parameter übergeben wird, wird kein Problem Array-Eigenschaft zurückgegeben, selbst wenn einige Eigenschaften nicht festgelegt wurden.</span><span class="sxs-lookup"><span data-stu-id="488b9-122">If a pointer to NULL is passed in the  _lppPropProblems_ parameter, no property problem array is returned even if some properties were not set.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="488b9-123">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="488b9-123">Return value</span></span>

<span data-ttu-id="488b9-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="488b9-124">S_OK</span></span> 
  
> <span data-ttu-id="488b9-125">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="488b9-125">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="488b9-126">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="488b9-126">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="488b9-127">Der Aufruf war insgesamt erfolgreich, aber eine oder mehrere Eigenschaften konnte nicht zugegriffen werden und mit der Eigenschaftentyp PT_ERROR zurückgegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="488b9-127">The call succeeded overall, but one or more properties could not be accessed and were returned with a property type of PT_ERROR.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="488b9-128">Hinweise</span><span class="sxs-lookup"><span data-stu-id="488b9-128">Remarks</span></span>

<span data-ttu-id="488b9-129">Eigenschaftsattribute nur auf Property-Objekte, d. h., durch Implementieren Objekte zugegriffen werden können die [IMAPIProp: IUnknown](imapipropiunknown.md) Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="488b9-129">Property attributes can only be accessed on property objects, that is, objects implementing the [IMAPIProp : IUnknown](imapipropiunknown.md) interface.</span></span> <span data-ttu-id="488b9-130">MAPI-Eigenschaften für ein OLE-Objekt strukturierter Speicher zur Verfügung zu stellen, [OpenIMsgOnIStg](openimsgonistg.md) erstellt eine [IMessage: IMAPIProp](imessageimapiprop.md) Objekt auf der Basis der OLE- **IStorage** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="488b9-130">To make MAPI properties available on an OLE structured storage object, [OpenIMsgOnIStg](openimsgonistg.md) builds an [IMessage : IMAPIProp](imessageimapiprop.md) object on top of the OLE **IStorage** object.</span></span> <span data-ttu-id="488b9-131">Die Eigenschaftenattribute für solche Objekte können festgelegt oder mit **SetAttribIMsgOnIStg** geändert und mit [GetAttribIMsgOnIStg](getattribimsgonistg.md)abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="488b9-131">The property attributes on such objects can be set or altered with **SetAttribIMsgOnIStg** and retrieved with [GetAttribIMsgOnIStg](getattribimsgonistg.md).</span></span> 
  
 <span data-ttu-id="488b9-132">**Hinweis** **GetAttribIMsgOnIStg** und **SetAttribIMsgOnIStg** nicht für alle Objekte, die **IMessage** eingesetzt werden.</span><span class="sxs-lookup"><span data-stu-id="488b9-132">**Note** **GetAttribIMsgOnIStg** and **SetAttribIMsgOnIStg** do not operate on all **IMessage** objects.</span></span> <span data-ttu-id="488b9-133">Sie sind nur für **IMessage**- auf - von **OpenIMsgOnIStg**zurückgegebene **IStorage** Objekte gültig.</span><span class="sxs-lookup"><span data-stu-id="488b9-133">They are only valid for **IMessage**-on- **IStorage** objects returned by **OpenIMsgOnIStg**.</span></span> 
  
<span data-ttu-id="488b9-134">In den _LpPropAttrs_ -Parameter müssen der Anzahl und die Position der Attribute der Anzahl und die Position der Eigenschaftentags im _LpPropTags_ -Parameter übergeben übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="488b9-134">In the  _lpPropAttrs_ parameter, the number and position of the attributes must match the number and position of the property tags passed in the  _lpPropTags_ parameter.</span></span> 
  
<span data-ttu-id="488b9-135">Die **SetAttribIMsgOnIStg** -Funktion wird verwendet, um Nachrichteneigenschaften schreibgeschützt, wenn das Schema **IMessage** erforderlich zu machen.</span><span class="sxs-lookup"><span data-stu-id="488b9-135">The **SetAttribIMsgOnIStg** function is used to make message properties read-only when required by the **IMessage** schema.</span></span> <span data-ttu-id="488b9-136">Der Nachricht Store Beispielanbieter verwendet sie für diesen Zweck.</span><span class="sxs-lookup"><span data-stu-id="488b9-136">The sample message store provider uses it for this purpose.</span></span> <span data-ttu-id="488b9-137">Weitere Informationen finden Sie unter [Nachrichten](mapi-messages.md).</span><span class="sxs-lookup"><span data-stu-id="488b9-137">For more information, see [Messages](mapi-messages.md).</span></span> 
  

