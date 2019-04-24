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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 396320c6b39553da09aa1f45d0c755f40a939382
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335693"
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
  
> Out Ein Zeiger auf die Bytezahl in der Eintrags-ID, auf die durch den _lppEntryID_ -Parameter verwiesen wird. 
    
 _lppEntryID_
  
> Out Ein Zeiger auf einen Zeiger auf die Eintrags-ID des Objekts, das die primäre Identität bereitstellt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die primäre Identität wurde erfolgreich zurückgegeben.
    
MAPI_W_NO_SERVICE 
  
> Der Aufruf war erfolgreich, aber es gibt keine primäre Identität für die Sitzung. Wenn diese Warnung zurückgegeben wird, sollte der Anruf als erfolgreich behandelt werden. Verwenden Sie zum Testen dieser Warnung das **HR_FAILED** -Makro. Weitere Informationen finden Sie unter [Verwenden von Makros zur Fehlerbehandlung](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPISession:: QueryIdentity** -Methode ruft die primäre Identität für die aktuelle Sitzung ab und gibt den Wert über den _lppEntryID_ -Parameter zurück. Die primäre Identität ist ein Objekt, in der Regel ein Messagingbenutzer, der den Benutzer einer Sitzung darstellt.  _lppEntryID_ gibt die primäre Identität für ein [IMailUser](imailuserimapiprop.md) -Objekt zurück, das auch als [PidTagEntryID](pidtagentryid-canonical-property.md) -Eigenschaft gespeichert wird. Sie können den in _lppEntryID_ zurückgegebenen Wert verwenden, um ein **IMailUser** -Objekt mit [IMAPISession:: OpenEntry](imapisession-openentry.md)zu öffnen.
  
Obwohl viele Dienstanbieter in mehreren Nachrichtendiensten die primäre Identität für eine Sitzung bereitstellen können, benennt MAPI einen einzelnen Dienstanbieter. Der Dienstanbieter, der die primäre Identität bereitstellt, legt die folgenden Elemente fest:
  
- Das STATUS_PRIMARY_IDENTITY-Flag in der **PR_RESOURCE_FLAGS** ([pidtagresourceflags (](pidtagresourceflags-canonical-property.md))-Eigenschaft.
    
- Die **PR_IDENTITY_DISPLAY** ([pidtagidentitydisplay (](pidtagidentitydisplay-canonical-property.md))-Eigenschaft.
    
- Die **PR_IDENTITY_ENTRYID** ([pidtagidentityentryid (](pidtagidentityentryid-canonical-property.md))-Eigenschaft.
    
- Die **PR_IDENTITY_SEARCH_KEY** ([pidtagidentitysearchkey (](pidtagidentitysearchkey-canonical-property.md))-Eigenschaft.
    
Wenn der Dienstanbieter, der die primäre Identität bereitstellt, zu einem Nachrichtendienst gehört, legen die anderen Dienstanbieter im Nachrichtendienst auch die PR_IDENTITY-Eigenschaften fest. Diese Eigenschaften werden in der Statustabelle der Sitzung veröffentlicht. 
  
Wenn möglich, gibt **QueryIdentity** den Wert für die **PR_IDENTITY_ENTRYID** -Eigenschaft aus der Zeile Status mit STATUS_PRIMARY_IDENTITY. Wenn die **PR_IDENTITY_ENTRYID** -Eigenschaft in der primären Identitätszeile fehlt, gibt **QueryIdentity** einen einmaligen Eintragsbezeichner zurück, der mit anderen Informationen aus dieser Zeile erstellt wurde. 
  
Wenn das STATUS_PRIMARY_IDENTITY-Flag in allen **PR_RESOURCE_FLAG** -Spalten in der Status-Tabelle fehlt, gibt **QueryIdentity** den ersten gefundenen Eintragsbezeichner zurück. Wenn kein entsprechender Eingabe Bezeichner vorhanden ist, wird **QueryIdentity** mit der Warnung MAPI_W_NO_SERVICE und _lppEntryID_ auf eine hart codierte Eintrags-ID. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Sie können die [IMsgServiceAdmin:: SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md) -Methode aufrufen, um einem Nachrichtendienst die Aufgabe zuzuweisen, die primäre Identität der Sitzung anzugeben. 
  
Eine weitere Möglichkeit zum Abrufen der primären Identität besteht darin, die Statustabelle für die Zeile zu durchsuchen, wobei die **PR_RESOURCE_FLAGS** -Spalten auf STATUS_PRIMARY_IDENTITY festgelegt sind. Weitere Informationen zu diesem alternativen Verfahren zum Abrufen von Identitätsinformationen finden Sie unter [Status Table-und Status-Objekte](status-table-and-status-objects.md).
  
Wenn Sie die Eintrags-ID für die primäre von **QueryIdentity**zurückgegebene Identität nicht mehr verwenden möchten, müssen Sie den Speicher freigeben, indem Sie die [mapifreebufferfreigegeben](mapifreebuffer.md) -Funktion aufrufen. 
  
Weitere Informationen zur Identität im Allgemeinen finden Sie unter [MAPI Primary Identity](mapi-primary-identity.md). 
  
Weitere Informationen zum Abrufen der MAPI-Sitzungs Identität finden Sie unter [Abrufen der primären und Anbieter Identität](retrieving-primary-and-provider-identity.md). 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MainDlg. cpp  <br/> |CMainDlg:: OnQueryIdentity  <br/> |MFCMAPI verwendet die **IMAPISession:: QueryIdentity** -Methode, um den Adressbucheintrag für die primäre Identität der Sitzung zu öffnen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPISession::OpenEntry](imapisession-openentry.md)
  
[IMsgServiceAdmin::SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPISession : IUnknown](imapisessioniunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)
  
[Primäre MAPI-Identität](mapi-primary-identity.md)
  
[Abrufen der primären und Anbieter Identität](retrieving-primary-and-provider-identity.md)
  
[Verwenden von Makros zur Fehlerbehandlung](using-macros-for-error-handling.md)
  
[Statustabelle und Statusobjekte](status-table-and-status-objects.md)

