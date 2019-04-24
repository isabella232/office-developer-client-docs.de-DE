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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 682e75c4e0a2f60dbd46a13b0b737ca4a8e18f3d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345777"
---
# <a name="mapierror"></a>MAPIERROR

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Stellt detaillierte Informationen zu einem Fehler bereit, der normalerweise vom Betriebssystem, MAPI oder einem Dienstanbieter generiert wird. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs. h  <br/> |
   
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
  
> Versionsnummer der Struktur. Das **ulVersion** -Element wird für zukünftige Erweiterungen verwendet und sollte auf MAPI_ERROR_VERSION festgelegt werden, das derzeit als NULL definiert ist. 
    
 **lpszError**
  
> Zeiger auf eine Zeichenfolge, die den Fehler beschreibt. Diese Zeichenfolge ist im Unicode-Format, wenn der _ulFlags_ -Parameter für die Methode, in der diese Struktur verwendet wird, auf MAPI_UNICODE festgelegt ist. 
    
 **lpszComponent**
  
> Zeiger auf eine Zeichenfolge, die die Komponente beschreibt, die den Fehler generiert hat. Diese Zeichenfolge ist im Unicode-Format, wenn der _ulFlags_ -Parameter für die Methode, in der diese Struktur verwendet wird, auf MAPI_UNICODE festgelegt ist. 
    
 **ulLowLevelError**
  
> Fehlerwert auf niedriger Ebene, der nur verwendet wird, wenn der zurückzugebende Fehler niedriger ist.
    
 **ulContext**
  
> Wert, der die Position in der Komponente darstellt, auf die durch das **lpszComponent** -Element verwiesen wird, das angibt, wo der Fehler aufgetreten ist. 
    
## <a name="remarks"></a>Bemerkungen

Die **MAPIERROR** -Struktur dient zur Beschreibung von Fehlerinformationen. Clients und Dienstanbieter übergeben einen Zeiger auf eine **MAPIERROR** -Struktur im _lppMAPIError_ -Parameter der [IMAPIProp:: getlasterroraufzurufen](imapiprop-getlasterror.md) -Methode. **Getlasterroraufzurufen** gibt Informationen zum vorherigen Fehler zurück, der auf ein Objekt aufgetreten ist. Aufrufer von **getlasterroraufzurufen** geben den Arbeitsspeicher für die **MAPIERROR** -Struktur frei, indem Sie [mapifreebufferfreigegeben](mapifreebuffer.md)aufrufen.
  
Das **lpszComponent** -Element kann verwendet werden, um die Hilfedatei der Komponente zuzuordnen, sofern vorhanden. Dienstanbieter sollten die Größe der Komponenten Zeichenfolge auf 30 Zeichen begrenzen, sodass Sie problemlos in einem Dialogfeld angezeigt werden kann. Das **ulContext** -Mitglied kann auch verwendet werden, um auf ein Onlinehilfethema für häufige Fehler zu verweisen. 
  
Da Dienstanbieter keine detaillierten Fehlerinformationen angeben müssen, sollten Clients nicht erwarten, dass die Mitglieder der **MAPIERROR** -Struktur, die zurückgegeben werden, gültige Daten enthalten. Bei einem Minimum von MAPI wird jedoch dringend empfohlen, dass Anbieter Informationen in den **lpszComponent** -und **ulContext** -Mitgliedern angeben. 
  
Weitere Informationen zur Fehlerbehandlung in MAPI finden Sie unter [Fehlerbehandlung](error-handling-in-mapi.md).
  
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

