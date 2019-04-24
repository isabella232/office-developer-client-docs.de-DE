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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 16e85eabc067bd82f5fb89c917afaf2831c75673
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300469"
---
# <a name="getattribimsgonistg"></a><span data-ttu-id="71643-103">GetAttribIMsgOnIStg</span><span class="sxs-lookup"><span data-stu-id="71643-103">GetAttribIMsgOnIStg</span></span>

  
  
<span data-ttu-id="71643-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="71643-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="71643-105">Ruft Attribute von Eigenschaften für ein [IMessage](imessageimapiprop.md) -Objekt ab, das von der [OpenIMsgOnIStg](openimsgonistg.md) -Funktion bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="71643-105">Retrieves attributes of properties on an [IMessage](imessageimapiprop.md) object supplied by the [OpenIMsgOnIStg](openimsgonistg.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="71643-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="71643-106">Header file:</span></span>  <br/> |<span data-ttu-id="71643-107">IMessage. h</span><span class="sxs-lookup"><span data-stu-id="71643-107">Imessage.h</span></span>  <br/> |
|<span data-ttu-id="71643-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="71643-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="71643-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="71643-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="71643-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="71643-110">Called by:</span></span>  <br/> |<span data-ttu-id="71643-111">Client Anwendungen und Nachrichtenspeicher Anbieter</span><span class="sxs-lookup"><span data-stu-id="71643-111">Client applications and message store providers</span></span>  <br/> |
   
```cpp
HRESULT GetAttribIMsgOnIStg(
  LPVOID lpObject,
  LPSPropTagArray lpPropTagArray,
  LPSPropAttrArray FAR * lppPropAttrArray
);
```

## <a name="parameters"></a><span data-ttu-id="71643-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="71643-112">Parameters</span></span>

 <span data-ttu-id="71643-113">_lpObject_</span><span class="sxs-lookup"><span data-stu-id="71643-113">_lpObject_</span></span>
  
> <span data-ttu-id="71643-114">in Zeiger auf ein **IMessage** -Objekt, das von der [OpenIMsgOnIStg](openimsgonistg.md) -Funktion abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="71643-114">[in] Pointer to an **IMessage** object obtained from the [OpenIMsgOnIStg](openimsgonistg.md) function.</span></span> 
    
 <span data-ttu-id="71643-115">_lpPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="71643-115">_lpPropTagArray_</span></span>
  
> <span data-ttu-id="71643-116">in Zeiger auf eine [SPropTagArray](sproptagarray.md) -Struktur, die ein Array von Property-Tags enthält, die die Eigenschaften angeben, für die Attribute abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="71643-116">[in] Pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags indicating the properties for which attributes are to be retrieved.</span></span> 
    
 <span data-ttu-id="71643-117">_lppPropAttrArray_</span><span class="sxs-lookup"><span data-stu-id="71643-117">_lppPropAttrArray_</span></span>
  
> <span data-ttu-id="71643-118">Out Zeiger auf einen Zeiger auf die zurückgegebene [SPropAttrArray](spropattrarray.md) -Struktur, die die abgerufenen Eigenschaftsattribute enthält.</span><span class="sxs-lookup"><span data-stu-id="71643-118">[out] Pointer to a pointer to the returned [SPropAttrArray](spropattrarray.md) structure that contains the retrieved property attributes.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="71643-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="71643-119">Return value</span></span>

<span data-ttu-id="71643-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="71643-120">S_OK</span></span> 
  
> <span data-ttu-id="71643-121">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="71643-121">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="71643-122">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="71643-122">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="71643-123">Der Aufruf war insgesamt erfolgreich, aber auf eine oder mehrere Eigenschaften konnte nicht zugegriffen werden, und es wurde ein Eigenschaftentyp von PT_ERROR zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="71643-123">The call succeeded overall, but one or more properties could not be accessed and were returned with a property type of PT_ERROR.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="71643-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="71643-124">Remarks</span></span>

<span data-ttu-id="71643-125">Auf Eigenschaftsattribute kann nur über Property-Objekte zugegriffen werden, also auf Objekte, die die [IMAPIProp: IUnknown](imapipropiunknown.md) -Schnittstelle implementieren.</span><span class="sxs-lookup"><span data-stu-id="71643-125">Property attributes can only be accessed on property objects, that is, objects implementing the [IMAPIProp : IUnknown](imapipropiunknown.md) interface.</span></span> <span data-ttu-id="71643-126">Um MAPI-Eigenschaften für ein OLE Structured Storage-Objekt verfügbar zu machen, erstellt [OpenIMsgOnIStg](openimsgonistg.md) ein [IMessage: IMAPIProp](imessageimapiprop.md) -Objekt über dem OLE- **IStorage** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="71643-126">To make MAPI properties available on an OLE structured storage object, [OpenIMsgOnIStg](openimsgonistg.md) builds an [IMessage : IMAPIProp](imessageimapiprop.md) object on top of the OLE **IStorage** object.</span></span> <span data-ttu-id="71643-127">Die Eigenschaftsattribute für solche Objekte können mit [SetAttribIMsgOnIStg](setattribimsgonistg.md) festgelegt oder geändert und mit **GetAttribIMsgOnIStg**abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="71643-127">The property attributes on such objects can be set or altered with [SetAttribIMsgOnIStg](setattribimsgonistg.md) and retrieved with **GetAttribIMsgOnIStg**.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="71643-128">**GetAttribIMsgOnIStg** und **SetAttribIMsgOnIStg** funktionieren nicht für alle **IMessage** -Objekte.</span><span class="sxs-lookup"><span data-stu-id="71643-128">**GetAttribIMsgOnIStg** and **SetAttribIMsgOnIStg** do not operate on all **IMessage** objects.</span></span> <span data-ttu-id="71643-129">Sie sind nur für **IMessage**-on- **IStorage** -Objekte gültig, die von **OpenIMsgOnIStg**zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="71643-129">They are only valid for **IMessage**-on- **IStorage** objects returned by **OpenIMsgOnIStg**.</span></span> 
  
<span data-ttu-id="71643-130">Die Anzahl und Position der Attribute im _lppPropAttrArray_ -Parameter entsprechen der Anzahl und Position der Property-Tags im _lpPropTagArray_ -Parameter.</span><span class="sxs-lookup"><span data-stu-id="71643-130">The number and positions of the attributes in the  _lppPropAttrArray_ parameter correspond to the number and positions of the property tags in the  _lpPropTagArray_ parameter.</span></span> 
  

