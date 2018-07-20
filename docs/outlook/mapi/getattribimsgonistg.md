---
title: GetAttribIMsgOnIStg
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.GetAttribIMsgOnIStg
api_type:
- COM
ms.assetid: bb27b28a-b2bd-4d4a-b0bb-0692f3de8e16
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: ddb6d692a8e76a9c24affc3af9f612a6f1c0d769
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791778"
---
# <a name="getattribimsgonistg"></a><span data-ttu-id="0f618-103">GetAttribIMsgOnIStg</span><span class="sxs-lookup"><span data-stu-id="0f618-103">GetAttribIMsgOnIStg</span></span>

  
  
<span data-ttu-id="0f618-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0f618-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0f618-105">Ruft Attribute der Eigenschaften für ein [IMessage](imessageimapiprop.md) -Objekt, das von der Funktion [OpenIMsgOnIStg](openimsgonistg.md) bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="0f618-105">Retrieves attributes of properties on an [IMessage](imessageimapiprop.md) object supplied by the [OpenIMsgOnIStg](openimsgonistg.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0f618-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="0f618-106">Header file:</span></span>  <br/> |<span data-ttu-id="0f618-107">IMessage.h</span><span class="sxs-lookup"><span data-stu-id="0f618-107">Imessage.h</span></span>  <br/> |
|<span data-ttu-id="0f618-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="0f618-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="0f618-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="0f618-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="0f618-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="0f618-110">Called by:</span></span>  <br/> |<span data-ttu-id="0f618-111">Clientanwendungen und Nachricht speichern-Anbieter</span><span class="sxs-lookup"><span data-stu-id="0f618-111">Client applications and message store providers</span></span>  <br/> |
   
```cpp
HRESULT GetAttribIMsgOnIStg(
  LPVOID lpObject,
  LPSPropTagArray lpPropTagArray,
  LPSPropAttrArray FAR * lppPropAttrArray
);
```

## <a name="parameters"></a><span data-ttu-id="0f618-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="0f618-112">Parameters</span></span>

 <span data-ttu-id="0f618-113">_lpObject_</span><span class="sxs-lookup"><span data-stu-id="0f618-113">_lpObject_</span></span>
  
> <span data-ttu-id="0f618-114">[in] Zeiger auf ein **IMessage** -Objekt, das von der Funktion [OpenIMsgOnIStg](openimsgonistg.md) abgerufen.</span><span class="sxs-lookup"><span data-stu-id="0f618-114">[in] Pointer to an **IMessage** object obtained from the [OpenIMsgOnIStg](openimsgonistg.md) function.</span></span> 
    
 <span data-ttu-id="0f618-115">_lpPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="0f618-115">_lpPropTagArray_</span></span>
  
> <span data-ttu-id="0f618-116">[in] Zeiger auf eine [SPropTagArray](sproptagarray.md) -Struktur, die ein Array von Eigenschaftentags enthält, der angibt, der Eigenschaften für die Attribute sind abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="0f618-116">[in] Pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags indicating the properties for which attributes are to be retrieved.</span></span> 
    
 <span data-ttu-id="0f618-117">_lppPropAttrArray_</span><span class="sxs-lookup"><span data-stu-id="0f618-117">_lppPropAttrArray_</span></span>
  
> <span data-ttu-id="0f618-118">[out] Zeiger auf einen Zeiger auf das zurückgegebene [SPropAttrArray](spropattrarray.md) -Struktur, die abgerufene Eigenschaftenattribute enthält.</span><span class="sxs-lookup"><span data-stu-id="0f618-118">[out] Pointer to a pointer to the returned [SPropAttrArray](spropattrarray.md) structure that contains the retrieved property attributes.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="0f618-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0f618-119">Return value</span></span>

<span data-ttu-id="0f618-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="0f618-120">S_OK</span></span> 
  
> <span data-ttu-id="0f618-121">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zurückgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="0f618-121">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="0f618-122">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="0f618-122">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="0f618-123">Der Aufruf war insgesamt erfolgreich, aber eine oder mehrere Eigenschaften konnte nicht zugegriffen werden und mit der Eigenschaftentyp PT_ERROR zurückgegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="0f618-123">The call succeeded overall, but one or more properties could not be accessed and were returned with a property type of PT_ERROR.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0f618-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0f618-124">Remarks</span></span>

<span data-ttu-id="0f618-125">Eigenschaftsattribute nur auf Property-Objekte, d. h., durch Implementieren Objekte zugegriffen werden können die [IMAPIProp: IUnknown](imapipropiunknown.md) Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="0f618-125">Property attributes can only be accessed on property objects, that is, objects implementing the [IMAPIProp : IUnknown](imapipropiunknown.md) interface.</span></span> <span data-ttu-id="0f618-126">MAPI-Eigenschaften für ein OLE-Objekt strukturierter Speicher zur Verfügung zu stellen, [OpenIMsgOnIStg](openimsgonistg.md) erstellt eine [IMessage: IMAPIProp](imessageimapiprop.md) Objekt auf der Basis der OLE- **IStorage** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="0f618-126">To make MAPI properties available on an OLE structured storage object, [OpenIMsgOnIStg](openimsgonistg.md) builds an [IMessage : IMAPIProp](imessageimapiprop.md) object on top of the OLE **IStorage** object.</span></span> <span data-ttu-id="0f618-127">Die Eigenschaftenattribute für solche Objekte können festgelegt oder mit [SetAttribIMsgOnIStg](setattribimsgonistg.md) geändert und mit **GetAttribIMsgOnIStg**abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="0f618-127">The property attributes on such objects can be set or altered with [SetAttribIMsgOnIStg](setattribimsgonistg.md) and retrieved with **GetAttribIMsgOnIStg**.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="0f618-128">**GetAttribIMsgOnIStg** und **SetAttribIMsgOnIStg** nicht für alle Objekte, die **IMessage** eingesetzt werden.</span><span class="sxs-lookup"><span data-stu-id="0f618-128">**GetAttribIMsgOnIStg** and **SetAttribIMsgOnIStg** do not operate on all **IMessage** objects.</span></span> <span data-ttu-id="0f618-129">Sie sind nur für **IMessage**- auf - von **OpenIMsgOnIStg**zurückgegebene **IStorage** Objekte gültig.</span><span class="sxs-lookup"><span data-stu-id="0f618-129">They are only valid for **IMessage**-on- **IStorage** objects returned by **OpenIMsgOnIStg**.</span></span> 
  
<span data-ttu-id="0f618-130">Die Anzahl und die Positionen der Attribute im _LppPropAttrArray_ -Parameter entsprechen der Anzahl und die Positionen der Eigenschaftentags im _LpPropTagArray_ -Parameter.</span><span class="sxs-lookup"><span data-stu-id="0f618-130">The number and positions of the attributes in the  _lppPropAttrArray_ parameter correspond to the number and positions of the property tags in the  _lpPropTagArray_ parameter.</span></span> 
  

