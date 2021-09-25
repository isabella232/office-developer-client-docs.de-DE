---
title: IMAPISessionQueryIdentity
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISession.QueryIdentity
api_type:
- COM
ms.assetid: a2cdda90-5457-49a7-b98c-7273ffe5cbbc
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 4d1bbe972f7b5a3223cc53a45aaefb08c85c8eb2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59584416"
---
# <a name="imapisessionqueryidentity"></a>IMAPISession::QueryIdentity

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt den Eintragsbezeichner des Objekts zurück, das die primäre Identität für die Sitzung bereitstellt.
  
```cpp
HRESULT QueryIdentity(
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID
);
```

## <a name="parameters"></a>Parameter

 _lpcbEntryID_
  
> [out] Ein Zeiger auf die Byteanzahl im Eintragsbezeichner, auf den der  _Parameter "lppEntryID"_ verweist. 
    
 _lppEntryID_
  
> [out] Ein Zeiger auf einen Zeiger auf den Eintragsbezeichner des Objekts, das die primäre Identität bereitstellt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die primäre Identität wurde erfolgreich zurückgegeben.
    
MAPI_W_NO_SERVICE 
  
> Der Aufruf war erfolgreich, aber es gibt keine primäre Identität für die Sitzung. Wenn diese Warnung zurückgegeben wird, sollte der Aufruf als erfolgreich behandelt werden. Verwenden Sie das Makro **HR_FAILED, um** diese Warnung zu testen. Weitere Informationen finden Sie unter [Verwenden von Makros für die Fehlerbehandlung.](using-macros-for-error-handling.md)
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IMAPISession::QueryIdentity-Methode** ruft die primäre Identität für die aktuelle Sitzung ab und gibt den Wert über den  _lppEntryID-Parameter_ zurück. Die primäre Identität ist ein Objekt, in der Regel ein Messagingbenutzer, das den Benutzer einer Sitzung darstellt.  _lppEntryID_ gibt die primäre Identität für ein [IMailUser-Objekt](imailuserimapiprop.md) zurück, das auch als [PidTagEntryID-Eigenschaft](pidtagentryid-canonical-property.md) gespeichert ist. You can use the value returned in  _lppEntryID_ to open an **IMailUser** object using [IMAPISession::OpenEntry](imapisession-openentry.md).
  
Obwohl viele Dienstanbieter in mehreren Nachrichtendiensten die primäre Identität für eine Sitzung bereitstellen können, bestimmt MAPI einen einzelnen Dienstanbieter. Der Dienstanbieter, der die primäre Identität bereitstellt, legt die folgenden Elemente fest:
  
- Das flag STATUS_PRIMARY_IDENTITY in der **Eigenschaft PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)).
    
- Die **PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md)) -Eigenschaft.
    
- Die **PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md)) -Eigenschaft.
    
- Die **PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md)) -Eigenschaft.
    
Wenn der Dienstanbieter, der die primäre Identität bereitstellt, zu einem Nachrichtendienst gehört, legen die anderen Dienstanbieter im Nachrichtendienst auch die PR_IDENTITY Eigenschaften fest. Diese Eigenschaften werden in der Statustabelle der Sitzung veröffentlicht. 
  
Wenn möglich, **gibt QueryIdentity** den Wert für die **PR_IDENTITY_ENTRYID-Eigenschaft** aus der Mit STATUS_PRIMARY_IDENTITY markierten Statuszeile zurück. Wenn die **PR_IDENTITY_ENTRYID** Eigenschaft in der primären Identitätszeile fehlt, gibt **QueryIdentity** einen einmaligen Eintragsbezeichner zurück, der mit anderen Informationen aus dieser Zeile erstellt wurde. 
  
Wenn das flag STATUS_PRIMARY_IDENTITY in allen **PR_RESOURCE_FLAG** Spalten in der Statustabelle fehlt, gibt **QueryIdentity** den ersten gefundenen Eintragsbezeichner zurück. Wenn kein geeigneter Eintragsbezeichner zurückgegeben werden kann, ist **QueryIdentity** erfolgreich mit der Warnung MAPI_W_NO_SERVICE und verweist  _lppEntryID_ auf einen hartcodierten Eintragsbezeichner. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Sie können die [IMsgServiceAdmin::SetPrimaryIdentity-Methode](imsgserviceadmin-setprimaryidentity.md) aufrufen, um einem Nachrichtendienst die Aufgabe zuzuweisen, die primäre Identität der Sitzung zu liefern. 
  
Eine weitere Möglichkeit zum Abrufen der primären Identität besteht darin, die Statustabelle nach der Zeile mit den **PR_RESOURCE_FLAGS** Spalten zu durchsuchen, die auf STATUS_PRIMARY_IDENTITY festgelegt sind. Weitere Informationen zu dieser alternativen Methode zum Abrufen von Identitätsinformationen finden Sie unter ["Statustabelle" und "Statusobjekte".](status-table-and-status-objects.md)
  
Wenn Sie mit der Verwendung des Eintragsbezeichners für die von **QueryIdentity** zurückgegebene primäre Identität fertig sind, geben Sie den Arbeitsspeicher frei, indem Sie die [MAPIFreeBuffer-Funktion](mapifreebuffer.md) aufrufen. 
  
Weitere Informationen zur Identität im Allgemeinen finden Sie unter [MAPI Primary Identity](mapi-primary-identity.md). 
  
Weitere Informationen zum Abrufen der MAPI-Sitzungsidentität finden Sie unter [Abrufen der primären und Anbieteridentität.](retrieving-primary-and-provider-identity.md) 
  
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
  
[Primäre MAPI-Identität](mapi-primary-identity.md)
  
[Abrufen der primären und der Anbieteridentität](retrieving-primary-and-provider-identity.md)
  
[Verwenden von Makros für die Fehlerbehandlung](using-macros-for-error-handling.md)
  
[StatusTabellen- und Statusobjekte](status-table-and-status-objects.md)

