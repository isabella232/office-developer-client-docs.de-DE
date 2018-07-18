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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: a865a751f3e274008c7004315906d6705ba55161
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792690"
---
# <a name="imslogongetlasterror"></a>IMSLogon::GetLastError

  
  
**Betrifft**: Outlook 
  
Gibt eine [MAPIERROR](mapierror.md) -Struktur, die Informationen über den letzten Fehler enthält, die für das Store-Nachrichtenspeicherobjekt aufgetreten sind. 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>Parameter

 _hResult_
  
> [in] Ein HRESULT-Datentyp, der den Fehlerwert generiert, die in der vorherigen Aufruf-Methode für die Nachricht Store-Objekt enthält.
    
 _ulFlags_
  
> [in] Eine Bitmaske aus Flags, die den Typ des zurückgegebenen Zeichenfolgen steuert. Das folgende Flag kann festgelegt werden:
    
PARAMETER MAPI_UNICODE 
  
> Die Zeichenfolgen in der **MAPIERROR** -Struktur zurückgegeben, die im Parameter _LppMAPIError_ sind im Unicode-Format. Wenn die Option MAPI_UNICODE nicht festgelegt ist, sind die Zeichenfolgen in ANSI-Format. 
    
 _lppMAPIError_
  
> [out] Ein Zeiger auf einen Zeiger auf das zurückgegebene **MAPIERROR** -Struktur, die Angaben zu Version, Komponente und Kontext für den Fehler enthält. Der Parameter _LppMAPIError_ kann auf NULL festgelegt werden, wenn es keine **MAPIERROR ist** zurückgegeben. 
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
MAPI_E_BAD_CHARWIDTH 
  
> Entweder die Option MAPI_UNICODE festgelegt wurde und die Implementierung unterstützt keine Unicode oder Parameter MAPI_UNICODE nicht festgelegt wurde und die Implementierung unterstützt nur Unicode.
    
## <a name="remarks"></a>Bemerkungen

Verwenden Sie die **IMSLogon::GetLastError** -Methode zum Abrufen von Informationen in einer Nachricht an den Benutzer über den letzten Fehler zurückgegeben, die von einem Methodenaufruf für das Objekt "Message" Store angezeigt. 
  
Um alle für die zurückgegebene **MAPIERROR** -Struktur von MAPI reservierten Arbeitsspeicher freizugeben, müssen Clientanwendungen nur die Funktion [MAPIFreeBuffer](mapifreebuffer.md) aufrufen. 
  
Der Rückgabewert von **GetLastError** muss S_OK für eine Anwendung für die **MAPIERROR**verwenden. Selbst wenn der Rückgabewert S_OK ist, kann ein **MAPIERROR** nicht zurückgegeben werden. Wenn die Implementierung nicht bestimmen kann, was letzten Fehlers wurde oder wenn ein **MAPIERROR** ist nicht verfügbar für Fehler; **GetLastError** einen Zeiger auf NULL in _LppMAPIError_ stattdessen zurück. 
  
## <a name="see-also"></a>Siehe auch



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMSLogon : IUnknown](imslogoniunknown.md)

