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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: b8ee83ad550106ae82f3308b9ef5692f66f5f5b6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792460"
---
# <a name="imapitablegetlasterror"></a>IMAPITable::GetLastError

  
  
**Betrifft**: Outlook 
  
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
  
> [in] HRESULT, das den im vorherigen Methodenaufruf generierten Fehler enthält.
    
 _ulFlags_
  
> [in] Bitmaske aus Flags, die den Typ des zurückgegebenen Zeichenfolgen steuert. Das folgende Flag kann festgelegt werden:
    
PARAMETER MAPI_UNICODE 
  
> Die Zeichenfolgen in der **MAPIERROR** -Struktur zurückgegeben, die im Parameter _LppMAPIError_ sind im Unicode-Format. Wenn die Option MAPI_UNICODE nicht festgelegt ist, sind die Zeichenfolgen in ANSI-Format. 
    
 _lppMAPIError_
  
> [out] Zeiger auf einen Zeiger auf das zurückgegebene **MAPIERROR** -Struktur, die Angaben zu Version, Komponente und Kontext für den Fehler enthält. Der Parameter _LppMAPIError_ kann auf NULL festgelegt werden, wenn eine **MAPIERROR** -Struktur mit den entsprechenden Informationen bereitgestellt werden kann. 
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
MAPI_E_BAD_CHARWIDTH 
  
> Entweder die Option MAPI_UNICODE festgelegt wurde und die Implementierung unterstützt keine Unicode oder Parameter MAPI_UNICODE nicht festgelegt wurde und die Implementierung unterstützt nur Unicode.
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPITable::GetLastError** -Methode gibt ausführliche Informationen zurück, wenn zu einem Aufruf der vorherigen-Methode, die nicht zur Verfügung. Diese Informationen kann in einer Nachricht oder ein Dialogfeld angezeigt werden. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Rufen Sie **GetLastError** , wenn Sie zum Anzeigen von Informationen zu einem Fehler, die dem Benutzer müssen. 
  
Sie können nutzen Sie die [MAPIERROR](mapierror.md) auf die Struktur durch den Parameter _LppMAPIError_ gezeigt, wenn das Table-Objekt eine stellt nur, wenn **GetLastError** gibt S_OK zurück. In einigen Fällen kann nicht die Implementierung der Tabelle ermitteln, was letzten Fehlers wurde oder nicht mehr zu dem Fehler gemeldet wurde. In diesem Fall wird der Mauszeiger am _LppMAPIError_ auf NULL festgelegt. 
  
Rufen Sie die [MAPIFreeBuffer](mapifreebuffer.md) -Funktion, um alle Arbeitsspeichers für die Struktur **MAPIERROR** freizugeben. 
  
Weitere Informationen über die **GetLastError** -Methode finden Sie unter [Extended MAPI-Fehler](mapi-extended-errors.md).
  
## <a name="see-also"></a>Siehe auch



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

