---
title: MAPIERROR
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MAPIERROR
api_type:
- COM
ms.assetid: e04c2228-aa0a-4958-b5b2-6467e93ab613
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 682e75c4e0a2f60dbd46a13b0b737ca4a8e18f3d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409146"
---
# <a name="mapierror"></a>MAPIERROR

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält detaillierte Informationen zu einem Fehler, der normalerweise vom Betriebssystem, der MAPI oder einem Dienstanbieter generiert wird. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _MAPIERROR
{
  ULONG ulVersion;
  LPSTR lpszError;
  LPSTR lpszComponent;
  ULONG ulLowLevelError;
  ULONG ulContext;
} MAPIERROR, FAR * LPMAPIERROR;

```

## <a name="members"></a>Elemente

 **ulVersion**
  
> Versionsnummer der Struktur. Das **ulVersion-Element** wird für die zukünftige Erweiterung verwendet und sollte auf MAPI_ERROR_VERSION festgelegt werden, das derzeit als Null definiert ist. 
    
 **lpszError**
  
> Zeiger auf eine Zeichenfolge, die den Fehler beschreibt. Diese Zeichenfolge wird im Unicode-Format angezeigt, wenn der  _ulFlags-Parameter_ für die Methode, in der diese Struktur verwendet wird, auf MAPI_UNICODE. 
    
 **lpszComponent**
  
> Zeiger auf eine Zeichenfolge, die die Komponente beschreibt, die den Fehler generiert hat. Diese Zeichenfolge wird im Unicode-Format angezeigt, wenn der  _ulFlags-Parameter_ für die Methode, in der diese Struktur verwendet wird, auf MAPI_UNICODE. 
    
 **ulLowLevelError**
  
> Niedriger Fehlerwert, der nur verwendet wird, wenn der zurückgegebene Fehler auf niedriger Ebene liegt.
    
 **ulContext**
  
> Wert, der die Position in der Komponente darstellt, auf die das **lpszComponent-Element** verweist, das den Fehler identifiziert. 
    
## <a name="remarks"></a>Hinweise

Die **MAPIERROR-Struktur** wird verwendet, um Fehlerinformationen zu beschreiben. Clients und Dienstanbieter übergeben einen Zeiger an eine **MAPIERROR-Struktur** im _lppMAPIError-Parameter_ der [IMAPIProp::GetLastError-Methode.](imapiprop-getlasterror.md) **GetLastError** gibt Informationen zum vorherigen Fehler zurück, der für ein Objekt aufgetreten ist. Aufrufer von **GetLastError** geben den Arbeitsspeicher für die **MAPIERROR-Struktur** frei, indem [sie MAPIFreeBuffer aufrufen.](mapifreebuffer.md)
  
Das **lpszComponent-Mitglied** kann verwendet werden, um die Hilfedatei der Komponente zu zuordnungen, sofern vorhanden. Dienstanbieter sollten die Größe der Komponentenzeichenfolge auf 30 Zeichen beschränken, damit sie problemlos in einem Dialogfeld angezeigt werden kann. Das **ulContext-Mitglied** kann auch verwendet werden, um auf ein Onlinehilfethema für häufige Fehler zu verweisen. 
  
Da Dienstanbieter keine detaillierten Fehlerinformationen bereitstellen müssen, sollten Clients keine Mitglieder der **MAPIERROR-Struktur** erwarten, die zurückgegeben werden, um gültige Daten zu enthalten. Mindestens jedoch empfiehlt MAPI dringend, dass Anbieter Informationen in den **lpszComponent-** und **ulContext-Mitgliedern** angeben. 
  
Weitere Informationen zur Fehlerbehandlung in MAPI finden Sie unter [Error Handling](error-handling-in-mapi.md).
  
## <a name="see-also"></a>Siehe auch



[IABLogon::GetLastError](iablogon-getlasterror.md)
  
[IABProvider::Logon](iabprovider-logon.md)
  
[IMAPIControl::GetLastError](imapicontrol-getlasterror.md)
  
[IMAPIProp::GetLastError](imapiprop-getlasterror.md)
  
[IMAPISession::GetLastError](imapisession-getlasterror.md)
  
[IMAPISupport::GetLastError](imapisupport-getlasterror.md)
  
[IMAPISupport::OpenAddressBook](imapisupport-openaddressbook.md)
  
[IMAPISession::OpenAddressBook](imapisession-openaddressbook.md)
  
[IMAPITable::GetLastError](imapitable-getlasterror.md)
  
[IMsgServiceAdmin::GetLastError](imsgserviceadmin-getlasterror.md)
  
[IMSLogon::GetLastError](imslogon-getlasterror.md)
  
[IMSProvider::Logon](imsprovider-logon.md)
  
[IProfAdmin::GetLastError](iprofadmin-getlasterror.md)
  
[IProviderAdmin::GetLastError](iprovideradmin-getlasterror.md)


[MAPI-Strukturen](mapi-structures.md)

