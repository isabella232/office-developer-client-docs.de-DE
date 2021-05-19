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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342140"
---
# <a name="imapiformfactorylockserver"></a>IMAPIFormFactory::LockServer

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Behält einen geöffneten Formularserver im Arbeitsspeicher bei.
  
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
  
> [in] **true,** um die Sperranzahl zu erhöhen. Andernfalls **false**.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
## <a name="remarks"></a>Hinweise

Formularbetrachter rufen die **IMAPIFormFactory::LockServer-Methode auf,** um eine geöffnete Formularserveranwendung im Arbeitsspeicher zu behalten. Das Halten des Formularservers im Arbeitsspeicher verbessert die Leistung, wenn Formulare häufig erstellt und freigegeben werden. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Die **IMAPIFormFactory::LockServer-Methode** ist der [IClassFactory::LockServer-Methode sehr](https://msdn.microsoft.com/library/ms682332%28v=VS.85%29.aspx) ähnlich. Im Wesentlichen behält die **IMAPIFormFactory::LockServer-Methode** die Anzahl der Aufrufe bei. Solange diese Anzahl größer als 0 ist, verhindert die Methode, dass der Formularserver aus dem Arbeitsspeicher entladen wird. Sie können [dies mithilfe der CoLockObjectExternal-Funktion](https://msdn.microsoft.com/library/ms680592%28VS.85%29.aspx) implementieren. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIFormFactory : IUnknown](imapiformfactoryiunknown.md)

