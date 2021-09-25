---
title: IMAPIFormFactoryLockServer
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIFormFactory.LockServer
api_type:
- COM
ms.assetid: b9bd389a-6975-41a2-a2f4-e501312e434b
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: d5aa2068b461a5bba1055ef990a5aff38b113879
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59551324"
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
  
> [in]  true, um die Sperranzahl zu erhöhen; andernfalls **false**.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
## <a name="remarks"></a>HinwBemerkungeneise

Formularviewer rufen die **IMAPIFormFactory::LockServer-Methode** auf, um eine geöffnete Formularserveranwendung im Arbeitsspeicher zu behalten. Das Beibehalten des Formularservers im Arbeitsspeicher verbessert die Leistung, wenn Formulare häufig erstellt und freigegeben werden. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Die **IMAPIFormFactory::LockServer-Methode** ist der [IClassFactory::LockServer-Methode](https://msdn.microsoft.com/library/ms682332%28v=VS.85%29.aspx) sehr ähnlich. Im Wesentlichen behält die **IMAPIFormFactory::LockServer-Methode** die Anzahl der Aufrufe bei. Solange diese Anzahl größer als 0 ist, verhindert die Methode, dass der Formularserver aus dem Arbeitsspeicher entladen wird. Sie können dies mit der [CoLockObjectExternal-Funktion](https://msdn.microsoft.com/library/ms680592%28VS.85%29.aspx) implementieren. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIFormFactory : IUnknown](imapiformfactoryiunknown.md)

