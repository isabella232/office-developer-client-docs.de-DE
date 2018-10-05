---
title: IProxyStoreObjectUnwrapNoRef
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProxyStoreObject.UnwrapNoRef
api_type:
- COM
ms.assetid: 1122b6e0-e7e1-e68a-e090-435777343d04
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: ef9f506c1a95fec86c7f092b0299198e6149d3ba
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382932"
---
# <a name="iproxystoreobjectunwrapnoref"></a><span data-ttu-id="b69a0-103">IProxyStoreObject::UnwrapNoRef</span><span class="sxs-lookup"><span data-stu-id="b69a0-103">IProxyStoreObject::UnwrapNoRef</span></span>

  
  
<span data-ttu-id="b69a0-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b69a0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b69a0-105">Ruft einen Zeiger auf ein allein stehenden Internet Message Access Protocol (IMAP) Store-Objekt, das Zugriff auf die zugrunde liegende Persönliche Ordner-Datei (PST) bietet ohne Synchronisation aufrufen und die Elemente herunterladen.</span><span class="sxs-lookup"><span data-stu-id="b69a0-105">Gets a pointer to an unwrapped Internet Message Access Protocol (IMAP) store object that provides access to the underlying Personal Folders file (PST) without invoking synchronization and downloading the items.</span></span>
  
```cpp
HRESULT IProxyStoreObject::UnwrapNoRef (     LPVOID *ppvObject ); 
```

## <a name="parameters"></a><span data-ttu-id="b69a0-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b69a0-106">Parameters</span></span>

 <span data-ttu-id="b69a0-107">_ppvObject_</span><span class="sxs-lookup"><span data-stu-id="b69a0-107">_ppvObject_</span></span>
  
> <span data-ttu-id="b69a0-108">[out] Zeiger auf eine [IMsgStore: IMAPIProp](imsgstoreimapiprop.md) allein stehenden ist Store-Objekt.</span><span class="sxs-lookup"><span data-stu-id="b69a0-108">[out] Pointer to an [IMsgStore : IMAPIProp](imsgstoreimapiprop.md) store object that is unwrapped.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="b69a0-109">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="b69a0-109">Return values</span></span>

<span data-ttu-id="b69a0-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="b69a0-110">S_OK</span></span>
  
- <span data-ttu-id="b69a0-111">Der Aufruf war erfolgreich, und ein Zeiger auf eine allein stehenden-Schnittstelle in _PpvObject_zurückgegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="b69a0-111">The call was successful and a pointer to an unwrapped interface has been returned in  _ppvObject_.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b69a0-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b69a0-112">Remarks</span></span>

<span data-ttu-id="b69a0-113">Ohne den ersten Entpacken einen IMAP-Speicher, kann den Zugriff auf eine Nachricht im Speicher eine Synchronisierung erzwingen, die versucht, laden Sie die gesamte Nachricht.</span><span class="sxs-lookup"><span data-stu-id="b69a0-113">Without first unwrapping an IMAP store, accessing a message in the store can force a synchronization that attempts to download the entire message.</span></span> <span data-ttu-id="b69a0-114">Ermöglicht den Zugriff auf die Nachricht im aktuellen Zustand ohne Auslösen der Download mit den allein stehenden Speicher.</span><span class="sxs-lookup"><span data-stu-id="b69a0-114">Using the unwrapped store allows access to the message in its current state without triggering a download.</span></span>
  
<span data-ttu-id="b69a0-115">Da **UnwrapNoRef** nicht den Referenzzähler für diese neuen Zeiger auf das allein stehenden Store-Objekt, nach dem erfolgreichen Aufruf von **UnwrapNoRef**erhöht, sollten Sie [IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) zum Verwalten von des Referenzzähler aufrufen.</span><span class="sxs-lookup"><span data-stu-id="b69a0-115">Because **UnwrapNoRef** does not increment the reference count for this new pointer to the unwrapped store object, after successfully calling **UnwrapNoRef**, you should call [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) to maintain the reference count.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b69a0-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b69a0-116">See also</span></span>



[<span data-ttu-id="b69a0-117">IProxyStoreObject</span><span class="sxs-lookup"><span data-stu-id="b69a0-117">IProxyStoreObject</span></span>](iproxystoreobject.md)

