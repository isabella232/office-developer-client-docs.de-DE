---
title: IMSLogonGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSLogon.GetLastError
api_type:
- COM
ms.assetid: 3e296f6d-4833-4c68-9b84-df0b09878474
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 472502d0f033370b06a69596944350152ab794f9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425876"
---
# <a name="imslogongetlasterror"></a>IMSLogon::GetLastError

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt eine [MAPIERROR-Struktur](mapierror.md) zurück, die Informationen zum letzten Fehler enthält, der für das Nachrichtenspeicherobjekt aufgetreten ist. 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>Parameter

 _hResult_
  
> [in] Ein HRESULT-Datentyp, der den Fehlerwert enthält, der im vorherigen Methodenaufruf für das Nachrichtenspeicherobjekt generiert wurde.
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die den Typ der zurückgegebenen Zeichenfolgen steuert. Das folgende Flag kann festgelegt werden:
    
MAPI_UNICODE 
  
> Die Zeichenfolgen in der **MAPIERROR-Struktur,** die im  _lppMAPIError-Parameter_ zurückgegeben wird, sind im Unicode-Format. Wenn das MAPI_UNICODE nicht festgelegt ist, befinden sich die Zeichenfolgen im ANSI-Format. 
    
 _lppMAPIError_
  
> [out] Ein Zeiger auf einen Zeiger auf die zurückgegebene **MAPIERROR-Struktur,** die Versions-, Komponenten- und Kontextinformationen für den Fehler enthält. Der  _lppMAPIError-Parameter_ kann auf NULL festgelegt werden, wenn **kein MAPIERROR zurückgegeben** werden soll. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
MAPI_E_BAD_CHARWIDTH 
  
> Entweder wurde MAPI_UNICODE-Flag festgelegt, und die Implementierung unterstützt unicode nicht, oder MAPI_UNICODE wurde nicht festgelegt, und die Implementierung unterstützt nur Unicode.
    
## <a name="remarks"></a>Hinweise

Verwenden Sie **die IMSLogon::GetLastError-Methode,** um Informationen abzurufen, die dem Benutzer in einer Meldung über den letzten Fehler angezeigt werden, der von einem Methodenaufruf für das Nachrichtenspeicherobjekt zurückgegeben wurde. 
  
Um den von MAPI zugewiesenen Arbeitsspeicher für die zurückgegebene **MAPIERROR-Struktur** frei zu geben, müssen Clientanwendungen nur die [MAPIFreeBuffer-Funktion](mapifreebuffer.md) aufrufen. 
  
Der Rückgabewert von **GetLastError** muss S_OK werden, damit eine Anwendung **MAPIERROR verwenden kann.** Selbst wenn der Rückgabewert S_OK, wird möglicherweise kein **MAPIERROR** zurückgegeben. Wenn die Implementierung nicht ermitteln kann, was der letzte Fehler war, oder wenn für diesen Fehler **kein MAPIERROR** verfügbar ist, gibt **GetLastError** stattdessen einen Zeiger auf NULL in  _lppMAPIError_ zurück. 
  
## <a name="see-also"></a>Siehe auch



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMSLogon : IUnknown](imslogoniunknown.md)

