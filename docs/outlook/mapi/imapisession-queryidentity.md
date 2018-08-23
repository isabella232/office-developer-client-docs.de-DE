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
ms.openlocfilehash: 6b64653aa87ff7ac983409978a69f59148251d7d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583414"
---
# <a name="imapisessionqueryidentity"></a>IMAPISession::QueryIdentity

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Gibt die Eintrags-ID des Objekts, das die primäre Identität für die Sitzung bereitstellt.
  
```cpp
HRESULT QueryIdentity(
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID
);
```

## <a name="parameters"></a>Parameter

 _lpcbEntryID_
  
> [out] Ein Zeiger auf die Byteanzahl von in die Eintrags-ID auf den durch den Parameter _LppEntryID_ verwiesen. 
    
 _lppEntryID_
  
> [out] Ein Zeiger auf einen Zeiger auf die Eintrags-ID des Objekts, das die primäre Identität bereitstellt.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Die primäre Identität wurde erfolgreich zurückgegeben.
    
MAPI_W_NO_SERVICE 
  
> Der Aufruf war erfolgreich, es gibt aber keine primäre Identität für die Sitzung. Wenn diese Warnung zurückgegeben wird, sollte der Anruf als erfolgreich verarbeitet. Verwenden Sie das Makro **HR_FAILED** , um für diese Warnung zu testen. Weitere Informationen finden Sie unter [Verwendung von Makros Fehlerbehandlung](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IMAPISession::QueryIdentity** -Methode die primäre Identität für die aktuelle Sitzung abgerufen und gibt den Wert über den Parameter _LppEntryID_ zurück. Die primäre Identität ist ein Objekt, in der Regel ein messaging-Benutzer, die den Benutzer einer Sitzung darstellt.  _LppEntryID_ gibt die primäre Identität bei einem [IMailUser](imailuserimapiprop.md) -Objekt, das auch als-Eigenschaft [PidTagEntryID](pidtagentryid-canonical-property.md) gespeichert ist. Den Rückgabewert in _LppEntryID_ können Sie um ein **IMailUser** -Objekt mit [IMAPISession::OpenEntry](imapisession-openentry.md)zu öffnen.
  
Obwohl viele Dienstanbieter in mehrere Nachrichtendienste für die die primäre Identität für eine Sitzung bereitstellen können, kennzeichnet MAPI einen einzelnen-Dienstanbieter. Der Dienstanbieter, der die primäre Identität liefert setzt die folgenden Elemente:
  
- Das Flag STATUS_PRIMARY_IDENTITY in der Eigenschaft **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)).
    
- Die Eigenschaft **PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md)).
    
- Die Eigenschaft **PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md)).
    
- Die Eigenschaft **PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md)).
    
Zugehörigkeit der Dienstanbieter, der die primäre Identität liefert eine Message Service, legen Sie die anderen Dienstanbieter den Dienst auch die PR_IDENTITY-Eigenschaften. Diese Eigenschaften werden in der Sitzung Statustabelle veröffentlicht. 
  
Wenn möglich, gibt **QueryIdentity** den Wert für die **PR_IDENTITY_ENTRYID** -Eigenschaft aus der Statuszeile, die mit STATUS_PRIMARY_IDENTITY markiert. Wenn die **PR_IDENTITY_ENTRYID** -Eigenschaft der primäre Identitätszeile nicht vorhanden ist, gibt **QueryIdentity** eine einmaligen Eintrags-ID, die mit anderen Informationen aus dieser Zeile erstellte zurück. 
  
Wenn das Flag STATUS_PRIMARY_IDENTITY aller **PR_RESOURCE_FLAG** Spalten in der Tabelle "Status" nicht vorhanden ist, gibt **QueryIdentity** die erste Eintrags-ID, die es findet zurück. Wird keine entsprechenden Eintrags-ID zurückgegeben, **QueryIdentity** erfolgreich ausgeführt wird, mit der Warnung MAPI_W_NO_SERVICE und enthält Verweise _LppEntryID_ auf einen Eintrag hartcodierte-Bezeichner. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Sie können die [IMsgServiceAdmin::SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md) -Methode, um einer Message Service weisen Sie die Aufgabe angeben primären Identität der Sitzung aufrufen. 
  
Eine andere Möglichkeit, die primäre Identität abrufen, ist suchen die Tabelle "Status" für die Zeile mit den **PR_RESOURCE_FLAGS** Spalten auf STATUS_PRIMARY_IDENTITY festgelegt. Weitere Informationen zu dieser alternative Möglichkeit zum Abrufen von Identitätsinformationen finden Sie unter [Statustabelle und Status-Objekte](status-table-and-status-objects.md).
  
Wenn Sie mit dem Eintrag Bezeichner für die primäre von **QueryIdentity**zurückgegebene Identität fertig sind, freigeben Sie seine Speicher durch Aufrufen der Funktion [MAPIFreeBuffer](mapifreebuffer.md) . 
  
Weitere Informationen zu Identität im Allgemeinen finden Sie unter [Primäre MAPI-Identität](mapi-primary-identity.md). 
  
Weitere Informationen zum Abrufen von MAPI-Sitzung Identität finden Sie unter [Abrufen von primären und Identity Provider](retrieving-primary-and-provider-identity.md). 
  
## <a name="mfcmapi-reference"></a>MFCMAPI (engl.) (engl.)

Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MainDlg.cpp  <br/> |CMainDlg::OnQueryIdentity  <br/> |MFCMAPI (engl.) verwendet die **IMAPISession::QueryIdentity** -Methode, um den Adressbuch-Adresseintrag für die primäre Identität der Sitzung zu öffnen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPISession::OpenEntry](imapisession-openentry.md)
  
[IMsgServiceAdmin::SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPISession: IUnknown](imapisessioniunknown.md)


[MFCMAPI als ein Codebeispiel](mfcmapi-as-a-code-sample.md)
  
[Primäre MAPI-Identität](mapi-primary-identity.md)
  
[Abrufen der primären und Anbieteridentität](retrieving-primary-and-provider-identity.md)
  
[Verwenden von Makros zur Fehlerbehandlung](using-macros-for-error-handling.md)
  
[Statustabelle und Statusobjekte](status-table-and-status-objects.md)

