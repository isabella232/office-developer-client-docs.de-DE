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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309737"
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
  
> in Ein Zeiger auf das MAPI-Unterstützungsobjekt für den Nachrichtenspeicher.
    
 _ulUIParam_
  
> in Ein Handle für das übergeordnete Fenster aller Dialogfelder oder Fenster, die diese Methode anzeigt. 
    
 _lpszProfileName_
  
> in Ein Zeiger auf eine Zeichenfolge, die den Namen des Profils enthält, das für die MAPI-Spooler-Anmeldung verwendet wird. Diese Zeichenfolge kann in Dialogfeldern angezeigt werden, in eine Protokolldatei geschrieben oder einfach ignoriert werden. Sie muss im Unicode-Format vorliegen, wenn das MAPI_UNICODE-Flag im _ulFlags_ -Parameter festgelegt ist. 
    
 _cbEntryID_
  
> in Die Größe der Eintrags-ID, auf die durch den _lpEntryID_ -Parameter verwiesen wird, in Bytes. 
    
 _lpEntryID_
  
> in Ein Zeiger auf die Eintrags-ID für den Nachrichtenspeicher. Das übergeben von NULL im Parameter _lpEntryID_ gibt an, dass noch kein Nachrichtenspeicher ausgewählt wurde und dass Dialogfelder, in denen der Benutzer einen Nachrichtenspeicher auswählen kann, angezeigt werden können. 
    
 _ulFlags_
  
> in Eine Bitmaske von Flags, die die Ausführung der Anmeldung steuert. Die folgenden Flags können festgelegt werden:
    
MAPI_DEFERRED_ERRORS 
  
> Der Aufruf kann auch dann erfolgreich ausgeführt werden, wenn das zugrunde liegende Objekt für die aufrufende Implementierung nicht verfügbar ist. Wenn das Objekt nicht verfügbar ist, kann bei einem nachfolgenden Aufruf des Objekts ein Fehler ausgelöst werden.
    
MAPI_UNICODE 
  
> Die übergebenen Zeichenfolgen sind im Unicode-Format. Wenn MAPI_UNICODE nicht festgelegt ist, werden die Zeichenfolgen im ANSI-Format.
    
MDB_NO_DIALOG 
  
> Verhindert die Anzeige von Anmelde Dialogfeldern. Wenn dieses Flag festgelegt ist, wird der Fehlerwert MAPI_E_LOGON_FAILED zurückgegeben, wenn die Anmeldung nicht erfolgreich ist. Wenn dieses Flag nicht festgelegt ist, kann der Nachrichtenspeicher Anbieter den Benutzer auffordern, einen Namen oder ein Kennwort zu korrigieren, einen Datenträger einzufügen oder andere erforderliche Aktionen auszuführen, um eine Verbindung mit dem Speicher herzustellen.
    
MDB_WRITE 
  
> Fordert Lese-/Schreibzugriff-Berechtigung an.
    
 _lpInterface_
  
> in Ein Zeiger auf die Schnittstellen-ID (IID) für den Nachrichtenspeicher, an dem sich die Anmeldung anmeldet. Übergeben von NULL gibt an, dass die MAPI-Schnittstelle für den Nachrichtenspeicher ([IMsgStore](imsgstoreimapiprop.md)) zurückgegeben wird. Der _lpInterface_ -Parameter kann auch auf einen Bezeichner für eine entsprechende Schnittstelle für den Nachrichtenspeicher festgelegt werden (beispielsweise IID_IUnknown oder IID_IMAPIProp). 
    
 _cbSpoolSecurity_
  
> in Ein Zeiger auf die Größe der Validierungsdaten im _lppbSpoolSecurity_ -Parameter in Byte. 
    
 _lpbSpoolSecurity_
  
> in Ein Zeiger auf einen Zeiger auf Validierungsdaten. Die **SpoolerLogon** -Methode verwendet diese Daten, um den MAPI-Spooler in demselben Speicher wie der zuvor angemeldete Nachrichtenspeicher Anbieter mithilfe der [IMSProvider:: Login](imsprovider-logon.md) -Methode zu protokollieren. 
    
 _lppMAPIError_
  
> Out Ein Zeiger auf einen Zeiger auf die zurückgegebene [MAPIERROR](mapierror.md) -Struktur, die Versions-, Komponenten-und Kontextinformationen für einen Fehler enthält. Der _lppMAPIError_ -Parameter kann auf NULL festgelegt werden, wenn keine **MAPIERROR** -Struktur zurückgegeben werden soll. 
    
 _lppMSLogon_
  
> Out Ein Zeiger auf den Zeiger auf das Nachrichtenspeicher-Anmeldeobjekt für die Anmeldung bei MAPI.
    
 _lppMDB_
  
> Out Ein Zeiger auf den Zeiger auf das Nachrichtenspeicherobjekt für die MAPI-Spooler und Clientanwendungen, die sich bei anmelden.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
MAPI_E_UNCONFIGURED 
  
> Das Profil enthält nicht genügend Informationen, damit die Anmeldung abgeschlossen werden kann. Wenn dieser Wert zurückgegeben wird, ruft MAPI die Nachrichtendienst-Einstiegspunktfunktion des Nachrichtenspeicher Anbieters auf.
    
MAPI_W_ERRORS_RETURNED 
  
> Der Aufruf war erfolgreich, aber der Nachrichtenspeicher Anbieter hat Fehlerinformationen. Wenn diese Warnung zurückgegeben wird, sollte der Anruf als erfolgreich behandelt werden. Verwenden Sie zum Testen dieser Warnung das **HR_FAILED** -Makro. Weitere Informationen finden Sie unter [Verwenden von Makros zur Fehlerbehandlung](using-macros-for-error-handling.md). Rufen Sie die [IMAPISession:: getlasterroraufzurufen](imapisession-getlasterror.md) -Methode auf, um die Fehlerinformationen vom Anbieter abzurufen. 
    
## <a name="remarks"></a>Bemerkungen

Der MAPI-Spooler Ruft die **IMSProvider:: SpoolerLogon** -Methode auf, um sich bei einem Nachrichtenspeicher anzumelden. Der MAPI-Spooler sollte das vom Nachrichtenspeicher Anbieter zurückgegebene Nachrichtenspeicherobjekt während und nach der Anmeldung im Parameter _lppMDB_ verwenden. 
  
Aus Gründen der Konsistenz mit der [IMSProvider:: Login](imsprovider-logon.md) -Methode gibt der Anbieter auch ein Anmeldeobjekt für den Nachrichtenspeicher im Parameter _lppMSLogon_ zurück. Die Verwendung des Store-Objekts und des LOGON-Objekts sind für die übliche Speicher Anmeldung identisch. Es sollte eine 1:1-Entsprechung zwischen dem Logon-Objekt und dem Store-Objekt vorhanden sein, sodass die Objekte so handeln, als ob es sich um ein Objekt handelt, das zwei Schnittstellen verfügbar macht. Die beiden Objekte werden zusammen erstellt und gemeinsam freigegeben. 
  
Der Informationsspeicher Anbieter sollte das zurückgegebene Nachrichtenspeicherobjekt intern kennzeichnen, um anzugeben, dass der Speicher vom MAPI-Spooler verwendet wird. Einige der Methoden für dieses Store-Objekt verhalten sich anders als für das Nachrichtenspeicherobjekt, das für Clientanwendungen bereitgestellt wird. Diese interne Markierung beizubehalten, ist die häufigste Methode zum Auslösen des Verhaltens, das für den MAPI-Spooler spezifisch ist.
  
## <a name="see-also"></a>Siehe auch



[IMSProvider::Logon](imsprovider-logon.md)
  
[MAPIERROR](mapierror.md)
  
[IMSProvider : IUnknown](imsprovideriunknown.md)

