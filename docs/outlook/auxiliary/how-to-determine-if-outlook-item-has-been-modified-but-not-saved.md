---
title: Bestimmen Sie, ob ein Outlook-Element geändert, jedoch nicht gespeichert (Outlook-Zusatzreferenz) wurde
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 65fba557-5fb0-42de-8715-eccda1f3c648
description: In diesem Thema wird veranschaulicht, wie Sie die dispidFDirty -Dispatch-ID verwenden, rufen Sie die entsprechende Eigenschaft für ein Outlook-Element, um festzustellen, ob das Element geändert wurde und nicht gespeichert wurde noch.
ms.openlocfilehash: e66a23983a3cc19a7cb51d4b4c3b2c1cee58a793
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395553"
---
# <a name="determine-if-an-outlook-item-has-been-modified-but-not-saved-outlook-auxiliary-reference"></a>Bestimmen Sie, ob ein Outlook-Element geändert, jedoch nicht gespeichert (Outlook-Zusatzreferenz) wurde

In diesem Thema wird veranschaulicht, wie Sie die **dispidFDirty** -Dispatch-ID verwenden, rufen Sie die entsprechende Eigenschaft für ein Outlook-Element, um festzustellen, ob das Element geändert wurde und nicht gespeichert wurde noch. 
  
Item-Objekt können Sie die [IUnknown::QueryInterface](https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q_)) -Methode verwenden, um einen [IDispatch](https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) -Schnittstellenzeiger zu erhalten. Die Funktion im Thema `FIsItemDirty` akzeptiert einen **IDispatch** -Zeiger _Pdisp_als Eingabeparameter.  `FIsItemDirty` Ruft die [IDispatch:: Invoke](https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-invoke) -Methode, und geben **dispidFDirty** als Argument für den Parameter  _dispIdMember_ und die Flags  `DISPATCH_METHOD | DISPATCH_PROPERTYGET` für  _wFlags_, um zu überprüfen, ob das Element geändert wurde.  `FIsItemDirty`Gibt einen booleschen Wert (**true,** um anzugeben, dass das Element nicht gespeicherte Änderungen; enthält andernfalls **"false"**).
  
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

## <a name="see-also"></a>Siehe auch

- [Konstanten (Outlook exportierter APIs)](constants-outlook-exported-apis.md)

