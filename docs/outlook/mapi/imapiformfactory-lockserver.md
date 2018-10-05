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
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: ab51b939651bc3c121f357545969d26832a19d19
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389057"
---
# <a name="imapiformfactorylockserver"></a>IMAPIFormFactory::LockServer

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
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
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
## <a name="remarks"></a>Hinweise

Formular Viewer rufen Sie die **IMAPIFormFactory::LockServer** -Methode, um eine geöffnete Formular-Server-Anwendung im Arbeitsspeicher zu halten. Aufrechterhaltung des Formulars im Arbeitsspeicher verbessert die Leistung, wenn Formulare häufig erstellt und veröffentlicht werden. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Die **IMAPIFormFactory::LockServer** -Methode ähnelt der [IClassFactory::LockServer](https://msdn.microsoft.com/library/ms682332%28v=VS.85%29.aspx) -Methode. Im Wesentlichen verwaltet die **IMAPIFormFactory::LockServer** -Methode an, dass die Anzahl, wie oft aufgerufen wurde. als diese Anzahl größer als 0 ist, verhindert, dass die-Methode den Formular-Server, die aus dem Speicher entladen wird. Die [CoLockObjectExternal](https://msdn.microsoft.com/library/ms680592%28VS.85%29.aspx) -Funktion können Sie um dies zu implementieren. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIFormFactory : IUnknown](imapiformfactoryiunknown.md)

