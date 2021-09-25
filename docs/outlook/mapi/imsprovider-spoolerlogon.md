---
title: IMSProviderSpoolerLogon
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMSProvider.SpoolerLogon
api_type:
- COM
ms.assetid: 79d5af23-efad-4013-a330-56babfb2bb0f
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 60148f32c89de365faa0b1eea66d930a2708a06e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59561453"
---
# <a name="imsproviderspoolerlogon"></a>IMSProvider::SpoolerLogon

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Protokolliert den MAPI-Spooler in einem Nachrichtenspeicher.
  
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
  
> [in] Ein Handle für das übergeordnete Fenster aller Dialogfelder oder Fenster, die von dieser Methode angezeigt werden. 
    
 _lpszProfileName_
  
> [in] Ein Zeiger auf eine Zeichenfolge, die den Namen des Profils enthält, das für die MAPI-Spooleranmeldung verwendet wird. Diese Zeichenfolge kann in Dialogfeldern angezeigt, in eine Protokolldatei geschrieben oder einfach ignoriert werden. Es muss im Unicode-Format vorliegen, wenn das MAPI_UNICODE-Flag im  _ulFlags-Parameter_ festgelegt ist. 
    
 _cbEntryID_
  
> [in] Die Größe (in Byte) des Eintragsbezeichners, auf den der  _parameter lpEntryID_ verweist. 
    
 _lpEntryID_
  
> [in] Ein Zeiger auf den Eintragsbezeichner für den Nachrichtenspeicher. Das Übergeben von NULL im  _lpEntryID-Parameter_ gibt an, dass noch kein Nachrichtenspeicher ausgewählt wurde und dass Dialogfelder, in denen der Benutzer einen Nachrichtenspeicher auswählen kann, angezeigt werden können. 
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die steuert, wie die Anmeldung durchgeführt wird. Die folgenden Flags können festgelegt werden:
    
MAPI_DEFERRED_ERRORS 
  
> Der Aufruf kann auch dann erfolgreich ausgeführt werden, wenn das zugrunde liegende Objekt für die aufrufende Implementierung nicht verfügbar ist. Wenn das Objekt nicht verfügbar ist, kann ein nachfolgender Aufruf des Objekts einen Fehler auslösen.
    
MAPI_UNICODE 
  
> Die übergebenen Zeichenfolgen haben das Unicode-Format. Wenn MAPI_UNICODE nicht festgelegt ist, haben die Zeichenfolgen das ANSI-Format.
    
MDB_NO_DIALOG 
  
> Verhindert die Anzeige von Anmeldedialogfeldern. Wenn dieses Kennzeichen festgelegt ist, wird der Fehlerwert MAPI_E_LOGON_FAILED zurückgegeben, wenn die Anmeldung nicht erfolgreich ist. Wenn dieses Kennzeichen nicht festgelegt ist, kann der Nachrichtenspeicheranbieter den Benutzer auffordern, einen Namen oder ein Kennwort zu korrigieren, einen Datenträger einzufügen oder andere Aktionen auszuführen, die zum Herstellen einer Verbindung mit dem Speicher erforderlich sind.
    
MDB_WRITE 
  
> Fordert Lese-/Schreibberechtigung an.
    
 _lpInterface_
  
> [in] Ein Zeiger auf den Schnittstellenbezeichner (IID), bei dem sich der Nachrichtenspeicher anmelden soll. Wenn NULL übergeben wird, wird die MAPI-Schnittstelle für den Nachrichtenspeicher ([IMsgStore](imsgstoreimapiprop.md)) zurückgegeben. Der  _lpInterface-Parameter_ kann auch auf einen Bezeichner für eine entsprechende Schnittstelle für den Nachrichtenspeicher festgelegt werden (z. B. IID_IUnknown oder IID_IMAPIProp). 
    
 _cbSpoolSecurity_
  
> [in] Ein Zeiger auf die Größe von Validierungsdaten im  _Parameter "lppbSpoolSecurity"_ in Bytes. 
    
 _lpbSpoolSecurity_
  
> [in] Ein Zeiger auf einen Zeiger auf Validierungsdaten. Die **SpoolerLogon-Methode** verwendet diese Daten, um den MAPI-Spooler im selben Speicher wie der Zuvor angemeldete Nachrichtenspeicheranbieter mithilfe der [IMSProvider::Logon-Methode](imsprovider-logon.md) zu protokollieren. 
    
 _lppMAPIError_
  
> [out] Ein Zeiger auf einen Zeiger auf die zurückgegebene [MAPIERROR-Struktur(](mapierror.md) falls vorhanden), die Versions-, Komponenten- und Kontextinformationen für einen Fehler enthält. Der  _lppMAPIError-Parameter_ kann auf NULL festgelegt werden, wenn keine **MAPIERROR-Struktur** zurückgegeben werden soll. 
    
 _lppMSLogon_
  
> [out] Ein Zeiger auf den Zeiger auf das Anmeldeobjekt des Nachrichtenspeichers, bei dem sich MAPI anmelden soll.
    
 _lppMDB_
  
> [out] Ein Zeiger auf den Zeiger auf das Nachrichtenspeicherobjekt für die MAPI-Spooler- und Clientanwendungen, bei denen sie sich anmelden möchten.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
MAPI_E_UNCONFIGURED 
  
> Das Profil enthält nicht genügend Informationen, damit die Anmeldung abgeschlossen werden kann. Wenn dieser Wert zurückgegeben wird, ruft MAPI die Nachrichtendienst-Einstiegspunktfunktion des Nachrichtenspeicheranbieters auf.
    
MAPI_W_ERRORS_RETURNED 
  
> Der Aufruf war erfolgreich, aber der Nachrichtenspeicheranbieter verfügt über Fehlerinformationen. Wenn diese Warnung zurückgegeben wird, sollte der Aufruf als erfolgreich behandelt werden. Verwenden Sie das Makro **HR_FAILED, um** diese Warnung zu testen. Weitere Informationen finden Sie unter [Verwenden von Makros für die Fehlerbehandlung.](using-macros-for-error-handling.md) Rufen Sie die [IMAPISession::GetLastError-Methode](imapisession-getlasterror.md) auf, um die Fehlerinformationen vom Anbieter abzurufen. 
    
## <a name="remarks"></a>HinwBemerkungeneise

Der MAPI-Spooler ruft die **IMSProvider::SpoolerLogon-Methode** auf, um sich bei einem Nachrichtenspeicher anzumelden. Der MAPI-Spooler sollte das Nachrichtenspeicherobjekt verwenden, das vom Nachrichtenspeicheranbieter im  _lppMDB-Parameter_ während und nach der Anmeldung zurückgegeben wird. 
  
Aus Gründen der Konsistenz mit der [IMSProvider::Logon-Methode](imsprovider-logon.md) gibt der Anbieter auch ein Anmeldeobjekt für den Nachrichtenspeicher im  _Parameter "lppMSLogon"_ zurück. Die Verwendung des Speicherobjekts und des Anmeldeobjekts ist bei der üblichen Store-Anmeldung identisch. Es sollte eine 1:1-Entsprechung zwischen dem Anmeldeobjekt und dem Speicherobjekt bestehen, sodass die Objekte so agieren, als wären sie ein Objekt, das zwei Schnittstellen verfügbar macht. Die beiden Objekte werden zusammen erstellt und freigegeben. 
  
Der Speicheranbieter sollte das zurückgegebene Nachrichtenspeicherobjekt intern markieren, um anzugeben, dass der Speicher vom MAPI-Spooler verwendet wird. Einige Der Methoden für dieses Speicherobjekt verhalten sich anders als für das Nachrichtenspeicherobjekt, das Clientanwendungen bereitgestellt wird. Das Beibehalten dieser internen Markierung ist die häufigste Möglichkeit, das für den MAPI-Spooler spezifische Verhalten auszulösen.
  
## <a name="see-also"></a>Siehe auch



[IMSProvider::Logon](imsprovider-logon.md)
  
[MAPIERROR](mapierror.md)
  
[IMSProvider : IUnknown](imsprovideriunknown.md)

