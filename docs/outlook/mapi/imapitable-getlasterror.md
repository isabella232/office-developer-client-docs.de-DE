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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329001"
---
# <a name="imapitablegetlasterror"></a>IMAPITable::GetLastError

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt eine [MAPIERROR](mapierror.md) -Struktur mit Informationen über den vorherigen Fehler in der Tabelle zurück. 
  
```cpp
HRESULT GetLastError(
HRESULT hResult,
ULONG ulFlags,
LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>Parameter

 _hResult_
  
> in HRESULT mit dem im vorherigen Methodenaufruf generierten Fehler.
    
 _ulFlags_
  
> in Bitmaske von Flags, die den Typ der zurückgegebenen Zeichenfolgen steuert. Das folgende Flag kann festgelegt werden:
    
MAPI_UNICODE 
  
> Die Zeichenfolgen in der **MAPIERROR** -Struktur, die im _lppMAPIError_ -Parameter zurückgegeben werden, sind im Unicode-Format. Wenn das MAPI_UNICODE-Flag nicht festgelegt ist, werden die Zeichenfolgen im ANSI-Format. 
    
 _lppMAPIError_
  
> Out Zeiger auf einen Zeiger auf die zurückgegebene **MAPIERROR** -Struktur, die Versions-, Komponenten-und Kontextinformationen für den Fehler enthält. Der _lppMAPIError_ -Parameter kann auf NULL festgelegt werden, wenn eine **MAPIERROR** -Struktur mit entsprechenden Informationen nicht bereitgestellt werden kann. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
MAPI_E_BAD_CHARWIDTH 
  
> Entweder wurde das MAPI_UNICODE-Flag festgelegt, und die Implementierung unterstützt Unicode nicht, oder MAPI_UNICODE wurde nicht festgelegt, und die Implementierung unterstützt nur Unicode.
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPITable:: getlasterroraufzurufen** -Methode gibt detaillierte Informationen zu einem fehlgeschlagenen Methodenaufruf zurück, falls verfügbar. Diese Informationen können in einer Nachricht oder einem Dialogfeld angezeigt werden. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Rufen Sie **getlasterroraufzurufen** auf, wenn Sie Informationen zu einem Fehler für den Benutzer anzeigen müssen. 
  
Sie können die [MAPIERROR](mapierror.md) -Struktur verwenden, auf die durch den _lppMAPIError_ -Parameter verwiesen wird, wenn das Table-Objekt nur dann einen Wert angibt, wenn **getlasterroraufzurufen** S_OK zurückgibt. In einigen Fällen kann die Tabellen Implementierung nicht ermitteln, was der letzte Fehler war oder nicht mehr über den Fehler berichtet. In dieser Situation ist der Zeiger bei _lppMAPIError_ auf NULL festgelegt. 
  
Rufen Sie die [mapifreebufferfreigegeben](mapifreebuffer.md) -Funktion auf, um den gesamten für die **MAPIERROR** -Struktur reservierten Arbeitsspeicher freizugeben. 
  
Weitere Informationen zur **getlasterroraufzurufen** -Methode finden Sie unter [MAPI Extended Errors](mapi-extended-errors.md).
  
## <a name="see-also"></a>Siehe auch



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

