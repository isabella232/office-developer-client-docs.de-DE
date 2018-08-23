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
ms.openlocfilehash: bbf8e2eb2961a3d149010b876d2b4cb3d0c8abc1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592528"
---
# <a name="mapierror"></a>MAPIERROR

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Enthält ausführliche Informationen zu einem Fehler, die in der Regel durch das Betriebssystem, MAPI- oder einem Dienstanbieter generiert. 
  
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
  
> Versionsnummer der Struktur. Der **UlVersion** Member wird für die zukünftige Erweiterung verwendet und sollte auf MAPI_ERROR_VERSION, derzeit definiert als 0 (null) festgelegt werden. 
    
 **lpszError**
  
> Zeiger auf eine Zeichenfolge, die den Fehler beschreibt. Diese Zeichenfolge wird im Unicode-Format sein, wenn der Parameter _UlFlags_ an die-Methode, in der diese Struktur verwendet wird, auf Parameter MAPI_UNICODE festgelegt ist. 
    
 **lpszComponent**
  
> Zeiger auf eine Zeichenfolge, die die Komponente beschreibt, die den Fehler verursacht hat. Diese Zeichenfolge wird im Unicode-Format sein, wenn der Parameter _UlFlags_ an die-Methode, in der diese Struktur verwendet wird, auf Parameter MAPI_UNICODE festgelegt ist. 
    
 **ulLowLevelError**
  
> Low-Level Fehlerwert, der verwendet wird, nur, wenn der Fehler zurückgegeben werden soll auf niedriger Ebene ist.
    
 **ulContext**
  
> Wert, der die Position in der Komponente darstellt, auf die der **LpszComponent** -Member, der angibt, in dem der Fehler aufgetreten ist. 
    
## <a name="remarks"></a>HinwBemerkungeneise

Die Struktur **MAPIERROR** wird verwendet, um die Fehlerinformationen zu beschreiben. Clients und Dienstanbieter übergeben einen Zeiger auf eine **MAPIERROR** -Struktur in der _LppMAPIError_ -Parameter der [IMAPIProp::GetLastError](imapiprop-getlasterror.md) -Methode. **GetLastError** gibt Informationen zu den vorherigen auf ein Objekt aufgetretenen Fehler zurück. **GetLastError** Aufrufer freigeben den Speicher für die Struktur **MAPIERROR** durch Aufrufen von [MAPIFreeBuffer](mapifreebuffer.md).
  
Der **LpszComponent** Member kann die Komponente Hilfedatei zuordnen verwendet werden, sofern vorhanden. Dienstanbieter sollte die Größe der Komponente Zeichenfolge auf 30 Zeichen einschränken, sodass es auf einfache Weise in einem Dialogfeld angezeigt werden kann. Das **UlContext** -Element kann auch verweisen auf ein Thema der Onlinehilfe für häufige Fehler verwendet werden. 
  
Dienstanbieter sind nicht erforderlich, um ausführliche Fehlerinformationen bereitzustellen, sollten Clients keine Member der Struktur **MAPIERROR** erwarten, die zurückgegeben werden, um gültige Daten enthalten. Allerdings empfiehlt unter minimale MAPI, Anbieter Informationen im **LpszComponent** und **UlContext** -Member angeben. 
  
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

