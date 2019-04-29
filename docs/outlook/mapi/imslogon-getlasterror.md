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
  
Gibt eine [MAPIERROR](mapierror.md) -Struktur zurück, die Informationen zum letzten Fehler enthält, der für das Nachrichtenspeicherobjekt aufgetreten ist. 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>Parameter

 _hResult_
  
> in Ein HRESULT-Datentyp, der den im vorherigen Methodenaufruf für das Nachrichtenspeicherobjekt generierten Fehlerwert enthält.
    
 _ulFlags_
  
> in Eine Bitmaske von Flags, die den Typ der zurückgegebenen Zeichenfolgen steuert. Das folgende Flag kann festgelegt werden:
    
MAPI_UNICODE 
  
> Die Zeichenfolgen in der **MAPIERROR** -Struktur, die im _lppMAPIError_ -Parameter zurückgegeben werden, sind im Unicode-Format. Wenn das MAPI_UNICODE-Flag nicht festgelegt ist, werden die Zeichenfolgen im ANSI-Format. 
    
 _lppMAPIError_
  
> Out Ein Zeiger auf einen Zeiger auf die zurückgegebene **MAPIERROR** -Struktur, die Versions-, Komponenten-und Kontextinformationen für den Fehler enthält. Der _lppMAPIError_ -Parameter kann auf NULL festgelegt werden, wenn keine **MAPIERROR** zurückgegeben werden soll. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
MAPI_E_BAD_CHARWIDTH 
  
> Entweder wurde das MAPI_UNICODE-Flag festgelegt, und die Implementierung unterstützt Unicode nicht, oder MAPI_UNICODE wurde nicht festgelegt, und die Implementierung unterstützt nur Unicode.
    
## <a name="remarks"></a>Bemerkungen

Verwenden Sie die **IMSLogon:: getlasterroraufzurufen** -Methode, um Informationen abzurufen, die dem Benutzer in einer Nachricht bezüglich des letzten von einem Methodenaufruf für das Nachrichtenspeicherobjekt zurückgegebenen Fehlers angezeigt werden sollen. 
  
Um den gesamten von MAPI reservierten Arbeitsspeicher für die zurückgegebene **MAPIERROR** -Struktur freizugeben, müssen Clientanwendungen nur die [mapifreebufferfreigegeben](mapifreebuffer.md) -Funktion aufrufen. 
  
Der Rückgabewert von **getlasterroraufzurufen** muss S_OK sein, damit eine Anwendung den **MAPIERROR**verwenden kann. Auch wenn der Rückgabewert S_OK ist, wird möglicherweise kein **MAPIERROR** zurückgegeben. Wenn die Implementierung nicht ermitteln kann, was der letzte Fehler war, oder wenn ein **MAPIERROR** für diesen Fehler nicht verfügbar ist, gibt **getlasterroraufzurufen** in _LPPMAPIERROR_ stattdessen einen Zeiger auf NULL zurück. 
  
## <a name="see-also"></a>Siehe auch



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMSLogon : IUnknown](imslogoniunknown.md)

