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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320153"
---
# <a name="iproxystoreobjectunwrapnoref"></a><span data-ttu-id="bb483-103">IProxyStoreObject::UnwrapNoRef</span><span class="sxs-lookup"><span data-stu-id="bb483-103">IProxyStoreObject::UnwrapNoRef</span></span>

  
  
<span data-ttu-id="bb483-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bb483-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bb483-105">Ruft einen Zeiger auf ein imAP (Unwraped Internet Message Access Protocol) gespeichertes Objekt ab, das Zugriff auf die zugrunde liegende Pst (Personal Folders File) ermöglicht, ohne die Synchronisierung aufrufen und die Elemente herunterladen zu müssen.</span><span class="sxs-lookup"><span data-stu-id="bb483-105">Gets a pointer to an unwrapped Internet Message Access Protocol (IMAP) store object that provides access to the underlying Personal Folders file (PST) without invoking synchronization and downloading the items.</span></span>
  
```cpp
HRESULT IProxyStoreObject::UnwrapNoRef (     LPVOID *ppvObject ); 
```

## <a name="parameters"></a><span data-ttu-id="bb483-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="bb483-106">Parameters</span></span>

 <span data-ttu-id="bb483-107">_ppvObject_</span><span class="sxs-lookup"><span data-stu-id="bb483-107">_ppvObject_</span></span>
  
> <span data-ttu-id="bb483-108">[out] Zeiger auf ein [IMsgStore : IMAPIProp](imsgstoreimapiprop.md) Store-Objekt, das entpackt ist.</span><span class="sxs-lookup"><span data-stu-id="bb483-108">[out] Pointer to an [IMsgStore : IMAPIProp](imsgstoreimapiprop.md) store object that is unwrapped.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="bb483-109">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="bb483-109">Return values</span></span>

<span data-ttu-id="bb483-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="bb483-110">S_OK</span></span>
  
- <span data-ttu-id="bb483-111">Der Aufruf war erfolgreich, und ein Zeiger auf eine entpackte Schnittstelle wurde in _ppvObject zurückgegeben._</span><span class="sxs-lookup"><span data-stu-id="bb483-111">The call was successful and a pointer to an unwrapped interface has been returned in  _ppvObject_.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="bb483-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="bb483-112">Remarks</span></span>

<span data-ttu-id="bb483-113">Ohne zunächst ein ImAP-Speicher zu entwrapping, kann der Zugriff auf eine Nachricht im Store eine Synchronisierung erzwingen, die versucht, die gesamte Nachricht herunterzuladen.</span><span class="sxs-lookup"><span data-stu-id="bb483-113">Without first unwrapping an IMAP store, accessing a message in the store can force a synchronization that attempts to download the entire message.</span></span> <span data-ttu-id="bb483-114">Die Verwendung des entpackten Speichers ermöglicht den Zugriff auf die Nachricht im aktuellen Status, ohne einen Download auszulösen.</span><span class="sxs-lookup"><span data-stu-id="bb483-114">Using the unwrapped store allows access to the message in its current state without triggering a download.</span></span>
  
<span data-ttu-id="bb483-115">Da **UnwrapNoRef** die Referenzanzahl für diesen neuen Zeiger nicht auf das nicht mehr ausgepackte Speicherobjekt erhöht, sollten Sie nach dem erfolgreichen Aufruf von **UnwrapNoRef** [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) aufrufen, um die Referenzanzahl zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="bb483-115">Because **UnwrapNoRef** does not increment the reference count for this new pointer to the unwrapped store object, after successfully calling **UnwrapNoRef**, you should call [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) to maintain the reference count.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="bb483-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bb483-116">See also</span></span>



[<span data-ttu-id="bb483-117">IProxyStoreObject</span><span class="sxs-lookup"><span data-stu-id="bb483-117">IProxyStoreObject</span></span>](iproxystoreobject.md)

