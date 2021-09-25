---
title: IMAPIViewContextGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIViewContext.GetLastError
api_type:
- COM
ms.assetid: 3306e37a-2500-4281-96c3-ca0d5c81909d
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 5010036c704b75638233695003dba59de21d6a0a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59600855"
---
# <a name="imapiviewcontextgetlasterror"></a>IMAPIViewContext::GetLastError

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt eine [MAPIERROR-Struktur](mapierror.md) zurück, die Informationen zum vorherigen Fehler enthält, der für das Ansichtskontextobjekt aufgetreten ist. 
  
```cpp
HRESULT GetLastError(
HRESULT hResult,
ULONG ulFlags,
LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>Parameter

 _Hresult_
  
> [in] HRESULT-Datentyp, der den Fehlerwert enthält, der im vorherigen Methodenaufruf generiert wurde.
    
 _ulFlags_
  
> [in] Bitmaske von Flags, die den Typ der zurückgegebenen Zeichenfolgen steuert. Das folgende Kennzeichen kann festgelegt werden:
    
MAPI_UNICODE 
  
> Die Zeichenfolgen in der **MAPIERROR-Struktur,** die im  _Parameter lppMAPIError_ zurückgegeben werden, weisen das Unicode-Format auf. Wenn das flag MAPI_UNICODE nicht festgelegt ist, haben die Zeichenfolgen das ANSI-Format. 
    
 _lppMAPIError_
  
> [out] Zeiger auf einen Zeiger auf die zurückgegebene **MAPIERROR-Struktur,** die Versions-, Komponenten- und Kontextinformationen für den Fehler enthält. Dieser Parameter kann auf NULL festgelegt werden, wenn keine **MAPIERROR-Struktur** zurückgegeben werden soll. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
MAPI_E_BAD_CHARWIDTH 
  
> Entweder wurde das MAPI_UNICODE-Flag festgelegt, und **GetLastError** unterstützt unicode nicht, oder MAPI_UNICODE wurde nicht festgelegt, und **GetLastError** unterstützt nur Unicode. 
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IMAPIViewContext::GetLastError-Methode** liefert Informationen zu einem vorherigen Methodenaufruf, bei dem ein Fehler aufgetreten ist. Anrufer können ihren Benutzern detaillierte Informationen zu dem Fehler bereitstellen, indem sie die Daten aus der **MAPIERROR-Struktur** in ein Dialogfeld einschließen. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Sie können die **MAPIERROR-Struktur verwenden,** auf die durch den  _lppMAPIError-Parameter_ verwiesen wird, wenn MAPI nur dann eine bereitstellt, wenn **GetLastError** S_OK zurückgibt. Manchmal kann die MAPI nicht ermitteln, was der letzte Fehler war, oder sie kann nichts mehr über den Fehler melden. In diesem Fall wird stattdessen ein Zeiger auf NULL in  _lppMAPIError_ zurückgegeben. 
  
Weitere Informationen zur **GetLastError** -Methode finden Sie unter [MAPI Extended Errors](mapi-extended-errors.md).
  
## <a name="see-also"></a>Siehe auch



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md)

