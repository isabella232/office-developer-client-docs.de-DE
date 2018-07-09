---
title: IProxyStoreObject
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProxyStoreObject
api_type:
- COM
ms.assetid: 567bede4-39a3-bfb4-af85-ba678e2cf4a5
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: f6566f567c228b6416a64dbd58653561bb592e6d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792794"
---
# <a name="iproxystoreobject"></a><span data-ttu-id="c1494-103">IProxyStoreObject</span><span class="sxs-lookup"><span data-stu-id="c1494-103">IProxyStoreObject</span></span>

  
  
<span data-ttu-id="c1494-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c1494-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c1494-105">Stellt ein Internet Message Access Protocol (IMAP) Store-Objekt, das seit allein stehenden und, die ermöglicht den Zugriff auf Elemente in der Persönliche Ordner-Datei (PST) ohne Synchronisation aufrufen und die Elemente herunterladen.</span><span class="sxs-lookup"><span data-stu-id="c1494-105">Provides an Internet Message Access Protocol (IMAP) store object that has been unwrapped and that allows access to items in the Personal Folders file (PST) without invoking synchronization and downloading the items.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="c1494-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="c1494-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c1494-107">Vererbte Berechtigungen aus:</span><span class="sxs-lookup"><span data-stu-id="c1494-107">Inherited from:</span></span>  <br/> |[<span data-ttu-id="c1494-108">IUnknown</span><span class="sxs-lookup"><span data-stu-id="c1494-108">IUnknown</span></span>](http://msdn.microsoft.com/de-de/library/ms680509%28v=VS.85%29.aspx) <br/> |
|<span data-ttu-id="c1494-109">Bereitgestellt von:</span><span class="sxs-lookup"><span data-stu-id="c1494-109">Provided By:</span></span>  <br/> |<span data-ttu-id="c1494-110">Nachricht Speicheranbieter</span><span class="sxs-lookup"><span data-stu-id="c1494-110">Message store provider</span></span>  <br/> |
|<span data-ttu-id="c1494-111">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="c1494-111">Interface identifier:</span></span>  <br/> |<span data-ttu-id="c1494-112">**IID_IProxyStoreObject**</span><span class="sxs-lookup"><span data-stu-id="c1494-112">**IID_IProxyStoreObject**</span></span> <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="c1494-113">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="c1494-113">Vtable order</span></span>

|||
|:-----|:-----|
| <span data-ttu-id="c1494-114">*Platzhalter-member*</span><span class="sxs-lookup"><span data-stu-id="c1494-114">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="c1494-115">*Nicht unterstützte oder dokumentiert.*</span><span class="sxs-lookup"><span data-stu-id="c1494-115">*Not supported or documented.*</span></span>  <br/> |
|[<span data-ttu-id="c1494-116">IProxyStoreObject::UnwrapNoRef</span><span class="sxs-lookup"><span data-stu-id="c1494-116">IProxyStoreObject::UnwrapNoRef</span></span>](iproxystoreobject-unwrapnoref.md) <br/> |<span data-ttu-id="c1494-117">Ruft einen Zeiger auf ein allein stehenden IMAP-Speicher ab.</span><span class="sxs-lookup"><span data-stu-id="c1494-117">Gets a pointer to an unwrapped IMAP store.</span></span>  <br/> |
| <span data-ttu-id="c1494-118">*Platzhalter-member*</span><span class="sxs-lookup"><span data-stu-id="c1494-118">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="c1494-119">*Nicht unterstützte oder dokumentiert.*</span><span class="sxs-lookup"><span data-stu-id="c1494-119">*Not supported or documented.*</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c1494-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c1494-120">Remarks</span></span>

<span data-ttu-id="c1494-121">Rufen Sie [QueryInterface](http://msdn.microsoft.com/de-de/library/ms682521%28v=VS.85%29.aspx) in der Quelle Nachrichtenspeicher die **IProxyStoreObject** -Schnittstelle abzurufen.</span><span class="sxs-lookup"><span data-stu-id="c1494-121">Call [IUnknown::QueryInterface](http://msdn.microsoft.com/de-de/library/ms682521%28v=VS.85%29.aspx) on the source message store to obtain the **IProxyStoreObject** interface.</span></span> <span data-ttu-id="c1494-122">Rufen Sie dann **IProxyStoreObject::UnwrapNoRef** , um das allein stehenden Store-Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="c1494-122">Then call **IProxyStoreObject::UnwrapNoRef** to obtain the unwrapped store object.</span></span> <span data-ttu-id="c1494-123">Wenn **QueryInterface** den Fehler **MAPI_E_INTERFACE_NOT_SUPPORTED**zurückgibt, wurde der Store nicht umgebrochen.</span><span class="sxs-lookup"><span data-stu-id="c1494-123">If **QueryInterface** returns the error **MAPI_E_INTERFACE_NOT_SUPPORTED**, then the store has not been wrapped.</span></span> 
  
<span data-ttu-id="c1494-124">Da **UnwrapNoRef** nicht den Referenzzähler für diese neuen Zeiger auf das allein stehenden Store-Objekt, nach dem erfolgreichen Aufruf von **UnwrapNoRef**erhöht, sollten Sie [IUnknown:: AddRef](http://msdn.microsoft.com/de-de/library/ms691379%28v=VS.85%29.aspx) zum Verwalten von des Referenzzähler aufrufen.</span><span class="sxs-lookup"><span data-stu-id="c1494-124">Because **UnwrapNoRef** does not increment the reference count for this new pointer to the unwrapped store object, after successfully calling **UnwrapNoRef**, you should call [IUnknown::AddRef](http://msdn.microsoft.com/de-de/library/ms691379%28v=VS.85%29.aspx) to maintain the reference count.</span></span> 
  

