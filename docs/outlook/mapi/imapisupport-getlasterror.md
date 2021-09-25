---
title: IMAPISupportGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISupport.GetLastError
api_type:
- COM
ms.assetid: 5b4290d9-230f-416a-9644-188578565c7b
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 15884634ea80b48dfade4f0ef86f617b60cd6bd4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59567459"
---
# <a name="imapisupportgetlasterror"></a>IMAPISupport::GetLastError

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt eine [MAPIERROR-Struktur](mapierror.md) zurück, die Informationen zum vorherigen Supportobjektfehler enthält. 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>Parameter

 _Hresult_
  
> [in] Ein Handle für den Fehlerwert, der im vorherigen Methodenaufruf für das Supportobjekt generiert wurde.
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die den Typ der zurückgegebenen Zeichenfolgen steuert. Das folgende Kennzeichen kann festgelegt werden:
    
MAPI_UNICODE 
  
> Die Zeichenfolgen in der **MAPIERROR-Struktur,** die im  _Parameter lppMAPIError_ zurückgegeben werden, weisen das Unicode-Format auf. Wenn das flag MAPI_UNICODE nicht festgelegt ist, haben die Zeichenfolgen das ANSI-Format. 
    
 _lppMAPIError_
  
> [out] Ein Zeiger auf einen Zeiger auf die **MAPIERROR-Struktur,** die Versions-, Komponenten- und Kontextinformationen für den Fehler enthält. Der  _lppMAPIError-Parameter_ kann auf NULL festgelegt werden, wenn keine **MAPIERROR-Struktur** mit entsprechenden Fehlerinformationen bereitgestellt werden kann. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf war erfolgreich und hat den erwarteten Wert oder die erwarteten Werte zurückgegeben.
    
MAPI_E_BAD_CHARWIDTH 
  
> Entweder wurde das MAPI_UNICODE-Flag festgelegt, und mapi unterstützt unicode nicht, oder MAPI_UNICODE nicht festgelegt wurde und MAPI nur Unicode unterstützt.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IMAPISupport::GetLastError-Methode** wird für alle Unterstützungsobjekte implementiert. Anrufer können ihren Benutzern detaillierte Informationen zu dem Fehler bereitstellen, indem sie die Daten aus der **MAPIERROR-Struktur** in ein Dialogfeld einschließen. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Sie können den Zeiger auf die **MAPIERROR-Struktur** im  _Parameter "lppMAPIError"_ nur verwenden, wenn MAPI eine bereitstellt, wenn **GetLastError** S_OK zurückgibt. Manchmal kann die MAPI nicht ermitteln, was der letzte Fehler war, oder sie hat nichts mehr, um über den Fehler zu berichten. In diesem Fall gibt  _lppMAPIError_ stattdessen einen Zeiger auf NULL zurück. 
  
Weitere Informationen zur **GetLastError** -Methode finden Sie unter [MAPI Extended Errors](mapi-extended-errors.md).
  
Rufen Sie die [MAPIFreeBuffer-Funktion](mapifreebuffer.md) für die zurückgegebene **MAPIERROR-Struktur** auf, um den gesamten von der MAPI zugewiesenen Arbeitsspeicher freizugeben. 
  
## <a name="see-also"></a>Siehe auch



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)


[MAPI Extended Errors](mapi-extended-errors.md)

