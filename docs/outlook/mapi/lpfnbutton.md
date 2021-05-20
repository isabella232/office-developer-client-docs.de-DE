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
  
Definiert eine Rückruffunktion, die MAPI aufruft, um ein optionales Schaltflächensteuerelement in einem Adressbuchdialogfeld zu aktivieren. Diese Schaltfläche ist in der Regel eine **Schaltfläche Details.** 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Definierte Funktion implementiert von:  <br/> |Dienstanbieter  <br/> |
|Definierte Funktion, die von:  <br/> |MAPI  <br/> |
   
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
  
> [in] Handle der übergeordneten Fenster für alle Dialogfelder oder Fenster, die diese Funktion anzeigt.
    
 _lpvContext_
  
> [in] Zeiger auf einen beliebigen Wert, der an die Rückruffunktion übergeben wird, wenn MAPI ihn aufruft. Dieser Wert kann eine Für die Clientanwendung wichtige Adresse darstellen. In der Regel stellt  _lpvContext_ für C++-Code einen Zeiger auf ein C++-Objekt dar. 
    
 _cbEntryID_
  
> [in] Größe des Eintragsbezeichners in Bytes, auf den der  _lpSelection-Parameter_ verweist. 
    
 _lpSelection_
  
> [in] Zeiger auf den Eintragsbezeichner, der die Auswahl im Dialogfeld definiert.
    
 _ulFlags_
  
> [in] Reserviert. NULL muss sein.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
## <a name="remarks"></a>Hinweise

Clientanwendungen rufen eine Rückruffunktion basierend auf dem **LPFNBUTTON-Prototyp** auf, um eine Schaltfläche in einem Detaildialogfeld zu definieren. Der Client übergibt einen Zeiger an die Rückruffunktion in Aufrufen der [IAddrBook::D etails-Methode.](iaddrbook-details.md) 
  
Dienstanbieter rufen eine Hookfunktion basierend auf dem **LPFNBUTTON-Prototyp** auf, um eine Schaltfläche in einem Detaildialogfeld zu definieren. Der Anbieter übergibt einen Zeiger auf diese Hookfunktion in Aufrufen der [IMAPISupport::D etails-Methode.](imapisupport-details.md) 
  
In beiden Fällen ruft MAPI **LPFNBUTTON** auf, wenn das Dialogfeld angezeigt wird und der Benutzer die definierte Schaltfläche aus wählt. 
  
## <a name="see-also"></a>Siehe auch



[BuildDisplayTable](builddisplaytable.md)

