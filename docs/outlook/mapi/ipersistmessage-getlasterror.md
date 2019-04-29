---
title: IPersistMessageGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPersistMessage.GetLastError
api_type:
- COM
ms.assetid: 32cc3a1f-1310-4788-b0f4-93c1e4940f37
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 2189a39e115236e6c2ec9de8a263ce3982d8b8e0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426709"
---
# <a name="ipersistmessagegetlasterror"></a>IPersistMessage::GetLastError

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt eine [MAPIERROR](mapierror.md) -Struktur zurück, die Informationen zum vorherigen Fehler im Form-Objekt enthält. 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>Parameter

 _hResult_
  
> in Ein HRESULT-Datentyp, der den im vorherigen Methodenaufruf generierten Fehlerwert enthält.
    
 _ulFlags_
  
> in Eine Bitmaske von Flags, die den Typ der zurückgegebenen Zeichenfolgen steuert. Das folgende Flag kann festgelegt werden:
    
MAPI_UNICODE 
  
> Die Zeichenfolgen in der [MAPIERROR](mapierror.md) -Struktur, die im _lppMAPIError_ -Parameter zurückgegeben werden, sind im Unicode-Format. Wenn das MAPI_UNICODE-Flag nicht festgelegt ist, werden die Zeichenfolgen im ANSI-Format. 
    
 _lppMAPIError_
  
> Out Ein Zeiger auf einen Zeiger auf eine **MAPIERROR** -Struktur, die Versions-, Komponenten-und Kontextinformationen für den Fehler enthält. Der _lppMAPIError_ -Parameter kann auf NULL festgelegt werden, wenn das Formular keine geeigneten Informationen für eine **MAPIERROR** -Struktur bereitstellen kann. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
MAPI_E_BAD_CHARWIDTH 
  
> Entweder wurde das MAPI_UNICODE-Flag festgelegt, und der Adressbuchanbieter unterstützt Unicode nicht, oder MAPI_UNICODE wurde nicht festgelegt, und der Adressbuchanbieter unterstützt nur Unicode.
    
## <a name="remarks"></a>Bemerkungen

Formularobjekte implementieren die **IPersistMessage:: getlasterroraufzurufen** -Methode, um Informationen zu einem fehlgeschlagenen Methodenaufruf bereitzustellen. Formular Betrachter können Ihren Benutzern detaillierte Informationen zu dem Fehler bereitstellen, indem Sie die Daten aus der [MAPIERROR](mapierror.md) -Struktur in ein Dialogfeld einschließen. 
  
Ein Aufruf von **getlasterroraufzurufen** wirkt sich nicht auf den Status des Formulars aus. Wenn **getlasterroraufzurufen** zurückgegeben wird, bleibt das Formular in dem Zustand, in dem Sie sich befanden, bevor der Anruf getätigt wurde. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Sie können die **MAPIERROR** -Struktur verwenden, wenn das Formular eine bereitstellt, auf die durch den _lppMAPIError_ -Parameter verwiesen wird, nur, wenn **getlasterroraufzurufen** S_OK zurückgibt. In einigen Fällen kann das Formular nicht ermitteln, was der letzte Fehler aufweist oder nicht mehr über den Fehler berichtet. In dieser Situation gibt das Formular stattdessen einen Zeiger auf NULL in _lppMAPIError_ zurück. 
  
Weitere Informationen zur **getlasterroraufzurufen** -Methode finden Sie unter [MAPI Extended Errors](mapi-extended-errors.md).
  
## <a name="see-also"></a>Siehe auch



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IPersistMessage : IUnknown](ipersistmessageiunknown.md)

