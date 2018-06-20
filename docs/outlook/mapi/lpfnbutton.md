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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: e1f15a5f031f5c5a9568b8a36722eaac011b814c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792902"
---
# <a name="lpfnbutton"></a>LPFNBUTTON

  
  
**Betrifft**: Outlook 
  
Definiert eine Rückruffunktion, die MAPI-aufrufen, um ein optional Schaltflächensteuerelement im Dialogfeld Adressbuch eine Adresse zu aktivieren. Diese Schaltfläche ist in der Regel eine Schaltfläche **Details** . 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Definierte Funktion von implementiert:  <br/> |Dienstanbieter  <br/> |
|Definierte Funktion aufgerufen:  <br/> |MAPI  <br/> |
   
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
  
> [in] Behandeln von der übergeordneten Windows für alle Dialogfelder oder Fenster, die diese Funktion zeigt.
    
 _lpvContext_
  
> [in] Zeiger auf einen beliebigen Wert wird an die Rückruffunktion übergeben, wenn MAPI aufgerufen. Dieser Wert kann eine an die Clientanwendung Vielfache von-Adresse dar. In der Regel stellt _LpvContext_ für C++-Code einen Zeiger auf ein C++-Objekt. 
    
 _cbEntryID_
  
> [in] Größe des Eintrags-ID, die auf das durch den Parameter _LpSelection_ in Bytes. 
    
 _lpSelection_
  
> [in] Zeiger auf die Eintrags-ID die Auswahl im Dialogfeld definieren.
    
 _ulFlags_
  
> [in] Reserviert. NULL muss sein.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
## <a name="remarks"></a>Hinweise

Clientanwendungen rufen Sie eine Rückruffunktion basierend auf den **LPFNBUTTON** Prototyp so definieren Sie eine Schaltfläche in einem Dialogfeld Details. Der Client übergibt einen Zeiger auf die Callback-Funktion in der [IAddrBook::Details](iaddrbook-details.md) -Methode aufrufen. 
  
Dienstanbieter anrufen basierte auf den **LPFNBUTTON** Prototyp so definieren Sie eine Schaltfläche in einem Dialogfeld Details Hook-Funktion. Der Anbieter übergibt einen Zeiger auf diese Hook-Funktion in der [IMAPISupport::Details](imapisupport-details.md) -Methode aufrufen. 
  
In beiden Fällen Ruft, wenn das Dialogfeld angezeigt wird und der Benutzer die Schaltfläche definierte wählt, MAPI **LPFNBUTTON**. 
  
## <a name="see-also"></a>Siehe auch



[BuildDisplayTable](builddisplaytable.md)

