---
title: IMAPIFormFactoryLockServer
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormFactory.LockServer
api_type:
- COM
ms.assetid: b9bd389a-6975-41a2-a2f4-e501312e434b
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: c33fea8a2aba875fcdc06dea3343add4b7ac5dde
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792145"
---
# <a name="imapiformfactorylockserver"></a>IMAPIFormFactory::LockServer

  
  
**Betrifft**: Outlook 
  
Wird einen geöffnete Formular Server im Arbeitsspeicher gespeichert.
  
```cpp
HRESULT LockServer(
  ULONG ulFlags,
  ULONG fLockServer
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> [in] Reserviert. NULL muss sein.
    
 _fLockServer_
  
> [in] **true,** um die Anzahl der Sperren zu erhöhen. anderenfalls **false**.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
## <a name="remarks"></a>Hinweise

Formular Viewer rufen Sie die **IMAPIFormFactory::LockServer** -Methode, um eine geöffnete Formular-Server-Anwendung im Arbeitsspeicher zu halten. Aufrechterhaltung des Formulars im Arbeitsspeicher verbessert die Leistung, wenn Formulare häufig erstellt und veröffentlicht werden. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Die **IMAPIFormFactory::LockServer** -Methode ähnelt der [IClassFactory::LockServer](http://msdn.microsoft.com/en-us/library/ms682332%28v=VS.85%29.aspx) -Methode. Im Wesentlichen verwaltet die **IMAPIFormFactory::LockServer** -Methode an, dass die Anzahl, wie oft aufgerufen wurde. als diese Anzahl größer als 0 ist, verhindert, dass die-Methode den Formular-Server, die aus dem Speicher entladen wird. Die [CoLockObjectExternal](http://msdn.microsoft.com/en-us/library/ms680592%28VS.85%29.aspx) -Funktion können Sie um dies zu implementieren. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIFormFactory : IUnknown](imapiformfactoryiunknown.md)

