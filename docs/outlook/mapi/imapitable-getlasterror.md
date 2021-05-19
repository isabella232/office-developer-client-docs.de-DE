---
title: IMAPITableGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.GetLastError
api_type:
- COM
ms.assetid: 832e2c18-ddba-4d18-a391-710d21fe23e6
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 2444ea7e05367423e7920be3a871c2ab68aad76d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419002"
---
# <a name="imapitablegetlasterror"></a>IMAPITable::GetLastError

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt eine [MAPIERROR-Struktur](mapierror.md) zurück, die Informationen zum vorherigen Fehler in der Tabelle enthält. 
  
```cpp
HRESULT GetLastError(
HRESULT hResult,
ULONG ulFlags,
LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>Parameter

 _hResult_
  
> [in] HRESULT, das den fehler enthält, der im vorherigen Methodenaufruf generiert wurde.
    
 _ulFlags_
  
> [in] Bitmaske von Flags, die den Typ der zurückgegebenen Zeichenfolgen steuert. Das folgende Flag kann festgelegt werden:
    
MAPI_UNICODE 
  
> Die Zeichenfolgen in der **MAPIERROR-Struktur,** die im  _lppMAPIError-Parameter_ zurückgegeben wird, sind im Unicode-Format. Wenn das MAPI_UNICODE nicht festgelegt ist, befinden sich die Zeichenfolgen im ANSI-Format. 
    
 _lppMAPIError_
  
> [out] Zeiger auf einen Zeiger auf die zurückgegebene **MAPIERROR-Struktur,** die Versions-, Komponenten- und Kontextinformationen für den Fehler enthält. Der  _lppMAPIError-Parameter_ kann auf NULL festgelegt werden, wenn keine **MAPIERROR-Struktur** mit entsprechenden Informationen bereitgestellt werden kann. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
MAPI_E_BAD_CHARWIDTH 
  
> Entweder wurde MAPI_UNICODE-Flag festgelegt, und die Implementierung unterstützt Unicode nicht, oder MAPI_UNICODE nicht festgelegt, und die Implementierung unterstützt nur Unicode.
    
## <a name="remarks"></a>Hinweise

Die **IMAPITable::GetLastError-Methode** gibt detaillierte Informationen zu einem vorherigen Methodenaufruf zurück, der fehlgeschlagen ist. Diese Informationen können in einer Nachricht oder in einem Dialogfeld angezeigt werden. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Rufen **Sie GetLastError** auf, wenn Dem Benutzer Informationen zu einem Fehler anzeigen müssen. 
  
Sie können die [MAPIERROR-Struktur](mapierror.md) verwenden, auf die der  _lppMAPIError-Parameter_ verweist, wenn das Tabellenobjekt nur dann eins liefert, wenn **GetLastError** S_OK. Manchmal kann die Tabellenimplementierung nicht bestimmen, was der letzte Fehler war oder hat nichts mehr über den Fehler zu melden. In diesem Fall ist der Zeiger bei  _lppMAPIError_ auf NULL festgelegt. 
  
Rufen Sie die [MAPIFreeBuffer-Funktion](mapifreebuffer.md) auf, um den für die **MAPIERROR-Struktur** zugewiesenen Arbeitsspeicher frei zu geben. 
  
Weitere Informationen zur **GetLastError-Methode** finden Sie unter [MAPI Extended Errors](mapi-extended-errors.md).
  
## <a name="see-also"></a>Siehe auch



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

