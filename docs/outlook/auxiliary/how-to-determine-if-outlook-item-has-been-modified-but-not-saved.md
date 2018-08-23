---
title: Bestimmen Sie, ob ein Outlook-Element geändert, jedoch nicht gespeichert (Outlook-Zusatzreferenz) wurde
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 65fba557-5fb0-42de-8715-eccda1f3c648
description: In diesem Thema wird veranschaulicht, wie Sie die dispidFDirty -Dispatch-ID verwenden, rufen Sie die entsprechende Eigenschaft für ein Outlook-Element, um festzustellen, ob das Element geändert wurde und nicht gespeichert wurde noch.
ms.openlocfilehash: adaa0f72d427a5cfc98b93e8aa4403d5a76ecd9d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588097"
---
# <a name="determine-if-an-outlook-item-has-been-modified-but-not-saved-outlook-auxiliary-reference"></a><span data-ttu-id="064fa-103">Bestimmen Sie, ob ein Outlook-Element geändert, jedoch nicht gespeichert (Outlook-Zusatzreferenz) wurde</span><span class="sxs-lookup"><span data-stu-id="064fa-103">Determine if an Outlook item has been modified but not saved (Outlook Auxiliary Reference)</span></span>

<span data-ttu-id="064fa-104">In diesem Thema wird veranschaulicht, wie Sie die **dispidFDirty** -Dispatch-ID verwenden, rufen Sie die entsprechende Eigenschaft für ein Outlook-Element, um festzustellen, ob das Element geändert wurde und nicht gespeichert wurde noch.</span><span class="sxs-lookup"><span data-stu-id="064fa-104">This topic shows how to use the **dispidFDirty** dispatch ID to invoke the corresponding property on an Outlook item, to see whether the item has been modified and has not been saved.</span></span> 
  
<span data-ttu-id="064fa-105">Item-Objekt können Sie die [IUnknown::QueryInterface](https://docs.microsoft.com/en-us/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q_)) -Methode verwenden, um einen [IDispatch](https://docs.microsoft.com/en-us/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) -Schnittstellenzeiger zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="064fa-105">Given an item object, you can use the [IUnknown::QueryInterface](https://docs.microsoft.com/en-us/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q_)) method to obtain an [IDispatch](https://docs.microsoft.com/en-us/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) interface pointer.</span></span> <span data-ttu-id="064fa-106">Die Funktion im Thema `FIsItemDirty` akzeptiert einen **IDispatch** -Zeiger _Pdisp_als Eingabeparameter.</span><span class="sxs-lookup"><span data-stu-id="064fa-106">The function in the topic `FIsItemDirty` accepts an **IDispatch** pointer,  _pdisp_, as an input parameter.</span></span>  <span data-ttu-id="064fa-107">`FIsItemDirty` Ruft die [IDispatch:: Invoke](https://docs.microsoft.com/en-us/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-invoke) -Methode, und geben **dispidFDirty** als Argument für den Parameter  _dispIdMember_ und die Flags  `DISPATCH_METHOD | DISPATCH_PROPERTYGET` für  _wFlags_, um zu überprüfen, ob das Element geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="064fa-107">`FIsItemDirty` calls the [IDispatch::Invoke](https://docs.microsoft.com/en-us/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-invoke) method, specifying **dispidFDirty** as the argument for the  _dispIdMember_ parameter, and the flags  `DISPATCH_METHOD | DISPATCH_PROPERTYGET` for  _wFlags_, to verify whether the item has been modified.</span></span>  <span data-ttu-id="064fa-108">`FIsItemDirty`Gibt einen booleschen Wert (**true,** um anzugeben, dass das Element nicht gespeicherte Änderungen; enthält andernfalls **"false"**).</span><span class="sxs-lookup"><span data-stu-id="064fa-108">`FIsItemDirty` returns a Boolean value (**True** to indicate that the item has unsaved changes; otherwise, **False**).</span></span>
  
```cpp
bool FIsItemDirty(IDispatch *pdisp)
{
    DISPPARAMS dispparams;
    UINT uArgErr;
    HRESULT hr = S_OK;
    CComVariant varDirty;
    dispparams.rgvarg = 0;
    dispparams.cArgs = 0;
    dispparams.cNamedArgs = 0;
    dispparams.rgdispidNamedArgs = NULL;
    hr = pdisp->Invoke(dispidFDirty,
        IID_NULL,
        LOCALE_SYSTEM_DEFAULT,
        DISPATCH_METHOD | DISPATCH_PROPERTYGET,
        &amp;dispparams,
        &amp;varDirty,
        NULL,
        &amp;uArgErr);
    return SUCCEEDED(hr) &amp;&amp; varDirty.bVal;
}

```

## <a name="see-also"></a><span data-ttu-id="064fa-109">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="064fa-109">See also</span></span>

- [<span data-ttu-id="064fa-110">Konstanten (Outlook exportierter APIs)</span><span class="sxs-lookup"><span data-stu-id="064fa-110">Constants (Outlook exported APIs)</span></span>](constants-outlook-exported-apis.md)

