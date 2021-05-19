---
title: IMAPIFormFactoryGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormFactory.GetLastError
api_type:
- COM
ms.assetid: 4b1d85f6-7996-4839-b985-abf83e305651
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 2c83f7788d9c01ab02f1a2bc39a35abe2c5a21c5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417007"
---
# <a name="imapiformfactorygetlasterror"></a>IMAPIFormFactory::GetLastError

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt eine [MAPIERROR-Struktur](mapierror.md) zurück, die Informationen zum vorherigen Fehler enthält, der für das Form Factory-Objekt aufgetreten ist. 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>Parameter

 _hResult_
  
> [in] Ein HRESULT-Datentyp, der den im vorherigen Methodenaufruf generierten Fehlerwert enthält.
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die den Typ der zurückgegebenen Zeichenfolgen steuert. Das folgende Flag kann festgelegt werden: 
    
MAPI_UNICODE 
  
> Die Zeichenfolgen in der **MAPIERROR-Struktur,** die im  _lppMAPIError-Parameter_ zurückgegeben wird, sind im Unicode-Format. Wenn das MAPI_UNICODE nicht festgelegt ist, befinden sich die Zeichenfolgen im ANSI-Format. 
    
 _lppMAPIError_
  
> [out] Ein Zeiger auf einen Zeiger auf die zurückgegebene **MAPIERROR-Struktur,** die Versions-, Komponenten- und Kontextinformationen für den Fehler enthält. Dieser Parameter kann auf NULL festgelegt werden, wenn keine **MAPIERROR-Struktur** zurückgegeben werden soll. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
MAPI_E_BAD_CHARWIDTH 
  
> Entweder wurde das MAPI_UNICODE festgelegt, **und GetLastError** unterstützt unicode nicht, oder MAPI_UNICODE nicht festgelegt, **und GetLastError** unterstützt nur Unicode. 
    
## <a name="remarks"></a>Hinweise

Die **IMAPIFormFactory::GetLastError-Methode** stellt Informationen zu einem vorherigen Methodenaufruf zur Verfügung, der fehlgeschlagen ist. Anrufer können ihren Benutzern detaillierte Informationen zu dem Fehler bereitstellen, indem sie die Daten aus der **MAPIERROR-Struktur** in ein Dialogfeld eingeben. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Sie können die **MAPIERROR-Struktur** verwenden, auf die der  _lppMAPIError-Parameter_ verweist, wenn MAPI nur dann einen angibt, wenn **GetLastError** S_OK. Manchmal kann MAPI nicht ermitteln, was der letzte Fehler war oder hat nichts mehr über den Fehler zu melden. In diesem Fall wird stattdessen ein Zeiger auf NULL in  _lppMAPIError_ zurückgegeben. 
  
Weitere Informationen zur **GetLastError-Methode** finden Sie unter [Using Extended Errors](mapi-extended-errors.md).
  
## <a name="see-also"></a>Siehe auch



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPIFormFactory : IUnknown](imapiformfactoryiunknown.md)

