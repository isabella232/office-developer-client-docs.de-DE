---
title: MAPIERROR
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.MAPIERROR
api_type:
- COM
ms.assetid: e04c2228-aa0a-4958-b5b2-6467e93ab613
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 5cdbd4d8f28562e659a5434ab17fe02eb3bf6c51
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59600715"
---
# <a name="mapierror"></a>MAPIERROR

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Stellt detaillierte Informationen zu einem Fehler bereit, der in der Regel vom Betriebssystem, der MAPI oder einem Dienstanbieter generiert wird. 
  
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

## <a name="members"></a>Members

 **ulVersion**
  
> Versionsnummer der Struktur. Der **ulVersion-Member** wird für zukünftige Erweiterungen verwendet und sollte auf MAPI_ERROR_VERSION festgelegt werden, der derzeit als Null definiert ist. 
    
 **lpszError**
  
> Zeiger auf eine Zeichenfolge, die den Fehler beschreibt. Diese Zeichenfolge hat das Unicode-Format, wenn der  _ulFlags-Parameter_ für die Methode, in der diese Struktur verwendet wird, auf MAPI_UNICODE festgelegt ist. 
    
 **lpszComponent**
  
> Zeiger auf eine Zeichenfolge, die die Komponente beschreibt, die den Fehler generiert hat. Diese Zeichenfolge hat das Unicode-Format, wenn der  _ulFlags-Parameter_ für die Methode, in der diese Struktur verwendet wird, auf MAPI_UNICODE festgelegt ist. 
    
 **ulLowLevelError**
  
> Fehlerwert auf niedriger Ebene, der nur verwendet wird, wenn der zurückzugebende Fehler auf niedriger Ebene liegt.
    
 **ulContext**
  
> Wert, der die Position in der Komponente darstellt, auf die vom **lpszComponent-Element** verwiesen wird, das angibt, wo der Fehler aufgetreten ist. 
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **MAPIERROR-Struktur** wird verwendet, um Fehlerinformationen zu beschreiben. Clients und Dienstanbieter übergeben einen Zeiger auf eine **MAPIERROR-Struktur** im _lppMAPIError-Parameter_ der [IMAPIProp::GetLastError-Methode.](imapiprop-getlasterror.md) **GetLastError** gibt Informationen zum vorherigen Fehler zurück, der für ein Objekt aufgetreten ist. Aufrufer von **GetLastError** geben den Speicher für die **MAPIERROR-Struktur** frei, indem [sie MAPIFreeBuffer](mapifreebuffer.md)aufrufen.
  
Der **lpszComponent-Member** kann verwendet werden, um die Hilfedatei der Komponente zuzuordnen, sofern vorhanden. Dienstanbieter sollten die Größe der Komponentenzeichenfolge auf 30 Zeichen beschränken, damit sie problemlos in einem Dialogfeld angezeigt werden kann. Das **ulContext-Element** kann auch verwendet werden, um auf häufige Fehler in einem Onlinehilfethema zu verweisen. 
  
Da Dienstanbieter keine detaillierten Fehlerinformationen bereitstellen müssen, sollten Clients nicht erwarten, dass elemente der **MAPIERROR-Struktur,** die zurückgegeben werden, gültige Daten enthalten. Allerdings empfiehlt mapi mindestens, dass Anbieter Informationen in den **LpszComponent-** und **ulContext-Membern** angeben. 
  
Weitere Informationen zur Fehlerbehandlung in MAPI finden Sie unter [Fehlerbehandlung.](error-handling-in-mapi.md)
  
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

