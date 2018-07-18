---
title: Bestimmen Sie, ob ein Outlook-Element geändert, jedoch nicht gespeichert (Outlook-Zusatzreferenz) wurde
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 65fba557-5fb0-42de-8715-eccda1f3c648
description: In diesem Thema wird veranschaulicht, wie Sie die dispidFDirty -Dispatch-ID verwenden, rufen Sie die entsprechende Eigenschaft für ein Outlook-Element, um festzustellen, ob das Element geändert wurde und nicht gespeichert wurde noch.
ms.openlocfilehash: ece6ede368cf2ffb3b18575161fef4b3f132fdf0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790938"
---
# <a name="determine-if-an-outlook-item-has-been-modified-but-not-saved-outlook-auxiliary-reference"></a>Bestimmen Sie, ob ein Outlook-Element geändert, jedoch nicht gespeichert (Outlook-Zusatzreferenz) wurde

In diesem Thema wird veranschaulicht, wie Sie die **dispidFDirty** -Dispatch-ID verwenden, rufen Sie die entsprechende Eigenschaft für ein Outlook-Element, um festzustellen, ob das Element geändert wurde und nicht gespeichert wurde noch. 
  
Item-Objekt können Sie die [IUnknown::QueryInterface](http://msdn.microsoft.com/library/com.iunknown_queryinterface.aspx) -Methode verwenden, um einen [IDispatch](http://msdn.microsoft.com/library/ebbff4bc-36b2-4861-9efa-ffa45e013eb5%28Office.15%29.aspx) -Schnittstellenzeiger zu erhalten. Die Funktion im Thema `FIsItemDirty` akzeptiert einen **IDispatch** -Zeiger _Pdisp_als Eingabeparameter.  `FIsItemDirty` Ruft die [IDispatch:: Invoke](http://msdn.microsoft.com/library/964ade8e-9d8a-4d32-bd47-aa678912a54d%28Office.15%29.aspx) -Methode, und geben **dispidFDirty** als Argument für den Parameter  _dispIdMember_ und die Flags  `DISPATCH_METHOD | DISPATCH_PROPERTYGET` für  _wFlags_, um zu überprüfen, ob das Element geändert wurde.  `FIsItemDirty`Gibt einen booleschen Wert (**true,** um anzugeben, dass das Element nicht gespeicherte Änderungen; enthält andernfalls **"false"**).
  
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

