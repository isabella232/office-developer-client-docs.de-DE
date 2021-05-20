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
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 794674df38266743cac8c947ec93dc1fcfff438b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430574"
---
# <a name="imsproviderspoolerlogon"></a>IMSProvider::SpoolerLogon

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Protokolliert den MAPI-Spooler bei einem Nachrichtenspeicher.
  
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
  
> [in] Ein Zeiger auf das MAPI-Unterstützungsobjekt für den Nachrichtenspeicher.
    
 _ulUIParam_
  
> [in] Ein Handle zum übergeordneten Fenster aller Dialogfelder oder Fenster, die diese Methode anzeigt. 
    
 _lpszProfileName_
  
> [in] Ein Zeiger auf eine Zeichenfolge, die den Namen des Profils enthält, das für die ANMELDUNG des MAPI-Spoolers verwendet wird. Diese Zeichenfolge kann in Dialogfelder angezeigt, in eine Protokolldatei geschrieben oder einfach ignoriert werden. Sie muss im Unicode-Format vorliegen, wenn MAPI_UNICODE im  _ulFlags-Parameter festgelegt_ ist. 
    
 _cbEntryID_
  
> [in] Die Größe des Eintragsbezeichners in Bytes, auf den der  _lpEntryID-Parameter_ verweist. 
    
 _lpEntryID_
  
> [in] Ein Zeiger auf die Eintrags-ID für den Nachrichtenspeicher. Das Übergeben von NULL im  _lpEntryID-Parameter_ gibt an, dass ein Nachrichtenspeicher noch nicht ausgewählt wurde und dass Dialogfelder angezeigt werden können, in denen der Benutzer einen Nachrichtenspeicher auswählen kann. 
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die steuert, wie die Anmeldung ausgeführt wird. Die folgenden Kennzeichen können festgelegt werden:
    
MAPI_DEFERRED_ERRORS 
  
> Der Aufruf kann auch dann erfolgreich sein, wenn das zugrunde liegende Objekt für die aufrufende Implementierung nicht verfügbar ist. Wenn das Objekt nicht verfügbar ist, kann ein nachfolgender Aufruf des Objekts einen Fehler zur Folge haben.
    
MAPI_UNICODE 
  
> Die übergebenen Zeichenfolgen sind im Unicode-Format. Wenn MAPI_UNICODE nicht festgelegt ist, werden die Zeichenfolgen im ANSI-Format angezeigt.
    
MDB_NO_DIALOG 
  
> Verhindert die Anzeige von Anmeldedialogfeldern. Wenn dieses Flag festgelegt ist, wird der Fehlerwert MAPI_E_LOGON_FAILED zurückgegeben, wenn die Anmeldung nicht erfolgreich ist. Wenn dieses Kennzeichen nicht festgelegt ist, kann der Nachrichtenspeicheranbieter den Benutzer zur Korrektur eines Namens oder Kennworts, zum Einfügen eines Datenträgers oder zum Ausführen anderer aktionen aufgefordert, die zum Herstellen einer Verbindung mit dem Speicher erforderlich sind.
    
MDB_WRITE 
  
> Fordert Lese-/Schreibberechtigungen an.
    
 _lpInterface_
  
> [in] Ein Zeiger auf die Schnittstellen-ID (Interface Identifier, IID), bei der sich der Nachrichtenspeicher anmelden soll. Das Übergeben von NULL gibt an, dass die MAPI-Schnittstelle für den Nachrichtenspeicher ([IMsgStore](imsgstoreimapiprop.md)) zurückgegeben wird. Der  _lpInterface-Parameter_ kann auch auf einen Bezeichner für eine geeignete Schnittstelle für den Nachrichtenspeicher festgelegt werden (z. B. IID_IUnknown oder IID_IMAPIProp). 
    
 _cbSpoolSecurity_
  
> [in] Ein Zeiger auf die Größe der Überprüfungsdaten im  _lppbSpoolSecurity-Parameter_ in Bytes. 
    
 _lpbSpoolSecurity_
  
> [in] Ein Zeiger auf einen Zeiger auf Validierungsdaten. Die **SpoolerLogon-Methode** verwendet diese Daten, um den MAPI-Spooler im selben Speicher wie der zuvor angemeldete Nachrichtenspeicheranbieter mit der [IMSProvider::Logon-Methode](imsprovider-logon.md) zu protokollieren. 
    
 _lppMAPIError_
  
> [out] Ein Zeiger auf einen Zeiger auf die zurückgegebene [MAPIERROR-Struktur,](mapierror.md) die Versions-, Komponenten- und Kontextinformationen für einen Fehler enthält. Der  _Parameter lppMAPIError_ kann auf NULL festgelegt werden, wenn keine **MAPIERROR-Struktur** zurückgegeben werden soll. 
    
 _lppMSLogon_
  
> [out] Ein Zeiger auf den Zeiger auf das Anmeldeobjekt des Nachrichtenspeichers, bei dem sich MAPI anmelden soll.
    
 _lppMDB_
  
> [out] Ein Zeiger auf den Zeiger auf das Nachrichtenspeicherobjekt, an dem sich der MAPI-Spooler und die Clientanwendungen anmelden können.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
MAPI_E_UNCONFIGURED 
  
> Das Profil enthält nicht genügend Informationen, damit die Anmeldung abgeschlossen werden kann. Wenn dieser Wert zurückgegeben wird, ruft MAPI die Einstiegspunktfunktion des Nachrichtenspeicheranbieters auf.
    
MAPI_W_ERRORS_RETURNED 
  
> Der Aufruf ist erfolgreich, der Nachrichtenspeicheranbieter verfügt jedoch über Fehlerinformationen. Wenn diese Warnung zurückgegeben wird, sollte der Anruf als erfolgreich behandelt werden. Verwenden Sie zum Testen dieser Warnung das **HR_FAILED** Makro. Weitere Informationen finden Sie unter [Using Macros for Error Handling](using-macros-for-error-handling.md). Rufen Sie die [IMAPISession::GetLastError-Methode](imapisession-getlasterror.md) auf, um die Fehlerinformationen vom Anbieter zu erhalten. 
    
## <a name="remarks"></a>Hinweise

Der MAPI-Spooler ruft die **IMSProvider::SpoolerLogon-Methode** auf, um sich bei einem Nachrichtenspeicher zu anmelden. Der MAPI-Spooler sollte das Nachrichtenspeicherobjekt verwenden, das vom Nachrichtenspeicheranbieter im  _lppMDB-Parameter_ während und nach der Anmeldung zurückgegeben wird. 
  
Zur Konsistenz mit der [IMSProvider::Logon-Methode](imsprovider-logon.md) gibt der Anbieter auch ein Anmeldeobjekt des Nachrichtenspeichers im  _lppMSLogon-Parameter_ zurück. Die Verwendung des Store-Objekts und des Anmeldeobjekts ist für die übliche Storeanmeldung identisch. Es sollte eine 1:1-Entsprechung zwischen dem Anmeldeobjekt und dem Storeobjekt sein, damit die Objekte so tun, als wären sie ein Objekt, das zwei Schnittstellen verfügbar macht. Die beiden Objekte werden zusammen erstellt und gemeinsam frei. 
  
Der Speicheranbieter sollte das zurückgegebene Nachrichtenspeicherobjekt intern markieren, um anzugeben, dass der Speicher vom MAPI-Spooler verwendet wird. Einige Methoden für dieses Speicherobjekt verhalten sich anders als für das Nachrichtenspeicherobjekt, das Clientanwendungen zur Verfügung gestellt wird. Das Behalten dieser internen Markierung ist die häufigste Methode, um das für den MAPI-Spooler spezifische Verhalten auszulösen.
  
## <a name="see-also"></a>Siehe auch



[IMSProvider::Logon](imsprovider-logon.md)
  
[MAPIERROR](mapierror.md)
  
[IMSProvider : IUnknown](imsprovideriunknown.md)

