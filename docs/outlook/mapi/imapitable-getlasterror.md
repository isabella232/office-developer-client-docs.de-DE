---
title: IMAPITableGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPITable.GetLastError
api_type:
- COM
ms.assetid: 832e2c18-ddba-4d18-a391-710d21fe23e6
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 5e102832e86317f33348235b3a13ae6dc6838382
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59630656"
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

 _Hresult_
  
> [in] HRESULT, das den Fehler enthält, der im vorherigen Methodenaufruf generiert wurde.
    
 _ulFlags_
  
> [in] Bitmaske von Flags, die den Typ der zurückgegebenen Zeichenfolgen steuert. Das folgende Kennzeichen kann festgelegt werden:
    
MAPI_UNICODE 
  
> Die Zeichenfolgen in der **MAPIERROR-Struktur,** die im  _Parameter lppMAPIError_ zurückgegeben werden, weisen das Unicode-Format auf. Wenn das flag MAPI_UNICODE nicht festgelegt ist, haben die Zeichenfolgen das ANSI-Format. 
    
 _lppMAPIError_
  
> [out] Zeiger auf einen Zeiger auf die zurückgegebene **MAPIERROR-Struktur,** die Versions-, Komponenten- und Kontextinformationen für den Fehler enthält. Der  _lppMAPIError-Parameter_ kann auf NULL festgelegt werden, wenn keine **MAPIERROR-Struktur** mit entsprechenden Informationen bereitgestellt werden kann. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
MAPI_E_BAD_CHARWIDTH 
  
> Entweder wurde das MAPI_UNICODE-Flag festgelegt, und die Implementierung unterstützt unicode nicht, oder MAPI_UNICODE wurde nicht festgelegt, und die Implementierung unterstützt nur Unicode.
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPITable::GetLastError-Methode** gibt, falls verfügbar, detaillierte Informationen zu einem fehlgeschlagenen vorherigen Methodenaufruf zurück. Diese Informationen können in einer Nachricht oder einem Dialogfeld angezeigt werden. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Rufen Sie **GetLastError** auf, wenn Sie dem Benutzer Informationen zu einem Fehler anzeigen müssen. 
  
Sie können die [MAPIERROR-Struktur verwenden,](mapierror.md) auf die durch den  _lppMAPIError-Parameter_ verwiesen wird, wenn das Tabellenobjekt nur dann eine bereitstellt, wenn **GetLastError** S_OK zurückgibt. Manchmal kann die Tabellenimplementierungen nicht ermitteln, was der letzte Fehler war, oder es gibt nichts mehr, um den Fehler zu melden. In diesem Fall ist der Zeiger bei  _lppMAPIError_ auf NULL festgelegt. 
  
Rufen Sie die [MAPIFreeBuffer-Funktion auf,](mapifreebuffer.md) um den gesamten Speicher freizugeben, der für die **MAPIERROR-Struktur** reserviert ist. 
  
Weitere Informationen zur **GetLastError** -Methode finden Sie unter [MAPI Extended Errors](mapi-extended-errors.md).
  
## <a name="see-also"></a>Siehe auch



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

