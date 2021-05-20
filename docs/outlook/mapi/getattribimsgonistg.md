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
ms.openlocfilehash: 16e85eabc067bd82f5fb89c917afaf2831c75673
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439996"
---
# <a name="getattribimsgonistg"></a><span data-ttu-id="a27e7-103">GetAttribIMsgOnIStg</span><span class="sxs-lookup"><span data-stu-id="a27e7-103">GetAttribIMsgOnIStg</span></span>

  
  
<span data-ttu-id="a27e7-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a27e7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a27e7-105">Ruft Attribute von Eigenschaften für ein [IMessage-Objekt](imessageimapiprop.md) ab, das von der [OpenIMsgOnIStg-Funktion bereitgestellt](openimsgonistg.md) wird.</span><span class="sxs-lookup"><span data-stu-id="a27e7-105">Retrieves attributes of properties on an [IMessage](imessageimapiprop.md) object supplied by the [OpenIMsgOnIStg](openimsgonistg.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a27e7-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="a27e7-106">Header file:</span></span>  <br/> |<span data-ttu-id="a27e7-107">Imessage.h</span><span class="sxs-lookup"><span data-stu-id="a27e7-107">Imessage.h</span></span>  <br/> |
|<span data-ttu-id="a27e7-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="a27e7-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="a27e7-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="a27e7-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="a27e7-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="a27e7-110">Called by:</span></span>  <br/> |<span data-ttu-id="a27e7-111">Clientanwendungen und Nachrichtenspeicheranbieter</span><span class="sxs-lookup"><span data-stu-id="a27e7-111">Client applications and message store providers</span></span>  <br/> |
   
```cpp
HRESULT GetAttribIMsgOnIStg(
  LPVOID lpObject,
  LPSPropTagArray lpPropTagArray,
  LPSPropAttrArray FAR * lppPropAttrArray
);
```

## <a name="parameters"></a><span data-ttu-id="a27e7-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="a27e7-112">Parameters</span></span>

 <span data-ttu-id="a27e7-113">_lpObject_</span><span class="sxs-lookup"><span data-stu-id="a27e7-113">_lpObject_</span></span>
  
> <span data-ttu-id="a27e7-114">[in] Zeiger auf ein **IMessage-Objekt,** das von der [OpenIMsgOnIStg-Funktion erhalten](openimsgonistg.md) wurde.</span><span class="sxs-lookup"><span data-stu-id="a27e7-114">[in] Pointer to an **IMessage** object obtained from the [OpenIMsgOnIStg](openimsgonistg.md) function.</span></span> 
    
 <span data-ttu-id="a27e7-115">_lpPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="a27e7-115">_lpPropTagArray_</span></span>
  
> <span data-ttu-id="a27e7-116">[in] Zeiger auf eine [SPropTagArray-Struktur,](sproptagarray.md) die ein Array von Eigenschaftstags enthält, die die Eigenschaften angeben, für die Attribute abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a27e7-116">[in] Pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags indicating the properties for which attributes are to be retrieved.</span></span> 
    
 <span data-ttu-id="a27e7-117">_lppPropAttrArray_</span><span class="sxs-lookup"><span data-stu-id="a27e7-117">_lppPropAttrArray_</span></span>
  
> <span data-ttu-id="a27e7-118">[out] Zeiger auf einen Zeiger auf die zurückgegebene [SPropAttrArray-Struktur,](spropattrarray.md) die die abgerufenen Eigenschaftsattribute enthält.</span><span class="sxs-lookup"><span data-stu-id="a27e7-118">[out] Pointer to a pointer to the returned [SPropAttrArray](spropattrarray.md) structure that contains the retrieved property attributes.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="a27e7-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a27e7-119">Return value</span></span>

<span data-ttu-id="a27e7-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="a27e7-120">S_OK</span></span> 
  
> <span data-ttu-id="a27e7-121">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="a27e7-121">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="a27e7-122">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="a27e7-122">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="a27e7-123">Der Aufruf war insgesamt erfolgreich, aber auf eine oder mehrere Eigenschaften konnte nicht zugegriffen werden und wurde mit dem Eigenschaftstyp PT_ERROR.</span><span class="sxs-lookup"><span data-stu-id="a27e7-123">The call succeeded overall, but one or more properties could not be accessed and were returned with a property type of PT_ERROR.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a27e7-124">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a27e7-124">Remarks</span></span>

<span data-ttu-id="a27e7-125">Auf Eigenschaftsattribute kann nur auf Eigenschaftsobjekte zugegriffen werden, d. h. auf Objekte, die die [IMAPIProp : IUnknown-Schnittstelle](imapipropiunknown.md) implementieren.</span><span class="sxs-lookup"><span data-stu-id="a27e7-125">Property attributes can only be accessed on property objects, that is, objects implementing the [IMAPIProp : IUnknown](imapipropiunknown.md) interface.</span></span> <span data-ttu-id="a27e7-126">Um MAPI-Eigenschaften für ein strukturiertes OLE-Speicherobjekt verfügbar zu machen, erstellt [OpenIMsgOnIStg](openimsgonistg.md) ein [IMessage : IMAPIProp-Objekt](imessageimapiprop.md) über dem OLE **IStorage-Objekt.**</span><span class="sxs-lookup"><span data-stu-id="a27e7-126">To make MAPI properties available on an OLE structured storage object, [OpenIMsgOnIStg](openimsgonistg.md) builds an [IMessage : IMAPIProp](imessageimapiprop.md) object on top of the OLE **IStorage** object.</span></span> <span data-ttu-id="a27e7-127">Die Eigenschaftenattribute für solche Objekte können mit [SetAttribIMsgOnIStg](setattribimsgonistg.md) festgelegt oder geändert und mit **GetAttribIMsgOnIStg abgerufen werden.**</span><span class="sxs-lookup"><span data-stu-id="a27e7-127">The property attributes on such objects can be set or altered with [SetAttribIMsgOnIStg](setattribimsgonistg.md) and retrieved with **GetAttribIMsgOnIStg**.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="a27e7-128">**GetAttribIMsgOnIStg** und **SetAttribIMsgOnIStg** funktionieren nicht für alle **IMessage-Objekte.**</span><span class="sxs-lookup"><span data-stu-id="a27e7-128">**GetAttribIMsgOnIStg** and **SetAttribIMsgOnIStg** do not operate on all **IMessage** objects.</span></span> <span data-ttu-id="a27e7-129">Sie sind nur gültig für **IMessage** **-on-IStorage-Objekte,** die von **OpenIMsgOnIStg zurückgegeben werden.**</span><span class="sxs-lookup"><span data-stu-id="a27e7-129">They are only valid for **IMessage**-on- **IStorage** objects returned by **OpenIMsgOnIStg**.</span></span> 
  
<span data-ttu-id="a27e7-130">Die Anzahl und die Positionen der Attribute im _lppPropAttrArray-Parameter_ entsprechen der Anzahl und position der Eigenschaftstags im _lpPropTagArray-Parameter._</span><span class="sxs-lookup"><span data-stu-id="a27e7-130">The number and positions of the attributes in the  _lppPropAttrArray_ parameter correspond to the number and positions of the property tags in the  _lpPropTagArray_ parameter.</span></span> 
  

