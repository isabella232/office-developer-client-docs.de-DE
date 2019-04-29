---
title: LPFNBUTTON
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.LPFNBUTTON
api_type:
- COM
ms.assetid: cb91ae1d-1ea8-4f02-a1f1-f2a356a71477
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 804bd23a148b942fd4580d1e3465fc1f65ff5978
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431512"
---
# <a name="lpfnbutton"></a>LPFNBUTTON

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Definiert eine Rückruffunktion, die von MAPI aufgerufen wird, um ein optionales Schaltflächen-Steuerelement in einem Adressbuch Dialogfeld zu aktivieren. Diese Schaltfläche ist in der Regel eine Schaltfläche **Details** . 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs. h  <br/> |
|Definierte Funktion, implementiert von:  <br/> |Dienstanbieter  <br/> |
|Definierte Funktion, aufgerufen von:  <br/> |MAPI  <br/> |
   
```cpp
SCODE (STDMETHODCALLTYPE FAR * LPFNBUTTON)(
  ULONG_PTR ulUIParam,
  LPVOID lpvContext,
  ULONG cbEntryID,
  LPENTRYID lpSelection,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameter

 _ulUIParam_
  
> in Handle der übergeordneten Fenster für alle Dialogfelder oder Windows, die diese Funktion anzeigt.
    
 _lpvContext_
  
> in Zeiger auf einen beliebigen Wert, der beim Aufrufen von MAPI an die Rückruffunktion übergeben wird. Dieser Wert kann eine für die Clientanwendung bedeutsame Adresse darstellen. Für C++-Code stellt _LpvContext_ in der Regel einen Zeiger auf ein c++-Objekt dar. 
    
 _cbEntryID_
  
> in Größe (in Bytes) der Eintrags-ID, auf die durch den _lpSelection_ -Parameter verwiesen wird. 
    
 _lpSelection_
  
> in Zeiger auf die Eintrags-ID, die die Auswahl im Dialogfeld definiert.
    
 _ulFlags_
  
> [in] Reserviert. NULL muss sein.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
## <a name="remarks"></a>Bemerkungen

Client Anwendungen rufen eine Rückruffunktion auf der Grundlage des **LPFNBUTTON** -Prototyps auf, um eine Schaltfläche in einem Detail Dialogfeld zu definieren. Der Client übergibt einen Zeiger auf die Rückruffunktion in Aufrufen der [IAddrBook::D ails](iaddrbook-details.md) -Methode. 
  
Dienstanbieter rufen eine Hookfunktion auf der Grundlage des **LPFNBUTTON** -Prototyps auf, um eine Schaltfläche in einem Detail Dialogfeld zu definieren. Der Anbieter übergibt einen Zeiger auf diese Hookfunktion in Aufrufen der [IMAPISupport::D ails](imapisupport-details.md) -Methode. 
  
Wenn das Dialogfeld angezeigt wird und der Benutzer die definierte Schaltfläche auswählt, ruft MAPI in beiden Fällen **LPFNBUTTON**auf. 
  
## <a name="see-also"></a>Siehe auch



[BuildDisplayTable](builddisplaytable.md)

