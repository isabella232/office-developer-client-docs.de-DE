---
title: IMAPISessionQueryIdentity
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.QueryIdentity
api_type:
- COM
ms.assetid: a2cdda90-5457-49a7-b98c-7273ffe5cbbc
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 396320c6b39553da09aa1f45d0c755f40a939382
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428221"
---
# <a name="imapisessionqueryidentity"></a>IMAPISession::QueryIdentity

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt den Eintragsbezeichner des Objekts zurück, das die primäre Identität für die Sitzung enthält.
  
```cpp
HRESULT QueryIdentity(
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID
);
```

## <a name="parameters"></a>Parameter

 _lpcbEntryID_
  
> [out] Ein Zeiger auf die Byteanzahl in der Eintrags-ID, auf die der  _lppEntryID-Parameter_ verweist. 
    
 _lppEntryID_
  
> [out] Ein Zeiger auf einen Zeiger auf die Eintrags-ID des Objekts, das die primäre Identität enthält.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die primäre Identität wurde erfolgreich zurückgegeben.
    
MAPI_W_NO_SERVICE 
  
> Der Aufruf ist erfolgreich, es gibt jedoch keine primäre Identität für die Sitzung. Wenn diese Warnung zurückgegeben wird, sollte der Anruf als erfolgreich behandelt werden. Verwenden Sie zum Testen dieser Warnung das **HR_FAILED** Makro. Weitere Informationen finden Sie unter [Using Macros for Error Handling](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Hinweise

Die **IMAPISession::QueryIdentity-Methode** ruft die primäre Identität für die aktuelle Sitzung ab und gibt den Wert über den  _lppEntryID-Parameter_ zurück. Die primäre Identität ist ein Objekt, in der Regel ein Messagingbenutzer, das den Benutzer einer Sitzung darstellt.  _lppEntryID_ gibt die primäre Identität für ein [IMailUser-Objekt](imailuserimapiprop.md) zurück, das auch als [PidTagEntryID-Eigenschaft gespeichert](pidtagentryid-canonical-property.md) wird. Sie können den in _lppEntryID zurückgegebenen_ Wert verwenden, um ein **IMailUser-Objekt** mithilfe von [IMAPISession::OpenEntry zu öffnen.](imapisession-openentry.md)
  
Obwohl viele Dienstanbieter in mehreren Nachrichtendiensten die primäre Identität für eine Sitzung bereitstellen können, bestimmt MAPI einen einzelnen Dienstanbieter. Der Dienstanbieter, der die primäre Identität liefert, legt die folgenden Elemente fest:
  
- Das STATUS_PRIMARY_IDENTITY in der **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) -Eigenschaft.
    
- Die **PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md)) -Eigenschaft.
    
- Die **PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md)) -Eigenschaft.
    
- Die **PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md)) -Eigenschaft.
    
Wenn der Dienstanbieter, der die primäre Identität liefert, zu einem Nachrichtendienst gehört, legen die anderen Dienstanbieter im Nachrichtendienst auch die eigenschaften PR_IDENTITY fest. Diese Eigenschaften werden in der Statustabelle der Sitzung veröffentlicht. 
  
Wenn möglich, **gibt QueryIdentity** den Wert für **die PR_IDENTITY_ENTRYID-Eigenschaft** aus der Statuszeile zurück, die mit STATUS_PRIMARY_IDENTITY. Wenn die **PR_IDENTITY_ENTRYID** in der primären Identitätszeile fehlt, gibt **QueryIdentity** einen einmal vorhandenen Eintragsbezeichner zurück, der mit anderen Informationen aus dieser Zeile erstellt wurde. 
  
Wenn das STATUS_PRIMARY_IDENTITY in allen spalten  PR_RESOURCE_FLAG in der Statustabelle fehlt, gibt **QueryIdentity** den ersten Eintragsbezeichner zurück, den es findet. Wenn keine geeignete Eintrags-ID zurückgegeben werden soll, ist **QueryIdentity** mit der Warnung MAPI_W_NO_SERVICE erfolgreich und verweist  _lppEntryID_ auf einen hart codierten Eintragsbezeichner. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Sie können die [IMsgServiceAdmin::SetPrimaryIdentity-Methode](imsgserviceadmin-setprimaryidentity.md) aufrufen, um einem Nachrichtendienst die Aufgabe zu zuweisen, die primäre Identität der Sitzung zu liefern. 
  
Eine weitere Möglichkeit zum Abrufen der primären Identität besteht in der Suche nach der Statustabelle für die Zeile, PR_RESOURCE_FLAGS **spalten** auf STATUS_PRIMARY_IDENTITY. Weitere Informationen zu dieser alternativen Methode zum Abrufen von Identitätsinformationen finden Sie unter [Status Table und Status Objects](status-table-and-status-objects.md).
  
Wenn Sie den Eintragsbezeichner für die von **QueryIdentity** zurückgegebene primäre Identität verwenden, geben Sie den Arbeitsspeicher frei, indem Sie die [MAPIFreeBuffer-Funktion](mapifreebuffer.md) aufrufen. 
  
Weitere Informationen zur Identität im Allgemeinen finden Sie unter [MAPI Primary Identity](mapi-primary-identity.md). 
  
Weitere Informationen zum Abrufen der MAPI-Sitzungsidentität finden Sie unter [Retrieving Primary and Provider Identity](retrieving-primary-and-provider-identity.md). 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MainDlg.cpp  <br/> |CMainDlg::OnQueryIdentity  <br/> |MFCMAPI verwendet die **IMAPISession::QueryIdentity-Methode,** um den Adressbucheintrag für die primäre Identität der Sitzung zu öffnen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPISession::OpenEntry](imapisession-openentry.md)
  
[IMsgServiceAdmin::SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPISession : IUnknown](imapisessioniunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)
  
[PRIMÄRE MAPI-Identität](mapi-primary-identity.md)
  
[Abrufen der primären und Anbieteridentität](retrieving-primary-and-provider-identity.md)
  
[Verwenden von Makros für die Fehlerbehandlung](using-macros-for-error-handling.md)
  
[Statustabelle und Statusobjekte](status-table-and-status-objects.md)

