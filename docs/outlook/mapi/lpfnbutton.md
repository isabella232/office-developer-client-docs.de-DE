---
title: LPFNBUTTON
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.LPFNBUTTON
api_type:
- COM
ms.assetid: cb91ae1d-1ea8-4f02-a1f1-f2a356a71477
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 05cce66e06e32162abf6f3183ed9c7b94d24e9b7
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59556210"
---
# <a name="lpfnbutton"></a>LPFNBUTTON

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Definiert eine Rückruffunktion, die MAPI aufruft, um ein optionales Schaltflächensteuerelement in einem Adressbuchdialogfeld zu aktivieren. Diese Schaltfläche ist in der Regel eine **Schaltfläche "Details".** 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Definierte Funktion implementiert von:  <br/> |Dienstanbieter  <br/> |
|Definierte Funktion aufgerufen von:  <br/> |MAPI  <br/> |
   
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
  
> [in] Behandeln der übergeordneten Fenster für alle Dialogfelder oder Fenster, die von dieser Funktion angezeigt werden.
    
 _lpvContext_
  
> [in] Zeiger auf einen beliebigen Wert, der an die Rückruffunktion übergeben wird, wenn die MAPI sie aufruft. Dieser Wert kann eine Adresse darstellen, die für die Clientanwendung von Bedeutung ist. In der Regel stellt  _lpvContext_ für C++-Code einen Zeiger auf ein C++-Objekt dar. 
    
 _cbEntryID_
  
> [in] Größe (in Byte) des Eintragsbezeichners, auf den der  _lpSelection-Parameter_ verweist. 
    
 _lpSelection_
  
> [in] Zeiger auf den Eintragsbezeichner, der die Auswahl im Dialogfeld definiert.
    
 _ulFlags_
  
> [in] Reserviert. NULL muss sein.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
## <a name="remarks"></a>HinwBemerkungeneise

Clientanwendungen rufen eine Rückruffunktion auf der Grundlage des **LPFNBUTTON-Prototyps** auf, um eine Schaltfläche in einem Detaildialogfeld zu definieren. Der Client übergibt einen Zeiger an die Rückruffunktion in Aufrufen der [IAddrBook::D etails-Methode.](iaddrbook-details.md) 
  
Dienstanbieter rufen eine Hookfunktion basierend auf dem **LPFNBUTTON-Prototyp** auf, um eine Schaltfläche in einem Detaildialogfeld zu definieren. Der Anbieter übergibt einen Zeiger auf diese Hookfunktion in Aufrufen der [IMAPISupport::D etails-Methode.](imapisupport-details.md) 
  
In beiden Fällen ruft MAPI **LPFNBUTTON** auf, wenn das Dialogfeld angezeigt wird und der Benutzer die definierte Schaltfläche auswählt. 
  
## <a name="see-also"></a>Siehe auch



[BuildDisplayTable](builddisplaytable.md)

