---
title: IMSProviderSpoolerLogon
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSProvider.SpoolerLogon
api_type:
- COM
ms.assetid: 79d5af23-efad-4013-a330-56babfb2bb0f
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: eaf84e1b2a747b313f1534eb66b190d86cf89df9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792689"
---
# <a name="imsproviderspoolerlogon"></a>IMSProvider::SpoolerLogon

  
  
**Betrifft**: Outlook 
  
Die MAPI-Warteschlange an einen Nachrichtenspeicher protokolliert.
  
```cpp
HRESULT SpoolerLogon(
  LPMAPISUP lpMAPISup,
  ULONG_PTR ulUIParam,
  LPSTR lpszProfileName,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulFlags,
  LPCIID lpInterface,
  ULONG cbSpoolSecurity,
  LPBYTE lpbSpoolSecurity,
  LPMAPIERROR FAR * lppMAPIError,
  LPMSLOGON FAR * lppMSLogon,
  LPMDB FAR * lppMDB     
);
```

## <a name="parameters"></a>Parameter

 _lpMAPISup_
  
> [in] Ein Zeiger auf die MAPI unterstützt Objekt für den Nachrichtenspeicher.
    
 _ulUIParam_
  
> [in] Ein Handle für das übergeordnete Fenster des alle Dialogfelder oder Fenster zeigt diese Methode an. 
    
 _lpszProfileName_
  
> [in] Ein Zeiger auf eine Zeichenfolge mit dem Namen des Profils, das für die Anmeldung des MAPI-Warteschlange verwendet wird. Diese Zeichenfolge kann in Dialogfeldern angezeigt, in eine Protokolldatei geschrieben oder einfach ignoriert werden. Es muss im Unicode-Format sein, wenn die Option MAPI_UNICODE im _UlFlags_ -Parameter festgelegt ist. 
    
 _cbEntryID_
  
> [in] Die Größe des Eintrags-ID, die auf das durch den Parameter _LpEntryID_ in Bytes. 
    
 _lpEntryID_
  
> [in] Ein Zeiger auf die Eintrags-ID für den Nachrichtenspeicher. NULL in der _LpEntryID_ -Parameter übergeben gibt an, dass ein Nachrichtenspeicher noch nicht ausgewählt wurden und Dialogfelder, mit denen den Benutzer die Auswahl ein Nachrichtenspeichers präsentiert werden können. 
    
 _ulFlags_
  
> [in] Eine Bitmaske aus Flags, die steuert, wie die Anmeldung ausgeführt wird. Die folgenden Kennzeichen können festgelegt werden:
    
MAPI_DEFERRED_ERRORS 
  
> Der Aufruf ist zulässig, erfolgreich ausgeführt werden kann, auch wenn das zugrunde liegende Objekt nicht an die Implementierung der aufrufenden verfügbar ist. Wenn das Objekt nicht verfügbar ist, kann ein nachfolgender Aufruf für das Objekt ein Fehler ausgelöst.
    
PARAMETER MAPI_UNICODE 
  
> Die übergebenen Zeichenfolgen sind im Unicode-Format. Wenn der Parameter MAPI_UNICODE nicht festgelegt ist, sind die Zeichenfolgen in ANSI-Format.
    
MDB_NO_DIALOG 
  
> Verhindert die Anzeige von Dialogfeldern für die Anmeldung. Wenn dieses Flag festgelegt ist, wird der Fehlerwert MAPI_E_LOGON_FAILED zurückgegeben, wenn die Anmeldung nicht erfolgreich ist. Wenn dieses Flag nicht festgelegt ist, kann die Nachricht Speicher-Anbieter den Benutzer an den richtigen einen Namen oder ein Kennwort, zum Einfügen von eines Datenträgers oder zum Ausführen anderer Aktionen erforderlich sind, um die Verbindung zu den Speicher auffordern.
    
MDB_WRITE 
  
> Anfragen Lese-/Schreibberechtigung.
    
 _lpInterface_
  
> [in] Ein Zeiger auf der Benutzeroberfläche IID (Identifier) für den Nachrichtenspeicher anmelden. Übergeben von NULL gibt an, dass die MAPI-Schnittstelle für den Nachrichtenspeicher ([IMsgStore](imsgstoreimapiprop.md)) zurückgegeben wird. Der Parameter _LpInterface_ kann auch auf einen Bezeichner für eine entsprechende Schnittstelle für den Nachrichtenspeicher (beispielsweise IID_IUnknown oder IID_IMAPIProp) festgelegt werden. 
    
 _cbSpoolSecurity_
  
> [in] Ein Zeiger auf die Größe des im Parameter _LppbSpoolSecurity_ Überprüfungsdaten in Bytes. 
    
 _lpbSpoolSecurity_
  
> [in] Ein Zeiger auf einen Zeiger auf Überprüfungsdaten. Die **SpoolerLogon** -Methode verwendet diese Daten zur Anmeldung bei der MAPI-Warteschlange an den gleichen Speicher als dem Anbieter für anmelden zuvor für die Anmeldung mithilfe der [IMSProvider::Logon](imsprovider-logon.md) -Methode. 
    
 _lppMAPIError_
  
> [out] Ein Zeiger auf einen Zeiger auf das zurückgegebene [MAPIERROR](mapierror.md) Struktur, falls vorhanden, die Angaben zu Version, Komponente und Kontext für einen Fehler enthält. Der Parameter _LppMAPIError_ kann auf NULL festgelegt werden, wenn es keine **MAPIERROR** -Struktur ist zurückgegeben. 
    
 _lppMSLogon_
  
> [out] Ein Zeiger auf den Zeiger auf die Nachricht speichern Objekt für die MAPI anmelden anmelden.
    
 _lppMDB_
  
> [out] Ein Zeiger auf den Zeiger auf die Nachricht speichern-Objekt für die MAPI-Warteschlange und Clientanwendungen anmelden.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
MAPI_E_UNCONFIGURED 
  
> Das Profil enthält nicht ausreichend Informationen für die Anmeldung für die Durchführung. Wenn dieser Wert zurückgegeben wird, ruft MAPI der Nachricht Informationsdienst Nachricht Service Entry Point-Funktion.
    
MAPI_W_ERRORS_RETURNED 
  
> Der Aufruf war erfolgreich, aber der Nachricht Speicheranbieter hat Fehlerinformationen verfügbar. Wenn diese Warnung zurückgegeben wird, sollte der Anruf als erfolgreich verarbeitet. Verwenden Sie das Makro **HR_FAILED** , um für diese Warnung zu testen. Weitere Informationen finden Sie unter [Verwendung von Makros Fehlerbehandlung](using-macros-for-error-handling.md). Wenn Sie die Fehlerinformationen vom Anbieter erhalten möchten, rufen Sie die [IMAPISession::GetLastError](imapisession-getlasterror.md) -Methode. 
    
## <a name="remarks"></a>Bemerkungen

Die MAPI-Warteschlange Ruft die **IMSProvider::SpoolerLogon** -Methode zur Anmeldung bei einem Nachrichtenspeicher. Die MAPI-Warteschlange sollten das Nachricht Store-Objekt von der Nachricht Informationsdienst im _LppMDB_ -Parameter zurückgegeben werden, während und nach der Anmeldung verwenden. 
  
Aus Gründen der Konsistenz mit der [IMSProvider::Logon](imsprovider-logon.md) -Methode gibt der Anbieter auch ein Message Store Anmeldung-Objekt im Parameter _LppMSLogon_ zurück. Die Verwendung von das Store-Objekt und das Anmeldeobjekt sind für die Anmeldung üblichen Store identisch. So, dass die Objekte fungieren, als wären sie ein Objekt, das zwei Schnittstellen verfügbar macht sollte eine 1: 1-Beziehung zwischen der Anmeldung-Objekt und das Store-Objekt sein. Die zwei Objekte werden zusammen und freigegebenen zusammen erstellt. 
  
Speicheranbieter sollten intern kennzeichnen zurückgegebene Message Store-Objekts, um anzugeben, dass der Speicher von den MAPI-Warteschlange verwendet wird. Einige der Methoden für dieses Objekt Store Verhalten sich anders als für die Nachricht Clientanwendungen bereitgestellte Objekt speichern. Nachhaltiger Schutz von dieser internen Mark ist am häufigsten das Verhalten, das speziell für die MAPI-Warteschlange auslösen.
  
## <a name="see-also"></a>Siehe auch



[IMSProvider::Logon](imsprovider-logon.md)
  
[MAPIERROR](mapierror.md)
  
[IMSProvider : IUnknown](imsprovideriunknown.md)

